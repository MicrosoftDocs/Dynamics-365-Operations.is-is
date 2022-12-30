---
title: Vinna úr leiðbeiningaramma
description: Þessi grein veitir upplýsingar um leiðbeiningaramma úrvinnslu fyrir þróunaraðila sem eru að stækka vöruhúsaferli fartækis í X++.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e88f32e0347a808d03615cf85e50b1592d691670
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860436"
---
# <a name="process-guide-framework"></a>Vinna úr leiðbeiningaramma

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um leiðbeiningaramma úrvinnslu fyrir þróunaraðila sem eru að stækka vöruhúsaferli fartækis í X++. Vöruhúsaferli fartækis eru stækkanleg vegna þess að ferlarnir eru hlutaðir niður í smærri skref. Smíði viðskiptagrunns og notandaviðmóts fyrir hvert skref hefur verið komið fyrir í stökum klösum, sem gerir stækkunarhæfni mögulega.

## <a name="overview-of-the-existing-design"></a>Yfirlit yfir fyrirliggjandi hönnun

Flæði vöruhúsaaðgerða í fartæki er sýnt í einni sérsniðinni endastöð þjónustu. Beiðnin kemur frá fartækjaforritinu sem XML-strengur, sem inniheldur lýsigögn notandaviðmótsins sem sýnt er í fartækjaforritinu, ásamt gildinum sem notandinn færði inn.

Þegar beiðnin er móttekin er fyrsta skrefið að afraða þessu XML. **WHSMobileAppServiceXMLTranslator** klasinn umbreytir XML í geymslu sem inniheldur bæði upplýsingar um stýringu og lotu.

Í framhaldinu eru upplýsingarnar í geymslunni notaðar til að fá úr því skorið hvaða vöruhúsaferli notandinn er að vinna í eða að fara að vinna í (sýnt með upptalningunni **WHSWorkExecuteMode**) og í samræmi við það að eintaka afleiddan klasa af **WHSWorkExecuteDisplay**. Aðferðin **displayform()** er kölluð fram, sem gerir þá eftirfarandi:

-   Vinnur úr gögnunum frá notandanum (úthlutað á klasann **WHSRFControlData**, en sumir ferlar innleiða tiltekin rök með því að hnekkja aðferðinni **processControl()**).

-   Keyrir viðskiptagrunn.

-   Stækkar skrefið.

-   Smíðar hólfið sem sýnir nýja notandaviðmótið (yfirleitt í **build...()** aðferð).

Hólfinu er síðan skilað til þýðandans, sem þá raðar XML og sendir það til baka sem svar til fartækisins.

Eftirfarandi myndaröð sýnir yfirlit yfir flæði framkvæmdar. Athugaðu að skýringarmyndin er meira til útskýringar en er ekki 1:1 framsetning á raunverulegum kóða.

![Yfirlit yfir ferlið í megindráttum.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Ástæða endurhönnunar

Ofangreind hönnun býður upp á mjög einfaldan ramma til að smíða ferla sem notaðir eru í flæði fartækis. Eins og kemur fram hér að ofan bera aðferðirnar **displayform()** hinsvegar ábyrgð á mörgu. Hún úthlutar þeim á aðrar aðferðir og klasa, en án ábyrgðar raunverulegs klasa er úthlutunin gerð á ósamræmdan hátt þvert yfir klasa. Einnig geta sumir klasarnir orðið nokkuð flóknir eftir því sem fjöldi studdra aðstæðna vex af sjálfu sér. Til að gera málin áhugaverðari eru sumir þessara klasa/aðferða hnekkt og endurnotuð á marga vegu. Niðurstaðan er afar langar aðferðir með háu flækjustigi. Viðhaldsvandamál hafa komið upp áður vegna þessa. Að laga villur í þessum aðferðum hefur reynst áhættusamt og getur gert illt verra.
Til dæmis er vísa margir ferlar í aðferðina **processWorkLine()** í klasanum **WhsWorkExecuteDisplay** (í raun hvar sem framkvæmd vinnu er gerð).

Til að gera þetta stækkunarhæft er ein leið að skipta aðferðum **displayForm** niður í smærri aðferðir og koma með punkta stækkunarhæfni. Hinsvegar vegna aðstæðufylkis gæti það reynst krefjandi fyrir samstarfsaðila að skrifa viðbætur og sannprófa gagnvart afturför. Ekki aðeins það, vegna skorts á skipulagðri ábyrgðardreifingu sem greint er frá hér að ofan, myndi kóðinn halda áfram að vaxa á ófyrirsjáanlegan hátt með tímanum, sem felur í sér áskoranir við að byggja upp gæðaviðbætur.

Þar af leiðandi er endurhönnunin sjálfbærasti kosturinn, þar sem markmiðið er að hafa skýrt skilgreinda klasa sem bera sjálfstæða ábyrgð. Klasi á að bera eina ábyrgð, eina ástæðu til að breyta og eina ástæðu til að stækka.

## <a name="design-overview"></a>Yfirlit hönnunar

Í endurhannaða rammanum snýst meginstefnan um tvær meginreglur: að skipta framkvæmdaflæðinu í einstaka þætti með vel skilgreindri ábyrgð og hafa vel skilgreinda stækkunarpunkta í hverjum þáttanna.

Heiti nýja rammans er „ProcessGuide“. Það er vegna þess að markmið þessara klasa er að leiðbeina notanda í gegnum viðskiptaferli (í stað þess að nota þungbiðlara sem upplifun í formi skjámyndar þar sem notandinn hefur meiri sveigjanleika í samskiptum við gögnin eða í hvaða röð hann sinnir verkefnum).

> [!NOTE]
> Eitt athyglisvert smáatriði er að forskeytinu „WHS“ er sleppt viljandi. Þó að ferlar fartækis hafi í upphafi verið innleiddir fyrir vöruhúsavinnu hafa þeir síðan farið yfir þau mörk til að styðja við ýmis framleiðslu- og birgðastjórnunarferli. Þar af leiðandi var tilvísun vöruhúss undanskilin í heiti rammans.

Til að bera kennsl á þættina er fyrsta skrefið að skoða upphafsferli framleiðslu (klasann **WhsWorkExecuteDisplayProdStart**). Hér er skýringarmynd af ferlinu.

![Skýringarmynd af ferlinu.](media/production-start-process-schematic.png)

Þegar horft er á stýriflæðið er þörf á eftirfarandi þáttum:

-   Stýring til að ná í gegnum allt viðskiptaferlið.
-   Skref sem ber ábyrgð á framkvæmd skrefs í ferlinu.
-   Gagnaúrvinnsla fyrir úrvinnslu gagna í skrefi.
-   Síðuhönnuður sem ber ábyrgð á hönnun notandaviðmótsins fyrir skref.
-   Flettari sem ber ábyrgð á skrefabreytingum.
-   Klasi sem ber ábyrgð á framkvæmd viðskiptaferlisins.

Í skýringarmynd vinnsluflæðis hér að ofan, ef þú byrjar á skrefi 1 og byrjar úrvinnslu gagna úr fyrra skrefinu og endar svo á að búa til notendaviðmót, mun úrvinnsla gagna halda áfram í næsta skrefi. Þetta kynnir sterka tengingu milli samhangandi skrefa og myndi nýja hástigs skemað okkar lítu svona út:

![Mynd af skematísku ferli á háu stigi.](media/high-level-schematic.png)

Eftirfarandi eru lykilþættir í endurhannaða ferlinu:

-   **ProcessGuideController** - Þessi klasi stýrir heildarframkvæmd viðskiptaferlisins. Hann skilgreinir verksmiðjurnar sem eintaka skrefið og flettarann, sem síðan myndi standa fyrir framkvæmdaferlið, sem og hreinsunarrökin fyrir því að afturkalla eða hætta við ferlið.

-   **ProcessGuideStep** - Þessi klasi táknar eitt skref í viðskiptaferlinu. Þessi klasi inniheldur skilgreiningu á verksmiðjum sem eintaka síðuhönnuð, aðgerðir og gagnavinnslu og sér um að kalla þær fram í réttri röð.

-   **ProcessGuideNavigationAgent** - Þessi klasi sér um flettingu milli skrefa. Þegar skrefi er lokið sér flettarinn um að skilgreina næsta skref og fer yfir allar færibreytur sem fyrra skrefið gæti þurft að senda til þess næsta.

-   **ProcessGuidePageBuilder** - Þessi klasi sér um eintaka notandaviðmótið.

-   **ProcessGuideAction** - Þessi klasi stendur fyrir aðgerð sem notandinn sér sem hnapp.

-   **ProcessGuideDataProcessor** - Þessi klasi sér um úrvinnslu á innslegnum gögnum notanda í reit.

## <a name="execution-flow"></a>Framkvæmdaflæði

Upphafsstaður framkvæmdaflæðis er óbreyttur. Beiðnin kemur því enn í gegnum sömu endastöðvarnar, fylgt eftir með afröðun XML í hólfið. Þetta hólf er síðan flutt í **getNextFormState()**.

Þrjá mikilvæga klasa skal hafa í huga:

-  **ProcessGuideSessionState** – Þetta inniheldur upplýsingar um lotustöðu – stillingu, áfram, stýringu og skref sem eru framkvæmd og svo framvegis.

-  **ProcessGuidePage** – Þetta inniheldur rammtagskipta framsetningu á lýsigögnum notandaviðmótsins.

-  **ProcessGuideRequest** – Þetta inniheldur tvennt ofangreint sem meðlimi og er rammtagskipt framsetning á móttekinni beiðni úr fartækinu.

Þessir klasar eru búnir til með því að nota upplýsingar um hólf (bæði stöðu og stýrigögn sem notandi slær inn). Þetta gefur örugga leið til að fá aðgang að og stjórna gildunum. Í samanburði við endurtekinn aðgang að hólfinu meðan á ferlinu stendur, veitir þetta ávinning bæði hvað varðar læsileika og frammistöðu.

Upplýsingar um lotustöðu eru notaðar til að eintaka réttan **ProcessGuideController** klasa. Þegar búið er að eintaka verður kallað á aðferðina **createResponse()** í klasanum **ProcessGuideController**. Þessi aðferð er aðgangsstaður fyrir rök leiðbeiningarúrvinnslu og eftir framkvæmd kemur hún til baka með svarið (sýnt í klasanum **ProcessGuideResponse**). Svarinu er síðan umbreytt aftur í hólfið og sent aftur í eldri rökin, sem þá raðar því í XML og sendir svarið til baka í fartækið.

Næst þarf stjórneiningin að finna næsta skref til að framkvæma. Ef þetta er upphaf nýs ferlis mun stjórneiningin kalla á **initialStep()** til að sækja fyrsta skrefið í ferlinu. Eftir það myndi hún kalla á aðferðina **execute()** í **ProcessGuideStep**. Þessi aðferð myndi síðan eintaka klasann **ProcessGuidePageBuilder** og kalla á **buildPage()** sem myndi þá skila hlutnum **ProcessGuidePage**, sem er sýndarframsetning notandaviðmótsins sem notandinn á að sjá. Næsta skref myndi síðan senda niðurstöðuna aftur til stýringarinnar, sem myndi þá vista núverandi lotustöðu og síðan skila niðurstöðunni aftur til **getNextFormState()** í skjámynd klasans **ProcessGuideResponse**. Eftir það er svarinu umbreytt aftur í hólfið og síðan raðað í XML og svarið sent til baka í fartækið.

Eftirfarandi myndaröð útskýrir þetta stýriflæði. Athugið að þetta er algengasta stýriflæðingin, einfölduð til að útskýra hönnunina.

![Stýriflæði einfaldað.](media/control-flow.png)

Þegar notandinn gerir aðgerð í fartækinu með því að smella á hnapp (eða skanna gildi – sem yfirleitt ræsir sjálfgefna aðgerð) – kemur beiðnin til aðferðarinnar **createResponse()** í klasanum **ProcessGuideController** í gegnum sömu leiðina. Í þetta sinn veit stýringin hins vegar frá upplýsingum um lotustöðuna í hvaða skrefi notandinn er. Í samræmi við það eintekur hún viðeigandi **ProcessGuideStep** klasa og ræsir úrvinnsluaðferðina. **ProcessGuideStep** les þá heiti aðgerðar sem notandinn kallaði á og eintekur síðan viðeigandi **ProcessGuideAction** klasa og kallar á **execute()**.

Klasinn **ProcessGuideAction** sér um að framkvæma tiltekna aðgerð, en hinsvegar eru tvær undantekningar sem vert er að minnast á.

Sú fyrri er klasinn **ProcessGuideOKAction**. Þessi aðgerð gefur til kynna að notandinn vilji staðfesta og halda áfram í ferlinu. Í samræmi við það – þessi aðferð svara í raun klasanum ProcessGuideStep, sem þýðir að skrefið ræsir **processData()** í **ProcessGuideDataProcessor**. Þetta vinnur úr gögnunum sem notandinn hefur slegið inn og uppfærir síðan stöðu skrefsins og sendir niðurstöðuna aftur til stýringarinnar. Það fer eftir niðurstöðu úrvinnslunnar hvort skrefið kallar fram síðuhönnuð til að hanna viðeigandi notandaviðmót eða setur stöðu skrefsins sem lokið. Þetta kemur fram í efri helmingi myndaraðar fyrir neðan.

Hin undantekningin er afturköllunaraðgerðin, sem er innleidd í klösunum **ProcessGuideCancelResetProcessAction** og **ProcessGuideCancelExitProcessAction**. Þessar aðgerðir tákna ásetning um að hætta við ferlið og fara aftur annaðhvort í upphaf ferlisins eða hætta ferlinu alveg. Svipað og í aðgerðinni **Í lagi** framkvæma þessar aðgerðir svar til skrefsins, sem kemur ásetningnum áleiðis til **ProcessGuideController**. Stýringin framkvæmir síðan nauðsynlega hreinsun á færibreytum stöðu og annaðhvort flytur stjórnun til fyrsta skrefsins í ferlinu eða hættir ferlinu.

Eftir að skrefinu er lokið, ef staða skrefsins er stillt á **Lokið**, þá eintekur stýringin **ProcessGuideNavigationAgent**, sem skilar heiti næsta skrefs. Stýringin eintekur þá þetta skref og kallar fram aðferðina **execute()** – og ferlið heldur áfram. Algengast er að nýja skrefið kalli fram samsvarandi **ProcessGuidePageBuilder** til að hanna notendaviðmótið fyrir næsta skjá sem á að sýna notandanu, sem er síðan sent til baka. Þetta flæði er sýnt á neðri hluta myndaraðarinnar hér að neðan.

![myndaröð.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Að búa til nýtt ferli með ramma ProcessGuide

Besta leiðin til að útskýra stýriflæðið er með því að nota dæmi sem er til í forritinu – Upphafsferli framleiðslu.

## <a name="overview-of-the-production-start-process"></a>Yfirlit yfir upphafsferli framleiðslunnar

Byrjum á því að skilja hvað vinnsluflæðið er. Í fyrsta skrefi er notandinn beðinn um auðkenni framleiðslupöntunar.

![Spyrja um framleiðslukenni.](media/production-id-prompt.png)

Þegar notandi færir inn auðkenni framleiðslupöntunar er pöntunarnúmerið staðfest. Sumar auðkenningarnar sem eru keyrðar byggja á því hvort pöntunin sé í sama vöruhúsinu og notandinn er skráður inn á og stöðu pöntunarinnar. Ef auðkenning mistekst fær notandinn upp villuboð. Ef auðkenning tekst fær notandinn að sjá upplýsingar um framleiðslupöntun og vöru.

Notandinn getur annaðhvort hætt við til að fara aftur í upphaf ferlisins eða smellt á **Í lagi** til að staðfesta. Í seinna tilvikinu er framleiðslupöntunin stillt á stöðuna **Hafið** eru samsvarandi færslubækur bókaðar, stýringin fer aftur í fyrsta skrefið og skilaboðin „Vinnu lokið“ eru sýnd notanda.


## <a name="creating-the-controller"></a>Stýring búin til

Fyrsta skrefið í að búa til viðskiptaferlið er að búa til stýrklasa út frá abstrakt klasanum **ProcessGuideController** sem innleiðir sjálfgefna hegðun stýringar. Nýja klasaheitið er **ProdProcessGuideProductionStartController** og skreytt með gildinu **WHSWorkExecuteMode** fyrir **StartProdOrder**. Sama eintaka **SysExtension** og var notuð í klösunum **WHSWorkExecuteDisplay** er notuð, sem hjálpar til við að eintaka stýringuna þegar notandinn framkvæmir valmyndaratriði fyrir þessa stillingu.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Nafngiftarmynstur klasans er **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Þetta er mynstrið sem er notað fyrir stýriklasana og til að ná til annarra klasa.


## <a name="building-the-first-step"></a>Fyrsta skrefið búið til

Næst, til að skilgreina fyrsta skrefið sem þú býrð til klasann **ProdProcessGuidePromptProductionIdStep**, sem nær frá **ProcessGuideStep**.

Verkið við að eintaka klasann er úthlutað á skrefasmiðju, sem grunnklasinn **ProcessGuideController** kallar fram. Sjálfgefin innleiðing smiðjunnar eintekur skrefið eftir heiti. Til að eintaka **ProdProcessGuidePromptProductionIdStep** sem fyrsta skrefið í stýringunni þarf því fyrst að gera tvennt:

-   Skreyta klasann **ProdProcessGuidePromptProductionIdStep** með eigind **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Í stýriklasanum skal innleiða abstrak aðferðina **initialStepName()** til að skila heiti skrefsins.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Gildið í eigindinni **ProcessGuideStepName** þarf ekki að passa nákvæmlega við klasaheitið eins og sýnt er hér að ofan. Með því að innleiða hana er þó hægt að ná fram samkvæmni og öryggi í kringum millitilvísanir þegar klasinn er notaður. Mælt er með að nota þessa nafnareglu.
>
> Eintaka skrefsins sem byggir á **ProcessGuideStepName** er innleidd í klasanum **ProcessGuideStepDefaultFactory**. Í sjaldgæfum tilfellum þar sem þú vilt aðra leið til að eintaka skrefið þarftu að gera eftirfarandi:
> -   Búðu til klasasmiðju sem erfir frá **ProcessGuidStepAbstractFactory**.
> -   Valfrjálst er að búa til nýjan færibreytuklasa sem innleiðir viðmótið **ProcessGuideIStepCreationParameters**, sem inniheldur færibreyturnar sem smiðjan þyrfti á að halda.
> -   Í stýriklasanum skal hnekka aðferðunum **stepFactory()** og **stepCreationParameters()** til að skila ofangreindri smiðju og færibreytum.

Næsta skref er að innleiða virkni klasans **ProdProcessGuidePromptProductionIdStep**. Þú þarft að innleiða rökin til að hanna notendaviðmótið, vinna úr gögnum sem notandi slær inn og ákveða hvernig skrefinu er lokið.

### <a name="building-the-user-interface-for-the-first-step"></a>Notandaviðmót hannað fyrir fyrsta skrefið

Notandaviðmótið er hannað með því að nota klasa sem erfir frá abstrakt klasanum **ProcessGuidePageBuilder**. Fyrir þetta skref skaltu gefa klasanum lýsandi heiti – **ProdProcessGuidePromptProductionIdPageBuilder**.

Leið eintöku klasans er svipuð og hvernig skrefið var eintekið af stýringunni. 

-   Skreyttu klasann **ProdProcessGuidePromptProductionIdPageBuilder** með eigindinni **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   Í klasanum **ProdProcessGuidePromptProductionIdStep** skal innleiða abstrakt aðferðina **pageBuilderName()** til að skila þessu heiti.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Líkt og skrefasmiðjan er einnig abstrakt smiðjumynstur innleitt fyrir smiðju síðuhönnuðar. Í sjaldgæfum tilfellum þar sem þú vilt aðra leið til að eintaka síðuhönnuðinn geturðu gert eftirfarandi:
> - Búðu til nýja klasasmiðju sem erfir frá **ProcessGuidePageBuilderAbstractFactory**.
> - Valfrjálst er að búa til nýjan færibreytuklasa sem innleiðir viðmótið **ProcessGuideIPageBuilderCreationParameters**, sem inniheldur færibreyturnar sem smiðjan þyrfti á að halda.
> - Í skrefaklasanum skal hnekkja aðferðunum **pageBuilderFactory()** og **pageBuilderCreationParameters()** til að skila ofangreindri smiðju og færibreytum.

Til að innleiða notandaviðmótið þarftu síðu með einu textahólfi til að færa inn auðkenni framleiðslupöntunarinnar, ásamt hnappnum **Í lagi** og hnappnum **Hætta við**. Hnappurinn **Hætta við** á að fara úr ferlinu.

Til að innleiða þetta þarftu að hnekkja tveimur aðferðum í klasanum **ProdProcessGuidePromptProductionIdPageBuilder**:

-   Notaðu aðferðina **addDataControls()** til að bæta við textahólfinu.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Notaðu aðferðina **addActionControls()** til að bæta við hnöppunum **Í lagi** og **Hætta við**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Þetta bætir við gagnastýringunum og hnapparnir fylgja með. Ef þú vilt hins vegar búa til sjá með ýmsum gagnastýringum og hnöppum er hægt að hnekkja aðferðinni **addControls()** í staðinn til að ná fram sveigjanleika.

Aðrar aðstæður til að hafa í huga er hvernig á að endurhanna síðuna ef upp kemur villa við auðkenningu, t.d. ef notandi slær inn röngu auðkenni framleiðslupöntunar. Grunnklasinn **ProcessGuidePageBuilder** innleiðir sjálfgefna hegðun, sem endurhannar notandaviðmótið, hreinsar út skannaða gildið og bætir við villustýringunni með villuboðinu. Þar sem þetta er sjálfgefin hegðun sem þú vilt nota þarftu ekki að bæta við neinum kóða til að meðhöndla villur.

> [!TIP]
> Ef þú vilt innleiða sérsniðna hegðun notandaviðmóts þar sem upp koma villur er hægt að hnekkja einni eða fleiri aðferðum **rebuildFromRequestPage()**, **isErrorState()** og **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Úrvinnsla gagna sem notandi slær inn í fyrsta skrefinu

Úrvinnsla gagnanna fer fram í klasanum **ProcessGuideDataProcessorDefault** sem á móti kallar fram gamla klasann **WhsRfControlData**. Engar breytingar eru nauðsynlegar á þessari sjálfgefnu hegðun og **WhsRfControlData** er þegar með rök fyrir auðkenningu reitsins **ProdId**, þannig að ekki þarf að skrifa nein rök til að meðhöndla þetta. Ef þörf er á nauðsynlegum viðbótum fyrir auðkenningarrökin skaltu íhuga að nota viðbót sem byggir á **WhsControl**.

### <a name="determine-if-the-first-step-is-complete"></a>Ákveða hvort fyrsta skrefinu sé lokið

Þegar auðkenningin tekst er komið að því að merkja skrefið sem lokið. Þetta er gert í grunnklasanum en þú þarft hinsvegar að innleiða skilyrðið til að ákvarða lok skrefsins. Eftirfarandi hnekkt aðferð gerir þetta.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Skref tvö: Skoða pöntunarupplýsingar og staðfesta

Í öðru skrefinu í ferlinu er notandanum sýndur skjár með upplýsingum um pöntunina. Notandinn getur annaðhvort smellt á hnappinn **Í lagi** til að staðfesta upphaf framleiðslupöntunar eða smellt á **Hætta við** til að fara aftur í upphaf ferlisins. Í þessu dæmi skal nefna skrefið **ProdProcessGuideConfirmProductionOrderStep** og síðuhönnunarklasann **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Klasinn ProdProcessGuideConfirmProductionOrderStep lítur út eins og eftirfarandi.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Þar sem notandinn slær ekki inn nein gildi hér þarf ekki að hnekkja aðferðinni **isComplete()**. Skrefinu er lokið þegar notandinn smellir á **Í lagi**.

Síðuhönnunarklasinn hnekkir aðferðinni **addDataControls()** til að bæta við þremur merkjum. Fyrsta merkið sýnir auðkenni framleiðslupöntunar, það seinna inniheldur upplýsingar um vöru (svo sem auðkenni vöru, víddir eða lýsingu) og það þriðja inniheldur magn og mælieiningu.

**addActionControls()** er síðan hnekkt til að bæta við tveimur hnöppum – hnappinum **Í lagi** og **Hætta við** til að hætta við ferlið og fara aftur í upphaf ferlisins.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Hægt er að finna sama frumkóða fyrir X++ aðferðirnar í þessari grein með því að nota Application Explorer. Síaðu klasaheitið og hægrismelltu svo á það og veldu **Skoða kóða**.

### <a name="step-3-start-the-production-order"></a>Skref 3: Hefja framleiðslupöntunina

Þriðja skrefið er þar sem viðskiptagrunnurinn fyrir að hefja framleiðslupöntun er framkvæmdur. Þetta skref er nokkuð frábrugðið fyrri skrefum vegna þess að ekkert notandaviðmót er til staðar. Skrefið er framkvæmt hljóðlega þegar notandinn smellir á **Í lagi** í fyrra skrefinu.

Abstrakt klasinn **ProcessGuideStepWithoutPrompt** innleiðir sjálfgefnu hegðunina fyrir slík skref. Núverandi skref ætti því að stækka klasann **ProcessGuideStepWithoutPrompt** og hnekkja aðferðinni **doExecute()**.

Eftirfarandi dæmi um kóða sýnir klasann innleiðingu aðferðarinnar **doExecute()**. Aðferðin sækir einfaldlega pöntunarkennið og notandakennið úr lotustöðunni og kallar fram aðferðina til að hefja þessa framleiðslupöntun.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Ef um undantekningu er að ræða tryggir ramminn fyrir rök meðhöndlunar á undantekningu að ferlinu sé snúið til baka í skrefið á undan.

> [!NOTE]
> Að kalla fram **addProcessCompletionMessage()** bætir skilaboðunum „Vinnu lokið“ við flettifæribreyturnar. Næsta skref (að því gefnu að það sé með notandaviðmót) mun sýna þessi skilaboð. Grunnklasarnir sjá um þessi rök og ekki þarf að bæta sérstökum kóða við klasa ferlisins til að ná fram þessari hegðun.


### <a name="building-the-navigation-through-the-steps"></a>Að hanna flettingu í gegnum skrefin

Grunnklasinn **ProcessGuideController** eintekur klasann **ProcessGuideNavigationAgentDefault** sem treystir á fyrirframskilgreinda flettileið sem er einfalt kort af skrefum upprunastaðar og endastaðar. Fyrir aðstæður framleiðsluupphafs, vegna þess að engin kvíslun háð skilyrðum er til staðar, mundi þessi innleiðing duga. Því þarf aðeins að hnekkja aðferðinni **initializeNavigationRoute()** til að skilgreina flettileiðina.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Það eru ferli þar sem skilyrt kvíslun er (byggt á aðgerðum notanda eða einhverjum öðrum skilyrðum). Slík ferli þurfa að gera eftirfarandi:

-   Innleiddu tiltekna flettara sem erfðir eru frá klasanum **ProcessGuideNavigationAgent**.

-   Innleiddu tiltekna flettarasmiðju sem er fengin úr klasanum **ProcessGuideNavigationAgentAbstractFactory**, sem inniheldur rök til að eintaka réttan flettara byggt á núverandi skrefi, lotustöðu, aðgerð notanda eða öðrum rökum.

-   Að öðrum kosti skal hnekkja **navigationAgentCreationParameters()** í stýriklasanum til að senda hentugar færibreytur.

-   Hnekktu **navigationAgentFactory()** í stýringunni til að eintaka flettarsmiðjunni sem var búin til hér fyrir ofan.

### <a name="action-classes"></a>Aðgerðaklasar

Aðgerðaklasar tákna aðgerðir notanda, þannig að þetta dæmi notar aðgerðina **Í lagi** til að sýna hvernig aðgerðirnar eru búnar til.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Klasinn verður að innleiða tvær abstrakt aðferðir:

-   **label()**, sem skilar merkinu sem á að birta í hnappastýringu sem er bundin við þessa aðgerð.

-   **doExecute()** sem framkvæmir aðgerðina. Eins og var minnst á sendir hnappurinn **Í lagi** einfaldlega svar til skrefsins. Hinsvegar gætu aðrar aðgerðir verið með flóknari rök hér.

Aðgerðirnar eru einteknar með rammanum **SysExtension** sem byggir á eigindinni **ProcessGuideActionName**. Líkt og eintekning síðuhönnuða, innleiðir skrefaklasinn sjálfgefna aðgerðasmiðju og það er mögulegt að hnekkja henni. Síðuhönnuðurinn bætir við stýrihnappi eins og þessum.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Þar með biður hann um næsta skref til að búa til aðgerðaklasa fyrir heitið sem fer í gegn og bindur þá aðgerð við hnappinn.

### <a name="summary"></a>Samantekt

Hér er ítarleg samantekt á kóðanum sem þarf fyrir ferlið til að taka saman allt sem hefur verið útskýrt í þessari grein:

1.  **ProdProcessGuideProductionStartController**

    1.  Hnekktu **initialStepName()** til að gefa upp heiti fyrsta skrefsins.
    2.  Hnekktu **initializeNavigationRoute()** til að setja saman flettikortið.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Hnekktu **isComplete()** til að tilgreina hvenær skrefinu er lokið.
    2.  Hnekktu **pageBuilderName()** til að tilgreina síðuhönnuð sem á að nota.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Hnekktu **addDataControls()** til að bæta við textareitnum **Framleiðslukenni**.
    2.  Hnekktu **addActionControls()** til að bæta við hnöppunum **Í lagi** og **Hætta við**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Hnekktu **pageBuilderName()** til að tilgreina síðuhönnuð sem á að nota.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Hnekktu **addDataControls()** til að bæta við upplýsingamerkjum pöntunar, vöru og magns.

    2.  Hnekktu **addActionControls()** til að bæta við hnöppunum **Í lagi** og **Hætta við**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Aðferðin **generateItemInfoForProdId()**, sem er notuð til að búa til merki vöruupplýsinga, er undanskilin frá þessari grein. Þessi aðferð sendir fyrirspurn á nokkrar töflur til að fá vörukenni, lýsingu og víddir. Ef þú vilt fá betri skilning á **generateItemInfoForProdId()** skaltu kíkja á frumkóðann.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Hnekktu **doExecute()** til að framkvæma upphafsferli framleiðslu og bæta við skilaboðunum um lok ferlisins.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Athugaðu að mikið af algengum mynstrum (endurmyndun notandaviðmóts við villu, stilling á skilaboðum um lok ferlis, **Í lagi** og **Hætta við** hegðun) hafa verið færð í rammann – þannig að þróunaraðili forritsins þarf ekki að skrifa kóða með föstum setningum þar sem villur koma gjarnan upp og felur í sér hættu á óstöðugri hegðun á milli ferla. Þar sem aðstæður þurfa að víkja frá sameiginlegu slóðinni er forritara þó gefinn kostur á að hnekkja viðeigandi aðferðum – en þá er það viljandi frávik sem er bæði skýrt og hægt að rekja.


### <a name="extending-a-business-process"></a>Að stækka viðskiptaferli

Hingað til hefur þessi grein lagt áherslu á hvernig hægt er að búa til nýtt ferli með því að nota rammann **ProcessGuide**. Í þessum lokahluta er að finna nokkur dæmi um hvernig hægt er að stækka viðskiptaferlana.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Bæta skrefi við flæði (með ProcessGuideNavigationAgentDefault)

Hvar á að stækka:

-   Undireining klasans **ProcessGuideController** fyrir ferlið.

Hvernig á að stækka:

-   Stækkaðu aðferðina **initializeNavigationRoute()** í stýriklasanum og kallaðu fram **addFollowingStep()** í klasanum **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Bæta skrefi við flæði (með sérstilltum flettara)

Hvar á að stækka:

-   Undireining **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

Hvernig á að stækka:

-   Búðu til nýjan undirklasa af **ProcessGuideNavigationAgent** sem skilar æskilegu heiti skrefs.

-   Búðu til nýjan klasa sem er leiddur af **ProcessGuideNavigationAgentFactory** sem með skilyrðum skilar flettaranum sem var búinn til hér að ofan.

-   Stækkaðu aðferðina **navigationAgentFactory()** í stýriklasanum til að skila smiðjunni sem var búin til hér að ofan.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Bæta við nýrri stýringu í notandaviðmóti fyrirliggjandi skrefs 

Hvar á að stækka:

-   Undireining af **ProdProcessGuidePageBuilder** fyrir skrefið.

Hvernig á að stækka:

-   Stækkaðu aðferðina **addDataControls()** og bættu við viðbótarstýringunni.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Ljúka endurskoðun á notandaviðmóti í fyrirliggjandi skrefi

Hvar á að stækka:

-   Undireining af **ProdProcessGuideStep**.

Hvernig á að stækka:

-   Búðu til nýjan undirklasa af klasanum **ProdProcessGuidePageBuilder** og innleiddu æskilegt notandaviðmót.

-   Stækkaðu aðferðina **pageBuildeName()** í skrefaklasanum til að skila **ProcessGuidePageBuilderNameAttribute** fyrir klasann sem var búinn til hér að ofan.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Breyta rökum þegar skrefi er lokið

Hvar á að stækka:

-   Undireining af **ProdProcessGuideStep**.

Hvernig á að stækka:

-   Stækkaðu aðferðina **isComplete()** til að búa til viðbótarrök.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
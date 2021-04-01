---
title: POS notendaviðmót sjónrænna stillinga
description: Þetta efnisatriði veitir upplýsingar um útlit afgreiðsluskjás fyrir Dynamics 365 Commerce sölustaður (POS) upplifun.
author: boycezhu
manager: annbe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 521fbd2c73adca1db38ba7258abf183f7350b109
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231297"
---
# <a name="pos-user-interface-visual-configurations"></a>Sjónrænar skilgreiningar fyrir notandaviðmót sölustaðar

[!include [banner](includes/banner.md)]


Hægt er að grunnstilla notendaviðmótið Microsoft Dynamics 365 Commerce smásölu með því að nota blöndu af sjónrænum forstillingum og skjáútliti sem eru úthlutað til verslunum, afgreiðslukassa og notendum. Þetta efni veitir upplýsingar um þessa stillingarvalkosti.

Eftirfarandi mynd sýnir tengsl milli hinna ýmsu eininga sem mynda hina stillanlegu útlitsþætti POS notendaviðmótsins (UI).

![POS skjáútlitseiningar](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Sjónræn regla

Sjónrænum forstillingum er úthlutað á afgreiðslukassa, og þær tilgreina sjónrænu þættina sem eru sértækir fyrir afgreiðslukassa og er deilt á meðal notenda. Sérhver notandi sem skráir sig inn í afgreiðslukassa sér sama þema, útlit, liti og myndir.

![POS upphafsskjár með ljósu þema](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![POS færsluskjár með dökku þema](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Forstillingarnúmer** - Forstillingarnúmerið er hið einkvæma kennimerki sjónrænu forstillingarinnar.
- **Lýsing** - Þú getur tilgreint merkingarbært nafn sem mun hjálpa til við að bera kennsl á rétta forstillingu fyrir þínar aðstæður.
- **Þema** - Þú getur valið á milli þemanna **Ljóst** og **Dökkt** fyrir forrit. Þemað hefur áhrif á leturgerð og bakgrunnslit allsstaðar í forritinu.
- **Áherslulitur** - Áherslulitur er notaður í gegnum allt POS til að aðgreina eða merkja tilteknar sjónrænar einingar, eins og t.d. flísar, skipunarhnappa og tengla. Þessar einingar eru yfirleitt aðgerðir.
- **Hauslitur** - Þú getur grunnstillt lit blaðsíðuhaussins til að uppfylla kröfur um vörumerkjaþróun frá smásöluaðila.
- **Leturkerfi** - Þú getur valið á milli leturkerfanna **Staðlað** og **Stórt**. Leturkerfið hefur áhrif á leturstærðina í öllu forritinu. Sjálfgefið val er **Staðlað**.
- **Sýna alltaf forritastikamerki** - Þegar kveikt er á þessum valkosti er texti merkimiða alltaf sýnilegur undir hnöppunum á forritastikunni.
- **Útlit** - Þú getur valið á milli útlitanna **Miðja** og **Hægri**. Útlitið hefur áhrif á röðun innskráningarboxsins á innskráningarskjánum. Sjálfgefið val er **Miðja**.
- **Sýna dagsetningu/tíma** - Þegar kveikt er á þessum möguleika eru núverandi dagsetning og tími sýndur í POS hausnum og á innskráningarskjánum.
- **Lyklaborð** - Þú getur valið á milli **Gera OS lyklaborð sjálfgefið** og **Sýna talnaborð** til að tilgreina sjálfgefið lyklaborð sem er notað til innsláttar á innskráningarskjánum. Talnaborðið er sýndarlyklaborð sem er aðallega notað fyrir snertitæki. Sjálfvalið er **Gera OS lyklaborð sjálfgefið**.
- **Fyrirtækismerki** - Þú getur tilgreint fyrirtækismerki sem sést á innskráningarskjánum. Við mælum með að þú notir mynd sem hefur gegnsæjan bakgrunn. Skráarstærð ætti að vera eins lítil og mögulegt er, þar sem hegðun og frammistaða forrits getur orðið fyrir áhrifum þegar stórar skrár eru geymdar og hlaðið upp.
- **Innskráningarbakgrunnur** - Þú getur tilgreint bakgrunnsmynd fyrir innskráningarskjáinn. Skráarstærð bakgrunnsmynda ætti að vera eins lítil og hægt er.
- **Bakgrunnur** - Þú getur tilgreint bakgrunnsmynd sem er notuð í staðinn fyrir samfelldan þemalitinn alls staðar í forritið. Hvað varðar bakgrunnsmyndir fyrir innskráningarskjáinn, ætti að hafa skráarstærðina eins litla og hægt er.

> [!NOTE]
> **Hægri** útlit og birting dagsetningar/tíma gilda ekki fyrir innskráningarskjáinn í þjappaði skoðun.

Þú þarft að keyra **1090** (**Afgreiðslukassar**) dreifingaráætlunarvinnslu til að samstilla nýjustu skilgreiningar á sjónrænu sniði við gagnagrunn rásar.

## <a name="screen-layouts"></a>Útlit afgreiðsluskjás

Grunnstillingar skjáútlits ákvarða aðgerðir, innihald og staðsetningu stjórnborðs notandaviðmóts á **upphafsskjá** POS og **færsluskjánum**.

![POS skjáútlit yfirlit](../commerce/media/POS-Screen-Layout-View.png)

- **Upphafsskjár** - Í flestum tilfellum er upphafsskjárinn síðan sem notendur sjá þegar þeir skrá sig fyrst inn í POS. Upphafsskjár getur verið samsettur af vörumerkjamynd og hnappahnitum sem veita aðgang að aðgerðum POS. Venjulega eru aðgerðir sem eru ekki sértækar fyrir núverandi færslur settar á þennan skjá.

    ![POS upphafsskjár](../commerce/media/POS-Welcome-Screen.png)

- **Færsluskjár** - **Færsla** skjárinn er aðalskjárinn í POS fyrir vinnslu sölufærslur og pantanir. Innihald og útlit er grunnstillt með því að nota skjáútlitshönnuður.

    ![POS-færsluskjár](../commerce/media/POS-Transaction-Screen.png)

- **Sjálfgefinn upphafsskjár** - Sumir smásalar vilja frekar að gjaldkeri fari beint á **Færslu** skjá eftir innskráningu. **Sjálfgefinn upphafsskjár** stillingin gerir þér kleift að tilgreina sjálfgefin skjá sem birtist eftir innskráningu fyrir hvert skjáútlit.

### <a name="assignment"></a>Verkefni

Hægt er að úthluta útliti afgreiðsluskjás á verslunar-, afgreiðslukassa- eða notandastigi. Notandaúthlutunin hnekkir afgreiðslukassa- og verslunarúthlutuninni, og afgreiðslukassaúthlutunin hnekkir verslunarúthlutuninni. Í einföldu dæmi þar sem allir notendur nota sömu útlitið, óháð afgreiðslukassa eða hlutverki, er aðeins hægt að stilla skjáuppsetninguna á verslunarstiginu. Í dæmum þar sem tilteknar afgreiðslukassar eða notendur þurfa sérsniðið útlit, þá er hægt að úthluta því útliti.

Allt eftir því hvaða stig skjáútlits er notað þarf að keyra **1070** (**Grunnstilling rásar**), **1090** (**afgreiðslukassar**), og/eða **1060** (**Starfsfólk**) dreifingaráætlunarvinnslur til að samstilla nýjustu skilgreiningar skjáútlits í gagnagrunni rásar.

### <a name="layout-sizes"></a>Útlitsstærðir

Flestir þættir POS notandaviðmóts eru móttækilegir og stærð útlitsins er breytt sjálfkrafa og lagfært með hliðsjón af skjástærð og stefnu. POS **Færsla** skjárinn verður samt sem áður að vera grunnstilltur fyrir allar skjáupplausnir sem búast má við.

Við ræsingu velur POS forritið sjálfkrafa nálægasta útlitsstærð sem er grunnstillt fyrir tækið. Útlit skjás getur einnig innihaldið grunnstillingar fyrir bæði langsniðs- og skammsniðsstillingar, og fyrir tæki í fullri stærð sem og smærri tæki. Þar af leiðandi getur notendum verið úthlutað á eina tegund skjáútlits sem virkar í mismunandi stærðar- og skjámyndaþáttum innan verslunarinnar.

![POS útlitsstærðir](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Nafn** - Þú getur slegið inn merkingarbært nafn til að auðkenna skjástærðina.
- **Útlitsgerð** - POS forritið getur sýnt notendaviðmótið í ýmsum stillingum til að veita bestu notendaupplifun á tilteknu tæki.

    - **Modern POS - Óþjappað** - Óþjappað útlit er venjulega best fyrir stærri skjái, svo sem skrifborskjái og spjaldtölvur. Þú getur valið viðmótseiningarnar til að ná yfir þær, tilgreina stærð og staðsetningu þeirra, og stilla nákvæma eiginleika þeirra. Full útlit styðja bæði þversniðis- og langsniðsskilgreiningar.
    - **Modern POS - Þjappað** - Þjappað útlit er venjulega best fyrir síma og litla spjaldtölvur. Hönnunarmöguleikar fyrir smærri tæki eru takmarkaðir. Þú getur grunnstillt dálkana og reitina fyrir kvittunar- og samtölugluggana.

- **Breidd/Hæð** - Þessi gildi tákna virka skjástærð, í pixlum, sem gert er ráð fyrir í þessu útliti. Mundu að sum stýrikerfi nota kvörðun fyrir háskerpu skjái.

> [!TIP]
> Þú getur fengið upplýsingar um útlitsstærðina sem krafist er fyrir POS-skjá með því að skoða upplausnina í forritinu. Ræstu POS og farðu í **Stillingar \> Upplýsingar um lotu**. POS sýnir skjáútlitið sem er nú hlaðið, útlitsstærð og upplausn forritsgluggans.

![Upplýsingasíða um sölustaðarlotu sem sýnir skjáútlit, útlitsstærð og upplausn forritagluggans sem er hlaðinn](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Hnappahnit

Fyrir hverja útlitsstærð í skjáútliti er hægt að grunnstilla og úthluta hnappahnitum fyrir upphafsskjár POS og **Færsla** skjár. Hnappahnit fyrir upphafsskjá er sjálfkrafa stillt upp frá vinstri til hægri, frá lægsta númerinu (Upphafsskjár 1) til hæsta númerið.

Í óþjöppuðu POS útliti er staðsetning hnappahnita tilgreind í skjáútlit hönnuður.

Í þjöppuðu POS útliti eru hnappahnitum stillt sjálfkrafa upp frá toppi til botns, frá lægsta númeri (Færsla skjár 1) í hæsta númerið. Hægt er að fara inn í það í **Aðgerðir** valmyndinni.

![Þjappað útlit hnappahnit](../commerce/media/Compact-View-Button-Grids.png)

> [!NOTE]
> Hnappastærðir í hönnuðin verða kvarðaðir þannig að þær passi við stærð gluggans, því er ekki víst að þær endurspegli raunverulega hnappa á sölustað. Til að herma eftir útliti hnappahnits skal stilla gluggahönnuð á sömu stærð og á sölustað.

### <a name="images"></a>Myndir

Fyrir hverja útlitsstærð í skjáútliti er hægt að tilgreina myndir til að vera með í POS notandaviðmótinu. Fyrir óþjappað POS útlit er hægt að skilgreina eina mynd fyrir upphafsskjár. Þessi mynd birtist sem fyrsta viðmótseining til vinstri. Á **Færsla** skjár, myndir er hægt að nota sem flipamyndir eða sem lógó. Þjappað POS útlit notar ekki þessar myndir.

### <a name="screen-layout-designer"></a>Útlitshönnuður afgreiðsluskjás

Skjáútlit hönnuður leyfir þér að grunnstilla ýmsa þætti POS **Færsla** skjásins fyrir hverja útlitsstærð, bæði í langsniðs- og skammsniðsstillingum, og fyrir bæði þjappað og óþjappað útlit. Skjáútlit hönnuður notar ClickOnce uppsetningartækni til að hlaða niður, setja upp og ræsa nýjustu útgáfuna af forritinu í hvert sinn sem notendur opna það. Vertu viss um að athuga kröfur vafrans fyrir ClickOnce. Sumir vafrar, svo sem Google Chrome, þurfa viðbætur.

> [!IMPORTANT]
> Þú verður að grunnstilla skjástærð fyrir hverja útlitsstærð sem er skilgreind og sem er notuð af POS.

### <a name="full-layout-designer"></a>Óþjappað útlit hönnuður

Óþjappað útlit hönnuður leyfir notendum að draga stýringu notandaviðmóts inn á POS **Færsla** skjár og grunnstilla þá stýringu.

![POS óþjappað útlit hönnuður (langsniðsstilling)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Innflutningur útlit/Útflutningur útlit** - Þú getur flutt inn og út POS skjáútlitshönnun sem XML skrá, svo að þú getur auðveldlega endurnýta og deila þeim yfir umhverfi. Það er mikilvægt að þú flytur inn útlitshönnun fyrir réttar útlitsstærðir. Annars er mögulegt að þættir notandaviðmóts passi ekki rétt á skjánum.
- **Langsnið/Skammsnið** - Ef POS-tækið leyfir notendum að skipta á milli langsniðs- og skammsniðsstillinga, verður þú að skilgreina skjáútlit fyrir hverja stillingu. POS greinir sjálfkrafa skjásnúning og sýnir rétta útlitið.
- **Útlitshnit** - POS útlit hönnuður notar 4-pixla hnit. Stýring notandaviðmóts „smellur“ á hnitið til að hjálpa þér að jafna efnið á réttan hátt.
- **Hönnuður aðdráttur** - Hægt er að þysja að og frá á hönnunarskjánum til að sjá betur efni á POS skjánum. Þessi eiginleiki kemur að góðum notum þegar skjáupplausnin á POS er mjög mismunandi frá upplausn skjásins sem notuð er í hönnuði.
- **Sýna/fela yfirlitsstiku** - Fyrir óþjappað POS útlit getur þú valið hvort vinstri yfirlitsstikan sé sýnileg á skjánum **Færsla**. Þessi eiginleiki er gagnlegur fyrir skjái sem eru með lægri upplausn. Til að stilla sýnileika skaltu hægrismella á yfirlitsstikuna í hönnuðinum og velja eða hreinsa **Alltaf sýnilegt** gátreitinn. Ef yfirlitsstikan er falin geta POS notendur ennþá fengið aðgang að henni með því að nota valmyndina efst til vinstri.

    ![Sýna/fela yfirlitsstiku](../commerce/media/Navigation-Bar.PNG)

- **POS stýring** - POS útlit hönnuður styður eftirfarandi stýringar. Þú getur grunnstillt margar stýringar með því að hægrismella og nota flýtivalmyndina.

    ![POS notandaviðmót stýring](../commerce/media/POS-UI-Controls.png)

    - **Talnaborð** - Talnaborðið er aðalbúnaðurinn fyrir notandainntak á POS **Færsla** skjánum. Þú getur grunnstillt stýringuna þannig að óþjappað talnaborð birtist. Þessi valkostur er tilvalin fyrir tæki með snertiskjá. Að öðrum kosti geturðu grunnstillt það þannig að aðeins ílagssvæðið sést. Í þessu tilviki er ytra lyklaborð notað fyrir inntak. Stillingar fyrir talnaborðið eru aðeins tiltæk fyrir óþjappað útlit. Fyrir þjappað útlit, allt talnaborðið er alltaf sýnd á **Færsla** skjánum.
    - **Samtölugluggi** - Hægt er að grunnstilla samtölugluggann í annaðhvort einum dálki eða tveimur dálkum, til að sýna gildi eins og línufjöldi, afsláttarupphæð, gjöld, millisamtala og skattur. Þjappað útlit styðja aðeins einn dálk.
    - **Kvittun gluggi** - Kvittun gluggi inniheldur sölulínur, greiðslulínur og afhendingarupplýsingar fyrir þær vörur og þjónustu sem eru unnin í POS. Þú getur tilgreint dálka, breidd og staðsetningu. Í þjöppuðu útliti er einnig hægt að grunnstilla viðbótarupplýsingar sem birtast í röðinni undir aðallínunni.
    - **Viðskiptamannaspjald** - Viðskiptamannaspjald sýnir upplýsingar um viðskiptavin sem tengist núverandi færslunni. Þú getur grunnstillt viðskiptamannaspjaldið til að fela eða sýna viðbótarupplýsingar.
    - **Flipastýring** - Þú getur bætt við flipastýringunni á skjáútlit og síðan sett aðrar stýringar, svo sem talnaborð, viðskiptamannaspjald eða hnappahnit, í það. Flipastýringin er geymir sem hjálpar þér að koma meira efni fyrir á skjánum. Flipastýringin er aðeins tiltæk fyrir óþjappað útlit.
    - **Mynd** - Hægt er að nota myndastýringuna til að sýna lógó verslunarinnar eða annað vörumerki á **Færsla** skjánum. Myndastýringin er aðeins í boði fyrir óþjappað útlit.
    - **Vörur sem mælt er með** - Ef stýring fyrir vörur sem mælt er með er grunnstillt fyrir umhverfið, sýnir hún vörutillögur sem byggja á námi vélar.
    - **Sérstillt stýring** - Sérstillt stýring virkar sem staðarhaldari í skjáútlitinu og gerir þér kleift að taka frá pláss fyrir sérstillt efni. Sérstillt stýring er aðeins tiltæk fyrir óþjappað útlit.

### <a name="compact-layout-designer"></a>Þjappað útlit hönnuður

Eins og hönnuður fyrir óþjappað útlit, gerir hönnuður fyrir þjappað útlit þér kleift að stilla POS skjáútlitið fyrir farsíma og litlar spjaldtölvur. Í þessu tilfelli er útlitið sjálft samt sem áður ákveðið. Þú getur grunnstillt stýringuna í útliti með því að hægrismella og nota flýtivalmyndina. Þú getur samt sem áður ekki notað draga-og-sleppa aðgerðir fyrir viðbótar efni.

![Þjappað útlit hönnuður](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Hönnuður hnappahnits

Hnappahnit hönnuður gerir þér kleift að grunnstilla hnappahnit sem hægt er að nota á POS upphafsskjár og **Færsla** skjár fyrir bæði óþjappað og þjappað útlit. Sama hnappahnitið getur verið notaður yfir útlit og útlitsgerðir. Eins og skjáútlit hönnuður, hnappahnit hönnuður notar ClickOnce uppsetningartækni til að hlaða niður, setja upp og ræsa nýjustu útgáfuna af forritinu í hvert sinn sem notendur opna það. Vertu viss um að athuga kröfur vafrans fyrir ClickOnce. Sumir vafrar, svo sem Google Chrome, þurfa viðbætur.

![Hönnuður hnappahnits](../commerce/media/Button-Grid-Designer.png)

- **Nýr hnappur** - Smelltu til að bæta nýjum hnappi við hnappahnitið. Nýir hnappar birtast að sjálfgefnu efst í vinstra horni hnitsins. Samt sem áður er hægt að raða hnappa með því að draga þau í útlitið.

    > [!IMPORTANT]
    > Innihald hnappahnitsins getur skarast. Þegar þú skipuleggur hnappa skaltu ganga úr skugga um að þau fela ekki aðra hnappa.

- **Ný hönnun** - Smelltu til sjálfkrafa að setja upp hnappahnitsútlit með því að tilgreina fjölda hnappa fyrir hverja röð og dálk.
- **Hnappaeiginleikar** - Þú getur grunnstillt eiginleika hnapps með því að hægrismella á hnappinn og nota flýtivalmyndina.

    > [!IMPORTANT]
    > Sumir hnappahnitsstillingar gilda aðeins um Enterprise POS, ekki um Modern POS eða Cloud POS.

    ![Eiginleikar hnapps í hnappahniti](../commerce/media/Button-grid-button-properties.png)

    - **Aðgerð** - Í listanum yfir viðeigandi POS aðgerðir, veldu þá aðgerð sem er kölluð fram þegar smellt er á hnappurinn í POS.

        Til að sjá lista yfir studdar POS aðgerðir, skoðaðu [Sölustaðaaðgerðir (POS) á netinu og utan nets](pos-operations.md).

    - **Færibreytur aðgerðar** - Sumar POS aðgerðir nota viðbótar færibreytur þegar þær eru kallaðar fram. Til dæmis, fyrir aðgerðina að bæta við vöru, geta notendur tilgreint vöruna sem á að bæta við.
    - **Hnappatexti** - Tilgreindu textann sem birtist á hnappinum í POS.
    - **Fela hnappatexta** - Notaðu þennan gátreit til að fela eða sýna hnappatexta. Hnappatexti er oft falin fyrir litla hnappa sem sýna aðeins tákn.
    - **Ábending** - Tilgreina viðbótar hjálpartexta sem birtist þegar notendur færa músina yfir hnappinn.
    - **Stærð í dálkum/Stærð í röðum** - Þú getur tilgreint hversu hár og breiður hnappurinn er.

        ![POS hnappastærðir í röðum og dálkum](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Sérstillt leturgerð** - Þegar þú velur **Virkja sérstillta leturgerð fyrir POS** gátreitinn getur þú tilgreint leturgerð, aðra en sjálfgefið leturgerð fyrir POS kerfið.
    - **Sérstillt þema** - Sjálfgefið notar POS hnappar áherslulit frá sjónrænu forstillingunni. Þegar þú velur **Notaðu sérstillt þema** gátreitinn geturðu tilgreint fleiri liti.

        > [!NOTE]
        > Modern POS og Cloud POS nota aðeins **Baklitur** og **Litur leturgerðar** gildin.

    - **Hnappamynd** - Hnappar geta innihaldið myndir eða tákn. Veldu á milli tiltækra mynda sem eru tilgreindar í **Retail og Commerce \> Uppsetning rásar \> POS uppsetning \> POS \> Myndir**.

![Dæmi hnappahnit í POS](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp útlitshönnuð smásöluverslunar (POS)](install-pos-layout-designer.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
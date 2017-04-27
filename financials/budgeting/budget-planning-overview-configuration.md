---
title: "Yfirlit áætlunar fjárhagsáætlunargerðar"
description: "Þetta grein kynnir fjárhagsáætlunargerð og inniheldur upplýsingar til að hjálpa við að skilgreina fjárhagsáætlunargerð og setja upp ferli fjárhagsáætlunargerðar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: d5073958f8ffe90e47dc10cde67e081420e559a1
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-overview"></a>Yfirlit áætlunar fjárhagsáætlunargerðar

[!include[banner](../includes/banner.md)]


Þetta grein kynnir fjárhagsáætlunargerð og inniheldur upplýsingar til að hjálpa við að skilgreina fjárhagsáætlunargerð og setja upp ferli fjárhagsáætlunargerðar.

<a name="overview-of-budget-planning"></a>Yfirlit fjárhagsáætlunargerðar
---------------------------

Þú framkvæmir Fjárhagsáætlunargerð við undirbúning áætlana sem fyrirtæki munu nota. Fyrirtæki getur skilgreint fjárhagsáætlunargerðar og sett síðan upp ferli fjárhagsáætlunargerðar til að uppfylla þeirra fyrirtækisreglur, ferlum og kröfur fyrir undirbúning fjárhagsáætlunar. 

Þegar þú skilur hugtök og sem eru notaðar í Microsoft Dynamics 365 fyrir Operations orðalisti, verður auðveldara fyrir þig að innleiða fjárhagsáætlunargerðar í þínu fyrirtæki.

### <a name="key-terms"></a>Lykilhugtök

-   **Fjárhagsáætlunarferli** Ferli fjárhagsáætlunargerðar ákvarðar hvernig hægt er að uppfæra, beina, endurskoða og samþykkja fjárhagsáætlanir innan stigveldis fyrirtækisins fyrir fjárhagsáætlunarferlið. Ferli fjárhagsáætlunargerðar er tengd ferli fjárhagsáætlunar og fyrirtæki gegnum lögaðila.
-   **Fjárhagsáætlunargerðir** – fjárhagsáætlunargerðir sem innihalda gögn fjárhagsáætlunar fyrir ferli fjárhagsáætlunar. Hægt er að hafa margar fjárhagsáætlanir sem eru notaðir í mismunandi tilgangi. Til dæmis má nota fjárhagsáætlunargerðir til að stofna áætlunarupphæðir fyrir mismunandi skipulagseiningar, eða þær geta hjálpað til við að gera samanburð og taka upplýstar ákvarðanir.
-   **Aðstæður fjárhagsáætlunargerðar** – aðstæður fjárhagsáætlunargerðar skilgreina gagnategundir fyrir fjárhagsáætlanir. Skilgreina aðstæður fjárhagsáætlunargerðar til að styðja peningalegir og aðrar einingar mælieiningu klasa, eins og magn. Dæmi um peningalegir aðstæður fjárhagsáætlunargerðar eru Deild fyrra árs og Deildarbeiðnir. Dæmi um aðstæður fjárhagsáætlunargerðar sem nota magn eru stuðningssímtöl fyrir fyrra ár og jafngildi starfsráðningarstuðuls fulls starfs (FTE).
-   **Stig fjárhagsáætlunargerðar** – stig Fjárhagsáætlunargerðar skilgreina skrefin sem fjárhagsáætlun fylgir frá upphafi til endanlegs samþykkis. Áætlunarstig áætlunar er skipað í verkflæði fjárhagsáætlunargerðar.
-   **Verkflæði fjárhagsáætlunargerðar** – verkflæði Fjárhagsáætlunargerð er samsett úr og skilgreinir stig fjárhagsáætlunargerðar. verkflæði fjárhagsáætlunargerðar eru tengdar við verkflæði fyrir Fjárhagsáætlunar. Verkflæði fjárhagsáætlunar eru sjálfvirkar og handvirkar vinnslur sem flytja fjárhagsáætlanir í gegnum stig fjárhagsáætlunargerðar.

[![Hugtök fjárhagsáætlunargerðar](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Sameiginleg verkefni

Hægt er að nota fjárhagsáætlunargerðar til að framkvæma eftirfarandi verkefni:

-   Stofna fjárhagsáætlanir til að skilgreina áætlaðar tekjur og útgjöld fyrir ferli fjárhagsáætlunar.
-   Greina og uppfæra fjárhagsáætlanir fyrir margar aðstæður.
-   Hægt er að sjálfvirkt beina fjárhagsáætlun, ásamt vinnublöðum, réttlætingarskjöl og önnur viðhengjum, til yfirferðar og samþykkis.
-   Sameina margar fjárhagsáætlunargerðir úr neðri stigum fyrirtækis í einni yfirfjárhagsáætlunargerð á hærra stigi í fyrirtækinu. Einnig er hægt að þróa eina fjárhagsáætlunargerð á hærra stigi fyrirtækisins og úthluta fjárhagsáætlun á neðri stig fyrirtækisins.

Fjárhagsáætlunargerð er samþætt með öðrum einingum Microsoft Dynamics 365 for Operations. Því er hægt að færa inn upplýsingar úr fyrri fjárhagsáætlanir, raunútgjöld, eignir og mannauður. Þar sem Fjárhagsáætlunargerð er einnig samþætt Microsoft Excel og Microsoft Word geturðu nota þessi tæki til að vinna með gögn fjárhagsáætlunargerðar. Til dæmis getur stjórnandi fjárhagsáætlunar flutt út deildabeiðni um fjárhagsáætlun í Excel vinnublað úr aðstæðum fjárhagsáætlunargerðar. Gögn hægt að greina, uppfært og charted í vinnublaðinu og birt svo aftur í línur fjárhagsáætlunargerðar.

## <a name="configuring-budget-planning"></a>Skilgreining fjárhagsáætlunargerðar
**skilgreiningu fjárhagsáætlunargerðar** síða inniheldur flestar stillingar sem þarf til að setja upp fjárhagsáætlunargerð. Eftirfarandi kaflar lýsa sumar lykilþáttum sem ætti að íhuga þegar þú skilgreina fjárhagsáætlunargerðar. Þegar þú hefur lokið skilgreiningunni, seturðu upp ferli fjárhagsáætlunargerðar.

### <a name="create-a-budget-planning-schema"></a>Stofna skema fjárhagsáætlunargerðar

valfrjáls en mælt er með að fyrsta skrefið sé að stofna skema sem sýnir ferli fyrirtækis þíns við að setja fram fjárhagsáætlun. Hægt er að nota hvaða aðferð sem er til að stofna þetta skema. Eftirfarandi skýringarmynd sýnir almennan dæmi þar sem aðskilda verkflæði fjárhagsáætlunargerðar eru stofnaðar fyrir mismunandi stig fyrirtækisins. Stig eru skilgreind innan hvers verkflæði og tiltekin tilvikum er úthlutað á hverju stigi til að halda gögnum fjárhagsáætlunar. Verk eru framkvæmd til að flytja gögn úr einu stigi í næsta. Til dæmis upphæðir er hægt að úthluta eða steypt saman í mismunandi lykla, samþykki eða öðrum skoðunarferlum. Í þessu dæmi sýnir skáletraður texti aðstæður sem er ekki hægt að breyta í stigi, eða gögn sem eru söguleg eða hefur verið samþykkt á fyrra stig og því ætti ekki að breyta. 

[![Almennt skema fjárhagsáætlunargerðar](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Í eftirfarandi dæmi áætlar höfuðstöðvar fyrirtækis grunnlínuupphæðir upphaflegrar fjárhagsáætlunar og dreifir þeim söludeildirnar. Söludeildirnar meta síðan og senda sína spá aftur í höfuðstöðvar þar sem fjárhagsáætlunarstjóri birtir og leiðréttir spá. Loks sendir fjárhagsáætlunarstjóri leiðrétt upphæð fjárhagsáætlunar til  Framkvæmdastjóra fyrir yfirferð, síðustu leiðréttingar og samþykkis. 

[![Dæmi um skema fjárhagsáætlunargerðar](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Stigveldi fyrirtækis fyrir fjárhagsáætlunargerð

Á **stigveldi Fyrirtækis** síðu er hægt að tilnefna stigveldi fyrirtækis sem stigveldi fjárhagsáætlunargerðar fyrir hverju ferli fjárhagsáætlunargerðar. Stigveldi fjárhagsáætlunargerðar þarf ekki að samsvara stöðluðu stigveldi fyrirtækis sem notað er í öðrum tilgangi. Þar sem þetta stigveldið er notuð til að safna og dreifa gögn, gætirðu vijað nota annað skipulag. Í dæmaskema eru söludeildirnar undir stigi höfuðstöðvar sem inniheldur deildir fjárhagsáætlunar og fjármála. Skipanin sem er notuð til að stjórna aðgerðum fyrir söludeildirnar er líklega ólík þessu skipulagi. Aðeins eitt stigveldi fyrirtækis getur verið úthlutað á hvert ferli fjárhagsáætlunargerðar. 

Nánari upplýsingar, sjá [Fyrirtæki og stigveldi fyrirtækis](/dynamics365/operations/organization-administration/organizations-organizational-hierarchies).

### <a name="user-security"></a>Notandaöryggi

Fjárhagsáætlunargerð getur farið að einu af tveimur öryggislíkönum til að skilgreina notandaheimildir. Til að tilgreina öryggislíkan stillirðu færibreytna fjárhagsáætlunargerðar á **skilgreiningu fjárhagsáætlunargerðar** síðu.

### <a name="budget-planning-workflows-stages"></a>Verkflæðisstig fjárhagsáætlunargerðar

verkflæði fjárhagsáætlunargerðar eru notaðar með verkflæði fyrir Fjárhagsáætlun til að stjórna stofnun og þróun fjárhagsáætlana.

Verkflæði fjárhagsáætlunargerðar samanstendur af röð stiga sem fjárhagsáætlunargerð færist í gegnum. Hvert verkflæði fjárhagsáætlunargerðar eru tengdar við verkflæði fyrir Fjárhagsáætlun. Verkflæði fjárhagsáætlunar eru ein gerð af verkflæði sem eru notuð alls staðar í Microsoft Dynamics 365 fyrir Operations. Verkflæði fjárhagsáætlunar beinir fjárhagsáætlunum, ásamt vinnublöðum, réttlætingum og viðhengjum, í gegnum fyrirtækið til yfirferðar og samþykkis. 

Þú stofnar verkflæði fjárhagsáætlunargerðar á **verkflæðisstig** hluta í **skilgreiningu fjárhagsáætlunargerðar** síðu. Þar er hægt að velja stig og verkflæði Fjárhagsáætlunar sem verður notuð og skilgreina einnig viðbótarstillingar. 

Góð regla er að stofna verkflæði fjárhagsáætlunargerðar fyrir hvert stig í stigveldi fjárhagsáætlunar. Síðan úthlutarðu verkflæði Fjárhagsáætlunar sem inniheldur einingar sem samsvara stig í verkflæði fjárhagsáætlunargerðar. Í dæmaskemað sem birtist fyrr í þessum grein yrði stofnað eitt verkflæði fjárhagsáætlunargerðar fyrir söludeildirnar og önnur yrði stofnuð fyrir höfuðstöðvum. Verkflæði Fjárhagsáætlunar flytur fjárhagsáætlunargerðir gegnum stig. 

Þú stofnar verkflæði Fjárhagsáætlunar fyrir fjárhagsáætlunargerð á **verkflæði Fjárhagsáætlunar** síðu. Ferlið svipar til ferlis að stofna önnur verkflæði í Microsoft Dynamics 365 for Operations. Eftirfarandi skýringarmynd sýnir dæmi um verkflæði höfuðstöðva. 

[![Verkflæði fjárhagsáætlunar fyrir fjárhagsáætlun](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Verkflæðið inniheldur einingar fyrir úthlutun til söludeildirnar og uppsöfnun þeirra sendinga, endurskoðun fjárhagsáætlunarstjóra, samþykkið Framkvæmdastjóra, og umskipti stiga á milli hvers stigs. 

Þú úthlutar verkflæði fjárhagsáætlunar á hvert verkflæði fjárhagsáætlunargerðar á **verkflæðisstig** hluta í **skilgreiningu fjárhagsáætlunargerðar** síðu.

### <a name="parameters-scenarios-and-stages"></a>Færibreytur, aðstæður og stig

Upprunalegar stillingar á **skilgreiningu fjárhagsáætlunargerðar** síðu gera mögulegt að stofna nokkrar einingar fyrir síðari skilgreiningarskref:

-   **Færibreytur** – Færibreytur skilgreina öryggisreglur sem á að nota á fjárhagsáætlanir og sjálfgefna fjárhagsvíddir sem á að nota þegar notendur kafa í upphæðir aðstæður fjárhagsáætlunargerðar.
-   **Aðstæður** – Aðstæður búa yfir flokkum gagna sem óskað er fyrir fjárhagsáætlanir. Skilgreina aðstæður fjárhagsáætlunargerðar til að styðja peningalegir og aðrar einingar mælieiningu klasa, eins og magn. Í fjárhagsáætlun, tákna aðstæður eina útgáfu af gögnum fjárhagsáætlunargerðar. Dæmi um peningalegar aðstæður fjárhagsáætlunargerðar eru sala fyrri árs og Undirritaðir samningar. Fjöldi sölusímtala og jafngildi starfsráðningarstuðuls fulls starfs eru dæmi um aðstæður sem nota magn.
-   **Stig** - Stig skilgreina skref sem fjárhagsáætlun fer eftir frá upphafi til endanlegs samþykkis. Dæmi um stig fjárhagsáætlunargerðar eru HQ Rollup, Yfirferð Framkvæmdastjóra og Endanleg.

### <a name="allocation-schedules"></a>Úthlutunaráætlanir

Í fjárhagsáætlunargerðar, er hægt að úthluta upphæðir eða magn á línur fjárhagsáætlunargerðar úr einni aðstæður í öðrum aðstæðum eða jafnvel í sömu aðstæður. Til dæmis gætirðu úthluta sömu aðstæður eigi að gera breytingar á fjárhagsvíddir eða dagsetningar upphæða í þeim aðstæðum. Hægt er að framkvæma úthlutun innan fjárhagsáætlunar eða frá einni fjárhagsáætlun til annarrar. 

Úthlutunaráætlanir úthluta sjálfkrafa fjárhagsáætlunarlína við verkflæðisferli. Hægt er að framkvæma úthlutanir með því að nota eitthvað af eftirfarandi aðferðum í **úthlutunaraðferð** lista:

-   **Úthlutun yfir tímabil ** – Þú notar úthlutunarlykill tímabils til að úthluta fjárhagsáætlunarlínum úr upprunaaðstæður fjárhagsáætlunargerðarinnar yfir mörg tímabil í viðtöku aðstæðum. **Ábending:** áður En hægt er að úthluta yfir tímabil, verður að setja upp úthlutunarlykla tímabils á síðunni ****Úthlutunartegundir tímabils****.
-   **Úthluta á víddir** – Línur fjárhagsáætlunar er úthlutað úr upprunalegum aðstæðum fjárhagsáætlunar yfir fjárhagsvíddir í viðtökuaðstæðum. **Ábending:** áður En hægt er að úthluta á víddir, verður að setja upp úthlutunarskilmála fjárhagsáætlunar á síðunni ****Úthlutunarskimlálar fjárhagsáætlunar****.
-   **Samanlagt** – Línur fjárhagsáætlunar eru safnað úr upprunaaðstæðum fjárhagsáætlunargerðar í tengdri fjárhagsáætlun í viðstökuaðstæðum í yfirskipuðu fjárhagsáætluninni.
-   **Dreifa** – Línur fjárhagsáætlunar eru dreifðar úr upprunaaðstæðum fjárhagsáætlunargerðar í yfirskipuðu fjárhagsáætluninni í viðstökuaðstæður æu tengdri fjárhagsáætlun.
-   **Nota úthlutunarreglur fjárhags** - Línur fjárhagsáætlunargerðar er dreift úr upprunaaðstæður fjárhagsáætlunargerðarinnar til viðtökuaðstæðna, á grundvelli úthlutunarreglu fjárhags sem er valin.
-   **Afrita úr fjárhagsáætlunargerð** – hægt er að velja aðra fjárhagsáætlunargerð sem nota á sem uppruna úthlutunar.

### <a name="stage-allocations"></a>Stigsúthlutanir

Stigsúthlutanir eru notaðar til að úthluta sjálfkrafa línum fjárhagsáætlunar á meðan á verkflæðisferli stendur. Þegar stigsúthlutanir eru notaðar, er hægt að stofna og breyta fjárhagsáætlunarlínur í viðtökuaðstæðum án íhlutunar undirbúningsaðila fjárhagsáætlunargerðar eða skoðunarmanns.

Þegar sett er upp stig úthlutunar tengirðu verkflæði fjárhagsáætlunargerðar og stig við áætlun úthlutunar. Verkflæði fjárhagsáætlunargerðar verður að vera tengt verkflæði Fjárhagsáætlunar sem notar sjálfvirka verkflæðið sem ****Úthlutun á stigi fjárhagsáætlunargerðar****. Þegar verkflæði nær tilgreindu stigi, á úthlutun sér sjálfkrafa stað. Hægt er að nota þessa sjálfvirku verki til að stofna línur fjárhagsáætlunargerðar í nýjar aðstæður. 

Í dæmaskemað sem birtist fyrr í þessum grein, er úthlutun framkvæmd til að flytja upphæðir úr fjárhagsáætlun og aðstæður í Grunnlínustig höfuðstöðva í aðra fjárhagsáætlun og aðstæður í áætlunarstigi söludeildar. Eftirfarandi skýringarmynd sýnir viðeigandi hluta dæmaskema.

[![Vöruúthlutun](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Þar að auki, í dæmaskema, er uppsöfnun er gert úr fjárhagsáætlunum og aðstæðum innan sendu stigi söludeildar í yfiráætlun í stig Samantektar höfuðstöðva. Eftirfarandi skýringarmynd sýnir viðeigandi hluta dæmaskema.

[![Uppsöfnun](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Forgangur

Einnig er hægt að nota forganga fjárhagsáætlunargerðar til að skilgreina tegundir og markmið fyrir fjárhagsáætlanir sem hefur verið sett upp. Einnig má nota forgangar til að skipuleggja flokka og meta nokkrar fjárhagsáætlanir. Til dæmis er hægt að stofna forgangsröðun fjárhagsáætlunar fyrir heilsu og öryggi og meta síðan fjárhagsáætlanir sem eru úthlutaðar því forgang. Einnig má úthluta tölu á vægi fjárhagsáætlunargerða þvert á allar fjárhagsáætlanir.

### <a name="columns-and-layouts"></a>Dálkar og útlit

Tölur fjárhagsáætlunar birtast á fjárhagsáætlun í línum og dálkum. Fyrst þarf að skilgreina dálka og síðan er hægt að stofna snið til að skilgreina framsetningu dálka. 

Til að skilgreina dálk, veldu aðstæður fjárhagsáætlunargerðar. Línuupphæðir úr þeim aðstæður eru sýndar á fjárhagsáætluninni. Hægt er að velja tímabil til að sía upphæð, og einnig er hægt að nota síur sem eru byggðar á fjárhagslykil. 

Þegar verið er að skilgreina útlit, veldu fjárhagsvíddarsamstæðu til að stofna línur fjárhagsáætlunargerðar sem á að birta þegar, og veljið dálka sem útlitseiningar. Hægt er að stofna margar útlit þannig að fjárhagsáætlun sýnir gögnin sem óskað er eftir á mismunandi stigum í ferli fjárhagsáætlunargerðar. 

Auk dálka fyrir áætlunarupphæðir, er hægt að skilgreina dálka fyrir verk, tillagt verk, eign og svæði tillagðrar eignar úr fjárhagsáætlunargerðar. Einnig er hægt að skilgreina dálka fyrir áætlaðar stöður. Þessi valkostur er mjög gagnlegur þegar þarf að greina áætlanir starfsfólks . 

Fyrir dæmaskema gætirðu viljar stofna dálka fyrir Sölu PY, Samninga, og Spáaðstæður (eftirfarandi dæmi sýnir viðeigandi hluta skema). síðan Er hægt sundurgreina eina eða allar þessar aðstæður í aðskildum dálkum fyrir hvern ársfjórðung fjárhagsárs, þannig að stjórnandi söludeild getur nákvæmlega fært inn spárupphæðir fyrir hvert tímabil.

[![Dálkar](./media/columns.png)](./media/columns.png) 

Þú tilgreinir einnig hvort hverja útlitseining (dálk) er hægt að breyta, og hvort hún er tiltæk í vinnublaðssniðmát sem er stofnuð fyrir það útlit. Fyrir Dæmaskema, í útliti sem er notað fyrir áætlunarstig, eru spárdálkar hægt að breyta, meðan dálkar PY Sölu og Samninga eru skrifvarin.

### <a name="templates"></a>Sniðmát

Í **Útlit** hluta í **skilgreiningu fjárhagsáætlunargerðar** síðu er einnig er hægt að mynda, skoða eða hlaða upp Excel sniðmát. Þessi sniðmát eru vinnubækur sem eru tengdar hverjum fjárhagsáætlunargerðar til að veita frekari getu fyrir greiningu, leitni og innfærslu gagna. 

Hægt er að mynda, skoðið eða hlaða upp sniðmát fyrir hvert útlit. Þegar sniðmát er myndað, er útlitið læst og ekki er hægt að breyta. Þessi læsing hjálpar til við að tryggja að snið sniðmáts samræmis útliti fjárhagsáætlunargerðar og innihalda sömu gögn. Eftir að sniðmát er myndað er hægt að skoða og breyta. Til dæmis hægt að bæta við gröfum við sniðmátið eða frekar sérsníða útlit hennar.

> [!NOTE] 
> Sniðmátið á að vista á stað sem notandi hefur aðgang að, þannig að það hægt að hlaða upp í útlitið eftir að breytingum er lokið. Þannig verður sniðmátið notað með fjárhagsáætlunargerðir sem nota útlitið.

### <a name="descriptions"></a>Lýsingar

Lýsingar sem hægt er að úthluta í **Útlit** hlutanum eru notaðir til að birta nafn fjárhagsvíddar sem er innifalin í útliti. Til dæmis gæti fyrirtækis viljað birta heiti aðallykilsins við númer aðallykilsins í fjárhagsáætlun, en gæti viljað sleppa nöfn aðrar fjárhagsvíddir til að forðast að skapa ringulreið í birtingu.

## <a name="setting-up-budget-planning-processes"></a>Setja upp ferli fjárhagsáætlunargerðar

Eftir að lokið hefur verið við að skilgreina fjárhagsáætlunargerð, er hægt að setja upp ferli fjárhagsáætlunargerðar á **ferli Fjárhagsáætlunargerðar ** síðu. Fjárhagsáætlunarferli eru safn reglna sem ákvarðar hvernig hægt er að uppfæra, beina, endurskoða og samþykkja fjárhagsáætlanir innan stigveldis fyrirtækisins sem gerir fjárhagsáætlunina. 

Fyrir hverja ferli fjárhagsáætlunargerðar, skal velja fyrst ferli fjárhagsáætlunar og fjárhag. Hver ferli fjárhagsáætlunargerðar tengist ferli aðeins einnar ferli fjárhagsáætlunar og eitt fjárhags. Veldu síðan stigveldi fyrirtækis fjárhagsáætlunar á **stjórnun ferlis fjárhagsáætlunargerðar** Flýtiflipa, og úthluta verkflæði fjárhagsáætlunargerðar á allar ábyrgðarstöðvar í fyrirtækinu sem birtast í hnitanetinu. 

Til að úthluta eða breyta verkflæði fjárhagsáætlunar fyrir svipaðar ábyrgðarstöðvar, smellið **úthluta verkflæði** og veljið síðan fyrirtækisgerð til að beinast að og verkflæði fjárhagsáætlunar til að nota. Verkflæðisauðkenni fjárhagsáætlunar sem er í tengslum við hvert verkflæði fjárhagsáætlunargerðar er bætt við hnitanet sjálfkrafa. 

Þegar reglur stigs og sniðmát eru skilgreind í **reglur og útlit fjárhagsáætlunargerðar** flýtiflipa, er hægt að skilgreina mismunandi safn reglna og sjálfgefin útlit fyrir hvert stig fjárhagsáætlunargerðar. Til dæmis áætlunarstig söludeildar getur leyft notendum að breyta línum í fjárhagsáætlun en hindra notendur í að bæta línum við. Sent stig leygir notendum að skoða línur, en ekki að bæta við eða breyta þeim, þar sem vinnu á stiginu hefur verið lokið og breytingar á fjárhagsáætlanir verður að koma í veg fyrir. Til að velja útlit sem eru tiltækar fyrir fjárhagsáætlunargerðir, smellt er á  **Önnur útlit**. 

Einnig er hægt að velja forganga fjárhagsáætlunargerðar á **skorður á forgangi fjárhagsáætlunargerðar** flýtiflipa. Hægt er að velja síðan forganga á fjárhagsáætlununum. 

Síðasta skrefið er að virkja ferli fjárhagsáætlunargerðar á **Aðgerðir** valmyndaratriði, ekki er hægt að nota ferli fjárhagsáætlunargerðar fyrr en það hefur verið gert virkt. 

Á **Aðgerðir** valmyndinni, er Einnig hægt að stofna nýja ferli með því að afrita ferli sem þegar er til. Þessi aðgerð er gagnleg fyrir fyrirtæki sem fylgja sama ferli flæðis í hverju ferli fjárhagsáætlunar, og gera nokkrar breytingar eða engar breytingar. 

Annað gagnlegt skipun í **Aðgerðir** valmyndinni er **Skoða stöðu ferlis fjárhagsáætlunar**. Þessi skipun sýnir myndrænt fjárhagsáætlunargerðir innan ferlis, með viðeigandi gögnum, eins og í verkflæðisstaða áætlunar, samantektir eftir upphæð og einingu og eins smells flettingu í fjárhagsáætlunargerðir sjálfar.

[![Ferli fjárhagsáætlunargerðar](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)





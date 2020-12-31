---
title: Yfirlit fjárhagsáætlunargerðar
description: Þetta efni lýsir gerð fjárhagsáætlunar. Það inniheldur upplýsingar sem geta hjálpað við að skilgreina fjárhagsáætlunargerð og setja upp ferli fjárhagsáætlunargerðar.
author: ryansandness
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3744fd823576b597b4550008338e3cc96cb585d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444506"
---
# <a name="budget-planning-overview"></a>Yfirlit fjárhagsáætlunargerðar

[!include [banner](../includes/banner.md)]

Þetta efni lýsir gerð fjárhagsáætlunar. Það inniheldur upplýsingar sem geta hjálpað við að skilgreina fjárhagsáætlunargerð og setja upp ferli fjárhagsáætlunargerðar.

## <a name="overview-of-budget-planning"></a>Yfirlit fjárhagsáætlunargerðar

Fyrirtæki getur skilgreint fjárhagsáætlunargerðar og sett síðan upp ferli fjárhagsáætlunargerðar til að uppfylla þeirra fyrirtækisreglur, ferlum og kröfur fyrir undirbúning fjárhagsáætlunar. Þegar þú skilur hugtök og orðaforða sem eru notuð í Microsoft Dynamics 365 Finance, verður auðveldara fyrir þig að innleiða gerð fjárhagsáætlunar í þínu fyrirtæki.

### <a name="key-terms"></a>Lykilhugtök

- **Fjárhagsáætlunarferli** Ferli fjárhagsáætlunargerðar ákvarðar hvernig hægt er að uppfæra, beina, endurskoða og samþykkja fjárhagsáætlanir innan stigveldis fyrirtækisins fyrir fjárhagsáætlunarferlið. Ferli fjárhagsáætlunargerðar er tengd ferli fjárhagsáætlunar og fyrirtæki gegnum lögaðila.
- **Fjárhagsáætlunargerðir** – fjárhagsáætlunargerðir sem innihalda gögn fjárhagsáætlunar fyrir ferli fjárhagsáætlunar. Hægt er að hafa margar fjárhagsáætlanir sem eru notaðir í mismunandi tilgangi. Til dæmis getur þú notað fjárhagsáætlanir til að búa til fjárhagsáætlunarupphæðir fyrir mismunandi skipulagseiningar. Þú getur líka notað þau til að gera samanburð og taka upplýstar ákvarðanir.
- **Aðstæður fjárhagsáætlunargerðar** – aðstæður fjárhagsáætlunargerðar skilgreina gagnategundir fyrir fjárhagsáætlanir. Skilgreina aðstæður fjárhagsáætlunargerðar til að styðja peningalega klasa og aðra mælieiningarklasa, eins og magn. Dæmi um peningalegir aðstæður fjárhagsáætlunargerðar eru „Deild fyrra árs” og „Deildarbeiðnir”. Dæmi um aðstæður fjárhagsáætlunargerðar sem nota magn eru „stuðningssímtöl fyrir fyrra ár” og „jafngildi starfsráðningarstuðuls fulls starfs (FTE)”.
- **Stig fjárhagsáætlunargerðar** – stig Fjárhagsáætlunargerðar skilgreina skrefin sem fjárhagsáætlun fylgir frá upphafi til endanlegs samþykkis. Áætlunarstig áætlunar er skipað í verkflæði fjárhagsáætlunargerðar.
- **Verkflæði fjárhagsáætlunargerðar** – verkflæði Fjárhagsáætlunargerð er samsett úr og skilgreinir stig fjárhagsáætlunargerðar. verkflæði fjárhagsáætlunargerðar eru tengdar við verkflæði fyrir fjárhagsáætlanir. Verkflæði fjárhagsáætlunar eru sjálfvirkar og handvirkar vinnslur sem flytja fjárhagsáætlanir í gegnum stig fjárhagsáætlunargerðar.

[![Hugtök fjárhagsáætlunargerðar](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Dæmigerð verkefni

Hægt er að nota fjárhagsáætlunargerðar til að framkvæma eftirfarandi verkefni:

- Stofna fjárhagsáætlanir til að skilgreina áætlaðar tekjur og útgjöld fyrir ferli fjárhagsáætlunar.
- Greina og uppfæra fjárhagsáætlanir fyrir margar aðstæður.
- Hægt er að sjálfvirkt beina fjárhagsáætlun, ásamt vinnublöðum, réttlætingarskjöl og önnur viðhengjum, til yfirferðar og samþykkis.
- Sameina margar fjárhagsáætlunargerðir úr neðri stigum fyrirtækis í einni yfirfjárhagsáætlunargerð á hærra stigi. Einnig er hægt að þróa eina fjárhagsáætlunargerð á hærra stigi fyrirtækisins og úthluta fjárhagsáætlun á neðri stig.

Fjárhagsáætlunargerð er samþætt við aðrar einingar. Því er hægt að hafa með upplýsingar úr fyrri fjárhagsáætlanir, raunútgjöld, eignir og mannauður. Þar sem Fjárhagsáætlunargerð er einnig samþætt Microsoft Excel og Microsoft Word geturðu nota þessi tæki til að vinna með gögn fjárhagsáætlunargerðar. Til dæmis getur stjórnandi fjárhagsáætlunar flutt út deildabeiðni um fjárhagsáætlun í Excel vinnublað úr aðstæðum fjárhagsáætlunargerðar. Gögnin er síðan hægt að greina, uppfæra og setja upp í töflu í vinnublaðinu og birta síðan aftur í línum fjárhagsáætlunargerðar.

## <a name="configuring-budget-planning"></a>Skilgreining fjárhagsáætlunargerðar

Virkni sem kynnt var í Dynamics 365 Finance útgáfu 10.0.9 (apríl 2020) inniheldur eiginleika sem hjálpar til við að bæta afköst þegar þú notar hnappinn **Birta** til að uppfæra núverandi skrár í Excel og birta þær síðan aftur til viðskiptavinarins. Þessi aðgerð flýtir fyrir uppfærsluferlinu og hjálpar einnig til við að draga úr líkum á því að lokað verði á uppfærslu þegar þú uppfærir margar skrár í einu. Til að gera þennan möguleika tiltækan skaltu fara í vinnusvæðið **Stjórnun eiginleika** og kveikja á eiginleikanum **Fínstilling fyrirspurnar fjárhagsáætlunar um afköst** undir **Fjárhagsáætlanir**. Við mælum með að þú kveikir á þessum eiginleika.

Síðan **Skilgreining fjárhagsáætlunargerðar** inniheldur flestar stillingar sem þarf til að setja upp fjárhagsáætlunargerð. Eftirfarandi kaflar lýsa sumum af þáttunum sem ætti að íhuga þegar þú skilgreina fjárhagsáætlunargerðar. Þegar þú hefur lokið skilgreiningunni, geturðu sett upp ferli fjárhagsáætlunargerðar.

### <a name="budget-planning-schema-optional"></a>Skema fjárhagsáætlunargerðar (valfrjálst)

Valfrjálst en ráðlagt fyrsta skrefi er að stofna skema sem sýnir ferli fyrirtækis þíns við að setja fram fjárhagsáætlun. Hægt er að nota hvaða aðferð sem er til að stofna þetta skema.

Eftirfarandi skýringarmynd sýnir almennan dæmi þar sem aðskilda verkflæði fjárhagsáætlunargerðar eru stofnaðar fyrir mismunandi stig fyrirtækisins. Stig eru skilgreind í hverju verkflæði og tiltekin tilvikum er úthlutað á hverju stigi til að halda gögnum fjárhagsáætlunar. Verkum er lokið til að flytja gögn úr einu stigi í næsta. Til dæmis upphæðir er hægt að úthluta eða steypt saman í mismunandi lykla, samþykki eða öðrum skoðunarferlum. Á þessari mynd sýnir skáletraður texti aðstæður sem er ekki hægt að breyta í stigi, eða gögn sem eru söguleg eða hefur verið samþykkt á fyrra stig og því ætti ekki að breyta.

[![Almennt skema fjárhagsáætlunargerðar](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Eftirfarandi mynd sýnir dæmi þar sem höfuðstöðvar fyrirtækis áætla grunnlínuupphæðir fyrir upphaflega fjárhagsáætlunar og dreifa þeim á söludeildirnar. Söludeildirnar meta síðan og senda sína spá aftur í höfuðstöðvar þar sem fjárhagsáætlunarstjóri birtir og leiðréttir spá. Loks sendir fjárhagsáætlunarstjóri leiðrétt upphæð fjárhagsáætlunar til framkvæmdastjóra fyrir yfirferð (CFO), síðustu leiðréttingar og samþykki.

[![Dæmi um skema fjárhagsáætlunargerðar](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Stigveldi fyrirtækis fyrir fjárhagsáætlunargerð

Á **stigveldi Fyrirtækis** síðu er hægt að tilgreina stigveldi fyrirtækis sem stigveldi fjárhagsáætlunargerðar fyrir hverju ferli fjárhagsáætlunargerðar. Stigveldi fjárhagsáætlunargerðar þarf ekki að samsvara stöðluðu stigveldi fyrirtækis sem notað er í öðrum tilgangi. Þar sem þetta stigveldið er notuð til að safna og dreifa gögn, gætirðu vijað nota annað skipulag. Í dæmaskema eru söludeildirnar undir stigi höfuðstöðvar sem inniheldur deildir fjárhagsáætlunar og fjármála. Skipanin sem er notuð til að stjórna aðgerðum fyrir söludeildirnar er líklega ólík þessu skipulagi. Aðeins eitt stigveldi fyrirtækis getur verið úthlutað á hvert ferli fjárhagsáætlunargerðar.

Nánari upplýsingar, sjá [Fyrirtæki og stigveldi fyrirtækis](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Notandaöryggi

Fjárhagsáætlunargerð getur farið að einu af tveimur öryggislíkönum til að skilgreina notandaheimildir. Til að tilgreina öryggislíkan stillirðu færibreytna fjárhagsáætlunargerðar á **skilgreiningu fjárhagsáætlunargerðar** síðu.

### <a name="budget-planning-workflows-stages"></a>Verkflæðisstig fjárhagsáætlunargerðar

Verkflæði fjárhagsáætlunargerðar eru notuð með verkflæði fyrir Fjárhagsáætlun til að stjórna stofnun og þróun fjárhagsáætlana.

Verkflæði fjárhagsáætlunargerðar samanstendur af röð stiga sem fjárhagsáætlunargerð færist í gegnum. Hvert verkflæði fjárhagsáætlunargerðar er tengt við verkflæði fyrir fjárhagsáætlun. Verkflæði fjárhagsáætlunar eru ein gerð af verkflæði sem eru notuð alls staðar í Dynamics 365 Finance. Þau beina fjárhagsáætlunum, ásamt vinnublöðum, réttlætingum og viðhengjum, í gegnum fyrirtækið til yfirferðar og samþykkis.

Þú stofnar verkflæði fjárhagsáætlunargerðar í hlutanum **verkflæðisstig** á síðunni **Skilgreining fjárhagsáætlunargerðar**. Þar er hægt að velja stig og verkflæði fjárhagsáætlunar sem verður notuð og skilgreina viðbótarstillingar.

Góð regla er að stofna verkflæði fjárhagsáætlunargerðar fyrir hvert stig í stigveldi fjárhagsáætlunar. Síðan úthlutarðu verkflæði fjárhagsáætlunar sem inniheldur einingar sem samsvara stig í verkflæði fjárhagsáætlunargerðar. Í dæmaskemað sem birtist fyrr í þessu efni verður eitt verkflæði fjárhagsáætlunargerðar stofnað fyrir söludeildirnar og annað verður stofnað fyrir höfuðstöðvarnar. Verkflæði fjárhagsáætlunar flytur fjárhagsáætlunargerðir gegnum stig.

Þú stofnar verkflæði fjárhagsáætlunar fyrir fjárhagsáætlunargerð á síðunni **Verkflæði fjárhagsáætlunargerðar**. Ferlinu svipar til ferlis til að stofna önnur verkflæði. Eftirfarandi skýringarmynd sýnir dæmi um verkflæði fyrir höfuðstöðvarnar.

[![Verkflæði fjárhagsáætlunar fyrir fjárhagsáætlun](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Verkflæðið inniheldur eftirfarandi einingar:

- Úthlutun til söludeildanna og uppsöfnun á sendingum þeirra
- Mat fjárhagsætlunarstjóra
- Samþykkt á CFO
- Tilfærslur sviðsetningar er skipt milli hvers áfanga í verkflæði fjárhagsáætlunargerðar

Þú úthlutar verkflæði fjárhagsáætlunar á hvert verkflæði fjárhagsáætlunargerðar í hlutanum **verkflæðisstig** á síðunni **Skilgreining fjárhagsáætlunargerðar**.

### <a name="parameters-scenarios-and-stages"></a>Færibreytur, aðstæður og stig

Upprunalegar stillingar á **skilgreiningu fjárhagsáætlunargerðar** síðu gera mögulegt að stofna nokkrar einingar fyrir síðari skilgreiningarskref:

- **Færibreytur** – Færibreytur skilgreina öryggisreglur sem á að nota á fjárhagsáætlanir og sjálfgefna fjárhagsvíddir sem á að nota þegar notendur kafa í upphæðir í aðstæðum fjárhagsáætlunargerðar.
- **Aðstæður** – Aðstæður búa yfir flokkum gagna sem óskað er fyrir fjárhagsáætlanir. Skilgreina aðstæður fjárhagsáætlunargerðar til að styðja peningalega klasa og aðra mælieiningarklasa, eins og magn. Í fjárhagsáætlun, tákna aðstæður eina útgáfu af gögnum fjárhagsáætlunargerðar. Dæmi um peningalegar aðstæður fjárhagsáætlunargerðar eru „sala fyrra árs” og „Undirritaðir samningar”. „Fjöldi sölusímtala” og „jafngildi starfsráðningarstuðuls fulls starfs” eru dæmi um aðstæður sem nota magn.
- **Stig** - Stig skilgreina skref sem fjárhagsáætlun fer eftir frá upphafi til endanlegs samþykkis. Dæmi um stig fjárhagsáætlunargerðar eru „HQ-samantekt”, „Yfirferð framkvæmdastjóra” og „Endanleg”.

### <a name="allocation-schedules"></a>Úthlutunaráætlanir

Í fjárhagsáætlunargerðar, er hægt að úthluta upphæðir eða magn á línur fjárhagsáætlunargerðar úr einni aðstæður í öðrum aðstæðum eða jafnvel í sömu aðstæður. Til dæmis gætirðu úthlutað upphæðum eða magni á sömu aðstæður eigi að gera breytingar á fjárhagsvíddir eða dagsetningar upphæða í þeim aðstæðum. Hægt er að framkvæma úthlutun innan fjárhagsáætlunar eða frá einni fjárhagsáætlun til annarrar.

Úthlutunaráætlanir úthluta sjálfkrafa fjárhagsáætlunarlína við verkflæðisferli. Hægt er að gera úthlutanir með því að nota eitthvað af eftirfarandi aðferðum í listanum **Úthlutunaraðferð**:

- **Úthlutun yfir tímabil** – Þú notar úthlutunarlykill tímabils til að úthluta fjárhagsáætlunarlínum úr upprunaaðstæður fjárhagsáætlunargerðarinnar yfir mörg tímabil í viðtöku aðstæðum.

    > [!NOTE]
    > Áður en hægt er að úthluta yfir tímabil þarf að setja upp úthlutunarlykla tímabils á síðunni **Flokkar tímabilsúthlutunar**.

- **Úthluta á víddir** – Línur fjárhagsáætlunar er úthlutað úr upprunalegum aðstæðum fjárhagsáætlunar yfir fjárhagsvíddir í viðtökuaðstæðum.

    > [!NOTE]
    > Áður en hægt er að úthluta á víddir þarf að setja upp úthlutunarskilmála fjárhagsáætlunar á síðunni **Úthlutunarskilmálar fjárhagsáætlunar**.

- **Samanlagt** – Línur fjárhagsáætlunar eru safnað úr upprunaaðstæðum fjárhagsáætlunargerðar í tengdri fjárhagsáætlun í viðstökuaðstæðum í yfirskipuðu fjárhagsáætluninni.
- **Dreifa** – Línur fjárhagsáætlunar eru dreifðar úr upprunaaðstæðum fjárhagsáætlunargerðar í yfirskipuðu fjárhagsáætluninni í viðstökuaðstæður æu tengdri fjárhagsáætlun.
- **Nota úthlutunarreglur fjárhags** - Línur fjárhagsáætlunargerðar er dreift úr upprunaaðstæður fjárhagsáætlunargerðarinnar til viðtökuaðstæðna, á grundvelli úthlutunarreglu fjárhags sem er valin.
- **Afrita úr fjárhagsáætlunargerð** – hægt er að velja aðra fjárhagsáætlunargerð sem nota á sem uppruna úthlutunar.

### <a name="stage-allocations"></a>Stigsúthlutanir

Stigsúthlutanir eru notaðar til að úthluta sjálfkrafa línum fjárhagsáætlunar á meðan á verkflæðisferli stendur. Þegar stigsúthlutanir eru notaðar, er hægt að stofna og breyta fjárhagsáætlunarlínum í viðtökuaðstæðum án íhlutunar einstaklingsins sem útbjó fjárhagsáætlunina eða skoðunarmanns.

Þegar sett er upp stig úthlutunar tengirðu verkflæði fjárhagsáætlunargerðar og stig við áætlun úthlutunar. Verkflæði fjárhagsáætlunargerðar verður að vera tengt verkflæði fjárhagsáætlunar sem notar sjálfvirka verkflæðið **Stigsúthlutun fjárhagsáætlunargerðar**. Þegar verkflæði nær tilgreindu stigi, á úthlutun sér sjálfkrafa stað. Hægt er að nota þessa sjálfvirku verki til að stofna línur fjárhagsáætlunargerðar í nýjar aðstæður.

Í dæmaskemað sem birtist fyrr í þessu efni, er úthlutun gerð til að flytja upphæðir úr fjárhagsáætlun og aðstæðum á stiginu „Grunnlína” fyrir höfuðstöðvar í aðra fjárhagsáætlun og aðstæður á stiginu „Mat” fyrir söludeildirnar. Eftirfarandi skýringarmynd sýnir viðeigandi hluta dæmaskema.

[![Vöruúthlutun](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Að auki, í dæmaskemanu, er uppsöfnun gerð úr fjárhagsáætlunum og aðstæðum í stiginu „Sent inn” fyrir söludeildina í yfiráætlun í stiginu „Samantekt” fyrir höfuðstöðvarnar. Eftirfarandi skýringarmynd sýnir viðeigandi hluta dæmaskema.

[![Uppsöfnun](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Forgangur

Einnig er hægt að nota forganga fjárhagsáætlunargerðar til að skilgreina tegundir og markmið fyrir fjárhagsáætlanir sem hafa verið sett upp. Einnig má nota forgangar til að skipuleggja flokka og meta nokkrar fjárhagsáætlanir. Til dæmis er hægt að stofna forgangsröðun fjárhagsáætlunar fyrir heilsu og öryggi og meta síðan fjárhagsáætlanir sem eru úthlutaðar því forgang. Þú getur einnig úthlutað númeri á fjárhagsáætlunaráætlanir þínar til að sýna röðun.

### <a name="columns-and-layouts"></a>Dálkar og útlit

Í fjárhagsáætlun birtast tölur fjárhagsáætlunar í línum og dálkum. Fyrst þarf að skilgreina dálka og síðan er hægt að stofna snið til að skilgreina framsetningu í þessum dálkum.

Til að skilgreina dálk, veldu aðstæður fjárhagsáætlunargerðar. Línuupphæðir úr þeim aðstæður eru sýndar í fjárhagsáætluninni. Hægt er að velja tímabil til að sía upphæð, og einnig er hægt að nota síur sem eru byggðar á fjárhagslykil.

Þegar verið er að skilgreina útlit, veldu fjárhagsvíddarsamstæðu til að stofna línur fjárhagsáætlunargerðar sem á að sýna, og veldu síðan dálka sem útlitseiningar. Hægt er að stofna margar útlit þannig að fjárhagsáætlun sýnir æskileg gögn á mismunandi stigum í ferli fjárhagsáætlunargerðar.

Auk dálka fyrir áætlunarupphæðir, er hægt að skilgreina dálka fyrir verk, tillagt verk, eign og svæði tillagðrar eignar úr fjárhagsáætlunargerðar. Einnig er hægt að skilgreina dálka fyrir áætlaðar stöður. Þessi valkostur er gagnlegur þegar þarf að greina áætlanir starfsfólks.

Fyrir t.d. skema, gætirðu viljað búa til dálka fyrir atburðarásina „PY Sala“, „Samninga“ og „Spá“. (Eftirfarandi mynd sýnir viðkomandi hluta skemans.) Síðan geturðu sundurgreint eina eða allar þessar aðstæður í aðskilda dálka fyrir hvern ársfjórðung fjárhagsárs, þannig að stjórnandi söludeildar getur nákvæmlega fært inn spárupphæðir fyrir hvert tímabil.

[![Dálkar](./media/columns.png)](./media/columns.png)

Þú tilgreinir einnig hvort hægt sé að breyta hverri útlitseiningu (dálki), og hvort hún sé tiltæk í vinnublaðssniðmáti sem er stofnuð fyrir það útlit. Fyrir dæmaskemað, í útliti sem er notað fyrir stigið „Mat”, eru dálkarnir „Spár” breytanlegir, en dálkarnir „PY-sala” og „Samningar” eru skrifvarðir.

> [!NOTE]
> Sjálfgefið að takmarkað sé við 36 dálka nema þú framlengir fjárhagsáætlunargerð með því að fylgja skrefunum í [Lengja skipulag fjárhagsáætlunar](./extending-budget-planning-layout.md).

### <a name="templates"></a>Sniðmát

Í hlutanum **Útlit** á síðunni **Skilgreiningu fjárhagsáætlunargerðar** er hægt að mynda, skoða eða hlaða upp Excel-sniðmáti fyrir hvert útlit. Þessi sniðmát eru vinnubækur sem eru tengdar hverjum fjárhagsáætlunargerðar til að veita frekari getu fyrir greiningu, leitni og innfærslu gagna.

Þegar sniðmát er myndað, er útlitið læst og ekki er hægt að breyta. Þessi læsing hjálpar til við að tryggja að snið sniðmáts samræmis útliti fjárhagsáætlunargerðar og innihalda sömu gögn. Eftir að sniðmát er myndað er hægt að skoða og breyta. Til dæmis hægt að bæta við gröfum við sniðmátið eða frekar sérsníða útlit hennar.

> [!NOTE]
> Sniðmát skal vista á stað sem notandi hefur aðgang að, þannig að það hægt að hlaða upp í útlitið eftir að breytingum er lokið. Þannig verður sniðmátið notað með fjárhagsáætlunargerðir sem nota útlitið.

### <a name="descriptions"></a>Lýsingar

Í hlutanum **Útlit** er hægt að úthluta lýsingum til að sýna heiti fjárhagsvíddar sem er innifalin í útliti. Til dæmis gætu fyrirtæki viljað sýna nafn aðalreiknings við hliðina á aðalreikningsnúmerinu í fjárhagsáætlun. Hins vegar gæti það viljað sleppa nöfnum annarra fjárhagsvídda, til að forðast ringulreið á skjánum.

## <a name="setting-up-budget-planning-processes"></a>Setja upp ferli fjárhagsáætlunargerðar

Eftir að lokið hefur verið við að skilgreina fjárhagsáætlunargerð, er hægt að setja upp ferli fjárhagsáætlunargerðar á **ferli Fjárhagsáætlunargerðar** síðu. Fjárhagsáætlunarferli eru safn reglna sem ákvarðar hvernig hægt er að uppfæra, beina, endurskoða og samþykkja fjárhagsáætlanir innan stigveldis fyrirtækisins sem gerir fjárhagsáætlunina.

Fyrir hverja ferli fjárhagsáætlunargerðar, skal velja fyrst ferli fjárhagsáætlunar og fjárhag. Hver ferli fjárhagsáætlunargerðar tengist ferli aðeins einnar ferli fjárhagsáætlunar og eitt fjárhags. Síðan velurðu stigveldi fyrirtækis fjárhagsáætlunar á **stjórnun ferlis fjárhagsáætlunargerðar** Flýtiflipa, og úthluta verkflæði fjárhagsáætlunargerðar á allar ábyrgðarstöðvar í fyrirtækinu sem birtast í hnitanetinu.

Til að úthluta eða breyta verkflæði fjárhagsáætlunar fyrir svipaðar ábyrgðarstöðvar, velurðu **úthluta verkflæði** og veljið síðan fyrirtækisgerð til að beinast að og verkflæði fjárhagsáætlunar til að nota. Verkflæðisauðkenni fjárhagsáætlunar sem er í tengslum við hvert verkflæði fjárhagsáætlunargerðar er sjálfkrafa bætt við hnitanetið.

Þegar reglur stigs og sniðmát eru skilgreind í **reglur og útlit fjárhagsáætlunargerðar** flýtiflipa, er hægt að skilgreina mismunandi safn reglna og sjálfgefin útlit fyrir hvert stig fjárhagsáætlunargerðar. Til dæmis getur stigið „Mat” fyrir söludeildirnar leyft notendum að breyta línum í fjárhagsáætlun en hindra notendur í að bæta línum við. Stigið „Sent” leyfir notendum að skoða línur, en ekki að bæta við eða breyta þeim, þar sem vinnu á stiginu hefur verið lokið og breytingar á fjárhagsáætlanir verður að koma í veg fyrir. Til að velja útlit sem eru tiltækar fyrir fjárhagsáætlunargerðir, velurðu **Önnur útlit**.

Einnig er hægt að velja forganga fjárhagsáætlunargerðar á **skorður á forgangi fjárhagsáætlunargerðar** flýtiflipa. Hægt er að velja síðan forganga á fjárhagsáætlununum.

Lokaskrefið er að virkja fjárhagsáætlunargerðina með því að nota valmyndina **Aðgerðir**. Ekki er hægt að nota ferli fjárhagsáætlunargerðar fyrr en það hefur verið virkjað.

Einnig er hægt að nota valmyndina **Aðgerðir** til að stofna nýtt ferli með því að afrita ferli sem þegar er til. Þessi aðgerð er gagnleg fyrir fyrirtæki sem fylgja sama ferli flæðis í hverju ferli fjárhagsáætlunar, og gera nokkrar breytingar eða engar breytingar.

Annað gagnlegt skipun í **Aðgerðir** valmyndinni er **Skoða stöðu ferlis fjárhagsáætlunar**. Þessi skipun sýnir myndrænt fjárhagsáætlunargerðir í ferli, með viðeigandi gögnum, eins og verkflæðisstöðu áætlana, samantektir eftir upphæð og einingu og eins smells flettingu í fjárhagsáætlunargerðir sjálfar.

[![Ferli fjárhagsáætlunargerðar](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)

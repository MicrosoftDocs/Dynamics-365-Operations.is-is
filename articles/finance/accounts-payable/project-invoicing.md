---
title: Reikningsfærsla verks
description: Þetta efnisatriði veitir yfirlit yfir reikningsfærslu verka fyrir tíma- og efnisverk og verkefni á föstu verði. Hún inniheldur upplýsingar um reikningstillögur (bráðabirgðareikningar), reikningsstjórnun, reikningsfærslu áfangareikninga, reikningsfærslu lánardrottna og kreditnótur.
author: TaylorVH
ms.date: 07/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: zezhangzhao
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: bdb5c9162ab85632c8780a737df0998e4cd34f0c
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733849"
---
# <a name="project-invoicing"></a>Reikningsfærsla verks

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir reikningsfærslu verka fyrir tíma- og efnisverk og verkefni á föstu verði. Hún inniheldur upplýsingar um reikningstillögur (bráðabirgðareikningar), reikningsstjórnun, reikningsfærslu áfangareikninga, reikningsfærslu lánardrottna og kreditnótur.

Verkgerðin ákvarðar hvaða reikningsfærsluaðferð skal beitt. Aðeins er hægt að reikningsfæra tvær ytri verkgerðir (Tíma- og efnisverk og fastverðsverk). Tíma- og efnisverk og fastverðsverk eru alltaf tengd við verksamning.

-   **Fastverðsverk** – reikningsupphæð viðskiptavinar er byggð á greiðsluáætlunum reikninga. Reikningsfærsla er framkvæmd í gegnum áfangareikningsuppsetningu sem einnig er vísað til sem greiðsluáætlunar. Hægt er að reikningsfæra fastverðsverk fyrir hvert verk eða fyrir hvern verksamning.
-   **Tíma-og efnisverk** - Reikningsupphæðin viðskiptavinar byggist á færslulínum sem eru færðar inn í verk. Hægt er að reikningsfæra færslur fyrir hvert verk eða fyrir hvern verksamning.

Þrjár leiðir eru til að tengja tíma- og efnisverk og fastverðsverk við reikningsverkin:

-   **Áfangareikningsfærsla** - Hægt er að reikningsfæra tíma- og efnisverk og fastverðsverk með áfangareikningi. Tvær gerðir af uppsetningum áfangareiknings eru nauðsynlegar, einn fyrir hverja gerð verks.
-   **Reglubundin reikningsfærsla** - Hægt er að reikningsfæra færslur þvert á verk með reglubundnum aðgerðum. Reglubundnar aðgerðir geta veitt yfirlit yfir færslur sem á að reikningsfæra.
-   **Með því að nota kreditnótur í reikningsfærslu** - Hægt er að stofna kreditnótu bæði fyrir tíma- og efnisverk og fastverðsverk.

## <a name="invoice-proposals"></a>Reikningstillögur
Áður en reikning viðskiptavinar er stofnaður fyrir verk, er hægt að stofna bráðabirgðareikningur, eða reikningstillögu. Í reikningstillögu, hægt er að velja verkfærsla til að taka með í verkreikning. Þú getur síðan farið yfir upplýsingar um reikning áður en bókað er verkreikningur og sendir til viðskiptavinar eða öðrum uppruni fjármögnunar.

### <a name="creating-invoice-proposals"></a>Stofnun reikningstillaga

Hægt er að stofna reikningstillögur með því að velja færslu handvirkt úr lista yfir tiltækar færslur fyrir tiltekið verk. Einnig er hægt að setja upp reikningsreglur sem tilgreina hvenær á að stofna sjálfkrafa reikningstillögu. Til dæmis er hægt að búa til reikningsreglu til að stofna reikningstillögu þegar vinna við verk er 25 prósent, 50 prósent, 75 prósent og 100 prósent lokið. 

Hægt er að stofna reikningstillaga fyrir eftirfarandi færslur:

-   Klukkustundir, útgjöld og aðrar verkfærslur
-   Upphæðir sem eru geymdar hjá viðskiptavinum á fyrri verkreikningum
-   Kreditnótur
-   Fjárhæðir sem viðskiptavinur greiðir til þín áður en verkefnið hefst

> [!NOTE]
> Eiginleikinn **Virkja flokkun eftir tilföngum við stofnun á reikningstillögu verks** gerir endurskoðanda verksins kleift að flokka verkfærslurnar sem eru tiltækar til innheimtu eftir tilfanginu við stofnun á nýrri tillögu að reikningstillögu verks. Hnitanetið sem sýnir tiltækar verkfærslur verður með aðskilda reiti fyrir **Auðkenni tilfangs** og **Tilfang**. Þessir reitir gera kleift að sía og raða tilfangaheitinu. Slökkt er á þessum eiginleika að sjálfgefnu. Hægt er að virkja hann með því að nota síðuna **Eiginleikastjórnun** (**Vinnusvæði > Eiginleikastjórnun**). Hafið samband við kerfisstjórann til að fá aðstoð við að kveikja á eiginleikanum.

Í reikningstillaga er hægt að stofna færslur fyrir þóknun í reikningstillögu. Einnig er hægt að breyta söluverði á klukkutíma, kostnaði, vöru og þóknunarfærslum. Þegar reikningstillaga er bókuð er uppfært verð og færslum bætt við skýrslur um verk og færslusögu. 

Til að stofna marga reikninga viðskiptavinar fyrir verk verður að stofna reikningstillögu fyrir hvern reikning. Til dæmis er hægt að stofna reikninga sem byggjast á færslugerð. Til að tilgreina tíma á einum reikningi viðskiptavinar og vörur á öðrum reikningi þarf að búa til sérstakar reikningstillögur fyrir tímafærslur og gjaldfærslur. 

Ef verk hefur fleiri en einn uppruni fjármögnunar er hægt að stofna aðskilda reikningstillögu fyrir hvern uppruni fjármögnunar. Í **Úthlutanir fjármögnunarreglu** síðu, er hægt að tilgreina hlutfall færsluupphæðar sem á að úthluta á hvern uppruni fjármögnunar, og upprunann til að bóka sléttunarmun á.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Búa til reikninga viðskiptavina frá reikningstillaga

Eftir að þú stofnar og bókar reikningstillögu er reikningur viðskiptavinar sjálfvirkt stofnaður fyrir færslur sem eru í reikningstillögunni. 

Hægt er að bæta við eða eyða færslum í reikningstillögu áður en hún er bókuð. Til dæmis er hægt að fjarlægja kostnaðarfærslur sem voru bókaðar á verk, en er ekki hægt að rukka viðskiptavin fyrir. 

Ef fyrirtækið þitt krefst þess að farið sé yfir reikningstillögur áður en þær eru bókaðar, gæti þurft að samþykkja reikningstillöguna gegnum verkflæðið „Endurskoða reikningstillögur verks“ áður en hún er bókuð.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>Skoða upplýsingar um styrki á listasíðum verkreikninga

Notendur í opinbera geiranum geta bætt **Kenni styrks** og **Heiti styrks** við listasíðurnar **Reikningstillögur verks** og **Verkreikningar**. Þessi dálkar eru virkjaðir með því að nota eiginleikann **Bæta við styrkupplýsingum á listasíður verkreiknings**. Slökkt er á þessum eiginleika að sjálfgefnu og hægt er að virkja hann í **Vinnusvæði > Eiginleikastjórnun**. Hafið samband við kerfisstjórann til að fá aðstoð við að kveikja á eiginleikanum.

## <a name="on-account-invoicing"></a>Reikningsfærslur áfangareikninga
Upphæðin sem færð er inn fyrir verk í áfangareikning á grundvelli tímasetningar, hlutfall þess sem er lokið og aðrar innheimtuskilyrða sem tilgreind eru í tengda verksamning. Upphæð er ekki reiknaður út á grundvelli klukkustundir, vörur, útgjöld eða þóknanir sem eru bókaðar í verk. 

Stofna verður áfangareikningsfærslu fyrir tíma- og efnisverk eða verk á föstu verði áður en hægt er að bæta þessari áfangareikningsfærslu við verkreikning. Á áfangareikningsfærslu færirðu inn upphæðina sem á að reikningsfæra á viðskiptavin. Til að stofna bráðabirgðareikning, til að búa til verkreikning fyrir upphæð, (reikningstillögu). Í reikningstillögu, velja áfangareikningsfærsla. Hægt er að skoða upplýsingar um áfangareikning í reikningstillögunni áður verkreikningur er stofnaður fyrir hann. 

### <a name="fixed-price-projects"></a>Fastverðsverk
Fyrir fastverðsverk, áfangareikningsfærslur eru byggð á er samþykkt við áfanga, eining eða framvindu reikningsfærslu skipan beðið sem tilgreindur er í verk. Ein lína er búin til fyrir hverja greiðslu sem verður að berast frá viðskiptavini verkefnisins. Enginn frádráttur er nauðsynlegur.

### <a name="time-and-material-projects"></a>Tíma- og efnisverk.

Fyrir Tíma- og efnisverk er hægt uppskriftavörur viðskiptavinar eða öðrum fjármögnunaraðila fyrir fyrirframgreiðslu með reikningstillaga áfangareiknings. Færa inn áfangareikningsfærslur sem ein lína. Einnig er hægt að færa inn fleiri línur sem frádrátt til að mótbóka allar fyrirframgreiðslur sem viðskiptavinurinn hefur þegar verið gerðar. Til að stofna frádráttarlínur þarf að slá inn mínusmerki á undan upphæðinni.

## <a name="invoice-control"></a>Reikningastýring
Hægt er að nota reikningsstýringu til að rekja bæði reikningsfærðar og óreikningsfærðar færslur og til að greina þær færslur á móti tilboð fyrir yfirlit frá upphafi til enda yfir verk þín úr stigi tilboðs til loka. Hægt er að sjá hvaða færslur er búið að reikningsfæra á tiltekið verk og línur sem hafa verið reikningsfærðar. Einnig er hægt að sjá einstakar færslur þannig að hægt sé að aðlaga þær eftir að þær eru bókaðar.

## <a name="invoicing-fixed-price-projects"></a>Reikningsfæra fastverðsverk
Til að reikningsfæra fastverðsverk, verður að skilgreina innheimtuáætlun og ljúktu við ferli reikningsfærslu.

### <a name="billing-schedule"></a>Reikningsáætlun

Hægt er að reikningsfæra fastverðsverk á reikningsáætlun. Reikningsáætlun er skilgreint með einum eða fleiri áfanga fyrir verkið. Fyrir hvern áfanga, hægt er að skilgreina ákveðna dagsetningu, sölugjaldmiðil, söluverð og aðgerð. 

Þú getur til dæmis sett upp eftirfarandi reikningsáætlun:

-   20 prósent þegar verksamningur er undirritaður
-   30 prósent við fyrstu afhendingu
-   15 prósent við aðra afhendingu
-   35 prósent við lokaafhendingu

### <a name="invoicing-procedure"></a>Reikningsfærsluferli

Þegar áfangagreiðslur eru tilbúnar fyrir reikningsfærslu er notað ferlið til að reikningsfæra upphæðir á áfangareikningi.

## <a name="vendor-invoicing"></a>Reikningsfærslur lánardrottins
Þegar vara pöntuð frá lánardrottni og vöru úthlutað á verk, ákvarðar línueiginleikinn sem er valinn fyrir innkaupapöntunarlínu fyrir þessa vöru hvort keypt vara er reikningsfærð á viðskiptavin. Ef sjálfgefnir línueiginleikar eru settir upp, birtast þeir fyrir vöruna innkaupapöntunarlínu (**Línuupplýsingar > Verk > Upphæðir línueiginleika**). Það eru tvær leiðir til að breyta línueiginleika:

-   Reikningsfæra viðskiptavin verksins fyrir vöruna. Til að gera þetta skal stilla línueiginleika fyrir vöruna á reikningshæft gildi í innkaupapöntuninni, og síðan reikningsfæra viðskiptavininn með því að nota rétta reikningsfærsluaðferð verks.
-   Ekki reikningsfæra viðskiptavin verksins fyrir vöruna. Til að gera þetta skal velja línueiginleikann **Reikningshæft** í innkaupapöntunarlínu fyrir vöruna. Síðan geturðu reikningsfært Innkaupapöntunin , og ekki þarf að gera frekari aðgerðir.

> [!NOTE] 
> Sjálfgefið er ekki hægt að reikningsfæra varðveislulínur losunar. Þetta þýðir að möguleikinn á að búa til reikningstillögu fyrir útgefna varðveislu er ekki virkur.

## <a name="credit-notes"></a>Kreditnótur
Þegar upphæð á reikningur viðskiptavinar hefur neikvætt gildi, er reikningurinn flokkaður sem kreditnóta. Þegar skjalið er prentað ber það titilinn „Kreditnóta." 

Þegar kreditnóta er stofnuð til að kreditfæra upphæð sem var áður reikningsfærð þarf fyrst að velja reikningsfærðu upphæðina sem á að kreditfæra. Svo er kreditnóta stofnuð með því að fylgja sama ferli sem er notað til að stofna venjulegan reikning viðskiptavinar. Þú velur færslur sem voru áður bókaðar fyrir reikning viðskiptavinar og stofna síðan og bóka tillögu að kreditnótu. 

Sama skjal getur innihaldið færslur sem eru valdar fyrir kreditfærslu, og færslur sem hafa verið bókaðar. Flokkun skjals er þá annað hvort reikningur eða kreditnóta eftir því hvort heildarupphæðin er jákvæð eða neikvæð. 

Til að kreditfæra reikningsfærða upphæð þarf fyrst að velja reikningsfærðu upphæðina sem á að kreditfæra og stofna síðan kreditnótu. Kreditnóta er stofnuð með því að fylgja sama ferli sem er notað til að mynda reikning viðskiptavinar. 

Hægt er að stofna reikning með neikvæðri upphæð; sem verður reikningur sem er flokkaður sem kreditnóta. Velja verður færslur sem voru áður bókaðar fyrir reikning viðskiptavinar og breyta síðan færslur til að stofna og prenta kreditnótu. Að undanskildum lögaðila með aðalaðsetur í Þýskalandi, er titill reikningsins "Leiðréttandi reikningur."





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

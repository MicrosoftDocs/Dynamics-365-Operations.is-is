---
title: Verkreikningur
description: "Þessi grein veitir yfirlit yfir verkreikninga fyrir Tíma- og efnisverk og fastverðsverk. Hún inniheldur upplýsingar um reikningstillögur (bráðabirgðareikningar), reikningsstjórnun, reikningsfærslu áfangareikninga, reikningsfærslu lánardrottna og kreditnótur."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76abfa35e53673f9780d1a6f8816bd24f9f8e48
ms.openlocfilehash: f09aef9cf1e516b80f908c34b2b3c3397dde8a0f
ms.lasthandoff: 03/31/2017


---

# <a name="project-invoicing"></a>Verkreikningur

[!include[banner](../includes/banner.md)]


Þessi grein veitir yfirlit yfir verkreikninga fyrir Tíma- og efnisverk og fastverðsverk. Hún inniheldur upplýsingar um reikningstillögur (bráðabirgðareikningar), reikningsstjórnun, reikningsfærslu áfangareikninga, reikningsfærslu lánardrottna og kreditnótur.

Verkgerðin ákvarðar hvaða reikningsfærsluaðferð skal beitt. Aðeins er hægt að reikningsfæra tvær ytri verkgerðir (Tíma- og efnisverk og fastverðsverk). Tíma- og efnisverk og fastverðsverk eru alltaf tengd við verksamning.

-   **Fastverðsverk** – reikningsupphæð viðskiptavinar er byggð á greiðsluáætlunum reikninga. Reikningsfærsla er framkvæmd í gegnum áfangareikningsuppsetningu sem  einnig er vísað til sem greiðsluáætlunar. Hægt er að reikningsfæra fastverðsverk fyrir hvert verk eða fyrir hvern verksamning.
-   **Tíma-og efnisverk ** - Reikningsupphæðin viðskiptavinar byggist á færslulínum sem eru færðar inn í verk. Hægt er að reikningsfæra færslur fyrir hvert verk eða fyrir hvern verksamning.

Þrjár leiðir eru til að tengja tíma- og efnisverk og fastverðsverk við reikningsverkin:

-   **Áfangareikningsfærsla ** - Hægt er að reikningsfæra tíma- og efnisverk og fastverðsverk með áfangareikningi. Tvær gerðir af uppsetningum áfangareiknings eru nauðsynlegar, einn fyrir hverja gerð verks.
-   **Reglubundin reikningsfærsla ** - Hægt er að reikningsfæra færslur þvert á verk með reglubundnum aðgerðum. Reglubundnar aðgerðir geta veitt yfirlit yfir færslur sem á að reikningsfæra.
-   **Með því að nota kreditnótur í reikningsfærslu ** - Hægt er að stofna kreditnótu bæði fyrir tíma- og efnisverk og fastverðsverk.

## <a name="invoice-proposals"></a>Reikningstillögur
Áður en reikning viðskiptavinar er stofnaður fyrir verk, er hægt að stofna bráðabirgðareikningur, eða reikningstillögu. Í reikningstillögu, hægt er að velja verkfærsla til að taka með í verkreikning. Þú getur síðan farið yfir upplýsingar um reikning áður en bókað er verkreikningur og sendir til viðskiptavinar eða öðrum uppruni fjármögnunar.

### <a name="creating-invoice-proposals"></a>Stofnun reikningstillaga

Hægt er að stofna reikningstillögur handvirkt með því að velja úr lista yfir færslur fyrir tilgreinda verkið. Einnig er hægt að setja upp reikningsreglur sem tilgreina hvenær á að stofna sjálfkrafa reikningstillögu. Til dæmis er hægt að stofna reikningsreglur til að stofna reikningstillögu þegar vinna við verkið er 25 prósent, 50 prósent, 75 prósent og 100 prósent lokið. 

Hægt er að stofna reikningstillaga fyrir eftirfarandi færslur:

-   Klukkustundir, útgjöld og aðrar verkfærslur
-   Upphæðir sem eru geymdar hjá viðskiptavinum á fyrri verkreikningum
-   Kreditnótur
-   Fjárhæðir sem viðskiptavinur greiðir til þín áður en verkefnið hefst

Í reikningstillaga er hægt að stofna færslur fyrir þóknun í reikningstillögu. Einnig er hægt að breyta söluverði á klukkutíma, kostnaði, vöru og þóknunarfærslum. Þegar reikningstillaga er bókuð er uppfært verð og færslum bætt við skýrslur um verk og færslusögu. 

Til að stofna marga reikninga viðskiptavinar fyrir verk verður að stofna reikningstillögu fyrir hvern reikning. Til dæmis er hægt að stofna reikninga sem byggjast á færslugerð. Ef óskað er að tilgreina tíma á einum reikningur viðskiptavinar og vörur á öðrum, verður að stofna reikningstillögu fyrir tímafærslur og aðskildar reikningstillögu fyrir þóknunarfærslur. 

Ef verk hefur fleiri en einn uppruni fjármögnunar er hægt að stofna aðskilda reikningstillögu fyrir hvern uppruni fjármögnunar. Í ** úthlutanir fjármögnunarreglu** síðu, er hægt að tilgreina hlutfall færsluupphæðar sem á að úthluta á hvern uppruni fjármögnunar, og upprunann til að bóka sléttunarmun.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Búa til reikninga viðskiptavina frá reikningstillaga

Eftir að þú stofnar og bókar reikningstillögu er reikningur viðskiptavinar sjálfvirkt stofnaður fyrir færslur sem eru í reikningstillögunni. 

Hægt er að bæta við eða eyða færslum í reikningstillögu áður en hún er bókuð. Til dæmis er hægt að fjarlægja kostnaðarfærslur sem voru bókaðar í verk en eru ekki reikningshæfar til viðskiptavinar. 

Ef fyrirtækið þitt krefst þess að fara yfir reikningstillögur áður en þær eru bókaðar, gæti þurft að samþykkja reikningstillögunni gegnum "endurskoða tillögur um verkreikning" áður en bókað er.

## <a name="on-account-invoicing"></a>Reikningsfærslur áfangareikninga
Upphæðin sem færð er inn fyrir verk í áfangareikning á grundvelli tímasetningar, hlutfall þess sem er lokið og aðrar innheimtuskilyrða sem tilgreind eru í tengda verksamning. Upphæð er ekki reiknaður út á grundvelli klukkustundir, vörur, útgjöld eða þóknanir sem eru bókaðar í verk. 

Þú verður að stofna í áfangareikningsfærslu fyrir tíma- og efnisverkefni eða fastverðsverk áður en hægt er að bæta við áfangareikningsfærsla við verkreikning. Á áfangareikningsfærslu færirðu inn upphæðina sem á að reikningsfæra á viðskiptavin. Til að stofna bráðabirgðareikning, til að búa til verkreikning fyrir upphæð, (reikningstillögu). Í reikningstillögu, velja áfangareikningsfærsla. Hægt er að skoða upplýsingar um áfangareikning í reikningstillögunni áður verkreikningur er stofnaður fyrir hann.

### <a name="fixed-price-projects"></a>Fastverðsverk

Fyrir fastverðsverk, áfangareikningsfærslur eru byggð á er samþykkt við áfanga, eining eða framvindu reikningsfærslu skipan beðið sem tilgreindur er í verk. Ein lína er búin til fyrir hverja greiðslu sem verður að berast frá viðskiptavini verkefnisins. Enginn frádráttur er nauðsynlegur.

### <a name="time-and-material-projects"></a>Tíma- og efnisverk.

Fyrir Tíma- og efnisverk er hægt uppskriftavörur viðskiptavinar eða öðrum fjármögnunaraðila fyrir fyrirframgreiðslu með reikningstillaga áfangareiknings. Færa inn áfangareikningsfærslur sem ein lína. Einnig er hægt að færa inn fleiri línur sem frádrátt til að mótbóka allar fyrirframgreiðslur sem viðskiptavinurinn hefur þegar verið gerðar. Til að stofna frádráttarlínur þarf að vera mínus tákn á undan upphæð.

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
Þegar vara pöntuð frá lánardrottni og vöru úthlutað á verk, ákvarðar línueiginleikinn sem er valinn fyrir innkaupapöntunarlínu fyrir þessa vöru hvort keypt vara er reikningsfærð á viðskiptavin. Ef sett er upp sjálfgefna línueiginleika, birtast þeir fyrir vöruna innkaupapöntunarlínu (Línuupplýsingar &gt; Verk &gt; Línueiginleikar). Það eru tvær leiðir til að breyta línueiginleika:

-   Reikningsfæra viðskiptavin verks fyrir vöru: Stilla línueiginleika fyrir vöru á reikningshæft gildi á innkaupapöntuninni, og reikningsfæra á viðskiptavininn með því að nota rétta reikningsfærsluaðferð verks.
-   Ekki reikningsfæra viðskiptavin verks fyrir vöru: ekki velja **Reikningshæfa** línueiginleikann á innkaupapöntunarlínu fyrir vörunnar. Síðan geturðu reikningsfært Innkaupapöntunin , og ekki þarf að gera frekari aðgerðir.

## <a name="credit-notes"></a>Kreditnótur
Þegar upphæð á reikningur viðskiptavinar hefur neikvætt gildi, er reikningurinn flokkaður sem kreditnóta. Þegar skjalið er prentað ber það titilinn „Kreditnóta." 

Þegar kreditnóta er stofnuð til að kreditfæra upphæð sem var áður reikningsfærð þarf fyrst að velja reikningsfærðu upphæðina sem á að kreditfæra. Svo er kreditnóta stofnuð með því að fylgja sama ferli sem er notað til að stofna venjulegan reikningur viðskiptavinar. Með öðrum orðum, Velja færslur sem voru áður bókaðar fyrir reikning viðskiptavinar og stofna síðan og bóka tillögu að kreditnótu. 

Sama skjal getur innihaldið færslur sem eru valdar fyrir kreditfærslu, og færslur sem hafa verið bókaðar. Flokkun skjals er þá annað hvort reikningur eða kreditnóta eftir því hvort heildarupphæðin er jákvæð eða neikvæð. 

Til að kreditfæra reikningsfærða upphæð þarf fyrst að velja reikningsfærðu upphæðina sem á að kreditfæra og stofna síðan kreditnótu. Kreditnóta er stofnuð með því að fylgja sama ferli sem er notað til að mynda reikning viðskiptavinar. 

Hægt er að stofna reikning með neikvæðri upphæð; sem verður reikningur sem er flokkaður sem kreditnóta. Velja verður færslur sem voru áður bókaðar fyrir reikning viðskiptavinar og breyta síðan færslur til að stofna og prenta kreditnótu. Að undanskildum lögaðila með aðalaðsetur í Þýskalandi, er titill reikningsins "Leiðréttandi reikningur."





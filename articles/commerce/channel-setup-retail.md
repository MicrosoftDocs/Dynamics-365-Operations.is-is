---
title: Setja upp smásölurás
description: Þetta efni lýsir því hvernig á að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8ac01f36912fa5e8a09bb4f324ef272cec737aa1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002382"
---
# <a name="set-up-a-retail-channel"></a>Setja upp smásölurás


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce styður margar smásölurásir. Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir). Hvert smásöluverslunarrás getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk. Setja verður upp allar þessar einingar áður en hægt er að stofna smásöluverslunarrás. 

Áður en smásölurás er búin til skaltu ganga úr skugga um að þú fylgir [forsendur rásar](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Stofna og stilla nýja smásölurás

1. Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Verslanir \> Allar smásöluverslanir**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.
1. Í svæðinu **Verslunarnúmer** skal gefa upp einkvæmt verslunarnúmer. Talan getur verið bók- eða tölustafir og að hámarki 10 stafir.
1. Í fellivallistanum **Lögaðili** skal slá inn viðeigandi lögaðila.
1. Í fellivallistanum **Vöruhús** slærðu inn viðeigandi vöruhús.
1. Í reitnum **Tímabelti verslunar** velurðu viðeigandi tímabelti.
1. Í fellilistanum **VSK-flokkur** velurðu viðeigandi VSK-flokk fyrir verslunina.
1. Í reitnum **Gjaldmiðill** velurðu viðeigandi gjaldmiðil.
1. Í reitnum **Heimilisfangabók viðskiptavina** gefurðu upp gilda aðsetursbók.
1. Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.
1. Í reitnum **Virkniregla** velurðu virknireglu ef við á.
1. Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir stofnun nýrrar smásölurásar.

![Ný smásölurás](media/channel-setup-retail-1.png)

Eftirfarandi mynd sýnir dæmi um smásölurás.

![Dæmi um smásölurás](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Aðrar stillingar

Það eru fjölmargar aðrar valkvæðar stillingar sem hægt er að stilla í hlutunum **Yfirlýsing/lokun** og **Ýmislegt**, miðað við þarfir smásöluverslunarinnar.

Að auki, sjá [Skjáupplýsingar fyrir sölustað (POS)](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json) til að fá upplýsingar um uppsetningu á sjálfgefinni skjáuppsetningu í hlutanum **Skjáskipulag** og [Stilla og setja upp Retail vélbúnaðarstöð](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation) fyrir uppsetningarupplýsingar um hlutann **Vélbúnaðarstöðvar**.

Eftirfarandi mynd sýnir dæmi um uppsetningarstillingu smásölurásar.

![Dæmi um stillingu smásölurásar](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Viðbótaruppsetning grunnrásar

Það eru fleiri hlutir sem þarf að setja upp fyrir rás sem er að finna í **aðgerðaglugganum** undir kaflanum **Setja upp**.

Viðbótarupplýsingar sem krafist er fyrir uppsetningu netrásar fela í sér uppsetningu á greiðslumáta, skilgreiningu reiðufjár, afhendingaraðferðum, tekju-/útgjaldalykli, hlutum, úthlutun uppfyllingarflokks og öryggishólfa.

Eftirfarandi mynd sýnir ýmsa viðbótaruppsetningarvalkosti smásölurásar á flipanum **Setja upp**.

![Setja upp rás](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Setja upp greiðsluhætti

Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í yfirlitsglugganum velurðu óskaðan greiðslumáta.
1. Í kaflanum **Almennt** skaltu gefa upp **Heiti aðgerðar** og stilla allar aðrar stillingar sem óskað er.
1. Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.

![Dæmi um greiðslumáta](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Setja upp skilgreiningar reiðufjár

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Skilgreining reiðufjár**.
1. Í aðgerðaglugganum velurðu **Nýtt** og síðan stofnarður öll gildi **myntar** og **seðla** sem eiga við.

Eftirfarandi mynd sýnir dæmi um skilgreingingu reiðufjár.

![Uppsetning á skilgreiningu reiðufjár](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Setja upp afhendingarmáta

Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í **Aðgerðarglugganum**.  

Fylgdu þessum skrefum til að breyta eða bæta við afhendingarmáta.

1. Í yfirlitsglugganum ferðu í **Einingar \> Birgðastjórnun \> Afhendingmáti**.
1. Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.
1. Í kaflanum **Smásölurásir** velurðu **Bæta við línu** til að bæta við rásinni. Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.

Eftirfarandi mynd sýnir dæmi um afhendingarmáta.

![Setja upp afhendingarmáta](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Setja upp tekju-/útgjaldalykil

Til að setja upp tekju-/útgjaldalykil skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Tekju-/útgjaldalykil**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Undir **Heiti** slærðu inn nafn.
1. Undir **Leitarheiti** slærðu inn leitarheiti.
1. Undir **Lykilgerð** færirðu inn lykilgerð.
1. Sláðu inn texta fyrir **Skilaboðalínu 1**, **Skilaboðalínu 2**, **Seðiltexta 1** og **Seðiltexta 2** eftir þörfum.
1. Undir **Bókun** slærðu inn upplýsingar um bókun.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um tekju-/útgjaldalykil.

![Setja upp tekju-/útgjaldalykla](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Setja upp hluta

Til að setja upp hluta skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Hlutar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Undir **Hlutanúmer** slærðu inn hlutanúmer.
1. Undir **Lýsing** skal færa inn lýsingu.
1. Undir **Hlutastærð** slærðu inn hlutastærð.
1. Stilla viðbótarstillingar fyrir **Almennt** og **Söluupplýsingar** eftir þörfum.
1. Í aðgerðaglugganum velurðu **Vista.**

### <a name="set-up-a-fulfillment-group-assignment"></a>Setja upp úthlutun uppfyllingarflokks

Til að setja upp úthlutun uppfyllingarflokks skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Úthlutun uppfyllingarflokks**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í fellilistanum **Uppfyllingarhópur** velurðu uppfyllingarhóp.
1. Í fellilistanum **Lýsing** skal færa inn lýsingu.
1. Í aðgerðaglugganum velurðu **Vista**.

Eftirfarandi mynd sýnir dæmi um uppstillingu úthlutunar uppfyllingarflokks.

![Setja upp úthlutanir uppfyllingarflokks](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Setja upp öryggishólf

Til að setja upp öryggishólf skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Öryggishólf**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Sláðu inn heiti fyrir öryggishólfið.
1. Í aðgerðaglugganum velurðu **Vista.**

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rásir](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Setja upp netrás](channel-setup-online.md)

[Setja upp rás símavers](channel-setup-callcenter.md)


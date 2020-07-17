---
title: Setja upp netrás
description: Þetta efni lýsir því hvernig á að stofna nýja netrás í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 0d803b23f9de9daf624537d1d1ef30f17dc05fea
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533322"
---
# <a name="set-up-an-online-channel"></a>Setja upp netrás


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að stofna nýja netrás í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce styður margar smásölurásir. Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir). Netverslun gefur viðskiptavinum val um að kaupa afurðir úr netverslun smásala til viðbótar við smásöluverslanir þeirra.

Til að stofna netverslun í Commerce verðurðu fyrst að búa til netrás. Áður en ný netrás er stofnuð skaltu ganga úr skugga um að þú hafir lokið við [Skilyrði fyrir rásauppsetningu](channels-prerequisites.md).

Áður en þú getur búið til nýja síðu verður að búa til að minnsta kosti eina netverslun í Commerce. Frekari upplýsingar eru í [Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Stofna og stilla nýja netrás

Til að stofna og stilla nýja netrás fylgirðu þessum skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Netverslanir**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.
1. Í fellivalmyndinni **Lögaðili** skal slá inn viðeigandi lögaðila.
1. Í fellivalmyndinni **Vöruhús** slærðu inn viðeigandi vöruhús.
1. Í reitnum **Tímabelti verslunar** velurðu viðeigandi tímabelti.
1. Í reitnum **Gjaldmiðill** velurðu viðeigandi gjaldmiðil.
1. Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.
1. Í reitnum **Heimilisfangabók viðskiptavina** gefurðu upp gilda aðsetursbók.
1. Í reitnum **Virkniregla** velurðu virknireglu ef við á.
1. Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir stofnun nýrrar netrásar.

![Ný netrás](media/channel-setup-online-1.png)

Eftirfarandi mynd sýnir dæmi um netrás.

![Dæmi um netrás](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>Setja upp tungumál

Ef netverslunarsíðan mun styðja mörg tungumál skaltu stækka hlutann **Tungumál** og bæta við fleiri tungumálum eftir þörfum.

## <a name="set-up-payment-account"></a>Setja upp greiðslulykil

Í hlutanum **Greiðslulykill** er hægt að bæta við greiðsluaðila þriðja aðila. Nánari upplýsingar um að setja upp Adyen greiðslutengi, sjá [Dynamics 365 greiðslutengi fyrir Adyen](../retail/dev-itpro/adyen-connector.md).

## <a name="additional-channel-set-up"></a>Viðbótaruppsetning grunnrásar

Viðbótarupplýsingar sem krafist er fyrir uppsetningu netrásar fela í sér uppsetningu á greiðslumáta, afhendingaraðferðum og úthlutanir uppfyllingarflokks.

Eftirfarandi mynd sýnir uppsetningarkostina **Afhendingarmáta**, **Greiðslumáta** og **Úthlutanir uppfyllingarflokks** á flipanum **Setja upp**.

![Viðbótar uppsetningaraðgerðir netrásar](media/channel-setup-online-3.png)

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

### <a name="set-up-modes-of-delivery"></a>Setja upp afhendingarmáta

Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í **Aðgerðarglugganum**.  

Fylgdu þessum skrefum til að breyta eða bæta við afhendingarmáta.

1. Í yfirlitsglugganum ferðu í **Einingar \> Birgðastjórnun \> Afhendingmáti**.
1. Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.
1. Í kaflanum **Smásölurásir** velurðu **Bæta við línu** til að bæta við rásinni. Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.

Eftirfarandi mynd sýnir dæmi um afhendingarmáta.

![Setja upp afhendingarmáta](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Setja upp úthlutun uppfyllingarflokks

Til að setja upp úthlutun uppfyllingarflokks skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Úthlutun uppfyllingarflokks**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í fellilistanum **Uppfyllingarhópur** velurðu uppfyllingarhóp.
1. Í fellilistanum **Lýsing** skal færa inn lýsingu.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um uppstillingu úthlutunar uppfyllingarflokks.

![Setja upp úthlutun uppfyllingarflokks](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rásir](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Setja upp smásölurás](channel-setup-retail.md)

[Setja upp rás símavers](channel-setup-callcenter.md)

[Dynamics 365-greiðslutengill fyrir Adyen](../retail/dev-itpro/adyen-connector.md)

---
title: Setja upp rás símavers
description: Þetta efni lýsir því hvernig á að stofna nýja símaversrás í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057880"
---
# <a name="set-up-a-call-center-channel"></a>Setja upp rás símavers


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að stofna nýja símaversrás í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Í Dynamics 365 Commerce er símaver tegund rásar sem hægt er að skilgreina í forritinu. Að skilgreina rás fyrir símaþjónustueiningar þínar gerir kerfinu kleift að binda tiltekin gögn og sjálfgildi pöntunarvinnslu við sölupantanir. Fyrirtæki getur skilgreint margar rásir símavers í Commerce. 

Áður en ný rás símavers er stofnuð skaltu ganga úr skugga um að þú hafir lokið við [Skilyrði fyrir rásauppsetningu](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Stofna og stilla nýja rás símavers

Til að stofna og stilla nýja rás símavers fylgirðu þessum skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Símaver \> Öll símaver**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.
1. Veldu viðeigandi **Lögaðila** af fellilistanum.
1. Veldu viðeigandi staðsetningu **vöruhúss** af fellilistanum.
1. Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.
1. Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.
1. Gefa upp upplýsingakóða **verðhnekkingar**. Athugaðu að þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.
1. Gefðu upp upplýsingakóðann **Biðkóði**. Athugaðu að þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.
1. Gefðu upp upplýsingakóðann **Kredit**. Athugaðu að þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.
1. Veljið **Vista**.

Eftirfarandi mynd sýnir stofnun nýrrar símaversrásar.

![Ný rás símavers](media/channel-setup-callcenter-1.png)

Eftirfarandi mynd sýnir dæmi um símaversrás.

![Dæmi um rás símavers](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Viðbótaruppsetning grunnrásar

Viðbótarupplýsingar sem krafist er fyrir uppsetningu símaversrásar fela í sér uppsetningu á greiðslumáta og afhendingaraðferðum.

Eftirfarandi mynd sýnir uppsetningarkostina **Afhendingarmáta** og **Greiðslumáta** á flipanum **Setja upp**.

![Viðbótar uppsetningaraðgerðir símaversrásar](media/channel-setup-callcenter-3.png)

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

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Söluvirkni símavers](call-center-functionality.md)

[Uppsetning valkosta pantanavinnslu símavers](set-up-order-processing-options.md)

[Vörulistar símavers](call-center-catalogs.md)

[Setja upp og vinna með svikaviðvaranir](set-up-fraud-alerts.md)

[Setja upp samfelldniáætlanir fyrir símaver](set-up-continuity-program.md)

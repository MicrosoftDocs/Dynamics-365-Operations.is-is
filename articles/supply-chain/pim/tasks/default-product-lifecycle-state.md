---
title: Stofna sjálfgefna lífferilsstöðu afurðar
description: Þessi aðferð sýnir hvernig á að búa til sjálfgefna lífferilsstöðu afurðar sem og hvernig á að tengja sjálfgefna stöðu við útgefnar afurðir.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a628ed2b609f48c22076f409889c212e4d9463ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578201"
---
# <a name="create-a-default-product-lifecycle-state"></a>Stofna sjálfgefna lífferilsstöðu afurðar

[!include [banner](../../includes/banner.md)]

Þessi aðferð sýnir hvernig á að búa til sjálfgefna lífferilsstöðu afurðar sem og hvernig á að tengja sjálfgefna stöðu við útgefnar afurðir.


## <a name="create-a-default-lifecycle-state"></a>Stofna sjálfgefna lífferilsstöðu
1. Fara í Upplýsingastjórnun afurðar > Uppsetning > Lífferilsstaða afurðar.
2. Smellið á „Nýtt“.
3. Í reitinn Staða skal slá inn gildi.
4. Velja Já í reitnum Hvenær afhent lögaðila er sjálfgefið.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Velja skal Nei í reitinum Er virk fyrir áætlunargerð.

> [!NOTE]
> Ef ný útgefin afurð á ekki að vera tekin með í aðaláætlanagerð skal velja Nei. Ef hún á að vera tekin með í aðaláætlanagerð skal hafa stýringuna á sjálfgefna gildinu Já.  

## <a name="create-a-new-released-product"></a>Stofna nýja útgefna afurð
1. Lokið síðunni.
2. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
3. Smellið á „Nýtt“.
4. Í reitinn Afurðarnúmer skal slá inn gildi.
5. Sláið inn gildi í reitinn Afurðarheiti.
6. Í svæði Leita að nafni skal slá inn gildi.
7. Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.
8. Í reitinn Vöruflokkur skal slá inn eða velja gildi.
9. Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.
10. Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.
11. Smellið á „Í lagi“.

> [!NOTE]
> Sjálfgefin lífferilsstaða afurðar er altæk skilgreining.  

## <a name="change-the-product-to-an-active-state"></a>Breyta afurðinni í virka stöðu
1. Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.

> [!NOTE]
> Gerum ráð fyrir að þú hafir sett upp virka stöðu, þú getur nú valið þessa virku stöðu til að heimila að afurðin sé notuð í aðaláætlanagerð og útreikningi á uppskriftastigi. Augljóslega er þetta aðeins skynsamlegt ef allar upplýsingar um afurð sem krafist er fyrir samræmda áætlanagerð eru tilgreindar.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
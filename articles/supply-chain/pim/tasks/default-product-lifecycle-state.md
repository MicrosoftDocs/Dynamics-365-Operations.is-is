---
title: Stofna sjálfgefna lífferilsstöðu afurðar
description: Þessi aðferð sýnir hvernig á að búa til sjálfgefna lífferilsstöðu afurðar sem og hvernig á að tengja sjálfgefna stöðu við útgefnar afurðir.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b62d47f52da7f9e18bce401578a5e2a629ac5eb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818134"
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
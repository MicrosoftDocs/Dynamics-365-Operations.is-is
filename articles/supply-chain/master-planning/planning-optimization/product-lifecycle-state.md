---
title: Útiloka afurðir sem hafa tilteknar líftímastöður afurðar
description: Þetta efnisatriði útskýrir hvernig á að útiloka afurðir miðað við líftímastöðu þeirra þegar fínstilling skipulagningar er notuð.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 02c31aa3862df8dabc2b8c065dc3a94877d237f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992421"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Útiloka afurðir sem hafa tilteknar líftímastöður afurðar

[!include [banner](../../includes/banner.md)]

Útgefnar afurðir og útgefnar afurðarútgáfur innihalda svæðið **Líftímastaða afurðar**. Þessi svæði gera þér m.a. kleift að stjórna hvaða afurðir eru innifaldar við aðaláætlanagerð. Hægt er að bæta við, fjarlægja og breyta líftímastöðu eftir þörfum með því að opna **Afurðarupplýsingastjórnun \> Uppsetning \> Líftímastaða afurðar**. Fyrir hverja líftímastöðu afurðar er valkosturinn **Er virk fyrir áætlunargerð** stilltur á *Já* ef taka skal með afurðir í slíkri stöðu með í aðaláætlanagerð. Þegar valkosturinn er stilltur á *Nei* verða tengdar afurðir og vöruvíddasamsetningar útilokaðar úr öllum aðaláætlanagerðum og öllum útreikningum á uppskriftarstigi.

Útgefnar afurðir og vöruvíddasamsetningar þar sem svæðið **Líftímastaða afurðar** er hafður autt eru meðhöndlaðir eins og þeir séu með líftímastöðu afurðar þar sem valkosturinn **Er virk fyrir áætlunargerð** er stilltur á *Já*. Með öðrum orðum eru þær teknar með meðan á aðaláætlanagerð stendur.

> [!NOTE]
> Í því skyni að koma í veg fyrir of margar framboðspantanir er eindregið mælt með því að tengja allar úreltar útgefnar afurðir og vöruvíddasamsetningar við líftímastöðu afurðar þar sem valkosturinn **Er virk fyrir áætlunargerð** er stilltur á *Nei*. Þessi aðferð er afar mikilvæg þegar unnið er með vöruvíddasamsetningar afurðarafbrigða sem eru ekki endurnýjanlegar, því slíkt aðstoðar við að koma í veg fyrir sóun.

## <a name="related-resources"></a>Tengd tilföng

Frekari upplýsingar um líftímastöður afurðar er að finna á [Yfirlit yfir líftímastöðu afurðar](../../pim/product-lifecycle.md).

Nánari ítarupplýsingar um hvernig á að nota lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð og útreikningum á BOM-stigi, spilaðu eða lesið verkefnaleiðbeiningarnar [Búðu til lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
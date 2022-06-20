---
title: Búa til virkniforstillingu á netinu
description: Þessi grein lýsir því hvernig á að búa til virkniprófíl á netinu í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 686bc6440c31f3a4d729f2d92e3e57a1cc7b641f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895427"
---
# <a name="create-an-online-functionality-profile"></a>Búa til virkniforstillingu á netinu

[!include [banner](includes/banner.md)]

Þessi grein sýnir yfirlit yfir að setja upp virkniprófíl á netinu fyrir Microsoft Dynamics 365 Commerce.

Online virkni sniðið veitir ýmsar stillingar sem notaðar eru fyrir netrásir. Hver rás á netinu verður að tilgreina prófíl á netinu.

## <a name="create-an-online-functionality-profile"></a>Búa til virkniforstillingu á netinu

Eftirfarandi aðferð útskýrir hvernig á að búa til netvirkni snið úr forritinu Commerce Headquarters.

1. Farðu í **Einingar \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í svæðið **Forstilling** skal færa inn kenni fyrir forstillinguna.
1. Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).
1. Í **Aðgerðir** kafla, breyttu **CART**, **RETAIL CUSTOMERS** eða **CHECKOUT** stillingar, eftir þörfum.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um netvirknireglu.
  
![Dæmi um netvirknireglur fyrir forstillingu.](media/online-functionality-profile.png)

## <a name="functions"></a>Aðgerðir

- **Samanlagðar vörur**: Þegar þetta er virkt gerir þessi aðgerð körfunni kleift að uppfæra magn þegar sama hlut er bætt við mörgum sinnum.
- **Leyfa afgreiðslu án greiðslna**: Þegar þetta er virkt annast þessi aðgerð atburðarás þegar hlutir sem bætt er við í körfu hafa verð $0.00.
- **Búðu til viðskiptavini í ósamstillta stillingu**: Þetta er eldri stilling sem gildir um þriðja aðila rafræn viðskipti og á ekki við Dynamics 365 netverslunarsíðuna.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit rása](channels-overview.md)

[Skilyrði fyrir uppsetningu rásar](channels-prerequisites.md)

[Setja upp netrás](channel-setup-online.md)

[Setja upp smásölurás](channel-setup-retail.md)

[Setja upp rás símavers](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Smásöluverslun birtist ekki í listanum yfir verslanir til að sækja úr
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar smásöluverslun birtist ekki í listanum yfir verslanir þar sem hægt er að sækja vörur.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020825"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Smásöluverslun birtist ekki í listanum yfir verslanir til að sækja úr

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar smásöluverslun birtist ekki í listanum yfir verslanir þar sem hægt er að sækja vörur.

## <a name="description"></a>lýsing

Smásöluverslun birtist ekki í listanum yfir verslanir þar sem hægt er að sækja vörur.

## <a name="resolution"></a>Upplausn

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Skilgreina lengdar- og breiddargráðu fyrir aðsetur verslunar í Commerce Headquarters

Til að skilgreina lengdar- og breiddargráðu fyrir aðsetur verslunar í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Smásala og viðskipti \> Rásir \> Verslanir \> Allar verslanir**.
1. Finnið verslunina sem á að birtast í valkostum fyrir sótt á svæði rafrænna viðskipta. Skráið hjá ykkur gildið fyrir **Númer rekstrareiningar**.
1. Farið í **Fyrirtækisstjórnun \> Fyrirtæki \> Rekstrareiningar**.
1. Leitið að númeri rekstrareiningarinnar sem var skráð niður hér á undan og veljið síðan rekstrareininguna í leitarniðurstöðunum.
1. Í flýtiflipanum **Aðsetur** skal velja **Fleiri valkostir** og síðan velja **Ítarlegt**.
1. Í flýtiflipanum **Almennt** skal ganga úr skugga um reitirnir **Lengdargráða** og **Breiddargráða** séu rétt stilltir. Sem hluti af þessu skrefi skal ganga úr skugga um að gildin séu rétt tilgreind sem jákvæðar og neikvæðar tölur.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Skilgreina uppfyllingarflokka í Commerce Headquarters

Til að skilgreina uppfyllingarflokka í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Smásala og viðskipti \> Rásir \> Netverslanir**.
1. Veljið netverslunina sem á að skilgreina.
1. Í aðgerðaglugganum skal velja **Setja upp** og því næst velja **Úthlutun uppfyllingarflokks**.
1. Á síðunni **Úthlutun uppfyllingarflokks** skal velja uppfyllingarflokkinn fyrir netverslunina.
1. Undir **Uppsetning** skal ganga úr skugga um smásöluverslunin sé rétt skilgreind fyrir uppfyllingarflokkinn.

## <a name="additional-resources"></a>Frekari upplýsingar 

[Stofna rekstrareiningu](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Setja upp netrás](../channel-setup-online.md)
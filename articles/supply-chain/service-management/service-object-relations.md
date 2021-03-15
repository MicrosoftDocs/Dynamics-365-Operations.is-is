---
title: Tengsl þjónustuhluta
description: Hægt er að stofna þjónustuhlutatengsl á milli þjónustuhlutar og þjónustusamnings eða þjónustupöntunar.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974336"
---
# <a name="service-object-relations"></a>Tengsl þjónustuhluta 

[!include [banner](../includes/banner.md)]

Hægt er að stofna þjónustuhlutatengsl á milli þjónustuhlutar og þjónustusamnings eða þjónustupöntunar. Þegar tengsl eru stofnuð er þjónustuhluturinn tengdur við þjónustusamning eða þjónustupöntun.

Eftir að tengslin hafa verið stofnuð er hægt að tengja þjónustuhlutinn við allar línur á þjónustusamningnum eða þjónustupöntun.

## <a name="template-boms"></a>Uppskriftir sniðmáts

Einnig er hægt að tilgreina sniðmátsuppskrift fyrir hlutatengslin. Sniðmátsuppskriftin er uppskrift fyrir hluti þar sem þjónusta fer fram. Ef hluti af þjónustuhlut þáttarins er skiptur út í þjónustuheimsókn er hægt að skrá breytinguna í þjónustuuppskrift með því að nota skjámyndina Þjónustuhlutir.

## <a name="example"></a>Dæmi

Í viðskiptavinasetri er stofnaður þjónustusamningur til að þjóna tveimur lyftum.
Þjónustusamningurinn hefur auðkennið SAL-001.

Lyfturnar eru settar upp sem hlutir í skjámyndinni Þjónustuhlutir sem EL-S/1000 og EL-L/1000.

Tengja skal þjónustuhlutina, EL-S/1000 og EL-L/1000, við þjónustusamninginn.

Ef óskað er eftir að skrá breytingar í uppskriftinni fyrir þjónustuhlutinn um leið og skipt er út hluta hlutarins, er þjónustuuppskrift tengd við þjónustuhlutatengsl, eins og lýst er í eftirfarandi töflu.

| Þjónustuhlutur | Tengsl – Þjónustusamningur | Þjónustuuppskrift   |
|----------------|------------------------------|---------------|
| EL-S/1000      | Kenni SAL-001                   | EL-S/1000-uppskrift |
| EL-L/1000      | Kenni SAL-001                   | BOM-EL-L/1000 |

Nú er hægt að stofna þjónustusamningslínur með þessum hlutum vegna þess að komin eru á þjónustuhlutatengsl eins og lýst er í eftirfarandi töflu.

| Færslugerð | Tegund           | Þjónustuhlutur |
|------------------|--------------------|----------------|
| Tími             | Eftirlit         | EL-S/1000      |
| Tími             | Gírkassi hreinsaður  | EL-S/1000      |
| Vara             | Hreinsun efnis | EL-S/1000      |
| Tími             | Eftirlit         | EL-L/1000      |
| Tími             | Gírkassi hreinsaður   | EL-L/1000      |
| Vara             | Hreinsun efnis | EL-L/1000      |

Í þjónustuheimsókn verður að skipta út gírkassanum fyrir EL-S/1000 lyftuna. Til að skipta um þáttahluta hlutarins er hægt að fá aðgang að uppskriftarhönnuði með því að nota þjónustuhlutatengslin sem sett voru upp fyrir gildandi þjónustusamning.

Aðgangur að uppskriftarhönnuði með því að nota þjónustuhlutatengsl

1. Þjónustusamningar
2. Tvísmellið á þjónustusamning eða smellið á Þjónustusamning til að stofna þjónustusamning.
3. Smellið á flipann „Setja upp“.
4. Smellið á Þjónustuhluti til að tengja sniðmátsuppskrift við þjónustusamninginn.
5. Í skjámyndinni Þjónustuhlutir skal smella á Hönnuð til að opna skjámyndina Hönnuður til að breyta sniðmátsuppskriftinni.

## <a name="automatically-created-service-orders"></a>Stofna þjónustupantanir sjálfvirkt

Ef þjónustupantanir eru stofnaðar sjálfkrafa fyrir þjónustusamning verða þjónustuhlutatengslin í samningnum einnig stofnuð í þjónustupöntunum.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
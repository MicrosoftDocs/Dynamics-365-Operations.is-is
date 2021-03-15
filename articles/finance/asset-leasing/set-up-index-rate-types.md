---
title: Setja upp vaxtavísitölur
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp vaxtavísitölu. Vaxtavísitölur eru áskildar ef fyrirtækið tengir upphæðir leigugreiðslna við safn af vaxtavísitölum.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f362bf4a6b5de3ce16330aea08880b07b4145792
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992865"
---
# <a name="set-up-index-rates"></a>Setja upp vaxtavísitölur

[!include [banner](../includes/banner.md)]

Ef leigugreiðslur eru háðar vísitölu er hægt að bæta við gerðum vaxtavísitala vinna með þær í kerfinu. Til að endurmeta leigugeriðslur á síðunni **Gerð vaxtavísitölu** notar endurmatsferli vaxtavísitölu nýjustu vaxtavísitöluna frá endurmatsdagsetningunni.

Fylgdu eftirfarandi skrefum til að bæta við gerðum vaxtarvísitala og vaxtarvísitölum.

1. Opnið **Eignarleiga \> Uppsetning \> Gerðir vaxtavísitölu**.
2. Veljið **Nýtt**.
3. Færið inn gerð vísitölunnar og heiti vaxtavísitölunnar í viðeigandi svæði.
4. Til að bæta við nýju gildi vaxtavísitölu skal velja gerð vaxtavísitölunnar og síðan valja **Bæta við**.
5. Veldu raunverulegan upphafsdag gildisins og veldu gildi vísitölunnar.

Velja verður annað hvort **Gildismun vaxtavísitölu** eða **Gildi vaxtavísitölu** sem aðferð vaxtavísitölu.

- Veldu aðferðina **Gildismun vaxtavísitölu** til að reikna út nýja leigugreiðslu miðað við mismuninn á milli vaxtavísitölu á upphafsdeginum og nýjustu vaxtavísitölunni. Vaxtavísitalan er skilgreind í svæðinu **Vaxtavísitala (%)**.
- Veldu aðferðina **Gildi vaxtavísitölu** til að reikna út leigugreiðsluna með því að nota prósentuhlutfallið sem er tilgreint í svæðinu **Vaxtavísitala (%)**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
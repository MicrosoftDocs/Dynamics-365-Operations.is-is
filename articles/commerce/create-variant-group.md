---
title: Stofna afbrigðaflokk
description: Þetta efni lýsir því hvernig á að búa til stærð, stíl eða litafbrigði fyrir vöru í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e19d9a2549fa9957126592f3db7e468147997261
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965152"
---
# <a name="create-a-variant-group"></a>Stofna afbrigðaflokk


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að búa til stærð, stíl eða litafbrigði fyrir vöru í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce styður mörg afbrigði fyrir vörur. Það er kjörið að setja upp afbrigðishópa fyrir mismunandi vöruflokka. Til dæmis er hægt að búa til stærðarhóp fyrir stuttermaboli með stærðunum extra small, small, medium, large og extra large, eða búa til litahóp til að innihalda alla tiltæka liti á vöru. Bæta skal við afbrigðishópum áður en afurðum er bætt við.

Í þessu efni verður stærðarhópur búinn til og stilltur. Hægt er að nota svipaðar aðferðir til að bæta við og stilla stílahópa og litahópa.

## <a name="create-a-size-group"></a>Stofna stærðarflokk

Til að stofna stærðarflokk, skal fylgja eftirfarandi skrefum.
 
1. Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afbrigðishópar \> Stærðarflokkar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitinn **Stærðarflokkur** færirðu inn heiti fyrir stærðarflokkinn.
1. Í reitinn **Lýsing** ritarðu viðeigandi lýsingu.
1. Í aðgerðaglugganum velurðu **Vista.**

## <a name="add-attributes-to-the-size-group"></a>Bættu eigindum við stærðarhópinn

Fylgið eftirfarandi skrefum til að bæta eigindum við stærðarflokk.

1. Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afbrigðishópar \> Stærðarflokkar**
1. Í yfirlitssvæðinu velurðu stærðarflokk.
1. Undir **Línur stærðarflokks** velurðu **Bæta við**.
1. Í reitinn **Stærð** færirðu inn streng sem sýnir stærð (til dæmis, „XL“).
1. Í reitinn **Stærðarheiti** slærðu inn heiti fyrir stærðina (til dæmis „Extra Large“).
1. Í reitinn **Áfyllingarþyngd** slærðu inn tölu sem sýnir áfyllingarþyngdina.
1. Í reitinn **Númer í strikamerki** slærðu inn númer sem táknar strikamerkið.
1. Í reitinn **Sýna röð** slærðu inn númer sem sýnir skjáröðunina.
1. Þegar þú hefur bætt við stærðum skaltu velja **Vista** á aðgerðarrúðunni.

Eftirfarandi mynd sýnir dæmi um stærðarhóp fyrir „stærðir á hversdagsskyrtum“.

![Stofna stærðarflokk](media/create-variant-group.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit afurðarupplýsinga](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Setja upp smásöluafurðir](set-up-retail-products.md)

[Afurðarvíddir](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
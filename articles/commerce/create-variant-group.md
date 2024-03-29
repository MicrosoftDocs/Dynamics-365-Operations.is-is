---
title: Búa til afbrigðaflokk
description: Þessi grein lýsir því hvernig á að búa til stærð, stíl eða litafbrigðishóp fyrir vöru í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
ms.openlocfilehash: 507076259c2d9dfe97a0e24d253b5ac0a8325fe2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270101"
---
# <a name="create-a-variant-group"></a>Búa til afbrigðaflokk


[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til stærð, stíl eða litafbrigðishóp fyrir vöru í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce styður mörg afbrigði fyrir vörur. Það er kjörið að setja upp afbrigðishópa fyrir mismunandi vöruflokka. Til dæmis er hægt að búa til stærðarhóp fyrir stuttermaboli með stærðunum extra small, small, medium, large og extra large, eða búa til litahóp til að innihalda alla tiltæka liti á vöru. Bæta skal við afbrigðishópum áður en afurðum er bætt við.

Í þessari grein verður stærðarhópur búinn til og stilltur. Hægt er að nota svipaðar aðferðir til að bæta við og stilla stílahópa og litahópa.

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

![Stofna stærðarflokk.](media/Size-Groups.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit afurðarupplýsinga](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Setja upp smásöluafurðir](set-up-retail-products.md)

[Afurðarvíddir](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

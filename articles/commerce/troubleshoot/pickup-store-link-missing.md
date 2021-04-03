---
title: Valkosturinn Sækja þetta birtist ekki í körfu eða upplýsingasíðu afurðar
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar valkosturinn fyrir sótt í verslun birtist ekki á körfusíðunni eða upplýsingasíðu afurðar.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585372"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Valkosturinn „Sækja þetta“ birtist ekki í körfu eða upplýsingasíðu afurðar

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar valkosturinn fyrir sótt í verslun birtist ekki á körfusíðunni eða upplýsingasíðu afurðar.

## <a name="description"></a>lýsing

Hnappurinn **Sækja þetta** birtist ekki á körfusíðu eða upplýsingasíðu afurðar.

Eftirfarandi skýringarmynd sýnir dæmi um síðu sem inniheldur hnappinn **Sækja þetta**.

![Hnappurinn Sækja þetta](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Upplausn

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Virkja BOPIS-viðbótina í vefsmið Commerce

Til að virkja (BOPIS)-viðbótina „kaupa á netinu, sækja í verslun“ í vefsmið Commerce skal fylgja þessum skrefum.

1. Veldu svæðið.
1. Veljið **Stillingar svæðis** og veljið því næst **Viðbætur**.
1. Gangið úr skugga um að valkosturinn **Slökkva á BOPIS** sé hreinsaður.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Skilgreina afhendingarmáta í Commerce Headquarters

Til að skilgreina afhendingarmáta í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Innkaup og aðföng \> Uppsetning \> Afhendingarmátar**.
1. Gangið úr skugga um að afhendingarmátinn **Viðskiptavinur sækir** hafi verið búinn til og honum hafi verið úthlutað afurðum og aðsetrum.
1. Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur**.
1. Í vinstri flettingunni skal velja **Pantanir viðskiptavinar**.
1. Gangið úr skugga um að **Sóttur afhendingarmáti** sé rétt skilgreindur.

### <a name="configure-customer-orders-payments"></a>Skilgreina greiðslur vegna pantana viðskiptavina

Til að skilgreina greiðslur vegna pantana viðskiptavina í Commerce Headquarters skal fylgja þessum skrefum.

1. Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur**.
1. Í vinstri flettingunni skal velja **Pantanir viðskiptavinar**.
1. Í flýtiflipanum **Greiðslur** skal ganga úr skugga um reitirnir **Greiðsluskilmálar** og **Greiðslumáti** séu rétt stilltir.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina BOPIS](../cpe-bopis.md)

[Virkja marga afhendingamáta fyrir pantanir viðskiptavinar](../multiple-pickup-modes.md)

[Greiðslur Commerce-pöntunar í samskiptamiðstöð](../dev-itpro/commerce-payments.md)

[Eining til að velja verslun](../store-selector.md)

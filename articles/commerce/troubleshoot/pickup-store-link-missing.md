---
title: Valkosturinn Sækja þetta birtist ekki í körfu eða upplýsingasíðu afurðar
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar valmöguleikinn fyrir afhendingu í verslun birtist ekki á körfusíðunni eða vöruupplýsingasíðum.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 85d102d3442e19377912cb9562010778a0575db8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284604"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Valkosturinn „Sækja þetta“ birtist ekki í körfu eða upplýsingasíðu afurðar

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar valmöguleikinn fyrir afhendingu í verslun birtist ekki á körfusíðunni eða vöruupplýsingasíðum.

## <a name="description"></a>lýsing

Hnappurinn **Sækja þetta** birtist ekki á körfusíðu eða upplýsingasíðu afurðar.

Eftirfarandi skýringarmynd sýnir dæmi um síðu sem inniheldur hnappinn **Sækja þetta**.

![Hnappurinn Sækja þetta.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Lausn

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

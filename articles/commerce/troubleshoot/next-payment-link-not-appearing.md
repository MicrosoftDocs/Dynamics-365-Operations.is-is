---
title: Valkosturinn Vista fyrir næstu greiðslu birtist ekki
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar gátreiturinn Vista fyrir næstu greiðslu birtist ekki undir greiðslumáta á greiðsluferlissíðu á svæði rafrænna viðskipta.
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
ms.openlocfilehash: 679c2453068695caca03ac9618573eba0686b863
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347321"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Valkosturinn „Vista fyrir næstu greiðslu“ birtist ekki

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar gátreiturinn **Vista fyrir næstu greiðslu** birtist ekki undir **Greiðslumáta** á greiðsluferlissíðu á svæði rafrænna viðskipta.

## <a name="description"></a>lýsing

Gátreiturinn **Vista fyrir næstu greiðslu** birtist ekki í hlutanum **Greiðslumáti** á greiðsluferlissíðu á svæði rafrænna viðskipta.

Eftirfarandi skýringarmynd sýnir dæmi um greiðsluferlissíðu sem inniheldur gátreitinn **Vista fyrir næstu greiðslu**.

![Gátreiturinn Vista fyrir næstu greiðslu í greiðslueiningunni.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Lausn

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Staðfesta að Dynamics 365-greiðslutengill fyrir Adyen sé rétt skilgreindur í Commerce Headquarters

Til að staðfesta að Dynamics 365-greiðslutengill fyrir Adyen sé rétt skilgreindur í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Smásala og viðskipti \> Rásir \> Netverslanir**.
1. Veljið netverslunina.
1. Í flipanum **Greiðslulyklar** skal ganga úr skugga um að reiturinn **Leyfa vistun greiðsluupplýsinga í rafrænum viðskiptum** sé stilltur á **Satt**.

![Reiturinn Leyfa vistun greiðsluupplýsinga í rafrænum viðskiptum í Commerce Headquarters.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Frekari upplýsingar

[Greiðslueining](../payment-module.md)

[Vista netgreiðslumáta með Adyen-tengli](../dev-itpro/adyen-connector-listPI.md)

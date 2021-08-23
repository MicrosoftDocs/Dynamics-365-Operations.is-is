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
ms.openlocfilehash: 4887cde3e4243ae7a4da6402782e69e780ae20331ed80df63ba1239ef5187e41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769272"
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

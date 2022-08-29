---
title: Valkosturinn Vista fyrir næstu greiðslu birtist ekki
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar gátreiturinn Vista fyrir næstu greiðslu birtist ekki undir Greiðslumáti á útskráningarsíðu netverslunarsíðunnar.
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
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287485"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Valkosturinn „Vista fyrir næstu greiðslu“ birtist ekki

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar **Sparaðu fyrir næstu greiðslu** gátreiturinn birtist ekki undir **Greiðslumáti** á afgreiðslusíðu netverslunarsíðunnar.

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

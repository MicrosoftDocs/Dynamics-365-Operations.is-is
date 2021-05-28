---
title: Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu
description: Þetta efnisatriði inniheldur leiðbeiningar sem geta hjálpað til við að leysa úr villu sem kann að koma upp þegar netpöntun er samstillt.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021128"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði inniheldur leiðbeiningar sem geta hjálpað til við að leysa úr villu sem kann að koma upp þegar netpöntun er samstillt.

## <a name="description"></a>lýsing

Eftirfarandi villuboð birtast þegar netpöntun er samstillt: „Sjálfgefin greiðsluþjónusta fyrir kreditkortafærslur þarf að vera til staðar.“

![Villa vegna þess að sjálfgefna greiðsluþjónustu vantar](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Upplausn

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce

Til að staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce skal fylgja þessum skrefum.

1. Farið í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluþjónustur**.
1. Ganga skal úr skugga um að valkosturinn **Sjálfgefinn örgjörvi fyrir ný kreditkort** sé stilltur á **Já** fyrir eina greiðsluþjónustu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Uppsetning kreditkorts, heimild og úthlutun](../../finance/accounts-receivable/credit-card-authorizations.md)
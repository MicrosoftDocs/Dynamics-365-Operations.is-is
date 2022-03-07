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
ms.openlocfilehash: 6f8e0ea7675ffc5cbada36207422b410234e33afcaec90636e90e573a90ac484
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715237"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði inniheldur leiðbeiningar sem geta hjálpað til við að leysa úr villu sem kann að koma upp þegar netpöntun er samstillt.

## <a name="description"></a>lýsing

Eftirfarandi villuboð birtast þegar netpöntun er samstillt: „Sjálfgefin greiðsluþjónusta fyrir kreditkortafærslur þarf að vera til staðar.“

![Villa vegna þess að sjálfgefna greiðsluþjónustu vantar.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Lausn

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce

Til að staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce skal fylgja þessum skrefum.

1. Farið í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluþjónustur**.
1. Ganga skal úr skugga um að valkosturinn **Sjálfgefinn örgjörvi fyrir ný kreditkort** sé stilltur á **Já** fyrir eina greiðsluþjónustu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Uppsetning kreditkorts, heimild og úthlutun](../../finance/accounts-receivable/credit-card-authorizations.md)
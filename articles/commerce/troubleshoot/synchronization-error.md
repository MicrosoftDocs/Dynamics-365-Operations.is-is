---
title: Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað til við að laga villu sem gæti komið upp þegar netpöntun er samstillt.
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
ms.openlocfilehash: aa57366fb8f351a8275c947220de78fe809b7b5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276690"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað til við að laga villu sem gæti komið upp þegar netpöntun er samstillt.

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

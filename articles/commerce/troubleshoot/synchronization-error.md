---
title: Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu
description: Þetta efnisatriði inniheldur leiðbeiningar sem geta hjálpað til við að leysa úr villu sem kann að koma upp þegar netpöntun er samstillt.
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585369"
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

[Uppsetning kreditkorts, heimild og úthlutun](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)

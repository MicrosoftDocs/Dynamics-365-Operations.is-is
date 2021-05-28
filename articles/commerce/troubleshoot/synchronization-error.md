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
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="7e2bc-103">Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu</span><span class="sxs-lookup"><span data-stu-id="7e2bc-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e2bc-104">Þetta efnisatriði inniheldur leiðbeiningar sem geta hjálpað til við að leysa úr villu sem kann að koma upp þegar netpöntun er samstillt.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="7e2bc-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="7e2bc-105">Description</span></span>

<span data-ttu-id="7e2bc-106">Eftirfarandi villuboð birtast þegar netpöntun er samstillt: „Sjálfgefin greiðsluþjónusta fyrir kreditkortafærslur þarf að vera til staðar.“</span><span class="sxs-lookup"><span data-stu-id="7e2bc-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Villa vegna þess að sjálfgefna greiðsluþjónustu vantar](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="7e2bc-108">Upplausn</span><span class="sxs-lookup"><span data-stu-id="7e2bc-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="7e2bc-109">Staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce</span><span class="sxs-lookup"><span data-stu-id="7e2bc-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="7e2bc-110">Til að staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7e2bc-111">Farið í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluþjónustur**.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="7e2bc-112">Ganga skal úr skugga um að valkosturinn **Sjálfgefinn örgjörvi fyrir ný kreditkort** sé stilltur á **Já** fyrir eina greiðsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="7e2bc-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e2bc-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7e2bc-113">Additional resources</span></span>

[<span data-ttu-id="7e2bc-114">Uppsetning kreditkorts, heimild og úthlutun</span><span class="sxs-lookup"><span data-stu-id="7e2bc-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)
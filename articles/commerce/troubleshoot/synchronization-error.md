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
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="aa700-103">Samstillingarvilla pöntunar tengist sjálfgefinni greiðsluþjónustu</span><span class="sxs-lookup"><span data-stu-id="aa700-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa700-104">Þetta efnisatriði inniheldur leiðbeiningar sem geta hjálpað til við að leysa úr villu sem kann að koma upp þegar netpöntun er samstillt.</span><span class="sxs-lookup"><span data-stu-id="aa700-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="aa700-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="aa700-105">Description</span></span>

<span data-ttu-id="aa700-106">Eftirfarandi villuboð birtast þegar netpöntun er samstillt: „Sjálfgefin greiðsluþjónusta fyrir kreditkortafærslur þarf að vera til staðar.“</span><span class="sxs-lookup"><span data-stu-id="aa700-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Villa vegna þess að sjálfgefna greiðsluþjónustu vantar](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="aa700-108">Upplausn</span><span class="sxs-lookup"><span data-stu-id="aa700-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="aa700-109">Staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce</span><span class="sxs-lookup"><span data-stu-id="aa700-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="aa700-110">Til að staðfesta eða stilla sjálfgefna greiðsluþjónustu í höfuðstöðvum Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="aa700-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="aa700-111">Farið í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluþjónustur**.</span><span class="sxs-lookup"><span data-stu-id="aa700-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="aa700-112">Ganga skal úr skugga um að valkosturinn **Sjálfgefinn örgjörvi fyrir ný kreditkort** sé stilltur á **Já** fyrir eina greiðsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="aa700-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa700-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="aa700-113">Additional resources</span></span>

[<span data-ttu-id="aa700-114">Uppsetning kreditkorts, heimild og úthlutun</span><span class="sxs-lookup"><span data-stu-id="aa700-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)

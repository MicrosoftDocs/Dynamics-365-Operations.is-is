---
title: Villan Greiðslugerð verður að vera kreditkort á sölupöntunarsíðunni
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar villuboð koma upp í sölupöntunarsíðunni þegar búið er að samstilla pöntun.
author: Reza-Assadi
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801676"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="1c276-103">Villan „Greiðslugerð verður að vera kreditkort“ á sölupöntunarsíðunni</span><span class="sxs-lookup"><span data-stu-id="1c276-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c276-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar villuboð koma upp í sölupöntunarsíðunni þegar búið er að samstilla pöntun.</span><span class="sxs-lookup"><span data-stu-id="1c276-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="1c276-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="1c276-105">Description</span></span>

<span data-ttu-id="1c276-106">Þegar sölupöntunarsíðan er opnuð eftir að pöntun er samstillt koma upp eftirfarandi villuboð: „Greiðslugerðin verður að vera kreditkort þar sem númer kreditkorts hefur verið tilgreint.“</span><span class="sxs-lookup"><span data-stu-id="1c276-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Villan Greiðslugerð verður að vera kreditkort](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="1c276-108">Upplausn</span><span class="sxs-lookup"><span data-stu-id="1c276-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="1c276-109">Stilla greiðslugerð í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1c276-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="1c276-110">Farið í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluskilmálar**.</span><span class="sxs-lookup"><span data-stu-id="1c276-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="1c276-111">Í vinstri flettingunni skal velja greiðsluskilmálana.</span><span class="sxs-lookup"><span data-stu-id="1c276-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="1c276-112">Í reitnum **Greiðslugerð** skal ganga úr skugga um **Kreditkort** sé valið.</span><span class="sxs-lookup"><span data-stu-id="1c276-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c276-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1c276-113">Additional resources</span></span>

[<span data-ttu-id="1c276-114">Bókun á netsölu og -greiðslum</span><span class="sxs-lookup"><span data-stu-id="1c276-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
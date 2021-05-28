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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018435"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="952eb-103">Valkosturinn „Vista fyrir næstu greiðslu“ birtist ekki</span><span class="sxs-lookup"><span data-stu-id="952eb-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="952eb-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar gátreiturinn **Vista fyrir næstu greiðslu** birtist ekki undir **Greiðslumáta** á greiðsluferlissíðu á svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="952eb-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="952eb-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="952eb-105">Description</span></span>

<span data-ttu-id="952eb-106">Gátreiturinn **Vista fyrir næstu greiðslu** birtist ekki í hlutanum **Greiðslumáti** á greiðsluferlissíðu á svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="952eb-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="952eb-107">Eftirfarandi skýringarmynd sýnir dæmi um greiðsluferlissíðu sem inniheldur gátreitinn **Vista fyrir næstu greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="952eb-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Gátreiturinn Vista fyrir næstu greiðslu í greiðslueiningunni](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="952eb-109">Upplausn</span><span class="sxs-lookup"><span data-stu-id="952eb-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="952eb-110">Staðfesta að Dynamics 365-greiðslutengill fyrir Adyen sé rétt skilgreindur í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="952eb-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="952eb-111">Til að staðfesta að Dynamics 365-greiðslutengill fyrir Adyen sé rétt skilgreindur í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="952eb-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="952eb-112">Farið í **Smásala og viðskipti \> Rásir \> Netverslanir**.</span><span class="sxs-lookup"><span data-stu-id="952eb-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="952eb-113">Veljið netverslunina.</span><span class="sxs-lookup"><span data-stu-id="952eb-113">Select the online store.</span></span>
1. <span data-ttu-id="952eb-114">Í flipanum **Greiðslulyklar** skal ganga úr skugga um að reiturinn **Leyfa vistun greiðsluupplýsinga í rafrænum viðskiptum** sé stilltur á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="952eb-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Reiturinn Leyfa vistun greiðsluupplýsinga í rafrænum viðskiptum í Commerce Headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="952eb-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="952eb-116">Additional resources</span></span>

[<span data-ttu-id="952eb-117">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="952eb-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="952eb-118">Vista netgreiðslumáta með Adyen-tengli</span><span class="sxs-lookup"><span data-stu-id="952eb-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)

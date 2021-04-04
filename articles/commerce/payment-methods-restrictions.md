---
title: Takmarka greiðslumáta fyrir skil án kvittunar
description: Þetta efnisatriði lýsir því hvernig hægt er að takmarka ákveðnar greiðslugerðir ef endurgreiðslurnar er gerðar án kvittunar.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: fc087ea24ebbebd5acd1cf37fdfd5c9422d44be8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257050"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="8779c-103">Takmarka greiðslumáta fyrir skil án kvittunar</span><span class="sxs-lookup"><span data-stu-id="8779c-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8779c-104">Það þarf að skilgreina hverja greiðslugerð sem smásali samþykkir þegar kerfið er uppsett.</span><span class="sxs-lookup"><span data-stu-id="8779c-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="8779c-105">Þetta efnisatriði lýsir því hvernig hægt er að takmarka ákveðnar greiðslugerðir ef endurgreiðslurnar er gerðar án kvittunar.</span><span class="sxs-lookup"><span data-stu-id="8779c-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="8779c-106">Setja upp greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="8779c-106">Set up payment methods</span></span>

<span data-ttu-id="8779c-107">Til að setja upp greiðslumáta verður eftirfarandi verkefnum að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="8779c-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="8779c-108">Búa til greiðslumáta sem eru samþykktir af öllu fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="8779c-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="8779c-109">Stofna kortategundir og kortanúmer fyrir fyrirtækið í heild sinni.</span><span class="sxs-lookup"><span data-stu-id="8779c-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="8779c-110">Ef taka á við kredit- eða debetkortum þarf að búa til einn greiðslumáta fyrir kort og búa síðan til kortategundir og kortanúmer fyrir fyrirtækið allt.</span><span class="sxs-lookup"><span data-stu-id="8779c-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="8779c-111">Setja upp greiðsluhætti verslunar.</span><span class="sxs-lookup"><span data-stu-id="8779c-111">Set up store payment methods.</span></span> <span data-ttu-id="8779c-112">Tengið greiðslumáta við hverja verslun og færið síðan inn stillingar fyrir einstakar verslanir fyrir hvern greiðslumáta verslunar.</span><span class="sxs-lookup"><span data-stu-id="8779c-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="8779c-113">Setja upp kortagreiðsluhætti fyrir verslanir.</span><span class="sxs-lookup"><span data-stu-id="8779c-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="8779c-114">Ljúkið kortauppsetningu fyrir alla greiðsluhætti korts sem verslunin tekur á móti.</span><span class="sxs-lookup"><span data-stu-id="8779c-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="8779c-115">![Uppsetning verslunar](media/NoReceiptReturns1.png "Uppsetning smásöluverslunar")</span><span class="sxs-lookup"><span data-stu-id="8779c-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="8779c-116">Takmarka greiðslumáta fyrir skil án kvittunar</span><span class="sxs-lookup"><span data-stu-id="8779c-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="8779c-117">Fyrir hvern greiðsluhátt verslunar, á síðunni **Stjórnun verslunar**, undir **Skil án kvittunar**, skal stilla **Takmarka endurgreiðslur án kvittunar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="8779c-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="8779c-118">Sjálfgefið gildi á valkostinum er **Nei**, sem tryggir að greiðslumátinn sé leyfður fyrir endurgreiðslur.</span><span class="sxs-lookup"><span data-stu-id="8779c-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="8779c-119">Þegar **Takmarka endurgreiðslur án kvittunar** er stillt á **Já** verður valinn greiðslumáti ekki leyfður fyrir endurgreiðslur.</span><span class="sxs-lookup"><span data-stu-id="8779c-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="8779c-120">![Greiðslumáti í verslun](media/NoReceiptReturns3.png "Greiðslumáti viðskiptakrafna")</span><span class="sxs-lookup"><span data-stu-id="8779c-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="8779c-121">Þegar gjaldkeri velur greiðslumáta sem takmarkar endurgreiðslu án kvittunar birtist skilaboð til að staðfesta viðeigandi greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="8779c-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="8779c-122">![Viðunandi greiðslumátar](media/NoReceiptReturns4.png "Viðunandi greiðslumátar")</span><span class="sxs-lookup"><span data-stu-id="8779c-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="8779c-123">Ef færsla er bæði með endurgreiðslu með kvittun og án kvittunar, verður ekki farið eftir skilmálum takmörkunar vegna þess að færslan verður verkflæði endurgreiðslu með kvittun.</span><span class="sxs-lookup"><span data-stu-id="8779c-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
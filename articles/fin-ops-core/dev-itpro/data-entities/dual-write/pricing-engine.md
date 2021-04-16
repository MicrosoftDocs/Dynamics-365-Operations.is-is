---
title: Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management
description: Þetta efnisatriði lýsir því hvernig hægt er að nota verð vélina í Microsoft Dynamics 365 Supply Chain Management úr Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750765"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="85216-103">Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="85216-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="85216-104">Microsoft Dynamics 365 Supply Chain Management felur í sér verðlagningarvél sem sér um viðskiptasamninga, verðskrár, vildarkerfi, kynningar og afslætti.</span><span class="sxs-lookup"><span data-stu-id="85216-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="85216-105">Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun.</span><span class="sxs-lookup"><span data-stu-id="85216-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="85216-106">Þegar þú notar tvöfalda skrifa notarðu annaðhvort stöðuga verðlagningu eða verð vél frá Dynamics 365 Supply Chain Management á tilboðs- og pöntunarsíðum í Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="85216-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="85216-107">Notaðu verðlagsvélina úr Supply Chain Management í Sales</span><span class="sxs-lookup"><span data-stu-id="85216-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="85216-108">Í Sales ferðu í **Sales \> Pantanir**.</span><span class="sxs-lookup"><span data-stu-id="85216-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="85216-109">Veldu **Nýtt** til að stofna nýja pöntun eða velja fyrirliggjandi pöntun í listanum **Mínar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="85216-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="85216-110">Bæta við nýrri pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="85216-110">Add a new order line.</span></span>
4. <span data-ttu-id="85216-111">Ef þú ert að búa til nýja pöntun skaltu velja **Verðpöntun** í aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="85216-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="85216-112">Ef þú ert að uppfæra fyrirliggjandi pöntun skaltu velja **Endurreikna** í aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="85216-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="85216-113">Eftirtaldir dálkar eru fylltir út sjálfkrafa:</span><span class="sxs-lookup"><span data-stu-id="85216-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="85216-114">Upplýsingar um upphæð</span><span class="sxs-lookup"><span data-stu-id="85216-114">Detail Amount</span></span>
    + <span data-ttu-id="85216-115">Afsláttar%</span><span class="sxs-lookup"><span data-stu-id="85216-115">Discount %</span></span>
    + <span data-ttu-id="85216-116">Afsláttur</span><span class="sxs-lookup"><span data-stu-id="85216-116">Discount</span></span>
    + <span data-ttu-id="85216-117">Upphæð fyrir farm</span><span class="sxs-lookup"><span data-stu-id="85216-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="85216-118">Farmupphæð</span><span class="sxs-lookup"><span data-stu-id="85216-118">Freight Amount</span></span>
    + <span data-ttu-id="85216-119">Heildarskattur</span><span class="sxs-lookup"><span data-stu-id="85216-119">Total Tax</span></span>
    + <span data-ttu-id="85216-120">Heildarupphæð</span><span class="sxs-lookup"><span data-stu-id="85216-120">Total Amount</span></span>
    
5. <span data-ttu-id="85216-121">Gerðu eftirfarandi til að tryggja að kerfið taki mið af viðskipta- og sölusamningum til að reikna verðið:</span><span class="sxs-lookup"><span data-stu-id="85216-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="85216-122">Flettu að umhverfi Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85216-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="85216-123">Farðu í **Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakröfu**.</span><span class="sxs-lookup"><span data-stu-id="85216-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="85216-124">Veldu flipann **Verð** á yfirlitsstikunni sem er til hliðar.</span><span class="sxs-lookup"><span data-stu-id="85216-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="85216-125">Fyrir neðan **Mat verðsamnings** skal afmerkja valkostinn **Handvirk færsla**.</span><span class="sxs-lookup"><span data-stu-id="85216-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="85216-126">Hvernig það virkar</span><span class="sxs-lookup"><span data-stu-id="85216-126">How it works</span></span>

<span data-ttu-id="85216-127">Þegar þú velur **Verðpöntun** í Sales er virknin **Samtölur** á flipanum **Sölupöntun \> Skoðun** í Supply Chain Management kölluð á tengdri sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="85216-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="85216-128">Gildin í samtölu pöntunar í Sales eru notuð til að fylla út samsvarandi dálka í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85216-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="85216-129">Þegar samtala sölupöntunar er reiknuð út í Supply Chain Management metur útreikningurinn fyrirliggjandi viðskiptasamninga og sölusamninga viðskiptavinarins og vörurnar sem eru skráðar í sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="85216-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="85216-130">Þessar upplýsingar eru notaðar til að reikna út samtölurnar.</span><span class="sxs-lookup"><span data-stu-id="85216-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="85216-131">Þegar **Verðpöntun** er valin endurspeglar Sales sjálfkrafa alla uppstillingu sem hefur verið gerð í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85216-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="85216-132">Takmarkanir</span><span class="sxs-lookup"><span data-stu-id="85216-132">Limitations</span></span>

<span data-ttu-id="85216-133">Þegar dálkar í Sales eru fylltir út gildir eftirfarandi takmörkun:</span><span class="sxs-lookup"><span data-stu-id="85216-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="85216-134">Uppsetning gjalds og úthlutunar gjalds í Supply Chain Management er ekki endurtekin í Sales.</span><span class="sxs-lookup"><span data-stu-id="85216-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="85216-135">Verðlagning tekur ekki tillit til sérstakrar smásöluverðlagningar sem er tilgreind í dálknum **Smásölurás** á síðu sölupöntunarlínu í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85216-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="85216-136">Afslættir sem eru skilgreindir í hlutanum **Stjórnun afsláttar** af Supply Chain Management eru ekki skoðaðir.</span><span class="sxs-lookup"><span data-stu-id="85216-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
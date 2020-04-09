---
title: Samstilling við Dynamics 365 Supply Chain Management verðlagningarkerfi eftir eftirspurn
description: Þetta efnisatriði lýsir því hvernig hægt er að nota verð vélina í Microsoft Dynamics 365 Supply Chain Management úr Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173178"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="32564-103">Samstilling við Dynamics 365 Supply Chain Management verðlagningarkerfi eftir eftirspurn</span><span class="sxs-lookup"><span data-stu-id="32564-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="32564-104">Microsoft Dynamics 365 Supply Chain Management felur í sér verðlagningarvél sem sér um viðskiptasamninga, verðskrár, vildarkerfi, kynningar og afslætti.</span><span class="sxs-lookup"><span data-stu-id="32564-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="32564-105">Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun.</span><span class="sxs-lookup"><span data-stu-id="32564-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="32564-106">Þegar þú notar tvöfalda skrifa notarðu annaðhvort stöðuga verðlagningu eða verð vél frá Dynamics 365 Supply Chain Management á tilboðs- og pöntunarsíðum í Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="32564-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="32564-107">Notaðu verðlagsvélina úr Supply Chain Management í Sales</span><span class="sxs-lookup"><span data-stu-id="32564-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="32564-108">Í Sales ferðu í **Sales \> Pantanir**.</span><span class="sxs-lookup"><span data-stu-id="32564-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="32564-109">Veldu **Nýtt** til að stofna nýja pöntun eða velja fyrirliggjandi pöntun í listanum **Mínar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="32564-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="32564-110">Bæta við nýrri pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32564-110">Add a new order line.</span></span>
4. <span data-ttu-id="32564-111">Ef þú ert að búa til nýja pöntun skaltu velja **Verðpöntun** í aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="32564-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="32564-112">Ef þú ert að uppfæra fyrirliggjandi pöntun skaltu velja **Endurreikna** í aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="32564-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="32564-113">Eftirfarandi reitir eru sjálfkrafa fylltir út:</span><span class="sxs-lookup"><span data-stu-id="32564-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="32564-114">Upplýsingar um upphæð</span><span class="sxs-lookup"><span data-stu-id="32564-114">Detail Amount</span></span>
    + <span data-ttu-id="32564-115">Afsláttar%</span><span class="sxs-lookup"><span data-stu-id="32564-115">Discount %</span></span>
    + <span data-ttu-id="32564-116">Afsláttur</span><span class="sxs-lookup"><span data-stu-id="32564-116">Discount</span></span>
    + <span data-ttu-id="32564-117">Upphæð fyrir farm</span><span class="sxs-lookup"><span data-stu-id="32564-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="32564-118">Farmupphæð</span><span class="sxs-lookup"><span data-stu-id="32564-118">Freight Amount</span></span>
    + <span data-ttu-id="32564-119">Heildarskattur</span><span class="sxs-lookup"><span data-stu-id="32564-119">Total Tax</span></span>
    + <span data-ttu-id="32564-120">Heildarupphæð</span><span class="sxs-lookup"><span data-stu-id="32564-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="32564-121">Hvernig það virkar</span><span class="sxs-lookup"><span data-stu-id="32564-121">How it works</span></span>

<span data-ttu-id="32564-122">Þegar þú velur **Verðpöntun** í Sales er virknin **Samtölur** á flipanum **Sölupöntun \> Skoðun** í Supply Chain Management kölluð á tengdri sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="32564-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="32564-123">Gildin í heildarpöntuninni í Sales eru notuð til að fylla út samsvarandi reiti í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="32564-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="32564-124">Þegar samtala sölupöntunar er reiknuð út í Supply Chain Management metur útreikningurinn fyrirliggjandi viðskiptasamninga og sölusamninga viðskiptavinarins og vörurnar sem eru skráðar í sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="32564-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="32564-125">Þessar upplýsingar eru notaðar til að reikna út samtölurnar.</span><span class="sxs-lookup"><span data-stu-id="32564-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="32564-126">Þegar **Verðpöntun** er valin endurspeglar Sales sjálfkrafa alla uppstillingu sem hefur verið gerð í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="32564-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="32564-127">Takmarkanir</span><span class="sxs-lookup"><span data-stu-id="32564-127">Limitations</span></span>

<span data-ttu-id="32564-128">Þegar reitirnir í Sales eru fylltir út gilda eftirfarandi takmarkanir:</span><span class="sxs-lookup"><span data-stu-id="32564-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="32564-129">Uppsetning gjalds og úthlutunar gjalds í Supply Chain Management er ekki endurtekin í Sales.</span><span class="sxs-lookup"><span data-stu-id="32564-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="32564-130">Verðlagning telur ekki sérstaka smásöluverðlagningu sem tilgreind er í reitnum **Verslunarrás** á sölupöntunarlínusíðunni í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="32564-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="32564-131">Afslættir sem eru skilgreindir í hlutanum **Stjórnun afsláttar** af Supply Chain Management eru ekki skoðaðir.</span><span class="sxs-lookup"><span data-stu-id="32564-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>

---
title: "Afskriftir fasts kostnaðar framleiddrar vöru"
description: "Fastur kostnaður framleiddrar vöru endurspeglar uppsetningartíma og íhlutina sem eru með föstu magni eða fastri rýrnunartölu."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: AndersGirke
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 75c0f5bcff0aae63aa8c7dae9b0767f8c7e6a81c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="8507e-103">Afskriftir fasts kostnaðar framleiddrar vöru</span><span class="sxs-lookup"><span data-stu-id="8507e-103">Amortize constant costs for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8507e-104">Fastur kostnaður framleiddrar vöru endurspeglar uppsetningartíma og íhlutina sem eru með föstu magni eða fastri rýrnunartölu.</span><span class="sxs-lookup"><span data-stu-id="8507e-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="8507e-105">Hugtakið kostnaðarlotustærð er notað til að afskrifa þennan fasta kostnað í reiknuðum kostnaði framleiddrar vöru.</span><span class="sxs-lookup"><span data-stu-id="8507e-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="8507e-106">Þetta hugtak er með nokkur samheiti, svo sem lotustærð bókhalds.</span><span class="sxs-lookup"><span data-stu-id="8507e-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="8507e-107">Hugtakið afskrifaður fastur kostnaður hefur einnig ýmis samheiti, eitt af því hlutfallslegan fastan kostnað.</span><span class="sxs-lookup"><span data-stu-id="8507e-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="8507e-108">Magn kostnaðarlotustærðar fyrir framleidda vöru er notað í uppskrift.</span><span class="sxs-lookup"><span data-stu-id="8507e-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="8507e-109">Magnið fer eftir því hvernig uppskriftarútreikningurinn er frumstilltur og gerður, eins og sést af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8507e-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="8507e-110">Sjálfgefið útreikningsmagn í uppskriftarútreikningi vöru − Staðlað pöntunarmagn vörunnar fyrir birgðir er sjálfgildi fyrir kostnaðarlotustærðina en sjálfgildið getur verið meira magn til að sýna pöntunarmagnsmargfeldi vörunnar.</span><span class="sxs-lookup"><span data-stu-id="8507e-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="8507e-111">Hægt er að skilgreina staðlað pöntunarmagn vöru og margfeldi í sjálfgefnum pöntunarstillingum hennar eða svæðispöntunarstillingum hennar.</span><span class="sxs-lookup"><span data-stu-id="8507e-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="8507e-112">Tiltekið útreikningsmagn í uppskriftarútreikningi vöru − Tiltekna útreikningsmagnið þjónar sem kostnaðarlotustærð fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="8507e-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="8507e-113">Útreiknað magn notar upphaflega staðlað pöntunarmagn vörunnar, en hægt er að skrifa yfir sjálfgefið gildi.</span><span class="sxs-lookup"><span data-stu-id="8507e-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="8507e-114">Tilgreint útreikningsmagn táknar kostnaðarlotustærð fyrir tilgreindu vöruna og fyrir framleidda íhluti með uppskriftarlínu af gerðinni framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="8507e-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="8507e-115">Þetta er þar sem gert er ráð fyrir því að það íhluturinn verði framleiddur í nákvæmu magni.</span><span class="sxs-lookup"><span data-stu-id="8507e-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="8507e-116">Kostnaðarlotustærð annarra framleiddra þátta sem hafa línugerð uppskriftar vöru munu endurspegla staðlað pöntunarmagn.</span><span class="sxs-lookup"><span data-stu-id="8507e-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="8507e-117">Tiltekið útreikningsmagn eftir pöntun í uppskriftarútreikningi  vöru − Tiltekna útreikningsmagnið er haft sem kostnaðarlotustærð fyrir vöruna og framleidda íhluti hennar þegar uppskriftarútreikningar nota niðurbrotsaðferðina "eftir pöntun".</span><span class="sxs-lookup"><span data-stu-id="8507e-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="8507e-118">Gert er ráð fyrir að íhlutirnir verði framleiddir í nákvæmu magni, rétt eins og framleiddur íhlutur sem hefur uppskriftarlínu af gerðinni framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="8507e-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="8507e-119">Tiltekið útreikningsmagn í sérstökum uppskriftarútreikningi vegna pöntunar - Hægt er að gera sérstakan uppskriftarútreikning vegna pöntunar fyrir vörulínu í sölupöntun, sölutilboði eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="8507e-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="8507e-120">Sjálfgefið útreikningsmagn notar magnið í upphaflegu vörulínunni en hægt er að hnekkja sjálfgefna magninu.</span><span class="sxs-lookup"><span data-stu-id="8507e-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="8507e-121">Hægt er að velja hvort sérstaki uppskriftarútreikningurinn vegna pöntunar notar niðurbrotsaðferðina samkvæmt pöntun eða margra stiga niðurbrot.</span><span class="sxs-lookup"><span data-stu-id="8507e-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="8507e-122">Reiknuð upphæð afskrifaðs fasts kostnaðar vöru fellur undir ýmis gjöld.</span><span class="sxs-lookup"><span data-stu-id="8507e-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>







---
title: "Greining algengra orsaka framleiðslufrávika"
description: "Þessi grein útskýrir ýmis dæmigert uppruna á hverja tegund af fráviki í framleiðslu."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 50f8cd7904e1d32175edd321fbd6533e985fb324
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="common-sources-of-production-variances"></a><span data-ttu-id="269b0-103">Greining algengra orsaka framleiðslufrávika</span><span class="sxs-lookup"><span data-stu-id="269b0-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="269b0-104">Þessi grein útskýrir ýmis dæmigert uppruna á hverja tegund af fráviki í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="269b0-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="269b0-105">Hér eru sumar dæmigert uppruna á frávikum **lotustærð**:</span><span class="sxs-lookup"><span data-stu-id="269b0-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="269b0-106">Ógallað magn framleiðslupöntunar er annað en útreikningsmagn sem er notað í útreikningi staðlaðs kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="269b0-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="269b0-107">Magnið gefur grunninn fyrir afskriftir fasts kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="269b0-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="269b0-108">Virði fasts kostnaðar í framleiðslupöntuninni getur verið ólíkt föstum kostnaði sem er notaður í stöðluðum kostnaðarútreikningi.</span><span class="sxs-lookup"><span data-stu-id="269b0-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="269b0-109">Fasts kostnaðar í framleiðslupöntuninni getur verið önnur út af nokkrar ástæðum.</span><span class="sxs-lookup"><span data-stu-id="269b0-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="269b0-110">Fastur kostnaður gæti til dæmis endurspeglað eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="269b0-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="269b0-111">Handvirk breytingar í framleiðsluuppskrift eða leiða</span><span class="sxs-lookup"><span data-stu-id="269b0-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="269b0-112">Val á annarri uppskriftarútgáfu eða leiðarútgáfu þegar framleiðslupöntunin er stofnuð</span><span class="sxs-lookup"><span data-stu-id="269b0-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="269b0-113">Áætlaðar skipulagsbreytingar á uppskriftarútgáfunni eða leiðarútgáfan sem er úthlutað á vöru</span><span class="sxs-lookup"><span data-stu-id="269b0-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="269b0-114">Hér eru sumar dæmigert uppruna á frávikum á **framleiðslukostnaði** :</span><span class="sxs-lookup"><span data-stu-id="269b0-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="269b0-115">Kostnaðarflokkur uppgefnu notkunarinnar í leiðaraðgerð (og verð hans) er annar en kostnaðarflokkurinn sem er notaður í útreikningi staðlaðs kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="269b0-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="269b0-116">Virkur kostnaður kostnaðarflokksverðsins er annar en kostnaðarflokksverðið sem er notað í útreikningi staðlaðs kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="269b0-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="269b0-117">Hér eru sumar dæmigert uppruna á frávikum á **framleiðslumagni** :</span><span class="sxs-lookup"><span data-stu-id="269b0-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="269b0-118">Þú gerir yfirúthreyfing efnisíhlutar eða undirúthreyfing efnisíhlutar.</span><span class="sxs-lookup"><span data-stu-id="269b0-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="269b0-119">Þú gerir yfirtilkynningartími leiðaráðgerðar eða undirtilkynningartími leiðaraðgerðar.</span><span class="sxs-lookup"><span data-stu-id="269b0-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="269b0-120">Yfirinnhreyfing undirinnhreyfing ógallaðs magns yfirvörunnar samkvæmt pöntunarmagninu.</span><span class="sxs-lookup"><span data-stu-id="269b0-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="269b0-121">Hinsvegar, full úthreyfing íhluta og tilkynnt um aðgerðir samkvæmt pöntunarmagni framleiðslupöntunarinnar</span><span class="sxs-lookup"><span data-stu-id="269b0-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="269b0-122">Hér eru sumar dæmigert uppruna á frávikum á **staðgengilsframleiðslu** :</span><span class="sxs-lookup"><span data-stu-id="269b0-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="269b0-123">Úthreyfing efnisíhlutar sem er ekki í framleiðsluuppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="269b0-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="269b0-124">Þú bætir Íhlut handvirkt við framleiðsluuppskriftina og tilkynnir þann íhlut sem notaðan.</span><span class="sxs-lookup"><span data-stu-id="269b0-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="269b0-125">Tilkynnt er um vöru sem notaða án þess að bæta henni handvirkt við framleiðsluuppskriftina</span><span class="sxs-lookup"><span data-stu-id="269b0-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="269b0-126">Aðgerð bætt handvirkt við framleiðsluleiðina og tilkynnt að sú aðgerð sé notuð.</span><span class="sxs-lookup"><span data-stu-id="269b0-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="269b0-127">Önnur uppskriftarútgáfa valin þegar framleiðsluuppskrift er stofnuð þar sem uppskriftarútgáfan er önnur en sú sem er notuð í útreikningi staðlaðs kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="269b0-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="269b0-128">Önnur leiðarútgáfa valin þegar framleiðsluuppskrift er stofnuð þar sem leiðarútgáfa er önnur en sú sem er notuð í útreikningi staðlaðs kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="269b0-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>






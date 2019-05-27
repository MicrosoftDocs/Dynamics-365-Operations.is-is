---
title: Stofna nýja afurð
description: Þetta verk sýnir hvernig á að stofna nýja samnýttra afurðar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548417"
---
# <a name="create-a-new-product"></a><span data-ttu-id="9e7df-103">Stofna nýja afurð</span><span class="sxs-lookup"><span data-stu-id="9e7df-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e7df-104">Þetta verk sýnir hvernig á að stofna nýja samnýttra afurðar.</span><span class="sxs-lookup"><span data-stu-id="9e7df-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="9e7df-105">Því er yfirleitt framkvæmd af vöruhönnuður.</span><span class="sxs-lookup"><span data-stu-id="9e7df-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="9e7df-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="9e7df-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="9e7df-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Afurðir.</span><span class="sxs-lookup"><span data-stu-id="9e7df-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="9e7df-108">Stofna afurð</span><span class="sxs-lookup"><span data-stu-id="9e7df-108">Create a product</span></span>
1. <span data-ttu-id="9e7df-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9e7df-109">Click New.</span></span>
2. <span data-ttu-id="9e7df-110">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9e7df-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="9e7df-111">Ef númeraröð hefur ekki verið sett upp fyrir afurðarnúmer þarf að slá það inn.</span><span class="sxs-lookup"><span data-stu-id="9e7df-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="9e7df-112">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="9e7df-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="9e7df-113">Afurðarheiti verður sjálfgefið það sama og leitarnafn.</span><span class="sxs-lookup"><span data-stu-id="9e7df-113">The product name defaults to the search name.</span></span> <span data-ttu-id="9e7df-114">Þessu gildi má breyta ef þarf.</span><span class="sxs-lookup"><span data-stu-id="9e7df-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="9e7df-115">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e7df-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="9e7df-116">Setja upp víddaflokka</span><span class="sxs-lookup"><span data-stu-id="9e7df-116">Set up dimension groups</span></span>
1. <span data-ttu-id="9e7df-117">Smellt er á Víddaflokkar til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9e7df-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="9e7df-118">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9e7df-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7df-119">Geymslurakningarflokkinn ákvarðar hvaða geymsluvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða meðhöndlaðar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="9e7df-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="9e7df-120">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9e7df-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7df-121">Geymslurakningarflokkinn ákvarðar hvaða rakningarvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða raktar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="9e7df-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="9e7df-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e7df-122">Click OK.</span></span>


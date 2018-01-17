--- 
title: "Stofna nýja afurð"
description: "Þetta verk sýnir hvernig á að stofna nýja samnýttra afurðar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 0ea85775e7be86eead716e88ef9d51cae9c007f3
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---
# <a name="create-a-new-product"></a><span data-ttu-id="4605e-103">Stofna nýja afurð</span><span class="sxs-lookup"><span data-stu-id="4605e-103">Create a new product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4605e-104">Þetta verk sýnir hvernig á að stofna nýja samnýttra afurðar.</span><span class="sxs-lookup"><span data-stu-id="4605e-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="4605e-105">Því er yfirleitt framkvæmd af vöruhönnuður.</span><span class="sxs-lookup"><span data-stu-id="4605e-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="4605e-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="4605e-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="4605e-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Afurðir.</span><span class="sxs-lookup"><span data-stu-id="4605e-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="4605e-108">Stofna afurð</span><span class="sxs-lookup"><span data-stu-id="4605e-108">Create a product</span></span>
1. <span data-ttu-id="4605e-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4605e-109">Click New.</span></span>
2. <span data-ttu-id="4605e-110">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4605e-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4605e-111">Ef númeraröð hefur ekki verið sett upp fyrir afurðarnúmer þarf að slá það inn.</span><span class="sxs-lookup"><span data-stu-id="4605e-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="4605e-112">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="4605e-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="4605e-113">Afurðarheiti verður sjálfgefið það sama og leitarnafn.</span><span class="sxs-lookup"><span data-stu-id="4605e-113">The product name defaults to the search name.</span></span> <span data-ttu-id="4605e-114">Þessu gildi má breyta ef þarf.</span><span class="sxs-lookup"><span data-stu-id="4605e-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="4605e-115">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4605e-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="4605e-116">Setja upp víddaflokka</span><span class="sxs-lookup"><span data-stu-id="4605e-116">Set up dimension groups</span></span>
1. <span data-ttu-id="4605e-117">Smellt er á Víddaflokkar til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4605e-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="4605e-118">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="4605e-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4605e-119">Geymslurakningarflokkinn ákvarðar hvaða geymsluvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða meðhöndlaðar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="4605e-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="4605e-120">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="4605e-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4605e-121">Geymslurakningarflokkinn ákvarðar hvaða rakningarvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða raktar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="4605e-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="4605e-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4605e-122">Click OK.</span></span>



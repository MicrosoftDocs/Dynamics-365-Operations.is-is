---
title: Stofna nýja afurð
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja sameiginlega afurð.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844802"
---
# <a name="create-a-new-product"></a><span data-ttu-id="57228-103">Stofna nýja afurð</span><span class="sxs-lookup"><span data-stu-id="57228-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57228-104">Í þessu efnisatriði er lýst hvernig eigi að stofna nýja sameiginlega afurð.</span><span class="sxs-lookup"><span data-stu-id="57228-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="57228-105">Því er yfirleitt framkvæmd af vöruhönnuður.</span><span class="sxs-lookup"><span data-stu-id="57228-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="57228-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="57228-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="57228-107">Stofna afurð</span><span class="sxs-lookup"><span data-stu-id="57228-107">Create a product</span></span>
1. <span data-ttu-id="57228-108">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Afurðir**.</span><span class="sxs-lookup"><span data-stu-id="57228-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="57228-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="57228-109">Select **New**.</span></span>
3. <span data-ttu-id="57228-110">Í reitnum **Afurðarnúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="57228-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="57228-111">Ef númeraröð hefur ekki verið sett upp fyrir afurðarnúmer þarf að slá það inn.</span><span class="sxs-lookup"><span data-stu-id="57228-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="57228-112">Í reitinn **Afurðarheiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="57228-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="57228-113">Afurðarheiti verður sjálfgefið það sama og leitarnafn.</span><span class="sxs-lookup"><span data-stu-id="57228-113">The product name defaults to the search name.</span></span> <span data-ttu-id="57228-114">Þessu gildi má breyta ef þarf.</span><span class="sxs-lookup"><span data-stu-id="57228-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="57228-115">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57228-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="57228-116">Setja upp víddaflokka</span><span class="sxs-lookup"><span data-stu-id="57228-116">Set up dimension groups</span></span>
1. <span data-ttu-id="57228-117">Veldu **Víddaflokkar** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="57228-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="57228-118">Í reitnum **Geymsluvíddarflokkur** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="57228-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="57228-119">Geymslurakningarflokkinn ákvarðar hvaða geymsluvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða meðhöndlaðar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="57228-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="57228-120">Í reitnum **Rakningarvíddarflokkur** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="57228-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="57228-121">Geymslurakningarflokkinn ákvarðar hvaða rakningarvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða raktar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="57228-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="57228-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="57228-122">Select **OK**.</span></span>


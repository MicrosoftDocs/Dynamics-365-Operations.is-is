---
title: Stofna nýja afurð
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja sameiginlega afurð.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bf15359e085b541407bb49c266f7d9505893e25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203711"
---
# <a name="create-a-new-product"></a><span data-ttu-id="ca889-103">Stofna nýja afurð</span><span class="sxs-lookup"><span data-stu-id="ca889-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca889-104">Í þessu efnisatriði er lýst hvernig eigi að stofna nýja sameiginlega afurð.</span><span class="sxs-lookup"><span data-stu-id="ca889-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="ca889-105">Því er yfirleitt framkvæmd af vöruhönnuður.</span><span class="sxs-lookup"><span data-stu-id="ca889-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="ca889-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="ca889-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="ca889-107">Stofna afurð</span><span class="sxs-lookup"><span data-stu-id="ca889-107">Create a product</span></span>
1. <span data-ttu-id="ca889-108">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ca889-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="ca889-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ca889-109">Select **New**.</span></span>
3. <span data-ttu-id="ca889-110">Í reitnum **Afurðarnúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ca889-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="ca889-111">Ef númeraröð hefur ekki verið sett upp fyrir afurðarnúmer þarf að slá það inn.</span><span class="sxs-lookup"><span data-stu-id="ca889-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="ca889-112">Í reitinn **Afurðarheiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ca889-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="ca889-113">Afurðarheiti verður sjálfgefið það sama og leitarnafn.</span><span class="sxs-lookup"><span data-stu-id="ca889-113">The product name defaults to the search name.</span></span> <span data-ttu-id="ca889-114">Þessu gildi má breyta ef þarf.</span><span class="sxs-lookup"><span data-stu-id="ca889-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="ca889-115">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ca889-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="ca889-116">Setja upp víddaflokka</span><span class="sxs-lookup"><span data-stu-id="ca889-116">Set up dimension groups</span></span>
1. <span data-ttu-id="ca889-117">Veldu **Víddaflokkar** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ca889-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="ca889-118">Í reitnum **Geymsluvíddarflokkur** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="ca889-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="ca889-119">Geymslurakningarflokkinn ákvarðar hvaða geymsluvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða meðhöndlaðar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="ca889-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="ca889-120">Í reitnum **Rakningarvíddarflokkur** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="ca889-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="ca889-121">Geymslurakningarflokkinn ákvarðar hvaða rakningarvíddir verður að færa inn á hverja færslu fyrir vöruna og hvernig það verða raktar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="ca889-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="ca889-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ca889-122">Select **OK**.</span></span>


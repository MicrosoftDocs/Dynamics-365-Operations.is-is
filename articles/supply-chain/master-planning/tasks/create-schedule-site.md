---
title: Stofna áætlun fyrir svæði
description: Þessi verklýsing sýnir hvernig á að raða framleiðslupöntunum sem eru ekki enn hafnar fyrir svæði.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e188c5059b3957f3c0291bc4b8c525aac4d399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214275"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="557f8-103">Stofna áætlun fyrir svæði</span><span class="sxs-lookup"><span data-stu-id="557f8-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="557f8-104">Þessi verklýsing sýnir hvernig á að raða framleiðslupöntunum sem eru ekki enn hafnar fyrir svæði.</span><span class="sxs-lookup"><span data-stu-id="557f8-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="557f8-105">Nota Sýnigögn fyrirtækisins fyrir að ljúka þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="557f8-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="557f8-106">Auðkenndu framleiðslupantanir sem eru ekki hafnar.</span><span class="sxs-lookup"><span data-stu-id="557f8-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="557f8-107">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="557f8-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="557f8-108">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="557f8-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="557f8-109">Til dæmis, sía á reitnum svæði með gildinu '1'.</span><span class="sxs-lookup"><span data-stu-id="557f8-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="557f8-110">1 táknar svæði í USMF.</span><span class="sxs-lookup"><span data-stu-id="557f8-110">1 represents a site in USMF.</span></span> <span data-ttu-id="557f8-111">Ef ekki er verið að nota USMF skal velja svæði úr þínu eigin fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="557f8-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="557f8-112">Opnið dálkasía Stöðu.</span><span class="sxs-lookup"><span data-stu-id="557f8-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="557f8-113">Notið síu á reitnum „Staða“ með gildinu „áætlað“ og notið til þess síuvirknitáknið „er nákvæmlega“.</span><span class="sxs-lookup"><span data-stu-id="557f8-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="557f8-114">Stofna áætlun.</span><span class="sxs-lookup"><span data-stu-id="557f8-114">Create a schedule</span></span>
1. <span data-ttu-id="557f8-115">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="557f8-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="557f8-116">Í Aðgerðarrúðunni er smellt á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="557f8-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="557f8-117">Smellt er á Raða vinnslum.</span><span class="sxs-lookup"><span data-stu-id="557f8-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="557f8-118">Í reitnum Stefna tímasetningar er valið „Afturábak frá afhendingardagsetningu“.</span><span class="sxs-lookup"><span data-stu-id="557f8-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="557f8-119">Veljið Nei í svæðinu Takmarkaða afkastaveita.</span><span class="sxs-lookup"><span data-stu-id="557f8-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="557f8-120">Veljið Nei í svæðinu Takmarkað efni.</span><span class="sxs-lookup"><span data-stu-id="557f8-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="557f8-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="557f8-121">Click OK.</span></span>
    * <span data-ttu-id="557f8-122">Þetta gæti tekið nokkra stund.</span><span class="sxs-lookup"><span data-stu-id="557f8-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="557f8-123">Skoða niðurstaða raðaðra framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="557f8-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="557f8-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="557f8-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="557f8-125">Hægt er að merkja hvaða línu sem er.</span><span class="sxs-lookup"><span data-stu-id="557f8-125">You can mark any row.</span></span>  
2. <span data-ttu-id="557f8-126">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="557f8-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="557f8-127">Smellt er á Allar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="557f8-127">Click All jobs.</span></span>
    * <span data-ttu-id="557f8-128">Á þessari síðu er hægt að sjá lista yfir verk.</span><span class="sxs-lookup"><span data-stu-id="557f8-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="557f8-129">Á flipanum Röðun er hægt að sjá upphafsdagsetningu og lokadagsetningu fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="557f8-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="557f8-130">Smellt er á Efnum.</span><span class="sxs-lookup"><span data-stu-id="557f8-130">Click Materials.</span></span>
    * <span data-ttu-id="557f8-131">Á þessari síðu er hægt að sjá metin efnisnotkun fyrir aðgerðir á gildandi tiltækum birgðum og framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="557f8-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
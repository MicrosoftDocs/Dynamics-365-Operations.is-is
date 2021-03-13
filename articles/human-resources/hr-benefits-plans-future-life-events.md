---
title: Grunnstilla viðburði í framtíðinni
description: Þú getur tímasett framtíðarviðburði í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f10d7b6c9b45f6cedc16972fb157e43b7e0c40b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113005"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="11093-103">Grunnstilla viðburði í framtíðinni</span><span class="sxs-lookup"><span data-stu-id="11093-103">Configure future life events</span></span>

<span data-ttu-id="11093-104">Þú getur tímasett framtíðarviðburði í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="11093-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="11093-105">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Lífsatburðir í framtíðinni**.</span><span class="sxs-lookup"><span data-stu-id="11093-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="11093-106">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="11093-106">Select **New**.</span></span>

3. <span data-ttu-id="11093-107">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="11093-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="11093-108">Svæði</span><span class="sxs-lookup"><span data-stu-id="11093-108">Field</span></span> | <span data-ttu-id="11093-109">Lýsing</span><span class="sxs-lookup"><span data-stu-id="11093-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="11093-110">Dagsetning viðburðar</span><span class="sxs-lookup"><span data-stu-id="11093-110">Life event date</span></span> | <span data-ttu-id="11093-111">Kerfið vinnur alla atburði á innritunartímabilinu sem eiga sér stað fram til þessa dags.</span><span class="sxs-lookup"><span data-stu-id="11093-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="11093-112">Viðburður er skráður</span><span class="sxs-lookup"><span data-stu-id="11093-112">Life event logged</span></span> | <span data-ttu-id="11093-113">Dagsetning og tími þegar viðburðurinn er skráður.</span><span class="sxs-lookup"><span data-stu-id="11093-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="11093-114">Skrárgerð</span><span class="sxs-lookup"><span data-stu-id="11093-114">Log type</span></span> | <span data-ttu-id="11093-115">Sýnir hvort aðgerðin er ein af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="11093-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="11093-116">- **Uppfæra** - breyting á núverandi skrá sem er að rekja atburði í lífinu</span><span class="sxs-lookup"><span data-stu-id="11093-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="11093-117">- **Setja inn** - stofnun nýrrar atburðarskrár yfir atburði í lífinu</span><span class="sxs-lookup"><span data-stu-id="11093-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="11093-118">Auðkenni gerðar viðburðar</span><span class="sxs-lookup"><span data-stu-id="11093-118">Life event type ID</span></span> | <span data-ttu-id="11093-119">Einkvæmt auðkenni viðburðargerðar.</span><span class="sxs-lookup"><span data-stu-id="11093-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="11093-120">Gerð viðburðar</span><span class="sxs-lookup"><span data-stu-id="11093-120">Life event type</span></span> | <span data-ttu-id="11093-121">Hvati til að uppfæra skráningu starfsmanna á fríðindum.</span><span class="sxs-lookup"><span data-stu-id="11093-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="11093-122">Nánari upplýsingar er að finna í kaflanum um atburði um viðburði.</span><span class="sxs-lookup"><span data-stu-id="11093-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="11093-123">Staða</span><span class="sxs-lookup"><span data-stu-id="11093-123">Status</span></span> | <span data-ttu-id="11093-124">Hvort viðburðurinn hafi verið unninn eða ekki.</span><span class="sxs-lookup"><span data-stu-id="11093-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="11093-125">Lína</span><span class="sxs-lookup"><span data-stu-id="11093-125">Line</span></span> | <span data-ttu-id="11093-126">Línunúmer framtíðarlífsviðburðarins.</span><span class="sxs-lookup"><span data-stu-id="11093-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="11093-127">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="11093-127">Select **Save**.</span></span> 

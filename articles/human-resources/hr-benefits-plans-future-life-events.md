---
title: Grunnstilla viðburði í framtíðinni
description: Þú getur tímasett framtíðarviðburði í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418979"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="b4c76-103">Grunnstilla viðburði í framtíðinni</span><span class="sxs-lookup"><span data-stu-id="b4c76-103">Configure future life events</span></span>

<span data-ttu-id="b4c76-104">Þú getur tímasett framtíðarviðburði í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b4c76-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="b4c76-105">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Lífsatburðir í framtíðinni**.</span><span class="sxs-lookup"><span data-stu-id="b4c76-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="b4c76-106">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4c76-106">Select **New**.</span></span>

3. <span data-ttu-id="b4c76-107">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="b4c76-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b4c76-108">Svæði</span><span class="sxs-lookup"><span data-stu-id="b4c76-108">Field</span></span> | <span data-ttu-id="b4c76-109">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b4c76-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b4c76-110">Dagsetning viðburðar</span><span class="sxs-lookup"><span data-stu-id="b4c76-110">Life event date</span></span> | <span data-ttu-id="b4c76-111">Kerfið vinnur alla atburði á innritunartímabilinu sem eiga sér stað fram til þessa dags.</span><span class="sxs-lookup"><span data-stu-id="b4c76-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="b4c76-112">Viðburður er skráður</span><span class="sxs-lookup"><span data-stu-id="b4c76-112">Life event logged</span></span> | <span data-ttu-id="b4c76-113">Dagsetning og tími þegar viðburðurinn er skráður.</span><span class="sxs-lookup"><span data-stu-id="b4c76-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="b4c76-114">Skrárgerð</span><span class="sxs-lookup"><span data-stu-id="b4c76-114">Log type</span></span> | <span data-ttu-id="b4c76-115">Sýnir hvort aðgerðin er ein af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="b4c76-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="b4c76-116">- **Uppfæra** - breyting á núverandi skrá sem er að rekja atburði í lífinu</span><span class="sxs-lookup"><span data-stu-id="b4c76-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="b4c76-117">- **Setja inn** - stofnun nýrrar atburðarskrár yfir atburði í lífinu</span><span class="sxs-lookup"><span data-stu-id="b4c76-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="b4c76-118">Auðkenni gerðar viðburðar</span><span class="sxs-lookup"><span data-stu-id="b4c76-118">Life event type ID</span></span> | <span data-ttu-id="b4c76-119">Einkvæmt auðkenni viðburðargerðar.</span><span class="sxs-lookup"><span data-stu-id="b4c76-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="b4c76-120">Gerð viðburðar</span><span class="sxs-lookup"><span data-stu-id="b4c76-120">Life event type</span></span> | <span data-ttu-id="b4c76-121">Hvati til að uppfæra skráningu starfsmanna á fríðindum.</span><span class="sxs-lookup"><span data-stu-id="b4c76-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="b4c76-122">Nánari upplýsingar er að finna í kaflanum um atburði um viðburði.</span><span class="sxs-lookup"><span data-stu-id="b4c76-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="b4c76-123">Staða</span><span class="sxs-lookup"><span data-stu-id="b4c76-123">Status</span></span> | <span data-ttu-id="b4c76-124">Hvort viðburðurinn hafi verið unninn eða ekki.</span><span class="sxs-lookup"><span data-stu-id="b4c76-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="b4c76-125">Lína</span><span class="sxs-lookup"><span data-stu-id="b4c76-125">Line</span></span> | <span data-ttu-id="b4c76-126">Línunúmer framtíðarlífsviðburðarins.</span><span class="sxs-lookup"><span data-stu-id="b4c76-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="b4c76-127">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4c76-127">Select **Save**.</span></span> 

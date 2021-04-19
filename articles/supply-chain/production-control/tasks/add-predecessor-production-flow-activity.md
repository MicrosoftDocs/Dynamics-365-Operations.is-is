---
title: Bæta forvera við framleiðsluflæðisverkþátt
description: Í framleiðsluflæðisútgáfu, verður að vera raðaðar öllum verkþáttum.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 968880db317f74db6bc6d92a4beca9136c0d8de4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825063"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="71781-103">Bæta forvera við framleiðsluflæðisverkþátt</span><span class="sxs-lookup"><span data-stu-id="71781-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71781-104">Í framleiðsluflæðisútgáfu, verður að vera raðaðar öllum verkþáttum.</span><span class="sxs-lookup"><span data-stu-id="71781-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="71781-105">Aðgerð getur haft eitt eða mörg forvera eða arftaka.</span><span class="sxs-lookup"><span data-stu-id="71781-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="71781-106">Þessi verklýsing sýnir hvernig á að tengja forvera við verkþætti.</span><span class="sxs-lookup"><span data-stu-id="71781-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="71781-107">Til að framkvæma þetta verk, Þú þarft framleiðsluflæði sem hefur drög að útgáfu með að minnsta kosti tvær aðgerðir sem má tengja.</span><span class="sxs-lookup"><span data-stu-id="71781-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="71781-108">Nánari upplýsingar, sjá hvítbókina með yfirskriftinni "Framleiðsluflæði og verkþættir í Lean-framleiðslu."</span><span class="sxs-lookup"><span data-stu-id="71781-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="71781-109">Finndu útgáfu og framleiðsluflæði</span><span class="sxs-lookup"><span data-stu-id="71781-109">Find the production flow and version</span></span>
1. <span data-ttu-id="71781-110">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="71781-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="71781-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="71781-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="71781-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="71781-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="71781-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="71781-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="71781-114">Smellt er á Verkþætti.</span><span class="sxs-lookup"><span data-stu-id="71781-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="71781-115">Veldu verkþátt og bæta við forvera</span><span class="sxs-lookup"><span data-stu-id="71781-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="71781-116">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="71781-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="71781-117">Smelltu á Bæta við forvera.</span><span class="sxs-lookup"><span data-stu-id="71781-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="71781-118">Í reitinn verkþáttur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="71781-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="71781-119">Færið inn tölu í reitnum Hlutfall ferlistíma.</span><span class="sxs-lookup"><span data-stu-id="71781-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="71781-120">Sjálfgefið hlutfall ferlistíma fyrir verkþáttarvensl er 1.</span><span class="sxs-lookup"><span data-stu-id="71781-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="71781-121">Þetta gerir ráð fyrir að báðir verkþættir keyri á sama hraða eða framleiðslutími á einingu.</span><span class="sxs-lookup"><span data-stu-id="71781-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="71781-122">Ef forveri keyrir á hærra hraða (lægri framleiðslutími á einingu), ætti hlutfall að vera lægri en 1, ef forveri keyrir á hægari hraða (hærri framleiðslutími á einingu) er hlutfall ferlistíma hærri en 1.</span><span class="sxs-lookup"><span data-stu-id="71781-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="71781-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="71781-123">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
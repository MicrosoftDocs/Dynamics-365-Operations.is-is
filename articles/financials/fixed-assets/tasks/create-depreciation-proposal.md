--- 
title: "Stofna afskriftartillögu"
description: "Þetta ferli lýsir því hvernig runutillaga afskriftar vinnur og útskýrir hvernig á að stofna afskriftartillögur fyrir eignir."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="edc77-103">Stofna afskriftartillögu</span><span class="sxs-lookup"><span data-stu-id="edc77-103">Create a depreciation proposal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="edc77-104">Þetta ferli lýsir því hvernig runutillaga afskriftar vinnur og útskýrir hvernig á að stofna afskriftartillögur fyrir eignir.</span><span class="sxs-lookup"><span data-stu-id="edc77-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="edc77-105">Þetta verk notar USMF sýnigögn fyrirtækis og hlutverk bókhaldara.</span><span class="sxs-lookup"><span data-stu-id="edc77-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="edc77-106">Stofna afskriftartillögu</span><span class="sxs-lookup"><span data-stu-id="edc77-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="edc77-107">Fara í Eignir > Færslubókarfærslur > Stofna afskriftartillögu.</span><span class="sxs-lookup"><span data-stu-id="edc77-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="edc77-108">Í reitnum Heiti færslubókar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="edc77-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="edc77-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="edc77-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="edc77-110">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="edc77-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="edc77-111">Velja skal valkostinn samantekt afskriftar til að taka saman mánaðarlegar afskriftir í eina færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="edc77-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="edc77-112">Sem dæmi, ef gildið Til dags er mars 31, 2015, eftirfarandi lýsing er stofnuð: “Afskrift frá 31. janúar, 2015.”</span><span class="sxs-lookup"><span data-stu-id="edc77-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="edc77-113">Gagnasvæði á tillagðri færslubókarlínur er síðan sett á 31. mars, 2015.</span><span class="sxs-lookup"><span data-stu-id="edc77-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="edc77-114">Hægt er að sía afskriftatillögu af eign, eignaflokk eða önnur skilyrði með því að nota valkostinn Síu.</span><span class="sxs-lookup"><span data-stu-id="edc77-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="edc77-115">Þegar Stofna eignarmyndunar eða afskriftartillaga fyrir eignir skjámynd er notuð er hægt að leggja til afskriftir í runum.</span><span class="sxs-lookup"><span data-stu-id="edc77-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="edc77-116">Þetta er það ráðlagt fyrir stærri tillögur sem á að nota fleiri kerfistilföng.</span><span class="sxs-lookup"><span data-stu-id="edc77-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="edc77-117">Ef valið er valkostur runu, er enn hægt að ljúka öðrum verkefnum á meðan.</span><span class="sxs-lookup"><span data-stu-id="edc77-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="edc77-118">Þegar lagðar eru til afskriftir á þennan hátt er afskrift reiknuð út fyrir virðislíkön eigna.</span><span class="sxs-lookup"><span data-stu-id="edc77-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="edc77-119">Smella skal Stofna færslubók.</span><span class="sxs-lookup"><span data-stu-id="edc77-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="edc77-120">Fara yfir færslur í afskriftabók</span><span class="sxs-lookup"><span data-stu-id="edc77-120">Review depreciation entries</span></span>
1. <span data-ttu-id="edc77-121">Fara í Eignir >°Færslubókarfærslur°> Eignabók.</span><span class="sxs-lookup"><span data-stu-id="edc77-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="edc77-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="edc77-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="edc77-123">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="edc77-123">Click Lines.</span></span>
4. <span data-ttu-id="edc77-124">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="edc77-124">Click Post.</span></span>



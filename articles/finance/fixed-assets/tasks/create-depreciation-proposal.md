---
title: Stofna afskriftartillögu
description: Þetta efnisatriði lýsir því hvernig afskriftartillögur runu vinnu og útskýrir hvernig á að leggja afskriftir eigna.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013c768c8a016f399a27b1488ad0d5b339fdf7cb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813580"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="32018-103">Stofna afskriftartillögu</span><span class="sxs-lookup"><span data-stu-id="32018-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32018-104">Þetta efnisatriði lýsir því hvernig afskriftartillögur runu vinnu og útskýrir hvernig á að leggja afskriftir eigna.</span><span class="sxs-lookup"><span data-stu-id="32018-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="32018-105">Þetta verk notar USMF sýnigögn fyrirtækis og hlutverk bókhaldara.</span><span class="sxs-lookup"><span data-stu-id="32018-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="32018-106">Stofna afskriftartillögu</span><span class="sxs-lookup"><span data-stu-id="32018-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="32018-107">Í skoðunarrúðunni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Stofna afskriftartillögu**.</span><span class="sxs-lookup"><span data-stu-id="32018-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="32018-108">Í reitnum **Heiti færslubókar** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="32018-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="32018-109">Í reitnum **Til dags.** færirðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="32018-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="32018-110">Velja skal valkostinn **Sundurliða afskriftir** til að taka saman mánaðarlegar afskriftir í eina færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="32018-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="32018-111">Sem dæmi, ef gildið Til dags er mars 31, 2015, eftirfarandi lýsing er stofnuð: „Afskrift frá 31. janúar, 2015.”</span><span class="sxs-lookup"><span data-stu-id="32018-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="32018-112">Reiturinn **Dagsetning** á tillögðum færslubókarlínum er síðan stilltur á 31. mars, 2015.</span><span class="sxs-lookup"><span data-stu-id="32018-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="32018-113">Hægt er að sía afskriftatillögu af eign, eignaflokki eða öðrum skilyrðum með því að nota valkostinn **Síu**.</span><span class="sxs-lookup"><span data-stu-id="32018-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="32018-114">Þegar skjámyndin **Stofna tillögur um eignarmyndun eða afskrifir fastra eigna** er notuð er hægt að leggja til afskriftir í runum.</span><span class="sxs-lookup"><span data-stu-id="32018-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="32018-115">Þetta er það ráðlagt fyrir stærri tillögur sem á að nota fleiri kerfistilföng.</span><span class="sxs-lookup"><span data-stu-id="32018-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="32018-116">Ef valið er valkostur runu, er enn hægt að ljúka öðrum verkefnum á meðan.</span><span class="sxs-lookup"><span data-stu-id="32018-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="32018-117">Þegar lagðar eru til afskriftir á þennan hátt er afskrift reiknuð út fyrir virðislíkön eigna.</span><span class="sxs-lookup"><span data-stu-id="32018-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="32018-118">Veldu **Stofna færslubók**.</span><span class="sxs-lookup"><span data-stu-id="32018-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="32018-119">Fara yfir færslur í afskriftabók</span><span class="sxs-lookup"><span data-stu-id="32018-119">Review depreciation entries</span></span>
1. <span data-ttu-id="32018-120">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Dagbók fastafjármuna**.</span><span class="sxs-lookup"><span data-stu-id="32018-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="32018-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="32018-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="32018-122">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="32018-122">Select **Lines**.</span></span>
4. <span data-ttu-id="32018-123">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="32018-123">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
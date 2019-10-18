---
title: Búðu til sniðmát um borð með því að nota Dynamics 365 Talent - Onboard
description: Þetta efni útskýrir hvernig á að nota Microsoft-forritið Dynamics 365 Talent - Onboard til að stofna sniðmát fyrir þjálfunarleiðbeiningar fyrir nýliða. Þetta verkefni er nauðsynlegt fyrsta skrefið í stefnunni ráðning til starfsloka í mannauðsstjórnun (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 63f13380f3d2c31c4cc9009142f320ad8a41e8ee
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009878"
---
# <a name="create-an-onboarding-template"></a><span data-ttu-id="aaf6a-104">Búa til nýliðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="aaf6a-104">Create an onboarding template</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aaf6a-105">Microsoft Dynamics 365 Talent: Onboard veitir ýmis sniðmát sem geta hjálpað þér að stofna þjálfunarleiðbeiningar eins fljótt og auðið er.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="aaf6a-106">Þú getur notað eitt eða fleiri af þessum sniðmátum eða búið til þitt eigið sniðmát.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="aaf6a-107">Onboard veitir sýnishornatexta sem þú getur notað þegar þú býrð til þín eigin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="aaf6a-108">Þess vegna er ferlið auðvelt jafnvel þó þú byrjir frá grunni.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="aaf6a-109">Stofnaðu þjálfunarsniðmát úr núverandi sniðmáti</span><span class="sxs-lookup"><span data-stu-id="aaf6a-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="aaf6a-110">Á vinstri valmyndinni velurðu **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="aaf6a-111">Undir **Vinsæl sniðmát úr safninu** eða **Sniðmátin mín** velurðu sniðmát.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="aaf6a-112">Til að skoða fleiri sniðmát velurðu **Meira í sniðmátasafni**.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="aaf6a-113">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="aaf6a-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="aaf6a-114">Ef sniðmátið er úr safninu skaltu velja **Vista sem sniðmátið mitt**, slá inn nýtt heiti fyrir sniðmátið og velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="aaf6a-115">Ef sniðmátið er úr **Sniðmátin mín** skaltu velja **Vista sem sniðmát**, slá inn nýtt heiti fyrir sniðmátið og velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="aaf6a-116">[![Stofnun á þjálfunarsniðmáti úr núverandi sniðmáti](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="aaf6a-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="aaf6a-117">Stofnaðu nýtt nýliðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="aaf6a-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="aaf6a-118">Á vinstri valmyndinni velurðu **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="aaf6a-119">Undir **Mín sniðmát** velurðu reitinn **Bæta við** (plúsmerki \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="aaf6a-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="aaf6a-120">[![Stonun á nýju sniðmáti](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="aaf6a-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="aaf6a-121">Í glugganum **Stofna kynningarsniðmát** slærðu inn inn heiti fyrir sniðmátið og velur síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="aaf6a-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="aaf6a-122">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="aaf6a-122">Next steps</span></span>

- [<span data-ttu-id="aaf6a-123">Breyta nýliðakynnngu og -sniðmátum</span><span class="sxs-lookup"><span data-stu-id="aaf6a-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="aaf6a-124">Deildu efni með öðrum þátttakendum</span><span class="sxs-lookup"><span data-stu-id="aaf6a-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="aaf6a-125">Skoða stöðu verkefna og nýja starfsmenn</span><span class="sxs-lookup"><span data-stu-id="aaf6a-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="aaf6a-126">Stofna ráðningarteymi í Onboard</span><span class="sxs-lookup"><span data-stu-id="aaf6a-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="aaf6a-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="aaf6a-127">See also</span></span>

- [<span data-ttu-id="aaf6a-128">Prófaðu eða keyptu Onboard-forritið</span><span class="sxs-lookup"><span data-stu-id="aaf6a-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="aaf6a-129">Nýjungar</span><span class="sxs-lookup"><span data-stu-id="aaf6a-129">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="aaf6a-130">Athugasemdir við útgáfu</span><span class="sxs-lookup"><span data-stu-id="aaf6a-130">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="aaf6a-131">Fá aðstoð</span><span class="sxs-lookup"><span data-stu-id="aaf6a-131">Get support</span></span>](./talent-support.md)

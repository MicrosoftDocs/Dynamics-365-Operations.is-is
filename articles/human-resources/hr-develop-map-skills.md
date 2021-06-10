---
title: Kortleggja hæfni
description: Hægt er að búa til hæfnisvörpunarleit til að finna hæfan einstakling í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076597"
---
# <a name="map-skills"></a><span data-ttu-id="bf84c-103">Kortleggja hæfni</span><span class="sxs-lookup"><span data-stu-id="bf84c-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bf84c-104">Hægt er að búa til hæfnisvörpunarleit til að finna hæfan einstakling í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bf84c-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bf84c-105">Hæfnisvörpunarleitir skila niðurstöðum fyrir skilyrði sem eru slegin inn með því að leita í eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="bf84c-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="bf84c-106">Hæfni</span><span class="sxs-lookup"><span data-stu-id="bf84c-106">Skills</span></span>
- <span data-ttu-id="bf84c-107">Menntun</span><span class="sxs-lookup"><span data-stu-id="bf84c-107">Education</span></span>
- <span data-ttu-id="bf84c-108">Skírteini</span><span class="sxs-lookup"><span data-stu-id="bf84c-108">Certificates</span></span>
- <span data-ttu-id="bf84c-109">Stöður</span><span class="sxs-lookup"><span data-stu-id="bf84c-109">Positions</span></span>
- <span data-ttu-id="bf84c-110">Verkreynsla</span><span class="sxs-lookup"><span data-stu-id="bf84c-110">Project experience</span></span>

<span data-ttu-id="bf84c-111">Þú getur til dæmis fundið fólk í stofnuninni/fyrirtækinu sem hefur unnið sér inn CPA.</span><span class="sxs-lookup"><span data-stu-id="bf84c-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="bf84c-112">Hæfnisvörpun gerir kleift að finna núverandi starfsmenn eða umsækjendur með hæfni sem samsvara beint viðskiptaþörfum.</span><span class="sxs-lookup"><span data-stu-id="bf84c-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="bf84c-113">Aðeins er hægt að birta starfskrafta, umsækjendur og tengiliði sem eru valdir til að vera með í hæfnisvörpunarleit í niðurstöðulista hæfnisvörpunar eða hafa þá með í hæfniforstillingum.</span><span class="sxs-lookup"><span data-stu-id="bf84c-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="bf84c-114">Til að hafa einstakling með í hæfnisvörpunarleitum er **Taka með í hæfnisvörpun** stillt á **Já** á eftirfarandi síðum:</span><span class="sxs-lookup"><span data-stu-id="bf84c-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="bf84c-115">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="bf84c-115">Worker</span></span><br>
> - <span data-ttu-id="bf84c-116">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="bf84c-116">Employee</span></span><br>
> - <span data-ttu-id="bf84c-117">Umsækjandi</span><span class="sxs-lookup"><span data-stu-id="bf84c-117">Applicant</span></span><br>
> - <span data-ttu-id="bf84c-118">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="bf84c-118">Contacts</span></span><br>

<span data-ttu-id="bf84c-119">Til að búa til hæfnisskrá skaltu fara á **Þróun starfsmanns > Tenglar > Hæfnisskrá**.</span><span class="sxs-lookup"><span data-stu-id="bf84c-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="bf84c-120">Til að búa til forstillingu hæfnisvörpunar skal fara í **Þróun starfsmanns > Tenglar > Forstillingar hæfnisvörpunar**.</span><span class="sxs-lookup"><span data-stu-id="bf84c-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="bf84c-121">Hæfnibilsgreining og greining hæfniforstillingar</span><span class="sxs-lookup"><span data-stu-id="bf84c-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="bf84c-122">Hægt er að stofna greiningu hæfniforstillingar til að skoða lista yfir hæfni starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="bf84c-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="bf84c-123">Hægt er að stofna hæfnibilsgreiningu til að bera hæfni einstaklings og hæfni sem krafist er fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="bf84c-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="bf84c-124">Til að búa til greiningu á bilinu skaltu fara á **Þróun starfsmanns > Tenglar > Greiningarverk hæfnibils - einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="bf84c-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="bf84c-125">Til að búa til greiningu á hæfni skaltu fara á **Þróun starfsmanns > Tenglar > Greining hæfniforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="bf84c-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf84c-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bf84c-126">See also</span></span>

[<span data-ttu-id="bf84c-127">Skilgreina hæfni</span><span class="sxs-lookup"><span data-stu-id="bf84c-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="bf84c-128">Slá inn hæfni</span><span class="sxs-lookup"><span data-stu-id="bf84c-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
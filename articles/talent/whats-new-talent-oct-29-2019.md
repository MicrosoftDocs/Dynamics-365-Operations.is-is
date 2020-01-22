---
title: Nýjungar eða breytingar í Dynamics 365 Talent (29. október 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897443"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="6b604-103">Nýjungar eða breytingar í Dynamics 365 Talent (29. október 2019)</span><span class="sxs-lookup"><span data-stu-id="6b604-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

<span data-ttu-id="6b604-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="6b604-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="6b604-105">Breytingar í Attract</span><span class="sxs-lookup"><span data-stu-id="6b604-105">Changes in Attract</span></span>

<span data-ttu-id="6b604-106">Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="6b604-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="6b604-107">Breytingar í Onboard</span><span class="sxs-lookup"><span data-stu-id="6b604-107">Changes in Onboard</span></span>

<span data-ttu-id="6b604-108">Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="6b604-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="6b604-109">Breytingar í Core HR</span><span class="sxs-lookup"><span data-stu-id="6b604-109">Changes in Core HR</span></span>

<span data-ttu-id="6b604-110">Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="6b604-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="6b604-111">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6b604-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="6b604-112">Eyða aðilum án hlutverka ætti að vera sjálfgefið (371233)</span><span class="sxs-lookup"><span data-stu-id="6b604-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="6b604-113">Þegar þú útvegar nýtt umhverfi í Talent er sjálfgefið kveikt á **Eyða aðilum ef engin hlutverk eru til**.</span><span class="sxs-lookup"><span data-stu-id="6b604-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="6b604-114">Þegar þú eyðir starfsmanni er aðilinn sem tengist starfsmanninum ekki fjarlægður nema að þessi stilling sé virk.</span><span class="sxs-lookup"><span data-stu-id="6b604-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="6b604-115">Þessi breyting takmarkar afritaðar færslur í altækri aðsetursbók þegar þú þarft að flytja inn, breyta eða flytja starfsmenn aftur inn.</span><span class="sxs-lookup"><span data-stu-id="6b604-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="6b604-116">Heimilt skal vera að eyða drögum og niðurfelldum orlofsbeiðnum í Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="6b604-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="6b604-117">Með þessari breytingu geturðu nú eytt leyfisbeiðnum með stöðuna **Drög** eða **Hætt við** í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6b604-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="6b604-118">Viðbótarlisti gilda í sérsniðnum reitum endurspeglast ekki í Common Data Service þegar smellt hefur verið á Sækja um í eyðublaðsreitnum Sérsnið (379599)</span><span class="sxs-lookup"><span data-stu-id="6b604-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="6b604-119">Þegar þú bætir nýjum listagildum við núverandi sérsniðinn reit sem þegar hefur verið samstilltur við Common Data Service eru þeir núna fáanlegir í Common Data Serivce eftir að þú hefur notað breytingarnar á gluggann **Sérsniðnir reitir**.</span><span class="sxs-lookup"><span data-stu-id="6b604-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="6b604-120">Notaðu nýliðagátlista um borð í lögaðila þegar fleiri en eitt starf er fyrir hendi (371270)</span><span class="sxs-lookup"><span data-stu-id="6b604-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="6b604-121">Í útgáfu vikunnar geturðu sótt gátlista yfir starfsmenn sem eru með fleiri en eitt starf í **Skjámyndin Starfskraftur > Gátlistar**.</span><span class="sxs-lookup"><span data-stu-id="6b604-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="6b604-122">Forskoðunareiginleikinn Opin innskráning bóta hefur verið fjarlægður</span><span class="sxs-lookup"><span data-stu-id="6b604-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="6b604-123">Í tengslum við tilkynningu okkar í bloggfærslunni [Strategískar fjárfestingar í kjarnastarfsemi HR keyra gæðarekstur](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) hefur Microsoft fjarlægt eiginleikann opin innskráning bóta úr forsýningu almennings.</span><span class="sxs-lookup"><span data-stu-id="6b604-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="6b604-124">Ný virkni gefinn út í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="6b604-124">New functionality will be released in the future.</span></span> <span data-ttu-id="6b604-125">Ekki er hægt að styðja framleiðslunotkun á eiginleikanum opin innskráning bóta.</span><span class="sxs-lookup"><span data-stu-id="6b604-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6b604-126">Væntanlegt</span><span class="sxs-lookup"><span data-stu-id="6b604-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="6b604-127">Prenta árangursumsagnir</span><span class="sxs-lookup"><span data-stu-id="6b604-127">Print performance reviews</span></span>

<span data-ttu-id="6b604-128">Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.</span><span class="sxs-lookup"><span data-stu-id="6b604-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="6b604-129">Vinnusvæði eiginleikastjórnunar</span><span class="sxs-lookup"><span data-stu-id="6b604-129">Feature management workspace</span></span>

<span data-ttu-id="6b604-130">Eiginleikum er bætt við og þeir uppfærðir í hverri útgáfu.</span><span class="sxs-lookup"><span data-stu-id="6b604-130">Features are added and updated in every release.</span></span> <span data-ttu-id="6b604-131">Upplifun eiginleikastjórnunar veitir vinnusvæði þar sem hægt er að skoða lista yfir eiginleika sem hafa verið gefnir út í hverri útgáfu.</span><span class="sxs-lookup"><span data-stu-id="6b604-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="6b604-132">Sjálfgefið er að slökkt sé á nýjum eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="6b604-132">By default, new features are turned off.</span></span> <span data-ttu-id="6b604-133">Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="6b604-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="6b604-134">Til að læra meira um breytingarnar sem fylgja eiginleikastjórnun, sjá [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="6b604-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

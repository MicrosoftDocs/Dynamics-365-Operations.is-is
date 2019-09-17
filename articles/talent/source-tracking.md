---
title: Fylgjast með stöðum til að finna notendaupplýsingar og umsóknir umsækjenda
description: Þessi efnisatriði veitir upplýsingar um hvernig á að fylgjast með uppruna fyrir notendaupplýsingar og umsóknir umsækjanda.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2cfa180f992a4f7a9b2e21e0fb3e0845c7546c94
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742718"
---
# <a name="track-candidate-sources"></a><span data-ttu-id="358c1-103">Rekja uppruna umsækjenda</span><span class="sxs-lookup"><span data-stu-id="358c1-103">Track candidate sources</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="358c1-104">Virkni sem getið er í þessu efnisatriði er í boði sem hluti af prufuútgáfu.</span><span class="sxs-lookup"><span data-stu-id="358c1-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="358c1-105">Innihald og virkni geta tekið breytingum.</span><span class="sxs-lookup"><span data-stu-id="358c1-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="358c1-106">Til að nota þennan eiginleika skal biðja stjórnanda að virkja hann með **Stjórnandastillingar** í Attract.</span><span class="sxs-lookup"><span data-stu-id="358c1-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="358c1-107">Síðari útgáfa mun bjóða upp á rakningarskýrslur á uppruna.</span><span class="sxs-lookup"><span data-stu-id="358c1-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="358c1-108">Frekari upplýsingar er að finna í [Fá aðgang að forskoðunareiginleikum í Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="358c1-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="358c1-109">Þegar umsækjendur sækja um starf mun Attract sjálfkrafa fylgjast með uppruna umsókna þeirra, sem veitir þér mikilvægar upplýsingar til að auðvelda þér ráðningarvinnuna.</span><span class="sxs-lookup"><span data-stu-id="358c1-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="358c1-110">Ráðningaraðilar og ráðningarstjórar geta einnig valið uppruna umsóknar á meðan þeir bæta umsækjanda handvirkt við starf eða hæfileikasafn.</span><span class="sxs-lookup"><span data-stu-id="358c1-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="358c1-111">Hægt er að skoða uppruna umsóknar í upplýsingum um umsóknaraðgerð undir flipanum **Aðgerð** sem og í umsóknarferli sem finnst undir **Notandaupplýsingar** í hæfileikasöfnum.</span><span class="sxs-lookup"><span data-stu-id="358c1-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="358c1-112">Hægt er að finna upprunastað á notandasíðu umsækjanda í upplýsingum um umsækjanda undir flipanum **Notandaupplýsingar** í bæði umsóknum og hæfileikasöfnum.</span><span class="sxs-lookup"><span data-stu-id="358c1-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="358c1-113">Hægt er að finna þessi sniðmát í [Viðbót við alhliða ráðningar](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="358c1-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="358c1-114">Forskilgreindir upprunastaðir</span><span class="sxs-lookup"><span data-stu-id="358c1-114">Pre-configured sources</span></span>

<span data-ttu-id="358c1-115">Sjálfgefinn upprunalisti inniheldur algenga upprunastaði umsóknar.</span><span class="sxs-lookup"><span data-stu-id="358c1-115">The default source list contains common application sources.</span></span> <span data-ttu-id="358c1-116">Sumar upprunagerðir, eins og **Atvinnutorg** og **Samfélagsmiðill** eru með upplýsingar um fleiri upprunastaði.</span><span class="sxs-lookup"><span data-stu-id="358c1-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="358c1-117">**Samfélagsmiðill** inniheldur til dæmis Facebook og Twitter.</span><span class="sxs-lookup"><span data-stu-id="358c1-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="358c1-118">Upprunagerðin **Tilvísandi** gerir þér kleift að tilgreina starfsmann innan fyrirtækis sem tilvísanda.</span><span class="sxs-lookup"><span data-stu-id="358c1-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="358c1-119">Sjálfgefinn upprunalisti inniheldur eftirfarandi forskilgreinda upprunastaði:</span><span class="sxs-lookup"><span data-stu-id="358c1-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="358c1-120">Ráðningarsíða Attract</span><span class="sxs-lookup"><span data-stu-id="358c1-120">Attract career site</span></span>

-   <span data-ttu-id="358c1-121">Stofnun</span><span class="sxs-lookup"><span data-stu-id="358c1-121">Agency</span></span>

-   <span data-ttu-id="358c1-122">Atvinnulífskynning</span><span class="sxs-lookup"><span data-stu-id="358c1-122">Career Fair</span></span>

-   <span data-ttu-id="358c1-123">Markaðssetning fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="358c1-123">Company Marketing</span></span>

-   <span data-ttu-id="358c1-124">Ráðstefnur og vörusýningar</span><span class="sxs-lookup"><span data-stu-id="358c1-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="358c1-125">Samband fagmanna</span><span class="sxs-lookup"><span data-stu-id="358c1-125">Professional Association</span></span>

-   <span data-ttu-id="358c1-126">Atvinnutorg</span><span class="sxs-lookup"><span data-stu-id="358c1-126">Job board</span></span>

    -   <span data-ttu-id="358c1-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="358c1-127">Indeed</span></span>

    -   <span data-ttu-id="358c1-128">Leita</span><span class="sxs-lookup"><span data-stu-id="358c1-128">Seek</span></span>

    -   <span data-ttu-id="358c1-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="358c1-129">CareerBuilder</span></span>

    -   <span data-ttu-id="358c1-130">Google-störf</span><span class="sxs-lookup"><span data-stu-id="358c1-130">Google Jobs</span></span>

    -   <span data-ttu-id="358c1-131">Xing</span><span class="sxs-lookup"><span data-stu-id="358c1-131">Xing</span></span>

    -   <span data-ttu-id="358c1-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="358c1-132">Glassdoor</span></span>

    -   <span data-ttu-id="358c1-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="358c1-133">Monster Jobs</span></span>

-   <span data-ttu-id="358c1-134">Tímarit og útgáfur</span><span class="sxs-lookup"><span data-stu-id="358c1-134">Magazines & Publications</span></span>

-   <span data-ttu-id="358c1-135">Samfélagsmiðill</span><span class="sxs-lookup"><span data-stu-id="358c1-135">Social Network</span></span>

    -   <span data-ttu-id="358c1-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="358c1-136">Facebook</span></span>

    -   <span data-ttu-id="358c1-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="358c1-137">Twitter</span></span>

-   <span data-ttu-id="358c1-138">Háskólaráðningar</span><span class="sxs-lookup"><span data-stu-id="358c1-138">University Recruiting</span></span>

-   <span data-ttu-id="358c1-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="358c1-139">LinkedIn</span></span>

-   <span data-ttu-id="358c1-140">Smáauglýsingar</span><span class="sxs-lookup"><span data-stu-id="358c1-140">Classifieds</span></span>

-   <span data-ttu-id="358c1-141">Tilvísun</span><span class="sxs-lookup"><span data-stu-id="358c1-141">Referral</span></span>

-   <span data-ttu-id="358c1-142">Bætt við af ráðningaraðila</span><span class="sxs-lookup"><span data-stu-id="358c1-142">Added by Recruiter</span></span>

-   <span data-ttu-id="358c1-143">Annað</span><span class="sxs-lookup"><span data-stu-id="358c1-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="358c1-144">Sérsníða upprunalista</span><span class="sxs-lookup"><span data-stu-id="358c1-144">Customize the source list</span></span> 

<span data-ttu-id="358c1-145">Þú getur stækkað upprunalistann til að innihalda fleiri upprunastaði umsóknar.</span><span class="sxs-lookup"><span data-stu-id="358c1-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="358c1-146">Til að sérsníða þennan lista skaltu fylgja leiðbeiningunum í [Safn valkosta fyrir stækkunarhæfni í Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="358c1-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="358c1-147">Breyta einingunni **TalentSource** til að innihalda fleiri upprunastaði.</span><span class="sxs-lookup"><span data-stu-id="358c1-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="358c1-148">Til að forðast að hafa neikvæð áhrif á notandaviðmótið skaltu ekki breyta eða eyða fasttextagildum **TalentCategory** (ekki nöfnum) fyrir eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="358c1-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="358c1-149">**Tilvísun**</span><span class="sxs-lookup"><span data-stu-id="358c1-149">**Referral**</span></span>
- <span data-ttu-id="358c1-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="358c1-150">**LinkedIn**</span></span>
- <span data-ttu-id="358c1-151">**Annað**</span><span class="sxs-lookup"><span data-stu-id="358c1-151">**Other**</span></span>

<span data-ttu-id="358c1-152">Í staðinn geturðu stækkað fasttextann **TalentSource** til að bæta við öðrum gerðum uppruna.</span><span class="sxs-lookup"><span data-stu-id="358c1-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>

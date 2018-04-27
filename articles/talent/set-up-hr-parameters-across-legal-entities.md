---
title: "Setja upp færibreytur mannauðs (HR) á milli lögaðila"
description: "Þú þarft að setja upp sameiginlegar færibreytur fyrir skýrslur sem eru samnýttar á milli fyrirtækja, svo sem stöðufærslur. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2e73441a3f4190561d1d16db40ee1581267c8dfb
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="0743a-104">Setja upp færibreytur mannauðs (HR) á milli lögaðila</span><span class="sxs-lookup"><span data-stu-id="0743a-104">Set up HR parameters across legal entities</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="0743a-105">Þú þarft að setja upp sameiginlegar færibreytur fyrir skýrslur sem eru samnýttar á milli fyrirtækja, svo sem stöðufærslur.</span><span class="sxs-lookup"><span data-stu-id="0743a-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="0743a-106">Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0743a-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="0743a-107">Sumar gerðir af færslum, eins og stöðufærslur, eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="0743a-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="0743a-108">Fyrir°þessar færslur þarf að setja upp samnýttar færibreytur.</span><span class="sxs-lookup"><span data-stu-id="0743a-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="0743a-109">Til dæmis er síðan **Samnýttar færibreytur fyrir mannauð** til að setja upp færibreytur mannauðs á milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0743a-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="0743a-110">Á síðunni **Samnýttar færibreytur fyrir mannauð** eru færibreyturnar flokkaðar í svæði,°byggt á virkni þeirra.</span><span class="sxs-lookup"><span data-stu-id="0743a-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="0743a-111">Áður losuð virkni</span><span class="sxs-lookup"><span data-stu-id="0743a-111">Previously released functionality</span></span>
<span data-ttu-id="0743a-112">Á flipanum **Auðkenni** verður að velja auðkenningargerðir sem tákna auðkennisnúmer sem skráð°eru á síðunni.</span><span class="sxs-lookup"><span data-stu-id="0743a-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="0743a-113">Setja verður upp gerð auðkennis áður en hægt er að færa inn auðkennisupplýsingar fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="0743a-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="0743a-114">Upplýsingar um kennitölu, þjóðkennisnúmer, auðkenni útlendinga og persónulegan auðkennikóða eru á síðunni **Gerð auðkennis**.</span><span class="sxs-lookup"><span data-stu-id="0743a-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="0743a-115">Til að skilgreina nýja auðkennisgerð eða fara yfir lista með fyrirliggjandi gerðum skal smella á **Stjórnun starfsfólks** &gt; **Tenglaflipa** &gt; **Uppsetningu** &gt; **Gerðir auðkenna**.</span><span class="sxs-lookup"><span data-stu-id="0743a-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="0743a-116">Hægt er að færa inn einfaldan kóða og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="0743a-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="0743a-117">Ef verið er að nota Dynamics 365 til Talent</span><span class="sxs-lookup"><span data-stu-id="0743a-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="0743a-118">Á flipanum **Auðkenni** verður að velja auðkenningargerðir sem tákna auðkennisnúmer sem skráð°eru á síðunni.</span><span class="sxs-lookup"><span data-stu-id="0743a-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="0743a-119">Setja verður upp gerð auðkennis áður en hægt er að færa inn auðkennisupplýsingar fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="0743a-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="0743a-120">Upplýsingar um kennitölu, þjóðkennisnúmer, auðkenni útlendinga og persónulegan auðkennikóða eru á síðunni **Gerð auðkennis**.</span><span class="sxs-lookup"><span data-stu-id="0743a-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="0743a-121">Til að skilgreina nýja auðkennisgerð eða fara yfir lista með fyrirliggjandi gerðum, smellið á **Mannauður** &gt; **Uppsetning** &gt; **Gerð auðkennis**.</span><span class="sxs-lookup"><span data-stu-id="0743a-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="0743a-122">Hægt er að færa inn einfaldan kóða og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="0743a-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="0743a-123">Á flipanum **Númeraraðir** er hægt að velja númeraraðir sem eru notaðir fyrir eftirfarandi færslur: Starfsmannanúmer, Stöðu, Auðkenni notandabeiðnar, I-9 skjal, Umsækjandi, Umræða, Auðkenni fríðinda og°starfsmannaaðgerðina (ef þessi færslugerð er virkjuð).</span><span class="sxs-lookup"><span data-stu-id="0743a-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="0743a-124">Til að viðhalda tilvísunum og kóða númeraraða skal nota°listasíðuna **Númeraraðir**°.</span><span class="sxs-lookup"><span data-stu-id="0743a-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="0743a-125">Notið síðuleitar eiginleikann til að finna þessa síðu.</span><span class="sxs-lookup"><span data-stu-id="0743a-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="0743a-126">Á flipanum **Stöður** skal gefa til kynna hvort nýjar stöður eru tiltækar fyrir sjálfgefna úthlutun:</span><span class="sxs-lookup"><span data-stu-id="0743a-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="0743a-127">**Alltaf** - Hægt er að tengja starfsmenn við nýjar stöður þegar stöður eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="0743a-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="0743a-128">Þegar stöður eru stofnaðar í **Tiltækt fyrir úthlutun** eru dagsetning og tími í **Almennt** flipanum á **Stöðu** síðunni sjálfkrafa sett á stofnunardagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="0743a-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="0743a-129">**Aldrei** - Þú getur ekki úthlutað starfsmönnum á nýjar stöður þegar stöður eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="0743a-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="0743a-130">Ef þessi valkostur er valinn þarf að opna síðuna **Staða** fyrir hverja nýja stöðu þegar hún verður tiltæk, og svo, á flipanum **Almennt** skal slá inn **Tiltækt fyrir úthlutun** dagsetninguna til að virkja úthlutun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="0743a-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="0743a-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0743a-131">See also</span></span>
--------

[<span data-ttu-id="0743a-132">Setja upp færibreytur mannauðs bundnar tilteknu fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="0743a-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)





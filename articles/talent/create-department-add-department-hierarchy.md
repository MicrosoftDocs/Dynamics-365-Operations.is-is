---
title: "Stofna deild og tengja hana við stigveldi deildar"
description: "Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis. Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði. Hægt er að nota deildir til að gefa skýrslur um virk svið. Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8da8f726e8192c208c1cf51595c96f47d6213d7a
ms.contentlocale: is-is
ms.lasthandoff: 01/31/2018

---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="d3713-106">Stofna deild og tengja hana við stigveldi deildar</span><span class="sxs-lookup"><span data-stu-id="d3713-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="d3713-107">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="d3713-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d3713-108">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="d3713-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d3713-109">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="d3713-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d3713-110">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="d3713-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d3713-111">deild gæti innifalið hóp af kostnaðarstöðum.</span><span class="sxs-lookup"><span data-stu-id="d3713-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="d3713-112">Hægt er að úthluta stöðum til deilda.</span><span class="sxs-lookup"><span data-stu-id="d3713-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="d3713-113">Til að stofna Deild er smellt á **Mannauður** &gt; **Deildir** &gt; **Deild**.</span><span class="sxs-lookup"><span data-stu-id="d3713-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="d3713-114">Eftirfarandi tafla lýsir svæðum sem eru tiltæk.</span><span class="sxs-lookup"><span data-stu-id="d3713-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="d3713-115">Reitur</span><span class="sxs-lookup"><span data-stu-id="d3713-115">Field</span></span>               | <span data-ttu-id="d3713-116">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d3713-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3713-117">Heiti</span><span class="sxs-lookup"><span data-stu-id="d3713-117">Name</span></span>                | <span data-ttu-id="d3713-118">Færið inn heiti fyrir deildina.</span><span class="sxs-lookup"><span data-stu-id="d3713-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="d3713-119">Deildarnúmer</span><span class="sxs-lookup"><span data-stu-id="d3713-119">Department number</span></span>   | <span data-ttu-id="d3713-120">Sjálfgefið gildi kann að vera myndað sjálfkrafa ef kóði númeraraðar er úthlutað á  **tilvísunarnúmer fyrirtækis** á síðunni **númeraröð**.</span><span class="sxs-lookup"><span data-stu-id="d3713-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="d3713-121">Leita að nafni</span><span class="sxs-lookup"><span data-stu-id="d3713-121">Search name</span></span>         | <span data-ttu-id="d3713-122">Færið inn nafn eða skammstöfun sem hægt er að nota til að leita að deildinni.</span><span class="sxs-lookup"><span data-stu-id="d3713-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="d3713-123">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="d3713-123">Memo</span></span>                | <span data-ttu-id="d3713-124">Færðu inn viðbótarupplýsingar hér.</span><span class="sxs-lookup"><span data-stu-id="d3713-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="d3713-125">Í stigveldi</span><span class="sxs-lookup"><span data-stu-id="d3713-125">In hierarchy</span></span>        | <span data-ttu-id="d3713-126">Valinn gátreitur getur til kynna að deildin er innifalin í stigveldi deildar.</span><span class="sxs-lookup"><span data-stu-id="d3713-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="d3713-127">Upplýsingar um það hvernig skal bæta við deild við stigveldi deildar, Sjá upplýsingar síðar í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="d3713-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="d3713-128">DUNS-númer</span><span class="sxs-lookup"><span data-stu-id="d3713-128">DUNS number</span></span>         | <span data-ttu-id="d3713-129">DUNS stendur fyrir Data Universal Number System.</span><span class="sxs-lookup"><span data-stu-id="d3713-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="d3713-130">Þetta er níu-stafa númer sem er gefið út af Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="d3713-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="d3713-131">Yfirmaður</span><span class="sxs-lookup"><span data-stu-id="d3713-131">Manager</span></span>             | <span data-ttu-id="d3713-132">Velja einstaklinginn sem hefur umsjón með deildinni</span><span class="sxs-lookup"><span data-stu-id="d3713-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="d3713-133">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="d3713-133">Addresses</span></span>           | <span data-ttu-id="d3713-134">Bæta við upplýsingar um aðsetur fyrir deildina.</span><span class="sxs-lookup"><span data-stu-id="d3713-134">Add the address information for the department.</span></span> <span data-ttu-id="d3713-135">Til dæmis, bæta við póstfangi byggingar sem deild er í.</span><span class="sxs-lookup"><span data-stu-id="d3713-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="d3713-136">Tengslaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="d3713-136">Contact information</span></span> | <span data-ttu-id="d3713-137">Bæta við tengslaupplýsingum fyrir deild.</span><span class="sxs-lookup"><span data-stu-id="d3713-137">Add contact information for the department.</span></span> <span data-ttu-id="d3713-138">Til dæmis er bætt við símanúmer fyrir þjónustuborð í deild.</span><span class="sxs-lookup"><span data-stu-id="d3713-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="d3713-139">Til að bæta deild við stigveldi deildar, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="d3713-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="d3713-140">Smellt er á **Mannauður** &gt; **Deildir** &gt; **Deildastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="d3713-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="d3713-141">Smellið á **Breyta**, og veljið síðan fyrirtæki sem deild ætti að vera undir.</span><span class="sxs-lookup"><span data-stu-id="d3713-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="d3713-142">Smellið á **Setja inn**, og veljið **Deild** á listanum.</span><span class="sxs-lookup"><span data-stu-id="d3713-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="d3713-143">Í lista yfir deildir sem birtist skal velja deild til að bæta við stigveldið.</span><span class="sxs-lookup"><span data-stu-id="d3713-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="d3713-144">Vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="d3713-144">Save your changes.</span></span> <span data-ttu-id="d3713-145">Þú færð Boð um að drög að stigveldi hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d3713-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="d3713-146">Þegar þú ert tilbúinn, smellið á **Birta** í hönnuði stigveldis.</span><span class="sxs-lookup"><span data-stu-id="d3713-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="d3713-147">Hægt er að færa inn gildisdagsetningu sem tilgreinir hvenær stigveldi skuli birt.</span><span class="sxs-lookup"><span data-stu-id="d3713-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="d3713-148">Til dæmis til að bæta við nýjum deild við upphaf næsta almanaksárs, skal stilla gildisdagsetningu til 1. Janúar á nýja almanaksárinu.</span><span class="sxs-lookup"><span data-stu-id="d3713-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="d3713-149">Breytingar á stigveldinu tekur gildi á þeim degi.</span><span class="sxs-lookup"><span data-stu-id="d3713-149">The changes to the hierarchy will take effect on that date.</span></span>






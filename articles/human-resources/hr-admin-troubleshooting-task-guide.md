---
title: Vista verkleiðbeiningar í LCS og spila þær aftur
description: Þessi grein útskýrir hvernig á að vista verkefnaleiðbeiningar í Microsoft Dynamics Lifecycle Services (LCS) og spila þær síðan aftur.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053276"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="134ea-103">Vista verkefnaleiðbeiningar í LCS og spila þær aftur</span><span class="sxs-lookup"><span data-stu-id="134ea-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="134ea-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="134ea-104">**Environment details**</span></span> 

<span data-ttu-id="134ea-105">Microsoft Dynamics 365 Human Resources, sem var sett upp með Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="134ea-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="134ea-106">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="134ea-106">**Issue**</span></span>

<span data-ttu-id="134ea-107">Viðskiptamaður vill vista nýjar verkskráningar í LCS-verkið sitt og síðan spila vistuðu verkefnaleiðbeiningarnar aftur.</span><span class="sxs-lookup"><span data-stu-id="134ea-107">The customer wants to save new task recordings to the LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="134ea-108">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="134ea-108">**Resolution**</span></span>

<span data-ttu-id="134ea-109">Fylgja skal þessum skrefum til að vista verkskráningu í LCS.</span><span class="sxs-lookup"><span data-stu-id="134ea-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="134ea-110">Skráðu þig inn í LCS og veldu verkið.</span><span class="sxs-lookup"><span data-stu-id="134ea-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="134ea-111">Veljið reitinn **Viðskiptaferlavinnsla**.</span><span class="sxs-lookup"><span data-stu-id="134ea-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="134ea-112">Skoðið síðuna í „Uppfærðri BPM-upplifun“.</span><span class="sxs-lookup"><span data-stu-id="134ea-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="134ea-113">Veljið safn og svo **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="134ea-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="134ea-114">Færið inn heiti á líkani viðskiptaferlavinnslu (BPM).</span><span class="sxs-lookup"><span data-stu-id="134ea-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="134ea-115">Skráðu þig inn í Human Resources frá LCS.</span><span class="sxs-lookup"><span data-stu-id="134ea-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="134ea-116">Í reitnum **Leita** skal fara í **Hjálp**.</span><span class="sxs-lookup"><span data-stu-id="134ea-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="134ea-117">Hjálp Lifecycle Services opnast.</span><span class="sxs-lookup"><span data-stu-id="134ea-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="134ea-118">Veljið hnappinn **Endurhlaða** fyrir hjálparskilgreiningu Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="134ea-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="134ea-119">Nýja BPM-safnið ætti að birtast og það ætti að vera virkt.</span><span class="sxs-lookup"><span data-stu-id="134ea-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="134ea-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="134ea-120">Close the page.</span></span>
10. <span data-ttu-id="134ea-121">Búið til verkskráningu.</span><span class="sxs-lookup"><span data-stu-id="134ea-121">Create a task recording.</span></span>
11. <span data-ttu-id="134ea-122">Þegar þessu er lokið skal velja **Vista í Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="134ea-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Vista í Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="134ea-124">Veljið BPM-safnið og hnútinn þar sem vista á verkskráninguna.</span><span class="sxs-lookup"><span data-stu-id="134ea-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="134ea-125">Fylgja skal þessum skrefum til að endurspila verkefnaleiðbeiningu úr LCS.</span><span class="sxs-lookup"><span data-stu-id="134ea-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="134ea-126">Ræsið verkskráningu.</span><span class="sxs-lookup"><span data-stu-id="134ea-126">Start Task recorder.</span></span>
2. <span data-ttu-id="134ea-127">Veljið **Opna í LCS**.</span><span class="sxs-lookup"><span data-stu-id="134ea-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="134ea-128">Veljið safnið og BPM-hnútinn sem eru með vistuðu verkefnaleiðbeininguna.</span><span class="sxs-lookup"><span data-stu-id="134ea-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="134ea-129">Opnið verkefnaleiðbeininguna.</span><span class="sxs-lookup"><span data-stu-id="134ea-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
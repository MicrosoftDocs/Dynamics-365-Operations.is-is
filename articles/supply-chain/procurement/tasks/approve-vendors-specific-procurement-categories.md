--- 
title: "Samþykkja lánardrottna fyrir tiltekna innkaupaflokka"
description: "Þegar innkaupabeiðni er stofnuð, gæti verið þörf á að velja samþykktum eða æskilegum lánardrottins, eftir því hvernig innkaupareglur eru settar upp."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8bd223f3bdcd9c389cd2f0c21805b9232f371950
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="935ad-103">Samþykkja lánardrottna fyrir tiltekna innkaupaflokka</span><span class="sxs-lookup"><span data-stu-id="935ad-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="935ad-104">Þegar innkaupabeiðni er stofnuð, gæti verið þörf á að velja samþykktum eða æskilegum lánardrottins, eftir því hvernig innkaupareglur eru settar upp.</span><span class="sxs-lookup"><span data-stu-id="935ad-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="935ad-105">Þessi verklýsing sýnir hvernig á að tilgreina að lánardrottin er samþykkt eða æskilegur fyrir tiltekna innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="935ad-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="935ad-106">Þetta verk myndi venjulega framkvæmtaf fagmanni á sviði innkaupa.</span><span class="sxs-lookup"><span data-stu-id="935ad-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="935ad-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="935ad-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="935ad-108">Farið í innkaup og aðföng > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="935ad-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="935ad-109">Veljið lánardrottinn sem á að setja sem samþykktir eða æskilegur fyrir tegund.</span><span class="sxs-lookup"><span data-stu-id="935ad-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="935ad-110">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="935ad-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="935ad-111">Smellt er á Tegundir.</span><span class="sxs-lookup"><span data-stu-id="935ad-111">Click Categories.</span></span>
5. <span data-ttu-id="935ad-112">Smelltu á Bæta við tegund</span><span class="sxs-lookup"><span data-stu-id="935ad-112">Click Add category.</span></span>
6. <span data-ttu-id="935ad-113">Veljið SKRIFSTOFU OG SKRIFBORÐS (SKRIFSTOFU OG SKRIFBORÐS FYLGIHLUTI) í svæðinu Tegund.</span><span class="sxs-lookup"><span data-stu-id="935ad-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="935ad-114">Í reitnum tegundarstaða Lánardrottins, veljið 'Æskilegt'.</span><span class="sxs-lookup"><span data-stu-id="935ad-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="935ad-115">Það er hægt að tilgreina fleiri en einn æskilegan lánardrottin fyrir tegund.</span><span class="sxs-lookup"><span data-stu-id="935ad-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="935ad-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="935ad-116">Click Save.</span></span>
9. <span data-ttu-id="935ad-117">Fara í Innkaup og uppruni > Innkaupaflokkar.</span><span class="sxs-lookup"><span data-stu-id="935ad-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="935ad-118">Veljið 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES', í trénu.</span><span class="sxs-lookup"><span data-stu-id="935ad-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="935ad-119">Stækka hlutann Lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="935ad-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="935ad-120">Athuga hvort lánardrottin sem þú valdir birtist sem æskilegur lánardrottin fyrir fylgihluti af tegundinni skrifstofa og skrifborð.</span><span class="sxs-lookup"><span data-stu-id="935ad-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="935ad-121">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk, þarf hugsanlega að smella á hnappinn Aflæsa svo hægt sé að fletta niður í lista yfir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="935ad-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="935ad-122">Einnig er hægt að bæta æskulegum og samþykktum lánardrottnum við á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="935ad-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="935ad-123">Í trénu skal víkka út 'OFFICE AND DESK ACCESSORIES'.</span><span class="sxs-lookup"><span data-stu-id="935ad-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="935ad-124">Í trénu skal velja „skæri“</span><span class="sxs-lookup"><span data-stu-id="935ad-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="935ad-125">Veljið Nei í Erfa lánardrottna frá yfirtegund: svæði.</span><span class="sxs-lookup"><span data-stu-id="935ad-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="935ad-126">Veljið Já í Erfa lánardrottna frá yfirtegund: svæði.</span><span class="sxs-lookup"><span data-stu-id="935ad-126">Select Yes in the Inherit vendors from parent category: field.</span></span>



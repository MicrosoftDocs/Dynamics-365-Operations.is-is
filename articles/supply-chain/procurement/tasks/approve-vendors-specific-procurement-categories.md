---
title: Samþykkja lánardrottna fyrir tiltekna innkaupaflokka
description: Þetta efni útskýrir hvernig eigi að samþykkja lánardrottna fyrir tiltekna innkaupaflokka í Dynamics 365 Supply Chain Management.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204931"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="564ff-103">Samþykkja lánardrottna fyrir tiltekna innkaupaflokka</span><span class="sxs-lookup"><span data-stu-id="564ff-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="564ff-104">Þetta efni útskýrir hvernig eigi að samþykkja lánardrottna fyrir tiltekna innkaupaflokka í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="564ff-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="564ff-105">Þegar innkaupabeiðni er stofnuð, gæti verið þörf á að velja samþykktum eða æskilegum lánardrottins, eftir því hvernig innkaupareglur eru settar upp.</span><span class="sxs-lookup"><span data-stu-id="564ff-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="564ff-106">Þessi verklýsing sýnir hvernig á að tilgreina að lánardrottin er samþykkt eða æskilegur fyrir tiltekna innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="564ff-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="564ff-107">Þetta verk myndi venjulega framkvæmtaf fagmanni á sviði innkaupa.</span><span class="sxs-lookup"><span data-stu-id="564ff-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="564ff-108">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="564ff-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="564ff-109">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Lánardrottnar > Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="564ff-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="564ff-110">Veljið lánardrottinn sem á að setja sem samþykktir eða æskilegur fyrir tegund.</span><span class="sxs-lookup"><span data-stu-id="564ff-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="564ff-111">Í aðgerðasvæðinu velurðu **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="564ff-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="564ff-112">Veldu **Flokkar**.</span><span class="sxs-lookup"><span data-stu-id="564ff-112">Select **Categories**.</span></span>
5. <span data-ttu-id="564ff-113">Velja **Bæta við flokki**.</span><span class="sxs-lookup"><span data-stu-id="564ff-113">Select **Add category**.</span></span>
6. <span data-ttu-id="564ff-114">Í retinum **Flokkur** velurðu **OFFICE AND DESK ACCESSORIES (SKRIFSTOFU- OG SKRIFBORÐSFYLGIHLUTIR)**.</span><span class="sxs-lookup"><span data-stu-id="564ff-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="564ff-115">Í reitnum **Flokkastaða lánardrottins** velurðu **Æskilegt**.</span><span class="sxs-lookup"><span data-stu-id="564ff-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="564ff-116">Það er hægt að tilgreina fleiri en einn æskilegan lánardrottin fyrir flokk.</span><span class="sxs-lookup"><span data-stu-id="564ff-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="564ff-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="564ff-117">Select **Save**.</span></span>
9. <span data-ttu-id="564ff-118">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Innkaupaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="564ff-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="564ff-119">Veljið **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES** í trénu.</span><span class="sxs-lookup"><span data-stu-id="564ff-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="564ff-120">Stækkaðu hlutann **Lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="564ff-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="564ff-121">Athuga hvort lánardrottin sem þú valdir birtist sem æskilegur lánardrottin fyrir fylgihluti af tegundinni skrifstofa og skrifborð.</span><span class="sxs-lookup"><span data-stu-id="564ff-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="564ff-122">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk, þarf hugsanlega að velja hnappinn **Aflæsa** svo hægt sé að fletta niður í lista yfir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="564ff-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="564ff-123">Einnig er hægt að bæta æskulegum og samþykktum lánardrottnum við á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="564ff-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="564ff-124">Stækkaðu í trénu **OFFICE AND DESK ACCESSORIES** og veldu **Skæri**.</span><span class="sxs-lookup"><span data-stu-id="564ff-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="564ff-125">Veljið **Nei** í reitnum **Erfa lánardrottna frá yfirtegund:**.</span><span class="sxs-lookup"><span data-stu-id="564ff-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="564ff-126">Veljið **Já** í reitnum **Erfa lánardrottna frá yfirtegund:**.</span><span class="sxs-lookup"><span data-stu-id="564ff-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>


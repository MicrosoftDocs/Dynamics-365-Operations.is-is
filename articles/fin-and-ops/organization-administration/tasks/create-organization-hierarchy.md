---
title: Stofna stigveldi fyrirtækis
description: Notaðu eftirfarandi ferli til að stofna stigveldi fyrirtækis
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 203a586b06a13a7c67f246384152d17627e22041
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545546"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="07747-103">Stofna stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="07747-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07747-104">Notaðu eftirfarandi ferli til að stofna stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="07747-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="07747-105">Hægt er að nota stigveldi fyrirtækis til að skoða og gefa skýrslu um reksturinn frá ýmsum sjónarhornum.</span><span class="sxs-lookup"><span data-stu-id="07747-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="07747-106">Til dæmis er hægt að setja upp eitt stigveldi fyrir skattalega-, lagalega- eða lögboðna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="07747-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="07747-107">Hægt að setja upp annað stigveldi til að gefa skýrslu um fjárhagslegar upplýsingar sem ekki er krafist samkvæmt lögum, en sem er notuð við innri skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="07747-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="07747-108">Áður en hægt er að stofna stigveldisskipan fyrirtækis þarf að stofna fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="07747-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="07747-109">Frekari upplýsingar eru í "Stofna lögaðila" eða "Stofna rekstrareiningu" verk.</span><span class="sxs-lookup"><span data-stu-id="07747-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="07747-110">Einnig er hægt að stofna deildir og teymi.</span><span class="sxs-lookup"><span data-stu-id="07747-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="07747-111">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="07747-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="07747-112">Búa til stigveldi</span><span class="sxs-lookup"><span data-stu-id="07747-112">Create a hierarchy</span></span>
1. <span data-ttu-id="07747-113">Fara á fyrirtækisstjórnun > Fyrirtæki > stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="07747-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="07747-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="07747-114">Click New.</span></span>
3. <span data-ttu-id="07747-115">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="07747-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="07747-116">Smellt er á Úthluta málefni.</span><span class="sxs-lookup"><span data-stu-id="07747-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="07747-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="07747-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="07747-118">Veljið tilgangur sem úthluta á stigveldi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="07747-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="07747-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="07747-119">Click Add.</span></span>
7. <span data-ttu-id="07747-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="07747-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="07747-121">Finna stigveldið sem var verið að stofna.</span><span class="sxs-lookup"><span data-stu-id="07747-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="07747-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="07747-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="07747-123">Bæta við fyrirtækjum í stigveldi áætlunar</span><span class="sxs-lookup"><span data-stu-id="07747-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="07747-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="07747-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="07747-125">Velja skal þitt stigveldi.</span><span class="sxs-lookup"><span data-stu-id="07747-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="07747-126">Smella á Skoða stigveldi</span><span class="sxs-lookup"><span data-stu-id="07747-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="07747-127">Bæta við fleiri fyrirtæki eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="07747-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="07747-128">Til að bæta við fyrirtæki, smelltu á breyta og síðan setja inn til að bæta við fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="07747-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="07747-129">Þegar gerðar eru breytingar er hægt drög að vista og/eða birta breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="07747-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  


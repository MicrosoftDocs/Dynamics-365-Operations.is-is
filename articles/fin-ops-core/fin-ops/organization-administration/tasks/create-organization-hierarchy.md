---
title: Stofna stigveldi fyrirtækis
description: Notaðu eftirfarandi ferli til að stofna stigveldi fyrirtækis
author: sericks007
manager: AnnBe
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d61d6eee3b55087d633a8416fbed3a6192e82b2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560580"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="874db-103">Stofna stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="874db-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="874db-104">Notaðu eftirfarandi ferli til að stofna stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="874db-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="874db-105">Hægt er að nota stigveldi fyrirtækis til að skoða og gefa skýrslu um reksturinn frá ýmsum sjónarhornum.</span><span class="sxs-lookup"><span data-stu-id="874db-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="874db-106">Til dæmis er hægt að setja upp eitt stigveldi fyrir skattalega-, lagalega- eða lögboðna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="874db-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="874db-107">Hægt að setja upp annað stigveldi til að gefa skýrslu um fjárhagslegar upplýsingar sem ekki er krafist samkvæmt lögum, en sem er notuð við innri skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="874db-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="874db-108">Áður en hægt er að stofna stigveldisskipan fyrirtækis þarf að stofna fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="874db-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="874db-109">Frekari upplýsingar eru í verkunum "Stofna lögaðila" eða "Stofna rekstrareiningu".</span><span class="sxs-lookup"><span data-stu-id="874db-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="874db-110">Einnig er hægt að stofna deildir og teymi.</span><span class="sxs-lookup"><span data-stu-id="874db-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="874db-111">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="874db-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="874db-112">Búa til stigveldi</span><span class="sxs-lookup"><span data-stu-id="874db-112">Create a hierarchy</span></span>
1. <span data-ttu-id="874db-113">Farðu í **Skoðunarrúðu > Kerfiseiningar > Fyrirtækisstjórnun > Fyrirtæki > Stigveldi fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="874db-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="874db-114">Í **aðgerðasvæðinu** er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="874db-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="874db-115">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="874db-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="874db-116">Í kaflanum **Tilgangur** skal smella á **Úthluta tilgangi**.</span><span class="sxs-lookup"><span data-stu-id="874db-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="874db-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="874db-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="874db-118">Veljið tilgangur sem úthluta á stigveldi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="874db-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="874db-119">Í hlutanum **Úthlutuð stigveldi** skal smella á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="874db-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="874db-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="874db-120">In the list, mark the selected row.</span></span> <span data-ttu-id="874db-121">Finna stigveldið sem var verið að stofna.</span><span class="sxs-lookup"><span data-stu-id="874db-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="874db-122">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="874db-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="874db-123">Bæta við fyrirtækjum í stigveldi áætlunar</span><span class="sxs-lookup"><span data-stu-id="874db-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="874db-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="874db-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="874db-125">Velja skal þitt stigveldi.</span><span class="sxs-lookup"><span data-stu-id="874db-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="874db-126">Í kaflanum **Úthlutuð stigveldi** skal smella á **Skoða stigveldi**.</span><span class="sxs-lookup"><span data-stu-id="874db-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="874db-127">Bæta við fleiri fyrirtæki eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="874db-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="874db-128">Til að bæta við fyrirtæki skal smella á **Breyta** og síðan **Setja inn** til að bæta við fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="874db-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="874db-129">Þegar gerðar eru breytingar er hægt að **Vista** drög og/eða **Birta** breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="874db-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
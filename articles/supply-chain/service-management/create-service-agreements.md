---
title: Þjónustusamningar stofnaðir
description: Þetta efnisatriði lýsir því hvernig á að nota aðgerðir þjónustustjórnunar og verkefnastjórnunar- og bókhaldskerfis til að stofna þjónustusamninga.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef5ca8cc9c80581b9f7ef69bd8c4403d3d0296e8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965967"
---
# <a name="create-service-agreements"></a><span data-ttu-id="aefa9-103">Þjónustusamningar stofnaðir</span><span class="sxs-lookup"><span data-stu-id="aefa9-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aefa9-104">Þetta efnisatriði lýsir því hvernig á að nota aðgerðir þjónustustjórnunar og verkefnastjórnunar- og bókhaldskerfis til að stofna þjónustusamninga.</span><span class="sxs-lookup"><span data-stu-id="aefa9-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="aefa9-105">Stofna þjónustusamning úr þjónustustjórnun.</span><span class="sxs-lookup"><span data-stu-id="aefa9-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="aefa9-106">Farið í **Þjónustustjórnun**.</span><span class="sxs-lookup"><span data-stu-id="aefa9-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="aefa9-107">Smellið á **Þjónustusamninga** til að stofna nýja þjónustusamningslínu á síðuhaus.</span><span class="sxs-lookup"><span data-stu-id="aefa9-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="aefa9-108">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="aefa9-108">Click **New**.</span></span> <span data-ttu-id="aefa9-109">Færið inn lýsingu, veljið tilvísun í verk í reitnum **Auðkenni verks** og fyllið inn í það sem eftir er af reitum og línum fyrir þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="aefa9-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="aefa9-110">Smellið á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="aefa9-110">Click **Save**.</span></span>
4. <span data-ttu-id="aefa9-111">Í flipanum **Tengsl** skal velja **Þjónustuhluti** eða **Þjónustuverk** til að stofna þjónustuhlutartengsl eða þjónustuverktengsl fyrir þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="aefa9-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="aefa9-112">Þjónustuhlutinn og verkið sem er búið að stofna tengsl fyrir er hægt að tengja við línur þjónustusamningsins.</span><span class="sxs-lookup"><span data-stu-id="aefa9-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="aefa9-113">Í neðri hluta síðunnar skal stofna þjónustusamningslínur með því að afrita línur úr þjónustusniðmáti, öðrum þjónustusamningi eða stofna þjónustusamningslínurnar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="aefa9-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="aefa9-114">Ef línur eru afritaðar inn í þjónustusamninginn úr öðrum þjónustusamningi er hægt að gefa til kynna hvort afrita eigi líka tengsl þjónustuhluta og þjónustuverka.</span><span class="sxs-lookup"><span data-stu-id="aefa9-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="aefa9-115">Ef þessi tengsl eru afrituð er þeim bætt við öll tengsl sem fyrir eru í þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="aefa9-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="aefa9-116">Ef þjónustupöntunarlínur eru afritaðar úr þjónustusniðmáti eru tengsl þjónustuhluta og þjónustuverka sjálfkrafa afritaðar sem tengsl þjónustuhlutar og tengsl þjónustuverks í nýju þjónustusamningslínunum.</span><span class="sxs-lookup"><span data-stu-id="aefa9-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="aefa9-117">Stofna þjónustusamningslínur handvirkt</span><span class="sxs-lookup"><span data-stu-id="aefa9-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="aefa9-118">Bætið við þjónustusamningslínu við hnitanetið á síðu **Þjónustusamninga**.</span><span class="sxs-lookup"><span data-stu-id="aefa9-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="aefa9-119">Færið inn viðeigandi upplýsingar fyrir línu þjónustusamningsins.</span><span class="sxs-lookup"><span data-stu-id="aefa9-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="aefa9-120">Ýtið á **CTRL+S** til að vista línuna og loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="aefa9-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="aefa9-121">Stofnið þjónustusamninga úr verki</span><span class="sxs-lookup"><span data-stu-id="aefa9-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="aefa9-122">Smellið á **Verkefnastjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="aefa9-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="aefa9-123">Smellið á **Öll verk**.</span><span class="sxs-lookup"><span data-stu-id="aefa9-123">Click **All projects**.</span></span>
3. <span data-ttu-id="aefa9-124">Veljið verkið úr listanum.</span><span class="sxs-lookup"><span data-stu-id="aefa9-124">Select the project from the list.</span></span>
4. <span data-ttu-id="aefa9-125">Í **Aðgerðarrúðunni** er smellt á **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="aefa9-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="aefa9-126">Í **Nýja** aðgerðarhópnum er smellt á **Þjónustu** og **Þjónustusamningur** valið.</span><span class="sxs-lookup"><span data-stu-id="aefa9-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="aefa9-127">Fylgið skrefunum í hlutanum sem heitir **Stofna þjónustusamning** eins og áður var lýst í þessu efnisatriði til að færa inn verktilvísunina.</span><span class="sxs-lookup"><span data-stu-id="aefa9-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="aefa9-128">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="aefa9-128">Related topics</span></span>

[<span data-ttu-id="aefa9-129">Yfirlit yfir þróaða og innleidda þjónustusamninga</span><span class="sxs-lookup"><span data-stu-id="aefa9-129">Develop and establish service agreements overview</span></span>](service-agreements.md)



---
title: Þjónustustig og lýsing
description: Þetta efni skýrir þjónustustig og lýsingu í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0aa23e7fe10e684e110126bd58bd761348e44700
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215494"
---
# <a name="service-level-and-description"></a><span data-ttu-id="8fd19-103">Þjónustustig og lýsing</span><span class="sxs-lookup"><span data-stu-id="8fd19-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8fd19-104">Þegar þú býrð til verkbeiðni gætirðu viljað skilgreina þjónustustig fyrir hana og bæta við almennri lýsingu.</span><span class="sxs-lookup"><span data-stu-id="8fd19-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="8fd19-105">Þú getur búið til þjónustustig verkbeiðni á síðunni **Þjónustustig verkbeiðni** og lýsingar á síðunni **Verkbeiðnilýsing**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="8fd19-106">Stofna þjónustustig</span><span class="sxs-lookup"><span data-stu-id="8fd19-106">Create a service level</span></span>

1. <span data-ttu-id="8fd19-107">Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Þjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="8fd19-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-108">Select **New**.</span></span>
3. <span data-ttu-id="8fd19-109">Í reitinn **Þjónustustig** slærðu inn þjónustustigið (til dæmis tölu).</span><span class="sxs-lookup"><span data-stu-id="8fd19-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="8fd19-110">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="8fd19-111">Á flýtiflipanum **Verkbeiðnir** er hægt að skilgreina áætlaðar upphafs- og lokadagsetningar og tíma.</span><span class="sxs-lookup"><span data-stu-id="8fd19-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="8fd19-112">Reitirnir á þessum flýtiflipa skilgreina tímabilið sem byrja skal og ljúka verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="8fd19-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="8fd19-113">Þeir eru notaðir fyrir verkbeiðnir sem eru stofnaðar handvirkt og verkbeiðnir sem eru stofnaðar á grundvelli viðhaldsbeiðna.</span><span class="sxs-lookup"><span data-stu-id="8fd19-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="8fd19-114">Í reitinn **Upphafsdagur** slærðu inn fjölda daga til að skilgreina tímabilið þegar verkbeiðnin skal hefjast.</span><span class="sxs-lookup"><span data-stu-id="8fd19-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="8fd19-115">Fjöldi daga er reiknaður úr stofndagsetningu verkbeiðninnar.</span><span class="sxs-lookup"><span data-stu-id="8fd19-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="8fd19-116">Til dæmis, ef verkbeiðnin skal hefjast þegar hún er búin til, sláðu þá inn **0**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="8fd19-117">Ef verkbeiðnin skal hefjast innan einnar viku eftir að hún er búin til, sláðu þá inn **7**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="8fd19-118">Til að stilla upphafstíma fyrir verkbeiðnina, auk upphafsdagsetningar, skaltu stilla valkostinn **Stilla upphafstíma** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="8fd19-119">Sláðu síðan upphafstímann inn í reitinn **Upphafstími**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="8fd19-120">Ef þú stillir möguleikann á **Nei** er núverandi tími dags notaður.</span><span class="sxs-lookup"><span data-stu-id="8fd19-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="8fd19-121">Í reitinn **Lokadagur** slærðu inn fjölda daga til að skilgreina tímabilið þegar verkbeiðni skal ljúka.</span><span class="sxs-lookup"><span data-stu-id="8fd19-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="8fd19-122">Fjöldi daga er reiknaður úr upphafsdagsetningu verkbeiðninnar.</span><span class="sxs-lookup"><span data-stu-id="8fd19-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="8fd19-123">Til dæmis, ef verkbeiðnin skal ljúka innan viku frá upphafsdegi hennar, sláðu þá inn **7**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="8fd19-124">Til að stilla lokatíma fyrir verkbeiðnina, auk lokadagsetningar, skaltu stilla valkostinn **Stilla lokatíma** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="8fd19-125">Sláðu síðan lokastímann inn í reitinn **Lokatími**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="8fd19-126">Ef þú stillir möguleikann á **Nei** er núverandi tími dags notaður.</span><span class="sxs-lookup"><span data-stu-id="8fd19-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="8fd19-127">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-127">Select **Save**.</span></span>

![Síðan Þjónustustig verkbeiðna](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="8fd19-129">Stofna lýsingu</span><span class="sxs-lookup"><span data-stu-id="8fd19-129">Create a description</span></span>

1. <span data-ttu-id="8fd19-130">Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Lýsingar**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="8fd19-131">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-131">Select **New**.</span></span>
3. <span data-ttu-id="8fd19-132">Í reitnum **Lýsing** skal færa inn lýsinguna.</span><span class="sxs-lookup"><span data-stu-id="8fd19-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="8fd19-133">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8fd19-133">Select **Save**.</span></span>

--- 
title: "Skilgreina möguleika tilfanga"
description: "Tilfangageta lýsa því hvað rekstrartilföng getur gert."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: aa24d9506b8d044679403039e9c659a1ebbd2d5d
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="define-resource-capabilities"></a><span data-ttu-id="27b8e-103">Skilgreina möguleika tilfanga</span><span class="sxs-lookup"><span data-stu-id="27b8e-103">Define resource capabilities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27b8e-104">Tilfangageta lýsa því hvað rekstrartilföng getur gert.</span><span class="sxs-lookup"><span data-stu-id="27b8e-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="27b8e-105">Við áætlunargerð, eru allar kröfur vinnslu og jafnaðar gagnvart getu tiltæk tilfanga.</span><span class="sxs-lookup"><span data-stu-id="27b8e-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="27b8e-106">Þessi leiðarvísi fyrir verk aðstoðar við að stofna getu tilfangs og úthluta á tilföngum.</span><span class="sxs-lookup"><span data-stu-id="27b8e-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="27b8e-107">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="27b8e-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="27b8e-108">Stofna tilfangagetu.</span><span class="sxs-lookup"><span data-stu-id="27b8e-108">Create a resource capability</span></span>
1. <span data-ttu-id="27b8e-109">Fara á Tilfangagetu</span><span class="sxs-lookup"><span data-stu-id="27b8e-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="27b8e-110">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="27b8e-110">Click New.</span></span>
3. <span data-ttu-id="27b8e-111">Færið inn Kenni tilfangagetu í svæðinu Getu.</span><span class="sxs-lookup"><span data-stu-id="27b8e-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="27b8e-112">Fyrir tiltekna aðgerð, notarðu auðkenni getu til að tilgreina að tilfanga verður að hafa þennan getu til að framkvæma aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="27b8e-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="27b8e-113">Í reitinn Lýsing er færð stutt lýsing á getunni.</span><span class="sxs-lookup"><span data-stu-id="27b8e-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="27b8e-114">Úthluta getu á tilföng</span><span class="sxs-lookup"><span data-stu-id="27b8e-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="27b8e-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="27b8e-115">Click Add.</span></span>
2. <span data-ttu-id="27b8e-116">Færið inn Kenni tilfanga í svæðinu Tilfanga.</span><span class="sxs-lookup"><span data-stu-id="27b8e-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="27b8e-117">Hægt er að úthluta getu tilfangs á ein eða fleiri tilföng.</span><span class="sxs-lookup"><span data-stu-id="27b8e-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="27b8e-118">Í reitinn lokadagsetning, skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="27b8e-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="27b8e-119">Hægt er að nota þetta svæði til að tilgreina að tilföng hefur getuna fyrir aðeins takmarkaðan tíma.</span><span class="sxs-lookup"><span data-stu-id="27b8e-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="27b8e-120">Í reitinn forgangur skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="27b8e-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="27b8e-121">Þegar þú áætlar vinnslur og aðgerðir, hægt er að tilgreina hvort að velja tilföng eftir forgangi.</span><span class="sxs-lookup"><span data-stu-id="27b8e-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="27b8e-122">Ef valið er að gera þetta, og fleiri en einn tilföng geta framkvæmt vinnslu eða aðgerðar á umbeðna dagsetningu, er valið tilfang með minnstan forgang með tilliti til getu sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="27b8e-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="27b8e-123">Í reitinn Stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="27b8e-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="27b8e-124">Þegar tilgreindur er vinnslu eða aðgerð sem krefst tiltekna getu, er einnig hægt að tilgreina lágmarksstig sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="27b8e-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="27b8e-125">Notaðu getistig til að aðgreina tilföng sem geta framkvæmt sömu vinnslu en með mismunandi hraða, styrkleikum, stærðir og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="27b8e-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  



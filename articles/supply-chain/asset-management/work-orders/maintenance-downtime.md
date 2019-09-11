---
title: Niðurtími vegna viðhalds
description: Þetta efni lýsir niðurtíma vegna viðhalds í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918245"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="be29a-103">Niðurtími vegna viðhalds</span><span class="sxs-lookup"><span data-stu-id="be29a-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="be29a-104">Þú getur búið til skráningar á niðurtíma vegna viðhalds á eigninni sem er valin í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="be29a-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="be29a-105">Þetta er gagnlegt ef þú vilt skrá niðurstöðutíma viðhalds á einni eða fleiri vélum á framleiðslusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="be29a-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="be29a-106">Fyrst býrðu til ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, til dæmis sundurliðun og fyrirhugað stopp.</span><span class="sxs-lookup"><span data-stu-id="be29a-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="be29a-107">Þetta er gert í **Ástæðukóðar niðurtíma vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="be29a-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="be29a-108">Næst geturðu búið til skráningar á niðurtíma vegna viðhalds í **Niðurtími vegna viðhalds** og bæta við viðeigandi ástæðukóðum.</span><span class="sxs-lookup"><span data-stu-id="be29a-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="be29a-109">Stofna ástæðukóða niðurtíma vegna viðhalds</span><span class="sxs-lookup"><span data-stu-id="be29a-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="be29a-110">Smelltu á **Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Ástæðukóðar niðurtíma vegna viðhaldsr**.</span><span class="sxs-lookup"><span data-stu-id="be29a-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="be29a-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="be29a-111">Click **New**.</span></span>

3. <span data-ttu-id="be29a-112">Settu inn auðkenni í reitinn **Ástæðukóði niðurtíma vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="be29a-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="be29a-113">Í reitnum **Heiti** slærðu inn heiti fyrir ástæðukóðann.</span><span class="sxs-lookup"><span data-stu-id="be29a-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="be29a-114">Veldu gátreitinn **Hafa með í afkastavísi** ef ástæðukóðinn ætti að vera með í útreikningu á afkastavísi eigna.</span><span class="sxs-lookup"><span data-stu-id="be29a-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="be29a-115">Almennt ætti ekki að taka fyrirhugaða framleiðslustöðvun með í útreikninga á afkastavísi þar sem þeir hafa ekki áhrif á vænt afköst.</span><span class="sxs-lookup"><span data-stu-id="be29a-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="be29a-116">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="be29a-116">Click **Save**.</span></span>

![Mynd 1](media/15-work-orders.png)


<span data-ttu-id="be29a-118">Þegar þú hefur búið til þá ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, getur þú búið til skráningar á niðurtími vegna viðhalds fyrir verkbeiðnir og eignir.</span><span class="sxs-lookup"><span data-stu-id="be29a-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="be29a-119">Stofna skráningar niðurtíma vegna viðhalds</span><span class="sxs-lookup"><span data-stu-id="be29a-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="be29a-120">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="be29a-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="be29a-121">Veldu verkbeiðnina og smelltu á **Niðurtíma vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="be29a-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="be29a-122">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="be29a-122">Click **New**.</span></span>

4. <span data-ttu-id="be29a-123">Settu dagsetningu og tímabil fyrir skráningu niðurtíma vegna viðhalds inn í reitina **Frá** og **Til**.</span><span class="sxs-lookup"><span data-stu-id="be29a-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="be29a-124">Þegar þú ferð úr reitnum **Til** er lengd í klukkustundum sjálfkrafa sett inn í reitnum **Tímalengd**.</span><span class="sxs-lookup"><span data-stu-id="be29a-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="be29a-125">Veldu ástæðukóða í reitnum **Ástæðukóði niðurtíma vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="be29a-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="be29a-126">Endurtaktu skref 3-6 ef þú vilt bæta við fleiri skráningum.</span><span class="sxs-lookup"><span data-stu-id="be29a-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="be29a-127">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="be29a-127">Click **Save**.</span></span>


![Mynd 2](media/16-work-orders.png)


<span data-ttu-id="be29a-129">Dagatalið sem notað er til að reikna út skráningu niðurtíma vegna viðhalds fer eftir vali þínu við uppsetningu eigna og færibreytur.</span><span class="sxs-lookup"><span data-stu-id="be29a-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="be29a-130">Ef tilföng eru valin á eign í flýtiflipanum **Allar eignir** > **Fastafjármunir** > reitnum **Tilföng** er dagatalið sem sett var upp fyrir tengdan tilfangahóp notað, eins og sýnt er á myndinni hér á eftir.</span><span class="sxs-lookup"><span data-stu-id="be29a-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Mynd 3](media/17-work-orders.png)


<span data-ttu-id="be29a-132">Ef engin tilföng eru valin á eigninni er staðlað dagatal sem valið er í **Færibreytum eignastýringar** notað, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="be29a-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Mynd 4](media/18-work-orders.png)


<span data-ttu-id="be29a-134">Smelltu á **Eignastjórnun fyrirtækja** > **Fyrirspurnir** > **Niðurtími vegna viðhalds** til að sjá yfirlit yfir allar skráningar á niðurtíma vegna viðhalds.</span><span class="sxs-lookup"><span data-stu-id="be29a-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="be29a-135">Öll dagatöl sem eru notuð í einingunni **Eignastjórnun** eru sett upp í **Fyrirtækisstjórnun** > **Uppsetning** > **Dagatöl** > **Dagatöl**.</span><span class="sxs-lookup"><span data-stu-id="be29a-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>


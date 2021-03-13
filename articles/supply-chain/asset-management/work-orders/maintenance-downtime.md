---
title: Niðurtími vegna viðhalds fyrir verkbeiðnir
description: Þetta efnisatriði lýsir því hvernig á að stofna niðurtímaskráningar vegna viðhalds á eigninni sem er valin í verkbeiðni.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53487a0173453ef7a8f5ea818672d999fe71cb65
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020912"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="5d8fc-103">Niðurtími vegna viðhalds fyrir verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="5d8fc-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="5d8fc-104">Þú getur búið til skráningar á niðurtíma vegna viðhalds á eigninni sem er valin í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="5d8fc-105">Þessi afkastageta er gagnleg ef þú vilt skrá niðurstöðutíma viðhalds á einni eða fleiri vélum á framleiðslusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="5d8fc-106">Fyrst býrðu til ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, eins og **Sundurliðun** og **Fyrirhugað stopp**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="5d8fc-107">Þetta skref er gert á síðunni **Ástæðukóðar niðurtíma vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="5d8fc-108">Síðan geturðu búið til skráningar á niðurtíma vegna viðhalds á síðunni **Niðurtími vegna viðhalds** og bætt við viðeigandi ástæðukóðum niðurtíma vegna viðhalds.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="5d8fc-109">Stofna ástæðukóða niðurtíma vegna viðhalds</span><span class="sxs-lookup"><span data-stu-id="5d8fc-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="5d8fc-110">Veldu **Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Ástæðukóðar niðurtíma vegna viðhaldsr**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="5d8fc-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-111">Select **New**.</span></span>

3. <span data-ttu-id="5d8fc-112">Í reitnum **Ástæðukóði niðurtíma vegna viðhalds** slærðu inn kenni fyrir ástæðukóða niðurtíma vegna viðhalds.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="5d8fc-113">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="5d8fc-114">Veldu gátreitinn **Hafa með í afkastavísi** ef ástæðukóðinn ætti að vera með í útreikningum á afkastavísi (KPI) fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="5d8fc-115">Almennt ætti ekki að taka fyrirhugaða framleiðslustöðvun með í útreikninga á afkastavísi þar sem þeir hafa ekki áhrif á vænt afköst.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="5d8fc-116">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-116">Select **Save**.</span></span>

<span data-ttu-id="5d8fc-117">Myndin hér að neðan sýnir dæmi um síðuna **Ástæðukóðar niðurtíma vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Mynd 1](media/15-work-orders.png)

<span data-ttu-id="5d8fc-119">Þegar þú hefur búið til þá ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, getur þú búið til skráningar á niðurtími vegna viðhalds fyrir verkbeiðnir og eignir.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="5d8fc-120">Stofna skráningar niðurtíma vegna viðhalds</span><span class="sxs-lookup"><span data-stu-id="5d8fc-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="5d8fc-121">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5d8fc-122">Veldu verkbeiðni og síðan á flipanum **Verkbeiðni**, í hópnum **Eign**, velurðu **Niðurtími vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="5d8fc-123">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-123">Select **New**.</span></span>

4. <span data-ttu-id="5d8fc-124">Í reitunum **Frá** og **Til** skilgreinirðu dagsetningu og tímabil fyrir skráningu á niðurtíma vegna viðhalds.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="5d8fc-125">Þegar þú ferð úr reitnum **Til** er lengd í klukkustundum sjálfkrafa sett inn í reitnum **Tímalengd**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="5d8fc-126">Í reitnum **Ástæðukóði niðurtíma vegna viðhalds** velurðu ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="5d8fc-127">Endurtakið skref 3 til og með 5 til að bæta við fleiri skráningum.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="5d8fc-128">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-128">Select **Save**.</span></span>

<span data-ttu-id="5d8fc-129">Eftirfarandi skýringarmynd hér að neðan sýnir dæmi um skráningu á niðurtíma vegna viðhalds.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Mynd 2](media/16-work-orders.png)

<span data-ttu-id="5d8fc-131">Dagatalið sem notað er til að reikna út skráningu niðurtíma vegna viðhalds fer eftir vali þínu við uppsetningu eigna og færibreytur.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="5d8fc-132">Ef tilföng eru valin á eign í reitnum **Tilföng** á flýtiflipanum **Föst eign** á síðunni **Allar eignir** er datalið sem sett var upp fyrir tengdan tilfangahóp notað, eins og sýnt er á myndinni hér á eftir.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Mynd 3](media/17-work-orders.png)

<span data-ttu-id="5d8fc-134">Ef engin tilföng eru valin á eigninni er staðlað dagatal sem valið er á síðunni **Færibreytum eignastýringar** notað, eins og sýnt er á eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Mynd 4](media/18-work-orders.png)

<span data-ttu-id="5d8fc-136">Til að sjá yfirlit yfir allar skráningar á niðurtíma vegna viðhalds smellirðu á **Eignastjórnun fyrirtækja** > **Fyrirspurnir** > **Niðurtími vegna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="5d8fc-137">Öll dagatöl sem eru notuð í einingunni **Eignastjórnun** eru sett upp í **Fyrirtækisstjórnun** > **Uppsetning** > **Dagatöl** > **Dagatöl**.</span><span class="sxs-lookup"><span data-stu-id="5d8fc-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>


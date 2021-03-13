---
title: Verkbeiðnihópar
description: Þetta efnisatriði lýsir því hvernig á að vinna með verkbeiðnisöfn í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: afea5b8d0f958c3ab53d6cef8c9a0e9030d7c67b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017518"
---
# <a name="work-order-pools"></a><span data-ttu-id="0d294-103">Verkbeiðnihópar</span><span class="sxs-lookup"><span data-stu-id="0d294-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="0d294-104">Þú getur notað verkbeiðnisöfn til að flokka verkbeiðnir sem eiga eitthvað sameiginlegt.</span><span class="sxs-lookup"><span data-stu-id="0d294-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="0d294-105">Hér eru nokkur dæmi um hluti sem þú getur búið til verkbeiðnisöfn fyrir:</span><span class="sxs-lookup"><span data-stu-id="0d294-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="0d294-106">Vinnuáhafnir, til dæmis viðhaldsáhafnir A eða viðhaldsáhafnir B</span><span class="sxs-lookup"><span data-stu-id="0d294-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="0d294-107">Faglega færni, til dæmis rafvirkjar eða pípulagningarmenn</span><span class="sxs-lookup"><span data-stu-id="0d294-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="0d294-108">Efnislegar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="0d294-108">Physical locations</span></span>  

- <span data-ttu-id="0d294-109">Tímaáætlanir, til dæmis vikur eða önnur tímabil</span><span class="sxs-lookup"><span data-stu-id="0d294-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="0d294-110">Hægt er að setja eina verkbeiðni í mörg verkbeiðnisöfn, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0d294-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="0d294-111">Stofna verkbeiðnasafn</span><span class="sxs-lookup"><span data-stu-id="0d294-111">Create a work order pool</span></span>

<span data-ttu-id="0d294-112">Á listasíðunni **Öll verkbeiðnisöfn** eða **Virk verkbeiðnisöfn** geturðu fengið yfirlit yfir verkbeiðnisöfn þín og búið til ný söfn.</span><span class="sxs-lookup"><span data-stu-id="0d294-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="0d294-113">Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnsöfn** > **Öll verkbeiðnasöfn** eða **Virk verkbeiðnasöfn**.</span><span class="sxs-lookup"><span data-stu-id="0d294-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="0d294-114">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0d294-114">Select **New**.</span></span>

3. <span data-ttu-id="0d294-115">Í reitnum **Safn** skal færa inn kenni fyrir verkbeiðnisafnið.</span><span class="sxs-lookup"><span data-stu-id="0d294-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="0d294-116">reitinn **Heiti** skal færa inn heiti.</span><span class="sxs-lookup"><span data-stu-id="0d294-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="0d294-117">Stilltu valkostinn **Virkt** á **Já** til að gefa til kynna að verkbeiðnisafnið sé virkt.</span><span class="sxs-lookup"><span data-stu-id="0d294-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="0d294-118">Stilltu valkostinn **Eyða samskiptum við verkbeiðni** á **Já** ef verkbeiðnir skulu vera sjálfkrafa fjarlægðar úr verkbeiðnisafninu.</span><span class="sxs-lookup"><span data-stu-id="0d294-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="0d294-119">Í reitnum **Eyða líftímastöðu** velurðu líftímastöðu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="0d294-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="0d294-120">Til dæmis væri hægt að stilla líftímastöðu verkbeiðninnar til að klára verkbeiðni til að eyða sjálfkrafa samskiptum við verkbeiðnisöfn.</span><span class="sxs-lookup"><span data-stu-id="0d294-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="0d294-121">Þú getur byrjað að bæta verkbeiðnum við verkbeiðnasafnið þitt strax.</span><span class="sxs-lookup"><span data-stu-id="0d294-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="0d294-122">Á flýtiflipanum **Verkbeiðnir** velurðu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="0d294-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="0d294-123">Í reitnum **Verkbeiðni** velurðu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="0d294-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="0d294-124">Tengdir reitir eru sjálfkrafa uppfærðir.</span><span class="sxs-lookup"><span data-stu-id="0d294-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="0d294-125">Endurtakið skref 8 til og með 9 til að bæta við fleiri verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="0d294-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="0d294-126">Ef verkbeiðnir sem þú bætir við ættu að vera gerðar í tiltekinni röð er hægt að slá inn í reitinn **Röð** tölurnar **1**, **2**, **3**, og svo framvegis, til að tilgreina þá röð.</span><span class="sxs-lookup"><span data-stu-id="0d294-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="0d294-127">Til að skoða lista yfir allar vinnupantanir sem eru innifaldar í vinnupöntunarlauginni, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Skoða safn yfir tengdar verkbeiðnir**, veldu **Verkbeiðnir** til að opna listasíðuna **Allar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="0d294-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="0d294-128">Til að reikna og skoða getu álags fyrir viðhaldsáætlun, óskipulagðar verkbeiðnir og áætlaðar verkbeiðnir, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Skoða safn yfir tengdar verkbeiðnir**, veldu **Álag** til að opna gluggann **Reikna álag**.</span><span class="sxs-lookup"><span data-stu-id="0d294-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="0d294-129">Til að reikna og skoða spár fyrir hluti (varahluti og aðra áskilda hluti) sem tengjast viðhaldsáætlun, óskipulagðar verkbeiðnir og áætlaðar verkbeiðnir, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Skoða safn yfir tengdar verkbeiðnir**, veldu **Vöruspá** til að opna gluggann **Reikna vöruspá**.</span><span class="sxs-lookup"><span data-stu-id="0d294-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="0d294-130">Til að skoða lista yfir innkaupabeiðnir sem tengjast verkbeiðnum í verkbeiðnisafninu, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Innkaup**, veldu **Innkaupabeiðni verkbeiðni** til að opna listasíðuna **Innkaupabeiðni verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="0d294-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="0d294-131">Til að skoða lista yfir innkaupapantanir sem tengjast verkbeiðnum í verkbeiðnisafninu, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Innkaup**, veldu **Innkaup verkbeiðni** til að opna listasíðuna **Innkaup verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="0d294-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="0d294-132">Þegar verkbeiðnisafn er ekki lengur viðeigandi fyrir vinnuáætlun þína skaltu stilla gátreitinn **Virkt** fyrir safnið á **Nei** í listasýninni á síðunni **Verkbeiðnisafn**.</span><span class="sxs-lookup"><span data-stu-id="0d294-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="0d294-133">Til að eyða öllum pöntunarlínum starfsmanna stillirðu valkostinn **Eyða samskiptum við verkbeiðni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="0d294-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="0d294-134">Þessi valkostur er gagnlegur ef þú vilt til dæmis búa til tómt safn sem þú getur notað seinna fyrir aðrar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="0d294-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="0d294-135">Þegar þú ert tilbúin/n til að nota verkbeiðnasafnið til að stofna ný tengsl verkbeiðna skaltu muna að stilla valkostinn **Eyða samskiptum við verkbeiðni** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="0d294-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="0d294-136">Skýringarmyndin hér að neðan sýnir dæmi um listasíðuna **Verkbeiðnasafn**.</span><span class="sxs-lookup"><span data-stu-id="0d294-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Mynd 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="0d294-138">Bættu verkbeiðni við verkbeiðnasafn</span><span class="sxs-lookup"><span data-stu-id="0d294-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="0d294-139">Eins og lýst er í kaflanum hér á undan, geturðu bætt verkbeiðnum við verkbeiðnisafn þegar þú stofnar safnið.</span><span class="sxs-lookup"><span data-stu-id="0d294-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="0d294-140">Þú getur líka bætt verkbeiðnum við verkbeiðnasafnið á listasíðunni **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="0d294-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="0d294-141">Veldu verkbeiðni og síðan á aðgerðarrúðunni, á flipanum **Verkbeiðni**, í hópnum **Viðhalda**, velurðu **Verkbeiðnisafn**.</span><span class="sxs-lookup"><span data-stu-id="0d294-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="0d294-142">Veldu verkbeiðnina á listanum og smelltu á **Verkbeiðnasafn**.</span><span class="sxs-lookup"><span data-stu-id="0d294-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="0d294-143">Í glugganum **Viðhalda verkbeiðnisafni** í reitnum **Bæta við/fjarlægja**, veldu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0d294-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="0d294-144">Í reitnum **Safn** velurðu verkbeiðnasafnið.</span><span class="sxs-lookup"><span data-stu-id="0d294-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="0d294-145">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0d294-145">Select **OK**.</span></span>

6. <span data-ttu-id="0d294-146">Til að setja verkbeiðnina sem þú bætir við í tiltekna röð í verkbeiðnasafnið, á listasíðunni **Öll verkbeiðnisöfn** eða **Virk verkbeiðnasöfn**, veldu safnið og veldu síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0d294-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="0d294-147">Síðan, á síðunni **Verkbeiðnasafn**, á flýtiflipanum **Verkbeiðnir**, notarðu reitinn **Röð** til að aðlaga röðun verkbeiðna sem eru innifaldar í safninu.</span><span class="sxs-lookup"><span data-stu-id="0d294-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="0d294-148">Til að fjarlægja valda vinnupöntun úr verkbeiðnasafni skaltu endurtaka þessi skref en velja **Fjarlægja** í þrepi 3.</span><span class="sxs-lookup"><span data-stu-id="0d294-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>


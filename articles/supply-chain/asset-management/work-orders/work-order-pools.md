---
title: Verkbeiðnihópar
description: Þetta efnisatriði lýsir því hvernig á að vinna með verkbeiðnisöfn í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875715"
---
# <a name="work-order-pools"></a><span data-ttu-id="d5c13-103">Verkbeiðnihópar</span><span class="sxs-lookup"><span data-stu-id="d5c13-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="d5c13-104">Þú getur notað verkbeiðnisöfn til að flokka verkbeiðnir sem eiga eitthvað sameiginlegt.</span><span class="sxs-lookup"><span data-stu-id="d5c13-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="d5c13-105">Til dæmis er hægt að búa til verkbeiðnisöfn fyrir</span><span class="sxs-lookup"><span data-stu-id="d5c13-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="d5c13-106">vinnuáhafnir, til dæmis viðhaldsáhafnir A, viðhaldsáhafnir B</span><span class="sxs-lookup"><span data-stu-id="d5c13-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="d5c13-107">faglega færni, til dæmis rafvirkjar eða pípulagningarmenn</span><span class="sxs-lookup"><span data-stu-id="d5c13-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="d5c13-108">efnislegar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="d5c13-108">physical locations</span></span>  

- <span data-ttu-id="d5c13-109">tímaáætlanir, til dæmis vikur eða önnur tímabil</span><span class="sxs-lookup"><span data-stu-id="d5c13-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="d5c13-110">Ef þess er krafist er hægt að setja eina verkbeiðni í mörg verkbeiðnisöfn.</span><span class="sxs-lookup"><span data-stu-id="d5c13-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="d5c13-111">Stofna verkbeiðnasafn</span><span class="sxs-lookup"><span data-stu-id="d5c13-111">Create work order pool</span></span>

<span data-ttu-id="d5c13-112">Í **Öllum verkbeiðnisöfnum** eða **Virkum verkbeiðnisöfnum** geturðu fengið yfirlit yfir verkbeiðnisöfn þín og búið til ný söfn.</span><span class="sxs-lookup"><span data-stu-id="d5c13-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="d5c13-113">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnsöfn** > **Öll verkbeiðnasöfn** eða **Virk verkbeiðnasöfn**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="d5c13-114">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-114">Click **New**.</span></span>

3. <span data-ttu-id="d5c13-115">Settu inn kenni verkbeiðnisafns í reitinn **Safn** og heiti í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="d5c13-116">Veldu „Já“ á skiptihnappnum **Virkur** til að gefa til kynna að verkbeiðnisafnið sé virkt.</span><span class="sxs-lookup"><span data-stu-id="d5c13-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="d5c13-117">Veldu „Já“ á skiptihnappnum **Eyða samskiptum við verkbeiðni** ef þú vilt að verkbeiðnir verði sjálfkrafa fjarlægðar úr verkbeiðnisafninu.</span><span class="sxs-lookup"><span data-stu-id="d5c13-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="d5c13-118">Í reitnum **Eyða líftímastöðu** velurðu líftímastöðu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="d5c13-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="d5c13-119">Til dæmis væri hægt að stilla líftímastöðu verkbeiðninnar til að klára verkbeiðni til að eyða sjálfkrafa samskiptum við verkbeiðnisöfn.</span><span class="sxs-lookup"><span data-stu-id="d5c13-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="d5c13-120">Þú getur byrjað að bæta verkbeiðnum við verkbeiðnasafnið þitt strax.</span><span class="sxs-lookup"><span data-stu-id="d5c13-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="d5c13-121">Á flýtiflipanum **Verkbeiðnir** er smellt á **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="d5c13-122">Veldu verkbeiðni í reitnum **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="d5c13-123">Tengdir reitir eru sjálfkrafa uppfærðir.</span><span class="sxs-lookup"><span data-stu-id="d5c13-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="d5c13-124">Endurtaktu skref 7-8 ef þú vilt bæta við fleiri verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="d5c13-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="d5c13-125">Í reitnum **Flokkun** geturðu gefið til kynna hvort verkbeiðnirnar ættu að fara fram í ákveðinni röð.</span><span class="sxs-lookup"><span data-stu-id="d5c13-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="d5c13-126">Settu inn tölur 1, 2, 3 og svo framvegis til að gefa til kynna ákveðna röð fyrir valdar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="d5c13-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="d5c13-127">Smelltu á hnappinn **Verkbeiðnir** til að sjá lista yfir allar verkbeiðnir sem fylgja með í verkbeiðnisafninu.</span><span class="sxs-lookup"><span data-stu-id="d5c13-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="d5c13-128">Smelltu á hnappinn **Álag** til að opna **Álag** til að reikna og skoða álag fyrir viðhaldsskema, óáætlaðar verkbeiðnir og áætlaðar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="d5c13-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="d5c13-129">Smelltu á hnappinn **Vöruspá** til að opna **Vöruspá** til að reikna út og skoða spár fyrir vörur (varahluti og aðrar umbeðnar vörur) sem tengjast viðhaldsskema, óáætluðum verkbeiðnum og áætluðum verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="d5c13-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="d5c13-130">Smelltu á hnappinn **Innkaupabeiðni um verkbeiðni** til að opna listann **Innkaupabeiðni um verkbeiðni** til að sjá lista yfir innkaupabeiðnir sem tengjast verkbeiðnum í verkbeiðnasafni.</span><span class="sxs-lookup"><span data-stu-id="d5c13-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="d5c13-131">Smelltu á hnappinn **Innkaupabeiðni um verkbeiðni** til að opna listann **Innkaupabeiðni um verkbeiðni** til að sjá lista yfir innkaupapandanir sem tengjast verkbeiðnum í verkbeiðnasafni.</span><span class="sxs-lookup"><span data-stu-id="d5c13-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="d5c13-132">Þegar verkbeiðnisafn er ekki lengur viðeigandi fyrir vinnuáætlun þína skaltu stilla gátreitinn **Virkur** fyrir safnið á „Nei“ í listasýninni **Verkbeiðnisafn**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="d5c13-133">Veldu gátreitinn **Eyða samskiptum við verkbeiðnir** ef þú vilt eyða öllum verkbeiðnilínum, til dæmis til að stofna tómt safn sem þú getur seinna notað fyrir aðrar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="d5c13-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="d5c13-134">Mundu að hreinsa gátreitinn **Eyða samskiptum við verkbeiðni** ef þú vilt nota verkbeiðnisafnið til að búa til ný verkbeiðnitengsl síðar.</span><span class="sxs-lookup"><span data-stu-id="d5c13-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Mynd 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="d5c13-136">Bættu verkbeiðni við verkbeiðnasafn</span><span class="sxs-lookup"><span data-stu-id="d5c13-136">Add work order to a work order pool</span></span>

<span data-ttu-id="d5c13-137">Eins og lýst er í kaflanum hér að ofan, geturðu bætt verkbeiðnum við verkbeiðnisafn þegar þú stofnar safnið.</span><span class="sxs-lookup"><span data-stu-id="d5c13-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="d5c13-138">Þú getur líka bætt við verkbeiðni í verkbeiðnasafnið úr einum af listunum **Allar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="d5c13-139">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="d5c13-140">Veldu verkbeiðnina á listanum og smelltu á **Verkbeiðnasafn**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="d5c13-141">Veldu „Bæta við“ í reitnum **Bæta við/fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="d5c13-142">Veldu verkbeiðnina í reitnum **Safn**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="d5c13-143">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-143">Click **OK**.</span></span>

6. <span data-ttu-id="d5c13-144">Eftir að þú hefur bætt verkbeiðni við verkbeiðnisafnið, ef þú vilt setja verkbeiðnina í tiltekna röð í safninu: Opnaðu eina af listasíðum verkbeiðnisafnanna, veldu safnið og smelltu á **Breyta** og aðlagaðu röðun verkbeiðnanna sem eru innifaldar í safninu í myndinni **Verkbeiðnasafn** > flýtiflipanum **Verkbeiðni** > reitnum **Flokkun**.</span><span class="sxs-lookup"><span data-stu-id="d5c13-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="d5c13-145">Ef þú vilt fjarlægja valda vinnupöntun úr verkbeiðnasafni skaltu velja „Fjarlægja“ í þrepi 3.</span><span class="sxs-lookup"><span data-stu-id="d5c13-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>


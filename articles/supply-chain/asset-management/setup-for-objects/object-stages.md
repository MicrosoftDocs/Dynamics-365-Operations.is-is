---
title: Lífferilsstöður eigna
description: Þetta efni skýrir eignalíftímastöður og líftímalíkön í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dffedfafd9d75320accf0e27f072bab6fd51f135
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016553"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="99949-103">Lífferilsstöður eigna</span><span class="sxs-lookup"><span data-stu-id="99949-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="99949-104">Þetta efni skýrir eignalíftímastöður og líftímalíkön í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="99949-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="99949-105">Líftímastöður eigna eru notaðar til að skilgreina hvort eignin sé virk eða óvirk.</span><span class="sxs-lookup"><span data-stu-id="99949-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="99949-106">Þú getur til dæmis sett upp eignalífsferilstig eins og **Stofnað**, **Virkur**, og **Hætt**.</span><span class="sxs-lookup"><span data-stu-id="99949-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="99949-107">Beiðni um líftímastöður er tengd við líftímastöður eigna.</span><span class="sxs-lookup"><span data-stu-id="99949-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="99949-108">Þess vegna, þegar beiðni er breytt í nýja líftímastöðu beiðni þá er eigninni sem fylgir beiðninni breytt í nýja líftímastöðu eignar.</span><span class="sxs-lookup"><span data-stu-id="99949-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="99949-109">Til dæmis, ef líftíma beiðni er breytt í **Á heimleið**, er líftímastöðu meðfylgjandi eignar breytt í líftímastöðuna sem var valin í reitnum **Líftímastaða á innleið** á flýtiflipanum **Líftímastaða eigna** á síðunni **Líkön líftímastöðu eigna**.</span><span class="sxs-lookup"><span data-stu-id="99949-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="99949-110">Hægt er að setja upp eignalíftímatöðu í líftímalíkönum eigna, þar sem þú getur skilgreint nauðsynleg líftímastöður fyrir mismunandi tegundir eigna.</span><span class="sxs-lookup"><span data-stu-id="99949-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="99949-111">Fyrst seturðu upp líftímastöður.</span><span class="sxs-lookup"><span data-stu-id="99949-111">You first set up lifecycle states.</span></span> <span data-ttu-id="99949-112">Síðan stofnaður líftímalíkan og velur líftímastöðu fyrir það.</span><span class="sxs-lookup"><span data-stu-id="99949-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="99949-113">Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="99949-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="99949-114">Veldu **Nýr** til að stofna nýja líftímastöðu eignar.</span><span class="sxs-lookup"><span data-stu-id="99949-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="99949-115">Í **Líftímastöðu** reitinn, sláðu inn auðkenni líftímastöðunnar.</span><span class="sxs-lookup"><span data-stu-id="99949-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="99949-116">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="99949-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="99949-117">Reiturinn **Líftímalíkön** sýnir fjölda líftímalíkana eigna sem nota líftímastöðu eigna.</span><span class="sxs-lookup"><span data-stu-id="99949-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="99949-118">Stilltu valkostinn **Virkt** á **Já** ef þessi líftímastaða á að vera virk líftímastaða (með öðrum orðum, ef hægt er að stofna verkbeiðnir fyrir eignir sem eru í þessari líftímastöðu).</span><span class="sxs-lookup"><span data-stu-id="99949-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="99949-119">Stilltu **Eyða opnum dagatalalínum** kostur á **Já** ef opnar eignadagatalalínur sem hafa eigið líftímastöðu eigna **Stofna** á að vera eytt þegar þær eru í þessari líftímastöðu.</span><span class="sxs-lookup"><span data-stu-id="99949-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="99949-120">Þessi stilling er gagnleg ef þú vilt hreinsa upp opnar viðhaldsáætlanir sem eru ekki lengur viðeigandi fyrir eignina (til dæmis ef eignin er ekki lengur virk).</span><span class="sxs-lookup"><span data-stu-id="99949-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="99949-121">Líftímastöður eigna, líftímalíkön eigna og tegundir eigna tengjast.</span><span class="sxs-lookup"><span data-stu-id="99949-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="99949-122">Þau eru notuð á sama hátt og líftímastöður verkbeiðni, líftímalíkön verkbeiðni og tegundir verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="99949-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="99949-123">Eftir að þú hefur búið til tilskildar líftímastöður eigna geturðu sett upp líftímastöður í líftímalíkönum eigna.</span><span class="sxs-lookup"><span data-stu-id="99949-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="99949-124">Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Líftímalíkön**.</span><span class="sxs-lookup"><span data-stu-id="99949-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="99949-125">Veldu **Nýr** til að stofna nýja líftímalíkani eignar.</span><span class="sxs-lookup"><span data-stu-id="99949-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="99949-126">Í **Líftímalíkan** reitinn, sláðu inn auðkenni líftímalíkansins.</span><span class="sxs-lookup"><span data-stu-id="99949-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="99949-127">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="99949-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="99949-128">Reiturinn **Líftímastöður** sýnir fjölda líftímastaða eigna sem eru valin í líftímalíkani eigna.</span><span class="sxs-lookup"><span data-stu-id="99949-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="99949-129">Reiturinn **Gerðir eigna** sýnir fjölda eignagerða sem nota líftímalíkanið.</span><span class="sxs-lookup"><span data-stu-id="99949-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="99949-130">Á flýtiflipanum **Líftímastöður** velurðu þær líftímastöður eigna sem ætti að vera með í líftímalíkani eigna:</span><span class="sxs-lookup"><span data-stu-id="99949-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="99949-131">Til að nota líftímastöðu fyrir líkanið skaltu velja það í **Eftirstandandi líftímastöður** kafla og veldu síðan hægri örvarhnappinn ![Hægri ör](media/15-setup-for-objects.png) til að færa það til **Valdar líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="99949-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="99949-132">Til að nota allar tiltækar líftímastöður fyrir líkanið velurðu hnappinn **Allar tiltækar líftímastöður** ![Allar tiltækar líftímastöður](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="99949-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="99949-133">Allar líftímastöður eru fluttar í hlutann **Valdar líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="99949-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="99949-134">Til að fjarlægja líftímastöðu úr líkani skaltu velja það í **valdar líftímastöður** kafla og veldu síðan vinstri örvarhnappinn ![Vinstri ör](media/16-setup-for-objects.png) til að færa það til **Eftirstandandi líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="99949-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="99949-135">Veldu **Uppfærslur á líftímastöðu** til að skilgreina líftímastöður eignar sem geta fylgt valinni líftímastöðu.</span><span class="sxs-lookup"><span data-stu-id="99949-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="99949-136">Þú notar flýtiflipann **Eignarstaða** ef þú annast eignir sem þú færð til viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="99949-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="99949-137">Í hlutanum **Innleið/útleið**, getur þú valið líftímastöður eigna til að gefa til kynna verkflæði eignar sem þú færð til viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="99949-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="99949-138">Ef þú býður upp á eignir til viðskiptavina eða deilda, í **Lán** kafla, getur þú valið líftímastöðu fyrir lánaeignir.</span><span class="sxs-lookup"><span data-stu-id="99949-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>

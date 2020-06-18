---
title: Samþætta eignastýringu með eignum
description: Þetta efnisatriði útskýrir hvernig á að samþætta einingar eignastýringar og eigna til að tengja saman eignir og viðhaldseignir.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276929"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="733d7-103">Samþætta eignastýringu með eignum</span><span class="sxs-lookup"><span data-stu-id="733d7-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="733d7-104">Með því að samþætta einingar **Eignastýringar** og **Eigna**, geturðu tengt eignir við viðhaldseignir.</span><span class="sxs-lookup"><span data-stu-id="733d7-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="733d7-105">Notendur eigna geta síðan búið til viðhaldseign úr nýrri eða núverandi eign og notendur eignastýringar geta tengt viðhaldseign við núverandi eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="733d7-106">Þessi eiginleiki gerir það einnig auðvelt fyrir notendur eigna að skoða kostnaðinn sem var bókaður úr verkbeiðnum vegna tengdra viðhaldseigna.</span><span class="sxs-lookup"><span data-stu-id="733d7-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="733d7-107">Í þessu efnisatriði vísa *viðhaldseignir* til eigna úr einingu **Eignastýringar** og *eignir* vísa til eigna úr einingunni **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="733d7-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="733d7-108">Veldu sjálfgefna staðsetningu að eigin vali fyrir nýjar viðhaldseignir sem eru búnar til úr eignum (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="733d7-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="733d7-109">Þessi valfrjálsa stilling gerir þér kleift að stilla sjálfgefna staðsetningu fyrir nýjar viðhaldseignir sem eru búnar til úr eignum.</span><span class="sxs-lookup"><span data-stu-id="733d7-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="733d7-110">Yfirleitt lýkur þú við þessa grunnstillingu í eitt sinn, ef þú lýkur við hana yfirhöfuð.</span><span class="sxs-lookup"><span data-stu-id="733d7-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="733d7-111">Fylgið eftirfarandi skrefum til að ljúka þessum skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="733d7-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="733d7-112">Opnaðu **Eignastýringu \> Uppsetningu \> Færibreytur eignastýringar**.</span><span class="sxs-lookup"><span data-stu-id="733d7-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="733d7-113">Veldu flipann **Eignir** á svæðinu **Virk staðsetning** og veldu sjálfgefnu staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="733d7-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="733d7-114">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="733d7-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="733d7-115">Vinna með samþættar viðhaldseignir og eignir</span><span class="sxs-lookup"><span data-stu-id="733d7-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="733d7-116">Þessi hluti inniheldur safn aðferða sem sýnir ýmsar leiðir til að vinna með eiginleika samþættrar eignastýringar og eigna.</span><span class="sxs-lookup"><span data-stu-id="733d7-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="733d7-117">Tengja núverandi viðhaldseign við eign</span><span class="sxs-lookup"><span data-stu-id="733d7-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="733d7-118">Fylgdu þessum skrefum til að tengja viðhaldseign sem fyrir er við eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="733d7-119">Opnaðu **Eignastýringu \> Eignir \> Allar eignir** (eða **Virkar eignir**).</span><span class="sxs-lookup"><span data-stu-id="733d7-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="733d7-120">Veljið eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-120">Select an asset.</span></span>
1. <span data-ttu-id="733d7-121">Á flýtiflipanum **Eign** á svæðinu **Númer eignar** skal velja núverandi eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="733d7-122">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="733d7-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="733d7-123">Skoða eignina sem er tengd valinni viðhaldseign</span><span class="sxs-lookup"><span data-stu-id="733d7-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="733d7-124">Fylgdu þessum skrefum til að skoða eignina sem er tengd valinni viðhaldseign.</span><span class="sxs-lookup"><span data-stu-id="733d7-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="733d7-125">Opnaðu **Eignastýringu \> Eignir \> Allar eignir** (eða **Virkar eignir**).</span><span class="sxs-lookup"><span data-stu-id="733d7-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="733d7-126">Veljið eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-126">Select an asset.</span></span>
1. <span data-ttu-id="733d7-127">Á flýtiflipanum **Eign** á svæðinu **Númer eignar** skaltu velja tengilinn.</span><span class="sxs-lookup"><span data-stu-id="733d7-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="733d7-128">Síðan **Eignir** fyrir valdar eignir er opnuð.</span><span class="sxs-lookup"><span data-stu-id="733d7-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="733d7-129">(Yfirleitt er þessa síðu að finna undir **Eignir \> Eignir \> Eignir**.)</span><span class="sxs-lookup"><span data-stu-id="733d7-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="733d7-130">Skoðaðu viðhaldseignina sem er tengd valinni eign</span><span class="sxs-lookup"><span data-stu-id="733d7-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="733d7-131">Fylgdu þessum skrefum til að skoða viðhaldseignina sem er tengd valinni eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="733d7-132">Opna **Eignir \> Eignir \> Eignir**.</span><span class="sxs-lookup"><span data-stu-id="733d7-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="733d7-133">Veljið eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-133">Select an asset.</span></span>
1. <span data-ttu-id="733d7-134">Veldu flipann **Eignastýring** í hópnum **Skoða** og veldu **Viðhaldseign**.</span><span class="sxs-lookup"><span data-stu-id="733d7-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="733d7-135">Síðan **Viðhaldseign** verður opnuð fyrir eignina sem er tengd valinni eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="733d7-136">(Yfirleitt er þessa síðu að finna undir **Eignastýring \> Eignir \> Allar eignir**.)</span><span class="sxs-lookup"><span data-stu-id="733d7-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="733d7-137">Skoða viðhaldskostnað sem tengist eign</span><span class="sxs-lookup"><span data-stu-id="733d7-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="733d7-138">Hægt er að bóka verkbeiðnir fyrir viðhaldseignir og yfirleitt fylgir kostnaður hverri slíkri verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="733d7-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="733d7-139">Þegar eign er tengd við viðhaldseign getur þú farið beint frá eigninni til að skoða tengdan kostnað.</span><span class="sxs-lookup"><span data-stu-id="733d7-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="733d7-140">Fylgdu þessum skrefum til að skoð viðhaldskostnað sem tengist eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="733d7-141">Opna **Eignir \> Eignir \> Eignir**.</span><span class="sxs-lookup"><span data-stu-id="733d7-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="733d7-142">Veljið eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-142">Select an asset.</span></span>
1. <span data-ttu-id="733d7-143">Á Aðgerðasvæðinu á flipanum **Eignastýring** í flokknum **Skoða** skaltu velja **Viðhaldskostnaður**.</span><span class="sxs-lookup"><span data-stu-id="733d7-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="733d7-144">Síðan **Viðhaldskostnaður** er opnuð og sýnir tengdan kostnað.</span><span class="sxs-lookup"><span data-stu-id="733d7-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="733d7-145">Búa til nýja viðhaldseign fyrir núverandi eign</span><span class="sxs-lookup"><span data-stu-id="733d7-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="733d7-146">Fylgdu þessum skrefum til að búa til nýja viðhaldseign fyrir núverandi eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="733d7-147">Opna **Eignir \> Eignir \> Eignir**.</span><span class="sxs-lookup"><span data-stu-id="733d7-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="733d7-148">Veljið eign.</span><span class="sxs-lookup"><span data-stu-id="733d7-148">Select an asset.</span></span>
1. <span data-ttu-id="733d7-149">Veldu flipann **Eignastýring** í hópnum **Nýtt** og veldu **Búa til viðhaldseign**.</span><span class="sxs-lookup"><span data-stu-id="733d7-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="733d7-150">(Ef þessi valkostur er ekki tiltækur gæti viðhaldseign þegar verið tengd valinni eign.)</span><span class="sxs-lookup"><span data-stu-id="733d7-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="733d7-151">Ljúktu við að búa til eignina eins og lýst er í [Búa til eign](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="733d7-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="733d7-152">Búa til nýja eign og bæta við viðhaldseign fyrir hana</span><span class="sxs-lookup"><span data-stu-id="733d7-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="733d7-153">Fylgdu þessum skrefum til að búa til nýja eign og bæta við nýrri viðhaldseign fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="733d7-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="733d7-154">Opna **Eignir \> Eignir \> Eignir**.</span><span class="sxs-lookup"><span data-stu-id="733d7-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="733d7-155">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="733d7-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="733d7-156">Ljúktu við að búa til eign eins og lýst er í [Búa til eign](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="733d7-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="733d7-157">Veldu flipann **Eignastýring** í hópnum **Nýtt** og veldu **Búa til viðhaldseign**.</span><span class="sxs-lookup"><span data-stu-id="733d7-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="733d7-158">Ljúktu við að búa til eignina eins og lýst er í [Búa til eign](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="733d7-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="733d7-159">Fjarlægið tengslin milli tveggja eigna</span><span class="sxs-lookup"><span data-stu-id="733d7-159">Remove the association between two assets</span></span>

<span data-ttu-id="733d7-160">Í sumum tilfellum gætirðu þurft að fjarlægja tengslin á milli viðhaldseignar og eignar hennar.</span><span class="sxs-lookup"><span data-stu-id="733d7-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="733d7-161">Til dæmis, ef þú vilt [búa til nýja viðhaldseign](#new-maintenance-from-fixed) úr eign, verður þú fyrst að fjarlægja öll núverandi tengsl.</span><span class="sxs-lookup"><span data-stu-id="733d7-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="733d7-162">Fylgdu þessum skrefum til að fjarlægja núverandi tengsl milli viðhaldseignar og eignar.</span><span class="sxs-lookup"><span data-stu-id="733d7-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="733d7-163">Opnaðu **Eignastýringu \> Eignir \> Allar eignir** (eða **Virkar eignir**).</span><span class="sxs-lookup"><span data-stu-id="733d7-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="733d7-164">Finndu og opnaðu eignina.</span><span class="sxs-lookup"><span data-stu-id="733d7-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="733d7-165">Á flýtiflipanum **Eign** hreinsaðu gildið af svæðinu **Virk staðsetning**.</span><span class="sxs-lookup"><span data-stu-id="733d7-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="733d7-166">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="733d7-166">On the Action Pane, select **Save**.</span></span>
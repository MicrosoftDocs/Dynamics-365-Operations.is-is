---
title: Eignauppskriftir
description: Þetta efni lýsir eignauppskriftum (BOMs) í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e5d6d6245f27534d176ac03ca762aff91afb0ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253183"
---
# <a name="asset-boms"></a><span data-ttu-id="0b9f8-103">Eignauppskriftir</span><span class="sxs-lookup"><span data-stu-id="0b9f8-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0b9f8-104">Þetta efni lýsir eignauppskriftum (BOMs) í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="0b9f8-105">Síðan **Uppskrift eignar** sýnir lista yfir alla hluti (varahluti og aðra hluti) sem eru notaðir á eign alla sína ævi.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="0b9f8-106">Þegar þú býrð til nýja eign, ættir þú að íhuga að setja upp uppskrift eignar sem hluta af uppsetningarferlinu.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="0b9f8-107">Á þennan hátt getur þú fylgst með sögu sögu eignarinnar frá stofnunardegi.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="0b9f8-108">Eftir að þú hefur lokið viðhaldsstörfum og neysla á hlutum hefur verið skráð í vinnupöntun geturðu fylgst með neyslu varahluta og annarra hluta sem eru notaðir á eignina.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="0b9f8-109">Þessi virkni gerir þér kleift að halda fullkomna neysluskrá hluta fyrir allar eignir þínar.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="0b9f8-110">Til dæmis er hægt að nota skrána til að fylgjast með því hvort skipt er um ákveðinn varahlut eða oft til að fylgjast með varahlutunum eða öðrum hlutum sem nú eru notaðir á eign.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="0b9f8-111">Í verkbeiðni gæti neysla á vöru bæði verið varahlutir og aðrir hlutir til viðbótar, svo sem smurefni, boltar og þéttingar.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="0b9f8-112">Hægt er að uppfæra uppskrift eignar sjálfkrafa út frá uppsetningunni í eignastjórnun.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="0b9f8-113">Ef búið er að búa til líftímastöðu verkbeiðni til að meðhöndla fullgerðar eða fullgerðar verkbeiðnir, og ef **Uppfæra uppskrift eignar** valkostur fyrir þá líftímastöðu verkbeiðni er stilltur á **Já** á síðunni **Líftímastöður verkbeiðna** verða allir hlutir sem eru notaðir í vinnupöntuninni sjálfkrafa uppfærðir á **Eignastýringarkerfi** síðu þegar verkbeiðnin er uppfærð í þá líftímastöðu.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="0b9f8-114">Þú getur einnig uppfært uppskrift eignar handvirkt með því að búa til nýjar vörulínur á **Eignastýringarkerfi** síðu.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="0b9f8-115">Á síðunni **Uppskrift eignar** geturðu fylgst með sögu um varahluti fyrir eignir eftir að neysla hlutar er skráð í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="0b9f8-116">Til að nota þessa virkni verður þú að velja þá vöruhópa sem nota ætti til varahlutaskráningar á síðunni **Hlutahópar varahluta**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="0b9f8-117">Til að nota virkni uppskrifta eigna verður þú fyrst að setja upp nauðsynlega hópa varahluta.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="0b9f8-118">Síðan, ef þú vilt að uppskrift eigna verði uppfærð sjálfkrafa þegar verkbeiðni er lokið, geturðu sett upp lítímastöðu verkbeiðni til að vinna með þá uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="0b9f8-119">Setja upp vöruflokka varahluta</span><span class="sxs-lookup"><span data-stu-id="0b9f8-119">Set up spare parts item groups</span></span>

<span data-ttu-id="0b9f8-120">Uppsetning sögu varahluta er byggð á vöruflokkum sem eru búnir til í einingunni **Birgðir og vöruhúsastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="0b9f8-121">Í eignastjórnun seturðu upp vöruflokka þannig að þú getur fylgst með varahlutasögu fyrir hlutina í völdum vöruflokkum.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="0b9f8-122">Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Varahlutir hlutahópar**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="0b9f8-123">Veldu **Nýtt** til að setja upp hlutahóp.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="0b9f8-124">Veldu hópinn í reitnum **Vöruhópur**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="0b9f8-125">Nafn hópsins er fært sjálfkrafa inn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="0b9f8-126">Skoða og uppfæra uppskriftir eignar</span><span class="sxs-lookup"><span data-stu-id="0b9f8-126">View and update asset BOMs</span></span>

<span data-ttu-id="0b9f8-127">Eftir að þú hefur sent vöruneyslu í verkbeiðni geturðu skoðað skráða neyslu hlutar á síðunni **Uppskrift eignar**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="0b9f8-128">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="0b9f8-129">Veldu eignina á listanum og veldu síðan **Uppskrift eignar**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b9f8-130">Veldu til að skoða allar neysluvörur skráningar á allar eignir **Eignastýring** \> **Fyrirspurnir** \> **Eignir** \> **Uppskrift eignar**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="0b9f8-131">Veldu **Uppfæra uppskrift eignar**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="0b9f8-132">Þú getur bætt eignum, eignategundum og tilföngum við uppfærsluna eins og þú þarfnast með því að velja **Veldu**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="0b9f8-133">Veldu **Í lagi** til að hefja uppfærsluna.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-133">Select **OK** to start the update.</span></span> <span data-ttu-id="0b9f8-134">Þú getur einnig sett upp uppfærsluaðgerðina sem runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="0b9f8-135">Ef þú vilt sjá frekari upplýsingar sem tengjast hlutunum geturðu bætt við birgðavíddum.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="0b9f8-136">Veldu **Birgðir** \> **Birting vídda** og veldu síðan gátreitina fyrir víddirnar sem þú vilt sjá.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="0b9f8-137">Til að halda þessari uppsetningu fyrir allar eignir á síðunni **Uppskrift eignar** stillirðu valkostinn **Vista uppsetningu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="0b9f8-138">Til að fá yfirlit yfir hvar í eignastýringu hluturinn á völdum línum er notaður, í tengslum við eignir, vanskil starfstegunda, varahluti og verkbeiðnir, veldu **Hlutur þar sem hann er notaður**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="0b9f8-139">Ef þú vilt sjá aðeins virka hlutalínur, veldu **Skoða** \> **Núverandi**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="0b9f8-140">Veldu til að sjá allar vörulínur, þar með talið línur þar sem gildistími er eldri en núverandi dagsetning **Skoða** \> **Allt**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="0b9f8-141">Þegar þú hefur lokið verkbeiðni, ef einhverjir hlutir eða varahlutir sem tengjast skyldri eign hafa runnið út eða skipt út fyrir aðra hluti eða varahluti, mælum við með að þú uppfærir uppskrift eignar til samræmis.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="0b9f8-142">Búðu til nýja hlutalínu í uppskrift eignar</span><span class="sxs-lookup"><span data-stu-id="0b9f8-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="0b9f8-143">Þú getur búið til hlutalínur handa eignum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="0b9f8-144">Á síðunni **Uppskrift eignar** skal velja **Nýr**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="0b9f8-145">Í **Eignir** reitinn, veldu eignina sem á að bæta við hlutalínu fyrir.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="0b9f8-146">Í reitinn **Línunúmer** skal slá inn raðlínunúmer.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="0b9f8-147">Í reitnum **Árangursrík** slærðu inn upphafsdagsetningu fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="0b9f8-148">Ef hluturinn rennur út, í **Fyrning** reitinn, sláðu inn lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="0b9f8-149">Veldu vöru í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="0b9f8-150">Nafn hópsins er fært sjálfkrafa inn í reitinn **Heiti afurðar**.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="0b9f8-151">Inn í reitinn **Magn** skal slá inn magnið sem er notað.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="0b9f8-152">Reiturinn **Eining** er sjálfkrafa uppfært.</span><span class="sxs-lookup"><span data-stu-id="0b9f8-152">The **Unit** field is automatically updated.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
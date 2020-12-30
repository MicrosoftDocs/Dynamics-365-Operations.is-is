---
title: Stofna eignir byggt á innkaupapöntunum
description: Þetta efni útskýrir hvernig þú getur búið til lista yfir eignaliði sem hægt er að nota sem grunn til að búa til eignir fyrir viðhaldsverk í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430280"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="67324-103">Stofna eignir byggt á innkaupapöntunum</span><span class="sxs-lookup"><span data-stu-id="67324-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="67324-104">Þetta efni útskýrir hvernig þú getur búið til lista yfir eignaliði sem hægt er að nota sem grunn til að búa til eignir fyrir viðhaldsverk í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="67324-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="67324-105">Miðað við eignaratriðin geturðu skoðað lista yfir innkaupapöntunarlínurnar sem eru búnar til á þeim hlutum.</span><span class="sxs-lookup"><span data-stu-id="67324-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="67324-106">Tilgangurinn með þessari virkni er að búa til eign í eignastýringu auðveldlega út frá innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="67324-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="67324-107">Í fyrsta lagi setur þú upp hlutina sem á að nota til að búa til eignir frá innkaupapöntun í **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="67324-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="67324-108">Eftir að þú hefur stofnað innkaupapöntunarlínu býrðu til eignirnar í **Eignir í bið**.</span><span class="sxs-lookup"><span data-stu-id="67324-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="67324-109">Það er hægt að ákveða á hvaða stigi innkaupapöntunar eignin ætti að vera stofnuð.</span><span class="sxs-lookup"><span data-stu-id="67324-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="67324-110">Velja eignaliði</span><span class="sxs-lookup"><span data-stu-id="67324-110">Select asset items</span></span>

1. <span data-ttu-id="67324-111">Smelltu á **Eignastýring** > **Uppsetning** > **Eignir** > **Hlutir**.</span><span class="sxs-lookup"><span data-stu-id="67324-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="67324-112">Smelltu á **Nýtt** til að stofna eignalið.</span><span class="sxs-lookup"><span data-stu-id="67324-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="67324-113">Veldu vöru í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="67324-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="67324-114">Þegar þú ferð úr þessum reit er nafn vörunnar sjálfkrafa sett inn í reitinn **Vöruheiti**.</span><span class="sxs-lookup"><span data-stu-id="67324-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="67324-115">Á flýtiflipanum **Almennt** velurðuu eignategund fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="67324-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="67324-116">Veldu eignaframleiðanda og gerð fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="67324-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="67324-117">Vista vöruna</span><span class="sxs-lookup"><span data-stu-id="67324-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="67324-118">Búðu til eignir úr eignum í bið</span><span class="sxs-lookup"><span data-stu-id="67324-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="67324-119">Smelltu á **Eignastýring** > **Sameiginlegt** > **Eignir** > **Eignir í bið**.</span><span class="sxs-lookup"><span data-stu-id="67324-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="67324-120">Þú munt sjá uppfærðan lista yfir innkaupapantanir út frá vörunum sem voru valdar í **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="67324-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="67324-121">Þú getur síað stöðu innkaupapantana til að velja í hvaða líftímastöðu eignin ætti að vera búin til.</span><span class="sxs-lookup"><span data-stu-id="67324-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="67324-122">Til dæmis gætirðu aðeins viljað búa til eignir þegar vörukvittun hefur verið bókuð í innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="67324-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="67324-123">Veldu tengilinn **Tilvísunarnúmer** á innkaupapöntunarlínu til að skoða ítarlegar upplýsingar um vöruna.</span><span class="sxs-lookup"><span data-stu-id="67324-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="67324-124">Ef þú vilt breyta hvaða víddir birtast á flýtiflipanum **Birgðavíddir** smellirðu á **Sýna víddir** og velur valkosti þína.</span><span class="sxs-lookup"><span data-stu-id="67324-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="67324-125">Ef þú vilt búa til eign byggða á innkaupapöntunarlínu skaltu velja gátreitinn í dálkinum **Merkja** fyrir þá línu á listasíðunni og smella á **Stofna eignir**.</span><span class="sxs-lookup"><span data-stu-id="67324-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="67324-126">Skilaboð verða birt þar sem upplýsingar um eignaauðkenni eru tilkynntar.</span><span class="sxs-lookup"><span data-stu-id="67324-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="67324-127">Veldu eignina í listanum **Allar eignir** og smelltu á hnappinn **Breyta** til að bæta meiri upplýsingum við eignina.</span><span class="sxs-lookup"><span data-stu-id="67324-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="67324-128">Í **Eignir í bið**, ef þú vilt eyða línu af því að þú vilt ekki búa til eign skaltu velja gátreitinn í dálkinum **Merkja** fyrir þá línu og smella á **Fleygja eignum í bið**.</span><span class="sxs-lookup"><span data-stu-id="67324-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="67324-129">Skilaboð verða birt þar sem upplýsingar um eignaauðkenni eru tilkynntar.</span><span class="sxs-lookup"><span data-stu-id="67324-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="67324-130">Þú ert ekki að eyða innkaupapöntuninni eða sölupöntuninni, heldur skránni sem þú gætir hafa stofna eign frá í **Eignastýring**.</span><span class="sxs-lookup"><span data-stu-id="67324-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="67324-131">Allar vöruvíddir (stærð, litur, stillingar osfrv.) eru sjálfkrafa færðir yfir í eignareigindirnar.</span><span class="sxs-lookup"><span data-stu-id="67324-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="67324-132">Rakningarvíddir (raðnúmer) eru geymdar beint á eigninni þegar eignin er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="67324-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="67324-133">Finndu eignir í bið</span><span class="sxs-lookup"><span data-stu-id="67324-133">Find pending assets</span></span>

<span data-ttu-id="67324-134">Þú getur keyrt **Fjöldi eigna í bið** til að athuga hvort eignir séu í bið.</span><span class="sxs-lookup"><span data-stu-id="67324-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="67324-135">Til dæmis er hægt að nota þessa aðgerð til að fá tilkynningu í hvert skipti sem eign í bið er tilbúin til að búa til sem eign.</span><span class="sxs-lookup"><span data-stu-id="67324-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="67324-136">Smelltu á **Eignastýring** > **Reglubundið** > **Eignir** > **Fjöldi eigna í bið**.</span><span class="sxs-lookup"><span data-stu-id="67324-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="67324-137">Smelltu á **Í lagi** til að keyra starfið og uppfæra listann í **Eignir í bið**.</span><span class="sxs-lookup"><span data-stu-id="67324-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="67324-138">Þú getur sett þetta starf upp til að keyra sem runuvinnslu, til dæmis einu sinni á dag.</span><span class="sxs-lookup"><span data-stu-id="67324-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="67324-139">**Varúð:** Ef gögnum er breytt í innkaupapöntun *eftir* að þú hefur búið til eign byggða á vörunni sem hún tilheyrir munu þessar breytingar ekki koma fram á eigninni.</span><span class="sxs-lookup"><span data-stu-id="67324-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>

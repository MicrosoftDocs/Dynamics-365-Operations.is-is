---
title: Búa til nýtt vöruhúsaútlit
description: Þetta efnisatriði lýsir hvernig setja á upp upplýsingar um staðsetningar í vöruhúsi.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07fee1787cc2719bafbe2bb6d54849edda14018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000035"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="f092e-103">Búa til nýtt vöruhúsaútlit</span><span class="sxs-lookup"><span data-stu-id="f092e-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f092e-104">Þetta efnisatriði lýsir hvernig setja á upp upplýsingar um staðsetningar í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="f092e-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="f092e-105">Þetta á aðeins við vöruhús sem eru stofnaðar með "grunn vöruhús" í kerfinu birgðastjórnun, ekki á við vöruhús sem er stofnað í vöruhúsakerfinu.</span><span class="sxs-lookup"><span data-stu-id="f092e-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="f092e-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="f092e-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="f092e-107">Stilla sjálfgefna afkastagetu staðsetningar</span><span class="sxs-lookup"><span data-stu-id="f092e-107">Set the default location capacity</span></span>
1. <span data-ttu-id="f092e-108">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Birgðir og færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="f092e-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="f092e-109">Veldu flipann **Staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="f092e-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="f092e-110">Í reitinn **Stöðluð breidd** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="f092e-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="f092e-111">Í reitinn **Stöðluð dýpt** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f092e-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="f092e-112">Í reitinn **Stöðluð hæð** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="f092e-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="f092e-113">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f092e-113">Select **Save**.</span></span>
7. <span data-ttu-id="f092e-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f092e-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="f092e-115">Skilgreina heiti staðsetningarsniðið</span><span class="sxs-lookup"><span data-stu-id="f092e-115">Define the location name format</span></span>
1. <span data-ttu-id="f092e-116">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Niðurbrot birgða > Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="f092e-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="f092e-117">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f092e-117">Select **New**.</span></span>
3. <span data-ttu-id="f092e-118">Í reitinn **Vöruhús** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f092e-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="f092e-119">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f092e-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f092e-120">Í reitnum **Svæði** velurðu skrána sem óskað er eftir í uppflettingunni.</span><span class="sxs-lookup"><span data-stu-id="f092e-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="f092e-121">Víxla útvíkkun á liðnum **Heiti staðsetninga**.</span><span class="sxs-lookup"><span data-stu-id="f092e-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="f092e-122">Valkostirnir í þessum hluta er að skilgreina sjálfgefið snið fyrir heiti staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f092e-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="f092e-123">Í dæminu okkar mælt verður að innihalda gangnúmers, rekkanúmer og hillunúmer.</span><span class="sxs-lookup"><span data-stu-id="f092e-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="f092e-124">Stilltu valkostinn **Taka gang með** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f092e-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="f092e-125">Stilltu valkostinn **Taka rekka með** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f092e-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="f092e-126">Í reitinn **Snið** ritarðu gildi fyrir rekkann.</span><span class="sxs-lookup"><span data-stu-id="f092e-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="f092e-127">Stilltu valkostinn **Taka hillu með** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f092e-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="f092e-128">Í reitinn **Snið** skal færa inn gildi fyrir hilluna.</span><span class="sxs-lookup"><span data-stu-id="f092e-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="f092e-129">Skilgreina Staðsetningar vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="f092e-129">Define warehouse locations</span></span>
1. <span data-ttu-id="f092e-130">Í aðgerðarúðunni velurðu **Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="f092e-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="f092e-131">Veldu **Leiðsagnarforrit staðsetninga**.</span><span class="sxs-lookup"><span data-stu-id="f092e-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="f092e-132">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="f092e-132">Select **Next**.</span></span>
4. <span data-ttu-id="f092e-133">Afveljið valkostinn **Úthlið**</span><span class="sxs-lookup"><span data-stu-id="f092e-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="f092e-134">Afveljið valkostinn **Fjöldastaðsetningar**</span><span class="sxs-lookup"><span data-stu-id="f092e-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="f092e-135">Veldu **Næst** þangað til þú kemur að möguleikanum á að velja **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="f092e-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="f092e-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f092e-136">Close the page.</span></span>
8. <span data-ttu-id="f092e-137">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="f092e-137">Refresh the page.</span></span>


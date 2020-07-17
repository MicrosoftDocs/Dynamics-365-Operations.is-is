---
title: Viðbótargögn um staðsetningu
description: Í þessu efnisatriði er að finna yfirlit yfir nýjar staðsetningar sem bætt hefur verið við Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9727187ad555f9e3d09beed3f3447a22c29ed22a
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530168"
---
# <a name="additional-location-zones"></a><span data-ttu-id="58c1d-103">Viðbótargögn um staðsetningu</span><span class="sxs-lookup"><span data-stu-id="58c1d-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58c1d-104">Þrír nýir svæðareitir eru í boði í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="58c1d-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="58c1d-105">Vöruhúsastjórnendur geta notað þá til að skilgreina fleiri fyrirtæki eða útlit vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="58c1d-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="58c1d-106">Nýju svæðareitina er hægt að stilla annaðhvort handvirkt eða með því að nota leiðsögnina **Uppsetning staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="58c1d-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="58c1d-107">Hægt er að nota þá fyrir allar fyrirspurnir eða síur sem nota staðsetningartöfluna.</span><span class="sxs-lookup"><span data-stu-id="58c1d-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="58c1d-108">Ekki er krafist frekari uppsetningar til að nota svæðareitina.</span><span class="sxs-lookup"><span data-stu-id="58c1d-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="58c1d-109">Kveiktu á eiginleikanum „Viðbótargögn um staðsetningu“</span><span class="sxs-lookup"><span data-stu-id="58c1d-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="58c1d-110">Áður en þú getur notað eiginleikann *Aukaleg staðsetning*, verður að vera kveikt á honum í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="58c1d-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="58c1d-111">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="58c1d-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="58c1d-112">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="58c1d-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="58c1d-113">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="58c1d-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="58c1d-114">**Heiti eiginleika:** *Aukaleg staðsetning*</span><span class="sxs-lookup"><span data-stu-id="58c1d-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="58c1d-115">Nota staðsetningar</span><span class="sxs-lookup"><span data-stu-id="58c1d-115">Use location zones</span></span>

1. <span data-ttu-id="58c1d-116">Farið í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Uppsetningarforrit staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="58c1d-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="58c1d-117">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="58c1d-117">Set the following values:</span></span>

    - <span data-ttu-id="58c1d-118">Í reitnum **Vöruhús** skal velja _62_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="58c1d-119">Í reitnum **Svæðiskenni** skal velja _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="58c1d-120">Í reitnum **Viðbótarsvæði 1** skal velja _PICKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="58c1d-121">Í reitnum **Viðbótarsvæði 2** skal velja _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="58c1d-122">Í reitnum **Forstillingarkenni staðsetningar** skal velja _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="58c1d-123">Veljið línuna **Gólf**.</span><span class="sxs-lookup"><span data-stu-id="58c1d-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="58c1d-124">Í reitinn **Númer frá** skal slá inn _1_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="58c1d-125">Í reitinn **Númer til** skal slá inn _3_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="58c1d-126">Veljið línuna **Gangur**.</span><span class="sxs-lookup"><span data-stu-id="58c1d-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="58c1d-127">Í reitinn **Númer frá** skal slá inn _1_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="58c1d-128">Í reitinn **Númer til** skal slá inn _5_.</span><span class="sxs-lookup"><span data-stu-id="58c1d-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="58c1d-129">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="58c1d-129">Select **Create**.</span></span>
8. <span data-ttu-id="58c1d-130">Skilaboð birtast sem segja að búið sé að bæta við nýju staðsetningunum.</span><span class="sxs-lookup"><span data-stu-id="58c1d-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="58c1d-131">Veljið hnappinn **Sýna skilaboð** til að skoða skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="58c1d-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="58c1d-132">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="58c1d-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="58c1d-133">Nýju staðsetningarnar birtast í listanum og allir svæðareitir eru tiltækir (þ.e. núverandi svæðareitur og nýju svæðareitirnir).</span><span class="sxs-lookup"><span data-stu-id="58c1d-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>

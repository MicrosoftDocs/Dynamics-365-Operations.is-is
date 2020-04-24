---
title: Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er ekki skyldug.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df79b8ea9ab6e37960cfbf0ca0edcbbc21484db
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213631"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="d1918-104">Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="d1918-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1918-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð.</span><span class="sxs-lookup"><span data-stu-id="d1918-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="d1918-106">Vöruhúsavíddin er ekki skyldug.</span><span class="sxs-lookup"><span data-stu-id="d1918-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="d1918-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="d1918-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="d1918-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="d1918-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="d1918-109">Ekki er hægt að breyta þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="d1918-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="d1918-110">Vöruhúsavíddin er ekki stillt sem skyldug.</span><span class="sxs-lookup"><span data-stu-id="d1918-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="d1918-111">Vöruhúsið gæti verið þekkt en er ekki notað í útreikningi aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="d1918-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="d1918-112">Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="d1918-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="d1918-113">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="d1918-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="d1918-114">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="d1918-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="d1918-115">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="d1918-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="d1918-116">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="d1918-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="d1918-117">Vöruhúsið er stillt á Handvirkt.</span><span class="sxs-lookup"><span data-stu-id="d1918-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="d1918-118">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="d1918-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d1918-119">Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.</span><span class="sxs-lookup"><span data-stu-id="d1918-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="d1918-120">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="d1918-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="d1918-121">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="d1918-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d1918-122">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="d1918-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="d1918-123">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="d1918-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="d1918-124">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="d1918-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d1918-125">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="d1918-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="d1918-126">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="d1918-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="d1918-127">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="d1918-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d1918-128">Veljið vöruna og svo á Aðgerðarrúða á flipa **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar**</span><span class="sxs-lookup"><span data-stu-id="d1918-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="d1918-129">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="d1918-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús ekki skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="d1918-131">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d1918-131">Additional resources</span></span>
--------

[<span data-ttu-id="d1918-132">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="d1918-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="d1918-133">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="d1918-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d1918-134">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="d1918-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d1918-135">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="d1918-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d1918-136">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="d1918-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)




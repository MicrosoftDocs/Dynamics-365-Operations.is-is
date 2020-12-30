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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e47531c75e54b23054464a5e1b1841eb2d82e093
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430073"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="6ed0d-104">Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="6ed0d-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ed0d-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="6ed0d-106">Vöruhúsavíddin er ekki skyldug.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="6ed0d-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="6ed0d-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="6ed0d-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="6ed0d-109">Ekki er hægt að breyta þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="6ed0d-110">Vöruhúsavíddin er ekki stillt sem skyldug.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="6ed0d-111">Vöruhúsið gæti verið þekkt en er ekki notað í útreikningi aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="6ed0d-112">Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="6ed0d-113">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="6ed0d-114">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="6ed0d-115">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="6ed0d-116">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="6ed0d-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="6ed0d-117">Vöruhúsið er stillt á Handvirkt.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="6ed0d-118">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="6ed0d-119">Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="6ed0d-120">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="6ed0d-121">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="6ed0d-122">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="6ed0d-123">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="6ed0d-124">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="6ed0d-125">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="6ed0d-126">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="6ed0d-127">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="6ed0d-128">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="6ed0d-129">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="6ed0d-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús ekki skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="6ed0d-131">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6ed0d-131">Additional resources</span></span>
--------

[<span data-ttu-id="6ed0d-132">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="6ed0d-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="6ed0d-133">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="6ed0d-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="6ed0d-134">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="6ed0d-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="6ed0d-135">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="6ed0d-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="6ed0d-136">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="6ed0d-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)




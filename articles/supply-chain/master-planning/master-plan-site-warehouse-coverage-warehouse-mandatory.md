---
title: Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús lögbundið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er skyldug.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11720b70697112085ac612fc9eded8292a68ab2d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815089"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="9b9fa-104">Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="9b9fa-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b9fa-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="9b9fa-106">Vöruhúsavíddin er skyldug.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="9b9fa-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="9b9fa-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="9b9fa-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="9b9fa-109">Vöruhúsavíddin er skyldug og hana þarf að færa inn í færslu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="9b9fa-110">Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="9b9fa-111">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="9b9fa-112">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="9b9fa-113">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="9b9fa-114">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="9b9fa-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="9b9fa-115">Vöruhúsið er stillt á **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="9b9fa-116">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="9b9fa-117">Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="9b9fa-118">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="9b9fa-119">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="9b9fa-120">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="9b9fa-121">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="9b9fa-122">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="9b9fa-123">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="9b9fa-124">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="9b9fa-125">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="9b9fa-126">Veljið vöruna og svo á Aðgerðarrúða á flipa **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar**</span><span class="sxs-lookup"><span data-stu-id="9b9fa-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="9b9fa-127">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="9b9fa-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="9b9fa-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9b9fa-129">Additional resources</span></span>
--------

[<span data-ttu-id="9b9fa-130">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="9b9fa-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="9b9fa-131">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="9b9fa-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="9b9fa-132">Aðaláætlanagerð fyrir þekju svæðis, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="9b9fa-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="9b9fa-133">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="9b9fa-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="9b9fa-134">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="9b9fa-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)




---
title: Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús lögbundið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er skyldug.
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a07a4588d042af53d6281afc174ff58ecf24ca06
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383344"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="3f94c-104">Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="3f94c-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f94c-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð.</span><span class="sxs-lookup"><span data-stu-id="3f94c-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="3f94c-106">Vöruhúsavíddin er skyldug.</span><span class="sxs-lookup"><span data-stu-id="3f94c-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="3f94c-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="3f94c-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="3f94c-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="3f94c-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="3f94c-109">Vöruhúsavíddin er skyldug og hana þarf að færa inn í færslu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="3f94c-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="3f94c-110">Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="3f94c-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="3f94c-111">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="3f94c-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="3f94c-112">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="3f94c-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="3f94c-113">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="3f94c-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="3f94c-114">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="3f94c-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="3f94c-115">Vöruhúsið er stillt á **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="3f94c-116">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="3f94c-117">Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.</span><span class="sxs-lookup"><span data-stu-id="3f94c-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="3f94c-118">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="3f94c-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="3f94c-119">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="3f94c-120">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="3f94c-121">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="3f94c-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="3f94c-122">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="3f94c-123">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="3f94c-124">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="3f94c-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="3f94c-125">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="3f94c-126">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="3f94c-127">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="3f94c-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="3f94c-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3f94c-129">Additional resources</span></span>
--------

[<span data-ttu-id="3f94c-130">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="3f94c-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="3f94c-131">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="3f94c-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3f94c-132">Aðaláætlanagerð fyrir þekju svæðis, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="3f94c-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3f94c-133">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="3f94c-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3f94c-134">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="3f94c-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)




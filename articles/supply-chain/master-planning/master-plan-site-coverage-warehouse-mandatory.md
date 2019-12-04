---
title: Aðaláætlanagerð fyrir svæðistryggingu, vöruhús áskilið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð. Vöruhúsavíddin er skyldug.
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 132817fefb9592764d1adaf9f714c27108ce88ae
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815112"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="0c97c-104">Aðaláætlanagerð fyrir svæðistryggingu, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="0c97c-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c97c-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð.</span><span class="sxs-lookup"><span data-stu-id="0c97c-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="0c97c-106">Vöruhúsavíddin er skyldug.</span><span class="sxs-lookup"><span data-stu-id="0c97c-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="0c97c-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="0c97c-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="0c97c-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="0c97c-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="0c97c-109">Ekki er hægt að breyta þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="0c97c-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="0c97c-110">Vöruhúsavíddin er skyldug og hana þarf að færa inn í færslu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="0c97c-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="0c97c-111">Svæðisvíddin er stillt á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="0c97c-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="0c97c-112">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="0c97c-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="0c97c-113">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="0c97c-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="0c97c-114">Vöruhúsavíddin er ekki stillt á þekjuáætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="0c97c-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="0c97c-115">Þessvegna, framboð og eftirspurn safnast upp á staðsetningu, og hugsanlega, á öðrum víddum sem eru með tryggingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="0c97c-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="0c97c-116">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="0c97c-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="0c97c-117">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="0c97c-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="0c97c-118">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="0c97c-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="0c97c-119">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="0c97c-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="0c97c-120">Veljið vöruna og smellið síðan á **Áætla &gt; Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="0c97c-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="0c97c-121">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="0c97c-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="0c97c-122">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="0c97c-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="0c97c-123">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitinn **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="0c97c-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="0c97c-124">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="0c97c-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="0c97c-125">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="0c97c-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="0c97c-126">Veldu vöruna og smelltu síðan á **Áætla &gt; Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="0c97c-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="0c97c-127">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="0c97c-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis, vöruhús skyldugt](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="0c97c-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0c97c-129">Additional resources</span></span>
--------

[<span data-ttu-id="0c97c-130">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="0c97c-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="0c97c-131">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="0c97c-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="0c97c-132">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="0c97c-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="0c97c-133">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="0c97c-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="0c97c-134">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="0c97c-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)




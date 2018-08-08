---
title: "Aðaláætlanagerð fyrir svæðistryggingu, vöruhús áskilið"
description: "Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð. Vöruhúsavíddin er skyldug."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 1f61c142fff73fdeeca573cca3f54e654511af1e
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="9f1f7-104">Aðaláætlanagerð fyrir svæðistryggingu, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="9f1f7-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f1f7-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="9f1f7-106">Vöruhúsavíddin er skyldug.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="9f1f7-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="9f1f7-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="9f1f7-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="9f1f7-109">Ekki er hægt að breyta þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="9f1f7-110">Vöruhúsavíddin er skyldug og hana þarf að færa inn í færslu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="9f1f7-111">Svæðisvíddin er stillt á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="9f1f7-112">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="9f1f7-113">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="9f1f7-114">Vöruhúsavíddin er ekki stillt á þekjuáætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="9f1f7-115">Þessvegna, framboð og eftirspurn safnast upp á staðsetningu, og hugsanlega, á öðrum víddum sem eru með tryggingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="9f1f7-116">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="9f1f7-117">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="9f1f7-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="9f1f7-118">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="9f1f7-119">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="9f1f7-120">Veljið vöruna og smellið síðan á **Áætla &gt; Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="9f1f7-121">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="9f1f7-122">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="9f1f7-123">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitinn **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="9f1f7-124">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="9f1f7-125">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="9f1f7-126">Veldu vöruna og smelltu síðan á **Áætla &gt; Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="9f1f7-127">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="9f1f7-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis, vöruhús skyldugt](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="9f1f7-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9f1f7-129">Additional resources</span></span>
--------

[<span data-ttu-id="9f1f7-130">Áætlanagerð og fjölsvæðiseiginleikinn</span><span class="sxs-lookup"><span data-stu-id="9f1f7-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="9f1f7-131">Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="9f1f7-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="9f1f7-132">Aðaláætlanagerð - trygging svæðis, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="9f1f7-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="9f1f7-133">Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús ekki lögbundið</span><span class="sxs-lookup"><span data-stu-id="9f1f7-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="9f1f7-134">Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="9f1f7-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)





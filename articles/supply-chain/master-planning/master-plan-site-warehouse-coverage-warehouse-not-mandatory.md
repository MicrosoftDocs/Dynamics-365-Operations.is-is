---
title: "Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið"
description: "Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er ekki skyldug."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9214a8f2b62aa261b05f0b360fd03faa63ce1ea
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="5b2af-104">Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="5b2af-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5b2af-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð.</span><span class="sxs-lookup"><span data-stu-id="5b2af-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="5b2af-106">Vöruhúsavíddin er ekki skyldug.</span><span class="sxs-lookup"><span data-stu-id="5b2af-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="5b2af-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="5b2af-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="5b2af-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="5b2af-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="5b2af-109">Ekki er hægt að breyta þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="5b2af-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="5b2af-110">Vöruhúsavíddin er ekki stillt sem skyldug.</span><span class="sxs-lookup"><span data-stu-id="5b2af-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="5b2af-111">Vöruhúsið gæti verið þekkt en er ekki notað í útreikningi aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="5b2af-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="5b2af-112">Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="5b2af-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="5b2af-113">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="5b2af-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="5b2af-114">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="5b2af-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="5b2af-115">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="5b2af-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="5b2af-116">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="5b2af-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="5b2af-117">Vöruhúsið er stillt á Handvirkt.</span><span class="sxs-lookup"><span data-stu-id="5b2af-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="5b2af-118">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="5b2af-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5b2af-119">Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.</span><span class="sxs-lookup"><span data-stu-id="5b2af-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="5b2af-120">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="5b2af-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="5b2af-121">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="5b2af-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5b2af-122">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="5b2af-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="5b2af-123">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="5b2af-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="5b2af-124">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="5b2af-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5b2af-125">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="5b2af-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="5b2af-126">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="5b2af-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="5b2af-127">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="5b2af-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5b2af-128">Veljið vöruna og svo á Aðgerðarrúða á flipa **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar**</span><span class="sxs-lookup"><span data-stu-id="5b2af-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="5b2af-129">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="5b2af-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús ekki skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a><span data-ttu-id="5b2af-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5b2af-131">See also</span></span>
--------

[<span data-ttu-id="5b2af-132">Áætlanagerð og fjölsvæðiseiginleikinn</span><span class="sxs-lookup"><span data-stu-id="5b2af-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="5b2af-133">Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="5b2af-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5b2af-134">Aðaláætlanagerð - trygging svæðis, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="5b2af-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5b2af-135">Aðaláætlanagerð- trygging svæðis,  vöruhús ekki lögbundið</span><span class="sxs-lookup"><span data-stu-id="5b2af-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5b2af-136">Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="5b2af-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)





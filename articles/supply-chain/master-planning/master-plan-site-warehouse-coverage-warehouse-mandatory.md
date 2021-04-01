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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ffc550ff719950a603811c65cb9b790ded5c2c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236052"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="36806-104">Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="36806-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36806-105">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð.</span><span class="sxs-lookup"><span data-stu-id="36806-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="36806-106">Vöruhúsavíddin er skyldug.</span><span class="sxs-lookup"><span data-stu-id="36806-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="36806-107">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="36806-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="36806-108">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="36806-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="36806-109">Vöruhúsavíddin er skyldug og hana þarf að færa inn í færslu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="36806-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="36806-110">Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="36806-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="36806-111">Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir.</span><span class="sxs-lookup"><span data-stu-id="36806-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="36806-112">Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.</span><span class="sxs-lookup"><span data-stu-id="36806-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="36806-113">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="36806-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="36806-114">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="36806-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="36806-115">Vöruhúsið er stillt á **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="36806-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="36806-116">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="36806-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="36806-117">Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.</span><span class="sxs-lookup"><span data-stu-id="36806-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="36806-118">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="36806-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="36806-119">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="36806-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="36806-120">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="36806-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="36806-121">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="36806-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="36806-122">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="36806-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="36806-123">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="36806-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="36806-124">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="36806-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="36806-125">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="36806-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="36806-126">Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="36806-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="36806-127">Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="36806-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="36806-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="36806-129">Additional resources</span></span>
--------

[<span data-ttu-id="36806-130">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="36806-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="36806-131">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="36806-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="36806-132">Aðaláætlanagerð fyrir þekju svæðis, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="36806-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="36806-133">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="36806-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="36806-134">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="36806-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
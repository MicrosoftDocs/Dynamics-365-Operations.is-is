---
title: Aðaláætlanagerð fyrir svæðistryggingu, vöruhús ekki áskilið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð.
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe5cb5f9d21afcd12f3041bb9acc89fff360c95e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970457"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="ed639-103">Aðaláætlanagerð fyrir svæðistryggingu, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="ed639-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed639-104">Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð.</span><span class="sxs-lookup"><span data-stu-id="ed639-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="ed639-105">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="ed639-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="ed639-106">Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="ed639-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="ed639-107">Vöruhúsavíddin er ekki stillt sem skyldug.</span><span class="sxs-lookup"><span data-stu-id="ed639-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="ed639-108">Vöruhúsið gæti verið þekkt en er ekki notað í útreikningi aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="ed639-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="ed639-109">Svæðisvíddin er stillt á þekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="ed639-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="ed639-110">Vöruhúsavíddin er ekki stillt á þekjuáætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="ed639-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="ed639-111">Þessvegna, framboð og eftirspurn safnast upp á staðsetningu, og hugsanlega, á öðrum víddum sem eru með tryggingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="ed639-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="ed639-112">Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram.</span><span class="sxs-lookup"><span data-stu-id="ed639-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="ed639-113">Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="ed639-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="ed639-114">Vöruþekja er skilgreind fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="ed639-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="ed639-115">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ed639-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ed639-116">Veljið vöruna og smellið síðan á **Áætla &gt; Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="ed639-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="ed639-117">Áfyllingarvensl eru skilgreind fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="ed639-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="ed639-118">Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="ed639-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="ed639-119">Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitinn **Aðalvöruhús**.</span><span class="sxs-lookup"><span data-stu-id="ed639-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="ed639-120">Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban.</span><span class="sxs-lookup"><span data-stu-id="ed639-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="ed639-121">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ed639-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ed639-122">Veldu vöruna og smelltu síðan á **Áætla &gt; Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="ed639-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="ed639-123">Í skjámyndinni **Sjálfgefnar pöntunarstillingar** er að finna reitinn **Sjálfgefin pöntunargerð**.</span><span class="sxs-lookup"><span data-stu-id="ed639-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Eftirspurn fyrir þekju svæðis, vöruhús ekki skyldugt](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="ed639-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ed639-125">Additional resources</span></span>
--------

[<span data-ttu-id="ed639-126">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="ed639-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="ed639-127">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="ed639-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ed639-128">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="ed639-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ed639-129">Aðaláætlanagerð fyrir þekju svæðis, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="ed639-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ed639-130">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="ed639-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)




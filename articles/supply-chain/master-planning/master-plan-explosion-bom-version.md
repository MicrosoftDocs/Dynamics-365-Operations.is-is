---
title: Niðurbrot uppskriftarútgáfu
description: Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f3c800d96805df38a2e31018f2d6c305e3ed7da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "353909"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="de9ec-103">Niðurbrot uppskriftarútgáfu</span><span class="sxs-lookup"><span data-stu-id="de9ec-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de9ec-104">Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="de9ec-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="de9ec-105">Niðurbrot eftirspurnar í uppskriftarútgáfunni býr til eftirspurn fyrir hverja uppskriftarlínuvöru við tiltekið svæði og mögulega við tiltekið vöruhús.</span><span class="sxs-lookup"><span data-stu-id="de9ec-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="de9ec-106">Uppskrift sem á við um°tiltekið setur gæti haft tiltekið vöruhús skilgreint fyrir hverja uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="de9ec-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="de9ec-107">Einnig ákvarða víddarstillingar vörunnar hvort vöruhúsið sé nauðsynlegt fyrir hverja uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="de9ec-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="de9ec-108">Þessi eftirspurn sem eftir er fyrir hverja uppskriftarlínuvöru verður svo°að upphafspunkti fyrir aukaniðurbrot eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="de9ec-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="de9ec-109">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="de9ec-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="de9ec-110">Svæðisvíddin er skylda og hana þarf að færa inn í færslu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="de9ec-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="de9ec-111">Svæðisvíddin er samræmd.</span><span class="sxs-lookup"><span data-stu-id="de9ec-111">The site dimension is consistent.</span></span> <span data-ttu-id="de9ec-112">Þess vegna er svæðið fyrir neðra-stigs eftirspurn hið sama og svæðið í upprunalegu eftirspurnarfærslunni.</span><span class="sxs-lookup"><span data-stu-id="de9ec-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="de9ec-113">Eftirfarandi mynd sýnir framvindu niðurbrots eftirspurnar í aðaláætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="de9ec-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Niðurbrot eftirspurnar með útgáfu uppskriftar](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="de9ec-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="de9ec-115">Additional resources</span></span>
--------

[<span data-ttu-id="de9ec-116">Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="de9ec-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="de9ec-117">Áætlanagerð og fjölsvæðiseiginleikinn</span><span class="sxs-lookup"><span data-stu-id="de9ec-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




---
title: Niðurbrot uppskriftarútgáfu
description: Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f50d9f2f7249ecb4090983e245d4700020e0886
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005178"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="dc090-103">Niðurbrot uppskriftarútgáfu</span><span class="sxs-lookup"><span data-stu-id="dc090-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc090-104">Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="dc090-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="dc090-105">Niðurbrot eftirspurnar í uppskriftarútgáfunni býr til eftirspurn fyrir hverja uppskriftarlínuvöru við tiltekið svæði og mögulega við tiltekið vöruhús.</span><span class="sxs-lookup"><span data-stu-id="dc090-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="dc090-106">Uppskrift sem á við um°tiltekið setur gæti haft tiltekið vöruhús skilgreint fyrir hverja uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="dc090-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="dc090-107">Einnig ákvarða víddarstillingar vörunnar hvort vöruhúsið sé nauðsynlegt fyrir hverja uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="dc090-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="dc090-108">Þessi eftirspurn sem eftir er fyrir hverja uppskriftarlínuvöru verður svo°að upphafspunkti fyrir aukaniðurbrot eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="dc090-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="dc090-109">Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:</span><span class="sxs-lookup"><span data-stu-id="dc090-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="dc090-110">Svæðisvíddin er skylda og hana þarf að færa inn í færslu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="dc090-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="dc090-111">Svæðisvíddin er samræmd.</span><span class="sxs-lookup"><span data-stu-id="dc090-111">The site dimension is consistent.</span></span> <span data-ttu-id="dc090-112">Þess vegna er svæðið fyrir neðra-stigs eftirspurn hið sama og svæðið í upprunalegu eftirspurnarfærslunni.</span><span class="sxs-lookup"><span data-stu-id="dc090-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="dc090-113">Eftirfarandi mynd sýnir framvindu niðurbrots eftirspurnar í aðaláætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="dc090-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Niðurbrot eftirspurnar með útgáfu uppskriftar](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="dc090-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dc090-115">Additional resources</span></span>
--------

[<span data-ttu-id="dc090-116">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="dc090-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="dc090-117">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="dc090-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)




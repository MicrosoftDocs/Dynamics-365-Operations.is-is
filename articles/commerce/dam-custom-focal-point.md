---
title: Sérsníða þungamiðju myndar
description: Þetta efni lýsir því hvernig á að sérsníða þungamiðju myndar í vefsvæðishönnuði í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b20fbc20f18243c712595795a0b16ae417e755e6
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594333"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="9f91e-103">Sérsníða þungamiðju myndar</span><span class="sxs-lookup"><span data-stu-id="9f91e-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f91e-104">Þetta efni lýsir því hvernig á að sérsníða þungamiðju myndar í vefsvæðishönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9f91e-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="9f91e-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="9f91e-105">Overview</span></span>

<span data-ttu-id="9f91e-106">Þegar mynd er hlaðið upp í margmiðlunarsafn í vefsíðuhönnuði Commerce reynir kerfið að ákvarða þungamiðju myndarinnar.</span><span class="sxs-lookup"><span data-stu-id="9f91e-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="9f91e-107">Til dæmis, ef myndin er af manneskju mun kerfið sjálfkrafa setja miðpunktinn á andlit viðkomandi.</span><span class="sxs-lookup"><span data-stu-id="9f91e-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="9f91e-108">Í flestum tilvikum virkar sjálfvirkur miðpunkturinn vel fyrir allar skoðunargáttir, en stundum gætirðu viljað stilla þungamiðjuna til að tryggja að ákveðinn hluti myndarinnar sé alltaf sýnilegur.</span><span class="sxs-lookup"><span data-stu-id="9f91e-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="9f91e-109">Skilgreindu sérsniðna þungamiðju fyrir mynd</span><span class="sxs-lookup"><span data-stu-id="9f91e-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="9f91e-110">Fylgdu þessum skrefum til að skilgreina sérsniðna þungamiðju fyrir mynd.</span><span class="sxs-lookup"><span data-stu-id="9f91e-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="9f91e-111">Í vinstri flettiglugganum á vefsvæðishönnuði Commerce velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="9f91e-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="9f91e-112">Í aðalglugganum velurðu myndina sem þú vilt breyta.</span><span class="sxs-lookup"><span data-stu-id="9f91e-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="9f91e-113">Á skipanastikunni velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="9f91e-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="9f91e-114">Veldu myndina sem á að fara inn í **Breyta stillingu**.</span><span class="sxs-lookup"><span data-stu-id="9f91e-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="9f91e-115">Undir **Breyta stillingu** velurðu **Breyta þungamiðju**.</span><span class="sxs-lookup"><span data-stu-id="9f91e-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="9f91e-116">Hringlaga miðpunktur birtist yfir myndinni.</span><span class="sxs-lookup"><span data-stu-id="9f91e-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="9f91e-117">Veldu miðpunktsstýringu til að færa hana yfir viðkomandi þungamiðju.</span><span class="sxs-lookup"><span data-stu-id="9f91e-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="9f91e-118">Þegar það er búið skaltu á skipanastikunni velja **Vista** og veldu síðan **Ljúka breytingu**.</span><span class="sxs-lookup"><span data-stu-id="9f91e-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f91e-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9f91e-119">Additional resources</span></span>

[<span data-ttu-id="9f91e-120">Yfirlit stjórnunar stafrænna eigna</span><span class="sxs-lookup"><span data-stu-id="9f91e-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="9f91e-121">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="9f91e-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="9f91e-122">Hlaða upp myndbandi</span><span class="sxs-lookup"><span data-stu-id="9f91e-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="9f91e-123">Hlaða upp skrám</span><span class="sxs-lookup"><span data-stu-id="9f91e-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="9f91e-124">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="9f91e-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="9f91e-125">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="9f91e-125">Upload and serve static files</span></span>](upload-serve-static-files.md)

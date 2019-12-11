---
title: Leiðir til að bæta við efni
description: Þetta efni veitir upplýsingar um hvernig á að bæta við og stjórna efni á Microsoft Dynamics 365 Commerce síðunni þinni.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3d91235837aee9ad06466ffe47727b435e39094f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770529"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="c8cbd-103">Leiðir til að bæta við efni</span><span class="sxs-lookup"><span data-stu-id="c8cbd-103">Ways to add content</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c8cbd-104">Þetta efni veitir upplýsingar um hvernig á að bæta við og stjórna efni á Microsoft Dynamics 365 Commerce síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="c8cbd-104">This topic provides information about how to add and manage content on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="c8cbd-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c8cbd-105">Overview</span></span>

<span data-ttu-id="c8cbd-106">Það eru margar leiðir til að breyta útliti og innihaldi vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="c8cbd-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="c8cbd-107">Það fer eftir áskildu stigi sérstillinga, en margar af þessum breytingum er hægt að innleiða af þeim sem eru ekki forritarar.</span><span class="sxs-lookup"><span data-stu-id="c8cbd-107">Depending on the required level of customization, many of these changes can be implemented by non-developers.</span></span> <span data-ttu-id="c8cbd-108">Til dæmis þarf ekki að skrifa neinn kóða til að smíða sniðmát, velja þemu og velja og stilla einingar.</span><span class="sxs-lookup"><span data-stu-id="c8cbd-108">For example, no code has to be written to build templates, select themes, and select and configure modules.</span></span> <span data-ttu-id="c8cbd-109">Aftur á móti þarf forritunarhæfileika til að búa til nýtt þema eða einingu, vegna þess að nota verður hugbúnaðarþróunarbúnað rafrænna viðskipta (SDK) og Microsoft Dynamics virkjunarverkflæði fyrir Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c8cbd-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="c8cbd-110">Eftirfarandi efnisatriði veita upplýsingar um hvernig á að bæta við og stjórna efni á vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="c8cbd-110">The following topics provide detailed information about how to add and manage site content.</span></span> <span data-ttu-id="c8cbd-111">Þau leggja áherslu á svæði á vefsvæðinu sem þarfnast ekki forritara.</span><span class="sxs-lookup"><span data-stu-id="c8cbd-111">They focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="c8cbd-112">Eftir því sem þarf, benda þeir á verkefni sem krefjast SDK-vinnu.</span><span class="sxs-lookup"><span data-stu-id="c8cbd-112">As required, they point out tasks that require SDK work.</span></span>

- <span data-ttu-id="c8cbd-113">Til að breyta texta, myndum eða myndskeiði á núverandi síðu skal sjá [Vinna með einingar](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="c8cbd-113">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="c8cbd-114">Til að hjálpa þér að tryggja höfundarétt reynslu af höfundarétti á vörumerkjum skal sjá [Vinna með sniðmát](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c8cbd-114">To help guarantee a foolproof, on-brand authoring experience for web content authors, see [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="c8cbd-115">Til að endurraða hlutum á vefsíðunni skal sjá [Vinna með skipulag](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="c8cbd-115">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="c8cbd-116">Til að breyta letri, litum og almennu útliti vefsíðna skal sjá [Veldu þema síðunnar](select-site-theme.md).</span><span class="sxs-lookup"><span data-stu-id="c8cbd-116">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8cbd-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c8cbd-117">Additional resources</span></span>

[<span data-ttu-id="c8cbd-118">Orðalisti blaðsíðna</span><span class="sxs-lookup"><span data-stu-id="c8cbd-118">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="c8cbd-119">Staða skjala og líftíma</span><span class="sxs-lookup"><span data-stu-id="c8cbd-119">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="c8cbd-120">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="c8cbd-120">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="c8cbd-121">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="c8cbd-121">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="c8cbd-122">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="c8cbd-122">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c8cbd-123">Sérstilla yfirlit svæðis</span><span class="sxs-lookup"><span data-stu-id="c8cbd-123">Customize site navigation</span></span>](customize-site-navigation.md)

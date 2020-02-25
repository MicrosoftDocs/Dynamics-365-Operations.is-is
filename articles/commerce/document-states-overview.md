---
title: Staða skjala og líftíma
description: Þetta efni fjallar um hinar ýmsu skjalastöður blaðsíðuþátta í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002982"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="ecb3d-103">Staða skjala og líftíma</span><span class="sxs-lookup"><span data-stu-id="ecb3d-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ecb3d-104">Þetta efni fjallar um hinar ýmsu skjalastöður blaðsíðuþátta í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="ecb3d-105">Lýsing skjalastöðu</span><span class="sxs-lookup"><span data-stu-id="ecb3d-105">Document state descriptions</span></span>

<span data-ttu-id="ecb3d-106">Efnið [Síðueiningar](page-elements-overview.md) er með lista yfir ýmsar gerðir skjala í efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="ecb3d-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="ecb3d-107">Þessar skjalategundir geta haft nokkrar stöður í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="ecb3d-108">Skjalastöðurnar hjálpa til við að koma í veg fyrir árekstur gagna og framfylgja útgáfustjórnun.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="ecb3d-109">Þær ákvarða hverjir geta breytt skjölunum, hvenær hægt er að breyta skjölunum og hvenær aðrir geta skoðað breytingar.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="ecb3d-110">Eftirfarandi tafla sýnir mögulegar skjalastöður síðueininga í Commerce.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="ecb3d-111">Staða skjals</span><span class="sxs-lookup"><span data-stu-id="ecb3d-111">Document state</span></span> | <span data-ttu-id="ecb3d-112">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ecb3d-112">Description</span></span> |
|---|---|
| <span data-ttu-id="ecb3d-113">Skráði sig út</span><span class="sxs-lookup"><span data-stu-id="ecb3d-113">Checked out</span></span> | <span data-ttu-id="ecb3d-114">Þegar CMS hlutur er skráður út til þín geta aðrir staðfestir kerfisnotendur ekki breytt honum.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="ecb3d-115">Allar breytingar sem þú gerir á hlutnum eru aðeins sýnilegar þér.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="ecb3d-116">Skráð inn</span><span class="sxs-lookup"><span data-stu-id="ecb3d-116">Checked in</span></span> | <span data-ttu-id="ecb3d-117">Þegar CMS hlutur er innritaður eru allar breytingar sýnilegar öðrum staðfestum kerfisnotendum og þessir notendur geta síðan skoðað hlutinn og breytt honum.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="ecb3d-118">Hver innskráning býr til útgáfu skjals í sögu hlutarins.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="ecb3d-119">Útgefið</span><span class="sxs-lookup"><span data-stu-id="ecb3d-119">Published</span></span> | <span data-ttu-id="ecb3d-120">Þegar CMS hlutur er gefinn út er honum ýtt á heimasíðuna þína og hægt verður að uppgötva hann á internetinu af utanaðkomandi notendum.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="ecb3d-121">Aðeins er hægt að birta hluti ef þeir hafa verið skráðir inn.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="ecb3d-122">Vistuð</span><span class="sxs-lookup"><span data-stu-id="ecb3d-122">Saved</span></span> | <span data-ttu-id="ecb3d-123">Hægt er að vista breytingar sem gerðar hafa verið á afrituðum CMS hlut á CMS áður en hluturinn er skráður inn eða birtur.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="ecb3d-124">Þessar vistuðu breytingar eru ekki sýnilegar öðrum staðfestum kerfisnotendum fyrr en hluturinn er skráður inn.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="ecb3d-125">Þær eru ekki sýnilegir fyrir utanaðkomandi notendur fyrr en hluturinn er birtur.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="ecb3d-126">Fargað við útskráningu</span><span class="sxs-lookup"><span data-stu-id="ecb3d-126">Discarded check out</span></span> | <span data-ttu-id="ecb3d-127">Þegar útskráðri CMS-vöru er fargað er öllum vistuðum breytingum eytt og varan snýr aftur í þá útgáfu sem síðast var skráð inn.</span><span class="sxs-lookup"><span data-stu-id="ecb3d-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ecb3d-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ecb3d-128">Additional resources</span></span>

[<span data-ttu-id="ecb3d-129">Leiðir til að bæta við efni</span><span class="sxs-lookup"><span data-stu-id="ecb3d-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="ecb3d-130">Orðalisti síðulíkans</span><span class="sxs-lookup"><span data-stu-id="ecb3d-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="ecb3d-131">Unnið með birta hópa</span><span class="sxs-lookup"><span data-stu-id="ecb3d-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="ecb3d-132">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="ecb3d-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="ecb3d-133">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="ecb3d-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="ecb3d-134">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="ecb3d-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="ecb3d-135">Sérstilla yfirlit svæðis</span><span class="sxs-lookup"><span data-stu-id="ecb3d-135">Customize site navigation</span></span>](customize-site-navigation.md)

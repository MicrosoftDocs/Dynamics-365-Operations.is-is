---
title: Staða skjala og líftíma
description: Þetta efni fjallar um hinar ýmsu skjalastöður blaðsíðuþátta í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413164"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="a6990-103">Staða skjala og líftíma</span><span class="sxs-lookup"><span data-stu-id="a6990-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6990-104">Þetta efni fjallar um hinar ýmsu skjalastöður blaðsíðuþátta í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6990-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="a6990-105">Lýsing skjalastöðu</span><span class="sxs-lookup"><span data-stu-id="a6990-105">Document state descriptions</span></span>

<span data-ttu-id="a6990-106">Efnið [Síðueiningar](page-elements-overview.md) er með lista yfir ýmsar gerðir skjala í efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="a6990-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="a6990-107">Þessar skjalategundir geta haft nokkrar stöður í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="a6990-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="a6990-108">Skjalastöðurnar hjálpa til við að koma í veg fyrir árekstur gagna og framfylgja útgáfustjórnun.</span><span class="sxs-lookup"><span data-stu-id="a6990-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="a6990-109">Þær ákvarða hverjir geta breytt skjölunum, hvenær hægt er að breyta skjölunum og hvenær aðrir geta skoðað breytingar.</span><span class="sxs-lookup"><span data-stu-id="a6990-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="a6990-110">Eftirfarandi tafla sýnir mögulegar skjalastöður síðueininga í Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6990-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="a6990-111">Staða skjals</span><span class="sxs-lookup"><span data-stu-id="a6990-111">Document state</span></span>      | <span data-ttu-id="a6990-112">Aðgerð vefsvæðishönnuðar</span><span class="sxs-lookup"><span data-stu-id="a6990-112">Site builder action</span></span>        | <span data-ttu-id="a6990-113">lýsing</span><span class="sxs-lookup"><span data-stu-id="a6990-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="a6990-114">Skráð út</span><span class="sxs-lookup"><span data-stu-id="a6990-114">Checked out</span></span>         | <span data-ttu-id="a6990-115">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a6990-115">Select **Edit**.</span></span>           | <span data-ttu-id="a6990-116">Viðeigandi skjal er skráð út til þín.</span><span class="sxs-lookup"><span data-stu-id="a6990-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="a6990-117">Meðan skjal er í þessari stöðu geta aðrir sannvottaðir kerfisnotendur ekki breytt því og allar breytingar sem þú gerir á skjalinu eru aðeins sýnilegar þér.</span><span class="sxs-lookup"><span data-stu-id="a6990-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="a6990-118">Vistuð</span><span class="sxs-lookup"><span data-stu-id="a6990-118">Saved</span></span>               | <span data-ttu-id="a6990-119">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a6990-119">Select **Save**.</span></span>           | <span data-ttu-id="a6990-120">Breytingar sem gerðar hafa verið á útskráðu skjali eru vistaðar í gagnagrunninn en skjalið hefur ekki enn verið skráð inn eða birt.</span><span class="sxs-lookup"><span data-stu-id="a6990-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="a6990-121">Vistuðu breytingarnar eru ekki sýnilegar öðrum staðfestum kerfisnotendum fyrr en höfundurinn velur **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="a6990-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="a6990-122">Þær eru ekki sýnilegir fyrir utanaðkomandi notendur fyrr en hluturinn er birtur.</span><span class="sxs-lookup"><span data-stu-id="a6990-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="a6990-123">Fargað við útskráningu</span><span class="sxs-lookup"><span data-stu-id="a6990-123">Discarded check out</span></span> | <span data-ttu-id="a6990-124">Veldu **Fleygja breytingum**.</span><span class="sxs-lookup"><span data-stu-id="a6990-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="a6990-125">Öllum breytingum á útskráðu skjali er fargað og varan snýr aftur í síðustu útgáfu sem var innskráð.</span><span class="sxs-lookup"><span data-stu-id="a6990-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="a6990-126">Skráð inn</span><span class="sxs-lookup"><span data-stu-id="a6990-126">Checked in</span></span>          | <span data-ttu-id="a6990-127">Veldu **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="a6990-127">Select **Finish editing**.</span></span> | <span data-ttu-id="a6990-128">Breytta skjalið er skráð inn.</span><span class="sxs-lookup"><span data-stu-id="a6990-128">The edited document is checked in.</span></span> <span data-ttu-id="a6990-129">Allar breytingar eru sýnilegar öðrum staðfestum kerfisnotendum og þeir notendur geta síðan breytt skjalinu.</span><span class="sxs-lookup"><span data-stu-id="a6990-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="a6990-130">Hver innskráning býr til útgáfu skjals í sögu hlutarins.</span><span class="sxs-lookup"><span data-stu-id="a6990-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="a6990-131">Útgefið</span><span class="sxs-lookup"><span data-stu-id="a6990-131">Published</span></span>           | <span data-ttu-id="a6990-132">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="a6990-132">Select **Publish**.</span></span>        | <span data-ttu-id="a6990-133">Skjalið er birt og breytingunum er ýtt á lifandi vefsvæðið og verða uppgötvaðar af utanaðkomandi notendum.</span><span class="sxs-lookup"><span data-stu-id="a6990-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="a6990-134">Aðeins er hægt að birta vörur ef þær hafa fyrst verið innritaðar með því að velja **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="a6990-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a6990-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a6990-135">Additional resources</span></span>

[<span data-ttu-id="a6990-136">Leiðir til að bæta við efni</span><span class="sxs-lookup"><span data-stu-id="a6990-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="a6990-137">Orðalisti síðulíkans</span><span class="sxs-lookup"><span data-stu-id="a6990-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="a6990-138">Vinna með birtingarhópa</span><span class="sxs-lookup"><span data-stu-id="a6990-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="a6990-139">Virkja og nota deilingu milli rása</span><span class="sxs-lookup"><span data-stu-id="a6990-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="a6990-140">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="a6990-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="a6990-141">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="a6990-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="a6990-142">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="a6990-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a6990-143">Sérstilla yfirlit svæðis</span><span class="sxs-lookup"><span data-stu-id="a6990-143">Customize site navigation</span></span>](customize-site-navigation.md)

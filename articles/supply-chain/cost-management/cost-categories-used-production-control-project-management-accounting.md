---
title: Um kostnaðartegundir notaðar í bókhaldi Framleiðslustýringar og Verkefnastjórnunar.
description: Sumar gerðir framleiðslu geta átt við um mat á verktíma og skýrslur. Þessi grein veitir upplýsingar um kostnaðarflokka sem verður að skilgreina fyrir þessar gerðir framleiðsluvinnu fyrir framleiðslu og verk.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cab4629740e92f9075b7afc7a5d228b2e01c4664
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557872"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="0c269-104">Um kostnaðartegundir notaðar í bókhaldi Framleiðslustýringar og Verkefnastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="0c269-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c269-105">Sumar gerðir framleiðslu geta átt við um mat á verktíma og skýrslur.</span><span class="sxs-lookup"><span data-stu-id="0c269-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="0c269-106">Þessi grein veitir upplýsingar um kostnaðarflokka sem verður að skilgreina fyrir þessar gerðir framleiðsluvinnu fyrir framleiðslu og verk.</span><span class="sxs-lookup"><span data-stu-id="0c269-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="0c269-107">Sumar gerðir framleiðslu geta átt við um mat á verktíma og skýrslur.</span><span class="sxs-lookup"><span data-stu-id="0c269-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="0c269-108">Í þessu tilfelli er kostnaðartegundar krafist fyrir framleiðslu og verk.</span><span class="sxs-lookup"><span data-stu-id="0c269-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="0c269-109">Þegar kostnaðartegund er notuð í framleiðslu og verk, verður að skilgreina viðbótarupplýsingar tengdar verki.</span><span class="sxs-lookup"><span data-stu-id="0c269-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="0c269-110">Til dæmis getur tímakostnaðurinn sem er tengdur verkum verið annar en sá sem tengist framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="0c269-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="0c269-111">Hægt er að nota síðuna **Kostnaðartegundir** til að skilgreina kostnaðartegund sem er notuð í bókhaldi Framleiðslustýringar og Verkefnastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="0c269-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="0c269-112">**Athugasemd:** Kostnaðarbókhald hefur síðuna **Verktegundir** en þessi síða tengist á engan hátt þeim aðgerðum sem er lýst í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="0c269-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="0c269-113">Þegar kostnaðartegund er notuð í verk, hefur síðan **Kostnaðartegundir** viðbótarflipa sem birta nánari verktengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="0c269-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="0c269-114">Þessar upplýsingar innihalda tegundaflokkinn, línueiginleika og fjárhagslykla sem eru úthlutaðir á kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="0c269-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="0c269-115">Kostnaðartegund verður að úthluta á tegundarflokk sem styður færslugerðina **Klukkustundir**.</span><span class="sxs-lookup"><span data-stu-id="0c269-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="0c269-116">Línueiginleiki tilgreinir sjálfgefnar upplýsingar um hvernig tilkynntur tími verður reikningshæfur á verk.</span><span class="sxs-lookup"><span data-stu-id="0c269-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="0c269-117">Yfirleitt eru fjárhagslyklarnir sem tengjast kostnaði og sölu skilgreindir fyrir tegundarflokkinn sem er tengdur kostnaðartegundinni.</span><span class="sxs-lookup"><span data-stu-id="0c269-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="0c269-118">Hins vegar er hægt að skilgreina tiltekna lykla fyrir stakar kostnaðartegundir.</span><span class="sxs-lookup"><span data-stu-id="0c269-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="0c269-119">Viðbótarhnappar á síðunni **Kostnaðartegundir** gefa aðgang að verktengdum upplýsingum um valda kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="0c269-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="0c269-120">T.d. er hægt að skoða verktengdar upplýsingar, skilgreina starfsmenn eða verk, skilgreina tímakostnað og söluverð og skoða skýrslur.</span><span class="sxs-lookup"><span data-stu-id="0c269-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




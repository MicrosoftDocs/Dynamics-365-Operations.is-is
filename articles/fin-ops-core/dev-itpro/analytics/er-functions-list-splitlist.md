---
title: SPLITLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLITLIST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 03/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745570"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="0925e-103">SPLITLIST ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="0925e-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0925e-104">Aðgerðin `SPLITLIST` skiptir tilgreindum lista niður í undirlista (eða runur) sem hver inniheldur tilgreindan fjölda skráa.</span><span class="sxs-lookup"><span data-stu-id="0925e-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="0925e-105">Hún skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum.</span><span class="sxs-lookup"><span data-stu-id="0925e-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0925e-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="0925e-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="0925e-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="0925e-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="0925e-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="0925e-108">Arguments</span></span>

<span data-ttu-id="0925e-109">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="0925e-109">`list`: *Record list*</span></span>

<span data-ttu-id="0925e-110">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="0925e-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0925e-111">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="0925e-111">`number`: *Integer*</span></span>

<span data-ttu-id="0925e-112">Hámarksfjöldi skráa í hverri runu.</span><span class="sxs-lookup"><span data-stu-id="0925e-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="0925e-113">`on-demand reading flag`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="0925e-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="0925e-114">*Boolean*-gildi tilgreinir hvort mynda eigi til einingar undirlista eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0925e-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="0925e-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="0925e-115">Return values</span></span>

<span data-ttu-id="0925e-116">*Færslulisti*</span><span class="sxs-lookup"><span data-stu-id="0925e-116">*Record list*</span></span>

<span data-ttu-id="0925e-117">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="0925e-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0925e-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="0925e-118">Usage notes</span></span>

<span data-ttu-id="0925e-119">Listi yfir runur sem er skilað inniheldur eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="0925e-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="0925e-120">**Gildi:** *Listi*</span><span class="sxs-lookup"><span data-stu-id="0925e-120">**Value:** *List*</span></span>

    <span data-ttu-id="0925e-121">Listi yfir skrár sem tilheyra núverandi runu.</span><span class="sxs-lookup"><span data-stu-id="0925e-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="0925e-122">**BatchNumber:** *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="0925e-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="0925e-123">Númer gildandi runu í skiluðum lista.</span><span class="sxs-lookup"><span data-stu-id="0925e-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="0925e-124">Þegar lestrarflagg eftir þörfum er stillt á **Satt** eru undirlistar búnir til eftir beiðni sem gerir notendum kleift að minnka minnisnotkun en sem getur haft áhrif á afköst ef einingar eru ekki notaðar í röð.</span><span class="sxs-lookup"><span data-stu-id="0925e-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="0925e-125">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0925e-125">Example</span></span>

<span data-ttu-id="0925e-126">Í eftirfarandi mynd er gagnagjafi **Lína** búinn til sem skráalisti sem hefur þrjár skrár.</span><span class="sxs-lookup"><span data-stu-id="0925e-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="0925e-127">Þessi listi er skiptur í runur, sem hver um sig inniheldur allt að tvær færslur.</span><span class="sxs-lookup"><span data-stu-id="0925e-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="0925e-128">Eftirfarandi mynd sýnir hannað útlit sniðs.</span><span class="sxs-lookup"><span data-stu-id="0925e-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="0925e-129">Í þessu sniðmáti eru tengsl við gagnagjafann **Línur** mynduð til að búa til úttak á XML sniði.</span><span class="sxs-lookup"><span data-stu-id="0925e-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="0925e-130">Þessi útkoma kynnir einstaka hnúta fyrir hverja runu og færslurnar í henni.</span><span class="sxs-lookup"><span data-stu-id="0925e-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="0925e-131">Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="0925e-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="0925e-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0925e-132">Additional resources</span></span>

[<span data-ttu-id="0925e-133">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="0925e-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

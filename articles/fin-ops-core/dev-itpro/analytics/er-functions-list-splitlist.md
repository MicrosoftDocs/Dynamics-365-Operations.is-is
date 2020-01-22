---
title: SPLITLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLITLIST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b324d42a53b35074ba62ccf3df7b77cb4db70450
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917213"
---
# <span data-ttu-id="a35ef-103"><a name="SPLITLIST">SPLITLIST ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="a35ef-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a35ef-104">Aðgerðin `SPLITLIST` skiptir tilgreindum lista niður í undirlista (eða runur) sem hver inniheldur tilgreindan fjölda skráa.</span><span class="sxs-lookup"><span data-stu-id="a35ef-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="a35ef-105">Hún skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum.</span><span class="sxs-lookup"><span data-stu-id="a35ef-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35ef-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="a35ef-106">Syntax</span></span>

```
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="a35ef-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="a35ef-107">Arguments</span></span>

<span data-ttu-id="a35ef-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a35ef-108">`list`: *Record list*</span></span>

<span data-ttu-id="a35ef-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="a35ef-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a35ef-110">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="a35ef-110">`number`: *Integer*</span></span>

<span data-ttu-id="a35ef-111">Hámarksfjöldi skráa í hverri runu.</span><span class="sxs-lookup"><span data-stu-id="a35ef-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="a35ef-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="a35ef-112">Return values</span></span>

<span data-ttu-id="a35ef-113">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a35ef-113">*Record list*</span></span>

<span data-ttu-id="a35ef-114">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="a35ef-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a35ef-115">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="a35ef-115">Usage notes</span></span>

<span data-ttu-id="a35ef-116">Listi yfir runur sem er skilað inniheldur eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="a35ef-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="a35ef-117">**Gildi:** *Listi*</span><span class="sxs-lookup"><span data-stu-id="a35ef-117">**Value:** *List*</span></span>

    <span data-ttu-id="a35ef-118">Listi yfir skrár sem tilheyra núverandi runu.</span><span class="sxs-lookup"><span data-stu-id="a35ef-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="a35ef-119">**BatchNumber:** *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="a35ef-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="a35ef-120">Númer gildandi runu í skiluðum lista.</span><span class="sxs-lookup"><span data-stu-id="a35ef-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="a35ef-121">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a35ef-121">Example</span></span>

<span data-ttu-id="a35ef-122">Í eftirfarandi mynd er gagnagjafi **Lína** búinn til sem skráalisti sem hefur þrjár skrár.</span><span class="sxs-lookup"><span data-stu-id="a35ef-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="a35ef-123">Þessi listi er skiptur í runur, sem hver um sig inniheldur allt að tvær færslur.</span><span class="sxs-lookup"><span data-stu-id="a35ef-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="a35ef-124">Eftirfarandi mynd sýnir hannað útlit sniðs.</span><span class="sxs-lookup"><span data-stu-id="a35ef-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="a35ef-125">Í þessu sniðmáti eru tengsl við gagnagjafann **Línur** mynduð til að búa til úttak á XML sniði.</span><span class="sxs-lookup"><span data-stu-id="a35ef-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="a35ef-126">Þessi útkoma kynnir einstaka hnúta fyrir hverja runu og færslurnar í henni.</span><span class="sxs-lookup"><span data-stu-id="a35ef-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="a35ef-127">Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="a35ef-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="a35ef-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a35ef-128">Additional resources</span></span>

[<span data-ttu-id="a35ef-129">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="a35ef-129">List functions</span></span>](er-functions-category-list.md)

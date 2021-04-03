---
title: SPLITLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLITLIST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559139"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="5eac6-103">SPLITLIST ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="5eac6-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eac6-104">Aðgerðin `SPLITLIST` skiptir tilgreindum lista niður í undirlista (eða runur) sem hver inniheldur tilgreindan fjölda skráa.</span><span class="sxs-lookup"><span data-stu-id="5eac6-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="5eac6-105">Hún skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum.</span><span class="sxs-lookup"><span data-stu-id="5eac6-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eac6-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="5eac6-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="5eac6-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="5eac6-107">Arguments</span></span>

<span data-ttu-id="5eac6-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="5eac6-108">`list`: *Record list*</span></span>

<span data-ttu-id="5eac6-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="5eac6-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="5eac6-110">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="5eac6-110">`number`: *Integer*</span></span>

<span data-ttu-id="5eac6-111">Hámarksfjöldi skráa í hverri runu.</span><span class="sxs-lookup"><span data-stu-id="5eac6-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="5eac6-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="5eac6-112">Return values</span></span>

<span data-ttu-id="5eac6-113">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="5eac6-113">*Record list*</span></span>

<span data-ttu-id="5eac6-114">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="5eac6-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5eac6-115">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="5eac6-115">Usage notes</span></span>

<span data-ttu-id="5eac6-116">Listi yfir runur sem er skilað inniheldur eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="5eac6-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="5eac6-117">**Gildi:** *Listi*</span><span class="sxs-lookup"><span data-stu-id="5eac6-117">**Value:** *List*</span></span>

    <span data-ttu-id="5eac6-118">Listi yfir skrár sem tilheyra núverandi runu.</span><span class="sxs-lookup"><span data-stu-id="5eac6-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="5eac6-119">**BatchNumber:** *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="5eac6-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="5eac6-120">Númer gildandi runu í skiluðum lista.</span><span class="sxs-lookup"><span data-stu-id="5eac6-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="5eac6-121">Dæmi</span><span class="sxs-lookup"><span data-stu-id="5eac6-121">Example</span></span>

<span data-ttu-id="5eac6-122">Í eftirfarandi mynd er gagnagjafi **Lína** búinn til sem skráalisti sem hefur þrjár skrár.</span><span class="sxs-lookup"><span data-stu-id="5eac6-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="5eac6-123">Þessi listi er skiptur í runur, sem hver um sig inniheldur allt að tvær færslur.</span><span class="sxs-lookup"><span data-stu-id="5eac6-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="5eac6-124">Eftirfarandi mynd sýnir hannað útlit sniðs.</span><span class="sxs-lookup"><span data-stu-id="5eac6-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="5eac6-125">Í þessu sniðmáti eru tengsl við gagnagjafann **Línur** mynduð til að búa til úttak á XML sniði.</span><span class="sxs-lookup"><span data-stu-id="5eac6-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="5eac6-126">Þessi útkoma kynnir einstaka hnúta fyrir hverja runu og færslurnar í henni.</span><span class="sxs-lookup"><span data-stu-id="5eac6-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="5eac6-127">Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="5eac6-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="5eac6-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5eac6-128">Additional resources</span></span>

[<span data-ttu-id="5eac6-129">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="5eac6-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: FIRST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FIRST í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917351"
---
# <span data-ttu-id="f26b5-103"><a name="FIRST">FIRST ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="f26b5-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f26b5-104">Aðgerðin `FIRST` skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef listinn er ekki tómur.</span><span class="sxs-lookup"><span data-stu-id="f26b5-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="f26b5-105">Ef listinn er tómur kastar þessi aðgerð frá sér undantekningu.</span><span class="sxs-lookup"><span data-stu-id="f26b5-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="f26b5-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f26b5-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="f26b5-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f26b5-107">Arguments</span></span>

<span data-ttu-id="f26b5-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f26b5-108">`list`: *Record list*</span></span>

<span data-ttu-id="f26b5-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="f26b5-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f26b5-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f26b5-110">Return values</span></span>

<span data-ttu-id="f26b5-111">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="f26b5-111">*Container (record)*</span></span>

<span data-ttu-id="f26b5-112">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="f26b5-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f26b5-113">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="f26b5-113">Example 1</span></span>

<span data-ttu-id="f26b5-114">Segðin `FIRST(SPLIT("ABC",1)).Value` skilar textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="f26b5-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f26b5-115">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="f26b5-115">Example 2</span></span>

<span data-ttu-id="f26b5-116">Segðin `FIRST(SPLIT("",1)).Value` gerir undantekningu á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="f26b5-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f26b5-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f26b5-117">Additional resources</span></span>

[<span data-ttu-id="f26b5-118">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="f26b5-118">List functions</span></span>](er-functions-category-list.md)

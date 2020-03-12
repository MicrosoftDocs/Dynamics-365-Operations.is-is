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
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042091"
---
# <span data-ttu-id="e51ab-103"><a name="FIRST">FIRST ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="e51ab-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e51ab-104">Aðgerðin `FIRST` skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef listinn er ekki tómur.</span><span class="sxs-lookup"><span data-stu-id="e51ab-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="e51ab-105">Ef listinn er tómur kastar þessi aðgerð frá sér undantekningu.</span><span class="sxs-lookup"><span data-stu-id="e51ab-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51ab-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="e51ab-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="e51ab-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="e51ab-107">Arguments</span></span>

<span data-ttu-id="e51ab-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="e51ab-108">`list`: *Record list*</span></span>

<span data-ttu-id="e51ab-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="e51ab-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e51ab-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="e51ab-110">Return values</span></span>

<span data-ttu-id="e51ab-111">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="e51ab-111">*Container (record)*</span></span>

<span data-ttu-id="e51ab-112">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="e51ab-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e51ab-113">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="e51ab-113">Example 1</span></span>

<span data-ttu-id="e51ab-114">Segðin `FIRST(SPLIT("ABC",1)).Value` skilar textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="e51ab-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e51ab-115">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="e51ab-115">Example 2</span></span>

<span data-ttu-id="e51ab-116">Segðin `FIRST(SPLIT("",1)).Value` gerir undantekningu á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="e51ab-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e51ab-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e51ab-117">Additional resources</span></span>

[<span data-ttu-id="e51ab-118">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="e51ab-118">List functions</span></span>](er-functions-category-list.md)

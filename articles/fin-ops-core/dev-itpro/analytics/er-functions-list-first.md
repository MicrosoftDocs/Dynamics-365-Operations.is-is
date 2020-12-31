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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679415"
---
# <a name="first-er-function"></a><span data-ttu-id="28107-103">FIRST ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="28107-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28107-104">Aðgerðin `FIRST` skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef listinn er ekki tómur.</span><span class="sxs-lookup"><span data-stu-id="28107-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="28107-105">Ef listinn er tómur kastar þessi aðgerð frá sér undantekningu.</span><span class="sxs-lookup"><span data-stu-id="28107-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="28107-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="28107-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="28107-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="28107-107">Arguments</span></span>

<span data-ttu-id="28107-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="28107-108">`list`: *Record list*</span></span>

<span data-ttu-id="28107-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="28107-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="28107-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="28107-110">Return values</span></span>

<span data-ttu-id="28107-111">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="28107-111">*Container (record)*</span></span>

<span data-ttu-id="28107-112">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="28107-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="28107-113">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="28107-113">Example 1</span></span>

<span data-ttu-id="28107-114">Segðin `FIRST(SPLIT("ABC",1)).Value` skilar textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="28107-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="28107-115">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="28107-115">Example 2</span></span>

<span data-ttu-id="28107-116">Segðin `FIRST(SPLIT("",1)).Value` gerir undantekningu á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="28107-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28107-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="28107-117">Additional resources</span></span>

[<span data-ttu-id="28107-118">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="28107-118">List functions</span></span>](er-functions-category-list.md)

---
title: INT64VALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin INT64VALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686052"
---
# <a name="int64value-er-function"></a><span data-ttu-id="4ba87-103">INT64VALUE ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="4ba87-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ba87-104">Aðerðin `INT64VALUE` skilar *Int64*-gildi sem táknar tilgreindan streng.</span><span class="sxs-lookup"><span data-stu-id="4ba87-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4ba87-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="4ba87-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="4ba87-106">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="4ba87-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="4ba87-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4ba87-107">Arguments</span></span>

<span data-ttu-id="4ba87-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="4ba87-108">`text`: *String*</span></span>

<span data-ttu-id="4ba87-109">Textagildi sem þarf umreikna í *Int64*-tölu.</span><span class="sxs-lookup"><span data-stu-id="4ba87-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="4ba87-110">`number`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="4ba87-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="4ba87-111">Tölugildið *Rauntala* eða *Heitala* sem þarf umreikna í *Int64*-tölu.</span><span class="sxs-lookup"><span data-stu-id="4ba87-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ba87-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4ba87-112">Return values</span></span>

<span data-ttu-id="4ba87-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="4ba87-113">*Int64*</span></span>

<span data-ttu-id="4ba87-114">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="4ba87-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4ba87-115">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="4ba87-115">Usage notes</span></span>

<span data-ttu-id="4ba87-116">Allir aukastafir eru styttir.</span><span class="sxs-lookup"><span data-stu-id="4ba87-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="4ba87-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="4ba87-117">Example 1</span></span>

<span data-ttu-id="4ba87-118">`INT64VALUE ("22565422744")` skilar *Int64*-gildinu **-22565422744**.</span><span class="sxs-lookup"><span data-stu-id="4ba87-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4ba87-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="4ba87-119">Example 2</span></span>

<span data-ttu-id="4ba87-120">`INT64VALUE ( VALUE("22565422744.77"))` skilar *Int64*-gildinu **-22565422744**.</span><span class="sxs-lookup"><span data-stu-id="4ba87-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ba87-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4ba87-121">Additional resources</span></span>

[<span data-ttu-id="4ba87-122">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="4ba87-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)

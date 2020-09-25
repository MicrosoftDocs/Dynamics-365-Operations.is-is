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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744840"
---
# <a name="int64value-er-function"></a><span data-ttu-id="83041-103">INT64VALUE ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="83041-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83041-104">Aðerðin `INT64VALUE` skilar *Int64*-gildi sem táknar tilgreindan streng.</span><span class="sxs-lookup"><span data-stu-id="83041-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="83041-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="83041-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="83041-106">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="83041-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="83041-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="83041-107">Arguments</span></span>

<span data-ttu-id="83041-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="83041-108">`text`: *String*</span></span>

<span data-ttu-id="83041-109">Textagildi sem þarf umreikna í *Int64*-tölu.</span><span class="sxs-lookup"><span data-stu-id="83041-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="83041-110">`number`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="83041-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="83041-111">Tölugildið *Rauntala* eða *Heitala* sem þarf umreikna í *Int64*-tölu.</span><span class="sxs-lookup"><span data-stu-id="83041-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="83041-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="83041-112">Return values</span></span>

<span data-ttu-id="83041-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="83041-113">*Int64*</span></span>

<span data-ttu-id="83041-114">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="83041-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="83041-115">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="83041-115">Usage notes</span></span>

<span data-ttu-id="83041-116">Allir aukastafir eru styttir.</span><span class="sxs-lookup"><span data-stu-id="83041-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="83041-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="83041-117">Example 1</span></span>

<span data-ttu-id="83041-118">`INT64VALUE ("22565422744")` skilar *Int64*-gildinu **-22565422744**.</span><span class="sxs-lookup"><span data-stu-id="83041-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="83041-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="83041-119">Example 2</span></span>

<span data-ttu-id="83041-120">`INT64VALUE ( VALUE("22565422744.77"))` skilar *Int64*-gildinu **-22565422744**.</span><span class="sxs-lookup"><span data-stu-id="83041-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83041-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="83041-121">Additional resources</span></span>

[<span data-ttu-id="83041-122">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="83041-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)

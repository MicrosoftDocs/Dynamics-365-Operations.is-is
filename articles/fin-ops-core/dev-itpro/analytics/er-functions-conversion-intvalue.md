---
title: INTVALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin INTVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755373"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="88240-103">INTVALUE ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="88240-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88240-104">Aðerðin `INTVALUE` skilar *Int*-gildi sem táknar tilgreindan streng.</span><span class="sxs-lookup"><span data-stu-id="88240-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="88240-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="88240-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="88240-106">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="88240-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="88240-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="88240-107">Arguments</span></span>

<span data-ttu-id="88240-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="88240-108">`text`: *String*</span></span>

<span data-ttu-id="88240-109">Textagildi sem þarf umreikna í *Int*-tölu.</span><span class="sxs-lookup"><span data-stu-id="88240-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="88240-110">`number`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="88240-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="88240-111">Tölugildið *Rauntala* eða *Heitala* sem þarf umreikna í *Int*-tölu.</span><span class="sxs-lookup"><span data-stu-id="88240-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="88240-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="88240-112">Return values</span></span>

<span data-ttu-id="88240-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="88240-113">*Int*</span></span>

<span data-ttu-id="88240-114">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="88240-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="88240-115">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="88240-115">Usage notes</span></span>

<span data-ttu-id="88240-116">Allir aukastafir eru styttir.</span><span class="sxs-lookup"><span data-stu-id="88240-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="88240-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="88240-117">Example 1</span></span>

<span data-ttu-id="88240-118">`INTVALUE ("100.77")` skilar *Int*-gildinu **100**.</span><span class="sxs-lookup"><span data-stu-id="88240-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="88240-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="88240-119">Example 2</span></span>

<span data-ttu-id="88240-120">`INTVALUE (-100.77)` skilar *Int*-gildinu **-100**.</span><span class="sxs-lookup"><span data-stu-id="88240-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88240-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="88240-121">Additional resources</span></span>

[<span data-ttu-id="88240-122">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="88240-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
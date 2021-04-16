---
title: INT64VALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin INT64VALUE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755397"
---
# <a name="int64value-er-function"></a><span data-ttu-id="688b1-103">INT64VALUE ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="688b1-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="688b1-104">Aðerðin `INT64VALUE` skilar *Int64*-gildi sem táknar tilgreindan streng.</span><span class="sxs-lookup"><span data-stu-id="688b1-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="688b1-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="688b1-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="688b1-106">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="688b1-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="688b1-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="688b1-107">Arguments</span></span>

<span data-ttu-id="688b1-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="688b1-108">`text`: *String*</span></span>

<span data-ttu-id="688b1-109">Textagildi sem þarf umreikna í *Int64*-tölu.</span><span class="sxs-lookup"><span data-stu-id="688b1-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="688b1-110">`number`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="688b1-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="688b1-111">Tölugildið *Rauntala* eða *Heitala* sem þarf umreikna í *Int64*-tölu.</span><span class="sxs-lookup"><span data-stu-id="688b1-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="688b1-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="688b1-112">Return values</span></span>

<span data-ttu-id="688b1-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="688b1-113">*Int64*</span></span>

<span data-ttu-id="688b1-114">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="688b1-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="688b1-115">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="688b1-115">Usage notes</span></span>

<span data-ttu-id="688b1-116">Allir aukastafir eru styttir.</span><span class="sxs-lookup"><span data-stu-id="688b1-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="688b1-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="688b1-117">Example 1</span></span>

<span data-ttu-id="688b1-118">`INT64VALUE ("22565422744")` skilar *Int64*-gildinu **-22565422744**.</span><span class="sxs-lookup"><span data-stu-id="688b1-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="688b1-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="688b1-119">Example 2</span></span>

<span data-ttu-id="688b1-120">`INT64VALUE ( VALUE("22565422744.77"))` skilar *Int64*-gildinu **-22565422744**.</span><span class="sxs-lookup"><span data-stu-id="688b1-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="688b1-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="688b1-121">Additional resources</span></span>

[<span data-ttu-id="688b1-122">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="688b1-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
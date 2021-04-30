---
title: NUMBERFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMBERFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890384"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="d082e-103">NUMBERFORMAT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="d082e-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d082e-104">Aðgerðin `NUMBERFORMAT` skilar *String*-gildi sem setur fram tilgreinda tölu á tilgreindu sniði og í valinni tiltekinni [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="d082e-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="d082e-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-numeric-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="d082e-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d082e-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="d082e-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d082e-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="d082e-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d082e-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="d082e-108">Arguments</span></span>

<span data-ttu-id="d082e-109">`number`: *Heiltala* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="d082e-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d082e-110">Tölugildi sem tilgreinir töluna sem verður að forsníða.</span><span class="sxs-lookup"><span data-stu-id="d082e-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="d082e-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="d082e-111">`format` : *String*</span></span>

<span data-ttu-id="d082e-112">Gildið *Strengur* sem táknar sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="d082e-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="d082e-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="d082e-113">`culture`: *String*</span></span>

<span data-ttu-id="d082e-114">Gildið *Strengur* sem táknar menninguna sem á að nota til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="d082e-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="d082e-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d082e-115">Return values</span></span>

<span data-ttu-id="d082e-116">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="d082e-116">*String*</span></span>

<span data-ttu-id="d082e-117">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="d082e-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d082e-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="d082e-118">Usage notes</span></span>

<span data-ttu-id="d082e-119">Ef menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar ákvarðar samhengið sem þessari aðgerð er keyrt í hvaða menning er notuð til að forsníða tölur.</span><span class="sxs-lookup"><span data-stu-id="d082e-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="d082e-120">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="d082e-120">Example 1</span></span>

<span data-ttu-id="d082e-121">Fyrir menninguna **EN-US** skilar `NUMBERFORMAT (0.45, "p")` **"45,00 %"** og `NUMBERFORMAT (10.45, "#")` skilar **"10"**.</span><span class="sxs-lookup"><span data-stu-id="d082e-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d082e-122">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="d082e-122">Example 2</span></span>

<span data-ttu-id="d082e-123">`NUMBERFORMAT (10/3, "F2", "de")` skilar **3,33** en `NUMBERFORMAT (10/3, "F2", "en-us")` skilar **3,33**.</span><span class="sxs-lookup"><span data-stu-id="d082e-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d082e-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d082e-124">Additional resources</span></span>

[<span data-ttu-id="d082e-125">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="d082e-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
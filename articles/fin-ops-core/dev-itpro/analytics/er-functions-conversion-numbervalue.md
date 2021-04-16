---
title: NUMBERVALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMBERVALUE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755349"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="8b5c3-103">NUMBERVALUE ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="8b5c3-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b5c3-104">Aðgerðin `NUMBERVALUE` skilar *Raun*-gildi sem er umreiknað úr tilgreindu *Streng*-gildi.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="8b5c3-105">Við umreikning er tekið tillit til tilgreindra flokkunarskiltákna aukastafa og tölustafa.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5c3-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="8b5c3-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="8b5c3-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="8b5c3-107">Arguments</span></span>

<span data-ttu-id="8b5c3-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="8b5c3-108">`text`: *String*</span></span>

<span data-ttu-id="8b5c3-109">Textagildi sem þarf umreikna í *Raun*-tölu.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="8b5c3-110">`decimal separator`: Strengur</span><span class="sxs-lookup"><span data-stu-id="8b5c3-110">`decimal separator`: String</span></span>

<span data-ttu-id="8b5c3-111">Skiltákn fyrir aukastaf.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-111">A decimal separator.</span></span> <span data-ttu-id="8b5c3-112">Það er notað til að aðgreina heiltölur og aukastafi brota.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="8b5c3-113">`digit grouping separator`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="8b5c3-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="8b5c3-114">Flokkunarskiltákn fyrir tölustafi.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-114">A digit grouping separator.</span></span> <span data-ttu-id="8b5c3-115">Það er notað sem þúsundaskiltákn.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="8b5c3-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="8b5c3-116">Return values</span></span>

<span data-ttu-id="8b5c3-117">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="8b5c3-117">*Real*</span></span>

<span data-ttu-id="8b5c3-118">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8b5c3-119">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8b5c3-119">Example</span></span>

<span data-ttu-id="8b5c3-120">`NUMBERVALUE( "1 234,56", ",", " ")` skilar **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="8b5c3-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b5c3-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8b5c3-121">Additional resources</span></span>

[<span data-ttu-id="8b5c3-122">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="8b5c3-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
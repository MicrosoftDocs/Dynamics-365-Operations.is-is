---
title: NUMBERVALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMBERVALUE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916523"
---
# <span data-ttu-id="3a565-103"><a name="NUMBERVALUE">NUMBERVALUE ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="3a565-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a565-104">Aðgerðin `NUMBERVALUE` skilar *Raun*-gildi sem er umreiknað úr tilgreindu *Streng*-gildi.</span><span class="sxs-lookup"><span data-stu-id="3a565-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="3a565-105">Við umreikning er tekið tillit til tilgreindra flokkunarskiltákna aukastafa og tölustafa.</span><span class="sxs-lookup"><span data-stu-id="3a565-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a565-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="3a565-106">Syntax</span></span>

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="3a565-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="3a565-107">Arguments</span></span>

<span data-ttu-id="3a565-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="3a565-108">`text`: *String*</span></span>

<span data-ttu-id="3a565-109">Textagildi sem þarf umreikna í *Raun*-tölu.</span><span class="sxs-lookup"><span data-stu-id="3a565-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="3a565-110">`decimal separator`: Strengur</span><span class="sxs-lookup"><span data-stu-id="3a565-110">`decimal separator`: String</span></span>

<span data-ttu-id="3a565-111">Skiltákn fyrir aukastaf.</span><span class="sxs-lookup"><span data-stu-id="3a565-111">A decimal separator.</span></span> <span data-ttu-id="3a565-112">Það er notað til að aðgreina heiltölur og aukastafi brota.</span><span class="sxs-lookup"><span data-stu-id="3a565-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="3a565-113">`digit grouping separator`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="3a565-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="3a565-114">Flokkunarskiltákn fyrir tölustafi.</span><span class="sxs-lookup"><span data-stu-id="3a565-114">A digit grouping separator.</span></span> <span data-ttu-id="3a565-115">Það er notað sem þúsundaskiltákn.</span><span class="sxs-lookup"><span data-stu-id="3a565-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a565-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="3a565-116">Return values</span></span>

<span data-ttu-id="3a565-117">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="3a565-117">*Real*</span></span>

<span data-ttu-id="3a565-118">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="3a565-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="3a565-119">Dæmi</span><span class="sxs-lookup"><span data-stu-id="3a565-119">Example</span></span>

<span data-ttu-id="3a565-120">`NUMBERVALUE( "1 234,56", ",", " ")` skilar **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="3a565-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a565-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3a565-121">Additional resources</span></span>

[<span data-ttu-id="3a565-122">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="3a565-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)

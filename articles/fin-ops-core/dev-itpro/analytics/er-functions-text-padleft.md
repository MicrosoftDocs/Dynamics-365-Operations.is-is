---
title: PADLEFT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin PADLEFT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680147"
---
# <a name="padleft-er-function"></a><span data-ttu-id="b12f0-103">PADLEFT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="b12f0-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b12f0-104">Aðgerðin `PADLEFT` skilar *strengjagildi* af tilgreindri lengd, þar sem upphaf tilgreinds strengs er fyllt með tilgreindum stöfum.</span><span class="sxs-lookup"><span data-stu-id="b12f0-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b12f0-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="b12f0-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="b12f0-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="b12f0-106">Arguments</span></span>

<span data-ttu-id="b12f0-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="b12f0-107">`text`: *String*</span></span>

<span data-ttu-id="b12f0-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="b12f0-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="b12f0-109">`length`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="b12f0-109">`length`: *Integer*</span></span>

<span data-ttu-id="b12f0-110">*Heiltölu*-gildi sem táknar lokafjölda stafa í fyllta strengnum.</span><span class="sxs-lookup"><span data-stu-id="b12f0-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="b12f0-111">`padding chars`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="b12f0-111">`padding chars`: *String*</span></span>

<span data-ttu-id="b12f0-112">Staftáknin sem á að nota við fyllingu.</span><span class="sxs-lookup"><span data-stu-id="b12f0-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="b12f0-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="b12f0-113">Return values</span></span>

<span data-ttu-id="b12f0-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="b12f0-114">*String*</span></span>

<span data-ttu-id="b12f0-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="b12f0-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b12f0-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b12f0-116">Example</span></span>

<span data-ttu-id="b12f0-117">`PADLEFT ("1234", 10, "`&nbsp;`")` skilar textastrengnum **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="b12f0-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b12f0-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b12f0-118">Additional resources</span></span>

[<span data-ttu-id="b12f0-119">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="b12f0-119">Text functions</span></span>](er-functions-category-text.md)

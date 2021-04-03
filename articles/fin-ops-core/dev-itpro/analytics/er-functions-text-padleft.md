---
title: PADLEFT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin PADLEFT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562686"
---
# <a name="padleft-er-function"></a><span data-ttu-id="f0ffe-103">PADLEFT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f0ffe-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0ffe-104">Aðgerðin `PADLEFT` skilar *strengjagildi* af tilgreindri lengd, þar sem upphaf tilgreinds strengs er fyllt með tilgreindum stöfum.</span><span class="sxs-lookup"><span data-stu-id="f0ffe-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ffe-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f0ffe-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="f0ffe-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f0ffe-106">Arguments</span></span>

<span data-ttu-id="f0ffe-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f0ffe-107">`text`: *String*</span></span>

<span data-ttu-id="f0ffe-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="f0ffe-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="f0ffe-109">`length`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="f0ffe-109">`length`: *Integer*</span></span>

<span data-ttu-id="f0ffe-110">*Heiltölu*-gildi sem táknar lokafjölda stafa í fyllta strengnum.</span><span class="sxs-lookup"><span data-stu-id="f0ffe-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="f0ffe-111">`padding chars`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f0ffe-111">`padding chars`: *String*</span></span>

<span data-ttu-id="f0ffe-112">Staftáknin sem á að nota við fyllingu.</span><span class="sxs-lookup"><span data-stu-id="f0ffe-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="f0ffe-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f0ffe-113">Return values</span></span>

<span data-ttu-id="f0ffe-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f0ffe-114">*String*</span></span>

<span data-ttu-id="f0ffe-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="f0ffe-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f0ffe-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f0ffe-116">Example</span></span>

<span data-ttu-id="f0ffe-117">`PADLEFT ("1234", 10, "`&nbsp;`")` skilar textastrengnum **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="f0ffe-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0ffe-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f0ffe-118">Additional resources</span></span>

[<span data-ttu-id="f0ffe-119">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="f0ffe-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
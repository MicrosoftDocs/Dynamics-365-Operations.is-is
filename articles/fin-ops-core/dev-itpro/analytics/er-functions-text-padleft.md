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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040964"
---
# <span data-ttu-id="04621-103"><a name="PADLEFT">PADLEFT ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="04621-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04621-104">Aðgerðin `PADLEFT` skilar *strengjagildi* af tilgreindri lengd, þar sem upphaf tilgreinds strengs er fyllt með tilgreindum stöfum.</span><span class="sxs-lookup"><span data-stu-id="04621-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="04621-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="04621-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="04621-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="04621-106">Arguments</span></span>

<span data-ttu-id="04621-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="04621-107">`text`: *String*</span></span>

<span data-ttu-id="04621-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="04621-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="04621-109">`length`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="04621-109">`length`: *Integer*</span></span>

<span data-ttu-id="04621-110">*Heiltölu*-gildi sem táknar lokafjölda stafa í fyllta strengnum.</span><span class="sxs-lookup"><span data-stu-id="04621-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="04621-111">`padding chars`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="04621-111">`padding chars`: *String*</span></span>

<span data-ttu-id="04621-112">Staftáknin sem á að nota við fyllingu.</span><span class="sxs-lookup"><span data-stu-id="04621-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="04621-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="04621-113">Return values</span></span>

<span data-ttu-id="04621-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="04621-114">*String*</span></span>

<span data-ttu-id="04621-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="04621-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="04621-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="04621-116">Example</span></span>

<span data-ttu-id="04621-117">`PADLEFT ("1234", 10, "`&nbsp;`")` skilar textastrengnum **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="04621-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04621-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="04621-118">Additional resources</span></span>

[<span data-ttu-id="04621-119">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="04621-119">Text functions</span></span>](er-functions-category-text.md)

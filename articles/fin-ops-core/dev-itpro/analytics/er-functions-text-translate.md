---
title: TRANSLATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TRANSLATE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916707"
---
# <span data-ttu-id="8cc21-103"><a name="TRANSLATE">TRANSLATE ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="8cc21-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cc21-104">Aðgerðin `TRANSLATE` skilar tilgreindum textastreng sem *Strengja*-gildi eftir að öllu því eða öllu leyti hefur verið skipt út fyrir annan streng.</span><span class="sxs-lookup"><span data-stu-id="8cc21-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc21-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="8cc21-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="8cc21-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="8cc21-106">Arguments</span></span>

<span data-ttu-id="8cc21-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="8cc21-107">`text`: *String*</span></span>

<span data-ttu-id="8cc21-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="8cc21-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="8cc21-109">`pattern`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="8cc21-109">`pattern`: *String*</span></span>

<span data-ttu-id="8cc21-110">Textinn sem verður að skipta út.</span><span class="sxs-lookup"><span data-stu-id="8cc21-110">The text that must be replaced.</span></span>

<span data-ttu-id="8cc21-111">`replacement`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="8cc21-111">`replacement`: *String*</span></span>

<span data-ttu-id="8cc21-112">Textinn sem á að nota í staðinn.</span><span class="sxs-lookup"><span data-stu-id="8cc21-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="8cc21-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="8cc21-113">Return values</span></span>

<span data-ttu-id="8cc21-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="8cc21-114">*String*</span></span>

<span data-ttu-id="8cc21-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="8cc21-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8cc21-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8cc21-116">Example</span></span>

<span data-ttu-id="8cc21-117">`TRANSLATE ("abcdef", "cd", "GH")` kemur í stað mynstursins **"cd"** með strengnum **"GH"** og skilar **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="8cc21-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cc21-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8cc21-118">Additional resources</span></span>

[<span data-ttu-id="8cc21-119">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="8cc21-119">Text functions</span></span>](er-functions-category-text.md)

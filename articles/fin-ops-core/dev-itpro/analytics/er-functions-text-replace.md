---
title: REPLACE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin REPLACE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040987"
---
# <span data-ttu-id="c194a-103"><a name="REPLACE">REPLACE ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="c194a-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c194a-104">Aðgerðin `REPLACE` skilar tilgreindum textastreng sem *Strengja*-gildi eftir að öllu því eða öllu leyti hefur verið skipt út fyrir annan streng.</span><span class="sxs-lookup"><span data-stu-id="c194a-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c194a-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="c194a-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="c194a-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="c194a-106">Arguments</span></span>

<span data-ttu-id="c194a-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c194a-107">`text`: *String*</span></span>

<span data-ttu-id="c194a-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="c194a-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="c194a-109">`pattern`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c194a-109">`pattern`: *String*</span></span>

<span data-ttu-id="c194a-110">Ef frumbreytan `regular expression flag` er **FALSE** inniheldur þessi frumbreyta textann sem þarf að skipta um.</span><span class="sxs-lookup"><span data-stu-id="c194a-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="c194a-111">Ef frumbreytan `regular expression flag` er **TRUE** inniheldur þessi frumbreyta reglulega segð sem skilgreinir bæði leitarmynstur og uppbótatexta.</span><span class="sxs-lookup"><span data-stu-id="c194a-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="c194a-112">`replacement`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c194a-112">`replacement`: *String*</span></span>

<span data-ttu-id="c194a-113">Ef frumbreytan `regular expression flag` er **FALSE** inniheldur þessi frumbreyta textann sem á að nota til að skipta um.</span><span class="sxs-lookup"><span data-stu-id="c194a-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="c194a-114">Ef frumbreytan `regular expression flag` er **TRUE** er þessi frumbreyta ekki notuð.</span><span class="sxs-lookup"><span data-stu-id="c194a-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="c194a-115">`regular expression flag`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="c194a-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="c194a-116">*Boolean*-gildi sem gefur til kynna hvort venjuleg segð sé notuð til að skipta um.</span><span class="sxs-lookup"><span data-stu-id="c194a-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="c194a-117">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="c194a-117">Return values</span></span>

<span data-ttu-id="c194a-118">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="c194a-118">*String*</span></span>

<span data-ttu-id="c194a-119">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="c194a-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c194a-120">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="c194a-120">Usage notes</span></span>

<span data-ttu-id="c194a-121">Ef frumbreytan `regular expression flag` er **TRUE** skilar þessi aðgerð tilgreindum streng eftir að henni hefur verið breytt með því að beita venjulegu segð sem er tilgreind af frumbreytunni `pattern`.</span><span class="sxs-lookup"><span data-stu-id="c194a-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="c194a-122">Reglulega segðin er notuð til að finna stafina sem verður að skipta út.</span><span class="sxs-lookup"><span data-stu-id="c194a-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="c194a-123">Ef frumbreytan `regular expression flag` er **FALSE** hagar þessi aðgerð sér eins og [TRANSLATE](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="c194a-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="c194a-124">Stafirnir sem eru tilgreindir af staðgengilsbreytunni `replacement` eru notaðir til að skipta út stöfum sem finnast.</span><span class="sxs-lookup"><span data-stu-id="c194a-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="c194a-125">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="c194a-125">Example 1</span></span>

<span data-ttu-id="c194a-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` notar reglulega segð sem fjarlægir öll tákn sem ekki eru tölur og skilar **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="c194a-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="c194a-127">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="c194a-127">Example 2</span></span>

<span data-ttu-id="c194a-128">`REPLACE ("abcdef", "cd", "GH", false)` kemur í stað mynstursins **"cd"** með strengnum **"GH"** og skilar **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="c194a-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c194a-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c194a-129">Additional resources</span></span>

[<span data-ttu-id="c194a-130">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="c194a-130">Text functions</span></span>](er-functions-category-text.md)

---
title: REPLACE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin REPLACE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746199"
---
# <a name="replace-er-function"></a><span data-ttu-id="ba47e-103">REPLACE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="ba47e-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba47e-104">Aðgerðin `REPLACE` skilar tilgreindum textastreng sem *Strengja*-gildi eftir að öllu því eða öllu leyti hefur verið skipt út fyrir annan streng.</span><span class="sxs-lookup"><span data-stu-id="ba47e-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba47e-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="ba47e-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="ba47e-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="ba47e-106">Arguments</span></span>

<span data-ttu-id="ba47e-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ba47e-107">`text`: *String*</span></span>

<span data-ttu-id="ba47e-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="ba47e-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="ba47e-109">`pattern`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ba47e-109">`pattern`: *String*</span></span>

<span data-ttu-id="ba47e-110">Ef frumbreytan `regular expression flag` er **FALSE** inniheldur þessi frumbreyta textann sem þarf að skipta um.</span><span class="sxs-lookup"><span data-stu-id="ba47e-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="ba47e-111">Ef frumbreytan `regular expression flag` er **TRUE** inniheldur þessi frumbreyta reglulega segð sem skilgreinir bæði leitarmynstur og uppbótatexta.</span><span class="sxs-lookup"><span data-stu-id="ba47e-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="ba47e-112">`replacement`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ba47e-112">`replacement`: *String*</span></span>

<span data-ttu-id="ba47e-113">Ef frumbreytan `regular expression flag` er **FALSE** inniheldur þessi frumbreyta textann sem á að nota til að skipta um.</span><span class="sxs-lookup"><span data-stu-id="ba47e-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="ba47e-114">Ef frumbreytan `regular expression flag` er **TRUE** er þessi frumbreyta ekki notuð.</span><span class="sxs-lookup"><span data-stu-id="ba47e-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="ba47e-115">`regular expression flag`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="ba47e-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="ba47e-116">*Boolean*-gildi sem gefur til kynna hvort venjuleg segð sé notuð til að skipta um.</span><span class="sxs-lookup"><span data-stu-id="ba47e-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba47e-117">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ba47e-117">Return values</span></span>

<span data-ttu-id="ba47e-118">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ba47e-118">*String*</span></span>

<span data-ttu-id="ba47e-119">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="ba47e-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ba47e-120">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="ba47e-120">Usage notes</span></span>

<span data-ttu-id="ba47e-121">Ef frumbreytan `regular expression flag` er **TRUE** skilar þessi aðgerð tilgreindum streng eftir að henni hefur verið breytt með því að beita venjulegu segð sem er tilgreind af frumbreytunni `pattern`.</span><span class="sxs-lookup"><span data-stu-id="ba47e-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="ba47e-122">Reglulega segðin er notuð til að finna stafina sem verður að skipta út.</span><span class="sxs-lookup"><span data-stu-id="ba47e-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="ba47e-123">Ef frumbreytan `regular expression flag` er **FALSE** skilar þessi aðgerð tilteknum streng á eftir stafasamstæðan sem er skilgreind í frumbreytunni `pattern` hefur verið skipt út fyrir stafina í frumbreytunni `replacement`.</span><span class="sxs-lookup"><span data-stu-id="ba47e-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="ba47e-124">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="ba47e-124">Example 1</span></span>

<span data-ttu-id="ba47e-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` notar reglulega segð sem fjarlægir öll tákn sem ekki eru tölur og skilar **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="ba47e-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="ba47e-126">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="ba47e-126">Example 2</span></span>

<span data-ttu-id="ba47e-127">`REPLACE ("abcdef", "cd", "GH", false)` kemur í stað mynstursins **"cd"** með strengnum **"GH"** og skilar **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="ba47e-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba47e-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ba47e-128">Additional resources</span></span>

[<span data-ttu-id="ba47e-129">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="ba47e-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
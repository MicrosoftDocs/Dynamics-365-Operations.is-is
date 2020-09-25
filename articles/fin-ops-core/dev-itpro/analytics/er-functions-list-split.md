---
title: SPLIT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLIT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: c171509353fed92b14ca0d7473742e4a9a54bad1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745274"
---
# <a name="split-er-function"></a><span data-ttu-id="f3a08-103">SPLIT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f3a08-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3a08-104">Aðgerðin `SPLIT` skiptir upp tilteknum ílagsstreng í undirstrengi og skilar niðurstöðunni sem nýju *Skráalista*-gildi.</span><span class="sxs-lookup"><span data-stu-id="f3a08-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="f3a08-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="f3a08-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="f3a08-106">Þessi málskipan er notuð til að skipta tilgreindum intaksstreng í undirstrengi, sem hvert um sig hefur tilgreinda lengd.</span><span class="sxs-lookup"><span data-stu-id="f3a08-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="f3a08-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="f3a08-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="f3a08-108">Þessi málskipan er notuð til að skipta tilgreindum innsláttarstreng í undirstrengi, byggt á tilgreindu skiltákni.</span><span class="sxs-lookup"><span data-stu-id="f3a08-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="f3a08-109">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f3a08-109">Arguments</span></span>

<span data-ttu-id="f3a08-110">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f3a08-110">`input`: *String*</span></span>

<span data-ttu-id="f3a08-111">Textinn sem á að skipta.</span><span class="sxs-lookup"><span data-stu-id="f3a08-111">The text to split.</span></span>

<span data-ttu-id="f3a08-112">`length`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="f3a08-112">`length`: *Integer*</span></span>

<span data-ttu-id="f3a08-113">Hámarkslengd staks undirstrengs.</span><span class="sxs-lookup"><span data-stu-id="f3a08-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="f3a08-114">`delimiter`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f3a08-114">`delimiter`: *String*</span></span>

<span data-ttu-id="f3a08-115">Afmarkari sem er notaður til að aðgreina undirstrengi.</span><span class="sxs-lookup"><span data-stu-id="f3a08-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="f3a08-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f3a08-116">Return values</span></span>

<span data-ttu-id="f3a08-117">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f3a08-117">*Record list*</span></span>

<span data-ttu-id="f3a08-118">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="f3a08-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f3a08-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="f3a08-119">Usage notes</span></span>

<span data-ttu-id="f3a08-120">Skráaskipulag listans sem er skilað samanstendur af reitnum **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="f3a08-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="f3a08-121">Sérhver skrá yfir listann sem er skilað inniheldur myndaða undirstrengi í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="f3a08-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="f3a08-122">Ef frumbreytan `delimiter` er tóm samantendur nýi listinn sem er skilað af einni skrá sem inniheldur reitinn **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="f3a08-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="f3a08-123">Þessi reitur inniheldur innsláttartexta.</span><span class="sxs-lookup"><span data-stu-id="f3a08-123">This field contains the input text.</span></span>

<span data-ttu-id="f3a08-124">Ef frumbreytan `input` er tóm er nýjum tómum lista skilað.</span><span class="sxs-lookup"><span data-stu-id="f3a08-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="f3a08-125">Ef annaðhvort frumbreyta `input` eða `delimiter` er óskilgreind (núll) er gerð undantekning í hugbúnaðinum.</span><span class="sxs-lookup"><span data-stu-id="f3a08-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="f3a08-126">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="f3a08-126">Example 1</span></span>

<span data-ttu-id="f3a08-127">`SPLIT ("abcd", 3)` skilar nýjum lista sem samanstendur af tveimur skrám sem eru með reitinn **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="f3a08-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="f3a08-128">Reiturinn **Gildi** í fyrstu skránni inniheldur textann **"abc"** og reiturinn **Gildi** í annarri skránni inniheldur textann **"d"**.</span><span class="sxs-lookup"><span data-stu-id="f3a08-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f3a08-129">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="f3a08-129">Example 2</span></span>

<span data-ttu-id="f3a08-130">`SPLIT ("XAb aBy", "aB")` skilar nýjum lista sem samanstendur af þremur skrám sem eru með reitinn **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="f3a08-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="f3a08-131">Reiturinn **Gildi** í fyrstu skránni inniheldur textann **"X"**, reiturinn **Gildi** í annarri skránni inniheldur textann **"&nbsp;"**, og reiturinn **Gildi** í þriðju skránni inniheldur textann **"y"**.</span><span class="sxs-lookup"><span data-stu-id="f3a08-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f3a08-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f3a08-132">Additional resources</span></span>

[<span data-ttu-id="f3a08-133">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="f3a08-133">List functions</span></span>](er-functions-category-list.md)

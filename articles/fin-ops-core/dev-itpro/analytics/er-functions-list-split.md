---
title: SPLIT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLIT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853444"
---
# <a name="split-er-function"></a><span data-ttu-id="bf1d3-103">SPLIT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="bf1d3-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf1d3-104">Aðgerðin `SPLIT` skiptir upp tilteknum ílagsstreng í undirstrengi og skilar niðurstöðunni sem nýju *Skráalista*-gildi.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="bf1d3-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="bf1d3-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="bf1d3-106">Þessi málskipan er notuð til að skipta tilgreindum intaksstreng í undirstrengi, sem hvert um sig hefur tilgreinda lengd.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="bf1d3-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="bf1d3-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="bf1d3-108">Þessi málskipan er notuð til að skipta tilgreindum innsláttarstreng í undirstrengi, byggt á tilgreindu skiltákni.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="bf1d3-109">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="bf1d3-109">Arguments</span></span>

<span data-ttu-id="bf1d3-110">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="bf1d3-110">`input`: *String*</span></span>

<span data-ttu-id="bf1d3-111">Textinn sem á að skipta.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-111">The text to split.</span></span>

<span data-ttu-id="bf1d3-112">`length`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="bf1d3-112">`length`: *Integer*</span></span>

<span data-ttu-id="bf1d3-113">Hámarkslengd staks undirstrengs.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="bf1d3-114">`delimiter`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="bf1d3-114">`delimiter`: *String*</span></span>

<span data-ttu-id="bf1d3-115">Afmarkari sem er notaður til að aðgreina undirstrengi.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="bf1d3-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="bf1d3-116">Return values</span></span>

<span data-ttu-id="bf1d3-117">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="bf1d3-117">*Record list*</span></span>

<span data-ttu-id="bf1d3-118">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bf1d3-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="bf1d3-119">Usage notes</span></span>

<span data-ttu-id="bf1d3-120">Skráaskipulag listans sem er skilað samanstendur af reitnum **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="bf1d3-121">Sérhver skrá yfir listann sem er skilað inniheldur myndaða undirstrengi í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="bf1d3-122">Ef frumbreytan `delimiter` er tóm samantendur nýi listinn sem er skilað af einni skrá sem inniheldur reitinn **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="bf1d3-123">Þessi reitur inniheldur innsláttartexta.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-123">This field contains the input text.</span></span>

<span data-ttu-id="bf1d3-124">Ef frumbreytan `input` er tóm er nýjum tómum lista skilað.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="bf1d3-125">Ef annaðhvort frumbreyta `input` eða `delimiter` er óskilgreind (núll) er gerð undantekning í hugbúnaðinum.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="bf1d3-126">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="bf1d3-126">Example 1</span></span>

<span data-ttu-id="bf1d3-127">`SPLIT ("abcd", 3)` skilar nýjum lista sem samanstendur af tveimur skrám sem eru með reitinn **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="bf1d3-128">Reiturinn **Gildi** í fyrstu skránni inniheldur textann **"abc"** og reiturinn **Gildi** í annarri skránni inniheldur textann **"d"**.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bf1d3-129">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="bf1d3-129">Example 2</span></span>

<span data-ttu-id="bf1d3-130">`SPLIT ("XAb aBy", "aB")` skilar nýjum lista sem samanstendur af þremur skrám sem eru með reitinn **Gildi** af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="bf1d3-131">Reiturinn **Gildi** í fyrstu skránni inniheldur textann **"X"**, reiturinn **Gildi** í annarri skránni inniheldur textann **"&nbsp;"**, og reiturinn **Gildi** í þriðju skránni inniheldur textann **"y"**.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="bf1d3-132">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="bf1d3-132">Example 3</span></span>

<span data-ttu-id="bf1d3-133">Hægt er að nota aðgerðina [INDEX](er-functions-list-index.md) til að fá aðgang að einstaka þáttum tiltekins innsláttarstrengs.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="bf1d3-134">Ef slegið er inn gagnaveitunni **MyList** af gerðinni **Reiknaður reitur** og segðin `SPLIT("abc", 1)` er skilgreind fyrir hann, skilar segðin `INDEX(MyList,2).Value` textanum **„b“**.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="bf1d3-135">Dæmi 4</span><span class="sxs-lookup"><span data-stu-id="bf1d3-135">Example 4</span></span>

<span data-ttu-id="bf1d3-136">Aðgerðin [ENUMERATE](er-functions-list-enumerate.md) hjálpar einnig til við að fá aðgang að einstaka þáttum tiltekins innsláttarstrengs.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="bf1d3-137">Ef gagnaveitan **MyList** er slegin inn fyrst af gerðinni **Reiknaður reitur** og segðin `SPLIT("abc", 1)` er skilgreind fyrir hann og svo er slegið inn gagnaveituna **EnumeratedList** af gerðinni **Reiknaður reitur** og segðin `ENUMERATE(MyList)` er skilgreind fyrir hann, skilar segðin `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` textanum **„b“**.</span><span class="sxs-lookup"><span data-stu-id="bf1d3-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf1d3-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bf1d3-138">Additional resources</span></span>

[<span data-ttu-id="bf1d3-139">Listaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="bf1d3-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: TRANSLATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TRANSLATE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746074"
---
# <a name="translate-er-function"></a><span data-ttu-id="985b7-103">TRANSLATE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="985b7-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="985b7-104">Aðgerðin `TRANSLATE` skilar gildinu *Strengur* sem inniheldur niðurstöðu þess að tilgreindum texta í stöfum er skipt út fyrir annað sett af stöfum.</span><span class="sxs-lookup"><span data-stu-id="985b7-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="985b7-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="985b7-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="985b7-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="985b7-106">Arguments</span></span>

<span data-ttu-id="985b7-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="985b7-107">`text`: *String*</span></span>

<span data-ttu-id="985b7-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="985b7-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="985b7-109">`pattern`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="985b7-109">`pattern`: *String*</span></span>

<span data-ttu-id="985b7-110">Textinn sem verður að skipta út.</span><span class="sxs-lookup"><span data-stu-id="985b7-110">The text that must be replaced.</span></span>

<span data-ttu-id="985b7-111">`replacement`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="985b7-111">`replacement`: *String*</span></span>

<span data-ttu-id="985b7-112">Textinn sem á að nota í staðinn.</span><span class="sxs-lookup"><span data-stu-id="985b7-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="985b7-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="985b7-113">Return values</span></span>

<span data-ttu-id="985b7-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="985b7-114">*String*</span></span>

<span data-ttu-id="985b7-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="985b7-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="985b7-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="985b7-116">Usage notes</span></span>

<span data-ttu-id="985b7-117">Aðgerðin `TRANSLATE` kemur í stað eins stafs í einu.</span><span class="sxs-lookup"><span data-stu-id="985b7-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="985b7-118">Aðgerðin skiptir út fyrsta stafnum í frumbreytunni `text` með fyrsta stafnum í frumbreytunni `pattern` og síðan öðrum stafnum og fylgir sama flæði þar til að því er lokið.</span><span class="sxs-lookup"><span data-stu-id="985b7-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="985b7-119">Þegar stafur úr frumbreytunum `text` og `pattern` stemmir er honum skipt út fyrir staf úr frumbreytunni `replacement` sem er staðsett í sömu stöðu og stafurinn úr frumbreytunni `pattern`.</span><span class="sxs-lookup"><span data-stu-id="985b7-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="985b7-120">Ef stafur birtist margoft í frumbreytunni `pattern` er frumbreytuvörpunin `replacement` sem samsvarar fyrsta tilfelli þessa starfs notuð.</span><span class="sxs-lookup"><span data-stu-id="985b7-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="985b7-121">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="985b7-121">Example 1</span></span>

<span data-ttu-id="985b7-122">`TRANSLATE ("abcdef", "cd", "GH")` skiptir út stafnum **„c”** í tilteknum **„abcdef”** texta fyrir stafinn **„G”** í textanum `replacement` vegna eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="985b7-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="985b7-123">Stafurinn **„c”** er sýndur í textanum `pattern` í fyrstu stöðu.</span><span class="sxs-lookup"><span data-stu-id="985b7-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="985b7-124">Fyrsta staða textans `replacement` inniheldur stafinn **„G”**.</span><span class="sxs-lookup"><span data-stu-id="985b7-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="985b7-125">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="985b7-125">Example 2</span></span>

<span data-ttu-id="985b7-126">`TRANSLATE ("abcdef", "ccd", "GH")` skilar **„abGdef”**.</span><span class="sxs-lookup"><span data-stu-id="985b7-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="985b7-127">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="985b7-127">Example 3</span></span>

<span data-ttu-id="985b7-128">`TRANSLATE ("abccba", "abc", "123")` skilar **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="985b7-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="985b7-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="985b7-129">Additional resources</span></span>

[<span data-ttu-id="985b7-130">Textaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="985b7-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
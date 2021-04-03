---
title: NUMERALSTOTEXT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMERALSTEXT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 0dfb36e21259eada97b158cb38b22ae19e0afa07
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562758"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="f2a26-103">NUMERALSTOTEXT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f2a26-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2a26-104">Aðgerðin `NUMERALSTOTEXT` skilar tilteknu tölunni sem *Strengja*-gildi eftir að það hefur verið stafsett (það er, breytt í textastrengi) á tilgreindu tungumáli.</span><span class="sxs-lookup"><span data-stu-id="f2a26-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a26-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f2a26-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="f2a26-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f2a26-106">Arguments</span></span>

<span data-ttu-id="f2a26-107">`number`: *Heiltala* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="f2a26-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="f2a26-108">Tölugildi sem tilgreinir töluna sem verður að stafa.</span><span class="sxs-lookup"><span data-stu-id="f2a26-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="f2a26-109">`language`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f2a26-109">`language`: *String*</span></span>

<span data-ttu-id="f2a26-110">Gildið *Strengur* sem táknar tungumálakóðann.</span><span class="sxs-lookup"><span data-stu-id="f2a26-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="f2a26-111">`currency`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f2a26-111">`currency`: *String*</span></span>

<span data-ttu-id="f2a26-112">Gildið *Strengur* sem táknar gjaldmiðilskóðann.</span><span class="sxs-lookup"><span data-stu-id="f2a26-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="f2a26-113">`print currency name flag`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="f2a26-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="f2a26-114">*Boolean*-gildi sem gefur til kynna hvort gjaldeyrisheiti verði að bæta við stafsetta textann.</span><span class="sxs-lookup"><span data-stu-id="f2a26-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="f2a26-115">`decimal points`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="f2a26-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="f2a26-116">*Heiltölu*-gildi sem gefur til kynna fjölda aukastafa sem stafsettur texti ætti að hafa.</span><span class="sxs-lookup"><span data-stu-id="f2a26-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="f2a26-117">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f2a26-117">Return values</span></span>

<span data-ttu-id="f2a26-118">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f2a26-118">*String*</span></span>

<span data-ttu-id="f2a26-119">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="f2a26-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f2a26-120">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="f2a26-120">Usage notes</span></span>

<span data-ttu-id="f2a26-121">Tungumálakóðinn er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="f2a26-121">The language code is optional.</span></span> <span data-ttu-id="f2a26-122">Ef hann er skilgreindur sem tómur strengur er tungumálakóðinn fyrir samhengið sem er í keyrslu notaður.</span><span class="sxs-lookup"><span data-stu-id="f2a26-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="f2a26-123">Sjálfgefinn tungumálakóði er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="f2a26-124">Tungumálakóðinn fyrir keyrandi samhengi er skilgreindur í þáttunum **möppu** eða **Skrá** í keyrandi sniði rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="f2a26-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="f2a26-125">Gjaldmiðilskóðinn er valkostur.</span><span class="sxs-lookup"><span data-stu-id="f2a26-125">The currency code is optional.</span></span> <span data-ttu-id="f2a26-126">Ef hann er skilgreindur sem tómur strengur er fyrirtækjagjaldmiðillinn fyrir samhengið sem er í keyrslu notaður.</span><span class="sxs-lookup"><span data-stu-id="f2a26-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="f2a26-127">Frumbreyturnar `print currency name flag` og `decimal points` eru aðeins greindar fyrir eftirfarandi tungumálakóða: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** og **RU**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="f2a26-128">Þar að auki er frumbreytan `print currency name flag` aðeins greind fyrir fyrirtæki þar sem samhengi landsins eða svæðisins styður frávik frá gjaldmiðlaheiti.</span><span class="sxs-lookup"><span data-stu-id="f2a26-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="f2a26-129">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="f2a26-129">Example 1</span></span>

<span data-ttu-id="f2a26-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` skilar **"One Thousand Two Hundred Thirty Four and 56"**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f2a26-131">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="f2a26-131">Example 2</span></span>

<span data-ttu-id="f2a26-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` skilar **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="f2a26-133">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="f2a26-133">Example 3</span></span>

<span data-ttu-id="f2a26-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` skilar **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2a26-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f2a26-135">Additional resources</span></span>

[<span data-ttu-id="f2a26-136">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="f2a26-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
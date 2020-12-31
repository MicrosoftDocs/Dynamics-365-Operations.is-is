---
title: DATETIMEFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETIMEFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: d42767b814f36eb75b4a43d07c663b2dd1b2c879
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684955"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="151d4-103">DATETIMEFORMAT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="151d4-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="151d4-104">Aðgerðin `DATETIMEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="151d4-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="151d4-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="151d4-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="151d4-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="151d4-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="151d4-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="151d4-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="151d4-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="151d4-108">Arguments</span></span>

<span data-ttu-id="151d4-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="151d4-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="151d4-110">Dagsetningar-/tímagildi sem táknar dagsetningu og tíma til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="151d4-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="151d4-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="151d4-111">`format`: *String*</span></span>

<span data-ttu-id="151d4-112">Snið úttaksstrengsins.</span><span class="sxs-lookup"><span data-stu-id="151d4-112">The format of the output string.</span></span>

<span data-ttu-id="151d4-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="151d4-113">`culture`: *String*</span></span>

<span data-ttu-id="151d4-114">Menningin sem á að nota til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="151d4-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="151d4-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="151d4-115">Return values</span></span>

<span data-ttu-id="151d4-116">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="151d4-116">*String*</span></span>

<span data-ttu-id="151d4-117">Strenggildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="151d4-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="151d4-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="151d4-118">Usage notes</span></span>

<span data-ttu-id="151d4-119">Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu.</span><span class="sxs-lookup"><span data-stu-id="151d4-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="151d4-120">Til dæmis, ef aðgerðin `DATETIMEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="151d4-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="151d4-121">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="151d4-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="151d4-122">Þegar aðgerðin `DATETIMEFORMAT` breytir tilteknu gildi fyrir dagsetningu/tíma tekur það tillit til tímabeltisstillingar notanda hugbúnaðar sem er að keyra ER-sniðið sem aðgerðin er kölluð í samhengi við.</span><span class="sxs-lookup"><span data-stu-id="151d4-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="151d4-123">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="151d4-123">Example 1</span></span>

<span data-ttu-id="151d4-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` skilar núverandi dagsetningar-/tímagildi hugbúnaðarþjóns, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="151d4-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="151d4-125">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="151d4-125">Example 2</span></span>

<span data-ttu-id="151d4-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` skilar núverandi dagsetningar-/tímagildi setu hugbúnaðar, 24. desember 2015, sem **"24.12.2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="151d4-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="151d4-127">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="151d4-127">Example 3</span></span>

<span data-ttu-id="151d4-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` skilar strenggildinu **2019-11-12T08:00:00.0000000-08:00** þegar það er kallað í ferli sem var hafið af notanda forrits sem hefur tímabeltisgildið **(GMT-08: 00) Kyrrahafstími (BNA og Kanada)** í hlutanum **Val á tungumáli og landi/svæði**.</span><span class="sxs-lookup"><span data-stu-id="151d4-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="151d4-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="151d4-129">Additional resources</span></span>

[<span data-ttu-id="151d4-130">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="151d4-130">Date and time functions</span></span>](er-functions-category-datetime.md)

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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98919f40751a77465ae26acbd46af4396c588b13
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916408"
---
# <span data-ttu-id="392a2-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="392a2-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="392a2-104">Aðgerðin `DATETIMEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="392a2-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="392a2-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="392a2-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="392a2-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="392a2-106">Syntax 1</span></span>

```
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="392a2-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="392a2-107">Syntax 2</span></span>

```
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="392a2-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="392a2-108">Arguments</span></span>

<span data-ttu-id="392a2-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="392a2-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="392a2-110">Dagsetningar-/tímagildi sem táknar dagsetningu og tíma til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="392a2-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="392a2-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="392a2-111">`format`: *String*</span></span>

<span data-ttu-id="392a2-112">Snið úttaksstrengsins.</span><span class="sxs-lookup"><span data-stu-id="392a2-112">The format of the output string.</span></span>

<span data-ttu-id="392a2-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="392a2-113">`culture`: *String*</span></span>

<span data-ttu-id="392a2-114">Menningin sem á að nota til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="392a2-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="392a2-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="392a2-115">Return values</span></span>

<span data-ttu-id="392a2-116">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="392a2-116">*String*</span></span>

<span data-ttu-id="392a2-117">Strenggildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="392a2-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="392a2-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="392a2-118">Usage notes</span></span>

<span data-ttu-id="392a2-119">Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu.</span><span class="sxs-lookup"><span data-stu-id="392a2-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="392a2-120">Til dæmis, ef aðgerðin `DATETIMEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="392a2-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="392a2-121">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="392a2-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="392a2-122">Þegar aðgerðin `DATETIMEFORMAT` breytir tilteknu gildi fyrir dagsetningu/tíma tekur það tillit til tímabeltisstillingar notanda hugbúnaðar sem er að keyra ER-sniðið sem aðgerðin er kölluð í samhengi við.</span><span class="sxs-lookup"><span data-stu-id="392a2-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="392a2-123">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="392a2-123">Example 1</span></span>

<span data-ttu-id="392a2-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` skilar núverandi dagsetningar-/tímagildi hugbúnaðarþjóns, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="392a2-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="392a2-125">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="392a2-125">Example 2</span></span>

<span data-ttu-id="392a2-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` skilar núverandi dagsetningar-/tímagildi setu hugbúnaðar, 24. desember 2015, sem **"24.12.2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="392a2-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="392a2-127">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="392a2-127">Example 3</span></span>

<span data-ttu-id="392a2-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` skilar strenggildinu **2019-11-12T08:00:00.0000000-08:00** þegar það er kallað í ferli sem var hafið af notanda forrits sem hefur tímabeltisgildið **(GMT-08: 00) Kyrrahafstími (BNA og Kanada)** í hlutanum **Val á tungumáli og landi/svæði**.</span><span class="sxs-lookup"><span data-stu-id="392a2-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="392a2-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="392a2-129">Additional resources</span></span>

[<span data-ttu-id="392a2-130">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="392a2-130">Date and time functions</span></span>](er-functions-category-datetime.md)

---
title: DATETIMEFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETIMEFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891258"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="356ab-103">DATETIMEFORMAT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="356ab-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="356ab-104">Aðgerðin `DATETIMEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="356ab-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="356ab-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="356ab-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="356ab-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="356ab-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="356ab-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="356ab-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="356ab-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="356ab-108">Arguments</span></span>

<span data-ttu-id="356ab-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="356ab-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="356ab-110">Dagsetningar-/tímagildi sem táknar dagsetningu og tíma til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="356ab-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="356ab-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="356ab-111">`format`: *String*</span></span>

<span data-ttu-id="356ab-112">Snið úttaksstrengsins.</span><span class="sxs-lookup"><span data-stu-id="356ab-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="356ab-113">Sniðstrengurinn tekur tillit til há- og lágstafa þegar notað er annaðhvort staðlað snið eða sérstillt snið.</span><span class="sxs-lookup"><span data-stu-id="356ab-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="356ab-114">Til dæmis skilar [staðlaða](/dotnet/standard/base-types/standard-date-and-time-format-strings) „d“-sniðsákvörðunin dagsetningunni með því að nota stutt dagsetningarsnið á meðan staðlaða „D“-sniðsákvörðunin skilar dagsetningunni með því að nota langt dagsetningarsnið.</span><span class="sxs-lookup"><span data-stu-id="356ab-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="356ab-115">Auk þess skilar [sérstillt](/dotnet/standard/base-types/custom-date-and-time-format-strings) „M“-sniðsákvörðun mánuðinum frá 1 til 12 á meðan sérstillt „m“-sniðsákvörðun skilar mínútu frá 0 til 59.</span><span class="sxs-lookup"><span data-stu-id="356ab-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="356ab-116">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="356ab-116">`culture`: *String*</span></span>

<span data-ttu-id="356ab-117">Menningin sem á að nota til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="356ab-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="356ab-118">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="356ab-118">Return values</span></span>

<span data-ttu-id="356ab-119">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="356ab-119">*String*</span></span>

<span data-ttu-id="356ab-120">Strenggildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="356ab-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="356ab-121">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="356ab-121">Usage notes</span></span>

<span data-ttu-id="356ab-122">Ef menningin er ekki skilgreind sem frumbreyta fyrir kallaða aðgerð er gildi `culture` skilgreint af samhengi köllunar.</span><span class="sxs-lookup"><span data-stu-id="356ab-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="356ab-123">Til dæmis, ef aðgerðin `DATETIMEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="356ab-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="356ab-124">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="356ab-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="356ab-125">Þegar aðgerðin `DATETIMEFORMAT` breytir tilteknu gildi fyrir dagsetningu/tíma tekur það tillit til tímabeltisstillingar notanda hugbúnaðar sem er að keyra ER-sniðið sem aðgerðin er kölluð í samhengi við.</span><span class="sxs-lookup"><span data-stu-id="356ab-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="356ab-126">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="356ab-126">Example 1</span></span>

<span data-ttu-id="356ab-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` skilar núverandi dagsetningar-/tímagildi hugbúnaðarþjóns, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="356ab-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="356ab-128">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="356ab-128">Example 2</span></span>

<span data-ttu-id="356ab-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` skilar núverandi dagsetningar-/tímagildi setu hugbúnaðar, 24. desember 2015, sem **"24.12.2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="356ab-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="356ab-130">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="356ab-130">Example 3</span></span>

<span data-ttu-id="356ab-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` skilar strengjagildinu **2019-11-12T08:00:00.0000000-08:00** þegar kallað er á aðgerðina í ferli sem var sett af stað af notanda forrits sem er með tímabeltið **(GMT-08:00) Kyrrahafstími (Bandaríkin og Kanada)** í hlutanum **Kjörstillingar tungumáls og lands/svæðis**.</span><span class="sxs-lookup"><span data-stu-id="356ab-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="356ab-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="356ab-132">Additional resources</span></span>

[<span data-ttu-id="356ab-133">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="356ab-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
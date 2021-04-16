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
ms.openlocfilehash: 859753c04e3b3d3b61d9a61edaf396637ed5a003
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746988"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="ba557-103">DATETIMEFORMAT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="ba557-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba557-104">Aðgerðin `DATETIMEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="ba557-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ba557-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ba557-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ba557-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="ba557-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ba557-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="ba557-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ba557-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="ba557-108">Arguments</span></span>

<span data-ttu-id="ba557-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="ba557-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="ba557-110">Dagsetningar-/tímagildi sem táknar dagsetningu og tíma til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="ba557-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="ba557-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ba557-111">`format`: *String*</span></span>

<span data-ttu-id="ba557-112">Snið úttaksstrengsins.</span><span class="sxs-lookup"><span data-stu-id="ba557-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="ba557-113">Sniðstrengurinn tekur tillit til há- og lágstafa þegar notað er annaðhvort staðlað snið eða sérstillt snið.</span><span class="sxs-lookup"><span data-stu-id="ba557-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="ba557-114">Til dæmis skilar [staðlaða](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) „d“-sniðsákvörðunin dagsetningunni með því að nota stutt dagsetningarsnið á meðan staðlaða „D“-sniðsákvörðunin skilar dagsetningunni með því að nota langt dagsetningarsnið.</span><span class="sxs-lookup"><span data-stu-id="ba557-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="ba557-115">Auk þess skilar [sérstillt](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) „M“-sniðsákvörðun mánuðinum frá 1 til 12 á meðan sérstillt „m“-sniðsákvörðun skilar mínútu frá 0 til 59.</span><span class="sxs-lookup"><span data-stu-id="ba557-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="ba557-116">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ba557-116">`culture`: *String*</span></span>

<span data-ttu-id="ba557-117">Menningin sem á að nota til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="ba557-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba557-118">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ba557-118">Return values</span></span>

<span data-ttu-id="ba557-119">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ba557-119">*String*</span></span>

<span data-ttu-id="ba557-120">Strenggildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="ba557-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ba557-121">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="ba557-121">Usage notes</span></span>

<span data-ttu-id="ba557-122">Ef menningin er ekki skilgreind sem frumbreyta fyrir kallaða aðgerð er gildi `culture` skilgreint af samhengi köllunar.</span><span class="sxs-lookup"><span data-stu-id="ba557-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ba557-123">Til dæmis, ef aðgerðin `DATETIMEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="ba557-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ba557-124">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ba557-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="ba557-125">Þegar aðgerðin `DATETIMEFORMAT` breytir tilteknu gildi fyrir dagsetningu/tíma tekur það tillit til tímabeltisstillingar notanda hugbúnaðar sem er að keyra ER-sniðið sem aðgerðin er kölluð í samhengi við.</span><span class="sxs-lookup"><span data-stu-id="ba557-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="ba557-126">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="ba557-126">Example 1</span></span>

<span data-ttu-id="ba557-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` skilar núverandi dagsetningar-/tímagildi hugbúnaðarþjóns, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="ba557-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ba557-128">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="ba557-128">Example 2</span></span>

<span data-ttu-id="ba557-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` skilar núverandi dagsetningar-/tímagildi setu hugbúnaðar, 24. desember 2015, sem **"24.12.2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="ba557-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="ba557-130">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="ba557-130">Example 3</span></span>

<span data-ttu-id="ba557-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` skilar strengjagildinu **2019-11-12T08:00:00.0000000-08:00** þegar kallað er á aðgerðina í ferli sem var sett af stað af notanda forrits sem er með tímabeltið **(GMT-08:00) Kyrrahafstími (Bandaríkin og Kanada)** í hlutanum **Kjörstillingar tungumáls og lands/svæðis**.</span><span class="sxs-lookup"><span data-stu-id="ba557-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba557-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ba557-132">Additional resources</span></span>

[<span data-ttu-id="ba557-133">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="ba557-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
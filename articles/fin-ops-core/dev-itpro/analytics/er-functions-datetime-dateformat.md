---
title: DATEFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATEFORMAT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684933"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="e1cc3-103">DATEFORMAT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="e1cc3-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1cc3-104">Aðgerðin `DATEFORMAT` skilar *String*-gildi sem setur fram tiltekið dagsetningargildi sem texta á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="e1cc3-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="e1cc3-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="e1cc3-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e1cc3-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="e1cc3-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="e1cc3-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="e1cc3-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="e1cc3-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="e1cc3-108">Arguments</span></span>

<span data-ttu-id="e1cc3-109">`date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="e1cc3-109">`date`: *Date*</span></span>

<span data-ttu-id="e1cc3-110">Dagsetningargildi sem táknar dagsetningu til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="e1cc3-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e1cc3-111">`format`: *String*</span></span>

<span data-ttu-id="e1cc3-112">Snið úttaksstrengsins.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-112">The format of the output string.</span></span>

<span data-ttu-id="e1cc3-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e1cc3-113">`culture`: *String*</span></span>

<span data-ttu-id="e1cc3-114">Menningin sem á að nota til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="e1cc3-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="e1cc3-115">Return values</span></span>

<span data-ttu-id="e1cc3-116">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="e1cc3-116">*String*</span></span>

<span data-ttu-id="e1cc3-117">Strenggildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e1cc3-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="e1cc3-118">Usage notes</span></span>

<span data-ttu-id="e1cc3-119">Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="e1cc3-120">Til dæmis, ef aðgerðin `DATEFORMAT` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="e1cc3-121">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="e1cc3-122">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="e1cc3-122">Example 1</span></span>

<span data-ttu-id="e1cc3-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` skilar núverandi dagsetningargildi hugbúnaðarþjóns, 24. desember, 2015, sem strenginn **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="e1cc3-124">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="e1cc3-124">Example 2</span></span>

<span data-ttu-id="e1cc3-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="e1cc3-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1cc3-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e1cc3-126">Additional resources</span></span>

[<span data-ttu-id="e1cc3-127">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="e1cc3-127">Date and time functions</span></span>](er-functions-category-datetime.md)

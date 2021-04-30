---
title: DATETIMEVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETIMEVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891282"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="786c8-103">DATETIMEVALUE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="786c8-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="786c8-104">Aðgerðin `DATETIMEVALUE` skilar *DateTime*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) í dagsetningar-/tímagildi.</span><span class="sxs-lookup"><span data-stu-id="786c8-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="786c8-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="786c8-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="786c8-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="786c8-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="786c8-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="786c8-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="786c8-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="786c8-108">Arguments</span></span>

<span data-ttu-id="786c8-109">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="786c8-109">`text`: *String*</span></span>

<span data-ttu-id="786c8-110">Texti sem táknar gildið til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="786c8-110">Text that represents the value to format.</span></span>

<span data-ttu-id="786c8-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="786c8-111">`format`: *String*</span></span>

<span data-ttu-id="786c8-112">Snið gefins texta.</span><span class="sxs-lookup"><span data-stu-id="786c8-112">The format of the given text.</span></span>

<span data-ttu-id="786c8-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="786c8-113">`culture`: *String*</span></span>

<span data-ttu-id="786c8-114">Menningin sem er notuð til að forsníða gefinn texta.</span><span class="sxs-lookup"><span data-stu-id="786c8-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="786c8-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="786c8-115">Return values</span></span>

<span data-ttu-id="786c8-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="786c8-116">*DateTime*</span></span>

<span data-ttu-id="786c8-117">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="786c8-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="786c8-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="786c8-118">Usage notes</span></span>

<span data-ttu-id="786c8-119">Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu.</span><span class="sxs-lookup"><span data-stu-id="786c8-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="786c8-120">Til dæmis, ef aðgerðin `DATETIMEVALUE` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="786c8-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="786c8-121">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="786c8-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="786c8-122">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="786c8-122">Example 1</span></span>

<span data-ttu-id="786c8-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` skilar **02:55 þann 21. desember, 2016**, byggt á tilteknu sérsniðnu sniði og sjálfgefninni menningu **EN-BNA** fyrir hugbúnaðinn.</span><span class="sxs-lookup"><span data-stu-id="786c8-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="786c8-124">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="786c8-124">Example 2</span></span>

<span data-ttu-id="786c8-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` skilar **02:55 þann 21. desember, 2016**, byggt á tilgreindu sérsniðnu sniði og menningu.</span><span class="sxs-lookup"><span data-stu-id="786c8-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="786c8-126">Hins vegar beitir `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` undantekningu til að upplýsa notandann um að tilgreindur strengur sé ekki viðurkenndur sem gild dagsetning.</span><span class="sxs-lookup"><span data-stu-id="786c8-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="786c8-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="786c8-127">Additional resources</span></span>

[<span data-ttu-id="786c8-128">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="786c8-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
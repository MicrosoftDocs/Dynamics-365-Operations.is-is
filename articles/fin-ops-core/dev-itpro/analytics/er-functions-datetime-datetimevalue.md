---
title: DATETIMEVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETIMEVALUE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: de601ad08b85797a4241ef74ecb3eba37eda37ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917535"
---
# <span data-ttu-id="68e3c-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="68e3c-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68e3c-104">Aðgerðin `DATETIMEVALUE` skilar *DateTime*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) í dagsetningar-/tímagildi.</span><span class="sxs-lookup"><span data-stu-id="68e3c-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="68e3c-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="68e3c-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="68e3c-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="68e3c-106">Syntax 1</span></span>

```
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="68e3c-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="68e3c-107">Syntax 2</span></span>

```
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="68e3c-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="68e3c-108">Arguments</span></span>

<span data-ttu-id="68e3c-109">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="68e3c-109">`text`: *String*</span></span>

<span data-ttu-id="68e3c-110">Texti sem táknar gildið til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="68e3c-110">Text that represents the value to format.</span></span>

<span data-ttu-id="68e3c-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="68e3c-111">`format`: *String*</span></span>

<span data-ttu-id="68e3c-112">Snið gefins texta.</span><span class="sxs-lookup"><span data-stu-id="68e3c-112">The format of the given text.</span></span>

<span data-ttu-id="68e3c-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="68e3c-113">`culture`: *String*</span></span>

<span data-ttu-id="68e3c-114">Menningin sem er notuð til að forsníða gefinn texta.</span><span class="sxs-lookup"><span data-stu-id="68e3c-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="68e3c-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="68e3c-115">Return values</span></span>

<span data-ttu-id="68e3c-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="68e3c-116">*DateTime*</span></span>

<span data-ttu-id="68e3c-117">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="68e3c-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="68e3c-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="68e3c-118">Usage notes</span></span>

<span data-ttu-id="68e3c-119">Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu.</span><span class="sxs-lookup"><span data-stu-id="68e3c-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="68e3c-120">Til dæmis, ef aðgerðin `DATETIMEVALUE` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="68e3c-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="68e3c-121">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="68e3c-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="68e3c-122">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="68e3c-122">Example 1</span></span>

<span data-ttu-id="68e3c-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` skilar **02:55 þann 21. desember, 2016**, byggt á tilteknu sérsniðnu sniði og sjálfgefninni menningu **EN-BNA** fyrir hugbúnaðinn.</span><span class="sxs-lookup"><span data-stu-id="68e3c-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="68e3c-124">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="68e3c-124">Example 2</span></span>

<span data-ttu-id="68e3c-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` skilar **02:55 þann 21. desember, 2016**, byggt á tilgreindu sérsniðnu sniði og menningu.</span><span class="sxs-lookup"><span data-stu-id="68e3c-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="68e3c-126">Hins vegar beitir `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` undantekningu til að upplýsa notandann um að tilgreindur strengur sé ekki viðurkenndur sem gild dagsetning.</span><span class="sxs-lookup"><span data-stu-id="68e3c-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68e3c-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="68e3c-127">Additional resources</span></span>

[<span data-ttu-id="68e3c-128">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="68e3c-128">Date and time functions</span></span>](er-functions-category-datetime.md)

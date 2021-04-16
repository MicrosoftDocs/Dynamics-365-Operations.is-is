---
title: DATEVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATEVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746940"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="d0786-103">DATEVALUE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="d0786-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0786-104">Aðgerðin `DATEVALUE` skilar *Date*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) í dagsetningargildi.</span><span class="sxs-lookup"><span data-stu-id="d0786-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="d0786-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="d0786-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d0786-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="d0786-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d0786-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="d0786-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d0786-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="d0786-108">Arguments</span></span>

<span data-ttu-id="d0786-109">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="d0786-109">`text`: *String*</span></span>

<span data-ttu-id="d0786-110">Texti sem táknar gildið til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="d0786-110">Text that represents the value to format.</span></span>

<span data-ttu-id="d0786-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="d0786-111">`format`: *String*</span></span>

<span data-ttu-id="d0786-112">Snið gefins texta.</span><span class="sxs-lookup"><span data-stu-id="d0786-112">The format of the given text.</span></span>

<span data-ttu-id="d0786-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="d0786-113">`culture`: *String*</span></span>

<span data-ttu-id="d0786-114">Menningin sem er notuð til að forsníða gefinn texta.</span><span class="sxs-lookup"><span data-stu-id="d0786-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0786-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d0786-115">Return values</span></span>

<span data-ttu-id="d0786-116">*Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="d0786-116">*Date*</span></span>

<span data-ttu-id="d0786-117">Dagsetningargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="d0786-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d0786-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="d0786-118">Usage notes</span></span>

<span data-ttu-id="d0786-119">Þegar menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar er gildið `culture` skilgreint af köllunarsamhenginu.</span><span class="sxs-lookup"><span data-stu-id="d0786-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="d0786-120">Til dæmis, ef aðgerðin `DATEVALUE` er kölluð með því að nota málskipan 1 á rafrænni skýrslugerð (ER) sniði fyrir **FILE**-þáttinn sem er stillt til að nota þýska menningu verður umbreytingin gerð með því að nota þýska menninguna.</span><span class="sxs-lookup"><span data-stu-id="d0786-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="d0786-121">Sjálfgefið gildi `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d0786-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="d0786-122">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="d0786-122">Example 1</span></span>

<span data-ttu-id="d0786-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` skilar dagsetnigargildinu **21. desember, 2016**, byggt á tilteknu sérsniðnu sniði og sjálfgefninni menningu **EN-BNA** fyrir hugbúnaðinn.</span><span class="sxs-lookup"><span data-stu-id="d0786-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="d0786-124">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="d0786-124">Example 2</span></span>

<span data-ttu-id="d0786-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` skilar dagsetningargildinu **21. janúar, 2016**, byggt á tilgreindu sérsniðnu sniði og menningu.</span><span class="sxs-lookup"><span data-stu-id="d0786-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="d0786-126">Hins vegar beitir `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` undantekningu til að upplýsa notandann um að tilgreindur strengur sé ekki viðurkenndur sem gild dagsetning fyrir tilgreinda menningu.</span><span class="sxs-lookup"><span data-stu-id="d0786-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0786-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d0786-127">Additional resources</span></span>

[<span data-ttu-id="d0786-128">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="d0786-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
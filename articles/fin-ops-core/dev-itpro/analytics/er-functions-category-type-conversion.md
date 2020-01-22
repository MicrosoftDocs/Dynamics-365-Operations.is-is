---
title: Listi yfir ER-aðgerðir í gerðaumbreytingaflokknum
description: Þetta efni veitir upplýsingar um umreikningsaðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2cfa5deb3b2c00565759e4334a002bf112f888ac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917650"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="4bba7-103">Listi yfir ER-aðgerðir í gerðaumbreytingaflokknum</span><span class="sxs-lookup"><span data-stu-id="4bba7-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bba7-104">Hægt er að nota umbreytingaraðgerðir fyrir rafræna skýrslugerð (ER) til að umbreyta gildi milli gerða.</span><span class="sxs-lookup"><span data-stu-id="4bba7-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="4bba7-105">Þetta efni gefur yfirlit yfir þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="4bba7-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="4bba7-106">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-106">Type conversion functions</span></span>

| <span data-ttu-id="4bba7-107">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-107">Function</span></span> | <span data-ttu-id="4bba7-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4bba7-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4bba7-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="4bba7-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="4bba7-110">Þessi aðgerð skilar *Int64*-gildi sem táknar tilgreindan streng.</span><span class="sxs-lookup"><span data-stu-id="4bba7-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="4bba7-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="4bba7-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="4bba7-112">Þessi aðgerð skilar *Int*-gildi sem táknar tilgreindan streng.</span><span class="sxs-lookup"><span data-stu-id="4bba7-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="4bba7-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="4bba7-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="4bba7-114">Þessi aðgerð skilar *Raun*-gildi sem er umreiknað úr tilgreindu *Streng*-gildi.</span><span class="sxs-lookup"><span data-stu-id="4bba7-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="4bba7-115">Við umreikning er tekið tillit til tilgreindra flokkunarskiltákna aukastafa og tölustafa.</span><span class="sxs-lookup"><span data-stu-id="4bba7-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="4bba7-116">Virði</span><span class="sxs-lookup"><span data-stu-id="4bba7-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="4bba7-117">Þessi aðgerð skilar *Raun*-gildi sem er umreiknað úr tilgreindu *Streng*-gildi.</span><span class="sxs-lookup"><span data-stu-id="4bba7-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="4bba7-118">Umreikningsaðgerðir gerðar í flokknum Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="4bba7-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="4bba7-119">Eftirfarandi tafla lýsir umreikningsaðgerðum gerða í [dagsetningar- og tímaflokknum](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="4bba7-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="4bba7-120">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-120">Function</span></span> | <span data-ttu-id="4bba7-121">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4bba7-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4bba7-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="4bba7-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="4bba7-123">Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu *strengja*-gildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningar-/tímagildi.</span><span class="sxs-lookup"><span data-stu-id="4bba7-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="4bba7-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="4bba7-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="4bba7-125">Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu *dagsetningar*-gildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="4bba7-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="4bba7-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="4bba7-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="4bba7-127">Þessi aðgerð skilar *Date*-gildi sem er umreiknað úr gefnu *strengja*-gildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningargildi.</span><span class="sxs-lookup"><span data-stu-id="4bba7-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="4bba7-128">Umreikningsaðgerðir gerðar í listaflokknum</span><span class="sxs-lookup"><span data-stu-id="4bba7-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="4bba7-129">Eftirfarandi tafla lýsir umreikningsaðgerðum gerða í [listaflokknum](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="4bba7-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="4bba7-130">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-130">Function</span></span> | <span data-ttu-id="4bba7-131">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4bba7-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4bba7-132">Listi</span><span class="sxs-lookup"><span data-stu-id="4bba7-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="4bba7-133">Þessi aðgerð skilar *Skráalista*-gildi sem nýjum lista sem er stofnaður úr tilgreindum frumbreytum af gerðinni *Ílát (skrá)*.</span><span class="sxs-lookup"><span data-stu-id="4bba7-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="4bba7-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="4bba7-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="4bba7-135">Þessi aðgerð skilar *Skráalista*-gildi sem er stofnað byggt á skipulagi gefinnar frumbreytu af gerðinni *Upptalning* eða *Ílát (skrá)*.</span><span class="sxs-lookup"><span data-stu-id="4bba7-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="4bba7-136">Skipta</span><span class="sxs-lookup"><span data-stu-id="4bba7-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="4bba7-137">Þessi aðgerð skiptir upp tilteknu *strengjagildi* í undirstrengi og skilar niðurstöðunni sem nýju *Skráalista*-gildi.</span><span class="sxs-lookup"><span data-stu-id="4bba7-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="4bba7-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="4bba7-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="4bba7-139">Þessi aðgerð skilar *strengjagildi* sem samanstendur af samsettum gildum tiltekins svæðis úr tilgreindu gildi *skráalista*.</span><span class="sxs-lookup"><span data-stu-id="4bba7-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="4bba7-140">Hægt er að aðskilja gildin með tilgreindri afmörkun.</span><span class="sxs-lookup"><span data-stu-id="4bba7-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="4bba7-141">Umreikningsaðgerðir gerðar í textaflokknum</span><span class="sxs-lookup"><span data-stu-id="4bba7-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="4bba7-142">Eftirfarandi tafla lýsir umreikningsaðgerðum gerða í [textaflokknum](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="4bba7-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="4bba7-143">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-143">Function</span></span> | <span data-ttu-id="4bba7-144">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4bba7-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4bba7-145">Char</span><span class="sxs-lookup"><span data-stu-id="4bba7-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="4bba7-146">Þessi aðgerð skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu.</span><span class="sxs-lookup"><span data-stu-id="4bba7-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="4bba7-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="4bba7-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="4bba7-148">Þessi aðgerð umreiknar tilgreint inntak af gerðinni *Strengur* í gagnaatriði af gerðinni *GUID*.</span><span class="sxs-lookup"><span data-stu-id="4bba7-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="4bba7-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="4bba7-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="4bba7-150">Þessi aðgerð skilar *String*-gildi sem setur fram tilgreinda tölu á tilgreindu sniði og í valinni tiltekinni menningu.</span><span class="sxs-lookup"><span data-stu-id="4bba7-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="4bba7-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="4bba7-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="4bba7-152">Þessi aðgerð skilar *Íláts*-gildi sem sýnir Quick Response Code (QR-kóða) myndar fyrir tiltekinn streng á tvíundarsniði.</span><span class="sxs-lookup"><span data-stu-id="4bba7-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="4bba7-153">Texti</span><span class="sxs-lookup"><span data-stu-id="4bba7-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="4bba7-154">Þessi aðgerð skilar tilgreindri tölu sem *strengjagildi* sem sýnir tilgreinda tölu eftir að hún hefur verið umreiknuð í textastreng sem er sniðinn í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki forrits.</span><span class="sxs-lookup"><span data-stu-id="4bba7-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4bba7-155">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4bba7-155">Additional resources</span></span>

[<span data-ttu-id="4bba7-156">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4bba7-157">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4bba7-158">Formúlutungumál í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="4bba7-158">Electronic reporting formula language</span></span>](er-formula-language.md)

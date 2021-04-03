---
title: Listi yfir ER-aðgerðir í flokknum Dagsetning og tími
description: Þetta efni veitir upplýsingar um aðgerðir dagsetningar og tíma sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 52b84f9b611f703fd390eca58c1364a4992bece2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561711"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="39fca-103">Listi yfir ER-aðgerðir í flokknum Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="39fca-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39fca-104">Hægt er að nota dagsetningar- og tímaaðgerðir rafrænnar skýrslugerðar (ER) til að ná upplýsingum úr dagsetningar- og tímagildum og framkvæma aðgerðir á þeim.</span><span class="sxs-lookup"><span data-stu-id="39fca-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="39fca-105">Þetta efni gefur yfirlit yfir þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="39fca-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="39fca-106">Listi yfir studdar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="39fca-106">List of supported functions</span></span>

| <span data-ttu-id="39fca-107">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="39fca-107">Function</span></span> | <span data-ttu-id="39fca-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="39fca-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="39fca-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="39fca-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="39fca-110">Þessi aðgerð skilar *DateTime*-gildi sem er tilgreindur fjöldi daga fyrir eða eftir tiltekinn upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="39fca-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="39fca-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="39fca-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="39fca-112">Þessi aðgerð skilar *String*-gildi sem setur fram tiltekið dagsetningargildi sem texta á tilteknu sniði og í valinni tiltekinni menningu.</span><span class="sxs-lookup"><span data-stu-id="39fca-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="39fca-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="39fca-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="39fca-114">Þessi aðgerð skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni menningu.</span><span class="sxs-lookup"><span data-stu-id="39fca-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="39fca-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="39fca-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="39fca-116">Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningar-/tímagildi.</span><span class="sxs-lookup"><span data-stu-id="39fca-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="39fca-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="39fca-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="39fca-118">Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu dagsetningargildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="39fca-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="39fca-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="39fca-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="39fca-120">Þessi aðgerð skilar *Date*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningargildi.</span><span class="sxs-lookup"><span data-stu-id="39fca-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="39fca-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="39fca-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="39fca-122">Þessi aðgerð skilar *heiltölu*-gildi sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="39fca-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="39fca-123">Dagar</span><span class="sxs-lookup"><span data-stu-id="39fca-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="39fca-124">Þessi aðgerð skilar *heiltölu*-gildi sem sýnir fjölda daga milli einnar tilgreindrar dagsetningar og annarrar tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="39fca-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="39fca-125">Now</span><span class="sxs-lookup"><span data-stu-id="39fca-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="39fca-126">Þessi aðgerð skilar *DateTime*-gildi sem táknar dagsetningu og tíma núverandi netþjóns hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="39fca-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="39fca-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="39fca-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="39fca-128">Þessi aðgerð skilar *Dagsetningar*-gildi sem táknar **núll** dagsetningu (1. janúar, 1900).</span><span class="sxs-lookup"><span data-stu-id="39fca-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="39fca-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="39fca-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="39fca-130">Þessi aðgerð skilar *DateTime*-gildi sem táknar **núll** dagsetningar-/tímagildi (1. janúar, 1900) í samræmdum alþjóðlegum tíma.</span><span class="sxs-lookup"><span data-stu-id="39fca-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="39fca-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="39fca-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="39fca-132">Þessi aðgerð skilar *DateTime*-gildi sem táknar setudagsetningu og -tíma núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="39fca-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="39fca-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="39fca-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="39fca-134">Þessi aðgerð skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="39fca-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="39fca-135">Í dag</span><span class="sxs-lookup"><span data-stu-id="39fca-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="39fca-136">Þessi aðgerð skilar *Date*-gildi sem táknar netþjónsdagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="39fca-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="39fca-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="39fca-137">Additional resources</span></span>

[<span data-ttu-id="39fca-138">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="39fca-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="39fca-139">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="39fca-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="39fca-140">Formúlutungumál í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="39fca-140">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
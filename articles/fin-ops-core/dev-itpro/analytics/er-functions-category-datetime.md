---
title: Listi yfir ER-aðgerðir í flokknum Dagsetning og tími
description: Þetta efni veitir upplýsingar um aðgerðir dagsetningar og tíma sem eru studdar í rafrænni skýrslugerð (ER).
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916569"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="bdd7f-103">Listi yfir ER-aðgerðir í flokknum Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="bdd7f-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdd7f-104">Hægt er að nota dagsetningar- og tímaaðgerðir rafrænnar skýrslugerðar (ER) til að ná upplýsingum úr dagsetningar- og tímagildum og framkvæma aðgerðir á þeim.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="bdd7f-105">Þetta efni gefur yfirlit yfir þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="bdd7f-106">Listi yfir studdar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="bdd7f-106">List of supported functions</span></span>

| <span data-ttu-id="bdd7f-107">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="bdd7f-107">Function</span></span> | <span data-ttu-id="bdd7f-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="bdd7f-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="bdd7f-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="bdd7f-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="bdd7f-110">Þessi aðgerð skilar *DateTime*-gildi sem er tilgreindur fjöldi daga fyrir eða eftir tiltekinn upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="bdd7f-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="bdd7f-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="bdd7f-112">Þessi aðgerð skilar *String*-gildi sem setur fram tiltekið dagsetningargildi sem texta á tilteknu sniði og í valinni tiltekinni menningu.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="bdd7f-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bdd7f-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="bdd7f-114">Þessi aðgerð skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni menningu.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="bdd7f-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="bdd7f-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="bdd7f-116">Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningar-/tímagildi.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="bdd7f-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="bdd7f-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="bdd7f-118">Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu dagsetningargildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="bdd7f-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="bdd7f-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="bdd7f-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="bdd7f-120">Þessi aðgerð skilar *Date*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningargildi.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="bdd7f-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="bdd7f-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="bdd7f-122">Þessi aðgerð skilar *heiltölu*-gildi sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="bdd7f-123">Dagar</span><span class="sxs-lookup"><span data-stu-id="bdd7f-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="bdd7f-124">Þessi aðgerð skilar *heiltölu*-gildi sem sýnir fjölda daga milli einnar tilgreindrar dagsetningar og annarrar tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="bdd7f-125">Now</span><span class="sxs-lookup"><span data-stu-id="bdd7f-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="bdd7f-126">Þessi aðgerð skilar *DateTime*-gildi sem táknar dagsetningu og tíma núverandi netþjóns hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="bdd7f-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="bdd7f-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="bdd7f-128">Þessi aðgerð skilar *Dagsetningar*-gildi sem táknar **núll** dagsetningu (1. janúar, 1900).</span><span class="sxs-lookup"><span data-stu-id="bdd7f-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="bdd7f-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="bdd7f-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="bdd7f-130">Þessi aðgerð skilar *DateTime*-gildi sem táknar **núll** dagsetningar-/tímagildi (1. janúar, 1900) í samræmdum alþjóðlegum tíma.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="bdd7f-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="bdd7f-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="bdd7f-132">Þessi aðgerð skilar *DateTime*-gildi sem táknar setudagsetningu og -tíma núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="bdd7f-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="bdd7f-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="bdd7f-134">Þessi aðgerð skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="bdd7f-135">Í dag</span><span class="sxs-lookup"><span data-stu-id="bdd7f-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="bdd7f-136">Þessi aðgerð skilar *Date*-gildi sem táknar netþjónsdagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="bdd7f-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bdd7f-137">Additional resources</span></span>

[<span data-ttu-id="bdd7f-138">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="bdd7f-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="bdd7f-139">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="bdd7f-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="bdd7f-140">Formúlutungumál í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="bdd7f-140">Electronic reporting formula language</span></span>](er-formula-language.md)

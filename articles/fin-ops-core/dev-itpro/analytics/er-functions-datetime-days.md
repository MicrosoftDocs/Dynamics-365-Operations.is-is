---
title: DAYS ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DAYS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47d992d061f8664a55332024ee5c6cd41e4bc495
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743568"
---
# <a name="days-er-function"></a><span data-ttu-id="cb9de-103">DAYS ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="cb9de-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb9de-104">Aðgerðin `DAYS` skilar *heiltölu*-gildi sem sýnir fjölda daga milli einnar tilgreindrar dagsetningar og annarrar tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="cb9de-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9de-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="cb9de-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="cb9de-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="cb9de-106">Arguments</span></span>

<span data-ttu-id="cb9de-107">`date 1`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="cb9de-107">`date 1`: *Date*</span></span>

<span data-ttu-id="cb9de-108">Dagsetningargildi sem táknar upphafsdagsetninguna fyrir útreikning á fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="cb9de-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="cb9de-109">`date 2`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="cb9de-109">`date 2`: *Date*</span></span>

<span data-ttu-id="cb9de-110">Dagsetningargildi sem táknar lokadagsetninguna fyrir útreikning á fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="cb9de-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb9de-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="cb9de-111">Return values</span></span>

<span data-ttu-id="cb9de-112">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="cb9de-112">*Integer*</span></span>

<span data-ttu-id="cb9de-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="cb9de-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cb9de-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="cb9de-114">Usage notes</span></span>

<span data-ttu-id="cb9de-115">Aðgerðin `DAYS` skilar jákvæðu gildi þegar fyrsta dagsetningin er seinna en seinni dagsetningin, hún skilar **0** (núll) þegar fyrsta dagsetningin er jafngild annarri dagsetningu og hún skilar neikvæðu gildi þegar fyrsta dagsetningin er á undan seinni dagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="cb9de-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="cb9de-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="cb9de-116">Example</span></span>

<span data-ttu-id="cb9de-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` skilar **-1**.</span><span class="sxs-lookup"><span data-stu-id="cb9de-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb9de-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cb9de-118">Additional resources</span></span>

[<span data-ttu-id="cb9de-119">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="cb9de-119">Date and time functions</span></span>](er-functions-category-datetime.md)

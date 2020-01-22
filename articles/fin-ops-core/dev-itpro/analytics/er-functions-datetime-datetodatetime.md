---
title: DATETODATETIME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DATETODATETIME í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916385"
---
# <span data-ttu-id="e0c90-103"><a name="DATETODATETIME">DATETODATETIME ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="e0c90-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0c90-104">Aðgerðin `DATETODATETIME` skilar *DateTime*-gildi sem er umreiknað úr gefnu dagsetningargildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="e0c90-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c90-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="e0c90-105">Syntax</span></span>

```
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="e0c90-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="e0c90-106">Arguments</span></span>

<span data-ttu-id="e0c90-107">`date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="e0c90-107">`date`: *Date*</span></span>

<span data-ttu-id="e0c90-108">Dagsetningargildi sem táknar dagsetningu til að umreikna.</span><span class="sxs-lookup"><span data-stu-id="e0c90-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="e0c90-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="e0c90-109">Return values</span></span>

<span data-ttu-id="e0c90-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="e0c90-110">*DateTime*</span></span>

<span data-ttu-id="e0c90-111">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="e0c90-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e0c90-112">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="e0c90-112">Example 1</span></span>

<span data-ttu-id="e0c90-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` skilar dagsetningu gildandi Microsoft Dynamics 365 Finance-setu, 24. desember, 2015, sem **12/24 / 2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="e0c90-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="e0c90-114">Í þessu dæmi er **CompInfo** gagnagjafi rafrænnar skýrslugerðar (ER) fyrir **Finance and Operations/tafla** gerð og vísar til CompanyInfo töflunnar.</span><span class="sxs-lookup"><span data-stu-id="e0c90-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="e0c90-115">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="e0c90-115">Example 2</span></span>

<span data-ttu-id="e0c90-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` skilar dagsetningar-/tímagildinu **11/12 / 2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="e0c90-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0c90-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e0c90-117">Additional resources</span></span>

[<span data-ttu-id="e0c90-118">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="e0c90-118">Date and time functions</span></span>](er-functions-category-datetime.md)

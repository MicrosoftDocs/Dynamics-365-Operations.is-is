---
title: NULLDATETIME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLDATETIME í rafrænni skýrslugerð (ER) er notuð.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65e9ef92dc30e46c297d93e262bad8878df47a0c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682294"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="d9ec2-103">NULLDATETIME ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="d9ec2-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9ec2-104">Aðgerðin `NULLDATETIME` skilar *DateTime*-gildi sem táknar **núll** dagsetningar-/tímagildi (1. janúar, 1900) í samræmdum alþjóðlegum tíma (Greenwich-tími \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="d9ec2-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ec2-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="d9ec2-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="d9ec2-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d9ec2-106">Return values</span></span>

<span data-ttu-id="d9ec2-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="d9ec2-107">*DateTime*</span></span>

<span data-ttu-id="d9ec2-108">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="d9ec2-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="d9ec2-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="d9ec2-109">Example</span></span>

<span data-ttu-id="d9ec2-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` skilar strengjagildinu **1900-01-01T00:00:00.0000000+00:00** þegar það er kallað í ferli sem hafið var af notanda forrits sem hefur tímabeltisgildið **(GMT) Samræmdur alþjóðlegur tími** í hlutanum **Kjörstillingar tungumála og lands/svæðis**.</span><span class="sxs-lookup"><span data-stu-id="d9ec2-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9ec2-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d9ec2-111">Additional resources</span></span>

[<span data-ttu-id="d9ec2-112">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="d9ec2-112">Date and time functions</span></span>](er-functions-category-datetime.md)

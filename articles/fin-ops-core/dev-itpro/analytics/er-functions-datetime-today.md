---
title: TODAY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TODAY í rafrænni skýrslugerð (ER) er notuð.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93a9171456fb69e16c8104b0afb9ad485311b1a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683796"
---
# <a name="today-er-function"></a><span data-ttu-id="264d8-103">TODAY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="264d8-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="264d8-104">Aðgerð `TODAY` skilar *Date*-gildi sem táknar netþjónsdagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="264d8-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="264d8-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="264d8-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="264d8-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="264d8-106">Return values</span></span>

<span data-ttu-id="264d8-107">*Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="264d8-107">*Date*</span></span>

<span data-ttu-id="264d8-108">Dagsetningargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="264d8-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="264d8-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="264d8-109">Example</span></span>

<span data-ttu-id="264d8-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` skilar núverandi dagsetningargildi hugbúnaðarþjóns, 24. desember, 2015, sem strenginn **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="264d8-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="264d8-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="264d8-111">Additional resources</span></span>

[<span data-ttu-id="264d8-112">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="264d8-112">Date and time functions</span></span>](er-functions-category-datetime.md)

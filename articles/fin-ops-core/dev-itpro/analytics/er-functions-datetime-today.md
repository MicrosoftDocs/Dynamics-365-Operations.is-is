---
title: TODAY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TODAY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746748"
---
# <a name="today-er-function"></a><span data-ttu-id="cc4cc-103">TODAY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="cc4cc-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc4cc-104">Aðgerð `TODAY` skilar *Date*-gildi sem táknar netþjónsdagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc4cc-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="cc4cc-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="cc4cc-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="cc4cc-106">Return values</span></span>

<span data-ttu-id="cc4cc-107">*Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="cc4cc-107">*Date*</span></span>

<span data-ttu-id="cc4cc-108">Dagsetningargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="cc4cc-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="cc4cc-109">Example</span></span>

<span data-ttu-id="cc4cc-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` skilar núverandi dagsetningargildi hugbúnaðarþjóns, 24. desember, 2015, sem strenginn **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc4cc-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cc4cc-111">Additional resources</span></span>

[<span data-ttu-id="cc4cc-112">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="cc4cc-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
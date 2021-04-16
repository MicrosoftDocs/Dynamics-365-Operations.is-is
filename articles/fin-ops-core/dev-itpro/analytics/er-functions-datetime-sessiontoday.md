---
title: SESSIONTODAY ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SESSIONTODAY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746772"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="3d624-103">SESSIONTODAY ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="3d624-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d624-104">Aðgerðin `SESSIONTODAY` skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="3d624-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d624-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="3d624-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="3d624-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="3d624-106">Return values</span></span>

<span data-ttu-id="3d624-107">*Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="3d624-107">*Date*</span></span>

<span data-ttu-id="3d624-108">Dagsetningargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="3d624-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="3d624-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="3d624-109">Example</span></span>

<span data-ttu-id="3d624-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="3d624-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d624-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3d624-111">Additional resources</span></span>

[<span data-ttu-id="3d624-112">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="3d624-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
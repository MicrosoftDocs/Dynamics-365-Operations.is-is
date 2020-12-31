---
title: SESSIONTODAY ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SESSIONTODAY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 87e8d5498c82d7c9ca6ee0a855f139dde77d75ab
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683820"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="a93a7-103">SESSIONTODAY ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="a93a7-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a93a7-104">Aðgerðin `SESSIONTODAY` skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="a93a7-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93a7-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="a93a7-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="a93a7-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="a93a7-106">Return values</span></span>

<span data-ttu-id="a93a7-107">*Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="a93a7-107">*Date*</span></span>

<span data-ttu-id="a93a7-108">Dagsetningargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="a93a7-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="a93a7-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a93a7-109">Example</span></span>

<span data-ttu-id="a93a7-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="a93a7-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a93a7-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a93a7-111">Additional resources</span></span>

[<span data-ttu-id="a93a7-112">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="a93a7-112">Date and time functions</span></span>](er-functions-category-datetime.md)

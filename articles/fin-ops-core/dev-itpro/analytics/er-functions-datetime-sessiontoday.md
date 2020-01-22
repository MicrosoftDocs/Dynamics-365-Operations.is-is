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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917466"
---
# <span data-ttu-id="ef5b0-103"><a name="SESSIONTODAY">SESSIONTODAY ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="ef5b0-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef5b0-104">Aðgerðin `SESSIONTODAY` skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef5b0-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="ef5b0-105">Syntax</span></span>

```
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="ef5b0-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ef5b0-106">Return values</span></span>

<span data-ttu-id="ef5b0-107">*Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="ef5b0-107">*Date*</span></span>

<span data-ttu-id="ef5b0-108">Dagsetningargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="ef5b0-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ef5b0-109">Example</span></span>

<span data-ttu-id="ef5b0-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` skilar núverandi setudagsetningu hugbúnaðar, 24. desember 2015, sem strengnum  **"24-12-2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef5b0-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ef5b0-111">Additional resources</span></span>

[<span data-ttu-id="ef5b0-112">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="ef5b0-112">Date and time functions</span></span>](er-functions-category-datetime.md)

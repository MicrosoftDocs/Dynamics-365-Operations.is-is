---
title: FA_SUM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_SUM í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687697"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="6c8bf-103">FA_SUM ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="6c8bf-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c8bf-104">Aðgerðin `FA_SUM` skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um upphæðir fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan og dagsetningatímabil.</span><span class="sxs-lookup"><span data-stu-id="6c8bf-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8bf-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="6c8bf-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="6c8bf-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="6c8bf-106">Arguments</span></span>

<span data-ttu-id="6c8bf-107">`fixed asset code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="6c8bf-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="6c8bf-108">Gildið *Strengur* sem táknar kóða fastafjármagnsliða sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="6c8bf-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="6c8bf-109">`value model code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="6c8bf-109">`value model code`: *String*</span></span>

<span data-ttu-id="6c8bf-110">Gildið *Strengur* sem táknar kóða virðislíkans sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="6c8bf-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="6c8bf-111">`start date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="6c8bf-111">`start date`: *Date*</span></span>

<span data-ttu-id="6c8bf-112">Gildið *Dagsetning* sem táknar upphafsdag tímabils sem fastafjárhæðir eru reiknaðar út fyrir.</span><span class="sxs-lookup"><span data-stu-id="6c8bf-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="6c8bf-113">`end date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="6c8bf-113">`end date`: *Date*</span></span>

<span data-ttu-id="6c8bf-114">Gildið *Dagsetning* sem táknar lokadag tímabils sem fastafjárhæðir eru reiknaðar út fyrir.</span><span class="sxs-lookup"><span data-stu-id="6c8bf-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="6c8bf-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="6c8bf-115">Return values</span></span>

<span data-ttu-id="6c8bf-116">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="6c8bf-116">*Container (record)*</span></span>

<span data-ttu-id="6c8bf-117">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="6c8bf-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="6c8bf-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6c8bf-118">Example</span></span>

<span data-ttu-id="6c8bf-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` skilar gagnaíláti fyrir fastaeignina **COMP-000001** sem hefur verið undirbúin fyrir virðislíkanið **Gildandi** og fyrir tímabil frá **Dagsetning1** til **Dagsetning2**.</span><span class="sxs-lookup"><span data-stu-id="6c8bf-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c8bf-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6c8bf-120">Additional resources</span></span>

[<span data-ttu-id="6c8bf-121">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="6c8bf-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

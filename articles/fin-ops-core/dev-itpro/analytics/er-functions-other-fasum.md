---
title: FA_SUM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_SUM í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744296"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="cc7c5-103">FA_SUM ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="cc7c5-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc7c5-104">Aðgerðin `FA_SUM` skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um upphæðir fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan og dagsetningatímabil.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc7c5-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="cc7c5-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="cc7c5-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="cc7c5-106">Arguments</span></span>

<span data-ttu-id="cc7c5-107">`fixed asset code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="cc7c5-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="cc7c5-108">Gildið *Strengur* sem táknar kóða fastafjármagnsliða sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="cc7c5-109">`value model code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="cc7c5-109">`value model code`: *String*</span></span>

<span data-ttu-id="cc7c5-110">Gildið *Strengur* sem táknar kóða virðislíkans sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="cc7c5-111">`start date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="cc7c5-111">`start date`: *Date*</span></span>

<span data-ttu-id="cc7c5-112">Gildið *Dagsetning* sem táknar upphafsdag tímabils sem fastafjárhæðir eru reiknaðar út fyrir.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="cc7c5-113">`end date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="cc7c5-113">`end date`: *Date*</span></span>

<span data-ttu-id="cc7c5-114">Gildið *Dagsetning* sem táknar lokadag tímabils sem fastafjárhæðir eru reiknaðar út fyrir.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="cc7c5-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="cc7c5-115">Return values</span></span>

<span data-ttu-id="cc7c5-116">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="cc7c5-116">*Container (record)*</span></span>

<span data-ttu-id="cc7c5-117">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="cc7c5-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="cc7c5-118">Example</span></span>

<span data-ttu-id="cc7c5-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` skilar gagnaíláti fyrir fastaeignina **COMP-000001** sem hefur verið undirbúin fyrir virðislíkanið **Gildandi** og fyrir tímabil frá **Dagsetning1** til **Dagsetning2**.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc7c5-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cc7c5-120">Additional resources</span></span>

[<span data-ttu-id="cc7c5-121">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="cc7c5-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
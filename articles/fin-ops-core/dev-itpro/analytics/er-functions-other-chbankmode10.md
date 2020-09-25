---
title: CH_BANK_MOD_10 ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CH_BANK_MOD_10 í rafrænni skýrslugerð (ER) er notuð.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c18a7f96096fbc6bbc7b6d15135c11bd70960d26
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744471"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="8c55f-103">CH_BANK_MOD_10 ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="8c55f-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c55f-104">Aðgerðin `CH_BANK_MOD_10` skilar *Streng*-gildi sem táknar tilvísun kröfuhafa sem MOD10 segð, byggða á tölustöfum tilgreinds reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="8c55f-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c55f-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="8c55f-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="8c55f-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="8c55f-106">Arguments</span></span>

<span data-ttu-id="8c55f-107">`invoice number digits`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="8c55f-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="8c55f-108">Textagildi sem stendur fyrir tölustafi reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="8c55f-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c55f-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="8c55f-109">Return values</span></span>

<span data-ttu-id="8c55f-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="8c55f-110">*String*</span></span>

<span data-ttu-id="8c55f-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="8c55f-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8c55f-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8c55f-112">Example</span></span>

<span data-ttu-id="8c55f-113">`CH_BANK_MOD_10 ("VEND-200002")` skilar **3**.</span><span class="sxs-lookup"><span data-stu-id="8c55f-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c55f-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8c55f-114">Additional resources</span></span>

[<span data-ttu-id="8c55f-115">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="8c55f-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

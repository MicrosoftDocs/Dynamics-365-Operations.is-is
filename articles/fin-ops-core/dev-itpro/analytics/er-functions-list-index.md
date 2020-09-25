---
title: INDEX ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin INDEX í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745178"
---
# <a name="index-er-function"></a><span data-ttu-id="63126-103">INDEX ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="63126-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63126-104">Aðgerðin `INDEX` skilar gildinu *Ílát (skrá)* sem er valið með því að nota tilgreindan töluvísi í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="63126-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="63126-105">Ef vísirinn er utan marka fyrir skrárnar í tilgreindum lista er undantekningu beitt.</span><span class="sxs-lookup"><span data-stu-id="63126-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="63126-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="63126-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="63126-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="63126-107">Arguments</span></span>

<span data-ttu-id="63126-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="63126-108">`list`: *Record list*</span></span>

<span data-ttu-id="63126-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="63126-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="63126-110">`index`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="63126-110">`index`: *Integer*</span></span>

<span data-ttu-id="63126-111">Töluvísitala sem gefur til kynna staðsetningu viðkomandi skráar á tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="63126-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="63126-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="63126-112">Return values</span></span>

<span data-ttu-id="63126-113">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="63126-113">*Container (record)*</span></span>

<span data-ttu-id="63126-114">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="63126-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="63126-115">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="63126-115">Example 1</span></span>

<span data-ttu-id="63126-116">Ef þú slærð inn gagnagjafann **DS** í reitinn *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` skilar segðin `DS.Value` textagildinu **"B"** fyrir seinni skrána í skráalistanum.</span><span class="sxs-lookup"><span data-stu-id="63126-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="63126-117">Segðin `INDEX (SPLIT ("A|B|C", "|"), 2).Value` skilar líka textagildinu **"B"**.</span><span class="sxs-lookup"><span data-stu-id="63126-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="63126-118">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="63126-118">Example 2</span></span>

<span data-ttu-id="63126-119">Ef þú slærð inn gagnagjafa **DS** af gerðinni *Reiknaður reiður* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` beitir segðin `INDEX (SPLIT ("A|B|C", "|"), 4).Value` undantekningu á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="63126-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63126-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="63126-120">Additional resources</span></span>

[<span data-ttu-id="63126-121">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="63126-121">List functions</span></span>](er-functions-category-list.md)

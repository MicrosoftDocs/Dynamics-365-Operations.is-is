---
title: ISEMPTY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ISEMPTY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 5b6fde7cbadec7aae052742ef598e1af4dbae793
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745130"
---
# <a name="isempty-er-function"></a><span data-ttu-id="1a886-103">ISEMPTY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="1a886-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a886-104">Aðgerðin `ISEMPTY` skilar *Boole*-gildinu **TRUE** ef tilgreindur listi inniheldur engar skrár.</span><span class="sxs-lookup"><span data-stu-id="1a886-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="1a886-105">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="1a886-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a886-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="1a886-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="1a886-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="1a886-107">Arguments</span></span>

<span data-ttu-id="1a886-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="1a886-108">`list`: *Record list*</span></span>

<span data-ttu-id="1a886-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="1a886-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1a886-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="1a886-110">Return values</span></span>

<span data-ttu-id="1a886-111">*Boole*</span><span class="sxs-lookup"><span data-stu-id="1a886-111">*Boolean*</span></span>

<span data-ttu-id="1a886-112">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="1a886-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="1a886-113">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="1a886-113">Example 1</span></span>

<span data-ttu-id="1a886-114">Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` skilar segðin `ISEMPTY(DS)` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="1a886-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1a886-115">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="1a886-115">Example 2</span></span>

<span data-ttu-id="1a886-116">Segðin `ISEMPTY (SPLIT ("",1))` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="1a886-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a886-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1a886-117">Additional resources</span></span>

[<span data-ttu-id="1a886-118">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="1a886-118">List functions</span></span>](er-functions-category-list.md)

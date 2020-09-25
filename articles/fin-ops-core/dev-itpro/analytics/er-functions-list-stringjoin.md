---
title: STRINGJOIN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin STRINGJOIN í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 4f5d6b9a0f43902160d1ff7fa91b86a7e2c3422d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743495"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="badf8-103">STRINGJOIN ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="badf8-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="badf8-104">Aðgerðin `STRINGJOIN` skilar *strengjagildi* sem samanstendur af samsettum gildum tiltekins svæðis úr tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="badf8-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="badf8-105">Hægt er að aðskilja gildin með tilgreindri afmörkun.</span><span class="sxs-lookup"><span data-stu-id="badf8-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="badf8-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="badf8-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="badf8-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="badf8-107">Arguments</span></span>

<span data-ttu-id="badf8-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="badf8-108">`list`: *Record list*</span></span>

<span data-ttu-id="badf8-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="badf8-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="badf8-110">`field`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="badf8-110">`field`: *Field*</span></span>

<span data-ttu-id="badf8-111">Gild slóð á reiti af gagnagerðinni *Strengur* í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="badf8-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="badf8-112">`delimiter`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="badf8-112">`delimiter`: *String*</span></span>

<span data-ttu-id="badf8-113">Afmarkari sem er notaður til að aðgreina undirstrengi.</span><span class="sxs-lookup"><span data-stu-id="badf8-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="badf8-114">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="badf8-114">Return values</span></span>

<span data-ttu-id="badf8-115">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="badf8-115">*String*</span></span>

<span data-ttu-id="badf8-116">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="badf8-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="badf8-117">Dæmi</span><span class="sxs-lookup"><span data-stu-id="badf8-117">Example</span></span>

<span data-ttu-id="badf8-118">Ef þú slærð inn `SPLIT("abc" , 1)` sem gagnagjafa **DS** skilar segðin `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="badf8-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="badf8-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="badf8-119">Additional resources</span></span>

[<span data-ttu-id="badf8-120">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="badf8-120">List functions</span></span>](er-functions-category-list.md)

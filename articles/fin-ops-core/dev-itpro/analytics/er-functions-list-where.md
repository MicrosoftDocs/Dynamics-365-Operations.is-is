---
title: WHERE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin WHERE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 94326986791c95eac7b0f5771f779014d865d3bb
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743437"
---
# <a name="where-er-function"></a><span data-ttu-id="4d1ff-103">WHERE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="4d1ff-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d1ff-104">Aðgerðin `WHERE` skilar tilgreindum lista sem *Skráalista*-gildi eftir að það hefur verið síað í samræmi við tilgreind skilyrði.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1ff-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4d1ff-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="4d1ff-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4d1ff-106">Arguments</span></span>

<span data-ttu-id="4d1ff-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="4d1ff-107">`list`: *Record list*</span></span>

<span data-ttu-id="4d1ff-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="4d1ff-109">`condition`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="4d1ff-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="4d1ff-110">Gild skilyrt tjáning sem er notuð til að sía skrár yfir tiltekinn lista.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="4d1ff-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4d1ff-111">Return values</span></span>

<span data-ttu-id="4d1ff-112">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="4d1ff-112">*Record list*</span></span>

<span data-ttu-id="4d1ff-113">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4d1ff-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="4d1ff-114">Usage notes</span></span>

<span data-ttu-id="4d1ff-115">Þessi aðgerð er frábrugðin [FILTER](er-functions-list-filter.md) aðgerðinni, vegna þess að tilgreint skilyrði er beitt á hvaða gagnagjafa rafrænnar skýrslugerðar (ER) af gerðinni *Skráalisti* sem er til staðar í minninu.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="4d1ff-116">Ef frumbreyturnar sem eru stilltar fyrir þessa aðgerð (`list` og `condition`) leyfa að þýða þessa beiðni yfir í beint SQL-kall eru send viðvörunarboð á hönnunartíma.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="4d1ff-117">Þessi skilaboð upplýsa notandann um að árangur gæti verið betri ef aðgerðin [FILTER](er-functions-list-filter.md) er notuð í staðinn fyrir `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="4d1ff-118">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="4d1ff-118">Example 1</span></span>

<span data-ttu-id="4d1ff-119">Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar til VendTable-töflunnar skilar segðin `WHERE (Vendors, Vendors.VendGroup = "40")` lista yfir aðeins lánardrottna sem tilheyra lánardrottnaflokki 40.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="4d1ff-120">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="4d1ff-120">Example 2</span></span>

<span data-ttu-id="4d1ff-121">Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` skilar segðin `WHERE( DS, DS.Value = "B")` lista yfir aðeins eina skrá sem inniheldur textann **"B"** í reitnum **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="4d1ff-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d1ff-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4d1ff-122">Additional resources</span></span>

[<span data-ttu-id="4d1ff-123">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="4d1ff-123">List functions</span></span>](er-functions-category-list.md)

---
title: ORDERBY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ORDERBY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5a995713a795b3f24a4fcfadcc4be596e932a22c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564167"
---
# <a name="orderby-er-function"></a><span data-ttu-id="f2524-103">ORDERBY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f2524-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2524-104">Aðgerðin `ORDERBY` skilar tilgreindum lista sem *Skráalista*-gildi eftir að því hefur verið raðað í samræmi við tilgreindar frumbreytur.</span><span class="sxs-lookup"><span data-stu-id="f2524-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="f2524-105">Þessi frumbreytur geta verið skilgreindar sem segðir.</span><span class="sxs-lookup"><span data-stu-id="f2524-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2524-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f2524-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="f2524-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f2524-107">Arguments</span></span>

<span data-ttu-id="f2524-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f2524-108">`list`: *Record list*</span></span>

<span data-ttu-id="f2524-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="f2524-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f2524-110">`expression 1`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="f2524-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="f2524-111">Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="f2524-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="f2524-112">Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="f2524-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="f2524-113">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="f2524-113">This argument is required.</span></span>

<span data-ttu-id="f2524-114">`expression N`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="f2524-114">`expression N`: *Field*</span></span>

<span data-ttu-id="f2524-115">Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="f2524-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="f2524-116">Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="f2524-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="f2524-117">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="f2524-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f2524-118">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f2524-118">Return values</span></span>

<span data-ttu-id="f2524-119">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f2524-119">*Record list*</span></span>

<span data-ttu-id="f2524-120">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="f2524-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="f2524-121">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="f2524-121">Example 1</span></span>

<span data-ttu-id="f2524-122">Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( ORDERBY( DS, DS. Value)).Value` textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="f2524-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f2524-123">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="f2524-123">Example 2</span></span>

<span data-ttu-id="f2524-124">Ef **Lánardrottinn** er stilltur sem gagnagjafi rafrænnar skýrslugerðar (ER) sem vísar til töflunnar VendTable skilar segðin `ORDERBY (Vendors, Vendors.'name()')` lista yfir lánardrottna sem er raðað eftir heiti í hækkandi röð.</span><span class="sxs-lookup"><span data-stu-id="f2524-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2524-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f2524-125">Additional resources</span></span>

[<span data-ttu-id="f2524-126">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="f2524-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
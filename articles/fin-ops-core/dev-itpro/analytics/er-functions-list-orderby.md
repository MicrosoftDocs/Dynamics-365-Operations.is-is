---
title: ORDERBY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ORDERBY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753193"
---
# <a name="orderby-er-function"></a><span data-ttu-id="81f50-103">ORDERBY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="81f50-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81f50-104">Aðgerðin `ORDERBY` skilar tilgreindum lista sem *Skráalista*-gildi eftir að því hefur verið raðað í samræmi við tilgreindar frumbreytur.</span><span class="sxs-lookup"><span data-stu-id="81f50-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="81f50-105">Þessi frumbreytur geta verið skilgreindar sem segðir.</span><span class="sxs-lookup"><span data-stu-id="81f50-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f50-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="81f50-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="81f50-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="81f50-107">Arguments</span></span>

<span data-ttu-id="81f50-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="81f50-108">`list`: *Record list*</span></span>

<span data-ttu-id="81f50-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="81f50-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="81f50-110">`expression 1`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="81f50-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="81f50-111">Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="81f50-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="81f50-112">Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="81f50-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="81f50-113">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="81f50-113">This argument is required.</span></span>

<span data-ttu-id="81f50-114">`expression N`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="81f50-114">`expression N`: *Field*</span></span>

<span data-ttu-id="81f50-115">Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="81f50-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="81f50-116">Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="81f50-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="81f50-117">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="81f50-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="81f50-118">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="81f50-118">Return values</span></span>

<span data-ttu-id="81f50-119">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="81f50-119">*Record list*</span></span>

<span data-ttu-id="81f50-120">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="81f50-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="81f50-121">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="81f50-121">Example 1</span></span>

<span data-ttu-id="81f50-122">Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( ORDERBY( DS, DS. Value)).Value` textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="81f50-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="81f50-123">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="81f50-123">Example 2</span></span>

<span data-ttu-id="81f50-124">Ef **Lánardrottinn** er stilltur sem gagnagjafi rafrænnar skýrslugerðar (ER) sem vísar til töflunnar VendTable skilar segðin `ORDERBY (Vendors, Vendors.'name()')` lista yfir lánardrottna sem er raðað eftir heiti í hækkandi röð.</span><span class="sxs-lookup"><span data-stu-id="81f50-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81f50-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="81f50-125">Additional resources</span></span>

[<span data-ttu-id="81f50-126">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="81f50-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
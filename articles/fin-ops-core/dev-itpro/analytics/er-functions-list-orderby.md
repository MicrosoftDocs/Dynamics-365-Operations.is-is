---
title: ORDERBY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ORDERBY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041953"
---
# <span data-ttu-id="4424d-103"><a name="ORDERBY">ORDERBY ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="4424d-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4424d-104">Aðgerðin `ORDERBY` skilar tilgreindum lista sem *Skráalista*-gildi eftir að því hefur verið raðað í samræmi við tilgreindar frumbreytur.</span><span class="sxs-lookup"><span data-stu-id="4424d-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="4424d-105">Þessi frumbreytur geta verið skilgreindar sem segðir.</span><span class="sxs-lookup"><span data-stu-id="4424d-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4424d-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4424d-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="4424d-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4424d-107">Arguments</span></span>

<span data-ttu-id="4424d-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="4424d-108">`list`: *Record list*</span></span>

<span data-ttu-id="4424d-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="4424d-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="4424d-110">`expression 1`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="4424d-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="4424d-111">Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4424d-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="4424d-112">Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="4424d-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="4424d-113">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="4424d-113">This argument is required.</span></span>

<span data-ttu-id="4424d-114">`expression N`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="4424d-114">`expression N`: *Field*</span></span>

<span data-ttu-id="4424d-115">Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4424d-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="4424d-116">Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="4424d-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="4424d-117">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="4424d-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4424d-118">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4424d-118">Return values</span></span>

<span data-ttu-id="4424d-119">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="4424d-119">*Record list*</span></span>

<span data-ttu-id="4424d-120">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="4424d-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="4424d-121">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="4424d-121">Example 1</span></span>

<span data-ttu-id="4424d-122">Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( ORDERBY( DS, DS. Value)).Value` textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="4424d-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4424d-123">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="4424d-123">Example 2</span></span>

<span data-ttu-id="4424d-124">Ef **Lánardrottinn** er stilltur sem gagnagjafi rafrænnar skýrslugerðar (ER) sem vísar til töflunnar VendTable skilar segðin `ORDERBY (Vendors, Vendors.'name()')` lista yfir lánardrottna sem er raðað eftir heiti í hækkandi röð.</span><span class="sxs-lookup"><span data-stu-id="4424d-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4424d-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4424d-125">Additional resources</span></span>

[<span data-ttu-id="4424d-126">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="4424d-126">List functions</span></span>](er-functions-category-list.md)

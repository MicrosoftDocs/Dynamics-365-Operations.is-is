---
title: LISTJOIN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTJOIN í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249036"
---
# <a name=""></a><span data-ttu-id="69cb6-103"><a name="LISTJOIN">LISTJOIN ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="69cb6-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69cb6-104">Aðgerðin `LISTJOIN` skilar *Skráalista*-gildi sem samanstendur af nýjum sameinuðum lista yfir skrár sem er stofnaður úr tilgreindum frumbreytum.</span><span class="sxs-lookup"><span data-stu-id="69cb6-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="69cb6-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="69cb6-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="69cb6-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="69cb6-106">Arguments</span></span>

<span data-ttu-id="69cb6-107">`list 1`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="69cb6-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="69cb6-108">Tilvísun í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="69cb6-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="69cb6-109">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="69cb6-109">This argument is mandatory.</span></span>

<span data-ttu-id="69cb6-110">`list N`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="69cb6-110">`list N`: *Record list*</span></span>

<span data-ttu-id="69cb6-111">Tilvísun í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="69cb6-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="69cb6-112">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="69cb6-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="69cb6-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="69cb6-113">Return values</span></span>

<span data-ttu-id="69cb6-114">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="69cb6-114">*Record list*</span></span>

<span data-ttu-id="69cb6-115">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="69cb6-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="69cb6-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="69cb6-116">Usage notes</span></span>

<span data-ttu-id="69cb6-117">Skipulag listans sem er stofnað inniheldur aðeins reitina sem eru settir fram í skipulagi hvers skráalista sem vísað er til í frumbreytunum.</span><span class="sxs-lookup"><span data-stu-id="69cb6-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="69cb6-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="69cb6-118">Example</span></span>

<span data-ttu-id="69cb6-119">Þú slærð inn gagnagjafann **Skrá 1** af gerðinni `Container`.</span><span class="sxs-lookup"><span data-stu-id="69cb6-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="69cb6-120">Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="69cb6-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="69cb6-121">**Kóði**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `String`.</span><span class="sxs-lookup"><span data-stu-id="69cb6-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="69cb6-122">**Upphæð**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Real`.</span><span class="sxs-lookup"><span data-stu-id="69cb6-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="69cb6-123">Síðan slærðu inn gagnagjafann **Skrá 2** af gerðinni `Container`.</span><span class="sxs-lookup"><span data-stu-id="69cb6-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="69cb6-124">Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="69cb6-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="69cb6-125">**Upphæð**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Real`.</span><span class="sxs-lookup"><span data-stu-id="69cb6-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="69cb6-126">**IsValid**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="69cb6-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="69cb6-127">Í þessu tilfelli skilar segðin `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` nýjum lista sem inniheldur tvær skrár.</span><span class="sxs-lookup"><span data-stu-id="69cb6-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="69cb6-128">Skipulag listans samanstendur af staka reitnum **Upphæð** af gerðinni `Real` þar sem þessi reitur er eini reiturinn sem er settur fram í öllum frumbreytum sem kalla aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="69cb6-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69cb6-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="69cb6-129">Additional resources</span></span>

[<span data-ttu-id="69cb6-130">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="69cb6-130">List functions</span></span>](er-functions-category-list.md)

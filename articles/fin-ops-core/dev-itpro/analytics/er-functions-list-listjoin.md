---
title: LISTJOIN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTJOIN í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efee93df7d1cf40d016b36042bb5e7f33c47ae44
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743800"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="2d216-103">LISTJOIN ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="2d216-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d216-104">Aðgerðin `LISTJOIN` skilar *Skráalista*-gildi sem samanstendur af nýjum sameinuðum lista yfir skrár sem er stofnaður úr tilgreindum frumbreytum.</span><span class="sxs-lookup"><span data-stu-id="2d216-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d216-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="2d216-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="2d216-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="2d216-106">Arguments</span></span>

<span data-ttu-id="2d216-107">`list 1`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="2d216-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="2d216-108">Tilvísun í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="2d216-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="2d216-109">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="2d216-109">This argument is mandatory.</span></span>

<span data-ttu-id="2d216-110">`list N`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="2d216-110">`list N`: *Record list*</span></span>

<span data-ttu-id="2d216-111">Tilvísun í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="2d216-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="2d216-112">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="2d216-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2d216-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="2d216-113">Return values</span></span>

<span data-ttu-id="2d216-114">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="2d216-114">*Record list*</span></span>

<span data-ttu-id="2d216-115">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="2d216-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2d216-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="2d216-116">Usage notes</span></span>

<span data-ttu-id="2d216-117">Skipulag listans sem er stofnað inniheldur aðeins reitina sem eru settir fram í skipulagi hvers skráalista sem vísað er til í frumbreytunum.</span><span class="sxs-lookup"><span data-stu-id="2d216-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="2d216-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="2d216-118">Example</span></span>

<span data-ttu-id="2d216-119">Þú slærð inn gagnagjafann **Skrá 1** af gerðinni `Container`.</span><span class="sxs-lookup"><span data-stu-id="2d216-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="2d216-120">Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="2d216-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="2d216-121">**Kóði**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `String`.</span><span class="sxs-lookup"><span data-stu-id="2d216-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="2d216-122">**Upphæð**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Real`.</span><span class="sxs-lookup"><span data-stu-id="2d216-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="2d216-123">Síðan slærðu inn gagnagjafann **Skrá 2** af gerðinni `Container`.</span><span class="sxs-lookup"><span data-stu-id="2d216-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="2d216-124">Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="2d216-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="2d216-125">**Upphæð**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Real`.</span><span class="sxs-lookup"><span data-stu-id="2d216-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="2d216-126">**IsValid**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="2d216-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![Hönnuðarsíðan ER-líkanavörpun](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="2d216-128">Í þessu tilfelli skilar segðin `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` nýjum lista sem inniheldur tvær skrár.</span><span class="sxs-lookup"><span data-stu-id="2d216-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![ER vörpun líkans hönnuður síða með tveimur færslum](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="2d216-130">Skipulag listans samanstendur af staka reitnum **Upphæð** af gerðinni `Real` þar sem þessi reitur er eini reiturinn sem er settur fram í öllum frumbreytum sem kalla aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="2d216-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER vörpun líkans hönnuður síða reitur upphæðar](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="2d216-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2d216-132">Additional resources</span></span>

[<span data-ttu-id="2d216-133">Listaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="2d216-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="2d216-134">Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu</span><span class="sxs-lookup"><span data-stu-id="2d216-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
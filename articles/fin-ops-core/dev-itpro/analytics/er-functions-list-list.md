---
title: LIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LIST í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: ee51b6da008d1c0fcfb303e9659f507629237333
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042022"
---
# <span data-ttu-id="feeea-103"><a name="LIST">LIST ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="feeea-103"><a name="LIST">LIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feeea-104">Aðgerðin `LIST` skilar *Skráalista*-gildi sem samanstendur af nýjum lista yfir skrár sem er stofnaður úr tilgreindum frumbreytum.</span><span class="sxs-lookup"><span data-stu-id="feeea-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="feeea-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="feeea-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="feeea-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="feeea-106">Arguments</span></span>

<span data-ttu-id="feeea-107">`record 1`: *Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="feeea-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="feeea-108">Tilvísun í gagnagjafa af gagnagerðinni *Skrá*.</span><span class="sxs-lookup"><span data-stu-id="feeea-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="feeea-109">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="feeea-109">This argument is required.</span></span>

<span data-ttu-id="feeea-110">`record N`: *Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="feeea-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="feeea-111">Tilvísun í gagnagjafa af gagnagerðinni *Skrá*.</span><span class="sxs-lookup"><span data-stu-id="feeea-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="feeea-112">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="feeea-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="feeea-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="feeea-113">Return values</span></span>

<span data-ttu-id="feeea-114">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="feeea-114">*Record list*</span></span>

<span data-ttu-id="feeea-115">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="feeea-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="feeea-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="feeea-116">Usage notes</span></span>

<span data-ttu-id="feeea-117">Skipulag listans sem er stofnað inniheldur aðeins reitina sem eru settir fram í skipulagi hverrar skráar sem nefnd er í frumbreytunum.</span><span class="sxs-lookup"><span data-stu-id="feeea-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="feeea-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="feeea-118">Example</span></span>

<span data-ttu-id="feeea-119">Þú slærð inn gagnagjafann **Skrá 1** af gerðinni *Ílát*.</span><span class="sxs-lookup"><span data-stu-id="feeea-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="feeea-120">Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni *Reiknaður reitur*:</span><span class="sxs-lookup"><span data-stu-id="feeea-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="feeea-121">**Kóði:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="feeea-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="feeea-122">**Upphæð:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Raun*.</span><span class="sxs-lookup"><span data-stu-id="feeea-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="feeea-123">Síðan slærðu inn gagnagjafann **Skrá 2** af gerðinni *Ílát*.</span><span class="sxs-lookup"><span data-stu-id="feeea-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="feeea-124">Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni *Reiknaður reitur*:</span><span class="sxs-lookup"><span data-stu-id="feeea-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="feeea-125">**Upphæð:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Raun*.</span><span class="sxs-lookup"><span data-stu-id="feeea-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="feeea-126">**ISValid:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Boolean*.</span><span class="sxs-lookup"><span data-stu-id="feeea-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="feeea-127">Í þessu tilfelli skilar segðin `LIST('Record 1', 'Record 2')` nýjum lista sem inniheldur tvær skrár.</span><span class="sxs-lookup"><span data-stu-id="feeea-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="feeea-128">Skipulag listans samanstendur af staka reitnum **Upphæð** af gerðinni *Raun* þar sem þessi reitur er eini reiturinn sem er settur fram í öllum frumbreytum sem kalla aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="feeea-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="feeea-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="feeea-129">Additional resources</span></span>

[<span data-ttu-id="feeea-130">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="feeea-130">List functions</span></span>](er-functions-category-list.md)

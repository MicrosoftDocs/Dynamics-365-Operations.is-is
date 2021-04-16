---
title: VALUEINLARGE ER aðgerð
description: Í þessu efnisatriði er að finna upplýsingar um hvernig VALUEINLARGE rafræn skýrslugerðarvirkni er notuð.
author: NickSelin
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 74d6856a0598293d87f79baabed4773d617164d0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743752"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="0d18a-103">VALUEINLARGE ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="0d18a-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d18a-104">`VALUEINLARGE` virknin ákvarðar hvort tilgreindur innsláttur *Int64* eða *Heiltala* passar við hvaða gildi hlutar sem er í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="0d18a-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0d18a-105">Virknin skilar *Boolean* gildið **TRUE** ef tilgreindur innsláttur passar við niðurstöðurnar af því að keyra tilgreinda segð fyrir að minnsta kosti eina færslu.</span><span class="sxs-lookup"><span data-stu-id="0d18a-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0d18a-106">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0d18a-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="0d18a-107">Til að skilja muninn með aðgerðinni `VALUEIN` skal skoða [Athugasemdir um notkun](#usage_note) síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="0d18a-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d18a-108">Málskipun</span><span class="sxs-lookup"><span data-stu-id="0d18a-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="0d18a-109">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="0d18a-109">Arguments</span></span>

<span data-ttu-id="0d18a-110">`input`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="0d18a-110">`input`: *Field*</span></span>

<span data-ttu-id="0d18a-111">Gild slóð gagnauppruna af gerðinni *Færslulisti*.</span><span class="sxs-lookup"><span data-stu-id="0d18a-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="0d18a-112">Gildi þessa hlutar verður jafnað.</span><span class="sxs-lookup"><span data-stu-id="0d18a-112">The value of this item will be matched.</span></span>

<span data-ttu-id="0d18a-113">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="0d18a-113">`list`: *Record list*</span></span>

<span data-ttu-id="0d18a-114">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="0d18a-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0d18a-115">`list item expression`: *Segð*</span><span class="sxs-lookup"><span data-stu-id="0d18a-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="0d18a-116">Gild skilyrðisbundið segð sem annaðhvort bendir á eða inniheldur stakan reit af tilgreindum lista sem á að nota við jöfnunina.</span><span class="sxs-lookup"><span data-stu-id="0d18a-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d18a-117">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="0d18a-117">Return values</span></span>

<span data-ttu-id="0d18a-118">*Boole*</span><span class="sxs-lookup"><span data-stu-id="0d18a-118">*Boolean*</span></span>

<span data-ttu-id="0d18a-119">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="0d18a-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="0d18a-120"><a name="usage_note">Notkunarbréf</a></span><span class="sxs-lookup"><span data-stu-id="0d18a-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="0d18a-121">Þegar tilgreint ílag stendur fyrir *Int64* eða *heiltölu* gerð gagnaupprunaatriðis er tilgreint hvaða kall er tengt við beina SQL-segð, listanum er breytt í tímabundna SQL-töflu og samsvörun er framkvæmd í gagnagrunninum með því að framkvæma eina `EXISTS JOIN` fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="0d18a-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="0d18a-122">Annars virkar aðgerðin eins og [`VALUEIN`](er-functions-logical-valuein.md) aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="0d18a-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="0d18a-123">Þegar tilgreint inntak stendur fyrir gagnaupprunavöru sem er hönnuð sem önnur vara en *Int64* og *heiltala* kemur fram villa á hönnunarstigi sem upplýsir að aðgerðin `VALUEINLARGE` eigi ekki við um skilgreinda segð rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="0d18a-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="0d18a-124">Þegar `VALUEINLARGE` aðgerðarsegð er keyrð og fleiri en ein tímabundin tafla er notuð fyrir umfang þessarar framkvæmdar, kemur upp villa í keyrslu.</span><span class="sxs-lookup"><span data-stu-id="0d18a-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="0d18a-125">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0d18a-125">Example</span></span>

<span data-ttu-id="0d18a-126">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="0d18a-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="0d18a-127">Gagnagjafinn **In** af gerðinni *Töfluskrár*.</span><span class="sxs-lookup"><span data-stu-id="0d18a-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="0d18a-128">Þessi gagnagjafi vísar í töfluna **Intrastat** .</span><span class="sxs-lookup"><span data-stu-id="0d18a-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="0d18a-129">Að sjálfgefnu er valkosturinn **Milli fyrirtækja** stilltur á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="0d18a-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="0d18a-130">**InMemory** gagnagjafi af gerðinni *Reiknaður reitur*.</span><span class="sxs-lookup"><span data-stu-id="0d18a-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="0d18a-131">Þessi gagnaveita inniheldur segðina `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="0d18a-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="0d18a-132">**InFiltered** gagnagjafi af gerðinni *Reiknaður reitur*.</span><span class="sxs-lookup"><span data-stu-id="0d18a-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="0d18a-133">Þessi gagnaveita inniheldur segðina `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="0d18a-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="0d18a-134">Þegar gagnagjafi **InFiltered** er kallaður undir samhengi fyrirtækisins **DEMF** er ný tímabundin tafla stofnuð í forritsgagnagrunninum, samansafn færslna auðkenniskóða í minnislista eru færð inn í þessa töflu og eftirfarandi SQL-yfirlit er myndað til að skila síuðum færslum af töflunni **Intrastat** .</span><span class="sxs-lookup"><span data-stu-id="0d18a-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="0d18a-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0d18a-135">Additional resources</span></span>

[<span data-ttu-id="0d18a-136">Rökfræðiaðgerðir</span><span class="sxs-lookup"><span data-stu-id="0d18a-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="0d18a-137">VALUEIN aðgerðir</span><span class="sxs-lookup"><span data-stu-id="0d18a-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
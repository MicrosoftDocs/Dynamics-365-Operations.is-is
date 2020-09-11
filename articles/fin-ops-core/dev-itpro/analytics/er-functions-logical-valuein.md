---
title: VALUEIN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin VALUEIN í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: 44459ae56891a08eb11a6c254f4b4d5652a0e693
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705120"
---
# <a name=""></a><span data-ttu-id="218a5-103"><a name="VALUEIN">VALUEIN ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="218a5-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="218a5-104">Aðgerðin `VALUEIN` ákvarðar hvort tilgreint ílag passar við eitthvert gildi tilgreinds hlutar sem er í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="218a5-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="218a5-105">Hún skilar *Boolean*-gildinu **TRUE** ef tilgreint inntak passar við niðurstöðu þess að keyra tiltekna segð fyrir að minnsta kosti eina skrá af tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="218a5-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="218a5-106">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="218a5-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="218a5-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="218a5-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="218a5-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="218a5-108">Arguments</span></span>

<span data-ttu-id="218a5-109">`input`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="218a5-109">`input`: *Field*</span></span>

<span data-ttu-id="218a5-110">Gild slóð hlutar í gagnagjafa af gerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="218a5-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="218a5-111">Gildi þessa hlutar verður jafnað.</span><span class="sxs-lookup"><span data-stu-id="218a5-111">The value of this item will be matched.</span></span>

<span data-ttu-id="218a5-112">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="218a5-112">`list`: *Record list*</span></span>

<span data-ttu-id="218a5-113">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="218a5-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="218a5-114">`list item expression`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="218a5-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="218a5-115">Gild skilyrðisbundið segð sem annaðhvort bendir á eða inniheldur stakan reit af tilgreindum lista sem á að nota við jöfnunina.</span><span class="sxs-lookup"><span data-stu-id="218a5-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="218a5-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="218a5-116">Return values</span></span>

<span data-ttu-id="218a5-117">*Boole*</span><span class="sxs-lookup"><span data-stu-id="218a5-117">*Boolean*</span></span>

<span data-ttu-id="218a5-118">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="218a5-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="218a5-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="218a5-119">Usage notes</span></span>

<span data-ttu-id="218a5-120">Almennt er virknin `VALUEIN` þýdd yfir í sett af **OR** skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="218a5-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="218a5-121">Ef listinn yfir **EÐA** skilyrði er stór og hugsanlega er farið yfir samtals hámarkslengd SQL-skipunar, skal íhuga að nota aðgerðina [`VALUEINLARGE`](er-functions-logical-valueinlarge.md).</span><span class="sxs-lookup"><span data-stu-id="218a5-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="218a5-122">SQLÍ sumum tilvikum er hægt að þýða það yfir í SQL-skipun gagnagrunns með því að nota virkjann `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="218a5-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="218a5-123">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="218a5-123">Example 1</span></span>

<span data-ttu-id="218a5-124">Í líkanavörpuninni skilgreinirðu gagnagjafann **Lista** af gerðinni *Reiknaður reitur*.</span><span class="sxs-lookup"><span data-stu-id="218a5-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="218a5-125">Þessi gagnaveita inniheldur segðina `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="218a5-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="218a5-126">Þegar gagnagjafi er kallaður, ef hann hefur verið stilltur sem segðin `VALUEIN ("B", List, List.Value)` skilar hann **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="218a5-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="218a5-127">Í þessu tilviki er aðgerðin `VALUEIN` þýdd í eftirfarandi samstæðu af skilyrðum: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, þar sem `("B" = "b")` er jafnt og **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="218a5-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="218a5-128">Þegar gagnagjafi er kallaður, ef hann hefur verið stilltur sem segðin `VALUEIN ("B", List, LEFT(List.Value, 0))` skilar hann **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="218a5-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="218a5-129">Í þessu tilviki er aðgerðin `VALUEIN` þýdd í eftirfarandi skilyrði: `("B" = "")` sem er ekki jafnt og **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="218a5-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="218a5-130">Efri mörkin fyrir fjölda stafa í texta slíks ástands eru 32.768 stafir.</span><span class="sxs-lookup"><span data-stu-id="218a5-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="218a5-131">Þess vegna ættir þú ekki að búa til gagnaveitur sem kunna að fara yfir þessi mörk við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="218a5-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="218a5-132">Ef farið er yfir mörkin mun forritið stöðvast og undantekning er gerð.</span><span class="sxs-lookup"><span data-stu-id="218a5-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="218a5-133">Til dæmis getur þetta ástand komið fram ef gagnaveitan er skilgreind sem `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` og listarnir **List1** og **List2** innihalda mikið magn af færslum.</span><span class="sxs-lookup"><span data-stu-id="218a5-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="218a5-134">Í sumum tilfellum er `VALUEIN` þýtt í gagnagrunnsstreng með því að nota `EXISTS JOIN` virknitáknið.</span><span class="sxs-lookup"><span data-stu-id="218a5-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="218a5-135">Þessi hegðun kemur fram þegar [`FILTER`](er-functions-list-filter.md) virknin er notuð og eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="218a5-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="218a5-136">Slökkt er á valkostinum **ASK FOR QUERY** fyrir gagnagjafa aðgerðarinnar `VALUEIN` sem vísar til lista yfir skrár.</span><span class="sxs-lookup"><span data-stu-id="218a5-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="218a5-137">Engum viðbótarskilyrðum verður beitt á þessum gagnaveitum meðan á keyrslu stendur.</span><span class="sxs-lookup"><span data-stu-id="218a5-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="218a5-138">Engar faldaðar segðir eru stilltar fyrir gagnaveituna `VALUEIN` aðgerðina sem vísar til listans yfir skrár.</span><span class="sxs-lookup"><span data-stu-id="218a5-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="218a5-139">Listaatriði `VALUEIN` aðgerðarinnar vísar til reitar af tilgreindri gagnaveitu, ekki til segðar eða aðferðar þeirrar gagnaveitu.</span><span class="sxs-lookup"><span data-stu-id="218a5-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="218a5-140">Íhugaðu að nota þennan valkost í staðinn fyrir [`WHERE`](er-functions-list-where.md) aðgerðina sem er lýst hér að framan í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="218a5-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="218a5-141">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="218a5-141">Example 2</span></span>

<span data-ttu-id="218a5-142">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="218a5-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="218a5-143">Gagnagjafinn **In** af gerðinni *Töfluskrár*.</span><span class="sxs-lookup"><span data-stu-id="218a5-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="218a5-144">Þessi gagnagjafi vísar til Intrastat töflunnar.</span><span class="sxs-lookup"><span data-stu-id="218a5-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="218a5-145">Gagnagjafinn **Port** af gerðinni *Töfluskrár*.</span><span class="sxs-lookup"><span data-stu-id="218a5-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="218a5-146">Þessi gagnagjafi vísar til IntrastatPort töflunnar.</span><span class="sxs-lookup"><span data-stu-id="218a5-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="218a5-147">Þegar gagnaveita er kölluð sem hefur verið stillt sem segðin `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, er eftirfarandi SQL-skipun sköpuð til að skila síuðum skrám af Intrastat töflunni.</span><span class="sxs-lookup"><span data-stu-id="218a5-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="218a5-148">Fyrir **dataAreaId** reiti er endanleg SQL-skipun mynduð með því að nota `IN` virknitákn.</span><span class="sxs-lookup"><span data-stu-id="218a5-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="218a5-149">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="218a5-149">Example 3</span></span>

<span data-ttu-id="218a5-150">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="218a5-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="218a5-151">Gagnagjafinn **Le** af gerðinni *Reiknaður reitur*.</span><span class="sxs-lookup"><span data-stu-id="218a5-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="218a5-152">Þessi gagnaveita inniheldur segðina `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="218a5-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="218a5-153">Gagnagjafinn **In** af gerðinni *Töfluskrár*.</span><span class="sxs-lookup"><span data-stu-id="218a5-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="218a5-154">Þessi gagnaheimild vísar til Intrastat töflunnar og kveikt er á valkostinum **Á milli fyrirtækja** fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="218a5-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="218a5-155">Þegar gagnaveita er kölluð sem hefur verið stillt sem segðin `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, inniheldur endanleg SQL-skipun eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="218a5-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="218a5-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="218a5-156">Additional resources</span></span>

[<span data-ttu-id="218a5-157">Rökfræðiaðgerðir</span><span class="sxs-lookup"><span data-stu-id="218a5-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="218a5-158">VALUEINLARGE aðgerðir</span><span class="sxs-lookup"><span data-stu-id="218a5-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)

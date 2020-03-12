---
title: LISTOFFIELDS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTOFFIELDS í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041999"
---
# <span data-ttu-id="c7a21-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="c7a21-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7a21-104">Aðgerðin `LISTOFFIELDS` skilar *Skráalista*-gildi sem er stofnað byggt á skipulagi tilgreindrar segðar af gerðinni *Upptalning* eða *Ílát (skrá)*.</span><span class="sxs-lookup"><span data-stu-id="c7a21-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c7a21-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="c7a21-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="c7a21-106">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="c7a21-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="c7a21-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="c7a21-107">Arguments</span></span>

<span data-ttu-id="c7a21-108">`path`: Tilvísun í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="c7a21-108">`path`: Data source reference</span></span>

<span data-ttu-id="c7a21-109">Gild tilvísunarslóð gagnagjafa af einni af eftirfarandi gagnagerðum:</span><span class="sxs-lookup"><span data-stu-id="c7a21-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="c7a21-110">Tölusetning líkans</span><span class="sxs-lookup"><span data-stu-id="c7a21-110">Model enumeration</span></span>
- <span data-ttu-id="c7a21-111">Tölusetning sniðs</span><span class="sxs-lookup"><span data-stu-id="c7a21-111">Format enumeration</span></span>
- <span data-ttu-id="c7a21-112">Upptalning forrita</span><span class="sxs-lookup"><span data-stu-id="c7a21-112">Application enumeration</span></span>
- <span data-ttu-id="c7a21-113">Gámur (skrá)</span><span class="sxs-lookup"><span data-stu-id="c7a21-113">Container (record)</span></span>

<span data-ttu-id="c7a21-114">`language`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c7a21-114">`language`: *String*</span></span>

<span data-ttu-id="c7a21-115">Texti sem táknar tungumálakóða.</span><span class="sxs-lookup"><span data-stu-id="c7a21-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7a21-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="c7a21-116">Return values</span></span>

<span data-ttu-id="c7a21-117">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="c7a21-117">*Record list*</span></span>

<span data-ttu-id="c7a21-118">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="c7a21-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c7a21-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="c7a21-119">Usage notes</span></span>

<span data-ttu-id="c7a21-120">Listinn sem er búinn til samanstendur af færslum sem hafa eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="c7a21-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="c7a21-121">**Heiti** (gagnagerðin *Strengur*)</span><span class="sxs-lookup"><span data-stu-id="c7a21-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="c7a21-122">**Merki** (gagnagerðin *Strengur*)</span><span class="sxs-lookup"><span data-stu-id="c7a21-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="c7a21-123">**Lýsing** (gagnagerðin *Strengur*)</span><span class="sxs-lookup"><span data-stu-id="c7a21-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="c7a21-124">**IsTranslated** (gagnagerðin *Boolean*)</span><span class="sxs-lookup"><span data-stu-id="c7a21-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="c7a21-125">Ef frumbreytan `path` vísar til gagnagjafa af gerðinni *Gámur (skrá)* er nýrri skrá bætt við listann sem var stofnaður fyrir hvern reit í gámaskránni sem vísað er til.</span><span class="sxs-lookup"><span data-stu-id="c7a21-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="c7a21-126">Fyrir hverja skrá sem er búin til skilar reiturinn **Heiti** heitinu á reit tilvísaðrar gámaskráar sem núverandi skrá var búin til fyrir.</span><span class="sxs-lookup"><span data-stu-id="c7a21-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="c7a21-127">Ef frumbreytan `path` vísar til gagnagjafa eins af gerðunum *Upptalning* er nýrri skrá bætt við listann sem var stofnaður fyrir hvert upptalningargildi í upptalningunni sem vísað er til.</span><span class="sxs-lookup"><span data-stu-id="c7a21-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="c7a21-128">Fyrir hverja skrá sem er búin til skilar reiturinn **Heiti** gildi tilvísunarupptalningarinnar sem núverandi skrá var stofnuð fyrir, reiturinn **Lýsing** skilar lýsingunni á þeirri upptalningu og reiturinn **Merki** skilar merki þeirrar upptalningar.</span><span class="sxs-lookup"><span data-stu-id="c7a21-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="c7a21-129">Á keyrslutíma, þegar málskipan 1 er notuð, verða reitirnir **Merki** og **Lýsing** að skila gildum sem eru byggðir á tungumálastillingum í sniði rafrænnar skýrslugerðar (ER) sem er í keyrslu:</span><span class="sxs-lookup"><span data-stu-id="c7a21-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="c7a21-130">Ef merki og lýsingar fyrir umbeðið tungumál eru í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á því tungumáli og reiturinn **IsTranslated** skilar **True**.</span><span class="sxs-lookup"><span data-stu-id="c7a21-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="c7a21-131">Ef merki og lýsingar fyrir umbeðið tungumál eru ekki í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á sjálfgefnu tungumáli **EN-US** og reiturinn **IsTranslated** skilar **False**.</span><span class="sxs-lookup"><span data-stu-id="c7a21-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="c7a21-132">Á keyrslutíma, þegar málskipan 2 er notuð, verða reitirnir **Merki** og **Lýsing** að skila gildum sem eru byggðir á tungumáli sem er skilgreint sem seinni frumgerð kallaðrar aðgerðar:</span><span class="sxs-lookup"><span data-stu-id="c7a21-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="c7a21-133">Ef merki og lýsingar fyrir umbeðið tungumál eru í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á því tungumáli og reiturinn **IsTranslated** skilar **True**.</span><span class="sxs-lookup"><span data-stu-id="c7a21-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="c7a21-134">Ef merki og lýsingar fyrir umbeðið tungumál eru ekki í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á tungumáli **EN-US** og reiturinn **IsTranslated** skilar **False**.</span><span class="sxs-lookup"><span data-stu-id="c7a21-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="c7a21-135">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="c7a21-135">Example 1</span></span>

<span data-ttu-id="c7a21-136">Í eftirfarandi mynd er kynnt upptalning í ER-gagnalíkönum.</span><span class="sxs-lookup"><span data-stu-id="c7a21-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="c7a21-137">Eftirfarandi mynd sýnir þessar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="c7a21-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="c7a21-138">Upptalning líkans er sett í skýrslu sem gagnagjafi.</span><span class="sxs-lookup"><span data-stu-id="c7a21-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="c7a21-139">Segð rafrænnar skýrslugerðar notar tölusetningarlíkanið sem breytu á `LISTOFFIELDS`-aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="c7a21-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="c7a21-140">Gagnagjafi af gerðinni *skráalisti* er settur í skýrslu með því að nota stofnaða segð rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="c7a21-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="c7a21-141">Eftirfarandi dæmi sýnir sniðseiningar rafrænnar skýrslugerðar sem eru bundin við gagnagjafa af gerðinni *skráalisti* sem var búin til með því að nota `LISTOFFIELDS`-aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="c7a21-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="c7a21-142">Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="c7a21-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="c7a21-143">Byggt á tungumálastillingum á yfirsniðseiningum **FILE** og **FOLDER**, er þýddur texti fyrir merki og lýsingar sleginn inn sem úttak ER-sniðs.</span><span class="sxs-lookup"><span data-stu-id="c7a21-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="c7a21-144">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="c7a21-144">Example 2</span></span>

<span data-ttu-id="c7a21-145">Þú notar gagnagjafagerðina *Útreiknað svæði* til að stilla gagnagjafa **enumType\_de** og **enumType\_deCH** fyrir tölusetningu gagnalíkansins **enumType**:</span><span class="sxs-lookup"><span data-stu-id="c7a21-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="c7a21-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="c7a21-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="c7a21-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="c7a21-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="c7a21-148">Í þessu tilfelli er hægt að nota eftirfarandi segð til að fá merkið á tölusetningargildinu á svissneskri þýsku, ef sú þýðing er í boði.</span><span class="sxs-lookup"><span data-stu-id="c7a21-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="c7a21-149">Ef svissnesk þýska þýðingin er ekki tiltæk er merkið á þýsku.</span><span class="sxs-lookup"><span data-stu-id="c7a21-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="c7a21-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c7a21-150">Additional resources</span></span>

[<span data-ttu-id="c7a21-151">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="c7a21-151">List functions</span></span>](er-functions-category-list.md)

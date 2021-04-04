---
title: LISTOFFIELDS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTOFFIELDS í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 494dc347fadf44121c7eae0acf8c30768c58f035
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567665"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="06974-103">LISTOFFIELDS ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="06974-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06974-104">Aðgerðin `LISTOFFIELDS` skilar *Skráalista*-gildi sem er stofnað byggt á skipulagi tilgreindrar segðar af gerðinni *Upptalning* eða *Ílát (skrá)*.</span><span class="sxs-lookup"><span data-stu-id="06974-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="06974-105">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="06974-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="06974-106">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="06974-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="06974-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="06974-107">Arguments</span></span>

<span data-ttu-id="06974-108">`path`: Tilvísun í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="06974-108">`path`: Data source reference</span></span>

<span data-ttu-id="06974-109">Gild tilvísunarslóð gagnagjafa af einni af eftirfarandi gagnagerðum:</span><span class="sxs-lookup"><span data-stu-id="06974-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="06974-110">Tölusetning líkans</span><span class="sxs-lookup"><span data-stu-id="06974-110">Model enumeration</span></span>
- <span data-ttu-id="06974-111">Tölusetning sniðs</span><span class="sxs-lookup"><span data-stu-id="06974-111">Format enumeration</span></span>
- <span data-ttu-id="06974-112">Upptalning forrita</span><span class="sxs-lookup"><span data-stu-id="06974-112">Application enumeration</span></span>
- <span data-ttu-id="06974-113">Gámur (skrá)</span><span class="sxs-lookup"><span data-stu-id="06974-113">Container (record)</span></span>

<span data-ttu-id="06974-114">`language`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="06974-114">`language`: *String*</span></span>

<span data-ttu-id="06974-115">Texti sem táknar tungumálakóða.</span><span class="sxs-lookup"><span data-stu-id="06974-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="06974-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="06974-116">Return values</span></span>

<span data-ttu-id="06974-117">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="06974-117">*Record list*</span></span>

<span data-ttu-id="06974-118">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="06974-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="06974-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="06974-119">Usage notes</span></span>

<span data-ttu-id="06974-120">Listinn sem er búinn til samanstendur af færslum sem hafa eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="06974-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="06974-121">**Heiti** (gagnagerðin *Strengur*)</span><span class="sxs-lookup"><span data-stu-id="06974-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="06974-122">**Merki** (gagnagerðin *Strengur*)</span><span class="sxs-lookup"><span data-stu-id="06974-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="06974-123">**Lýsing** (gagnagerðin *Strengur*)</span><span class="sxs-lookup"><span data-stu-id="06974-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="06974-124">**IsTranslated** (gagnagerðin *Boolean*)</span><span class="sxs-lookup"><span data-stu-id="06974-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="06974-125">Ef frumbreytan `path` vísar til gagnagjafa af gerðinni *Gámur (skrá)* er nýrri skrá bætt við listann sem var stofnaður fyrir hvern reit í gámaskránni sem vísað er til.</span><span class="sxs-lookup"><span data-stu-id="06974-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="06974-126">Fyrir hverja skrá sem er búin til skilar reiturinn **Heiti** heitinu á reit tilvísaðrar gámaskráar sem núverandi skrá var búin til fyrir.</span><span class="sxs-lookup"><span data-stu-id="06974-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="06974-127">Ef frumbreytan `path` vísar til gagnagjafa eins af gerðunum *Upptalning* er nýrri skrá bætt við listann sem var stofnaður fyrir hvert upptalningargildi í upptalningunni sem vísað er til.</span><span class="sxs-lookup"><span data-stu-id="06974-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="06974-128">Fyrir hverja skrá sem er búin til skilar reiturinn **Heiti** gildi tilvísunarupptalningarinnar sem núverandi skrá var stofnuð fyrir, reiturinn **Lýsing** skilar lýsingunni á þeirri upptalningu og reiturinn **Merki** skilar merki þeirrar upptalningar.</span><span class="sxs-lookup"><span data-stu-id="06974-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="06974-129">Á keyrslutíma, þegar málskipan 1 er notuð, verða reitirnir **Merki** og **Lýsing** að skila gildum sem eru byggðir á tungumálastillingum í sniði rafrænnar skýrslugerðar (ER) sem er í keyrslu:</span><span class="sxs-lookup"><span data-stu-id="06974-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="06974-130">Ef merki og lýsingar fyrir umbeðið tungumál eru í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á því tungumáli og reiturinn **IsTranslated** skilar **True**.</span><span class="sxs-lookup"><span data-stu-id="06974-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="06974-131">Ef merki og lýsingar fyrir umbeðið tungumál eru ekki í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á sjálfgefnu tungumáli **EN-US** og reiturinn **IsTranslated** skilar **False**.</span><span class="sxs-lookup"><span data-stu-id="06974-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="06974-132">Á keyrslutíma, þegar málskipan 2 er notuð, verða reitirnir **Merki** og **Lýsing** að skila gildum sem eru byggðir á tungumáli sem er skilgreint sem seinni frumgerð kallaðrar aðgerðar:</span><span class="sxs-lookup"><span data-stu-id="06974-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="06974-133">Ef merki og lýsingar fyrir umbeðið tungumál eru í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á því tungumáli og reiturinn **IsTranslated** skilar **True**.</span><span class="sxs-lookup"><span data-stu-id="06974-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="06974-134">Ef merki og lýsingar fyrir umbeðið tungumál eru ekki í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á tungumáli **EN-US** og reiturinn **IsTranslated** skilar **False**.</span><span class="sxs-lookup"><span data-stu-id="06974-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="06974-135">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="06974-135">Example 1</span></span>

<span data-ttu-id="06974-136">Í eftirfarandi mynd er kynnt upptalning í ER-gagnalíkönum.</span><span class="sxs-lookup"><span data-stu-id="06974-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="06974-137">Eftirfarandi mynd sýnir þessar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="06974-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="06974-138">Upptalning líkans er sett í skýrslu sem gagnagjafi.</span><span class="sxs-lookup"><span data-stu-id="06974-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="06974-139">Segð rafrænnar skýrslugerðar notar tölusetningarlíkanið sem breytu á `LISTOFFIELDS`-aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="06974-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="06974-140">Gagnagjafi af gerðinni *skráalisti* er settur í skýrslu með því að nota stofnaða segð rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="06974-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="06974-141">Eftirfarandi dæmi sýnir sniðseiningar rafrænnar skýrslugerðar sem eru bundin við gagnagjafa af gerðinni *skráalisti* sem var búin til með því að nota `LISTOFFIELDS`-aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="06974-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="06974-142">Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="06974-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="06974-143">Byggt á tungumálastillingum á yfirsniðseiningum **FILE** og **FOLDER**, er þýddur texti fyrir merki og lýsingar sleginn inn sem úttak ER-sniðs.</span><span class="sxs-lookup"><span data-stu-id="06974-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="06974-144">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="06974-144">Example 2</span></span>

<span data-ttu-id="06974-145">Þú notar gagnagjafagerðina *Útreiknað svæði* til að stilla gagnagjafa **enumType\_de** og **enumType\_deCH** fyrir tölusetningu gagnalíkansins **enumType**:</span><span class="sxs-lookup"><span data-stu-id="06974-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="06974-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="06974-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="06974-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="06974-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="06974-148">Í þessu tilfelli er hægt að nota eftirfarandi segð til að fá merkið á tölusetningargildinu á svissneskri þýsku, ef sú þýðing er í boði.</span><span class="sxs-lookup"><span data-stu-id="06974-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="06974-149">Ef svissnesk þýska þýðingin er ekki tiltæk er merkið á þýsku.</span><span class="sxs-lookup"><span data-stu-id="06974-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="06974-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="06974-150">Additional resources</span></span>

[<span data-ttu-id="06974-151">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="06974-151">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
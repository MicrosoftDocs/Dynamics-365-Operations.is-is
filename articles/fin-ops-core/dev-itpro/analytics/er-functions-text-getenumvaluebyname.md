---
title: GETENUMVALUEBYNAME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETNUMVALUEBYNAME í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: 722ea8ea233d617b0584e21e98073428f16c0801
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885228"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="6a646-103">GETENUMVALUEBYNAME ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="6a646-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a646-104">Aðgerðin `GETENUMVALUEBYNAME` leitar að tilteknu *Enum*-gildi í tilgreindum tölusetningargagnagjafa með því að nota tölusetningarheitið sem er tilgreint sem *Strengja*-gildi.</span><span class="sxs-lookup"><span data-stu-id="6a646-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="6a646-105">Ef *Enum*-gildi finnst skilar aðgerðin því.</span><span class="sxs-lookup"><span data-stu-id="6a646-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="6a646-106">Að öðrum kosti skilar aðgerðin upptalningargildinu **núll**.</span><span class="sxs-lookup"><span data-stu-id="6a646-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a646-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="6a646-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="6a646-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="6a646-108">Arguments</span></span>

<span data-ttu-id="6a646-109">`enumeration data source path`: *Upptalning*</span><span class="sxs-lookup"><span data-stu-id="6a646-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="6a646-110">Gild slóð gagnagjafa af einni af eftirfarandi upptalningargerðum:</span><span class="sxs-lookup"><span data-stu-id="6a646-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="6a646-111">Líkanaupptalning rafrænnar skýrslugerðar (ER)</span><span class="sxs-lookup"><span data-stu-id="6a646-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="6a646-112">Upptalning ER-sniðs</span><span class="sxs-lookup"><span data-stu-id="6a646-112">ER format enumeration</span></span>
- <span data-ttu-id="6a646-113">Upptalning Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="6a646-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="6a646-114">`enumeration value text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="6a646-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="6a646-115">Strengagildi sem táknar heiti staks upptalningargildis.</span><span class="sxs-lookup"><span data-stu-id="6a646-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="6a646-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="6a646-116">Return values</span></span>

<span data-ttu-id="6a646-117">Má vera núll *Enum*</span><span class="sxs-lookup"><span data-stu-id="6a646-117">Nullable *Enum*</span></span>

<span data-ttu-id="6a646-118">Upptalningargildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="6a646-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6a646-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="6a646-119">Usage notes</span></span>

<span data-ttu-id="6a646-120">Engin undantekning er gerð ef gildið *Enum* er ekki að finna með því að nota heiti upptalningargildisins sem er tilgreint sem gildið *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="6a646-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="6a646-121">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="6a646-121">Example 1</span></span>

<span data-ttu-id="6a646-122">Í eftirfarandi mynd er **ReportDirection** upptalningin kynnt í gagnalíkani.</span><span class="sxs-lookup"><span data-stu-id="6a646-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="6a646-123">Athugaðu að merki eru skilgreind fyrir tölusetningargildin.</span><span class="sxs-lookup"><span data-stu-id="6a646-123">Notice that labels are defined for the enumeration values.</span></span>

![Tiltæk gildi fyrir tölusetningu gagnalíkans](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="6a646-125">Eftirfarandi mynd sýnir þessar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="6a646-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="6a646-126">Gagnagjafinn **$Direction** er stilltur í ER-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="6a646-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="6a646-127">Þessi gagnagjafi er stilltur út frá líkanaupptalningunni **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="6a646-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="6a646-128">Segðin `$IsArrivals` er hönnuð til að nota líkanatölusetningarbyggðan gagnagjafa **$Direction** sem færibreytu þessarar aðgerðar.</span><span class="sxs-lookup"><span data-stu-id="6a646-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="6a646-129">Gildi þessarar samanburðarsegðar er **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="6a646-129">The value of this comparison expression is **TRUE**.</span></span>

![Dæmi um tölusetningu gagnalíkans](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="6a646-131">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="6a646-131">Example 2</span></span>

<span data-ttu-id="6a646-132">Aðgerðirnar `GETENUMVALUEBYNAME` og [`LISTOFFIELDS`](er-functions-list-listoffields.md) gerir þér kleift að sækja gildi og merki yfir studdar tölusetningar sem textagildi.</span><span class="sxs-lookup"><span data-stu-id="6a646-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="6a646-133">(Studdar tölusetningar eru tölusetningar forrits, tölusetningar gagnalíkans og tölusetningar sniðs.)</span><span class="sxs-lookup"><span data-stu-id="6a646-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="6a646-134">Á eftirfarandi mynd er gagnagjafinn **TransType** kynntur í líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="6a646-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="6a646-135">Þessi gagnagjafi vísar í forritstölusetningu **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="6a646-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Gagnagjafi líkanavörpunar sem vísar í tölusetningu forrits](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="6a646-137">Eftirfarandi mynd sýnir gagnagjafann **TransTypeList** sem er skilgreindur í líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="6a646-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="6a646-138">Þessi gagnagjafi er skilgreindur út frá **TransType** tölusetningu forrits.</span><span class="sxs-lookup"><span data-stu-id="6a646-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="6a646-139">`LISTOFFIELDS`-aðgerðin er notuð til að skila öllum gildum tölusetningar sem lista yfir færslur sem innihalda reiti.</span><span class="sxs-lookup"><span data-stu-id="6a646-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="6a646-140">Á þennan hátt verða upplýsingar um sérhvert gildi tölusetningar sýndar.</span><span class="sxs-lookup"><span data-stu-id="6a646-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="6a646-141">**EnumValue** gildið er skilgreint fyrir **TransTypeList** gagnagjafann með því að nota `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`-segðina.</span><span class="sxs-lookup"><span data-stu-id="6a646-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="6a646-142">Þessi reitur skilar gildi tölusetningar fyrir hverja færslu í þessum lista.</span><span class="sxs-lookup"><span data-stu-id="6a646-142">This field returns an enumeration value for every record in this list.</span></span>

![Gagnagjafi líkanavörpunar sem skilar öllum tölusetningargildum af valinni tölusetningu sem lista yfir færslur](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="6a646-144">Eftirfarandi mynd sýnir gagnagjafann **VendTrans** sem er skilgreindur í líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="6a646-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="6a646-145">Þessi gagnagjafi skilar lánardrottnafærslum úr forritstöflu **VendTrans**.</span><span class="sxs-lookup"><span data-stu-id="6a646-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="6a646-146">Fjárhagsgerð hverrar færslu er skilgreind eftir gildinu á reitnum **TransType**.</span><span class="sxs-lookup"><span data-stu-id="6a646-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="6a646-147">**TransTypeTitle** gildið er skilgreint fyrir **VendTrans** gagnagjafann með því að nota `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`-segðina.</span><span class="sxs-lookup"><span data-stu-id="6a646-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="6a646-148">Þessi reitur skilar merki tölusetningargildis af núverandi færslu sem texta, ef þetta tölusetningargildi er í boði.</span><span class="sxs-lookup"><span data-stu-id="6a646-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="6a646-149">Annars skilar hann auðum streng.</span><span class="sxs-lookup"><span data-stu-id="6a646-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="6a646-150">Reiturinn **TransTypeTitle** er bundinn við **LedgerType** reit gagnalíkans sem gerir kleift að nota þessar upplýsingar í öllum sniðum rafrænnar skýrslugerðar sem notar gagnalíkanið sem upprunastað gagna.</span><span class="sxs-lookup"><span data-stu-id="6a646-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Gagnagjafi líkanavörpunar sem skilar lánardrottnafærslum](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="6a646-152">Eftirfarandi mynd sýnir hvernig hægt er að nota [kembiforrit gagnagjafans](er-debug-data-sources.md) til að prófa skilgreinda líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="6a646-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Nota kembiforrit gagnagjafa til að prófa skilgreinda líkanavörpun](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="6a646-154">**LedgerType** reitur gagnalíkans sýnir merki af færslugerðum eins og búist var við.</span><span class="sxs-lookup"><span data-stu-id="6a646-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="6a646-155">Ef ætlunin er að nota þessa nálgun fyrir mikið magn af færslugögnum verður að íhuga afköst keyrslunnar.</span><span class="sxs-lookup"><span data-stu-id="6a646-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="6a646-156">Frekari upplýsingar er að finna í [Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="6a646-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a646-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6a646-157">Additional resources</span></span>

[<span data-ttu-id="6a646-158">Textaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="6a646-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="6a646-159">Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum</span><span class="sxs-lookup"><span data-stu-id="6a646-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="6a646-160">LISTOFFIELDS ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="6a646-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="6a646-161">FIRSTORNULL ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="6a646-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="6a646-162">WHERE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="6a646-162">WHERE ER function</span></span>](er-functions-list-where.md)

---
title: NUMSEQVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMSEQVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: b513d04bfeb3a37aa0b1703d0fdde040885a5159
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680591"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="b2c62-103">NUMSEQVALUE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="b2c62-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2c62-104">Aðgerðin `NUMSEQVALUE` skilar *strengja*-gildi sem táknar nýtt myndað gildi númeraraðar, byggt á tilgreindri númeraröð, umfangi og umfangskenni.</span><span class="sxs-lookup"><span data-stu-id="b2c62-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="b2c62-105">Umfangskennið jafngildir fyrirtækjakóðanum sem er til staðar í því samhengi sem snið rafrænnar skýrslurgerðar (ER) er keyrt undir.</span><span class="sxs-lookup"><span data-stu-id="b2c62-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b2c62-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="b2c62-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="b2c62-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="b2c62-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="b2c62-108">Málskipun 3</span><span class="sxs-lookup"><span data-stu-id="b2c62-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="b2c62-109">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="b2c62-109">Arguments</span></span>

<span data-ttu-id="b2c62-110">`number sequence code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="b2c62-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="b2c62-111">Textagildi sem táknar kóða númeraraðarinnar sem nýtt gildi er krafist í.</span><span class="sxs-lookup"><span data-stu-id="b2c62-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="b2c62-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="b2c62-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="b2c62-113">Gildið *Int64* sem táknar upptökuskilríki plötunnar í töflunni NumberSequenceTable sem inniheldur skilgreininguna á talnaröðinni sem nýtt gildi er krafist í.</span><span class="sxs-lookup"><span data-stu-id="b2c62-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="b2c62-114">`scope type`: *Upptaln.gildi*</span><span class="sxs-lookup"><span data-stu-id="b2c62-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="b2c62-115">Upptalningargildi upptalningarinnar **ERExpressionNumberSequenceScopeType** sem skilgreinir umfang númeraraðar sem nýtt gildi er krafist í.</span><span class="sxs-lookup"><span data-stu-id="b2c62-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="b2c62-116">Fyrirliggjandi tegundir umfangs eru **Samnýtt**, **Lögaðili** og **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="b2c62-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="b2c62-117">`scope ID`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="b2c62-117">`scope ID`: *String*</span></span>

<span data-ttu-id="b2c62-118">Gildið *Strengur* sem auðkennir umfangið, byggt á tiltekinni umfangsgerð.</span><span class="sxs-lookup"><span data-stu-id="b2c62-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b2c62-119">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="b2c62-119">Return values</span></span>

<span data-ttu-id="b2c62-120">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="b2c62-120">*String*</span></span>

<span data-ttu-id="b2c62-121">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="b2c62-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b2c62-122">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="b2c62-122">Usage notes</span></span>

<span data-ttu-id="b2c62-123">Fyrir umfangsgerðina **Samnýtt** skal tilgreina tóman streng sem umfangskenni.</span><span class="sxs-lookup"><span data-stu-id="b2c62-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="b2c62-124">Fyrir umfangsgerðirnar **Fyrirtækis** og **Lögaðila** skal tilgreina fyrirtækjakóðann sem umfangskennið.</span><span class="sxs-lookup"><span data-stu-id="b2c62-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="b2c62-125">Ef þú tilgreinir tóman streng sem umfangskenni fyrir þessar umfangsgerðir er kóði gildandi fyrirtækis notaður.</span><span class="sxs-lookup"><span data-stu-id="b2c62-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="b2c62-126">Þegar málskipan 1 er notuð er beðið um númeraröð fyrir umfangsgerðina **Fyrirtæki** og fyrirtækjakóðinn er veittur með því samhengi sem ER-sniðið er keyrt undir.</span><span class="sxs-lookup"><span data-stu-id="b2c62-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="b2c62-127">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="b2c62-127">Example 1</span></span>

<span data-ttu-id="b2c62-128">Á ER-sniðinu skilgreinir þú gagnagjafann **AskNumSeq** af gerðinni *Innsláttarfæribreytur notanda*.</span><span class="sxs-lookup"><span data-stu-id="b2c62-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="b2c62-129">Þessi gagnagjafi vísar til framlengdu gagnagerðarinnar (EDT) **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="b2c62-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="b2c62-130">Næst skilgreinirðu gagnagjafann **NumSeq** af gerðinni *Reiknaður reitur*.</span><span class="sxs-lookup"><span data-stu-id="b2c62-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b2c62-131">Þessi gagnaveita inniheldur segðina `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="b2c62-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="b2c62-132">Þegar gagnagjafinn **NumSeq** er kallaður skilar það nýju mynduðu gildi númeraraðar sem var tilgreind á keyrslutíma með því að slá kóðann inn í valmyndina.</span><span class="sxs-lookup"><span data-stu-id="b2c62-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="b2c62-133">Óskað er eftir númeraröð fyrir umfangsgerðina **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="b2c62-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="b2c62-134">Fyrirtækjakóðinn er veittur með því samhengi sem ER-sniðið er keyrt undir.</span><span class="sxs-lookup"><span data-stu-id="b2c62-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="b2c62-135">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="b2c62-135">Example 2</span></span>

<span data-ttu-id="b2c62-136">Eftirfarandi gagnagjafar eru skilgreindir í líkanavörpuninni:</span><span class="sxs-lookup"><span data-stu-id="b2c62-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="b2c62-137">Gagnagjafinn **LegderParms** af gerðinni *Tafla*.</span><span class="sxs-lookup"><span data-stu-id="b2c62-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="b2c62-138">Þessi gagnagjafi vísar til LedgerParameters töflunnar.</span><span class="sxs-lookup"><span data-stu-id="b2c62-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="b2c62-139">Gagnagjafinn **NumSeq** af gerðinni *Reiknaður reitur*.</span><span class="sxs-lookup"><span data-stu-id="b2c62-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b2c62-140">Þessi gagnaveita inniheldur segðina `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="b2c62-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="b2c62-141">Þegar **NumSeq** gagnaveitan er kölluð skilar hún nýmynduðu gildi númeraraðarinnar sem hefur verið skilgreint í fjárhagsfæribreytum fyrir fyrirtækið sem leggur til samhengið sem ER-sniði er keyrt undir.</span><span class="sxs-lookup"><span data-stu-id="b2c62-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="b2c62-142">Þessi númeraröð auðkennir færslubókina á einkvæman hátt og vinnur sem lotunúmer sem tengir færslurnar saman.</span><span class="sxs-lookup"><span data-stu-id="b2c62-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="b2c62-143">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="b2c62-143">Example 3</span></span>

<span data-ttu-id="b2c62-144">Eftirfarandi gagnagjafar eru skilgreindir í líkanavörpuninni:</span><span class="sxs-lookup"><span data-stu-id="b2c62-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="b2c62-145">Gagnagjafinn **enumScope** af Microsoft Dynamics 365 Finance gerðinni *upptalning*.</span><span class="sxs-lookup"><span data-stu-id="b2c62-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="b2c62-146">Þessi gagnagjafi vísar til upptalningarinnar **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="b2c62-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="b2c62-147">Gagnagjafinn **NumSeq** af gerðinni *Reiknaður reitur*.</span><span class="sxs-lookup"><span data-stu-id="b2c62-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b2c62-148">Þessi gagnaveita inniheldur segðina `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="b2c62-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="b2c62-149">Þegar **NumSeq** gagnaveitan er kölluð skilar hún nýmynduðu gildi **Gene\_1** númeraröðarinnar sem hefur verið skilgreint fyrir fyrirtækið sem leggur til samhengið sem ER-sniði er keyrt undir.</span><span class="sxs-lookup"><span data-stu-id="b2c62-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2c62-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b2c62-150">Additional resources</span></span>

[<span data-ttu-id="b2c62-151">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="b2c62-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

---
title: Rafræn skýrslugerðarvirkni LISTDISTINCT
description: Í þessu efnisatriði er að finna upplýsingar um hvernig rafræn skýrslugerðarvirkni LISTDISTINCT er notuð.
author: NickSelin
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 9ab9354b0fdb1c08c192b90e6bab303cb85ea41a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743824"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="ce232-103">Rafræn skýrslugerðarvirkni LISTDISTINCT</span><span class="sxs-lookup"><span data-stu-id="ce232-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ce232-104">Virknin `LISTDISTINCT` reiknar tilgreinda segð sem val fyrir hverja færslu í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="ce232-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="ce232-105">Hún skilar nýju gildi *Færslulista* sem inniheldur eina færslu fyrir hvert einkvæmt valgildi.</span><span class="sxs-lookup"><span data-stu-id="ce232-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce232-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="ce232-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="ce232-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="ce232-107">Arguments</span></span>

<span data-ttu-id="ce232-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="ce232-108">`list`: *Record list*</span></span>

<span data-ttu-id="ce232-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="ce232-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ce232-110">`selector`: *Frumstæð gagnagerð*</span><span class="sxs-lookup"><span data-stu-id="ce232-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="ce232-111">Gild segð sem notuð er til að reikna valgildi fyrir hverja færslu í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="ce232-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="ce232-112">Eftirfarandi gagnagerðir eru studdar fyrir þessa færibreytu:</span><span class="sxs-lookup"><span data-stu-id="ce232-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="ce232-113">Boole</span><span class="sxs-lookup"><span data-stu-id="ce232-113">Boolean</span></span>
- <span data-ttu-id="ce232-114">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="ce232-114">Date</span></span>
- <span data-ttu-id="ce232-115">DateTime-gildi</span><span class="sxs-lookup"><span data-stu-id="ce232-115">DateTime</span></span>
- <span data-ttu-id="ce232-116">Guid</span><span class="sxs-lookup"><span data-stu-id="ce232-116">GUID</span></span>
- <span data-ttu-id="ce232-117">Heiltala</span><span class="sxs-lookup"><span data-stu-id="ce232-117">Integer</span></span>
- <span data-ttu-id="ce232-118">Int64</span><span class="sxs-lookup"><span data-stu-id="ce232-118">Int64</span></span>
- <span data-ttu-id="ce232-119">Rauntala</span><span class="sxs-lookup"><span data-stu-id="ce232-119">Real</span></span>
- <span data-ttu-id="ce232-120">Strengur</span><span class="sxs-lookup"><span data-stu-id="ce232-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="ce232-121">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ce232-121">Return values</span></span>

<span data-ttu-id="ce232-122">*Færslulisti*</span><span class="sxs-lookup"><span data-stu-id="ce232-122">*Record list*</span></span>

<span data-ttu-id="ce232-123">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="ce232-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ce232-124">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="ce232-124">Usage notes</span></span>

<span data-ttu-id="ce232-125">Skipulagið á listanum sem er stofnaður samsvarar skipulagi tilgreinda listans.</span><span class="sxs-lookup"><span data-stu-id="ce232-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="ce232-126">Sama valgildið kann að vera reiknað út fyrir margar færslur í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="ce232-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="ce232-127">Í þessu tilfelli samsvara reitargildi samsvarandi færslu í stofnaða listanum gildum fyrstu færslunnar úr tilgreindum lista sem valgildið er reiknað út fyrir.</span><span class="sxs-lookup"><span data-stu-id="ce232-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="ce232-128">Framkvæmd þessarar virkni er gerð í hvaða gagnagjafa [Rafrænnar skýrslugerðar](general-electronic-reporting.md) sem er af gerðinni *Færslulisti* sem er til staðar í minni.</span><span class="sxs-lookup"><span data-stu-id="ce232-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="ce232-129">Einnig er hægt að nota gagnagjafann **GROUPBY** til að búa til lista yfir færslur sem valið sem er með sérstæð gildi er reiknað fyrir.</span><span class="sxs-lookup"><span data-stu-id="ce232-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="ce232-130">Hins vegar, séð út frá afköstum og minnisnotkun, er betra að nota virknina `LISTDISTINCT` í stað gagnagjafans **GROUPBY** vegna þess að virknin er keyrð í minni.</span><span class="sxs-lookup"><span data-stu-id="ce232-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="ce232-131">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ce232-131">Example</span></span>

<span data-ttu-id="ce232-132">Eftirfarandi dæmi sýnir hvernig hægt er að fá listann yfir einkvæmt númer viðskiptavinalykils sem að minnsta kosti einn sölureikningur eða verkreikningur hefur verið gefinn út á yfir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="ce232-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="ce232-133">Færið inn gagnagjafann **SalesInvoice** af gerðinni `Record list` sem vísar í jöfnunartöfluna **CustInvoiceJour** og síar sölureikninga fyrir ákveðin tímabil.</span><span class="sxs-lookup"><span data-stu-id="ce232-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="ce232-134">Svæðið `InvoiceAccount` í þessum gagnagjafa skilar lykilnúmeri reikningsfærðs viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ce232-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="ce232-135">Færið inn gagnagjafann **ProjectInvoice** af gerðinni `Record list` sem vísar í jöfnunartöfluna **ProjInvoiceJour** og síar verkeikninga fyrir ákveðin tímabil.</span><span class="sxs-lookup"><span data-stu-id="ce232-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="ce232-136">Svæðið `InvoiceAccount` í þessum gagnagjafa skilar lykilnúmeri reikningsfærðs viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ce232-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="ce232-137">Skilgreinið gagnagjafann **AllInvoices** af gerðinni `Calculated field` sem inniheldur segðina `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="ce232-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="ce232-138">Þessi gagnagjafi skilar sameinaða listanum yfir sölureikninga og verkreikninga.</span><span class="sxs-lookup"><span data-stu-id="ce232-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="ce232-139">Skilgreinið gagnagjafann **InvoicedCustomer** af gerðinni `Record list` sem inniheldur segðina `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="ce232-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="ce232-140">Þessi gagnagjafi skilar nýjum lista sem inniheldur eina færslu fyrir hvern einkvæman viðskiptavin sem hefur verið reikningsfærður á skilgreindu tímabili.</span><span class="sxs-lookup"><span data-stu-id="ce232-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="ce232-141">Svæðið `InvoiceAccount` í þessum lista inniheldur númer viðskiptavinalykils.</span><span class="sxs-lookup"><span data-stu-id="ce232-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce232-142">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ce232-142">Additional resources</span></span>

[<span data-ttu-id="ce232-143">Listaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="ce232-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: ALLITEMSQUERY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ALLITEMSQUERY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 647019a103006c8b74bc26885c51f5372dcf0c42
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917512"
---
# <span data-ttu-id="53c1d-103"><a name="ALLITEMSQUERY">ALLITEMSQUERY ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="53c1d-103"><a name="ALLITEMSQUERY">ALLITEMSQUERY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53c1d-104">Aðgerðin `ALLITEMSQUERY` keyrir sem sameinuð SQL-fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="53c1d-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="53c1d-105">Það skilar nýju flöttu gildi *Skráalista* sem samanstendur af lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð.</span><span class="sxs-lookup"><span data-stu-id="53c1d-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c1d-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="53c1d-106">Syntax</span></span>

```
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="53c1d-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="53c1d-107">Arguments</span></span>

<span data-ttu-id="53c1d-108">`path`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="53c1d-108">`path`: *Record list*</span></span>

<span data-ttu-id="53c1d-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="53c1d-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="53c1d-110">Hann verður að innihalda að minnsta kosti ein tengsl.</span><span class="sxs-lookup"><span data-stu-id="53c1d-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="53c1d-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="53c1d-111">Return values</span></span>

<span data-ttu-id="53c1d-112">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="53c1d-112">*Record list*</span></span>

<span data-ttu-id="53c1d-113">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="53c1d-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="53c1d-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="53c1d-114">Usage notes</span></span>

<span data-ttu-id="53c1d-115">Tilgreind slóð verður að vera skilgreind sem gild slóð gagnagjafa á gagnagjafaþætti af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="53c1d-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="53c1d-116">Hann verður einnig að innihalda að minnsta kosti ein tengsl.</span><span class="sxs-lookup"><span data-stu-id="53c1d-116">It must also contain at least one relation.</span></span> <span data-ttu-id="53c1d-117">Gagnaeiningar eins og slóðin *Strengur* og *Dagsetning* ættu að gefa upp villu í segðasmíði rafrænnar skýrslugerðar (ER) á tíma hönnunar.</span><span class="sxs-lookup"><span data-stu-id="53c1d-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="53c1d-118">Þegar þessari aðgerð er beitt á gagnagjafa af gagnagerðinni *Skráalisti* sem vísar til forritshlutar sem hægt er að kalla beint með því að nota SQL (til dæmis töflu, einingu eða fyrirspurn) keyrir hún sem sameinuð SQL-fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="53c1d-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="53c1d-119">Annars keyrir það í minni sem aðgerðin [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="53c1d-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="53c1d-120">Dæmi</span><span class="sxs-lookup"><span data-stu-id="53c1d-120">Example</span></span>

<span data-ttu-id="53c1d-121">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="53c1d-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="53c1d-122">Gagnagjafinn **CustInv** af gerðinni *Töfluskrár* sem vísar til töflunnar CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="53c1d-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="53c1d-123">Gagnagjafinn **FilteredInv** af gerðnni *Reiknað svæði* sem inniheldur segðina `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="53c1d-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="53c1d-124">Gagnagjafinn **JourLines** af gerðnni *Reiknað svæði* sem inniheldur segðina `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="53c1d-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="53c1d-125">Þegar þú keyrir líkanavörpunina til að kalla á gagnagjafann **JourLines** keyrist eftirfarandi SQL-skipun:</span><span class="sxs-lookup"><span data-stu-id="53c1d-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="53c1d-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="53c1d-126">Additional resources</span></span>

[<span data-ttu-id="53c1d-127">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="53c1d-127">List functions</span></span>](er-functions-category-list.md)

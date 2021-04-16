---
title: ALLITEMSQUERY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ALLITEMSQUERY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746700"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="68339-103">ALLITEMSQUERY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="68339-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68339-104">Aðgerðin `ALLITEMSQUERY` keyrir sem sameinuð SQL-fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="68339-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="68339-105">Það skilar nýju flöttu gildi *Skráalista* sem samanstendur af lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð.</span><span class="sxs-lookup"><span data-stu-id="68339-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="68339-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="68339-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="68339-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="68339-107">Arguments</span></span>

<span data-ttu-id="68339-108">`path`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="68339-108">`path`: *Record list*</span></span>

<span data-ttu-id="68339-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="68339-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="68339-110">Hann verður að innihalda að minnsta kosti ein tengsl.</span><span class="sxs-lookup"><span data-stu-id="68339-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="68339-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="68339-111">Return values</span></span>

<span data-ttu-id="68339-112">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="68339-112">*Record list*</span></span>

<span data-ttu-id="68339-113">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="68339-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="68339-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="68339-114">Usage notes</span></span>

<span data-ttu-id="68339-115">Tilgreind slóð verður að vera skilgreind sem gild slóð gagnagjafa á gagnagjafaþætti af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="68339-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="68339-116">Hann verður einnig að innihalda að minnsta kosti ein tengsl.</span><span class="sxs-lookup"><span data-stu-id="68339-116">It must also contain at least one relation.</span></span> <span data-ttu-id="68339-117">Gagnaeiningar eins og slóðin *Strengur* og *Dagsetning* ættu að gefa upp villu í segðasmíði rafrænnar skýrslugerðar (ER) á tíma hönnunar.</span><span class="sxs-lookup"><span data-stu-id="68339-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="68339-118">Þegar þessari aðgerð er beitt á gagnagjafa af gagnagerðinni *Skráalisti* sem vísar til forritshlutar sem hægt er að kalla beint með því að nota SQL (til dæmis töflu, einingu eða fyrirspurn) keyrir hún sem sameinuð SQL-fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="68339-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="68339-119">Annars keyrir það í minni sem aðgerðin [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="68339-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="68339-120">Dæmi</span><span class="sxs-lookup"><span data-stu-id="68339-120">Example</span></span>

<span data-ttu-id="68339-121">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="68339-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="68339-122">Gagnagjafinn **CustInv** af gerðinni *Töfluskrár* sem vísar til töflunnar CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="68339-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="68339-123">Gagnagjafinn **FilteredInv** af gerðnni *Reiknað svæði* sem inniheldur segðina `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="68339-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="68339-124">Gagnagjafinn **JourLines** af gerðnni *Reiknað svæði* sem inniheldur segðina `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="68339-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="68339-125">Þegar þú keyrir líkanavörpunina til að kalla á gagnagjafann **JourLines** keyrist eftirfarandi SQL-skipun:</span><span class="sxs-lookup"><span data-stu-id="68339-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="68339-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="68339-126">Additional resources</span></span>

[<span data-ttu-id="68339-127">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="68339-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
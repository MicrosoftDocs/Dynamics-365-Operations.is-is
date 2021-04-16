---
title: FILTER ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FILTER í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746604"
---
# <a name="filter-er-function"></a><span data-ttu-id="6803b-103">FILTER ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="6803b-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6803b-104">Aðgerðin `FILTER` skilar tilgreindum lista sem *Skráalista*-gildi eftir að fyrirspurninni hefur verið breytt þannig að hún síar að tilteknu ástandi.</span><span class="sxs-lookup"><span data-stu-id="6803b-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6803b-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="6803b-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="6803b-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="6803b-106">Arguments</span></span>

<span data-ttu-id="6803b-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="6803b-107">`list`: *Record list*</span></span>

<span data-ttu-id="6803b-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="6803b-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="6803b-109">`condition`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="6803b-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="6803b-110">Gild skilyrt tjáning sem er notuð til að sía skrár yfir tiltekinn lista.</span><span class="sxs-lookup"><span data-stu-id="6803b-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="6803b-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="6803b-111">Return values</span></span>

<span data-ttu-id="6803b-112">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="6803b-112">*Record list*</span></span>

<span data-ttu-id="6803b-113">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="6803b-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6803b-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="6803b-114">Usage notes</span></span>

<span data-ttu-id="6803b-115">Þessi aðgerð er frábrugðin [WHERE](er-functions-list-where.md) aðgerðinni, vegna þess að tilgreint skilyrði er beitt á hvaða gagnagjafa rafrænnar skýrslugerðar (ER) af gerðinni *Töflufærslur* á gagnagrunnsstigi.</span><span class="sxs-lookup"><span data-stu-id="6803b-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="6803b-116">Listinn og forsendurnar er hægt að skilgreina með því að nota töflur og samskipti.</span><span class="sxs-lookup"><span data-stu-id="6803b-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="6803b-117">Ef ein eða báðar frumbreyturnar sem eru stilltar fyrir þessa aðgerð (`list` og `condition`) leyfa ekki að þýða þessa beiðni yfir í beint SQL-kall er gerð undantekning á hönnunartíma.</span><span class="sxs-lookup"><span data-stu-id="6803b-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="6803b-118">Þessi undantekning upplýsir notandann um að ekki sé hægt að nota annaðhvort `list` eða `condition` til að spyrjast fyrir um gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="6803b-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="6803b-119">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="6803b-119">Example 1</span></span>

<span data-ttu-id="6803b-120">Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar til VendTable-töflunnar skilar segðin `FILTER (Vendors, Vendors.VendGroup = "40")` lista yfir aðeins lánardrottna sem tilheyra lánardrottnaflokki 40.</span><span class="sxs-lookup"><span data-stu-id="6803b-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="6803b-121">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="6803b-121">Example 2</span></span>

<span data-ttu-id="6803b-122">Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar í VendTable-töfluna og ef **parmVendorBankGroup** er stillt sem ER-gagnagjafi sem skilar gildi af gagnagerðinni *Strengur* skilar segðin `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` lista yfir aðeins lánardrottnalykla sem tilheyra tilteknum bankaflokk.</span><span class="sxs-lookup"><span data-stu-id="6803b-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="6803b-123">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="6803b-123">Example 3</span></span>

<span data-ttu-id="6803b-124">Þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="6803b-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="6803b-125">Síðan slærðu inn aðra segð, `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="6803b-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="6803b-126">Þegar þú reynir að vista þessa segð í ER-formúluhönnuðinum er eftirfarandi undantekning gerð: "Staðfestingarvilla: Listasegðin í FILTER-aðgerð er ekki fyrirspurn."</span><span class="sxs-lookup"><span data-stu-id="6803b-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6803b-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6803b-127">Additional resources</span></span>

[<span data-ttu-id="6803b-128">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="6803b-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
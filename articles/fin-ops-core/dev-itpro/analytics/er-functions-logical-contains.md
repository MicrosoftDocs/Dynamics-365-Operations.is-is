---
title: CONTAINS-aðgerð rafrænnar skýrslugerðar
description: Þetta efnisatriði inniheldur upplýsingar um hvernig CONTAINS-aðgerð rafrænnar skýrslugerðar er notuð.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557527"
---
# <a name="contains-er-function"></a><span data-ttu-id="ac1ca-103">CONTAINS-aðgerð rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="ac1ca-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac1ca-104">Aðgerðin `CONTAINS` ákvarðar hvort tilgreindur innsláttur inniheldur tiltekinn texta.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="ac1ca-105">Hún skilar *Boole-gildinu* **TRUE** ef tilgreindur innsláttur inniheldur tilgreindan texta.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="ac1ca-106">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1ca-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="ac1ca-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="ac1ca-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="ac1ca-108">Arguments</span></span>

<span data-ttu-id="ac1ca-109">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ac1ca-109">`input`: *String*</span></span>

<span data-ttu-id="ac1ca-110">Gild slóð atriðis fyrir gagnagjafa af gerðinni *Strengur* eða strengjafasti, gildi sem gæti innihaldið seinni frumbreytuna.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="ac1ca-111">`search text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ac1ca-111">`search text`: *String*</span></span>

<span data-ttu-id="ac1ca-112">Gild slóð gagnagjafa af gerðinni *Strengur* eða strengjafasti, gildi sem fyrsta frumbreytan gæti innihaldið.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="ac1ca-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ac1ca-113">Return values</span></span>

<span data-ttu-id="ac1ca-114">*Boole*</span><span class="sxs-lookup"><span data-stu-id="ac1ca-114">*Boolean*</span></span>

<span data-ttu-id="ac1ca-115">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ac1ca-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="ac1ca-116">Usage notes</span></span>

<span data-ttu-id="ac1ca-117">Þessa aðgerð er hægt að nota til að tilgreina segð skilyrðis fyrir aðgerðina [FILTER](er-functions-list-filter.md) aðeins þegar tilheyrandi vörpun er skilgreind í [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til að fá aðgang að [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ca-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="ac1ca-118">Annars er undantekning notuð á hönnunartíma.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="ac1ca-119">Skilaboðin sem birtast ráðleggja að nota aðgerðina [WHERE](er-functions-list-where.md) í staðinn fyrir aðgerðina `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="ac1ca-120">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="ac1ca-120">Example 1</span></span>

<span data-ttu-id="ac1ca-121">Segðin `CONTAINS ("abc", "d")` skilar **FALSE** á meðan segðin `CONTAINS ("abc", "C")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ac1ca-122">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="ac1ca-122">Example 2</span></span>

<span data-ttu-id="ac1ca-123">Segðin `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` skilar **TRUE** ef gildið reitsins **Aðsetur** af gagngjafanum **líkan** innheldur strenginn **DEU**.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="ac1ca-124">Annars skilar hún **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ac1ca-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac1ca-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ac1ca-125">Additional resources</span></span>

[<span data-ttu-id="ac1ca-126">Rökfræðiaðgerðir</span><span class="sxs-lookup"><span data-stu-id="ac1ca-126">Logical functions</span></span>](er-functions-category-logical.md)

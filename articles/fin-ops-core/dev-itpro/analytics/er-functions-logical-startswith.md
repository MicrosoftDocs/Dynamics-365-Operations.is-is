---
title: STARTSWITH-aðgerð rafrænnar skýrslugerðar
description: Þetta efnisatriði inniheldur upplýsingar um hvernig ESTARTSWITH-aðgerð rafrænnar skýrslugerðar er notuð.
author: NickSelin
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
ms.openlocfilehash: ef7e9c88abff2b4b58ecb8abf1e69f7853f9b3fa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751681"
---
# <a name="startswith-er-function"></a><span data-ttu-id="9a877-103">STARTSWITH-aðgerð rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9a877-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a877-104">Aðgerðin `STARTSWITH` ákvarðar hvort tilgreindur innsláttur hefst á tilteknum texta.</span><span class="sxs-lookup"><span data-stu-id="9a877-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="9a877-105">Hún skilar *Boole-gildinu* **TRUE** ef tilgreindur innsláttur byrjar á tilgreindum texta.</span><span class="sxs-lookup"><span data-stu-id="9a877-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="9a877-106">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9a877-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a877-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9a877-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="9a877-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9a877-108">Arguments</span></span>

<span data-ttu-id="9a877-109">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="9a877-109">`input`: *String*</span></span>

<span data-ttu-id="9a877-110">Gild slóð atriðis fyrir gagnagjafa af gerðinni *Strengur* eða strengjafasti, gildi sem gæti byrjað á seinni frumbreytunni.</span><span class="sxs-lookup"><span data-stu-id="9a877-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="9a877-111">`start text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="9a877-111">`start text`: *String*</span></span>

<span data-ttu-id="9a877-112">Gild slóð gagnagjafa af gerðinni *Strengur* eða strengjafasti, gildi sem fyrri frumbreytan gæti byrjað á.</span><span class="sxs-lookup"><span data-stu-id="9a877-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a877-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9a877-113">Return values</span></span>

<span data-ttu-id="9a877-114">*Boole*</span><span class="sxs-lookup"><span data-stu-id="9a877-114">*Boolean*</span></span>

<span data-ttu-id="9a877-115">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="9a877-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9a877-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="9a877-116">Usage notes</span></span>

<span data-ttu-id="9a877-117">Þessa aðgerð er hægt að nota til að tilgreina segð skilyrðis fyrir aðgerðina [FILTER](er-functions-list-filter.md) aðeins þegar tilheyrandi vörpun er skilgreind í [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til að fá aðgang að [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="9a877-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="9a877-118">Annars er undantekning notuð á hönnunartíma.</span><span class="sxs-lookup"><span data-stu-id="9a877-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="9a877-119">Skilaboðin sem birtast ráðleggja að nota aðgerðina [WHERE](er-functions-list-where.md) í staðinn fyrir aðgerðina `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="9a877-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="9a877-120">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="9a877-120">Example 1</span></span>

<span data-ttu-id="9a877-121">Segðin `STARTSWITH ("abc", "d")` skilar **FALSE** á meðan segðin `STARTSWITH ("abc", "A")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9a877-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9a877-122">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="9a877-122">Example 2</span></span>

<span data-ttu-id="9a877-123">Segðin `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` skilar **TRUE** ef gildi reitsins **Aðsetur** af gagngjafanum **líkan** byrjar á strengnum **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="9a877-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="9a877-124">Annars skilar hún **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9a877-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a877-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9a877-125">Additional resources</span></span>

[<span data-ttu-id="9a877-126">Rökfræðiaðgerðir</span><span class="sxs-lookup"><span data-stu-id="9a877-126">Logical functions</span></span>](er-functions-category-logical.md)

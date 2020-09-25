---
title: CONVERTCURRENCY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CONVERTCURRENCY í rafrænni skýrslugerð (ER) er notuð.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744312"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="9b7cc-103">CONVERTCURRENCY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="9b7cc-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b7cc-104">Aðgerðin `CONVERTCURRENCY` skilar *raungildi* sem sýnir niðurstöður umreiknings á tilgreindri peningaupphæð frá tilgreindum upprunagjaldmiðli til tilgreinds markgjaldmiðils með því að nota stillingar tilgreinds fyrirtækis á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b7cc-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9b7cc-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="9b7cc-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9b7cc-106">Arguments</span></span>

<span data-ttu-id="9b7cc-107">`amount`: *Heiltala* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="9b7cc-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="9b7cc-108">Tölugildi sem táknar peningaupphæðina sem þarf að breyta.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="9b7cc-109">`source currency`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="9b7cc-109">`source currency`: *String*</span></span>

<span data-ttu-id="9b7cc-110">Kóði upprunagjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-110">The code of the source currency.</span></span>

<span data-ttu-id="9b7cc-111">`target currency`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="9b7cc-111">`target currency`: *String*</span></span>

<span data-ttu-id="9b7cc-112">Kóði markgjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-112">The code of the target currency.</span></span>

<span data-ttu-id="9b7cc-113">`date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="9b7cc-113">`date`: *Date*</span></span>

<span data-ttu-id="9b7cc-114">Gildið *Dagsetning* sem táknar dagsetninguna sem er notuð til að ákvarða gengi viðskipta.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="9b7cc-115">`company`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="9b7cc-115">`company`: *String*</span></span>

<span data-ttu-id="9b7cc-116">Gildið *Strengur* sem táknar kóða fyrirtækisins sem veitir stillingarnar sem notaðar eru við umreikninginn.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b7cc-117">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9b7cc-117">Return values</span></span>

<span data-ttu-id="9b7cc-118">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="9b7cc-118">*Real*</span></span>

<span data-ttu-id="9b7cc-119">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="9b7cc-120">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9b7cc-120">Example</span></span>

<span data-ttu-id="9b7cc-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` skilar jafngildi einni evru í Bandarískum dollurum á dagsetningu núverandi setu, byggða á stillingum **DEMF**-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="9b7cc-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b7cc-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9b7cc-122">Additional resources</span></span>

[<span data-ttu-id="9b7cc-123">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="9b7cc-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

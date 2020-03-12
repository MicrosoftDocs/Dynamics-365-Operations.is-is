---
title: VALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin VALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042620"
---
# <span data-ttu-id="c6494-103"><a name="VALUE">VALUE ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="c6494-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6494-104">Aðgerðin `VALUE` skilar *Raun*-gildi sem er umreiknað úr tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="c6494-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6494-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="c6494-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="c6494-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="c6494-106">Arguments</span></span>

<span data-ttu-id="c6494-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c6494-107">`text`: *String*</span></span>

<span data-ttu-id="c6494-108">Strengjagildi sem þarf umreikna í tölulegt gildi.</span><span class="sxs-lookup"><span data-stu-id="c6494-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6494-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="c6494-109">Return values</span></span>

<span data-ttu-id="c6494-110">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="c6494-110">*Real*</span></span>

<span data-ttu-id="c6494-111">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="c6494-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c6494-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="c6494-112">Usage notes</span></span>

<span data-ttu-id="c6494-113">Kommur og punktar (.) skoðast sem skiltákn aukastafa, og bandstrik fremst (-) er notað sem neikvætt formerki.</span><span class="sxs-lookup"><span data-stu-id="c6494-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="c6494-114">Undantekningu er beitt á keyrslutíma ef tilgreindur strengur inniheldur önnur tákn sem eru ekki tölur.</span><span class="sxs-lookup"><span data-stu-id="c6494-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="c6494-115">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="c6494-115">Example 1</span></span>

<span data-ttu-id="c6494-116">`VALUE ("1 234,56")` gerir undantekningu.</span><span class="sxs-lookup"><span data-stu-id="c6494-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="c6494-117">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="c6494-117">Example 2</span></span>

<span data-ttu-id="c6494-118">`VALUE ("1234,56")` skilar **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="c6494-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6494-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c6494-119">Additional resources</span></span>

[<span data-ttu-id="c6494-120">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="c6494-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)

---
title: VALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin VALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752581"
---
# <a name="value-er-function"></a><span data-ttu-id="8adeb-103">VALUE ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="8adeb-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8adeb-104">Aðgerðin `VALUE` skilar *Raun*-gildi sem er umreiknað úr tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="8adeb-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8adeb-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="8adeb-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="8adeb-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="8adeb-106">Arguments</span></span>

<span data-ttu-id="8adeb-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="8adeb-107">`text`: *String*</span></span>

<span data-ttu-id="8adeb-108">Strengjagildi sem þarf umreikna í tölulegt gildi.</span><span class="sxs-lookup"><span data-stu-id="8adeb-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="8adeb-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="8adeb-109">Return values</span></span>

<span data-ttu-id="8adeb-110">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="8adeb-110">*Real*</span></span>

<span data-ttu-id="8adeb-111">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="8adeb-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8adeb-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="8adeb-112">Usage notes</span></span>

<span data-ttu-id="8adeb-113">Kommur og punktar (.) skoðast sem skiltákn aukastafa, og bandstrik fremst (-) er notað sem neikvætt formerki.</span><span class="sxs-lookup"><span data-stu-id="8adeb-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="8adeb-114">Undantekningu er beitt á keyrslutíma ef tilgreindur strengur inniheldur önnur tákn sem eru ekki tölur.</span><span class="sxs-lookup"><span data-stu-id="8adeb-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="8adeb-115">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="8adeb-115">Example 1</span></span>

<span data-ttu-id="8adeb-116">`VALUE ("1 234,56")` gerir undantekningu.</span><span class="sxs-lookup"><span data-stu-id="8adeb-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="8adeb-117">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="8adeb-117">Example 2</span></span>

<span data-ttu-id="8adeb-118">`VALUE ("1234,56")` skilar **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="8adeb-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8adeb-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8adeb-119">Additional resources</span></span>

[<span data-ttu-id="8adeb-120">Aðgerðir fyrir umbreytingu á gerð</span><span class="sxs-lookup"><span data-stu-id="8adeb-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
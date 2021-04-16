---
title: CURCREDREF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CURCREDREF í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 65f04e23000e4d2429574db71b18b6907403855e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744344"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="ea544-103">CURCREDREF ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="ea544-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea544-104">Aðgerðin `CURCREDREF` skilar *Streng*-gildi sem táknar tilvísun kröfuhafa, byggða á tölustöfum tilgreinds reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="ea544-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea544-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="ea544-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="ea544-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="ea544-106">Arguments</span></span>

<span data-ttu-id="ea544-107">`invoice number digits`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea544-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="ea544-108">Textagildi sem stendur fyrir tölustafi reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="ea544-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="ea544-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ea544-109">Return values</span></span>

<span data-ttu-id="ea544-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea544-110">*String*</span></span>

<span data-ttu-id="ea544-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="ea544-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ea544-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea544-112">Example</span></span>

<span data-ttu-id="ea544-113">`CURCredRef ("VEND-200002")` skilar **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="ea544-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea544-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ea544-114">Additional resources</span></span>

[<span data-ttu-id="ea544-115">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="ea544-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
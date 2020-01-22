---
title: CURCREDREF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CURCREDREF í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 5633541b1c7e25a0cfb837c4679691506806421b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917006"
---
# <span data-ttu-id="eb571-103"><a name="CURCREDREF">CURCREDREF ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="eb571-103"><a name="CURCREDREF">CURCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb571-104">Aðgerðin `CURCREDREF` skilar *Streng*-gildi sem táknar tilvísun kröfuhafa, byggða á tölustöfum tilgreinds reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="eb571-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb571-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="eb571-105">Syntax</span></span>

```
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="eb571-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="eb571-106">Arguments</span></span>

<span data-ttu-id="eb571-107">`invoice number digits`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="eb571-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="eb571-108">Textagildi sem stendur fyrir tölustafi reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="eb571-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb571-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="eb571-109">Return values</span></span>

<span data-ttu-id="eb571-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="eb571-110">*String*</span></span>

<span data-ttu-id="eb571-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="eb571-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="eb571-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="eb571-112">Example</span></span>

<span data-ttu-id="eb571-113">`CURCredRef ("VEND-200002")` skilar **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="eb571-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb571-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="eb571-114">Additional resources</span></span>

[<span data-ttu-id="eb571-115">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="eb571-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

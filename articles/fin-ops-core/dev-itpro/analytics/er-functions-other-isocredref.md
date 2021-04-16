---
title: ISOCREDREF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ISOCREDREF í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748318"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="573ae-103">ISOCREDREF ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="573ae-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="573ae-104">Aðgerðin `ISOCREDREF` skilar *strengja*-gildi sem sýnir tilvísun Alþjóðlegu staðlastofnunarinnar (ISO), byggt á tölustöfum og stafrófstáknum í tilgreindu númeri vörureiknings.</span><span class="sxs-lookup"><span data-stu-id="573ae-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="573ae-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="573ae-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="573ae-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="573ae-106">Arguments</span></span>

<span data-ttu-id="573ae-107">`invoice number digits`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="573ae-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="573ae-108">Textagildi sem stendur fyrir tölustafi reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="573ae-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="573ae-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="573ae-109">Return values</span></span>

<span data-ttu-id="573ae-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="573ae-110">*String*</span></span>

<span data-ttu-id="573ae-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="573ae-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="573ae-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="573ae-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="573ae-113">Til að útiloka tákn frá stafrófum sem ekki eru í samræmi við ISO skal frumbreytan `invoice number digits` þýdd áður en hún er sett inn í þessa aðgerð.</span><span class="sxs-lookup"><span data-stu-id="573ae-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="573ae-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="573ae-114">Example</span></span>

<span data-ttu-id="573ae-115">`ISOCredRef ("VEND-200002")` skilar **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="573ae-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="573ae-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="573ae-116">Additional resources</span></span>

[<span data-ttu-id="573ae-117">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="573ae-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
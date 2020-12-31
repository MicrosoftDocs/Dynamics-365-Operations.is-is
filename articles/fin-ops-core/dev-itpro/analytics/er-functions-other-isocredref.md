---
title: ISOCREDREF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ISOCREDREF í rafrænni skýrslugerð (ER) er notuð.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680687"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="92acc-103">ISOCREDREF ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="92acc-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92acc-104">Aðgerðin `ISOCREDREF` skilar *strengja*-gildi sem sýnir tilvísun Alþjóðlegu staðlastofnunarinnar (ISO), byggt á tölustöfum og stafrófstáknum í tilgreindu númeri vörureiknings.</span><span class="sxs-lookup"><span data-stu-id="92acc-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="92acc-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="92acc-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="92acc-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="92acc-106">Arguments</span></span>

<span data-ttu-id="92acc-107">`invoice number digits`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="92acc-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="92acc-108">Textagildi sem stendur fyrir tölustafi reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="92acc-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="92acc-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="92acc-109">Return values</span></span>

<span data-ttu-id="92acc-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="92acc-110">*String*</span></span>

<span data-ttu-id="92acc-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="92acc-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="92acc-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="92acc-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="92acc-113">Til að útiloka tákn frá stafrófum sem ekki eru í samræmi við ISO skal frumbreytan `invoice number digits` þýdd áður en hún er sett inn í þessa aðgerð.</span><span class="sxs-lookup"><span data-stu-id="92acc-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="92acc-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="92acc-114">Example</span></span>

<span data-ttu-id="92acc-115">`ISOCredRef ("VEND-200002")` skilar **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="92acc-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92acc-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="92acc-116">Additional resources</span></span>

[<span data-ttu-id="92acc-117">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="92acc-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

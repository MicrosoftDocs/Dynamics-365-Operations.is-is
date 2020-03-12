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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041378"
---
# <span data-ttu-id="e27c3-103"><a name="ISOCREDREF">ISOCREDREF ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="e27c3-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e27c3-104">Aðgerðin `ISOCREDREF` skilar *strengja*-gildi sem sýnir tilvísun Alþjóðlegu staðlastofnunarinnar (ISO), byggt á tölustöfum og stafrófstáknum í tilgreindu númeri vörureiknings.</span><span class="sxs-lookup"><span data-stu-id="e27c3-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e27c3-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="e27c3-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="e27c3-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="e27c3-106">Arguments</span></span>

<span data-ttu-id="e27c3-107">`invoice number digits`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e27c3-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="e27c3-108">Textagildi sem stendur fyrir tölustafi reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="e27c3-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="e27c3-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="e27c3-109">Return values</span></span>

<span data-ttu-id="e27c3-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="e27c3-110">*String*</span></span>

<span data-ttu-id="e27c3-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="e27c3-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e27c3-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="e27c3-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="e27c3-113">Til að útiloka tákn frá stafrófum sem ekki eru í samræmi við ISO skal frumbreytan `invoice number digits` þýdd áður en hún er sett inn í þessa aðgerð.</span><span class="sxs-lookup"><span data-stu-id="e27c3-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="e27c3-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="e27c3-114">Example</span></span>

<span data-ttu-id="e27c3-115">`ISOCredRef ("VEND-200002")` skilar **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="e27c3-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e27c3-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e27c3-116">Additional resources</span></span>

[<span data-ttu-id="e27c3-117">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="e27c3-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

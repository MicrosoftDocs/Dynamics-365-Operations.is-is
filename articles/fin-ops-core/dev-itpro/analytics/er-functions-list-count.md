---
title: COUNT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin COUNT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567893"
---
# <a name="count-er-function"></a><span data-ttu-id="11c40-103">COUNT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="11c40-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11c40-104">Aðgerðin `COUNT` skilar *Heiltölu*-gildi sem táknar fjölda skráa á tilgreindum lista, ef listinn er ekki tómur.</span><span class="sxs-lookup"><span data-stu-id="11c40-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="11c40-105">Ef listinn er tómur skilar þessi aðgerð **0** (núlli).</span><span class="sxs-lookup"><span data-stu-id="11c40-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="11c40-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="11c40-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="11c40-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="11c40-107">Arguments</span></span>

<span data-ttu-id="11c40-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="11c40-108">`list`: *Record list*</span></span>

<span data-ttu-id="11c40-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="11c40-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="11c40-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="11c40-110">Return values</span></span>

<span data-ttu-id="11c40-111">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="11c40-111">*Integer*</span></span>

<span data-ttu-id="11c40-112">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="11c40-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="11c40-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="11c40-113">Example</span></span>

<span data-ttu-id="11c40-114">`COUNT (SPLIT("abcd" , 3))` skilar **2**, vegna þess að aðgerðin `SPLIT` sem er notuð í þessu dæmi býr til lista sem samanstendur af tveimur skrám.</span><span class="sxs-lookup"><span data-stu-id="11c40-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11c40-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="11c40-115">Additional resources</span></span>

[<span data-ttu-id="11c40-116">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="11c40-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
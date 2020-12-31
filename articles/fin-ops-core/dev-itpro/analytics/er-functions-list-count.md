---
title: COUNT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin COUNT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b3a5bb33964c70c85c7d8571057060c1c2b9d433
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687721"
---
# <a name="count-er-function"></a><span data-ttu-id="47a91-103">COUNT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="47a91-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47a91-104">Aðgerðin `COUNT` skilar *Heiltölu*-gildi sem táknar fjölda skráa á tilgreindum lista, ef listinn er ekki tómur.</span><span class="sxs-lookup"><span data-stu-id="47a91-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="47a91-105">Ef listinn er tómur skilar þessi aðgerð **0** (núlli).</span><span class="sxs-lookup"><span data-stu-id="47a91-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="47a91-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="47a91-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="47a91-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="47a91-107">Arguments</span></span>

<span data-ttu-id="47a91-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="47a91-108">`list`: *Record list*</span></span>

<span data-ttu-id="47a91-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="47a91-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="47a91-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="47a91-110">Return values</span></span>

<span data-ttu-id="47a91-111">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="47a91-111">*Integer*</span></span>

<span data-ttu-id="47a91-112">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="47a91-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="47a91-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="47a91-113">Example</span></span>

<span data-ttu-id="47a91-114">`COUNT (SPLIT("abcd" , 3))` skilar **2**, vegna þess að aðgerðin `SPLIT` sem er notuð í þessu dæmi býr til lista sem samanstendur af tveimur skrám.</span><span class="sxs-lookup"><span data-stu-id="47a91-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47a91-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="47a91-115">Additional resources</span></span>

[<span data-ttu-id="47a91-116">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="47a91-116">List functions</span></span>](er-functions-category-list.md)

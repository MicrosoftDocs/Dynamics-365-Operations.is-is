---
title: EMPTYLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin EMPTYLIST í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: ccb52d7d88f292720360ae913ead5be239165193
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687671"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="81c20-103">EMPTYLIST ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="81c20-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81c20-104">Aðgerðin `EMPTYLIST` skilar tómu *Skráarlista*-gildi með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.</span><span class="sxs-lookup"><span data-stu-id="81c20-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c20-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="81c20-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="81c20-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="81c20-106">Arguments</span></span>

<span data-ttu-id="81c20-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="81c20-107">`list`: *Record list*</span></span>

<span data-ttu-id="81c20-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="81c20-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="81c20-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="81c20-109">Return values</span></span>

<span data-ttu-id="81c20-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="81c20-110">*Record list*</span></span>

<span data-ttu-id="81c20-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="81c20-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="81c20-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="81c20-112">Example</span></span>

<span data-ttu-id="81c20-113">`EMPTYLIST (SPLIT ("abc", 1))` skilar nýjum tómum lista sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni sem er notuð.</span><span class="sxs-lookup"><span data-stu-id="81c20-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81c20-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="81c20-114">Additional resources</span></span>

[<span data-ttu-id="81c20-115">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="81c20-115">List functions</span></span>](er-functions-category-list.md)

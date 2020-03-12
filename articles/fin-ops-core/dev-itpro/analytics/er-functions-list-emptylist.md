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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fb991eb9ee08aeb418313eb782dbde7fa22b763
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042183"
---
# <span data-ttu-id="206e4-103"><a name="EMPTYLIST">EMPTYLIST ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="206e4-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="206e4-104">Aðgerðin `EMPTYLIST` skilar tómu *Skráarlista*-gildi með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.</span><span class="sxs-lookup"><span data-stu-id="206e4-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="206e4-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="206e4-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="206e4-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="206e4-106">Arguments</span></span>

<span data-ttu-id="206e4-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="206e4-107">`list`: *Record list*</span></span>

<span data-ttu-id="206e4-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="206e4-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="206e4-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="206e4-109">Return values</span></span>

<span data-ttu-id="206e4-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="206e4-110">*Record list*</span></span>

<span data-ttu-id="206e4-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="206e4-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="206e4-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="206e4-112">Example</span></span>

<span data-ttu-id="206e4-113">`EMPTYLIST (SPLIT ("abc", 1))` skilar nýjum tómum lista sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni sem er notuð.</span><span class="sxs-lookup"><span data-stu-id="206e4-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="206e4-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="206e4-114">Additional resources</span></span>

[<span data-ttu-id="206e4-115">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="206e4-115">List functions</span></span>](er-functions-category-list.md)

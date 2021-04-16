---
title: EMPTYLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin EMPTYLIST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746676"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="0047a-103">EMPTYLIST ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="0047a-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0047a-104">Aðgerðin `EMPTYLIST` skilar tómu *Skráarlista*-gildi með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.</span><span class="sxs-lookup"><span data-stu-id="0047a-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0047a-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="0047a-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="0047a-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="0047a-106">Arguments</span></span>

<span data-ttu-id="0047a-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="0047a-107">`list`: *Record list*</span></span>

<span data-ttu-id="0047a-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="0047a-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0047a-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="0047a-109">Return values</span></span>

<span data-ttu-id="0047a-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="0047a-110">*Record list*</span></span>

<span data-ttu-id="0047a-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="0047a-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="0047a-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0047a-112">Example</span></span>

<span data-ttu-id="0047a-113">`EMPTYLIST (SPLIT ("abc", 1))` skilar nýjum tómum lista sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni sem er notuð.</span><span class="sxs-lookup"><span data-stu-id="0047a-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0047a-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0047a-114">Additional resources</span></span>

[<span data-ttu-id="0047a-115">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="0047a-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: LISTOFFIRSTITEM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTOFFIRSTITEM í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 6dd6c84b43bea36bf922ae9348f95b450e882832
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750181"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="f4731-103">LISTOFFIRSTITEM ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f4731-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4731-104">Aðgerðin `LISTOFFIRSTITEM` skilar *Skráalista*-gildi sem samanstendur af aðeins fyrstu skránni á tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="f4731-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4731-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f4731-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="f4731-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f4731-106">Arguments</span></span>

<span data-ttu-id="f4731-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f4731-107">`list`: *Record list*</span></span>

<span data-ttu-id="f4731-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="f4731-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f4731-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f4731-109">Return values</span></span>

<span data-ttu-id="f4731-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f4731-110">*Record list*</span></span>

<span data-ttu-id="f4731-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="f4731-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="f4731-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f4731-112">Example</span></span>

<span data-ttu-id="f4731-113">Segðin `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` skilar textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="f4731-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4731-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f4731-114">Additional resources</span></span>

[<span data-ttu-id="f4731-115">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="f4731-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
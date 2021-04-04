---
title: LISTOFFIRSTITEM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTOFFIRSTITEM í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: f2e1f7e55c61f883aebb9d5a522a883a9a9de694
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569841"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="ff3ec-103">LISTOFFIRSTITEM ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="ff3ec-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff3ec-104">Aðgerðin `LISTOFFIRSTITEM` skilar *Skráalista*-gildi sem samanstendur af aðeins fyrstu skránni á tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff3ec-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="ff3ec-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="ff3ec-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="ff3ec-106">Arguments</span></span>

<span data-ttu-id="ff3ec-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="ff3ec-107">`list`: *Record list*</span></span>

<span data-ttu-id="ff3ec-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff3ec-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ff3ec-109">Return values</span></span>

<span data-ttu-id="ff3ec-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="ff3ec-110">*Record list*</span></span>

<span data-ttu-id="ff3ec-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="ff3ec-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ff3ec-112">Example</span></span>

<span data-ttu-id="ff3ec-113">Segðin `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` skilar textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff3ec-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ff3ec-114">Additional resources</span></span>

[<span data-ttu-id="ff3ec-115">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="ff3ec-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
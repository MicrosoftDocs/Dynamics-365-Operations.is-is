---
title: LISTOFFIRSTITEM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTOFFIRSTITEM í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041976"
---
# <span data-ttu-id="33ba5-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="33ba5-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33ba5-104">Aðgerðin `LISTOFFIRSTITEM` skilar *Skráalista*-gildi sem samanstendur af aðeins fyrstu skránni á tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="33ba5-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ba5-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="33ba5-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="33ba5-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="33ba5-106">Arguments</span></span>

<span data-ttu-id="33ba5-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="33ba5-107">`list`: *Record list*</span></span>

<span data-ttu-id="33ba5-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="33ba5-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="33ba5-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="33ba5-109">Return values</span></span>

<span data-ttu-id="33ba5-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="33ba5-110">*Record list*</span></span>

<span data-ttu-id="33ba5-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="33ba5-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="33ba5-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="33ba5-112">Example</span></span>

<span data-ttu-id="33ba5-113">Segðin `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` skilar textagildinu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="33ba5-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33ba5-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="33ba5-114">Additional resources</span></span>

[<span data-ttu-id="33ba5-115">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="33ba5-115">List functions</span></span>](er-functions-category-list.md)

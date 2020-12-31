---
title: LEFT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LEFT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685884"
---
# <a name="left-er-function"></a><span data-ttu-id="7aa36-103">LEFT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="7aa36-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7aa36-104">Aðgerðin `LEFT` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá upphafi tiltekins strengs.</span><span class="sxs-lookup"><span data-stu-id="7aa36-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa36-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="7aa36-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="7aa36-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="7aa36-106">Arguments</span></span>

<span data-ttu-id="7aa36-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="7aa36-107">`text`: *String*</span></span>

<span data-ttu-id="7aa36-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="7aa36-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="7aa36-109">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="7aa36-109">`number`: *Integer*</span></span>

<span data-ttu-id="7aa36-110">Fjöldi stafa sem þarf að skila úr upphafi frumtextans.</span><span class="sxs-lookup"><span data-stu-id="7aa36-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="7aa36-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="7aa36-111">Return values</span></span>

<span data-ttu-id="7aa36-112">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7aa36-112">*String*</span></span>

<span data-ttu-id="7aa36-113">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="7aa36-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7aa36-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="7aa36-114">Example</span></span>

<span data-ttu-id="7aa36-115">`LEFT ("Sample", 3)` skilar **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="7aa36-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7aa36-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7aa36-116">Additional resources</span></span>

[<span data-ttu-id="7aa36-117">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="7aa36-117">Text functions</span></span>](er-functions-category-text.md)

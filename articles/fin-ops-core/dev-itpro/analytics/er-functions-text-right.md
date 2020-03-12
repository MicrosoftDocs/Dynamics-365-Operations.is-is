---
title: RIGHT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin RIGHT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040872"
---
# <span data-ttu-id="9e3a0-103"><a name="RIGHT">RIGHT ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="9e3a0-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e3a0-104">Aðgerðin `RIGHT` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá lokum tiltekins strengs.</span><span class="sxs-lookup"><span data-stu-id="9e3a0-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3a0-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9e3a0-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="9e3a0-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9e3a0-106">Arguments</span></span>

<span data-ttu-id="9e3a0-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="9e3a0-107">`text`: *String*</span></span>

<span data-ttu-id="9e3a0-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="9e3a0-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="9e3a0-109">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="9e3a0-109">`number`: *Integer*</span></span>

<span data-ttu-id="9e3a0-110">Fjöldi stafa sem þarf að skila úr enda frumtextans.</span><span class="sxs-lookup"><span data-stu-id="9e3a0-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9e3a0-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9e3a0-111">Return values</span></span>

<span data-ttu-id="9e3a0-112">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="9e3a0-112">*String*</span></span>

<span data-ttu-id="9e3a0-113">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="9e3a0-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9e3a0-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9e3a0-114">Example</span></span>

<span data-ttu-id="9e3a0-115">`RIGHT ("Sample", 3)` skilar **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="9e3a0-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e3a0-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9e3a0-116">Additional resources</span></span>

[<span data-ttu-id="9e3a0-117">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="9e3a0-117">Text functions</span></span>](er-functions-category-text.md)

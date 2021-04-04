---
title: LEFT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LEFT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569993"
---
# <a name="left-er-function"></a><span data-ttu-id="37dfd-103">LEFT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="37dfd-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37dfd-104">Aðgerðin `LEFT` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá upphafi tiltekins strengs.</span><span class="sxs-lookup"><span data-stu-id="37dfd-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="37dfd-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="37dfd-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="37dfd-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="37dfd-106">Arguments</span></span>

<span data-ttu-id="37dfd-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="37dfd-107">`text`: *String*</span></span>

<span data-ttu-id="37dfd-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="37dfd-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="37dfd-109">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="37dfd-109">`number`: *Integer*</span></span>

<span data-ttu-id="37dfd-110">Fjöldi stafa sem þarf að skila úr upphafi frumtextans.</span><span class="sxs-lookup"><span data-stu-id="37dfd-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="37dfd-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="37dfd-111">Return values</span></span>

<span data-ttu-id="37dfd-112">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="37dfd-112">*String*</span></span>

<span data-ttu-id="37dfd-113">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="37dfd-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="37dfd-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="37dfd-114">Example</span></span>

<span data-ttu-id="37dfd-115">`LEFT ("Sample", 3)` skilar **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="37dfd-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37dfd-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="37dfd-116">Additional resources</span></span>

[<span data-ttu-id="37dfd-117">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="37dfd-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
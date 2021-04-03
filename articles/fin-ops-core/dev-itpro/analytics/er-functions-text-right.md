---
title: RIGHT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin RIGHT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570241"
---
# <a name="right-er-function"></a><span data-ttu-id="2c85a-103">RIGHT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="2c85a-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c85a-104">Aðgerðin `RIGHT` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá lokum tiltekins strengs.</span><span class="sxs-lookup"><span data-stu-id="2c85a-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c85a-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="2c85a-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="2c85a-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="2c85a-106">Arguments</span></span>

<span data-ttu-id="2c85a-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="2c85a-107">`text`: *String*</span></span>

<span data-ttu-id="2c85a-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="2c85a-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="2c85a-109">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="2c85a-109">`number`: *Integer*</span></span>

<span data-ttu-id="2c85a-110">Fjöldi stafa sem þarf að skila úr enda frumtextans.</span><span class="sxs-lookup"><span data-stu-id="2c85a-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c85a-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="2c85a-111">Return values</span></span>

<span data-ttu-id="2c85a-112">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="2c85a-112">*String*</span></span>

<span data-ttu-id="2c85a-113">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="2c85a-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2c85a-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="2c85a-114">Example</span></span>

<span data-ttu-id="2c85a-115">`RIGHT ("Sample", 3)` skilar **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="2c85a-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c85a-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2c85a-116">Additional resources</span></span>

[<span data-ttu-id="2c85a-117">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="2c85a-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
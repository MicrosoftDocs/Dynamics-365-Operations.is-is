---
title: CONCATENATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CONCATENATE í rafrænni skýrslugerð (ER) er notuð
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569606"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="3882b-103">CONCATENATE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="3882b-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3882b-104">Aðgerðin `CONCATENATE` skilar öllum tilgreindum textastrengjum sem *Strengja*-gildi eftir að þeir hafa verið sameinaðir í einn streng.</span><span class="sxs-lookup"><span data-stu-id="3882b-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3882b-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="3882b-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="3882b-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="3882b-106">Arguments</span></span>

<span data-ttu-id="3882b-107">`text 1`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="3882b-107">`text 1`: *String*</span></span>

<span data-ttu-id="3882b-108">Tilvísun í gagnagjafa af gagnagerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="3882b-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="3882b-109">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="3882b-109">This argument is required.</span></span>

<span data-ttu-id="3882b-110">`text N`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="3882b-110">`text N`: *String*</span></span>

<span data-ttu-id="3882b-111">Tilvísun í gagnagjafa af gagnagerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="3882b-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="3882b-112">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="3882b-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="3882b-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="3882b-113">Return values</span></span>

<span data-ttu-id="3882b-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="3882b-114">*String*</span></span>

<span data-ttu-id="3882b-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="3882b-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3882b-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="3882b-116">Example</span></span>

<span data-ttu-id="3882b-117">`CONCATENATE ("abc", "def")` skilar **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="3882b-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3882b-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="3882b-118">Usage notes</span></span>

<span data-ttu-id="3882b-119">Segðin `"abc" & "def"` skilar einnig **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="3882b-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3882b-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3882b-120">Additional resources</span></span>

[<span data-ttu-id="3882b-121">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="3882b-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
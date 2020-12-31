---
title: CONCATENATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CONCATENATE í rafrænni skýrslugerð (ER) er notuð
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687939"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="32021-103">CONCATENATE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="32021-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32021-104">Aðgerðin `CONCATENATE` skilar öllum tilgreindum textastrengjum sem *Strengja*-gildi eftir að þeir hafa verið sameinaðir í einn streng.</span><span class="sxs-lookup"><span data-stu-id="32021-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="32021-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="32021-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="32021-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="32021-106">Arguments</span></span>

<span data-ttu-id="32021-107">`text 1`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="32021-107">`text 1`: *String*</span></span>

<span data-ttu-id="32021-108">Tilvísun í gagnagjafa af gagnagerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="32021-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="32021-109">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="32021-109">This argument is required.</span></span>

<span data-ttu-id="32021-110">`text N`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="32021-110">`text N`: *String*</span></span>

<span data-ttu-id="32021-111">Tilvísun í gagnagjafa af gagnagerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="32021-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="32021-112">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="32021-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="32021-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="32021-113">Return values</span></span>

<span data-ttu-id="32021-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="32021-114">*String*</span></span>

<span data-ttu-id="32021-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="32021-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="32021-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="32021-116">Example</span></span>

<span data-ttu-id="32021-117">`CONCATENATE ("abc", "def")` skilar **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="32021-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="32021-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="32021-118">Usage notes</span></span>

<span data-ttu-id="32021-119">Segðin `"abc" & "def"` skilar einnig **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="32021-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32021-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="32021-120">Additional resources</span></span>

[<span data-ttu-id="32021-121">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="32021-121">Text functions</span></span>](er-functions-category-text.md)

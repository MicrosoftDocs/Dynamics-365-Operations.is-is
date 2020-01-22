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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915764"
---
# <span data-ttu-id="f4788-103"><a name="CONCATENATE">CONCATENATE ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="f4788-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4788-104">Aðgerðin `CONCATENATE` skilar öllum tilgreindum textastrengjum sem *Strengja*-gildi eftir að þeir hafa verið sameinaðir í einn streng.</span><span class="sxs-lookup"><span data-stu-id="f4788-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4788-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f4788-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="f4788-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f4788-106">Arguments</span></span>

<span data-ttu-id="f4788-107">`text 1`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f4788-107">`text 1`: *String*</span></span>

<span data-ttu-id="f4788-108">Tilvísun í gagnagjafa af gagnagerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="f4788-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="f4788-109">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="f4788-109">This argument is required.</span></span>

<span data-ttu-id="f4788-110">`text N`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f4788-110">`text N`: *String*</span></span>

<span data-ttu-id="f4788-111">Tilvísun í gagnagjafa af gagnagerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="f4788-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="f4788-112">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="f4788-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f4788-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f4788-113">Return values</span></span>

<span data-ttu-id="f4788-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f4788-114">*String*</span></span>

<span data-ttu-id="f4788-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="f4788-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f4788-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f4788-116">Example</span></span>

<span data-ttu-id="f4788-117">`CONCATENATE ("abc", "def")` skilar **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="f4788-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f4788-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="f4788-118">Usage notes</span></span>

<span data-ttu-id="f4788-119">Segðin `"abc" & "def"` skilar einnig **abcdef**.</span><span class="sxs-lookup"><span data-stu-id="f4788-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4788-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f4788-120">Additional resources</span></span>

[<span data-ttu-id="f4788-121">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="f4788-121">Text functions</span></span>](er-functions-category-text.md)

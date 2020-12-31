---
title: TRIM ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TRIM í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 908da840ffcb94f4a60bb41ce041f5f263c921eb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688367"
---
# <a name="trim-er-function"></a><span data-ttu-id="e61b1-103">TRIM ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="e61b1-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e61b1-104">Aðgerðin `TRIM` skilar tilgreindum textastreng sem *strengjagildi* eftir að bilum fyrir framan og aftan hefur verið eytt, og eftir að samfelld bil milli orðanna hafa verið fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="e61b1-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61b1-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="e61b1-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="e61b1-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="e61b1-106">Arguments</span></span>

<span data-ttu-id="e61b1-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e61b1-107">`text`: *String*</span></span>

<span data-ttu-id="e61b1-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="e61b1-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e61b1-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="e61b1-109">Return values</span></span>

<span data-ttu-id="e61b1-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="e61b1-110">*String*</span></span>

<span data-ttu-id="e61b1-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="e61b1-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e61b1-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="e61b1-112">Example</span></span>

<span data-ttu-id="e61b1-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` skilar **"Sample text"**.</span><span class="sxs-lookup"><span data-stu-id="e61b1-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e61b1-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e61b1-114">Additional resources</span></span>

[<span data-ttu-id="e61b1-115">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="e61b1-115">Text functions</span></span>](er-functions-category-text.md)

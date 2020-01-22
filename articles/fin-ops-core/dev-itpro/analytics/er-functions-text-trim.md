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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915534"
---
# <span data-ttu-id="b599f-103"><a name="TRIM">TRIM ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="b599f-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b599f-104">Aðgerðin `TRIM` skilar tilgreindum textastreng sem *strengjagildi* eftir að bilum fyrir framan og aftan hefur verið eytt, og eftir að samfelld bil milli orðanna hafa verið fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="b599f-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b599f-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="b599f-105">Syntax</span></span>

```
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="b599f-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="b599f-106">Arguments</span></span>

<span data-ttu-id="b599f-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="b599f-107">`text`: *String*</span></span>

<span data-ttu-id="b599f-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="b599f-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b599f-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="b599f-109">Return values</span></span>

<span data-ttu-id="b599f-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="b599f-110">*String*</span></span>

<span data-ttu-id="b599f-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="b599f-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b599f-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b599f-112">Example</span></span>

<span data-ttu-id="b599f-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` skilar **"Sample text"**.</span><span class="sxs-lookup"><span data-stu-id="b599f-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b599f-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b599f-114">Additional resources</span></span>

[<span data-ttu-id="b599f-115">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="b599f-115">Text functions</span></span>](er-functions-category-text.md)

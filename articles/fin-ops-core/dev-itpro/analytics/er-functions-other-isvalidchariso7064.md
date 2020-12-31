---
title: ISVALIDCHARACTERISO7064 ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ISVALIDCHARACTERISO7064 í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680663"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="f18b2-103">ISVALIDCHARACTERISO7064 ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f18b2-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f18b2-104">Aðgerðin `ISVALIDCHARACTERISO7064` skilar *Boolean*-gildinu **TRUE** ef tilgreindur strengur táknar gildan alþjóðlegan bankareikning (IBAN).</span><span class="sxs-lookup"><span data-stu-id="f18b2-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="f18b2-105">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f18b2-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18b2-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f18b2-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="f18b2-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f18b2-107">Arguments</span></span>

<span data-ttu-id="f18b2-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="f18b2-108">`text`: *String*</span></span>

<span data-ttu-id="f18b2-109">Textagildi sem táknar IBAN.</span><span class="sxs-lookup"><span data-stu-id="f18b2-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="f18b2-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f18b2-110">Return values</span></span>

<span data-ttu-id="f18b2-111">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f18b2-111">*String*</span></span>

<span data-ttu-id="f18b2-112">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="f18b2-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f18b2-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f18b2-113">Example</span></span>

<span data-ttu-id="f18b2-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="f18b2-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="f18b2-115">`ISVALIDCHARACTERISO7064 ("AT61")` skilar **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f18b2-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f18b2-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f18b2-116">Additional resources</span></span>

[<span data-ttu-id="f18b2-117">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="f18b2-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

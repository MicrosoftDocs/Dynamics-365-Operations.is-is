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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041401"
---
# <span data-ttu-id="56c3b-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="56c3b-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56c3b-104">Aðgerðin `ISVALIDCHARACTERISO7064` skilar *Boolean*-gildinu **TRUE** ef tilgreindur strengur táknar gildan alþjóðlegan bankareikning (IBAN).</span><span class="sxs-lookup"><span data-stu-id="56c3b-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="56c3b-105">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="56c3b-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c3b-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="56c3b-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="56c3b-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="56c3b-107">Arguments</span></span>

<span data-ttu-id="56c3b-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="56c3b-108">`text`: *String*</span></span>

<span data-ttu-id="56c3b-109">Textagildi sem táknar IBAN.</span><span class="sxs-lookup"><span data-stu-id="56c3b-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="56c3b-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="56c3b-110">Return values</span></span>

<span data-ttu-id="56c3b-111">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="56c3b-111">*String*</span></span>

<span data-ttu-id="56c3b-112">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="56c3b-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="56c3b-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="56c3b-113">Example</span></span>

<span data-ttu-id="56c3b-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="56c3b-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="56c3b-115">`ISVALIDCHARACTERISO7064 ("AT61")` skilar **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="56c3b-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56c3b-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="56c3b-116">Additional resources</span></span>

[<span data-ttu-id="56c3b-117">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="56c3b-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

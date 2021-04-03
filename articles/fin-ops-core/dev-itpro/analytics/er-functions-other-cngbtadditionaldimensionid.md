---
title: CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CN_GBT_ADDITIONALDIMENSIONID í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 5774bb6928ae321af923819d6b2cc609dbf35b99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564143"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="43b6c-103">CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="43b6c-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43b6c-104">Aðgerðin `CN_GBT_ADDITIONALDIMENSIONID` skilar *Streng*-gildi sem táknar stakt fjárhagsvíddarkenni sem er tekið úr tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="43b6c-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="43b6c-105">Tilgreindur strengur sýnir allar víddir sem kommuaðskilinn lista yfir kenni.</span><span class="sxs-lookup"><span data-stu-id="43b6c-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b6c-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="43b6c-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="43b6c-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="43b6c-107">Arguments</span></span>

<span data-ttu-id="43b6c-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="43b6c-108">`text`: *String*</span></span>

<span data-ttu-id="43b6c-109">*Strengjagildi* sem sýnir allar víddir sem kommuaðskilinn lista yfir kenni.</span><span class="sxs-lookup"><span data-stu-id="43b6c-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="43b6c-110">`number`: Heiltala</span><span class="sxs-lookup"><span data-stu-id="43b6c-110">`number`: Integer</span></span>

<span data-ttu-id="43b6c-111">Gildi *heiltölu* skilgreinir kóða númeraraðar af umbeðinni vídd í tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="43b6c-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="43b6c-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="43b6c-112">Return values</span></span>

<span data-ttu-id="43b6c-113">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="43b6c-113">*String*</span></span>

<span data-ttu-id="43b6c-114">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="43b6c-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="43b6c-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="43b6c-115">Example</span></span>

<span data-ttu-id="43b6c-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` skilar **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="43b6c-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43b6c-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="43b6c-117">Additional resources</span></span>

[<span data-ttu-id="43b6c-118">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="43b6c-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
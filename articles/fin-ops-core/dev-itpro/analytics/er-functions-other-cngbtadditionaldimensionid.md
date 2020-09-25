---
title: CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CN_GBT_ADDITIONALDIMENSIONID í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744432"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="6471f-103">CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="6471f-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6471f-104">Aðgerðin `CN_GBT_ADDITIONALDIMENSIONID` skilar *Streng*-gildi sem táknar stakt fjárhagsvíddarkenni sem er tekið úr tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="6471f-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="6471f-105">Tilgreindur strengur sýnir allar víddir sem kommuaðskilinn lista yfir kenni.</span><span class="sxs-lookup"><span data-stu-id="6471f-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="6471f-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="6471f-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="6471f-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="6471f-107">Arguments</span></span>

<span data-ttu-id="6471f-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="6471f-108">`text`: *String*</span></span>

<span data-ttu-id="6471f-109">*Strengjagildi* sem sýnir allar víddir sem kommuaðskilinn lista yfir kenni.</span><span class="sxs-lookup"><span data-stu-id="6471f-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="6471f-110">`number`: Heiltala</span><span class="sxs-lookup"><span data-stu-id="6471f-110">`number`: Integer</span></span>

<span data-ttu-id="6471f-111">Gildi *heiltölu* skilgreinir kóða númeraraðar af umbeðinni vídd í tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="6471f-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="6471f-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="6471f-112">Return values</span></span>

<span data-ttu-id="6471f-113">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="6471f-113">*String*</span></span>

<span data-ttu-id="6471f-114">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="6471f-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="6471f-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6471f-115">Example</span></span>

<span data-ttu-id="6471f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` skilar **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="6471f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6471f-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6471f-117">Additional resources</span></span>

[<span data-ttu-id="6471f-118">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="6471f-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

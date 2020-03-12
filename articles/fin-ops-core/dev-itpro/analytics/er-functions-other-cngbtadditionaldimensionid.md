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
ms.openlocfilehash: 2395a1932e543e35ced28a2a6e56ab44835de19a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041539"
---
# <span data-ttu-id="738ec-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="738ec-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="738ec-104">Aðgerðin `CN_GBT_ADDITIONALDIMENSIONID` skilar *Streng*-gildi sem táknar stakt fjárhagsvíddarkenni sem er tekið úr tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="738ec-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="738ec-105">Tilgreindur strengur sýnir allar víddir sem kommuaðskilinn lista yfir kenni.</span><span class="sxs-lookup"><span data-stu-id="738ec-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="738ec-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="738ec-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="738ec-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="738ec-107">Arguments</span></span>

<span data-ttu-id="738ec-108">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="738ec-108">`text`: *String*</span></span>

<span data-ttu-id="738ec-109">*Strengjagildi* sem sýnir allar víddir sem kommuaðskilinn lista yfir kenni.</span><span class="sxs-lookup"><span data-stu-id="738ec-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="738ec-110">`number`: Heiltala</span><span class="sxs-lookup"><span data-stu-id="738ec-110">`number`: Integer</span></span>

<span data-ttu-id="738ec-111">Gildi *heiltölu* skilgreinir kóða númeraraðar af umbeðinni vídd í tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="738ec-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="738ec-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="738ec-112">Return values</span></span>

<span data-ttu-id="738ec-113">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="738ec-113">*String*</span></span>

<span data-ttu-id="738ec-114">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="738ec-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="738ec-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="738ec-115">Example</span></span>

<span data-ttu-id="738ec-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` skilar **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="738ec-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="738ec-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="738ec-117">Additional resources</span></span>

[<span data-ttu-id="738ec-118">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="738ec-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

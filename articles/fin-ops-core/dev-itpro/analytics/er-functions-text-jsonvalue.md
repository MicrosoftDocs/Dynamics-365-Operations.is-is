---
title: JSONVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin JSONVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 203fe1b1616f724ddf3015258306e0d9e8d4f599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570017"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="1807e-103">JSONVALUE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="1807e-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1807e-104">Aðgerðin `JSONVALUE` þáttar gögn í JavaScript Object Notation (JSON) sniði sem er aðgengilegt á tilgreindri slóð og dregur út tölugildi sem hefur tilgreint auðkenni.</span><span class="sxs-lookup"><span data-stu-id="1807e-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="1807e-105">Hún skilar síðan útdregnu tölugildinu sem *Strengja*-gildi.</span><span class="sxs-lookup"><span data-stu-id="1807e-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1807e-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="1807e-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="1807e-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="1807e-107">Arguments</span></span>

<span data-ttu-id="1807e-108">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="1807e-108">`input`: *String*</span></span>

<span data-ttu-id="1807e-109">Gild slóð í gagnagjafa af gerðinni *Strengur* sem inniheldur JSON-gögn.</span><span class="sxs-lookup"><span data-stu-id="1807e-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="1807e-110">`path`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="1807e-110">`path`: *String*</span></span>

<span data-ttu-id="1807e-111">Kennimerki tölugildis í JSON-gögnum.</span><span class="sxs-lookup"><span data-stu-id="1807e-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="1807e-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="1807e-112">Return values</span></span>

<span data-ttu-id="1807e-113">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="1807e-113">*String*</span></span>

<span data-ttu-id="1807e-114">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="1807e-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1807e-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="1807e-115">Example</span></span>

<span data-ttu-id="1807e-116">Gagnagjafinn **JsonField** inniheldur eftirfarandi gögn á JSON-sniði: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="1807e-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="1807e-117">Í þessu tilfelli skilar segðin `JSONVALUE (JsonField, "BuildNumber")` eftirfarandi gildi af gagnagerðinni *Strengur*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="1807e-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1807e-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1807e-118">Additional resources</span></span>

[<span data-ttu-id="1807e-119">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="1807e-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
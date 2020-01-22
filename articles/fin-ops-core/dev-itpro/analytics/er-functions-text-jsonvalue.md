---
title: JSONVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin JSONVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: d8209f8ce9d244ab7c82f897e4f59283e94e0522
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915672"
---
# <span data-ttu-id="4304f-103"><a name="JSONVALUE">JSONVALUE ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="4304f-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4304f-104">Aðgerðin `JSONVALUE` þáttar gögn í JavaScript Object Notation (JSON) sniði sem er aðgengilegt á tilgreindri slóð og dregur út tölugildi sem hefur tilgreint auðkenni.</span><span class="sxs-lookup"><span data-stu-id="4304f-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="4304f-105">Hún skilar síðan útdregnu tölugildinu sem *Strengja*-gildi.</span><span class="sxs-lookup"><span data-stu-id="4304f-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4304f-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4304f-106">Syntax</span></span>

```
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="4304f-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4304f-107">Arguments</span></span>

<span data-ttu-id="4304f-108">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="4304f-108">`input`: *String*</span></span>

<span data-ttu-id="4304f-109">Gild slóð í gagnagjafa af gerðinni *Strengur* sem inniheldur JSON-gögn.</span><span class="sxs-lookup"><span data-stu-id="4304f-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="4304f-110">`path`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="4304f-110">`path`: *String*</span></span>

<span data-ttu-id="4304f-111">Kennimerki tölugildis í JSON-gögnum.</span><span class="sxs-lookup"><span data-stu-id="4304f-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="4304f-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4304f-112">Return values</span></span>

<span data-ttu-id="4304f-113">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="4304f-113">*String*</span></span>

<span data-ttu-id="4304f-114">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="4304f-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4304f-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4304f-115">Example</span></span>

<span data-ttu-id="4304f-116">Gagnagjafinn **JsonField** inniheldur eftirfarandi gögn á JSON-sniði: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="4304f-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="4304f-117">Í þessu tilfelli skilar segðin `JSONVALUE (JsonField, "BuildNumber")` eftirfarandi gildi af gagnagerðinni *Strengur*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="4304f-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4304f-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4304f-118">Additional resources</span></span>

[<span data-ttu-id="4304f-119">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="4304f-119">Text functions</span></span>](er-functions-category-text.md)

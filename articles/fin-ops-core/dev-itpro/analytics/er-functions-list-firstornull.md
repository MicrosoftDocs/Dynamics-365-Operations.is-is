---
title: FIRSTORNULL ER-aðgerð
description: Þetta efni útskýrir hvernig aðgerðin FIRSTORNULL í rafrænni skýrslugerð (ER) er notuð
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753217"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="3a812-103">FIRSTORNULL ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="3a812-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a812-104">Aðgerð `FIRSTORNULL` skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef skráin er ekki tóm.</span><span class="sxs-lookup"><span data-stu-id="3a812-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="3a812-105">Ef skráin er tóm skilar þessi aðgerð núll *Ílát (skrá)* gildi.</span><span class="sxs-lookup"><span data-stu-id="3a812-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a812-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="3a812-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="3a812-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="3a812-107">Arguments</span></span>

<span data-ttu-id="3a812-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="3a812-108">`list`: *Record list*</span></span>

<span data-ttu-id="3a812-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="3a812-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a812-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="3a812-110">Return values</span></span>

<span data-ttu-id="3a812-111">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="3a812-111">*Container (record)*</span></span>

<span data-ttu-id="3a812-112">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="3a812-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="3a812-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="3a812-113">Example</span></span>

<span data-ttu-id="3a812-114">Segðin `FIRSTORNULL(SPLIT("",1)).Value` skilar tómum streng (**""**).</span><span class="sxs-lookup"><span data-stu-id="3a812-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a812-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3a812-115">Additional resources</span></span>

[<span data-ttu-id="3a812-116">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="3a812-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
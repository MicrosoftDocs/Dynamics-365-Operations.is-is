---
title: EMPTYRECORD ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin EMPTYRECORD í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1cf23f11fa92adfb7a050efd9c68e80e1bee621f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916891"
---
# <span data-ttu-id="77b68-103"><a name="EMPTYRECORD">EMPTYRECORD ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="77b68-103"><a name="EMPTYRECORD">EMPTYRECORD ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77b68-104">Aðgerðin `EMPTYRECORD` skilar núll gildi fyrir *Ílát (skrá)* sem hefur sama skipulag og tilgreindur skráalisti eða skrá.</span><span class="sxs-lookup"><span data-stu-id="77b68-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b68-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="77b68-105">Syntax</span></span>

```
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="77b68-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="77b68-106">Arguments</span></span>

<span data-ttu-id="77b68-107">`list`: *Skráalisti* eða *Ílát (skrá)*</span><span class="sxs-lookup"><span data-stu-id="77b68-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="77b68-108">Gild slóð hlutar í gagnagjafa af annaðhvort gerðinni *Skráalisti* eða *Gámur (skrá)*.</span><span class="sxs-lookup"><span data-stu-id="77b68-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="77b68-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="77b68-109">Return values</span></span>

<span data-ttu-id="77b68-110">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="77b68-110">*Container (record)*</span></span>

<span data-ttu-id="77b68-111">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="77b68-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="77b68-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="77b68-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="77b68-113">Færsla núll er færsla þar sem allir reitir eru með tómt gildi.</span><span class="sxs-lookup"><span data-stu-id="77b68-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="77b68-114">Tómt gildi er **0** (núll) fyrir tölur, tóman streng fyrir strengi og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="77b68-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="77b68-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="77b68-115">Example</span></span>

<span data-ttu-id="77b68-116">`EMPTYRECORD (SPLIT ("abc", 1))` skilar nýrri tómri skrá sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="77b68-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="77b68-117">Frekari upplýsingar er að finna á [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="77b68-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77b68-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="77b68-118">Additional resources</span></span>

[<span data-ttu-id="77b68-119">Færsluvirkni</span><span class="sxs-lookup"><span data-stu-id="77b68-119">Record functions</span></span>](er-functions-category-record.md)

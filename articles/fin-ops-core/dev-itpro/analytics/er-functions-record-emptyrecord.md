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
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743951"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="975da-103">EMPTYRECORD ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="975da-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="975da-104">Aðgerðin `EMPTYRECORD` skilar núll gildi fyrir *Ílát (skrá)* sem hefur sama skipulag og tilgreindur skráalisti eða skrá.</span><span class="sxs-lookup"><span data-stu-id="975da-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="975da-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="975da-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="975da-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="975da-106">Arguments</span></span>

<span data-ttu-id="975da-107">`list`: *Skráalisti* eða *Ílát (skrá)*</span><span class="sxs-lookup"><span data-stu-id="975da-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="975da-108">Gild slóð hlutar í gagnagjafa af annaðhvort gerðinni *Skráalisti* eða *Gámur (skrá)*.</span><span class="sxs-lookup"><span data-stu-id="975da-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="975da-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="975da-109">Return values</span></span>

<span data-ttu-id="975da-110">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="975da-110">*Container (record)*</span></span>

<span data-ttu-id="975da-111">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="975da-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="975da-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="975da-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="975da-113">Færsla núll er færsla þar sem allir reitir eru með tómt gildi.</span><span class="sxs-lookup"><span data-stu-id="975da-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="975da-114">Tómt gildi er **0** (núll) fyrir tölur, tóman streng fyrir strengi og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="975da-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="975da-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="975da-115">Example</span></span>

<span data-ttu-id="975da-116">`EMPTYRECORD (SPLIT ("abc", 1))` skilar nýrri tómri skrá sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="975da-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="975da-117">Frekari upplýsingar er að finna á [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="975da-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="975da-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="975da-118">Additional resources</span></span>

[<span data-ttu-id="975da-119">Færsluvirkni</span><span class="sxs-lookup"><span data-stu-id="975da-119">Record functions</span></span>](er-functions-category-record.md)

---
title: NULLCONTAINER ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLCONTAINER í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563223"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="9b623-103">NULLCONTAINER ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="9b623-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b623-104">Aðgerðin `NULLCONTAINER` skilar núll gildi fyrir *Ílát (skrá)* sem hefur sama skipulag og tilgreindur skráalisti eða skrá.</span><span class="sxs-lookup"><span data-stu-id="9b623-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b623-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9b623-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="9b623-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9b623-106">Arguments</span></span>

<span data-ttu-id="9b623-107">`list`: *Skráalisti* eða *Ílát (skrá)*</span><span class="sxs-lookup"><span data-stu-id="9b623-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="9b623-108">Gild slóð hlutar í gagnagjafa af annaðhvort gerðinni *Skráalisti* eða *Gámur (skrá)*.</span><span class="sxs-lookup"><span data-stu-id="9b623-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b623-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9b623-109">Return values</span></span>

<span data-ttu-id="9b623-110">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="9b623-110">*Container (record)*</span></span>

<span data-ttu-id="9b623-111">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="9b623-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9b623-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="9b623-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="9b623-113">Þessi aðgerð er úrelt.</span><span class="sxs-lookup"><span data-stu-id="9b623-113">This function is obsolete.</span></span> <span data-ttu-id="9b623-114">Notaði aðgerðina `EMPTYRECORD` í staðinn.</span><span class="sxs-lookup"><span data-stu-id="9b623-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="9b623-115">Frekari upplýsingar er að finna á [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="9b623-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="9b623-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9b623-116">Example</span></span>

<span data-ttu-id="9b623-117">`NULLCONTAINER (SPLIT ("abc", 1))` skilar nýrri tómri skrá sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="9b623-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="9b623-118">Frekari upplýsingar er að finna á [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="9b623-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b623-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9b623-119">Additional resources</span></span>

[<span data-ttu-id="9b623-120">Færsluvirkni</span><span class="sxs-lookup"><span data-stu-id="9b623-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
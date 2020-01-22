---
title: GETENUMVALUEBYNAME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETNUMVALUEBYNAME í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916845"
---
# <span data-ttu-id="c1b8f-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="c1b8f-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1b8f-104">Aðgerðin `GETENUMVALUEBYNAME` leitar að tilteknu *Enum*-gildi í tilgreindum tölusetningargagnagjafa með því að nota tölusetningarheitið sem er tilgreint sem *Strengja*-gildi.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="c1b8f-105">Ef *Enum*-gildi finnst skilar aðgerðin því.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="c1b8f-106">Að öðrum kosti skilar aðgerðin upptalningargildinu **núll**.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b8f-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="c1b8f-107">Syntax</span></span>

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="c1b8f-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="c1b8f-108">Arguments</span></span>

<span data-ttu-id="c1b8f-109">`enumeration data source path`: *Upptalning*</span><span class="sxs-lookup"><span data-stu-id="c1b8f-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="c1b8f-110">Gild slóð gagnagjafa af einni af eftirfarandi upptalningargerðum:</span><span class="sxs-lookup"><span data-stu-id="c1b8f-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="c1b8f-111">Líkanaupptalning rafrænnar skýrslugerðar (ER)</span><span class="sxs-lookup"><span data-stu-id="c1b8f-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="c1b8f-112">Upptalning ER-sniðs</span><span class="sxs-lookup"><span data-stu-id="c1b8f-112">ER format enumeration</span></span>
- <span data-ttu-id="c1b8f-113">Upptalning Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="c1b8f-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="c1b8f-114">`enumeration value text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c1b8f-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="c1b8f-115">Strengagildi sem táknar heiti staks upptalningargildis.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="c1b8f-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="c1b8f-116">Return values</span></span>

<span data-ttu-id="c1b8f-117">Má vera núll *Enum*</span><span class="sxs-lookup"><span data-stu-id="c1b8f-117">Nullable *Enum*</span></span>

<span data-ttu-id="c1b8f-118">Upptalningargildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c1b8f-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="c1b8f-119">Usage notes</span></span>

<span data-ttu-id="c1b8f-120">Engin undantekning er gerð ef gildið *Enum* er ekki að finna með því að nota heiti upptalningargildisins sem er tilgreint sem gildið *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="c1b8f-121">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c1b8f-121">Example</span></span>

<span data-ttu-id="c1b8f-122">Í eftirfarandi mynd er **ReportDirection** upptalningin kynnt í gagnalíkani.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="c1b8f-123">Athugaðu að merki eru skilgreind fyrir tölusetningargildin.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="c1b8f-124">Eftirfarandi mynd sýnir þessar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="c1b8f-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="c1b8f-125">Gagnagjafinn **$Direction** er stilltur í ER-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="c1b8f-126">Þessi gagnagjafi er stilltur út frá líkanaupptalningunni **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="c1b8f-127">Segðin `$IsArrivals` er hönnuð til að nota líkanatölusetningarbyggðan gagnagjafa **$Direction** sem færibreytu þessarar aðgerðar.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="c1b8f-128">Gildi þessarar samanburðarsegðar er **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="c1b8f-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="c1b8f-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c1b8f-129">Additional resources</span></span>

[<span data-ttu-id="c1b8f-130">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="c1b8f-130">Text functions</span></span>](er-functions-category-text.md)

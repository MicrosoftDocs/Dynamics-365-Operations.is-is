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
ms.openlocfilehash: 87613978c149b5d41aefc58f9896424229819626
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041178"
---
# <span data-ttu-id="1b97d-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="1b97d-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b97d-104">Aðgerðin `GETENUMVALUEBYNAME` leitar að tilteknu *Enum*-gildi í tilgreindum tölusetningargagnagjafa með því að nota tölusetningarheitið sem er tilgreint sem *Strengja*-gildi.</span><span class="sxs-lookup"><span data-stu-id="1b97d-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="1b97d-105">Ef *Enum*-gildi finnst skilar aðgerðin því.</span><span class="sxs-lookup"><span data-stu-id="1b97d-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="1b97d-106">Að öðrum kosti skilar aðgerðin upptalningargildinu **núll**.</span><span class="sxs-lookup"><span data-stu-id="1b97d-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b97d-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="1b97d-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="1b97d-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="1b97d-108">Arguments</span></span>

<span data-ttu-id="1b97d-109">`enumeration data source path`: *Upptalning*</span><span class="sxs-lookup"><span data-stu-id="1b97d-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="1b97d-110">Gild slóð gagnagjafa af einni af eftirfarandi upptalningargerðum:</span><span class="sxs-lookup"><span data-stu-id="1b97d-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="1b97d-111">Líkanaupptalning rafrænnar skýrslugerðar (ER)</span><span class="sxs-lookup"><span data-stu-id="1b97d-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="1b97d-112">Upptalning ER-sniðs</span><span class="sxs-lookup"><span data-stu-id="1b97d-112">ER format enumeration</span></span>
- <span data-ttu-id="1b97d-113">Upptalning Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1b97d-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="1b97d-114">`enumeration value text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="1b97d-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="1b97d-115">Strengagildi sem táknar heiti staks upptalningargildis.</span><span class="sxs-lookup"><span data-stu-id="1b97d-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b97d-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="1b97d-116">Return values</span></span>

<span data-ttu-id="1b97d-117">Má vera núll *Enum*</span><span class="sxs-lookup"><span data-stu-id="1b97d-117">Nullable *Enum*</span></span>

<span data-ttu-id="1b97d-118">Upptalningargildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="1b97d-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1b97d-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="1b97d-119">Usage notes</span></span>

<span data-ttu-id="1b97d-120">Engin undantekning er gerð ef gildið *Enum* er ekki að finna með því að nota heiti upptalningargildisins sem er tilgreint sem gildið *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="1b97d-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="1b97d-121">Dæmi</span><span class="sxs-lookup"><span data-stu-id="1b97d-121">Example</span></span>

<span data-ttu-id="1b97d-122">Í eftirfarandi mynd er **ReportDirection** upptalningin kynnt í gagnalíkani.</span><span class="sxs-lookup"><span data-stu-id="1b97d-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="1b97d-123">Athugaðu að merki eru skilgreind fyrir tölusetningargildin.</span><span class="sxs-lookup"><span data-stu-id="1b97d-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="1b97d-124">Eftirfarandi mynd sýnir þessar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="1b97d-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="1b97d-125">Gagnagjafinn **$Direction** er stilltur í ER-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="1b97d-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="1b97d-126">Þessi gagnagjafi er stilltur út frá líkanaupptalningunni **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="1b97d-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="1b97d-127">Segðin `$IsArrivals` er hönnuð til að nota líkanatölusetningarbyggðan gagnagjafa **$Direction** sem færibreytu þessarar aðgerðar.</span><span class="sxs-lookup"><span data-stu-id="1b97d-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="1b97d-128">Gildi þessarar samanburðarsegðar er **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="1b97d-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="1b97d-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1b97d-129">Additional resources</span></span>

[<span data-ttu-id="1b97d-130">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="1b97d-130">Text functions</span></span>](er-functions-category-text.md)

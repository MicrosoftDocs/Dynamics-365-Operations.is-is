---
title: TABLENAME2ID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TABLENAME2ID í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563271"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="380c7-103">TABLENAME2ID ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="380c7-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="380c7-104">Aðgerðin `TABLENAME2ID` skilar tölulegri framsetningu töfluauðkennis fyrir tilgreint töfluheiti sem *heiltölu*-gildi.</span><span class="sxs-lookup"><span data-stu-id="380c7-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="380c7-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="380c7-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="380c7-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="380c7-106">Arguments</span></span>

<span data-ttu-id="380c7-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="380c7-107">`text`: *String*</span></span>

<span data-ttu-id="380c7-108">Textagildi sem táknar gilt töfluheiti.</span><span class="sxs-lookup"><span data-stu-id="380c7-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="380c7-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="380c7-109">Return values</span></span>

<span data-ttu-id="380c7-110">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="380c7-110">*Integer*</span></span>

<span data-ttu-id="380c7-111">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="380c7-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="380c7-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="380c7-112">Usage notes</span></span>

<span data-ttu-id="380c7-113">Framkvæmd þessarar aðgerðar getur haft mismunandi niðurstöður í mismunandi tilvikum Microsoft Dynamics 365 Finance, jafnvel þó að sama fyrirtækisheiti sé notað.</span><span class="sxs-lookup"><span data-stu-id="380c7-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="380c7-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="380c7-114">Example</span></span>

<span data-ttu-id="380c7-115">`TABLENAME2ID ("Intrastat")` skilar **1510**.</span><span class="sxs-lookup"><span data-stu-id="380c7-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="380c7-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="380c7-116">Additional resources</span></span>

[<span data-ttu-id="380c7-117">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="380c7-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
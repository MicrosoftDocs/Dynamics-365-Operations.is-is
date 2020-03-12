---
title: TABLENAME2ID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TABLENAME2ID í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041266"
---
# <span data-ttu-id="505dc-103"><a name="TABLENAME2ID">TABLENAME2ID ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="505dc-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="505dc-104">Aðgerðin `TABLENAME2ID` skilar tölulegri framsetningu töfluauðkennis fyrir tilgreint töfluheiti sem *heiltölu*-gildi.</span><span class="sxs-lookup"><span data-stu-id="505dc-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="505dc-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="505dc-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="505dc-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="505dc-106">Arguments</span></span>

<span data-ttu-id="505dc-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="505dc-107">`text`: *String*</span></span>

<span data-ttu-id="505dc-108">Textagildi sem táknar gilt töfluheiti.</span><span class="sxs-lookup"><span data-stu-id="505dc-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="505dc-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="505dc-109">Return values</span></span>

<span data-ttu-id="505dc-110">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="505dc-110">*Integer*</span></span>

<span data-ttu-id="505dc-111">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="505dc-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="505dc-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="505dc-112">Usage notes</span></span>

<span data-ttu-id="505dc-113">Framkvæmd þessarar aðgerðar getur haft mismunandi niðurstöður í mismunandi tilvikum Microsoft Dynamics 365 Finance, jafnvel þó að sama fyrirtækisheiti sé notað.</span><span class="sxs-lookup"><span data-stu-id="505dc-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="505dc-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="505dc-114">Example</span></span>

<span data-ttu-id="505dc-115">`TABLENAME2ID ("Intrastat")` skilar **1510**.</span><span class="sxs-lookup"><span data-stu-id="505dc-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="505dc-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="505dc-116">Additional resources</span></span>

[<span data-ttu-id="505dc-117">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="505dc-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

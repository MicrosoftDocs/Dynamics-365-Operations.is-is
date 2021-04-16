---
title: ENUMERATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ENUMERATE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746652"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="a771b-103">ENUMERATE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="a771b-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a771b-104">Aðgerðin `ENUMERATE` skilar nýju *Skráalista*-gildi sem samanstendur af tölusettum skrám á tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="a771b-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a771b-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="a771b-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="a771b-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="a771b-106">Arguments</span></span>

<span data-ttu-id="a771b-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a771b-107">`list`: *Record list*</span></span>

<span data-ttu-id="a771b-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="a771b-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a771b-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="a771b-109">Return values</span></span>

<span data-ttu-id="a771b-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a771b-110">*Record list*</span></span>

<span data-ttu-id="a771b-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="a771b-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a771b-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="a771b-112">Usage notes</span></span>

<span data-ttu-id="a771b-113">Listi yfir upptaldar skrár sem skilað er afhjúpar eftirfarandi viðbótarþætti:</span><span class="sxs-lookup"><span data-stu-id="a771b-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="a771b-114">Skrá reitanna (íhlutinn **Gildi**)</span><span class="sxs-lookup"><span data-stu-id="a771b-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="a771b-115">Gildandi færsluvísir (**Númer** þáttur)</span><span class="sxs-lookup"><span data-stu-id="a771b-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="a771b-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a771b-116">Example</span></span>

<span data-ttu-id="a771b-117">Í eftirfarandi mynd er búinn til **Tölusettur** gagnagjafi sem tölusettur listi yfir færslur seljanda frá **Lánardrottnum** gagnagjafans sem vísar til VendTable töflunnar.</span><span class="sxs-lookup"><span data-stu-id="a771b-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="a771b-118">Eftirfarandi skýringarmynd sýnir snið rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="a771b-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="a771b-119">Í þessu sniði eru gagnatengsl mynduð til að búa til úttak á XML sniði.</span><span class="sxs-lookup"><span data-stu-id="a771b-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="a771b-120">Þetta úttak kynnir einstaka söluaðila sem upptalda hnúta.</span><span class="sxs-lookup"><span data-stu-id="a771b-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="a771b-121">Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="a771b-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="a771b-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a771b-122">Additional resources</span></span>

[<span data-ttu-id="a771b-123">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="a771b-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
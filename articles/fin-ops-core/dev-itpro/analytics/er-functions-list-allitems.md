---
title: ALLITEMS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ALLITEMS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1eae005a71f50a08c1ef85a7a93c3b2c407c8848
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559225"
---
# <a name="allitems-er-function"></a><span data-ttu-id="a600d-103">ALLITEMS ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="a600d-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a600d-104">Aðgerðin `ALLITEMS` keyrir sem val í minni og skilar nýju flöttu gildi *Skráalista* sem lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð.</span><span class="sxs-lookup"><span data-stu-id="a600d-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="a600d-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="a600d-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="a600d-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="a600d-106">Arguments</span></span>

<span data-ttu-id="a600d-107">`path`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a600d-107">`path`: *Record list*</span></span>

<span data-ttu-id="a600d-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="a600d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a600d-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="a600d-109">Return values</span></span>

<span data-ttu-id="a600d-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a600d-110">*Record list*</span></span>

<span data-ttu-id="a600d-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="a600d-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a600d-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="a600d-112">Usage notes</span></span>

<span data-ttu-id="a600d-113">Slóðin verður að vera skilgreind sem gild slóð gagnagjafa á gagnagjafaþætti af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="a600d-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="a600d-114">Gagnaeiningar eins og slóð strengs og dagsetning ætti að gefa upp villu í segðasmíði rafrænnar skýrslugerðar (ER) á tíma hönnunar.</span><span class="sxs-lookup"><span data-stu-id="a600d-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="a600d-115">Við mælum ekki með að þú notir þessa aðgerð fyrir færslugagnauppruna sem gætu innihaldið mikið magn gagna.</span><span class="sxs-lookup"><span data-stu-id="a600d-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="a600d-116">Í staðinn skaltu íhuga að nota aðgerðina [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="a600d-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="a600d-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="a600d-117">Example 1</span></span>

<span data-ttu-id="a600d-118">Ef þú slærð inn `SPLIT("abcdef" , 2)` sem gagnagjafa **DS** skilar segðin `COUNT( ALLITEMS (DS))` **3**.</span><span class="sxs-lookup"><span data-stu-id="a600d-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a600d-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="a600d-119">Example 2</span></span>

<span data-ttu-id="a600d-120">Ef þú slærð inn **Vend** sem gagnagjafa gagnagerðarinnar *Skráalisti* sem vísar til jöfnunartöflunnar VendTable skilar segðin `ALLITEMS (Vend.'<Relations'.ContactPerson)` flötum lista yfir skrár sem eru með töfluskipulagið **ContactPerson** og innihalda alla tengiliði sem hægt er að opna með tengslunum **ContactPerson.ContactForParty == VendTable.Party** og eru tiltæk fyrir alla lánardrottna úr tilvísaðri lánardrottnatöflu.</span><span class="sxs-lookup"><span data-stu-id="a600d-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a600d-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a600d-121">Additional resources</span></span>

[<span data-ttu-id="a600d-122">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="a600d-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
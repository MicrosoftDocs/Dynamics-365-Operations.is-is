---
title: ALLITEMS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ALLITEMS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 15ab88512e49b51dbefa19056c3e1846715dcadb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687769"
---
# <a name="allitems-er-function"></a><span data-ttu-id="a100c-103">ALLITEMS ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="a100c-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a100c-104">Aðgerðin `ALLITEMS` keyrir sem val í minni og skilar nýju flöttu gildi *Skráalista* sem lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð.</span><span class="sxs-lookup"><span data-stu-id="a100c-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="a100c-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="a100c-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="a100c-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="a100c-106">Arguments</span></span>

<span data-ttu-id="a100c-107">`path`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a100c-107">`path`: *Record list*</span></span>

<span data-ttu-id="a100c-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="a100c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a100c-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="a100c-109">Return values</span></span>

<span data-ttu-id="a100c-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="a100c-110">*Record list*</span></span>

<span data-ttu-id="a100c-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="a100c-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a100c-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="a100c-112">Usage notes</span></span>

<span data-ttu-id="a100c-113">Slóðin verður að vera skilgreind sem gild slóð gagnagjafa á gagnagjafaþætti af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="a100c-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="a100c-114">Gagnaeiningar eins og slóð strengs og dagsetning ætti að gefa upp villu í segðasmíði rafrænnar skýrslugerðar (ER) á tíma hönnunar.</span><span class="sxs-lookup"><span data-stu-id="a100c-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="a100c-115">Við mælum ekki með að þú notir þessa aðgerð fyrir færslugagnauppruna sem gætu innihaldið mikið magn gagna.</span><span class="sxs-lookup"><span data-stu-id="a100c-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="a100c-116">Í staðinn skaltu íhuga að nota aðgerðina [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="a100c-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="a100c-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="a100c-117">Example 1</span></span>

<span data-ttu-id="a100c-118">Ef þú slærð inn `SPLIT("abcdef" , 2)` sem gagnagjafa **DS** skilar segðin `COUNT( ALLITEMS (DS))` **3**.</span><span class="sxs-lookup"><span data-stu-id="a100c-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a100c-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="a100c-119">Example 2</span></span>

<span data-ttu-id="a100c-120">Ef þú slærð inn **Vend** sem gagnagjafa gagnagerðarinnar *Skráalisti* sem vísar til jöfnunartöflunnar VendTable skilar segðin `ALLITEMS (Vend.'<Relations'.ContactPerson)` flötum lista yfir skrár sem eru með töfluskipulagið **ContactPerson** og innihalda alla tengiliði sem hægt er að opna með tengslunum **ContactPerson.ContactForParty == VendTable.Party** og eru tiltæk fyrir alla lánardrottna úr tilvísaðri lánardrottnatöflu.</span><span class="sxs-lookup"><span data-stu-id="a100c-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a100c-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a100c-121">Additional resources</span></span>

[<span data-ttu-id="a100c-122">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="a100c-122">List functions</span></span>](er-functions-category-list.md)

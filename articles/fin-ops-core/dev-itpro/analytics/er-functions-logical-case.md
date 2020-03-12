---
title: CASE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CASE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 3bba9cd190db61fda3636cc3c8093030f886b9bd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041769"
---
# <span data-ttu-id="15f57-103"><a name="CASE">CASE ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="15f57-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15f57-104">Aðgerðin `CASE` metur gildi tiltekinnar segðar á móti tilgreindum valkostum og skilar niðurstöðu fyrsta valmöguleikans sem jafngildir gildi tiltekinnar segðar.</span><span class="sxs-lookup"><span data-stu-id="15f57-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="15f57-105">Annars skilar hún valkvæðri sjálfgefinni niðurstöðu, ef sjálfgefin niðurstaða er tilgreind sem síðasta frumbreyta kallaðrar aðgerðar sem valkostur kemur ekki á undan.</span><span class="sxs-lookup"><span data-stu-id="15f57-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="15f57-106">Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="15f57-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f57-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="15f57-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="15f57-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="15f57-108">Arguments</span></span>

<span data-ttu-id="15f57-109">`expression`: *Frumstæð gagnagerð* (Boolean, tölulegt eða texti)</span><span class="sxs-lookup"><span data-stu-id="15f57-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="15f57-110">Gild segð sem skilar gildi frumstæðrar gagnagerðar.</span><span class="sxs-lookup"><span data-stu-id="15f57-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="15f57-111">`option 1`: *Frumstæð gagnagerð* (Boolean, tölulegt eða texti)</span><span class="sxs-lookup"><span data-stu-id="15f57-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="15f57-112">Gild segð sem skilar gildi sömu frumstæðu gagnagerðar og frumbreytan `expression` í kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="15f57-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="15f57-113">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="15f57-113">This argument is required.</span></span>

<span data-ttu-id="15f57-114">`result 1`: *Einhver af þeim gagnagerðum sem studdar eru*</span><span class="sxs-lookup"><span data-stu-id="15f57-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="15f57-115">Niðurstaðan sem er skilað og samsvarar valkostinum á undan.</span><span class="sxs-lookup"><span data-stu-id="15f57-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="15f57-116">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="15f57-116">This argument is required.</span></span>

<span data-ttu-id="15f57-117">`option N`: *Frumstæð gagnagerð* (Boolean, tölulegt eða texti)</span><span class="sxs-lookup"><span data-stu-id="15f57-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="15f57-118">Gild segð sem skilar gildi sömu frumstæðu gagnagerðar og frumbreytan `expression` í kallaðri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="15f57-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="15f57-119">Þessi frumbreya er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="15f57-119">This argument is optional.</span></span>

<span data-ttu-id="15f57-120">`result N`: *Einhver af þeim gagnagerðum sem studdar eru*</span><span class="sxs-lookup"><span data-stu-id="15f57-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="15f57-121">Niðurstaðan sem er skilað og samsvarar valkostinum á undan.</span><span class="sxs-lookup"><span data-stu-id="15f57-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="15f57-122">Þessi frumbreya er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="15f57-122">This argument is optional.</span></span>

<span data-ttu-id="15f57-123">`default result`: *Einhver af þeim gagnagerðum sem studdar eru*</span><span class="sxs-lookup"><span data-stu-id="15f57-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="15f57-124">Árangurinn sem ætti að vera skilað ef ekki er samsvörun.</span><span class="sxs-lookup"><span data-stu-id="15f57-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="15f57-125">Þessi frumbreya er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="15f57-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="15f57-126">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="15f57-126">Return values</span></span>

<span data-ttu-id="15f57-127">*Einhver af þeim gagnagerðum sem studdar eru*</span><span class="sxs-lookup"><span data-stu-id="15f57-127">*Any of the supported data types*</span></span>

<span data-ttu-id="15f57-128">Gildið sem myndast við einhverja af þeim gagnategundum sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="15f57-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="15f57-129">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="15f57-129">Usage notes</span></span>

<span data-ttu-id="15f57-130">Undantekning er gerð þegar keyrslutími er ekki samsvarandi og valkvæð sjálfgefin niðurstaða er ekki skilgreind.</span><span class="sxs-lookup"><span data-stu-id="15f57-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="15f57-131">Tilgreina verður allar niðurstöður með sömu gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="15f57-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="15f57-132">Undantekning er gerð á hönnunartíma ef gagnagerðir stilltra niðurstaðna passa ekki saman.</span><span class="sxs-lookup"><span data-stu-id="15f57-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="15f57-133">Ef fyrsta niðurstöðugildið og *N*-ta niðurstöðugildið eru gildi af gagnagerðinni *Ílát (skrá)* eða *Skráalisti* er niðurstaðan aðeins með reitina sem eru til í báðum gildum.</span><span class="sxs-lookup"><span data-stu-id="15f57-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="15f57-134">Dæmi</span><span class="sxs-lookup"><span data-stu-id="15f57-134">Example</span></span>

<span data-ttu-id="15f57-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` skilar strengnum **"WINTER"** ef gildandi setudagsetning forrits er á milli októbers og desembers.</span><span class="sxs-lookup"><span data-stu-id="15f57-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="15f57-136">Annars skilar það auður strengur.</span><span class="sxs-lookup"><span data-stu-id="15f57-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15f57-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="15f57-137">Additional resources</span></span>

[<span data-ttu-id="15f57-138">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="15f57-138">Logical functions</span></span>](er-functions-category-logical.md)

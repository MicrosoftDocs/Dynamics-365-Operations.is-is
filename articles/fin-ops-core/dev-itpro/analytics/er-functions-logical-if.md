---
title: IF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin IF í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565905"
---
# <a name="if-er-function"></a><span data-ttu-id="679d9-103">IF ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="679d9-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="679d9-104">Aðgerðin `IF` skilar fyrsta tilgreinda gildinu ef tilgreinda skilyrðið er uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="679d9-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="679d9-105">Að öðrum kosti skilar hún öðru tilgreinda gildinu.</span><span class="sxs-lookup"><span data-stu-id="679d9-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="679d9-106">Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="679d9-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="679d9-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="679d9-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="679d9-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="679d9-108">Arguments</span></span>

<span data-ttu-id="679d9-109">`condition`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="679d9-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="679d9-110">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="679d9-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="679d9-111">`first value`: *Einhver af þeim gagnagerðum sem studdar eru*</span><span class="sxs-lookup"><span data-stu-id="679d9-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="679d9-112">Niðurstaðan sem er skilað ef skilyrðið er uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="679d9-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="679d9-113">`second value`: *Einhver af þeim gagnagerðum sem studdar eru*</span><span class="sxs-lookup"><span data-stu-id="679d9-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="679d9-114">Niðurstaðan sem er skilað ef skilyrðið er ekki uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="679d9-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="679d9-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="679d9-115">Return values</span></span>

<span data-ttu-id="679d9-116">*Einhver af þeim gagnagerðum sem studdar eru*</span><span class="sxs-lookup"><span data-stu-id="679d9-116">*Any of the supported data types*</span></span>

<span data-ttu-id="679d9-117">Gildið sem myndast við einhverja af þeim gagnategundum sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="679d9-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="679d9-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="679d9-118">Usage notes</span></span>

<span data-ttu-id="679d9-119">Frumbreyturnar `first value` og `second value` verða að vera tilgreindar með því að nota sömu gagnagerð.</span><span class="sxs-lookup"><span data-stu-id="679d9-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="679d9-120">Undantekning er gerð á hönnunartíma ef gagnagerðir stilltra gilda passa ekki saman.</span><span class="sxs-lookup"><span data-stu-id="679d9-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="679d9-121">Ef fyrsta gildið og annað gildið eru gildi af gagnagerðinni *Gámur (skrá)* eða *Skáalisti* er niðurstaðan aðeins með reitina sem eru til í báðum gildum.</span><span class="sxs-lookup"><span data-stu-id="679d9-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="679d9-122">Dæmi</span><span class="sxs-lookup"><span data-stu-id="679d9-122">Example</span></span>

<span data-ttu-id="679d9-123">`IF (1=2, "condition is met", "condition is not met")` skilar strengnum **"condition is not met"**.</span><span class="sxs-lookup"><span data-stu-id="679d9-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="679d9-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="679d9-124">Additional resources</span></span>

[<span data-ttu-id="679d9-125">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="679d9-125">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
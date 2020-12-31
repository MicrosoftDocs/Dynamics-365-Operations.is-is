---
title: GUIDVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GUIDVALUE í rafrænni skýrslugerð (ER) er notuð.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685955"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="5b82b-103">GUIDVALUE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="5b82b-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b82b-104">Aðgerðin `GUIDVALUE` umreiknar tilgreint inntak af gerðinni *Strengur* í gagnaatriði af gerðinni *GUID*.</span><span class="sxs-lookup"><span data-stu-id="5b82b-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b82b-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="5b82b-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="5b82b-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="5b82b-106">Arguments</span></span>

<span data-ttu-id="5b82b-107">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="5b82b-107">`input`: *String*</span></span>

<span data-ttu-id="5b82b-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="5b82b-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5b82b-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="5b82b-109">Return values</span></span>

<span data-ttu-id="5b82b-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5b82b-110">*GUID*</span></span>

<span data-ttu-id="5b82b-111">Gildi altækts einkvæms auðkennis (GUID) sem myndast.</span><span class="sxs-lookup"><span data-stu-id="5b82b-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5b82b-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="5b82b-112">Usage notes</span></span>

<span data-ttu-id="5b82b-113">Til að umbreyta í gagnstæða átt (það er að breyta tilteknu inntaki *GUID* gagnagerðarinnar í gagnaatriði *Strengur* gagnagerðarinnar) er hægt að nota [TEXT](er-functions-text-text.md) virknina.</span><span class="sxs-lookup"><span data-stu-id="5b82b-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="5b82b-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="5b82b-114">Example</span></span>

<span data-ttu-id="5b82b-115">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="5b82b-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="5b82b-116">Gagnagjafinn **myID** af gerðnni *Reiknað svæði* sem inniheldur segðina `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="5b82b-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="5b82b-117">Gagnagjafinn **Users** af gerðinni *Töfluskrár* sem vísar til töflunnar UserInfo</span><span class="sxs-lookup"><span data-stu-id="5b82b-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="5b82b-118">Þú getur síðan notað segð eins og `FILTER (Users, Users.objectId = myID)` til að sía UserInfo töfluna með reitnum **ObjectId** í gagnagjafanum *GUID*.</span><span class="sxs-lookup"><span data-stu-id="5b82b-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b82b-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5b82b-119">Additional resources</span></span>

[<span data-ttu-id="5b82b-120">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="5b82b-120">Text functions</span></span>](er-functions-category-text.md)

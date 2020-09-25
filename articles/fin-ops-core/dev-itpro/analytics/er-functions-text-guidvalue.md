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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b4c65063cd22b5370ca6000a32c6fd1cc9ce6b6
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743832"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="06124-103">GUIDVALUE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="06124-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06124-104">Aðgerðin `GUIDVALUE` umreiknar tilgreint inntak af gerðinni *Strengur* í gagnaatriði af gerðinni *GUID*.</span><span class="sxs-lookup"><span data-stu-id="06124-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="06124-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="06124-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="06124-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="06124-106">Arguments</span></span>

<span data-ttu-id="06124-107">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="06124-107">`input`: *String*</span></span>

<span data-ttu-id="06124-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="06124-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="06124-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="06124-109">Return values</span></span>

<span data-ttu-id="06124-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="06124-110">*GUID*</span></span>

<span data-ttu-id="06124-111">Gildi altækts einkvæms auðkennis (GUID) sem myndast.</span><span class="sxs-lookup"><span data-stu-id="06124-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="06124-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="06124-112">Usage notes</span></span>

<span data-ttu-id="06124-113">Til að umbreyta í gagnstæða átt (það er að breyta tilteknu inntaki *GUID* gagnagerðarinnar í gagnaatriði *Strengur* gagnagerðarinnar) er hægt að nota [TEXT](er-functions-text-text.md) virknina.</span><span class="sxs-lookup"><span data-stu-id="06124-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="06124-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="06124-114">Example</span></span>

<span data-ttu-id="06124-115">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="06124-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="06124-116">Gagnagjafinn **myID** af gerðnni *Reiknað svæði* sem inniheldur segðina `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="06124-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="06124-117">Gagnagjafinn **Users** af gerðinni *Töfluskrár* sem vísar til töflunnar UserInfo</span><span class="sxs-lookup"><span data-stu-id="06124-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="06124-118">Þú getur síðan notað segð eins og `FILTER (Users, Users.objectId = myID)` til að sía UserInfo töfluna með reitnum **ObjectId** í gagnagjafanum *GUID*.</span><span class="sxs-lookup"><span data-stu-id="06124-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06124-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="06124-119">Additional resources</span></span>

[<span data-ttu-id="06124-120">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="06124-120">Text functions</span></span>](er-functions-category-text.md)

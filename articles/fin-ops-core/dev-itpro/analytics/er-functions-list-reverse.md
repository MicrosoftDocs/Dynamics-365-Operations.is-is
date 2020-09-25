---
title: REVERSE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin REVERSE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: ab953136b7500665bdb13e6ff585e3b76896c9ee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744986"
---
# <a name="reverse-er-function"></a><span data-ttu-id="f2fcf-103">REVERSE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f2fcf-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2fcf-104">Aðgerðin `REVERSE` skilar tilgreindum lista sem *Skráalista*-gildi í öfugri röð.</span><span class="sxs-lookup"><span data-stu-id="f2fcf-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fcf-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f2fcf-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="f2fcf-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f2fcf-106">Arguments</span></span>

<span data-ttu-id="f2fcf-107">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f2fcf-107">`list`: *Record list*</span></span>

<span data-ttu-id="f2fcf-108">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="f2fcf-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f2fcf-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f2fcf-109">Return values</span></span>

<span data-ttu-id="f2fcf-110">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="f2fcf-110">*Record list*</span></span>

<span data-ttu-id="f2fcf-111">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="f2fcf-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="f2fcf-112">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="f2fcf-112">Example 1</span></span>

<span data-ttu-id="f2fcf-113">Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` textagildinu **"C"**.</span><span class="sxs-lookup"><span data-stu-id="f2fcf-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f2fcf-114">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="f2fcf-114">Example 2</span></span>

<span data-ttu-id="f2fcf-115">Ef **Lánardrottinn** er stilltur sem gagnagjafi rafrænnar skýrslugerðar (ER) sem vísar til töflunnar VendTable skilar segðin `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` lista yfir lánardrottna sem er raðað eftir nafni í lækkandi röð.</span><span class="sxs-lookup"><span data-stu-id="f2fcf-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2fcf-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f2fcf-116">Additional resources</span></span>

[<span data-ttu-id="f2fcf-117">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="f2fcf-117">List functions</span></span>](er-functions-category-list.md)

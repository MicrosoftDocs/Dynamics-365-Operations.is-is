---
title: TEXT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TEXT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682896"
---
# <a name="text-er-function"></a><span data-ttu-id="5aa80-103">TEXT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="5aa80-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aa80-104">Aðgerðin `TEXT` skilar tilgreindri tölu sem *strengjagildi* eftir að því hefur verið breytt í textastreng sem er sniðið í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki forrits.</span><span class="sxs-lookup"><span data-stu-id="5aa80-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa80-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="5aa80-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="5aa80-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="5aa80-106">Arguments</span></span>

<span data-ttu-id="5aa80-107">`number`: *Heiltala* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="5aa80-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="5aa80-108">Tala sem þarf umreikna í textastreng.</span><span class="sxs-lookup"><span data-stu-id="5aa80-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="5aa80-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="5aa80-109">Return values</span></span>

<span data-ttu-id="5aa80-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="5aa80-110">*String*</span></span>

<span data-ttu-id="5aa80-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="5aa80-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5aa80-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="5aa80-112">Usage notes</span></span>

<span data-ttu-id="5aa80-113">Fyrir gildi í af gerðinni *rauntala* takmarkast umbreyting strengs við sem nemur tveimur tugasætum.</span><span class="sxs-lookup"><span data-stu-id="5aa80-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="5aa80-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="5aa80-114">Example</span></span>

<span data-ttu-id="5aa80-115">Ef þjónsstaðsetning á tilviki Microsoft Dynamics 365 Finance er skilgreind sem **EN-US** skilar `TEXT (NOW ())` gildandi setudagsetningu Finance, desember 17, 2015, sem textastrenginn **12/17/2015 07:59:23 fyrir hádegi**.</span><span class="sxs-lookup"><span data-stu-id="5aa80-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="5aa80-116">`TEXT (1/3)` skilar **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="5aa80-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5aa80-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5aa80-117">Additional resources</span></span>

[<span data-ttu-id="5aa80-118">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="5aa80-118">Text functions</span></span>](er-functions-category-text.md)

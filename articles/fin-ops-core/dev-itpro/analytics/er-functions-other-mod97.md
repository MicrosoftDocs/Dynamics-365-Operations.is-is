---
title: MOD_97 ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin MOD_97 í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 618cb2b101dd0b1c91b3b1538ef3f87c21e4a70a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563343"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="9d75a-103">MOD_97 ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="9d75a-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d75a-104">Aðgerðin `MOD_97` skilar *Streng*-gildi sem táknar tilvísun kröfuhafa sem MOD97 segð, byggða á tölustöfum tilgreinds reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="9d75a-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d75a-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9d75a-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="9d75a-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9d75a-106">Arguments</span></span>

<span data-ttu-id="9d75a-107">`invoice number digits`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="9d75a-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="9d75a-108">Textagildi sem stendur fyrir tölustafi reikningsnúmers.</span><span class="sxs-lookup"><span data-stu-id="9d75a-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d75a-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9d75a-109">Return values</span></span>

<span data-ttu-id="9d75a-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="9d75a-110">*String*</span></span>

<span data-ttu-id="9d75a-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="9d75a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9d75a-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9d75a-112">Example</span></span>

<span data-ttu-id="9d75a-113">`MOD_97 ("VEND-200002")` skilar **"20000285"**.</span><span class="sxs-lookup"><span data-stu-id="9d75a-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d75a-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9d75a-114">Additional resources</span></span>

[<span data-ttu-id="9d75a-115">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="9d75a-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: FA_BALANCE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_BALANCE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 76a087157ae53e2c571654ade7383d7bd7a005c3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041447"
---
# <span data-ttu-id="b2eba-103"><a name="FA_BALANCE">FA_BALANCE ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="b2eba-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2eba-104">Aðgerðin `FA_BALANCE` skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um varanleika fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan, skýrsluár og skýrsludag.</span><span class="sxs-lookup"><span data-stu-id="b2eba-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2eba-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="b2eba-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="b2eba-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="b2eba-106">Arguments</span></span>

<span data-ttu-id="b2eba-107">`fixed asset code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="b2eba-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="b2eba-108">Gildið *Strengur* sem táknar kóða fastafjármagnsliða sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="b2eba-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="b2eba-109">`value model code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="b2eba-109">`value model code`: *String*</span></span>

<span data-ttu-id="b2eba-110">Gildið *Strengur* sem táknar kóða virðislíkans sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="b2eba-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="b2eba-111">`reporting year`: *Upptalningargildi*</span><span class="sxs-lookup"><span data-stu-id="b2eba-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="b2eba-112">Upptalningargildi forritsupptalningarinnar **AssetYear** sem skilgreinir tímabil fyrir útreikning á stöðu.</span><span class="sxs-lookup"><span data-stu-id="b2eba-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="b2eba-113">`reporting date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="b2eba-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="b2eba-114">Gildið *Dagsetning* sem skilgreinir dagsetningu fyrir útreikning á stöðu.</span><span class="sxs-lookup"><span data-stu-id="b2eba-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="b2eba-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="b2eba-115">Return values</span></span>

<span data-ttu-id="b2eba-116">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="b2eba-116">*Container (record)*</span></span>

<span data-ttu-id="b2eba-117">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="b2eba-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="b2eba-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b2eba-118">Example</span></span>

<span data-ttu-id="b2eba-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` skilar tilbúnum gagnageymi fyrir stöðu eignar **"COMP-000001"** sem hefur **"Núverandi"** gildislíkan á núverandi setudagsetningu forrits.</span><span class="sxs-lookup"><span data-stu-id="b2eba-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2eba-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b2eba-120">Additional resources</span></span>

[<span data-ttu-id="b2eba-121">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="b2eba-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

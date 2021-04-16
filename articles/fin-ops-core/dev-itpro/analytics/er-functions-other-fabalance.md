---
title: FA_BALANCE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FA_BALANCE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: ec78b9c5bf800503023315eb893076486b0a1fb0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744320"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="10ae7-103">FA_BALANCE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="10ae7-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10ae7-104">Aðgerðin `FA_BALANCE` skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um varanleika fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan, skýrsluár og skýrsludag.</span><span class="sxs-lookup"><span data-stu-id="10ae7-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ae7-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="10ae7-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="10ae7-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="10ae7-106">Arguments</span></span>

<span data-ttu-id="10ae7-107">`fixed asset code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="10ae7-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="10ae7-108">Gildið *Strengur* sem táknar kóða fastafjármagnsliða sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="10ae7-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="10ae7-109">`value model code`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="10ae7-109">`value model code`: *String*</span></span>

<span data-ttu-id="10ae7-110">Gildið *Strengur* sem táknar kóða virðislíkans sem staðan er reiknuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="10ae7-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="10ae7-111">`reporting year`: *Upptalningargildi*</span><span class="sxs-lookup"><span data-stu-id="10ae7-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="10ae7-112">Upptalningargildi forritsupptalningarinnar **AssetYear** sem skilgreinir tímabil fyrir útreikning á stöðu.</span><span class="sxs-lookup"><span data-stu-id="10ae7-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="10ae7-113">`reporting date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="10ae7-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="10ae7-114">Gildið *Dagsetning* sem skilgreinir dagsetningu fyrir útreikning á stöðu.</span><span class="sxs-lookup"><span data-stu-id="10ae7-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="10ae7-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="10ae7-115">Return values</span></span>

<span data-ttu-id="10ae7-116">*Gámur (skrá)*</span><span class="sxs-lookup"><span data-stu-id="10ae7-116">*Container (record)*</span></span>

<span data-ttu-id="10ae7-117">Skráargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="10ae7-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="10ae7-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="10ae7-118">Example</span></span>

<span data-ttu-id="10ae7-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` skilar tilbúnum gagnageymi fyrir stöðu eignar **"COMP-000001"** sem hefur **"Núverandi"** gildislíkan á núverandi setudagsetningu forrits.</span><span class="sxs-lookup"><span data-stu-id="10ae7-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10ae7-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="10ae7-120">Additional resources</span></span>

[<span data-ttu-id="10ae7-121">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="10ae7-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
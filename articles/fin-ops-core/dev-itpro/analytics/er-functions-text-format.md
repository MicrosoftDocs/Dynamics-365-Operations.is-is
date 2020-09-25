---
title: FORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FORMAT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 3f3e8e5f6676c26b8d604ed950470463f04c0473
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743880"
---
# <a name="format-er-function"></a><span data-ttu-id="4152d-103">FORMAT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="4152d-103">FORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4152d-104">Aðgerðin `FORMAT` skilar tilgreindum streng sem *strengja*-gildi eftir að hann hefur verið sniðinn með því að skipta út öllum tilvikum af **%N** með *n*tu frumbreytunni.</span><span class="sxs-lookup"><span data-stu-id="4152d-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="4152d-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4152d-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="4152d-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4152d-106">Arguments</span></span>

<span data-ttu-id="4152d-107">`string`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="4152d-107">`string`: *String*</span></span>

<span data-ttu-id="4152d-108">Tilvísun í gagnagjafa af gerðinni *Strengur* sem verður að forsníða.</span><span class="sxs-lookup"><span data-stu-id="4152d-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="4152d-109">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="4152d-109">This argument is required.</span></span>

<span data-ttu-id="4152d-110">`argument 1`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="4152d-110">`argument 1`: *String*</span></span>

<span data-ttu-id="4152d-111">Fyrsta frumbreytan, sem er notuð til að koma í staðinn fyrir **%1**.</span><span class="sxs-lookup"><span data-stu-id="4152d-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="4152d-112">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="4152d-112">This argument is required.</span></span>

<span data-ttu-id="4152d-113">`argument N`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="4152d-113">`argument N`: *String*</span></span>

<span data-ttu-id="4152d-114">Fyrsta *N*ta frumbreytan, sem er notuð til að koma í staðinn fyrir **%2**, **%3** o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="4152d-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="4152d-115">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="4152d-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4152d-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4152d-116">Return values</span></span>

<span data-ttu-id="4152d-117">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="4152d-117">*String*</span></span>

<span data-ttu-id="4152d-118">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="4152d-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4152d-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="4152d-119">Usage notes</span></span>

<span data-ttu-id="4152d-120">Ef frumbreyta er ekki gefin upp fyrir færibreytu, er færibreytan skilað sem **"%N"** í strengnum.</span><span class="sxs-lookup"><span data-stu-id="4152d-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="4152d-121">Fyrir gildi í af gerðinni *rauntala* takmarkast sjálfgefin umbreyting strengs við sem nemur tveimur tugasætum.</span><span class="sxs-lookup"><span data-stu-id="4152d-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="4152d-122">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4152d-122">Example</span></span>

<span data-ttu-id="4152d-123">Í eftirfarandi mynd skilar gagnagjafninn **PaymentModel** lista yfir skrár viðskiptavina með því að nota íhlutinn **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="4152d-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="4152d-124">Það skilar gildi vinnsludags með því að nota reitinn **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="4152d-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="4152d-125">Í sniði rafrænnar skýrslugerðar (ER) sem er hannað til að mynda rafræna skrá fyrir valda viðskiptavini er **PaymentModel** valið sem gagnagjafi og það stýrir flæði ferlis.</span><span class="sxs-lookup"><span data-stu-id="4152d-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="4152d-126">Ef valinn viðskiptavinur hefur hætt á deginum sem skýrslan er unnin er undantekningu beitt til að upplýsa notandann.</span><span class="sxs-lookup"><span data-stu-id="4152d-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="4152d-127">Formúlu sem er hannað fyrir þessa gerð vinnslustýringar getur notað eftirfarandi tilföng:</span><span class="sxs-lookup"><span data-stu-id="4152d-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="4152d-128">Merki SYS70894 sem hefur eftirfarandi texta:</span><span class="sxs-lookup"><span data-stu-id="4152d-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="4152d-129">**Fyrir tungumál EN-US:** "Ekkert til að prenta"</span><span class="sxs-lookup"><span data-stu-id="4152d-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="4152d-130">**Fyrir tungumálið DE:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="4152d-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="4152d-131">Merki SYS18389 sem hefur eftirfarandi texta:</span><span class="sxs-lookup"><span data-stu-id="4152d-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="4152d-132">**Fyrir tungumál EN-US:** "Customer %1 is stopped for %2."</span><span class="sxs-lookup"><span data-stu-id="4152d-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="4152d-133">**Fyrir tungumálið DE:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="4152d-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="4152d-134">Hér er segðin sem hægt er að hanna.</span><span class="sxs-lookup"><span data-stu-id="4152d-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="4152d-135">Ef skýrsla er unnin fyrir **Litware Retail** viðskiptavin 17. desember 2015, í **EN-US** menningu og **EN-US** tungumáli, skilar þessi formúla eftirfarandi texta, sem hægt er að birta fyrir notandann sem undantekningarskilaboð:</span><span class="sxs-lookup"><span data-stu-id="4152d-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="4152d-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span><span class="sxs-lookup"><span data-stu-id="4152d-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="4152d-137">Ef sama skýrslan er unnin fyrir viðskiptavininn **Litware Retail** þann 17. desember 2015 í menningunni **DE** og tungumálinu **DE** skilar formúlan eftirfarandi texta, sem notar annað snið dagsetningar:</span><span class="sxs-lookup"><span data-stu-id="4152d-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="4152d-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="4152d-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="4152d-139">Eftirfarandi setningafræði er beitt í formúlum rafrænnar skýrslugerðar fyrir merki:</span><span class="sxs-lookup"><span data-stu-id="4152d-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="4152d-140">**Fyrir merki úr tilföngum í forriti Microsoft Dynamics 365 Finance:** **\@X**, þar sem **X** er merkjakennið í hugbúnaðarhlutatrénu (AOT)</span><span class="sxs-lookup"><span data-stu-id="4152d-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="4152d-141">**Fyrir merki sem eru í ER-skilgreiningum:** **@GER_LABEL:X"**, þar sem **X** er merkjakenni í ER-skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="4152d-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4152d-142">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4152d-142">Additional resources</span></span>

[<span data-ttu-id="4152d-143">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="4152d-143">Text functions</span></span>](er-functions-category-text.md)

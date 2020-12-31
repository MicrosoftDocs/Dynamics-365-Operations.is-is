---
title: Listi yfir ER-aðgerðir í rökfræðiflokknum
description: Þetta efni veitir upplýsingar um röklegar aðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: a37b3341b05fde1283a21a0c52faec26cd1a7030
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686188"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="0b76d-103">Listi yfir ER-aðgerðir í rökfræðiflokknum</span><span class="sxs-lookup"><span data-stu-id="0b76d-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b76d-104">Rafrænar skýrslutökur (ER) geta verið notaðar til að vinna með rökleg gildi til að framkvæma fleiri en einn samanburð á einni tjáningu eða prófa margar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="0b76d-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="0b76d-105">Þetta efni gefur yfirlit yfir þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="0b76d-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="0b76d-106">Listi yfir studdar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="0b76d-106">List of supported functions</span></span>

| <span data-ttu-id="0b76d-107">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="0b76d-107">Function</span></span> | <span data-ttu-id="0b76d-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="0b76d-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0b76d-109">Og</span><span class="sxs-lookup"><span data-stu-id="0b76d-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="0b76d-110">Þessi aðgerð skilar *Boolean*-gildi **SATT** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="0b76d-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="0b76d-111">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0b76d-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0b76d-112">Tilvik</span><span class="sxs-lookup"><span data-stu-id="0b76d-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="0b76d-113">Þessi aðgerð metur gildi tiltekinnar segðar á móti tilgreindum valkostum og skilar niðurstöðu fyrsta valmöguleikans sem jafngildir gildi tiltekinnar segðar.</span><span class="sxs-lookup"><span data-stu-id="0b76d-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="0b76d-114">Annars skilar hún valkvæðri sjálfgefinni niðurstöðu, ef sjálfgefin niðurstaða er tilgreind sem síðasta frumbreyta kallaðrar aðgerðar sem valkostur kemur ekki á undan.</span><span class="sxs-lookup"><span data-stu-id="0b76d-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="0b76d-115">Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="0b76d-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="0b76d-116">Ef</span><span class="sxs-lookup"><span data-stu-id="0b76d-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="0b76d-117">Þessi aðgerð skilar fyrsta tilgreinda gildinu ef tilgreinda skilyrðið er uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="0b76d-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="0b76d-118">Að öðrum kosti skilar hún öðru tilgreinda gildinu.</span><span class="sxs-lookup"><span data-stu-id="0b76d-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="0b76d-119">Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="0b76d-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="0b76d-120">Ekki</span><span class="sxs-lookup"><span data-stu-id="0b76d-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="0b76d-121">Þessi aðgerð skilar bakfærðu röklegu gildi tilgreinds skilyrðis sem *Boolean*-gildi.</span><span class="sxs-lookup"><span data-stu-id="0b76d-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="0b76d-122">Or</span><span class="sxs-lookup"><span data-stu-id="0b76d-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="0b76d-123">Þessi aðgerð skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn.</span><span class="sxs-lookup"><span data-stu-id="0b76d-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="0b76d-124">Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="0b76d-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="0b76d-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="0b76d-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="0b76d-126">Þessi aðgerð ákvarðar hvort tilgreint ílag passar við eitthvert gildi tilgreinds hlutar sem er í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="0b76d-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0b76d-127">Hún skilar *Boolean*-gildinu **TRUE** ef tilgreint inntak passar við niðurstöðu þess að keyra tiltekna segð fyrir að minnsta kosti eina skrá af tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="0b76d-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0b76d-128">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0b76d-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0b76d-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="0b76d-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="0b76d-130">Þessi virknin ákvarðar hvort tilgreindur innsláttur *Int64* eða *Heiltala* passar við eitthvað gildi hlutar sem er í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="0b76d-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0b76d-131">Hún skilar *Boolean*-gildinu **TRUE** ef tilgreint inntak passar við niðurstöðu þess að keyra tiltekna segð fyrir að minnsta kosti eina skrá af tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="0b76d-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0b76d-132">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0b76d-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="0b76d-133">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0b76d-133">Additional resources</span></span>

[<span data-ttu-id="0b76d-134">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="0b76d-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="0b76d-135">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="0b76d-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="0b76d-136">Formúlutungumál í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="0b76d-136">Electronic reporting formula language</span></span>](er-formula-language.md)

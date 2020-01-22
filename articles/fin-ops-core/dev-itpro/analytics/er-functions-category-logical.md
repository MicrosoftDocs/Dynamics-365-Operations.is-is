---
title: Listi yfir ER-aðgerðir í rökfræðiflokknum
description: Þetta efni veitir upplýsingar um röklegar aðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916638"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="a09a1-103">Listi yfir ER-aðgerðir í rökfræðiflokknum</span><span class="sxs-lookup"><span data-stu-id="a09a1-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a09a1-104">Rafrænar skýrslutökur (ER) geta verið notaðar til að vinna með rökleg gildi til að framkvæma fleiri en einn samanburð á einni tjáningu eða prófa margar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="a09a1-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="a09a1-105">Þetta efni gefur yfirlit yfir þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="a09a1-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="a09a1-106">Listi yfir studdar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="a09a1-106">List of supported functions</span></span>

| <span data-ttu-id="a09a1-107">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="a09a1-107">Function</span></span> | <span data-ttu-id="a09a1-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="a09a1-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="a09a1-109">Og</span><span class="sxs-lookup"><span data-stu-id="a09a1-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="a09a1-110">Þessi aðgerð skilar *Boolean*-gildi **SATT** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="a09a1-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="a09a1-111">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a09a1-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="a09a1-112">Tilvik</span><span class="sxs-lookup"><span data-stu-id="a09a1-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="a09a1-113">Þessi aðgerð metur gildi tiltekinnar segðar á móti tilgreindum valkostum og skilar niðurstöðu fyrsta valmöguleikans sem jafngildir gildi tiltekinnar segðar.</span><span class="sxs-lookup"><span data-stu-id="a09a1-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="a09a1-114">Annars skilar hún valkvæðri sjálfgefinni niðurstöðu, ef sjálfgefin niðurstaða er tilgreind sem síðasta frumbreyta kallaðrar aðgerðar sem valkostur kemur ekki á undan.</span><span class="sxs-lookup"><span data-stu-id="a09a1-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="a09a1-115">Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="a09a1-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="a09a1-116">Ef</span><span class="sxs-lookup"><span data-stu-id="a09a1-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="a09a1-117">Þessi aðgerð skilar fyrsta tilgreinda gildinu ef tilgreinda skilyrðið er uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="a09a1-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="a09a1-118">Að öðrum kosti skilar hún öðru tilgreinda gildinu.</span><span class="sxs-lookup"><span data-stu-id="a09a1-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="a09a1-119">Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru.</span><span class="sxs-lookup"><span data-stu-id="a09a1-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="a09a1-120">Ekki</span><span class="sxs-lookup"><span data-stu-id="a09a1-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="a09a1-121">Þessi aðgerð skilar bakfærðu röklegu gildi tilgreinds skilyrðis sem *Boolean*-gildi.</span><span class="sxs-lookup"><span data-stu-id="a09a1-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="a09a1-122">Or</span><span class="sxs-lookup"><span data-stu-id="a09a1-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="a09a1-123">Þessi aðgerð skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn.</span><span class="sxs-lookup"><span data-stu-id="a09a1-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="a09a1-124">Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="a09a1-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="a09a1-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="a09a1-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="a09a1-126">Þessi aðgerð ákvarðar hvort tilgreint ílag passar við eitthvert gildi tilgreinds hlutar sem er í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="a09a1-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="a09a1-127">Hún skilar *Boolean*-gildinu **TRUE** ef tilgreint inntak passar við niðurstöðu þess að keyra tiltekna segð fyrir að minnsta kosti eina skrá af tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="a09a1-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="a09a1-128">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a09a1-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a09a1-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a09a1-129">Additional resources</span></span>

[<span data-ttu-id="a09a1-130">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a09a1-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a09a1-131">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a09a1-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="a09a1-132">Formúlutungumál í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a09a1-132">Electronic reporting formula language</span></span>](er-formula-language.md)

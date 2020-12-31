---
title: Fjöldi bóka í hverri færslubók
description: Í þessu efnisatriði er lýst venslum á milli færslubóka og eignabóka þegar eignakaup eða afskriftartillaga er stofnuð í gegnum runuvinnslu. Hægt er að skilgreina hámarksfjölda bóka sem eru innifaldar fyrir hver kaup og fyrir afskriftir.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d4ba98cefdc0b555eedfaa56b6a3ca4870b5de93
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650666"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="ee498-104">Fjöldi bóka í hverri færslubók</span><span class="sxs-lookup"><span data-stu-id="ee498-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee498-105">Í þessu efnisatriði er lýst venslum á milli færslubóka og eignabóka þegar eignakaup eða afskriftartillaga er stofnuð í gegnum runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="ee498-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="ee498-106">Hægt er að skilgreina hámarksfjölda bóka sem eru teknar með fyrir hver kaup og fyrir afskriftir með því að nota svæðin í hlutanum **Fjölda bóka á færslubók** á flipanum **Almennt** á síðunni **Eignafæribreytur** (**Eignir \> Uppsetning \> Eignafæribreytur**).</span><span class="sxs-lookup"><span data-stu-id="ee498-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="ee498-107">Þessi svæði gera þér kleift að dreifa fjölda eignabóka á hverja kaupabók og afskriftarbók.</span><span class="sxs-lookup"><span data-stu-id="ee498-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="ee498-108">Fyrir kauptillögu er sjálfgefið gildi að minnsta kosti 10.000 bækur.</span><span class="sxs-lookup"><span data-stu-id="ee498-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="ee498-109">Fyrir afskriftartillögu er sjálfgefið gildi að minnsta kosti 2.000 bækur.</span><span class="sxs-lookup"><span data-stu-id="ee498-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="ee498-110">Til dæmis ef það eru 4000 eignir og tvær bækur eru tengdar við hverja eign verður ein bók bókuð í núgildandi lag og hin bókin verður bókuð á skattalagið.</span><span class="sxs-lookup"><span data-stu-id="ee498-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="ee498-111">Ef 4.000 eignir eru keyptar í gegnum runuvinnslu, mun runuvinnslan sem stofnar eina eignakaupbók innihalda 4.000 eignabækur.</span><span class="sxs-lookup"><span data-stu-id="ee498-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="ee498-112">Færslubókin sem er stofnuð verður áfram notuð þar til runuvinnslunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="ee498-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="ee498-113">Afleiddar bækur eru ekki teknar með í hámarksfjölda bóka fyrir hverja færslubók.</span><span class="sxs-lookup"><span data-stu-id="ee498-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="ee498-114">Hægt er að nota runuvinnslu til að keyra afskriftir fyrir sama safn af keyptum eignum.</span><span class="sxs-lookup"><span data-stu-id="ee498-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="ee498-115">Til dæmis er stofnar runuvinnsla tvær afskriftarbækur, sem hvor samanstendur af 2000 eignabókum.</span><span class="sxs-lookup"><span data-stu-id="ee498-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="ee498-116">Fyrsta færslubókin mun innihalda bækur sem eru tengdar við eignir sem eru númeraðar 1 til 2.000.</span><span class="sxs-lookup"><span data-stu-id="ee498-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="ee498-117">Önnur færslubókin mun svo innihalda bækur sem eru tengdar við eignir sem eru númeraðar 2.001 til 4.000.</span><span class="sxs-lookup"><span data-stu-id="ee498-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="ee498-118">Runuvinnslu útilokar lokaðar bækur.</span><span class="sxs-lookup"><span data-stu-id="ee498-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="ee498-119">Í runuvinnslu fyrir afskrift er t.d. 10 af fyrstu 2.000 bókunum lokað.</span><span class="sxs-lookup"><span data-stu-id="ee498-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="ee498-120">Í þessu tilfelli mun fyrsta færslubókin innihalda bækur sem eru tengdar við eignir sem eru númeraðar 1 til 2011.</span><span class="sxs-lookup"><span data-stu-id="ee498-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="ee498-121">Önnur færslubókin mun svo innihalda bækur sem eru tengdar við eignir sem eru númeraðar 2.012 til 4.000.</span><span class="sxs-lookup"><span data-stu-id="ee498-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

<span data-ttu-id="ee498-122">Mörkin á fjölda bóka eru notuð ef tvítekin eignaauðkenni eru ekki til í sömu færslubók.</span><span class="sxs-lookup"><span data-stu-id="ee498-122">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="ee498-123">Hins vegar ef eignaauðkennið er það sama og auðkenni bókarinnar, er hægt að fara umfram fjölda bóka fyrir hverja færslubók til að halda eignaauðkenninu í sömu færslubók.</span><span class="sxs-lookup"><span data-stu-id="ee498-123">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="ee498-124">Til dæmis eru til 5001 eignaauðkenni, þrjár bækur eru tengdar við hvert auðkenni og hver eignabók er bókuð á sama bókunarlagið.</span><span class="sxs-lookup"><span data-stu-id="ee498-124">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="ee498-125">Afskriftir eru keyrðar fyrir þrjá samfellda mánuði, án samantektar.</span><span class="sxs-lookup"><span data-stu-id="ee498-125">You run depreciation for three consecutive months, without summarization.</span></span> <span data-ttu-id="ee498-126">Afskriftarbókin verður stofnuð í gegnum runuvinnslu og kerfið býr til sjö færslubækur með 667 eignaauðkennum og þremur bókum fyrir hvert auðkenni.</span><span class="sxs-lookup"><span data-stu-id="ee498-126">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="ee498-127">Útkoman verður 2.001 bækur.</span><span class="sxs-lookup"><span data-stu-id="ee498-127">The result will be 2,001 books.</span></span> <span data-ttu-id="ee498-128">Eftir þrjá mánuði verða því 6003 færslubókarlínur til að viðhalda sömu auðkennum eignar í sömu færslubók.</span><span class="sxs-lookup"><span data-stu-id="ee498-128">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="ee498-129">Kerfið stofnar einnig eina færslubók með 332 eignaauðkennum og þremur bókum fyrir hvert auðkenni.</span><span class="sxs-lookup"><span data-stu-id="ee498-129">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="ee498-130">Eftir þrjá mánuði verða línurnar 2.988.</span><span class="sxs-lookup"><span data-stu-id="ee498-130">In three months, there will be 2,988 lines.</span></span>

---
title: Afskriftaraðferðir og venjur
description: Þessi grein veitir yfirlit yfir afskriftarreglur og afskriftaraðferðir sem eru studdar af Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a7bce93c955ce64da129bdb1a3e9905279838c3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840626"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="a4b55-103">Afskriftaaðferðir og hefðir</span><span class="sxs-lookup"><span data-stu-id="a4b55-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4b55-104">Þessi grein veitir yfirlit yfir afskriftarreglur og afskriftaraðferðir sem eru studdar af Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a4b55-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a4b55-105">Hægt er að velja ýmsar afskriftaaðferðir og reglur.</span><span class="sxs-lookup"><span data-stu-id="a4b55-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="a4b55-106">Tilgangur aðferðanna er að úthluta afskriftavirði eignarinnar á fjárhagstímabil.</span><span class="sxs-lookup"><span data-stu-id="a4b55-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="a4b55-107">Afskriftavirði eignarinnar er kaupverðið að frádregnu hugsanlegu rýrnunarvirði.</span><span class="sxs-lookup"><span data-stu-id="a4b55-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="a4b55-108">Ef afskriftareglur eru notaðar og síðustu dagsetningu afskriftakeyrslu eignar er breytt, sem veldur því síðan að nokkrum afskriftum er sleppt, gætu afskriftir síðasta árs verið meiri eða minni en áætlað var.</span><span class="sxs-lookup"><span data-stu-id="a4b55-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="a4b55-109">Afskriftirnar eru leiðréttar eftir fjölda afskriftatímabila sem verða fyrir áhrifum af breytingunni á síðustu dagsetningu afskriftakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="a4b55-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="a4b55-110">Til dæmis, ef hálfsárs afskriftareglan hefur verið notuð í þrjú ár, eiga afskriftirnar sér stað yfir 3 1/2 ár.</span><span class="sxs-lookup"><span data-stu-id="a4b55-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="a4b55-111">Ef síðustu dagsetningu afskriftakeyrslu þessa 3 1/2 árs var breytt, flytur síðasta afskriftaárið út fjölda tímabila sem urðu fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="a4b55-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="a4b55-112">Ef dagsetningin er flutt um þrjá mánuði, hefur síðasta árið níu mánaða virði til afskrifta þegar alla jafna hefði verið sex mánaða virði til afskrifta.</span><span class="sxs-lookup"><span data-stu-id="a4b55-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="a4b55-113">Hægt er að velja úr eftirfarandi afskriftareglum.</span><span class="sxs-lookup"><span data-stu-id="a4b55-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="a4b55-114">Hálft ár</span><span class="sxs-lookup"><span data-stu-id="a4b55-114">Half year</span></span>
-   <span data-ttu-id="a4b55-115">Heill mánuður</span><span class="sxs-lookup"><span data-stu-id="a4b55-115">Full month</span></span>
-   <span data-ttu-id="a4b55-116">Miður fjórðungur</span><span class="sxs-lookup"><span data-stu-id="a4b55-116">Mid quarter</span></span>
-   <span data-ttu-id="a4b55-117">Miður mánuður (fyrsti mánaðar)</span><span class="sxs-lookup"><span data-stu-id="a4b55-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="a4b55-118">Miður mánuður (15. mánaðar)</span><span class="sxs-lookup"><span data-stu-id="a4b55-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="a4b55-119">Hálft ár (byrjun árs)</span><span class="sxs-lookup"><span data-stu-id="a4b55-119">Half year (start of year)</span></span>
-   <span data-ttu-id="a4b55-120">Hálft ár (næsta ár)</span><span class="sxs-lookup"><span data-stu-id="a4b55-120">Half year (next year)</span></span>

<span data-ttu-id="a4b55-121">Hægt er að velja á milli eftirfarandi afskriftaraðferða.</span><span class="sxs-lookup"><span data-stu-id="a4b55-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="a4b55-122">Línuleg á líftíma</span><span class="sxs-lookup"><span data-stu-id="a4b55-122">Straight line service life</span></span>
-   <span data-ttu-id="a4b55-123">Bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-123">Reducing balance</span></span>
-   <span data-ttu-id="a4b55-124">Beinskiptur</span><span class="sxs-lookup"><span data-stu-id="a4b55-124">Manual</span></span>
-   <span data-ttu-id="a4b55-125">Stuðull</span><span class="sxs-lookup"><span data-stu-id="a4b55-125">Factor</span></span>
-   <span data-ttu-id="a4b55-126">Notkun</span><span class="sxs-lookup"><span data-stu-id="a4b55-126">Consumption</span></span>
-   <span data-ttu-id="a4b55-127">Línuleg á eftirstöðvum líftíma</span><span class="sxs-lookup"><span data-stu-id="a4b55-127">Straight line life remaining</span></span>
-   <span data-ttu-id="a4b55-128">200% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-128">200% reducing balance</span></span>
-   <span data-ttu-id="a4b55-129">175% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-129">175% reducing balance</span></span>
-   <span data-ttu-id="a4b55-130">150% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-130">150% reducing balance</span></span>
-   <span data-ttu-id="a4b55-131">125% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="a4b55-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a4b55-132">Additional resources</span></span>
--------

[<span data-ttu-id="a4b55-133">Afskriftir eigna</span><span class="sxs-lookup"><span data-stu-id="a4b55-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="a4b55-134">Línuleg afskrift líftíma</span><span class="sxs-lookup"><span data-stu-id="a4b55-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="a4b55-135">Afskrift bókfærðs virðis</span><span class="sxs-lookup"><span data-stu-id="a4b55-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="a4b55-136">Handvirkar afskriftir</span><span class="sxs-lookup"><span data-stu-id="a4b55-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="a4b55-137">Afskrift stuðuls</span><span class="sxs-lookup"><span data-stu-id="a4b55-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="a4b55-138">Notkunarafskrift</span><span class="sxs-lookup"><span data-stu-id="a4b55-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="a4b55-139">Línuleg afskrift eftirstandandi líftíma</span><span class="sxs-lookup"><span data-stu-id="a4b55-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="a4b55-140">Afskriftir fyrir 125% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a4b55-141">Afskriftir fyrir 150% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a4b55-142">Afskriftir fyrir 175% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a4b55-143">Afskriftir fyrir 200% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a4b55-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)




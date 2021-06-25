---
title: Afskriftaraðferðir og venjur
description: Þessi grein veitir yfirlit yfir afskriftarreglur og afskriftaraðferðir sem eru studdar af Microsoft Dynamics 365 Finance.
author: ShylaThompson
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76b20c895519edb7316c2b9a6b223a109a307e77
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189398"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="a434e-103">Afskriftaaðferðir og hefðir</span><span class="sxs-lookup"><span data-stu-id="a434e-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a434e-104">Þessi grein veitir yfirlit yfir studdar afskriftarreglur og afskriftaraðferðir.</span><span class="sxs-lookup"><span data-stu-id="a434e-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="a434e-105">Hægt er að velja ýmsar afskriftaaðferðir og reglur.</span><span class="sxs-lookup"><span data-stu-id="a434e-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="a434e-106">Tilgangur aðferðanna er að úthluta afskriftavirði eignarinnar á fjárhagstímabil.</span><span class="sxs-lookup"><span data-stu-id="a434e-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="a434e-107">Afskriftavirði eignarinnar er kaupverðið að frádregnu hugsanlegu rýrnunarvirði.</span><span class="sxs-lookup"><span data-stu-id="a434e-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="a434e-108">Ef afskriftareglur eru notaðar og síðustu dagsetningu afskriftakeyrslu eignar er breytt, sem veldur því síðan að nokkrum afskriftum er sleppt, gætu afskriftir síðasta árs verið meiri eða minni en áætlað var.</span><span class="sxs-lookup"><span data-stu-id="a434e-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="a434e-109">Afskriftirnar eru leiðréttar eftir fjölda afskriftatímabila sem verða fyrir áhrifum af breytingunni á síðustu dagsetningu afskriftakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="a434e-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="a434e-110">Til dæmis, ef hálfsárs afskriftareglan hefur verið notuð í þrjú ár, eiga afskriftirnar sér stað yfir 3 1/2 ár.</span><span class="sxs-lookup"><span data-stu-id="a434e-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="a434e-111">Ef síðustu dagsetningu afskriftakeyrslu þessa 3 1/2 árs var breytt, flytur síðasta afskriftaárið út fjölda tímabila sem urðu fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="a434e-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="a434e-112">Ef dagsetningin er flutt um þrjá mánuði, hefur síðasta árið níu mánaða virði til afskrifta þegar alla jafna hefði verið sex mánaða virði til afskrifta.</span><span class="sxs-lookup"><span data-stu-id="a434e-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="a434e-113">Hægt er að velja úr eftirfarandi afskriftareglum.</span><span class="sxs-lookup"><span data-stu-id="a434e-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="a434e-114">Hálft ár</span><span class="sxs-lookup"><span data-stu-id="a434e-114">Half year</span></span>
-   <span data-ttu-id="a434e-115">Heill mánuður</span><span class="sxs-lookup"><span data-stu-id="a434e-115">Full month</span></span>
-   <span data-ttu-id="a434e-116">Miður fjórðungur</span><span class="sxs-lookup"><span data-stu-id="a434e-116">Mid quarter</span></span>
-   <span data-ttu-id="a434e-117">Miður mánuður (fyrsti mánaðar)</span><span class="sxs-lookup"><span data-stu-id="a434e-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="a434e-118">Miður mánuður (15. mánaðar)</span><span class="sxs-lookup"><span data-stu-id="a434e-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="a434e-119">Hálft ár (byrjun árs)</span><span class="sxs-lookup"><span data-stu-id="a434e-119">Half year (start of year)</span></span>
-   <span data-ttu-id="a434e-120">Hálft ár (næsta ár)</span><span class="sxs-lookup"><span data-stu-id="a434e-120">Half year (next year)</span></span>

<span data-ttu-id="a434e-121">Hægt er að velja á milli eftirfarandi afskriftaraðferða.</span><span class="sxs-lookup"><span data-stu-id="a434e-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="a434e-122">Línuleg á líftíma</span><span class="sxs-lookup"><span data-stu-id="a434e-122">Straight line service life</span></span>
-   <span data-ttu-id="a434e-123">Bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-123">Reducing balance</span></span>
-   <span data-ttu-id="a434e-124">Beinskiptur</span><span class="sxs-lookup"><span data-stu-id="a434e-124">Manual</span></span>
-   <span data-ttu-id="a434e-125">Stuðull</span><span class="sxs-lookup"><span data-stu-id="a434e-125">Factor</span></span>
-   <span data-ttu-id="a434e-126">Notkun</span><span class="sxs-lookup"><span data-stu-id="a434e-126">Consumption</span></span>
-   <span data-ttu-id="a434e-127">Línuleg á eftirstöðvum líftíma</span><span class="sxs-lookup"><span data-stu-id="a434e-127">Straight line life remaining</span></span>
-   <span data-ttu-id="a434e-128">200% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-128">200% reducing balance</span></span>
-   <span data-ttu-id="a434e-129">175% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-129">175% reducing balance</span></span>
-   <span data-ttu-id="a434e-130">150% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-130">150% reducing balance</span></span>
-   <span data-ttu-id="a434e-131">125% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-131">125% reducing balance</span></span>





## <a name="additional-resources"></a><span data-ttu-id="a434e-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a434e-132">Additional resources</span></span>

[<span data-ttu-id="a434e-133">Afskriftir eigna</span><span class="sxs-lookup"><span data-stu-id="a434e-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="a434e-134">Línuleg afskrift líftíma</span><span class="sxs-lookup"><span data-stu-id="a434e-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="a434e-135">Afskrift lækkandi stöðu</span><span class="sxs-lookup"><span data-stu-id="a434e-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="a434e-136">Handvirkar afskriftir</span><span class="sxs-lookup"><span data-stu-id="a434e-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="a434e-137">Afskrift stuðuls</span><span class="sxs-lookup"><span data-stu-id="a434e-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="a434e-138">Notkunarafskrift</span><span class="sxs-lookup"><span data-stu-id="a434e-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="a434e-139">Línuleg afskrift eftirstandandi líftíma</span><span class="sxs-lookup"><span data-stu-id="a434e-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="a434e-140">Afskriftir fyrir 125% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a434e-141">Afskriftir fyrir 150% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a434e-142">Afskriftir fyrir 175% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a434e-143">Afskriftir fyrir 200% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a434e-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
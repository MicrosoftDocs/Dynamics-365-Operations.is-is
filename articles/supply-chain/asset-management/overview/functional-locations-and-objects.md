---
title: Virkar staðsetningar og eignir
description: Þetta efni lýsir virkum staðsetningum og eignum í eignastýringu. Eignastýring er ítarleg eining til að stjórna eignum og viðhaldsstörfum í Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53091f2e3c159f73f11b3dfcefd597f2c1494d19
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253087"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="e2949-104">Virkar staðsetningar og eignir</span><span class="sxs-lookup"><span data-stu-id="e2949-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e2949-105">Þetta efni lýsir virkum staðsetningum og eignum í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="e2949-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="e2949-106">Eignastýring er ítarleg eining til að stjórna eignum og viðhaldsstörfum í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2949-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="e2949-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e2949-107">Overview</span></span>

<span data-ttu-id="e2949-108">Eignastjórnun er samþætt óaðfinnanlega við nokkrar einingar við önnur forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2949-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="e2949-109">Eftirfarandi mynd sýnir viðmót við aðrar einingar.</span><span class="sxs-lookup"><span data-stu-id="e2949-109">The following illustration shows the interfaces with other modules.</span></span>

![Skýringarmynd sem sýnir hvernig eignastjórnun tengist öðrum einingum](media/01-overview-image.png)

<span data-ttu-id="e2949-111">Eignastjórnun gerir þér kleift að stjórna og framkvæma öll verkefni sem tengjast stjórnun og þjónustu á mörgum gerðum búnaðar í fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="e2949-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="e2949-112">Þessi búnaður inniheldur vélar, framleiðslutæki og farartæki.</span><span class="sxs-lookup"><span data-stu-id="e2949-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="e2949-113">Eignastjórnun styður einnig lausnir í fjölmörgum atvinnugreinum.</span><span class="sxs-lookup"><span data-stu-id="e2949-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="e2949-114">Eftirfarandi mynd sýnir yfirlit yfir helstu virkni sem fellur undir eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="e2949-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Skýringarmynd sem sýnir helstu virkni í eignastýringu](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="e2949-116">Virkar staðsetningar og eignir</span><span class="sxs-lookup"><span data-stu-id="e2949-116">Functional locations and assets</span></span>

<span data-ttu-id="e2949-117">Virkar staðsetningar eru notaðar til að stjórna eignum á stöðum.</span><span class="sxs-lookup"><span data-stu-id="e2949-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="e2949-118">Þessi stjórnun felur í sér mælingar á eignakostnaði á virkum stöðum.</span><span class="sxs-lookup"><span data-stu-id="e2949-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="e2949-119">Virkar staðsetningar eru byggðar upp með stigveldi og staðsetningar geta verið með undirstaðsetningar.</span><span class="sxs-lookup"><span data-stu-id="e2949-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="e2949-120">Uppbygging virkrar staðsetningar er föst.</span><span class="sxs-lookup"><span data-stu-id="e2949-120">The structure of functional locations is static.</span></span> <span data-ttu-id="e2949-121">Með öðrum orðum, staðsetningar geta ekki breytt staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="e2949-121">In other words, locations can't change place.</span></span> <span data-ttu-id="e2949-122">Hægt er að setja upp eignir á virkum stöðum og, eins og krafist er, hægt að setja þær upp á öðrum virkum stöðum síðar.</span><span class="sxs-lookup"><span data-stu-id="e2949-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="e2949-123">Eignakostnaður fylgir alltaf staðsetningu eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="e2949-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="e2949-124">Með öðrum orðum, ef þú setur upp eign á nýjum stað, notar eignin sjálfkrafa fjárhagsvíddina sem tengjast nýju virku staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="e2949-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="e2949-125">Þess vegna er eignakostnaður alltaf tengdur virku staðsetningunni sem eignin er nú sett upp á.</span><span class="sxs-lookup"><span data-stu-id="e2949-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="e2949-126">Þessi sjálfvirka meðhöndlun fjárhagsvíddar hjálpar til við að tryggja fullkomnar mælingar á kostnaði þegar fyrirtæki þitt framkvæmir verkefnastjórnun og skýrslugerð um virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="e2949-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="e2949-127">Hvernig þú byggir stigveldi þitt yfir virkar staðsetningar fer eftir kröfum fyrirtækisins um viðhald á innri búnaði eða þjónustu við viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="e2949-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="e2949-128">Eftirfarandi mynd sýnir dæmi um virkar staðsetningar sem eru byggðir á landfræðilegum stöðum.</span><span class="sxs-lookup"><span data-stu-id="e2949-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Skýringarmynd sem sýnir virkar staðsetningar út frá landfræðilegum stöðum](media/03-overview-image.png)

<span data-ttu-id="e2949-130">Eftirfarandi mynd sýnir dæmi um virkar staðsetningar sem eru byggðir á viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="e2949-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Skýringarmynd sem sýnir virkar staðsetningar út frá viðskiptavinum](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
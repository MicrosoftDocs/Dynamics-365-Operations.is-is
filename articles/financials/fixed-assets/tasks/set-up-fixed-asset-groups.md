---
title: Setja upp eignaflokka
description: Þessi ferli sýnir hvernig á að stofna nýjan flokk eigna.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48784ef4eb12a4a1cae3387e3a45afdf34f2a0fd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546433"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="d79bf-103">Setja upp eignaflokka</span><span class="sxs-lookup"><span data-stu-id="d79bf-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d79bf-104">Þessi ferli sýnir hvernig á að stofna nýjan flokk eigna.</span><span class="sxs-lookup"><span data-stu-id="d79bf-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="d79bf-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="d79bf-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d79bf-106">Fara í Eignir > Uppsetning > Eignaflokkar.</span><span class="sxs-lookup"><span data-stu-id="d79bf-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="d79bf-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d79bf-107">Click New.</span></span>
3. <span data-ttu-id="d79bf-108">Færa inn gildi í svæðinu eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="d79bf-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="d79bf-109">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d79bf-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d79bf-110">Tölusetja fastar eignir og kóða númeraraðar í eignaflokknum mun hnekkja stillingum í færibreytum eigna.</span><span class="sxs-lookup"><span data-stu-id="d79bf-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="d79bf-111">Hægt er að breyta því hér ef eignir í þessum eignaflokki hafa mismunandi tölusetningu af öðrum flokki.</span><span class="sxs-lookup"><span data-stu-id="d79bf-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="d79bf-112">Smelltu á bækur.</span><span class="sxs-lookup"><span data-stu-id="d79bf-112">Click Books.</span></span>
6. <span data-ttu-id="d79bf-113">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="d79bf-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d79bf-114">Svæði Reikna út afskriftir er á Já, eignabók verður taka með í afskriftartillaga.</span><span class="sxs-lookup"><span data-stu-id="d79bf-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="d79bf-115">Ef Reikna afskrift er stillt á Nei, verða eign ekki að vera sjálfkrafa afskrifa .</span><span class="sxs-lookup"><span data-stu-id="d79bf-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="d79bf-116">Stillið líftíma ef viðbótin eykur líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="d79bf-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="d79bf-117">Athugaðu að svæði afskriftartímabils gildið er reiknað eftir uppsetningu líftíma.</span><span class="sxs-lookup"><span data-stu-id="d79bf-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="d79bf-118">Veljið valkost í svæðinu afskriftarregla.</span><span class="sxs-lookup"><span data-stu-id="d79bf-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="d79bf-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d79bf-119">Close the page.</span></span>


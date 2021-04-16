---
title: Setja upp eignaflokka
description: Þetta efni útskýrir hvernig á að stofna nýjan flokk eigna.
author: saraschi2
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c1b97193f09cfbb943522ca7af6bace9a14d9cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819555"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="8dc93-103">Setja upp eignaflokka</span><span class="sxs-lookup"><span data-stu-id="8dc93-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8dc93-104">Þetta efni útskýrir hvernig á að stofna nýjan flokk eigna.</span><span class="sxs-lookup"><span data-stu-id="8dc93-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="8dc93-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="8dc93-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8dc93-106">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Uppsetning > Eignaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="8dc93-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="8dc93-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8dc93-107">Select **New**.</span></span>
3. <span data-ttu-id="8dc93-108">Færa inn gildi í reitnum **Eignaflokkur**.</span><span class="sxs-lookup"><span data-stu-id="8dc93-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="8dc93-109">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8dc93-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="8dc93-110">Tölusetning fastra eigna og kóða númeraraðar í **Eignaflokknum** mun hnekkja stillingum í færibreytum eigna.</span><span class="sxs-lookup"><span data-stu-id="8dc93-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="8dc93-111">Hægt er að breyta því hér ef eignir í þessum eignaflokki hafa mismunandi tölusetningu af öðrum flokki.</span><span class="sxs-lookup"><span data-stu-id="8dc93-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="8dc93-112">Veldu **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="8dc93-112">Select **Books**.</span></span>
6. <span data-ttu-id="8dc93-113">Sláið inn eða veldu gildi í reitnum **Bók**.</span><span class="sxs-lookup"><span data-stu-id="8dc93-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="8dc93-114">Reiturinn **Reikna út afskriftir** er stilltur á **Já**, svo að eignabók verður tekin með í afskriftartillögur.</span><span class="sxs-lookup"><span data-stu-id="8dc93-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="8dc93-115">Ef **Reikna afskrift** er stillt á **Nei** verður eignin ekki sjálfkrafa afskrifuð.</span><span class="sxs-lookup"><span data-stu-id="8dc93-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="8dc93-116">Stillið líftíma ef viðbótin eykur líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="8dc93-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="8dc93-117">Athugaðu að reitagildið **Afskriftartímabil** er reiknað eftir uppsetningu líftíma.</span><span class="sxs-lookup"><span data-stu-id="8dc93-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="8dc93-118">Veljið valkost í reitnum **Afskriftarregla**.</span><span class="sxs-lookup"><span data-stu-id="8dc93-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="8dc93-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8dc93-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Setja upp aukagjöld stöðvar og sniðmát fyrir aukaþjónustu
description: Þessi ferli sýnir hvernig stofna á aukalegt sniðmát fyrir stöðvar í og nota sniðmátið til að stofna aukagjald stöðvar.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSHubAccessorial, TMSAccessorialMaster, TMSCarrierAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f728339ed9a0c6fffa8f6d8171976aafc41fc75e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016540"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="aebda-103">Setja upp aukagjöld stöðvar og sniðmát fyrir aukaþjónustu</span><span class="sxs-lookup"><span data-stu-id="aebda-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aebda-104">Þessi ferli sýnir hvernig stofna á aukalegt sniðmát fyrir stöðvar í og nota sniðmátið til að stofna aukagjald stöðvar.</span><span class="sxs-lookup"><span data-stu-id="aebda-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="aebda-105">Þessi aðferð notar gagnamengi USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="aebda-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="aebda-106">Þessi uppsetning er yfirleitt gert af samræmingaraðili flutninga.</span><span class="sxs-lookup"><span data-stu-id="aebda-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="aebda-107">Setja upp stöðvarsniðmát</span><span class="sxs-lookup"><span data-stu-id="aebda-107">Set up a hub master</span></span>
1. <span data-ttu-id="aebda-108">Fara í flutningsstjórnun > Uppsetning > Einkunn > Aukalegt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="aebda-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="aebda-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="aebda-109">Click New.</span></span>
3. <span data-ttu-id="aebda-110">Í reitinn Aukalegt sniðmát skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="aebda-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="aebda-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="aebda-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="aebda-112">Veljið 'Stöðvar' í svæðinu gerð þess aukalega.</span><span class="sxs-lookup"><span data-stu-id="aebda-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="aebda-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="aebda-113">Click Save.</span></span>
7. <span data-ttu-id="aebda-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="aebda-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="aebda-115">Setja upp aukagjald stöðvar</span><span class="sxs-lookup"><span data-stu-id="aebda-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="aebda-116">Fara í flutningsstjórnun > Uppsetning >Einkunn > Aukagjald stöðvar.</span><span class="sxs-lookup"><span data-stu-id="aebda-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="aebda-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="aebda-117">Click New.</span></span>
3. <span data-ttu-id="aebda-118">Færa inn gildi í reitnum aukalegt Auðkenni Stöðvar.</span><span class="sxs-lookup"><span data-stu-id="aebda-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="aebda-119">Í reitnum Stöð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aebda-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="aebda-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aebda-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="aebda-121">Í reitnum Staða stöðvar skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="aebda-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="aebda-122">Hægt er að stofna gjaldið sem söfnunar- eða affermingargjald.</span><span class="sxs-lookup"><span data-stu-id="aebda-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="aebda-123">Eftir því hvað var valið mun gjöld vera lögð á samsvarandi flutningshluta á leiðinni þinni.</span><span class="sxs-lookup"><span data-stu-id="aebda-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="aebda-124">Í reitnum Aukalegt sniðmát skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aebda-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="aebda-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="aebda-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aebda-126">Velja sniðmát sem nýverið var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="aebda-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="aebda-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="aebda-127">Click Save.</span></span>
10. <span data-ttu-id="aebda-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="aebda-128">Close the page.</span></span>


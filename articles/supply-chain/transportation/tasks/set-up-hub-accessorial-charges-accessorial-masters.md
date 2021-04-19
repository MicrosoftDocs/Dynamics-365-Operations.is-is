---
title: Setja upp aukagjöld stöðvar og sniðmát fyrir aukaþjónustu
description: Þessi ferli sýnir hvernig stofna á aukalegt sniðmát fyrir stöðvar í og nota sniðmátið til að stofna aukagjald stöðvar.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f4c0d3af96e6ef6735b01165a49c1450b3b633b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837563"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="842bd-103">Setja upp aukagjöld stöðvar og sniðmát fyrir aukaþjónustu</span><span class="sxs-lookup"><span data-stu-id="842bd-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="842bd-104">Þessi ferli sýnir hvernig stofna á aukalegt sniðmát fyrir stöðvar í og nota sniðmátið til að stofna aukagjald stöðvar.</span><span class="sxs-lookup"><span data-stu-id="842bd-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="842bd-105">Þessi aðferð notar gagnamengi USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="842bd-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="842bd-106">Þessi uppsetning er yfirleitt gert af samræmingaraðili flutninga.</span><span class="sxs-lookup"><span data-stu-id="842bd-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="842bd-107">Setja upp stöðvarsniðmát</span><span class="sxs-lookup"><span data-stu-id="842bd-107">Set up a hub master</span></span>
1. <span data-ttu-id="842bd-108">Fara í flutningsstjórnun > Uppsetning > Einkunn > Aukalegt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="842bd-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="842bd-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="842bd-109">Click New.</span></span>
3. <span data-ttu-id="842bd-110">Í reitinn Aukalegt sniðmát skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="842bd-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="842bd-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="842bd-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="842bd-112">Veljið 'Stöðvar' í svæðinu gerð þess aukalega.</span><span class="sxs-lookup"><span data-stu-id="842bd-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="842bd-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="842bd-113">Click Save.</span></span>
7. <span data-ttu-id="842bd-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="842bd-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="842bd-115">Setja upp aukagjald stöðvar</span><span class="sxs-lookup"><span data-stu-id="842bd-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="842bd-116">Fara í flutningsstjórnun > Uppsetning >Einkunn > Aukagjald stöðvar.</span><span class="sxs-lookup"><span data-stu-id="842bd-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="842bd-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="842bd-117">Click New.</span></span>
3. <span data-ttu-id="842bd-118">Færa inn gildi í reitnum aukalegt Auðkenni Stöðvar.</span><span class="sxs-lookup"><span data-stu-id="842bd-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="842bd-119">Í reitnum Stöð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="842bd-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="842bd-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="842bd-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="842bd-121">Í reitnum Staða stöðvar skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="842bd-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="842bd-122">Hægt er að stofna gjaldið sem söfnunar- eða affermingargjald.</span><span class="sxs-lookup"><span data-stu-id="842bd-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="842bd-123">Eftir því hvað var valið mun gjöld vera lögð á samsvarandi flutningshluta á leiðinni þinni.</span><span class="sxs-lookup"><span data-stu-id="842bd-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="842bd-124">Í reitnum Aukalegt sniðmát skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="842bd-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="842bd-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="842bd-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="842bd-126">Velja sniðmát sem nýverið var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="842bd-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="842bd-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="842bd-127">Click Save.</span></span>
10. <span data-ttu-id="842bd-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="842bd-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Birgðamerking með fínstillingu áætlanagerðar
description: Þetta efnisatriði inniheldur upplýsingar um valkostina sem eru tiltækir til að merkja birgðir í staðfestum pöntunum þegar fínstilling skipulagningar er notuð.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263351"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="008dc-103">Birgðamerking með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="008dc-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="008dc-104">Þetta efnisatriði inniheldur upplýsingar um valkostina sem eru tiltækir til að merkja birgðir í staðfestum pöntunum þegar fínstilling skipulagningar er notuð.</span><span class="sxs-lookup"><span data-stu-id="008dc-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="008dc-105">*Merking* er notuð til að tengja framboð og eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="008dc-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="008dc-106">Slíkt er svipað og *þarfarakning*, sem gefur til kynna hvernig aðaláætlanagerð gerir ráð fyrir því að uppfylla eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="008dc-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="008dc-107">Frá áætlunarsjónarmiði séð er helsti munurinn sá að merking er varanlegri en þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="008dc-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="008dc-108">Merking var tekin í notkun til að styðja við sérstakar kostnaðaraðstæður samkvæmt reglum FIFO- og LIFO-birgðarmatsaðferðanna.</span><span class="sxs-lookup"><span data-stu-id="008dc-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="008dc-109">Hins vegar er það nú einnig notað fyrir aðstæður sem ekki fela í sér kostnað.</span><span class="sxs-lookup"><span data-stu-id="008dc-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="008dc-110">Merking milli framboðs og eftirspurnar er valfrjáls og nær varanleg.</span><span class="sxs-lookup"><span data-stu-id="008dc-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="008dc-111">Notandi getur fjarlægt merkingu handvirkt eða hana má fjarlægja með því að keyra niðurbrot sölupöntunarlínu þar sem valkosturinn **Fjarlægja merkingu** er valinn.</span><span class="sxs-lookup"><span data-stu-id="008dc-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="008dc-112">Þarfarakningu er stjórnað af aðaláætlanagerð á meðan á þekju stendur til að tengja eftirspurn við nauðsynleg framboð.</span><span class="sxs-lookup"><span data-stu-id="008dc-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="008dc-113">Hægt er að uppfæra þarfarakningu fyrir hverja áætlunarkeyrslu til að fínstilla framboðið sem þarf til að uppfylla eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="008dc-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="008dc-114">Þegar aðaláætlanagerð uppfærir upplýsingar þarfarakningar tekur hún mið af fyrirliggjandi merkingu.</span><span class="sxs-lookup"><span data-stu-id="008dc-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="008dc-115">Þarfarakning hefst með því að taka með viðeigandi merkingar, frátekningar á lager og frátekningar í pöntun, í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="008dc-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="008dc-116">Merking framboðs og eftirspurnar</span><span class="sxs-lookup"><span data-stu-id="008dc-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="008dc-117">Frátekningar í birgðum</span><span class="sxs-lookup"><span data-stu-id="008dc-117">On-hand reservations</span></span>
1. <span data-ttu-id="008dc-118">Frátekningar í pöntun</span><span class="sxs-lookup"><span data-stu-id="008dc-118">On-order reservations</span></span>

<span data-ttu-id="008dc-119">Um leið og áætluð pöntun er staðfest veitir svarglugginn **Staðfesting** svæðið **Uppfæra merki** sem notað er til að stilla valkosti merkisins fyrir pantanirnar sem eru stofnaðar við staðfestingu.</span><span class="sxs-lookup"><span data-stu-id="008dc-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="008dc-120">Veljið eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="008dc-120">Select one of the following values:</span></span>

- <span data-ttu-id="008dc-121">**Nei** – Engar birgðir eru merktar.</span><span class="sxs-lookup"><span data-stu-id="008dc-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="008dc-122">**Staðlað** – Birgðamerking er uppfærð í samræmi við jöfnun.</span><span class="sxs-lookup"><span data-stu-id="008dc-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="008dc-123">Þarfapöntun (þarfir) er merkt gagnvart fullnaðarpöntun (birgðir).</span><span class="sxs-lookup"><span data-stu-id="008dc-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="008dc-124">Þegar eitthvað magn er eftir í fullnaðarpöntuninni er það ekki merkt og tilvísunarupplýsingarnar eru skildar eftir auðar.</span><span class="sxs-lookup"><span data-stu-id="008dc-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="008dc-125">Þegar t.d. pöntun á 100 EA er fest við innkaupapöntun fyrir 150 EA verður tilvísunarupplýsingum aðeins úthlutað á sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="008dc-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="008dc-126">**Útvíkkað** – Bæði þarfapöntun (eftirspurn) og fullnaðarpöntun (framboð) er merkt, burtséð frá því hvort eitthvert magn er eftir í fullnaðarpöntuninni.</span><span class="sxs-lookup"><span data-stu-id="008dc-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="008dc-127">Þegar t.d. pöntun á 100 EA er fest við innkaupapöntun fyrir 150 EA verður tilvísunarupplýsingum bæði úthlutað á sölupöntunina og innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="008dc-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
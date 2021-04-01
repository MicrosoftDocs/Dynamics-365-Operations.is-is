---
title: Gera útgáfu framleiðsluflæðis óvirka
description: Þegar virkrar framleiðsluflæðisútgáfu er ekki lengur þörf er hægt að afvirkja hana.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b062bcab17a708be0cd40f2cc6451707d6993a4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257340"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="83c10-103">Gera útgáfu framleiðsluflæðis óvirka</span><span class="sxs-lookup"><span data-stu-id="83c10-103">Deactivate a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83c10-104">Þegar virkrar framleiðsluflæðisútgáfu er ekki lengur þörf er hægt að afvirkja hana.</span><span class="sxs-lookup"><span data-stu-id="83c10-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="83c10-105">Aðeins ætti að nota þennan valkost ef öllum kanban-reglum og verkþáttum hefur verið lokið og ekki verður gert virkt aftur.</span><span class="sxs-lookup"><span data-stu-id="83c10-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="83c10-106">Athugið að lokadagsetning allra kanban-reglna sem tengjast þessari útgáfu framleiðsluflæðis verður uppfærð með núverandi dagsetningu og tími.</span><span class="sxs-lookup"><span data-stu-id="83c10-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="83c10-107">Til að breyta virkri útgáfu framleiðsluflæðis skaltu íhuga að stilla lokadag fyrir virka útgáfu og búa til nýja útgáfu.</span><span class="sxs-lookup"><span data-stu-id="83c10-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="83c10-108">Þetta leyfir að haldið sé áfram framleiðslaðgerðum við undirbúning á nýrri útgáfu og tengdum kanban-reglum.</span><span class="sxs-lookup"><span data-stu-id="83c10-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="83c10-109">Til að fella virka framleiðsluflæðisútgáfu úr gildi þarf að setja inn lokadag.</span><span class="sxs-lookup"><span data-stu-id="83c10-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="83c10-110">Í þeim skilningi er afvirkjun frekar undantekning en regla.</span><span class="sxs-lookup"><span data-stu-id="83c10-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="83c10-111">Fyrir þetta ferli þarf framleiðsluflæði með útgáfu sem hægt er að gera óvirka.</span><span class="sxs-lookup"><span data-stu-id="83c10-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="83c10-112">Reyndu þetta ekki í framleiðsluumhverfi nema þú sért 100% viss um að útgáfan sé alveg úrelt.</span><span class="sxs-lookup"><span data-stu-id="83c10-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="83c10-113">Gera útgáfu framleiðsluflæðis óvirka</span><span class="sxs-lookup"><span data-stu-id="83c10-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="83c10-114">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="83c10-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="83c10-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="83c10-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="83c10-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="83c10-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="83c10-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="83c10-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="83c10-118">Smellið á Afvirkja.</span><span class="sxs-lookup"><span data-stu-id="83c10-118">Click Deactivate.</span></span>
    * <span data-ttu-id="83c10-119">Ekki halda áfram ef notandi er ekki 100% viss um að þessi útgáfa framleiðsluflæðis sé úrelt.</span><span class="sxs-lookup"><span data-stu-id="83c10-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="83c10-120">Með því að smella á í Lagi renna allar virkar kanban-reglur út og allar aðgerðir framleiðslu og áfyllingar stöðvast tafarlaust af þessari útgáfu framleiðsluflæðis.</span><span class="sxs-lookup"><span data-stu-id="83c10-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="83c10-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83c10-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
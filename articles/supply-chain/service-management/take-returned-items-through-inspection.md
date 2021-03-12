---
title: Setja skilaðar vörur í skoðun
description: Fara með skilavörur í skoðun.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53cb727cc0f001a6ac344d37f25273999f992d8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974086"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="df16c-103">Setja skilaðar vörur í skoðun</span><span class="sxs-lookup"><span data-stu-id="df16c-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="df16c-104">Smelltu á **Birgðastjórnun** \> **Reglubundið** \> **Gæðastjórnun** \> **Biðgeymslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="df16c-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="df16c-105">Finnið pöntunarlínuna sem samsvarar skiluðu vörunni sem er í skoðun.</span><span class="sxs-lookup"><span data-stu-id="df16c-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="df16c-106">Aðeins er hægt að tengja biðgeymslupöntun við eitt vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="df16c-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="df16c-107">Ef 10 vörum með tíu mismunandi vörunúmerum er skilað í einni sendingu og sendar í biðgeymslu eru 10 biðgeymslupantanir stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="df16c-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="df16c-108">Eftir að hafa skoðað vöruna skaltu velja í reitnum **Ráðstöfunarkóði** til að tilgreina hvað ætti að gera við vöruna og hvernig á að meðhöndla tengda fjárhagsfærslu.</span><span class="sxs-lookup"><span data-stu-id="df16c-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="df16c-109">Til dæmis er hægt að skila vörunni í birgðir og endurgreiða viðskiptavininum, henda vörunni og senda skiptivöru til viðskiptavinarins, eða skila vörunni til viðskiptavinarins án inneignar.</span><span class="sxs-lookup"><span data-stu-id="df16c-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="df16c-110">Ef ekki er hægt að úthluta mörgum skilavörum fyrir staka runu vörunúmers sama ráðstöfunarkóðanum verður þú að skipta upp biðgeymslupöntuninni (<STRONG>Aðgerðir</STRONG> &gt; <STRONG>Skipta</STRONG>) til að úthluta hverri undirrunu mismunandi ráðstöfunarkóða.</span><span class="sxs-lookup"><span data-stu-id="df16c-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="df16c-111">Þegar þú hefur lokið við skoðunina skaltu smella á **Bóka sem búið** til að losa skilavörurnar og stofna færslu vörukomubókar.</span><span class="sxs-lookup"><span data-stu-id="df16c-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="df16c-112">Aðilinn eða deildin sem tekur á móti vörunum vinnur með færslubókina fyrir þær vörur sem á að skila í birgðir.</span><span class="sxs-lookup"><span data-stu-id="df16c-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="df16c-113">– eða –</span><span class="sxs-lookup"><span data-stu-id="df16c-113">–or–</span></span>
    
    <span data-ttu-id="df16c-114">Ljúktu við biðgeymslupöntunina og færðu vörurnar beint aftur í birgðir með því að nota eina af aðgerðunum fyrir **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="df16c-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="df16c-115">Skjámyndinni er lokað til að vista breytingar.</span><span class="sxs-lookup"><span data-stu-id="df16c-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="df16c-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="df16c-116">See also</span></span>

[<span data-ttu-id="df16c-117">Tilgreint hvernig losa eigi skilaðar vörur</span><span class="sxs-lookup"><span data-stu-id="df16c-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  



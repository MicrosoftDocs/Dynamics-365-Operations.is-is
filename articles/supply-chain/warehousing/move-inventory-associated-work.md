---
title: "Hreyfing birgða með tengdri vinnu í vöruhúsakerfi"
description: "Í þessu efnisatriði er því lýst hvernig eigi að setja upp og nota staðfestingu einingartiltektar úr fartæki."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2889f04017bdd20be05174146ba88a24cbefacbb
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="f7da9-103">Hreyfing birgða með tengdri vinnu í vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="f7da9-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7da9-104">Með notkun á hreyfingu birgða er hægt að skera úr um hvaða starfsmenn í vöruhúsi megi hreyfa fráteknar birgðir.</span><span class="sxs-lookup"><span data-stu-id="f7da9-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="f7da9-105">Þetta gefur sveigjanleika í stýrðum vöruhúsum, þar sem þú getur ákveðið að heimila ekki starfsmanni að velja nýja tiltektarstaðsetningu fyrir tínsluvinnu sem hefur þegar verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="f7da9-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="f7da9-106">Það gerir vöruhúsastjóra einnig kleift að stýra hvaða heimildir reynsluminni starfsmenn eiga að hafa.</span><span class="sxs-lookup"><span data-stu-id="f7da9-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="f7da9-107">Sveigjanleiki til að stjórna daglegri starfsemi starfsfólks í vöruhúsi getur verið gagnlegur við aðstæður sem þessar:</span><span class="sxs-lookup"><span data-stu-id="f7da9-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="f7da9-108">Aðstæður 1</span><span class="sxs-lookup"><span data-stu-id="f7da9-108">Scenario 1</span></span>
<span data-ttu-id="f7da9-109">Fyrirtæki hefur tiltölulega lítið móttökusvæði og það er yfirfullt af brettum og kössum sem bíða frágangs.</span><span class="sxs-lookup"><span data-stu-id="f7da9-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="f7da9-110">Stór sending er væntanleg síðar sama dag þannig að starfsmaður í móttöku ákveður að hreinsa móttökusvæðið með því að færa sum brettin í biðgeymslu fyrir vörur á innleið.</span><span class="sxs-lookup"><span data-stu-id="f7da9-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="f7da9-111">Aðstæður 2</span><span class="sxs-lookup"><span data-stu-id="f7da9-111">Scenario 2</span></span>
<span data-ttu-id="f7da9-112">Reyndur starfsmaður í vöruhúsi sér tækifæri til að sameina vörurnar á einni staðsetningu í stað þess að dreifa þeim á þrjár nærliggjandi staðsetningar með litlu magni í hverri þeirra.</span><span class="sxs-lookup"><span data-stu-id="f7da9-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="f7da9-113">Starfsmaðurinn vill sameina magnið með því að færa vörurnar úr hverri þessara staðsetninga á sömu staðsetningu og á sömu númeraplötuna.</span><span class="sxs-lookup"><span data-stu-id="f7da9-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="f7da9-114">Aðstæður 3</span><span class="sxs-lookup"><span data-stu-id="f7da9-114">Scenario 3</span></span>
<span data-ttu-id="f7da9-115">Bretti bíður sendingar í biðgeymslu, eins og BIÐ01 sem er nálægt AFGREIÐSLUHURÐ01.</span><span class="sxs-lookup"><span data-stu-id="f7da9-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="f7da9-116">Hins vegar verður breyting, þar sem flutningabíllinn á að koma í AFGREIÐSLUHURÐ04.</span><span class="sxs-lookup"><span data-stu-id="f7da9-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="f7da9-117">Starfsmaður sem sér um sendinguna er meðvitaður um þetta og þarf að sjá til þess að flutningabíllinn þurfi ekki að bíða þess að vera fermdur úr BIÐ01.</span><span class="sxs-lookup"><span data-stu-id="f7da9-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="f7da9-118">Starfsmaðurinn ákveður að færa vörurnar í þeirri sendingu úr BIÐ01 í BIÐ04, sem er nær nýju staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="f7da9-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="f7da9-119">Núverandi takmarkanir</span><span class="sxs-lookup"><span data-stu-id="f7da9-119">Current limitations</span></span>

<span data-ttu-id="f7da9-120">Vinnufrátektir sem þú getur fært takmarkast við Sölupöntun, Útgáfu flutningspöntunar, Innhreyfingu flutningspöntunar, Innkaupapöntun og Áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="f7da9-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="f7da9-121">Hreyfing á vörum takmarkast við að skipta upp vinnulínum.</span><span class="sxs-lookup"><span data-stu-id="f7da9-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="f7da9-122">Þetta þýðir að ef þú ert með vinnulínu fyrir 100 stk. af vöru A úr staðsetningu Sta1, er ekki hægt að færa bara 30 stk. af vöru A þaðan í aðra staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f7da9-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="f7da9-123">Það myndi þýða skiptingu á fyrirliggjandi vinnulínu í 30 og 70, þar sem staðsetningarnar eru nú mismunandi.</span><span class="sxs-lookup"><span data-stu-id="f7da9-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="f7da9-124">Þegar um er að ræða biðgeymsluaðstæður, þar sem númeraplatan sem þú færir vörur frá eða númeraplata sem þú færir vörur á, er stillt á Marknúmeraplötu fyrir verkbeiðni, má aðeins færa alla númeraplötuna þannig að marknúmeraplata sé ekki brotin upp.</span><span class="sxs-lookup"><span data-stu-id="f7da9-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="f7da9-125">Aðeins tilfallandi hreyfing er studd eins og er.</span><span class="sxs-lookup"><span data-stu-id="f7da9-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="f7da9-126">Þetta þýðir að ekki verður hægt að færa fráteknar birgðir með hreyfingu sniðmátsvalmyndaratriða úr fartæki.</span><span class="sxs-lookup"><span data-stu-id="f7da9-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="f7da9-127">Setja heimild til að færa fráteknar birgðir fyrir einstaka starfsmenn</span><span class="sxs-lookup"><span data-stu-id="f7da9-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="f7da9-128">Fyrir starfsmann sem má flytja fráteknar birgðir skal velja gátreitinn **Leyfa hreyfingu birgða með tengdri vinnu** undir **Vöruhúsastjórnun** > **Uppsetning** > **Starfsmaður**.</span><span class="sxs-lookup"><span data-stu-id="f7da9-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="f7da9-129">Bakfært</span><span class="sxs-lookup"><span data-stu-id="f7da9-129">Backported</span></span>

<span data-ttu-id="f7da9-130">Þessi eiginleiki hefur einnig verið bakfærður í Microsoft Dynamics AX 2012 R3 og verður í boði sem hluti af CU12.</span><span class="sxs-lookup"><span data-stu-id="f7da9-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="f7da9-131">Einnig er hægt að hlaða honum niður einum og sér í gegnum KB-númer 3192548.</span><span class="sxs-lookup"><span data-stu-id="f7da9-131">It can also be downloaded individually through KB number 3192548.</span></span> 



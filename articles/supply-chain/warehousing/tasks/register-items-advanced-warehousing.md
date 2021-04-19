---
title: Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók
description: Þetta efnisatriði lýsir aðstæðum sem sýnir hvernig á að skrá vörur með komubók þegar ítarleg felri vöruhúsastjórnunar eru notuð.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830835"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="120bc-103">Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók</span><span class="sxs-lookup"><span data-stu-id="120bc-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="120bc-104">Þetta efnisatriði lýsir aðstæðum sem sýnir hvernig á að skrá vörur með komubók þegar ítarleg felri vöruhúsastjórnunar eru notuð.</span><span class="sxs-lookup"><span data-stu-id="120bc-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="120bc-105">Þetta væri yfirleitt gert með af móttöku starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="120bc-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="120bc-106">Virkja gögn sýnishorna</span><span class="sxs-lookup"><span data-stu-id="120bc-106">Enable sample data</span></span>

<span data-ttu-id="120bc-107">Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind í þessu efnisatriði er nauðsynlegt að nota kerfi þar sem venjuleg sýnigögn eru sett upp og velja þarf lögaðilann *USMF* áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="120bc-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="120bc-108">Hægt er að vinna með þessar astæður með því að skipta gildum úr eigin gögnum ef eftirfarandi gögn eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="120bc-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="120bc-109">Þú þarft að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="120bc-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="120bc-110">Varan á línunni verðu að vera á lager.</span><span class="sxs-lookup"><span data-stu-id="120bc-110">The item on the line must be stocked.</span></span> <span data-ttu-id="120bc-111">Það má ekki nota afurðarafbrigði og má ekki hafa rakningarvíddir.</span><span class="sxs-lookup"><span data-stu-id="120bc-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="120bc-112">Varan verður að vera tengd við geymsluvíddarflokk sem er með virkt vöruhúsakerfisferli.</span><span class="sxs-lookup"><span data-stu-id="120bc-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="120bc-113">Vöruhús sem er notað verður að vera virkt fyrir vöruhúsakerfisferli og staðsetning sem er notað fyrir móttöku verður að vera númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="120bc-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="120bc-114">Stofna haus vörukomubókar sem notar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="120bc-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="120bc-115">Eftirfarandi aðstæður sýna hvernig á að stofna síðuhaus í komubók vöru sem notar vöruhúsakerfi:</span><span class="sxs-lookup"><span data-stu-id="120bc-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="120bc-116">Gangið úr skugga um að kerfið innihaldi staðfesta innkaupapöntun sem uppfyllir kröfurnar sem lýst er í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="120bc-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="120bc-117">Þessi atburðarás notar innkaupapöntun fyrir fyrirtæki *USMF*, lánardrottnalykil *1001*, vöruhús *51* með pöntunarlínu fyrir *10 bretti* af vörunúmeri *M9200*.</span><span class="sxs-lookup"><span data-stu-id="120bc-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="120bc-118">Skráið niður innkaupapöntunarnúmerið sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="120bc-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="120bc-119">Farið í **Birgðastjórnun \> Færslubókarfærslur \> Vörumóttaka \> Vörumóttaka**.</span><span class="sxs-lookup"><span data-stu-id="120bc-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="120bc-120">Veljið **Nýtt** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="120bc-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="120bc-121">Svarglugginn **Stofna færslubók vöruhúsakerfis** opnast.</span><span class="sxs-lookup"><span data-stu-id="120bc-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="120bc-122">Veljið færslubókarheiti í svæðinu **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="120bc-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="120bc-123">Ef *USMF* sýnigögn eru notuð skal velja *WHS*.</span><span class="sxs-lookup"><span data-stu-id="120bc-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="120bc-124">Ef eigin gögn eru notuð verður færslubókin sem er valin að vera með **Athuga tiltektarstaðsetningu** stillt á *Nei* og **Biðgeymslustjórnun** stillt á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="120bc-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="120bc-125">Stillið **Tilvísun** á *Innkaupapöntun*.</span><span class="sxs-lookup"><span data-stu-id="120bc-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="120bc-126">Stillið **Reikningsnúmer** á *1001*.</span><span class="sxs-lookup"><span data-stu-id="120bc-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="120bc-127">Stillið **Númer** á númer innkaupapöntunarinnar sem var tengd fyrir þessa æfingu.</span><span class="sxs-lookup"><span data-stu-id="120bc-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="120bc-128">![Vörukomubók](../media/item-arrival-journal-header.png "Vörukomubók")</span><span class="sxs-lookup"><span data-stu-id="120bc-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="120bc-129">Veldu **Í lagi** til að búa til færslubókarhausinn.</span><span class="sxs-lookup"><span data-stu-id="120bc-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="120bc-130">Í hlutanum **Færslubókarlínur** skal velja **Bæta við línu** og færa inn eftirfarandi gögn:</span><span class="sxs-lookup"><span data-stu-id="120bc-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="120bc-131">**Vörunúmer** – Stillið á *M9200*.</span><span class="sxs-lookup"><span data-stu-id="120bc-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="120bc-132">**Svæðið**, **Vöruhúsið** og **Magnið** verður stillt út frá birgðafærslugögnunum fyrir 10 bretti (1000 ea.).</span><span class="sxs-lookup"><span data-stu-id="120bc-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="120bc-133">**Staðsetning** – stillt á  *001*.</span><span class="sxs-lookup"><span data-stu-id="120bc-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="120bc-134">Þessi tiltekna staðsetning rekur ekki númeraplötur.</span><span class="sxs-lookup"><span data-stu-id="120bc-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="120bc-135">![Lína vörukomubókar](../media/item-arrival-journal-line.png "Lína vörukomubókar")</span><span class="sxs-lookup"><span data-stu-id="120bc-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="120bc-136">Reiturinn **Dagsetning** ákvarðar dagsetninguna sem verður að skrá magn á lager fyrir þessa vöru í birgðum.</span><span class="sxs-lookup"><span data-stu-id="120bc-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="120bc-137">**Lotukenni** er fyllt út af kerfinu ef hægt er að auðkenna það úr uppgefnum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="120bc-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="120bc-138">Annars þarf að slá þetta inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="120bc-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="120bc-139">áskilið svæði skyldusvæði sem tengir þessa skráningu við tiltekna upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="120bc-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="120bc-140">Veljið **Villuleita** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="120bc-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="120bc-141">Þetta athugar hvort færslubókin sé tilbúin til bókunar.</span><span class="sxs-lookup"><span data-stu-id="120bc-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="120bc-142">Ef sannvottun bregst verður að lagfæra villurnar áður en hægt er að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="120bc-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="120bc-143">Svarglugginn **Villuleita færslubók** opnast.</span><span class="sxs-lookup"><span data-stu-id="120bc-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="120bc-144">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="120bc-144">Select **OK**.</span></span>
1. <span data-ttu-id="120bc-145">Skoða skilaboðastiku.</span><span class="sxs-lookup"><span data-stu-id="120bc-145">Review the message bar.</span></span> <span data-ttu-id="120bc-146">Skilaboð ættu að birtast sem segja að aðgerðinni sé lokið.</span><span class="sxs-lookup"><span data-stu-id="120bc-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="120bc-147">Á aðgerðasvæðinu skal velja **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="120bc-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="120bc-148">Svarglugginn **Bóka færslubók** opnast.</span><span class="sxs-lookup"><span data-stu-id="120bc-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="120bc-149">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="120bc-149">Select **OK**.</span></span>
1. <span data-ttu-id="120bc-150">Skoða skilaboðastiku.</span><span class="sxs-lookup"><span data-stu-id="120bc-150">Review the message bar.</span></span> <span data-ttu-id="120bc-151">Skilaboð ættu að birtast um að aðgerðinni sé lokið.</span><span class="sxs-lookup"><span data-stu-id="120bc-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="120bc-152">Veljið **Aðgerðir > Innhreyfingarskjal afurðar** á aðgerðasvæðinu til að uppfæra innkaupapöntunarlínuna og bóka innhreyfingarskjal afurðar.</span><span class="sxs-lookup"><span data-stu-id="120bc-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

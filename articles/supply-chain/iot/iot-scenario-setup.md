---
title: Uppsetning á aðstæðum fyrir IoT gervigreind
description: Þetta efnisatriði lýsir því hvernig skilgreina á aðstæður í Supply Chain Management fyrir IoT-gervigreind.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386526"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="cca7b-103">Uppsetning á aðstæðum fyrir IoT gervigreind</span><span class="sxs-lookup"><span data-stu-id="cca7b-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cca7b-104">Þetta efnisatriði lýsir því hvernig skilgreina á aðstæður í Supply Chain Management fyrir IoT-gervigreind.</span><span class="sxs-lookup"><span data-stu-id="cca7b-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="cca7b-105">Áður en hægt er að setja upp aðstæðurnar þarf að [setja upp LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="cca7b-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="cca7b-106">Í þessu efnisatriði er hægt að skilgreina aðstæðurnar **Niðurtími búnaðar** til að mynda tilkynningu í Supply Chain Management þegar vél verður óvirk.</span><span class="sxs-lookup"><span data-stu-id="cca7b-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="cca7b-107">Skilgreina **Niðurtími búnaðar** aðstæður í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cca7b-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="cca7b-108">**Niðurtími búnaðar** aðstæður varpar merki fyrir hlut út í viðvörunarþröskuldi vélar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="cca7b-109">Aðeins er fylgst með vélum þegar vél er valin fyrir aðstæðurnar og hún er stillt á að keyra í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cca7b-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="cca7b-110">Ef tíminn frá því að vélin síðast tók við merki fyrir hlut út er meiri en viðvörunarþröskuldurinn, þá er **Vél óvirk** tilkynning ræst.</span><span class="sxs-lookup"><span data-stu-id="cca7b-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="cca7b-111">Ef vél er enn í gangi, þegar næsta **hlutur út** merki hefur borist er **Vél virk** tilkynning ræst.</span><span class="sxs-lookup"><span data-stu-id="cca7b-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="cca7b-112">Ef vél er óvirk í 30 mín er ný **Vél óvirk** tilkynning ræst.</span><span class="sxs-lookup"><span data-stu-id="cca7b-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="cca7b-113">**Niðurtími búnaðar** aðstæðurnar hafa þessi tengsl:</span><span class="sxs-lookup"><span data-stu-id="cca7b-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="cca7b-114">Framleiðslupöntun verður að vera í vinnslu á varpaðri vél til að viðvörun sé ræst.</span><span class="sxs-lookup"><span data-stu-id="cca7b-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="cca7b-115">Merki sem stendur fyrir merki varpaðrar vélar fyrir hlut út verður að senda á IoT-miðstöð með einkvæmu heiti eiginleika.</span><span class="sxs-lookup"><span data-stu-id="cca7b-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="cca7b-116">Unix-millisekúndutímastimpill verður að vera til staðar í skilaboðum IoT miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="cca7b-117">Til að skilgreina aðstæðurnar skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="cca7b-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="cca7b-118">Skrá inn á Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cca7b-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="cca7b-119">Virkja eiginleikaflaggið IoT-gervigreind.</span><span class="sxs-lookup"><span data-stu-id="cca7b-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="cca7b-120">Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cca7b-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="cca7b-121">Skilgreinið mælingarnar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-121">Configure the metrics.</span></span> <span data-ttu-id="cca7b-122">Frekari upplýsingar eru í [Hvernig skal skilgreina mælingar](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="cca7b-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="cca7b-123">Farið í **Framleiðslustýring**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="cca7b-124">Farið í **Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="cca7b-125">Smellið á **Grunnstilla** á reitnum **Niðurtími búnaðar**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="cca7b-126">Skilgreiningarforritið byrjar á síðunni **Skilgreining á skema fyrir skynjunarbúnað**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="cca7b-127">Markmiðið hér er að setja upp skema í Supply Chain Management til að samsvara JSON-sniði IoT skilaboða.</span><span class="sxs-lookup"><span data-stu-id="cca7b-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="cca7b-128">Hægt er að skilgreina mörg skilaboðaskema.</span><span class="sxs-lookup"><span data-stu-id="cca7b-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="cca7b-129">Frekari upplýsingar er að finna í [Snið skilaboðaskema fyrir IoT-miðstöð](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="cca7b-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="cca7b-130">Í þessu dæmi er inniheldur innihald skilaboða runu skilaboða með þessu sniði:</span><span class="sxs-lookup"><span data-stu-id="cca7b-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="cca7b-131">Bæta línu við töfluna.</span><span class="sxs-lookup"><span data-stu-id="cca7b-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="cca7b-132">Stillið **Heiti skema** á **Kenni**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="cca7b-133">Stillið **Slóð skema** á **/innihald[\*]/kenni**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="cca7b-134">Stillið **Lýsing** á **Skilaboðakenni**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="cca7b-135">Bæta línu við töfluna.</span><span class="sxs-lookup"><span data-stu-id="cca7b-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="cca7b-136">Stillið **Heiti skema** á **Tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="cca7b-137">Stillið **Slóð skema** á **/innihald[\*]/tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="cca7b-138">Stillið **Lýsing** á **Tímastimpill skilaboða**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="cca7b-139">Bæta línu við töfluna.</span><span class="sxs-lookup"><span data-stu-id="cca7b-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="cca7b-140">Stillið **Heiti skema** á **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="cca7b-141">Stillið **Slóð skema** á **/innihald[\*]/gildi**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="cca7b-142">Stillið **Lýsing** á **Gildi skilaboða**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="cca7b-143">Ekki þarf að skilgreina alla eiginleikana í skilaboðunum, aðeins þær sem þörf er á.</span><span class="sxs-lookup"><span data-stu-id="cca7b-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="cca7b-144">Í þessu dæmi var ekki stofnuð lína fyrir **Tímastimpill rótar**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="cca7b-145">Slóðin fyrir **Tímastimpill rótar** væri **/tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="cca7b-146">Smellið á **Áfram** til að fara á síðuna **Skemavörpun á skynjunarbúnaði**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="cca7b-147">Í línu fyrir **Tilfangakenni búnaðar** skal stilla **Heiti skema** á **Kenni**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="cca7b-148">Gild gildi eru birt í fellitöflu.</span><span class="sxs-lookup"><span data-stu-id="cca7b-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="cca7b-149">Í línunni fyrir **UTC-tími** skal stilla **Heiti skema** á **Tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="cca7b-150">Gild gildi eru birt í fellitöflu.</span><span class="sxs-lookup"><span data-stu-id="cca7b-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="cca7b-151">Í línunni fyrir **Framleiðslumerki hlutar** skal stilla **Heiti skema** á **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="cca7b-152">Gild gildi eru birt í fellitöflu.</span><span class="sxs-lookup"><span data-stu-id="cca7b-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="cca7b-153">Smellið á **Áfram** fyrir síðuna **Grunnstilling tilfangakennis búnaðar**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="cca7b-154">Í þessu skrefi er skeytagildunum á IoT-miðstöð varpað í tilföng Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cca7b-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="cca7b-155">Í töflunni **Gagnagildi merkis** skal bæta við nýrri línu og færa inn **IoTInt.Machine1225.PartOut** í dálknum **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="cca7b-156">Gildið **IoTInt.Machine1225.PartOut** kemur frá eiginleikanum JSON **kenni** í skilaboðum IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="cca7b-157">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-157">Click **Save**.</span></span>
    3. <span data-ttu-id="cca7b-158">Í töflunni **Vörpun viðskiptafærslu** er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="cca7b-159">Sjálfgildi fyrir **Gerð viðskiptafærslu** er útfyllt sjálfkrafa, og óþarfi er að breyta því.</span><span class="sxs-lookup"><span data-stu-id="cca7b-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="cca7b-160">Í dálkinum **Viðskiptafærsla** skal velja aðfangakeðjustjórnun tilfanga vélar sem þetta merkisgildi er sent frá.</span><span class="sxs-lookup"><span data-stu-id="cca7b-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="cca7b-161">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-161">Click **Save**.</span></span>
    6. <span data-ttu-id="cca7b-162">Endurtekið þessi skref og bætið við nýrri viðskiptafærsluvörpun fyrir **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="cca7b-163">Hægt er að varpa mörgum gagnagildum merkis í eina færslu í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cca7b-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="cca7b-164">Notaðu dálkinn **Valið** til að velja hvaða vélar á að vinna með.</span><span class="sxs-lookup"><span data-stu-id="cca7b-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="cca7b-165">Ekki þarf að skilgreina öll merkigildi og ekki þarf að velja allar vélar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="cca7b-166">Smellið á **Áfram** til að fara á síðuna **Grunnstilling framleiðslumerkis hlutar**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="cca7b-167">Í töflunni **Gagnagildi merkis** skal bæta við línu og stilla **Gildi** á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="cca7b-168">Gildið **Satt** kemur frá eiginleikanum JSON **gildi** í skilaboðum IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="cca7b-169">Hægt er að bæta við eins mörgum gildum og nauðsynlegt er fyrir aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="cca7b-170">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-170">Click **Save**.</span></span>
20. <span data-ttu-id="cca7b-171">Smellið á **Áfram** til að opna síðuna **Niðurtímaþröskuldur búnaðar**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="cca7b-172">Vélarnar sem taldar eru upp eru vélarnar sem áður hafa verið varpað á merki gilda.</span><span class="sxs-lookup"><span data-stu-id="cca7b-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="cca7b-173">Í þessu skrefi er þröskuldur skilgreindur til að ákvarða hvort vél er óvirk.</span><span class="sxs-lookup"><span data-stu-id="cca7b-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="cca7b-174">Til dæmis ef þröskuldur er stilltur á 10 skal Supply Chain Management mynda tilkynningu ef engin skilaboð um hlut út frá vél hafa verið send í 10 mínútur.</span><span class="sxs-lookup"><span data-stu-id="cca7b-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="cca7b-175">Smellið á **Áfram** til að fara á síðuna **Virkja aðstæður**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="cca7b-176">Víxlið sleðanum til að virkja aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="cca7b-177">Smellt er á **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-177">Click **Finish**.</span></span>

<span data-ttu-id="cca7b-178">Uppsetningu aðstæðnanna er lokið.</span><span class="sxs-lookup"><span data-stu-id="cca7b-178">The scenario setup is complete.</span></span> <span data-ttu-id="cca7b-179">IoT gervigreind ræsir sjálfkrafa vinnslu á skilaboðum IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="cca7b-180">Skilgreina **Gæði afurðar** aðstæður í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cca7b-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="cca7b-181">**Gæði afurðar** aðstæður myndar tilkynningu ef eigind vöru er utan tiltekins sviðs.</span><span class="sxs-lookup"><span data-stu-id="cca7b-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="cca7b-182">Til dæmis gæti skynjari sent þyngd hverrar vöru í IoT-miðstöð.</span><span class="sxs-lookup"><span data-stu-id="cca7b-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="cca7b-183">Í Supply Chain Management væri mynduð tilkynning ef varan væri of þung eða of létt.</span><span class="sxs-lookup"><span data-stu-id="cca7b-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="cca7b-184">Aðstæðurnar eru með þessi tengsl:</span><span class="sxs-lookup"><span data-stu-id="cca7b-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="cca7b-185">Framleiðslupöntun verður að vera í keyrslu á varpaðri vél og framleiða afurð með varpaðri runueigind til að viðvörun verður ræst.</span><span class="sxs-lookup"><span data-stu-id="cca7b-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="cca7b-186">Merki sem stendur fyrir runueigind verður að senda á IoT-miðstöð með einkvæmu heiti eiginleika.</span><span class="sxs-lookup"><span data-stu-id="cca7b-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="cca7b-187">Unix-millisekúndutímastimpill verður að vera til staðar í skilaboðum IoT miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="cca7b-188">Skilgreina **Framleiðslutafir** aðstæður í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cca7b-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="cca7b-189">**Framleiðslutafir** aðstæður myndar tilkynningu ef gegnumstreymi framleiðslu fellur undir þröskuldsgildi.</span><span class="sxs-lookup"><span data-stu-id="cca7b-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="cca7b-190">Í þessum aðstæðum er **Hlutur út** merki sent í IoT miðstöð fyrir hverja vöru sem er framleidd.</span><span class="sxs-lookup"><span data-stu-id="cca7b-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="cca7b-191">Í Supply Chain Management er pöntunarfrestur reiknaður út frá því hversu lengi framleiðslupöntunin á að keyra, hversu margar vörur á að framleiða, hversu lengi vinnslan hefur verið í gangi og hversu mörg **Hlutur út** merki eru móttekin.</span><span class="sxs-lookup"><span data-stu-id="cca7b-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="cca7b-192">Tilkynning um tafir yrði mynduð ef númerið á **Hlutur út** merki fyrir vinnsluna fellur undir þröskuldsgildi væntanlegs gildis.</span><span class="sxs-lookup"><span data-stu-id="cca7b-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="cca7b-193">Aðstæðurnar eru með þessi tengsl:</span><span class="sxs-lookup"><span data-stu-id="cca7b-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="cca7b-194">Framleiðslupöntun verður að vera í vinnslu á varpaðri vél til að viðvörun sé ræst.</span><span class="sxs-lookup"><span data-stu-id="cca7b-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="cca7b-195">Merki sem stendur fyrir merki varpaðrar vélar fyrir hlut út verður að senda á IoT-miðstöð með einkvæmu heiti eiginleika.</span><span class="sxs-lookup"><span data-stu-id="cca7b-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="cca7b-196">Unix-millisekúndutímastimpill verður að vera til staðar í skilaboðum IoT miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="cca7b-197">Hvernig á að gera aðstæður óvirkar</span><span class="sxs-lookup"><span data-stu-id="cca7b-197">How to disable a scenario</span></span>

<span data-ttu-id="cca7b-198">Til að gera aðstæður óvirkar skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="cca7b-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="cca7b-199">Í Supply Chain Management er farið í **Framleiðslustýring \> Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.</span><span class="sxs-lookup"><span data-stu-id="cca7b-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="cca7b-200">Smellið á **Grunnstilla** á aðstæðunum.</span><span class="sxs-lookup"><span data-stu-id="cca7b-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="cca7b-201">Smellið á **Áfram** til að komast á flipann fyrir síðustu leiðsögn.</span><span class="sxs-lookup"><span data-stu-id="cca7b-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="cca7b-202">Víxlið sleðanum til að gera aðstæðurnar óvirkar.</span><span class="sxs-lookup"><span data-stu-id="cca7b-202">Toggle the slider to disable the scenario.</span></span>

---
title: Uppsetning á aðstæðum fyrir IoT gervigreind
description: Þetta efnisatriði útskýrir hvernig á að skilgreina atburðarásir fyrir IoT-gervigreind í Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1deaa2130b63272da39a42315c6a1bc4b7ccb8a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430583"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="3e07e-103">Uppsetning á aðstæðum fyrir IoT gervigreind</span><span class="sxs-lookup"><span data-stu-id="3e07e-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e07e-104">Þetta efnisatriði útskýrir hvernig á að skilgreina atburðarásir fyrir IoT-gervigreind í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e07e-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3e07e-105">Áður en þú getur sett upp atburðarásirnar verður þú að [setja upp Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="3e07e-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="3e07e-106">Í þessu efnisatriði er hægt að skilgreina aðstæðurnar **Niðurtími búnaðar** þannig að tilkynning er búin til í Supply Chain Management þegar vél verður óvirk.</span><span class="sxs-lookup"><span data-stu-id="3e07e-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="3e07e-107">Í efnisatriðinu er einnig sýnt hvernig á að skilgreina aðstæðurnar **Gæði afurðar** þannig að tilkynning er búin til ef eigind vöru er utan tiltekins sviðs og hvernig á að skilgreina aðstæðurnar **Tafir á framleiðslu** þannig að tilkynning er búin til ef gegnumstreymi framleiðslunnar fellur undir þröskuldsgildi.</span><span class="sxs-lookup"><span data-stu-id="3e07e-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="3e07e-108">Skilgreina Niðurtími búnaðar aðstæður í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3e07e-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="3e07e-109">Aðstæðurnar **Niðurtími búnaðar** varpa **PartOut** merki til viðvörunarþröskulds vélar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="3e07e-110">Aðeins er fylgst með vélinni þegar hún er valin fyrir aðstæðurnar og hún er stillt á **Keyrslu** í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e07e-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="3e07e-111">Ef tíminn frá því að **PartOut** merki sem síðast var móttekið frá vélinni fer yfir viðvörunarþröskuldinn kviknar á tilkynningunni **Vél niðri**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="3e07e-112">Ef vél er enn í gangi kviknar á **Vél virk** tilkynningu þegar næsta **PartOut** merki er móttekið.</span><span class="sxs-lookup"><span data-stu-id="3e07e-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="3e07e-113">Ef vél er óvirk í 30 mínútur ræsist ný tilkynning um **Vél niðri**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="3e07e-114">**Niðurtími búnaðar** aðstæðurnar hafa eftirfarandi tengsl:</span><span class="sxs-lookup"><span data-stu-id="3e07e-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="3e07e-115">Aðeins er hægt að virkja viðvörun ef framleiðslupöntun er keyrð á varpaðri vél.</span><span class="sxs-lookup"><span data-stu-id="3e07e-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="3e07e-116">Merki sem stendur fyrir **PartOut** merki merktrar vélar, verður að vera send til IoT-miðstöðvarinnar og einkvæmt heiti eiginleika verður að vera innifalið.</span><span class="sxs-lookup"><span data-stu-id="3e07e-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="3e07e-117">UNIX **tímastimpils** eiginleiki, þar sem gildin eru sýnd í millisekúndum (ms), verður að vera til staðar í skilaboði Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3e07e-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="3e07e-118">Til að skilgreina aðstæðurnar skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3e07e-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="3e07e-119">Skráðu þig inn í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e07e-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="3e07e-120">Virkja eiginleikaflaggið IoT-gervigreind.</span><span class="sxs-lookup"><span data-stu-id="3e07e-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="3e07e-121">Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="3e07e-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="3e07e-122">Skilgreinið mælingarnar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-122">Configure the metrics.</span></span> <span data-ttu-id="3e07e-123">Frekari upplýsingar eru í [Hvernig skal skilgreina mælingar](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="3e07e-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="3e07e-124">Farðu í **Framleiðslustýring \> Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="3e07e-125">Í reitnum **Niðurtími búnaðar** skal velja **Skilgreina** til að opna leiðsagnarforrit skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="3e07e-126">Fyrsta síða í leiðsagnarforritinu er síðan **Skilgreining á skema fyrir skynjunarbúnað**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="3e07e-127">Á þessari síðu er markmið þitt að setja upp skema í Supply Chain Management þannig að það passi við JavaScript Object Notation-snið (JSON) í skilaboðum IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3e07e-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="3e07e-128">Hægt er að skilgreina mörg skilaboðaskema.</span><span class="sxs-lookup"><span data-stu-id="3e07e-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="3e07e-129">Frekari upplýsingar er að finna í [Snið skemu fyrir skilaboð IoT Hub](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="3e07e-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="3e07e-130">Í þessu dæmi felur innihald skilaboðanna í sér runu af skilaboðum sem eru á eftirfarandi sniði.</span><span class="sxs-lookup"><span data-stu-id="3e07e-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="3e07e-131">Bætið línu við töfluna og stillið eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="3e07e-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="3e07e-132">Stillið reitinn **Heiti skema** á **Kenni**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="3e07e-133">Stillið reitinn **Slóð skema** á **/innihald\[\*\]/kenni**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="3e07e-134">Stillið reitinn **Lýsing** á **Skilaboðakenni**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="3e07e-135">Bæta annarri línu við töfluna og stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="3e07e-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="3e07e-136">Stillið reitinn **Heiti skema** á **Tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="3e07e-137">Stillið **Slóð skema** á **/innihald\[\*\]/tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="3e07e-138">Stillið reitinn **Lýsing** á **Tímastimpill skilaboða**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="3e07e-139">Bæta annarri línu við töfluna og stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="3e07e-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="3e07e-140">Stillið reitinn **Heiti skema** á **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="3e07e-141">Stillið reitinn **Slóð skema** á **/innihald\[\*\]/gildi**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="3e07e-142">Stillið reitinn **Lýsing** á **Gildi skilaboða**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e07e-143">Ekki þarf að skilgreina alla eiginleikana í skilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="3e07e-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="3e07e-144">Skilgreina aðeins eiginleikana sem eru nauðsynlegir.</span><span class="sxs-lookup"><span data-stu-id="3e07e-144">Define only the properties that you require.</span></span> <span data-ttu-id="3e07e-145">Í skrefunum á undan var ekki stofnuð lína fyrir **Tímastimpil rótar**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="3e07e-146">Slóðin fyrir **Tímastimpil rótar** væri **/tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="3e07e-147">Veljið **Áfram** til að fara á síðuna **Skemavörpun á skynjunarbúnaði**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="3e07e-148">Í línunni fyrir **Tilfangakenni búnaðar**, í reitnum **Heiti skema**, skal velja **Kenni**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="3e07e-149">Í línunni fyrir **UTC-tími**, í reitnum **Heiti skema**, skal velja **Tímastimpill**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="3e07e-150">Í línunni fyrir **Framleiðslumerki hlutar** skal stilla **Heiti skema** á **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="3e07e-151">Veljið **Næst** til að fara á síðuna **Skilgreining á tilfangakenni búnaðar**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="3e07e-152">Fylgið eftirfarandi skrefum til að varpa gildunum úr skilaboðum IoT Hub yfir í tilföng Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="3e07e-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="3e07e-153">Í töflunni **Gagnagildi merkis** skal bæta við nýrri línu.</span><span class="sxs-lookup"><span data-stu-id="3e07e-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="3e07e-154">Í reitinn **Gildi** skal færa inn **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="3e07e-155">Þetta gildi kemur frá JSON-eiginleikanum **kenni** í skilaboðum IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="3e07e-156">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-156">Select **Save**.</span></span>
    3. <span data-ttu-id="3e07e-157">Í töflunni **Vörpun viðskiptafærslu** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="3e07e-158">Sjálfgefið gildi fyrir **Gerð viðskiptafærslu** er sjálfkrafa fyllt út og ekki þarf að breyta því.</span><span class="sxs-lookup"><span data-stu-id="3e07e-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="3e07e-159">Í dálkinum **Viðskiptafærsla** skal velja tilfang vélar Supply Chain Management sem þetta merkjagildi er sent frá.</span><span class="sxs-lookup"><span data-stu-id="3e07e-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="3e07e-160">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-160">Select **Save**.</span></span>
    6. <span data-ttu-id="3e07e-161">Endurtekið þessi skref til að bæta við nýrri viðskiptafærsluvörpun fyrir **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="3e07e-162">Hægt er að varpa mörgum gagnagildum merkis í eina færslu í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e07e-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="3e07e-163">Notið dálkinn **Valið** til að velja hvaða vélar á að vinna með.</span><span class="sxs-lookup"><span data-stu-id="3e07e-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="3e07e-164">Ekki þarf að skilgreina öll merkjagildi og ekki þarf að velja allar vélar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="3e07e-165">Veljið **Áfram** til að fara á síðuna **Grunnstilling framleiðslumerkis hlutar**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="3e07e-166">Í töflunni **Gagnagildi merkis** skal bæta við línu og stilla reitinn **Gildi** á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="3e07e-167">Þetta gildi kemur frá JSON-eiginleikanum **gildi** í skilaboðum IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="3e07e-168">Hægt er að bæta við eins mörgum gildum og nauðsynlegt er fyrir aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="3e07e-169">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-169">Select **Save**.</span></span>
20. <span data-ttu-id="3e07e-170">Veljið **Áfram** til að opna síðuna **Niðurtímaþröskuldur búnaðar**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="3e07e-171">Vélarnar sem taldar eru upp eru vélarnar sem var varpað áður á merkjagildi.</span><span class="sxs-lookup"><span data-stu-id="3e07e-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="3e07e-172">Á þessari síðu eru mörk skilgreind til að ákvarða hvort vél er niðri.</span><span class="sxs-lookup"><span data-stu-id="3e07e-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="3e07e-173">Til dæmis ef þröskuldur er stilltur á **10** býr Supply Chain Management til tilkynningu ef ekkert **PartOut** merki er móttekið frá vél í 10 mínútur.</span><span class="sxs-lookup"><span data-stu-id="3e07e-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="3e07e-174">Veljið **Áfram** til að fara á síðuna **Virkja aðstæður**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="3e07e-175">Stillið valkostinn til að virkja aðsmengitæðurnar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="3e07e-176">Veljið **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-176">Select **Finish**.</span></span>

<span data-ttu-id="3e07e-177">Uppsetning aðstæðna er nú lokið.</span><span class="sxs-lookup"><span data-stu-id="3e07e-177">The scenario setup is now completed.</span></span> <span data-ttu-id="3e07e-178">IoT-gervigreind hefst sjálfkrafa handa við að vinna úr skilaboðum IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3e07e-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="3e07e-179">Skilgreina Gæði afurðar aðstæður í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3e07e-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="3e07e-180">**Gæði afurðar** aðstæður myndar tilkynningu ef eigind vöru er utan tiltekins sviðs.</span><span class="sxs-lookup"><span data-stu-id="3e07e-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="3e07e-181">Til dæmis sendir skynjari þyngd hverrar vöru til IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="3e07e-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="3e07e-182">Ef vara er of þung eða of létt er tilkynning búin til í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e07e-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="3e07e-183">Aðstæðurnar **Gæði afurðar** eru háðar eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="3e07e-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="3e07e-184">Viðvörun getur aðeins verið ræst ef framleiðslupöntun er keyrð á varpaðri vél og framleiðir afurð sem er með varpaða runueigind.</span><span class="sxs-lookup"><span data-stu-id="3e07e-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="3e07e-185">Merki sem stendur fyrir runueigindina verður að vera send til IoT-miðstöðvar og einkvæmt heiti eiginleika verður að fylgja.</span><span class="sxs-lookup"><span data-stu-id="3e07e-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="3e07e-186">UNIX **tímastimpils** eiginleiki, þar sem gildið er sýnt í millisekúndum, verður að vera til staðar í skilaboði Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3e07e-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="3e07e-187">Skilgreina Framleiðslutafir aðstæður í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3e07e-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="3e07e-188">**Framleiðslutafir** aðstæður myndar tilkynningu ef gegnumstreymi framleiðslu fellur undir þröskuldsgildi.</span><span class="sxs-lookup"><span data-stu-id="3e07e-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="3e07e-189">Í þessum aðstæðum er **PartOut** merki sent til IoT-miðstöðvar fyrir hverja vöru sem er framleidd.</span><span class="sxs-lookup"><span data-stu-id="3e07e-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="3e07e-190">Í Supply Chain Management eru framleiðslutafir reiknaðar út frá tímanum sem áætlað er að framleiðslupöntunin taki, fjölda vara sem á að framleiða, tímanum sem vinnslan hefur verið í gangi og fjölda **PartOut** merkja sem eru móttekin.</span><span class="sxs-lookup"><span data-stu-id="3e07e-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="3e07e-191">Tilkynning um tafir er mynduð ef númerið á **PartOut** merkjum fyrir vinnsluna fellur undir þröskuldsgildi væntanlegs gildis.</span><span class="sxs-lookup"><span data-stu-id="3e07e-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="3e07e-192">Aðstæðurnar **Tafir á framleiðslu** eru háðar eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="3e07e-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="3e07e-193">Aðeins er hægt að virkja viðvörun ef framleiðslupöntun er keyrð á varpaðri vél.</span><span class="sxs-lookup"><span data-stu-id="3e07e-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="3e07e-194">Merki sem stendur fyrir **PartOut** merki merktrar vélar, verður að vera send til Azure IoT-miðstöðvarinnar og einkvæmt heiti eiginleika verður að vera innifalið.</span><span class="sxs-lookup"><span data-stu-id="3e07e-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="3e07e-195">UNIX **tímastimpils** eiginleiki, þar sem gildið er sýnt í millisekúndum, verður að vera til staðar í skilaboði Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3e07e-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="3e07e-196">Gera aðstæður óvirkar</span><span class="sxs-lookup"><span data-stu-id="3e07e-196">Disable a scenario</span></span>

<span data-ttu-id="3e07e-197">Til að gera aðstæður óvirkar skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3e07e-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="3e07e-198">Í Supply Chain Management er farið í **Framleiðslustýring \> Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="3e07e-199">Á svæðinu fyrir aðstæðurnar skal velja **Skilgreina**.</span><span class="sxs-lookup"><span data-stu-id="3e07e-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="3e07e-200">Veljið **Næst** til að fara á síðustu leiðsagnarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="3e07e-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="3e07e-201">Stillið valkostinn til að slökkva á aðstæðunum.</span><span class="sxs-lookup"><span data-stu-id="3e07e-201">Set the option to disable the scenario.</span></span>

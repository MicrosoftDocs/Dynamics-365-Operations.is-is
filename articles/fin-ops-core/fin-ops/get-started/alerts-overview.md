---
title: Yfirlit yfir viðvaranir
description: Þetta efnisatriði gefur almennar upplýsingar um viðvaranir. Þú getur notað viðvaranir til að fylgjast með atburðum sem þú vilt rekja meðan á vinnudegi stendur.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 191f8a5d788f57964e7870167109e98cbde65c43
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694165"
---
# <a name="alerts-overview"></a><span data-ttu-id="7f6f3-104">Yfirlit yfir viðvaranir</span><span class="sxs-lookup"><span data-stu-id="7f6f3-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="7f6f3-105">Um viðvaranir</span><span class="sxs-lookup"><span data-stu-id="7f6f3-105">About alerts</span></span>
<span data-ttu-id="7f6f3-106">Viðvaranir skapa tilkynningarkerfi fyrir mikilvæga atburði í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="7f6f3-107">Þú getur notað viðvaranir til að fylgjast með atburðum sem þú vilt rekja meðan á vinnudegi stendur.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="7f6f3-108">Þú getur auðveldlega búið til þitt eigið sett af viðvörunarreglum þannig að þú fáir viðvaranir um afhendingar sem er komnar fram yfir á tíma, pantanir sem eru eyddar, verð sem breytast eða aðra atburði sem þú verður að bregðast við.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="7f6f3-109">Í áætlunar- og bókhaldskerfi (ERP) eru nokkrar dæmigerðar aðstæður þar sem hægt er að nota viðvörunareiginleikann.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="7f6f3-110">Hér eru nokkur dæmi.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="7f6f3-111">Dæmi 1: Búðu til viðvörunarreglu fyrir nýjar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="7f6f3-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="7f6f3-112">Opnaðu síðuna **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="7f6f3-113">Á aðgerðasvæðinu, á flipanum **Valkostir** í flokknum **Deila** skal velja **Búa til sérsniðna viðvörun**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="7f6f3-114">Í svarglugganum **Búa til viðvörunarreglu**, á flýtiflipanum **Láta mig vita þegar**, í reitnum **Atvik** skal velja **Færsla hefur verið búin til**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="7f6f3-115">Dæmi 2: Búðu til viðvörunarreglu um frestun á afhendingardegi</span><span class="sxs-lookup"><span data-stu-id="7f6f3-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="7f6f3-116">Opnaðu síðuna **Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="7f6f3-117">Veldu kenni innkaupapöntunar til að fá aðgang að upplýsingum um innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="7f6f3-118">Stækkaðu flýtiflipann **Haus innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="7f6f3-119">Á aðgerðasvæðinu, á flipanum **Valkostir** í flokknum **Deila** skal velja **Búa til sérsniðna viðvörun**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="7f6f3-120">Í svarglugganum **Búa til viðvörunarreglu**, á flýtiflipanum **Láta mig vita þegar**, í reitnum **Reitur** skal velja **Afhendingardagur**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="7f6f3-121">Í reitnum **Atvik** skal velja **hefur verið frestað**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="7f6f3-122">Eftir að þú hefur lokað svarglugganum **Búa til viðvörunarreglu** birtist reglan þín á síðunni **Stjórna viðvörunarreglum**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="7f6f3-123">Þú getur notað síðuna **Stjórna viðvörunarreglum** til að uppfæra núverandi viðvörunarreglur.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="7f6f3-124">Til dæmis getur þú breytt atburðakveikjum, uppfært tilkynningar um viðburði og uppfært lokadagsetningar.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="7f6f3-125">Til að opna síðuna **Stjórna viðvörunarreglum** skal nota hnappinn **Láta mig vita þegar** á flipanum **Valkostir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="7f6f3-126">Hvað gerist þegar viðvörunarregla er búin til?</span><span class="sxs-lookup"><span data-stu-id="7f6f3-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="7f6f3-127">Þegar þú býrð til viðvörunarreglur getur þú tengt fyrirframskilgreint atvik við tiltekinn reit.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="7f6f3-128">Til dæmis þegar kemur að dagsetningunni sem tilgreind er í reitnum eða innihald reitsins breytist.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="7f6f3-129">Að öðrum kosti er hægt að tengja atvik við færslurnar á tiltekinni síðu.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="7f6f3-130">Til dæmis þegar færsla er búin til eða færslu er eytt.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="7f6f3-131">Þegar valið atvik á sér stað fyrir reitinn eða fyrir færslu á síðunni er viðvörun send á þig.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="7f6f3-132">Til dæmis, getur þú búið til reglu sem þú tengir reitinn **Afhendingardagur** á tiltekinni innkaupapöntunarlínu við atvikið **var komið á tíma fyrir þetta löngum tíma síðan**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="7f6f3-133">Þú stillir tímarammann í fimm daga.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-133">You set the time frame to five days.</span></span> <span data-ttu-id="7f6f3-134">Í þessu tilviki er viðvörun send fimm dögum eftir afhendingardag á þessari innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="7f6f3-135">Að auki geturðu þrengt viðvörunarreglur með því að setja skilyrði.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="7f6f3-136">Til dæmis getur þú fengið viðvörun um nýjar innkaupapantanir sem eru búnar til fyrir tiltekna lánardrottnalykla.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="7f6f3-137">Undirbúningur fyrir viðvörun</span><span class="sxs-lookup"><span data-stu-id="7f6f3-137">Preparing for an alert</span></span>

<span data-ttu-id="7f6f3-138">Áður en þú setur upp viðvörunarreglu skaltu ákveða hvenær eða í hvaða aðstæðum þú vilt fá viðvaranir.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="7f6f3-139">Þegar þú veist hvaða atvik þú vilt fá tilkynningu um skaltu finna síðuna með gögnunum sem eru þess valdandi að atvikið birtist.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="7f6f3-140">Atvikið getur verið dagsetning sem kemur eða tilteknar breytingar sem eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="7f6f3-141">Þess vegna verður þú að finna síðuna þar sem dagsetningin er tilgreind eða hvar reiturinn er sem breytist eða hvar nýja færslan birtist sem er búin til.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="7f6f3-142">Eftir að þú hefur þessar upplýsingar er hægt að búa til viðvörunarregluna.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="7f6f3-143">Hlutar viðvörunarreglu</span><span class="sxs-lookup"><span data-stu-id="7f6f3-143">Components of an alert rule</span></span>

<span data-ttu-id="7f6f3-144">Viðvörunarregla hefur fimm hluta:</span><span class="sxs-lookup"><span data-stu-id="7f6f3-144">An alert rule has five components:</span></span>

- <span data-ttu-id="7f6f3-145">**Atvik** - Atvikið sem kveikir á viðvörunarregla getur verið dagsetning sem kemur eða tiltekin breyting sem á sér stað.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="7f6f3-146">Þú skilgreinir atburði á flýtiflipanum **Senda viðvörun í tölvupósti vegna breytinga á stöðu vinnslu** í svarglugganum **Búa til viðvörunarreglu**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="7f6f3-147">**Skilyrði** - Á flýtiflipanum **Láta mig vita um** í svarglugganum **Búa til viðvörunarreglu** er hægt að velja umfang skilyrðisins til að stjórna því hvenær þú færð viðvörun um atvik.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="7f6f3-148">Þú getur notað regluna annaðhvort aðeins á gildandi færslu eða öllum sýnilegum færslum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="7f6f3-149">Ef reglan gildir þvert yfir lögaðila, getur þú stillt valkostinn **Fyrirtækið í heild sinni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="7f6f3-150">**Fyrning á reglu** - Á flýtiflipanum **Láta mig vita þangað til** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hversu lengi viðvörunarreglan á að vera virk.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="7f6f3-151">**Efni** - Á flýtiflipanum **Láta mig vita með** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina efnistexta og textaskilaboð sem viðvörunarskilaboðin eiga að nota.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="7f6f3-152">**Notandi** - Á flýtiflipanum **Láta hvern vita** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hvaða notandi á að taka á móti viðvörunarskilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="7f6f3-153">Að sjálfgefnu er notandakenni þitt valið.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f6f3-154">Þessi valkostur er takmarkaður við stjórnendur fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-154">This option is restricted to organization administrators.</span></span>

## <a name="videos"></a><span data-ttu-id="7f6f3-155">Myndskeið</span><span class="sxs-lookup"><span data-stu-id="7f6f3-155">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="7f6f3-156">Hvernig á að nota viðvaranir til að fylgjast með síuðum gögnum</span><span class="sxs-lookup"><span data-stu-id="7f6f3-156">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="7f6f3-157">Myndskeiðið [Hvernig á að nota viðvaranir til að fylgjast með síuðum gögnum](https://youtu.be/ZYKMcv6kl9s) (sýnt hér að ofan) er innifalið í [Finance and Operations spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er að finna á YouTube.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-157">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="7f6f3-158">Valkostir viðvaranareglu</span><span class="sxs-lookup"><span data-stu-id="7f6f3-158">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="7f6f3-159">Myndskeiðið [Valkostir viðvaranareglu](https://youtu.be/cpzimwOjicM) (sýnt hér að ofan) er innifalið í [Finance and Operations spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er að finna á YouTube.</span><span class="sxs-lookup"><span data-stu-id="7f6f3-159">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>



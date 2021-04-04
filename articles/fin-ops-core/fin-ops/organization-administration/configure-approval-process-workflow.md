---
title: Grunnstilla samþykktarferli í verkflæði
description: Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.
author: ChrisGarty
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37a079ee98495a27c1462df32f2973b012069ca8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562814"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="ae9fa-103">Grunnstilla samþykktarferli í verkflæði</span><span class="sxs-lookup"><span data-stu-id="ae9fa-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae9fa-104">Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="ae9fa-105">Til að skilgreina samþykktarferli í verkflæðisritlinum, er hægrismellt á samþykktareiningu og smellið síðan á **Eiginleika** til að opna skjámyndina **Eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="ae9fa-106">Gefa samþykktarferlinu heiti</span><span class="sxs-lookup"><span data-stu-id="ae9fa-106">Name the approval process</span></span>

<span data-ttu-id="ae9fa-107">Fylgið eftirfarandi skrefum til að gefa samþykktarferlinu heiti.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="ae9fa-108">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ae9fa-109">Í reitinn **Heiti** er slegið inn einkvæmt heiti fyrir samþykktarferlið.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="ae9fa-110">Tilgreindu hvenær kerfið bregst sjálfkrafa við vegna skjals</span><span class="sxs-lookup"><span data-stu-id="ae9fa-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="ae9fa-111">Hægt er að skilgreina kerfið þannig það vinni sjálfkrafa að skjölum sem standast ákveðin skilyrði.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="ae9fa-112">Til dæmis, getur kerfið samþykkja kostnaðarskýrslur sem hafa heildarupphæðir sem eru lægri en 100 USD.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="ae9fa-113">Fylgið eftirfarandi skrefum til að tilgreina hvenær kerfið grípur til aðgerða vegna skjals.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="ae9fa-114">Í vinstri glugganum, smelltu á **sjálfvirkar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="ae9fa-115">Útvíkkið gátreitur **virkja sjálfvirkar aðgerðir** .</span><span class="sxs-lookup"><span data-stu-id="ae9fa-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="ae9fa-116">Smelltu á **Bæta við Aðgerð**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="ae9fa-117">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-117">Enter a condition.</span></span>
5. <span data-ttu-id="ae9fa-118">Færa inn viðbótarskilyrði ef þess gerist þörf:</span><span class="sxs-lookup"><span data-stu-id="ae9fa-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="ae9fa-119">Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal ljúka eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="ae9fa-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="ae9fa-120">Smellið á **Prófun** til að opna **Kanna verkflæðisskilyrði** skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="ae9fa-121">Veljið færslu í svæðinu **Villuleita skilyrði** á skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="ae9fa-122">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-122">Click **Test**.</span></span> <span data-ttu-id="ae9fa-123">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="ae9fa-124">Smelltu á **Í lagi** eða **Hætta við** til að fara aftur síðuna **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="ae9fa-125">Í listanum **ljúka aðgerð sjálfvirkt** skal velja aðgerðina sem kerfið á að grípa til vegna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="ae9fa-126">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="ae9fa-126">Specify when notifications are sent</span></span>

<span data-ttu-id="ae9fa-127">Hægt er að senda tilkynningar til fólks þegar skjal hefur verið samþykkt, hafnað, framselja eða stigmagnað, eða þegar beðið hefur verið um breytingu.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="ae9fa-128">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="ae9fa-129">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="ae9fa-130">Veldu gátreitinn sem er við hliðina á tilvikunum sem á að senda tilkynningar vegna.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="ae9fa-131">**Úthluta** – Úthluta skjalinu til annars notanda til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="ae9fa-132">**Hækka** – Þegar úthlutaður notandi hefur ekki bregðast á skjal í tíminn.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="ae9fa-133">**Samþykkja** – Þegar skjal hefur verið samþykkt.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="ae9fa-134">**Hafna** – Þegar skjali hefur verið hafnað.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="ae9fa-135">**Biðja um breytingu** – úthlutaður notandi hefur beðið um breytingu á skjalinu sem var sent.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="ae9fa-136">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="ae9fa-137">Smellið á flipann **Tilkynningartexti**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="ae9fa-138">Færið inn tilkynningartextann í textareitinn.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="ae9fa-139">Hægt er að sérsníða textann með því að færa inn staðgengla sem skipt verður út fyrir viðeigandi gagna þegar þau birtast notendum.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="ae9fa-140">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="ae9fa-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="ae9fa-141">Smella skal á textareit þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ae9fa-142">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="ae9fa-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ae9fa-143">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ae9fa-144">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-144">Click **Insert**.</span></span>

7. <span data-ttu-id="ae9fa-145">Til að bæta þýðingum á tilkynningunni við skal smella á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="ae9fa-146">Í skjámyndinni sem birtist, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="ae9fa-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="ae9fa-147">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-147">Click **Add**.</span></span>
    2. <span data-ttu-id="ae9fa-148">Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="ae9fa-149">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="ae9fa-150">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="ae9fa-151">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-151">Click **Close**.</span></span>

8. <span data-ttu-id="ae9fa-152">Smellið á flipann **viðtakandi**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="ae9fa-153">Tilgreinið til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="ae9fa-154">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 10.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ae9fa-155">Valkostur</span><span class="sxs-lookup"><span data-stu-id="ae9fa-155">Option</span></span></th>
    <th><span data-ttu-id="ae9fa-156">Viðtakendur tilkynninga.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="ae9fa-157">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="ae9fa-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ae9fa-158"><strong>Þátttakendur</strong></span><span class="sxs-lookup"><span data-stu-id="ae9fa-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="ae9fa-159">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="ae9fa-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ae9fa-160">Eftir að <strong>Þáttakandi</strong> er valin, smellið á <strong>byggt á hlutverki</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="ae9fa-161">Í listanum <strong>gerð Þátttakanda</strong> skal velja gerð hóps eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="ae9fa-162">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ae9fa-163"><strong>Verkflæðisnotandi</strong></span><span class="sxs-lookup"><span data-stu-id="ae9fa-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="ae9fa-164">Notendur sem taka þátt í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="ae9fa-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ae9fa-165">Eftir að þú velur <strong>Notanda verkflæðis</strong>, skal smellið á <strong>Notanda verkflæðis</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="ae9fa-166">Í <strong>verkflæðisnotandi</strong> skal velja notandann sem tekur þátt í verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ae9fa-167"><strong>Notandi</strong></span><span class="sxs-lookup"><span data-stu-id="ae9fa-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="ae9fa-168">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="ae9fa-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ae9fa-169">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ae9fa-170">Veldu notendur til að senda tilkynningar til og færðu síðan þessa notendur í listann <strong>Valdir notendur</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="ae9fa-171">Endurtakið skref 3 til 9 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="ae9fa-172">Tilgreina hver endanlegur samþykkjandi er</span><span class="sxs-lookup"><span data-stu-id="ae9fa-172">Specify a final approver</span></span>

<span data-ttu-id="ae9fa-173">Þú getur tilnefnt endanlegt samþykki fyrir atburðarás þar sem samþykki er sá sem sendi skjalið til samþykktar og „banna samþykki sendanda“ er notað.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="ae9fa-174">Fylgið eftirfarandi skrefum til að tilgreina endanlegan samþykkjanda.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="ae9fa-175">Í verkflæðisritlinum er hægrismellt á samþykktareiningu og síðan valið **Eiginleikar** til að opna skjámyndina **Eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="ae9fa-176">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="ae9fa-177">Veljið gátreitinn **Nota endanlegs samþykkjanda**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="ae9fa-178">Veljið notanda, sem verður endanlegi samþykkjandinn, af listanum.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="ae9fa-179">Setja upp tímamörk</span><span class="sxs-lookup"><span data-stu-id="ae9fa-179">Set a time limit</span></span>

<span data-ttu-id="ae9fa-180">Fylgið eftirfarandi skrefum ef verður að ljúka samþykktarferlinu innan tiltekins tíma.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="ae9fa-181">Valkostirnir sem valdir í þessum skrefum munu hnekkja valkostunum sem valdir eru á flipunum **Verkefni** og **Hækkun** í hverju samþykktarskrefi.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="ae9fa-182">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="ae9fa-183">Beldu **Stilla tímamörk** **verkflæðiseiningar** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="ae9fa-184">Í reitnum **tímalengd** tilgreinið þegar samþykktarferli á að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="ae9fa-185">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="ae9fa-185">Select one of the following options:</span></span>

    - <span data-ttu-id="ae9fa-186">**Klukkustundir** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="ae9fa-187">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ae9fa-188">**Dagar** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="ae9fa-189">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ae9fa-190">**Vikur** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="ae9fa-191">**Mánuðir** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="ae9fa-192">Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ae9fa-193">**Ár** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="ae9fa-194">Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="ae9fa-195">Ef farið er yfir tímamörkin mun kerfið grípa til aðgerða vegna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="ae9fa-196">Veljið aðgerðina, sem kerfið á að framkvæma, í listanum **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="ae9fa-197">Tilgreina hvaða aðgerðir verða tiltækar notandanum.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="ae9fa-198">Þegar notandi fær skjal úthlutað til samþykktar verður hann að vinna í skjalinu.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="ae9fa-199">Fylgið eftirfarandi skrefum til að tilgreina hvaða aðgerðir notandi getur gripið til vegna skjalsins sem lagt var fyrir.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="ae9fa-200">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="ae9fa-201">Veljið gátreitinn **Samþykkja** ef notendur eiga að geta samþykkt skjöl.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="ae9fa-202">Veljið gátreitinn **hafna** ef notendur eiga að geta hafnað skjöl.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="ae9fa-203">Veljið gátreitinn **Breytingabeiðni** ef notendur eiga að geta beðið um breytingar á skjölum.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="ae9fa-204">Veljið gátreitinn **framselja** ef notandinn á að geta framselt skjalinu til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="ae9fa-205">Gátreiturinn **Heimila aðgerðir úr verkefnalistanum í Enterprise Portal** er úreltur.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="ae9fa-206">Skilgreining samþykktarskrefs</span><span class="sxs-lookup"><span data-stu-id="ae9fa-206">Configure the approval steps</span></span>

<span data-ttu-id="ae9fa-207">Samþykktarferli samanstendur af samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="ae9fa-208">Ljúktu við eftirfarandi ferli til að bæta skrefum samþykktarferlið og skilgreina skrefum.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="ae9fa-209">Tvísmellið samþykktarferlið í ritill verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="ae9fa-210">Verkflæðisritlinum birtir skref í samþykktarferlinu.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="ae9fa-211">Til að bæta við samþykktarskrefi, draga skrefið í **verkflæðiseiningar** á vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="ae9fa-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="ae9fa-212">Til að skilgreina samþykktarskref, sjá [Skilgreina samþykktarskref í verkflæði](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="ae9fa-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Grunnstilla samþykktarferli í verkflæði
description: Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09d09464eae932bf9caf4f2ea38cbbb3b4f0162
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190213"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="4aac0-103">Grunnstilla samþykktarferli í verkflæði</span><span class="sxs-lookup"><span data-stu-id="4aac0-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aac0-104">Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="4aac0-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="4aac0-105">Til að skilgreina samþykktarferli í verkflæðisritlinum, er hægrismellt á samþykktareiningu og smellið síðan á **Eiginleika** til að opna skjámyndina **Eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="4aac0-106">Gefa samþykktarferlinu heiti</span><span class="sxs-lookup"><span data-stu-id="4aac0-106">Name the approval process</span></span>

<span data-ttu-id="4aac0-107">Fylgið eftirfarandi skrefum til að gefa samþykktarferlinu heiti.</span><span class="sxs-lookup"><span data-stu-id="4aac0-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="4aac0-108">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="4aac0-109">Í reitinn **Heiti** er slegið inn einkvæmt heiti fyrir samþykktarferlið.</span><span class="sxs-lookup"><span data-stu-id="4aac0-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="4aac0-110">Tilgreindu hvenær kerfið bregst sjálfkrafa við vegna skjals</span><span class="sxs-lookup"><span data-stu-id="4aac0-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="4aac0-111">Hægt er að skilgreina kerfið þannig það vinni sjálfkrafa að skjölum sem standast ákveðin skilyrði.</span><span class="sxs-lookup"><span data-stu-id="4aac0-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="4aac0-112">Til dæmis, getur kerfið samþykkja kostnaðarskýrslur sem hafa heildarupphæðir sem eru lægri en 100 USD.</span><span class="sxs-lookup"><span data-stu-id="4aac0-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="4aac0-113">Fylgið eftirfarandi skrefum til að tilgreina hvenær kerfið grípur til aðgerða vegna skjals.</span><span class="sxs-lookup"><span data-stu-id="4aac0-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="4aac0-114">Í vinstri glugganum, smelltu á **sjálfvirkar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="4aac0-115">Útvíkkið gátreitur **virkja sjálfvirkar aðgerðir** .</span><span class="sxs-lookup"><span data-stu-id="4aac0-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="4aac0-116">Smelltu á **Bæta við Aðgerð**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="4aac0-117">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="4aac0-117">Enter a condition.</span></span>
5. <span data-ttu-id="4aac0-118">Færa inn viðbótarskilyrði ef þess gerist þörf:</span><span class="sxs-lookup"><span data-stu-id="4aac0-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="4aac0-119">Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal ljúka eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="4aac0-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="4aac0-120">Smellið á **Prófun** til að opna **Kanna verkflæðisskilyrði** skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="4aac0-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="4aac0-121">Veljið færslu í svæðinu **Villuleita skilyrði** á skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="4aac0-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="4aac0-122">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-122">Click **Test**.</span></span> <span data-ttu-id="4aac0-123">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.</span><span class="sxs-lookup"><span data-stu-id="4aac0-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="4aac0-124">Smelltu á **Í lagi** eða **Hætta við** til að fara aftur síðuna **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="4aac0-125">Í listanum **ljúka aðgerð sjálfvirkt** skal velja aðgerðina sem kerfið á að grípa til vegna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="4aac0-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="4aac0-126">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="4aac0-126">Specify when notifications are sent</span></span>

<span data-ttu-id="4aac0-127">Hægt er að senda tilkynningar til fólks þegar skjal hefur verið samþykkt, hafnað, framselja eða stigmagnað, eða þegar beðið hefur verið um breytingu.</span><span class="sxs-lookup"><span data-stu-id="4aac0-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="4aac0-128">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="4aac0-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="4aac0-129">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="4aac0-130">Veldu gátreitinn sem er við hliðina á tilvikunum sem á að senda tilkynningar vegna.</span><span class="sxs-lookup"><span data-stu-id="4aac0-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="4aac0-131">**Úthluta** – Úthluta skjalinu til annars notanda til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="4aac0-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="4aac0-132">**Hækka** – Þegar úthlutaður notandi hefur ekki bregðast á skjal í tíminn.</span><span class="sxs-lookup"><span data-stu-id="4aac0-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="4aac0-133">**Samþykkja** – Þegar skjal hefur verið samþykkt.</span><span class="sxs-lookup"><span data-stu-id="4aac0-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="4aac0-134">**Hafna** – Þegar skjali hefur verið hafnað.</span><span class="sxs-lookup"><span data-stu-id="4aac0-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="4aac0-135">**Biðja um breytingu** – úthlutaður notandi hefur beðið um breytingu á skjalinu sem var sent.</span><span class="sxs-lookup"><span data-stu-id="4aac0-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="4aac0-136">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="4aac0-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="4aac0-137">Smellið á flipann **Tilkynningartexti**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="4aac0-138">Færið inn tilkynningartextann í textareitinn.</span><span class="sxs-lookup"><span data-stu-id="4aac0-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="4aac0-139">Hægt er að sérsníða textann með því að færa inn staðgengla sem skipt verður út fyrir viðeigandi gagna þegar þau birtast notendum.</span><span class="sxs-lookup"><span data-stu-id="4aac0-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="4aac0-140">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="4aac0-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="4aac0-141">Smella skal á textareit þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="4aac0-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="4aac0-142">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="4aac0-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="4aac0-143">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="4aac0-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="4aac0-144">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-144">Click **Insert**.</span></span>

7. <span data-ttu-id="4aac0-145">Til að bæta þýðingum á tilkynningunni við skal smella á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="4aac0-146">Í skjámyndinni sem birtist, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="4aac0-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="4aac0-147">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-147">Click **Add**.</span></span>
    2. <span data-ttu-id="4aac0-148">Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="4aac0-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="4aac0-149">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="4aac0-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="4aac0-150">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="4aac0-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="4aac0-151">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-151">Click **Close**.</span></span>

8. <span data-ttu-id="4aac0-152">Smellið á flipann **viðtakandi**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="4aac0-153">Tilgreinið til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="4aac0-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="4aac0-154">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 10.</span><span class="sxs-lookup"><span data-stu-id="4aac0-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="4aac0-155">Valkostur</span><span class="sxs-lookup"><span data-stu-id="4aac0-155">Option</span></span></th>
    <th><span data-ttu-id="4aac0-156">Viðtakendur tilkynninga.</span><span class="sxs-lookup"><span data-stu-id="4aac0-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="4aac0-157">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="4aac0-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="4aac0-158"><strong>Þátttakendur</strong></span><span class="sxs-lookup"><span data-stu-id="4aac0-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="4aac0-159">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="4aac0-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4aac0-160">Eftir að <strong>Þáttakandi</strong> er valin, smellið á <strong>byggt á hlutverki</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="4aac0-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="4aac0-161">Í listanum <strong>gerð Þátttakanda</strong> skal velja gerð hóps eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="4aac0-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="4aac0-162">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="4aac0-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="4aac0-163"><strong>Verkflæðisnotandi</strong></span><span class="sxs-lookup"><span data-stu-id="4aac0-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="4aac0-164">Notendur sem taka þátt í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="4aac0-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4aac0-165">Eftir að þú velur <strong>Notanda verkflæðis</strong>, skal smellið á <strong>Notanda verkflæðis</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="4aac0-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="4aac0-166">Í <strong>verkflæðisnotandi</strong> skal velja notandann sem tekur þátt í verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="4aac0-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="4aac0-167"><strong>Notandi</strong></span><span class="sxs-lookup"><span data-stu-id="4aac0-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="4aac0-168">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="4aac0-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4aac0-169">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="4aac0-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="4aac0-170">Veldu notendur til að senda tilkynningar til og færðu síðan þessa notendur í listann <strong>Valdir notendur</strong>.</span><span class="sxs-lookup"><span data-stu-id="4aac0-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="4aac0-171">Endurtakið skref 3 til 9 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="4aac0-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="4aac0-172">Tilgreina hver endanlegur samþykkjandi er</span><span class="sxs-lookup"><span data-stu-id="4aac0-172">Specify a final approver</span></span>

<span data-ttu-id="4aac0-173">Gott gæti verið að tilnefna endanlegur samþykkjandi fyrir aðstæður þar sem samþykkjandi er sá sem sendi skjalið til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="4aac0-173">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="4aac0-174">Fylgið eftirfarandi skrefum til að tilgreina endanlegan samþykkjanda.</span><span class="sxs-lookup"><span data-stu-id="4aac0-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="4aac0-175">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-175">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="4aac0-176">Veljið gátreitinn **Nota endanlegs samþykkjanda**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-176">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="4aac0-177">Veljið notandann, sem verður endanlegi samþykkjandinn, af listanum.</span><span class="sxs-lookup"><span data-stu-id="4aac0-177">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="4aac0-178">Setja upp tímamörk</span><span class="sxs-lookup"><span data-stu-id="4aac0-178">Set a time limit</span></span>

<span data-ttu-id="4aac0-179">Fylgið eftirfarandi skrefum ef verður að ljúka samþykktarferlinu innan tiltekins tíma.</span><span class="sxs-lookup"><span data-stu-id="4aac0-179">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="4aac0-180">Valkostirnir sem valdir í þessum skrefum munu hnekkja valkostunum sem valdir eru á flipunum **Verkefni** og **Hækkun** í hverju samþykktarskrefi.</span><span class="sxs-lookup"><span data-stu-id="4aac0-180">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="4aac0-181">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-181">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="4aac0-182">Beldu **Stilla tímamörk** **verkflæðiseiningar** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="4aac0-182">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="4aac0-183">Í reitnum **tímalengd** tilgreinið þegar samþykktarferli á að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="4aac0-183">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="4aac0-184">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="4aac0-184">Select one of the following options:</span></span>

    - <span data-ttu-id="4aac0-185">**Klukkustundir** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="4aac0-185">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="4aac0-186">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4aac0-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="4aac0-187">**Dagar** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="4aac0-187">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="4aac0-188">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4aac0-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="4aac0-189">**Vikur** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="4aac0-189">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="4aac0-190">**Mánuðir** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir.</span><span class="sxs-lookup"><span data-stu-id="4aac0-190">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="4aac0-191">Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="4aac0-191">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="4aac0-192">**Ár** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir.</span><span class="sxs-lookup"><span data-stu-id="4aac0-192">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="4aac0-193">Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="4aac0-193">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="4aac0-194">Ef farið er yfir tímamörkin mun kerfið grípa til aðgerða vegna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="4aac0-194">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="4aac0-195">Veljið aðgerðina, sem kerfið á að framkvæma, í listanum **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-195">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="4aac0-196">Tilgreina hvaða aðgerðir verða tiltækar notandanum.</span><span class="sxs-lookup"><span data-stu-id="4aac0-196">Specify which actions are available to the user</span></span>

<span data-ttu-id="4aac0-197">Þegar notandi fær skjal úthlutað til samþykktar verður hann að vinna í skjalinu.</span><span class="sxs-lookup"><span data-stu-id="4aac0-197">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="4aac0-198">Fylgið eftirfarandi skrefum til að tilgreina hvaða aðgerðir notandi getur gripið til vegna skjalsins sem lagt var fyrir.</span><span class="sxs-lookup"><span data-stu-id="4aac0-198">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="4aac0-199">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="4aac0-199">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="4aac0-200">Veljið gátreitinn **Samþykkja** ef notendur eiga að geta samþykkt skjöl.</span><span class="sxs-lookup"><span data-stu-id="4aac0-200">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="4aac0-201">Veljið gátreitinn **hafna** ef notendur eiga að geta hafnað skjöl.</span><span class="sxs-lookup"><span data-stu-id="4aac0-201">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="4aac0-202">Veljið gátreitinn **Breytingabeiðni** ef notendur eiga að geta beðið um breytingar á skjölum.</span><span class="sxs-lookup"><span data-stu-id="4aac0-202">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="4aac0-203">Veljið gátreitinn **framselja** ef notandinn á að geta framselt skjalinu til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="4aac0-203">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="4aac0-204">Gátreiturinn **Heimila aðgerðir úr verkefnalistanum í Enterprise Portal** er úreltur.</span><span class="sxs-lookup"><span data-stu-id="4aac0-204">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="4aac0-205">Skilgreining samþykktarskrefs</span><span class="sxs-lookup"><span data-stu-id="4aac0-205">Configure the approval steps</span></span>

<span data-ttu-id="4aac0-206">Samþykktarferli samanstendur af samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="4aac0-206">An approval process consists of approval steps.</span></span> <span data-ttu-id="4aac0-207">Ljúktu við eftirfarandi ferli til að bæta skrefum samþykktarferlið og skilgreina skrefum.</span><span class="sxs-lookup"><span data-stu-id="4aac0-207">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="4aac0-208">Tvísmellið samþykktarferlið í ritill verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="4aac0-208">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="4aac0-209">Verkflæðisritlinum birtir skref í samþykktarferlinu.</span><span class="sxs-lookup"><span data-stu-id="4aac0-209">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="4aac0-210">Til að bæta við samþykktarskrefi, draga skrefið í **verkflæðiseiningar** á vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="4aac0-210">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="4aac0-211">Til að skilgreina samþykktarskref, sjá [Skilgreina samþykktarskref](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="4aac0-211">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>
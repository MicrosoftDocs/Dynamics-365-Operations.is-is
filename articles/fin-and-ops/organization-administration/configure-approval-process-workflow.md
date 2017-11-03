---
title: "Skilgreining samþykktarferlis í verkflæði"
description: "Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf3523b2768b197b3c75b9a8490f621eced91a7a
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-approval-process-in-a-workflow"></a><span data-ttu-id="aa2d7-103">Skilgreining samþykktarferlis í verkflæði</span><span class="sxs-lookup"><span data-stu-id="aa2d7-103">Configure an approval process in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="aa2d7-104">Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="aa2d7-105">Til að skilgreina samþykktarferli í verkflæðisritlinum, er hægrismellt á samþykktareiningu og smellið síðan á **Eiginleika** til að opna skjámyndina **Eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="aa2d7-106">Gefa samþykktarferlinu heiti</span><span class="sxs-lookup"><span data-stu-id="aa2d7-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="aa2d7-107">Fylgið eftirfarandi skrefum til að gefa samþykktarferlinu heiti.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="aa2d7-108">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="aa2d7-109">Í reitinn **Heiti** er slegið inn einkvæmt heiti fyrir samþykktarferlið.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="aa2d7-110">Tilgreindu hvenær kerfið bregst sjálfkrafa við vegna skjals</span><span class="sxs-lookup"><span data-stu-id="aa2d7-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="aa2d7-111">Hægt er að skilgreina kerfið þannig það vinni sjálfkrafa að skjölum sem standast ákveðin skilyrði.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="aa2d7-112">Til dæmis, getur kerfið samþykkja kostnaðarskýrslur sem hafa heildarupphæðir sem eru lægri en 100 USD.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="aa2d7-113">Fylgið eftirfarandi skrefum til að tilgreina hvenær kerfið grípur til aðgerða vegna skjals.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="aa2d7-114">Í vinstri glugganum, smelltu á **sjálfvirkar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="aa2d7-115">Útvíkkið gátreitur **virkja sjálfvirkar aðgerðir** .</span><span class="sxs-lookup"><span data-stu-id="aa2d7-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="aa2d7-116">Smelltu á **Bæta við Aðgerð**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="aa2d7-117">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-117">Enter a condition.</span></span>
5.  <span data-ttu-id="aa2d7-118">Færa inn viðbótarskilyrði ef þess gerist þörf:</span><span class="sxs-lookup"><span data-stu-id="aa2d7-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="aa2d7-119">Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal ljúka eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="aa2d7-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="aa2d7-120">Smellið á **Prófun** til að opna **Kanna verkflæðisskilyrði** skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="aa2d7-121">Veljið færslu í svæðinu **Villuleita skilyrði** á skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="aa2d7-122">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-122">Click **Test**.</span></span> <span data-ttu-id="aa2d7-123">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="aa2d7-124">Smelltu á **Í lagi** eða **Hætta við** til að fara aftur síðuna **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="aa2d7-125">Í listanum **ljúka aðgerð sjálfvirkt** skal velja aðgerðina sem kerfið á að grípa til vegna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="aa2d7-126">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="aa2d7-126">Specify when notifications are sent</span></span>
<span data-ttu-id="aa2d7-127">Hægt er að senda tilkynningar til fólks þegar skjal hefur verið samþykkt, hafnað, framselja eða stigmagnað, eða þegar beðið hefur verið um breytingu.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="aa2d7-128">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="aa2d7-129">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="aa2d7-130">Veldu gátreitinn sem er við hliðina á tilvikunum sem á að senda tilkynningar vegna.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="aa2d7-131">**Úthluta** – Úthluta skjalinu til annars notanda til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="aa2d7-132">**Hækka** – Þegar úthlutaður notandi hefur ekki bregðast á skjal í tíminn.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="aa2d7-133">**Samþykkja** – Þegar skjal hefur verið samþykkt.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="aa2d7-134">**Hafna** – Þegar skjali hefur verið hafnað.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="aa2d7-135">**Biðja um breytingu** – úthlutaður notandi hefur beðið um breytingu á skjalinu sem var sent.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="aa2d7-136">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="aa2d7-137">Smellið á flipann **Tilkynningartexti**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="aa2d7-138">Færið inn tilkynningartextann í textareitinn.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="aa2d7-139">Hægt er að sérsníða textann með því að færa inn staðgengla sem skipt verður út fyrir viðeigandi gagna þegar þau birtast notendum.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="aa2d7-140">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="aa2d7-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="aa2d7-141">Smella skal á textareit þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="aa2d7-142">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="aa2d7-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="aa2d7-143">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="aa2d7-144">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="aa2d7-145">Til að bæta þýðingum á tilkynningunni við skal smella á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="aa2d7-146">Í skjámyndinni sem birtist, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="aa2d7-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="aa2d7-147">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="aa2d7-148">Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="aa2d7-149">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="aa2d7-150">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="aa2d7-151">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-151">Click **Close**.</span></span>

8.  <span data-ttu-id="aa2d7-152">Smellið á flipann **viðtakandi**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="aa2d7-153">Tilgreinið til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="aa2d7-154">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 10.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="aa2d7-155">Valkostur</span><span class="sxs-lookup"><span data-stu-id="aa2d7-155">Option</span></span></th>
    <th><span data-ttu-id="aa2d7-156">Viðtakendur tilkynninga.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="aa2d7-157">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="aa2d7-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="aa2d7-158"><strong>Þátttakendur</strong></span><span class="sxs-lookup"><span data-stu-id="aa2d7-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="aa2d7-159">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="aa2d7-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="aa2d7-160">Eftir að <strong>Þáttakandi</strong> er valin, smellið á <strong>byggt á hlutverki</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="aa2d7-161">Í listanum <strong>gerð Þátttakanda</strong> skal velja gerð hóps eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="aa2d7-162">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="aa2d7-163"><strong>Verkflæðisnotandi</strong></span><span class="sxs-lookup"><span data-stu-id="aa2d7-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="aa2d7-164">Notendur sem taka þátt í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="aa2d7-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="aa2d7-165">Eftir að þú velur <strong>Notanda verkflæðis</strong>, skal smellið á <strong>Notanda verkflæðis</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="aa2d7-166">Í <strong>verkflæðisnotandi</strong> skal velja notandann sem tekur þátt í verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="aa2d7-167"><strong>Notandi</strong></span><span class="sxs-lookup"><span data-stu-id="aa2d7-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="aa2d7-168">Sértækir notendur Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="aa2d7-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="aa2d7-169">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="aa2d7-170">Listinn <strong>Tiltækir notendur</strong>: inniheldur alla notendur í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="aa2d7-171">Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong>: lista.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="aa2d7-172">Endurtakið skref 3 til 9 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="aa2d7-173">Tilgreina hver endanlegur samþykkjandi er</span><span class="sxs-lookup"><span data-stu-id="aa2d7-173">Specify a final approver</span></span>
<span data-ttu-id="aa2d7-174">Gott gæti verið að tilnefna endanlegur samþykkjandi fyrir aðstæður þar sem samþykkjandi er sá sem sendi skjalið til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="aa2d7-175">Fylgið eftirfarandi skrefum til að tilgreina endanlegan samþykkjanda.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="aa2d7-176">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="aa2d7-177">Veljið gátreitinn **Nota endanlegs samþykkjanda**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="aa2d7-178">Veljið notandann, sem verður endanlegi samþykkjandinn, af listanum.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="aa2d7-179">Setja upp tímamörk</span><span class="sxs-lookup"><span data-stu-id="aa2d7-179">Set a time limit</span></span>
<span data-ttu-id="aa2d7-180">Fylgið eftirfarandi skrefum ef verður að ljúka samþykktarferlinu innan tiltekins tíma.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-180">Follow these steps if the approval process must be completed in a specific time.</span></span>
| <span data-ttu-id="aa2d7-181">**Ábending**</span><span class="sxs-lookup"><span data-stu-id="aa2d7-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2d7-182">Valkostirnir sem valdir í þessum skrefum munu hnekkja valkostunum sem valdir eru á flipunum **Verkefni** og **Hækkun** í hverju samþykktarskrefi.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="aa2d7-183">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="aa2d7-184">Beldu **Stilla tímamörk** **verkflæðiseiningar** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="aa2d7-185">Í reitnum **tímalengd** tilgreinið þegar samþykktarferli á að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="aa2d7-186">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="aa2d7-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="aa2d7-187">**Klukkustundir** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="aa2d7-188">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="aa2d7-189">**Dagar** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="aa2d7-190">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="aa2d7-191">**Vikur** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="aa2d7-192">**Mánuðir** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="aa2d7-193">Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="aa2d7-194">**Ár** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="aa2d7-195">Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="aa2d7-196">Ef farið er yfir tímamörkin mun kerfið grípa til aðgerða vegna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="aa2d7-197">Veljið aðgerðina, sem kerfið á að framkvæma, í listanum **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="aa2d7-198">Tilgreina hvaða aðgerðir verða tiltækar notandanum.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="aa2d7-199">Þegar notandi fær skjal úthlutað til samþykktar verður hann að vinna í skjalinu.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="aa2d7-200">Fylgið eftirfarandi skrefum til að tilgreina hvaða aðgerðir notandi getur gripið til vegna skjalsins sem lagt var fyrir.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="aa2d7-201">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="aa2d7-202">Veljið gátreitinn **Samþykkja** ef notendur eiga að geta samþykkt skjöl.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="aa2d7-203">Veljið gátreitinn **hafna** ef notendur eiga að geta hafnað skjöl.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="aa2d7-204">Veljið gátreitinn **Breytingabeiðni** ef notendur eiga að geta beðið um breytingar á skjölum.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="aa2d7-205">Veljið gátreitinn **framselja** ef notandinn á að geta framselt skjalinu til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="aa2d7-206">**Athugasemd**: **Heimila aðgerðir úr verklistanum í Enterprise Portal** gátreitur er úreltur.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="aa2d7-207">Skilgreining samþykktarskrefs</span><span class="sxs-lookup"><span data-stu-id="aa2d7-207">Configure the approval steps</span></span>
<span data-ttu-id="aa2d7-208">Samþykktarferli samanstendur af samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="aa2d7-209">Ljúktu við eftirfarandi ferli til að bæta skrefum samþykktarferlið og skilgreina skrefum.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="aa2d7-210">Tvísmellið samþykktarferlið í ritill verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="aa2d7-211">Verkflæðisritlinum birtir skref í samþykktarferlinu.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="aa2d7-212">Til að bæta við samþykktarskrefi, draga skrefið í **verkflæðiseiningar** á vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="aa2d7-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="aa2d7-213">Til að skilgreina samþykktarskref, sjá [Skilgreina samþykktarskref](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="aa2d7-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>







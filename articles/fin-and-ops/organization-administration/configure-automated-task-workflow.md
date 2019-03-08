---
title: Skilgreina sjálfvirk verk í verkflæði
description: Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika sjálfvirks verks.
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
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a9f37228beedafa085987668d5c89b06c6c9d61
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "365110"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="5dbfc-103">Skilgreina sjálfvirk verk í verkflæði</span><span class="sxs-lookup"><span data-stu-id="5dbfc-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dbfc-104">Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika sjálfvirks verks.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="5dbfc-105">Til að skilgreina sjálfvirkt verk í verkflæðisritlinum, er hægrismellt á samþykktarskrefið og smellið síðan á **Eiginleika** til að opna í **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="5dbfc-106">Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir sjálfvirkt verk.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="5dbfc-107">Gefa verkinu heiti</span><span class="sxs-lookup"><span data-stu-id="5dbfc-107">Name the task</span></span>

<span data-ttu-id="5dbfc-108">Fylgið þessum skrefum til að færa inn heiti á sjálfvirkt verk.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="5dbfc-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5dbfc-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="5dbfc-111">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="5dbfc-111">Specify when notifications are sent</span></span>

<span data-ttu-id="5dbfc-112">Hægt er að senda tilkynningar til fólks þegar sjálfvirkt verk hefur verið keyrt eða hætt við.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="5dbfc-113">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers þær eru sendar.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="5dbfc-114">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="5dbfc-115">Veldu gátreitinn sem er við hliðina á tilvikunum sem á að senda tilkynningar vegna.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="5dbfc-116">**Framkvæmd** – Tilkynningar eru sendar þegar verkið hefur verið keyrð.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="5dbfc-117">**Hætt við** – Tilkynningar eru sendar þegar verkið hefur verið hætt við.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="5dbfc-118">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="5dbfc-119">Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="5dbfc-120">Hægt er að sérsníða tilkynningu með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="5dbfc-121">Staðgenglar eru settir í stað viðeigandi gagna þegar tilkynning birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="5dbfc-122">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="5dbfc-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5dbfc-123">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5dbfc-124">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="5dbfc-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5dbfc-125">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5dbfc-126">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-126">Click **Insert**.</span></span>

6. <span data-ttu-id="5dbfc-127">Til að bæta þýðingum við Tilkynningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="5dbfc-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="5dbfc-128">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="5dbfc-129">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5dbfc-130">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5dbfc-131">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5dbfc-132">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 5.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="5dbfc-133">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-133">Click **Close**.</span></span>

7. <span data-ttu-id="5dbfc-134">Á **Viðtakanda** flipanum, tilgreinið hverjum tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="5dbfc-135">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 8.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5dbfc-136">Valkostur</span><span class="sxs-lookup"><span data-stu-id="5dbfc-136">Option</span></span></th>
    <th><span data-ttu-id="5dbfc-137">Viðtakendur tilkynninga.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="5dbfc-138">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="5dbfc-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5dbfc-139">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="5dbfc-139">Participant</span></span></td>
    <td><span data-ttu-id="5dbfc-140">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="5dbfc-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5dbfc-141">Eftor að þú velur <strong>viðtakanda</strong>, Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="5dbfc-142">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5dbfc-143">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="5dbfc-143">Workflow user</span></span></td>
    <td><span data-ttu-id="5dbfc-144">Notendur sem taka þátt í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="5dbfc-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5dbfc-145">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5dbfc-146">Notandi</span><span class="sxs-lookup"><span data-stu-id="5dbfc-146">User</span></span></td>
    <td><span data-ttu-id="5dbfc-147">Tilteknir Microsoft Dynamics 365 for Finance and Operations notendur</span><span class="sxs-lookup"><span data-stu-id="5dbfc-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5dbfc-148">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5dbfc-149">Listinn <strong>Tiltækir notendur</strong>: inniheldur alla notendur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="5dbfc-150">Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="5dbfc-151">Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="5dbfc-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

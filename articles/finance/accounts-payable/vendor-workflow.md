---
title: Verkflæði lánardrottins
description: Breyta lánardrottnaupplýsingum og nota verkflæði til að samþykkja þær.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 00cdc657fa075e84e62682e33ed3c1bace3f4ad0
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2020
ms.locfileid: "4444607"
---
# <a name="vendor-workflow"></a><span data-ttu-id="c3037-103">Verkflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c3037-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3037-104">Þegar verkflæði lánardrottins er notað eru breytingar sem gerðar eru á tilteknum reitum sendar í verkflæðið til samþykktar áður en þeim er bætt við lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="c3037-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="c3037-105">Setja upp verkflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c3037-105">Set up the vendor workflow</span></span>

<span data-ttu-id="c3037-106">Áður en hægt er að nota eiginleikann fyrir verkflæði þarf að virkja hann.</span><span class="sxs-lookup"><span data-stu-id="c3037-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="c3037-107">Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="c3037-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="c3037-108">Á flipanum **Almennt** á flýtiflipanum **Samþykki lánardrottins** skal stilla valkostinn **Virkja samþykki lánardrottins** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c3037-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="c3037-109">Í reitnum **Hegðun gagnaeiningar** skal velja þá hegðun sem á að nota þegar gögn eru flutt:</span><span class="sxs-lookup"><span data-stu-id="c3037-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="c3037-110">**Leyfa breytingar án samþykkis** – gagnaeiningin getur uppfært færslu lánardrottins án þess að vinna hana í gegnum verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="c3037-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="c3037-111">**Hafna breytingum** – ekki er hægt að gera breytingar á færslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c3037-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="c3037-112">Innflutningur mun mistakast fyrir reitina sem eru virkir fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="c3037-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="c3037-113">**Búa til tillögur að breytingum** – öllum reitum verður breytt nema reitunum sem eru virkir fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="c3037-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="c3037-114">Nýju gildunum fyrir þá reiti verður bætt við lánardrottin sem fyrirhuguðum breytingum og verkflæðið verður ræst sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="c3037-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="c3037-115">Í listanum yfir reiti lánardrottins skal velja gátreitinn **Virkja** fyrir hvern reit sem þarf að samþykkja áður en breytingarnar eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="c3037-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="c3037-116">Farðu í **Viðskiptaskuldir \> Uppsetning \> Verkflæði viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="c3037-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="c3037-117">Velja **Nýja**.</span><span class="sxs-lookup"><span data-stu-id="c3037-117">Select **New**.</span></span>
7. <span data-ttu-id="c3037-118">Veldu **Verkflæði fyrir fyrirhugaðar breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c3037-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="c3037-119">Setjið upp verkflæðið svo að það passi við samþykktarferlið.</span><span class="sxs-lookup"><span data-stu-id="c3037-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="c3037-120">Verkflæðissamþykktareiningin **Verkflæðissamþykki fyrir fyrirhugaða breytingu á lánardrottni** mun gera breytingarnar á lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="c3037-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="c3037-121">Breyta upplýsingum um lánardrottin og senda breytingarnar í verkflæðið</span><span class="sxs-lookup"><span data-stu-id="c3037-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="c3037-122">Þegar reit sem er virkur fyrir verkflæðið er breytt birtist síðan **Fyrirhugaðar breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c3037-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="c3037-123">Þessi síða sýnir upphaflegt gildi reitarins og nýja gildið sem slegið var inn.</span><span class="sxs-lookup"><span data-stu-id="c3037-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="c3037-124">Reitnum sem var breytt er breytt aftur í upprunalegt gildi.</span><span class="sxs-lookup"><span data-stu-id="c3037-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="c3037-125">Stöðuskilaboð gefa einnig til kynna að breytingarnar hafa ekki verið sendar inn.</span><span class="sxs-lookup"><span data-stu-id="c3037-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="c3037-126">Í hvert sinn sem reit sem er virkur fyrir verkflæðið er breytt er honum bætt á listann á síðunni **Fyrirhugaðar breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c3037-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="c3037-127">Til að fleygja fyrirhuguðu gildi fyrir reit skal nota hnappinn **Fleygja** við hliðina á reitnum í listanum.</span><span class="sxs-lookup"><span data-stu-id="c3037-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="c3037-128">Til að fleygja öllum breytingum skal nota hnappinn **Fleygja öllum breytingum** neðst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="c3037-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="c3037-129">Velja skal **Í lagi** til að loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="c3037-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="c3037-130">Eftir að a.m.k. ein fyrirhuguð breyting hefur verið gerð birtast tveir flipar í viðbót á aðgerðarsvæðinu: **Fyrirhugaðar breytingar** og **Verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="c3037-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="c3037-131">Velja skal **Fyrirhugaðar breytingar** til að opna síðuna **Fyrirhugaðar breytingar** og skoða breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="c3037-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="c3037-132">Velja skal **Verkflæði \> Senda inn til að senda breytingarnar í verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="c3037-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="c3037-133">Stöðunni á síðunni er breytt í **Breytingar bíða samþykkis**.</span><span class="sxs-lookup"><span data-stu-id="c3037-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="c3037-134">Verkflæðið fylgir venjulegu verkflæðisferli.</span><span class="sxs-lookup"><span data-stu-id="c3037-134">The workflow follows the standard workflow process.</span></span> <span data-ttu-id="c3037-135">Samþykktaraðila er beint á síðuna **Lánardrottinn** þar sem hægt er að fara yfir breytingar á síðunni **Fyrirhugaðar breytingar** og velja síðan **Verkflæði \> Samþykkja** til að samþykkja verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="c3037-135">The approver is directed to the **Vendor** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="c3037-136">Þegar búið er að samþykkja allt eru reitirnir uppfærðir með gildunum sem lögð voru til.</span><span class="sxs-lookup"><span data-stu-id="c3037-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>

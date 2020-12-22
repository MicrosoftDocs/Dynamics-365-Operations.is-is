---
title: Verkflæði viðskiptavinar
description: Í þessu efnisatriði er að finna upplýsingar um verkflæði viðskiptavinar. Tilgreindum reitum fyrir viðskiptavin er breytt og breytingarnar eru síðan sendar til samþykktar með því að nota verkflæðið áður en þeim er bætt við viðskiptavininn.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5998a492e12cb93aeec029c6e56f811f8b90055a
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2020
ms.locfileid: "4459274"
---
# <a name="customer-workflow"></a><span data-ttu-id="084fd-104">Verkflæði viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="084fd-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="084fd-105">Verkflæði viðskiptavinar hefur verið bætt við útgáfu 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="084fd-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="084fd-106">Hægt er að breyta tilgreindum reitum fyrir viðskiptavin og senda breytingarnar síðan til samþykktar með því að nota verkflæðið áður en þeim er bætt við viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="084fd-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="084fd-107">Setja upp verkflæði viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="084fd-107">Set up the customer workflow</span></span>

<span data-ttu-id="084fd-108">Áður en hægt er að nota eiginleikann fyrir verkflæði viðskiptavinar þarf að virkja hann.</span><span class="sxs-lookup"><span data-stu-id="084fd-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="084fd-109">Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="084fd-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="084fd-110">Á flipanum **Almennt** á flýtiflipanum **Samþykki viðskiptavinar** skal stilla valkostinn **Virkja samþykki viðskiptavinar** á **Já** til að virkja eiginleikann.</span><span class="sxs-lookup"><span data-stu-id="084fd-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="084fd-111">Í reitnum **Hegðun gagnaeiningar** skal velja þá hegðun sem gagnaeiningarnar eiga að nota þegar gögn eru flutt:</span><span class="sxs-lookup"><span data-stu-id="084fd-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="084fd-112">**Leyfa breytingar án samþykkis** – eining getur uppfært færslu viðskiptavinar án þess að vinna hana í gegnum verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="084fd-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="084fd-113">**Hafna breytingum** – ekki er hægt að gera breytingar á færslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="084fd-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="084fd-114">Innflutningur mun mistakast fyrir reitina sem eru virkir fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="084fd-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="084fd-115">**Búa til tillögur að breytingum** – öllum reitum verður breytt nema reitunum sem eru virkir fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="084fd-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="084fd-116">Nýju gildunum fyrir þá reiti verður bætt við viðskiptavininn sem fyrirhuguðum breytingum og verkflæðið verður ræst sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="084fd-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="084fd-117">Í listanum yfir reiti viðskiptavinar skal velja gátreitinn **Virkja** fyrir hvern reit sem þarf að samþykkja áður en breytingarnar eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="084fd-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="084fd-118">Opnið **Viðskiptakröfur \> Setja upp \> Verkflæði viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="084fd-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="084fd-119">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="084fd-119">Select **New**.</span></span>
7. <span data-ttu-id="084fd-120">Veljið **Verkflæði fyrir fyrirhugaða breytingu á viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="084fd-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="084fd-121">Setjið upp verkflæðið svo að það passi við samþykktarferlið.</span><span class="sxs-lookup"><span data-stu-id="084fd-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="084fd-122">Verkflæðissamþykktareiningin **Verkflæðissamþykki fyrir fyrirhugaða breytingu á viðskiptavini** mun gera breytingarnar á viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="084fd-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="084fd-123">Breyta upplýsingum um viðskiptavin og senda breytingarnar í verkflæðið</span><span class="sxs-lookup"><span data-stu-id="084fd-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="084fd-124">Þegar reit sem er virkur fyrir verkflæðið er breytt birtist síðan **Fyrirhugaðar breytingar**.</span><span class="sxs-lookup"><span data-stu-id="084fd-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="084fd-125">Þessi síða sýnir upphaflegt gildi reitarins og nýja gildið sem slegið var inn.</span><span class="sxs-lookup"><span data-stu-id="084fd-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="084fd-126">Reitnum sem var breytt er breytt aftur í upprunalegt gildi.</span><span class="sxs-lookup"><span data-stu-id="084fd-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="084fd-127">Stöðuskilaboð á síðunni gefa til kynna að breytingarnar hafa ekki verið sendar inn.</span><span class="sxs-lookup"><span data-stu-id="084fd-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="084fd-128">Í hvert sinn sem reit sem er virkur fyrir verkflæðið er breytt er honum bætt á listann yfir fyrirhugaðar breytingar.</span><span class="sxs-lookup"><span data-stu-id="084fd-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="084fd-129">Til að fleygja fyrirhuguðu gildi fyrir reit skal nota hnappinn **Fleygja** við hliðina á reitnum í listanum.</span><span class="sxs-lookup"><span data-stu-id="084fd-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="084fd-130">Til að fleygja öllum breytingum skal nota hnappinn **Fleygja öllum breytingum** neðst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="084fd-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="084fd-131">Velja skal **Í lagi** til að loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="084fd-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="084fd-132">Eftir að a.m.k. ein fyrirhuguð breyting hefur verið gerð birtast tvær valmyndir á aðgerðarsvæðinu: **Fyrirhugaðar breytingar** og **Verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="084fd-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="084fd-133">Velja skal **Fyrirhugaðar breytingar** til að opna síðuna **Fyrirhugaðar breytingar** og skoða breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="084fd-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="084fd-134">Velja skal **Verkflæði \> Senda inn** til að senda breytingarnar í verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="084fd-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="084fd-135">Stöðunni á síðunni er breytt í **Breytingar bíða samþykkis**.</span><span class="sxs-lookup"><span data-stu-id="084fd-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="084fd-136">Verkflæðið fylgir venjulegu verkflæðisferli í forritinu.</span><span class="sxs-lookup"><span data-stu-id="084fd-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="084fd-137">Samþykktaraðila er beint á síðuna **Viðskiptavinur** þar sem hægt er að fara yfir breytingar á síðunni **Fyrirhugaðar breytingar** og velja síðan **Verkflæði \> Samþykkja** til að samþykkja verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="084fd-137">The approver is directed to the **Customer** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="084fd-138">Þegar búið er að samþykkja allt eru reitirnir uppfærðir með gildunum sem lögð voru til.</span><span class="sxs-lookup"><span data-stu-id="084fd-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>

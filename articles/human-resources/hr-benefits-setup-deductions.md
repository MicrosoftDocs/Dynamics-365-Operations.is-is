---
title: Grunnstilla frádrætti
description: Notaðu frádrátt í Microsoft Dynamics 365 Human Resources til að ákvarða hve mikið, ef einhver er, til að draga frá launaávísun starfsmanns fyrir hverja bætur.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5287161f352b386ae4e13067f40228d7c1bce62
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092730"
---
# <a name="configure-deductions"></a><span data-ttu-id="d5883-103">Grunnstilla frádrætti</span><span class="sxs-lookup"><span data-stu-id="d5883-103">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d5883-104">Notaðu frádrátt í Microsoft Dynamics 365 Human Resources til að ákvarða hve mikið, ef einhver er, til að draga frá launaávísun starfsmanns fyrir hverja bætur.</span><span class="sxs-lookup"><span data-stu-id="d5883-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="d5883-105">Frádráttur er gildandi frá dagsetningunni, svo þú getur haldið sögulega skrá yfir frádráttarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="d5883-105">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="d5883-106">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Frádráttur**.</span><span class="sxs-lookup"><span data-stu-id="d5883-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="d5883-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d5883-107">Select **New**.</span></span>

3. <span data-ttu-id="d5883-108">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="d5883-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d5883-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="d5883-109">Field</span></span> | <span data-ttu-id="d5883-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d5883-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d5883-111">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="d5883-111">Deduction</span></span> | <span data-ttu-id="d5883-112">Sérstakt auðkenni sem er notað til að bera kennsl á fríðindafrádráttinn.</span><span class="sxs-lookup"><span data-stu-id="d5883-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="d5883-113">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d5883-113">Description</span></span> | <span data-ttu-id="d5883-114">Lýsing á frádrætti.</span><span class="sxs-lookup"><span data-stu-id="d5883-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="d5883-115">Virkt</span><span class="sxs-lookup"><span data-stu-id="d5883-115">Effective</span></span> | <span data-ttu-id="d5883-116">Upphafsdagsetningin.</span><span class="sxs-lookup"><span data-stu-id="d5883-116">The start date.</span></span> <span data-ttu-id="d5883-117">Sjálfgefið gildi er núverandi kerfisdagsetning.</span><span class="sxs-lookup"><span data-stu-id="d5883-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="d5883-118">Lok gildistíma</span><span class="sxs-lookup"><span data-stu-id="d5883-118">Expiration</span></span> | <span data-ttu-id="d5883-119">Lokadagsetningin.</span><span class="sxs-lookup"><span data-stu-id="d5883-119">The end date.</span></span> <span data-ttu-id="d5883-120">Sjálfgefið gildi er 12/31/2154, sem táknar aldrei.</span><span class="sxs-lookup"><span data-stu-id="d5883-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="d5883-121">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="d5883-121">Heading</span></span> | <span data-ttu-id="d5883-122">Fyrirsagnarkóði frá launakerfi sem þessi frádráttur mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá.</span><span class="sxs-lookup"><span data-stu-id="d5883-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d5883-123">Þetta er notað þegar þú notar þriðja aðila launaskrá.</span><span class="sxs-lookup"><span data-stu-id="d5883-123">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d5883-124">Tilvísun starfsmanns í launafrádrátt</span><span class="sxs-lookup"><span data-stu-id="d5883-124">Employee payroll deduction reference</span></span> | <span data-ttu-id="d5883-125">Kóðinn úr launakerfinu sem frádrátturinn notar fyrir hluta starfsmannsins eða atvinnuveitandans af frádrættinum þegar fríðindi eru reiknuð út miðað við laun.</span><span class="sxs-lookup"><span data-stu-id="d5883-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="d5883-126">Fyrirsögn upphæðar</span><span class="sxs-lookup"><span data-stu-id="d5883-126">Amount heading</span></span> | <span data-ttu-id="d5883-127">Fyrirsagnarkóði frá launakerfi sem þessi frádráttarupphæð mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá.</span><span class="sxs-lookup"><span data-stu-id="d5883-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d5883-128">Þetta er venjulega notað þegar þú notar þriðja aðila launaskrá.</span><span class="sxs-lookup"><span data-stu-id="d5883-128">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d5883-129">Má eyða</span><span class="sxs-lookup"><span data-stu-id="d5883-129">Can delete</span></span> | <span data-ttu-id="d5883-130">Tilgreinir hvort flutt gildi frá Dynamics 365 for Finance and Operations getur valdið því að gildinu er eytt í launakerfinu.</span><span class="sxs-lookup"><span data-stu-id="d5883-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="d5883-131">Paraðir dálkar</span><span class="sxs-lookup"><span data-stu-id="d5883-131">Paired columns</span></span> | <span data-ttu-id="d5883-132">Tilgreinir hvort flytja eigi fyrirsögn og frádráttarupphæð í pöruðum aðliggjandi dálkum til launakerfisins.</span><span class="sxs-lookup"><span data-stu-id="d5883-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="d5883-133">Breyta gildisdegi</span><span class="sxs-lookup"><span data-stu-id="d5883-133">Change effective date</span></span> | <span data-ttu-id="d5883-134">Dagsetningin þegar frádráttarbreyting fríðinda verður virk.</span><span class="sxs-lookup"><span data-stu-id="d5883-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="d5883-135">Á þessum degi mun kerfið sjálfkrafa breyta frítekjumarkinu og uppfæra allar fríðindaáætlanir sem fylgja þessu frádrætti, svo framarlega sem þú keyrir vinnslu frádráttaruppfærsluskipta.</span><span class="sxs-lookup"><span data-stu-id="d5883-135">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="d5883-136">Lokið er við að gera breytingar á frádrætti</span><span class="sxs-lookup"><span data-stu-id="d5883-136">Deduction change completed</span></span> | <span data-ttu-id="d5883-137">Gátreiturinn frá frádráttarbreytingum lokið verður sjálfkrafa valinn þegar breytingum á frádrætti bótagreiðslna hefur verið lokið með frávinnslu breytinga á frádrátti.</span><span class="sxs-lookup"><span data-stu-id="d5883-137">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="d5883-138">Veldu til að fylgjast með og viðhalda breytingum á uppbótarhlutfalli **Aðgerðir** og veldu síðan **Viðhalda útgáfum**.</span><span class="sxs-lookup"><span data-stu-id="d5883-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="d5883-139">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d5883-139">Select **Save**.</span></span> 
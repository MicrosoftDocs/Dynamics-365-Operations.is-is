---
title: Grunnstilla frádrætti
description: ''
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009432"
---
# <a name="configure-deductions"></a><span data-ttu-id="644df-102">Grunnstilla frádrætti</span><span class="sxs-lookup"><span data-stu-id="644df-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="644df-103">Notaðu frádrátt í Microsoft Dynamics 365 Human Resources til að ákvarða hve mikið, ef einhver er, til að draga frá launaávísun starfsmanns fyrir hverja bætur.</span><span class="sxs-lookup"><span data-stu-id="644df-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="644df-104">Frádráttur er gildandi frá dagsetningunni, svo þú getur haldið sögulega skrá yfir frádráttarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="644df-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="644df-105">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Frádráttur**.</span><span class="sxs-lookup"><span data-stu-id="644df-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="644df-106">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="644df-106">Select **New**.</span></span>

3. <span data-ttu-id="644df-107">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="644df-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="644df-108">Svæði</span><span class="sxs-lookup"><span data-stu-id="644df-108">Field</span></span> | <span data-ttu-id="644df-109">Lýsing</span><span class="sxs-lookup"><span data-stu-id="644df-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="644df-110">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="644df-110">Deduction</span></span> | <span data-ttu-id="644df-111">Sérstakt auðkenni sem er notað til að bera kennsl á fríðindafrádráttinn.</span><span class="sxs-lookup"><span data-stu-id="644df-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="644df-112">Lýsing</span><span class="sxs-lookup"><span data-stu-id="644df-112">Description</span></span> | <span data-ttu-id="644df-113">Lýsing á frádrætti.</span><span class="sxs-lookup"><span data-stu-id="644df-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="644df-114">Virkt</span><span class="sxs-lookup"><span data-stu-id="644df-114">Effective</span></span> | <span data-ttu-id="644df-115">Upphafsdagsetningin.</span><span class="sxs-lookup"><span data-stu-id="644df-115">The start date.</span></span> <span data-ttu-id="644df-116">Sjálfgefið gildi er núverandi kerfisdagsetning.</span><span class="sxs-lookup"><span data-stu-id="644df-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="644df-117">Lok gildistíma</span><span class="sxs-lookup"><span data-stu-id="644df-117">Expiration</span></span> | <span data-ttu-id="644df-118">Lokadagsetningin.</span><span class="sxs-lookup"><span data-stu-id="644df-118">The end date.</span></span> <span data-ttu-id="644df-119">Sjálfgefið gildi er 12/31/2154, sem táknar aldrei.</span><span class="sxs-lookup"><span data-stu-id="644df-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="644df-120">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="644df-120">Heading</span></span> | <span data-ttu-id="644df-121">Fyrirsagnarkóði frá launakerfi sem þessi frádráttur mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá.</span><span class="sxs-lookup"><span data-stu-id="644df-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="644df-122">Þetta er notað þegar þú notar þriðja aðila launaskrá.</span><span class="sxs-lookup"><span data-stu-id="644df-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="644df-123">Tilvísun starfsmanns í launafrádrátt</span><span class="sxs-lookup"><span data-stu-id="644df-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="644df-124">Kóðinn úr launakerfinu sem frádrátturinn notar fyrir hluta starfsmannsins eða atvinnuveitandans af frádrættinum þegar fríðindi eru reiknuð út miðað við laun.</span><span class="sxs-lookup"><span data-stu-id="644df-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="644df-125">Fyrirsögn upphæðar</span><span class="sxs-lookup"><span data-stu-id="644df-125">Amount heading</span></span> | <span data-ttu-id="644df-126">Fyrirsagnarkóði frá launakerfi sem þessi frádráttarupphæð mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá.</span><span class="sxs-lookup"><span data-stu-id="644df-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="644df-127">Þetta er venjulega notað þegar þú notar þriðja aðila launaskrá.</span><span class="sxs-lookup"><span data-stu-id="644df-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="644df-128">Má eyða</span><span class="sxs-lookup"><span data-stu-id="644df-128">Can delete</span></span> | <span data-ttu-id="644df-129">Tilgreinir hvort flutt gildi frá Dynamics 365 for Finance and Operations getur valdið því að gildinu er eytt í launakerfinu.</span><span class="sxs-lookup"><span data-stu-id="644df-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="644df-130">Paraðir dálkar</span><span class="sxs-lookup"><span data-stu-id="644df-130">Paired columns</span></span> | <span data-ttu-id="644df-131">Tilgreinir hvort flytja eigi fyrirsögn og frádráttarupphæð í pöruðum aðliggjandi dálkum til launakerfisins.</span><span class="sxs-lookup"><span data-stu-id="644df-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="644df-132">Breyta gildisdegi</span><span class="sxs-lookup"><span data-stu-id="644df-132">Change effective date</span></span> | <span data-ttu-id="644df-133">Dagsetningin þegar frádráttarbreyting fríðinda verður virk.</span><span class="sxs-lookup"><span data-stu-id="644df-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="644df-134">Á þessum degi mun kerfið sjálfkrafa breyta frítekjumarkinu og uppfæra allar fríðindaáætlanir sem fylgja þessu frádrætti, svo framarlega sem þú keyrir vinnslu frádráttaruppfærsluskipta.</span><span class="sxs-lookup"><span data-stu-id="644df-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="644df-135">Lokið er við að gera breytingar á frádrætti</span><span class="sxs-lookup"><span data-stu-id="644df-135">Deduction change completed</span></span> | <span data-ttu-id="644df-136">Gátreiturinn frá frádráttarbreytingum lokið verður sjálfkrafa valinn þegar breytingum á frádrætti bótagreiðslna hefur verið lokið með frávinnslu breytinga á frádrátti.</span><span class="sxs-lookup"><span data-stu-id="644df-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="644df-137">Veldu til að fylgjast með og viðhalda breytingum á uppbótarhlutfalli **Aðgerðir** og veldu síðan **Viðhalda útgáfum**.</span><span class="sxs-lookup"><span data-stu-id="644df-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="644df-138">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="644df-138">Select **Save**.</span></span> 

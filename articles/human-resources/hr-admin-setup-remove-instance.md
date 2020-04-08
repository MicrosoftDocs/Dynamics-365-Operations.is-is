---
title: Fjarlægja tilvik
description: Þessi grein fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources.
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
ms.openlocfilehash: a40b9619e92b81272208ad4241a2455330a342a7
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124429"
---
# <a name="remove-an-instance"></a><span data-ttu-id="81204-103">Fjarlægja tilvik</span><span class="sxs-lookup"><span data-stu-id="81204-103">Remove an instance</span></span>

<span data-ttu-id="81204-104">Þessi grein fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="81204-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="81204-105">Fjarlægja prufukeyrsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="81204-105">Remove a test drive environment</span></span>

<span data-ttu-id="81204-106">Human Resources prufukeyrslum er úthlutað með 60 daga gildistíma.</span><span class="sxs-lookup"><span data-stu-id="81204-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="81204-107">Hins vegar hafa eigendur prufukeyrsluumhverfa kost á því að ljúka prufuútgáfu snemma með því að ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="81204-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="81204-108">Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="81204-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="81204-109">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="81204-109">Select **Environments**.</span></span>
3. <span data-ttu-id="81204-110">Veldu umhverfi prufukeyrslu, sem er með nafngiftarmynstur svipað þessu: Prufukeyrsla - alias@domain</span><span class="sxs-lookup"><span data-stu-id="81204-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="81204-111">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="81204-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="81204-112">Núverandi umhverfi prufukeyrslu verður fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="81204-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="81204-113">Þegar það er fjarlægt getur þú skráð þig fyrir nýju prufukeyrsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="81204-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="81204-114">Fjarlægja framleiðsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="81204-114">Remove a production environment</span></span>

<span data-ttu-id="81204-115">Þeessi grein gerir ráð fyrir að þú hafir keypt Human Resources í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA).</span><span class="sxs-lookup"><span data-stu-id="81204-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="81204-116">Vegna þess að eitt Human Resources umhverfi er innifalið í einu Power Apps umhverfi, eru tveir valkostir sem þarf að hafa í huga.</span><span class="sxs-lookup"><span data-stu-id="81204-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="81204-117">Fyrsti valkosturinn felur í sér að fjarlægja allt Power Apps umhverfið; annar valkosturinn felur í sér að fjarlægja aðeins Human Resources.</span><span class="sxs-lookup"><span data-stu-id="81204-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="81204-118">Fyrsti kosturinn er valinn þegar þú hefur búið til Power Apps umhverfi sérstaklega með það fyrir augum að ráðstafa Human Resources, og þú hefur nýverið hafið framkvæmd eða þú hefur ekki sett af stað neinar samþættingar.</span><span class="sxs-lookup"><span data-stu-id="81204-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="81204-119">Annar kosturinn er viðeigandi þegar þú hefur komið fyrir Power Apps umhverfi sem er útfyllt af ríkulegum gögnum sem eru fengin úr Power Apps og Power Automate.</span><span class="sxs-lookup"><span data-stu-id="81204-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="81204-120">Áður en Power Apps umhverfið er fjarlægt skal tryggja að það sé ekki verið að nota það við samþættingu ríkulegra gagna utan Human Resources sviðsins.</span><span class="sxs-lookup"><span data-stu-id="81204-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="81204-121">Athugaðu einnig að sjálfgefið Power Apps umhverfi er ekki hægt að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="81204-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="81204-122">Til að fjarlægja allt Power Apps umhverfið, þar á meðal Human Resources og tengd forrit og flæði:</span><span class="sxs-lookup"><span data-stu-id="81204-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="81204-123">Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="81204-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="81204-124">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="81204-124">Select **Environments**.</span></span>
3. <span data-ttu-id="81204-125">Veldu umhverfið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="81204-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="81204-126">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="81204-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="81204-127">Bíddu þar til eyðingunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="81204-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="81204-128">Skráðu þig inn á [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Human Resources.</span><span class="sxs-lookup"><span data-stu-id="81204-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="81204-129">Veldu Human Resources verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="81204-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="81204-130">Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="81204-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="81204-131">Veldu tilvikið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="81204-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="81204-132">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="81204-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="81204-133">Til að fjarlægja Human Resources umhverfi úr núverandi Power Apps umhverfi skaltu ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="81204-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="81204-134">Athugaðu að nauðsyn þess að blanda notendaþjónustu við og hafa samband við hugbúnaðarteymi þróunar og aðgerða (DevOps) fyrir Human Resources er tímabundið þar til þessi eiginleiki er virkjaður beint í LCS.</span><span class="sxs-lookup"><span data-stu-id="81204-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="81204-135">Hafðu samband við Notendaþjónustu til að hefja beiðni um fjarlægingu.</span><span class="sxs-lookup"><span data-stu-id="81204-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="81204-136">Notendaþjónustan mun setja af stað beiðni um fjarlægingu með DevOps teymi fyrir Human Resources.</span><span class="sxs-lookup"><span data-stu-id="81204-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="81204-137">Haltu áfram eftir að orðsending berst um að umhverfið hafi verið fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="81204-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="81204-138">Skráðu þig inn á LCS með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Human Resources.</span><span class="sxs-lookup"><span data-stu-id="81204-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="81204-139">Veldu Human Resources verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="81204-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="81204-140">Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="81204-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="81204-141">Veldu tilvikið sem þú vilt fjarlægja, sem ætti að vera merkt með uppsetningarstöðuna **Mistókst**.</span><span class="sxs-lookup"><span data-stu-id="81204-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="81204-142">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="81204-142">Select **Remove instance** and confirm your decision.</span></span> 
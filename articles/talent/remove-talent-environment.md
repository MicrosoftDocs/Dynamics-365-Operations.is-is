---
title: "Fjarlægja Talent-umhverfi"
description: "Þetta efnisatriði fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: e0422a5b7ac227ad03ccafb4e34e614dc770a363
ms.contentlocale: is-is
ms.lasthandoff: 09/17/2018

---
# <a name="remove-talent-environments"></a><span data-ttu-id="29647-103">Fjarlægja Talent-umhverfi</span><span class="sxs-lookup"><span data-stu-id="29647-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="29647-104">Þetta efnisatriði fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="29647-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="29647-105">Að fjarlægja prufukeyrsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="29647-105">Removing a test drive environment</span></span>

<span data-ttu-id="29647-106">Talent prufukeyrslum er úthlutað með 60 daga gildistíma.</span><span class="sxs-lookup"><span data-stu-id="29647-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="29647-107">Hins vegar hafa eigendur prufukeyrsluumhverfa kost á því að ljúka prufuútgáfu snemma með því að ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="29647-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="29647-108">Farðu í [Stjórnendamiðstöð PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="29647-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="29647-109">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="29647-109">Select **Environments**.</span></span>
3. <span data-ttu-id="29647-110">Veldu umhverfi prufukeyrslu, sem er með nafngiftarmynstur svipað þessu: Prufukeyrsla - alias@domain</span><span class="sxs-lookup"><span data-stu-id="29647-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="29647-111">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="29647-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="29647-112">Núverandi umhverfi prufukeyrslu verður fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="29647-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="29647-113">Þegar það er fjarlægt getur þú skráð þig fyrir nýju prufukeyrsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="29647-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="29647-114">Að fjarlægja framleiðsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="29647-114">Removing a production environment</span></span>

<span data-ttu-id="29647-115">Þetta efnisatriði gerir ráð fyrir að þú hafir keypt Talent í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA).</span><span class="sxs-lookup"><span data-stu-id="29647-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="29647-116">Vegna þess að eitt Talent umhverfi er „innifalið“ í einu PowerApps umhverfi, eru tveir valkostir sem þarf að hafa í huga.</span><span class="sxs-lookup"><span data-stu-id="29647-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="29647-117">Fyrsti valkosturinn felur í sér að fjarlægja allt PowerApps umhverfið; annar valkosturinn felur í sér að fjarlægja aðeins Talent.</span><span class="sxs-lookup"><span data-stu-id="29647-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="29647-118">Fyrsti kosturinn er valinn þegar þú hefur búið til PowerApps umhverfi sérstaklega með það fyrir augum að ráðstafa Talent, og þú hefur nýverið hafið framkvæmd eða þú hefur ekki sett af stað neinar samþættingar.</span><span class="sxs-lookup"><span data-stu-id="29647-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="29647-119">Annar kosturinn er viðeigandi þegar þú hefur komið fyrir PowerApps umhverfi sem er útfyllt af ríkulegum gögnum sem eru fengin úr PowerApps og Flows.</span><span class="sxs-lookup"><span data-stu-id="29647-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="29647-120">Áður en PowerApps umhverfið er fjarlægt skal tryggja að það sé ekki verið að nota það við samþættingu ríkulegra gagna utan Talent sviðsins.</span><span class="sxs-lookup"><span data-stu-id="29647-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="29647-121">Athugaðu einnig að sjálfgefið PowerApps umhverfi er ekki hægt að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="29647-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="29647-122">Til að fjarlægja allt PowerApps umhverfið, þar á meðal Talent og tengd forrit og Flows:</span><span class="sxs-lookup"><span data-stu-id="29647-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="29647-123">Farðu í [Stjórnendamiðstöð PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="29647-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="29647-124">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="29647-124">Select **Environments**.</span></span>
3. <span data-ttu-id="29647-125">Veldu umhverfið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="29647-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="29647-126">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="29647-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="29647-127">Bíddu þar til eyðingunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="29647-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="29647-128">Skráðu þig inn á [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent.</span><span class="sxs-lookup"><span data-stu-id="29647-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="29647-129">Veldu Talent verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="29647-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="29647-130">Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="29647-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="29647-131">Veldu tilvikið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="29647-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="29647-132">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="29647-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="29647-133">Til að fjarlægja Talent umhverfi úr núverandi PowerApps umhverfi skaltu ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="29647-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="29647-134">Athugaðu að nauðsyn þess að blanda notendaþjónustu við og hafa samband við hugbúnaðarteymi þróunar og aðgerða (DevOps) fyrir Talent er tímabundið þar til þessi eiginleiki er virkjaður beint í LCS.</span><span class="sxs-lookup"><span data-stu-id="29647-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="29647-135">Hafðu samband við Notendaþjónustu til að hefja beiðni um fjarlægingu.</span><span class="sxs-lookup"><span data-stu-id="29647-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="29647-136">Notendaþjónustan mun setja af stað beiðni um fjarlægingu með DevOps teymi fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="29647-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="29647-137">Haltu áfram eftir að orðsending berst um að umhverfið hafi verið fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="29647-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="29647-138">Skráðu þig inn í LCS með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent.</span><span class="sxs-lookup"><span data-stu-id="29647-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="29647-139">Veldu Talent verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="29647-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="29647-140">Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="29647-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="29647-141">Veldu tilvikið sem þú vilt fjarlægja, sem ætti að vera merkt með uppsetningarstöðuna **Mistókst**.</span><span class="sxs-lookup"><span data-stu-id="29647-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="29647-142">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="29647-142">Select **Remove instance** and confirm your decision.</span></span> 



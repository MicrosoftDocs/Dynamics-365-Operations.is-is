---
title: Fjarlægja Talent-umhverfi
description: Þetta efnisatriði fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e752d658388fc6cb6f4b84ac83cb12a71522199b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898111"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="8b613-103">Fjarlægja Talent-umhverfi</span><span class="sxs-lookup"><span data-stu-id="8b613-103">Remove Talent environments</span></span>

<span data-ttu-id="8b613-104">Þetta efnisatriði fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="8b613-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="8b613-105">Að fjarlægja prufukeyrsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="8b613-105">Removing a test drive environment</span></span>

<span data-ttu-id="8b613-106">Talent prufukeyrslum er úthlutað með 60 daga gildistíma.</span><span class="sxs-lookup"><span data-stu-id="8b613-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="8b613-107">Hins vegar hafa eigendur prufukeyrsluumhverfa kost á því að ljúka prufuútgáfu snemma með því að ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="8b613-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="8b613-108">Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="8b613-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8b613-109">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="8b613-109">Select **Environments**.</span></span>
3. <span data-ttu-id="8b613-110">Veldu umhverfi prufukeyrslu, sem er með nafngiftarmynstur svipað þessu: Prufukeyrsla - alias@domain</span><span class="sxs-lookup"><span data-stu-id="8b613-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="8b613-111">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8b613-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="8b613-112">Núverandi umhverfi prufukeyrslu verður fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="8b613-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="8b613-113">Þegar það er fjarlægt getur þú skráð þig fyrir nýju prufukeyrsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="8b613-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="8b613-114">Að fjarlægja framleiðsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="8b613-114">Removing a production environment</span></span>

<span data-ttu-id="8b613-115">Þetta efnisatriði gerir ráð fyrir að þú hafir keypt Talent í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA).</span><span class="sxs-lookup"><span data-stu-id="8b613-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="8b613-116">Vegna þess að eitt Talent umhverfi er „innifalið“ í einu Power Apps umhverfi, eru tveir valkostir sem þarf að hafa í huga.</span><span class="sxs-lookup"><span data-stu-id="8b613-116">Since a single Talent environment is “contained” within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="8b613-117">Fyrsti valkosturinn felur í sér að fjarlægja allt Power Apps umhverfið; annar valkosturinn felur í sér að fjarlægja aðeins Talent.</span><span class="sxs-lookup"><span data-stu-id="8b613-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="8b613-118">Fyrsti kosturinn er valinn þegar þú hefur búið til Power Apps umhverfi sérstaklega með það fyrir augum að ráðstafa Talent, og þú hefur nýverið hafið framkvæmd eða þú hefur ekki sett af stað neinar samþættingar.</span><span class="sxs-lookup"><span data-stu-id="8b613-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="8b613-119">Annar kosturinn er viðeigandi þegar þú hefur komið fyrir Power Apps umhverfi sem er útfyllt af ríkulegum gögnum sem eru fengin úr Power Apps og Power Automate.</span><span class="sxs-lookup"><span data-stu-id="8b613-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="8b613-120">Áður en Power Apps umhverfið er fjarlægt skal tryggja að það sé ekki verið að nota það við samþættingu ríkulegra gagna utan Talent sviðsins.</span><span class="sxs-lookup"><span data-stu-id="8b613-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="8b613-121">Athugaðu einnig að sjálfgefið Power Apps umhverfi er ekki hægt að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="8b613-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="8b613-122">Til að fjarlægja allt Power Apps umhverfið, þar á meðal Talent og tengd forrit og flæði:</span><span class="sxs-lookup"><span data-stu-id="8b613-122">To remove the entire Power Apps environment, including Talent and the associated apps and flows:</span></span>

1. <span data-ttu-id="8b613-123">Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="8b613-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8b613-124">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="8b613-124">Select **Environments**.</span></span>
3. <span data-ttu-id="8b613-125">Veldu umhverfið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="8b613-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="8b613-126">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8b613-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="8b613-127">Bíddu þar til eyðingunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="8b613-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="8b613-128">Skráðu þig inn á [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent.</span><span class="sxs-lookup"><span data-stu-id="8b613-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="8b613-129">Veldu Talent verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="8b613-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="8b613-130">Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="8b613-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="8b613-131">Veldu tilvikið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="8b613-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="8b613-132">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="8b613-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="8b613-133">Til að fjarlægja Talent umhverfi úr núverandi Power Apps umhverfi skaltu ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="8b613-133">To remove a Talent environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="8b613-134">Athugaðu að nauðsyn þess að blanda notendaþjónustu við og hafa samband við hugbúnaðarteymi þróunar og aðgerða (DevOps) fyrir Talent er tímabundið þar til þessi eiginleiki er virkjaður beint í LCS.</span><span class="sxs-lookup"><span data-stu-id="8b613-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="8b613-135">Hafðu samband við Notendaþjónustu til að hefja beiðni um fjarlægingu.</span><span class="sxs-lookup"><span data-stu-id="8b613-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="8b613-136">Notendaþjónustan mun setja af stað beiðni um fjarlægingu með DevOps teymi fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="8b613-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="8b613-137">Haltu áfram eftir að orðsending berst um að umhverfið hafi verið fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="8b613-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="8b613-138">Skráðu þig inn í LCS með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent.</span><span class="sxs-lookup"><span data-stu-id="8b613-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="8b613-139">Veldu Talent verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="8b613-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="8b613-140">Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="8b613-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="8b613-141">Veldu tilvikið sem þú vilt fjarlægja, sem ætti að vera merkt með uppsetningarstöðuna **Mistókst**.</span><span class="sxs-lookup"><span data-stu-id="8b613-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="8b613-142">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="8b613-142">Select **Remove instance** and confirm your decision.</span></span> 


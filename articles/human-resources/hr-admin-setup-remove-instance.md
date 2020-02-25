---
title: Fjarlægja tilvik
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
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009363"
---
# <a name="remove-an-instance"></a><span data-ttu-id="dc5b3-102">Fjarlægja tilvik</span><span class="sxs-lookup"><span data-stu-id="dc5b3-102">Remove an instance</span></span>

<span data-ttu-id="dc5b3-103">Þessi grein fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="dc5b3-104">Fjarlægja prufukeyrsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="dc5b3-104">Remove a test drive environment</span></span>

<span data-ttu-id="dc5b3-105">Human Resources prufukeyrslum er úthlutað með 60 daga gildistíma.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="dc5b3-106">Hins vegar hafa eigendur prufukeyrsluumhverfa kost á því að ljúka prufuútgáfu snemma með því að ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="dc5b3-107">Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="dc5b3-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="dc5b3-108">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-108">Select **Environments**.</span></span>
3. <span data-ttu-id="dc5b3-109">Veldu umhverfi prufukeyrslu, sem er með nafngiftarmynstur svipað þessu: Prufukeyrsla - alias@domain</span><span class="sxs-lookup"><span data-stu-id="dc5b3-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="dc5b3-110">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="dc5b3-111">Núverandi umhverfi prufukeyrslu verður fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="dc5b3-112">Þegar það er fjarlægt getur þú skráð þig fyrir nýju prufukeyrsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="dc5b3-113">Fjarlægja framleiðsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="dc5b3-113">Remove a production environment</span></span>

<span data-ttu-id="dc5b3-114">Þeessi grein gerir ráð fyrir að þú hafir keypt Human Resources í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA).</span><span class="sxs-lookup"><span data-stu-id="dc5b3-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="dc5b3-115">Vegna þess að eitt Human Resources umhverfi er innifalið í einu Power Apps umhverfi, eru tveir valkostir sem þarf að hafa í huga.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="dc5b3-116">Fyrsti valkosturinn felur í sér að fjarlægja allt Power Apps umhverfið; annar valkosturinn felur í sér að fjarlægja aðeins Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="dc5b3-117">Fyrsti kosturinn er valinn þegar þú hefur búið til Power Apps umhverfi sérstaklega með það fyrir augum að ráðstafa Human Resources, og þú hefur nýverið hafið framkvæmd eða þú hefur ekki sett af stað neinar samþættingar.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="dc5b3-118">Annar kosturinn er viðeigandi þegar þú hefur komið fyrir Power Apps umhverfi sem er útfyllt af ríkulegum gögnum sem eru fengin úr Power Apps og Power Automate.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="dc5b3-119">Áður en Power Apps umhverfið er fjarlægt skal tryggja að það sé ekki verið að nota það við samþættingu ríkulegra gagna utan Human Resources sviðsins.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="dc5b3-120">Athugaðu einnig að sjálfgefið Power Apps umhverfi er ekki hægt að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="dc5b3-121">Til að fjarlægja allt Power Apps umhverfið, þar á meðal Human Resources og tengd forrit og flæði:</span><span class="sxs-lookup"><span data-stu-id="dc5b3-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="dc5b3-122">Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="dc5b3-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="dc5b3-123">Veldu **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-123">Select **Environments**.</span></span>
3. <span data-ttu-id="dc5b3-124">Veldu umhverfið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="dc5b3-125">Veldu **Eyða** og staðfestu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="dc5b3-126">Bíddu þar til eyðingunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="dc5b3-127">Skráðu þig inn á [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="dc5b3-128">Veldu Human Resources verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="dc5b3-129">Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="dc5b3-130">Veldu tilvikið sem á að fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="dc5b3-131">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="dc5b3-132">Til að fjarlægja Human Resources umhverfi úr núverandi Power Apps umhverfi skaltu ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="dc5b3-133">Athugaðu að nauðsyn þess að blanda notendaþjónustu við og hafa samband við hugbúnaðarteymi þróunar og aðgerða (DevOps) fyrir Human Resources er tímabundið þar til þessi eiginleiki er virkjaður beint í LCS.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="dc5b3-134">Hafðu samband við Notendaþjónustu til að hefja beiðni um fjarlægingu.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="dc5b3-135">Notendaþjónustan mun setja af stað beiðni um fjarlægingu með DevOps teymi fyrir Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="dc5b3-136">Haltu áfram eftir að orðsending berst um að umhverfið hafi verið fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="dc5b3-137">Skráðu þig inn á LCS með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="dc5b3-138">Veldu Human Resources verkið sem inniheldur umhverfið.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="dc5b3-139">Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="dc5b3-140">Veldu tilvikið sem þú vilt fjarlægja, sem ætti að vera merkt með uppsetningarstöðuna **Mistókst**.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="dc5b3-141">Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-141">Select **Remove instance** and confirm your decision.</span></span> 

---
title: Úrræðaleit vandamála við fyrstu uppsetningu
description: Þetta efni veitir upplýsingar um bilanaleit sem geta hjálpað þér að laga vandamál sem gætu komið upp við upphaflega uppsetningu tvískiptrar skrifunar á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172669"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="e5a5b-103">Úrræðaleit vandamála við fyrstu uppsetningu</span><span class="sxs-lookup"><span data-stu-id="e5a5b-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e5a5b-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="e5a5b-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega uppsetningu á samþættingu tvöfaldra skrifa.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5a5b-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="e5a5b-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="e5a5b-108">Þú getur ekki tengt forrit Finance and Operations við Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e5a5b-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="e5a5b-109">**Nauðsynleg skilríki til að setja upp tvískipt skrifun:** Azure AD leigjandastjóri</span><span class="sxs-lookup"><span data-stu-id="e5a5b-109">**Required credentials to set up dual-write:** Azure AD tenant admin</span></span>

<span data-ttu-id="e5a5b-110">Villur á síðunni **Setja upp tengil á Common Data Service** orsakast venjulega af ólokinni uppsetningu eða heimildavandamálum.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="e5a5b-111">Gakktu úr skugga um að öll ástandsskoðunin standist á síðunni **Setja upp tengil á Common Data Service** eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="e5a5b-112">Þú getur ekki tengt tvískipt skrif nema öll ástandsskoðunin standist.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-112">You can't link dual-write unless the whole health check passes.</span></span>

![Vel heppnuð ástandsskoðun](media/health_check.png)

<span data-ttu-id="e5a5b-114">Þú verður að hafa Azure AD leigjandastjóraskilríki til að tengja Finance and Operations og Common Data Service umhverfin.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="e5a5b-115">Eftir að þú hefur tengt umhverfið geta notendur skráð sig inn með því að nota reikningsskilríki sín og uppfært núverandi einingakort.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="e5a5b-116">Villa þegar þú opnar tengilinn á síðuna Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e5a5b-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="e5a5b-117">**Nauðsynleg skilríki til að laga vandann:** Azure AD leigjandastjóri</span><span class="sxs-lookup"><span data-stu-id="e5a5b-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="e5a5b-118">Þú gætir fengið eftirfarandi villuboð þegar þú opnar **Tengill við síðuna Common Data Service** í forriti Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e5a5b-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="e5a5b-119">*Kóði svörunarstöðu bendir ekki til árangurs: 404 (Not Found.)*</span><span class="sxs-lookup"><span data-stu-id="e5a5b-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="e5a5b-120">Þessi villa kemur upp þegar samþykkisskrefinu hefur ekki verið lokið.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="e5a5b-121">Til að staðfesta hvort samþykkisskrefinu hafi verið lokið, skráðu þig inn á portal.Azure.com með því að nota Azure AD leigjandastjórareikning og sjáðu hvort forritið frá þriðja aðila sem hefur auðkenni **33976c19-1db5-4c02-810e-c243db79efde** birtist á listanum Azure AD **Enterprise-forrit**.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="e5a5b-122">Ef það gengur ekki verður þú að veita samþykki í forriti.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="e5a5b-123">Fylgdu þessum skrefum til að veita samþykki í forriti.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="e5a5b-124">Opnaðu eftirfarandi slóð með því að nota skilríki stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="e5a5b-125">Þú ættir að fá kvaðninu um samþykki.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="e5a5b-126">Veldu **Samþykkja** til að gefa til kynna að þú veiti samþykki þitt fyrir uppsetningu á forritinu sem er með kennið **33976c19-1db5-4c02-810e-c243db79efde** í leigjanda þínum.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="e5a5b-127">Þetta forrit er nauðsynlegt til að tengja forritin Common Data Service og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="e5a5b-128">Ef þú átt í vandræðum með þetta skref skaltu opna vafrann þinn í huliðsstillingu (í Google Chrome) eða InPrivate ham (í Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="e5a5b-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="e5a5b-129">Gakktu úr skugga um að fyrirtækjagögn og tvískipt teymi séu sett upp rétt við tengingu</span><span class="sxs-lookup"><span data-stu-id="e5a5b-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="e5a5b-130">Til að tryggja að tvískipt skrifun virki rétt eru fyrirtækin sem þú velur við stillingar stofnuð í Common Data Service umhverfi.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="e5a5b-131">Sjálfgefið er að þessi fyrirtæki séu skrifvarin og eiginleikinn **IsDualWriteEnable** stilltur á **True**.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="e5a5b-132">Að auki eru sjálfgefnir eigendur viðskiptaeininga og teymi stofnuð og fela í sér nafn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="e5a5b-133">Áður en þú kveikir á kortunum skaltu ganga úr skugga um að sjálfgefinn eigandi hópsins sé tilgreindur.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="e5a5b-134">Til að finna eininguna **Companies (CDM\_Company)** fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="e5a5b-135">Veldu síuna í efra hægra horninu í líkansdrifna forritinu í Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="e5a5b-136">Í fellilistanum velurðu **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="e5a5b-137">Veldu **Keyra** til að sjá niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="e5a5b-138">Veldu fyrirtækið sem var tengt þegar þú stillir tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="e5a5b-139">Staðfestu að reiturinn **Sjálfgefið eigendateymi** hefur gildi.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="e5a5b-140">Á eftirfarandi mynd er reiturinn **Sjálfgefið eigendateymi** stilltur á **USMF tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![Staðfestir sjálfgefið eigendateymi](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="e5a5b-142">Finndu takmörk á fjölda lögaðila eða fyrirtækja sem hægt er að tengja fyrir tvískipt skrif</span><span class="sxs-lookup"><span data-stu-id="e5a5b-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="e5a5b-143">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að virkja varpanir:</span><span class="sxs-lookup"><span data-stu-id="e5a5b-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="e5a5b-144">*Dual write failure - Plugin registration failed: \[(Ekki tókst að fá skiltáknakort fyrir verk DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Villa fer fram yfir hámarksskiltákn leyfð fyrir vörpun á DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Ein eða fleiri villur komu upp.*</span><span class="sxs-lookup"><span data-stu-id="e5a5b-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="e5a5b-145">Núverandi takmörk þegar þú tengir umhverfið eru um það bil 40 lögaðilar.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="e5a5b-146">Þessi villa kemur upp ef þú reynir að virkja kort og meira en 40 lögaðilar eru tengdir milli umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="e5a5b-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>
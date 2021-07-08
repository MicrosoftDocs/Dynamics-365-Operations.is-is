---
title: Hafist handa með altækt birgðabókhald
description: Í þessu efnisatriði er lýst hvernig á að hefjast handa með altækt birgðabókhald.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301699"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="c8536-103">Hafist handa með altækt birgðabókhald</span><span class="sxs-lookup"><span data-stu-id="c8536-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="c8536-104">Altækt birgðabókhald gerir kleift að nota meira en eitt birgðabókhald í fjárhagsbókum altæks birgðabókhalds sem búið er að setja upp.</span><span class="sxs-lookup"><span data-stu-id="c8536-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="c8536-105">Tengja verður hvern fjárhag altæks birgðabókhalds við *viðtekna reglu*.</span><span class="sxs-lookup"><span data-stu-id="c8536-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="c8536-106">Regla er safn af eftirfarandi gerðum reikningsskilaaðferða:</span><span class="sxs-lookup"><span data-stu-id="c8536-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="c8536-107">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="c8536-107">Cost object</span></span>
- <span data-ttu-id="c8536-108">Grunnmæling inntaks</span><span class="sxs-lookup"><span data-stu-id="c8536-108">Input measurement basis</span></span>
- <span data-ttu-id="c8536-109">Áætlun kostnaðarflæðis</span><span class="sxs-lookup"><span data-stu-id="c8536-109">Cost flow assumption</span></span>
- <span data-ttu-id="c8536-110">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="c8536-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="c8536-111">Jafnvel eftir að kveikt er á altæku birgðabókhaldi er enn hægt að sinna birgðabókhaldi í Microsoft Dynamics 365 Supply Chain Management eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="c8536-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="c8536-112">Altækt birgðabókhald er innbót.</span><span class="sxs-lookup"><span data-stu-id="c8536-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="c8536-113">Til að gera aðgerðir þess aðgengilegar verður þú að setja hana upp frá Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c8536-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c8536-114">Þú getur valið að meta það í prufuumhverfi áður en þú setur það í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="c8536-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="c8536-115">Eins og er styður altækt birgðabókhald ekki alla eiginleika kostnaðarstjórnunar sem eru innbyggðir í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c8536-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="c8536-116">Þess vegna er mikilvægt að þú metir hvort grunneiginleikarnir sem nú eru tiltækir uppfylli kröfur þínar.</span><span class="sxs-lookup"><span data-stu-id="c8536-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="c8536-117">Hvernig á að fá opna forútgáfu altæks birgðabókhalds</span><span class="sxs-lookup"><span data-stu-id="c8536-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8536-118">Til að nota altækt birgðabókhald verður þú að vera með stöðugt LCS-virkjað umhverfi (ekki OneBox-umhverfi).</span><span class="sxs-lookup"><span data-stu-id="c8536-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="c8536-119">Auk þess þarf að keyra Supply Chain Management útgáfu 10.0.19 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="c8536-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="c8536-120">Til að skrá sig fyrir opinni forútgáfu altæks birgðabókhalds skal senda LCS-umhverfiskennið í tölvupósti á [Teymi altæks birgðabókhalds](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c8536-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="c8536-121">Þegar þú hefur fengið samþykki fyrir forritinu mun teymið senda þér eftirfylgnipóst sem inniheldur beta-lykil altæks birgðabókhalds og endastöðvar þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="c8536-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="c8536-122">Þegar þú hefur fengið beta-lykilinn geturðu [sett upp innbótina](#install).</span><span class="sxs-lookup"><span data-stu-id="c8536-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="c8536-123">Leyfisveiting</span><span class="sxs-lookup"><span data-stu-id="c8536-123">Licensing</span></span>

<span data-ttu-id="c8536-124">Leyfisveiting altæks birgðabókhalds fer saman við hefðbundna eiginleika birgðabókhalds sem eru í boði fyrir Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c8536-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="c8536-125">Þú þarft ekki að kaupa viðbótarleyfi til að nota altækt birgðabókhald.</span><span class="sxs-lookup"><span data-stu-id="c8536-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8536-126">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="c8536-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="c8536-127">Setja upp Microsoft Power Platform-samþættingu</span><span class="sxs-lookup"><span data-stu-id="c8536-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="c8536-128">Áður en hægt er að virkja virkni innbótarinnar þarf að samþætta við Microsoft Power Platform með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c8536-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="c8536-129">Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="c8536-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="c8536-130">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="c8536-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="c8536-131">Í hlutanum **Power Platform samþætting** skal velja **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="c8536-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="c8536-132">Í svarglugganum **Uppsetning á umhverfi Power Platform** er gátreiturinn valinn og síðan **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="c8536-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="c8536-133">Venjulega tekur uppsetningin á milli 60 og 90 mínútur.</span><span class="sxs-lookup"><span data-stu-id="c8536-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="c8536-134">Að lokinni uppsetningu Microsoft Power Platform sýnir síðan heiti umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="c8536-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="c8536-135">Auk þess sýnir hlutinn **Power Platform samþætting** fullyrðinguna „uppsetningu Power Platform-umhverfis er lokið“.</span><span class="sxs-lookup"><span data-stu-id="c8536-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="c8536-136">Altækt birgðabókhald krefst ekki forrits tvöfaldrar skráningar.</span><span class="sxs-lookup"><span data-stu-id="c8536-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="c8536-137">Frekari upplýsingar er að finna í [Uppsetning að lokinni uppsetningu umhverfis](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="c8536-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="c8536-138">Setja upp Dataverse</span><span class="sxs-lookup"><span data-stu-id="c8536-138">Set up Dataverse</span></span>

<span data-ttu-id="c8536-139">Áður en Dataverse er sett upp skal bæta þjónustureglum altæks birgðabókhalds við leigjandann með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c8536-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="c8536-140">Setjið upp Azure AD einingu fyrir Windows PowerShell v2 eins og lýst er í [Setja upp Azure Active Directory PowerShell fyrir Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="c8536-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="c8536-141">Keyra eftirfarandi PowerShell-skipun.</span><span class="sxs-lookup"><span data-stu-id="c8536-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="c8536-142">Næst skal stofna notendur forrits fyrir altækt birgðabókhald í Dataverse með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c8536-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="c8536-143">Opnið vefslóð Dataverse umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="c8536-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="c8536-144">Farið í **Ítarleg stilling \> Kerfi \> Öryggi \> Notendur** og stofnið notanda forrits.</span><span class="sxs-lookup"><span data-stu-id="c8536-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="c8536-145">Notið reitinn **Yfirlit** til að breyta síðuyfirlitinu í *Notendur forrits*.</span><span class="sxs-lookup"><span data-stu-id="c8536-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="c8536-146">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c8536-146">Select **New**.</span></span>
1. <span data-ttu-id="c8536-147">Stilltu reitinn **Forritskenni** á *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="c8536-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="c8536-148">Veljið **Úthluta hlutverki** og veljið því næst *Kerfisstjóri*.</span><span class="sxs-lookup"><span data-stu-id="c8536-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="c8536-149">Ef til er hlutverk sem heitir *Common Data Service Notandi* skal líka velja það.</span><span class="sxs-lookup"><span data-stu-id="c8536-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="c8536-150">Endurtakið skrefin á undan, en stillið reitinn **Forritskenni** á *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="c8536-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="c8536-151">Frekari upplýsingar eru í [Stofna notanda forrits](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="c8536-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="c8536-152">Ef sjálfgefið tungumál Dataverse-uppsetningar er ekki enska skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c8536-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="c8536-153">Farið í **Ítarleg stilling \> Stjórnun \> Tungumál**.</span><span class="sxs-lookup"><span data-stu-id="c8536-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="c8536-154">Veljið *Enska* (*LanguageCode=1033*) og síðan **Nota**.</span><span class="sxs-lookup"><span data-stu-id="c8536-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="c8536-155">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="c8536-155">Install the add-in</span></span>

<span data-ttu-id="c8536-156">Fylgið þessum skrefum til að setja upp innbótina þannig að hægt sé að nota altækt birgðabókhald.</span><span class="sxs-lookup"><span data-stu-id="c8536-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="c8536-157">[Skráðu þig](#sign-up) fyrir opinni forútgáfu altæks birgðabókhalds.</span><span class="sxs-lookup"><span data-stu-id="c8536-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="c8536-158">Skráðu þig inn í [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="c8536-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="c8536-159">Farið í **Stjórnun forskoðunareiginleika**.</span><span class="sxs-lookup"><span data-stu-id="c8536-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="c8536-160">Veldu plústáknið (**+**).</span><span class="sxs-lookup"><span data-stu-id="c8536-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="c8536-161">Í reitinn **Kóði** skal slá inn beta-lykil innbótar fyrir altækt birgðabókhald.</span><span class="sxs-lookup"><span data-stu-id="c8536-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="c8536-162">(Þú ættir að hafa fengið beta-lykilinn í tölvupósti þegar þú nýskráðir þig.)</span><span class="sxs-lookup"><span data-stu-id="c8536-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="c8536-163">Veldu síðan **Opna fyrir**.</span><span class="sxs-lookup"><span data-stu-id="c8536-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="c8536-164">Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="c8536-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="c8536-165">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="c8536-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="c8536-166">Farið í **Power Platform samþætting** og veljið **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="c8536-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="c8536-167">Í svarglugganum **Uppsetning á umhverfi Power Platform** er gátreiturinn valinn og síðan **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="c8536-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="c8536-168">Venjulega tekur uppsetningin á milli 60 og 90 mínútur.</span><span class="sxs-lookup"><span data-stu-id="c8536-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="c8536-169">Að lokinni uppsetningu á Microsoft Power Platform-umhverfinu, í flýtiflipanum **Innbætur umhverfis**, skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="c8536-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="c8536-170">Veljið **Altækt birgðabókhald**.</span><span class="sxs-lookup"><span data-stu-id="c8536-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="c8536-171">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="c8536-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="c8536-172">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="c8536-172">Select **Install**.</span></span>
1. <span data-ttu-id="c8536-173">Í flýtiflipanum **Innbætur umhverfis** ættir þú að sjá að verið er að setja upp altækt birgðabókhald.</span><span class="sxs-lookup"><span data-stu-id="c8536-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="c8536-174">Eftir nokkrar mínútur ætti staðan að breytast úr *Setur upp* í *Uppsett*.</span><span class="sxs-lookup"><span data-stu-id="c8536-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="c8536-175">(Hugsanlega verður þú að endurhlaða síðuna til að breytingin komi í ljós). Á þeim tímapunkti er altækt birgðabókhald tilbúið til notkunar.</span><span class="sxs-lookup"><span data-stu-id="c8536-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="c8536-176">Setja upp samþættingu</span><span class="sxs-lookup"><span data-stu-id="c8536-176">Set up the integration</span></span>

<span data-ttu-id="c8536-177">Fylgið þessum skrefum til að setja upp samþættingu milli altæks birgðabókhalds og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c8536-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="c8536-178">Skráðu þig inn í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c8536-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="c8536-179">Farið í **Kerfisstjórnun \> Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c8536-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="c8536-180">Veldu **Leita að uppfærslum**.</span><span class="sxs-lookup"><span data-stu-id="c8536-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="c8536-181">Í flipanum **Allt** skal leita að eiginleikanum sem heitir *Altækt birgðabókhald*.</span><span class="sxs-lookup"><span data-stu-id="c8536-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="c8536-182">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="c8536-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="c8536-183">Farið í **Altækt birgðabókhald \> Uppsetning \> Færibreytur altæks birgðabókhalds \> Færibreytur samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="c8536-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="c8536-184">Í reitina **Endastöð gagnaþjónustu** og **Endastöð altæks birgðabókhalds** skal færa inn vefslóðir úr tölvupóstinum sem teymi altæks birgðabókhalds sendi þér þegar þú nýskráðir þig fyrir forútgáfunni.</span><span class="sxs-lookup"><span data-stu-id="c8536-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="c8536-185">Altækt birgðabókhald er nú tilbúið til notkunar.</span><span class="sxs-lookup"><span data-stu-id="c8536-185">Global Inventory Accounting is now ready to use.</span></span>

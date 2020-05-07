---
title: Hafist handa með kostnaðarbókhaldsþjónustu
description: Þetta efnisatriði inniheldur leiðbeiningar varðandi leyfi og leiðbeiningar um uppsetningu á kostnaðarbókhaldsþjónustuna.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276928"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="deae4-103">Hafist handa með kostnaðarbókhaldsþjónustu</span><span class="sxs-lookup"><span data-stu-id="deae4-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="deae4-104">Virkni sem getið er í þessu efnisatriði er tiltæk sem hluti af sérstakri prufuútgáfu.</span><span class="sxs-lookup"><span data-stu-id="deae4-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="deae4-105">Efni þessa efnisatriðis og virknin sem þar er lýst geta breyst.</span><span class="sxs-lookup"><span data-stu-id="deae4-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="deae4-106">Frekari upplýsingar um forútgáfur er að finna í hlutanum [Algengar spurningar um uppfærslureglur fyrir „Ein útgáfa“](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="deae4-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="deae4-107">Kostnaðarbókhaldsþjónusta gerir þér kleift að framkvæma fjöldamörg birgðabókhöld í fjárhagi kostnaðarbókhalds sem þú hefur sett upp.</span><span class="sxs-lookup"><span data-stu-id="deae4-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="deae4-108">Þú tengir hvern fjárhag kostnaðarbókhalds við *reglu*.</span><span class="sxs-lookup"><span data-stu-id="deae4-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="deae4-109">Regla er safn af eftirfarandi gerðum reikningsskilaaðferða:</span><span class="sxs-lookup"><span data-stu-id="deae4-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="deae4-110">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="deae4-110">Cost object</span></span>
- <span data-ttu-id="deae4-111">Grunnmæling inntaks</span><span class="sxs-lookup"><span data-stu-id="deae4-111">Input measurement basis</span></span>
- <span data-ttu-id="deae4-112">Áætlun kostnaðarflæðis</span><span class="sxs-lookup"><span data-stu-id="deae4-112">Cost flow assumption</span></span>
- <span data-ttu-id="deae4-113">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="deae4-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="deae4-114">Jafnvel eftir að þú hefur kveikt á kostnaðarbókhaldsþjónustunni geturðu samt gert birgðabókhald í Microsoft Dynamics 365 Supply Chain Management eins og áður.</span><span class="sxs-lookup"><span data-stu-id="deae4-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="deae4-115">Kostnaðarbókhaldsþjónustan er viðbót.</span><span class="sxs-lookup"><span data-stu-id="deae4-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="deae4-116">Til að gera aðgerðir þess aðgengilegar verður þú að setja hana upp frá Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="deae4-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="deae4-117">Þess vegna getur þú valið að meta það í prufuumhverfi áður en þú setur það í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="deae4-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="deae4-118">Kostnaðarbókhaldsþjónustan styður ekki sem stendur alla þá kostnaðarstjórnunareiginleika sem eru innbyggðir í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="deae4-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="deae4-119">Þess vegna er mikilvægt að þú metir hvort grunneiginleikarnir sem nú eru tiltækir uppfylli kröfur þínar.</span><span class="sxs-lookup"><span data-stu-id="deae4-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="deae4-120">Leyfisveiting</span><span class="sxs-lookup"><span data-stu-id="deae4-120">Licensing</span></span>

<span data-ttu-id="deae4-121">Kostnaðarbókhaldþjónustan er háð leyfi ásamt stöðluðu eiginleikum birgðabókhalds sem eru í boði fyrir Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="deae4-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="deae4-122">Þú þarft ekki að kaupa viðbótarleyfi til að nota kostnaðarbókhaldsþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="deae4-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="deae4-123">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="deae4-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="deae4-124">Til að nota kostnaðarbókhaldsþjónustuna verður þú að vera með LCS-virkt umhverfi með mikið framboð (ekki OneBox umhverfi) og þú verður að keyra útgáfu 10.0.11 af Dynamics 365 Supply Chain Management eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="deae4-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="deae4-125">Til að nota kostnaðarbókhaldsþjónustuna, skaltu setja upp viðbót kostnaðarbókhaldsþjónustu fyrir Supply Chain Management eins og lýst er í eftirfarandi aðferð.</span><span class="sxs-lookup"><span data-stu-id="deae4-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="deae4-126">Skráðu þig inn í LCS.</span><span class="sxs-lookup"><span data-stu-id="deae4-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="deae4-127">Farið í **Stjórnun forskoðunareiginleika**.</span><span class="sxs-lookup"><span data-stu-id="deae4-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="deae4-128">Veldu plústáknið (**+**).</span><span class="sxs-lookup"><span data-stu-id="deae4-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="deae4-129">Sláðu inn beta-lykilinn fyrir viðbót kostnaðarbókhaldsþjónustu á svæðið **Kóði**.</span><span class="sxs-lookup"><span data-stu-id="deae4-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="deae4-130">(Þú hefðir átt að fá lykilinn þinn með tölvupósti.)</span><span class="sxs-lookup"><span data-stu-id="deae4-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="deae4-131">Veldu síðan **Opna fyrir**.</span><span class="sxs-lookup"><span data-stu-id="deae4-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="deae4-132">Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="deae4-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="deae4-133">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="deae4-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="deae4-134">Flettu niður að flýtiflipanum **Umhverfisinnbætur**.</span><span class="sxs-lookup"><span data-stu-id="deae4-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="deae4-135">Veldu **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="deae4-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="deae4-136">Veljið **Kostnaðarbókhaldsþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="deae4-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="deae4-137">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="deae4-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="deae4-138">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="deae4-138">Select **Install**.</span></span>

1. <span data-ttu-id="deae4-139">Í flýtiflipanum **Viðbætur fyrir umhverfi** ættir þú að sjá að kostnaðarbókhaldsþjónustan er sett upp.</span><span class="sxs-lookup"><span data-stu-id="deae4-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="deae4-140">Eftir nokkrar mínútur ætti staðan að breytast úr **Setur upp** í **Uppsett**.</span><span class="sxs-lookup"><span data-stu-id="deae4-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="deae4-141">(Hugsanlega verður þú að endurhlaða síðuna til að breytingin komi í ljós). Á þeim tímapunkti er kostnaðarbókhaldsþjónustan tilbúin til notkunar.</span><span class="sxs-lookup"><span data-stu-id="deae4-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="deae4-142">Setja upp samþættingu</span><span class="sxs-lookup"><span data-stu-id="deae4-142">Set up the integration</span></span>

<span data-ttu-id="deae4-143">Til að setja upp samþættingu milli kostnaðarbókhaldsþjónustu og Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="deae4-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="deae4-144">Farðu í **Kerfisstjórnun > Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="deae4-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="deae4-145">Veldu **Leita að uppfærslum**.</span><span class="sxs-lookup"><span data-stu-id="deae4-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="deae4-146">Opnaðu flipann **Allt** og leitaðu að eiginleika sem heitir *Kostnaðarbókhaldsþjónusta*.</span><span class="sxs-lookup"><span data-stu-id="deae4-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="deae4-147">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="deae4-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="deae4-148">Farðu í **Kostnaðarstjórnun > Kostnaðarbókhaldsþjónusta > Uppsetning > Þjónustubreytur kostnaðarbókhalds > Samþættingarbreytur**.</span><span class="sxs-lookup"><span data-stu-id="deae4-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="deae4-149">Í **Kenni forrits** skal slá inn eftirfarandi kóða:</span><span class="sxs-lookup"><span data-stu-id="deae4-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="deae4-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="deae4-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="deae4-151">Sláðu inn eftirfarandi vefslóð í svæðið **Endastöð gagnaþjónustu**:</span><span class="sxs-lookup"><span data-stu-id="deae4-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="deae4-152">Sláðu inn eftirfarandi vefslóð í svæðið **Endastöð kostnaðarbókhaldsþjónustu**:</span><span class="sxs-lookup"><span data-stu-id="deae4-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="deae4-153">Kostnaðarbókhaldsþjónustan er nú tilbúin til notkunar.</span><span class="sxs-lookup"><span data-stu-id="deae4-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="deae4-154">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="deae4-154">Related resources</span></span>

[<span data-ttu-id="deae4-155">Heimasíða kostnaðarbókhaldsþjónustu</span><span class="sxs-lookup"><span data-stu-id="deae4-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)

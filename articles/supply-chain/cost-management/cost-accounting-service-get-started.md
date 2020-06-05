---
title: Hafist handa með kostnaðarbókhaldsþjónustu (einkaforskoðun)
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
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 7fec9dc5297ed6e687d4a0dff099922d59d6a830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372737"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="79bce-103">Hafist handa með kostnaðarbókhaldsþjónustu (einkaforskoðun)</span><span class="sxs-lookup"><span data-stu-id="79bce-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="79bce-104">Virkni sem getið er í þessu efnisatriði er tiltæk sem hluti af sérstakri prufuútgáfu.</span><span class="sxs-lookup"><span data-stu-id="79bce-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="79bce-105">Efni þessa efnisatriðis og virknin sem þar er lýst geta breyst.</span><span class="sxs-lookup"><span data-stu-id="79bce-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="79bce-106">Frekari upplýsingar um forútgáfur er að finna í hlutanum [Algengar spurningar um uppfærslureglur fyrir „Ein útgáfa“](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="79bce-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="79bce-107">Kostnaðarbókhaldsþjónusta gerir þér kleift að framkvæma fjöldamörg birgðabókhöld í fjárhagi kostnaðarbókhalds sem þú hefur sett upp.</span><span class="sxs-lookup"><span data-stu-id="79bce-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="79bce-108">Þú tengir hvern fjárhag kostnaðarbókhalds við *reglu*.</span><span class="sxs-lookup"><span data-stu-id="79bce-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="79bce-109">Regla er safn af eftirfarandi gerðum reikningsskilaaðferða:</span><span class="sxs-lookup"><span data-stu-id="79bce-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="79bce-110">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="79bce-110">Cost object</span></span>
- <span data-ttu-id="79bce-111">Grunnmæling inntaks</span><span class="sxs-lookup"><span data-stu-id="79bce-111">Input measurement basis</span></span>
- <span data-ttu-id="79bce-112">Áætlun kostnaðarflæðis</span><span class="sxs-lookup"><span data-stu-id="79bce-112">Cost flow assumption</span></span>
- <span data-ttu-id="79bce-113">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="79bce-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="79bce-114">Jafnvel eftir að þú hefur kveikt á kostnaðarbókhaldsþjónustunni geturðu samt gert birgðabókhald í Microsoft Dynamics 365 Supply Chain Management eins og áður.</span><span class="sxs-lookup"><span data-stu-id="79bce-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="79bce-115">Kostnaðarbókhaldsþjónustan er viðbót.</span><span class="sxs-lookup"><span data-stu-id="79bce-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="79bce-116">Til að gera aðgerðir þess aðgengilegar verður þú að setja hana upp frá Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="79bce-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="79bce-117">Þess vegna getur þú valið að meta það í prufuumhverfi áður en þú setur það í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="79bce-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="79bce-118">Kostnaðarbókhaldsþjónustan styður ekki sem stendur alla þá kostnaðarstjórnunareiginleika sem eru innbyggðir í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79bce-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="79bce-119">Þess vegna er mikilvægt að þú metir hvort grunneiginleikarnir sem nú eru tiltækir uppfylli kröfur þínar.</span><span class="sxs-lookup"><span data-stu-id="79bce-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="79bce-120">Hvernig á að sækja kostnaðarbókhaldsþjónustu (einkaforskoðun)</span><span class="sxs-lookup"><span data-stu-id="79bce-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79bce-121">Til að nota kostnaðarbókhaldsþjónustuna verður þú að vera með LCS-virkt umhverfi með mikið framboð (ekki OneBox umhverfi) og þú verður að keyra útgáfu 10.0.11 af Dynamics 365 Supply Chain Management eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="79bce-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="79bce-122">Til að skrá sig fyrir einkasniðforskoðun kostnaðarbókhalds skulu notendur senda umhverfiskenni LCS í tölvupósti á [Kostnaðarbókhaldsþjónusta (einkaforskoðun)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="79bce-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="79bce-123">Þegar notandi er samþykktur fær hann sendan tölvupóst sem inniheldur beta-lykil fyrir kostnaðarbókhaldsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="79bce-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="79bce-124">Þegar beta-lykllinn er móttekinn er hægt að halda áfram með því að [setja upp innbótina](#install).</span><span class="sxs-lookup"><span data-stu-id="79bce-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="79bce-125">Leyfisveiting</span><span class="sxs-lookup"><span data-stu-id="79bce-125">Licensing</span></span>

<span data-ttu-id="79bce-126">Kostnaðarbókhaldþjónustan er háð leyfi ásamt stöðluðu eiginleikum birgðabókhalds sem eru í boði fyrir Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79bce-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="79bce-127">Þú þarft ekki að kaupa viðbótarleyfi til að nota kostnaðarbókhaldsþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="79bce-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="79bce-128">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="79bce-128">Install the add-in</span></span>

<span data-ttu-id="79bce-129">Til að nota kostnaðarbókhaldsþjónustuna, skaltu setja upp viðbót kostnaðarbókhaldsþjónustu fyrir Supply Chain Management eins og lýst er í eftirfarandi aðferð.</span><span class="sxs-lookup"><span data-stu-id="79bce-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="79bce-130">[Skráning](#sign-up) fyrir kostnaðarbókhaldsþjónustu (einkasforskoðun).</span><span class="sxs-lookup"><span data-stu-id="79bce-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="79bce-131">Skráðu þig inn í LCS.</span><span class="sxs-lookup"><span data-stu-id="79bce-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="79bce-132">Farið í **Stjórnun forskoðunareiginleika**.</span><span class="sxs-lookup"><span data-stu-id="79bce-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="79bce-133">Veldu plústáknið (**+**).</span><span class="sxs-lookup"><span data-stu-id="79bce-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="79bce-134">Sláðu inn beta-lykilinn fyrir viðbót kostnaðarbókhaldsþjónustu á svæðið **Kóði**.</span><span class="sxs-lookup"><span data-stu-id="79bce-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="79bce-135">(Þú hefðir átt að fá lykilinn þinn með tölvupósti.)</span><span class="sxs-lookup"><span data-stu-id="79bce-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="79bce-136">Veldu síðan **Opna fyrir**.</span><span class="sxs-lookup"><span data-stu-id="79bce-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="79bce-137">Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="79bce-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="79bce-138">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="79bce-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="79bce-139">Flettu niður að flýtiflipanum **Umhverfisinnbætur**.</span><span class="sxs-lookup"><span data-stu-id="79bce-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="79bce-140">Veldu **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="79bce-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="79bce-141">Veljið **Kostnaðarbókhaldsþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="79bce-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="79bce-142">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="79bce-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="79bce-143">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="79bce-143">Select **Install**.</span></span>

1. <span data-ttu-id="79bce-144">Í flýtiflipanum **Viðbætur fyrir umhverfi** ættir þú að sjá að kostnaðarbókhaldsþjónustan er sett upp.</span><span class="sxs-lookup"><span data-stu-id="79bce-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="79bce-145">Eftir nokkrar mínútur ætti staðan að breytast úr **Setur upp** í **Uppsett**.</span><span class="sxs-lookup"><span data-stu-id="79bce-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="79bce-146">(Hugsanlega verður þú að endurhlaða síðuna til að breytingin komi í ljós). Á þeim tímapunkti er kostnaðarbókhaldsþjónustan tilbúin til notkunar.</span><span class="sxs-lookup"><span data-stu-id="79bce-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="79bce-147">Setja upp samþættingu</span><span class="sxs-lookup"><span data-stu-id="79bce-147">Set up the integration</span></span>

<span data-ttu-id="79bce-148">Til að setja upp samþættingu milli kostnaðarbókhaldsþjónustu og Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="79bce-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="79bce-149">Farðu í **Kerfisstjórnun > Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="79bce-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="79bce-150">Veldu **Leita að uppfærslum**.</span><span class="sxs-lookup"><span data-stu-id="79bce-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="79bce-151">Opnaðu flipann **Allt** og leitaðu að eiginleika sem heitir *Kostnaðarbókhaldsþjónusta*.</span><span class="sxs-lookup"><span data-stu-id="79bce-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="79bce-152">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="79bce-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="79bce-153">Farðu í **Kostnaðarstjórnun > Kostnaðarbókhaldsþjónusta > Uppsetning > Þjónustubreytur kostnaðarbókhalds > Samþættingarbreytur**.</span><span class="sxs-lookup"><span data-stu-id="79bce-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="79bce-154">Í **Kenni forrits** skal slá inn eftirfarandi kóða:</span><span class="sxs-lookup"><span data-stu-id="79bce-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="79bce-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="79bce-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="79bce-156">Sláðu inn eftirfarandi vefslóð í svæðið **Endastöð gagnaþjónustu**:</span><span class="sxs-lookup"><span data-stu-id="79bce-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="79bce-157">Sláðu inn eftirfarandi vefslóð í svæðið **Endastöð kostnaðarbókhaldsþjónustu**:</span><span class="sxs-lookup"><span data-stu-id="79bce-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="79bce-158">Kostnaðarbókhaldsþjónustan er nú tilbúin til notkunar.</span><span class="sxs-lookup"><span data-stu-id="79bce-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="79bce-159">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="79bce-159">Related resources</span></span>

[<span data-ttu-id="79bce-160">Heimasíða kostnaðarbókhaldsþjónustu</span><span class="sxs-lookup"><span data-stu-id="79bce-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)

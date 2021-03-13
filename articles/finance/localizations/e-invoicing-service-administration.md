---
title: Stjórnunarhlutar viðbótar rafrænnar reikningsfærslu
description: Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á viðbót rafrænnar reikningsfærslu.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104395"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="7336d-103">Stjórnunarhlutar viðbótar rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="7336d-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7336d-104">Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="7336d-105">Þar er einnig að finna upplýsingar um hvernig eigi að skilgreina viðbót rafrænnar reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="7336d-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="7336d-106">Azure</span><span class="sxs-lookup"><span data-stu-id="7336d-106">Azure</span></span>

<span data-ttu-id="7336d-107">Notið Microsoft Azure til að stofna leynilykil fyrir lyklageymslu og geymslureikning.</span><span class="sxs-lookup"><span data-stu-id="7336d-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="7336d-108">Notið síðan leynilyklana í skilgreiningu á viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="7336d-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7336d-109">Lifecycle Services</span></span>

<span data-ttu-id="7336d-110">Notið Microsoft Dynamics Lifecycle Services (LCS) til að virkja viðbótina fyrir microservices fyrir LCS-uppsetningarverkið.</span><span class="sxs-lookup"><span data-stu-id="7336d-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="7336d-111">Í LCS skal velja reitinn **Stjórnun forskoðunareiginleika** og síðan kveikja á eiginleikanum **Þjónusta rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="7336d-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="7336d-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="7336d-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="7336d-113">Dynamics 365 Regulatory Configuration Services (RCS) er viðmótið sem er notað til að skilgreina viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="7336d-114">Tilföng eins og umhverfi og eiginleikar rafrænnar reikningsfærslu eru búin til, unnið með og hýst í RCS.</span><span class="sxs-lookup"><span data-stu-id="7336d-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="7336d-115">Þegar tilföngin eru tilbúin eru þau birt í viðbót rafrænnar reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="7336d-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="7336d-116">Frekari upplýsingar um RCS er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="7336d-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="7336d-117">Samþætting við viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="7336d-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="7336d-118">Áður en hægt er að nota RCS til að skilgreina rafræna reikninga verður að skilgreina RCS til að leyfa samskipti við viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="7336d-119">Þessi skilgreining er kláruð í flipanum **Viðbót rafrænnar reikningsfærslu** á síðunni **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="7336d-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="7336d-120">Endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="7336d-120">Service endpoint</span></span>

<span data-ttu-id="7336d-121">Vefslóð fyrir endastöð viðbótar rafrænnar reikningsfærslu getur verið breytileg eftir staðsetningu Azure-gagnamiðstöðvarinnar.</span><span class="sxs-lookup"><span data-stu-id="7336d-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="7336d-122">Eftirfarandi tafla sýnir tiltækileika eftir svæði:</span><span class="sxs-lookup"><span data-stu-id="7336d-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="7336d-123">Staðsetning Azure-gagnamiðstöðvar</span><span class="sxs-lookup"><span data-stu-id="7336d-123">Azure datacenter geography</span></span> | <span data-ttu-id="7336d-124">ULR endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="7336d-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="7336d-125">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="7336d-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="7336d-126">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="7336d-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="7336d-127">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="7336d-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="7336d-128">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="7336d-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="7336d-129">Kenni umsóknar</span><span class="sxs-lookup"><span data-stu-id="7336d-129">Application ID</span></span>

<span data-ttu-id="7336d-130">Forritsauðkenni er kenni forrits fyrir viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="7336d-131">Í þessu tilfelli er gildið fast: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="7336d-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="7336d-132">Auðkenni LCS-umhverfis</span><span class="sxs-lookup"><span data-stu-id="7336d-132">LCS environment ID</span></span>

<span data-ttu-id="7336d-133">Auðkenni LCS-umhverfis er kenni LCS-áskriftar fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="7336d-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="7336d-134">Þjónustuumhverfi</span><span class="sxs-lookup"><span data-stu-id="7336d-134">Service environments</span></span>

<span data-ttu-id="7336d-135">Þjónustuumhverfi eru rökréttar skiptingar sem eru gerðar til að styðja framkvæmd á eiginleikum rafrænnar reikningsfærslu í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="7336d-136">Öryggislyklar og stafræn vottorð og umsjón (þ.e. aðgangsheimildir) verða að vera skilgreind á öryggisstigi þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="7336d-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="7336d-137">Viðskiptavinir geta búið til eins mörg þjónustuumhverfi og þeir vilja.</span><span class="sxs-lookup"><span data-stu-id="7336d-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="7336d-138">Öll þjónustuumhverfi sem viðskiptavinur býr til eru óháð hvert öðru.</span><span class="sxs-lookup"><span data-stu-id="7336d-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="7336d-139">Þjónustuumhverfi verða að vera búin til og haldið við í RCS.</span><span class="sxs-lookup"><span data-stu-id="7336d-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="7336d-140">Þegar þjónustuumhverfi eru tilbúin þarf að birta þau í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="7336d-141">Staða þjónustuumhverfis</span><span class="sxs-lookup"><span data-stu-id="7336d-141">Service environment status</span></span>

<span data-ttu-id="7336d-142">Hægt er að stjórna þjónustuumhverfum í gegnum stöðuna.</span><span class="sxs-lookup"><span data-stu-id="7336d-142">Service environments can be managed through status.</span></span> <span data-ttu-id="7336d-143">Mögulegir valkostir eru:</span><span class="sxs-lookup"><span data-stu-id="7336d-143">The possible options are:</span></span>

- <span data-ttu-id="7336d-144">**Ekki birt** – Umhverfið hefur verið stofnað, en hefur ekki verið birt.</span><span class="sxs-lookup"><span data-stu-id="7336d-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="7336d-145">**Birt** – Umhverfið hefur verið birt í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="7336d-146">**Breytt** – Eigindum útgefins umhverfis hefur verið breytt, en breytingarnar hafa ekki enn verið gefnar út.</span><span class="sxs-lookup"><span data-stu-id="7336d-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="7336d-147">Leynilyklar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="7336d-147">Customer secrets</span></span>

<span data-ttu-id="7336d-148">Viðbót rafrænnar reikningsfærsluþjónustu ber ábyrgð á því að geyma öll viðskiptagögn í Azure-tilföngum sem fyrirtækið á.</span><span class="sxs-lookup"><span data-stu-id="7336d-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="7336d-149">Til að tryggja að þjónustan virki rétt og að öll viðskiptagögnin sem þarf fyrir og eru búin til af viðbót rafrænnar reikningsfærslu er aðeins opnuð af viðbótinni, þarf að stofna tvö aðaltilföng Azure:</span><span class="sxs-lookup"><span data-stu-id="7336d-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="7336d-150">Azure-geymslureikningur (Blob-geymsla) sem geymir rafræna reikninga</span><span class="sxs-lookup"><span data-stu-id="7336d-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="7336d-151">Azure-lyklageymsla sem geymir vottorð og URI geymslureikningsins</span><span class="sxs-lookup"><span data-stu-id="7336d-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="7336d-152">Úthluta verður tiltekinni lyklageymslu viðskiptavinar sem er sérstaklega notað með viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="7336d-153">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="7336d-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="7336d-154">Notendur</span><span class="sxs-lookup"><span data-stu-id="7336d-154">Users</span></span>

<span data-ttu-id="7336d-155">Hvert þjónustuumhverfi verður að sýna notendurna sem geta tengst frá Dynamics 365 Finance og Dynamics 365 Supply Chain Management í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="7336d-156">Birting</span><span class="sxs-lookup"><span data-stu-id="7336d-156">Publication</span></span>

<span data-ttu-id="7336d-157">Gefa þarf út þjónustuumhverfi í viðbót rafrænnar reikningsfærslu áður en hægt er að nota þau.</span><span class="sxs-lookup"><span data-stu-id="7336d-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="7336d-158">Finance and Supply Chain Management getur aðeins opnað útgefin umhverfi.</span><span class="sxs-lookup"><span data-stu-id="7336d-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="7336d-159">Þar að auki verður að birta þjónustuumhverfi áður en nokkrar uppfærslur á eigindum þess taka gildi í þjónustu rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="7336d-160">Tengd forrit</span><span class="sxs-lookup"><span data-stu-id="7336d-160">Connected applications</span></span>

<span data-ttu-id="7336d-161">Tengd forrit eru tilvik Finance and Supply Chain Management sem þú gætir viljað nálgast í gegnum RCS.</span><span class="sxs-lookup"><span data-stu-id="7336d-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="7336d-162">Fyrir utan vefslóð forritsins og leigjanda þess, inniheldur tengt forrit innskráningarupplýsingar sem gerir RCS kleift að tengjast við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="7336d-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="7336d-163">Í gegnum tengd forrit er hægt að skilgreina hluta af eiginleika rafrænnar reikningsfærslu í Finance and Supply Chain Management til að fá allan eiginleika rafrænnar reikningsfærslu til að virka.</span><span class="sxs-lookup"><span data-stu-id="7336d-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="7336d-164">Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7336d-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="7336d-165">Samþætting við viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="7336d-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="7336d-166">Áður en hægt er að nota Finance and Supply Chain Management til að gefa út rafræna reikninga í gegnum viðbót rafrænnar reikningsfærslu þarf að skilgreina viðbótina til að leyfa samskipti við þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="7336d-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="7336d-167">Samþættingareiginleiki viðbótar rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="7336d-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="7336d-168">Til að virkja samskipti á milli Finance and Supply Chain Management og viðbótar rafrænnar reikningsfærslu þarf að kveikja á eiginleikanum **Samþætting viðbótar rafrænnar reikningsfærslu** á vinnusvæðinu **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7336d-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="7336d-169">Endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="7336d-169">Service endpoint</span></span>

<span data-ttu-id="7336d-170">Endastöð þjónustu er vefslóðin þar sem viðbót rafrænnar reikningsfærslu er staðsett.</span><span class="sxs-lookup"><span data-stu-id="7336d-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="7336d-171">Áður en hægt er að gefa út rafræna reikninga verður að skilgreina endastöð þjónustunnar í Finance and Supply Chain Management til að leyfa samskipti við þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="7336d-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="7336d-172">Til að skilgreina endastöð þjónustunnar skal fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreyta rafræns skjals** og síðan í flipanum **Þjónusta innsendingar**, í reitinn **Vefslóð fyrir viðbót rafrænnar reikningsfærslu**, skal færa inn vefslóðina eins og lýst er í töflunni sem lýst er í hlutanum **Endastöð þjónustu**.</span><span class="sxs-lookup"><span data-stu-id="7336d-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="7336d-173">Umhverfi</span><span class="sxs-lookup"><span data-stu-id="7336d-173">Environments</span></span>

<span data-ttu-id="7336d-174">Heiti umhverfis sem fært er inn í Finance and Supply Chain Management vísar í heitið á umhverfinu sem er búið til í RCS og birt í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7336d-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="7336d-175">Skilgreina þarf umhverfið í flipanum **Þjónustur innsendingar** á síðunni **Færibreyta rafræns skjals** þannig að allar beiðnir um að gefa út rafræna reikninga innihaldi umhverfið þar sem viðbót rafrænnar reikningsfærslu getur ákvarðað hvaða eiginleiki rafrænnar reikningsfærslu verður að vinna úr beiðninni.</span><span class="sxs-lookup"><span data-stu-id="7336d-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7336d-176">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7336d-176">Additional resources</span></span>

- [<span data-ttu-id="7336d-177">Skilgreina rafræna reikninga í RCS</span><span class="sxs-lookup"><span data-stu-id="7336d-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="7336d-178">Gefa út rafræna reikninga í Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7336d-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)

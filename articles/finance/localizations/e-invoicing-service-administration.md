---
title: Stjórnunarhlutar viðbótar rafrænnar reikningsfærslu
description: Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á viðbót rafrænnar reikningsfærslu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592575"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="d37bf-103">Stjórnunarhlutar viðbótar rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="d37bf-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d37bf-104">Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="d37bf-105">Þar er einnig að finna upplýsingar um hvernig eigi að skilgreina viðbót rafrænnar reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="d37bf-106">Azure</span><span class="sxs-lookup"><span data-stu-id="d37bf-106">Azure</span></span>

<span data-ttu-id="d37bf-107">Notið Microsoft Azure til að stofna leynilykil fyrir lyklageymslu og geymslureikning.</span><span class="sxs-lookup"><span data-stu-id="d37bf-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="d37bf-108">Notið síðan leynilyklana í skilgreiningu á viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="d37bf-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d37bf-109">Lifecycle Services</span></span>

<span data-ttu-id="d37bf-110">Notið Microsoft Dynamics Lifecycle Services (LCS) til að virkja viðbótina fyrir microservices fyrir LCS-uppsetningarverkið.</span><span class="sxs-lookup"><span data-stu-id="d37bf-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="d37bf-111">Uppsetning örþjónustuviðbóta í LCS krefst að minnsta kosti Tier 2 sýndarvélar.</span><span class="sxs-lookup"><span data-stu-id="d37bf-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="d37bf-112">Nánari upplýsingar um umhverfisskipulag er að finna í [Umhverfisskipulag](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="d37bf-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="d37bf-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="d37bf-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="d37bf-114">Dynamics 365 Regulatory Configuration Services (RCS) er viðmótið sem er notað til að skilgreina viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="d37bf-115">Tilföng eins og umhverfi og eiginleikar rafrænnar reikningsfærslu eru búin til, unnið með og hýst í RCS.</span><span class="sxs-lookup"><span data-stu-id="d37bf-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="d37bf-116">Þegar tilföngin eru tilbúin eru þau birt í viðbót rafrænnar reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="d37bf-117">Fyrir RCS-innskráningu, sjá [Regulatory Services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="d37bf-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="d37bf-118">Frekari upplýsingar um RCS er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="d37bf-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="d37bf-119">Samþætting við viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="d37bf-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="d37bf-120">Áður en hægt er að nota RCS til að skilgreina rafræna reikninga verður að skilgreina RCS til að leyfa samskipti við viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="d37bf-121">Þessi skilgreining er kláruð í flipanum **Viðbót rafrænnar reikningsfærslu** á síðunni **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="d37bf-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="d37bf-122">Endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="d37bf-122">Service endpoint</span></span>

<span data-ttu-id="d37bf-123">Rafræna reikningsfærsluviðbótin er tiltæk í nokkrum Azure Datacenter löndum.</span><span class="sxs-lookup"><span data-stu-id="d37bf-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="d37bf-124">Eftirfarandi tafla sýnir framboði eftir svæði.</span><span class="sxs-lookup"><span data-stu-id="d37bf-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="d37bf-125">Staðsetning Azure-gagnamiðstöðvar</span><span class="sxs-lookup"><span data-stu-id="d37bf-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="d37bf-126">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="d37bf-126">East US</span></span>                    |
| <span data-ttu-id="d37bf-127">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="d37bf-127">West US</span></span>                    |
| <span data-ttu-id="d37bf-128">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="d37bf-128">North EU</span></span>                   |
| <span data-ttu-id="d37bf-129">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="d37bf-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="d37bf-130">Þjónustuumhverfi</span><span class="sxs-lookup"><span data-stu-id="d37bf-130">Service environments</span></span>

<span data-ttu-id="d37bf-131">Þjónustuumhverfi eru rökréttar skiptingar sem eru gerðar til að styðja framkvæmd á eiginleikum rafrænnar reikningsfærslu í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="d37bf-132">Öryggislyklar og stafræn vottorð og umsjón (þ.e. aðgangsheimildir) verða að vera skilgreind á öryggisstigi þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="d37bf-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="d37bf-133">Viðskiptavinir geta búið til eins mörg þjónustuumhverfi og þeir vilja.</span><span class="sxs-lookup"><span data-stu-id="d37bf-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="d37bf-134">Öll þjónustuumhverfi sem viðskiptavinur býr til eru óháð hvert öðru.</span><span class="sxs-lookup"><span data-stu-id="d37bf-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="d37bf-135">Þjónustuumhverfi verða að vera búin til og haldið við í RCS.</span><span class="sxs-lookup"><span data-stu-id="d37bf-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="d37bf-136">Þegar þjónustuumhverfi eru tilbúin þarf að birta þau í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="d37bf-137">Staða þjónustuumhverfis</span><span class="sxs-lookup"><span data-stu-id="d37bf-137">Service environment status</span></span>

<span data-ttu-id="d37bf-138">Hægt er að stjórna þjónustuumhverfum í gegnum stöðuna.</span><span class="sxs-lookup"><span data-stu-id="d37bf-138">Service environments can be managed through status.</span></span> <span data-ttu-id="d37bf-139">Mögulegir valkostir eru:</span><span class="sxs-lookup"><span data-stu-id="d37bf-139">The possible options are:</span></span>

- <span data-ttu-id="d37bf-140">**Ekki birt** – Umhverfið hefur verið stofnað, en hefur ekki verið birt.</span><span class="sxs-lookup"><span data-stu-id="d37bf-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="d37bf-141">**Birt** – Umhverfið hefur verið birt í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="d37bf-142">**Breytt** – Eigindum útgefins umhverfis hefur verið breytt, en breytingarnar hafa ekki enn verið gefnar út.</span><span class="sxs-lookup"><span data-stu-id="d37bf-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="d37bf-143">Leynilyklar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="d37bf-143">Customer secrets</span></span>

<span data-ttu-id="d37bf-144">Viðbót rafrænnar reikningsfærsluþjónustu ber ábyrgð á því að geyma öll viðskiptagögn í Azure-tilföngum sem fyrirtækið á.</span><span class="sxs-lookup"><span data-stu-id="d37bf-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="d37bf-145">Til að tryggja að þjónustan virki rétt og að öll viðskiptagögnin sem þarf fyrir og eru búin til af viðbót rafrænnar reikningsfærslu er aðeins opnuð af viðbótinni, þarf að stofna tvö aðaltilföng Azure:</span><span class="sxs-lookup"><span data-stu-id="d37bf-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="d37bf-146">Azure-geymslureikningur (Blob-geymsla) sem geymir rafræna reikninga</span><span class="sxs-lookup"><span data-stu-id="d37bf-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="d37bf-147">Azure-lyklageymsla sem geymir vottorð og URI geymslureikningsins</span><span class="sxs-lookup"><span data-stu-id="d37bf-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="d37bf-148">Úthluta verður tiltekinni lyklageymslu viðskiptavinar sem er sérstaklega notað með viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="d37bf-149">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="d37bf-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="d37bf-150">Notendur</span><span class="sxs-lookup"><span data-stu-id="d37bf-150">Users</span></span>

<span data-ttu-id="d37bf-151">Hvert þjónustuumhverfi verður að sýna notendurna sem geta tengst frá Dynamics 365 Finance og Dynamics 365 Supply Chain Management í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="d37bf-152">Birting</span><span class="sxs-lookup"><span data-stu-id="d37bf-152">Publication</span></span>

<span data-ttu-id="d37bf-153">Gefa þarf út þjónustuumhverfi í viðbót rafrænnar reikningsfærslu áður en hægt er að nota þau.</span><span class="sxs-lookup"><span data-stu-id="d37bf-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="d37bf-154">Finance and Supply Chain Management getur aðeins opnað útgefin umhverfi.</span><span class="sxs-lookup"><span data-stu-id="d37bf-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="d37bf-155">Þar að auki verður að birta þjónustuumhverfi áður en nokkrar uppfærslur á eigindum þess taka gildi í þjónustu rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="d37bf-156">Tengd forrit</span><span class="sxs-lookup"><span data-stu-id="d37bf-156">Connected applications</span></span>

<span data-ttu-id="d37bf-157">Tengd forrit eru tilvik Finance and Supply Chain Management sem þú gætir viljað nálgast í gegnum RCS.</span><span class="sxs-lookup"><span data-stu-id="d37bf-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="d37bf-158">Fyrir utan vefslóð forritsins og leigjanda þess, inniheldur tengt forrit innskráningarupplýsingar sem gerir RCS kleift að tengjast við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="d37bf-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="d37bf-159">Í gegnum tengd forrit er hægt að skilgreina hluta af eiginleika rafrænnar reikningsfærslu í Finance and Supply Chain Management til að fá allan eiginleika rafrænnar reikningsfærslu til að virka.</span><span class="sxs-lookup"><span data-stu-id="d37bf-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="d37bf-160">Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d37bf-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="d37bf-161">Samþætting við viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="d37bf-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="d37bf-162">Áður en hægt er að nota Finance and Supply Chain Management til að gefa út rafræna reikninga í gegnum viðbót rafrænnar reikningsfærslu þarf að skilgreina viðbótina til að leyfa samskipti við þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="d37bf-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="d37bf-163">Samþættingareiginleiki viðbótar rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="d37bf-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="d37bf-164">Til að virkja samskipti á milli Finance and Supply Chain Management og viðbótar rafrænnar reikningsfærslu þarf að kveikja á eiginleikanum **Samþætting viðbótar rafrænnar reikningsfærslu** á vinnusvæðinu **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="d37bf-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="d37bf-165">Endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="d37bf-165">Service endpoint</span></span>

<span data-ttu-id="d37bf-166">Endastöð þjónustu er vefslóðin þar sem viðbót rafrænnar reikningsfærslu er staðsett.</span><span class="sxs-lookup"><span data-stu-id="d37bf-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="d37bf-167">Áður en hægt er að gefa út rafræna reikninga verður að skilgreina endastöð þjónustunnar í Finance and Supply Chain Management til að leyfa samskipti við þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="d37bf-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="d37bf-168">Til að skilgreina endastöð þjónustunnar skal fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreyta rafræns skjals** og síðan í flipanum **Þjónusta innsendingar**, í reitinn **Vefslóð fyrir viðbót rafrænnar reikningsfærslu**, skal færa inn vefslóðina eins og lýst er í töflunni sem lýst er í hlutanum **Endastöð þjónustu**.</span><span class="sxs-lookup"><span data-stu-id="d37bf-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="d37bf-169">Umhverfi</span><span class="sxs-lookup"><span data-stu-id="d37bf-169">Environments</span></span>

<span data-ttu-id="d37bf-170">Heiti umhverfis sem fært er inn í Finance and Supply Chain Management vísar í heitið á umhverfinu sem er búið til í RCS og birt í viðbót rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d37bf-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="d37bf-171">Skilgreina þarf umhverfið í flipanum **Þjónustur innsendingar** á síðunni **Færibreyta rafræns skjals** þannig að allar beiðnir um að gefa út rafræna reikninga innihaldi umhverfið þar sem viðbót rafrænnar reikningsfærslu getur ákvarðað hvaða eiginleiki rafrænnar reikningsfærslu verður að vinna úr beiðninni.</span><span class="sxs-lookup"><span data-stu-id="d37bf-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d37bf-172">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d37bf-172">Additional resources</span></span>

- [<span data-ttu-id="d37bf-173">Skilgreina rafræna reikninga í RCS</span><span class="sxs-lookup"><span data-stu-id="d37bf-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="d37bf-174">Gefa út rafræna reikninga í Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d37bf-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

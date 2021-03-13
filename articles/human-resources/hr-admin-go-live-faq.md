---
title: Algengar spurningar um keyrslu
description: Í þessu efnisatriði eru algengar spurningar um hvernig á að keyra Dynamics 365 Human Resources innleiðingarverk.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
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
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5041d515b261bb3e4b14885e0ec0ce788edf729
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112947"
---
# <a name="go-live-faq"></a><span data-ttu-id="488d7-103">Algengar spurningar um keyrslu</span><span class="sxs-lookup"><span data-stu-id="488d7-103">Go-live FAQ</span></span> 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="488d7-104">Í þessu efnisatriði eru algengar spurningar um hvernig á að keyra Dynamics 365 Human Resources innleiðingarverk.</span><span class="sxs-lookup"><span data-stu-id="488d7-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="488d7-105">Hvenær get ég skilgreint og beðið um vinnsluumhverfið mitt?</span><span class="sxs-lookup"><span data-stu-id="488d7-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="488d7-106">Yfirleitt er vinnsluumhverfi virkjað eftir að eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="488d7-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="488d7-107">Allar sérstillingar hafa verið kóðaðar.</span><span class="sxs-lookup"><span data-stu-id="488d7-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="488d7-108">Samþykkisprófun notanda er lokið.</span><span class="sxs-lookup"><span data-stu-id="488d7-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="488d7-109">Viðskiptavinurinn hefur samþykkt lausnina.</span><span class="sxs-lookup"><span data-stu-id="488d7-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="488d7-110">Ekkert stendur í vegi fyrir keyrslu.</span><span class="sxs-lookup"><span data-stu-id="488d7-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="488d7-111">Þegar hæfir viðskiptavinir eru á þessu stigi mun Microsoft FastTrack-teymið vinna með verkefnateyminu að gerð keyrslumats.</span><span class="sxs-lookup"><span data-stu-id="488d7-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="488d7-112">Hver eru skilyrðin fyrir virkjun vinnsluumhverfis?</span><span class="sxs-lookup"><span data-stu-id="488d7-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="488d7-113">Fyrir lista yfir forkröfur skal skoða  [Undirbúa keyrslu](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="488d7-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="488d7-114">Hvað er keyrslumat?</span><span class="sxs-lookup"><span data-stu-id="488d7-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="488d7-115">Keyrslumatið er hluti af  [Microsoft FastTrack-áætluninni](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span><span class="sxs-lookup"><span data-stu-id="488d7-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="488d7-116">Við þessa yfirferð leggur úrlausnarhönnuður mat á hvort innleiðingarverk sé tilbúið fyrir flutning og keyrslu.</span><span class="sxs-lookup"><span data-stu-id="488d7-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="488d7-117">Þessi yfirferð er áskilin fyrir hvert innleiðingarverk áður en hægt er að óska eftir því að keyra vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="488d7-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="488d7-118">Sandkassaumhverfin okkar eru virkjuð í gagnamiðstöð í miðríkjum Bandaríkjanna.</span><span class="sxs-lookup"><span data-stu-id="488d7-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="488d7-119">Við viljum að vinnsluumhverfi okkar séu virkjuð í gagnamiðstöð í vesturríkjum Bandaríkjanna.</span><span class="sxs-lookup"><span data-stu-id="488d7-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="488d7-120">Get ég valið vesturríki Bandaríkjanna sem gagnamiðstöð í vinnsluskilgreiningunni minni?</span><span class="sxs-lookup"><span data-stu-id="488d7-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="488d7-121">LCS hindrar þig ekki í að velja aðra gagnamiðstöð þegar Human Resources-umhverfi er sett upp, en við mælum eindregið með því að velja ekki aðra gagnamiðstöð.</span><span class="sxs-lookup"><span data-stu-id="488d7-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="488d7-122">Ef þú vilt að vinnsluumhverfið þitt sé í gagnamiðstöð í vesturríkjum Bandaríkjanna ættirðu fyrst að endurvirkja sandkassaumhverfi þín í gagnamiðstöð í vesturríkjum Bandaríkjanna, prófa þau og samþykkja.</span><span class="sxs-lookup"><span data-stu-id="488d7-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="488d7-123">Frekari upplýsingar um val á réttri gagnamiðstöð er að finna í [Netkröfur](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="488d7-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="488d7-124">Hvaða aðgangsstig er ég með í Azure-tilföngum fyrir Human Resources-umhverfið mitt?</span><span class="sxs-lookup"><span data-stu-id="488d7-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="488d7-125">Aðgangur að umhverfi Human Resources er háður takmörkunum.</span><span class="sxs-lookup"><span data-stu-id="488d7-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="488d7-126">Ekki er hægt að fá aðgang að sýndarvél eða Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="488d7-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="488d7-127">Einnig er ekki hægt að opna gagnagrunninn í gegnum Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="488d7-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="488d7-128">Þótt þú getir ekki fengið beinan aðgang að Azure-tilföngum eða Dynamics 365 Human Resources-umhverfinu, eru til fleiri eiginleikar sem þú getur notað til að fá aðgang að gögnunum þínum:</span><span class="sxs-lookup"><span data-stu-id="488d7-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="488d7-129">Hægt er að setja upp Azure SQL-gagnagrunn í eigin Azure-leigjanda og eiginleikann BYOD-gagnagrunnur til að samstilla gögn.</span><span class="sxs-lookup"><span data-stu-id="488d7-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="488d7-130">Frekari upplýsingar er að finna í [Koma með eigin gagnagrunn (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="488d7-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="488d7-131">Hægt er að nota Dataverse-samþættingu til að samstilla valdar einingar við Dataverse-gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="488d7-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="488d7-132">Frekari upplýsingar eru í [Dataverse töflur](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="488d7-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="488d7-133">Hversu oft er verið að afrita vinnslugrunninn minn?</span><span class="sxs-lookup"><span data-stu-id="488d7-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="488d7-134">Gagnagrunnar eru varðir með sjálfvirkum öryggisafritunum með eftirfarandi millibili:</span><span class="sxs-lookup"><span data-stu-id="488d7-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="488d7-135">Gerð öryggisafritunar</span><span class="sxs-lookup"><span data-stu-id="488d7-135">Type of backup</span></span> | <span data-ttu-id="488d7-136">Tíðni</span><span class="sxs-lookup"><span data-stu-id="488d7-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="488d7-137">Heildarafritun gagnagrunns</span><span class="sxs-lookup"><span data-stu-id="488d7-137">Full database backup</span></span> | <span data-ttu-id="488d7-138">Vikulega</span><span class="sxs-lookup"><span data-stu-id="488d7-138">Weekly</span></span> |
| <span data-ttu-id="488d7-139">Milliafritun gagnagrunns</span><span class="sxs-lookup"><span data-stu-id="488d7-139">Differential database backup</span></span> | <span data-ttu-id="488d7-140">Á 12-24 klukkustunda fresti</span><span class="sxs-lookup"><span data-stu-id="488d7-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="488d7-141">Öryggisafritun færslukladda</span><span class="sxs-lookup"><span data-stu-id="488d7-141">Transaction log backup</span></span> | <span data-ttu-id="488d7-142">Á 5 til 10 mínútna fresti</span><span class="sxs-lookup"><span data-stu-id="488d7-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="488d7-143">Microsoft heldur eftir nægum öryggisafritunum til að geta endurheimt tímapunkt innan síðustu 14 daga.</span><span class="sxs-lookup"><span data-stu-id="488d7-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="488d7-144">Frekari upplýsingar er að finna í  [Fræðast um sjálfvirka öryggisafritun SQL-gagnagrunns](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="488d7-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="488d7-145">Get ég óskað eftir afriti af öryggisafritun vinnslugrunnsins míns?</span><span class="sxs-lookup"><span data-stu-id="488d7-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="488d7-146">Nei.</span><span class="sxs-lookup"><span data-stu-id="488d7-146">No.</span></span> <span data-ttu-id="488d7-147">Hinsvegar er hægt að senda inn þjónustubeiðni um gagnagrunnsuppfærslu til að afrita vinnsluumhverfið þitt í sandkassaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="488d7-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="488d7-148">Hægt er að setja upp Azure SQL-gagnagrunn í eigin Azure-leigjanda og nota BYOD-gagnagrunnseiginleikann til að samstilla gögn úr vinnsluumhverfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="488d7-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="488d7-149">Frekari upplýsingar er að finna í [Koma með eigin gagnagrunn (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="488d7-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="488d7-150">Hvernig flyt ég sandkasssumhverfið mitt í vinnslu fyrir keyrslu?</span><span class="sxs-lookup"><span data-stu-id="488d7-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="488d7-151">Vegna þess að afritunareiginleiki er ekki í boði til að flytja umhverfið þitt úr sandkassa í vinnsluumhverfi, verður þú að nota gagnapakka til að flytja gögn í vinnsluumhverfið þitt.</span><span class="sxs-lookup"><span data-stu-id="488d7-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="488d7-152">Við mælum með því að halda utan um skýran lista yfir einingar sem eru skilgreindar í sandkassanum þínu í gegnum verkið.</span><span class="sxs-lookup"><span data-stu-id="488d7-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="488d7-153">Prófaðu síðan flutningsferlið á einhverjum gagnapakka sem þarf fyrir keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="488d7-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="488d7-154">Þú verður að færa gagnapakka handvirkt inn í vinnsluumhverfið þegar þú ert tilbúin(n) fyrir keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="488d7-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="488d7-155">Hvað á ég að taka til bragðs ef vinnsluumhverfið mitt er niðri?</span><span class="sxs-lookup"><span data-stu-id="488d7-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="488d7-156">Til að tilkynna stöðvun á vinnslu skal fylgja ferlinu sem lýst er í  [Tilkynna framleiðslustöðvun](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span><span class="sxs-lookup"><span data-stu-id="488d7-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="488d7-157">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="488d7-157">See also</span></span>

 [<span data-ttu-id="488d7-158">Undirbúa keyrslu</span><span class="sxs-lookup"><span data-stu-id="488d7-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)

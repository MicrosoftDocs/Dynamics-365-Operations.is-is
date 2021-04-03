---
title: Uppfærsluferli
description: Microsoft Dynamics 365 Human Resources er sannur hugbúnaður sem þjónusta (SaaS) sem veitir stöðugar, snertilausar þjónustuuppfærslur fyrir breytingar á forriti og verkvangi.
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27561bfd9cb4f115cc507954c837ea93f9c93b72
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466833"
---
# <a name="update-process"></a><span data-ttu-id="6cd82-103">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="6cd82-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6cd82-104">Microsoft Dynamics 365 Human Resources er sannur hugbúnaður sem þjónusta (SaaS) sem veitir stöðugar, snertilausar þjónustuuppfærslur.</span><span class="sxs-lookup"><span data-stu-id="6cd82-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="6cd82-105">Þessar uppfærslur innihalda bæði forrits- og vettvangsbreytingar sem oft veita mikilvægar endurbætur á þjónustunni, þ.mt uppfærslur á reglugerðum.</span><span class="sxs-lookup"><span data-stu-id="6cd82-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="6cd82-106">Uppfæra stefnu</span><span class="sxs-lookup"><span data-stu-id="6cd82-106">Update policy</span></span>

<span data-ttu-id="6cd82-107">Uppfærslur eru gefnar út með reglubundnum hætti fyrir öll umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6cd82-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="6cd82-108">Human Resources er stutt samkvæmt [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) sem býður upp á stöðugar og einfaldar leiðbeiningar fyrir tiltækileika stuðnings við vöru.</span><span class="sxs-lookup"><span data-stu-id="6cd82-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="6cd82-109">Losunartaktur</span><span class="sxs-lookup"><span data-stu-id="6cd82-109">Release cadence</span></span> 

<span data-ttu-id="6cd82-110">Uppfærslum á Human Resources er beitt sjálfkrafa í öll umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6cd82-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="6cd82-111">Human Resources veitir tvenns konar útgáfur:</span><span class="sxs-lookup"><span data-stu-id="6cd82-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="6cd82-112">**Þjónustuuppfærslur**: Uppfærslur verða á tveggja vinkna fresti sem innihalda villuleiðréttingar og nýja eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6cd82-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="6cd82-113">Þjónustuuppfærslur innihalda einnig viðeigandi uppfærslur á palli þegar þær eru gefnar út.</span><span class="sxs-lookup"><span data-stu-id="6cd82-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="6cd82-114">Sjá til að fá hugmynd um hvenær uppfærslur á verkvangi eru gefnar út [Tafla 3: Verkvangsútgáfur](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="6cd82-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="6cd82-115">Uppfærslur á tveggja vikna fresti eru settar á svið alþjóðlegt útbreiðsla milli svæða.</span><span class="sxs-lookup"><span data-stu-id="6cd82-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="6cd82-116">Nánari upplýsingar um uppfærslur á tveggja vikna fresti eru í [Hvað er nýtt eða breytt í Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="6cd82-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="6cd82-117">Öll studd gagnaver uppfæra á tveggja vikna fresti nema annað sé tekið fram.</span><span class="sxs-lookup"><span data-stu-id="6cd82-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="6cd82-118">Bandaríkin, Ástralía, Evrópa, Bretland, Asía og Kanada eru með í uppfærslum á tveggja vikna fresti.</span><span class="sxs-lookup"><span data-stu-id="6cd82-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="6cd82-119">**Dataverse lausnir uppfærslur**: Þessar uppfærslur eiga sér stað um það bil á sex vikna fresti eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="6cd82-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="6cd82-120">Þau fela í sér nýja aðila og breytingar á núverandi aðilum í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6cd82-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="6cd82-121">Þessar uppfærslur koma út á sömu svæðum og uppfærslur á tveggja vikna fresti og það tekur um sex vikur að endurtaka í gegnum öll gagnaver.</span><span class="sxs-lookup"><span data-stu-id="6cd82-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="6cd82-122">Lausn uppfærslna kann eða er ekki í samræmi við þjónustuuppfærslur á tveggja vikna fresti.</span><span class="sxs-lookup"><span data-stu-id="6cd82-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="6cd82-123">Lausnaruppfærslur eru fáanlegar á öllum gagnaverum þegar þeim er sleppt.</span><span class="sxs-lookup"><span data-stu-id="6cd82-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="6cd82-124">Ef þú vilt ekki bíða eftir að uppfærslurnar endurtaki sig sjálfkrafa geturðu beitt þessum uppfærslum handvirkt á hvaða umhverfi sem er í hvaða gagnaveri sem er.</span><span class="sxs-lookup"><span data-stu-id="6cd82-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="6cd82-125">Þegar þörf er á veitir Human Resources einnig eftirfarandi gerðir af lagfæringum:</span><span class="sxs-lookup"><span data-stu-id="6cd82-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="6cd82-126">**Endurskoðun (leiðrétting)**: villuleiðréttingar sem geta komið fram annaðhvort með eða fyrir utan þjónustuuppfærslu á tveggja vikna fresti</span><span class="sxs-lookup"><span data-stu-id="6cd82-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="6cd82-127">**Neyðarúrræði**: Fyrirbyggjandi og viðbragðsbráðabirgafærslur sem eru sjálfstætt í eðli sínu, geta innihaldið eingöngu stillingar eða kóðabreytingar til að leysa vandamál á vefnum og geta komið fyrir utan útgáfu þjónustuuppfærslu á tveggja vikna fresti</span><span class="sxs-lookup"><span data-stu-id="6cd82-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="6cd82-128">Útgáfur eru skoðaðar, prófaðar og staðfestar í innra umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6cd82-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="6cd82-129">Eftir að búið er að slökkva á smíðum er þeim síðan sent til framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="6cd82-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="6cd82-130">Undantekningar á útgáfutíðni árið 2020</span><span class="sxs-lookup"><span data-stu-id="6cd82-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="6cd82-131">Til að taka með frídaga er úttektaráætlun fyrir nóvember og desember 2020 sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="6cd82-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="6cd82-132">Nóvemberútgáfa: 2. nóvember til 13. nóvember</span><span class="sxs-lookup"><span data-stu-id="6cd82-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="6cd82-133">Desemberútgáfa: 30. nóvember til 11. desember</span><span class="sxs-lookup"><span data-stu-id="6cd82-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="6cd82-134">Tveggja vikna útgáfa mun halda áfram eins og venjulega þann 11. janúar 2021.</span><span class="sxs-lookup"><span data-stu-id="6cd82-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="6cd82-135">Samskipti</span><span class="sxs-lookup"><span data-stu-id="6cd82-135">Communications</span></span>

<span data-ttu-id="6cd82-136">Þú getur fundið út hvað er í verkunum fyrir Human Resources og hvað við höfum sent frá okkur á eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="6cd82-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="6cd82-137">Dynamics 365 Human Resources leiðarvísir</span><span class="sxs-lookup"><span data-stu-id="6cd82-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="6cd82-138">Útgáfuáætlanir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6cd82-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="6cd82-139">Nýjungar eða breytingar í Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="6cd82-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="6cd82-140">[Vandamálaleit í Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (aðeins fyrir villur sem tengjast verkvangi)</span><span class="sxs-lookup"><span data-stu-id="6cd82-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="6cd82-141">Human Resources-bloggið</span><span class="sxs-lookup"><span data-stu-id="6cd82-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="6cd82-142">Human Resources Yammer samfélag</span><span class="sxs-lookup"><span data-stu-id="6cd82-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="6cd82-143">Forskoðaðu aðgerðir í sandkassaumhverfi</span><span class="sxs-lookup"><span data-stu-id="6cd82-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="6cd82-144">Þú getur sannreynt forsýningaraðgerðir í sandkassaumhverfi áður en þú virkjar þá í framleiðsluumhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="6cd82-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="6cd82-145">Nánari upplýsingar um virkjun eiginleika er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="6cd82-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="6cd82-146">Allar nýju aðgerðirnar eru áfram í forskoðun í að minnsta kosti 30 daga og venjulega 30-60 daga.</span><span class="sxs-lookup"><span data-stu-id="6cd82-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="6cd82-147">Helstu eiginleikar eru venjulega fáanlegir í október og apríl ár hvert í kjölfar forskoðunartímabilsins.</span><span class="sxs-lookup"><span data-stu-id="6cd82-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="6cd82-148">Um leið og þú sérð nýja möguleika í vinnusvæðinu Stjórnun eiginleika er hægt að kveikja á þeim.</span><span class="sxs-lookup"><span data-stu-id="6cd82-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="6cd82-149">Sumar aðgerðir kunna að vera sjálfkrafa á.</span><span class="sxs-lookup"><span data-stu-id="6cd82-149">Some features may be on by default.</span></span>

<span data-ttu-id="6cd82-150">Stundum er sambyggður eiginleiki virkur og ekki er hægt að slökkva á honum (til dæmis vinnusvæðinu Stjórnun eiginleika).</span><span class="sxs-lookup"><span data-stu-id="6cd82-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="6cd82-151">Þegar eiginleiki er almennt tiltækur kann að vera kveikt eða slökkt á honum í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="6cd82-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="6cd82-152">Vinnusvæðið Stjórnun eiginleika gefur til kynna hvenær forsýningareiginleiki verður nauðsynlegur.</span><span class="sxs-lookup"><span data-stu-id="6cd82-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="6cd82-153">Þessi dagsetning er venjulega 1. október eða 1. apríl til að samræma hálfsársáætlun um losun.</span><span class="sxs-lookup"><span data-stu-id="6cd82-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="6cd82-154">Ekki er hægt að slökkva á skyldueiginleikum.</span><span class="sxs-lookup"><span data-stu-id="6cd82-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="6cd82-155">Þar til það verður skylda geturðu kveikt og slökkt á eiginleikum í öllu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6cd82-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="6cd82-156">Við mælum mjög með því að forskoða aðgerðir í sandkassa eða prufuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="6cd82-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="6cd82-157">Best er að búa til afrit af núverandi framleiðsluumhverfi eða gagnagrunni í sandkassaumhverfi svo að þú getir fengið fullkomna reynslu af nýju aðgerðunum með gögnunum þínum.</span><span class="sxs-lookup"><span data-stu-id="6cd82-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="6cd82-158">Nánari upplýsingar um vistun á sandkassaumhverfi, sjá [Veita verk Human Resources](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="6cd82-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="6cd82-159">Sjá til að fjarlægja prófunarumhverfi [Fjarlægja tilvik](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="6cd82-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="6cd82-160">Tilkynntu villur</span><span class="sxs-lookup"><span data-stu-id="6cd82-160">Report bugs</span></span>

<span data-ttu-id="6cd82-161">Þó að prófa forskoðunareiginleika eða prófa nýja möguleika gætirðu fundið hluti sem virka ekki eins og búist var við.</span><span class="sxs-lookup"><span data-stu-id="6cd82-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="6cd82-162">Vinsamlegast tilkynnið allar villur í gegnum [Microsoft Dynamics 365 stuðning](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="6cd82-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="6cd82-163">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6cd82-163">See also</span></span>

[<span data-ttu-id="6cd82-164">Útgáfuáætlanir Dynamics 365 og Power Platform</span><span class="sxs-lookup"><span data-stu-id="6cd82-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="6cd82-165">Nýjungar eða breytingar í Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="6cd82-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="6cd82-166">Reglur um stuðningstíma hugbúnaðar</span><span class="sxs-lookup"><span data-stu-id="6cd82-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Afritið tilvik
description: Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi.
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40ca0a4d9733fc2a163daa4ea1c27a3bfae6d3bf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527838"
---
# <a name="copy-an-instance"></a><span data-ttu-id="1a36b-103">Afritið tilvik</span><span class="sxs-lookup"><span data-stu-id="1a36b-103">Copy an instance</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1a36b-104">Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="1a36b-105">Ef þú ert með annað sandkassaumhverfi geturðu einnig afritað gagnagrunninn úr því umhverfi yfir í markviss sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="1a36b-106">Til að afrita tilvik skal hafa eftirfarandi í huga:</span><span class="sxs-lookup"><span data-stu-id="1a36b-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="1a36b-107">Tilvik Human Resources sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="1a36b-108">Umhverfið sem þú ert að afrita af og til verður að vera á sama svæði.</span><span class="sxs-lookup"><span data-stu-id="1a36b-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="1a36b-109">Þú getur ekki afritað á milli svæða.</span><span class="sxs-lookup"><span data-stu-id="1a36b-109">You can't copy across regions.</span></span>

- <span data-ttu-id="1a36b-110">Þú verður að vera stjórnandi í markumhverfinu svo þú getir skráð þig inn á það eftir að hafa afritað tilvikið.</span><span class="sxs-lookup"><span data-stu-id="1a36b-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="1a36b-111">Þegar þú afritar gagnagrunn Human Resources, afritar þú ekki þá þætti (forrit eða gögn) sem eru í Microsoft Power Apps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="1a36b-112">Fyrir upplýsingar um hvernig á að afrita þætti í Power Apps-umhverfi, sjá [Afrita umhverfi](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="1a36b-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="1a36b-113">Power Apps-umhverfið sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="1a36b-114">Þú verður að vera alþjóðlegur leigjandi stjórnandi til að breyta Power Apps-framleiðsluumhverfi í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="1a36b-115">Fyrir frekari upplýsingar um að breyta Power Apps-umhverfi, sjáðu [Skiptu um dæmi](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="1a36b-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="1a36b-116">Ef tilvik er afritað inn í sandkassaumhverfi og ætlunin er að samþætta sandkassaumhverfið við Common Data Service þarf að endurnota sérstillta reiti í Common Data Service einingarnar.</span><span class="sxs-lookup"><span data-stu-id="1a36b-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span> <span data-ttu-id="1a36b-117">Sjá [Nota sérstillta reiti á Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="1a36b-117">See [Apply custom fields to Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="1a36b-118">Áhrif afritunar gagnagrunns Human Resources</span><span class="sxs-lookup"><span data-stu-id="1a36b-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="1a36b-119">Eftirfarandi atburðir eiga sér stað þegar þú afritar gagnagrunn Human Resources:</span><span class="sxs-lookup"><span data-stu-id="1a36b-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="1a36b-120">Afritunarferlið eyðir núverandi gagnagrunni í markumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="1a36b-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="1a36b-121">Eftir að afritunarferlinu er lokið geturðu ekki endurheimt núverandi gagnagrunn.</span><span class="sxs-lookup"><span data-stu-id="1a36b-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="1a36b-122">Markaumhverfið verður ekki tiltækt fyrr en afritunarferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="1a36b-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="1a36b-123">Skjöl í Microsoft Azure Blob geymsla er ekki afrituð úr einu umhverfi í annað.</span><span class="sxs-lookup"><span data-stu-id="1a36b-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="1a36b-124">Þar af leiðandi verða öll skjöl og sniðmát sem eru hengd við ekki afrituð og verða áfram í upprunaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="1a36b-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="1a36b-125">Allir notendur nema stjórnandi og aðrar notendareikningar innri þjónustu verða gerðir óvirkir.</span><span class="sxs-lookup"><span data-stu-id="1a36b-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="1a36b-126">Stjórnandi getur eytt eða lokað á gögn áður en aðrir notendur eru leyfðir aftur í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="1a36b-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="1a36b-127">Stjórnandi notandinn verður að gera nauðsynlegar stillingarbreytingar, svo sem aftur að tengja endapunkta samþættingar við tiltekna þjónustu eða vefslóðir.</span><span class="sxs-lookup"><span data-stu-id="1a36b-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="1a36b-128">Afritaðu gagnagrunn Human Resources</span><span class="sxs-lookup"><span data-stu-id="1a36b-128">Copy the Human Resources database</span></span>

<span data-ttu-id="1a36b-129">Til að ljúka þessu verkefni afritarðu fyrst dæmi og skráir þig síðan inn á Microsoft Power Platform Admin Center til að afrita Power Apps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="1a36b-130">Þegar þú afritar dæmi er gagnagrunninum eytt í markatilvikinu.</span><span class="sxs-lookup"><span data-stu-id="1a36b-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="1a36b-131">Markmiðið er ekki tiltækt meðan á þessu ferli stendur.</span><span class="sxs-lookup"><span data-stu-id="1a36b-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="1a36b-132">Skráðu þig inn á LCS og veldu LCS verkefnið sem inniheldur dæmið sem þú vilt afrita.</span><span class="sxs-lookup"><span data-stu-id="1a36b-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="1a36b-133">Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="1a36b-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="1a36b-134">Veldu dæmið sem á að afrita og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="1a36b-135">Í verkglugganum **Afritaðu dæmi**, veldu dæmið sem á að skrifa yfir og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="1a36b-136">Bíddu eftir því að gildið í reitnum **Afrita stöðu** sé uppfært í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="1a36b-137">Veldu dæmi til að skrifa yfir</span><span class="sxs-lookup"><span data-stu-id="1a36b-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="1a36b-138">Veldu **Power Platform** og skráðu þig inn í Admin Center Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="1a36b-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="1a36b-139">Veldu Power Platform</span><span class="sxs-lookup"><span data-stu-id="1a36b-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="1a36b-140">Veldu Power Apps-umhverfið sem á að afrita og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="1a36b-141">Þegar afritunarferlinu er lokið, skráðu þig inn á markstaðinn og virkjaðu samþættinguna Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1a36b-141">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="1a36b-142">Nánari upplýsingar og leiðbeiningar, sjá [Skilgreina samþættingu Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="1a36b-142">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="1a36b-143">Gagnaþátta og staða</span><span class="sxs-lookup"><span data-stu-id="1a36b-143">Data elements and statuses</span></span>

<span data-ttu-id="1a36b-144">Eftirfarandi gagnaþættir eru ekki afritaðir þegar þú afritar tilvik Human Resources:</span><span class="sxs-lookup"><span data-stu-id="1a36b-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="1a36b-145">Netföng í töflunni **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="1a36b-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="1a36b-146">Runuvinnslusaga í töflunum **BatchJobHistory**, **BatchHistory**, og **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="1a36b-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="1a36b-147">SMTP lykilorð lykilorðsins í töflunni **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="1a36b-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="1a36b-148">SMTP gengi miðlarans í töflunni **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="1a36b-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="1a36b-149">Prentastjórnunarstillingar í töflunum **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="1a36b-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="1a36b-150">Umhverfissértækar skrár í töflunum **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="1a36b-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="1a36b-151">Skjal viðhengi í DocuValue-töflunni.</span><span class="sxs-lookup"><span data-stu-id="1a36b-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="1a36b-152">Þessi viðhengi innihalda öll Microsoft Office-sniðmát sem skrifað var yfir í heimildarumhverfinu</span><span class="sxs-lookup"><span data-stu-id="1a36b-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="1a36b-153">Tengingarstrengurinn í töflunni **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="1a36b-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="1a36b-154">Sumar þessara eininga eru ekki afritaðar vegna þess að þær eru háðar tilteknu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="1a36b-155">Sem dæmi má nefna skrárnar **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="1a36b-156">Aðrir þættir eru ekki afritaðir vegna magns stuðningsmiða.</span><span class="sxs-lookup"><span data-stu-id="1a36b-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="1a36b-157">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="1a36b-157">For example:</span></span>

- <span data-ttu-id="1a36b-158">Hægt er að senda afrit af tölvupóstum vegna þess að SMTP er enn virkt í samþykkisprófun notanda (sandkassa).</span><span class="sxs-lookup"><span data-stu-id="1a36b-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="1a36b-159">Ógild samþættingarskilaboð kunna að verða send vegna þess að runuvinnslur eru enn virkar.</span><span class="sxs-lookup"><span data-stu-id="1a36b-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="1a36b-160">Notendur gætu verið virkir áður en stjórnendur getur framkvæmt hreinsunaraðgerðir eftir uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="1a36b-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="1a36b-161">Einnig breytast eftirfarandi stöður þegar tilvik er afritað:</span><span class="sxs-lookup"><span data-stu-id="1a36b-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="1a36b-162">Allir notendur nema stjórnandi eru stilltir á **Avirkjað**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="1a36b-163">Allar runuvinnslur nema nokkrar kerfisvinnslur eru stilltar á **Halda eftir**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="1a36b-164">Umhverfisstjóri</span><span class="sxs-lookup"><span data-stu-id="1a36b-164">Environment admin</span></span>

<span data-ttu-id="1a36b-165">Öllum notendum í marksandkassaumhverfinu, þar með talið stjórnendum, er skipt út fyrir stjórnendur í upprunaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="1a36b-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="1a36b-166">Vertu viss um að þú sér stjórnandi í upprunaumhverfinu áður en þú afritar dæmi.</span><span class="sxs-lookup"><span data-stu-id="1a36b-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="1a36b-167">Ef þú ert það ekki geturðu ekki skráp þig inn í sandkassaumhverfi viðtökustaða eftir að afritun er lokið.</span><span class="sxs-lookup"><span data-stu-id="1a36b-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="1a36b-168">Allir notendur sem ekki eru kerfisstjórar í markkassasumhverfinu eru óvirkir til að koma í veg fyrir óæskileg innritun í sandkassaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="1a36b-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="1a36b-169">Stjórnendur geta endurtekið notendur ef þörf er á.</span><span class="sxs-lookup"><span data-stu-id="1a36b-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-common-data-service"></a><span data-ttu-id="1a36b-170">Nota sérstillta reiti á Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1a36b-170">Apply custom fields to Common Data Service</span></span>

<span data-ttu-id="1a36b-171">Ef tilvik er afritað inn í sandkassaumhverfi og ætlunin er að samþætta sandkassaumhverfið við Common Data Service þarf að endurnota sérstillta reiti í Common Data Service einingarnar.</span><span class="sxs-lookup"><span data-stu-id="1a36b-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span>

<span data-ttu-id="1a36b-172">Fyrir hvern sérstilltan fyrir Common Data Service einingar skal gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="1a36b-172">For each custom field that's exposed on Common Data Service entities, do the following steps:</span></span>

1. <span data-ttu-id="1a36b-173">Farið í sérstillta reitinn og veljið **Breyta völdu**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="1a36b-174">Afvelja skal reitinn **Virkur** fyrir hverja cdm_\* einingu sem sérstillti reiturinn er virkur fyrir.</span><span class="sxs-lookup"><span data-stu-id="1a36b-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="1a36b-175">Veljið **Nota breytingar**.</span><span class="sxs-lookup"><span data-stu-id="1a36b-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="1a36b-176">Veljið **Breyta** aftur.</span><span class="sxs-lookup"><span data-stu-id="1a36b-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="1a36b-177">Velja skal svæðið **Virkt** fyrir hverja cdm_\* einingu sem sérstillti reiturinn er virkur fyrir.</span><span class="sxs-lookup"><span data-stu-id="1a36b-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="1a36b-178">Veljið **Nota breytingar** aftur.</span><span class="sxs-lookup"><span data-stu-id="1a36b-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="1a36b-179">Ferlið við að afturkalla valið, nota breytingar, endurvelja og endurnota breytingar kalla á uppfærslu skema í Common Data Service til að taka með sérstillta reiti.</span><span class="sxs-lookup"><span data-stu-id="1a36b-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Common Data Service to include the custom fields.</span></span>

<span data-ttu-id="1a36b-180">Frekari upplýsingar um sérsniðna reiti er að finna á [Stofna og vinna með sérstillt svæði](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="1a36b-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a36b-181">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1a36b-181">See also</span></span>

[<span data-ttu-id="1a36b-182">Ráðstafa Human Resources</span><span class="sxs-lookup"><span data-stu-id="1a36b-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="1a36b-183">Fjarlægja tilvik</span><span class="sxs-lookup"><span data-stu-id="1a36b-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="1a36b-184">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="1a36b-184">Update process</span></span>](hr-admin-setup-update-process.md)


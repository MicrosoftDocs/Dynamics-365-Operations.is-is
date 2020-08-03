---
title: Afritið tilvik
description: Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: b14baf49517f5d606038af20366944788b22eba2
ms.sourcegitcommit: 1ec931f8fe86bde27f6def36ea214a2a05fb22f6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2020
ms.locfileid: "3554326"
---
# <a name="copy-an-instance"></a><span data-ttu-id="78985-103">Afritið tilvik</span><span class="sxs-lookup"><span data-stu-id="78985-103">Copy an instance</span></span>

<span data-ttu-id="78985-104">Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="78985-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="78985-105">Ef þú ert með annað sandkassaumhverfi geturðu einnig afritað gagnagrunninn úr því umhverfi yfir í markviss sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="78985-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="78985-106">Til að afrita dæmi verður þú að tryggja eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="78985-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="78985-107">Tilvik Human Resources sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="78985-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="78985-108">Umhverfið sem þú ert að afrita frá og til verður að vera á sama svæði.</span><span class="sxs-lookup"><span data-stu-id="78985-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="78985-109">Þú getur ekki afritað á milli svæða.</span><span class="sxs-lookup"><span data-stu-id="78985-109">You can't copy across regions.</span></span>

- <span data-ttu-id="78985-110">Þú verður að vera stjórnandi í markumhverfinu svo þú getir skráð þig inn á það eftir að hafa afritað tilvikið.</span><span class="sxs-lookup"><span data-stu-id="78985-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="78985-111">Þegar þú afritar gagnagrunn Human Resources, afritar þú ekki þá þætti (forrit eða gögn) sem eru í Microsoft PowerApps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="78985-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="78985-112">Fyrir upplýsingar um hvernig á að afrita þætti í PowerApps-umhverfi, sjá [Afrita umhverfi](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="78985-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="78985-113">PowerApps-umhverfið sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="78985-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="78985-114">Þú verður að vera alþjóðlegur leigjandi stjórnandi til að breyta PowerApps-framleiðsluumhverfi í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="78985-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="78985-115">Fyrir frekari upplýsingar um að breyta PowerApps-umhverfi, sjáðu [Skiptu um dæmi](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="78985-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="78985-116">Áhrif afritunar gagnagrunns Human Resources</span><span class="sxs-lookup"><span data-stu-id="78985-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="78985-117">Eftirfarandi atburðir eiga sér stað þegar þú afritar gagnagrunn Human Resources:</span><span class="sxs-lookup"><span data-stu-id="78985-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="78985-118">Afritunarferlið eyðir núverandi gagnagrunni í markumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="78985-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="78985-119">Eftir að afritunarferlinu er lokið geturðu ekki endurheimt núverandi gagnagrunn.</span><span class="sxs-lookup"><span data-stu-id="78985-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="78985-120">Markaumhverfið verður ekki tiltækt fyrr en afritunarferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="78985-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="78985-121">Skjöl í Microsoft Azure Blob geymsla er ekki afrituð úr einu umhverfi í annað.</span><span class="sxs-lookup"><span data-stu-id="78985-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="78985-122">Þess vegna verða öll skjöl og sniðmát sem fylgja eru ekki afrituð og þau verða áfram í upprunaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="78985-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="78985-123">Allir notendur nema stjórnandi og aðrar notendareikningar innri þjónustu verða gerðir óvirkir.</span><span class="sxs-lookup"><span data-stu-id="78985-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="78985-124">Þess vegna getur stjórnandi notandinn eytt eða skyggt á gögn áður en aðrir notendur eru leyfðir aftur inn í kerfið.</span><span class="sxs-lookup"><span data-stu-id="78985-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="78985-125">Stjórnandi notandinn verður að gera nauðsynlegar stillingarbreytingar, svo sem aftur að tengja endapunkta samþættingar við tiltekna þjónustu eða vefslóðir.</span><span class="sxs-lookup"><span data-stu-id="78985-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="78985-126">Afritaðu gagnagrunn Human Resources</span><span class="sxs-lookup"><span data-stu-id="78985-126">Copy the Human Resources database</span></span>

<span data-ttu-id="78985-127">Til að ljúka þessu verkefni afritarðu fyrst dæmi og skráir þig síðan inn á Microsoft Power Platform Admin Center til að afrita PowerApps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="78985-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="78985-128">Þegar þú afritar dæmi er gagnagrunninum eytt í markatilvikinu.</span><span class="sxs-lookup"><span data-stu-id="78985-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="78985-129">Markmiðið er ekki tiltækt meðan á þessu ferli stendur.</span><span class="sxs-lookup"><span data-stu-id="78985-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="78985-130">Skráðu þig inn á LCS og veldu LCS verkefnið sem inniheldur dæmið sem þú vilt afrita.</span><span class="sxs-lookup"><span data-stu-id="78985-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="78985-131">Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="78985-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="78985-132">Veldu dæmið sem á að afrita og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="78985-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="78985-133">Í verkglugganum **Afritaðu dæmi**, veldu dæmið sem á að skrifa yfir og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="78985-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="78985-134">Bíddu eftir því að gildið í reitnum **Afrita stöðu** sé uppfært í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="78985-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="78985-135">Veldu dæmi til að skrifa yfir</span><span class="sxs-lookup"><span data-stu-id="78985-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="78985-136">Veldu **Power Platform** og skráðu þig inn í Admin Center Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="78985-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="78985-137">Veldu Power Platform</span><span class="sxs-lookup"><span data-stu-id="78985-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="78985-138">Veldu PowerApps-umhverfið sem á að afrita og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="78985-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="78985-139">Þegar afritunarferlinu er lokið, skráðu þig inn á markstaðinn og virkjaðu samþættinguna Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="78985-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="78985-140">Nánari upplýsingar og leiðbeiningar, sjá [Skilgreina samþættingu Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="78985-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="78985-141">Gagnaþátta og staða</span><span class="sxs-lookup"><span data-stu-id="78985-141">Data elements and statuses</span></span>

<span data-ttu-id="78985-142">Eftirfarandi gagnaþættir eru ekki afritaðir þegar þú afritar tilvik Human Resources:</span><span class="sxs-lookup"><span data-stu-id="78985-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="78985-143">Netföng í töflunni **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="78985-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="78985-144">Runuvinnslusaga í töflunum **BatchJobHistory**, **BatchHistory**, og **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="78985-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="78985-145">SMTP lykilorð lykilorðsins í töflunni **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="78985-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="78985-146">SMTP gengi miðlarans í töflunni **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="78985-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="78985-147">Prentastjórnunarstillingar í töflunum **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="78985-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="78985-148">Umhverfissértækar skrár í töflunum **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="78985-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="78985-149">Skjal viðhengi í DocuValue-töflunni.</span><span class="sxs-lookup"><span data-stu-id="78985-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="78985-150">Þessi viðhengi innihalda öll Microsoft Office-sniðmát sem skrifað var yfir í heimildarumhverfinu</span><span class="sxs-lookup"><span data-stu-id="78985-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="78985-151">Tengingarstrengurinn í töflunni **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="78985-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="78985-152">Sumir af þessum þáttum eru ekki afritaðir vegna þess að þeir eru umhverfissértækir.</span><span class="sxs-lookup"><span data-stu-id="78985-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="78985-153">Sem dæmi má nefna skrárnar **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="78985-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="78985-154">Aðrir þættir eru ekki afritaðir vegna magns stuðningsmiða.</span><span class="sxs-lookup"><span data-stu-id="78985-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="78985-155">Til dæmis gætu tvíteknir tölvupóstar verið sendir vegna þess að SMTP er ennþá virkt í umhverfi notendasamþykktarprófunar (sandkassi), ógild samþættingarskilaboð gætu verið send vegna þess að hópastörf eru ennþá virk og notendur gætu verið virkjaðir áður en umsjónarmenn geta framkvæmt hreinsunaraðgerðir eftir endurnýjun.</span><span class="sxs-lookup"><span data-stu-id="78985-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="78985-156">Að auki breytast eftirfarandi stöðu þegar þú afritar tilvik:</span><span class="sxs-lookup"><span data-stu-id="78985-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="78985-157">Allir notendur nema stjórnandi eru stilltir á **Avirkjað**.</span><span class="sxs-lookup"><span data-stu-id="78985-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="78985-158">Allar runuvinnslur nema nokkrar kerfisvinnslur eru stilltar á **Halda eftir**.</span><span class="sxs-lookup"><span data-stu-id="78985-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="78985-159">Umhverfisstjóri</span><span class="sxs-lookup"><span data-stu-id="78985-159">Environment admin</span></span>

<span data-ttu-id="78985-160">Öllum notendum í marksandkassaumhverfinu, þar með talið stjórnendum, er skipt út fyrir stjórnendur í upprunaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="78985-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="78985-161">Vertu viss um að þú sér stjórnandi í upprunaumhverfinu áður en þú afritar dæmi.</span><span class="sxs-lookup"><span data-stu-id="78985-161">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="78985-162">Ef þú ert það ekki muntu ekki geta skráð þig inn í sandkassaumhverfið eftir að afritið er lokið.</span><span class="sxs-lookup"><span data-stu-id="78985-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="78985-163">Allir notendur sem ekki eru kerfisstjórar í markkassasumhverfinu eru óvirkir til að koma í veg fyrir óæskileg innritun í sandkassaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="78985-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="78985-164">Stjórnendur geta endurtekið notendur ef þörf er á.</span><span class="sxs-lookup"><span data-stu-id="78985-164">Administrators can reenable users if needed.</span></span>

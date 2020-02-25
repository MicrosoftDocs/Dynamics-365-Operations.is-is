---
title: Afritið tilvik
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009364"
---
# <a name="copy-an-instance"></a><span data-ttu-id="961d9-102">Afritið tilvik</span><span class="sxs-lookup"><span data-stu-id="961d9-102">Copy an instance</span></span>

<span data-ttu-id="961d9-103">Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="961d9-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="961d9-104">Ef þú ert með annað sandkassaumhverfi geturðu einnig afritað gagnagrunninn úr því umhverfi yfir í markviss sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="961d9-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="961d9-105">Til að afrita dæmi verður þú að tryggja eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="961d9-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="961d9-106">Tilvik Human Resources sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="961d9-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="961d9-107">Umhverfið sem þú ert að afrita frá og til verður að vera á sama svæði.</span><span class="sxs-lookup"><span data-stu-id="961d9-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="961d9-108">Þú getur ekki afritað á milli svæða.</span><span class="sxs-lookup"><span data-stu-id="961d9-108">You can't copy across regions.</span></span>

- <span data-ttu-id="961d9-109">Þú verður að vera stjórnandi í markumhverfinu svo þú getir skráð þig inn á það eftir að hafa afritað tilvikið.</span><span class="sxs-lookup"><span data-stu-id="961d9-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="961d9-110">Þegar þú afritar gagnagrunn Human Resources, afritar þú ekki þá þætti (forrit eða gögn) sem eru í Microsoft PowerApps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="961d9-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="961d9-111">Fyrir upplýsingar um hvernig á að afrita þætti í PowerApps-umhverfi, sjá [Afrita umhverfi](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="961d9-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="961d9-112">PowerApps-umhverfið sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="961d9-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="961d9-113">Þú verður að vera alþjóðlegur leigjandi stjórnandi til að breyta PowerApps-framleiðsluumhverfi í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="961d9-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="961d9-114">Fyrir frekari upplýsingar um að breyta PowerApps-umhverfi, sjáðu [Skiptu um dæmi](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="961d9-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="961d9-115">Áhrif afritunar gagnagrunns Human Resources</span><span class="sxs-lookup"><span data-stu-id="961d9-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="961d9-116">Eftirfarandi atburðir eiga sér stað þegar þú afritar gagnagrunn Human Resources:</span><span class="sxs-lookup"><span data-stu-id="961d9-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="961d9-117">Afritunarferlið eyðir núverandi gagnagrunni í markumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="961d9-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="961d9-118">Eftir að afritunarferlinu er lokið geturðu ekki endurheimt núverandi gagnagrunn.</span><span class="sxs-lookup"><span data-stu-id="961d9-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="961d9-119">Markaumhverfið verður ekki tiltækt fyrr en afritunarferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="961d9-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="961d9-120">Skjöl í Microsoft Azure Blob geymsla er ekki afrituð úr einu umhverfi í annað.</span><span class="sxs-lookup"><span data-stu-id="961d9-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="961d9-121">Þess vegna verða öll skjöl og sniðmát sem fylgja eru ekki afrituð og þau verða áfram í upprunaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="961d9-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="961d9-122">Allir notendur nema stjórnandi og aðrar notendareikningar innri þjónustu verða gerðir óvirkir.</span><span class="sxs-lookup"><span data-stu-id="961d9-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="961d9-123">Þess vegna getur stjórnandi notandinn eytt eða skyggt á gögn áður en aðrir notendur eru leyfðir aftur inn í kerfið.</span><span class="sxs-lookup"><span data-stu-id="961d9-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="961d9-124">Stjórnandi notandinn verður að gera nauðsynlegar stillingarbreytingar, svo sem aftur að tengja endapunkta samþættingar við tiltekna þjónustu eða vefslóðir.</span><span class="sxs-lookup"><span data-stu-id="961d9-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="961d9-125">Afritaðu gagnagrunn Human Resources</span><span class="sxs-lookup"><span data-stu-id="961d9-125">Copy the Human Resources database</span></span>

<span data-ttu-id="961d9-126">Til að ljúka þessu verkefni afritarðu fyrst dæmi og skráir þig síðan inn á Microsoft Power Platform Admin Center til að afrita PowerApps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="961d9-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="961d9-127">Þegar þú afritar dæmi er gagnagrunninum eytt í markatilvikinu.</span><span class="sxs-lookup"><span data-stu-id="961d9-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="961d9-128">Markmiðið er ekki tiltækt meðan á þessu ferli stendur.</span><span class="sxs-lookup"><span data-stu-id="961d9-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="961d9-129">Skráðu þig inn á LCS og veldu LCS verkefnið sem inniheldur dæmið sem þú vilt afrita.</span><span class="sxs-lookup"><span data-stu-id="961d9-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="961d9-130">Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.</span><span class="sxs-lookup"><span data-stu-id="961d9-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="961d9-131">Veldu dæmið sem á að afrita og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="961d9-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="961d9-132">Í verkglugganum **Afritaðu dæmi**, veldu dæmið sem á að skrifa yfir og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="961d9-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="961d9-133">Bíddu eftir því að gildið í reitnum **Afrita stöðu** sé uppfært í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="961d9-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="961d9-134">Veldu dæmi til að skrifa yfir</span><span class="sxs-lookup"><span data-stu-id="961d9-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="961d9-135">Veldu **Power Platform** og skráðu þig inn í Admin Center Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="961d9-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="961d9-136">Veldu Power Platform</span><span class="sxs-lookup"><span data-stu-id="961d9-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="961d9-137">Veldu PowerApps-umhverfið sem á að afrita og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="961d9-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="961d9-138">Þegar afritunarferlinu er lokið, skráðu þig inn á markstaðinn og virkjaðu samþættinguna Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="961d9-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="961d9-139">Nánari upplýsingar og leiðbeiningar, sjá [Skilgreina samþættingu Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="961d9-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="961d9-140">Gagnaþátta og staða</span><span class="sxs-lookup"><span data-stu-id="961d9-140">Data elements and statuses</span></span>

<span data-ttu-id="961d9-141">Eftirfarandi gagnaþættir eru ekki afritaðir þegar þú afritar tilvik Human Resources:</span><span class="sxs-lookup"><span data-stu-id="961d9-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="961d9-142">Netföng í töflunni **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="961d9-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="961d9-143">Runuvinnslusaga í töflunum **BatchJobHistory**, **BatchHistory**, og **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="961d9-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="961d9-144">SMTP lykilorð lykilorðsins í töflunni **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="961d9-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="961d9-145">SMTP gengi miðlarans í töflunni **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="961d9-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="961d9-146">Prentastjórnunarstillingar í töflunum **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="961d9-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="961d9-147">Umhverfissértækar skrár í töflunum **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="961d9-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="961d9-148">Skjal viðhengi í DocuValue-töflunni.</span><span class="sxs-lookup"><span data-stu-id="961d9-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="961d9-149">Þessi viðhengi innihalda öll Microsoft Office-sniðmát sem skrifað var yfir í heimildarumhverfinu</span><span class="sxs-lookup"><span data-stu-id="961d9-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="961d9-150">Tengingarstrengurinn í töflunni **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="961d9-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="961d9-151">Sumir af þessum þáttum eru ekki afritaðir vegna þess að þeir eru umhverfissértækir.</span><span class="sxs-lookup"><span data-stu-id="961d9-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="961d9-152">Sem dæmi má nefna skrárnar **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="961d9-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="961d9-153">Aðrir þættir eru ekki afritaðir vegna magns stuðningsmiða.</span><span class="sxs-lookup"><span data-stu-id="961d9-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="961d9-154">Til dæmis gætu tvíteknir tölvupóstar verið sendir vegna þess að SMTP er ennþá virkt í umhverfi notendasamþykktarprófunar (sandkassi), ógild samþættingarskilaboð gætu verið send vegna þess að hópastörf eru ennþá virk og notendur gætu verið virkjaðir áður en umsjónarmenn geta framkvæmt hreinsunaraðgerðir eftir endurnýjun.</span><span class="sxs-lookup"><span data-stu-id="961d9-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="961d9-155">Að auki breytast eftirfarandi stöðu þegar þú afritar tilvik:</span><span class="sxs-lookup"><span data-stu-id="961d9-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="961d9-156">Allir notendur nema stjórnandi eru stilltir á **Avirkjað**.</span><span class="sxs-lookup"><span data-stu-id="961d9-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="961d9-157">Allar runuvinnslur nema nokkrar kerfisvinnslur eru stilltar á **Halda eftir**.</span><span class="sxs-lookup"><span data-stu-id="961d9-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="961d9-158">Umhverfisstjóri</span><span class="sxs-lookup"><span data-stu-id="961d9-158">Environment admin</span></span>

<span data-ttu-id="961d9-159">Öllum notendum í marksandkassaumhverfinu, þar með talið stjórnendum, er skipt út fyrir stjórnendur í upprunaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="961d9-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="961d9-160">Vertu viss um að þú sért stjórnandi í markumhverfinu áður en þú afritar tilvik.</span><span class="sxs-lookup"><span data-stu-id="961d9-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="961d9-161">Ef þú ert það ekki muntu ekki geta skráð þig inn í sandkassaumhverfið eftir að afritið er lokið.</span><span class="sxs-lookup"><span data-stu-id="961d9-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="961d9-162">Allir notendur sem ekki eru kerfisstjórar í markkassasumhverfinu eru óvirkir til að koma í veg fyrir óæskileg innritun í sandkassaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="961d9-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="961d9-163">Stjórnendur geta endurtekið notendur ef þörf er á.</span><span class="sxs-lookup"><span data-stu-id="961d9-163">Administrators can reenable users if needed.</span></span>

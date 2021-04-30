---
title: Skilgreina samþættingu við Dayforce
description: Samþættingin milli Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessari grein. Nauðsynlegt er að skilgreina samþættinguna bæði í Human Resources og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890005"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="6e273-104">Skilgreina samþættingu við Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6e273-105">Samþættingin milli Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="6e273-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="6e273-106">Nauðsynlegt er að skilgreina samþættinguna bæði í Human Resources og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="6e273-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="6e273-107">Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e273-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="6e273-108">Samþættingin krefst tilgreindra gagna frá Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e273-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="6e273-109">Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Human Resources á þann hátt sem styður samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="6e273-110">Samþættingin notar eftirfarandi víðtæka flokka gagna:</span><span class="sxs-lookup"><span data-stu-id="6e273-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="6e273-111">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="6e273-111">Human resources data</span></span>
- <span data-ttu-id="6e273-112">Launagögn</span><span class="sxs-lookup"><span data-stu-id="6e273-112">Compensation data</span></span>
- <span data-ttu-id="6e273-113">Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="6e273-114">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="6e273-114">Worker data</span></span>

<span data-ttu-id="6e273-115">Þessi grein fjallar um skrefin sem verður að fylgja til að virkja samþættinginu.</span><span class="sxs-lookup"><span data-stu-id="6e273-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="6e273-116">Það útskýrir einnig gerð gagna og upplýsingar um skilgreiningar sem samþættingin krefst.</span><span class="sxs-lookup"><span data-stu-id="6e273-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="6e273-117">Virkja samþættingu</span><span class="sxs-lookup"><span data-stu-id="6e273-117">Enable the integration</span></span>

<span data-ttu-id="6e273-118">Í Human Resources er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="6e273-119">Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 Finance þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance.</span><span class="sxs-lookup"><span data-stu-id="6e273-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="6e273-120">Til að kveikja á samþættingu í Human Resources skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6e273-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="6e273-121">Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="6e273-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="6e273-122">Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.</span><span class="sxs-lookup"><span data-stu-id="6e273-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="6e273-123">Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.</span><span class="sxs-lookup"><span data-stu-id="6e273-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="6e273-124">Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6e273-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="6e273-125">Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt.</span><span class="sxs-lookup"><span data-stu-id="6e273-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="6e273-126">Hægt er að breyta tíðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="6e273-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="6e273-127">Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi greinum Azure:</span><span class="sxs-lookup"><span data-stu-id="6e273-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="6e273-128">Um Azure-geymslureikninga</span><span class="sxs-lookup"><span data-stu-id="6e273-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="6e273-129">Skilgreina tengistrengi Azure-geymslu</span><span class="sxs-lookup"><span data-stu-id="6e273-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="6e273-130">Tæknilýsing þegar launasamþætting er virk</span><span class="sxs-lookup"><span data-stu-id="6e273-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="6e273-131">Að kveikja á launasamþættingu hefur aðallega tvennt í för með sér:</span><span class="sxs-lookup"><span data-stu-id="6e273-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="6e273-132">Gagnaútflutningsverk sem heitir "Útflutningur launasamþættingar" er búið til.</span><span class="sxs-lookup"><span data-stu-id="6e273-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="6e273-133">Þetta verk inniheldur þær einingar og reiti sem þarf fyrir launasamþættinguna.</span><span class="sxs-lookup"><span data-stu-id="6e273-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="6e273-134">Til að skoða verkið skaltu fara í **Kerfisstjórnun**, velja reitinn **Gagnastjórnun** og opna síðan gagnaverkið af listanum yfir verk.</span><span class="sxs-lookup"><span data-stu-id="6e273-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="6e273-135">Þessi runuvinnsla keyrir gagnaútflutningsverkið, dulkóðar gagnapakkann sem fylgir því og flytur gagnapakkaskrána á SFTP-endastöðina sem er skilgreind á skjánum **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="6e273-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="6e273-136">Gagnapakkinn sem er fluttur til SFTP-endastöðvarinnar er dulkóðaður með lykli sem er einkvæmur fyrir pakkann.</span><span class="sxs-lookup"><span data-stu-id="6e273-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="6e273-137">Lykillinn er í Azure-lykageymslu er aðeins aðgengileg af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="6e273-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="6e273-138">Ekki er hægt að afkóða og skoða innihald gagnapakka.</span><span class="sxs-lookup"><span data-stu-id="6e273-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="6e273-139">Ef þú þarft að skoða innihald gagnapakka þarftu að flytja út gagnaverkið „Útflutningur launasamþættingar“ handvirkt, hlaða niður því og opna það síðan.</span><span class="sxs-lookup"><span data-stu-id="6e273-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="6e273-140">Handvirkur útflutningur mun ekki beita dulkóðun eða flytja pakkann.</span><span class="sxs-lookup"><span data-stu-id="6e273-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="6e273-141">Þegar samþættingarskrár eru t.d. sendar úr Dynamics 365 Human Resources UAT eða sandkassaumhverfi í Ceridian Dayforce prófunarumhverfi er hægt að nota eftirfarandi slóð lyklageymslu: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="6e273-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="6e273-142">Skilgreina gögnin þín</span><span class="sxs-lookup"><span data-stu-id="6e273-142">Configure your data</span></span> 

<span data-ttu-id="6e273-143">Til að afgreiða laun þarf að skilgreina mannauðsgögn í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e273-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="6e273-144">Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun.</span><span class="sxs-lookup"><span data-stu-id="6e273-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="6e273-145">Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.</span><span class="sxs-lookup"><span data-stu-id="6e273-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="6e273-146">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="6e273-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="6e273-147">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="6e273-147">Benefits</span></span> 

<span data-ttu-id="6e273-148">Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.</span><span class="sxs-lookup"><span data-stu-id="6e273-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="6e273-149">Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="6e273-150">Fríðindaáætlanir</span><span class="sxs-lookup"><span data-stu-id="6e273-150">Benefit plans</span></span>

- <span data-ttu-id="6e273-151">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-151">Plan (required)</span></span>
- <span data-ttu-id="6e273-152">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-152">Type (required)</span></span>
- <span data-ttu-id="6e273-153">Áhrif á launaskrá (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-153">Payroll impact (required)</span></span>
- <span data-ttu-id="6e273-154">Endurheimta vangoldnar greiðslur</span><span class="sxs-lookup"><span data-stu-id="6e273-154">Recover arrears</span></span>
- <span data-ttu-id="6e273-155">Frádráttaraðferð</span><span class="sxs-lookup"><span data-stu-id="6e273-155">Deduction method</span></span>
- <span data-ttu-id="6e273-156">Frádráttarforgangur</span><span class="sxs-lookup"><span data-stu-id="6e273-156">Deduction priority</span></span>
- <span data-ttu-id="6e273-157">Takmörkunartímabil</span><span class="sxs-lookup"><span data-stu-id="6e273-157">Limit period</span></span>
- <span data-ttu-id="6e273-158">Takmarka upphæð</span><span class="sxs-lookup"><span data-stu-id="6e273-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="6e273-159">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="6e273-159">Benefits</span></span>

- <span data-ttu-id="6e273-160">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-160">Plan (required)</span></span>
- <span data-ttu-id="6e273-161">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-161">Type (required)</span></span>
- <span data-ttu-id="6e273-162">Valkostur (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-162">Option (required)</span></span>
- <span data-ttu-id="6e273-163">Fríðindaauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-163">Benefit ID (required)</span></span>
- <span data-ttu-id="6e273-164">Tíðni</span><span class="sxs-lookup"><span data-stu-id="6e273-164">Frequency</span></span>
- <span data-ttu-id="6e273-165">Grunnur</span><span class="sxs-lookup"><span data-stu-id="6e273-165">Basis</span></span>
- <span data-ttu-id="6e273-166">Upphæð eða taxti</span><span class="sxs-lookup"><span data-stu-id="6e273-166">Amount or rate</span></span>
- <span data-ttu-id="6e273-167">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="6e273-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="6e273-168">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="6e273-168">Supported frequencies</span></span> 

- <span data-ttu-id="6e273-169">Vikulega</span><span class="sxs-lookup"><span data-stu-id="6e273-169">Weekly</span></span>
- <span data-ttu-id="6e273-170">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="6e273-170">Bi-weekly</span></span>
- <span data-ttu-id="6e273-171">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="6e273-171">Semi-monthly</span></span>
- <span data-ttu-id="6e273-172">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="6e273-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="6e273-173">Studdir grunnar</span><span class="sxs-lookup"><span data-stu-id="6e273-173">Supported bases</span></span> 

- <span data-ttu-id="6e273-174">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="6e273-174">Fixed amount</span></span>
- <span data-ttu-id="6e273-175">Prósenta af tekjum</span><span class="sxs-lookup"><span data-stu-id="6e273-175">Percent of earnings</span></span>
- <span data-ttu-id="6e273-176">Virkar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="6e273-176">Productive hours</span></span>

<span data-ttu-id="6e273-177">Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.</span><span class="sxs-lookup"><span data-stu-id="6e273-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="6e273-178">Val í Human Resources</span><span class="sxs-lookup"><span data-stu-id="6e273-178">Selection in Human Resources</span></span>        | <span data-ttu-id="6e273-179">Niðurstaða í Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="6e273-180">Enginn</span><span class="sxs-lookup"><span data-stu-id="6e273-180">None</span></span>                       | <span data-ttu-id="6e273-181">Enginn frádráttur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="6e273-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="6e273-182">Eingöngu frádráttur</span><span class="sxs-lookup"><span data-stu-id="6e273-182">Deduction only</span></span>             | <span data-ttu-id="6e273-183">Frádráttur starfsmanns er búinn til.</span><span class="sxs-lookup"><span data-stu-id="6e273-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="6e273-184">Eingöngu framlag</span><span class="sxs-lookup"><span data-stu-id="6e273-184">Contribution only</span></span>          | <span data-ttu-id="6e273-185">Frádráttur vinnuveitanda er búinn til.</span><span class="sxs-lookup"><span data-stu-id="6e273-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="6e273-186">Frádráttur og framlag</span><span class="sxs-lookup"><span data-stu-id="6e273-186">Deduction and contribution</span></span> | <span data-ttu-id="6e273-187">Frádrættir starfsmanns og vinnuveitanda eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="6e273-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="6e273-188">Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="6e273-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="6e273-189">Leggja fram starfskjaraáætlun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="6e273-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="6e273-190">Stofna ný fríðindi</span><span class="sxs-lookup"><span data-stu-id="6e273-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="6e273-191">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="6e273-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="6e273-192">Skrá og fjarlægja fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="6e273-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="6e273-193">Laun</span><span class="sxs-lookup"><span data-stu-id="6e273-193">Compensation</span></span> 

<span data-ttu-id="6e273-194">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="6e273-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="6e273-195">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="6e273-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="6e273-196">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="6e273-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="6e273-197">Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="6e273-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="6e273-198">Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta.</span><span class="sxs-lookup"><span data-stu-id="6e273-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="6e273-199">Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="6e273-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="6e273-200">Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="6e273-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="6e273-201">Launafyrirkomulag fastra launa stofnað</span><span class="sxs-lookup"><span data-stu-id="6e273-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="6e273-202">Launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="6e273-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="6e273-203">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="6e273-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="6e273-204">Launaútreikningur</span><span class="sxs-lookup"><span data-stu-id="6e273-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="6e273-205">Skilgreina launavinnslu og reikna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="6e273-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="6e273-206">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="6e273-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="6e273-207">Skrá starfsmann í launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="6e273-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="6e273-208">Störf</span><span class="sxs-lookup"><span data-stu-id="6e273-208">Jobs</span></span> 

<span data-ttu-id="6e273-209">Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið.</span><span class="sxs-lookup"><span data-stu-id="6e273-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="6e273-210">Frekari upplýsingar er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="6e273-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="6e273-211">Setja upp íhluta verks</span><span class="sxs-lookup"><span data-stu-id="6e273-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="6e273-212">Skilgreina ný störf</span><span class="sxs-lookup"><span data-stu-id="6e273-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="6e273-213">Stöður</span><span class="sxs-lookup"><span data-stu-id="6e273-213">Positions</span></span>

<span data-ttu-id="6e273-214">Staða er sérstakt tilvik starfs.</span><span class="sxs-lookup"><span data-stu-id="6e273-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="6e273-215">Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“.</span><span class="sxs-lookup"><span data-stu-id="6e273-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="6e273-216">Staða er til í deild.</span><span class="sxs-lookup"><span data-stu-id="6e273-216">A position exists in a department.</span></span> <span data-ttu-id="6e273-217">Einungis einn starfsmaður getur tengst hverri stöðu.</span><span class="sxs-lookup"><span data-stu-id="6e273-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="6e273-218">Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:</span><span class="sxs-lookup"><span data-stu-id="6e273-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="6e273-219">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-219">Position (required)</span></span>
- <span data-ttu-id="6e273-220">Lýsing (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-220">Description (required)</span></span>
- <span data-ttu-id="6e273-221">Starf (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-221">Job (required)</span></span>
- <span data-ttu-id="6e273-222">Deild (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-222">Department (required)</span></span>
- <span data-ttu-id="6e273-223">Stöðugerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-223">Position type (required)</span></span>
- <span data-ttu-id="6e273-224">Jafngildi fulls starfs</span><span class="sxs-lookup"><span data-stu-id="6e273-224">Full-time equivalent</span></span>
- <span data-ttu-id="6e273-225">Reglulegar árlegar vinnustundir (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="6e273-226">Greitt eftir lögaðila (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="6e273-227">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-227">Pay cycle (required)</span></span>
- <span data-ttu-id="6e273-228">Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="6e273-229">Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="6e273-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="6e273-230">Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="6e273-231">Frekari upplýsingar er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="6e273-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="6e273-232">Vinnuafl skipulagt með notkun deilda, starfa og staða</span><span class="sxs-lookup"><span data-stu-id="6e273-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="6e273-233">Setja upp stöður</span><span class="sxs-lookup"><span data-stu-id="6e273-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="6e273-234">Deildir</span><span class="sxs-lookup"><span data-stu-id="6e273-234">Departments</span></span>

<span data-ttu-id="6e273-235">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="6e273-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="6e273-236">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="6e273-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="6e273-237">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="6e273-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="6e273-238">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="6e273-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="6e273-239">Frekari upplýsingar er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="6e273-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="6e273-240">Stofnun deildar og tenging hennar við deildastigveldið</span><span class="sxs-lookup"><span data-stu-id="6e273-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="6e273-241">Skilgreina nýjar deildir</span><span class="sxs-lookup"><span data-stu-id="6e273-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="6e273-242">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="6e273-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="6e273-243">Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="6e273-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="6e273-244">Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="6e273-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="6e273-245">Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur.</span><span class="sxs-lookup"><span data-stu-id="6e273-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="6e273-246">Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.</span><span class="sxs-lookup"><span data-stu-id="6e273-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="6e273-247">Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli.</span><span class="sxs-lookup"><span data-stu-id="6e273-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="6e273-248">Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp.</span><span class="sxs-lookup"><span data-stu-id="6e273-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="6e273-249">Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.</span><span class="sxs-lookup"><span data-stu-id="6e273-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="6e273-250">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="6e273-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="6e273-251">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-251">Pay cycle (required)</span></span>
- <span data-ttu-id="6e273-252">Tíðni greiðsluferlis (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="6e273-253">Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="6e273-254">Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="6e273-255">Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="6e273-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="6e273-256">Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="6e273-257">Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e273-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="6e273-258">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-258">Earning codes</span></span>

<span data-ttu-id="6e273-259">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="6e273-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6e273-260">Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="6e273-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="6e273-261">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="6e273-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="6e273-262">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-262">Earning Code (required)</span></span>
- <span data-ttu-id="6e273-263">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-263">Description</span></span>
- <span data-ttu-id="6e273-264">Mælieining</span><span class="sxs-lookup"><span data-stu-id="6e273-264">Unit of measure</span></span>
- <span data-ttu-id="6e273-265">Framleiðni</span><span class="sxs-lookup"><span data-stu-id="6e273-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="6e273-266">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="6e273-266">Worker data</span></span>

<span data-ttu-id="6e273-267">Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="6e273-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="6e273-268">Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="6e273-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="6e273-269">Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:</span><span class="sxs-lookup"><span data-stu-id="6e273-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="6e273-270">**Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="6e273-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="6e273-271">**Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.</span><span class="sxs-lookup"><span data-stu-id="6e273-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="6e273-272">**Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.</span><span class="sxs-lookup"><span data-stu-id="6e273-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="6e273-273">**Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.</span><span class="sxs-lookup"><span data-stu-id="6e273-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="6e273-274">Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="6e273-275">Almennar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e273-275">General information</span></span>

- <span data-ttu-id="6e273-276">Númer starfsmanns (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-276">Personnel number (required)</span></span>
- <span data-ttu-id="6e273-277">Fornafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-277">First name (required)</span></span>
- <span data-ttu-id="6e273-278">Eftirnafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-278">Last name (required)</span></span>
- <span data-ttu-id="6e273-279">Millinafn</span><span class="sxs-lookup"><span data-stu-id="6e273-279">Middle name</span></span>
- <span data-ttu-id="6e273-280">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="6e273-280">Seniority date</span></span>
- <span data-ttu-id="6e273-281">Þekkt sem</span><span class="sxs-lookup"><span data-stu-id="6e273-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="6e273-282">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e273-282">Personal information</span></span>

- <span data-ttu-id="6e273-283">Hjúskaparstaða (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-283">Marital status (required)</span></span>
- <span data-ttu-id="6e273-284">Fæðingardagur (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-284">Birth date (required)</span></span>
- <span data-ttu-id="6e273-285">Kyn (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-285">Gender (required)</span></span>
- <span data-ttu-id="6e273-286">Einstaklingur sem á við fötlun að stríða</span><span class="sxs-lookup"><span data-stu-id="6e273-286">Person with disabilities</span></span>
- <span data-ttu-id="6e273-287">Þjóðerni land svæði (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="6e273-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="6e273-288">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="6e273-288">Address information</span></span>

- <span data-ttu-id="6e273-289">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-289">Primary (required)</span></span>
- <span data-ttu-id="6e273-290">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-290">Country/region (required)</span></span>
- <span data-ttu-id="6e273-291">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-291">Postal code (required)</span></span>
- <span data-ttu-id="6e273-292">Götunúmer (krafist) (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="6e273-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="6e273-293">Viðbygging (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="6e273-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="6e273-294">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-294">City (required)</span></span>
- <span data-ttu-id="6e273-295">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-295">State (required)</span></span>
- <span data-ttu-id="6e273-296">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="6e273-297">Samskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e273-297">Contact information</span></span> 

- <span data-ttu-id="6e273-298">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-298">Primary (required)</span></span>
- <span data-ttu-id="6e273-299">Símanúmer tengiliðar (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-299">Contact number (required)</span></span>
- <span data-ttu-id="6e273-300">Skráarending</span><span class="sxs-lookup"><span data-stu-id="6e273-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="6e273-301">Launaupplýsingar og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-301">Payroll information and earning codes</span></span>

<span data-ttu-id="6e273-302">Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6e273-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="6e273-303">Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.</span><span class="sxs-lookup"><span data-stu-id="6e273-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="6e273-304">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-304">Earning codes</span></span>

- <span data-ttu-id="6e273-305">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-305">Position (required)</span></span>
- <span data-ttu-id="6e273-306">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-306">Earning Code (required)</span></span>
- <span data-ttu-id="6e273-307">Tíðni (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-307">Frequency (required)</span></span>
- <span data-ttu-id="6e273-308">Upphæð (áskilin)</span><span class="sxs-lookup"><span data-stu-id="6e273-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="6e273-309">Launaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e273-309">Payroll information</span></span>

- <span data-ttu-id="6e273-310">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="6e273-310">Payment Method</span></span>
- <span data-ttu-id="6e273-311">Efnahagssvæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-311">Economic Region (required)</span></span>
- <span data-ttu-id="6e273-312">Kenni fyrir fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="6e273-312">Employee Benefits ID</span></span>
- <span data-ttu-id="6e273-313">Kennitala (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-313">National ID Number (required)</span></span>
- <span data-ttu-id="6e273-314">Hernaðarþjónustunúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-314">Military Service Number</span></span>
- <span data-ttu-id="6e273-315">Auðkenni vaktar (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-315">Shift ID (required)</span></span>
- <span data-ttu-id="6e273-316">Skattanúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-316">Tax Number (required)</span></span>
- <span data-ttu-id="6e273-317">Auðkenni stéttarfélags (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-317">Union ID (required)</span></span>
- <span data-ttu-id="6e273-318">Vinnudagskenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-318">Work Day ID (required)</span></span>
- <span data-ttu-id="6e273-319">Vinnuleyfisnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="6e273-320">Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="6e273-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="6e273-321">Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="6e273-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="6e273-322">Atvinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e273-322">Employment details</span></span>

<span data-ttu-id="6e273-323">Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="6e273-324">Dayforce styður aðeins eina starfsferilsskrá í einu.</span><span class="sxs-lookup"><span data-stu-id="6e273-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="6e273-325">Upphafsdagsetning ráðningar (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-325">Employment start date (required)</span></span>
- <span data-ttu-id="6e273-326">Dagsetning starfsloka</span><span class="sxs-lookup"><span data-stu-id="6e273-326">Employment end date</span></span>
- <span data-ttu-id="6e273-327">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="6e273-327">Start date</span></span>
- <span data-ttu-id="6e273-328">Breyttur fyrsti starfsdagur</span><span class="sxs-lookup"><span data-stu-id="6e273-328">Adjusted start date</span></span>
- <span data-ttu-id="6e273-329">Dagsetning starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="6e273-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="6e273-330">Ástæða starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="6e273-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="6e273-331">Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="6e273-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="6e273-332">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-332">Human Resources</span></span>                | <span data-ttu-id="6e273-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e273-334">Nýlegasti ráðningardagurinn</span><span class="sxs-lookup"><span data-stu-id="6e273-334">Most recent hire date</span></span> | <span data-ttu-id="6e273-335">Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="6e273-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="6e273-336">Starfslokadagur</span><span class="sxs-lookup"><span data-stu-id="6e273-336">Termination date</span></span>      | <span data-ttu-id="6e273-337">Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="6e273-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="6e273-338">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="6e273-338">Start date</span></span>            | <span data-ttu-id="6e273-339">Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="6e273-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="6e273-340">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="6e273-340">Original hire date</span></span>    | <span data-ttu-id="6e273-341">Upphaf ráðningar fyrir elsta atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="6e273-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="6e273-342">Laun</span><span class="sxs-lookup"><span data-stu-id="6e273-342">Compensation</span></span>

<span data-ttu-id="6e273-343">Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil.</span><span class="sxs-lookup"><span data-stu-id="6e273-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="6e273-344">Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.</span><span class="sxs-lookup"><span data-stu-id="6e273-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="6e273-345">Gildisdagsetning (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-345">Effective Date (required)</span></span>
- <span data-ttu-id="6e273-346">Gildistími</span><span class="sxs-lookup"><span data-stu-id="6e273-346">Expiration date</span></span>
- <span data-ttu-id="6e273-347">Launataxti (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-347">Pay Rate (required)</span></span>
- <span data-ttu-id="6e273-348">Umreikningur launataxta (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="6e273-349">Árlegt jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="6e273-350">Klukkutíma jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="6e273-351">Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="6e273-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="6e273-352">Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="6e273-353">Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="6e273-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="6e273-354">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="6e273-355">Auðkenni kennitölu</span><span class="sxs-lookup"><span data-stu-id="6e273-355">Social Security identifier</span></span> 

<span data-ttu-id="6e273-356">Sérhver starfsmaður verður að hafa eitt aðalauðkenni.</span><span class="sxs-lookup"><span data-stu-id="6e273-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="6e273-357">Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="6e273-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="6e273-358">Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="6e273-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="6e273-359">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-359">Primary (required)</span></span>
- <span data-ttu-id="6e273-360">Gerð auðkennis = „Kennitala“</span><span class="sxs-lookup"><span data-stu-id="6e273-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="6e273-361">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="6e273-361">Issued Date</span></span>
- <span data-ttu-id="6e273-362">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="6e273-362">Expiration Date</span></span>

<span data-ttu-id="6e273-363">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="6e273-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="6e273-364">Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.</span><span class="sxs-lookup"><span data-stu-id="6e273-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="6e273-365">Bankareikningar og útborganir</span><span class="sxs-lookup"><span data-stu-id="6e273-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="6e273-366">Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="6e273-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="6e273-367">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-367">Human Resources</span></span>                         | <span data-ttu-id="6e273-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e273-369">Bankareikningsnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="6e273-370">SWIFT-kóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-370">SWIFT code (required)</span></span>          | <span data-ttu-id="6e273-371">Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="6e273-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="6e273-372">Númer útibús (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="6e273-373">Gerð bankareiknings (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-373">Bank account type (required)</span></span>   | <span data-ttu-id="6e273-374">Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="6e273-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="6e273-375">Studd gildi innihalda **Athugun** og **Launaskrá**.</span><span class="sxs-lookup"><span data-stu-id="6e273-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="6e273-376">Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka.</span><span class="sxs-lookup"><span data-stu-id="6e273-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="6e273-377">Allir aðrir reikningar eru hunsaðir.</span><span class="sxs-lookup"><span data-stu-id="6e273-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="6e273-378">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="6e273-378">Address information</span></span>

<span data-ttu-id="6e273-379">Sérhver starfsmaður verður að hafa eina aðalstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="6e273-379">Every employee must have one primary location.</span></span> <span data-ttu-id="6e273-380">Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="6e273-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="6e273-381">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-381">Primary (required)</span></span>
- <span data-ttu-id="6e273-382">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-382">Country/region (required)</span></span>
- <span data-ttu-id="6e273-383">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="6e273-384">Gata (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-384">Street (required)</span></span>
- <span data-ttu-id="6e273-385">Götunúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-385">Street Number (required)</span></span>
- <span data-ttu-id="6e273-386">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="6e273-386">Building Complement</span></span>
- <span data-ttu-id="6e273-387">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-387">City (required)</span></span>
- <span data-ttu-id="6e273-388">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-388">State (required)</span></span>
- <span data-ttu-id="6e273-389">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="6e273-390">Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada</span><span class="sxs-lookup"><span data-stu-id="6e273-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="6e273-391">Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="6e273-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="6e273-392">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="6e273-392">Departments are required on positions.</span></span>
- <span data-ttu-id="6e273-393">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="6e273-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="6e273-394">Þú getur stillt Human Resources til að krefjast þess að stöður tilgreini deild.</span><span class="sxs-lookup"><span data-stu-id="6e273-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="6e273-395">Til að gera þetta skal fara í **Samnýttar stöður mannauðs > Stöður > Krefjast deilda á stöðum**.</span><span class="sxs-lookup"><span data-stu-id="6e273-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="6e273-396">Við mælum með að þessari stillingu sé framfylgt fyrir samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="6e273-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="6e273-397">Starfsgerðir</span><span class="sxs-lookup"><span data-stu-id="6e273-397">Job types</span></span>

<span data-ttu-id="6e273-398">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="6e273-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="6e273-399">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="6e273-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="6e273-400">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="6e273-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="6e273-401">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="6e273-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="6e273-402">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6e273-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="6e273-403">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="6e273-403">Job type</span></span>   | <span data-ttu-id="6e273-404">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="6e273-405">Tímar</span><span class="sxs-lookup"><span data-stu-id="6e273-405">Hourly</span></span>     | <span data-ttu-id="6e273-406">Tímar</span><span class="sxs-lookup"><span data-stu-id="6e273-406">Hourly</span></span>      |
| <span data-ttu-id="6e273-407">Föst laun</span><span class="sxs-lookup"><span data-stu-id="6e273-407">Salaried</span></span>   | <span data-ttu-id="6e273-408">Föst laun</span><span class="sxs-lookup"><span data-stu-id="6e273-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="6e273-409">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="6e273-409">Position types</span></span> 

<span data-ttu-id="6e273-410">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="6e273-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="6e273-411">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="6e273-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="6e273-412">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6e273-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="6e273-413">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="6e273-413">Position type</span></span>   | <span data-ttu-id="6e273-414">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="6e273-415">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="6e273-415">Full-time</span></span>       | <span data-ttu-id="6e273-416">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="6e273-416">Full time employee</span></span> |
| <span data-ttu-id="6e273-417">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="6e273-417">Part-time</span></span>       | <span data-ttu-id="6e273-418">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="6e273-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="6e273-419">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-419">Reason codes</span></span>

<span data-ttu-id="6e273-420">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="6e273-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="6e273-421">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="6e273-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="6e273-422">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6e273-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="6e273-423">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="6e273-423">Reason code</span></span>    | <span data-ttu-id="6e273-424">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-424">Description</span></span>      | <span data-ttu-id="6e273-425">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="6e273-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="6e273-426">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="6e273-426">RESIGNATION</span></span>    | <span data-ttu-id="6e273-427">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="6e273-427">Resignation</span></span>      | <span data-ttu-id="6e273-428">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-428">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-429">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="6e273-429">TERMINATION</span></span>    | <span data-ttu-id="6e273-430">Lok</span><span class="sxs-lookup"><span data-stu-id="6e273-430">Termination</span></span>      | <span data-ttu-id="6e273-431">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-431">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-432">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="6e273-432">RETIREMENT</span></span>     | <span data-ttu-id="6e273-433">Starfslok</span><span class="sxs-lookup"><span data-stu-id="6e273-433">Retirement</span></span>       | <span data-ttu-id="6e273-434">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-434">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-435">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="6e273-435">OTHER</span></span>          | <span data-ttu-id="6e273-436">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="6e273-436">Other Reasons</span></span>    | <span data-ttu-id="6e273-437">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-437">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-438">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="6e273-438">DEATH</span></span>          | <span data-ttu-id="6e273-439">Dauði</span><span class="sxs-lookup"><span data-stu-id="6e273-439">Death</span></span>            | <span data-ttu-id="6e273-440">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-440">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-441">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="6e273-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="6e273-442">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="6e273-442">Leave of Absence</span></span> | <span data-ttu-id="6e273-443">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-443">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-444">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="6e273-444">CONTRACTEND</span></span>    | <span data-ttu-id="6e273-445">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="6e273-445">End of Contract</span></span>  | <span data-ttu-id="6e273-446">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-446">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-447">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="6e273-447">SALARYCHANGE</span></span>   | <span data-ttu-id="6e273-448">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="6e273-448">Change of Salary</span></span> | <span data-ttu-id="6e273-449">Laun</span><span class="sxs-lookup"><span data-stu-id="6e273-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="6e273-450">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="6e273-450">Marital status</span></span>

<span data-ttu-id="6e273-451">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6e273-452">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="6e273-453">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-453">Human Resources</span></span>                 | <span data-ttu-id="6e273-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="6e273-455">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="6e273-455">Married</span></span>                | <span data-ttu-id="6e273-456">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="6e273-456">Married</span></span>              |
| <span data-ttu-id="6e273-457">Ein</span><span class="sxs-lookup"><span data-stu-id="6e273-457">Single</span></span>                 | <span data-ttu-id="6e273-458">Ein</span><span class="sxs-lookup"><span data-stu-id="6e273-458">Single</span></span>               |
| <span data-ttu-id="6e273-459">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="6e273-459">Widowed</span></span>                | <span data-ttu-id="6e273-460">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="6e273-460">Widowed</span></span>              |
| <span data-ttu-id="6e273-461">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="6e273-461">Divorced</span></span>               | <span data-ttu-id="6e273-462">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="6e273-462">Divorced</span></span>             |
| <span data-ttu-id="6e273-463">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="6e273-463">Registered Partnership</span></span> | <span data-ttu-id="6e273-464">Sambúð</span><span class="sxs-lookup"><span data-stu-id="6e273-464">Domestic Partnership</span></span> |
| <span data-ttu-id="6e273-465">None</span><span class="sxs-lookup"><span data-stu-id="6e273-465">None</span></span>                   | <span data-ttu-id="6e273-466">None</span><span class="sxs-lookup"><span data-stu-id="6e273-466">None</span></span>                 |
| <span data-ttu-id="6e273-467">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="6e273-467">Cohabiting</span></span>             | <span data-ttu-id="6e273-468">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="6e273-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="6e273-469">Kyn</span><span class="sxs-lookup"><span data-stu-id="6e273-469">Gender</span></span>

<span data-ttu-id="6e273-470">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6e273-471">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="6e273-472">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-472">Human Resources</span></span>       | <span data-ttu-id="6e273-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="6e273-474">Karl</span><span class="sxs-lookup"><span data-stu-id="6e273-474">Male</span></span>         | <span data-ttu-id="6e273-475">Karl</span><span class="sxs-lookup"><span data-stu-id="6e273-475">Male</span></span>            |
| <span data-ttu-id="6e273-476">Kona</span><span class="sxs-lookup"><span data-stu-id="6e273-476">Female</span></span>       | <span data-ttu-id="6e273-477">Kona</span><span class="sxs-lookup"><span data-stu-id="6e273-477">Female</span></span>          |
| <span data-ttu-id="6e273-478">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="6e273-478">Non-specific</span></span> | <span data-ttu-id="6e273-479">*Ekki stutt*</span><span class="sxs-lookup"><span data-stu-id="6e273-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="6e273-480">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-480">Earning codes</span></span>

<span data-ttu-id="6e273-481">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="6e273-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6e273-482">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="6e273-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="6e273-483">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="6e273-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="6e273-484">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="6e273-484">Supported frequencies</span></span>

- <span data-ttu-id="6e273-485">Allir</span><span class="sxs-lookup"><span data-stu-id="6e273-485">All</span></span>
- <span data-ttu-id="6e273-486">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="6e273-486">EVERYPAY</span></span>
- <span data-ttu-id="6e273-487">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="6e273-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="6e273-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="6e273-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="6e273-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="6e273-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="6e273-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-490">1OFMTH</span></span>
- <span data-ttu-id="6e273-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-491">LASTOFMTH</span></span>
- <span data-ttu-id="6e273-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-492">2OFMTH</span></span>
- <span data-ttu-id="6e273-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-493">3OFMTH</span></span>
- <span data-ttu-id="6e273-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-494">4OFMTH</span></span>
- <span data-ttu-id="6e273-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-495">5OFMTH</span></span>
- <span data-ttu-id="6e273-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-496">1N2OFMTH</span></span>
- <span data-ttu-id="6e273-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-497">3N4OFMTH</span></span>
- <span data-ttu-id="6e273-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-498">1N3OFMTH</span></span>
- <span data-ttu-id="6e273-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-499">1N4OFMTH</span></span>
- <span data-ttu-id="6e273-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-500">2N3OFMTH</span></span>
- <span data-ttu-id="6e273-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-501">2N4OFMTH</span></span>
- <span data-ttu-id="6e273-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="6e273-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="6e273-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="6e273-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="6e273-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="6e273-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="6e273-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="6e273-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="6e273-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="6e273-509">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="6e273-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="6e273-510">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="6e273-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="6e273-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="6e273-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="6e273-512">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6e273-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="6e273-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6e273-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="6e273-514">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="6e273-514">Addresses</span></span>

<span data-ttu-id="6e273-515">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="6e273-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="6e273-516">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="6e273-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="6e273-517">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-517">Human Resources</span></span>          | <span data-ttu-id="6e273-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="6e273-519">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="6e273-519">Country/Region</span></span>  | <span data-ttu-id="6e273-520">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-520">Country Code</span></span>          |
| <span data-ttu-id="6e273-521">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-521">Zip/Postal Code</span></span> | <span data-ttu-id="6e273-522">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-522">Postal Code</span></span>           |
| <span data-ttu-id="6e273-523">Ríki</span><span class="sxs-lookup"><span data-stu-id="6e273-523">State</span></span>           | <span data-ttu-id="6e273-524">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="6e273-524">State Code</span></span>            |
| <span data-ttu-id="6e273-525">Póststöð</span><span class="sxs-lookup"><span data-stu-id="6e273-525">City</span></span>            | <span data-ttu-id="6e273-526">Póststöð</span><span class="sxs-lookup"><span data-stu-id="6e273-526">City</span></span>                  |
| <span data-ttu-id="6e273-527">Sýsla</span><span class="sxs-lookup"><span data-stu-id="6e273-527">County</span></span>          | <span data-ttu-id="6e273-528">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="6e273-528">County (Municipality)</span></span> |
| <span data-ttu-id="6e273-529">Gata</span><span class="sxs-lookup"><span data-stu-id="6e273-529">Street</span></span>          | <span data-ttu-id="6e273-530">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="6e273-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="6e273-531">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="6e273-531">Tax regions</span></span>

<span data-ttu-id="6e273-532">Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="6e273-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="6e273-533">Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="6e273-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="6e273-534">Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="6e273-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="6e273-535">Skattumdæmi (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-535">Tax region (required)</span></span>
- <span data-ttu-id="6e273-536">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-536">Country/Region (required)</span></span>
- <span data-ttu-id="6e273-537">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-537">State (required)</span></span>
- <span data-ttu-id="6e273-538">Sýsla</span><span class="sxs-lookup"><span data-stu-id="6e273-538">County</span></span> 
- <span data-ttu-id="6e273-539">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="6e273-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="6e273-540">Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="6e273-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="6e273-541">Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="6e273-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="6e273-542">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="6e273-542">Departments are required on positions.</span></span>
- <span data-ttu-id="6e273-543">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="6e273-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="6e273-544">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="6e273-544">Job types</span></span>

<span data-ttu-id="6e273-545">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="6e273-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="6e273-546">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="6e273-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="6e273-547">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="6e273-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="6e273-548">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="6e273-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="6e273-549">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6e273-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="6e273-550">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="6e273-550">Job type</span></span>   | <span data-ttu-id="6e273-551">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="6e273-552">Tímar</span><span class="sxs-lookup"><span data-stu-id="6e273-552">Hourly</span></span>     | <span data-ttu-id="6e273-553">MX tímakaup</span><span class="sxs-lookup"><span data-stu-id="6e273-553">MX Hourly</span></span>   |
| <span data-ttu-id="6e273-554">Föst laun</span><span class="sxs-lookup"><span data-stu-id="6e273-554">Salaried</span></span>   | <span data-ttu-id="6e273-555">MX föst laun</span><span class="sxs-lookup"><span data-stu-id="6e273-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="6e273-556">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="6e273-556">Position types</span></span> 

<span data-ttu-id="6e273-557">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="6e273-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="6e273-558">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="6e273-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="6e273-559">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6e273-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="6e273-560">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="6e273-560">Position type</span></span>   | <span data-ttu-id="6e273-561">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="6e273-562">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="6e273-562">Full-time</span></span>       | <span data-ttu-id="6e273-563">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="6e273-563">Full time employee</span></span> |
| <span data-ttu-id="6e273-564">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="6e273-564">Part-time</span></span>       | <span data-ttu-id="6e273-565">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="6e273-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="6e273-566">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-566">Reason codes</span></span>

<span data-ttu-id="6e273-567">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="6e273-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="6e273-568">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="6e273-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="6e273-569">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6e273-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="6e273-570">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="6e273-570">Reason code</span></span>            | <span data-ttu-id="6e273-571">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-571">Description</span></span>                    | <span data-ttu-id="6e273-572">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="6e273-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="6e273-573">BROTTFÖR Á UNDAN LAUNAGREIÐSLU</span><span class="sxs-lookup"><span data-stu-id="6e273-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="6e273-574">Brottför á undan launum</span><span class="sxs-lookup"><span data-stu-id="6e273-574">Departure before first payroll</span></span> | <span data-ttu-id="6e273-575">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-575">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-576">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="6e273-576">RESIGNATION</span></span>            | <span data-ttu-id="6e273-577">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="6e273-577">Resignation</span></span>                    | <span data-ttu-id="6e273-578">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-578">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-579">LÍFEYRIR</span><span class="sxs-lookup"><span data-stu-id="6e273-579">PENSION</span></span>                | <span data-ttu-id="6e273-580">Lífeyrir</span><span class="sxs-lookup"><span data-stu-id="6e273-580">Pension</span></span>                        | <span data-ttu-id="6e273-581">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-581">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-582">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="6e273-582">TERMINATION</span></span>            | <span data-ttu-id="6e273-583">Lok</span><span class="sxs-lookup"><span data-stu-id="6e273-583">Termination</span></span>                    | <span data-ttu-id="6e273-584">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-584">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-585">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="6e273-585">RETIREMENT</span></span>             | <span data-ttu-id="6e273-586">Starfslok</span><span class="sxs-lookup"><span data-stu-id="6e273-586">Retirement</span></span>                     | <span data-ttu-id="6e273-587">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-587">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-588">FJARVERA</span><span class="sxs-lookup"><span data-stu-id="6e273-588">ABSENTEE</span></span>               | <span data-ttu-id="6e273-589">Fjarvera</span><span class="sxs-lookup"><span data-stu-id="6e273-589">Absentee</span></span>                       | <span data-ttu-id="6e273-590">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-590">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-591">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="6e273-591">OTHER</span></span>                  | <span data-ttu-id="6e273-592">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="6e273-592">Other Reasons</span></span>                  | <span data-ttu-id="6e273-593">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-593">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-594">LOKUN</span><span class="sxs-lookup"><span data-stu-id="6e273-594">CLOSURE</span></span>                | <span data-ttu-id="6e273-595">Viðskiptalokun</span><span class="sxs-lookup"><span data-stu-id="6e273-595">Business Closure</span></span>               | <span data-ttu-id="6e273-596">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-596">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-597">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="6e273-597">DEATH</span></span>                  | <span data-ttu-id="6e273-598">Dauði</span><span class="sxs-lookup"><span data-stu-id="6e273-598">Death</span></span>                          | <span data-ttu-id="6e273-599">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-599">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-600">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="6e273-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="6e273-601">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="6e273-601">Leave of Absence</span></span>               | <span data-ttu-id="6e273-602">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-602">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-603">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="6e273-603">CONTRACTEND</span></span>            | <span data-ttu-id="6e273-604">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="6e273-604">End of Contract</span></span>                | <span data-ttu-id="6e273-605">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="6e273-605">Terminate worker</span></span>     |
| <span data-ttu-id="6e273-606">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="6e273-606">SALARYCHANGE</span></span>           | <span data-ttu-id="6e273-607">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="6e273-607">Change of Salary</span></span>               | <span data-ttu-id="6e273-608">Laun</span><span class="sxs-lookup"><span data-stu-id="6e273-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="6e273-609">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="6e273-609">Terms of employment</span></span>

<span data-ttu-id="6e273-610">Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar.</span><span class="sxs-lookup"><span data-stu-id="6e273-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="6e273-611">Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.</span><span class="sxs-lookup"><span data-stu-id="6e273-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="6e273-612">Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6e273-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="6e273-613">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="6e273-613">Terms of employment</span></span>   | <span data-ttu-id="6e273-614">lýsing</span><span class="sxs-lookup"><span data-stu-id="6e273-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="6e273-615">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="6e273-615">Regular</span></span>               | <span data-ttu-id="6e273-616">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="6e273-616">Regular</span></span>     |
| <span data-ttu-id="6e273-617">Beint</span><span class="sxs-lookup"><span data-stu-id="6e273-617">Direct</span></span>                | <span data-ttu-id="6e273-618">Beint</span><span class="sxs-lookup"><span data-stu-id="6e273-618">Direct</span></span>      |
| <span data-ttu-id="6e273-619">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="6e273-619">Internship</span></span>            | <span data-ttu-id="6e273-620">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="6e273-620">Internship</span></span>  |
| <span data-ttu-id="6e273-621">Fast</span><span class="sxs-lookup"><span data-stu-id="6e273-621">Permanent</span></span>             | <span data-ttu-id="6e273-622">Fast</span><span class="sxs-lookup"><span data-stu-id="6e273-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="6e273-623">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="6e273-623">Marital status</span></span>

<span data-ttu-id="6e273-624">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6e273-625">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="6e273-626">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-626">Human Resources</span></span>                 | <span data-ttu-id="6e273-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="6e273-628">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="6e273-628">Married</span></span>                | <span data-ttu-id="6e273-629">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="6e273-629">Married</span></span>                   |
| <span data-ttu-id="6e273-630">Ein</span><span class="sxs-lookup"><span data-stu-id="6e273-630">Single</span></span>                 | <span data-ttu-id="6e273-631">Ein</span><span class="sxs-lookup"><span data-stu-id="6e273-631">Single</span></span>                    |
| <span data-ttu-id="6e273-632">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="6e273-632">Widowed</span></span>                | <span data-ttu-id="6e273-633">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="6e273-633">Widowed</span></span>                   |
| <span data-ttu-id="6e273-634">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="6e273-634">Divorced</span></span>               | <span data-ttu-id="6e273-635">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="6e273-635">Divorced</span></span>                  |
| <span data-ttu-id="6e273-636">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="6e273-636">Registered Partnership</span></span> | <span data-ttu-id="6e273-637">Sambúð</span><span class="sxs-lookup"><span data-stu-id="6e273-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="6e273-638">None</span><span class="sxs-lookup"><span data-stu-id="6e273-638">None</span></span>                   | <span data-ttu-id="6e273-639">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6e273-640">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="6e273-640">Cohabiting</span></span>             | <span data-ttu-id="6e273-641">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="6e273-642">Kyn</span><span class="sxs-lookup"><span data-stu-id="6e273-642">Gender</span></span>

<span data-ttu-id="6e273-643">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6e273-644">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="6e273-645">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-645">Human Resources</span></span>       | <span data-ttu-id="6e273-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="6e273-647">Karl</span><span class="sxs-lookup"><span data-stu-id="6e273-647">Male</span></span>         | <span data-ttu-id="6e273-648">Karl</span><span class="sxs-lookup"><span data-stu-id="6e273-648">Male</span></span>                      |
| <span data-ttu-id="6e273-649">Kona</span><span class="sxs-lookup"><span data-stu-id="6e273-649">Female</span></span>       | <span data-ttu-id="6e273-650">Kona</span><span class="sxs-lookup"><span data-stu-id="6e273-650">Female</span></span>                    |
| <span data-ttu-id="6e273-651">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="6e273-651">Non-specific</span></span> | <span data-ttu-id="6e273-652">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="6e273-653">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="6e273-653">Payment method</span></span>

<span data-ttu-id="6e273-654">Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="6e273-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="6e273-655">Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6e273-656">Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="6e273-657">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-657">Human Resources</span></span>             | <span data-ttu-id="6e273-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="6e273-659">Innlausn</span><span class="sxs-lookup"><span data-stu-id="6e273-659">Cash</span></span>               | <span data-ttu-id="6e273-660">Innlausn</span><span class="sxs-lookup"><span data-stu-id="6e273-660">Cash</span></span>                      |
| <span data-ttu-id="6e273-661">Rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="6e273-661">Electronic Payment</span></span> | <span data-ttu-id="6e273-662">Flutningur</span><span class="sxs-lookup"><span data-stu-id="6e273-662">Transfer</span></span>                  |
| <span data-ttu-id="6e273-663">Villuleit</span><span class="sxs-lookup"><span data-stu-id="6e273-663">Check</span></span>              | <span data-ttu-id="6e273-664">Ávísun</span><span class="sxs-lookup"><span data-stu-id="6e273-664">Cheque</span></span>                    |
| <span data-ttu-id="6e273-665">Bankaávísun</span><span class="sxs-lookup"><span data-stu-id="6e273-665">Bank Draft</span></span>         | <span data-ttu-id="6e273-666">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6e273-667">Annað</span><span class="sxs-lookup"><span data-stu-id="6e273-667">Other</span></span>              | <span data-ttu-id="6e273-668">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="6e273-669">Gerð bankareiknings</span><span class="sxs-lookup"><span data-stu-id="6e273-669">Bank account type</span></span>

<span data-ttu-id="6e273-670">Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="6e273-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="6e273-671">Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga.</span><span class="sxs-lookup"><span data-stu-id="6e273-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="6e273-672">Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="6e273-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="6e273-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-673">Human Resources</span></span>            | <span data-ttu-id="6e273-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="6e273-675">Ávísanareikningur</span><span class="sxs-lookup"><span data-stu-id="6e273-675">Checking Account</span></span>  | <span data-ttu-id="6e273-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="6e273-676">CheckingAccount</span></span>           |
| <span data-ttu-id="6e273-677">Launareikningur</span><span class="sxs-lookup"><span data-stu-id="6e273-677">Payroll Account</span></span>   | <span data-ttu-id="6e273-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="6e273-678">PayrollAccount</span></span>            |
| <span data-ttu-id="6e273-679">Sparnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="6e273-679">Savings Account</span></span>   | <span data-ttu-id="6e273-680">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6e273-681">BankGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="6e273-681">BankGirot account</span></span> | <span data-ttu-id="6e273-682">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6e273-683">PlusGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="6e273-683">PlusGirot account</span></span> | <span data-ttu-id="6e273-684">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="6e273-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="6e273-685">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="6e273-685">Earning codes</span></span>

<span data-ttu-id="6e273-686">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="6e273-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6e273-687">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="6e273-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="6e273-688">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="6e273-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="6e273-689">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="6e273-689">Supported frequencies</span></span>

- <span data-ttu-id="6e273-690">Allir</span><span class="sxs-lookup"><span data-stu-id="6e273-690">All</span></span>
- <span data-ttu-id="6e273-691">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="6e273-691">EVERYPAY</span></span>
- <span data-ttu-id="6e273-692">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="6e273-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="6e273-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="6e273-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="6e273-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="6e273-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="6e273-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-695">1OFMTH</span></span>
- <span data-ttu-id="6e273-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-696">LASTOFMTH</span></span>
- <span data-ttu-id="6e273-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-697">2OFMTH</span></span>
- <span data-ttu-id="6e273-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-698">3OFMTH</span></span>
- <span data-ttu-id="6e273-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-699">4OFMTH</span></span>
- <span data-ttu-id="6e273-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-700">5OFMTH</span></span>
- <span data-ttu-id="6e273-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-701">1N2OFMTH</span></span>
- <span data-ttu-id="6e273-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-702">3N4OFMTH</span></span>
- <span data-ttu-id="6e273-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-703">1N3OFMTH</span></span>
- <span data-ttu-id="6e273-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-704">1N4OFMTH</span></span>
- <span data-ttu-id="6e273-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-705">2N3OFMTH</span></span>
- <span data-ttu-id="6e273-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-706">2N4OFMTH</span></span>
- <span data-ttu-id="6e273-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="6e273-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="6e273-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="6e273-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="6e273-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6e273-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="6e273-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="6e273-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="6e273-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="6e273-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="6e273-714">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="6e273-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="6e273-715">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="6e273-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="6e273-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="6e273-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="6e273-717">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6e273-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="6e273-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6e273-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="6e273-719">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="6e273-719">Addresses</span></span>

<span data-ttu-id="6e273-720">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="6e273-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="6e273-721">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="6e273-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="6e273-722">Mannauður</span><span class="sxs-lookup"><span data-stu-id="6e273-722">Human Resources</span></span>              | <span data-ttu-id="6e273-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6e273-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="6e273-724">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="6e273-724">Country/Region</span></span>      | <span data-ttu-id="6e273-725">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-725">Country Code</span></span>          |
| <span data-ttu-id="6e273-726">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-726">Zip/Postal Code</span></span>     | <span data-ttu-id="6e273-727">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-727">Postal Code</span></span>           |
| <span data-ttu-id="6e273-728">Ríki</span><span class="sxs-lookup"><span data-stu-id="6e273-728">State</span></span>               | <span data-ttu-id="6e273-729">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="6e273-729">State Code</span></span>            |
| <span data-ttu-id="6e273-730">Póststöð</span><span class="sxs-lookup"><span data-stu-id="6e273-730">City</span></span>                | <span data-ttu-id="6e273-731">Póststöð</span><span class="sxs-lookup"><span data-stu-id="6e273-731">City</span></span>                  |
| <span data-ttu-id="6e273-732">Sýsla</span><span class="sxs-lookup"><span data-stu-id="6e273-732">County</span></span>              | <span data-ttu-id="6e273-733">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="6e273-733">County (Municipality)</span></span> |
| <span data-ttu-id="6e273-734">Gata</span><span class="sxs-lookup"><span data-stu-id="6e273-734">Street</span></span>              | <span data-ttu-id="6e273-735">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="6e273-735">Address Line 1</span></span>        |
| <span data-ttu-id="6e273-736">Húsnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-736">Street Number</span></span>       | <span data-ttu-id="6e273-737">Heimilisfang, lína 2</span><span class="sxs-lookup"><span data-stu-id="6e273-737">Address Line 2</span></span>        |
| <span data-ttu-id="6e273-738">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="6e273-738">Building Complement</span></span> | <span data-ttu-id="6e273-739">Heimilisfang, lína 5</span><span class="sxs-lookup"><span data-stu-id="6e273-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="6e273-740">Vegabréfsnúmer</span><span class="sxs-lookup"><span data-stu-id="6e273-740">Passport number</span></span>

<span data-ttu-id="6e273-741">Starfsmenn geta gefið upp vegabréfsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="6e273-741">Employees can declare passport information.</span></span> <span data-ttu-id="6e273-742">Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="6e273-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="6e273-743">Gerð auðkennis = „Vegabréf“</span><span class="sxs-lookup"><span data-stu-id="6e273-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="6e273-744">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="6e273-744">Issued Date</span></span>
- <span data-ttu-id="6e273-745">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="6e273-745">Expiration Date</span></span>

<span data-ttu-id="6e273-746">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**.</span><span class="sxs-lookup"><span data-stu-id="6e273-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="6e273-747">Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="6e273-748">Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6e273-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
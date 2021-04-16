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
ms.openlocfilehash: bcb57082a49fc07a4139aa37f9507890ca7ed620
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805083"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="c0ef5-104">Skilgreina samþættingu við Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c0ef5-105">Samþættingin milli Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="c0ef5-106">Nauðsynlegt er að skilgreina samþættinguna bæði í Human Resources og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="c0ef5-107">Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="c0ef5-108">Samþættingin krefst tilgreindra gagna frá Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="c0ef5-109">Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Human Resources á þann hátt sem styður samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="c0ef5-110">Samþættingin notar eftirfarandi víðtæka flokka gagna:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="c0ef5-111">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-111">Human resources data</span></span>
- <span data-ttu-id="c0ef5-112">Launagögn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-112">Compensation data</span></span>
- <span data-ttu-id="c0ef5-113">Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="c0ef5-114">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-114">Worker data</span></span>

<span data-ttu-id="c0ef5-115">Þessi grein fjallar um skrefin sem verður að fylgja til að virkja samþættinginu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="c0ef5-116">Það útskýrir einnig gerð gagna og upplýsingar um skilgreiningar sem samþættingin krefst.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="c0ef5-117">Virkja samþættingu</span><span class="sxs-lookup"><span data-stu-id="c0ef5-117">Enable the integration</span></span>

<span data-ttu-id="c0ef5-118">Í Human Resources er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="c0ef5-119">Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 Finance þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="c0ef5-120">Til að kveikja á samþættingu í Human Resources skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="c0ef5-121">Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="c0ef5-122">Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="c0ef5-123">Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="c0ef5-124">Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="c0ef5-125">Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="c0ef5-126">Hægt er að breyta tíðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="c0ef5-127">Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi greinum Azure:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="c0ef5-128">Um Azure-geymslureikninga</span><span class="sxs-lookup"><span data-stu-id="c0ef5-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="c0ef5-129">Skilgreina tengistrengi Azure-geymslu</span><span class="sxs-lookup"><span data-stu-id="c0ef5-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="c0ef5-130">Tæknilýsing þegar launasamþætting er virk</span><span class="sxs-lookup"><span data-stu-id="c0ef5-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="c0ef5-131">Að kveikja á launasamþættingu hefur aðallega tvennt í för með sér:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="c0ef5-132">Gagnaútflutningsverk sem heitir "Útflutningur launasamþættingar" er búið til.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="c0ef5-133">Þetta verk inniheldur þær einingar og reiti sem þarf fyrir launasamþættinguna.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="c0ef5-134">Til að skoða verkið skaltu fara í **Kerfisstjórnun**, velja reitinn **Gagnastjórnun** og opna síðan gagnaverkið af listanum yfir verk.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="c0ef5-135">Þessi runuvinnsla keyrir gagnaútflutningsverkið, dulkóðar gagnapakkann sem fylgir því og flytur gagnapakkaskrána á SFTP-endastöðina sem er skilgreind á skjánum **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="c0ef5-136">Gagnapakkinn sem er fluttur til SFTP-endastöðvarinnar er dulkóðaður með lykli sem er einkvæmur fyrir pakkann.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="c0ef5-137">Lykillinn er í Azure-lykageymslu er aðeins aðgengileg af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="c0ef5-138">Ekki er hægt að afkóða og skoða innihald gagnapakka.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="c0ef5-139">Ef þú þarft að skoða innihald gagnapakka þarftu að flytja út gagnaverkið „Útflutningur launasamþættingar“ handvirkt, hlaða niður því og opna það síðan.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="c0ef5-140">Handvirkur útflutningur mun ekki beita dulkóðun eða flytja pakkann.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="c0ef5-141">Skilgreina gögnin þín</span><span class="sxs-lookup"><span data-stu-id="c0ef5-141">Configure your data</span></span> 

<span data-ttu-id="c0ef5-142">Til að afgreiða laun þarf að skilgreina mannauðsgögn í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="c0ef5-143">Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="c0ef5-144">Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="c0ef5-145">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="c0ef5-146">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-146">Benefits</span></span> 

<span data-ttu-id="c0ef5-147">Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="c0ef5-148">Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="c0ef5-149">Fríðindaáætlanir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-149">Benefit plans</span></span>

- <span data-ttu-id="c0ef5-150">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-150">Plan (required)</span></span>
- <span data-ttu-id="c0ef5-151">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-151">Type (required)</span></span>
- <span data-ttu-id="c0ef5-152">Áhrif á launaskrá (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-152">Payroll impact (required)</span></span>
- <span data-ttu-id="c0ef5-153">Endurheimta vangoldnar greiðslur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-153">Recover arrears</span></span>
- <span data-ttu-id="c0ef5-154">Frádráttaraðferð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-154">Deduction method</span></span>
- <span data-ttu-id="c0ef5-155">Frádráttarforgangur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-155">Deduction priority</span></span>
- <span data-ttu-id="c0ef5-156">Takmörkunartímabil</span><span class="sxs-lookup"><span data-stu-id="c0ef5-156">Limit period</span></span>
- <span data-ttu-id="c0ef5-157">Takmarka upphæð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="c0ef5-158">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-158">Benefits</span></span>

- <span data-ttu-id="c0ef5-159">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-159">Plan (required)</span></span>
- <span data-ttu-id="c0ef5-160">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-160">Type (required)</span></span>
- <span data-ttu-id="c0ef5-161">Valkostur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-161">Option (required)</span></span>
- <span data-ttu-id="c0ef5-162">Fríðindaauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-162">Benefit ID (required)</span></span>
- <span data-ttu-id="c0ef5-163">Tíðni</span><span class="sxs-lookup"><span data-stu-id="c0ef5-163">Frequency</span></span>
- <span data-ttu-id="c0ef5-164">Grunnur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-164">Basis</span></span>
- <span data-ttu-id="c0ef5-165">Upphæð eða taxti</span><span class="sxs-lookup"><span data-stu-id="c0ef5-165">Amount or rate</span></span>
- <span data-ttu-id="c0ef5-166">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="c0ef5-167">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-167">Supported frequencies</span></span> 

- <span data-ttu-id="c0ef5-168">Vikulega</span><span class="sxs-lookup"><span data-stu-id="c0ef5-168">Weekly</span></span>
- <span data-ttu-id="c0ef5-169">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c0ef5-169">Bi-weekly</span></span>
- <span data-ttu-id="c0ef5-170">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c0ef5-170">Semi-monthly</span></span>
- <span data-ttu-id="c0ef5-171">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c0ef5-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="c0ef5-172">Studdir grunnar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-172">Supported bases</span></span> 

- <span data-ttu-id="c0ef5-173">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-173">Fixed amount</span></span>
- <span data-ttu-id="c0ef5-174">Prósenta af tekjum</span><span class="sxs-lookup"><span data-stu-id="c0ef5-174">Percent of earnings</span></span>
- <span data-ttu-id="c0ef5-175">Virkar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-175">Productive hours</span></span>

<span data-ttu-id="c0ef5-176">Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="c0ef5-177">Val í Human Resources</span><span class="sxs-lookup"><span data-stu-id="c0ef5-177">Selection in Human Resources</span></span>        | <span data-ttu-id="c0ef5-178">Niðurstaða í Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c0ef5-179">Enginn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-179">None</span></span>                       | <span data-ttu-id="c0ef5-180">Enginn frádráttur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="c0ef5-181">Eingöngu frádráttur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-181">Deduction only</span></span>             | <span data-ttu-id="c0ef5-182">Frádráttur starfsmanns er búinn til.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="c0ef5-183">Eingöngu framlag</span><span class="sxs-lookup"><span data-stu-id="c0ef5-183">Contribution only</span></span>          | <span data-ttu-id="c0ef5-184">Frádráttur vinnuveitanda er búinn til.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="c0ef5-185">Frádráttur og framlag</span><span class="sxs-lookup"><span data-stu-id="c0ef5-185">Deduction and contribution</span></span> | <span data-ttu-id="c0ef5-186">Frádrættir starfsmanns og vinnuveitanda eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="c0ef5-187">Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="c0ef5-188">Leggja fram starfskjaraáætlun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="c0ef5-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="c0ef5-189">Stofna ný fríðindi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="c0ef5-190">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="c0ef5-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="c0ef5-191">Skrá og fjarlægja fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="c0ef5-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="c0ef5-192">Laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-192">Compensation</span></span> 

<span data-ttu-id="c0ef5-193">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="c0ef5-194">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="c0ef5-195">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="c0ef5-196">Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="c0ef5-197">Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="c0ef5-198">Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="c0ef5-199">Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="c0ef5-200">Launafyrirkomulag fastra launa stofnað</span><span class="sxs-lookup"><span data-stu-id="c0ef5-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="c0ef5-201">Launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="c0ef5-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="c0ef5-202">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="c0ef5-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="c0ef5-203">Launaútreikningur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="c0ef5-204">Skilgreina launavinnslu og reikna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="c0ef5-205">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="c0ef5-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="c0ef5-206">Skrá starfsmann í launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="c0ef5-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="c0ef5-207">Störf</span><span class="sxs-lookup"><span data-stu-id="c0ef5-207">Jobs</span></span> 

<span data-ttu-id="c0ef5-208">Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="c0ef5-209">Frekari upplýsingar er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c0ef5-210">Setja upp íhluta verks</span><span class="sxs-lookup"><span data-stu-id="c0ef5-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="c0ef5-211">Skilgreina ný störf</span><span class="sxs-lookup"><span data-stu-id="c0ef5-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="c0ef5-212">Stöður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-212">Positions</span></span>

<span data-ttu-id="c0ef5-213">Staða er sérstakt tilvik starfs.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="c0ef5-214">Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="c0ef5-215">Staða er til í deild.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-215">A position exists in a department.</span></span> <span data-ttu-id="c0ef5-216">Einungis einn starfsmaður getur tengst hverri stöðu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="c0ef5-217">Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="c0ef5-218">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-218">Position (required)</span></span>
- <span data-ttu-id="c0ef5-219">Lýsing (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-219">Description (required)</span></span>
- <span data-ttu-id="c0ef5-220">Starf (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-220">Job (required)</span></span>
- <span data-ttu-id="c0ef5-221">Deild (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-221">Department (required)</span></span>
- <span data-ttu-id="c0ef5-222">Stöðugerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-222">Position type (required)</span></span>
- <span data-ttu-id="c0ef5-223">Jafngildi fulls starfs</span><span class="sxs-lookup"><span data-stu-id="c0ef5-223">Full-time equivalent</span></span>
- <span data-ttu-id="c0ef5-224">Reglulegar árlegar vinnustundir (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="c0ef5-225">Greitt eftir lögaðila (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="c0ef5-226">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-226">Pay cycle (required)</span></span>
- <span data-ttu-id="c0ef5-227">Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="c0ef5-228">Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="c0ef5-229">Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="c0ef5-230">Frekari upplýsingar er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c0ef5-231">Vinnuafl skipulagt með notkun deilda, starfa og staða</span><span class="sxs-lookup"><span data-stu-id="c0ef5-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="c0ef5-232">Setja upp stöður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="c0ef5-233">Deildir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-233">Departments</span></span>

<span data-ttu-id="c0ef5-234">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="c0ef5-235">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="c0ef5-236">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="c0ef5-237">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="c0ef5-238">Frekari upplýsingar er hægt að finna í eftirfarandi greinum:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c0ef5-239">Stofnun deildar og tenging hennar við deildastigveldið</span><span class="sxs-lookup"><span data-stu-id="c0ef5-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="c0ef5-240">Skilgreina nýjar deildir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="c0ef5-241">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="c0ef5-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="c0ef5-242">Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="c0ef5-243">Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="c0ef5-244">Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="c0ef5-245">Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="c0ef5-246">Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="c0ef5-247">Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="c0ef5-248">Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="c0ef5-249">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c0ef5-250">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-250">Pay cycle (required)</span></span>
- <span data-ttu-id="c0ef5-251">Tíðni greiðsluferlis (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="c0ef5-252">Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="c0ef5-253">Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="c0ef5-254">Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="c0ef5-255">Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="c0ef5-256">Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="c0ef5-257">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-257">Earning codes</span></span>

<span data-ttu-id="c0ef5-258">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c0ef5-259">Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="c0ef5-260">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c0ef5-261">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-261">Earning Code (required)</span></span>
- <span data-ttu-id="c0ef5-262">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-262">Description</span></span>
- <span data-ttu-id="c0ef5-263">Mælieining</span><span class="sxs-lookup"><span data-stu-id="c0ef5-263">Unit of measure</span></span>
- <span data-ttu-id="c0ef5-264">Framleiðni</span><span class="sxs-lookup"><span data-stu-id="c0ef5-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="c0ef5-265">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-265">Worker data</span></span>

<span data-ttu-id="c0ef5-266">Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="c0ef5-267">Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="c0ef5-268">Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="c0ef5-269">**Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="c0ef5-270">**Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="c0ef5-271">**Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="c0ef5-272">**Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="c0ef5-273">Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="c0ef5-274">Almennar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-274">General information</span></span>

- <span data-ttu-id="c0ef5-275">Númer starfsmanns (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-275">Personnel number (required)</span></span>
- <span data-ttu-id="c0ef5-276">Fornafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-276">First name (required)</span></span>
- <span data-ttu-id="c0ef5-277">Eftirnafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-277">Last name (required)</span></span>
- <span data-ttu-id="c0ef5-278">Millinafn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-278">Middle name</span></span>
- <span data-ttu-id="c0ef5-279">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="c0ef5-279">Seniority date</span></span>
- <span data-ttu-id="c0ef5-280">Þekkt sem</span><span class="sxs-lookup"><span data-stu-id="c0ef5-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="c0ef5-281">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-281">Personal information</span></span>

- <span data-ttu-id="c0ef5-282">Hjúskaparstaða (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-282">Marital status (required)</span></span>
- <span data-ttu-id="c0ef5-283">Fæðingardagur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-283">Birth date (required)</span></span>
- <span data-ttu-id="c0ef5-284">Kyn (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-284">Gender (required)</span></span>
- <span data-ttu-id="c0ef5-285">Einstaklingur sem á við fötlun að stríða</span><span class="sxs-lookup"><span data-stu-id="c0ef5-285">Person with disabilities</span></span>
- <span data-ttu-id="c0ef5-286">Þjóðerni land svæði (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="c0ef5-287">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-287">Address information</span></span>

- <span data-ttu-id="c0ef5-288">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-288">Primary (required)</span></span>
- <span data-ttu-id="c0ef5-289">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-289">Country/region (required)</span></span>
- <span data-ttu-id="c0ef5-290">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-290">Postal code (required)</span></span>
- <span data-ttu-id="c0ef5-291">Götunúmer (krafist) (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="c0ef5-292">Viðbygging (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="c0ef5-293">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-293">City (required)</span></span>
- <span data-ttu-id="c0ef5-294">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-294">State (required)</span></span>
- <span data-ttu-id="c0ef5-295">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="c0ef5-296">Samskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-296">Contact information</span></span> 

- <span data-ttu-id="c0ef5-297">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-297">Primary (required)</span></span>
- <span data-ttu-id="c0ef5-298">Símanúmer tengiliðar (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-298">Contact number (required)</span></span>
- <span data-ttu-id="c0ef5-299">Skráarending</span><span class="sxs-lookup"><span data-stu-id="c0ef5-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="c0ef5-300">Launaupplýsingar og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-300">Payroll information and earning codes</span></span>

<span data-ttu-id="c0ef5-301">Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="c0ef5-302">Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="c0ef5-303">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-303">Earning codes</span></span>

- <span data-ttu-id="c0ef5-304">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-304">Position (required)</span></span>
- <span data-ttu-id="c0ef5-305">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-305">Earning Code (required)</span></span>
- <span data-ttu-id="c0ef5-306">Tíðni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-306">Frequency (required)</span></span>
- <span data-ttu-id="c0ef5-307">Upphæð (áskilin)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="c0ef5-308">Launaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-308">Payroll information</span></span>

- <span data-ttu-id="c0ef5-309">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-309">Payment Method</span></span>
- <span data-ttu-id="c0ef5-310">Efnahagssvæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-310">Economic Region (required)</span></span>
- <span data-ttu-id="c0ef5-311">Kenni fyrir fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="c0ef5-311">Employee Benefits ID</span></span>
- <span data-ttu-id="c0ef5-312">Kennitala (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-312">National ID Number (required)</span></span>
- <span data-ttu-id="c0ef5-313">Hernaðarþjónustunúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-313">Military Service Number</span></span>
- <span data-ttu-id="c0ef5-314">Auðkenni vaktar (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-314">Shift ID (required)</span></span>
- <span data-ttu-id="c0ef5-315">Skattanúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-315">Tax Number (required)</span></span>
- <span data-ttu-id="c0ef5-316">Auðkenni stéttarfélags (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-316">Union ID (required)</span></span>
- <span data-ttu-id="c0ef5-317">Vinnudagskenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-317">Work Day ID (required)</span></span>
- <span data-ttu-id="c0ef5-318">Vinnuleyfisnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="c0ef5-319">Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="c0ef5-320">Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="c0ef5-321">Atvinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-321">Employment details</span></span>

<span data-ttu-id="c0ef5-322">Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="c0ef5-323">Dayforce styður aðeins eina starfsferilsskrá í einu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="c0ef5-324">Upphafsdagsetning ráðningar (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-324">Employment start date (required)</span></span>
- <span data-ttu-id="c0ef5-325">Dagsetning starfsloka</span><span class="sxs-lookup"><span data-stu-id="c0ef5-325">Employment end date</span></span>
- <span data-ttu-id="c0ef5-326">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-326">Start date</span></span>
- <span data-ttu-id="c0ef5-327">Breyttur fyrsti starfsdagur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-327">Adjusted start date</span></span>
- <span data-ttu-id="c0ef5-328">Dagsetning starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="c0ef5-329">Ástæða starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="c0ef5-330">Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="c0ef5-331">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-331">Human Resources</span></span>                | <span data-ttu-id="c0ef5-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ef5-333">Nýlegasti ráðningardagurinn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-333">Most recent hire date</span></span> | <span data-ttu-id="c0ef5-334">Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="c0ef5-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c0ef5-335">Starfslokadagur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-335">Termination date</span></span>      | <span data-ttu-id="c0ef5-336">Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="c0ef5-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c0ef5-337">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-337">Start date</span></span>            | <span data-ttu-id="c0ef5-338">Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="c0ef5-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="c0ef5-339">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="c0ef5-339">Original hire date</span></span>    | <span data-ttu-id="c0ef5-340">Upphaf ráðningar fyrir elsta atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="c0ef5-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="c0ef5-341">Laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-341">Compensation</span></span>

<span data-ttu-id="c0ef5-342">Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="c0ef5-343">Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="c0ef5-344">Gildisdagsetning (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-344">Effective Date (required)</span></span>
- <span data-ttu-id="c0ef5-345">Gildistími</span><span class="sxs-lookup"><span data-stu-id="c0ef5-345">Expiration date</span></span>
- <span data-ttu-id="c0ef5-346">Launataxti (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-346">Pay Rate (required)</span></span>
- <span data-ttu-id="c0ef5-347">Umreikningur launataxta (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="c0ef5-348">Árlegt jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="c0ef5-349">Klukkutíma jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="c0ef5-350">Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="c0ef5-351">Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="c0ef5-352">Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="c0ef5-353">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="c0ef5-354">Auðkenni kennitölu</span><span class="sxs-lookup"><span data-stu-id="c0ef5-354">Social Security identifier</span></span> 

<span data-ttu-id="c0ef5-355">Sérhver starfsmaður verður að hafa eitt aðalauðkenni.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="c0ef5-356">Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="c0ef5-357">Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="c0ef5-358">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-358">Primary (required)</span></span>
- <span data-ttu-id="c0ef5-359">Gerð auðkennis = „Kennitala“</span><span class="sxs-lookup"><span data-stu-id="c0ef5-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="c0ef5-360">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="c0ef5-360">Issued Date</span></span>
- <span data-ttu-id="c0ef5-361">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-361">Expiration Date</span></span>

<span data-ttu-id="c0ef5-362">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="c0ef5-363">Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="c0ef5-364">Bankareikningar og útborganir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="c0ef5-365">Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="c0ef5-366">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-366">Human Resources</span></span>                         | <span data-ttu-id="c0ef5-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ef5-368">Bankareikningsnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="c0ef5-369">SWIFT-kóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-369">SWIFT code (required)</span></span>          | <span data-ttu-id="c0ef5-370">Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="c0ef5-371">Númer útibús (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="c0ef5-372">Gerð bankareiknings (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-372">Bank account type (required)</span></span>   | <span data-ttu-id="c0ef5-373">Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="c0ef5-374">Studd gildi innihalda **Athugun** og **Launaskrá**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="c0ef5-375">Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="c0ef5-376">Allir aðrir reikningar eru hunsaðir.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="c0ef5-377">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-377">Address information</span></span>

<span data-ttu-id="c0ef5-378">Sérhver starfsmaður verður að hafa eina aðalstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-378">Every employee must have one primary location.</span></span> <span data-ttu-id="c0ef5-379">Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="c0ef5-380">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-380">Primary (required)</span></span>
- <span data-ttu-id="c0ef5-381">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-381">Country/region (required)</span></span>
- <span data-ttu-id="c0ef5-382">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="c0ef5-383">Gata (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-383">Street (required)</span></span>
- <span data-ttu-id="c0ef5-384">Götunúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-384">Street Number (required)</span></span>
- <span data-ttu-id="c0ef5-385">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="c0ef5-385">Building Complement</span></span>
- <span data-ttu-id="c0ef5-386">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-386">City (required)</span></span>
- <span data-ttu-id="c0ef5-387">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-387">State (required)</span></span>
- <span data-ttu-id="c0ef5-388">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="c0ef5-389">Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada</span><span class="sxs-lookup"><span data-stu-id="c0ef5-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="c0ef5-390">Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="c0ef5-391">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-391">Departments are required on positions.</span></span>
- <span data-ttu-id="c0ef5-392">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="c0ef5-393">Þú getur stillt Human Resources til að krefjast þess að stöður tilgreini deild.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="c0ef5-394">Til að gera þetta skal fara í **Samnýttar stöður mannauðs > Stöður > Krefjast deilda á stöðum**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="c0ef5-395">Við mælum með að þessari stillingu sé framfylgt fyrir samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="c0ef5-396">Starfsgerðir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-396">Job types</span></span>

<span data-ttu-id="c0ef5-397">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c0ef5-398">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="c0ef5-399">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c0ef5-400">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c0ef5-401">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c0ef5-402">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-402">Job type</span></span>   | <span data-ttu-id="c0ef5-403">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c0ef5-404">Tímar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-404">Hourly</span></span>     | <span data-ttu-id="c0ef5-405">Tímar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-405">Hourly</span></span>      |
| <span data-ttu-id="c0ef5-406">Föst laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-406">Salaried</span></span>   | <span data-ttu-id="c0ef5-407">Föst laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="c0ef5-408">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-408">Position types</span></span> 

<span data-ttu-id="c0ef5-409">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c0ef5-410">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c0ef5-411">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c0ef5-412">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="c0ef5-412">Position type</span></span>   | <span data-ttu-id="c0ef5-413">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c0ef5-414">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="c0ef5-414">Full-time</span></span>       | <span data-ttu-id="c0ef5-415">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-415">Full time employee</span></span> |
| <span data-ttu-id="c0ef5-416">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="c0ef5-416">Part-time</span></span>       | <span data-ttu-id="c0ef5-417">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c0ef5-418">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-418">Reason codes</span></span>

<span data-ttu-id="c0ef5-419">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c0ef5-420">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c0ef5-421">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c0ef5-422">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-422">Reason code</span></span>    | <span data-ttu-id="c0ef5-423">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-423">Description</span></span>      | <span data-ttu-id="c0ef5-424">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="c0ef5-425">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="c0ef5-425">RESIGNATION</span></span>    | <span data-ttu-id="c0ef5-426">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-426">Resignation</span></span>      | <span data-ttu-id="c0ef5-427">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-427">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-428">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="c0ef5-428">TERMINATION</span></span>    | <span data-ttu-id="c0ef5-429">Lok</span><span class="sxs-lookup"><span data-stu-id="c0ef5-429">Termination</span></span>      | <span data-ttu-id="c0ef5-430">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-430">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-431">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="c0ef5-431">RETIREMENT</span></span>     | <span data-ttu-id="c0ef5-432">Starfslok</span><span class="sxs-lookup"><span data-stu-id="c0ef5-432">Retirement</span></span>       | <span data-ttu-id="c0ef5-433">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-433">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-434">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="c0ef5-434">OTHER</span></span>          | <span data-ttu-id="c0ef5-435">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-435">Other Reasons</span></span>    | <span data-ttu-id="c0ef5-436">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-436">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-437">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="c0ef5-437">DEATH</span></span>          | <span data-ttu-id="c0ef5-438">Dauði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-438">Death</span></span>            | <span data-ttu-id="c0ef5-439">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-439">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-440">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="c0ef5-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="c0ef5-441">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-441">Leave of Absence</span></span> | <span data-ttu-id="c0ef5-442">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-442">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-443">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="c0ef5-443">CONTRACTEND</span></span>    | <span data-ttu-id="c0ef5-444">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-444">End of Contract</span></span>  | <span data-ttu-id="c0ef5-445">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-445">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-446">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-446">SALARYCHANGE</span></span>   | <span data-ttu-id="c0ef5-447">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="c0ef5-447">Change of Salary</span></span> | <span data-ttu-id="c0ef5-448">Laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="c0ef5-449">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="c0ef5-449">Marital status</span></span>

<span data-ttu-id="c0ef5-450">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0ef5-451">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0ef5-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-452">Human Resources</span></span>                 | <span data-ttu-id="c0ef5-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="c0ef5-454">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-454">Married</span></span>                | <span data-ttu-id="c0ef5-455">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-455">Married</span></span>              |
| <span data-ttu-id="c0ef5-456">Ein</span><span class="sxs-lookup"><span data-stu-id="c0ef5-456">Single</span></span>                 | <span data-ttu-id="c0ef5-457">Ein</span><span class="sxs-lookup"><span data-stu-id="c0ef5-457">Single</span></span>               |
| <span data-ttu-id="c0ef5-458">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c0ef5-458">Widowed</span></span>                | <span data-ttu-id="c0ef5-459">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c0ef5-459">Widowed</span></span>              |
| <span data-ttu-id="c0ef5-460">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-460">Divorced</span></span>               | <span data-ttu-id="c0ef5-461">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-461">Divorced</span></span>             |
| <span data-ttu-id="c0ef5-462">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="c0ef5-462">Registered Partnership</span></span> | <span data-ttu-id="c0ef5-463">Sambúð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-463">Domestic Partnership</span></span> |
| <span data-ttu-id="c0ef5-464">None</span><span class="sxs-lookup"><span data-stu-id="c0ef5-464">None</span></span>                   | <span data-ttu-id="c0ef5-465">None</span><span class="sxs-lookup"><span data-stu-id="c0ef5-465">None</span></span>                 |
| <span data-ttu-id="c0ef5-466">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-466">Cohabiting</span></span>             | <span data-ttu-id="c0ef5-467">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="c0ef5-468">Kyn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-468">Gender</span></span>

<span data-ttu-id="c0ef5-469">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0ef5-470">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0ef5-471">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-471">Human Resources</span></span>       | <span data-ttu-id="c0ef5-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="c0ef5-473">Karl</span><span class="sxs-lookup"><span data-stu-id="c0ef5-473">Male</span></span>         | <span data-ttu-id="c0ef5-474">Karl</span><span class="sxs-lookup"><span data-stu-id="c0ef5-474">Male</span></span>            |
| <span data-ttu-id="c0ef5-475">Kona</span><span class="sxs-lookup"><span data-stu-id="c0ef5-475">Female</span></span>       | <span data-ttu-id="c0ef5-476">Kona</span><span class="sxs-lookup"><span data-stu-id="c0ef5-476">Female</span></span>          |
| <span data-ttu-id="c0ef5-477">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="c0ef5-477">Non-specific</span></span> | <span data-ttu-id="c0ef5-478">*Ekki stutt*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c0ef5-479">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-479">Earning codes</span></span>

<span data-ttu-id="c0ef5-480">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c0ef5-481">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c0ef5-482">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c0ef5-483">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-483">Supported frequencies</span></span>

- <span data-ttu-id="c0ef5-484">Allir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-484">All</span></span>
- <span data-ttu-id="c0ef5-485">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-485">EVERYPAY</span></span>
- <span data-ttu-id="c0ef5-486">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="c0ef5-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c0ef5-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c0ef5-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c0ef5-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c0ef5-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c0ef5-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-489">1OFMTH</span></span>
- <span data-ttu-id="c0ef5-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-490">LASTOFMTH</span></span>
- <span data-ttu-id="c0ef5-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-491">2OFMTH</span></span>
- <span data-ttu-id="c0ef5-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-492">3OFMTH</span></span>
- <span data-ttu-id="c0ef5-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-493">4OFMTH</span></span>
- <span data-ttu-id="c0ef5-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-494">5OFMTH</span></span>
- <span data-ttu-id="c0ef5-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-495">1N2OFMTH</span></span>
- <span data-ttu-id="c0ef5-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-496">3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-497">1N3OFMTH</span></span>
- <span data-ttu-id="c0ef5-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-498">1N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-499">2N3OFMTH</span></span>
- <span data-ttu-id="c0ef5-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-500">2N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="c0ef5-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c0ef5-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c0ef5-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c0ef5-508">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c0ef5-509">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c0ef5-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c0ef5-511">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c0ef5-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c0ef5-513">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-513">Addresses</span></span>

<span data-ttu-id="c0ef5-514">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c0ef5-515">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c0ef5-516">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-516">Human Resources</span></span>          | <span data-ttu-id="c0ef5-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="c0ef5-518">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-518">Country/Region</span></span>  | <span data-ttu-id="c0ef5-519">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-519">Country Code</span></span>          |
| <span data-ttu-id="c0ef5-520">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-520">Zip/Postal Code</span></span> | <span data-ttu-id="c0ef5-521">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-521">Postal Code</span></span>           |
| <span data-ttu-id="c0ef5-522">Ríki</span><span class="sxs-lookup"><span data-stu-id="c0ef5-522">State</span></span>           | <span data-ttu-id="c0ef5-523">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-523">State Code</span></span>            |
| <span data-ttu-id="c0ef5-524">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-524">City</span></span>            | <span data-ttu-id="c0ef5-525">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-525">City</span></span>                  |
| <span data-ttu-id="c0ef5-526">Sýsla</span><span class="sxs-lookup"><span data-stu-id="c0ef5-526">County</span></span>          | <span data-ttu-id="c0ef5-527">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-527">County (Municipality)</span></span> |
| <span data-ttu-id="c0ef5-528">Gata</span><span class="sxs-lookup"><span data-stu-id="c0ef5-528">Street</span></span>          | <span data-ttu-id="c0ef5-529">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="c0ef5-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="c0ef5-530">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-530">Tax regions</span></span>

<span data-ttu-id="c0ef5-531">Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="c0ef5-532">Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="c0ef5-533">Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="c0ef5-534">Skattumdæmi (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-534">Tax region (required)</span></span>
- <span data-ttu-id="c0ef5-535">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-535">Country/Region (required)</span></span>
- <span data-ttu-id="c0ef5-536">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-536">State (required)</span></span>
- <span data-ttu-id="c0ef5-537">Sýsla</span><span class="sxs-lookup"><span data-stu-id="c0ef5-537">County</span></span> 
- <span data-ttu-id="c0ef5-538">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="c0ef5-539">Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="c0ef5-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="c0ef5-540">Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="c0ef5-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="c0ef5-541">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-541">Departments are required on positions.</span></span>
- <span data-ttu-id="c0ef5-542">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="c0ef5-543">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-543">Job types</span></span>

<span data-ttu-id="c0ef5-544">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c0ef5-545">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="c0ef5-546">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c0ef5-547">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c0ef5-548">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c0ef5-549">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-549">Job type</span></span>   | <span data-ttu-id="c0ef5-550">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c0ef5-551">Tímar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-551">Hourly</span></span>     | <span data-ttu-id="c0ef5-552">MX tímakaup</span><span class="sxs-lookup"><span data-stu-id="c0ef5-552">MX Hourly</span></span>   |
| <span data-ttu-id="c0ef5-553">Föst laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-553">Salaried</span></span>   | <span data-ttu-id="c0ef5-554">MX föst laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="c0ef5-555">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-555">Position types</span></span> 

<span data-ttu-id="c0ef5-556">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c0ef5-557">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c0ef5-558">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c0ef5-559">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="c0ef5-559">Position type</span></span>   | <span data-ttu-id="c0ef5-560">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c0ef5-561">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="c0ef5-561">Full-time</span></span>       | <span data-ttu-id="c0ef5-562">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-562">Full time employee</span></span> |
| <span data-ttu-id="c0ef5-563">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="c0ef5-563">Part-time</span></span>       | <span data-ttu-id="c0ef5-564">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c0ef5-565">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-565">Reason codes</span></span>

<span data-ttu-id="c0ef5-566">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c0ef5-567">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c0ef5-568">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c0ef5-569">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-569">Reason code</span></span>            | <span data-ttu-id="c0ef5-570">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-570">Description</span></span>                    | <span data-ttu-id="c0ef5-571">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="c0ef5-572">BROTTFÖR Á UNDAN LAUNAGREIÐSLU</span><span class="sxs-lookup"><span data-stu-id="c0ef5-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="c0ef5-573">Brottför á undan launum</span><span class="sxs-lookup"><span data-stu-id="c0ef5-573">Departure before first payroll</span></span> | <span data-ttu-id="c0ef5-574">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-574">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-575">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="c0ef5-575">RESIGNATION</span></span>            | <span data-ttu-id="c0ef5-576">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-576">Resignation</span></span>                    | <span data-ttu-id="c0ef5-577">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-577">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-578">LÍFEYRIR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-578">PENSION</span></span>                | <span data-ttu-id="c0ef5-579">Lífeyrir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-579">Pension</span></span>                        | <span data-ttu-id="c0ef5-580">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-580">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-581">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="c0ef5-581">TERMINATION</span></span>            | <span data-ttu-id="c0ef5-582">Lok</span><span class="sxs-lookup"><span data-stu-id="c0ef5-582">Termination</span></span>                    | <span data-ttu-id="c0ef5-583">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-583">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-584">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="c0ef5-584">RETIREMENT</span></span>             | <span data-ttu-id="c0ef5-585">Starfslok</span><span class="sxs-lookup"><span data-stu-id="c0ef5-585">Retirement</span></span>                     | <span data-ttu-id="c0ef5-586">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-586">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-587">FJARVERA</span><span class="sxs-lookup"><span data-stu-id="c0ef5-587">ABSENTEE</span></span>               | <span data-ttu-id="c0ef5-588">Fjarvera</span><span class="sxs-lookup"><span data-stu-id="c0ef5-588">Absentee</span></span>                       | <span data-ttu-id="c0ef5-589">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-589">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-590">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="c0ef5-590">OTHER</span></span>                  | <span data-ttu-id="c0ef5-591">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-591">Other Reasons</span></span>                  | <span data-ttu-id="c0ef5-592">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-592">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-593">LOKUN</span><span class="sxs-lookup"><span data-stu-id="c0ef5-593">CLOSURE</span></span>                | <span data-ttu-id="c0ef5-594">Viðskiptalokun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-594">Business Closure</span></span>               | <span data-ttu-id="c0ef5-595">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-595">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-596">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="c0ef5-596">DEATH</span></span>                  | <span data-ttu-id="c0ef5-597">Dauði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-597">Death</span></span>                          | <span data-ttu-id="c0ef5-598">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-598">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-599">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="c0ef5-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="c0ef5-600">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-600">Leave of Absence</span></span>               | <span data-ttu-id="c0ef5-601">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-601">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-602">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="c0ef5-602">CONTRACTEND</span></span>            | <span data-ttu-id="c0ef5-603">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="c0ef5-603">End of Contract</span></span>                | <span data-ttu-id="c0ef5-604">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c0ef5-604">Terminate worker</span></span>     |
| <span data-ttu-id="c0ef5-605">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-605">SALARYCHANGE</span></span>           | <span data-ttu-id="c0ef5-606">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="c0ef5-606">Change of Salary</span></span>               | <span data-ttu-id="c0ef5-607">Laun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="c0ef5-608">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-608">Terms of employment</span></span>

<span data-ttu-id="c0ef5-609">Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="c0ef5-610">Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="c0ef5-611">Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="c0ef5-612">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-612">Terms of employment</span></span>   | <span data-ttu-id="c0ef5-613">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0ef5-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c0ef5-614">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="c0ef5-614">Regular</span></span>               | <span data-ttu-id="c0ef5-615">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="c0ef5-615">Regular</span></span>     |
| <span data-ttu-id="c0ef5-616">Beint</span><span class="sxs-lookup"><span data-stu-id="c0ef5-616">Direct</span></span>                | <span data-ttu-id="c0ef5-617">Beint</span><span class="sxs-lookup"><span data-stu-id="c0ef5-617">Direct</span></span>      |
| <span data-ttu-id="c0ef5-618">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="c0ef5-618">Internship</span></span>            | <span data-ttu-id="c0ef5-619">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="c0ef5-619">Internship</span></span>  |
| <span data-ttu-id="c0ef5-620">Fast</span><span class="sxs-lookup"><span data-stu-id="c0ef5-620">Permanent</span></span>             | <span data-ttu-id="c0ef5-621">Fast</span><span class="sxs-lookup"><span data-stu-id="c0ef5-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="c0ef5-622">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="c0ef5-622">Marital status</span></span>

<span data-ttu-id="c0ef5-623">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0ef5-624">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0ef5-625">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-625">Human Resources</span></span>                 | <span data-ttu-id="c0ef5-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="c0ef5-627">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-627">Married</span></span>                | <span data-ttu-id="c0ef5-628">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-628">Married</span></span>                   |
| <span data-ttu-id="c0ef5-629">Ein</span><span class="sxs-lookup"><span data-stu-id="c0ef5-629">Single</span></span>                 | <span data-ttu-id="c0ef5-630">Ein</span><span class="sxs-lookup"><span data-stu-id="c0ef5-630">Single</span></span>                    |
| <span data-ttu-id="c0ef5-631">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c0ef5-631">Widowed</span></span>                | <span data-ttu-id="c0ef5-632">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c0ef5-632">Widowed</span></span>                   |
| <span data-ttu-id="c0ef5-633">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-633">Divorced</span></span>               | <span data-ttu-id="c0ef5-634">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-634">Divorced</span></span>                  |
| <span data-ttu-id="c0ef5-635">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="c0ef5-635">Registered Partnership</span></span> | <span data-ttu-id="c0ef5-636">Sambúð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="c0ef5-637">None</span><span class="sxs-lookup"><span data-stu-id="c0ef5-637">None</span></span>                   | <span data-ttu-id="c0ef5-638">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0ef5-639">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-639">Cohabiting</span></span>             | <span data-ttu-id="c0ef5-640">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="c0ef5-641">Kyn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-641">Gender</span></span>

<span data-ttu-id="c0ef5-642">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0ef5-643">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0ef5-644">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-644">Human Resources</span></span>       | <span data-ttu-id="c0ef5-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="c0ef5-646">Karl</span><span class="sxs-lookup"><span data-stu-id="c0ef5-646">Male</span></span>         | <span data-ttu-id="c0ef5-647">Karl</span><span class="sxs-lookup"><span data-stu-id="c0ef5-647">Male</span></span>                      |
| <span data-ttu-id="c0ef5-648">Kona</span><span class="sxs-lookup"><span data-stu-id="c0ef5-648">Female</span></span>       | <span data-ttu-id="c0ef5-649">Kona</span><span class="sxs-lookup"><span data-stu-id="c0ef5-649">Female</span></span>                    |
| <span data-ttu-id="c0ef5-650">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="c0ef5-650">Non-specific</span></span> | <span data-ttu-id="c0ef5-651">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="c0ef5-652">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="c0ef5-652">Payment method</span></span>

<span data-ttu-id="c0ef5-653">Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="c0ef5-654">Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0ef5-655">Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0ef5-656">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-656">Human Resources</span></span>             | <span data-ttu-id="c0ef5-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="c0ef5-658">Innlausn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-658">Cash</span></span>               | <span data-ttu-id="c0ef5-659">Innlausn</span><span class="sxs-lookup"><span data-stu-id="c0ef5-659">Cash</span></span>                      |
| <span data-ttu-id="c0ef5-660">Rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="c0ef5-660">Electronic Payment</span></span> | <span data-ttu-id="c0ef5-661">Flutningur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-661">Transfer</span></span>                  |
| <span data-ttu-id="c0ef5-662">Villuleit</span><span class="sxs-lookup"><span data-stu-id="c0ef5-662">Check</span></span>              | <span data-ttu-id="c0ef5-663">Ávísun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-663">Cheque</span></span>                    |
| <span data-ttu-id="c0ef5-664">Bankaávísun</span><span class="sxs-lookup"><span data-stu-id="c0ef5-664">Bank Draft</span></span>         | <span data-ttu-id="c0ef5-665">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0ef5-666">Annað</span><span class="sxs-lookup"><span data-stu-id="c0ef5-666">Other</span></span>              | <span data-ttu-id="c0ef5-667">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="c0ef5-668">Gerð bankareiknings</span><span class="sxs-lookup"><span data-stu-id="c0ef5-668">Bank account type</span></span>

<span data-ttu-id="c0ef5-669">Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="c0ef5-670">Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="c0ef5-671">Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="c0ef5-672">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-672">Human Resources</span></span>            | <span data-ttu-id="c0ef5-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="c0ef5-674">Ávísanareikningur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-674">Checking Account</span></span>  | <span data-ttu-id="c0ef5-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="c0ef5-675">CheckingAccount</span></span>           |
| <span data-ttu-id="c0ef5-676">Launareikningur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-676">Payroll Account</span></span>   | <span data-ttu-id="c0ef5-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="c0ef5-677">PayrollAccount</span></span>            |
| <span data-ttu-id="c0ef5-678">Sparnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-678">Savings Account</span></span>   | <span data-ttu-id="c0ef5-679">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0ef5-680">BankGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-680">BankGirot account</span></span> | <span data-ttu-id="c0ef5-681">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0ef5-682">PlusGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-682">PlusGirot account</span></span> | <span data-ttu-id="c0ef5-683">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c0ef5-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c0ef5-684">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c0ef5-684">Earning codes</span></span>

<span data-ttu-id="c0ef5-685">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c0ef5-686">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c0ef5-687">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c0ef5-688">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-688">Supported frequencies</span></span>

- <span data-ttu-id="c0ef5-689">Allir</span><span class="sxs-lookup"><span data-stu-id="c0ef5-689">All</span></span>
- <span data-ttu-id="c0ef5-690">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-690">EVERYPAY</span></span>
- <span data-ttu-id="c0ef5-691">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="c0ef5-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c0ef5-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c0ef5-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c0ef5-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c0ef5-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c0ef5-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-694">1OFMTH</span></span>
- <span data-ttu-id="c0ef5-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-695">LASTOFMTH</span></span>
- <span data-ttu-id="c0ef5-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-696">2OFMTH</span></span>
- <span data-ttu-id="c0ef5-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-697">3OFMTH</span></span>
- <span data-ttu-id="c0ef5-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-698">4OFMTH</span></span>
- <span data-ttu-id="c0ef5-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-699">5OFMTH</span></span>
- <span data-ttu-id="c0ef5-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-700">1N2OFMTH</span></span>
- <span data-ttu-id="c0ef5-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-701">3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-702">1N3OFMTH</span></span>
- <span data-ttu-id="c0ef5-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-703">1N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-704">2N3OFMTH</span></span>
- <span data-ttu-id="c0ef5-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-705">2N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="c0ef5-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0ef5-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c0ef5-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c0ef5-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c0ef5-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c0ef5-713">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c0ef5-714">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c0ef5-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c0ef5-716">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c0ef5-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0ef5-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c0ef5-718">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-718">Addresses</span></span>

<span data-ttu-id="c0ef5-719">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c0ef5-720">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c0ef5-721">Mannauður</span><span class="sxs-lookup"><span data-stu-id="c0ef5-721">Human Resources</span></span>              | <span data-ttu-id="c0ef5-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0ef5-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="c0ef5-723">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-723">Country/Region</span></span>      | <span data-ttu-id="c0ef5-724">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-724">Country Code</span></span>          |
| <span data-ttu-id="c0ef5-725">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-725">Zip/Postal Code</span></span>     | <span data-ttu-id="c0ef5-726">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-726">Postal Code</span></span>           |
| <span data-ttu-id="c0ef5-727">Ríki</span><span class="sxs-lookup"><span data-stu-id="c0ef5-727">State</span></span>               | <span data-ttu-id="c0ef5-728">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="c0ef5-728">State Code</span></span>            |
| <span data-ttu-id="c0ef5-729">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-729">City</span></span>                | <span data-ttu-id="c0ef5-730">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c0ef5-730">City</span></span>                  |
| <span data-ttu-id="c0ef5-731">Sýsla</span><span class="sxs-lookup"><span data-stu-id="c0ef5-731">County</span></span>              | <span data-ttu-id="c0ef5-732">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="c0ef5-732">County (Municipality)</span></span> |
| <span data-ttu-id="c0ef5-733">Gata</span><span class="sxs-lookup"><span data-stu-id="c0ef5-733">Street</span></span>              | <span data-ttu-id="c0ef5-734">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="c0ef5-734">Address Line 1</span></span>        |
| <span data-ttu-id="c0ef5-735">Húsnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-735">Street Number</span></span>       | <span data-ttu-id="c0ef5-736">Heimilisfang, lína 2</span><span class="sxs-lookup"><span data-stu-id="c0ef5-736">Address Line 2</span></span>        |
| <span data-ttu-id="c0ef5-737">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="c0ef5-737">Building Complement</span></span> | <span data-ttu-id="c0ef5-738">Heimilisfang, lína 5</span><span class="sxs-lookup"><span data-stu-id="c0ef5-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="c0ef5-739">Vegabréfsnúmer</span><span class="sxs-lookup"><span data-stu-id="c0ef5-739">Passport number</span></span>

<span data-ttu-id="c0ef5-740">Starfsmenn geta gefið upp vegabréfsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-740">Employees can declare passport information.</span></span> <span data-ttu-id="c0ef5-741">Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="c0ef5-742">Gerð auðkennis = „Vegabréf“</span><span class="sxs-lookup"><span data-stu-id="c0ef5-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="c0ef5-743">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="c0ef5-743">Issued Date</span></span>
- <span data-ttu-id="c0ef5-744">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="c0ef5-744">Expiration Date</span></span>

<span data-ttu-id="c0ef5-745">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="c0ef5-746">Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="c0ef5-747">Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0ef5-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
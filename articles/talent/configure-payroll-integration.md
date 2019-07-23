---
title: Skilgreina launasamþættingu milli Talent og Dayforce
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla samþættingu milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce svo hægt sé að afgreiða launakeyrslu.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59234ef44ad22383ae5daf71d4b663c6183e6c05
ms.sourcegitcommit: d599bc1fc60a010c2753ca547219ae21456b1df9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/25/2019
ms.locfileid: "1702819"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="f92a6-103">Skilgreina launasamþættingu milli Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f92a6-104">Samþættingin milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="f92a6-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="f92a6-105">Nauðsynlegt er að skilgreina samþættinguna bæði í Talent og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="f92a6-106">Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Talent.</span><span class="sxs-lookup"><span data-stu-id="f92a6-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="f92a6-107">Samþættingin krefst tilgreindra gagna frá Talent.</span><span class="sxs-lookup"><span data-stu-id="f92a6-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="f92a6-108">Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Talent á þann hátt sem styður samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="f92a6-109">Samþættingin notar eftirfarandi víðtæka flokka gagna:</span><span class="sxs-lookup"><span data-stu-id="f92a6-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="f92a6-110">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="f92a6-110">Human resources data</span></span>
- <span data-ttu-id="f92a6-111">Launagögn</span><span class="sxs-lookup"><span data-stu-id="f92a6-111">Compensation data</span></span>
- <span data-ttu-id="f92a6-112">Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="f92a6-113">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="f92a6-113">Worker data</span></span>

<span data-ttu-id="f92a6-114">Þetta efnisatriði fjallar um skrefin sem verður að fylgja til að virkja samþættinginu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="f92a6-115">Það útskýrir einnig gerð gagna og upplýsingar um skilgreiningar sem samþættingin krefst.</span><span class="sxs-lookup"><span data-stu-id="f92a6-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="f92a6-116">Virkja samþættingu</span><span class="sxs-lookup"><span data-stu-id="f92a6-116">Enable the integration</span></span>

<span data-ttu-id="f92a6-117">Í Talent er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="f92a6-118">Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 for Finance and Operations þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f92a6-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="f92a6-119">Til að kveikja á samþættingu í Talent skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="f92a6-120">Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="f92a6-121">Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.</span><span class="sxs-lookup"><span data-stu-id="f92a6-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="f92a6-122">Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.</span><span class="sxs-lookup"><span data-stu-id="f92a6-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="f92a6-123">Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="f92a6-124">Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt.</span><span class="sxs-lookup"><span data-stu-id="f92a6-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="f92a6-125">Hægt er að breyta tíðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="f92a6-126">Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi efnisatriðum Azure:</span><span class="sxs-lookup"><span data-stu-id="f92a6-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="f92a6-127">Um Azure-geymslureikninga</span><span class="sxs-lookup"><span data-stu-id="f92a6-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="f92a6-128">Skilgreina tengistrengi Azure-geymslu</span><span class="sxs-lookup"><span data-stu-id="f92a6-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="f92a6-129">Tæknilýsing þegar launasamþætting er virk</span><span class="sxs-lookup"><span data-stu-id="f92a6-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="f92a6-130">Að kveikja á launasamþættingu hefur aðallega tvennt í för með sér:</span><span class="sxs-lookup"><span data-stu-id="f92a6-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="f92a6-131">Gagnaútflutningsverk sem heitir "Útflutningur launasamþættingar" er búið til.</span><span class="sxs-lookup"><span data-stu-id="f92a6-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="f92a6-132">Þetta verk inniheldur þær einingar og reiti sem þarf fyrir launasamþættinguna.</span><span class="sxs-lookup"><span data-stu-id="f92a6-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="f92a6-133">Til að skoða verkið skaltu fara í **Kerfisstjórnun**, velja reitinn **Gagnastjórnun** og opna síðan gagnaverkið af listanum yfir verk.</span><span class="sxs-lookup"><span data-stu-id="f92a6-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="f92a6-134">Þessi runuvinnsla keyrir gagnaútflutningsverkið, dulkóðar gagnapakkann sem fylgir því og flytur gagnapakkaskrána á SFTP-endastöðina sem er skilgreind á skjánum **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="f92a6-135">Gagnapakkinn sem er fluttur til SFTP-endastöðvarinnar er dulkóðaður með lykli sem er einkvæmur fyrir pakkann.</span><span class="sxs-lookup"><span data-stu-id="f92a6-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="f92a6-136">Lykillinn er í Azure-lykageymslu er aðeins aðgengileg af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="f92a6-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="f92a6-137">Ekki er hægt að afkóða og skoða innihald gagnapakka.</span><span class="sxs-lookup"><span data-stu-id="f92a6-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="f92a6-138">Ef þú þarft að skoða innihald gagnapakka þarftu að flytja út gagnaverkið „Útflutningur launasamþættingar“ handvirkt, hlaða niður því og opna það síðan.</span><span class="sxs-lookup"><span data-stu-id="f92a6-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="f92a6-139">Handvirkur útflutningur mun ekki beita dulkóðun eða flytja pakkann.</span><span class="sxs-lookup"><span data-stu-id="f92a6-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="f92a6-140">Skilgreina gögnin þín</span><span class="sxs-lookup"><span data-stu-id="f92a6-140">Configure your data</span></span> 

<span data-ttu-id="f92a6-141">Til að afgreiða laun þarf að skilgreina mannauðsgögn í Talent.</span><span class="sxs-lookup"><span data-stu-id="f92a6-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="f92a6-142">Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun.</span><span class="sxs-lookup"><span data-stu-id="f92a6-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="f92a6-143">Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.</span><span class="sxs-lookup"><span data-stu-id="f92a6-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="f92a6-144">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="f92a6-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="f92a6-145">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="f92a6-145">Benefits</span></span> 

<span data-ttu-id="f92a6-146">Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.</span><span class="sxs-lookup"><span data-stu-id="f92a6-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="f92a6-147">Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="f92a6-148">Fríðindaáætlanir</span><span class="sxs-lookup"><span data-stu-id="f92a6-148">Benefit plans</span></span>

- <span data-ttu-id="f92a6-149">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-149">Plan (required)</span></span>
- <span data-ttu-id="f92a6-150">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-150">Type (required)</span></span>
- <span data-ttu-id="f92a6-151">Áhrif á launaskrá (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-151">Payroll impact (required)</span></span>
- <span data-ttu-id="f92a6-152">Endurheimta vangoldnar greiðslur</span><span class="sxs-lookup"><span data-stu-id="f92a6-152">Recover arrears</span></span>
- <span data-ttu-id="f92a6-153">Frádráttaraðferð</span><span class="sxs-lookup"><span data-stu-id="f92a6-153">Deduction method</span></span>
- <span data-ttu-id="f92a6-154">Frádráttarforgangur</span><span class="sxs-lookup"><span data-stu-id="f92a6-154">Deduction priority</span></span>
- <span data-ttu-id="f92a6-155">Takmörkunartímabil</span><span class="sxs-lookup"><span data-stu-id="f92a6-155">Limit period</span></span>
- <span data-ttu-id="f92a6-156">Takmarka upphæð</span><span class="sxs-lookup"><span data-stu-id="f92a6-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="f92a6-157">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="f92a6-157">Benefits</span></span>

- <span data-ttu-id="f92a6-158">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-158">Plan (required)</span></span>
- <span data-ttu-id="f92a6-159">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-159">Type (required)</span></span>
- <span data-ttu-id="f92a6-160">Valkostur (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-160">Option (required)</span></span>
- <span data-ttu-id="f92a6-161">Fríðindaauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-161">Benefit ID (required)</span></span>
- <span data-ttu-id="f92a6-162">Tíðni</span><span class="sxs-lookup"><span data-stu-id="f92a6-162">Frequency</span></span>
- <span data-ttu-id="f92a6-163">Grunnur</span><span class="sxs-lookup"><span data-stu-id="f92a6-163">Basis</span></span>
- <span data-ttu-id="f92a6-164">Upphæð eða taxti</span><span class="sxs-lookup"><span data-stu-id="f92a6-164">Amount or rate</span></span>
- <span data-ttu-id="f92a6-165">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="f92a6-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="f92a6-166">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="f92a6-166">Supported frequencies</span></span> 

- <span data-ttu-id="f92a6-167">Vikulega</span><span class="sxs-lookup"><span data-stu-id="f92a6-167">Weekly</span></span>
- <span data-ttu-id="f92a6-168">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="f92a6-168">Bi-weekly</span></span>
- <span data-ttu-id="f92a6-169">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="f92a6-169">Semi-monthly</span></span>
- <span data-ttu-id="f92a6-170">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="f92a6-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="f92a6-171">Studdir grunnar</span><span class="sxs-lookup"><span data-stu-id="f92a6-171">Supported bases</span></span> 

- <span data-ttu-id="f92a6-172">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="f92a6-172">Fixed amount</span></span>
- <span data-ttu-id="f92a6-173">Prósenta af tekjum</span><span class="sxs-lookup"><span data-stu-id="f92a6-173">Percent of earnings</span></span>
- <span data-ttu-id="f92a6-174">Virkar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="f92a6-174">Productive hours</span></span>

<span data-ttu-id="f92a6-175">Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.</span><span class="sxs-lookup"><span data-stu-id="f92a6-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="f92a6-176">Val í Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-176">Selection in Talent</span></span>        | <span data-ttu-id="f92a6-177">Niðurstaða í Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f92a6-178">None</span><span class="sxs-lookup"><span data-stu-id="f92a6-178">None</span></span>                       | <span data-ttu-id="f92a6-179">Enginn frádráttur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="f92a6-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="f92a6-180">Eingöngu frádráttur</span><span class="sxs-lookup"><span data-stu-id="f92a6-180">Deduction only</span></span>             | <span data-ttu-id="f92a6-181">Frádráttur starfsmanns er búinn til.</span><span class="sxs-lookup"><span data-stu-id="f92a6-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="f92a6-182">Eingöngu framlag</span><span class="sxs-lookup"><span data-stu-id="f92a6-182">Contribution only</span></span>          | <span data-ttu-id="f92a6-183">Frádráttur vinnuveitanda er búinn til.</span><span class="sxs-lookup"><span data-stu-id="f92a6-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="f92a6-184">Frádráttur og framlag</span><span class="sxs-lookup"><span data-stu-id="f92a6-184">Deduction and contribution</span></span> | <span data-ttu-id="f92a6-185">Frádrættir starfsmanns og vinnuveitanda eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="f92a6-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="f92a6-186">Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="f92a6-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="f92a6-187">Leggja fram fríðindaáætlun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="f92a6-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="f92a6-188">Stofna ný fríðindi</span><span class="sxs-lookup"><span data-stu-id="f92a6-188">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="f92a6-189">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="f92a6-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="f92a6-190">Skrá og fjarlægja fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="f92a6-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="f92a6-191">Laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-191">Compensation</span></span> 

<span data-ttu-id="f92a6-192">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="f92a6-193">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="f92a6-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="f92a6-194">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="f92a6-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="f92a6-195">Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="f92a6-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="f92a6-196">Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta.</span><span class="sxs-lookup"><span data-stu-id="f92a6-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="f92a6-197">Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="f92a6-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="f92a6-198">Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="f92a6-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="f92a6-199">Launafyrirkomulag fastra launa stofnað</span><span class="sxs-lookup"><span data-stu-id="f92a6-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="f92a6-200">Launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="f92a6-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="f92a6-201">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="f92a6-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="f92a6-202">Launaútreikningur</span><span class="sxs-lookup"><span data-stu-id="f92a6-202">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="f92a6-203">Skilgreina launavinnslu og reikna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="f92a6-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="f92a6-204">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="f92a6-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="f92a6-205">Skrá starfsmann í launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="f92a6-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="f92a6-206">Störf</span><span class="sxs-lookup"><span data-stu-id="f92a6-206">Jobs</span></span> 

<span data-ttu-id="f92a6-207">Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið.</span><span class="sxs-lookup"><span data-stu-id="f92a6-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="f92a6-208">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="f92a6-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f92a6-209">Setja upp íhluta verks</span><span class="sxs-lookup"><span data-stu-id="f92a6-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="f92a6-210">Skilgreina ný störf</span><span class="sxs-lookup"><span data-stu-id="f92a6-210">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="f92a6-211">Stöður</span><span class="sxs-lookup"><span data-stu-id="f92a6-211">Positions</span></span>

<span data-ttu-id="f92a6-212">Staða er sérstakt tilvik starfs.</span><span class="sxs-lookup"><span data-stu-id="f92a6-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="f92a6-213">Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“.</span><span class="sxs-lookup"><span data-stu-id="f92a6-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="f92a6-214">Staða er til í deild.</span><span class="sxs-lookup"><span data-stu-id="f92a6-214">A position exists in a department.</span></span> <span data-ttu-id="f92a6-215">Einungis einn starfsmaður getur tengst hverri stöðu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="f92a6-216">Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:</span><span class="sxs-lookup"><span data-stu-id="f92a6-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="f92a6-217">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-217">Position (required)</span></span>
- <span data-ttu-id="f92a6-218">Lýsing (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-218">Description (required)</span></span>
- <span data-ttu-id="f92a6-219">Starf (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-219">Job (required)</span></span>
- <span data-ttu-id="f92a6-220">Deild (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-220">Department (required)</span></span>
- <span data-ttu-id="f92a6-221">Stöðugerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-221">Position type (required)</span></span>
- <span data-ttu-id="f92a6-222">Jafngildi fulls starfs</span><span class="sxs-lookup"><span data-stu-id="f92a6-222">Full-time equivalent</span></span>
- <span data-ttu-id="f92a6-223">Reglulegar árlegar vinnustundir (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="f92a6-224">Greitt eftir lögaðila (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="f92a6-225">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-225">Pay cycle (required)</span></span>
- <span data-ttu-id="f92a6-226">Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="f92a6-227">Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="f92a6-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="f92a6-228">Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="f92a6-229">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="f92a6-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f92a6-230">Vinnuafl skipulagt með notkun deilda, starfa og staða</span><span class="sxs-lookup"><span data-stu-id="f92a6-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="f92a6-231">Setja upp stöður</span><span class="sxs-lookup"><span data-stu-id="f92a6-231">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="f92a6-232">Deildir</span><span class="sxs-lookup"><span data-stu-id="f92a6-232">Departments</span></span>

<span data-ttu-id="f92a6-233">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="f92a6-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="f92a6-234">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="f92a6-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="f92a6-235">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="f92a6-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="f92a6-236">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="f92a6-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="f92a6-237">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="f92a6-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f92a6-238">Stofnun deildar og tenging hennar við deildastigveldið</span><span class="sxs-lookup"><span data-stu-id="f92a6-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="f92a6-239">Skilgreina nýjar deildir</span><span class="sxs-lookup"><span data-stu-id="f92a6-239">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="f92a6-240">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="f92a6-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="f92a6-241">Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="f92a6-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="f92a6-242">Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="f92a6-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="f92a6-243">Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur.</span><span class="sxs-lookup"><span data-stu-id="f92a6-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="f92a6-244">Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.</span><span class="sxs-lookup"><span data-stu-id="f92a6-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="f92a6-245">Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli.</span><span class="sxs-lookup"><span data-stu-id="f92a6-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="f92a6-246">Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp.</span><span class="sxs-lookup"><span data-stu-id="f92a6-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="f92a6-247">Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.</span><span class="sxs-lookup"><span data-stu-id="f92a6-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="f92a6-248">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f92a6-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f92a6-249">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-249">Pay cycle (required)</span></span>
- <span data-ttu-id="f92a6-250">Tíðni greiðsluferlis (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="f92a6-251">Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="f92a6-252">Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="f92a6-253">Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="f92a6-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="f92a6-254">Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="f92a6-255">Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Talent.</span><span class="sxs-lookup"><span data-stu-id="f92a6-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="f92a6-256">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-256">Earning codes</span></span>

<span data-ttu-id="f92a6-257">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="f92a6-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f92a6-258">Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="f92a6-259">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f92a6-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f92a6-260">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-260">Earning Code (required)</span></span>
- <span data-ttu-id="f92a6-261">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-261">Description</span></span>
- <span data-ttu-id="f92a6-262">Mælieining</span><span class="sxs-lookup"><span data-stu-id="f92a6-262">Unit of measure</span></span>
- <span data-ttu-id="f92a6-263">Framleiðni</span><span class="sxs-lookup"><span data-stu-id="f92a6-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="f92a6-264">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="f92a6-264">Worker data</span></span>

<span data-ttu-id="f92a6-265">Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="f92a6-266">Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="f92a6-267">Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:</span><span class="sxs-lookup"><span data-stu-id="f92a6-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="f92a6-268">**Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="f92a6-269">**Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="f92a6-270">**Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.</span><span class="sxs-lookup"><span data-stu-id="f92a6-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="f92a6-271">**Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.</span><span class="sxs-lookup"><span data-stu-id="f92a6-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="f92a6-272">Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="f92a6-273">Almennar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f92a6-273">General information</span></span>

- <span data-ttu-id="f92a6-274">Númer starfsmanns (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-274">Personnel number (required)</span></span>
- <span data-ttu-id="f92a6-275">Fornafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-275">First name (required)</span></span>
- <span data-ttu-id="f92a6-276">Eftirnafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-276">Last name (required)</span></span>
- <span data-ttu-id="f92a6-277">Millinafn</span><span class="sxs-lookup"><span data-stu-id="f92a6-277">Middle name</span></span>
- <span data-ttu-id="f92a6-278">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="f92a6-278">Seniority date</span></span>
- <span data-ttu-id="f92a6-279">Þekkt sem</span><span class="sxs-lookup"><span data-stu-id="f92a6-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="f92a6-280">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f92a6-280">Personal information</span></span>

- <span data-ttu-id="f92a6-281">Hjúskaparstaða (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-281">Marital status (required)</span></span>
- <span data-ttu-id="f92a6-282">Fæðingardagur (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-282">Birth date (required)</span></span>
- <span data-ttu-id="f92a6-283">Kyn (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-283">Gender (required)</span></span>
- <span data-ttu-id="f92a6-284">Einstaklingur sem á við fötlun að stríða</span><span class="sxs-lookup"><span data-stu-id="f92a6-284">Person with disabilities</span></span>
- <span data-ttu-id="f92a6-285">Þjóðerni land svæði (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="f92a6-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="f92a6-286">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="f92a6-286">Address information</span></span>

- <span data-ttu-id="f92a6-287">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-287">Primary (required)</span></span>
- <span data-ttu-id="f92a6-288">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-288">Country/region (required)</span></span>
- <span data-ttu-id="f92a6-289">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-289">Postal code (required)</span></span>
- <span data-ttu-id="f92a6-290">Götunúmer (krafist) (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="f92a6-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="f92a6-291">Viðbygging (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="f92a6-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="f92a6-292">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-292">City (required)</span></span>
- <span data-ttu-id="f92a6-293">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-293">State (required)</span></span>
- <span data-ttu-id="f92a6-294">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="f92a6-295">Samskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="f92a6-295">Contact information</span></span> 

- <span data-ttu-id="f92a6-296">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-296">Primary (required)</span></span>
- <span data-ttu-id="f92a6-297">Símanúmer tengiliðar (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-297">Contact number (required)</span></span>
- <span data-ttu-id="f92a6-298">Skráarending</span><span class="sxs-lookup"><span data-stu-id="f92a6-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="f92a6-299">Launaupplýsingar og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-299">Payroll information and earning codes</span></span>

<span data-ttu-id="f92a6-300">Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f92a6-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="f92a6-301">Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="f92a6-302">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-302">Earning codes</span></span>

- <span data-ttu-id="f92a6-303">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-303">Position (required)</span></span>
- <span data-ttu-id="f92a6-304">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-304">Earning Code (required)</span></span>
- <span data-ttu-id="f92a6-305">Tíðni (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-305">Frequency (required)</span></span>
- <span data-ttu-id="f92a6-306">Upphæð (áskilin)</span><span class="sxs-lookup"><span data-stu-id="f92a6-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="f92a6-307">Launaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="f92a6-307">Payroll information</span></span>

- <span data-ttu-id="f92a6-308">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="f92a6-308">Payment Method</span></span>
- <span data-ttu-id="f92a6-309">Efnahagssvæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-309">Economic Region (required)</span></span>
- <span data-ttu-id="f92a6-310">Kenni fyrir fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="f92a6-310">Employee Benefits ID</span></span>
- <span data-ttu-id="f92a6-311">Kennitala (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-311">National ID Number (required)</span></span>
- <span data-ttu-id="f92a6-312">Hernaðarþjónustunúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-312">Military Service Number</span></span>
- <span data-ttu-id="f92a6-313">Auðkenni vaktar (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-313">Shift ID (required)</span></span>
- <span data-ttu-id="f92a6-314">Skattanúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-314">Tax Number (required)</span></span>
- <span data-ttu-id="f92a6-315">Auðkenni stéttarfélags (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-315">Union ID (required)</span></span>
- <span data-ttu-id="f92a6-316">Vinnudagskenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-316">Work Day ID (required)</span></span>
- <span data-ttu-id="f92a6-317">Vinnuleyfisnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="f92a6-318">Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="f92a6-319">Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="f92a6-320">Atvinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="f92a6-320">Employment details</span></span>

<span data-ttu-id="f92a6-321">Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="f92a6-322">Dayforce styður aðeins eina starfsferilsskrá í einu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="f92a6-323">Upphafsdagsetning ráðningar (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-323">Employment start date (required)</span></span>
- <span data-ttu-id="f92a6-324">Dagsetning starfsloka</span><span class="sxs-lookup"><span data-stu-id="f92a6-324">Employment end date</span></span>
- <span data-ttu-id="f92a6-325">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="f92a6-325">Start date</span></span>
- <span data-ttu-id="f92a6-326">Breyttur fyrsti starfsdagur</span><span class="sxs-lookup"><span data-stu-id="f92a6-326">Adjusted start date</span></span>
- <span data-ttu-id="f92a6-327">Dagsetning starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="f92a6-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="f92a6-328">Ástæða starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="f92a6-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="f92a6-329">Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="f92a6-330">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-330">Talent</span></span>                | <span data-ttu-id="f92a6-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f92a6-332">Nýlegasti ráðningardagurinn</span><span class="sxs-lookup"><span data-stu-id="f92a6-332">Most recent hire date</span></span> | <span data-ttu-id="f92a6-333">Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="f92a6-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f92a6-334">Starfslokadagur</span><span class="sxs-lookup"><span data-stu-id="f92a6-334">Termination date</span></span>      | <span data-ttu-id="f92a6-335">Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="f92a6-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f92a6-336">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="f92a6-336">Start date</span></span>            | <span data-ttu-id="f92a6-337">Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="f92a6-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="f92a6-338">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="f92a6-338">Original hire date</span></span>    | <span data-ttu-id="f92a6-339">Upphaf ráðningar fyrir elsta atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="f92a6-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="f92a6-340">Laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-340">Compensation</span></span>

<span data-ttu-id="f92a6-341">Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil.</span><span class="sxs-lookup"><span data-stu-id="f92a6-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="f92a6-342">Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="f92a6-343">Gildisdagsetning (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-343">Effective Date (required)</span></span>
- <span data-ttu-id="f92a6-344">Gildistími</span><span class="sxs-lookup"><span data-stu-id="f92a6-344">Expiration date</span></span>
- <span data-ttu-id="f92a6-345">Launataxti (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-345">Pay Rate (required)</span></span>
- <span data-ttu-id="f92a6-346">Umreikningur launataxta (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="f92a6-347">Árlegt jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="f92a6-348">Klukkutíma jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="f92a6-349">Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="f92a6-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="f92a6-350">Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="f92a6-351">Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="f92a6-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="f92a6-352">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="f92a6-353">Auðkenni kennitölu</span><span class="sxs-lookup"><span data-stu-id="f92a6-353">Social Security identifier</span></span> 

<span data-ttu-id="f92a6-354">Sérhver starfsmaður verður að hafa eitt aðalauðkenni.</span><span class="sxs-lookup"><span data-stu-id="f92a6-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="f92a6-355">Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="f92a6-356">Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="f92a6-357">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-357">Primary (required)</span></span>
- <span data-ttu-id="f92a6-358">Gerð auðkennis = „Kennitala“</span><span class="sxs-lookup"><span data-stu-id="f92a6-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="f92a6-359">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="f92a6-359">Issued Date</span></span>
- <span data-ttu-id="f92a6-360">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="f92a6-360">Expiration Date</span></span>

<span data-ttu-id="f92a6-361">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="f92a6-362">Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.</span><span class="sxs-lookup"><span data-stu-id="f92a6-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="f92a6-363">Bankareikningar og útborganir</span><span class="sxs-lookup"><span data-stu-id="f92a6-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="f92a6-364">Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="f92a6-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="f92a6-365">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-365">Talent</span></span>                         | <span data-ttu-id="f92a6-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f92a6-367">Bankareikningsnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="f92a6-368">SWIFT-kóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-368">SWIFT code (required)</span></span>          | <span data-ttu-id="f92a6-369">Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="f92a6-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="f92a6-370">Númer útibús (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="f92a6-371">Gerð bankareiknings (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-371">Bank account type (required)</span></span>   | <span data-ttu-id="f92a6-372">Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="f92a6-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="f92a6-373">Studd gildi innihalda **Athugun** og **Launaskrá**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="f92a6-374">Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka.</span><span class="sxs-lookup"><span data-stu-id="f92a6-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="f92a6-375">Allir aðrir reikningar eru hunsaðir.</span><span class="sxs-lookup"><span data-stu-id="f92a6-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="f92a6-376">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="f92a6-376">Address information</span></span>

<span data-ttu-id="f92a6-377">Sérhver starfsmaður verður að hafa eina aðalstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-377">Every employee must have one primary location.</span></span> <span data-ttu-id="f92a6-378">Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="f92a6-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="f92a6-379">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-379">Primary (required)</span></span>
- <span data-ttu-id="f92a6-380">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-380">Country/region (required)</span></span>
- <span data-ttu-id="f92a6-381">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="f92a6-382">Gata (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-382">Street (required)</span></span>
- <span data-ttu-id="f92a6-383">Götunúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-383">Street Number (required)</span></span>
- <span data-ttu-id="f92a6-384">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="f92a6-384">Building Complement</span></span>
- <span data-ttu-id="f92a6-385">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-385">City (required)</span></span>
- <span data-ttu-id="f92a6-386">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-386">State (required)</span></span>
- <span data-ttu-id="f92a6-387">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="f92a6-388">Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada</span><span class="sxs-lookup"><span data-stu-id="f92a6-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="f92a6-389">Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="f92a6-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="f92a6-390">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="f92a6-390">Departments are required on positions.</span></span>
- <span data-ttu-id="f92a6-391">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="f92a6-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="f92a6-392">Þú getur stillt Talent til að krefjast þess að stöður tilgreini deild.</span><span class="sxs-lookup"><span data-stu-id="f92a6-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="f92a6-393">Til að gera þetta skal fara í **Samnýttar stöður mannauðs > Stöður > Krefjast deilda á stöðum**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="f92a6-394">Við mælum með að þessari stillingu sé framfylgt fyrir samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="f92a6-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="f92a6-395">Starfsgerðir</span><span class="sxs-lookup"><span data-stu-id="f92a6-395">Job types</span></span>

<span data-ttu-id="f92a6-396">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="f92a6-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f92a6-397">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="f92a6-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="f92a6-398">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="f92a6-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f92a6-399">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f92a6-400">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f92a6-401">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="f92a6-401">Job type</span></span>   | <span data-ttu-id="f92a6-402">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f92a6-403">Tímar</span><span class="sxs-lookup"><span data-stu-id="f92a6-403">Hourly</span></span>     | <span data-ttu-id="f92a6-404">Tímar</span><span class="sxs-lookup"><span data-stu-id="f92a6-404">Hourly</span></span>      |
| <span data-ttu-id="f92a6-405">Föst laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-405">Salaried</span></span>   | <span data-ttu-id="f92a6-406">Föst laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="f92a6-407">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="f92a6-407">Position types</span></span> 

<span data-ttu-id="f92a6-408">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="f92a6-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f92a6-409">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="f92a6-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f92a6-410">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f92a6-411">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="f92a6-411">Position type</span></span>   | <span data-ttu-id="f92a6-412">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f92a6-413">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="f92a6-413">Full-time</span></span>       | <span data-ttu-id="f92a6-414">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="f92a6-414">Full time employee</span></span> |
| <span data-ttu-id="f92a6-415">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="f92a6-415">Part-time</span></span>       | <span data-ttu-id="f92a6-416">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="f92a6-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f92a6-417">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-417">Reason codes</span></span>

<span data-ttu-id="f92a6-418">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="f92a6-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f92a6-419">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="f92a6-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f92a6-420">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f92a6-421">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="f92a6-421">Reason code</span></span>    | <span data-ttu-id="f92a6-422">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-422">Description</span></span>      | <span data-ttu-id="f92a6-423">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="f92a6-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="f92a6-424">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="f92a6-424">RESIGNATION</span></span>    | <span data-ttu-id="f92a6-425">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="f92a6-425">Resignation</span></span>      | <span data-ttu-id="f92a6-426">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-426">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-427">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="f92a6-427">TERMINATION</span></span>    | <span data-ttu-id="f92a6-428">Lok</span><span class="sxs-lookup"><span data-stu-id="f92a6-428">Termination</span></span>      | <span data-ttu-id="f92a6-429">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-429">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-430">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="f92a6-430">RETIREMENT</span></span>     | <span data-ttu-id="f92a6-431">Starfslok</span><span class="sxs-lookup"><span data-stu-id="f92a6-431">Retirement</span></span>       | <span data-ttu-id="f92a6-432">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-432">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-433">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="f92a6-433">OTHER</span></span>          | <span data-ttu-id="f92a6-434">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="f92a6-434">Other Reasons</span></span>    | <span data-ttu-id="f92a6-435">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-435">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-436">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="f92a6-436">DEATH</span></span>          | <span data-ttu-id="f92a6-437">Dauði</span><span class="sxs-lookup"><span data-stu-id="f92a6-437">Death</span></span>            | <span data-ttu-id="f92a6-438">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-438">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-439">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="f92a6-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="f92a6-440">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="f92a6-440">Leave of Absence</span></span> | <span data-ttu-id="f92a6-441">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-441">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-442">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="f92a6-442">CONTRACTEND</span></span>    | <span data-ttu-id="f92a6-443">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="f92a6-443">End of Contract</span></span>  | <span data-ttu-id="f92a6-444">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-444">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-445">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-445">SALARYCHANGE</span></span>   | <span data-ttu-id="f92a6-446">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="f92a6-446">Change of Salary</span></span> | <span data-ttu-id="f92a6-447">Laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="f92a6-448">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="f92a6-448">Marital status</span></span>

<span data-ttu-id="f92a6-449">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f92a6-450">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f92a6-451">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-451">Talent</span></span>                 | <span data-ttu-id="f92a6-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="f92a6-453">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="f92a6-453">Married</span></span>                | <span data-ttu-id="f92a6-454">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="f92a6-454">Married</span></span>              |
| <span data-ttu-id="f92a6-455">Ein</span><span class="sxs-lookup"><span data-stu-id="f92a6-455">Single</span></span>                 | <span data-ttu-id="f92a6-456">Ein</span><span class="sxs-lookup"><span data-stu-id="f92a6-456">Single</span></span>               |
| <span data-ttu-id="f92a6-457">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="f92a6-457">Widowed</span></span>                | <span data-ttu-id="f92a6-458">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="f92a6-458">Widowed</span></span>              |
| <span data-ttu-id="f92a6-459">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="f92a6-459">Divorced</span></span>               | <span data-ttu-id="f92a6-460">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="f92a6-460">Divorced</span></span>             |
| <span data-ttu-id="f92a6-461">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="f92a6-461">Registered Partnership</span></span> | <span data-ttu-id="f92a6-462">Sambúð</span><span class="sxs-lookup"><span data-stu-id="f92a6-462">Domestic Partnership</span></span> |
| <span data-ttu-id="f92a6-463">None</span><span class="sxs-lookup"><span data-stu-id="f92a6-463">None</span></span>                   | <span data-ttu-id="f92a6-464">None</span><span class="sxs-lookup"><span data-stu-id="f92a6-464">None</span></span>                 |
| <span data-ttu-id="f92a6-465">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="f92a6-465">Cohabiting</span></span>             | <span data-ttu-id="f92a6-466">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="f92a6-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="f92a6-467">Kyn</span><span class="sxs-lookup"><span data-stu-id="f92a6-467">Gender</span></span>

<span data-ttu-id="f92a6-468">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f92a6-469">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f92a6-470">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-470">Talent</span></span>       | <span data-ttu-id="f92a6-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="f92a6-472">Karl</span><span class="sxs-lookup"><span data-stu-id="f92a6-472">Male</span></span>         | <span data-ttu-id="f92a6-473">Karl</span><span class="sxs-lookup"><span data-stu-id="f92a6-473">Male</span></span>            |
| <span data-ttu-id="f92a6-474">Kona</span><span class="sxs-lookup"><span data-stu-id="f92a6-474">Female</span></span>       | <span data-ttu-id="f92a6-475">Kona</span><span class="sxs-lookup"><span data-stu-id="f92a6-475">Female</span></span>          |
| <span data-ttu-id="f92a6-476">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="f92a6-476">Non-specific</span></span> | <span data-ttu-id="f92a6-477">*Ekki stutt*</span><span class="sxs-lookup"><span data-stu-id="f92a6-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f92a6-478">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-478">Earning codes</span></span>

<span data-ttu-id="f92a6-479">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="f92a6-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f92a6-480">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f92a6-481">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="f92a6-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f92a6-482">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="f92a6-482">Supported frequencies</span></span>

- <span data-ttu-id="f92a6-483">Allir</span><span class="sxs-lookup"><span data-stu-id="f92a6-483">All</span></span>
- <span data-ttu-id="f92a6-484">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="f92a6-484">EVERYPAY</span></span>
- <span data-ttu-id="f92a6-485">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="f92a6-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f92a6-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f92a6-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f92a6-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f92a6-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f92a6-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-488">1OFMTH</span></span>
- <span data-ttu-id="f92a6-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-489">LASTOFMTH</span></span>
- <span data-ttu-id="f92a6-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-490">2OFMTH</span></span>
- <span data-ttu-id="f92a6-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-491">3OFMTH</span></span>
- <span data-ttu-id="f92a6-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-492">4OFMTH</span></span>
- <span data-ttu-id="f92a6-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-493">5OFMTH</span></span>
- <span data-ttu-id="f92a6-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-494">1N2OFMTH</span></span>
- <span data-ttu-id="f92a6-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-495">3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-496">1N3OFMTH</span></span>
- <span data-ttu-id="f92a6-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-497">1N4OFMTH</span></span>
- <span data-ttu-id="f92a6-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-498">2N3OFMTH</span></span>
- <span data-ttu-id="f92a6-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-499">2N4OFMTH</span></span>
- <span data-ttu-id="f92a6-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="f92a6-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="f92a6-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f92a6-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f92a6-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f92a6-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f92a6-507">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f92a6-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f92a6-508">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f92a6-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f92a6-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f92a6-510">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f92a6-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f92a6-512">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="f92a6-512">Addresses</span></span>

<span data-ttu-id="f92a6-513">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="f92a6-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f92a6-514">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="f92a6-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f92a6-515">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-515">Talent</span></span>          | <span data-ttu-id="f92a6-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="f92a6-517">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="f92a6-517">Country/Region</span></span>  | <span data-ttu-id="f92a6-518">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-518">Country Code</span></span>          |
| <span data-ttu-id="f92a6-519">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-519">Zip/Postal Code</span></span> | <span data-ttu-id="f92a6-520">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-520">Postal Code</span></span>           |
| <span data-ttu-id="f92a6-521">Ríki</span><span class="sxs-lookup"><span data-stu-id="f92a6-521">State</span></span>           | <span data-ttu-id="f92a6-522">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="f92a6-522">State Code</span></span>            |
| <span data-ttu-id="f92a6-523">Póststöð</span><span class="sxs-lookup"><span data-stu-id="f92a6-523">City</span></span>            | <span data-ttu-id="f92a6-524">Póststöð</span><span class="sxs-lookup"><span data-stu-id="f92a6-524">City</span></span>                  |
| <span data-ttu-id="f92a6-525">Sýsla</span><span class="sxs-lookup"><span data-stu-id="f92a6-525">County</span></span>          | <span data-ttu-id="f92a6-526">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="f92a6-526">County (Municipality)</span></span> |
| <span data-ttu-id="f92a6-527">Gata</span><span class="sxs-lookup"><span data-stu-id="f92a6-527">Street</span></span>          | <span data-ttu-id="f92a6-528">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="f92a6-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="f92a6-529">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="f92a6-529">Tax regions</span></span>

<span data-ttu-id="f92a6-530">Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="f92a6-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="f92a6-531">Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="f92a6-532">Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="f92a6-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="f92a6-533">Skattumdæmi (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-533">Tax region (required)</span></span>
- <span data-ttu-id="f92a6-534">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-534">Country/Region (required)</span></span>
- <span data-ttu-id="f92a6-535">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-535">State (required)</span></span>
- <span data-ttu-id="f92a6-536">Sýsla</span><span class="sxs-lookup"><span data-stu-id="f92a6-536">County</span></span> 
- <span data-ttu-id="f92a6-537">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="f92a6-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="f92a6-538">Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="f92a6-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="f92a6-539">Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="f92a6-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="f92a6-540">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="f92a6-540">Departments are required on positions.</span></span>
- <span data-ttu-id="f92a6-541">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="f92a6-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="f92a6-542">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="f92a6-542">Job types</span></span>

<span data-ttu-id="f92a6-543">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="f92a6-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f92a6-544">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="f92a6-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="f92a6-545">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="f92a6-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f92a6-546">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="f92a6-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f92a6-547">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f92a6-548">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="f92a6-548">Job type</span></span>   | <span data-ttu-id="f92a6-549">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f92a6-550">Tímar</span><span class="sxs-lookup"><span data-stu-id="f92a6-550">Hourly</span></span>     | <span data-ttu-id="f92a6-551">MX tímakaup</span><span class="sxs-lookup"><span data-stu-id="f92a6-551">MX Hourly</span></span>   |
| <span data-ttu-id="f92a6-552">Föst laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-552">Salaried</span></span>   | <span data-ttu-id="f92a6-553">MX föst laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="f92a6-554">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="f92a6-554">Position types</span></span> 

<span data-ttu-id="f92a6-555">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="f92a6-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f92a6-556">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="f92a6-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f92a6-557">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f92a6-558">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="f92a6-558">Position type</span></span>   | <span data-ttu-id="f92a6-559">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f92a6-560">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="f92a6-560">Full-time</span></span>       | <span data-ttu-id="f92a6-561">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="f92a6-561">Full time employee</span></span> |
| <span data-ttu-id="f92a6-562">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="f92a6-562">Part-time</span></span>       | <span data-ttu-id="f92a6-563">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="f92a6-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f92a6-564">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-564">Reason codes</span></span>

<span data-ttu-id="f92a6-565">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="f92a6-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f92a6-566">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="f92a6-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f92a6-567">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f92a6-568">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="f92a6-568">Reason code</span></span>            | <span data-ttu-id="f92a6-569">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-569">Description</span></span>                    | <span data-ttu-id="f92a6-570">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="f92a6-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="f92a6-571">BROTTFÖR Á UNDAN LAUNAGREIÐSLU</span><span class="sxs-lookup"><span data-stu-id="f92a6-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="f92a6-572">Brottför á undan launum</span><span class="sxs-lookup"><span data-stu-id="f92a6-572">Departure before first payroll</span></span> | <span data-ttu-id="f92a6-573">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-573">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-574">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="f92a6-574">RESIGNATION</span></span>            | <span data-ttu-id="f92a6-575">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="f92a6-575">Resignation</span></span>                    | <span data-ttu-id="f92a6-576">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-576">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-577">LÍFEYRIR</span><span class="sxs-lookup"><span data-stu-id="f92a6-577">PENSION</span></span>                | <span data-ttu-id="f92a6-578">Lífeyrir</span><span class="sxs-lookup"><span data-stu-id="f92a6-578">Pension</span></span>                        | <span data-ttu-id="f92a6-579">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-579">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-580">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="f92a6-580">TERMINATION</span></span>            | <span data-ttu-id="f92a6-581">Lok</span><span class="sxs-lookup"><span data-stu-id="f92a6-581">Termination</span></span>                    | <span data-ttu-id="f92a6-582">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-582">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-583">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="f92a6-583">RETIREMENT</span></span>             | <span data-ttu-id="f92a6-584">Starfslok</span><span class="sxs-lookup"><span data-stu-id="f92a6-584">Retirement</span></span>                     | <span data-ttu-id="f92a6-585">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-585">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-586">FJARVERA</span><span class="sxs-lookup"><span data-stu-id="f92a6-586">ABSENTEE</span></span>               | <span data-ttu-id="f92a6-587">Fjarvera</span><span class="sxs-lookup"><span data-stu-id="f92a6-587">Absentee</span></span>                       | <span data-ttu-id="f92a6-588">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-588">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-589">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="f92a6-589">OTHER</span></span>                  | <span data-ttu-id="f92a6-590">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="f92a6-590">Other Reasons</span></span>                  | <span data-ttu-id="f92a6-591">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-591">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-592">LOKUN</span><span class="sxs-lookup"><span data-stu-id="f92a6-592">CLOSURE</span></span>                | <span data-ttu-id="f92a6-593">Viðskiptalokun</span><span class="sxs-lookup"><span data-stu-id="f92a6-593">Business Closure</span></span>               | <span data-ttu-id="f92a6-594">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-594">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-595">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="f92a6-595">DEATH</span></span>                  | <span data-ttu-id="f92a6-596">Dauði</span><span class="sxs-lookup"><span data-stu-id="f92a6-596">Death</span></span>                          | <span data-ttu-id="f92a6-597">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-597">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-598">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="f92a6-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="f92a6-599">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="f92a6-599">Leave of Absence</span></span>               | <span data-ttu-id="f92a6-600">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-600">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-601">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="f92a6-601">CONTRACTEND</span></span>            | <span data-ttu-id="f92a6-602">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="f92a6-602">End of Contract</span></span>                | <span data-ttu-id="f92a6-603">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="f92a6-603">Terminate worker</span></span>     |
| <span data-ttu-id="f92a6-604">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-604">SALARYCHANGE</span></span>           | <span data-ttu-id="f92a6-605">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="f92a6-605">Change of Salary</span></span>               | <span data-ttu-id="f92a6-606">Laun</span><span class="sxs-lookup"><span data-stu-id="f92a6-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="f92a6-607">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="f92a6-607">Terms of employment</span></span>

<span data-ttu-id="f92a6-608">Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="f92a6-609">Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.</span><span class="sxs-lookup"><span data-stu-id="f92a6-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="f92a6-610">Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="f92a6-611">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="f92a6-611">Terms of employment</span></span>   | <span data-ttu-id="f92a6-612">lýsing</span><span class="sxs-lookup"><span data-stu-id="f92a6-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f92a6-613">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="f92a6-613">Regular</span></span>               | <span data-ttu-id="f92a6-614">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="f92a6-614">Regular</span></span>     |
| <span data-ttu-id="f92a6-615">Beint</span><span class="sxs-lookup"><span data-stu-id="f92a6-615">Direct</span></span>                | <span data-ttu-id="f92a6-616">Beint</span><span class="sxs-lookup"><span data-stu-id="f92a6-616">Direct</span></span>      |
| <span data-ttu-id="f92a6-617">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="f92a6-617">Internship</span></span>            | <span data-ttu-id="f92a6-618">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="f92a6-618">Internship</span></span>  |
| <span data-ttu-id="f92a6-619">Fast</span><span class="sxs-lookup"><span data-stu-id="f92a6-619">Permanent</span></span>             | <span data-ttu-id="f92a6-620">Fast</span><span class="sxs-lookup"><span data-stu-id="f92a6-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="f92a6-621">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="f92a6-621">Marital status</span></span>

<span data-ttu-id="f92a6-622">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f92a6-623">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f92a6-624">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-624">Talent</span></span>                 | <span data-ttu-id="f92a6-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="f92a6-626">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="f92a6-626">Married</span></span>                | <span data-ttu-id="f92a6-627">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="f92a6-627">Married</span></span>                   |
| <span data-ttu-id="f92a6-628">Ein</span><span class="sxs-lookup"><span data-stu-id="f92a6-628">Single</span></span>                 | <span data-ttu-id="f92a6-629">Ein</span><span class="sxs-lookup"><span data-stu-id="f92a6-629">Single</span></span>                    |
| <span data-ttu-id="f92a6-630">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="f92a6-630">Widowed</span></span>                | <span data-ttu-id="f92a6-631">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="f92a6-631">Widowed</span></span>                   |
| <span data-ttu-id="f92a6-632">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="f92a6-632">Divorced</span></span>               | <span data-ttu-id="f92a6-633">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="f92a6-633">Divorced</span></span>                  |
| <span data-ttu-id="f92a6-634">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="f92a6-634">Registered Partnership</span></span> | <span data-ttu-id="f92a6-635">Sambúð</span><span class="sxs-lookup"><span data-stu-id="f92a6-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="f92a6-636">None</span><span class="sxs-lookup"><span data-stu-id="f92a6-636">None</span></span>                   | <span data-ttu-id="f92a6-637">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f92a6-638">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="f92a6-638">Cohabiting</span></span>             | <span data-ttu-id="f92a6-639">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="f92a6-640">Kyn</span><span class="sxs-lookup"><span data-stu-id="f92a6-640">Gender</span></span>

<span data-ttu-id="f92a6-641">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f92a6-642">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f92a6-643">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-643">Talent</span></span>       | <span data-ttu-id="f92a6-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="f92a6-645">Karl</span><span class="sxs-lookup"><span data-stu-id="f92a6-645">Male</span></span>         | <span data-ttu-id="f92a6-646">Karl</span><span class="sxs-lookup"><span data-stu-id="f92a6-646">Male</span></span>                      |
| <span data-ttu-id="f92a6-647">Kona</span><span class="sxs-lookup"><span data-stu-id="f92a6-647">Female</span></span>       | <span data-ttu-id="f92a6-648">Kona</span><span class="sxs-lookup"><span data-stu-id="f92a6-648">Female</span></span>                    |
| <span data-ttu-id="f92a6-649">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="f92a6-649">Non-specific</span></span> | <span data-ttu-id="f92a6-650">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="f92a6-651">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="f92a6-651">Payment method</span></span>

<span data-ttu-id="f92a6-652">Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="f92a6-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="f92a6-653">Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f92a6-654">Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="f92a6-655">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-655">Talent</span></span>             | <span data-ttu-id="f92a6-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="f92a6-657">Innlausn</span><span class="sxs-lookup"><span data-stu-id="f92a6-657">Cash</span></span>               | <span data-ttu-id="f92a6-658">Innlausn</span><span class="sxs-lookup"><span data-stu-id="f92a6-658">Cash</span></span>                      |
| <span data-ttu-id="f92a6-659">Rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="f92a6-659">Electronic Payment</span></span> | <span data-ttu-id="f92a6-660">Flutningur</span><span class="sxs-lookup"><span data-stu-id="f92a6-660">Transfer</span></span>                  |
| <span data-ttu-id="f92a6-661">Merkja</span><span class="sxs-lookup"><span data-stu-id="f92a6-661">Check</span></span>              | <span data-ttu-id="f92a6-662">Ávísun</span><span class="sxs-lookup"><span data-stu-id="f92a6-662">Cheque</span></span>                    |
| <span data-ttu-id="f92a6-663">Bankaávísun</span><span class="sxs-lookup"><span data-stu-id="f92a6-663">Bank Draft</span></span>         | <span data-ttu-id="f92a6-664">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f92a6-665">Annað</span><span class="sxs-lookup"><span data-stu-id="f92a6-665">Other</span></span>              | <span data-ttu-id="f92a6-666">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="f92a6-667">Gerð bankareiknings</span><span class="sxs-lookup"><span data-stu-id="f92a6-667">Bank account type</span></span>

<span data-ttu-id="f92a6-668">Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="f92a6-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="f92a6-669">Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga.</span><span class="sxs-lookup"><span data-stu-id="f92a6-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="f92a6-670">Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="f92a6-671">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-671">Talent</span></span>            | <span data-ttu-id="f92a6-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="f92a6-673">Ávísanareikningur</span><span class="sxs-lookup"><span data-stu-id="f92a6-673">Checking Account</span></span>  | <span data-ttu-id="f92a6-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="f92a6-674">CheckingAccount</span></span>           |
| <span data-ttu-id="f92a6-675">Launareikningur</span><span class="sxs-lookup"><span data-stu-id="f92a6-675">Payroll Account</span></span>   | <span data-ttu-id="f92a6-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="f92a6-676">PayrollAccount</span></span>            |
| <span data-ttu-id="f92a6-677">Sparnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="f92a6-677">Savings Account</span></span>   | <span data-ttu-id="f92a6-678">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f92a6-679">BankGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="f92a6-679">BankGirot account</span></span> | <span data-ttu-id="f92a6-680">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f92a6-681">PlusGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="f92a6-681">PlusGirot account</span></span> | <span data-ttu-id="f92a6-682">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="f92a6-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f92a6-683">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="f92a6-683">Earning codes</span></span>

<span data-ttu-id="f92a6-684">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="f92a6-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f92a6-685">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="f92a6-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f92a6-686">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="f92a6-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f92a6-687">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="f92a6-687">Supported frequencies</span></span>

- <span data-ttu-id="f92a6-688">Allir</span><span class="sxs-lookup"><span data-stu-id="f92a6-688">All</span></span>
- <span data-ttu-id="f92a6-689">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="f92a6-689">EVERYPAY</span></span>
- <span data-ttu-id="f92a6-690">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="f92a6-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f92a6-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f92a6-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f92a6-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f92a6-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f92a6-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-693">1OFMTH</span></span>
- <span data-ttu-id="f92a6-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-694">LASTOFMTH</span></span>
- <span data-ttu-id="f92a6-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-695">2OFMTH</span></span>
- <span data-ttu-id="f92a6-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-696">3OFMTH</span></span>
- <span data-ttu-id="f92a6-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-697">4OFMTH</span></span>
- <span data-ttu-id="f92a6-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-698">5OFMTH</span></span>
- <span data-ttu-id="f92a6-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-699">1N2OFMTH</span></span>
- <span data-ttu-id="f92a6-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-700">3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-701">1N3OFMTH</span></span>
- <span data-ttu-id="f92a6-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-702">1N4OFMTH</span></span>
- <span data-ttu-id="f92a6-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-703">2N3OFMTH</span></span>
- <span data-ttu-id="f92a6-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-704">2N4OFMTH</span></span>
- <span data-ttu-id="f92a6-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="f92a6-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="f92a6-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f92a6-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f92a6-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f92a6-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f92a6-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f92a6-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f92a6-712">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f92a6-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f92a6-713">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f92a6-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f92a6-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f92a6-715">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f92a6-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f92a6-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f92a6-717">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="f92a6-717">Addresses</span></span>

<span data-ttu-id="f92a6-718">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="f92a6-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f92a6-719">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="f92a6-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f92a6-720">Talent</span><span class="sxs-lookup"><span data-stu-id="f92a6-720">Talent</span></span>              | <span data-ttu-id="f92a6-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f92a6-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="f92a6-722">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="f92a6-722">Country/Region</span></span>      | <span data-ttu-id="f92a6-723">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-723">Country Code</span></span>          |
| <span data-ttu-id="f92a6-724">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-724">Zip/Postal Code</span></span>     | <span data-ttu-id="f92a6-725">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-725">Postal Code</span></span>           |
| <span data-ttu-id="f92a6-726">Ríki</span><span class="sxs-lookup"><span data-stu-id="f92a6-726">State</span></span>               | <span data-ttu-id="f92a6-727">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="f92a6-727">State Code</span></span>            |
| <span data-ttu-id="f92a6-728">Póststöð</span><span class="sxs-lookup"><span data-stu-id="f92a6-728">City</span></span>                | <span data-ttu-id="f92a6-729">Póststöð</span><span class="sxs-lookup"><span data-stu-id="f92a6-729">City</span></span>                  |
| <span data-ttu-id="f92a6-730">Sýsla</span><span class="sxs-lookup"><span data-stu-id="f92a6-730">County</span></span>              | <span data-ttu-id="f92a6-731">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="f92a6-731">County (Municipality)</span></span> |
| <span data-ttu-id="f92a6-732">Gata</span><span class="sxs-lookup"><span data-stu-id="f92a6-732">Street</span></span>              | <span data-ttu-id="f92a6-733">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="f92a6-733">Address Line 1</span></span>        |
| <span data-ttu-id="f92a6-734">Húsnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-734">Street Number</span></span>       | <span data-ttu-id="f92a6-735">Heimilisfang, lína 2</span><span class="sxs-lookup"><span data-stu-id="f92a6-735">Address Line 2</span></span>        |
| <span data-ttu-id="f92a6-736">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="f92a6-736">Building Complement</span></span> | <span data-ttu-id="f92a6-737">Heimilisfang, lína 5</span><span class="sxs-lookup"><span data-stu-id="f92a6-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="f92a6-738">Vegabréfsnúmer</span><span class="sxs-lookup"><span data-stu-id="f92a6-738">Passport number</span></span>

<span data-ttu-id="f92a6-739">Starfsmenn geta gefið upp vegabréfsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f92a6-739">Employees can declare passport information.</span></span> <span data-ttu-id="f92a6-740">Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="f92a6-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="f92a6-741">Gerð auðkennis = „Vegabréf“</span><span class="sxs-lookup"><span data-stu-id="f92a6-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="f92a6-742">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="f92a6-742">Issued Date</span></span>
- <span data-ttu-id="f92a6-743">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="f92a6-743">Expiration Date</span></span>

<span data-ttu-id="f92a6-744">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**.</span><span class="sxs-lookup"><span data-stu-id="f92a6-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="f92a6-745">Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="f92a6-746">Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

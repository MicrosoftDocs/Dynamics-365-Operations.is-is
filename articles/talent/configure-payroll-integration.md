---
title: Skilgreina launasamþættingu milli Talent og Dayforce
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla samþættingu milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce svo hægt sé að afgreiða launakeyrslu.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304815"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="7095c-103">Skilgreina launasamþættingu milli Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7095c-104">Samþættingin milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="7095c-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="7095c-105">Nauðsynlegt er að skilgreina samþættinguna bæði í Talent og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="7095c-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="7095c-106">Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Talent.</span><span class="sxs-lookup"><span data-stu-id="7095c-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="7095c-107">Samþættingin krefst tilgreindra gagna frá Talent.</span><span class="sxs-lookup"><span data-stu-id="7095c-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="7095c-108">Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Talent á þann hátt sem styður samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="7095c-109">Samþættingin notar eftirfarandi víðtæka flokka gagna:</span><span class="sxs-lookup"><span data-stu-id="7095c-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="7095c-110">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="7095c-110">Human resources data</span></span>
- <span data-ttu-id="7095c-111">Launagögn</span><span class="sxs-lookup"><span data-stu-id="7095c-111">Compensation data</span></span>
- <span data-ttu-id="7095c-112">Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="7095c-113">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="7095c-113">Worker data</span></span>

<span data-ttu-id="7095c-114">Þetta efnisatriði fjallar um skrefin sem verður að fylgja til að virkja samþættinginu.</span><span class="sxs-lookup"><span data-stu-id="7095c-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="7095c-115">Það útskýrir einnig gerð gagna og upplýsingar um skilgreiningar sem samþættingin krefst.</span><span class="sxs-lookup"><span data-stu-id="7095c-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="7095c-116">Virkja samþættingu</span><span class="sxs-lookup"><span data-stu-id="7095c-116">Enable the integration</span></span>

<span data-ttu-id="7095c-117">Í Talent er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="7095c-118">Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 for Finance and Operations þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7095c-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="7095c-119">Til að kveikja á samþættingu í Talent skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7095c-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="7095c-120">Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="7095c-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="7095c-121">Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.</span><span class="sxs-lookup"><span data-stu-id="7095c-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="7095c-122">Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.</span><span class="sxs-lookup"><span data-stu-id="7095c-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="7095c-123">Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="7095c-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="7095c-124">Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt.</span><span class="sxs-lookup"><span data-stu-id="7095c-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="7095c-125">Hægt er að breyta tíðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="7095c-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="7095c-126">Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi efnisatriðum Azure:</span><span class="sxs-lookup"><span data-stu-id="7095c-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="7095c-127">Um Azure-geymslureikninga</span><span class="sxs-lookup"><span data-stu-id="7095c-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="7095c-128">Skilgreina tengistrengi Azure-geymslu</span><span class="sxs-lookup"><span data-stu-id="7095c-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="7095c-129">Skilgreina gögnin þín</span><span class="sxs-lookup"><span data-stu-id="7095c-129">Configure your data</span></span> 

<span data-ttu-id="7095c-130">Til að afgreiða laun þarf að skilgreina mannauðsgögn í Talent.</span><span class="sxs-lookup"><span data-stu-id="7095c-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="7095c-131">Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun.</span><span class="sxs-lookup"><span data-stu-id="7095c-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="7095c-132">Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.</span><span class="sxs-lookup"><span data-stu-id="7095c-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="7095c-133">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="7095c-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="7095c-134">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="7095c-134">Benefits</span></span> 

<span data-ttu-id="7095c-135">Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.</span><span class="sxs-lookup"><span data-stu-id="7095c-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="7095c-136">Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="7095c-137">Fríðindaáætlanir</span><span class="sxs-lookup"><span data-stu-id="7095c-137">Benefit plans</span></span>

- <span data-ttu-id="7095c-138">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-138">Plan (required)</span></span>
- <span data-ttu-id="7095c-139">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-139">Type (required)</span></span>
- <span data-ttu-id="7095c-140">Áhrif á launaskrá (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-140">Payroll impact (required)</span></span>
- <span data-ttu-id="7095c-141">Endurheimta vangoldnar greiðslur</span><span class="sxs-lookup"><span data-stu-id="7095c-141">Recover arrears</span></span>
- <span data-ttu-id="7095c-142">Frádráttaraðferð</span><span class="sxs-lookup"><span data-stu-id="7095c-142">Deduction method</span></span>
- <span data-ttu-id="7095c-143">Frádráttarforgangur</span><span class="sxs-lookup"><span data-stu-id="7095c-143">Deduction priority</span></span>
- <span data-ttu-id="7095c-144">Takmörkunartímabil</span><span class="sxs-lookup"><span data-stu-id="7095c-144">Limit period</span></span>
- <span data-ttu-id="7095c-145">Takmarka upphæð</span><span class="sxs-lookup"><span data-stu-id="7095c-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="7095c-146">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="7095c-146">Benefits</span></span>

- <span data-ttu-id="7095c-147">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-147">Plan (required)</span></span>
- <span data-ttu-id="7095c-148">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-148">Type (required)</span></span>
- <span data-ttu-id="7095c-149">Valkostur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-149">Option (required)</span></span>
- <span data-ttu-id="7095c-150">Fríðindaauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-150">Benefit ID (required)</span></span>
- <span data-ttu-id="7095c-151">Tíðni</span><span class="sxs-lookup"><span data-stu-id="7095c-151">Frequency</span></span>
- <span data-ttu-id="7095c-152">Grunnur</span><span class="sxs-lookup"><span data-stu-id="7095c-152">Basis</span></span>
- <span data-ttu-id="7095c-153">Upphæð eða taxti</span><span class="sxs-lookup"><span data-stu-id="7095c-153">Amount or rate</span></span>
- <span data-ttu-id="7095c-154">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="7095c-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="7095c-155">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="7095c-155">Supported frequencies</span></span> 

- <span data-ttu-id="7095c-156">Vikulega</span><span class="sxs-lookup"><span data-stu-id="7095c-156">Weekly</span></span>
- <span data-ttu-id="7095c-157">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="7095c-157">Bi-weekly</span></span>
- <span data-ttu-id="7095c-158">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="7095c-158">Semi-monthly</span></span>
- <span data-ttu-id="7095c-159">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="7095c-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="7095c-160">Studdir grunnar</span><span class="sxs-lookup"><span data-stu-id="7095c-160">Supported bases</span></span> 

- <span data-ttu-id="7095c-161">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="7095c-161">Fixed amount</span></span>
- <span data-ttu-id="7095c-162">Prósenta af tekjum</span><span class="sxs-lookup"><span data-stu-id="7095c-162">Percent of earnings</span></span>
- <span data-ttu-id="7095c-163">Virkar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="7095c-163">Productive hours</span></span>

<span data-ttu-id="7095c-164">Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.</span><span class="sxs-lookup"><span data-stu-id="7095c-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="7095c-165">Val í Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-165">Selection in Talent</span></span>        | <span data-ttu-id="7095c-166">Niðurstaða í Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7095c-167">None</span><span class="sxs-lookup"><span data-stu-id="7095c-167">None</span></span>                       | <span data-ttu-id="7095c-168">Enginn frádráttur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="7095c-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="7095c-169">Eingöngu frádráttur</span><span class="sxs-lookup"><span data-stu-id="7095c-169">Deduction only</span></span>             | <span data-ttu-id="7095c-170">Frádráttur starfsmanns er búinn til.</span><span class="sxs-lookup"><span data-stu-id="7095c-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="7095c-171">Eingöngu framlag</span><span class="sxs-lookup"><span data-stu-id="7095c-171">Contribution only</span></span>          | <span data-ttu-id="7095c-172">Frádráttur vinnuveitanda er búinn til.</span><span class="sxs-lookup"><span data-stu-id="7095c-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="7095c-173">Frádráttur og framlag</span><span class="sxs-lookup"><span data-stu-id="7095c-173">Deduction and contribution</span></span> | <span data-ttu-id="7095c-174">Frádrættir starfsmanns og vinnuveitanda eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="7095c-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="7095c-175">Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="7095c-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="7095c-176">Leggja fram fríðindaáætlun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="7095c-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="7095c-177">Stofna ný fríðindi</span><span class="sxs-lookup"><span data-stu-id="7095c-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="7095c-178">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="7095c-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="7095c-179">Skrá og fjarlægja fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="7095c-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="7095c-180">Laun</span><span class="sxs-lookup"><span data-stu-id="7095c-180">Compensation</span></span> 

<span data-ttu-id="7095c-181">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="7095c-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="7095c-182">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="7095c-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="7095c-183">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="7095c-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="7095c-184">Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7095c-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="7095c-185">Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta.</span><span class="sxs-lookup"><span data-stu-id="7095c-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="7095c-186">Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="7095c-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="7095c-187">Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="7095c-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="7095c-188">Launafyrirkomulag fastra launa stofnað</span><span class="sxs-lookup"><span data-stu-id="7095c-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="7095c-189">Launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="7095c-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="7095c-190">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="7095c-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="7095c-191">Launaútreikningur</span><span class="sxs-lookup"><span data-stu-id="7095c-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="7095c-192">Skilgreina launavinnslu og reikna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="7095c-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="7095c-193">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="7095c-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="7095c-194">Skrá starfsmann í launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="7095c-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="7095c-195">Störf</span><span class="sxs-lookup"><span data-stu-id="7095c-195">Jobs</span></span> 

<span data-ttu-id="7095c-196">Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið.</span><span class="sxs-lookup"><span data-stu-id="7095c-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="7095c-197">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="7095c-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7095c-198">Setja upp íhluta verks</span><span class="sxs-lookup"><span data-stu-id="7095c-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="7095c-199">Skilgreina ný störf</span><span class="sxs-lookup"><span data-stu-id="7095c-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="7095c-200">Stöður</span><span class="sxs-lookup"><span data-stu-id="7095c-200">Positions</span></span>

<span data-ttu-id="7095c-201">Staða er sérstakt tilvik starfs.</span><span class="sxs-lookup"><span data-stu-id="7095c-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="7095c-202">Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“.</span><span class="sxs-lookup"><span data-stu-id="7095c-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="7095c-203">Staða er til í deild.</span><span class="sxs-lookup"><span data-stu-id="7095c-203">A position exists in a department.</span></span> <span data-ttu-id="7095c-204">Einungis einn starfsmaður getur tengst hverri stöðu.</span><span class="sxs-lookup"><span data-stu-id="7095c-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="7095c-205">Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:</span><span class="sxs-lookup"><span data-stu-id="7095c-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="7095c-206">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-206">Position (required)</span></span>
- <span data-ttu-id="7095c-207">Lýsing (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-207">Description (required)</span></span>
- <span data-ttu-id="7095c-208">Starf (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-208">Job (required)</span></span>
- <span data-ttu-id="7095c-209">Deild (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-209">Department (required)</span></span>
- <span data-ttu-id="7095c-210">Stöðugerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-210">Position type (required)</span></span>
- <span data-ttu-id="7095c-211">Jafngildi fulls starfs</span><span class="sxs-lookup"><span data-stu-id="7095c-211">Full-time equivalent</span></span>
- <span data-ttu-id="7095c-212">Reglulegar árlegar vinnustundir (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="7095c-213">Greitt eftir lögaðila (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="7095c-214">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-214">Pay cycle (required)</span></span>
- <span data-ttu-id="7095c-215">Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="7095c-216">Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="7095c-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="7095c-217">Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="7095c-218">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="7095c-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7095c-219">Vinnuafl skipulagt með notkun deilda, starfa og staða</span><span class="sxs-lookup"><span data-stu-id="7095c-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="7095c-220">Setja upp stöður</span><span class="sxs-lookup"><span data-stu-id="7095c-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="7095c-221">Deildir</span><span class="sxs-lookup"><span data-stu-id="7095c-221">Departments</span></span>

<span data-ttu-id="7095c-222">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="7095c-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="7095c-223">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="7095c-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="7095c-224">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="7095c-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="7095c-225">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="7095c-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="7095c-226">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="7095c-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7095c-227">Stofnun deildar og tenging hennar við deildastigveldið</span><span class="sxs-lookup"><span data-stu-id="7095c-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="7095c-228">Skilgreina nýjar deildir</span><span class="sxs-lookup"><span data-stu-id="7095c-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="7095c-229">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="7095c-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="7095c-230">Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="7095c-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="7095c-231">Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="7095c-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="7095c-232">Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur.</span><span class="sxs-lookup"><span data-stu-id="7095c-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="7095c-233">Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.</span><span class="sxs-lookup"><span data-stu-id="7095c-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="7095c-234">Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli.</span><span class="sxs-lookup"><span data-stu-id="7095c-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="7095c-235">Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp.</span><span class="sxs-lookup"><span data-stu-id="7095c-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="7095c-236">Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.</span><span class="sxs-lookup"><span data-stu-id="7095c-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="7095c-237">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="7095c-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="7095c-238">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-238">Pay cycle (required)</span></span>
- <span data-ttu-id="7095c-239">Tíðni greiðsluferlis (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="7095c-240">Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="7095c-241">Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="7095c-242">Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="7095c-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="7095c-243">Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="7095c-244">Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Talent.</span><span class="sxs-lookup"><span data-stu-id="7095c-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="7095c-245">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-245">Earning codes</span></span>

<span data-ttu-id="7095c-246">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="7095c-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7095c-247">Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="7095c-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="7095c-248">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="7095c-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="7095c-249">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-249">Earning Code (required)</span></span>
- <span data-ttu-id="7095c-250">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-250">Description</span></span>
- <span data-ttu-id="7095c-251">Mælieining</span><span class="sxs-lookup"><span data-stu-id="7095c-251">Unit of measure</span></span>
- <span data-ttu-id="7095c-252">Framleiðni</span><span class="sxs-lookup"><span data-stu-id="7095c-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="7095c-253">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="7095c-253">Worker data</span></span>

<span data-ttu-id="7095c-254">Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="7095c-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="7095c-255">Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="7095c-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="7095c-256">Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:</span><span class="sxs-lookup"><span data-stu-id="7095c-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="7095c-257">**Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="7095c-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="7095c-258">**Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.</span><span class="sxs-lookup"><span data-stu-id="7095c-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="7095c-259">**Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.</span><span class="sxs-lookup"><span data-stu-id="7095c-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="7095c-260">**Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.</span><span class="sxs-lookup"><span data-stu-id="7095c-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="7095c-261">Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="7095c-262">Almennar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7095c-262">General information</span></span>

- <span data-ttu-id="7095c-263">Númer starfsmanns (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-263">Personnel number (required)</span></span>
- <span data-ttu-id="7095c-264">Fornafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-264">First name (required)</span></span>
- <span data-ttu-id="7095c-265">Eftirnafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-265">Last name (required)</span></span>
- <span data-ttu-id="7095c-266">Millinafn</span><span class="sxs-lookup"><span data-stu-id="7095c-266">Middle name</span></span>
- <span data-ttu-id="7095c-267">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="7095c-267">Seniority date</span></span>
- <span data-ttu-id="7095c-268">Þekkt sem</span><span class="sxs-lookup"><span data-stu-id="7095c-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="7095c-269">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7095c-269">Personal information</span></span>

- <span data-ttu-id="7095c-270">Hjúskaparstaða (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-270">Marital status (required)</span></span>
- <span data-ttu-id="7095c-271">Fæðingardagur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-271">Birth date (required)</span></span>
- <span data-ttu-id="7095c-272">Kyn (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-272">Gender (required)</span></span>
- <span data-ttu-id="7095c-273">Einstaklingur sem á við fötlun að stríða</span><span class="sxs-lookup"><span data-stu-id="7095c-273">Person with disabilities</span></span>
- <span data-ttu-id="7095c-274">Þjóðerni land svæði (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="7095c-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="7095c-275">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="7095c-275">Address information</span></span>

- <span data-ttu-id="7095c-276">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-276">Primary (required)</span></span>
- <span data-ttu-id="7095c-277">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-277">Country/region (required)</span></span>
- <span data-ttu-id="7095c-278">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-278">Postal code (required)</span></span>
- <span data-ttu-id="7095c-279">Götunúmer (krafist) (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="7095c-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="7095c-280">Viðbygging (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="7095c-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="7095c-281">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-281">City (required)</span></span>
- <span data-ttu-id="7095c-282">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-282">State (required)</span></span>
- <span data-ttu-id="7095c-283">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="7095c-284">Samskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="7095c-284">Contact information</span></span> 

- <span data-ttu-id="7095c-285">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-285">Primary (required)</span></span>
- <span data-ttu-id="7095c-286">Símanúmer tengiliðar (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-286">Contact number (required)</span></span>
- <span data-ttu-id="7095c-287">Skráarending</span><span class="sxs-lookup"><span data-stu-id="7095c-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="7095c-288">Launaupplýsingar og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-288">Payroll information and earning codes</span></span>

<span data-ttu-id="7095c-289">Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7095c-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="7095c-290">Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.</span><span class="sxs-lookup"><span data-stu-id="7095c-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="7095c-291">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-291">Earning codes</span></span>

- <span data-ttu-id="7095c-292">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-292">Position (required)</span></span>
- <span data-ttu-id="7095c-293">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-293">Earning Code (required)</span></span>
- <span data-ttu-id="7095c-294">Tíðni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-294">Frequency (required)</span></span>
- <span data-ttu-id="7095c-295">Upphæð (áskilin)</span><span class="sxs-lookup"><span data-stu-id="7095c-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="7095c-296">Launaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="7095c-296">Payroll information</span></span>

- <span data-ttu-id="7095c-297">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="7095c-297">Payment Method</span></span>
- <span data-ttu-id="7095c-298">Efnahagssvæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-298">Economic Region (required)</span></span>
- <span data-ttu-id="7095c-299">Kenni fyrir fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="7095c-299">Employee Benefits ID</span></span>
- <span data-ttu-id="7095c-300">Kennitala (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-300">National ID Number (required)</span></span>
- <span data-ttu-id="7095c-301">Hernaðarþjónustunúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-301">Military Service Number</span></span>
- <span data-ttu-id="7095c-302">Auðkenni vaktar (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-302">Shift ID (required)</span></span>
- <span data-ttu-id="7095c-303">Skattanúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-303">Tax Number (required)</span></span>
- <span data-ttu-id="7095c-304">Auðkenni stéttarfélags (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-304">Union ID (required)</span></span>
- <span data-ttu-id="7095c-305">Vinnudagskenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-305">Work Day ID (required)</span></span>
- <span data-ttu-id="7095c-306">Vinnuleyfisnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="7095c-307">Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="7095c-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="7095c-308">Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="7095c-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="7095c-309">Atvinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="7095c-309">Employment details</span></span>

<span data-ttu-id="7095c-310">Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="7095c-311">Dayforce styður aðeins eina starfsferilsskrá í einu.</span><span class="sxs-lookup"><span data-stu-id="7095c-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="7095c-312">Upphafsdagsetning ráðningar (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-312">Employment start date (required)</span></span>
- <span data-ttu-id="7095c-313">Dagsetning starfsloka</span><span class="sxs-lookup"><span data-stu-id="7095c-313">Employment end date</span></span>
- <span data-ttu-id="7095c-314">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="7095c-314">Start date</span></span>
- <span data-ttu-id="7095c-315">Breyttur fyrsti starfsdagur</span><span class="sxs-lookup"><span data-stu-id="7095c-315">Adjusted start date</span></span>
- <span data-ttu-id="7095c-316">Dagsetning starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="7095c-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="7095c-317">Ástæða starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="7095c-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="7095c-318">Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="7095c-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="7095c-319">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-319">Talent</span></span>                | <span data-ttu-id="7095c-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7095c-321">Nýlegasti ráðningardagurinn</span><span class="sxs-lookup"><span data-stu-id="7095c-321">Most recent hire date</span></span> | <span data-ttu-id="7095c-322">Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="7095c-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="7095c-323">Starfslokadagur</span><span class="sxs-lookup"><span data-stu-id="7095c-323">Termination date</span></span>      | <span data-ttu-id="7095c-324">Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="7095c-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="7095c-325">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="7095c-325">Start date</span></span>            | <span data-ttu-id="7095c-326">Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="7095c-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="7095c-327">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="7095c-327">Original hire date</span></span>    | <span data-ttu-id="7095c-328">Upphaf ráðningar fyrir elsta atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="7095c-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="7095c-329">Laun</span><span class="sxs-lookup"><span data-stu-id="7095c-329">Compensation</span></span>

<span data-ttu-id="7095c-330">Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil.</span><span class="sxs-lookup"><span data-stu-id="7095c-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="7095c-331">Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.</span><span class="sxs-lookup"><span data-stu-id="7095c-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="7095c-332">Gildisdagsetning (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-332">Effective Date (required)</span></span>
- <span data-ttu-id="7095c-333">Gildistími</span><span class="sxs-lookup"><span data-stu-id="7095c-333">Expiration date</span></span>
- <span data-ttu-id="7095c-334">Launataxti (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-334">Pay Rate (required)</span></span>
- <span data-ttu-id="7095c-335">Umreikningur launataxta (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="7095c-336">Árlegt jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="7095c-337">Klukkutíma jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="7095c-338">Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7095c-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="7095c-339">Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="7095c-340">Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7095c-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="7095c-341">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="7095c-342">Auðkenni kennitölu</span><span class="sxs-lookup"><span data-stu-id="7095c-342">Social Security identifier</span></span> 

<span data-ttu-id="7095c-343">Sérhver starfsmaður verður að hafa eitt aðalauðkenni.</span><span class="sxs-lookup"><span data-stu-id="7095c-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="7095c-344">Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="7095c-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="7095c-345">Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="7095c-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="7095c-346">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-346">Primary (required)</span></span>
- <span data-ttu-id="7095c-347">Gerð auðkennis = „Kennitala“</span><span class="sxs-lookup"><span data-stu-id="7095c-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="7095c-348">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="7095c-348">Issued Date</span></span>
- <span data-ttu-id="7095c-349">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="7095c-349">Expiration Date</span></span>

<span data-ttu-id="7095c-350">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="7095c-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="7095c-351">Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.</span><span class="sxs-lookup"><span data-stu-id="7095c-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="7095c-352">Bankareikningar og útborganir</span><span class="sxs-lookup"><span data-stu-id="7095c-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="7095c-353">Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="7095c-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="7095c-354">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-354">Talent</span></span>                         | <span data-ttu-id="7095c-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7095c-356">Bankareikningsnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="7095c-357">SWIFT-kóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-357">SWIFT code (required)</span></span>          | <span data-ttu-id="7095c-358">Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="7095c-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="7095c-359">Númer útibús (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="7095c-360">Gerð bankareiknings (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-360">Bank account type (required)</span></span>   | <span data-ttu-id="7095c-361">Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="7095c-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="7095c-362">Studd gildi innihalda **Athugun** og **Launaskrá**.</span><span class="sxs-lookup"><span data-stu-id="7095c-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="7095c-363">Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka.</span><span class="sxs-lookup"><span data-stu-id="7095c-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="7095c-364">Allir aðrir reikningar eru hunsaðir.</span><span class="sxs-lookup"><span data-stu-id="7095c-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="7095c-365">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="7095c-365">Address information</span></span>

<span data-ttu-id="7095c-366">Sérhver starfsmaður verður að hafa eina aðalstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="7095c-366">Every employee must have one primary location.</span></span> <span data-ttu-id="7095c-367">Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="7095c-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="7095c-368">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-368">Primary (required)</span></span>
- <span data-ttu-id="7095c-369">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-369">Country/region (required)</span></span>
- <span data-ttu-id="7095c-370">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="7095c-371">Gata (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-371">Street (required)</span></span>
- <span data-ttu-id="7095c-372">Götunúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-372">Street Number (required)</span></span>
- <span data-ttu-id="7095c-373">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="7095c-373">Building Complement</span></span>
- <span data-ttu-id="7095c-374">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-374">City (required)</span></span>
- <span data-ttu-id="7095c-375">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-375">State (required)</span></span>
- <span data-ttu-id="7095c-376">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="7095c-377">Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada</span><span class="sxs-lookup"><span data-stu-id="7095c-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="7095c-378">Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="7095c-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="7095c-379">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="7095c-379">Departments are required on positions.</span></span>
- <span data-ttu-id="7095c-380">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="7095c-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="7095c-381">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="7095c-381">Job types</span></span>

<span data-ttu-id="7095c-382">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="7095c-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="7095c-383">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="7095c-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="7095c-384">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="7095c-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="7095c-385">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="7095c-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="7095c-386">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7095c-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="7095c-387">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="7095c-387">Job type</span></span>   | <span data-ttu-id="7095c-388">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="7095c-389">Tímar</span><span class="sxs-lookup"><span data-stu-id="7095c-389">Hourly</span></span>     | <span data-ttu-id="7095c-390">Tímar</span><span class="sxs-lookup"><span data-stu-id="7095c-390">Hourly</span></span>      |
| <span data-ttu-id="7095c-391">Föst laun</span><span class="sxs-lookup"><span data-stu-id="7095c-391">Salaried</span></span>   | <span data-ttu-id="7095c-392">Föst laun</span><span class="sxs-lookup"><span data-stu-id="7095c-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="7095c-393">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="7095c-393">Position types</span></span> 

<span data-ttu-id="7095c-394">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="7095c-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="7095c-395">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="7095c-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="7095c-396">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7095c-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="7095c-397">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="7095c-397">Position type</span></span>   | <span data-ttu-id="7095c-398">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="7095c-399">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="7095c-399">Full-time</span></span>       | <span data-ttu-id="7095c-400">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="7095c-400">Full time employee</span></span> |
| <span data-ttu-id="7095c-401">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="7095c-401">Part-time</span></span>       | <span data-ttu-id="7095c-402">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="7095c-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="7095c-403">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-403">Reason codes</span></span>

<span data-ttu-id="7095c-404">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7095c-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="7095c-405">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="7095c-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="7095c-406">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7095c-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="7095c-407">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="7095c-407">Reason code</span></span>    | <span data-ttu-id="7095c-408">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-408">Description</span></span>      | <span data-ttu-id="7095c-409">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="7095c-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="7095c-410">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="7095c-410">RESIGNATION</span></span>    | <span data-ttu-id="7095c-411">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="7095c-411">Resignation</span></span>      | <span data-ttu-id="7095c-412">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-412">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-413">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="7095c-413">TERMINATION</span></span>    | <span data-ttu-id="7095c-414">Lok</span><span class="sxs-lookup"><span data-stu-id="7095c-414">Termination</span></span>      | <span data-ttu-id="7095c-415">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-415">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-416">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="7095c-416">RETIREMENT</span></span>     | <span data-ttu-id="7095c-417">Starfslok</span><span class="sxs-lookup"><span data-stu-id="7095c-417">Retirement</span></span>       | <span data-ttu-id="7095c-418">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-418">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-419">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="7095c-419">OTHER</span></span>          | <span data-ttu-id="7095c-420">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="7095c-420">Other Reasons</span></span>    | <span data-ttu-id="7095c-421">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-421">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-422">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="7095c-422">DEATH</span></span>          | <span data-ttu-id="7095c-423">Dauði</span><span class="sxs-lookup"><span data-stu-id="7095c-423">Death</span></span>            | <span data-ttu-id="7095c-424">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-424">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-425">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="7095c-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="7095c-426">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="7095c-426">Leave of Absence</span></span> | <span data-ttu-id="7095c-427">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-427">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-428">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="7095c-428">CONTRACTEND</span></span>    | <span data-ttu-id="7095c-429">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="7095c-429">End of Contract</span></span>  | <span data-ttu-id="7095c-430">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-430">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-431">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="7095c-431">SALARYCHANGE</span></span>   | <span data-ttu-id="7095c-432">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="7095c-432">Change of Salary</span></span> | <span data-ttu-id="7095c-433">Laun</span><span class="sxs-lookup"><span data-stu-id="7095c-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="7095c-434">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="7095c-434">Marital status</span></span>

<span data-ttu-id="7095c-435">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7095c-436">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="7095c-437">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-437">Talent</span></span>                 | <span data-ttu-id="7095c-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="7095c-439">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7095c-439">Married</span></span>                | <span data-ttu-id="7095c-440">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7095c-440">Married</span></span>              |
| <span data-ttu-id="7095c-441">Ein</span><span class="sxs-lookup"><span data-stu-id="7095c-441">Single</span></span>                 | <span data-ttu-id="7095c-442">Ein</span><span class="sxs-lookup"><span data-stu-id="7095c-442">Single</span></span>               |
| <span data-ttu-id="7095c-443">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7095c-443">Widowed</span></span>                | <span data-ttu-id="7095c-444">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7095c-444">Widowed</span></span>              |
| <span data-ttu-id="7095c-445">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7095c-445">Divorced</span></span>               | <span data-ttu-id="7095c-446">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7095c-446">Divorced</span></span>             |
| <span data-ttu-id="7095c-447">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="7095c-447">Registered Partnership</span></span> | <span data-ttu-id="7095c-448">Sambúð</span><span class="sxs-lookup"><span data-stu-id="7095c-448">Domestic Partnership</span></span> |
| <span data-ttu-id="7095c-449">None</span><span class="sxs-lookup"><span data-stu-id="7095c-449">None</span></span>                   | <span data-ttu-id="7095c-450">None</span><span class="sxs-lookup"><span data-stu-id="7095c-450">None</span></span>                 |
| <span data-ttu-id="7095c-451">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="7095c-451">Cohabiting</span></span>             | <span data-ttu-id="7095c-452">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="7095c-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="7095c-453">Kyn</span><span class="sxs-lookup"><span data-stu-id="7095c-453">Gender</span></span>

<span data-ttu-id="7095c-454">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7095c-455">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="7095c-456">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-456">Talent</span></span>       | <span data-ttu-id="7095c-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="7095c-458">Karl</span><span class="sxs-lookup"><span data-stu-id="7095c-458">Male</span></span>         | <span data-ttu-id="7095c-459">Karl</span><span class="sxs-lookup"><span data-stu-id="7095c-459">Male</span></span>            |
| <span data-ttu-id="7095c-460">Kona</span><span class="sxs-lookup"><span data-stu-id="7095c-460">Female</span></span>       | <span data-ttu-id="7095c-461">Kona</span><span class="sxs-lookup"><span data-stu-id="7095c-461">Female</span></span>          |
| <span data-ttu-id="7095c-462">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="7095c-462">Non-specific</span></span> | <span data-ttu-id="7095c-463">*Ekki stutt*</span><span class="sxs-lookup"><span data-stu-id="7095c-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="7095c-464">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-464">Earning codes</span></span>

<span data-ttu-id="7095c-465">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="7095c-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7095c-466">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="7095c-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="7095c-467">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="7095c-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="7095c-468">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="7095c-468">Supported frequencies</span></span>

- <span data-ttu-id="7095c-469">Allir</span><span class="sxs-lookup"><span data-stu-id="7095c-469">All</span></span>
- <span data-ttu-id="7095c-470">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="7095c-470">EVERYPAY</span></span>
- <span data-ttu-id="7095c-471">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="7095c-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="7095c-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="7095c-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="7095c-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="7095c-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="7095c-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-474">1OFMTH</span></span>
- <span data-ttu-id="7095c-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-475">LASTOFMTH</span></span>
- <span data-ttu-id="7095c-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-476">2OFMTH</span></span>
- <span data-ttu-id="7095c-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-477">3OFMTH</span></span>
- <span data-ttu-id="7095c-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-478">4OFMTH</span></span>
- <span data-ttu-id="7095c-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-479">5OFMTH</span></span>
- <span data-ttu-id="7095c-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-480">1N2OFMTH</span></span>
- <span data-ttu-id="7095c-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-481">3N4OFMTH</span></span>
- <span data-ttu-id="7095c-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-482">1N3OFMTH</span></span>
- <span data-ttu-id="7095c-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-483">1N4OFMTH</span></span>
- <span data-ttu-id="7095c-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-484">2N3OFMTH</span></span>
- <span data-ttu-id="7095c-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-485">2N4OFMTH</span></span>
- <span data-ttu-id="7095c-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="7095c-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="7095c-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="7095c-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="7095c-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="7095c-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="7095c-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="7095c-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="7095c-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="7095c-493">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="7095c-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="7095c-494">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="7095c-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="7095c-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="7095c-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="7095c-496">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7095c-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="7095c-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7095c-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="7095c-498">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="7095c-498">Addresses</span></span>

<span data-ttu-id="7095c-499">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="7095c-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="7095c-500">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="7095c-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="7095c-501">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-501">Talent</span></span>          | <span data-ttu-id="7095c-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="7095c-503">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="7095c-503">Country/Region</span></span>  | <span data-ttu-id="7095c-504">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-504">Country Code</span></span>          |
| <span data-ttu-id="7095c-505">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-505">Zip/Postal Code</span></span> | <span data-ttu-id="7095c-506">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-506">Postal Code</span></span>           |
| <span data-ttu-id="7095c-507">Ríki</span><span class="sxs-lookup"><span data-stu-id="7095c-507">State</span></span>           | <span data-ttu-id="7095c-508">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="7095c-508">State Code</span></span>            |
| <span data-ttu-id="7095c-509">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7095c-509">City</span></span>            | <span data-ttu-id="7095c-510">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7095c-510">City</span></span>                  |
| <span data-ttu-id="7095c-511">Sýsla</span><span class="sxs-lookup"><span data-stu-id="7095c-511">County</span></span>          | <span data-ttu-id="7095c-512">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="7095c-512">County (Municipality)</span></span> |
| <span data-ttu-id="7095c-513">Gata</span><span class="sxs-lookup"><span data-stu-id="7095c-513">Street</span></span>          | <span data-ttu-id="7095c-514">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="7095c-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="7095c-515">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="7095c-515">Tax regions</span></span>

<span data-ttu-id="7095c-516">Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="7095c-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="7095c-517">Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="7095c-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="7095c-518">Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="7095c-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="7095c-519">Skattumdæmi (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-519">Tax region (required)</span></span>
- <span data-ttu-id="7095c-520">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-520">Country/Region (required)</span></span>
- <span data-ttu-id="7095c-521">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-521">State (required)</span></span>
- <span data-ttu-id="7095c-522">Sýsla</span><span class="sxs-lookup"><span data-stu-id="7095c-522">County</span></span> 
- <span data-ttu-id="7095c-523">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="7095c-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="7095c-524">Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="7095c-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="7095c-525">Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="7095c-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="7095c-526">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="7095c-526">Departments are required on positions.</span></span>
- <span data-ttu-id="7095c-527">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="7095c-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="7095c-528">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="7095c-528">Job types</span></span>

<span data-ttu-id="7095c-529">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="7095c-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="7095c-530">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="7095c-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="7095c-531">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="7095c-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="7095c-532">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="7095c-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="7095c-533">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7095c-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="7095c-534">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="7095c-534">Job type</span></span>   | <span data-ttu-id="7095c-535">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="7095c-536">Tímar</span><span class="sxs-lookup"><span data-stu-id="7095c-536">Hourly</span></span>     | <span data-ttu-id="7095c-537">MX tímakaup</span><span class="sxs-lookup"><span data-stu-id="7095c-537">MX Hourly</span></span>   |
| <span data-ttu-id="7095c-538">Föst laun</span><span class="sxs-lookup"><span data-stu-id="7095c-538">Salaried</span></span>   | <span data-ttu-id="7095c-539">MX föst laun</span><span class="sxs-lookup"><span data-stu-id="7095c-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="7095c-540">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="7095c-540">Position types</span></span> 

<span data-ttu-id="7095c-541">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="7095c-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="7095c-542">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="7095c-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="7095c-543">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7095c-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="7095c-544">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="7095c-544">Position type</span></span>   | <span data-ttu-id="7095c-545">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="7095c-546">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="7095c-546">Full-time</span></span>       | <span data-ttu-id="7095c-547">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="7095c-547">Full time employee</span></span> |
| <span data-ttu-id="7095c-548">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="7095c-548">Part-time</span></span>       | <span data-ttu-id="7095c-549">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="7095c-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="7095c-550">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-550">Reason codes</span></span>

<span data-ttu-id="7095c-551">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7095c-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="7095c-552">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="7095c-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="7095c-553">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7095c-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="7095c-554">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="7095c-554">Reason code</span></span>            | <span data-ttu-id="7095c-555">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-555">Description</span></span>                    | <span data-ttu-id="7095c-556">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="7095c-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="7095c-557">BROTTFÖR Á UNDAN LAUNAGREIÐSLU</span><span class="sxs-lookup"><span data-stu-id="7095c-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="7095c-558">Brottför á undan launum</span><span class="sxs-lookup"><span data-stu-id="7095c-558">Departure before first payroll</span></span> | <span data-ttu-id="7095c-559">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-559">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-560">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="7095c-560">RESIGNATION</span></span>            | <span data-ttu-id="7095c-561">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="7095c-561">Resignation</span></span>                    | <span data-ttu-id="7095c-562">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-562">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-563">LÍFEYRIR</span><span class="sxs-lookup"><span data-stu-id="7095c-563">PENSION</span></span>                | <span data-ttu-id="7095c-564">Lífeyrir</span><span class="sxs-lookup"><span data-stu-id="7095c-564">Pension</span></span>                        | <span data-ttu-id="7095c-565">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-565">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-566">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="7095c-566">TERMINATION</span></span>            | <span data-ttu-id="7095c-567">Lok</span><span class="sxs-lookup"><span data-stu-id="7095c-567">Termination</span></span>                    | <span data-ttu-id="7095c-568">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-568">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-569">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="7095c-569">RETIREMENT</span></span>             | <span data-ttu-id="7095c-570">Starfslok</span><span class="sxs-lookup"><span data-stu-id="7095c-570">Retirement</span></span>                     | <span data-ttu-id="7095c-571">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-571">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-572">FJARVERA</span><span class="sxs-lookup"><span data-stu-id="7095c-572">ABSENTEE</span></span>               | <span data-ttu-id="7095c-573">Fjarvera</span><span class="sxs-lookup"><span data-stu-id="7095c-573">Absentee</span></span>                       | <span data-ttu-id="7095c-574">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-574">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-575">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="7095c-575">OTHER</span></span>                  | <span data-ttu-id="7095c-576">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="7095c-576">Other Reasons</span></span>                  | <span data-ttu-id="7095c-577">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-577">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-578">LOKUN</span><span class="sxs-lookup"><span data-stu-id="7095c-578">CLOSURE</span></span>                | <span data-ttu-id="7095c-579">Viðskiptalokun</span><span class="sxs-lookup"><span data-stu-id="7095c-579">Business Closure</span></span>               | <span data-ttu-id="7095c-580">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-580">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-581">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="7095c-581">DEATH</span></span>                  | <span data-ttu-id="7095c-582">Dauði</span><span class="sxs-lookup"><span data-stu-id="7095c-582">Death</span></span>                          | <span data-ttu-id="7095c-583">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-583">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-584">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="7095c-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="7095c-585">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="7095c-585">Leave of Absence</span></span>               | <span data-ttu-id="7095c-586">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-586">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-587">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="7095c-587">CONTRACTEND</span></span>            | <span data-ttu-id="7095c-588">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="7095c-588">End of Contract</span></span>                | <span data-ttu-id="7095c-589">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7095c-589">Terminate worker</span></span>     |
| <span data-ttu-id="7095c-590">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="7095c-590">SALARYCHANGE</span></span>           | <span data-ttu-id="7095c-591">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="7095c-591">Change of Salary</span></span>               | <span data-ttu-id="7095c-592">Laun</span><span class="sxs-lookup"><span data-stu-id="7095c-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="7095c-593">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="7095c-593">Terms of employment</span></span>

<span data-ttu-id="7095c-594">Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar.</span><span class="sxs-lookup"><span data-stu-id="7095c-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="7095c-595">Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.</span><span class="sxs-lookup"><span data-stu-id="7095c-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="7095c-596">Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7095c-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="7095c-597">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="7095c-597">Terms of employment</span></span>   | <span data-ttu-id="7095c-598">lýsing</span><span class="sxs-lookup"><span data-stu-id="7095c-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="7095c-599">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="7095c-599">Regular</span></span>               | <span data-ttu-id="7095c-600">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="7095c-600">Regular</span></span>     |
| <span data-ttu-id="7095c-601">Beint</span><span class="sxs-lookup"><span data-stu-id="7095c-601">Direct</span></span>                | <span data-ttu-id="7095c-602">Beint</span><span class="sxs-lookup"><span data-stu-id="7095c-602">Direct</span></span>      |
| <span data-ttu-id="7095c-603">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="7095c-603">Internship</span></span>            | <span data-ttu-id="7095c-604">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="7095c-604">Internship</span></span>  |
| <span data-ttu-id="7095c-605">Fast</span><span class="sxs-lookup"><span data-stu-id="7095c-605">Permanent</span></span>             | <span data-ttu-id="7095c-606">Fast</span><span class="sxs-lookup"><span data-stu-id="7095c-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="7095c-607">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="7095c-607">Marital status</span></span>

<span data-ttu-id="7095c-608">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7095c-609">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="7095c-610">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-610">Talent</span></span>                 | <span data-ttu-id="7095c-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="7095c-612">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7095c-612">Married</span></span>                | <span data-ttu-id="7095c-613">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7095c-613">Married</span></span>                   |
| <span data-ttu-id="7095c-614">Ein</span><span class="sxs-lookup"><span data-stu-id="7095c-614">Single</span></span>                 | <span data-ttu-id="7095c-615">Ein</span><span class="sxs-lookup"><span data-stu-id="7095c-615">Single</span></span>                    |
| <span data-ttu-id="7095c-616">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7095c-616">Widowed</span></span>                | <span data-ttu-id="7095c-617">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7095c-617">Widowed</span></span>                   |
| <span data-ttu-id="7095c-618">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7095c-618">Divorced</span></span>               | <span data-ttu-id="7095c-619">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7095c-619">Divorced</span></span>                  |
| <span data-ttu-id="7095c-620">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="7095c-620">Registered Partnership</span></span> | <span data-ttu-id="7095c-621">Sambúð</span><span class="sxs-lookup"><span data-stu-id="7095c-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="7095c-622">None</span><span class="sxs-lookup"><span data-stu-id="7095c-622">None</span></span>                   | <span data-ttu-id="7095c-623">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7095c-624">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="7095c-624">Cohabiting</span></span>             | <span data-ttu-id="7095c-625">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="7095c-626">Kyn</span><span class="sxs-lookup"><span data-stu-id="7095c-626">Gender</span></span>

<span data-ttu-id="7095c-627">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7095c-628">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="7095c-629">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-629">Talent</span></span>       | <span data-ttu-id="7095c-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="7095c-631">Karl</span><span class="sxs-lookup"><span data-stu-id="7095c-631">Male</span></span>         | <span data-ttu-id="7095c-632">Karl</span><span class="sxs-lookup"><span data-stu-id="7095c-632">Male</span></span>                      |
| <span data-ttu-id="7095c-633">Kona</span><span class="sxs-lookup"><span data-stu-id="7095c-633">Female</span></span>       | <span data-ttu-id="7095c-634">Kona</span><span class="sxs-lookup"><span data-stu-id="7095c-634">Female</span></span>                    |
| <span data-ttu-id="7095c-635">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="7095c-635">Non-specific</span></span> | <span data-ttu-id="7095c-636">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="7095c-637">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="7095c-637">Payment method</span></span>

<span data-ttu-id="7095c-638">Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="7095c-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="7095c-639">Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7095c-640">Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="7095c-641">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-641">Talent</span></span>             | <span data-ttu-id="7095c-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="7095c-643">Innlausn</span><span class="sxs-lookup"><span data-stu-id="7095c-643">Cash</span></span>               | <span data-ttu-id="7095c-644">Innlausn</span><span class="sxs-lookup"><span data-stu-id="7095c-644">Cash</span></span>                      |
| <span data-ttu-id="7095c-645">Rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="7095c-645">Electronic Payment</span></span> | <span data-ttu-id="7095c-646">Flutningur</span><span class="sxs-lookup"><span data-stu-id="7095c-646">Transfer</span></span>                  |
| <span data-ttu-id="7095c-647">Merkja</span><span class="sxs-lookup"><span data-stu-id="7095c-647">Check</span></span>              | <span data-ttu-id="7095c-648">Ávísun</span><span class="sxs-lookup"><span data-stu-id="7095c-648">Cheque</span></span>                    |
| <span data-ttu-id="7095c-649">Bankaávísun</span><span class="sxs-lookup"><span data-stu-id="7095c-649">Bank Draft</span></span>         | <span data-ttu-id="7095c-650">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7095c-651">Annað</span><span class="sxs-lookup"><span data-stu-id="7095c-651">Other</span></span>              | <span data-ttu-id="7095c-652">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="7095c-653">Gerð bankareiknings</span><span class="sxs-lookup"><span data-stu-id="7095c-653">Bank account type</span></span>

<span data-ttu-id="7095c-654">Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="7095c-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="7095c-655">Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga.</span><span class="sxs-lookup"><span data-stu-id="7095c-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="7095c-656">Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7095c-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="7095c-657">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-657">Talent</span></span>            | <span data-ttu-id="7095c-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="7095c-659">Ávísanareikningur</span><span class="sxs-lookup"><span data-stu-id="7095c-659">Checking Account</span></span>  | <span data-ttu-id="7095c-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="7095c-660">CheckingAccount</span></span>           |
| <span data-ttu-id="7095c-661">Launareikningur</span><span class="sxs-lookup"><span data-stu-id="7095c-661">Payroll Account</span></span>   | <span data-ttu-id="7095c-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="7095c-662">PayrollAccount</span></span>            |
| <span data-ttu-id="7095c-663">Sparnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="7095c-663">Savings Account</span></span>   | <span data-ttu-id="7095c-664">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7095c-665">BankGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="7095c-665">BankGirot account</span></span> | <span data-ttu-id="7095c-666">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7095c-667">PlusGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="7095c-667">PlusGirot account</span></span> | <span data-ttu-id="7095c-668">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7095c-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="7095c-669">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7095c-669">Earning codes</span></span>

<span data-ttu-id="7095c-670">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="7095c-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7095c-671">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="7095c-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="7095c-672">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="7095c-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="7095c-673">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="7095c-673">Supported frequencies</span></span>

- <span data-ttu-id="7095c-674">Allir</span><span class="sxs-lookup"><span data-stu-id="7095c-674">All</span></span>
- <span data-ttu-id="7095c-675">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="7095c-675">EVERYPAY</span></span>
- <span data-ttu-id="7095c-676">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="7095c-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="7095c-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="7095c-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="7095c-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="7095c-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="7095c-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-679">1OFMTH</span></span>
- <span data-ttu-id="7095c-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-680">LASTOFMTH</span></span>
- <span data-ttu-id="7095c-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-681">2OFMTH</span></span>
- <span data-ttu-id="7095c-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-682">3OFMTH</span></span>
- <span data-ttu-id="7095c-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-683">4OFMTH</span></span>
- <span data-ttu-id="7095c-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-684">5OFMTH</span></span>
- <span data-ttu-id="7095c-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-685">1N2OFMTH</span></span>
- <span data-ttu-id="7095c-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-686">3N4OFMTH</span></span>
- <span data-ttu-id="7095c-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-687">1N3OFMTH</span></span>
- <span data-ttu-id="7095c-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-688">1N4OFMTH</span></span>
- <span data-ttu-id="7095c-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-689">2N3OFMTH</span></span>
- <span data-ttu-id="7095c-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-690">2N4OFMTH</span></span>
- <span data-ttu-id="7095c-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="7095c-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="7095c-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="7095c-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="7095c-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7095c-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="7095c-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="7095c-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="7095c-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="7095c-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="7095c-698">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="7095c-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="7095c-699">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="7095c-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="7095c-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="7095c-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="7095c-701">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7095c-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="7095c-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7095c-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="7095c-703">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="7095c-703">Addresses</span></span>

<span data-ttu-id="7095c-704">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="7095c-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="7095c-705">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="7095c-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="7095c-706">Talent</span><span class="sxs-lookup"><span data-stu-id="7095c-706">Talent</span></span>              | <span data-ttu-id="7095c-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7095c-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="7095c-708">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="7095c-708">Country/Region</span></span>      | <span data-ttu-id="7095c-709">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-709">Country Code</span></span>          |
| <span data-ttu-id="7095c-710">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-710">Zip/Postal Code</span></span>     | <span data-ttu-id="7095c-711">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-711">Postal Code</span></span>           |
| <span data-ttu-id="7095c-712">Ríki</span><span class="sxs-lookup"><span data-stu-id="7095c-712">State</span></span>               | <span data-ttu-id="7095c-713">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="7095c-713">State Code</span></span>            |
| <span data-ttu-id="7095c-714">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7095c-714">City</span></span>                | <span data-ttu-id="7095c-715">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7095c-715">City</span></span>                  |
| <span data-ttu-id="7095c-716">Sýsla</span><span class="sxs-lookup"><span data-stu-id="7095c-716">County</span></span>              | <span data-ttu-id="7095c-717">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="7095c-717">County (Municipality)</span></span> |
| <span data-ttu-id="7095c-718">Gata</span><span class="sxs-lookup"><span data-stu-id="7095c-718">Street</span></span>              | <span data-ttu-id="7095c-719">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="7095c-719">Address Line 1</span></span>        |
| <span data-ttu-id="7095c-720">Húsnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-720">Street Number</span></span>       | <span data-ttu-id="7095c-721">Heimilisfang, lína 2</span><span class="sxs-lookup"><span data-stu-id="7095c-721">Address Line 2</span></span>        |
| <span data-ttu-id="7095c-722">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="7095c-722">Building Complement</span></span> | <span data-ttu-id="7095c-723">Heimilisfang, lína 5</span><span class="sxs-lookup"><span data-stu-id="7095c-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="7095c-724">Vegabréfsnúmer</span><span class="sxs-lookup"><span data-stu-id="7095c-724">Passport number</span></span>

<span data-ttu-id="7095c-725">Starfsmenn geta gefið upp vegabréfsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="7095c-725">Employees can declare passport information.</span></span> <span data-ttu-id="7095c-726">Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7095c-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="7095c-727">Gerð auðkennis = „Vegabréf“</span><span class="sxs-lookup"><span data-stu-id="7095c-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="7095c-728">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="7095c-728">Issued Date</span></span>
- <span data-ttu-id="7095c-729">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="7095c-729">Expiration Date</span></span>

<span data-ttu-id="7095c-730">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**.</span><span class="sxs-lookup"><span data-stu-id="7095c-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="7095c-731">Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="7095c-732">Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7095c-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

---
title: "Skilgreina launasamþættingu milli Talent og Dayforce"
description: "Þetta efnisatriði útskýrir hvernig á að grunnstilla samþættingu milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce svo hægt sé að afgreiða launakeyrslu."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="c3464-103">Skilgreina launasamþættingu milli Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3464-104">Samþættingin milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="c3464-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="c3464-105">Nauðsynlegt er að skilgreina samþættinguna bæði í Talent og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="c3464-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="c3464-106">Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Talent.</span><span class="sxs-lookup"><span data-stu-id="c3464-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="c3464-107">Samþættingin krefst tilgreindra gagna frá Talent.</span><span class="sxs-lookup"><span data-stu-id="c3464-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="c3464-108">Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Talent á þann hátt sem styður samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="c3464-109">Samþættingin notar eftirfarandi víðtæka flokka gagna:</span><span class="sxs-lookup"><span data-stu-id="c3464-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="c3464-110">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="c3464-110">Human resources data</span></span>
- <span data-ttu-id="c3464-111">Launagögn</span><span class="sxs-lookup"><span data-stu-id="c3464-111">Compensation data</span></span>
- <span data-ttu-id="c3464-112">Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="c3464-113">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="c3464-113">Worker data</span></span>

<span data-ttu-id="c3464-114">Þetta efnisatriði fjallar um skrefin sem verður að fylgja til að virkja samþættinginu.</span><span class="sxs-lookup"><span data-stu-id="c3464-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="c3464-115">Það útskýrir einnig gerð gagna og upplýsingar um skilgreiningar sem samþættingin krefst.</span><span class="sxs-lookup"><span data-stu-id="c3464-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="c3464-116">Virkja samþættingu</span><span class="sxs-lookup"><span data-stu-id="c3464-116">Enable the integration</span></span>

<span data-ttu-id="c3464-117">Í Talent er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="c3464-118">Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 for Finance and Operations þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3464-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="c3464-119">Til að kveikja á samþættingu í Talent skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c3464-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="c3464-120">Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="c3464-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="c3464-121">Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.</span><span class="sxs-lookup"><span data-stu-id="c3464-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="c3464-122">Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.</span><span class="sxs-lookup"><span data-stu-id="c3464-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="c3464-123">Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c3464-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="c3464-124">Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt.</span><span class="sxs-lookup"><span data-stu-id="c3464-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="c3464-125">Hægt er að breyta tíðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c3464-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="c3464-126">Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi efnisatriðum Azure:</span><span class="sxs-lookup"><span data-stu-id="c3464-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="c3464-127">Um Azure-geymslureikninga</span><span class="sxs-lookup"><span data-stu-id="c3464-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="c3464-128">Skilgreina tengistrengi Azure-geymslu</span><span class="sxs-lookup"><span data-stu-id="c3464-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="c3464-129">Skilgreina gögnin þín</span><span class="sxs-lookup"><span data-stu-id="c3464-129">Configure your data</span></span> 

<span data-ttu-id="c3464-130">Til að afgreiða laun þarf að skilgreina mannauðsgögn í Talent.</span><span class="sxs-lookup"><span data-stu-id="c3464-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="c3464-131">Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun.</span><span class="sxs-lookup"><span data-stu-id="c3464-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="c3464-132">Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.</span><span class="sxs-lookup"><span data-stu-id="c3464-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="c3464-133">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="c3464-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="c3464-134">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="c3464-134">Benefits</span></span> 

<span data-ttu-id="c3464-135">Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.</span><span class="sxs-lookup"><span data-stu-id="c3464-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="c3464-136">Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="c3464-137">Fríðindaáætlanir</span><span class="sxs-lookup"><span data-stu-id="c3464-137">Benefit plans</span></span>

- <span data-ttu-id="c3464-138">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-138">Plan (required)</span></span>
- <span data-ttu-id="c3464-139">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-139">Type (required)</span></span>
- <span data-ttu-id="c3464-140">Áhrif á launaskrá (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-140">Payroll impact (required)</span></span>
- <span data-ttu-id="c3464-141">Endurheimta vangoldnar greiðslur</span><span class="sxs-lookup"><span data-stu-id="c3464-141">Recover arrears</span></span>
- <span data-ttu-id="c3464-142">Frádráttaraðferð</span><span class="sxs-lookup"><span data-stu-id="c3464-142">Deduction method</span></span>
- <span data-ttu-id="c3464-143">Frádráttarforgangur</span><span class="sxs-lookup"><span data-stu-id="c3464-143">Deduction priority</span></span>
- <span data-ttu-id="c3464-144">Takmörkunartímabil</span><span class="sxs-lookup"><span data-stu-id="c3464-144">Limit period</span></span>
- <span data-ttu-id="c3464-145">Takmarka upphæð</span><span class="sxs-lookup"><span data-stu-id="c3464-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="c3464-146">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="c3464-146">Benefits</span></span>

- <span data-ttu-id="c3464-147">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-147">Plan (required)</span></span>
- <span data-ttu-id="c3464-148">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-148">Type (required)</span></span>
- <span data-ttu-id="c3464-149">Valkostur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-149">Option (required)</span></span>
- <span data-ttu-id="c3464-150">Fríðindaauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-150">Benefit ID (required)</span></span>
- <span data-ttu-id="c3464-151">Tíðni</span><span class="sxs-lookup"><span data-stu-id="c3464-151">Frequency</span></span>
- <span data-ttu-id="c3464-152">Grunnur</span><span class="sxs-lookup"><span data-stu-id="c3464-152">Basis</span></span>
- <span data-ttu-id="c3464-153">Upphæð eða taxti</span><span class="sxs-lookup"><span data-stu-id="c3464-153">Amount or rate</span></span>
- <span data-ttu-id="c3464-154">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="c3464-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="c3464-155">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="c3464-155">Supported frequencies</span></span> 

- <span data-ttu-id="c3464-156">Vikulega</span><span class="sxs-lookup"><span data-stu-id="c3464-156">Weekly</span></span>
- <span data-ttu-id="c3464-157">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c3464-157">Bi-weekly</span></span>
- <span data-ttu-id="c3464-158">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c3464-158">Semi-monthly</span></span>
- <span data-ttu-id="c3464-159">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c3464-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="c3464-160">Studdir grunnar</span><span class="sxs-lookup"><span data-stu-id="c3464-160">Supported bases</span></span> 

- <span data-ttu-id="c3464-161">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="c3464-161">Fixed amount</span></span>
- <span data-ttu-id="c3464-162">Prósenta af tekjum</span><span class="sxs-lookup"><span data-stu-id="c3464-162">Percent of earnings</span></span>
- <span data-ttu-id="c3464-163">Virkar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="c3464-163">Productive hours</span></span>

<span data-ttu-id="c3464-164">Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.</span><span class="sxs-lookup"><span data-stu-id="c3464-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="c3464-165">Val í Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-165">Selection in Talent</span></span>        | <span data-ttu-id="c3464-166">Niðurstaða í Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c3464-167">None</span><span class="sxs-lookup"><span data-stu-id="c3464-167">None</span></span>                       | <span data-ttu-id="c3464-168">Enginn frádráttur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="c3464-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="c3464-169">Eingöngu frádráttur</span><span class="sxs-lookup"><span data-stu-id="c3464-169">Deduction only</span></span>             | <span data-ttu-id="c3464-170">Frádráttur starfsmanns er búinn til.</span><span class="sxs-lookup"><span data-stu-id="c3464-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="c3464-171">Eingöngu framlag</span><span class="sxs-lookup"><span data-stu-id="c3464-171">Contribution only</span></span>          | <span data-ttu-id="c3464-172">Frádráttur vinnuveitanda er búinn til.</span><span class="sxs-lookup"><span data-stu-id="c3464-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="c3464-173">Frádráttur og framlag</span><span class="sxs-lookup"><span data-stu-id="c3464-173">Deduction and contribution</span></span> | <span data-ttu-id="c3464-174">Frádrættir starfsmanns og vinnuveitanda eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="c3464-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="c3464-175">Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="c3464-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="c3464-176">Leggja fram fríðindaáætlun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="c3464-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="c3464-177">Stofna ný fríðindi</span><span class="sxs-lookup"><span data-stu-id="c3464-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="c3464-178">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="c3464-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="c3464-179">Skrá og fjarlægja fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="c3464-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="c3464-180">Laun</span><span class="sxs-lookup"><span data-stu-id="c3464-180">Compensation</span></span> 

<span data-ttu-id="c3464-181">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="c3464-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="c3464-182">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="c3464-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="c3464-183">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="c3464-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="c3464-184">Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c3464-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="c3464-185">Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta.</span><span class="sxs-lookup"><span data-stu-id="c3464-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="c3464-186">Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="c3464-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="c3464-187">Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="c3464-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="c3464-188">Launafyrirkomulag fastra launa stofnað</span><span class="sxs-lookup"><span data-stu-id="c3464-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="c3464-189">Launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="c3464-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="c3464-190">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="c3464-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="c3464-191">Launaútreikningur</span><span class="sxs-lookup"><span data-stu-id="c3464-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="c3464-192">Skilgreina launavinnslu og reikna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="c3464-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="c3464-193">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="c3464-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="c3464-194">Skrá starfsmann í launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="c3464-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="c3464-195">Störf</span><span class="sxs-lookup"><span data-stu-id="c3464-195">Jobs</span></span> 

<span data-ttu-id="c3464-196">Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið.</span><span class="sxs-lookup"><span data-stu-id="c3464-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="c3464-197">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="c3464-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c3464-198">Setja upp íhluta verks</span><span class="sxs-lookup"><span data-stu-id="c3464-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="c3464-199">Skilgreina ný störf</span><span class="sxs-lookup"><span data-stu-id="c3464-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="c3464-200">Stöður</span><span class="sxs-lookup"><span data-stu-id="c3464-200">Positions</span></span>

<span data-ttu-id="c3464-201">Staða er sérstakt tilvik starfs.</span><span class="sxs-lookup"><span data-stu-id="c3464-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="c3464-202">Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“.</span><span class="sxs-lookup"><span data-stu-id="c3464-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="c3464-203">Staða er til í deild.</span><span class="sxs-lookup"><span data-stu-id="c3464-203">A position exists in a department.</span></span> <span data-ttu-id="c3464-204">Einungis einn starfsmaður getur tengst hverri stöðu.</span><span class="sxs-lookup"><span data-stu-id="c3464-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="c3464-205">Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:</span><span class="sxs-lookup"><span data-stu-id="c3464-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="c3464-206">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-206">Position (required)</span></span>
- <span data-ttu-id="c3464-207">Lýsing (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-207">Description (required)</span></span>
- <span data-ttu-id="c3464-208">Starf (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-208">Job (required)</span></span>
- <span data-ttu-id="c3464-209">Deild (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-209">Department (required)</span></span>
- <span data-ttu-id="c3464-210">Stöðugerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-210">Position type (required)</span></span>
- <span data-ttu-id="c3464-211">Jafngildi fulls starfs</span><span class="sxs-lookup"><span data-stu-id="c3464-211">Full-time equivalent</span></span>
- <span data-ttu-id="c3464-212">Reglulegar árlegar vinnustundir (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="c3464-213">Greitt eftir lögaðila (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="c3464-214">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-214">Pay cycle (required)</span></span>
- <span data-ttu-id="c3464-215">Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="c3464-216">Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="c3464-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="c3464-217">Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="c3464-218">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="c3464-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c3464-219">Vinnuafl skipulagt með notkun deilda, starfa og staða</span><span class="sxs-lookup"><span data-stu-id="c3464-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="c3464-220">Setja upp stöður</span><span class="sxs-lookup"><span data-stu-id="c3464-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="c3464-221">Deildir</span><span class="sxs-lookup"><span data-stu-id="c3464-221">Departments</span></span>

<span data-ttu-id="c3464-222">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c3464-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="c3464-223">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="c3464-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="c3464-224">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="c3464-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="c3464-225">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="c3464-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="c3464-226">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="c3464-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c3464-227">Stofnun deildar og tenging hennar við deildastigveldið</span><span class="sxs-lookup"><span data-stu-id="c3464-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="c3464-228">Skilgreina nýjar deildir</span><span class="sxs-lookup"><span data-stu-id="c3464-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="c3464-229">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="c3464-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="c3464-230">Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="c3464-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="c3464-231">Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="c3464-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="c3464-232">Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur.</span><span class="sxs-lookup"><span data-stu-id="c3464-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="c3464-233">Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.</span><span class="sxs-lookup"><span data-stu-id="c3464-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="c3464-234">Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli.</span><span class="sxs-lookup"><span data-stu-id="c3464-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="c3464-235">Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp.</span><span class="sxs-lookup"><span data-stu-id="c3464-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="c3464-236">Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.</span><span class="sxs-lookup"><span data-stu-id="c3464-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="c3464-237">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="c3464-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c3464-238">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-238">Pay cycle (required)</span></span>
- <span data-ttu-id="c3464-239">Tíðni greiðsluferlis (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="c3464-240">Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="c3464-241">Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="c3464-242">Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="c3464-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="c3464-243">Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="c3464-244">Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Talent.</span><span class="sxs-lookup"><span data-stu-id="c3464-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="c3464-245">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-245">Earning codes</span></span>

<span data-ttu-id="c3464-246">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="c3464-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c3464-247">Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="c3464-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="c3464-248">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="c3464-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c3464-249">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-249">Earning Code (required)</span></span>
- <span data-ttu-id="c3464-250">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-250">Description</span></span>
- <span data-ttu-id="c3464-251">Mælieining</span><span class="sxs-lookup"><span data-stu-id="c3464-251">Unit of measure</span></span>
- <span data-ttu-id="c3464-252">Framleiðni</span><span class="sxs-lookup"><span data-stu-id="c3464-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="c3464-253">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="c3464-253">Worker data</span></span>

<span data-ttu-id="c3464-254">Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="c3464-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="c3464-255">Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="c3464-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="c3464-256">Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:</span><span class="sxs-lookup"><span data-stu-id="c3464-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="c3464-257">**Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c3464-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="c3464-258">**Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.</span><span class="sxs-lookup"><span data-stu-id="c3464-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="c3464-259">**Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.</span><span class="sxs-lookup"><span data-stu-id="c3464-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="c3464-260">**Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.</span><span class="sxs-lookup"><span data-stu-id="c3464-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="c3464-261">Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="c3464-262">Almennar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c3464-262">General information</span></span>

- <span data-ttu-id="c3464-263">Númer starfsmanns (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-263">Personnel number (required)</span></span>
- <span data-ttu-id="c3464-264">Fornafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-264">First name (required)</span></span>
- <span data-ttu-id="c3464-265">Eftirnafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-265">Last name (required)</span></span>
- <span data-ttu-id="c3464-266">Millinafn</span><span class="sxs-lookup"><span data-stu-id="c3464-266">Middle name</span></span>
- <span data-ttu-id="c3464-267">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="c3464-267">Seniority date</span></span>
- <span data-ttu-id="c3464-268">Þekkt sem</span><span class="sxs-lookup"><span data-stu-id="c3464-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="c3464-269">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c3464-269">Personal information</span></span>

- <span data-ttu-id="c3464-270">Hjúskaparstaða (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-270">Marital status (required)</span></span>
- <span data-ttu-id="c3464-271">Fæðingardagur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-271">Birth date (required)</span></span>
- <span data-ttu-id="c3464-272">Kyn (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-272">Gender (required)</span></span>
- <span data-ttu-id="c3464-273">Einstaklingur sem á við fötlun að stríða</span><span class="sxs-lookup"><span data-stu-id="c3464-273">Person with disabilities</span></span>
- <span data-ttu-id="c3464-274">Þjóðerni land svæði (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="c3464-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="c3464-275">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="c3464-275">Address information</span></span>

- <span data-ttu-id="c3464-276">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-276">Primary (required)</span></span>
- <span data-ttu-id="c3464-277">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-277">Country/region (required)</span></span>
- <span data-ttu-id="c3464-278">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-278">Postal code (required)</span></span>
- <span data-ttu-id="c3464-279">Götunúmer (krafist) (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="c3464-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="c3464-280">Viðbygging (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="c3464-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="c3464-281">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-281">City (required)</span></span>
- <span data-ttu-id="c3464-282">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-282">State (required)</span></span>
- <span data-ttu-id="c3464-283">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="c3464-284">Samskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c3464-284">Contact information</span></span> 

- <span data-ttu-id="c3464-285">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-285">Primary (required)</span></span>
- <span data-ttu-id="c3464-286">Símanúmer tengiliðar (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-286">Contact number (required)</span></span>
- <span data-ttu-id="c3464-287">Skráarending</span><span class="sxs-lookup"><span data-stu-id="c3464-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="c3464-288">Launaupplýsingar og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-288">Payroll information and earning codes</span></span>

<span data-ttu-id="c3464-289">Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c3464-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="c3464-290">Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.</span><span class="sxs-lookup"><span data-stu-id="c3464-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="c3464-291">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-291">Earning codes</span></span>

- <span data-ttu-id="c3464-292">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-292">Position (required)</span></span>
- <span data-ttu-id="c3464-293">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-293">Earning Code (required)</span></span>
- <span data-ttu-id="c3464-294">Tíðni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-294">Frequency (required)</span></span>
- <span data-ttu-id="c3464-295">Upphæð (áskilin)</span><span class="sxs-lookup"><span data-stu-id="c3464-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="c3464-296">Launaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c3464-296">Payroll information</span></span>

- <span data-ttu-id="c3464-297">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="c3464-297">Payment Method</span></span>
- <span data-ttu-id="c3464-298">Efnahagssvæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-298">Economic Region (required)</span></span>
- <span data-ttu-id="c3464-299">Kenni fyrir fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="c3464-299">Employee Benefits ID</span></span>
- <span data-ttu-id="c3464-300">Kennitala (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-300">National ID Number (required)</span></span>
- <span data-ttu-id="c3464-301">Hernaðarþjónustunúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-301">Military Service Number</span></span>
- <span data-ttu-id="c3464-302">Auðkenni vaktar (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-302">Shift ID (required)</span></span>
- <span data-ttu-id="c3464-303">Skattanúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-303">Tax Number (required)</span></span>
- <span data-ttu-id="c3464-304">Auðkenni stéttarfélags (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-304">Union ID (required)</span></span>
- <span data-ttu-id="c3464-305">Vinnudagskenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-305">Work Day ID (required)</span></span>
- <span data-ttu-id="c3464-306">Vinnuleyfisnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="c3464-307">Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="c3464-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="c3464-308">Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="c3464-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="c3464-309">Atvinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c3464-309">Employment details</span></span>

<span data-ttu-id="c3464-310">Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="c3464-311">Dayforce styður aðeins eina starfsferilsskrá í einu.</span><span class="sxs-lookup"><span data-stu-id="c3464-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="c3464-312">Upphafsdagsetning ráðningar (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-312">Employment start date (required)</span></span>
- <span data-ttu-id="c3464-313">Dagsetning starfsloka</span><span class="sxs-lookup"><span data-stu-id="c3464-313">Employment end date</span></span>
- <span data-ttu-id="c3464-314">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="c3464-314">Start date</span></span>
- <span data-ttu-id="c3464-315">Breyttur fyrsti starfsdagur</span><span class="sxs-lookup"><span data-stu-id="c3464-315">Adjusted start date</span></span>
- <span data-ttu-id="c3464-316">Dagsetning starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="c3464-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="c3464-317">Ástæða starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="c3464-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="c3464-318">Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="c3464-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="c3464-319">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-319">Talent</span></span>                | <span data-ttu-id="c3464-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3464-321">Nýlegasti ráðningardagurinn</span><span class="sxs-lookup"><span data-stu-id="c3464-321">Most recent hire date</span></span> | <span data-ttu-id="c3464-322">Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="c3464-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c3464-323">Starfslokadagur</span><span class="sxs-lookup"><span data-stu-id="c3464-323">Termination date</span></span>      | <span data-ttu-id="c3464-324">Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="c3464-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c3464-325">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="c3464-325">Start date</span></span>            | <span data-ttu-id="c3464-326">Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="c3464-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="c3464-327">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="c3464-327">Original hire date</span></span>    | <span data-ttu-id="c3464-328">Upphaf ráðningar fyrir elsta atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="c3464-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="c3464-329">Laun</span><span class="sxs-lookup"><span data-stu-id="c3464-329">Compensation</span></span>

<span data-ttu-id="c3464-330">Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil.</span><span class="sxs-lookup"><span data-stu-id="c3464-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="c3464-331">Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.</span><span class="sxs-lookup"><span data-stu-id="c3464-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="c3464-332">Gildisdagsetning (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-332">Effective Date (required)</span></span>
- <span data-ttu-id="c3464-333">Gildistími</span><span class="sxs-lookup"><span data-stu-id="c3464-333">Expiration date</span></span>
- <span data-ttu-id="c3464-334">Launataxti (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-334">Pay Rate (required)</span></span>
- <span data-ttu-id="c3464-335">Umreikningur launataxta (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="c3464-336">Árlegt jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="c3464-337">Klukkutíma jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="c3464-338">Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c3464-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="c3464-339">Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="c3464-340">Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c3464-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="c3464-341">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="c3464-342">Auðkenni kennitölu</span><span class="sxs-lookup"><span data-stu-id="c3464-342">Social Security identifier</span></span> 

<span data-ttu-id="c3464-343">Sérhver starfsmaður verður að hafa eitt aðalauðkenni.</span><span class="sxs-lookup"><span data-stu-id="c3464-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="c3464-344">Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="c3464-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="c3464-345">Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="c3464-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="c3464-346">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-346">Primary (required)</span></span>
- <span data-ttu-id="c3464-347">Gerð auðkennis = „Kennitala“</span><span class="sxs-lookup"><span data-stu-id="c3464-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="c3464-348">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="c3464-348">Issued Date</span></span>
- <span data-ttu-id="c3464-349">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="c3464-349">Expiration Date</span></span>

<span data-ttu-id="c3464-350">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="c3464-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="c3464-351">Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.</span><span class="sxs-lookup"><span data-stu-id="c3464-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="c3464-352">Bankareikningar og útborganir</span><span class="sxs-lookup"><span data-stu-id="c3464-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="c3464-353">Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="c3464-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="c3464-354">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-354">Talent</span></span>                         | <span data-ttu-id="c3464-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3464-356">Bankareikningsnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="c3464-357">SWIFT-kóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-357">SWIFT code (required)</span></span>          | <span data-ttu-id="c3464-358">Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="c3464-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="c3464-359">Númer útibús (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="c3464-360">Gerð bankareiknings (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-360">Bank account type (required)</span></span>   | <span data-ttu-id="c3464-361">Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="c3464-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="c3464-362">Studd gildi innihalda **Athugun** og **Launaskrá**.</span><span class="sxs-lookup"><span data-stu-id="c3464-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="c3464-363">Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka.</span><span class="sxs-lookup"><span data-stu-id="c3464-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="c3464-364">Allir aðrir reikningar eru hunsaðir.</span><span class="sxs-lookup"><span data-stu-id="c3464-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="c3464-365">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="c3464-365">Address information</span></span>

<span data-ttu-id="c3464-366">Sérhver starfsmaður verður að hafa eina aðalstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="c3464-366">Every employee must have one primary location.</span></span> <span data-ttu-id="c3464-367">Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="c3464-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="c3464-368">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-368">Primary (required)</span></span>
- <span data-ttu-id="c3464-369">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-369">Country/region (required)</span></span>
- <span data-ttu-id="c3464-370">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="c3464-371">Gata (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-371">Street (required)</span></span>
- <span data-ttu-id="c3464-372">Götunúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-372">Street Number (required)</span></span>
- <span data-ttu-id="c3464-373">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="c3464-373">Building Complement</span></span>
- <span data-ttu-id="c3464-374">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-374">City (required)</span></span>
- <span data-ttu-id="c3464-375">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-375">State (required)</span></span>
- <span data-ttu-id="c3464-376">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="c3464-377">Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada</span><span class="sxs-lookup"><span data-stu-id="c3464-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="c3464-378">Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="c3464-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="c3464-379">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="c3464-379">Departments are required on positions.</span></span>
- <span data-ttu-id="c3464-380">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="c3464-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="c3464-381">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="c3464-381">Job types</span></span>

<span data-ttu-id="c3464-382">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="c3464-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c3464-383">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="c3464-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="c3464-384">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="c3464-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c3464-385">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="c3464-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c3464-386">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c3464-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c3464-387">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="c3464-387">Job type</span></span>   | <span data-ttu-id="c3464-388">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c3464-389">Tímar</span><span class="sxs-lookup"><span data-stu-id="c3464-389">Hourly</span></span>     | <span data-ttu-id="c3464-390">Tímar</span><span class="sxs-lookup"><span data-stu-id="c3464-390">Hourly</span></span>      |
| <span data-ttu-id="c3464-391">Föst laun</span><span class="sxs-lookup"><span data-stu-id="c3464-391">Salaried</span></span>   | <span data-ttu-id="c3464-392">Föst laun</span><span class="sxs-lookup"><span data-stu-id="c3464-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="c3464-393">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="c3464-393">Position types</span></span> 

<span data-ttu-id="c3464-394">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="c3464-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c3464-395">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="c3464-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c3464-396">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c3464-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c3464-397">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="c3464-397">Position type</span></span>   | <span data-ttu-id="c3464-398">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c3464-399">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="c3464-399">Full-time</span></span>       | <span data-ttu-id="c3464-400">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="c3464-400">Full time employee</span></span> |
| <span data-ttu-id="c3464-401">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="c3464-401">Part-time</span></span>       | <span data-ttu-id="c3464-402">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="c3464-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c3464-403">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-403">Reason codes</span></span>

<span data-ttu-id="c3464-404">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c3464-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c3464-405">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="c3464-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c3464-406">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c3464-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c3464-407">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="c3464-407">Reason code</span></span>    | <span data-ttu-id="c3464-408">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-408">Description</span></span>      | <span data-ttu-id="c3464-409">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="c3464-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="c3464-410">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="c3464-410">RESIGNATION</span></span>    | <span data-ttu-id="c3464-411">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="c3464-411">Resignation</span></span>      | <span data-ttu-id="c3464-412">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-412">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-413">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="c3464-413">TERMINATION</span></span>    | <span data-ttu-id="c3464-414">Lok</span><span class="sxs-lookup"><span data-stu-id="c3464-414">Termination</span></span>      | <span data-ttu-id="c3464-415">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-415">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-416">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="c3464-416">RETIREMENT</span></span>     | <span data-ttu-id="c3464-417">Starfslok</span><span class="sxs-lookup"><span data-stu-id="c3464-417">Retirement</span></span>       | <span data-ttu-id="c3464-418">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-418">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-419">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="c3464-419">OTHER</span></span>          | <span data-ttu-id="c3464-420">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="c3464-420">Other Reasons</span></span>    | <span data-ttu-id="c3464-421">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-421">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-422">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="c3464-422">DEATH</span></span>          | <span data-ttu-id="c3464-423">Dauði</span><span class="sxs-lookup"><span data-stu-id="c3464-423">Death</span></span>            | <span data-ttu-id="c3464-424">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-424">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-425">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="c3464-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="c3464-426">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="c3464-426">Leave of Absence</span></span> | <span data-ttu-id="c3464-427">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-427">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-428">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="c3464-428">CONTRACTEND</span></span>    | <span data-ttu-id="c3464-429">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="c3464-429">End of Contract</span></span>  | <span data-ttu-id="c3464-430">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-430">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-431">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="c3464-431">SALARYCHANGE</span></span>   | <span data-ttu-id="c3464-432">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="c3464-432">Change of Salary</span></span> | <span data-ttu-id="c3464-433">Laun</span><span class="sxs-lookup"><span data-stu-id="c3464-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="c3464-434">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="c3464-434">Marital status</span></span>

<span data-ttu-id="c3464-435">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c3464-436">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c3464-437">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-437">Talent</span></span>                 | <span data-ttu-id="c3464-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="c3464-439">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c3464-439">Married</span></span>                | <span data-ttu-id="c3464-440">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c3464-440">Married</span></span>              |
| <span data-ttu-id="c3464-441">Ein</span><span class="sxs-lookup"><span data-stu-id="c3464-441">Single</span></span>                 | <span data-ttu-id="c3464-442">Ein</span><span class="sxs-lookup"><span data-stu-id="c3464-442">Single</span></span>               |
| <span data-ttu-id="c3464-443">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c3464-443">Widowed</span></span>                | <span data-ttu-id="c3464-444">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c3464-444">Widowed</span></span>              |
| <span data-ttu-id="c3464-445">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c3464-445">Divorced</span></span>               | <span data-ttu-id="c3464-446">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c3464-446">Divorced</span></span>             |
| <span data-ttu-id="c3464-447">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="c3464-447">Registered Partnership</span></span> | <span data-ttu-id="c3464-448">Sambúð</span><span class="sxs-lookup"><span data-stu-id="c3464-448">Domestic Partnership</span></span> |
| <span data-ttu-id="c3464-449">None</span><span class="sxs-lookup"><span data-stu-id="c3464-449">None</span></span>                   | <span data-ttu-id="c3464-450">None</span><span class="sxs-lookup"><span data-stu-id="c3464-450">None</span></span>                 |
| <span data-ttu-id="c3464-451">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="c3464-451">Cohabiting</span></span>             | <span data-ttu-id="c3464-452">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="c3464-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="c3464-453">Kyn</span><span class="sxs-lookup"><span data-stu-id="c3464-453">Gender</span></span>

<span data-ttu-id="c3464-454">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c3464-455">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c3464-456">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-456">Talent</span></span>       | <span data-ttu-id="c3464-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="c3464-458">Karl</span><span class="sxs-lookup"><span data-stu-id="c3464-458">Male</span></span>         | <span data-ttu-id="c3464-459">Karl</span><span class="sxs-lookup"><span data-stu-id="c3464-459">Male</span></span>            |
| <span data-ttu-id="c3464-460">Kona</span><span class="sxs-lookup"><span data-stu-id="c3464-460">Female</span></span>       | <span data-ttu-id="c3464-461">Kona</span><span class="sxs-lookup"><span data-stu-id="c3464-461">Female</span></span>          |
| <span data-ttu-id="c3464-462">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="c3464-462">Non-specific</span></span> | <span data-ttu-id="c3464-463">*Ekki stutt*</span><span class="sxs-lookup"><span data-stu-id="c3464-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c3464-464">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-464">Earning codes</span></span>

<span data-ttu-id="c3464-465">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="c3464-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c3464-466">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="c3464-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c3464-467">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="c3464-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c3464-468">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="c3464-468">Supported frequencies</span></span>

- <span data-ttu-id="c3464-469">Allir</span><span class="sxs-lookup"><span data-stu-id="c3464-469">All</span></span>
- <span data-ttu-id="c3464-470">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="c3464-470">EVERYPAY</span></span>
- <span data-ttu-id="c3464-471">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="c3464-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c3464-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c3464-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c3464-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c3464-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c3464-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-474">1OFMTH</span></span>
- <span data-ttu-id="c3464-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-475">LASTOFMTH</span></span>
- <span data-ttu-id="c3464-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-476">2OFMTH</span></span>
- <span data-ttu-id="c3464-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-477">3OFMTH</span></span>
- <span data-ttu-id="c3464-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-478">4OFMTH</span></span>
- <span data-ttu-id="c3464-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-479">5OFMTH</span></span>
- <span data-ttu-id="c3464-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-480">1N2OFMTH</span></span>
- <span data-ttu-id="c3464-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-481">3N4OFMTH</span></span>
- <span data-ttu-id="c3464-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-482">1N3OFMTH</span></span>
- <span data-ttu-id="c3464-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-483">1N4OFMTH</span></span>
- <span data-ttu-id="c3464-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-484">2N3OFMTH</span></span>
- <span data-ttu-id="c3464-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-485">2N4OFMTH</span></span>
- <span data-ttu-id="c3464-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="c3464-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="c3464-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="c3464-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="c3464-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c3464-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c3464-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c3464-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c3464-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c3464-493">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c3464-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c3464-494">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c3464-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c3464-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c3464-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c3464-496">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c3464-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c3464-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c3464-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c3464-498">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="c3464-498">Addresses</span></span>

<span data-ttu-id="c3464-499">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="c3464-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c3464-500">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="c3464-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c3464-501">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-501">Talent</span></span>          | <span data-ttu-id="c3464-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="c3464-503">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="c3464-503">Country/Region</span></span>  | <span data-ttu-id="c3464-504">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-504">Country Code</span></span>          |
| <span data-ttu-id="c3464-505">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-505">Zip/Postal Code</span></span> | <span data-ttu-id="c3464-506">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-506">Postal Code</span></span>           |
| <span data-ttu-id="c3464-507">Ríki</span><span class="sxs-lookup"><span data-stu-id="c3464-507">State</span></span>           | <span data-ttu-id="c3464-508">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="c3464-508">State Code</span></span>            |
| <span data-ttu-id="c3464-509">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c3464-509">City</span></span>            | <span data-ttu-id="c3464-510">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c3464-510">City</span></span>                  |
| <span data-ttu-id="c3464-511">Sýsla</span><span class="sxs-lookup"><span data-stu-id="c3464-511">County</span></span>          | <span data-ttu-id="c3464-512">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="c3464-512">County (Municipality)</span></span> |
| <span data-ttu-id="c3464-513">Gata</span><span class="sxs-lookup"><span data-stu-id="c3464-513">Street</span></span>          | <span data-ttu-id="c3464-514">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="c3464-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="c3464-515">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="c3464-515">Tax regions</span></span>

<span data-ttu-id="c3464-516">Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="c3464-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="c3464-517">Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="c3464-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="c3464-518">Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="c3464-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="c3464-519">Skattumdæmi (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-519">Tax region (required)</span></span>
- <span data-ttu-id="c3464-520">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-520">Country/Region (required)</span></span>
- <span data-ttu-id="c3464-521">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-521">State (required)</span></span>
- <span data-ttu-id="c3464-522">Sýsla</span><span class="sxs-lookup"><span data-stu-id="c3464-522">County</span></span> 
- <span data-ttu-id="c3464-523">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="c3464-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="c3464-524">Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="c3464-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="c3464-525">Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="c3464-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="c3464-526">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="c3464-526">Departments are required on positions.</span></span>
- <span data-ttu-id="c3464-527">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="c3464-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="c3464-528">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="c3464-528">Job types</span></span>

<span data-ttu-id="c3464-529">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="c3464-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c3464-530">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="c3464-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="c3464-531">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="c3464-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c3464-532">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="c3464-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c3464-533">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c3464-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c3464-534">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="c3464-534">Job type</span></span>   | <span data-ttu-id="c3464-535">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c3464-536">Tímar</span><span class="sxs-lookup"><span data-stu-id="c3464-536">Hourly</span></span>     | <span data-ttu-id="c3464-537">MX tímakaup</span><span class="sxs-lookup"><span data-stu-id="c3464-537">MX Hourly</span></span>   |
| <span data-ttu-id="c3464-538">Föst laun</span><span class="sxs-lookup"><span data-stu-id="c3464-538">Salaried</span></span>   | <span data-ttu-id="c3464-539">MX föst laun</span><span class="sxs-lookup"><span data-stu-id="c3464-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="c3464-540">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="c3464-540">Position types</span></span> 

<span data-ttu-id="c3464-541">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="c3464-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c3464-542">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="c3464-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c3464-543">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c3464-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c3464-544">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="c3464-544">Position type</span></span>   | <span data-ttu-id="c3464-545">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c3464-546">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="c3464-546">Full-time</span></span>       | <span data-ttu-id="c3464-547">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="c3464-547">Full time employee</span></span> |
| <span data-ttu-id="c3464-548">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="c3464-548">Part-time</span></span>       | <span data-ttu-id="c3464-549">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="c3464-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c3464-550">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-550">Reason codes</span></span>

<span data-ttu-id="c3464-551">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c3464-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c3464-552">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="c3464-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c3464-553">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c3464-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c3464-554">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="c3464-554">Reason code</span></span>            | <span data-ttu-id="c3464-555">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-555">Description</span></span>                    | <span data-ttu-id="c3464-556">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="c3464-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="c3464-557">BROTTFÖR Á UNDAN LAUNAGREIÐSLU</span><span class="sxs-lookup"><span data-stu-id="c3464-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="c3464-558">Brottför á undan launum</span><span class="sxs-lookup"><span data-stu-id="c3464-558">Departure before first payroll</span></span> | <span data-ttu-id="c3464-559">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-559">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-560">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="c3464-560">RESIGNATION</span></span>            | <span data-ttu-id="c3464-561">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="c3464-561">Resignation</span></span>                    | <span data-ttu-id="c3464-562">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-562">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-563">LÍFEYRIR</span><span class="sxs-lookup"><span data-stu-id="c3464-563">PENSION</span></span>                | <span data-ttu-id="c3464-564">Lífeyrir</span><span class="sxs-lookup"><span data-stu-id="c3464-564">Pension</span></span>                        | <span data-ttu-id="c3464-565">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-565">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-566">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="c3464-566">TERMINATION</span></span>            | <span data-ttu-id="c3464-567">Lok</span><span class="sxs-lookup"><span data-stu-id="c3464-567">Termination</span></span>                    | <span data-ttu-id="c3464-568">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-568">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-569">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="c3464-569">RETIREMENT</span></span>             | <span data-ttu-id="c3464-570">Starfslok</span><span class="sxs-lookup"><span data-stu-id="c3464-570">Retirement</span></span>                     | <span data-ttu-id="c3464-571">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-571">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-572">FJARVERA</span><span class="sxs-lookup"><span data-stu-id="c3464-572">ABSENTEE</span></span>               | <span data-ttu-id="c3464-573">Fjarvera</span><span class="sxs-lookup"><span data-stu-id="c3464-573">Absentee</span></span>                       | <span data-ttu-id="c3464-574">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-574">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-575">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="c3464-575">OTHER</span></span>                  | <span data-ttu-id="c3464-576">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="c3464-576">Other Reasons</span></span>                  | <span data-ttu-id="c3464-577">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-577">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-578">LOKUN</span><span class="sxs-lookup"><span data-stu-id="c3464-578">CLOSURE</span></span>                | <span data-ttu-id="c3464-579">Viðskiptalokun</span><span class="sxs-lookup"><span data-stu-id="c3464-579">Business Closure</span></span>               | <span data-ttu-id="c3464-580">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-580">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-581">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="c3464-581">DEATH</span></span>                  | <span data-ttu-id="c3464-582">Dauði</span><span class="sxs-lookup"><span data-stu-id="c3464-582">Death</span></span>                          | <span data-ttu-id="c3464-583">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-583">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-584">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="c3464-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="c3464-585">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="c3464-585">Leave of Absence</span></span>               | <span data-ttu-id="c3464-586">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-586">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-587">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="c3464-587">CONTRACTEND</span></span>            | <span data-ttu-id="c3464-588">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="c3464-588">End of Contract</span></span>                | <span data-ttu-id="c3464-589">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="c3464-589">Terminate worker</span></span>     |
| <span data-ttu-id="c3464-590">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="c3464-590">SALARYCHANGE</span></span>           | <span data-ttu-id="c3464-591">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="c3464-591">Change of Salary</span></span>               | <span data-ttu-id="c3464-592">Laun</span><span class="sxs-lookup"><span data-stu-id="c3464-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="c3464-593">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="c3464-593">Terms of employment</span></span>

<span data-ttu-id="c3464-594">Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar.</span><span class="sxs-lookup"><span data-stu-id="c3464-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="c3464-595">Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.</span><span class="sxs-lookup"><span data-stu-id="c3464-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="c3464-596">Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="c3464-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="c3464-597">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="c3464-597">Terms of employment</span></span>   | <span data-ttu-id="c3464-598">lýsing</span><span class="sxs-lookup"><span data-stu-id="c3464-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c3464-599">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="c3464-599">Regular</span></span>               | <span data-ttu-id="c3464-600">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="c3464-600">Regular</span></span>     |
| <span data-ttu-id="c3464-601">Beint</span><span class="sxs-lookup"><span data-stu-id="c3464-601">Direct</span></span>                | <span data-ttu-id="c3464-602">Beint</span><span class="sxs-lookup"><span data-stu-id="c3464-602">Direct</span></span>      |
| <span data-ttu-id="c3464-603">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="c3464-603">Internship</span></span>            | <span data-ttu-id="c3464-604">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="c3464-604">Internship</span></span>  |
| <span data-ttu-id="c3464-605">Fast</span><span class="sxs-lookup"><span data-stu-id="c3464-605">Permanent</span></span>             | <span data-ttu-id="c3464-606">Fast</span><span class="sxs-lookup"><span data-stu-id="c3464-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="c3464-607">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="c3464-607">Marital status</span></span>

<span data-ttu-id="c3464-608">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c3464-609">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c3464-610">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-610">Talent</span></span>                 | <span data-ttu-id="c3464-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="c3464-612">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c3464-612">Married</span></span>                | <span data-ttu-id="c3464-613">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="c3464-613">Married</span></span>                   |
| <span data-ttu-id="c3464-614">Ein</span><span class="sxs-lookup"><span data-stu-id="c3464-614">Single</span></span>                 | <span data-ttu-id="c3464-615">Ein</span><span class="sxs-lookup"><span data-stu-id="c3464-615">Single</span></span>                    |
| <span data-ttu-id="c3464-616">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c3464-616">Widowed</span></span>                | <span data-ttu-id="c3464-617">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="c3464-617">Widowed</span></span>                   |
| <span data-ttu-id="c3464-618">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c3464-618">Divorced</span></span>               | <span data-ttu-id="c3464-619">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="c3464-619">Divorced</span></span>                  |
| <span data-ttu-id="c3464-620">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="c3464-620">Registered Partnership</span></span> | <span data-ttu-id="c3464-621">Sambúð</span><span class="sxs-lookup"><span data-stu-id="c3464-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="c3464-622">None</span><span class="sxs-lookup"><span data-stu-id="c3464-622">None</span></span>                   | <span data-ttu-id="c3464-623">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c3464-624">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="c3464-624">Cohabiting</span></span>             | <span data-ttu-id="c3464-625">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="c3464-626">Kyn</span><span class="sxs-lookup"><span data-stu-id="c3464-626">Gender</span></span>

<span data-ttu-id="c3464-627">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c3464-628">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c3464-629">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-629">Talent</span></span>       | <span data-ttu-id="c3464-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="c3464-631">Karl</span><span class="sxs-lookup"><span data-stu-id="c3464-631">Male</span></span>         | <span data-ttu-id="c3464-632">Karl</span><span class="sxs-lookup"><span data-stu-id="c3464-632">Male</span></span>                      |
| <span data-ttu-id="c3464-633">Kona</span><span class="sxs-lookup"><span data-stu-id="c3464-633">Female</span></span>       | <span data-ttu-id="c3464-634">Kona</span><span class="sxs-lookup"><span data-stu-id="c3464-634">Female</span></span>                    |
| <span data-ttu-id="c3464-635">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="c3464-635">Non-specific</span></span> | <span data-ttu-id="c3464-636">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="c3464-637">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="c3464-637">Payment method</span></span>

<span data-ttu-id="c3464-638">Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="c3464-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="c3464-639">Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c3464-640">Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="c3464-641">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-641">Talent</span></span>             | <span data-ttu-id="c3464-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="c3464-643">Innlausn</span><span class="sxs-lookup"><span data-stu-id="c3464-643">Cash</span></span>               | <span data-ttu-id="c3464-644">Innlausn</span><span class="sxs-lookup"><span data-stu-id="c3464-644">Cash</span></span>                      |
| <span data-ttu-id="c3464-645">Rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="c3464-645">Electronic Payment</span></span> | <span data-ttu-id="c3464-646">Flutningur</span><span class="sxs-lookup"><span data-stu-id="c3464-646">Transfer</span></span>                  |
| <span data-ttu-id="c3464-647">Merkja</span><span class="sxs-lookup"><span data-stu-id="c3464-647">Check</span></span>              | <span data-ttu-id="c3464-648">Ávísun</span><span class="sxs-lookup"><span data-stu-id="c3464-648">Cheque</span></span>                    |
| <span data-ttu-id="c3464-649">Bankaávísun</span><span class="sxs-lookup"><span data-stu-id="c3464-649">Bank Draft</span></span>         | <span data-ttu-id="c3464-650">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c3464-651">Annað</span><span class="sxs-lookup"><span data-stu-id="c3464-651">Other</span></span>              | <span data-ttu-id="c3464-652">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="c3464-653">Gerð bankareiknings</span><span class="sxs-lookup"><span data-stu-id="c3464-653">Bank account type</span></span>

<span data-ttu-id="c3464-654">Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="c3464-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="c3464-655">Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga.</span><span class="sxs-lookup"><span data-stu-id="c3464-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="c3464-656">Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c3464-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="c3464-657">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-657">Talent</span></span>            | <span data-ttu-id="c3464-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="c3464-659">Ávísanareikningur</span><span class="sxs-lookup"><span data-stu-id="c3464-659">Checking Account</span></span>  | <span data-ttu-id="c3464-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="c3464-660">CheckingAccount</span></span>           |
| <span data-ttu-id="c3464-661">Launareikningur</span><span class="sxs-lookup"><span data-stu-id="c3464-661">Payroll Account</span></span>   | <span data-ttu-id="c3464-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="c3464-662">PayrollAccount</span></span>            |
| <span data-ttu-id="c3464-663">Sparnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="c3464-663">Savings Account</span></span>   | <span data-ttu-id="c3464-664">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c3464-665">BankGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="c3464-665">BankGirot account</span></span> | <span data-ttu-id="c3464-666">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c3464-667">PlusGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="c3464-667">PlusGirot account</span></span> | <span data-ttu-id="c3464-668">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="c3464-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c3464-669">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="c3464-669">Earning codes</span></span>

<span data-ttu-id="c3464-670">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="c3464-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c3464-671">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="c3464-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c3464-672">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="c3464-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c3464-673">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="c3464-673">Supported frequencies</span></span>

- <span data-ttu-id="c3464-674">Allir</span><span class="sxs-lookup"><span data-stu-id="c3464-674">All</span></span>
- <span data-ttu-id="c3464-675">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="c3464-675">EVERYPAY</span></span>
- <span data-ttu-id="c3464-676">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="c3464-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c3464-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c3464-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c3464-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c3464-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c3464-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-679">1OFMTH</span></span>
- <span data-ttu-id="c3464-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-680">LASTOFMTH</span></span>
- <span data-ttu-id="c3464-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-681">2OFMTH</span></span>
- <span data-ttu-id="c3464-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-682">3OFMTH</span></span>
- <span data-ttu-id="c3464-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-683">4OFMTH</span></span>
- <span data-ttu-id="c3464-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-684">5OFMTH</span></span>
- <span data-ttu-id="c3464-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-685">1N2OFMTH</span></span>
- <span data-ttu-id="c3464-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-686">3N4OFMTH</span></span>
- <span data-ttu-id="c3464-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-687">1N3OFMTH</span></span>
- <span data-ttu-id="c3464-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-688">1N4OFMTH</span></span>
- <span data-ttu-id="c3464-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-689">2N3OFMTH</span></span>
- <span data-ttu-id="c3464-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-690">2N4OFMTH</span></span>
- <span data-ttu-id="c3464-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="c3464-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="c3464-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="c3464-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="c3464-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c3464-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c3464-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c3464-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c3464-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c3464-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c3464-698">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c3464-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c3464-699">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c3464-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c3464-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c3464-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c3464-701">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c3464-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c3464-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c3464-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c3464-703">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="c3464-703">Addresses</span></span>

<span data-ttu-id="c3464-704">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="c3464-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c3464-705">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="c3464-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c3464-706">Talent</span><span class="sxs-lookup"><span data-stu-id="c3464-706">Talent</span></span>              | <span data-ttu-id="c3464-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c3464-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="c3464-708">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="c3464-708">Country/Region</span></span>      | <span data-ttu-id="c3464-709">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-709">Country Code</span></span>          |
| <span data-ttu-id="c3464-710">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-710">Zip/Postal Code</span></span>     | <span data-ttu-id="c3464-711">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-711">Postal Code</span></span>           |
| <span data-ttu-id="c3464-712">Ríki</span><span class="sxs-lookup"><span data-stu-id="c3464-712">State</span></span>               | <span data-ttu-id="c3464-713">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="c3464-713">State Code</span></span>            |
| <span data-ttu-id="c3464-714">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c3464-714">City</span></span>                | <span data-ttu-id="c3464-715">Póststöð</span><span class="sxs-lookup"><span data-stu-id="c3464-715">City</span></span>                  |
| <span data-ttu-id="c3464-716">Sýsla</span><span class="sxs-lookup"><span data-stu-id="c3464-716">County</span></span>              | <span data-ttu-id="c3464-717">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="c3464-717">County (Municipality)</span></span> |
| <span data-ttu-id="c3464-718">Gata</span><span class="sxs-lookup"><span data-stu-id="c3464-718">Street</span></span>              | <span data-ttu-id="c3464-719">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="c3464-719">Address Line 1</span></span>        |
| <span data-ttu-id="c3464-720">Húsnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-720">Street Number</span></span>       | <span data-ttu-id="c3464-721">Heimilisfang, lína 2</span><span class="sxs-lookup"><span data-stu-id="c3464-721">Address Line 2</span></span>        |
| <span data-ttu-id="c3464-722">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="c3464-722">Building Complement</span></span> | <span data-ttu-id="c3464-723">Heimilisfang, lína 5</span><span class="sxs-lookup"><span data-stu-id="c3464-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="c3464-724">Vegabréfsnúmer</span><span class="sxs-lookup"><span data-stu-id="c3464-724">Passport number</span></span>

<span data-ttu-id="c3464-725">Starfsmenn geta gefið upp vegabréfsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c3464-725">Employees can declare passport information.</span></span> <span data-ttu-id="c3464-726">Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="c3464-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="c3464-727">Gerð auðkennis = „Vegabréf“</span><span class="sxs-lookup"><span data-stu-id="c3464-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="c3464-728">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="c3464-728">Issued Date</span></span>
- <span data-ttu-id="c3464-729">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="c3464-729">Expiration Date</span></span>

<span data-ttu-id="c3464-730">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**.</span><span class="sxs-lookup"><span data-stu-id="c3464-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="c3464-731">Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="c3464-732">Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c3464-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>


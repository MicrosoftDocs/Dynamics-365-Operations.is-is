---
title: Skilgreina launasamþættingu milli Talent og Dayforce
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla samþættingu milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce svo hægt sé að afgreiða launakeyrslu.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
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
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518232"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="b3397-103">Skilgreina launasamþættingu milli Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3397-104">Samþættingin milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="b3397-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="b3397-105">Nauðsynlegt er að skilgreina samþættinguna bæði í Talent og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="b3397-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="b3397-106">Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Talent.</span><span class="sxs-lookup"><span data-stu-id="b3397-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="b3397-107">Samþættingin krefst tilgreindra gagna frá Talent.</span><span class="sxs-lookup"><span data-stu-id="b3397-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="b3397-108">Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Talent á þann hátt sem styður samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="b3397-109">Samþættingin notar eftirfarandi víðtæka flokka gagna:</span><span class="sxs-lookup"><span data-stu-id="b3397-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="b3397-110">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="b3397-110">Human resources data</span></span>
- <span data-ttu-id="b3397-111">Launagögn</span><span class="sxs-lookup"><span data-stu-id="b3397-111">Compensation data</span></span>
- <span data-ttu-id="b3397-112">Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="b3397-113">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="b3397-113">Worker data</span></span>

<span data-ttu-id="b3397-114">Þetta efnisatriði fjallar um skrefin sem verður að fylgja til að virkja samþættinginu.</span><span class="sxs-lookup"><span data-stu-id="b3397-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="b3397-115">Það útskýrir einnig gerð gagna og upplýsingar um skilgreiningar sem samþættingin krefst.</span><span class="sxs-lookup"><span data-stu-id="b3397-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="b3397-116">Virkja samþættingu</span><span class="sxs-lookup"><span data-stu-id="b3397-116">Enable the integration</span></span>

<span data-ttu-id="b3397-117">Í Talent er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="b3397-118">Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 for Finance and Operations þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b3397-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="b3397-119">Til að kveikja á samþættingu í Talent skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b3397-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="b3397-120">Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="b3397-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="b3397-121">Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.</span><span class="sxs-lookup"><span data-stu-id="b3397-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="b3397-122">Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.</span><span class="sxs-lookup"><span data-stu-id="b3397-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="b3397-123">Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b3397-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="b3397-124">Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt.</span><span class="sxs-lookup"><span data-stu-id="b3397-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="b3397-125">Hægt er að breyta tíðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b3397-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="b3397-126">Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi efnisatriðum Azure:</span><span class="sxs-lookup"><span data-stu-id="b3397-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="b3397-127">Um Azure-geymslureikninga</span><span class="sxs-lookup"><span data-stu-id="b3397-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="b3397-128">Skilgreina tengistrengi Azure-geymslu</span><span class="sxs-lookup"><span data-stu-id="b3397-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="b3397-129">Skilgreina gögnin þín</span><span class="sxs-lookup"><span data-stu-id="b3397-129">Configure your data</span></span> 

<span data-ttu-id="b3397-130">Til að afgreiða laun þarf að skilgreina mannauðsgögn í Talent.</span><span class="sxs-lookup"><span data-stu-id="b3397-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="b3397-131">Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun.</span><span class="sxs-lookup"><span data-stu-id="b3397-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="b3397-132">Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.</span><span class="sxs-lookup"><span data-stu-id="b3397-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="b3397-133">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="b3397-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="b3397-134">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="b3397-134">Benefits</span></span> 

<span data-ttu-id="b3397-135">Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.</span><span class="sxs-lookup"><span data-stu-id="b3397-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="b3397-136">Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="b3397-137">Fríðindaáætlanir</span><span class="sxs-lookup"><span data-stu-id="b3397-137">Benefit plans</span></span>

- <span data-ttu-id="b3397-138">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-138">Plan (required)</span></span>
- <span data-ttu-id="b3397-139">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-139">Type (required)</span></span>
- <span data-ttu-id="b3397-140">Áhrif á launaskrá (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-140">Payroll impact (required)</span></span>
- <span data-ttu-id="b3397-141">Endurheimta vangoldnar greiðslur</span><span class="sxs-lookup"><span data-stu-id="b3397-141">Recover arrears</span></span>
- <span data-ttu-id="b3397-142">Frádráttaraðferð</span><span class="sxs-lookup"><span data-stu-id="b3397-142">Deduction method</span></span>
- <span data-ttu-id="b3397-143">Frádráttarforgangur</span><span class="sxs-lookup"><span data-stu-id="b3397-143">Deduction priority</span></span>
- <span data-ttu-id="b3397-144">Takmörkunartímabil</span><span class="sxs-lookup"><span data-stu-id="b3397-144">Limit period</span></span>
- <span data-ttu-id="b3397-145">Takmarka upphæð</span><span class="sxs-lookup"><span data-stu-id="b3397-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="b3397-146">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="b3397-146">Benefits</span></span>

- <span data-ttu-id="b3397-147">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-147">Plan (required)</span></span>
- <span data-ttu-id="b3397-148">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-148">Type (required)</span></span>
- <span data-ttu-id="b3397-149">Valkostur (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-149">Option (required)</span></span>
- <span data-ttu-id="b3397-150">Fríðindaauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-150">Benefit ID (required)</span></span>
- <span data-ttu-id="b3397-151">Tíðni</span><span class="sxs-lookup"><span data-stu-id="b3397-151">Frequency</span></span>
- <span data-ttu-id="b3397-152">Grunnur</span><span class="sxs-lookup"><span data-stu-id="b3397-152">Basis</span></span>
- <span data-ttu-id="b3397-153">Upphæð eða taxti</span><span class="sxs-lookup"><span data-stu-id="b3397-153">Amount or rate</span></span>
- <span data-ttu-id="b3397-154">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="b3397-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="b3397-155">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="b3397-155">Supported frequencies</span></span> 

- <span data-ttu-id="b3397-156">Vikulega</span><span class="sxs-lookup"><span data-stu-id="b3397-156">Weekly</span></span>
- <span data-ttu-id="b3397-157">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="b3397-157">Bi-weekly</span></span>
- <span data-ttu-id="b3397-158">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="b3397-158">Semi-monthly</span></span>
- <span data-ttu-id="b3397-159">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="b3397-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="b3397-160">Studdir grunnar</span><span class="sxs-lookup"><span data-stu-id="b3397-160">Supported bases</span></span> 

- <span data-ttu-id="b3397-161">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="b3397-161">Fixed amount</span></span>
- <span data-ttu-id="b3397-162">Prósenta af tekjum</span><span class="sxs-lookup"><span data-stu-id="b3397-162">Percent of earnings</span></span>
- <span data-ttu-id="b3397-163">Virkar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="b3397-163">Productive hours</span></span>

<span data-ttu-id="b3397-164">Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.</span><span class="sxs-lookup"><span data-stu-id="b3397-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="b3397-165">Val í Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-165">Selection in Talent</span></span>        | <span data-ttu-id="b3397-166">Niðurstaða í Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b3397-167">None</span><span class="sxs-lookup"><span data-stu-id="b3397-167">None</span></span>                       | <span data-ttu-id="b3397-168">Enginn frádráttur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="b3397-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="b3397-169">Eingöngu frádráttur</span><span class="sxs-lookup"><span data-stu-id="b3397-169">Deduction only</span></span>             | <span data-ttu-id="b3397-170">Frádráttur starfsmanns er búinn til.</span><span class="sxs-lookup"><span data-stu-id="b3397-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="b3397-171">Eingöngu framlag</span><span class="sxs-lookup"><span data-stu-id="b3397-171">Contribution only</span></span>          | <span data-ttu-id="b3397-172">Frádráttur vinnuveitanda er búinn til.</span><span class="sxs-lookup"><span data-stu-id="b3397-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="b3397-173">Frádráttur og framlag</span><span class="sxs-lookup"><span data-stu-id="b3397-173">Deduction and contribution</span></span> | <span data-ttu-id="b3397-174">Frádrættir starfsmanns og vinnuveitanda eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="b3397-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="b3397-175">Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="b3397-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="b3397-176">Leggja fram fríðindaáætlun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="b3397-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="b3397-177">Stofna ný fríðindi</span><span class="sxs-lookup"><span data-stu-id="b3397-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="b3397-178">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="b3397-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="b3397-179">Skrá og fjarlægja fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="b3397-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="b3397-180">Laun</span><span class="sxs-lookup"><span data-stu-id="b3397-180">Compensation</span></span> 

<span data-ttu-id="b3397-181">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="b3397-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b3397-182">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="b3397-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b3397-183">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="b3397-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="b3397-184">Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b3397-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="b3397-185">Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta.</span><span class="sxs-lookup"><span data-stu-id="b3397-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="b3397-186">Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="b3397-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="b3397-187">Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="b3397-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="b3397-188">Launafyrirkomulag fastra launa stofnað</span><span class="sxs-lookup"><span data-stu-id="b3397-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="b3397-189">Launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="b3397-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="b3397-190">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="b3397-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="b3397-191">Launaútreikningur</span><span class="sxs-lookup"><span data-stu-id="b3397-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="b3397-192">Skilgreina launavinnslu og reikna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="b3397-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="b3397-193">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="b3397-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="b3397-194">Skrá starfsmann í launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="b3397-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="b3397-195">Störf</span><span class="sxs-lookup"><span data-stu-id="b3397-195">Jobs</span></span> 

<span data-ttu-id="b3397-196">Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið.</span><span class="sxs-lookup"><span data-stu-id="b3397-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="b3397-197">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="b3397-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b3397-198">Setja upp íhluta verks</span><span class="sxs-lookup"><span data-stu-id="b3397-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="b3397-199">Skilgreina ný störf</span><span class="sxs-lookup"><span data-stu-id="b3397-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="b3397-200">Stöður</span><span class="sxs-lookup"><span data-stu-id="b3397-200">Positions</span></span>

<span data-ttu-id="b3397-201">Staða er sérstakt tilvik starfs.</span><span class="sxs-lookup"><span data-stu-id="b3397-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="b3397-202">Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“.</span><span class="sxs-lookup"><span data-stu-id="b3397-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="b3397-203">Staða er til í deild.</span><span class="sxs-lookup"><span data-stu-id="b3397-203">A position exists in a department.</span></span> <span data-ttu-id="b3397-204">Einungis einn starfsmaður getur tengst hverri stöðu.</span><span class="sxs-lookup"><span data-stu-id="b3397-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="b3397-205">Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:</span><span class="sxs-lookup"><span data-stu-id="b3397-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="b3397-206">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-206">Position (required)</span></span>
- <span data-ttu-id="b3397-207">Lýsing (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-207">Description (required)</span></span>
- <span data-ttu-id="b3397-208">Starf (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-208">Job (required)</span></span>
- <span data-ttu-id="b3397-209">Deild (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-209">Department (required)</span></span>
- <span data-ttu-id="b3397-210">Stöðugerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-210">Position type (required)</span></span>
- <span data-ttu-id="b3397-211">Jafngildi fulls starfs</span><span class="sxs-lookup"><span data-stu-id="b3397-211">Full-time equivalent</span></span>
- <span data-ttu-id="b3397-212">Reglulegar árlegar vinnustundir (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="b3397-213">Greitt eftir lögaðila (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="b3397-214">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-214">Pay cycle (required)</span></span>
- <span data-ttu-id="b3397-215">Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="b3397-216">Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="b3397-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="b3397-217">Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="b3397-218">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="b3397-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b3397-219">Vinnuafl skipulagt með notkun deilda, starfa og staða</span><span class="sxs-lookup"><span data-stu-id="b3397-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="b3397-220">Setja upp stöður</span><span class="sxs-lookup"><span data-stu-id="b3397-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="b3397-221">Deildir</span><span class="sxs-lookup"><span data-stu-id="b3397-221">Departments</span></span>

<span data-ttu-id="b3397-222">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="b3397-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="b3397-223">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="b3397-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="b3397-224">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="b3397-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="b3397-225">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="b3397-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="b3397-226">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="b3397-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b3397-227">Stofnun deildar og tenging hennar við deildastigveldið</span><span class="sxs-lookup"><span data-stu-id="b3397-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="b3397-228">Skilgreina nýjar deildir</span><span class="sxs-lookup"><span data-stu-id="b3397-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="b3397-229">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="b3397-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="b3397-230">Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="b3397-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="b3397-231">Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="b3397-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="b3397-232">Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur.</span><span class="sxs-lookup"><span data-stu-id="b3397-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="b3397-233">Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.</span><span class="sxs-lookup"><span data-stu-id="b3397-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="b3397-234">Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli.</span><span class="sxs-lookup"><span data-stu-id="b3397-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="b3397-235">Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp.</span><span class="sxs-lookup"><span data-stu-id="b3397-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="b3397-236">Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.</span><span class="sxs-lookup"><span data-stu-id="b3397-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="b3397-237">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="b3397-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b3397-238">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-238">Pay cycle (required)</span></span>
- <span data-ttu-id="b3397-239">Tíðni greiðsluferlis (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="b3397-240">Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="b3397-241">Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="b3397-242">Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="b3397-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="b3397-243">Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="b3397-244">Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Talent.</span><span class="sxs-lookup"><span data-stu-id="b3397-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="b3397-245">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-245">Earning codes</span></span>

<span data-ttu-id="b3397-246">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="b3397-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b3397-247">Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="b3397-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="b3397-248">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="b3397-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b3397-249">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-249">Earning Code (required)</span></span>
- <span data-ttu-id="b3397-250">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-250">Description</span></span>
- <span data-ttu-id="b3397-251">Mælieining</span><span class="sxs-lookup"><span data-stu-id="b3397-251">Unit of measure</span></span>
- <span data-ttu-id="b3397-252">Framleiðni</span><span class="sxs-lookup"><span data-stu-id="b3397-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="b3397-253">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="b3397-253">Worker data</span></span>

<span data-ttu-id="b3397-254">Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="b3397-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="b3397-255">Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="b3397-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="b3397-256">Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:</span><span class="sxs-lookup"><span data-stu-id="b3397-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="b3397-257">**Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b3397-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="b3397-258">**Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.</span><span class="sxs-lookup"><span data-stu-id="b3397-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="b3397-259">**Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.</span><span class="sxs-lookup"><span data-stu-id="b3397-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="b3397-260">**Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.</span><span class="sxs-lookup"><span data-stu-id="b3397-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="b3397-261">Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="b3397-262">Almennar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b3397-262">General information</span></span>

- <span data-ttu-id="b3397-263">Númer starfsmanns (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-263">Personnel number (required)</span></span>
- <span data-ttu-id="b3397-264">Fornafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-264">First name (required)</span></span>
- <span data-ttu-id="b3397-265">Eftirnafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-265">Last name (required)</span></span>
- <span data-ttu-id="b3397-266">Millinafn</span><span class="sxs-lookup"><span data-stu-id="b3397-266">Middle name</span></span>
- <span data-ttu-id="b3397-267">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="b3397-267">Seniority date</span></span>
- <span data-ttu-id="b3397-268">Þekkt sem</span><span class="sxs-lookup"><span data-stu-id="b3397-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="b3397-269">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b3397-269">Personal information</span></span>

- <span data-ttu-id="b3397-270">Hjúskaparstaða (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-270">Marital status (required)</span></span>
- <span data-ttu-id="b3397-271">Fæðingardagur (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-271">Birth date (required)</span></span>
- <span data-ttu-id="b3397-272">Kyn (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-272">Gender (required)</span></span>
- <span data-ttu-id="b3397-273">Einstaklingur sem á við fötlun að stríða</span><span class="sxs-lookup"><span data-stu-id="b3397-273">Person with disabilities</span></span>
- <span data-ttu-id="b3397-274">Þjóðerni land svæði (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="b3397-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="b3397-275">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="b3397-275">Address information</span></span>

- <span data-ttu-id="b3397-276">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-276">Primary (required)</span></span>
- <span data-ttu-id="b3397-277">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-277">Country/region (required)</span></span>
- <span data-ttu-id="b3397-278">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-278">Postal code (required)</span></span>
- <span data-ttu-id="b3397-279">Götunúmer (krafist) (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="b3397-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="b3397-280">Viðbygging (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="b3397-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="b3397-281">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-281">City (required)</span></span>
- <span data-ttu-id="b3397-282">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-282">State (required)</span></span>
- <span data-ttu-id="b3397-283">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="b3397-284">Samskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="b3397-284">Contact information</span></span> 

- <span data-ttu-id="b3397-285">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-285">Primary (required)</span></span>
- <span data-ttu-id="b3397-286">Símanúmer tengiliðar (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-286">Contact number (required)</span></span>
- <span data-ttu-id="b3397-287">Skráarending</span><span class="sxs-lookup"><span data-stu-id="b3397-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="b3397-288">Launaupplýsingar og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-288">Payroll information and earning codes</span></span>

<span data-ttu-id="b3397-289">Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b3397-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="b3397-290">Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.</span><span class="sxs-lookup"><span data-stu-id="b3397-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="b3397-291">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-291">Earning codes</span></span>

- <span data-ttu-id="b3397-292">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-292">Position (required)</span></span>
- <span data-ttu-id="b3397-293">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-293">Earning Code (required)</span></span>
- <span data-ttu-id="b3397-294">Tíðni (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-294">Frequency (required)</span></span>
- <span data-ttu-id="b3397-295">Upphæð (áskilin)</span><span class="sxs-lookup"><span data-stu-id="b3397-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="b3397-296">Launaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="b3397-296">Payroll information</span></span>

- <span data-ttu-id="b3397-297">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="b3397-297">Payment Method</span></span>
- <span data-ttu-id="b3397-298">Efnahagssvæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-298">Economic Region (required)</span></span>
- <span data-ttu-id="b3397-299">Kenni fyrir fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="b3397-299">Employee Benefits ID</span></span>
- <span data-ttu-id="b3397-300">Kennitala (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-300">National ID Number (required)</span></span>
- <span data-ttu-id="b3397-301">Hernaðarþjónustunúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-301">Military Service Number</span></span>
- <span data-ttu-id="b3397-302">Auðkenni vaktar (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-302">Shift ID (required)</span></span>
- <span data-ttu-id="b3397-303">Skattanúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-303">Tax Number (required)</span></span>
- <span data-ttu-id="b3397-304">Auðkenni stéttarfélags (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-304">Union ID (required)</span></span>
- <span data-ttu-id="b3397-305">Vinnudagskenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-305">Work Day ID (required)</span></span>
- <span data-ttu-id="b3397-306">Vinnuleyfisnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="b3397-307">Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="b3397-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="b3397-308">Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="b3397-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="b3397-309">Atvinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="b3397-309">Employment details</span></span>

<span data-ttu-id="b3397-310">Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="b3397-311">Dayforce styður aðeins eina starfsferilsskrá í einu.</span><span class="sxs-lookup"><span data-stu-id="b3397-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="b3397-312">Upphafsdagsetning ráðningar (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-312">Employment start date (required)</span></span>
- <span data-ttu-id="b3397-313">Dagsetning starfsloka</span><span class="sxs-lookup"><span data-stu-id="b3397-313">Employment end date</span></span>
- <span data-ttu-id="b3397-314">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="b3397-314">Start date</span></span>
- <span data-ttu-id="b3397-315">Breyttur fyrsti starfsdagur</span><span class="sxs-lookup"><span data-stu-id="b3397-315">Adjusted start date</span></span>
- <span data-ttu-id="b3397-316">Dagsetning starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="b3397-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="b3397-317">Ástæða starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="b3397-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="b3397-318">Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="b3397-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="b3397-319">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-319">Talent</span></span>                | <span data-ttu-id="b3397-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3397-321">Nýlegasti ráðningardagurinn</span><span class="sxs-lookup"><span data-stu-id="b3397-321">Most recent hire date</span></span> | <span data-ttu-id="b3397-322">Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="b3397-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b3397-323">Starfslokadagur</span><span class="sxs-lookup"><span data-stu-id="b3397-323">Termination date</span></span>      | <span data-ttu-id="b3397-324">Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="b3397-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b3397-325">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="b3397-325">Start date</span></span>            | <span data-ttu-id="b3397-326">Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="b3397-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="b3397-327">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="b3397-327">Original hire date</span></span>    | <span data-ttu-id="b3397-328">Upphaf ráðningar fyrir elsta atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="b3397-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="b3397-329">Laun</span><span class="sxs-lookup"><span data-stu-id="b3397-329">Compensation</span></span>

<span data-ttu-id="b3397-330">Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil.</span><span class="sxs-lookup"><span data-stu-id="b3397-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="b3397-331">Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.</span><span class="sxs-lookup"><span data-stu-id="b3397-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="b3397-332">Gildisdagsetning (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-332">Effective Date (required)</span></span>
- <span data-ttu-id="b3397-333">Gildistími</span><span class="sxs-lookup"><span data-stu-id="b3397-333">Expiration date</span></span>
- <span data-ttu-id="b3397-334">Launataxti (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-334">Pay Rate (required)</span></span>
- <span data-ttu-id="b3397-335">Umreikningur launataxta (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="b3397-336">Árlegt jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="b3397-337">Klukkutíma jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="b3397-338">Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b3397-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="b3397-339">Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="b3397-340">Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b3397-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="b3397-341">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="b3397-342">Auðkenni kennitölu</span><span class="sxs-lookup"><span data-stu-id="b3397-342">Social Security identifier</span></span> 

<span data-ttu-id="b3397-343">Sérhver starfsmaður verður að hafa eitt aðalauðkenni.</span><span class="sxs-lookup"><span data-stu-id="b3397-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="b3397-344">Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="b3397-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="b3397-345">Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="b3397-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="b3397-346">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-346">Primary (required)</span></span>
- <span data-ttu-id="b3397-347">Gerð auðkennis = „Kennitala“</span><span class="sxs-lookup"><span data-stu-id="b3397-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="b3397-348">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="b3397-348">Issued Date</span></span>
- <span data-ttu-id="b3397-349">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="b3397-349">Expiration Date</span></span>

<span data-ttu-id="b3397-350">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="b3397-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="b3397-351">Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.</span><span class="sxs-lookup"><span data-stu-id="b3397-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="b3397-352">Bankareikningar og útborganir</span><span class="sxs-lookup"><span data-stu-id="b3397-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="b3397-353">Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="b3397-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="b3397-354">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-354">Talent</span></span>                         | <span data-ttu-id="b3397-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3397-356">Bankareikningsnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="b3397-357">SWIFT-kóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-357">SWIFT code (required)</span></span>          | <span data-ttu-id="b3397-358">Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="b3397-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="b3397-359">Númer útibús (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="b3397-360">Gerð bankareiknings (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-360">Bank account type (required)</span></span>   | <span data-ttu-id="b3397-361">Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="b3397-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="b3397-362">Studd gildi innihalda **Athugun** og **Launaskrá**.</span><span class="sxs-lookup"><span data-stu-id="b3397-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="b3397-363">Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka.</span><span class="sxs-lookup"><span data-stu-id="b3397-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="b3397-364">Allir aðrir reikningar eru hunsaðir.</span><span class="sxs-lookup"><span data-stu-id="b3397-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="b3397-365">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="b3397-365">Address information</span></span>

<span data-ttu-id="b3397-366">Sérhver starfsmaður verður að hafa eina aðalstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b3397-366">Every employee must have one primary location.</span></span> <span data-ttu-id="b3397-367">Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="b3397-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="b3397-368">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-368">Primary (required)</span></span>
- <span data-ttu-id="b3397-369">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-369">Country/region (required)</span></span>
- <span data-ttu-id="b3397-370">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="b3397-371">Gata (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-371">Street (required)</span></span>
- <span data-ttu-id="b3397-372">Götunúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-372">Street Number (required)</span></span>
- <span data-ttu-id="b3397-373">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="b3397-373">Building Complement</span></span>
- <span data-ttu-id="b3397-374">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-374">City (required)</span></span>
- <span data-ttu-id="b3397-375">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-375">State (required)</span></span>
- <span data-ttu-id="b3397-376">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="b3397-377">Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada</span><span class="sxs-lookup"><span data-stu-id="b3397-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="b3397-378">Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="b3397-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="b3397-379">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="b3397-379">Departments are required on positions.</span></span>
- <span data-ttu-id="b3397-380">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="b3397-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="b3397-381">Þú getur stillt Talent til að krefjast þess að stöður tilgreini deild.</span><span class="sxs-lookup"><span data-stu-id="b3397-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="b3397-382">Til að gera þetta skal fara í **Samnýttar stöður mannauðs > Stöður > Krefjast deilda á stöðum**.</span><span class="sxs-lookup"><span data-stu-id="b3397-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="b3397-383">Við mælum með að þessari stillingu sé framfylgt fyrir samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="b3397-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="b3397-384">Starfsgerðir</span><span class="sxs-lookup"><span data-stu-id="b3397-384">Job types</span></span>

<span data-ttu-id="b3397-385">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="b3397-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b3397-386">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="b3397-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="b3397-387">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="b3397-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b3397-388">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="b3397-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b3397-389">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="b3397-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b3397-390">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="b3397-390">Job type</span></span>   | <span data-ttu-id="b3397-391">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b3397-392">Tímar</span><span class="sxs-lookup"><span data-stu-id="b3397-392">Hourly</span></span>     | <span data-ttu-id="b3397-393">Tímar</span><span class="sxs-lookup"><span data-stu-id="b3397-393">Hourly</span></span>      |
| <span data-ttu-id="b3397-394">Föst laun</span><span class="sxs-lookup"><span data-stu-id="b3397-394">Salaried</span></span>   | <span data-ttu-id="b3397-395">Föst laun</span><span class="sxs-lookup"><span data-stu-id="b3397-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="b3397-396">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="b3397-396">Position types</span></span> 

<span data-ttu-id="b3397-397">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="b3397-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b3397-398">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="b3397-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b3397-399">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="b3397-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b3397-400">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="b3397-400">Position type</span></span>   | <span data-ttu-id="b3397-401">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b3397-402">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="b3397-402">Full-time</span></span>       | <span data-ttu-id="b3397-403">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="b3397-403">Full time employee</span></span> |
| <span data-ttu-id="b3397-404">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="b3397-404">Part-time</span></span>       | <span data-ttu-id="b3397-405">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="b3397-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b3397-406">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-406">Reason codes</span></span>

<span data-ttu-id="b3397-407">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b3397-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b3397-408">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="b3397-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b3397-409">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="b3397-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b3397-410">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="b3397-410">Reason code</span></span>    | <span data-ttu-id="b3397-411">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-411">Description</span></span>      | <span data-ttu-id="b3397-412">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="b3397-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="b3397-413">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="b3397-413">RESIGNATION</span></span>    | <span data-ttu-id="b3397-414">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="b3397-414">Resignation</span></span>      | <span data-ttu-id="b3397-415">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-415">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-416">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="b3397-416">TERMINATION</span></span>    | <span data-ttu-id="b3397-417">Lok</span><span class="sxs-lookup"><span data-stu-id="b3397-417">Termination</span></span>      | <span data-ttu-id="b3397-418">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-418">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-419">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="b3397-419">RETIREMENT</span></span>     | <span data-ttu-id="b3397-420">Starfslok</span><span class="sxs-lookup"><span data-stu-id="b3397-420">Retirement</span></span>       | <span data-ttu-id="b3397-421">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-421">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-422">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="b3397-422">OTHER</span></span>          | <span data-ttu-id="b3397-423">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="b3397-423">Other Reasons</span></span>    | <span data-ttu-id="b3397-424">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-424">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-425">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="b3397-425">DEATH</span></span>          | <span data-ttu-id="b3397-426">Dauði</span><span class="sxs-lookup"><span data-stu-id="b3397-426">Death</span></span>            | <span data-ttu-id="b3397-427">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-427">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-428">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="b3397-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="b3397-429">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="b3397-429">Leave of Absence</span></span> | <span data-ttu-id="b3397-430">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-430">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-431">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="b3397-431">CONTRACTEND</span></span>    | <span data-ttu-id="b3397-432">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="b3397-432">End of Contract</span></span>  | <span data-ttu-id="b3397-433">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-433">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-434">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="b3397-434">SALARYCHANGE</span></span>   | <span data-ttu-id="b3397-435">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="b3397-435">Change of Salary</span></span> | <span data-ttu-id="b3397-436">Laun</span><span class="sxs-lookup"><span data-stu-id="b3397-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="b3397-437">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="b3397-437">Marital status</span></span>

<span data-ttu-id="b3397-438">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3397-439">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3397-440">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-440">Talent</span></span>                 | <span data-ttu-id="b3397-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="b3397-442">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="b3397-442">Married</span></span>                | <span data-ttu-id="b3397-443">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="b3397-443">Married</span></span>              |
| <span data-ttu-id="b3397-444">Ein</span><span class="sxs-lookup"><span data-stu-id="b3397-444">Single</span></span>                 | <span data-ttu-id="b3397-445">Ein</span><span class="sxs-lookup"><span data-stu-id="b3397-445">Single</span></span>               |
| <span data-ttu-id="b3397-446">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="b3397-446">Widowed</span></span>                | <span data-ttu-id="b3397-447">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="b3397-447">Widowed</span></span>              |
| <span data-ttu-id="b3397-448">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="b3397-448">Divorced</span></span>               | <span data-ttu-id="b3397-449">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="b3397-449">Divorced</span></span>             |
| <span data-ttu-id="b3397-450">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="b3397-450">Registered Partnership</span></span> | <span data-ttu-id="b3397-451">Sambúð</span><span class="sxs-lookup"><span data-stu-id="b3397-451">Domestic Partnership</span></span> |
| <span data-ttu-id="b3397-452">None</span><span class="sxs-lookup"><span data-stu-id="b3397-452">None</span></span>                   | <span data-ttu-id="b3397-453">None</span><span class="sxs-lookup"><span data-stu-id="b3397-453">None</span></span>                 |
| <span data-ttu-id="b3397-454">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="b3397-454">Cohabiting</span></span>             | <span data-ttu-id="b3397-455">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="b3397-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="b3397-456">Kyn</span><span class="sxs-lookup"><span data-stu-id="b3397-456">Gender</span></span>

<span data-ttu-id="b3397-457">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3397-458">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3397-459">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-459">Talent</span></span>       | <span data-ttu-id="b3397-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="b3397-461">Karl</span><span class="sxs-lookup"><span data-stu-id="b3397-461">Male</span></span>         | <span data-ttu-id="b3397-462">Karl</span><span class="sxs-lookup"><span data-stu-id="b3397-462">Male</span></span>            |
| <span data-ttu-id="b3397-463">Kona</span><span class="sxs-lookup"><span data-stu-id="b3397-463">Female</span></span>       | <span data-ttu-id="b3397-464">Kona</span><span class="sxs-lookup"><span data-stu-id="b3397-464">Female</span></span>          |
| <span data-ttu-id="b3397-465">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="b3397-465">Non-specific</span></span> | <span data-ttu-id="b3397-466">*Ekki stutt*</span><span class="sxs-lookup"><span data-stu-id="b3397-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b3397-467">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-467">Earning codes</span></span>

<span data-ttu-id="b3397-468">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="b3397-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b3397-469">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="b3397-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b3397-470">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="b3397-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b3397-471">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="b3397-471">Supported frequencies</span></span>

- <span data-ttu-id="b3397-472">Allir</span><span class="sxs-lookup"><span data-stu-id="b3397-472">All</span></span>
- <span data-ttu-id="b3397-473">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="b3397-473">EVERYPAY</span></span>
- <span data-ttu-id="b3397-474">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="b3397-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b3397-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b3397-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b3397-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b3397-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b3397-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-477">1OFMTH</span></span>
- <span data-ttu-id="b3397-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-478">LASTOFMTH</span></span>
- <span data-ttu-id="b3397-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-479">2OFMTH</span></span>
- <span data-ttu-id="b3397-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-480">3OFMTH</span></span>
- <span data-ttu-id="b3397-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-481">4OFMTH</span></span>
- <span data-ttu-id="b3397-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-482">5OFMTH</span></span>
- <span data-ttu-id="b3397-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-483">1N2OFMTH</span></span>
- <span data-ttu-id="b3397-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-484">3N4OFMTH</span></span>
- <span data-ttu-id="b3397-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-485">1N3OFMTH</span></span>
- <span data-ttu-id="b3397-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-486">1N4OFMTH</span></span>
- <span data-ttu-id="b3397-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-487">2N3OFMTH</span></span>
- <span data-ttu-id="b3397-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-488">2N4OFMTH</span></span>
- <span data-ttu-id="b3397-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="b3397-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="b3397-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="b3397-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="b3397-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b3397-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b3397-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b3397-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b3397-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b3397-496">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3397-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b3397-497">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3397-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b3397-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3397-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b3397-499">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3397-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b3397-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3397-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b3397-501">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="b3397-501">Addresses</span></span>

<span data-ttu-id="b3397-502">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="b3397-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b3397-503">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="b3397-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b3397-504">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-504">Talent</span></span>          | <span data-ttu-id="b3397-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="b3397-506">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="b3397-506">Country/Region</span></span>  | <span data-ttu-id="b3397-507">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-507">Country Code</span></span>          |
| <span data-ttu-id="b3397-508">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-508">Zip/Postal Code</span></span> | <span data-ttu-id="b3397-509">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-509">Postal Code</span></span>           |
| <span data-ttu-id="b3397-510">Ríki</span><span class="sxs-lookup"><span data-stu-id="b3397-510">State</span></span>           | <span data-ttu-id="b3397-511">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="b3397-511">State Code</span></span>            |
| <span data-ttu-id="b3397-512">Póststöð</span><span class="sxs-lookup"><span data-stu-id="b3397-512">City</span></span>            | <span data-ttu-id="b3397-513">Póststöð</span><span class="sxs-lookup"><span data-stu-id="b3397-513">City</span></span>                  |
| <span data-ttu-id="b3397-514">Sýsla</span><span class="sxs-lookup"><span data-stu-id="b3397-514">County</span></span>          | <span data-ttu-id="b3397-515">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="b3397-515">County (Municipality)</span></span> |
| <span data-ttu-id="b3397-516">Gata</span><span class="sxs-lookup"><span data-stu-id="b3397-516">Street</span></span>          | <span data-ttu-id="b3397-517">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="b3397-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="b3397-518">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="b3397-518">Tax regions</span></span>

<span data-ttu-id="b3397-519">Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="b3397-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="b3397-520">Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="b3397-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="b3397-521">Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="b3397-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="b3397-522">Skattumdæmi (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-522">Tax region (required)</span></span>
- <span data-ttu-id="b3397-523">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-523">Country/Region (required)</span></span>
- <span data-ttu-id="b3397-524">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-524">State (required)</span></span>
- <span data-ttu-id="b3397-525">Sýsla</span><span class="sxs-lookup"><span data-stu-id="b3397-525">County</span></span> 
- <span data-ttu-id="b3397-526">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="b3397-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="b3397-527">Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="b3397-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="b3397-528">Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="b3397-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="b3397-529">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="b3397-529">Departments are required on positions.</span></span>
- <span data-ttu-id="b3397-530">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="b3397-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b3397-531">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="b3397-531">Job types</span></span>

<span data-ttu-id="b3397-532">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="b3397-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b3397-533">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="b3397-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="b3397-534">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="b3397-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b3397-535">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="b3397-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b3397-536">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="b3397-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b3397-537">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="b3397-537">Job type</span></span>   | <span data-ttu-id="b3397-538">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b3397-539">Tímar</span><span class="sxs-lookup"><span data-stu-id="b3397-539">Hourly</span></span>     | <span data-ttu-id="b3397-540">MX tímakaup</span><span class="sxs-lookup"><span data-stu-id="b3397-540">MX Hourly</span></span>   |
| <span data-ttu-id="b3397-541">Föst laun</span><span class="sxs-lookup"><span data-stu-id="b3397-541">Salaried</span></span>   | <span data-ttu-id="b3397-542">MX föst laun</span><span class="sxs-lookup"><span data-stu-id="b3397-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="b3397-543">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="b3397-543">Position types</span></span> 

<span data-ttu-id="b3397-544">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="b3397-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b3397-545">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="b3397-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b3397-546">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="b3397-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b3397-547">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="b3397-547">Position type</span></span>   | <span data-ttu-id="b3397-548">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b3397-549">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="b3397-549">Full-time</span></span>       | <span data-ttu-id="b3397-550">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="b3397-550">Full time employee</span></span> |
| <span data-ttu-id="b3397-551">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="b3397-551">Part-time</span></span>       | <span data-ttu-id="b3397-552">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="b3397-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b3397-553">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-553">Reason codes</span></span>

<span data-ttu-id="b3397-554">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b3397-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b3397-555">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="b3397-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b3397-556">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="b3397-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b3397-557">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="b3397-557">Reason code</span></span>            | <span data-ttu-id="b3397-558">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-558">Description</span></span>                    | <span data-ttu-id="b3397-559">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="b3397-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="b3397-560">BROTTFÖR Á UNDAN LAUNAGREIÐSLU</span><span class="sxs-lookup"><span data-stu-id="b3397-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="b3397-561">Brottför á undan launum</span><span class="sxs-lookup"><span data-stu-id="b3397-561">Departure before first payroll</span></span> | <span data-ttu-id="b3397-562">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-562">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-563">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="b3397-563">RESIGNATION</span></span>            | <span data-ttu-id="b3397-564">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="b3397-564">Resignation</span></span>                    | <span data-ttu-id="b3397-565">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-565">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-566">LÍFEYRIR</span><span class="sxs-lookup"><span data-stu-id="b3397-566">PENSION</span></span>                | <span data-ttu-id="b3397-567">Lífeyrir</span><span class="sxs-lookup"><span data-stu-id="b3397-567">Pension</span></span>                        | <span data-ttu-id="b3397-568">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-568">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-569">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="b3397-569">TERMINATION</span></span>            | <span data-ttu-id="b3397-570">Lok</span><span class="sxs-lookup"><span data-stu-id="b3397-570">Termination</span></span>                    | <span data-ttu-id="b3397-571">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-571">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-572">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="b3397-572">RETIREMENT</span></span>             | <span data-ttu-id="b3397-573">Starfslok</span><span class="sxs-lookup"><span data-stu-id="b3397-573">Retirement</span></span>                     | <span data-ttu-id="b3397-574">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-574">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-575">FJARVERA</span><span class="sxs-lookup"><span data-stu-id="b3397-575">ABSENTEE</span></span>               | <span data-ttu-id="b3397-576">Fjarvera</span><span class="sxs-lookup"><span data-stu-id="b3397-576">Absentee</span></span>                       | <span data-ttu-id="b3397-577">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-577">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-578">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="b3397-578">OTHER</span></span>                  | <span data-ttu-id="b3397-579">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="b3397-579">Other Reasons</span></span>                  | <span data-ttu-id="b3397-580">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-580">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-581">LOKUN</span><span class="sxs-lookup"><span data-stu-id="b3397-581">CLOSURE</span></span>                | <span data-ttu-id="b3397-582">Viðskiptalokun</span><span class="sxs-lookup"><span data-stu-id="b3397-582">Business Closure</span></span>               | <span data-ttu-id="b3397-583">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-583">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-584">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="b3397-584">DEATH</span></span>                  | <span data-ttu-id="b3397-585">Dauði</span><span class="sxs-lookup"><span data-stu-id="b3397-585">Death</span></span>                          | <span data-ttu-id="b3397-586">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-586">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-587">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="b3397-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="b3397-588">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="b3397-588">Leave of Absence</span></span>               | <span data-ttu-id="b3397-589">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-589">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-590">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="b3397-590">CONTRACTEND</span></span>            | <span data-ttu-id="b3397-591">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="b3397-591">End of Contract</span></span>                | <span data-ttu-id="b3397-592">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="b3397-592">Terminate worker</span></span>     |
| <span data-ttu-id="b3397-593">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="b3397-593">SALARYCHANGE</span></span>           | <span data-ttu-id="b3397-594">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="b3397-594">Change of Salary</span></span>               | <span data-ttu-id="b3397-595">Laun</span><span class="sxs-lookup"><span data-stu-id="b3397-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="b3397-596">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="b3397-596">Terms of employment</span></span>

<span data-ttu-id="b3397-597">Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar.</span><span class="sxs-lookup"><span data-stu-id="b3397-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="b3397-598">Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.</span><span class="sxs-lookup"><span data-stu-id="b3397-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="b3397-599">Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="b3397-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="b3397-600">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="b3397-600">Terms of employment</span></span>   | <span data-ttu-id="b3397-601">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3397-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b3397-602">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="b3397-602">Regular</span></span>               | <span data-ttu-id="b3397-603">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="b3397-603">Regular</span></span>     |
| <span data-ttu-id="b3397-604">Beint</span><span class="sxs-lookup"><span data-stu-id="b3397-604">Direct</span></span>                | <span data-ttu-id="b3397-605">Beint</span><span class="sxs-lookup"><span data-stu-id="b3397-605">Direct</span></span>      |
| <span data-ttu-id="b3397-606">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="b3397-606">Internship</span></span>            | <span data-ttu-id="b3397-607">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="b3397-607">Internship</span></span>  |
| <span data-ttu-id="b3397-608">Fast</span><span class="sxs-lookup"><span data-stu-id="b3397-608">Permanent</span></span>             | <span data-ttu-id="b3397-609">Fast</span><span class="sxs-lookup"><span data-stu-id="b3397-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="b3397-610">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="b3397-610">Marital status</span></span>

<span data-ttu-id="b3397-611">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3397-612">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3397-613">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-613">Talent</span></span>                 | <span data-ttu-id="b3397-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="b3397-615">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="b3397-615">Married</span></span>                | <span data-ttu-id="b3397-616">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="b3397-616">Married</span></span>                   |
| <span data-ttu-id="b3397-617">Ein</span><span class="sxs-lookup"><span data-stu-id="b3397-617">Single</span></span>                 | <span data-ttu-id="b3397-618">Ein</span><span class="sxs-lookup"><span data-stu-id="b3397-618">Single</span></span>                    |
| <span data-ttu-id="b3397-619">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="b3397-619">Widowed</span></span>                | <span data-ttu-id="b3397-620">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="b3397-620">Widowed</span></span>                   |
| <span data-ttu-id="b3397-621">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="b3397-621">Divorced</span></span>               | <span data-ttu-id="b3397-622">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="b3397-622">Divorced</span></span>                  |
| <span data-ttu-id="b3397-623">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="b3397-623">Registered Partnership</span></span> | <span data-ttu-id="b3397-624">Sambúð</span><span class="sxs-lookup"><span data-stu-id="b3397-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="b3397-625">None</span><span class="sxs-lookup"><span data-stu-id="b3397-625">None</span></span>                   | <span data-ttu-id="b3397-626">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3397-627">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="b3397-627">Cohabiting</span></span>             | <span data-ttu-id="b3397-628">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="b3397-629">Kyn</span><span class="sxs-lookup"><span data-stu-id="b3397-629">Gender</span></span>

<span data-ttu-id="b3397-630">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3397-631">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3397-632">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-632">Talent</span></span>       | <span data-ttu-id="b3397-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="b3397-634">Karl</span><span class="sxs-lookup"><span data-stu-id="b3397-634">Male</span></span>         | <span data-ttu-id="b3397-635">Karl</span><span class="sxs-lookup"><span data-stu-id="b3397-635">Male</span></span>                      |
| <span data-ttu-id="b3397-636">Kona</span><span class="sxs-lookup"><span data-stu-id="b3397-636">Female</span></span>       | <span data-ttu-id="b3397-637">Kona</span><span class="sxs-lookup"><span data-stu-id="b3397-637">Female</span></span>                    |
| <span data-ttu-id="b3397-638">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="b3397-638">Non-specific</span></span> | <span data-ttu-id="b3397-639">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="b3397-640">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="b3397-640">Payment method</span></span>

<span data-ttu-id="b3397-641">Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="b3397-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="b3397-642">Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3397-643">Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3397-644">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-644">Talent</span></span>             | <span data-ttu-id="b3397-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="b3397-646">Innlausn</span><span class="sxs-lookup"><span data-stu-id="b3397-646">Cash</span></span>               | <span data-ttu-id="b3397-647">Innlausn</span><span class="sxs-lookup"><span data-stu-id="b3397-647">Cash</span></span>                      |
| <span data-ttu-id="b3397-648">Rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="b3397-648">Electronic Payment</span></span> | <span data-ttu-id="b3397-649">Flutningur</span><span class="sxs-lookup"><span data-stu-id="b3397-649">Transfer</span></span>                  |
| <span data-ttu-id="b3397-650">Merkja</span><span class="sxs-lookup"><span data-stu-id="b3397-650">Check</span></span>              | <span data-ttu-id="b3397-651">Ávísun</span><span class="sxs-lookup"><span data-stu-id="b3397-651">Cheque</span></span>                    |
| <span data-ttu-id="b3397-652">Bankaávísun</span><span class="sxs-lookup"><span data-stu-id="b3397-652">Bank Draft</span></span>         | <span data-ttu-id="b3397-653">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3397-654">Annað</span><span class="sxs-lookup"><span data-stu-id="b3397-654">Other</span></span>              | <span data-ttu-id="b3397-655">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="b3397-656">Gerð bankareiknings</span><span class="sxs-lookup"><span data-stu-id="b3397-656">Bank account type</span></span>

<span data-ttu-id="b3397-657">Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="b3397-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="b3397-658">Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga.</span><span class="sxs-lookup"><span data-stu-id="b3397-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="b3397-659">Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b3397-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="b3397-660">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-660">Talent</span></span>            | <span data-ttu-id="b3397-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="b3397-662">Ávísanareikningur</span><span class="sxs-lookup"><span data-stu-id="b3397-662">Checking Account</span></span>  | <span data-ttu-id="b3397-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="b3397-663">CheckingAccount</span></span>           |
| <span data-ttu-id="b3397-664">Launareikningur</span><span class="sxs-lookup"><span data-stu-id="b3397-664">Payroll Account</span></span>   | <span data-ttu-id="b3397-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="b3397-665">PayrollAccount</span></span>            |
| <span data-ttu-id="b3397-666">Sparnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="b3397-666">Savings Account</span></span>   | <span data-ttu-id="b3397-667">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3397-668">BankGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="b3397-668">BankGirot account</span></span> | <span data-ttu-id="b3397-669">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3397-670">PlusGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="b3397-670">PlusGirot account</span></span> | <span data-ttu-id="b3397-671">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="b3397-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b3397-672">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="b3397-672">Earning codes</span></span>

<span data-ttu-id="b3397-673">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="b3397-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b3397-674">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="b3397-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b3397-675">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="b3397-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b3397-676">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="b3397-676">Supported frequencies</span></span>

- <span data-ttu-id="b3397-677">Allir</span><span class="sxs-lookup"><span data-stu-id="b3397-677">All</span></span>
- <span data-ttu-id="b3397-678">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="b3397-678">EVERYPAY</span></span>
- <span data-ttu-id="b3397-679">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="b3397-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b3397-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b3397-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b3397-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b3397-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b3397-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-682">1OFMTH</span></span>
- <span data-ttu-id="b3397-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-683">LASTOFMTH</span></span>
- <span data-ttu-id="b3397-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-684">2OFMTH</span></span>
- <span data-ttu-id="b3397-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-685">3OFMTH</span></span>
- <span data-ttu-id="b3397-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-686">4OFMTH</span></span>
- <span data-ttu-id="b3397-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-687">5OFMTH</span></span>
- <span data-ttu-id="b3397-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-688">1N2OFMTH</span></span>
- <span data-ttu-id="b3397-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-689">3N4OFMTH</span></span>
- <span data-ttu-id="b3397-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-690">1N3OFMTH</span></span>
- <span data-ttu-id="b3397-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-691">1N4OFMTH</span></span>
- <span data-ttu-id="b3397-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-692">2N3OFMTH</span></span>
- <span data-ttu-id="b3397-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-693">2N4OFMTH</span></span>
- <span data-ttu-id="b3397-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="b3397-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="b3397-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="b3397-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="b3397-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3397-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b3397-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b3397-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b3397-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b3397-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b3397-701">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3397-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b3397-702">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3397-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b3397-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3397-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b3397-704">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3397-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b3397-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3397-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b3397-706">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="b3397-706">Addresses</span></span>

<span data-ttu-id="b3397-707">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="b3397-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b3397-708">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="b3397-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b3397-709">Talent</span><span class="sxs-lookup"><span data-stu-id="b3397-709">Talent</span></span>              | <span data-ttu-id="b3397-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3397-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="b3397-711">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="b3397-711">Country/Region</span></span>      | <span data-ttu-id="b3397-712">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-712">Country Code</span></span>          |
| <span data-ttu-id="b3397-713">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-713">Zip/Postal Code</span></span>     | <span data-ttu-id="b3397-714">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-714">Postal Code</span></span>           |
| <span data-ttu-id="b3397-715">Ríki</span><span class="sxs-lookup"><span data-stu-id="b3397-715">State</span></span>               | <span data-ttu-id="b3397-716">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="b3397-716">State Code</span></span>            |
| <span data-ttu-id="b3397-717">Póststöð</span><span class="sxs-lookup"><span data-stu-id="b3397-717">City</span></span>                | <span data-ttu-id="b3397-718">Póststöð</span><span class="sxs-lookup"><span data-stu-id="b3397-718">City</span></span>                  |
| <span data-ttu-id="b3397-719">Sýsla</span><span class="sxs-lookup"><span data-stu-id="b3397-719">County</span></span>              | <span data-ttu-id="b3397-720">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="b3397-720">County (Municipality)</span></span> |
| <span data-ttu-id="b3397-721">Gata</span><span class="sxs-lookup"><span data-stu-id="b3397-721">Street</span></span>              | <span data-ttu-id="b3397-722">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="b3397-722">Address Line 1</span></span>        |
| <span data-ttu-id="b3397-723">Húsnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-723">Street Number</span></span>       | <span data-ttu-id="b3397-724">Heimilisfang, lína 2</span><span class="sxs-lookup"><span data-stu-id="b3397-724">Address Line 2</span></span>        |
| <span data-ttu-id="b3397-725">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="b3397-725">Building Complement</span></span> | <span data-ttu-id="b3397-726">Heimilisfang, lína 5</span><span class="sxs-lookup"><span data-stu-id="b3397-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="b3397-727">Vegabréfsnúmer</span><span class="sxs-lookup"><span data-stu-id="b3397-727">Passport number</span></span>

<span data-ttu-id="b3397-728">Starfsmenn geta gefið upp vegabréfsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b3397-728">Employees can declare passport information.</span></span> <span data-ttu-id="b3397-729">Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b3397-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="b3397-730">Gerð auðkennis = „Vegabréf“</span><span class="sxs-lookup"><span data-stu-id="b3397-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="b3397-731">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="b3397-731">Issued Date</span></span>
- <span data-ttu-id="b3397-732">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="b3397-732">Expiration Date</span></span>

<span data-ttu-id="b3397-733">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**.</span><span class="sxs-lookup"><span data-stu-id="b3397-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="b3397-734">Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="b3397-735">Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b3397-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

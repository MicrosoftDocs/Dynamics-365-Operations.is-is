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
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/26/2019
ms.locfileid: "898445"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="7c2d9-103">Skilgreina launasamþættingu milli Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c2d9-104">Samþættingin milli Microsoft Dynamics 365 for Talent og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="7c2d9-105">Nauðsynlegt er að skilgreina samþættinguna bæði í Talent og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="7c2d9-106">Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Talent.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="7c2d9-107">Samþættingin krefst tilgreindra gagna frá Talent.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="7c2d9-108">Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Talent á þann hátt sem styður samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="7c2d9-109">Samþættingin notar eftirfarandi víðtæka flokka gagna:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="7c2d9-110">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-110">Human resources data</span></span>
- <span data-ttu-id="7c2d9-111">Launagögn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-111">Compensation data</span></span>
- <span data-ttu-id="7c2d9-112">Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="7c2d9-113">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-113">Worker data</span></span>

<span data-ttu-id="7c2d9-114">Þetta efnisatriði fjallar um skrefin sem verður að fylgja til að virkja samþættinginu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="7c2d9-115">Það útskýrir einnig gerð gagna og upplýsingar um skilgreiningar sem samþættingin krefst.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="7c2d9-116">Virkja samþættingu</span><span class="sxs-lookup"><span data-stu-id="7c2d9-116">Enable the integration</span></span>

<span data-ttu-id="7c2d9-117">Í Talent er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="7c2d9-118">Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 for Finance and Operations þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="7c2d9-119">Til að kveikja á samþættingu í Talent skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="7c2d9-120">Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="7c2d9-121">Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="7c2d9-122">Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="7c2d9-123">Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="7c2d9-124">Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="7c2d9-125">Hægt er að breyta tíðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="7c2d9-126">Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi efnisatriðum Azure:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="7c2d9-127">Um Azure-geymslureikninga</span><span class="sxs-lookup"><span data-stu-id="7c2d9-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="7c2d9-128">Skilgreina tengistrengi Azure-geymslu</span><span class="sxs-lookup"><span data-stu-id="7c2d9-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="7c2d9-129">Skilgreina gögnin þín</span><span class="sxs-lookup"><span data-stu-id="7c2d9-129">Configure your data</span></span> 

<span data-ttu-id="7c2d9-130">Til að afgreiða laun þarf að skilgreina mannauðsgögn í Talent.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="7c2d9-131">Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="7c2d9-132">Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="7c2d9-133">Mannauðsgögn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="7c2d9-134">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-134">Benefits</span></span> 

<span data-ttu-id="7c2d9-135">Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="7c2d9-136">Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="7c2d9-137">Fríðindaáætlanir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-137">Benefit plans</span></span>

- <span data-ttu-id="7c2d9-138">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-138">Plan (required)</span></span>
- <span data-ttu-id="7c2d9-139">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-139">Type (required)</span></span>
- <span data-ttu-id="7c2d9-140">Áhrif á launaskrá (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-140">Payroll impact (required)</span></span>
- <span data-ttu-id="7c2d9-141">Endurheimta vangoldnar greiðslur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-141">Recover arrears</span></span>
- <span data-ttu-id="7c2d9-142">Frádráttaraðferð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-142">Deduction method</span></span>
- <span data-ttu-id="7c2d9-143">Frádráttarforgangur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-143">Deduction priority</span></span>
- <span data-ttu-id="7c2d9-144">Takmörkunartímabil</span><span class="sxs-lookup"><span data-stu-id="7c2d9-144">Limit period</span></span>
- <span data-ttu-id="7c2d9-145">Takmarka upphæð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="7c2d9-146">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-146">Benefits</span></span>

- <span data-ttu-id="7c2d9-147">Áætlun (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-147">Plan (required)</span></span>
- <span data-ttu-id="7c2d9-148">Gerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-148">Type (required)</span></span>
- <span data-ttu-id="7c2d9-149">Valkostur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-149">Option (required)</span></span>
- <span data-ttu-id="7c2d9-150">Fríðindaauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-150">Benefit ID (required)</span></span>
- <span data-ttu-id="7c2d9-151">Tíðni</span><span class="sxs-lookup"><span data-stu-id="7c2d9-151">Frequency</span></span>
- <span data-ttu-id="7c2d9-152">Grunnur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-152">Basis</span></span>
- <span data-ttu-id="7c2d9-153">Upphæð eða taxti</span><span class="sxs-lookup"><span data-stu-id="7c2d9-153">Amount or rate</span></span>
- <span data-ttu-id="7c2d9-154">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="7c2d9-155">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-155">Supported frequencies</span></span> 

- <span data-ttu-id="7c2d9-156">Vikulega</span><span class="sxs-lookup"><span data-stu-id="7c2d9-156">Weekly</span></span>
- <span data-ttu-id="7c2d9-157">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="7c2d9-157">Bi-weekly</span></span>
- <span data-ttu-id="7c2d9-158">Hálfsmánaðarlega</span><span class="sxs-lookup"><span data-stu-id="7c2d9-158">Semi-monthly</span></span>
- <span data-ttu-id="7c2d9-159">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="7c2d9-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="7c2d9-160">Studdir grunnar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-160">Supported bases</span></span> 

- <span data-ttu-id="7c2d9-161">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-161">Fixed amount</span></span>
- <span data-ttu-id="7c2d9-162">Prósenta af tekjum</span><span class="sxs-lookup"><span data-stu-id="7c2d9-162">Percent of earnings</span></span>
- <span data-ttu-id="7c2d9-163">Virkar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-163">Productive hours</span></span>

<span data-ttu-id="7c2d9-164">Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="7c2d9-165">Val í Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-165">Selection in Talent</span></span>        | <span data-ttu-id="7c2d9-166">Niðurstaða í Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7c2d9-167">None</span><span class="sxs-lookup"><span data-stu-id="7c2d9-167">None</span></span>                       | <span data-ttu-id="7c2d9-168">Enginn frádráttur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="7c2d9-169">Eingöngu frádráttur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-169">Deduction only</span></span>             | <span data-ttu-id="7c2d9-170">Frádráttur starfsmanns er búinn til.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="7c2d9-171">Eingöngu framlag</span><span class="sxs-lookup"><span data-stu-id="7c2d9-171">Contribution only</span></span>          | <span data-ttu-id="7c2d9-172">Frádráttur vinnuveitanda er búinn til.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="7c2d9-173">Frádráttur og framlag</span><span class="sxs-lookup"><span data-stu-id="7c2d9-173">Deduction and contribution</span></span> | <span data-ttu-id="7c2d9-174">Frádrættir starfsmanns og vinnuveitanda eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="7c2d9-175">Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="7c2d9-176">Leggja fram fríðindaáætlun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="7c2d9-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="7c2d9-177">Stofna ný fríðindi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="7c2d9-178">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="7c2d9-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="7c2d9-179">Skrá og fjarlægja fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="7c2d9-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="7c2d9-180">Laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-180">Compensation</span></span> 

<span data-ttu-id="7c2d9-181">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="7c2d9-182">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="7c2d9-183">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="7c2d9-184">Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="7c2d9-185">Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="7c2d9-186">Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="7c2d9-187">Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="7c2d9-188">Launafyrirkomulag fastra launa stofnað</span><span class="sxs-lookup"><span data-stu-id="7c2d9-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="7c2d9-189">Launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="7c2d9-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="7c2d9-190">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="7c2d9-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="7c2d9-191">Launaútreikningur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="7c2d9-192">Skilgreina launavinnslu og reikna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="7c2d9-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="7c2d9-193">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="7c2d9-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="7c2d9-194">Skrá starfsmann í launafyrirkomulag breytilegra launa</span><span class="sxs-lookup"><span data-stu-id="7c2d9-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="7c2d9-195">Störf</span><span class="sxs-lookup"><span data-stu-id="7c2d9-195">Jobs</span></span> 

<span data-ttu-id="7c2d9-196">Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="7c2d9-197">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7c2d9-198">Setja upp íhluta verks</span><span class="sxs-lookup"><span data-stu-id="7c2d9-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="7c2d9-199">Skilgreina ný störf</span><span class="sxs-lookup"><span data-stu-id="7c2d9-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="7c2d9-200">Stöður</span><span class="sxs-lookup"><span data-stu-id="7c2d9-200">Positions</span></span>

<span data-ttu-id="7c2d9-201">Staða er sérstakt tilvik starfs.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="7c2d9-202">Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="7c2d9-203">Staða er til í deild.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-203">A position exists in a department.</span></span> <span data-ttu-id="7c2d9-204">Einungis einn starfsmaður getur tengst hverri stöðu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="7c2d9-205">Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="7c2d9-206">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-206">Position (required)</span></span>
- <span data-ttu-id="7c2d9-207">Lýsing (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-207">Description (required)</span></span>
- <span data-ttu-id="7c2d9-208">Starf (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-208">Job (required)</span></span>
- <span data-ttu-id="7c2d9-209">Deild (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-209">Department (required)</span></span>
- <span data-ttu-id="7c2d9-210">Stöðugerð (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-210">Position type (required)</span></span>
- <span data-ttu-id="7c2d9-211">Jafngildi fulls starfs</span><span class="sxs-lookup"><span data-stu-id="7c2d9-211">Full-time equivalent</span></span>
- <span data-ttu-id="7c2d9-212">Reglulegar árlegar vinnustundir (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="7c2d9-213">Greitt eftir lögaðila (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="7c2d9-214">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-214">Pay cycle (required)</span></span>
- <span data-ttu-id="7c2d9-215">Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="7c2d9-216">Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="7c2d9-217">Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="7c2d9-218">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7c2d9-219">Vinnuafl skipulagt með notkun deilda, starfa og staða</span><span class="sxs-lookup"><span data-stu-id="7c2d9-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="7c2d9-220">Setja upp stöður</span><span class="sxs-lookup"><span data-stu-id="7c2d9-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="7c2d9-221">Deildir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-221">Departments</span></span>

<span data-ttu-id="7c2d9-222">Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="7c2d9-223">Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="7c2d9-224">Hægt er að nota deildir til að gefa skýrslur um virk svið.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="7c2d9-225">Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="7c2d9-226">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7c2d9-227">Stofnun deildar og tenging hennar við deildastigveldið</span><span class="sxs-lookup"><span data-stu-id="7c2d9-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="7c2d9-228">Skilgreina nýjar deildir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="7c2d9-229">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="7c2d9-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="7c2d9-230">Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="7c2d9-231">Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="7c2d9-232">Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="7c2d9-233">Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="7c2d9-234">Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="7c2d9-235">Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="7c2d9-236">Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="7c2d9-237">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="7c2d9-238">Greiðsluferli (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-238">Pay cycle (required)</span></span>
- <span data-ttu-id="7c2d9-239">Tíðni greiðsluferlis (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="7c2d9-240">Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="7c2d9-241">Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="7c2d9-242">Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="7c2d9-243">Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="7c2d9-244">Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Talent.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="7c2d9-245">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-245">Earning codes</span></span>

<span data-ttu-id="7c2d9-246">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7c2d9-247">Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="7c2d9-248">Eftirfarandi upplýsingar eru notaðar í Dayforce:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="7c2d9-249">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-249">Earning Code (required)</span></span>
- <span data-ttu-id="7c2d9-250">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-250">Description</span></span>
- <span data-ttu-id="7c2d9-251">Mælieining</span><span class="sxs-lookup"><span data-stu-id="7c2d9-251">Unit of measure</span></span>
- <span data-ttu-id="7c2d9-252">Framleiðni</span><span class="sxs-lookup"><span data-stu-id="7c2d9-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="7c2d9-253">Starfsmannagögn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-253">Worker data</span></span>

<span data-ttu-id="7c2d9-254">Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="7c2d9-255">Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="7c2d9-256">Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="7c2d9-257">**Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="7c2d9-258">**Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="7c2d9-259">**Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="7c2d9-260">**Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="7c2d9-261">Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="7c2d9-262">Almennar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-262">General information</span></span>

- <span data-ttu-id="7c2d9-263">Númer starfsmanns (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-263">Personnel number (required)</span></span>
- <span data-ttu-id="7c2d9-264">Fornafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-264">First name (required)</span></span>
- <span data-ttu-id="7c2d9-265">Eftirnafn (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-265">Last name (required)</span></span>
- <span data-ttu-id="7c2d9-266">Millinafn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-266">Middle name</span></span>
- <span data-ttu-id="7c2d9-267">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="7c2d9-267">Seniority date</span></span>
- <span data-ttu-id="7c2d9-268">Þekkt sem</span><span class="sxs-lookup"><span data-stu-id="7c2d9-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="7c2d9-269">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-269">Personal information</span></span>

- <span data-ttu-id="7c2d9-270">Hjúskaparstaða (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-270">Marital status (required)</span></span>
- <span data-ttu-id="7c2d9-271">Fæðingardagur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-271">Birth date (required)</span></span>
- <span data-ttu-id="7c2d9-272">Kyn (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-272">Gender (required)</span></span>
- <span data-ttu-id="7c2d9-273">Einstaklingur sem á við fötlun að stríða</span><span class="sxs-lookup"><span data-stu-id="7c2d9-273">Person with disabilities</span></span>
- <span data-ttu-id="7c2d9-274">Þjóðerni land svæði (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="7c2d9-275">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-275">Address information</span></span>

- <span data-ttu-id="7c2d9-276">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-276">Primary (required)</span></span>
- <span data-ttu-id="7c2d9-277">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-277">Country/region (required)</span></span>
- <span data-ttu-id="7c2d9-278">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-278">Postal code (required)</span></span>
- <span data-ttu-id="7c2d9-279">Götunúmer (krafist) (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="7c2d9-280">Viðbygging (aðeins fyrir Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="7c2d9-281">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-281">City (required)</span></span>
- <span data-ttu-id="7c2d9-282">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-282">State (required)</span></span>
- <span data-ttu-id="7c2d9-283">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="7c2d9-284">Samskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-284">Contact information</span></span> 

- <span data-ttu-id="7c2d9-285">Aðalaðsetur (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-285">Primary (required)</span></span>
- <span data-ttu-id="7c2d9-286">Símanúmer tengiliðar (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-286">Contact number (required)</span></span>
- <span data-ttu-id="7c2d9-287">Skráarending</span><span class="sxs-lookup"><span data-stu-id="7c2d9-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="7c2d9-288">Launaupplýsingar og tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-288">Payroll information and earning codes</span></span>

<span data-ttu-id="7c2d9-289">Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="7c2d9-290">Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="7c2d9-291">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-291">Earning codes</span></span>

- <span data-ttu-id="7c2d9-292">Staða (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-292">Position (required)</span></span>
- <span data-ttu-id="7c2d9-293">Tekjukóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-293">Earning Code (required)</span></span>
- <span data-ttu-id="7c2d9-294">Tíðni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-294">Frequency (required)</span></span>
- <span data-ttu-id="7c2d9-295">Upphæð (áskilin)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="7c2d9-296">Launaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-296">Payroll information</span></span>

- <span data-ttu-id="7c2d9-297">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-297">Payment Method</span></span>
- <span data-ttu-id="7c2d9-298">Efnahagssvæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-298">Economic Region (required)</span></span>
- <span data-ttu-id="7c2d9-299">Kenni fyrir fríðindi starfsmanna</span><span class="sxs-lookup"><span data-stu-id="7c2d9-299">Employee Benefits ID</span></span>
- <span data-ttu-id="7c2d9-300">Kennitala (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-300">National ID Number (required)</span></span>
- <span data-ttu-id="7c2d9-301">Hernaðarþjónustunúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-301">Military Service Number</span></span>
- <span data-ttu-id="7c2d9-302">Auðkenni vaktar (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-302">Shift ID (required)</span></span>
- <span data-ttu-id="7c2d9-303">Skattanúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-303">Tax Number (required)</span></span>
- <span data-ttu-id="7c2d9-304">Auðkenni stéttarfélags (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-304">Union ID (required)</span></span>
- <span data-ttu-id="7c2d9-305">Vinnudagskenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-305">Work Day ID (required)</span></span>
- <span data-ttu-id="7c2d9-306">Vinnuleyfisnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="7c2d9-307">Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="7c2d9-308">Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="7c2d9-309">Atvinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-309">Employment details</span></span>

<span data-ttu-id="7c2d9-310">Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="7c2d9-311">Dayforce styður aðeins eina starfsferilsskrá í einu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="7c2d9-312">Upphafsdagsetning ráðningar (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-312">Employment start date (required)</span></span>
- <span data-ttu-id="7c2d9-313">Dagsetning starfsloka</span><span class="sxs-lookup"><span data-stu-id="7c2d9-313">Employment end date</span></span>
- <span data-ttu-id="7c2d9-314">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-314">Start date</span></span>
- <span data-ttu-id="7c2d9-315">Breyttur fyrsti starfsdagur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-315">Adjusted start date</span></span>
- <span data-ttu-id="7c2d9-316">Dagsetning starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="7c2d9-317">Ástæða starfsloka (krafist við starfslok)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="7c2d9-318">Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="7c2d9-319">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-319">Talent</span></span>                | <span data-ttu-id="7c2d9-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2d9-321">Nýlegasti ráðningardagurinn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-321">Most recent hire date</span></span> | <span data-ttu-id="7c2d9-322">Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="7c2d9-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="7c2d9-323">Starfslokadagur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-323">Termination date</span></span>      | <span data-ttu-id="7c2d9-324">Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið</span><span class="sxs-lookup"><span data-stu-id="7c2d9-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="7c2d9-325">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-325">Start date</span></span>            | <span data-ttu-id="7c2d9-326">Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="7c2d9-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="7c2d9-327">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="7c2d9-327">Original hire date</span></span>    | <span data-ttu-id="7c2d9-328">Upphaf ráðningar fyrir elsta atvinnuferil</span><span class="sxs-lookup"><span data-stu-id="7c2d9-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="7c2d9-329">Laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-329">Compensation</span></span>

<span data-ttu-id="7c2d9-330">Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="7c2d9-331">Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="7c2d9-332">Gildisdagsetning (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-332">Effective Date (required)</span></span>
- <span data-ttu-id="7c2d9-333">Gildistími</span><span class="sxs-lookup"><span data-stu-id="7c2d9-333">Expiration date</span></span>
- <span data-ttu-id="7c2d9-334">Launataxti (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-334">Pay Rate (required)</span></span>
- <span data-ttu-id="7c2d9-335">Umreikningur launataxta (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="7c2d9-336">Árlegt jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="7c2d9-337">Klukkutíma jafngildi (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="7c2d9-338">Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="7c2d9-339">Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="7c2d9-340">Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="7c2d9-341">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="7c2d9-342">Auðkenni kennitölu</span><span class="sxs-lookup"><span data-stu-id="7c2d9-342">Social Security identifier</span></span> 

<span data-ttu-id="7c2d9-343">Sérhver starfsmaður verður að hafa eitt aðalauðkenni.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="7c2d9-344">Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="7c2d9-345">Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="7c2d9-346">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-346">Primary (required)</span></span>
- <span data-ttu-id="7c2d9-347">Gerð auðkennis = „Kennitala“</span><span class="sxs-lookup"><span data-stu-id="7c2d9-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="7c2d9-348">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="7c2d9-348">Issued Date</span></span>
- <span data-ttu-id="7c2d9-349">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-349">Expiration Date</span></span>

<span data-ttu-id="7c2d9-350">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="7c2d9-351">Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="7c2d9-352">Bankareikningar og útborganir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="7c2d9-353">Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="7c2d9-354">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-354">Talent</span></span>                         | <span data-ttu-id="7c2d9-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2d9-356">Bankareikningsnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="7c2d9-357">SWIFT-kóði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-357">SWIFT code (required)</span></span>          | <span data-ttu-id="7c2d9-358">Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="7c2d9-359">Númer útibús (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="7c2d9-360">Gerð bankareiknings (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-360">Bank account type (required)</span></span>   | <span data-ttu-id="7c2d9-361">Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="7c2d9-362">Studd gildi innihalda **Athugun** og **Launaskrá**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="7c2d9-363">Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="7c2d9-364">Allir aðrir reikningar eru hunsaðir.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="7c2d9-365">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-365">Address information</span></span>

<span data-ttu-id="7c2d9-366">Sérhver starfsmaður verður að hafa eina aðalstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-366">Every employee must have one primary location.</span></span> <span data-ttu-id="7c2d9-367">Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="7c2d9-368">Aðalauðkenni (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-368">Primary (required)</span></span>
- <span data-ttu-id="7c2d9-369">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-369">Country/region (required)</span></span>
- <span data-ttu-id="7c2d9-370">Póstnúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="7c2d9-371">Gata (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-371">Street (required)</span></span>
- <span data-ttu-id="7c2d9-372">Götunúmer (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-372">Street Number (required)</span></span>
- <span data-ttu-id="7c2d9-373">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="7c2d9-373">Building Complement</span></span>
- <span data-ttu-id="7c2d9-374">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-374">City (required)</span></span>
- <span data-ttu-id="7c2d9-375">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-375">State (required)</span></span>
- <span data-ttu-id="7c2d9-376">Sýsla (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="7c2d9-377">Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada</span><span class="sxs-lookup"><span data-stu-id="7c2d9-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="7c2d9-378">Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="7c2d9-379">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-379">Departments are required on positions.</span></span>
- <span data-ttu-id="7c2d9-380">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="7c2d9-381">Þú getur stillt Talent til að krefjast þess að stöður tilgreini deild.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="7c2d9-382">Til að gera þetta skal fara í **Samnýttar stöður mannauðs > Stöður > Krefjast deilda á stöðum**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="7c2d9-383">Við mælum með að þessari stillingu sé framfylgt fyrir samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="7c2d9-384">Starfsgerðir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-384">Job types</span></span>

<span data-ttu-id="7c2d9-385">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="7c2d9-386">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="7c2d9-387">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="7c2d9-388">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="7c2d9-389">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="7c2d9-390">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-390">Job type</span></span>   | <span data-ttu-id="7c2d9-391">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="7c2d9-392">Tímar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-392">Hourly</span></span>     | <span data-ttu-id="7c2d9-393">Tímar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-393">Hourly</span></span>      |
| <span data-ttu-id="7c2d9-394">Föst laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-394">Salaried</span></span>   | <span data-ttu-id="7c2d9-395">Föst laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="7c2d9-396">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-396">Position types</span></span> 

<span data-ttu-id="7c2d9-397">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="7c2d9-398">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="7c2d9-399">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="7c2d9-400">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="7c2d9-400">Position type</span></span>   | <span data-ttu-id="7c2d9-401">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="7c2d9-402">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="7c2d9-402">Full-time</span></span>       | <span data-ttu-id="7c2d9-403">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-403">Full time employee</span></span> |
| <span data-ttu-id="7c2d9-404">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="7c2d9-404">Part-time</span></span>       | <span data-ttu-id="7c2d9-405">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="7c2d9-406">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-406">Reason codes</span></span>

<span data-ttu-id="7c2d9-407">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="7c2d9-408">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="7c2d9-409">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="7c2d9-410">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-410">Reason code</span></span>    | <span data-ttu-id="7c2d9-411">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-411">Description</span></span>      | <span data-ttu-id="7c2d9-412">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="7c2d9-413">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="7c2d9-413">RESIGNATION</span></span>    | <span data-ttu-id="7c2d9-414">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-414">Resignation</span></span>      | <span data-ttu-id="7c2d9-415">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-415">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-416">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="7c2d9-416">TERMINATION</span></span>    | <span data-ttu-id="7c2d9-417">Lok</span><span class="sxs-lookup"><span data-stu-id="7c2d9-417">Termination</span></span>      | <span data-ttu-id="7c2d9-418">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-418">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-419">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="7c2d9-419">RETIREMENT</span></span>     | <span data-ttu-id="7c2d9-420">Starfslok</span><span class="sxs-lookup"><span data-stu-id="7c2d9-420">Retirement</span></span>       | <span data-ttu-id="7c2d9-421">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-421">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-422">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="7c2d9-422">OTHER</span></span>          | <span data-ttu-id="7c2d9-423">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="7c2d9-423">Other Reasons</span></span>    | <span data-ttu-id="7c2d9-424">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-424">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-425">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="7c2d9-425">DEATH</span></span>          | <span data-ttu-id="7c2d9-426">Dauði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-426">Death</span></span>            | <span data-ttu-id="7c2d9-427">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-427">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-428">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="7c2d9-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="7c2d9-429">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-429">Leave of Absence</span></span> | <span data-ttu-id="7c2d9-430">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-430">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-431">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="7c2d9-431">CONTRACTEND</span></span>    | <span data-ttu-id="7c2d9-432">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-432">End of Contract</span></span>  | <span data-ttu-id="7c2d9-433">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-433">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-434">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-434">SALARYCHANGE</span></span>   | <span data-ttu-id="7c2d9-435">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="7c2d9-435">Change of Salary</span></span> | <span data-ttu-id="7c2d9-436">Laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="7c2d9-437">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="7c2d9-437">Marital status</span></span>

<span data-ttu-id="7c2d9-438">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7c2d9-439">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="7c2d9-440">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-440">Talent</span></span>                 | <span data-ttu-id="7c2d9-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="7c2d9-442">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-442">Married</span></span>                | <span data-ttu-id="7c2d9-443">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-443">Married</span></span>              |
| <span data-ttu-id="7c2d9-444">Ein</span><span class="sxs-lookup"><span data-stu-id="7c2d9-444">Single</span></span>                 | <span data-ttu-id="7c2d9-445">Ein</span><span class="sxs-lookup"><span data-stu-id="7c2d9-445">Single</span></span>               |
| <span data-ttu-id="7c2d9-446">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7c2d9-446">Widowed</span></span>                | <span data-ttu-id="7c2d9-447">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7c2d9-447">Widowed</span></span>              |
| <span data-ttu-id="7c2d9-448">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-448">Divorced</span></span>               | <span data-ttu-id="7c2d9-449">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-449">Divorced</span></span>             |
| <span data-ttu-id="7c2d9-450">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="7c2d9-450">Registered Partnership</span></span> | <span data-ttu-id="7c2d9-451">Sambúð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-451">Domestic Partnership</span></span> |
| <span data-ttu-id="7c2d9-452">None</span><span class="sxs-lookup"><span data-stu-id="7c2d9-452">None</span></span>                   | <span data-ttu-id="7c2d9-453">None</span><span class="sxs-lookup"><span data-stu-id="7c2d9-453">None</span></span>                 |
| <span data-ttu-id="7c2d9-454">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-454">Cohabiting</span></span>             | <span data-ttu-id="7c2d9-455">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="7c2d9-456">Kyn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-456">Gender</span></span>

<span data-ttu-id="7c2d9-457">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7c2d9-458">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="7c2d9-459">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-459">Talent</span></span>       | <span data-ttu-id="7c2d9-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="7c2d9-461">Karl</span><span class="sxs-lookup"><span data-stu-id="7c2d9-461">Male</span></span>         | <span data-ttu-id="7c2d9-462">Karl</span><span class="sxs-lookup"><span data-stu-id="7c2d9-462">Male</span></span>            |
| <span data-ttu-id="7c2d9-463">Kona</span><span class="sxs-lookup"><span data-stu-id="7c2d9-463">Female</span></span>       | <span data-ttu-id="7c2d9-464">Kona</span><span class="sxs-lookup"><span data-stu-id="7c2d9-464">Female</span></span>          |
| <span data-ttu-id="7c2d9-465">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="7c2d9-465">Non-specific</span></span> | <span data-ttu-id="7c2d9-466">*Ekki stutt*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="7c2d9-467">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-467">Earning codes</span></span>

<span data-ttu-id="7c2d9-468">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7c2d9-469">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="7c2d9-470">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="7c2d9-471">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-471">Supported frequencies</span></span>

- <span data-ttu-id="7c2d9-472">Allir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-472">All</span></span>
- <span data-ttu-id="7c2d9-473">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-473">EVERYPAY</span></span>
- <span data-ttu-id="7c2d9-474">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="7c2d9-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="7c2d9-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="7c2d9-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="7c2d9-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="7c2d9-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="7c2d9-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-477">1OFMTH</span></span>
- <span data-ttu-id="7c2d9-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-478">LASTOFMTH</span></span>
- <span data-ttu-id="7c2d9-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-479">2OFMTH</span></span>
- <span data-ttu-id="7c2d9-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-480">3OFMTH</span></span>
- <span data-ttu-id="7c2d9-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-481">4OFMTH</span></span>
- <span data-ttu-id="7c2d9-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-482">5OFMTH</span></span>
- <span data-ttu-id="7c2d9-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-483">1N2OFMTH</span></span>
- <span data-ttu-id="7c2d9-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-484">3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-485">1N3OFMTH</span></span>
- <span data-ttu-id="7c2d9-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-486">1N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-487">2N3OFMTH</span></span>
- <span data-ttu-id="7c2d9-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-488">2N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="7c2d9-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="7c2d9-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="7c2d9-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="7c2d9-496">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="7c2d9-497">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="7c2d9-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="7c2d9-499">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="7c2d9-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="7c2d9-501">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-501">Addresses</span></span>

<span data-ttu-id="7c2d9-502">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="7c2d9-503">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="7c2d9-504">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-504">Talent</span></span>          | <span data-ttu-id="7c2d9-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="7c2d9-506">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-506">Country/Region</span></span>  | <span data-ttu-id="7c2d9-507">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-507">Country Code</span></span>          |
| <span data-ttu-id="7c2d9-508">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-508">Zip/Postal Code</span></span> | <span data-ttu-id="7c2d9-509">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-509">Postal Code</span></span>           |
| <span data-ttu-id="7c2d9-510">Ríki</span><span class="sxs-lookup"><span data-stu-id="7c2d9-510">State</span></span>           | <span data-ttu-id="7c2d9-511">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-511">State Code</span></span>            |
| <span data-ttu-id="7c2d9-512">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-512">City</span></span>            | <span data-ttu-id="7c2d9-513">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-513">City</span></span>                  |
| <span data-ttu-id="7c2d9-514">Sýsla</span><span class="sxs-lookup"><span data-stu-id="7c2d9-514">County</span></span>          | <span data-ttu-id="7c2d9-515">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-515">County (Municipality)</span></span> |
| <span data-ttu-id="7c2d9-516">Gata</span><span class="sxs-lookup"><span data-stu-id="7c2d9-516">Street</span></span>          | <span data-ttu-id="7c2d9-517">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="7c2d9-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="7c2d9-518">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-518">Tax regions</span></span>

<span data-ttu-id="7c2d9-519">Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="7c2d9-520">Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="7c2d9-521">Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="7c2d9-522">Skattumdæmi (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-522">Tax region (required)</span></span>
- <span data-ttu-id="7c2d9-523">Land/svæði (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-523">Country/Region (required)</span></span>
- <span data-ttu-id="7c2d9-524">Ríki (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-524">State (required)</span></span>
- <span data-ttu-id="7c2d9-525">Sýsla</span><span class="sxs-lookup"><span data-stu-id="7c2d9-525">County</span></span> 
- <span data-ttu-id="7c2d9-526">Borg (krafist)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="7c2d9-527">Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó</span><span class="sxs-lookup"><span data-stu-id="7c2d9-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="7c2d9-528">Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="7c2d9-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="7c2d9-529">Deildir eru nauðsynlegar fyrir stöður.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-529">Departments are required on positions.</span></span>
- <span data-ttu-id="7c2d9-530">Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="7c2d9-531">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-531">Job types</span></span>

<span data-ttu-id="7c2d9-532">Starfsgerðir eru notaðar til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="7c2d9-533">Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="7c2d9-534">Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="7c2d9-535">Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="7c2d9-536">Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="7c2d9-537">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-537">Job type</span></span>   | <span data-ttu-id="7c2d9-538">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="7c2d9-539">Tímar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-539">Hourly</span></span>     | <span data-ttu-id="7c2d9-540">MX tímakaup</span><span class="sxs-lookup"><span data-stu-id="7c2d9-540">MX Hourly</span></span>   |
| <span data-ttu-id="7c2d9-541">Föst laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-541">Salaried</span></span>   | <span data-ttu-id="7c2d9-542">MX föst laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="7c2d9-543">Stöðugerðir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-543">Position types</span></span> 

<span data-ttu-id="7c2d9-544">Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="7c2d9-545">Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="7c2d9-546">Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="7c2d9-547">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="7c2d9-547">Position type</span></span>   | <span data-ttu-id="7c2d9-548">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="7c2d9-549">Fullt starf</span><span class="sxs-lookup"><span data-stu-id="7c2d9-549">Full-time</span></span>       | <span data-ttu-id="7c2d9-550">Starfsmaður í fullu starfi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-550">Full time employee</span></span> |
| <span data-ttu-id="7c2d9-551">Hlutastarf</span><span class="sxs-lookup"><span data-stu-id="7c2d9-551">Part-time</span></span>       | <span data-ttu-id="7c2d9-552">Starfsmaður í hlutastarfi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="7c2d9-553">Ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-553">Reason codes</span></span>

<span data-ttu-id="7c2d9-554">Ástæðukóðar veita upplýsingar um stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="7c2d9-555">Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="7c2d9-556">Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="7c2d9-557">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-557">Reason code</span></span>            | <span data-ttu-id="7c2d9-558">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-558">Description</span></span>                    | <span data-ttu-id="7c2d9-559">Tiltækar sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="7c2d9-560">BROTTFÖR Á UNDAN LAUNAGREIÐSLU</span><span class="sxs-lookup"><span data-stu-id="7c2d9-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="7c2d9-561">Brottför á undan launum</span><span class="sxs-lookup"><span data-stu-id="7c2d9-561">Departure before first payroll</span></span> | <span data-ttu-id="7c2d9-562">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-562">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-563">UPPSÖGN</span><span class="sxs-lookup"><span data-stu-id="7c2d9-563">RESIGNATION</span></span>            | <span data-ttu-id="7c2d9-564">Uppsögn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-564">Resignation</span></span>                    | <span data-ttu-id="7c2d9-565">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-565">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-566">LÍFEYRIR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-566">PENSION</span></span>                | <span data-ttu-id="7c2d9-567">Lífeyrir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-567">Pension</span></span>                        | <span data-ttu-id="7c2d9-568">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-568">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-569">STARFSLOK</span><span class="sxs-lookup"><span data-stu-id="7c2d9-569">TERMINATION</span></span>            | <span data-ttu-id="7c2d9-570">Lok</span><span class="sxs-lookup"><span data-stu-id="7c2d9-570">Termination</span></span>                    | <span data-ttu-id="7c2d9-571">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-571">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-572">STARFSLOK SÖKUM ALDURS</span><span class="sxs-lookup"><span data-stu-id="7c2d9-572">RETIREMENT</span></span>             | <span data-ttu-id="7c2d9-573">Starfslok</span><span class="sxs-lookup"><span data-stu-id="7c2d9-573">Retirement</span></span>                     | <span data-ttu-id="7c2d9-574">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-574">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-575">FJARVERA</span><span class="sxs-lookup"><span data-stu-id="7c2d9-575">ABSENTEE</span></span>               | <span data-ttu-id="7c2d9-576">Fjarvera</span><span class="sxs-lookup"><span data-stu-id="7c2d9-576">Absentee</span></span>                       | <span data-ttu-id="7c2d9-577">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-577">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-578">ANNAÐ</span><span class="sxs-lookup"><span data-stu-id="7c2d9-578">OTHER</span></span>                  | <span data-ttu-id="7c2d9-579">Aðrar ástæður</span><span class="sxs-lookup"><span data-stu-id="7c2d9-579">Other Reasons</span></span>                  | <span data-ttu-id="7c2d9-580">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-580">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-581">LOKUN</span><span class="sxs-lookup"><span data-stu-id="7c2d9-581">CLOSURE</span></span>                | <span data-ttu-id="7c2d9-582">Viðskiptalokun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-582">Business Closure</span></span>               | <span data-ttu-id="7c2d9-583">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-583">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-584">DAUÐI</span><span class="sxs-lookup"><span data-stu-id="7c2d9-584">DEATH</span></span>                  | <span data-ttu-id="7c2d9-585">Dauði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-585">Death</span></span>                          | <span data-ttu-id="7c2d9-586">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-586">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-587">FJARVISTARLEYFI</span><span class="sxs-lookup"><span data-stu-id="7c2d9-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="7c2d9-588">Fjarvistarleyfi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-588">Leave of Absence</span></span>               | <span data-ttu-id="7c2d9-589">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-589">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-590">SAMNINGSLOK</span><span class="sxs-lookup"><span data-stu-id="7c2d9-590">CONTRACTEND</span></span>            | <span data-ttu-id="7c2d9-591">Lok á samningi</span><span class="sxs-lookup"><span data-stu-id="7c2d9-591">End of Contract</span></span>                | <span data-ttu-id="7c2d9-592">Segja starfskrafti upp</span><span class="sxs-lookup"><span data-stu-id="7c2d9-592">Terminate worker</span></span>     |
| <span data-ttu-id="7c2d9-593">LAUNABREYTINGAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-593">SALARYCHANGE</span></span>           | <span data-ttu-id="7c2d9-594">Breyting launa</span><span class="sxs-lookup"><span data-stu-id="7c2d9-594">Change of Salary</span></span>               | <span data-ttu-id="7c2d9-595">Laun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="7c2d9-596">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-596">Terms of employment</span></span>

<span data-ttu-id="7c2d9-597">Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="7c2d9-598">Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="7c2d9-599">Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="7c2d9-600">Ráðningarskilmálar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-600">Terms of employment</span></span>   | <span data-ttu-id="7c2d9-601">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c2d9-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="7c2d9-602">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="7c2d9-602">Regular</span></span>               | <span data-ttu-id="7c2d9-603">Venjuleg</span><span class="sxs-lookup"><span data-stu-id="7c2d9-603">Regular</span></span>     |
| <span data-ttu-id="7c2d9-604">Beint</span><span class="sxs-lookup"><span data-stu-id="7c2d9-604">Direct</span></span>                | <span data-ttu-id="7c2d9-605">Beint</span><span class="sxs-lookup"><span data-stu-id="7c2d9-605">Direct</span></span>      |
| <span data-ttu-id="7c2d9-606">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="7c2d9-606">Internship</span></span>            | <span data-ttu-id="7c2d9-607">Starfsnám</span><span class="sxs-lookup"><span data-stu-id="7c2d9-607">Internship</span></span>  |
| <span data-ttu-id="7c2d9-608">Fast</span><span class="sxs-lookup"><span data-stu-id="7c2d9-608">Permanent</span></span>             | <span data-ttu-id="7c2d9-609">Fast</span><span class="sxs-lookup"><span data-stu-id="7c2d9-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="7c2d9-610">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="7c2d9-610">Marital status</span></span>

<span data-ttu-id="7c2d9-611">Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7c2d9-612">Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="7c2d9-613">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-613">Talent</span></span>                 | <span data-ttu-id="7c2d9-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="7c2d9-615">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-615">Married</span></span>                | <span data-ttu-id="7c2d9-616">Gift(ur)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-616">Married</span></span>                   |
| <span data-ttu-id="7c2d9-617">Ein</span><span class="sxs-lookup"><span data-stu-id="7c2d9-617">Single</span></span>                 | <span data-ttu-id="7c2d9-618">Ein</span><span class="sxs-lookup"><span data-stu-id="7c2d9-618">Single</span></span>                    |
| <span data-ttu-id="7c2d9-619">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7c2d9-619">Widowed</span></span>                | <span data-ttu-id="7c2d9-620">Ekkja/ekkill</span><span class="sxs-lookup"><span data-stu-id="7c2d9-620">Widowed</span></span>                   |
| <span data-ttu-id="7c2d9-621">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-621">Divorced</span></span>               | <span data-ttu-id="7c2d9-622">Fráskilin(n)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-622">Divorced</span></span>                  |
| <span data-ttu-id="7c2d9-623">Skráð hjónaband</span><span class="sxs-lookup"><span data-stu-id="7c2d9-623">Registered Partnership</span></span> | <span data-ttu-id="7c2d9-624">Sambúð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="7c2d9-625">None</span><span class="sxs-lookup"><span data-stu-id="7c2d9-625">None</span></span>                   | <span data-ttu-id="7c2d9-626">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7c2d9-627">Í sambúð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-627">Cohabiting</span></span>             | <span data-ttu-id="7c2d9-628">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="7c2d9-629">Kyn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-629">Gender</span></span>

<span data-ttu-id="7c2d9-630">Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7c2d9-631">Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="7c2d9-632">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-632">Talent</span></span>       | <span data-ttu-id="7c2d9-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="7c2d9-634">Karl</span><span class="sxs-lookup"><span data-stu-id="7c2d9-634">Male</span></span>         | <span data-ttu-id="7c2d9-635">Karl</span><span class="sxs-lookup"><span data-stu-id="7c2d9-635">Male</span></span>                      |
| <span data-ttu-id="7c2d9-636">Kona</span><span class="sxs-lookup"><span data-stu-id="7c2d9-636">Female</span></span>       | <span data-ttu-id="7c2d9-637">Kona</span><span class="sxs-lookup"><span data-stu-id="7c2d9-637">Female</span></span>                    |
| <span data-ttu-id="7c2d9-638">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="7c2d9-638">Non-specific</span></span> | <span data-ttu-id="7c2d9-639">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="7c2d9-640">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="7c2d9-640">Payment method</span></span>

<span data-ttu-id="7c2d9-641">Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="7c2d9-642">Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7c2d9-643">Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="7c2d9-644">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-644">Talent</span></span>             | <span data-ttu-id="7c2d9-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="7c2d9-646">Innlausn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-646">Cash</span></span>               | <span data-ttu-id="7c2d9-647">Innlausn</span><span class="sxs-lookup"><span data-stu-id="7c2d9-647">Cash</span></span>                      |
| <span data-ttu-id="7c2d9-648">Rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="7c2d9-648">Electronic Payment</span></span> | <span data-ttu-id="7c2d9-649">Flutningur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-649">Transfer</span></span>                  |
| <span data-ttu-id="7c2d9-650">Merkja</span><span class="sxs-lookup"><span data-stu-id="7c2d9-650">Check</span></span>              | <span data-ttu-id="7c2d9-651">Ávísun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-651">Cheque</span></span>                    |
| <span data-ttu-id="7c2d9-652">Bankaávísun</span><span class="sxs-lookup"><span data-stu-id="7c2d9-652">Bank Draft</span></span>         | <span data-ttu-id="7c2d9-653">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7c2d9-654">Annað</span><span class="sxs-lookup"><span data-stu-id="7c2d9-654">Other</span></span>              | <span data-ttu-id="7c2d9-655">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="7c2d9-656">Gerð bankareiknings</span><span class="sxs-lookup"><span data-stu-id="7c2d9-656">Bank account type</span></span>

<span data-ttu-id="7c2d9-657">Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="7c2d9-658">Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="7c2d9-659">Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="7c2d9-660">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-660">Talent</span></span>            | <span data-ttu-id="7c2d9-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="7c2d9-662">Ávísanareikningur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-662">Checking Account</span></span>  | <span data-ttu-id="7c2d9-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="7c2d9-663">CheckingAccount</span></span>           |
| <span data-ttu-id="7c2d9-664">Launareikningur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-664">Payroll Account</span></span>   | <span data-ttu-id="7c2d9-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="7c2d9-665">PayrollAccount</span></span>            |
| <span data-ttu-id="7c2d9-666">Sparnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-666">Savings Account</span></span>   | <span data-ttu-id="7c2d9-667">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7c2d9-668">BankGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-668">BankGirot account</span></span> | <span data-ttu-id="7c2d9-669">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7c2d9-670">PlusGirot-reikningur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-670">PlusGirot account</span></span> | <span data-ttu-id="7c2d9-671">*Ekki stutt af Mexíkó*</span><span class="sxs-lookup"><span data-stu-id="7c2d9-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="7c2d9-672">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7c2d9-672">Earning codes</span></span>

<span data-ttu-id="7c2d9-673">Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7c2d9-674">Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="7c2d9-675">Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="7c2d9-676">Studdar tíðnir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-676">Supported frequencies</span></span>

- <span data-ttu-id="7c2d9-677">Allir</span><span class="sxs-lookup"><span data-stu-id="7c2d9-677">All</span></span>
- <span data-ttu-id="7c2d9-678">ALLAR LAUNAGREIÐSLUR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-678">EVERYPAY</span></span>
- <span data-ttu-id="7c2d9-679">SÉRHVERT LAUNATÍMABIL</span><span class="sxs-lookup"><span data-stu-id="7c2d9-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="7c2d9-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="7c2d9-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="7c2d9-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="7c2d9-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="7c2d9-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-682">1OFMTH</span></span>
- <span data-ttu-id="7c2d9-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-683">LASTOFMTH</span></span>
- <span data-ttu-id="7c2d9-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-684">2OFMTH</span></span>
- <span data-ttu-id="7c2d9-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-685">3OFMTH</span></span>
- <span data-ttu-id="7c2d9-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-686">4OFMTH</span></span>
- <span data-ttu-id="7c2d9-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-687">5OFMTH</span></span>
- <span data-ttu-id="7c2d9-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-688">1N2OFMTH</span></span>
- <span data-ttu-id="7c2d9-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-689">3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-690">1N3OFMTH</span></span>
- <span data-ttu-id="7c2d9-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-691">1N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-692">2N3OFMTH</span></span>
- <span data-ttu-id="7c2d9-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-693">2N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="7c2d9-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7c2d9-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="7c2d9-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="7c2d9-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="7c2d9-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="7c2d9-701">LASTOFQTR - LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="7c2d9-702">LASTMTHOFQTR - LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="7c2d9-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="7c2d9-704">LASTOFYEAR - LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="7c2d9-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7c2d9-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="7c2d9-706">Aðsetur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-706">Addresses</span></span>

<span data-ttu-id="7c2d9-707">Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="7c2d9-708">Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="7c2d9-709">Talent</span><span class="sxs-lookup"><span data-stu-id="7c2d9-709">Talent</span></span>              | <span data-ttu-id="7c2d9-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="7c2d9-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="7c2d9-711">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-711">Country/Region</span></span>      | <span data-ttu-id="7c2d9-712">Landsnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-712">Country Code</span></span>          |
| <span data-ttu-id="7c2d9-713">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-713">Zip/Postal Code</span></span>     | <span data-ttu-id="7c2d9-714">Póstnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-714">Postal Code</span></span>           |
| <span data-ttu-id="7c2d9-715">Ríki</span><span class="sxs-lookup"><span data-stu-id="7c2d9-715">State</span></span>               | <span data-ttu-id="7c2d9-716">Ríkiskóði</span><span class="sxs-lookup"><span data-stu-id="7c2d9-716">State Code</span></span>            |
| <span data-ttu-id="7c2d9-717">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-717">City</span></span>                | <span data-ttu-id="7c2d9-718">Póststöð</span><span class="sxs-lookup"><span data-stu-id="7c2d9-718">City</span></span>                  |
| <span data-ttu-id="7c2d9-719">Sýsla</span><span class="sxs-lookup"><span data-stu-id="7c2d9-719">County</span></span>              | <span data-ttu-id="7c2d9-720">Sýsla (sveitarfélag)</span><span class="sxs-lookup"><span data-stu-id="7c2d9-720">County (Municipality)</span></span> |
| <span data-ttu-id="7c2d9-721">Gata</span><span class="sxs-lookup"><span data-stu-id="7c2d9-721">Street</span></span>              | <span data-ttu-id="7c2d9-722">Heimilisfang, lína 1</span><span class="sxs-lookup"><span data-stu-id="7c2d9-722">Address Line 1</span></span>        |
| <span data-ttu-id="7c2d9-723">Húsnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-723">Street Number</span></span>       | <span data-ttu-id="7c2d9-724">Heimilisfang, lína 2</span><span class="sxs-lookup"><span data-stu-id="7c2d9-724">Address Line 2</span></span>        |
| <span data-ttu-id="7c2d9-725">Býr til viðbót</span><span class="sxs-lookup"><span data-stu-id="7c2d9-725">Building Complement</span></span> | <span data-ttu-id="7c2d9-726">Heimilisfang, lína 5</span><span class="sxs-lookup"><span data-stu-id="7c2d9-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="7c2d9-727">Vegabréfsnúmer</span><span class="sxs-lookup"><span data-stu-id="7c2d9-727">Passport number</span></span>

<span data-ttu-id="7c2d9-728">Starfsmenn geta gefið upp vegabréfsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-728">Employees can declare passport information.</span></span> <span data-ttu-id="7c2d9-729">Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="7c2d9-730">Gerð auðkennis = „Vegabréf“</span><span class="sxs-lookup"><span data-stu-id="7c2d9-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="7c2d9-731">Útgáfudagsetning</span><span class="sxs-lookup"><span data-stu-id="7c2d9-731">Issued Date</span></span>
- <span data-ttu-id="7c2d9-732">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="7c2d9-732">Expiration Date</span></span>

<span data-ttu-id="7c2d9-733">Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="7c2d9-734">Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="7c2d9-735">Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.</span><span class="sxs-lookup"><span data-stu-id="7c2d9-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

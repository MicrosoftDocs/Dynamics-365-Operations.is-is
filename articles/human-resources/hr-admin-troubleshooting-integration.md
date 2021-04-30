---
title: Algengar spurningar um samþættingu við Finance
description: Þessi grein útskýrir hvaða gögn eru samstillt í samþættingu á Human Resources og Finance.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5befac6c72153332319eefc1aaeab30c33f4c69
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892252"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="31131-103">Algengar spurningar um samþættingu við Finance</span><span class="sxs-lookup"><span data-stu-id="31131-103">Integration with Finance FAQ</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="31131-104">Þetta efnisatriði svarar algengum spurningum sem tengjast gögnunum sem eru samstillt þegar Dynamics 365 Human Resources er samþætt við Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="31131-105">Get ég breytt Dynamics 365 Talent notanda í Power Apps?</span><span class="sxs-lookup"><span data-stu-id="31131-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="31131-106">Nei.</span><span class="sxs-lookup"><span data-stu-id="31131-106">No.</span></span> <span data-ttu-id="31131-107">Ef notanda Human Resources er breytt gæti samþætting milli Human Resources og Dataverse mistekist.</span><span class="sxs-lookup"><span data-stu-id="31131-107">If you edit the Human Resources application user, the integration between Human Resources and Dataverse might fail.</span></span> <span data-ttu-id="31131-108">Eftirfarandi tafla sýnir sjálfgefnar stillingar fyrir Talent notanda.</span><span class="sxs-lookup"><span data-stu-id="31131-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="31131-109">Fullt nafn</span><span class="sxs-lookup"><span data-stu-id="31131-109">Full Name</span></span> | <span data-ttu-id="31131-110">Kenni umsóknar</span><span class="sxs-lookup"><span data-stu-id="31131-110">Application ID</span></span> | <span data-ttu-id="31131-111">Azure AD Kenni hlutar</span><span class="sxs-lookup"><span data-stu-id="31131-111">Azure AD Object ID</span></span> | <span data-ttu-id="31131-112">URI forritskennis</span><span class="sxs-lookup"><span data-stu-id="31131-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="31131-113">Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="31131-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="31131-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="31131-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="31131-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span><span class="sxs-lookup"><span data-stu-id="31131-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="31131-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="31131-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![Sjálfgefnar stillingar fyrir notanda Talent-forrits](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="31131-118">Eru öll gögn samstillt eða bara sumar gagnaeiningar?</span><span class="sxs-lookup"><span data-stu-id="31131-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="31131-119">Undirsafn af gögnunum er samstillt.</span><span class="sxs-lookup"><span data-stu-id="31131-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="31131-120">Fyrir lista yfir allar einingarnar skal sjá [Samþætting við Dynamics 365 Finance](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="31131-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a><span data-ttu-id="31131-121">Af hverju sé ég engin gögn samstillt við Dataverse?</span><span class="sxs-lookup"><span data-stu-id="31131-121">Why don't I see any data synced to Dataverse?</span></span>

<span data-ttu-id="31131-122">Sjálfgefið er að slökkt sé á samþættingu Dataverse í nýju umhverfi sem inniheldur ekki meðfylgjandi kynningargögn.</span><span class="sxs-lookup"><span data-stu-id="31131-122">By default, the Dataverse integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="31131-123">Sjálfgefið er að kveikt sé á því í nýju umhverfi sem innihalda kynningargögn og samstilling gagna hefst þegar umhverfið er útvegað.</span><span class="sxs-lookup"><span data-stu-id="31131-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="31131-124">Eftir að umhverfi þitt er tilbúið til að samstilla gögn geturðu kveikt á samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="31131-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="31131-125">Nánari upplýsingar er að finna í [Skilgreina Dataverse samþættingu](hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="31131-125">For more information, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="31131-126">Get ég búið til nýja vörpun án þess að nota sniðmátin?</span><span class="sxs-lookup"><span data-stu-id="31131-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="31131-127">Sniðmát eru upphafspunktur.</span><span class="sxs-lookup"><span data-stu-id="31131-127">Templates are the starting point.</span></span> <span data-ttu-id="31131-128">Hægt er að búa til sitt eigið sniðmát, en alltaf er þörf á sniðmáti þegar samþættingarverk er búið til.</span><span class="sxs-lookup"><span data-stu-id="31131-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="31131-129">Nánari upplýsingar um Data Integrator (DI), sniðmát og verk er að finna í [Samþætta gögn í Microsoft Dataverse](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="31131-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Microsoft Dataverse](/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="31131-130">Er hægt að varpa fjárhagsvíddum í flutning milli Human Resources og Finance?</span><span class="sxs-lookup"><span data-stu-id="31131-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="31131-131">Sem stendur eru fjárhagsvíddir ekki í Dataverse og eru þar af leiðandi ekki hluti af sjálfgefna sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="31131-131">Financial dimensions aren’t currently in Dataverse and as a result aren’t part of the default template.</span></span> <span data-ttu-id="31131-132">Þessi eining er fyrirhuguð en engin tímalína útgáfu er til eins og er.</span><span class="sxs-lookup"><span data-stu-id="31131-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="31131-133">Fyrir gögn sem eru í Finance en eru ekki til í Human Resources, skal tengja kerfin tvö saman með **Skilgreina tengla** í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31131-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![Varpa fjárhagsvíddum](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="31131-135">Stundum þegar ég flyt inn starfsmenn fara þeir í óvirka starfskrafta í Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="31131-136">Af hverju?</span><span class="sxs-lookup"><span data-stu-id="31131-136">Why?</span></span>

<span data-ttu-id="31131-137">Þú gætir fengið þessa villu ef starfsmenn hafa ekki virka skrá með starfsupplýsingum í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31131-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="31131-138">Til að leysa þetta skal fara í **Starfsmannastjórnun \> Starfsmenn \> Starfsferill \> Stjórnun dagsetninga** og staðfesta að til sé virk skrá starfsupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="31131-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="31131-139">Ef ég vel að varpa eingöngu undirsafni af svæðum, munu breytingar sem gerðar eru á óvörpuðum reitum kveikja á samstillingu?</span><span class="sxs-lookup"><span data-stu-id="31131-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="31131-140">Samstilling gagna fylgir framkvæmdaráætlun.</span><span class="sxs-lookup"><span data-stu-id="31131-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="31131-141">Samþættingin mun taka upp skrá ef eitthvert svæði í skránni breytist óháð því hvort svæðið er hluti af samþættingu vörpunar.</span><span class="sxs-lookup"><span data-stu-id="31131-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="31131-142">Hvernig get ég sent einungis breytingar á virkum starfskrafti og ekki riftum skrám?</span><span class="sxs-lookup"><span data-stu-id="31131-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="31131-143">Með því að nota „Ítarleg fyrirspurn“ geturðu síað og mótað upprunagögn áður en þau eru send inn í staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="31131-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Ítarleg fyrirspurn virkra starfskrafta](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="31131-145">Get ég tilgreint hvaða svæði skal senda til Finance fyrir tiltekna einingu?</span><span class="sxs-lookup"><span data-stu-id="31131-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="31131-146">Hægt er að bæta við eða fjarlægja svæði úr samþættingarverkinu.</span><span class="sxs-lookup"><span data-stu-id="31131-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="31131-147">Ekki öll gagnasvæði sem til eru í töflu Dataverse verða fyllt út í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="31131-147">Not all data fields that exist on the Dataverse table will be populated from Human Resources.</span></span>
<span data-ttu-id="31131-148">Hægt er að fylla út viðbótargögn í gegnum Power Apps.</span><span class="sxs-lookup"><span data-stu-id="31131-148">Additional data can be populated via Power Apps.</span></span>

![Bæta við eða fjarlægja reiti í eða úr samþættingarverki](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="31131-150">Ég setti upp samþættingu sem runuvinnslu en Human Resources missti tengingu við kerfi áfangastaðar.</span><span class="sxs-lookup"><span data-stu-id="31131-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="31131-151">Hvernig get ég sent sama sett af breytingum til kerfi áfangastaðar?</span><span class="sxs-lookup"><span data-stu-id="31131-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="31131-152">Ekki er krafist sérstakrar uppsetningar fyrir meðhöndlun frávika.</span><span class="sxs-lookup"><span data-stu-id="31131-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="31131-153">Data Integrator mun sjálfkrafa grípa og tilkynna villur sem gerast hjá uppruna og áfangastað og mun leyfa handvirkar endurtekningar.</span><span class="sxs-lookup"><span data-stu-id="31131-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="31131-154">Hins vegar leyfir hún ekki handvirka gagnaleiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="31131-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="31131-155">Ef nauðsynlegt er að uppfæra gögn, þá ætti það að gerast annað hvort við uppruna eða áfangastað.</span><span class="sxs-lookup"><span data-stu-id="31131-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="31131-156">Get ég sett upp samþættingu í báðar áttir?</span><span class="sxs-lookup"><span data-stu-id="31131-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="31131-157">Nei, samþætting er sem stendur ein leið (Human Resources til Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="31131-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="31131-158">Hins vegar er sjálfgefið sniðmát í boði til að senda gögn frá Human Resources til Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="31131-159">Get ég leyft skráareyðingu sem hluta af samþættingu minni?</span><span class="sxs-lookup"><span data-stu-id="31131-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="31131-160">Nei, Data Integrator mun ekki sækja eyddar færslur fyrir gagnaflutning.</span><span class="sxs-lookup"><span data-stu-id="31131-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="31131-161">Aðeins stofnun og uppfærslur á gögnum (UPSERT) eru innifaldar sem stendur.</span><span class="sxs-lookup"><span data-stu-id="31131-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="31131-162">Get ég keyrt aftur framkvæmd með villum?</span><span class="sxs-lookup"><span data-stu-id="31131-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="31131-163">Ef svo er, mun það senda heila skrá eða aðeins breytingarnar?</span><span class="sxs-lookup"><span data-stu-id="31131-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="31131-164">Fyrsta keyrsla Data Integrator er alltaf full keyrsla.</span><span class="sxs-lookup"><span data-stu-id="31131-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="31131-165">Næstu keyrslur byggjast á rakningu breytinga.</span><span class="sxs-lookup"><span data-stu-id="31131-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="31131-166">Við framkvæmd villukeyrslu eru færslurnar dregnar út samkvæmt umfangi keyrslunnar og nýjustu breytingar eru sendar út úr Dataverse.</span><span class="sxs-lookup"><span data-stu-id="31131-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Dataverse.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="31131-167">Þegar ég vista verkið fæ ég villuna: „Verk er með vörpunarvillur“.</span><span class="sxs-lookup"><span data-stu-id="31131-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="31131-168">Hvað geri ég?</span><span class="sxs-lookup"><span data-stu-id="31131-168">What do I do?</span></span>

<span data-ttu-id="31131-169">Athugaðu uppsetningu samþættingarlykla, gerðu nauðsynlegar breytingar á uppsetningunni og endurnýjaðu einingarnar í verkinu.</span><span class="sxs-lookup"><span data-stu-id="31131-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="31131-170">Þegar sjálfgefið sniðmát er notað verða samþættingarlyklarnir sjálfkrafa fluttir inn.</span><span class="sxs-lookup"><span data-stu-id="31131-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="31131-171">Þetta vandamál getur komið fram þegar nýjum verkum eru bætt við núverandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="31131-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="31131-172">Ef ég er með N fjölda lögaðila þar sem starfskraftar hafa vinnu, þarf ég að búa til vörpun fyrir hvern þeirra?</span><span class="sxs-lookup"><span data-stu-id="31131-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="31131-173">Já, fyrir hvern lögaðila í Finance þarf sérstakt samþættingarverk í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="31131-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="31131-174">Ég þarf að flytja gögn sem ekki eru hluti af sjálfgefna sniðmátinu sem Microsoft býður upp á.</span><span class="sxs-lookup"><span data-stu-id="31131-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="31131-175">Get ég gert þetta?</span><span class="sxs-lookup"><span data-stu-id="31131-175">Can I do this?</span></span>

<span data-ttu-id="31131-176">Já, hægt er að bæta við eða fjarlægja svæði úr núverandi sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="31131-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="31131-177">Sniðmátinu má breyta til að innihalda viðbótarupplýsingar úr öðrum töflum Dataverse.</span><span class="sxs-lookup"><span data-stu-id="31131-177">The template can be modified to include additional data from other Dataverse tables.</span></span> <span data-ttu-id="31131-178">Einingin verður að vera í Dataverse til að hún verði hluti af sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="31131-178">The entity must be in Dataverse for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="31131-179">Ég var að stofna ný umhverfi Finance og Human Resources og ég fæ villuna: „Gagnagildið brýtur hömlur fyrir heilleika.“</span><span class="sxs-lookup"><span data-stu-id="31131-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="31131-180">Af hverju?</span><span class="sxs-lookup"><span data-stu-id="31131-180">Why?</span></span>

<span data-ttu-id="31131-181">Ástæður þessarar villu geta falið í sér:</span><span class="sxs-lookup"><span data-stu-id="31131-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="31131-182">Gagnaflutningurinn leiddi til tvítekningar á gögnum sem voru dregin út úr upprunanum (Dataverse).</span><span class="sxs-lookup"><span data-stu-id="31131-182">The data transfer resulted in duplicate records extraction at the source (Dataverse).</span></span>

- <span data-ttu-id="31131-183">Gagnaflutningurinn hefur núll gildi fyrir svæði sem krafist er í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="31131-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="31131-184">Staðfestu að gögnin sem eru í Dataverse uppfylli kröfur Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="31131-184">Verify the data that is in Dataverse and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="31131-185">Ef framkvæmdavillur koma upp og auðkenni starfsmanns samstilltist ekki, hvernig finn ég þá vinnsluferilinn sem inniheldur starfsmannafærsluna?</span><span class="sxs-lookup"><span data-stu-id="31131-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="31131-186">Data Integrator mun búa til mörg verk í Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="31131-187">Sambandið milli verks Data Integrator og verks Finance er einn á móti einum.</span><span class="sxs-lookup"><span data-stu-id="31131-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="31131-188">Rektu tímann frá framkvæmdaferil Data Integrator og leitaðu að vísinum -1 fyrir verk Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="31131-189">Ef verknúmerið er 9 í Data Integrator er vísirinn í Finance 8.</span><span class="sxs-lookup"><span data-stu-id="31131-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="31131-190">Sæktu vísi verksins úr Data Integrator (í þessu dæmi er hann „9“).</span><span class="sxs-lookup"><span data-stu-id="31131-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![Sæktu vísi verks úr Data Integrator](media/CaptureTaskIndex.png)

2. <span data-ttu-id="31131-192">Rektu tíma framkvæmdar fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="31131-192">Track the execution time of the project.</span></span>

    ![Rektu tíma framkvæmdar fyrir verk](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="31131-194">Í Fjármálum skaltu bera kennsl á vísitölu - 1.</span><span class="sxs-lookup"><span data-stu-id="31131-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="31131-195">Í þessu dæmi passar verkið með viðskeytið „8“ og tíma framkvæmdar með vísi „0“ við tíma framkvæmdar í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="31131-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![Auðkenna vísi](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="31131-197">Eftir að hafa samþætt Human Resources og Finance, fæ ég ekki séð Human Resources-gögnin mín í Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="31131-198">Hvað geri ég?</span><span class="sxs-lookup"><span data-stu-id="31131-198">What do I do?</span></span>

<span data-ttu-id="31131-199">Samþættingin við Finance er ferli í tveimur skrefum.</span><span class="sxs-lookup"><span data-stu-id="31131-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="31131-200">Fyrst skaltu staðfesta að Human Resources-gögnin séu uppfærð og tiltæk í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="31131-200">First, verify that the Human Resources data is updated and available in Dataverse.</span></span> <span data-ttu-id="31131-201">Þetta er nærri því samstilling í rauntíma og hægt er að sannprófa hana í Power Apps með því að líta á gögnin innan gagnataflanna.</span><span class="sxs-lookup"><span data-stu-id="31131-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data tables.</span></span>

![Gögn í Dataverse](media/DataInCDS.png)

<span data-ttu-id="31131-203">Ef gögnin birtast ekki eins og búist er við í Dataverse skaltu staðfesta að einingin sé studd í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="31131-203">If the data is not appearing as expected in Dataverse, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="31131-204">Til að bæta við viðbótargögnum í Dataverse verður breyting af hálfu Windows að gerast.</span><span class="sxs-lookup"><span data-stu-id="31131-204">To include additional data in Dataverse, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="31131-205">Ef einingin er studd og gögnin eru tiltæk í Dataverse skaltu staðfesta að vörpunin sé rétt í Data Integrator.</span><span class="sxs-lookup"><span data-stu-id="31131-205">If the entity is supported and the data is available in Dataverse, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="31131-206">Ef vörpun samþættingar lítur vel út skaltu staðfesta að keyrsla á vinnslum gagnastjórnunar hafi tekist.</span><span class="sxs-lookup"><span data-stu-id="31131-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="31131-207">Villur geta komið fram meðan á framkvæmd runuvinnslunnar stendur.</span><span class="sxs-lookup"><span data-stu-id="31131-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="31131-208">Nánari upplýsingar um stjórnun gagna er að finna í [Gagnastjórnun](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="31131-208">For more information about Data Management, see [Data management](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="31131-209">Heimilisföngin fyrir starfsmennina mína eru rangar eftir að ég flyt þær inn í Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="31131-210">Hvað ætti ég að gera?</span><span class="sxs-lookup"><span data-stu-id="31131-210">What should I do?</span></span>

<span data-ttu-id="31131-211">Númeraröðin fyrir **Staðsetningarkenni** notar sama mynstur í bæði Human Resources og Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="31131-212">Númeraröðin þarf að vera einkvæm á báðum hliðum, svo að það verði engir árekstrar á heimilisföngum við samþættingu gagna frá Dataverse til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="31131-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Dataverse to Finance and Operations.</span></span>

<span data-ttu-id="31131-213">Við innleiðingu á Human Resources skal staðfesta að númeraraðirnar séu ekki þær sömu í Human Resources og Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="31131-214">Staðfestið að allar númeraraðir séu ekki eins þar sem gögn kunna að vera í báðum kerfum.</span><span class="sxs-lookup"><span data-stu-id="31131-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="31131-215">Þegar ég er bý til tengistillinguna mína, get ég ekki séð tenginguna í fellilista tengingarinnar.</span><span class="sxs-lookup"><span data-stu-id="31131-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="31131-216">Hvað geri ég?</span><span class="sxs-lookup"><span data-stu-id="31131-216">What do I do?</span></span>

<span data-ttu-id="31131-217">Gakktu úr skugga um að þegar þú býrð til tengingar velurðu Dynamics 365 Finance og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="31131-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Dataverse.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="31131-218">Við samstillingu starfsmanna fæ ég villurnar „CompanyInfo_FL er ekki til“ eða „Gildið '12/31/2154 11:59:59 pm‘ í reitnum „Lokadagur starfsmanns finnst ekki í tengdri töflu „Starfsmaður“.“ Hvað ætti ég að gera?</span><span class="sxs-lookup"><span data-stu-id="31131-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="31131-219">Gakktu úr skugga um að þú varpir í rétta lögaðila.</span><span class="sxs-lookup"><span data-stu-id="31131-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="31131-220">Samstilling lögaðila er ekki hluti af sjálfgefna sniðmátinu, þannig að það er gert ráð fyrir að hver lögaðili sem er til staðar í Human Resources og Dataverse sé einnig til staðar í Finance.</span><span class="sxs-lookup"><span data-stu-id="31131-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Dataverse is also present in Finance.</span></span>
<span data-ttu-id="31131-221">Gakktu einnig úr skugga um að þú veljir rétta lögaðila fyrir tengda tengistillingu.</span><span class="sxs-lookup"><span data-stu-id="31131-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="31131-222">Eftir að verkefnið var sett upp virðist vörpun reita fyrir Finance vera tóm.</span><span class="sxs-lookup"><span data-stu-id="31131-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="31131-223">Hvað ætti ég að gera?</span><span class="sxs-lookup"><span data-stu-id="31131-223">What should I do?</span></span>

<span data-ttu-id="31131-224">Uppfæra gagnaeiningarnar í Finance með því að fara í **Gagnastjórnun \> Færibreytur ramma \> Einingastillingar \> Uppfæra einingalista.**</span><span class="sxs-lookup"><span data-stu-id="31131-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="31131-225">Þetta ætti að taka nokkrar mínútur að klárast, síðan ættir þú að sjá þessar varpanir.</span><span class="sxs-lookup"><span data-stu-id="31131-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="31131-226">Þetta mál kemur upp þegar ný verkefni eru búin til.</span><span class="sxs-lookup"><span data-stu-id="31131-226">This issue occurs when new projects are created.</span></span>

![Vörpun reita vantar](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="31131-228">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="31131-228">Additional resources</span></span>

- <span data-ttu-id="31131-229">Data Integrator (DI):</span><span class="sxs-lookup"><span data-stu-id="31131-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="31131-230">Samþætta gögn í Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="31131-230">Integrate data into Microsoft Dataverse</span></span>](/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="31131-231">Villumeðhöndlun og úrræðaleit Data Integrator</span><span class="sxs-lookup"><span data-stu-id="31131-231">Data Integrator error management and troubleshooting</span></span>](/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="31131-232">Viðbrögð við DSR-beiðnum fyrir kerfismyndaða kladda í Power Apps, Microsoft Power Automate og Dataverse</span><span class="sxs-lookup"><span data-stu-id="31131-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Dataverse</span></span>](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="31131-233">Stjórnun gagna:</span><span class="sxs-lookup"><span data-stu-id="31131-233">Data Management:</span></span>

  - [<span data-ttu-id="31131-234">Gagnastjórnun</span><span class="sxs-lookup"><span data-stu-id="31131-234">Data management</span></span>](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
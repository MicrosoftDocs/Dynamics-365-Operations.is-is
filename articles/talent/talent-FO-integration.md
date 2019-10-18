---
title: Algengar spurningar um samþættingu Dynamics 365 Talent til Dynamics 365 Finance
description: Þetta efnisatriði útskýrir hvaða gögn eru samstillt í samþættingu á Talent og Finance.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251015"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="4bcef-103">Algengar spurningar um samþættingu Dynamics 365 Talent til Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="4bcef-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4bcef-104">Þetta efnisatriði svarar algengum spurningum sem tengjast gögnunum sem eru samstillt þegar Dynamics 365 Talent er samþætt við Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="4bcef-105">Eru öll gögn samstillt eða bara sumar gagnaeiningar?</span><span class="sxs-lookup"><span data-stu-id="4bcef-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="4bcef-106">Fyrir Core HR er undirsafn af gögnunum samstillt við.</span><span class="sxs-lookup"><span data-stu-id="4bcef-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="4bcef-107">Fyrir lista yfir allar einingarnar skal sjá [Samþætting frá Dynamics 365 Talent til Dynamics 365 Finance](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="4bcef-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="4bcef-108">Fyrir Attract og Onboard eru öll gögn staðbundin við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4bcef-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="4bcef-109">Get ég búið til nýja vörpun án þess að nota sniðmátin?</span><span class="sxs-lookup"><span data-stu-id="4bcef-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="4bcef-110">Sniðmát eru upphafspunktur.</span><span class="sxs-lookup"><span data-stu-id="4bcef-110">Templates are the starting point.</span></span> <span data-ttu-id="4bcef-111">Hægt er að búa til sitt eigið sniðmát, en alltaf er þörf á sniðmáti þegar samþættingarverk er búið til.</span><span class="sxs-lookup"><span data-stu-id="4bcef-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="4bcef-112">Nánari upplýsingar um Data Integrator (DI), sniðmát og verk er að finna í [Samþætta gögn í Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="4bcef-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="4bcef-113">Er hægt að varpa fjárhagsvíddum í flutning milli Talent og Finance?</span><span class="sxs-lookup"><span data-stu-id="4bcef-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="4bcef-114">Sem stendur eru fjárhagsvíddir ekki í Common Data Service og eru þar af leiðandi ekki hluti af sjálfgefna sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="4bcef-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="4bcef-115">Þessi eining er fyrirhuguð en engin tímalína útgáfu er til eins og er.</span><span class="sxs-lookup"><span data-stu-id="4bcef-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="4bcef-116">Fyrir gögn sem eru í Finance en eru ekki til í Talent, skal tengja kerfin tvö saman með **Skilgreina tengla** í Talent.</span><span class="sxs-lookup"><span data-stu-id="4bcef-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="4bcef-117">Nánari upplýsingar um hvernig á að skilgreina tengla milli Talent og Finance er að finna í [Hvað er nýtt eða breytt í Dynamics 365 Talent: Core HR (31. október 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="4bcef-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![Varpa fjárhagsvíddum](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="4bcef-119">Stundum þegar ég flyt inn starfsmenn fara þeir í óvirka starfskrafta í Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="4bcef-120">Af hverju?</span><span class="sxs-lookup"><span data-stu-id="4bcef-120">Why?</span></span>

<span data-ttu-id="4bcef-121">Þú gætir fengið þessa villu ef starfsmenn hafa ekki virka skrá með starfsupplýsingum í Talent.</span><span class="sxs-lookup"><span data-stu-id="4bcef-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="4bcef-122">Til að leysa þetta skal fara í **Starfsmannastjórnun \> Starfsmenn \> Starfsferill \> Stjórnun dagsetninga** og staðfesta að til sé virk skrá starfsupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="4bcef-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="4bcef-123">Ef ég vel að varpa eingöngu undirsafni af svæðum, munu breytingar sem gerðar eru á óvörpuðum reitum kveikja á samstillingu?</span><span class="sxs-lookup"><span data-stu-id="4bcef-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="4bcef-124">Samstilling gagna fylgir framkvæmdaráætlun.</span><span class="sxs-lookup"><span data-stu-id="4bcef-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="4bcef-125">Samþættingin mun taka upp skrá ef eitthvert svæði í skránni breytist óháð því hvort svæðið er hluti af samþættingu vörpunar.</span><span class="sxs-lookup"><span data-stu-id="4bcef-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="4bcef-126">Hvernig get ég sent einungis breytingar á virkum starfskrafti og ekki riftum skrám?</span><span class="sxs-lookup"><span data-stu-id="4bcef-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="4bcef-127">Með því að nota „Ítarleg fyrirspurn“ geturðu síað og mótað upprunagögn áður en þau eru send inn í staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="4bcef-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Ítarleg fyrirspurn virkra starfskrafta](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="4bcef-129">Get ég tilgreint hvaða svæði skal senda til Finance fyrir tiltekna einingu?</span><span class="sxs-lookup"><span data-stu-id="4bcef-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="4bcef-130">Hægt er að bæta við eða fjarlægja svæði úr samþættingarverkinu.</span><span class="sxs-lookup"><span data-stu-id="4bcef-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="4bcef-131">Ekki öll gagnasvæði sem til eru í einingu Common Data Service verða fylltir út frá Core HR.</span><span class="sxs-lookup"><span data-stu-id="4bcef-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="4bcef-132">Hægt er að fylla út viðbótargögn í gegnum PowerApps.</span><span class="sxs-lookup"><span data-stu-id="4bcef-132">Additional data can be populated via PowerApps.</span></span>

![Bæta við eða fjarlægja reiti í eða úr samþættingarverki](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="4bcef-134">Ég setti upp samþættingu sem runuvinnslu en Talent missti tengingu við kerfi áfangastaðar.</span><span class="sxs-lookup"><span data-stu-id="4bcef-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="4bcef-135">Hvernig get ég sent sama sett af breytingum til kerfi áfangastaðar?</span><span class="sxs-lookup"><span data-stu-id="4bcef-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="4bcef-136">Ekki er krafist sérstakrar uppsetningar fyrir meðhöndlun frávika.</span><span class="sxs-lookup"><span data-stu-id="4bcef-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="4bcef-137">Data Integrator mun sjálfkrafa grípa og tilkynna villur sem gerast hjá uppruna og áfangastað og mun leyfa handvirkar endurtekningar.</span><span class="sxs-lookup"><span data-stu-id="4bcef-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="4bcef-138">Hins vegar leyfir hún ekki handvirka gagnaleiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="4bcef-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="4bcef-139">Ef nauðsynlegt er að uppfæra gögn, þá ætti það að gerast annað hvort við uppruna eða áfangastað.</span><span class="sxs-lookup"><span data-stu-id="4bcef-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="4bcef-140">Get ég sett upp samþættingu í báðar áttir?</span><span class="sxs-lookup"><span data-stu-id="4bcef-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="4bcef-141">Nei, sem stendur er samþætting í aðra áttina (Talent til Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="4bcef-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="4bcef-142">Hins vegar er sjálfgefið sniðmát í boði til að senda gögn frá Talent til Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="4bcef-143">Get ég leyft skráareyðingu sem hluta af samþættingu minni?</span><span class="sxs-lookup"><span data-stu-id="4bcef-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="4bcef-144">Nei, Data Integrator mun ekki sækja eyddar færslur fyrir gagnaflutning.</span><span class="sxs-lookup"><span data-stu-id="4bcef-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="4bcef-145">Aðeins stofnun og uppfærslur á gögnum (UPSERT) eru innifaldar sem stendur.</span><span class="sxs-lookup"><span data-stu-id="4bcef-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="4bcef-146">Get ég keyrt aftur framkvæmd með villum?</span><span class="sxs-lookup"><span data-stu-id="4bcef-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="4bcef-147">Ef svo er, mun það senda heila skrá eða aðeins breytingarnar?</span><span class="sxs-lookup"><span data-stu-id="4bcef-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="4bcef-148">Fyrsta keyrsla Data Integrator er alltaf full keyrsla.</span><span class="sxs-lookup"><span data-stu-id="4bcef-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="4bcef-149">Næstu keyrslur byggjast á rakningu breytinga.</span><span class="sxs-lookup"><span data-stu-id="4bcef-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="4bcef-150">Við framkvæmd villukeyrslu eru færslurnar dregnar út samkvæmt umfangi keyrslunnar og nýjustu breytingar eru sendar út úr Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4bcef-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="4bcef-151">Þegar ég vista verkið fæ ég villuna: „Verk er með vörpunarvillur“.</span><span class="sxs-lookup"><span data-stu-id="4bcef-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="4bcef-152">Hvað geri ég?</span><span class="sxs-lookup"><span data-stu-id="4bcef-152">What do I do?</span></span>

<span data-ttu-id="4bcef-153">Athugaðu uppsetningu samþættingarlykla, gerðu nauðsynlegar breytingar á uppsetningunni og endurnýjaðu einingarnar í verkinu.</span><span class="sxs-lookup"><span data-stu-id="4bcef-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="4bcef-154">Þegar sjálfgefið sniðmát er notað verða samþættingarlyklarnir sjálfkrafa fluttir inn.</span><span class="sxs-lookup"><span data-stu-id="4bcef-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="4bcef-155">Þetta vandamál getur komið fram þegar nýjum verkum eru bætt við núverandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="4bcef-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="4bcef-156">Ef ég er með N fjölda lögaðila þar sem starfskraftar hafa vinnu, þarf ég að búa til vörpun fyrir hvern þeirra?</span><span class="sxs-lookup"><span data-stu-id="4bcef-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="4bcef-157">Já, fyrir hvern lögaðila í Finance þarf sérstakt samþættingarverk í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="4bcef-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="4bcef-158">Ég þarf að flytja gögn sem ekki eru hluti af sjálfgefna sniðmátinu sem Microsoft býður upp á.</span><span class="sxs-lookup"><span data-stu-id="4bcef-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="4bcef-159">Get ég gert þetta?</span><span class="sxs-lookup"><span data-stu-id="4bcef-159">Can I do this?</span></span>

<span data-ttu-id="4bcef-160">Já, hægt er að bæta við eða fjarlægja svæði úr núverandi sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="4bcef-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="4bcef-161">Sniðmátinu má breyta til að innihalda viðbótarupplýsingar úr öðrum einingum Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4bcef-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="4bcef-162">Einingin verður að vera í Common Data Service til að hún verði hluti af sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="4bcef-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="4bcef-163">Ég var að stofna ný umhverfi Finance og Talent og ég fæ villuna: „Gagnagildið brýtur hömlur fyrir heilleika.“</span><span class="sxs-lookup"><span data-stu-id="4bcef-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="4bcef-164">Af hverju?</span><span class="sxs-lookup"><span data-stu-id="4bcef-164">Why?</span></span>

<span data-ttu-id="4bcef-165">Ástæður þessarar villu geta falið í sér:</span><span class="sxs-lookup"><span data-stu-id="4bcef-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="4bcef-166">Gagnaflutningurinn leiddi til tvítekningar á gögnum sem voru dregin út úr upprunanum (Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="4bcef-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="4bcef-167">Gagnaflutningurinn hefur núll gildi fyrir svæði sem krafist er í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4bcef-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="4bcef-168">Staðfestu að gögnin sem eru í Common Data Service uppfylli kröfur Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4bcef-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="4bcef-169">Ef framkvæmdavillur koma upp og auðkenni starfsmanns samstilltist ekki, hvernig finn ég þá vinnsluferilinn sem inniheldur starfsmannafærsluna?</span><span class="sxs-lookup"><span data-stu-id="4bcef-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="4bcef-170">Data Integrator mun búa til mörg verk í Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="4bcef-171">Sambandið milli verks Data Integrator og verks Finance er einn á móti einum.</span><span class="sxs-lookup"><span data-stu-id="4bcef-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="4bcef-172">Rektu tímann frá framkvæmdaferil Data Integrator og leitaðu að vísinum -1 fyrir verk Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="4bcef-173">Ef verknúmerið er 9 í Data Integrator er vísirinn í Finance 8.</span><span class="sxs-lookup"><span data-stu-id="4bcef-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="4bcef-174">Sæktu vísi verksins úr Data Integrator (í þessu dæmi er hann „9“).</span><span class="sxs-lookup"><span data-stu-id="4bcef-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Sæktu vísi verks úr Data Integrator](media/CaptureTaskIndex.png)

2. <span data-ttu-id="4bcef-176">Rektu tíma framkvæmdar fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="4bcef-176">Track the execution time of the project.</span></span>

![Rektu tíma framkvæmdar fyrir verk](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="4bcef-178">Í Fjármálum skaltu bera kennsl á vísitölu - 1.</span><span class="sxs-lookup"><span data-stu-id="4bcef-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="4bcef-179">Í þessu dæmi passar verkið með viðskeytið „8“ og tíma framkvæmdar með vísi „0“ við tíma framkvæmdar í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="4bcef-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Auðkenna vísi](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="4bcef-181">Eftir að hafa samþætt Talent og Finance, sé ég ekki Talent-gögnin mín í Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="4bcef-182">Hvað geri ég?</span><span class="sxs-lookup"><span data-stu-id="4bcef-182">What do I do?</span></span>

<span data-ttu-id="4bcef-183">Samþættingin við Finance er ferli í tveimur skrefum.</span><span class="sxs-lookup"><span data-stu-id="4bcef-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="4bcef-184">Fyrst skaltu staðfesta að Talent-gögnin séu uppfærð og tiltæk í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4bcef-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="4bcef-185">Þetta er nærri því samstilling í rauntíma og hægt er að sannprófa hana í PowerApps með því að líta á gögnin innan gagnaeininganna.</span><span class="sxs-lookup"><span data-stu-id="4bcef-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Gögn í Common Data Service](media/DataInCDS.png)

<span data-ttu-id="4bcef-187">Ef gögnin birtast ekki eins og búist er við í Common Data Service skaltu staðfesta að einingin sé studd í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="4bcef-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="4bcef-188">Til að bæta við viðbótargögnum í Common Data Service verður breyting af hálfu Windows að gerast.</span><span class="sxs-lookup"><span data-stu-id="4bcef-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="4bcef-189">Ef einingin er studd og gögnin eru tiltæk í Common Data Service skaltu staðfesta að vörpunin sé rétt í Data Integrator.</span><span class="sxs-lookup"><span data-stu-id="4bcef-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="4bcef-190">Ef vörpun samþættingar lítur vel út skaltu staðfesta að keyrsla á vinnslum gagnastjórnunar hafi tekist.</span><span class="sxs-lookup"><span data-stu-id="4bcef-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="4bcef-191">Villur geta komið fram meðan á framkvæmd runuvinnslunnar stendur.</span><span class="sxs-lookup"><span data-stu-id="4bcef-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="4bcef-192">Nánari upplýsingar um stjórnun gagna er að finna í [Gagnastjórnun](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="4bcef-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="4bcef-193">Heimilisföngin fyrir starfsmennina mína eru rangar eftir að ég flyt þær inn í Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="4bcef-194">Hvað ætti ég að gera?</span><span class="sxs-lookup"><span data-stu-id="4bcef-194">What should I do?</span></span>

<span data-ttu-id="4bcef-195">Númeraröðin fyrir **Staðsetningarkenni** notar sama mynstur í bæði Talent og Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="4bcef-196">Númeraröðin þarf að vera einkvæm á báðum hliðum, svo að það verði engir árekstrar á heimilisföngum við samþættingu gagna frá Common Data Service til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4bcef-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="4bcef-197">Við innleiðingu á Talent skal staðfesta að númeraraðirnar séu ekki þær sömu í Talent og Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="4bcef-198">Staðfestið að allar númeraraðir séu ekki eins þar sem gögn kunna að vera í báðum kerfum.</span><span class="sxs-lookup"><span data-stu-id="4bcef-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="4bcef-199">Þegar ég er bý til tengistillinguna mína, get ég ekki séð tenginguna í fellilista tengingarinnar.</span><span class="sxs-lookup"><span data-stu-id="4bcef-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="4bcef-200">Hvað geri ég?</span><span class="sxs-lookup"><span data-stu-id="4bcef-200">What do I do?</span></span>

<span data-ttu-id="4bcef-201">Gakktu úr skugga um að þegar þú býrð til tengingar velurðu Dynamics 365 Finance og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4bcef-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="4bcef-202">Við samstillingu starfsmanna fæ ég villurnar „CompanyInfo_FL er ekki til“ eða „Gildið '12/31/2154 11:59:59 pm‘ í reitnum „Lokadagur starfsmanns finnst ekki í tengdri töflu „Starfsmaður“.“ Hvað ætti ég að gera?</span><span class="sxs-lookup"><span data-stu-id="4bcef-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="4bcef-203">Gakktu úr skugga um að þú varpir í rétta lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4bcef-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="4bcef-204">Samstilling lögaðila er ekki hluti af sjálfgefna sniðmátinu, þannig að það er gert ráð fyrir að hver lögaðili sem er til staðar í Talent og Common Data Service sé einnig til staðar í Finance.</span><span class="sxs-lookup"><span data-stu-id="4bcef-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="4bcef-205">Gakktu einnig úr skugga um að þú veljir rétta lögaðila fyrir tengda tengistillingu.</span><span class="sxs-lookup"><span data-stu-id="4bcef-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="4bcef-206">Eftir að verkefnið var sett upp virðist vörpun reita fyrir Finance vera tóm.</span><span class="sxs-lookup"><span data-stu-id="4bcef-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="4bcef-207">Hvað ætti ég að gera?</span><span class="sxs-lookup"><span data-stu-id="4bcef-207">What should I do?</span></span>

<span data-ttu-id="4bcef-208">Uppfæra gagnaeiningarnar í Finance með því að fara í **Gagnastjórnun \> Færibreytur ramma \> Einingastillingar \> Uppfæra einingalista.**</span><span class="sxs-lookup"><span data-stu-id="4bcef-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="4bcef-209">Þetta ætti að taka nokkrar mínútur að klárast, síðan ættir þú að sjá þessar varpanir.</span><span class="sxs-lookup"><span data-stu-id="4bcef-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="4bcef-210">Þetta mál kemur upp þegar ný verkefni eru búin til.</span><span class="sxs-lookup"><span data-stu-id="4bcef-210">This issue occurs when new projects are created.</span></span>

![Vörpun reita vantar](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="4bcef-212">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4bcef-212">Additional resources</span></span>

- <span data-ttu-id="4bcef-213">Data Integrator (DI):</span><span class="sxs-lookup"><span data-stu-id="4bcef-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="4bcef-214">Samþætta gögn í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4bcef-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="4bcef-215">Villumeðhöndlun og úrræðaleit Data Integrator</span><span class="sxs-lookup"><span data-stu-id="4bcef-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="4bcef-216">Viðbrögð við DSR-beiðnum fyrir kerfismyndaða kladda í PowerApps, Microsoft Flow og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4bcef-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="4bcef-217">Stjórnun gagna:</span><span class="sxs-lookup"><span data-stu-id="4bcef-217">Data Management:</span></span>

  - [<span data-ttu-id="4bcef-218">Gagnastjórnun</span><span class="sxs-lookup"><span data-stu-id="4bcef-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)

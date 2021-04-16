---
title: Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda
description: Í þessu efnisatriði er API-samþættingu Dynamics 365 Human Resources rakningakerfis umsækjanda (ATS) lýst.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 599f9728019cd6bc59c59a4f08df06c6c9c9ac31
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798418"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="d1c23-103">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="d1c23-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d1c23-104">Í þessu efnisatriði er API-samþættingu Dynamics 365 Human Resources rakningakerfis umsækjanda (ATS) lýst.</span><span class="sxs-lookup"><span data-stu-id="d1c23-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="d1c23-105">Ætlun API er að virkja einfalda samþættingu milli Dynamics 365 Human Resources og ATS samstarfsaðila.</span><span class="sxs-lookup"><span data-stu-id="d1c23-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![Samþættingarferli ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="d1c23-107">Samþætta upplifunin hefst í Human Resources þegar ráðningarstjóri stofnar ráðningarbeiðni.</span><span class="sxs-lookup"><span data-stu-id="d1c23-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="d1c23-108">Þegar beiðnin er virkjuð sækir ATS upplýsingar um beiðnina til að búa til ráðningarverk.</span><span class="sxs-lookup"><span data-stu-id="d1c23-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="d1c23-109">Síðan fylgir það ráðningarlínunni til að velja og ráða umsækjanda fyrir stöðuna/stöðurnar.</span><span class="sxs-lookup"><span data-stu-id="d1c23-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="d1c23-110">Að lokum lýkur ATS samþættingarferlinu með því að senda valda færslu umsækjanda inn í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d1c23-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="d1c23-111">Færsla umsækjanda getur þá farið í gegnum fleiri villuleitir innleiðingar og verkferla til að búa til starfsmannsfærsluna.</span><span class="sxs-lookup"><span data-stu-id="d1c23-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="d1c23-112">Til að virkja samþættinguna hefur Human Resources bætt við eftirfarandi hlutum:</span><span class="sxs-lookup"><span data-stu-id="d1c23-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="d1c23-113">Virkni til að stofna ráðningarbeiðni.</span><span class="sxs-lookup"><span data-stu-id="d1c23-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="d1c23-114">Útvíkkaðar notandaupplýsingar umsækjanda og tengdir verkferlar.</span><span class="sxs-lookup"><span data-stu-id="d1c23-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="d1c23-115">API-samþætting sem opnar nýju virknina til að samþætta forrit.</span><span class="sxs-lookup"><span data-stu-id="d1c23-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="d1c23-116">Frekari upplýsingar um uppsetningu og notkun ráðningarbeiðni og virkni umsækjanda er að finna í [Ráða umsækjendur](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="d1c23-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="d1c23-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="d1c23-117">Microsoft Dataverse</span></span>

<span data-ttu-id="d1c23-118">Þetta API er byggt á Microsoft Dataverse (áður Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="d1c23-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="d1c23-119">Öll RESTful-samþætting við þetta API er gert í gegnum Microsoft Dataverse vef-API sem notar OData.</span><span class="sxs-lookup"><span data-stu-id="d1c23-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="d1c23-120">Þetta API er undirsafn Dataverse vef-API.</span><span class="sxs-lookup"><span data-stu-id="d1c23-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="d1c23-121">Dataverse Vef-API skilgreinir einkenni á borð við auðkenningu, þjónustustigssamninga, runu, samvinnslustýringu og villumeðhöndlun.</span><span class="sxs-lookup"><span data-stu-id="d1c23-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="d1c23-122">Til að fá frekari almennar upplýsingar um Microsoft Dataverse vef-API skal sjá:</span><span class="sxs-lookup"><span data-stu-id="d1c23-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="d1c23-123">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="d1c23-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="d1c23-124">Nota Microsoft Dataverse vef-API</span><span class="sxs-lookup"><span data-stu-id="d1c23-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="d1c23-125">Microsoft Dataverse leiðbeiningar þróunaraðila</span><span class="sxs-lookup"><span data-stu-id="d1c23-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="d1c23-126">Ofangreind fylgigögn innihalda upplýsingar og leiðbeiningar þróunaraðila um notkun á Dataverse vef-API, svo sem [stjórnun sannvottunar](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [framkvæmd aðgerða](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [notkun Postman með API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) og [notkun breytingarrakningar eða Delta-tákns](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) með API.</span><span class="sxs-lookup"><span data-stu-id="d1c23-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="d1c23-127">Safn valkosta</span><span class="sxs-lookup"><span data-stu-id="d1c23-127">Option sets</span></span>

<span data-ttu-id="d1c23-128">Gagnalíkanið fyrir API-samþættingu ATS sem lýst er í þessu skjali inniheldur safn valkosta sem bjóða upp á númeruð gildi sem tengjast eiginleikum einingar.</span><span class="sxs-lookup"><span data-stu-id="d1c23-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="d1c23-129">Frekari upplýsingar um hvernig nota skuli safn valkosta í Dataverse vef-API er að finna í [Búa til og uppfæra safn valkosta með vef-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="d1c23-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="d1c23-130">Safn valkosta er skilgreint fyrir hvert Dataverse-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="d1c23-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="d1c23-131">Sýndartöflur fyrir Human Resources í Dataverse</span><span class="sxs-lookup"><span data-stu-id="d1c23-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="d1c23-132">Endastöðvar fyrir API-Samþætting ATS nota verkvangsmöguleika sýndartöflunnnar fyrir Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d1c23-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="d1c23-133">Sjálfgefið er að sýndartöflurnar og tengdu API-endastöðvarnar þeirra eru ekki uppsettar fyrir umhverfi Human Resources sem gerir fyrirtækjum kleift að ákveða hvaða OData-endastöðvar verða notaðar í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="d1c23-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="d1c23-134">Til að nota API þarf að mynda sýndartöflur fyrir einingar Human Resources fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="d1c23-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="d1c23-135">Frekari upplýsingar um myndun sýndartaflna fyrir API er að finna í [Skilgreina Dataverse sýndartöflur](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="d1c23-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="d1c23-136">Gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="d1c23-136">Data model</span></span>

<span data-ttu-id="d1c23-137">Gagnalíkanið miðast við tvær aðaleiningar:</span><span class="sxs-lookup"><span data-stu-id="d1c23-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="d1c23-138">**RecruitingRequest** stendur fyrir beiðni til ATS um að ráða í eina eða fleiri lausar stöður. Dæmi um fyrirspurn er að finna í [Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="d1c23-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="d1c23-139">**CandidateToHire** sýnir upplýsingar um umsækjanda sem hefur samþykkt boð um stöðu.</span><span class="sxs-lookup"><span data-stu-id="d1c23-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="d1c23-140">**Einstaklingur** stendur fyrir einstaklinginn sem er umsækjandinn.</span><span class="sxs-lookup"><span data-stu-id="d1c23-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="d1c23-141">Einstaklingur getur haft mörg hlutverk í fyrirtækinu, t.d. umsækjandi, starfskraftur, starfsmaður eða verktaki.</span><span class="sxs-lookup"><span data-stu-id="d1c23-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="d1c23-142">Dæmi um fyrirspurn er að finna í [Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="d1c23-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="d1c23-143">Eftirfarandi skýringarmynd sýnir vensl innan API.</span><span class="sxs-lookup"><span data-stu-id="d1c23-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="d1c23-144">Nokkrar gerðir eru með ytri lykla fyrir aðrar fyrirliggjandi einingar í Human Resources sem ekki eru sýndar hér.</span><span class="sxs-lookup"><span data-stu-id="d1c23-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="d1c23-145">Í þessu skjali eru upplýsingar um einingar sem eiga sérstaklega við samþættingaraðstæður ráðningar.</span><span class="sxs-lookup"><span data-stu-id="d1c23-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="d1c23-146">Hins vegar eru margar aðrar einingar í Dataverse vef-API fyrir Dynamics 365 Human Resources sem kunna einnig að skipta máli fyrir samþættingu þína.</span><span class="sxs-lookup"><span data-stu-id="d1c23-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="d1c23-147">Til dæmis gæti einnig þurft upplýsingar fyrir starfsmenn, störf, stöður eða aðrar einingar sem ekki eru skilgreindar hér.</span><span class="sxs-lookup"><span data-stu-id="d1c23-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="d1c23-148">Vísað er í margar þessara eininga í tengslum ytri lykla eða skoðunareiginleikum.</span><span class="sxs-lookup"><span data-stu-id="d1c23-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Gagnalíkan API-samþættingar ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="d1c23-150">Ráðningarbeiðni og tengdar einingar og söfn valkosta</span><span class="sxs-lookup"><span data-stu-id="d1c23-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="d1c23-151">Dæmi um fyrirspurn:</span><span class="sxs-lookup"><span data-stu-id="d1c23-151">Example query:</span></span> 

- [<span data-ttu-id="d1c23-152">Dæmi um fyrirspurn fyrir ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="d1c23-153">Einingar:</span><span class="sxs-lookup"><span data-stu-id="d1c23-153">Entities:</span></span>

- [<span data-ttu-id="d1c23-154">Ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="d1c23-155">Staða í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="d1c23-156">Færni í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="d1c23-157">Menntun í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="d1c23-158">Staðsetning í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="d1c23-159">Safn valkosta:</span><span class="sxs-lookup"><span data-stu-id="d1c23-159">Option sets:</span></span>

- [<span data-ttu-id="d1c23-160">Undanþágustaða starfs</span><span class="sxs-lookup"><span data-stu-id="d1c23-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="d1c23-161">Staða starfs í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="d1c23-162">Staða í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="d1c23-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="d1c23-163">Flokkur stjórnunarstarfs</span><span class="sxs-lookup"><span data-stu-id="d1c23-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="d1c23-164">Umsækjendur til að ráða og tengdar einingar og söfn valkosta</span><span class="sxs-lookup"><span data-stu-id="d1c23-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="d1c23-165">Dæmi um fyrirspurn:</span><span class="sxs-lookup"><span data-stu-id="d1c23-165">Example query:</span></span>

- [<span data-ttu-id="d1c23-166">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="d1c23-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="d1c23-167">Einingar:</span><span class="sxs-lookup"><span data-stu-id="d1c23-167">Entities:</span></span>

- [<span data-ttu-id="d1c23-168">Umsækjandi til að ráða</span><span class="sxs-lookup"><span data-stu-id="d1c23-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="d1c23-169">Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="d1c23-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="d1c23-170">Menntun einstaklings</span><span class="sxs-lookup"><span data-stu-id="d1c23-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="d1c23-171">Starfsreynsla einstaklings</span><span class="sxs-lookup"><span data-stu-id="d1c23-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="d1c23-172">Aðsetur einstaklings</span><span class="sxs-lookup"><span data-stu-id="d1c23-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="d1c23-173">Tengiliður aðila</span><span class="sxs-lookup"><span data-stu-id="d1c23-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="d1c23-174">Hæfni einstaklings</span><span class="sxs-lookup"><span data-stu-id="d1c23-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="d1c23-175">Matsstig</span><span class="sxs-lookup"><span data-stu-id="d1c23-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="d1c23-176">Skírteini einstaklings</span><span class="sxs-lookup"><span data-stu-id="d1c23-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="d1c23-177">Gerð skírteinis</span><span class="sxs-lookup"><span data-stu-id="d1c23-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="d1c23-178">Skoðun einstaklings</span><span class="sxs-lookup"><span data-stu-id="d1c23-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="d1c23-179">Skoðunargerðir</span><span class="sxs-lookup"><span data-stu-id="d1c23-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="d1c23-180">Kennitala einstaklings</span><span class="sxs-lookup"><span data-stu-id="d1c23-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="d1c23-181">Safn valkosta:</span><span class="sxs-lookup"><span data-stu-id="d1c23-181">Option sets:</span></span>

- [<span data-ttu-id="d1c23-182">Niðurstöður samþættingar umsækjanda</span><span class="sxs-lookup"><span data-stu-id="d1c23-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="d1c23-183">Autt Já Nei</span><span class="sxs-lookup"><span data-stu-id="d1c23-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="d1c23-184">Staða á lokið</span><span class="sxs-lookup"><span data-stu-id="d1c23-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="d1c23-185">Gerð tengiliðar</span><span class="sxs-lookup"><span data-stu-id="d1c23-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="d1c23-186">Einingagrunnur menntunar</span><span class="sxs-lookup"><span data-stu-id="d1c23-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="d1c23-187">Kyn</span><span class="sxs-lookup"><span data-stu-id="d1c23-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="d1c23-188">Hjúskaparstaða</span><span class="sxs-lookup"><span data-stu-id="d1c23-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="d1c23-189">Mánuðir árs</span><span class="sxs-lookup"><span data-stu-id="d1c23-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="d1c23-190">Nei Já</span><span class="sxs-lookup"><span data-stu-id="d1c23-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="d1c23-191">Tímabilseining</span><span class="sxs-lookup"><span data-stu-id="d1c23-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="d1c23-192">Tíðni skoðunar</span><span class="sxs-lookup"><span data-stu-id="d1c23-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="d1c23-193">Tíðni skoðunar mynduð úr</span><span class="sxs-lookup"><span data-stu-id="d1c23-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="d1c23-194">Gerð hæfnisstig</span><span class="sxs-lookup"><span data-stu-id="d1c23-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="d1c23-195">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d1c23-195">See also</span></span>

[<span data-ttu-id="d1c23-196">Ráða umsækjendur</span><span class="sxs-lookup"><span data-stu-id="d1c23-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="d1c23-197">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="d1c23-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="d1c23-198">Nota Microsoft Dataverse vef-API</span><span class="sxs-lookup"><span data-stu-id="d1c23-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="d1c23-199">Búa til og uppfæra söfn valkosta með vef-API</span><span class="sxs-lookup"><span data-stu-id="d1c23-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
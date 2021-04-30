---
title: Kynning á API launasamþættingar
description: Þetta efnisatriði lýsir API Dynamics 365 Human Resources launasamþættingar.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61b90c566325bb8d83b09fceebc721cfb14d3fc8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891127"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="772be-103">Kynning á API launasamþættingar</span><span class="sxs-lookup"><span data-stu-id="772be-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="772be-104">Þetta skjal lýsir API Dynamics 365 Human Resources launasamþættingar.</span><span class="sxs-lookup"><span data-stu-id="772be-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="772be-105">API virkjar einfaldaða heildarsamþættingu á milli Human Resources og launakerfa samstarfsaðila.</span><span class="sxs-lookup"><span data-stu-id="772be-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="772be-106">Samþætta upplifunin hefst í Human Resources með upplýsingar um forstillingu starfsmanns, laun og frádrátt og framlag.</span><span class="sxs-lookup"><span data-stu-id="772be-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="772be-107">Þegar starfsmaður er ráðinn og færðar er inn nauðsynleg forstilling og launaupplýsingar í Human Resources, sækir launakerfið þessar upplýsingar til að nota þegar unnið er úr launum.</span><span class="sxs-lookup"><span data-stu-id="772be-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="772be-108">Allar uppfærslur sem gerðar eru á upplýsingum um starfsmann eða laun eru einnig sóttar til að nota í síðari launakeyrslum.</span><span class="sxs-lookup"><span data-stu-id="772be-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Flæði launasamþættingar](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="772be-110">Til að virkja samþættinguna hefur Human Resources bætt við eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="772be-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="772be-111">Virkni til að merkja starfsmann sem tilbúinn til greiðslu</span><span class="sxs-lookup"><span data-stu-id="772be-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="772be-112">API-samþætting sem opnar nýju virknina til að samþætta forrit</span><span class="sxs-lookup"><span data-stu-id="772be-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="772be-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="772be-113">Microsoft Dataverse</span></span>

<span data-ttu-id="772be-114">Þetta API er byggt á Microsoft Dataverse (áður Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="772be-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="772be-115">Öll RESTful-samþætting við þetta API er gert í gegnum Microsoft Dataverse vef-API sem notar OData.</span><span class="sxs-lookup"><span data-stu-id="772be-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="772be-116">Þetta API er undirsafn Dataverse vef-API.</span><span class="sxs-lookup"><span data-stu-id="772be-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="772be-117">Dataverse Vef-API skilgreinir einkenni á borð við auðkenningu, þjónustustigssamninga, runu, samvinnslustýringu og villumeðhöndlun.</span><span class="sxs-lookup"><span data-stu-id="772be-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="772be-118">Til að fá frekari almennar upplýsingar um Microsoft Dataverse vef-API skal sjá:</span><span class="sxs-lookup"><span data-stu-id="772be-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="772be-119">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="772be-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="772be-120">Nota Microsoft Dataverse vef-API</span><span class="sxs-lookup"><span data-stu-id="772be-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="772be-121">Microsoft Dataverse leiðbeiningar þróunaraðila</span><span class="sxs-lookup"><span data-stu-id="772be-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="772be-122">Þessi fylgigögn innihalda nánari upplýsingar og leiðbeiningar þróunaraðila til að nota Dataverse vef API, þ.m.t. eftirfarandi efnisatriði:</span><span class="sxs-lookup"><span data-stu-id="772be-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="772be-123">Sannvotta fyrir Microsoft Dataverse með vef-API</span><span class="sxs-lookup"><span data-stu-id="772be-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="772be-124">Framkvæma aðgerðir með vef-API</span><span class="sxs-lookup"><span data-stu-id="772be-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="772be-125">Nota Postman með vef-API</span><span class="sxs-lookup"><span data-stu-id="772be-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="772be-126">Nota breytingarrakningu til að samstilla gögn við ytri kerfi</span><span class="sxs-lookup"><span data-stu-id="772be-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="772be-127">Sýndartöflur fyrir Human Resources í Dataverse</span><span class="sxs-lookup"><span data-stu-id="772be-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="772be-128">Endastöðvar fyrir API-samþættingu launa nota verkvangsmöguleika sýndartöflunnnar fyrir Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="772be-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="772be-129">Sjálfgefið er að sýndartöflurnar og tengdu API-endastöðvarnar þeirra eru ekki uppsettar fyrir umhverfi Human Resources sem gerir fyrirtækjum kleift að ákveða hvaða OData-endastöðvar verða notaðar í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="772be-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="772be-130">Til að nota API þarf að mynda sýndartöflur fyrir einingar Human Resources fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="772be-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="772be-131">Frekari upplýsingar um myndun sýndartaflna fyrir API er að finna í [Skilgreina Dataverse sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="772be-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="772be-132">Gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="772be-132">Data model</span></span>

<span data-ttu-id="772be-133">Eftirfarandi skýringarmynd sýnir vensl innan API.</span><span class="sxs-lookup"><span data-stu-id="772be-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="772be-134">Nokkrar gerðir eru með ytri lykla fyrir aðrar fyrirliggjandi einingar í Human Resources sem ekki eru sýndar hér.</span><span class="sxs-lookup"><span data-stu-id="772be-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="772be-135">Í þessu skjali eru upplýsingar um einingar sem eiga sérstaklega við samþættingaraðstæður launa.</span><span class="sxs-lookup"><span data-stu-id="772be-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="772be-136">Hins vegar eru margar aðrar einingar í Dataverse vef-API fyrir Human Resources sem kunna einnig að skipta máli fyrir samþættingu þína.</span><span class="sxs-lookup"><span data-stu-id="772be-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="772be-137">Vísað er í sumar þessara eininga í tengslum ytri lykla eða skoðunareiginleikum.</span><span class="sxs-lookup"><span data-stu-id="772be-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Gagnalíkan API-samþættingar launa](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="772be-139">Starfsmaður á launaskrá og tengdar einingar</span><span class="sxs-lookup"><span data-stu-id="772be-139">Payroll employee and related entities</span></span>

<span data-ttu-id="772be-140">Einingar:</span><span class="sxs-lookup"><span data-stu-id="772be-140">Entities:</span></span>

- [<span data-ttu-id="772be-141">Starfsmaður á launaskrá</span><span class="sxs-lookup"><span data-stu-id="772be-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="772be-142">Heimilisfang starfskrafts á launaskrá</span><span class="sxs-lookup"><span data-stu-id="772be-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="772be-143">Launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="772be-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="772be-144">Launastöðuvinnsla</span><span class="sxs-lookup"><span data-stu-id="772be-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="772be-145">Launastaða</span><span class="sxs-lookup"><span data-stu-id="772be-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="772be-146">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="772be-146">See also</span></span>

[<span data-ttu-id="772be-147">Mynda og yfirfara launaaðila</span><span class="sxs-lookup"><span data-stu-id="772be-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="772be-148">Grunnstilla færibreytur Human Resources</span><span class="sxs-lookup"><span data-stu-id="772be-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="772be-149">Grunnstilla samnýttar færibreytur Human Resources</span><span class="sxs-lookup"><span data-stu-id="772be-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="772be-150">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="772be-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="772be-151">Nota Microsoft Dataverse vef-API</span><span class="sxs-lookup"><span data-stu-id="772be-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
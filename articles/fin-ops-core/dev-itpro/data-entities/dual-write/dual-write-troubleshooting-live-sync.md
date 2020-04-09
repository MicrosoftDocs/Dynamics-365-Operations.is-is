---
title: Úrræðaleit í beinni samstillingarvandamál
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með beinni samstillingu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 60839bbd1b3ae642cdd419c7df2388292776a461
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172738"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="25d73-103">Úrræðaleit í beinni samstillingarvandamál</span><span class="sxs-lookup"><span data-stu-id="25d73-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="25d73-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="25d73-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="25d73-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með beinni samstillingu.</span><span class="sxs-lookup"><span data-stu-id="25d73-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25d73-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="25d73-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="25d73-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="25d73-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="25d73-108">Lifandi samstilling kastar 403 Forbidden villa þegar þú býrð til skrá í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="25d73-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="25d73-109">Þú gætir fengið eftirfarandi villuboð þegar þú stofnar skrá í forriti Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="25d73-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="25d73-110">*\[{\\"villa\\":{\\"kóði\\":\\"0x80072560\\",\\"skilaboð\\":\\"Notandinn er ekki meðlimur í fyrirtækinu.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span><span class="sxs-lookup"><span data-stu-id="25d73-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="25d73-111">Til að laga vandann fylgirðu skrefunum í [Kerfiskröfur og forsendur](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="25d73-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="25d73-112">Til að ljúka þessum skrefum verða notendur tvískiptra forrita sem eru búnir til í Common Data Service að hafa kerfisstjórarhlutverkið.</span><span class="sxs-lookup"><span data-stu-id="25d73-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="25d73-113">Sjálfgefið eigendateymi verður einnig að hafa kerfisstjórarhlutverkið.</span><span class="sxs-lookup"><span data-stu-id="25d73-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="25d73-114">Lifandi samstilling fyrir einingu sýnir stöðugt svipaða villu þegar þú býrð til skrá í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="25d73-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="25d73-115">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="25d73-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="25d73-116">Þú gætir fengið villuboð eins og eftirfarandi í hvert skipti sem þú reynir að vista gögn um einingar í forriti Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="25d73-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="25d73-117">*Ekki hægt að vista breytingarnar í gagnagrunninum. Vinnueining getur ekki gert færslu. Ekki er hægt að skrifa gögn í mælieiningar einingar. Skrifun í UnitOfMeasureEntity mistókst með villuboðin Ekki var hægt að samstilla við mælieiningar einingar.*</span><span class="sxs-lookup"><span data-stu-id="25d73-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="25d73-118">Til að laga málið verður þú að ganga úr skugga um að forsendur tilvísunargagna séu til í bæði forriti Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="25d73-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="25d73-119">Til dæmis ef viðskiptavinurinn sem þú ert í forriti Finance and Operations tilheyrir ákveðnum viðskiptavinahópi skaltu ganga úr skugga um að viðskiptavinahópurinn sé til í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="25d73-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="25d73-120">Fylgdu þessum skrefum ef gögn eru til af báðum hliðum og þú hefur staðfest að málið er ekki gagnatengt.</span><span class="sxs-lookup"><span data-stu-id="25d73-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="25d73-121">Stöðvaðu tengda einingu.</span><span class="sxs-lookup"><span data-stu-id="25d73-121">Stop the related entity.</span></span>
2. <span data-ttu-id="25d73-122">Skráðu þig inn í forrit Finance and Operations og passaðu að skrár fyrir eininguna sem mistekst séu til í töflunum DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="25d73-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="25d73-123">Hér er til dæmis hvernig fyrirspurnin lítur út ef einingin **Viðskiptavinir** er að mistakast.</span><span class="sxs-lookup"><span data-stu-id="25d73-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="25d73-124">Ef það eru skrár fyrir eininguna sem fellur ekki út jafnvel eftir að þú hættir vörpunar einingarinnar skaltu eyða þeim gögnum sem tengjast einingunni sem mistakast.</span><span class="sxs-lookup"><span data-stu-id="25d73-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="25d73-125">Gerðu athugasemd við dálkinn **projectname** í DualWriteProjectConfiguration töflunni og sæktu færsluna í DualWriteProjectFieldConfiguration töfluna með því að nota verkefnisheitið til að eyða skránni.</span><span class="sxs-lookup"><span data-stu-id="25d73-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="25d73-126">Hefja vörpun einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="25d73-126">Start the entity mapping.</span></span> <span data-ttu-id="25d73-127">Staðfestu hvort gögnin séu samstillt án nokkurra vandamála.</span><span class="sxs-lookup"><span data-stu-id="25d73-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="25d73-128">Meðhöndla villur til að lesa eða skrifa réttindi þegar þú býrð til gögn í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="25d73-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="25d73-129">Þú gætir fengið villuboð „Slæm beiðni“ sem líkjast eftirfarandi dæmi þegar þú býrð til gögn í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25d73-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Dæmi um villuboðin Bad Request](media/error_record_id_source.png)

<span data-ttu-id="25d73-131">Til að laga málið verður þú að úthluta réttu öryggishlutverki til teymis kortlagða Dynamics 365 Sales eða Dynamics 365 Customer Service til að gera það sem vantar réttindi.</span><span class="sxs-lookup"><span data-stu-id="25d73-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="25d73-132">Í forriti Finance and Operations finnurðu viðskiptaeininguna sem er varpað í gagnasamsetningar tengingarsettinu.</span><span class="sxs-lookup"><span data-stu-id="25d73-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Fyrirtækjavörpun](media/mapped_business_unit.png)

2. <span data-ttu-id="25d73-134">Skráðu þig inn í umhverfið í líkanadrifna forritinu í Dynamics 365, farðu í **Stilling \> Öryggi** og finndu hóp varpaðrar viðskiptaeiningar.</span><span class="sxs-lookup"><span data-stu-id="25d73-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Hópur varpaðrar viðskiptaeiningar](media/setting_security_page.png)

3. <span data-ttu-id="25d73-136">Opnaðu síðuna fyrir hópinn sem á að breyta og veldu síðan **Stjórna hlutverkum** til að opna valmyndina **Stjórna hóphlutverkum**.</span><span class="sxs-lookup"><span data-stu-id="25d73-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Hnappurinn Stjórna hlutverkum](media/manage_team_roles.png)

4. <span data-ttu-id="25d73-138">Úthlutaðu hlutverkinu sem hefur lestrar-/skriftarréttindi fyrir viðkomandi einingar og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="25d73-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="25d73-139">Laga samstillingarvandamál í umhverfi sem er með nýlega breytt Common Data Service umhverfi</span><span class="sxs-lookup"><span data-stu-id="25d73-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="25d73-140">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="25d73-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="25d73-141">Þú gætir fengið eftirfarandi villuboð þegar þú stofnar gögn í forriti Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="25d73-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="25d73-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Ekki tókst að mynda farm fyrir eininguna CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Stofnun farms tókst ekki með villunni Ógilt URI: URI er tómt."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="25d73-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="25d73-143">Svona lítur villan út í líkanadrifnu forritinu í Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="25d73-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="25d73-144">*Óvænt villa kom upp úr ISV kóða. (ErrorType = ClientError) Óvænt undantekning frá viðbót (Framkvæmd): Microsoft.Dynamics.Integrator.CrmPlugins.Plugin: System.Exception: tókst ekki að vinna úr einingareikningi - (Tengingartilraun mistókst vegna þess að tengdur aðili svaraði ekki almennilega eftir a tíma eða komið var á fót tengingu vegna þess að tengdur gestgjafi hefur ekki svarað*</span><span class="sxs-lookup"><span data-stu-id="25d73-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.CrmPlugins.Plugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="25d73-145">Þessi villa kemur upp þegar Common Data Service umhverfi er rangt endurstillt á sama tíma og þú reynir að búa til gögn í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25d73-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="25d73-146">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="25d73-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="25d73-147">Skráðu þig inn á Finance and Operations sýndarvél (VM), opnaðu SQL Server Management Studio (SSMS) og leitaðu að gögnum í DUALWRITEPROJECTCONFIGURATIONENTITY töflunni þar sem **internalentityname** jafngildir **Viðskiptavinir V3** og **externalentityname** jafngildir **reikningar**.</span><span class="sxs-lookup"><span data-stu-id="25d73-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="25d73-148">Hér er hvernig fyrirspurnin lítur út.</span><span class="sxs-lookup"><span data-stu-id="25d73-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="25d73-149">Notaðu heiti verkefnisins úr niðurstöðum fyrri fyrirspurnar til að keyra eftirfarandi fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="25d73-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="25d73-150">Gakktu úr skugga um að dálkurinn **externalenvironmentURL** sé með rétt Common Data Service eða forritsslóð.</span><span class="sxs-lookup"><span data-stu-id="25d73-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="25d73-151">Eyða afritaskrám sem benda á ranga Common Data Service vefslóð.</span><span class="sxs-lookup"><span data-stu-id="25d73-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="25d73-152">Eyða samsvarandi gögnum í DUALWRITEPROJECTFIELDCONFIGURATION og DUALWRITEPROJECTCONFIGURATION töflunum.</span><span class="sxs-lookup"><span data-stu-id="25d73-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="25d73-153">Hættu að varpa einingunni og endurræstu hana síðan</span><span class="sxs-lookup"><span data-stu-id="25d73-153">Stop the entity mapping, and then restart it</span></span>

---
title: Úrræðaleit í beinni samstillingarvandamál
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með beinni samstillingu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b40b71eb45ae5a95a732c9554356afcddecb750e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566814"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="a5c1f-103">Úrræðaleit í beinni samstillingarvandamál</span><span class="sxs-lookup"><span data-stu-id="a5c1f-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="a5c1f-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="a5c1f-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með beinni samstillingu.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5c1f-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a5c1f-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="a5c1f-108">Samstilling í beinni veldur 403 Bannvillu þegar lína er stofnuð í Finance and Operations -forriti</span><span class="sxs-lookup"><span data-stu-id="a5c1f-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="a5c1f-109">Eftirfarandi villuboð kunna að birtast þegar lína er stofnuð í Finance and Operations forriti:</span><span class="sxs-lookup"><span data-stu-id="a5c1f-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="a5c1f-110">*\[{\\"villa\\":{\\"kóði\\":\\"0x80072560\\",\\"skilaboð\\":\\"Notandinn er ekki meðlimur í fyrirtækinu.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span><span class="sxs-lookup"><span data-stu-id="a5c1f-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="a5c1f-111">Til að laga vandann fylgirðu skrefunum í [Kerfiskröfur og forsendur](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="a5c1f-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="a5c1f-112">Til að ljúka þessum skrefum verða notendur tvískiptra forrita sem eru búnir til í Dataverse að hafa kerfisstjórarhlutverkið.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="a5c1f-113">Sjálfgefið eigendateymi verður einnig að hafa kerfisstjórarhlutverkið.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="a5c1f-114">Samstilling í beinni fyrir sérhverja töflu veldur svipaðri villu þegar lína er stofnuð í Finance and Operations -forriti</span><span class="sxs-lookup"><span data-stu-id="a5c1f-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="a5c1f-115">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a5c1f-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="a5c1f-116">Þú gætir fengið villuboð eins og eftirfarandi í hvert skipti sem þú reynir að töflugögn um einingar í forriti Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a5c1f-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="a5c1f-117">*Ekki hægt að vista breytingarnar í gagnagrunninum. Vinnueining getur ekki gert færslu. Ekki er hægt að skrifa gögn í mælieiningar einingar. Skrifun í UnitOfMeasureEntity mistókst með villuboðin Ekki var hægt að samstilla við mælieiningar einingar.*</span><span class="sxs-lookup"><span data-stu-id="a5c1f-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="a5c1f-118">Til að laga málið verður þú að ganga úr skugga um að forsendur tilvísunargagna séu til í bæði forriti Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="a5c1f-119">Til dæmis ef viðskiptavinurinn sem þú ert í forriti Finance and Operations tilheyrir ákveðnum viðskiptavinahópi skaltu ganga úr skugga um að viðskiptavinahópurinn sé til í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="a5c1f-120">Fylgdu þessum skrefum ef gögn eru til af báðum hliðum og þú hefur staðfest að málið er ekki gagnatengt.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="a5c1f-121">Stöðvaðu tengda töflu.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-121">Stop the related table.</span></span>
2. <span data-ttu-id="a5c1f-122">Skráðu þig inn í Finance and Operations -forritið og gakktu úr skugga um að línur töflunnar sem mistókst séu til staðar í DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration töflunum.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="a5c1f-123">Hér er til dæmis hvernig fyrirspurnin lítur út ef taflan **Viðskiptavinir** er að mistakast.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="a5c1f-124">Ef línur eru til staðar fyrir eininguna sem mistókst, jafnvel eftir að töfluvörpun er stöðvuð, skal eyða línunum sem tengjast töflunni sem mistókst.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="a5c1f-125">Gera skal athugasemd við dálkinn **projectname** í töflunni DualWriteProjectConfiguration og sækja línuna í DualWriteProjectFieldConfiguration töfluna með því að nota verkheitið til að eyða línunni.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="a5c1f-126">Hefja töfluvörpun.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-126">Start the table mapping.</span></span> <span data-ttu-id="a5c1f-127">Staðfestu hvort gögnin séu samstillt án nokkurra vandamála.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="a5c1f-128">Meðhöndla villur til að lesa eða skrifa réttindi þegar þú býrð til gögn í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5c1f-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="a5c1f-129">Þú gætir fengið villuboð „Slæm beiðni“ sem líkjast eftirfarandi dæmi þegar þú býrð til gögn í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Dæmi um villuboðin Bad Request](media/error_record_id_source.png)

<span data-ttu-id="a5c1f-131">Til að laga málið verður þú að úthluta réttu öryggishlutverki til teymis kortlagða Dynamics 365 Sales eða Dynamics 365 Customer Service til að gera það sem vantar réttindi.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="a5c1f-132">Í forriti Finance and Operations finnurðu viðskiptaeininguna sem er varpað í gagnasamsetningar tengingarsettinu.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Fyrirtækjavörpun](media/mapped_business_unit.png)

2. <span data-ttu-id="a5c1f-134">Skráðu þig inn í umhverfið í líkanadrifna forritinu í Dynamics 365, farðu í **Stilling \> Öryggi** og finndu hóp varpaðrar viðskiptaeiningar.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Hópur varpaðrar viðskiptaeiningar](media/setting_security_page.png)

3. <span data-ttu-id="a5c1f-136">Opnaðu síðuna fyrir hópinn sem á að breyta og veldu síðan **Stjórna hlutverkum** til að opna valmyndina **Stjórna hóphlutverkum**.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Hnappurinn Stjórna hlutverkum](media/manage_team_roles.png)

4. <span data-ttu-id="a5c1f-138">Úthlutið hlutverkið sem er með les-/skrifheimild fyrir viðeigandi töflur og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="a5c1f-139">Laga samstillingarvandamál í umhverfi sem er með nýlega breytt Dataverse umhverfi</span><span class="sxs-lookup"><span data-stu-id="a5c1f-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="a5c1f-140">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a5c1f-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="a5c1f-141">Þú gætir fengið eftirfarandi villuboð þegar þú stofnar gögn í forriti Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a5c1f-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="a5c1f-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Ekki tókst að mynda farm fyrir eininguna CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Stofnun farms tókst ekki með villunni Ógilt URI: URI er tómt."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="a5c1f-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="a5c1f-143">Svona lítur villan út í líkanadrifnu forritinu í Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="a5c1f-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="a5c1f-144">*Óvænt villa kom upp úr ISV kóða. (ErrorType = ClientError) Óvænt undantekning frá viðbót (Keyra): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: tókst ekki að vinna úr einingareikningi - (Tengingartilraun mistókst vegna þess að tengdur aðili svaraði ekki á fullnægjandi hátt eftir nokkurn tíma, eða ekki tókst að koma á tengingu vegna þess að tengdur hýsill svaraði ekki*</span><span class="sxs-lookup"><span data-stu-id="a5c1f-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="a5c1f-145">Þessi villa kemur upp þegar Dataverse umhverfi er rangt endurstillt á sama tíma og þú reynir að búa til gögn í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="a5c1f-146">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="a5c1f-147">Skráðu þig inn á Finance and Operations sýndarvél (VL), opnaðu SQL Server Management Studio (SSMS) og leitaðu að línum í DUALWRITEPROJECTCONFIGURATIONENTITY töflunni þar sem **internalentityname** er jafnt **viðskiptavinum V3** og **externalentityname** jafngildir **reikningum**.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="a5c1f-148">Hér er hvernig fyrirspurnin lítur út.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="a5c1f-149">Notaðu heiti verkefnisins úr niðurstöðum fyrri fyrirspurnar til að keyra eftirfarandi fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="a5c1f-150">Gakktu úr skugga um að dálkurinn **externalenvironmentURL** sé með rétt Dataverse eða forritsslóð.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="a5c1f-151">Eyða öllum tvíteknum línum sem benda á ranga Dataverse vefslóð.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="a5c1f-152">Eyðið samsvarandi línum í tölfunum DUALWRITEPROJECTFIELDCONFIGURATION og DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="a5c1f-153">Stöðvaðu töfluvörpunina og endurræstu hana</span><span class="sxs-lookup"><span data-stu-id="a5c1f-153">Stop the table mapping, and then restart it</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
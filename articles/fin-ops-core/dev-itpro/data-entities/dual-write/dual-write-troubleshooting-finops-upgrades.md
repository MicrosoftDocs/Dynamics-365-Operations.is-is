---
title: Úrræðaleit vandamál sem tengjast uppfærslu á forritum Finance and Operations
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem tengjast uppfærslu á forritum Finance and Operations.
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172878"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="ccc4e-103">Úrræðaleit vandamál sem tengjast uppfærslu á forritum Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ccc4e-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="ccc4e-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ccc4e-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast uppfærslu á forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccc4e-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="ccc4e-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="ccc4e-108">Villur í gagnagrunnssamstillingu</span><span class="sxs-lookup"><span data-stu-id="ccc4e-108">Database synchronization errors</span></span>

<span data-ttu-id="ccc4e-109">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="ccc4e-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="ccc4e-110">Þú gætir fengið villuboð sem líkjast eftirfarandi dæmi þegar þú reynir að nota eininguna **DualWriteProjectConfiguration** til að uppfæra forrit Finance and Operations í verkvangs uppfærslu 30.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="ccc4e-111">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="ccc4e-112">Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="ccc4e-113">Opnaðu Visual Studio sem stjórnandi og opnaðu hugbúnaðarhlutatré (AOT).</span><span class="sxs-lookup"><span data-stu-id="ccc4e-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="ccc4e-114">Leita að **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="ccc4e-115">I AOT hægrismellirðu á **DualWriteProjectConfiguration** og velur **Bæta við nýtt verkefni**.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="ccc4e-116">Veldu **Í lagi** til að búa til nýja verkið sem notar sjálfgefna valkosti.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="ccc4e-117">Í Solution Explorer hægrismellirðu á **Eiginleikar verks** og stillir **Samstilla gagnagrunn á uppbyggingu** á **True**.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="ccc4e-118">Smíðaðu verkefnið og staðfestu að smíðin heppnaðist.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="ccc4e-119">Í valmyndinni **Dynamics 365** velurðu **Samstilla gagnagrunn**.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="ccc4e-120">Veldu **Samstilla** til að gera fulla samstillingu gagnagrunnsins.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="ccc4e-121">Eftir að samstilling gagnagrunnsins hefur náðst að fullu skaltu endurtaka samstillingu gagnagrunnsins Microsoft Dynamics Lifecycle Services (LCS) og notaðu handvirka uppfærsluhandritin eftir því sem við á, svo þú getir haldið áfram með uppfærsluna.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="ccc4e-122">Reitir sem vantar einingar á kortum</span><span class="sxs-lookup"><span data-stu-id="ccc4e-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="ccc4e-123">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="ccc4e-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="ccc4e-124">Á síðunni **Tvöfalt skrif** gætirðu fengið villuboð sem líkjast eftirfarandi dæmi:</span><span class="sxs-lookup"><span data-stu-id="ccc4e-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="ccc4e-125">*Upprunasvið vantar \<reitnafn\> í skemanu.*</span><span class="sxs-lookup"><span data-stu-id="ccc4e-125">*Missing source field \<field name\> in the schema.*</span></span>

![Dæmi um villuboð vantar upprunasvið](media/error_missing_field.png)

<span data-ttu-id="ccc4e-127">Til að laga málið, fylgdu fyrst þessum skrefum til að ganga úr skugga um að reitirnir séu í einingunni.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="ccc4e-128">Skráðu þig inn á VM fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="ccc4e-129">Farðu í **Vinnusvæði \> Gagnastjórnun**, veldu reitinn **Rammafæribreytur** og síðan, á flipanum **Einingarstillingar**, velurðu **Uppfæra einingalista** til að endurræsa einingarnar.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="ccc4e-130">Farðu í **Vinnusvæði \> Gagnastjórnun**, veldu flipann **Gagnaeiningar** og gakktu úr skugga um að einingin sé skráð.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="ccc4e-131">Ef einingin er ekki skráð skaltu skrá þig inn á VM fyrir forrit Finance and Operations og gakktu úr skugga um að einingin sé tiltæk.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="ccc4e-132">Opnaðu síðuna **Vörpun eininga** af síðunni **Tvöfalt skrif** í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="ccc4e-133">Veldu **Uppfæra einingalista** til að fylla sjálfkrafa reitina í vörpunum eininga.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="ccc4e-134">Ef málið er enn ekki lagað skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccc4e-135">Þessi skref leiðbeina þér í gegnum ferlið við að eyða einingu og bæta henni síðan við aftur.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="ccc4e-136">Vertu viss um að fylgja leiðbeiningunum nákvæmlega til að forðast vandamál.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="ccc4e-137">Í forriti Finance and Operations ferðu í **Vinnusvæði \> Gagnastjórnun** og velur reitinn **Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="ccc4e-138">Finndu eininguna sem vantar reitinn.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="ccc4e-139">Skrifaðu mið af einingunni, stigatöflu, heiti einingarinnar og öðrum dálkagildum.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="ccc4e-140">Ef einhver af vinnsluhópunum þínum er háður þessari einingu, gerðu viðeigandi ráðstafanir fyrir vinnsluhópana áður en þú eyðir einingunni.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="ccc4e-141">Eyddu einingunni sem vantar reitinn.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="ccc4e-142">Veldu **Nýtt** og bættu einingunni aftur við.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="ccc4e-143">Tilgreindu gildin sem þú tókst eftir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="ccc4e-144">Opnaðu síðuna **Vörpun eininga** af síðunni **Tvöfalt skrif** í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="ccc4e-145">Veldu **Uppfæra einingalista** til að fylla sjálfkrafa reitina í vörpunum eininga.</span><span class="sxs-lookup"><span data-stu-id="ccc4e-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

---
title: Úrræðaleit vandamála vegna uppfærslna Finance and Operations forrita
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131222"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="c3cac-103">Úrræðaleit vandamála vegna uppfærslna Finance and Operations forrita</span><span class="sxs-lookup"><span data-stu-id="c3cac-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="c3cac-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c3cac-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="c3cac-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast uppfærslu á forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3cac-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3cac-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="c3cac-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c3cac-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="c3cac-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="c3cac-108">Villur í gagnagrunnssamstillingu</span><span class="sxs-lookup"><span data-stu-id="c3cac-108">Database synchronization errors</span></span>

<span data-ttu-id="c3cac-109">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="c3cac-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="c3cac-110">Þú gætir fengið villuboð sem líkjast eftirfarandi dæmi þegar þú reynir að nota töfluna **DualWriteProjectConfiguration** til að uppfæra forrit Finance and Operations í verkvangs uppfærslu 30.</span><span class="sxs-lookup"><span data-stu-id="c3cac-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="c3cac-111">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c3cac-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="c3cac-112">Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3cac-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="c3cac-113">Opnaðu Visual Studio sem stjórnandi og opnaðu hugbúnaðarhlutatré (AOT).</span><span class="sxs-lookup"><span data-stu-id="c3cac-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="c3cac-114">Leita að **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="c3cac-115">I AOT hægrismellirðu á **DualWriteProjectConfiguration** og velur **Bæta við nýtt verkefni**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="c3cac-116">Veldu **Í lagi** til að búa til nýja verkið sem notar sjálfgefna valkosti.</span><span class="sxs-lookup"><span data-stu-id="c3cac-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="c3cac-117">Í Solution Explorer hægrismellirðu á **Eiginleikar verks** og stillir **Samstilla gagnagrunn á uppbyggingu** á **True**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="c3cac-118">Smíðaðu verkefnið og staðfestu að smíðin heppnaðist.</span><span class="sxs-lookup"><span data-stu-id="c3cac-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="c3cac-119">Í valmyndinni **Dynamics 365** velurðu **Samstilla gagnagrunn**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="c3cac-120">Veldu **Samstilla** til að gera fulla samstillingu gagnagrunnsins.</span><span class="sxs-lookup"><span data-stu-id="c3cac-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="c3cac-121">Eftir að samstilling gagnagrunnsins hefur náðst að fullu skaltu endurtaka samstillingu gagnagrunnsins Microsoft Dynamics Lifecycle Services (LCS) og notaðu handvirka uppfærsluhandritin eftir því sem við á, svo þú getir haldið áfram með uppfærsluna.</span><span class="sxs-lookup"><span data-stu-id="c3cac-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="c3cac-122">Vandamál með töfludálka sem vantar á kort</span><span class="sxs-lookup"><span data-stu-id="c3cac-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="c3cac-123">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="c3cac-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="c3cac-124">Á síðunni **Tvöfalt skrif** gætirðu fengið villuboð sem líkjast eftirfarandi dæmi:</span><span class="sxs-lookup"><span data-stu-id="c3cac-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="c3cac-125">*Upprunareitur sem vantar \<field name\> í skemanu.*</span><span class="sxs-lookup"><span data-stu-id="c3cac-125">*Missing source field \<field name\> in the schema.*</span></span>

![Dæmi um villuboð vantar upprunadálk](media/error_missing_field.png)

<span data-ttu-id="c3cac-127">Til að laga málið skaltu fyrst fylgja þessum skrefum til að ganga úr skugga um að dálkarnir séu í töflunni.</span><span class="sxs-lookup"><span data-stu-id="c3cac-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="c3cac-128">Skráðu þig inn á VM fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3cac-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="c3cac-129">Opnaðu **Vinnusvæði \> Gagnastjórnun**, veldu reitinn **Færibreytur ramma** og síðan á flipanum **Töflustillingar** skaltu velja **Uppfæra töflulista** til að uppfæra töflurnar.</span><span class="sxs-lookup"><span data-stu-id="c3cac-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="c3cac-130">Opnaðu **Vinnusvæði \> Gagnastjórnun**, veldu flipann **Gagnatöflur** og gakktu úr skugga um að taflan sé skráð.</span><span class="sxs-lookup"><span data-stu-id="c3cac-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="c3cac-131">Ef taflan er ekki skráð skaltu skrá þig inn á VM fyrir forrit Finance and Operations og ganga úr skugga um að taflan sé tiltæk.</span><span class="sxs-lookup"><span data-stu-id="c3cac-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="c3cac-132">Opnaðu síðuna **Vörpun töflu** á síðunni **Tvöföld skráning** í Finance and Operations -forritinu.</span><span class="sxs-lookup"><span data-stu-id="c3cac-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="c3cac-133">Veldu **Uppfæra töflulista** til að fylla sjálfkrafa út reitina í töfluvörpunum.</span><span class="sxs-lookup"><span data-stu-id="c3cac-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="c3cac-134">Ef málið er enn ekki lagað skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c3cac-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3cac-135">Þessi skref leiðbeina þér í gegnum ferlið við að eyða töflu og bæta henni síðan við aftur.</span><span class="sxs-lookup"><span data-stu-id="c3cac-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="c3cac-136">Vertu viss um að fylgja leiðbeiningunum nákvæmlega til að forðast vandamál.</span><span class="sxs-lookup"><span data-stu-id="c3cac-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="c3cac-137">Í Finance and Operations -forritinu skal opna **Vinnusvæði \> Gagnastjórnun** og velja reitinn **Gagnatöflur**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="c3cac-138">Finnið töfluna sem vantar eigindina.</span><span class="sxs-lookup"><span data-stu-id="c3cac-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="c3cac-139">Smelltu á **Breyta markvörpun** á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="c3cac-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="c3cac-140">Á **Varpa sviðsetningu á mark** svæðinu skaltu smella á **Búa til vörpun**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="c3cac-141">Opnaðu síðuna **Vörpun töflu** á síðunni **Tvöföld skráning** í Finance and Operations -forritinu.</span><span class="sxs-lookup"><span data-stu-id="c3cac-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="c3cac-142">Ef vörpunin býr ekki sjálfkrafa til eigindina skaltu bæta henni við með því að smella á **Bæta við eigind** hnappinn og svo **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="c3cac-143">Veldu vörpunina og smelltu á **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="c3cac-143">Select the map and click **Run**.</span></span>

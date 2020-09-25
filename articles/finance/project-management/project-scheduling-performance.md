---
title: Frammistaða tilfangaáætlunar verks
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að bæta afköst tilfangaáætlunar fyrir mikinn fjölda verkefna.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760579"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="5ac6c-103">Frammistaða tilfangaáætlunar verks</span><span class="sxs-lookup"><span data-stu-id="5ac6c-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="5ac6c-104">Afkastavandamálum sem tengjast tilfangaáætlun getur átt sér stað þegar um þúsundir verka er að ræða.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="5ac6c-105">Til að bæta afköst tilfangaáætlunar gerir tiltekinn eiginleiki notendum kleift að stytta tímann sem tekur að opna skjámyndina fyrir tilföng til ráðstöfunar.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="5ac6c-106">Sérstaklega fjarlægir þetta samstillingu tilfangagetu samantekta og notar **ResProjectResource** töfluna til að flýta leit tilfanga.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="5ac6c-107">Athugið að ekki er lengur hægt að nota töfluna **ResRollup**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ac6c-108">Ef samstillingarferli forðagetu eða **ResProjectResource** taflan eru tengd ekki skal nota þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="5ac6c-109">Virkja afkastaaukningu tilfangaáætlunar</span><span class="sxs-lookup"><span data-stu-id="5ac6c-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="5ac6c-110">Til að virkja endurbætt frammistöðu tilfangaáætlunar skal ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="5ac6c-111">Farðu í **Eiginleikastjórnun** > **Allt** og á eiginleikalistanum skal finna **Virkja eiginleika afkastaaukningar fyrir áætlanagerð verktilfangs**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="5ac6c-112">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="5ac6c-113">Ef ekki er hægt að finna eiginleikann á listanum skal velja **Leita að uppfærslum** til að uppfæra listann.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="5ac6c-114">Endurhlaðið vafrann og farið síðan í **Verkefnastjórnun og bókhald** > **Reglubundið** > **Verktilföng** > **Samstilla afkastagetu tilfangadagatala í öllum fyrirtækjum**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="5ac6c-115">Stilltu **Fjarlæga fyrirliggjandi afkastagetuskrár** á **Já** til að fjarlægja fyrri gögn.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="5ac6c-116">Ef búa á til stigvaxandi gögn skal stilla það á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="5ac6c-117">Í reitnum **Tímabilskóði** skal velja tímabilið sem á að mynda gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="5ac6c-118">Ef tímabilskóði er valinn þarf ekki að skilgreina upphafs- og lokadagsetningar.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="5ac6c-119">Ef reiturinn **Tímabilskóði** er skilinn eftir auður skal velja tilteknar upphafs- og lokadagsetningar til að búa til gögn.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="5ac6c-120">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="5ac6c-121">Þetta dreifir almennum gögnum á **ResCalendarCapacity** töflu yfir öll fyrirtæki í umhverfinu og því þarf aðeins að keyra runuvinnsluna hjá einum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="5ac6c-122">Gögnin í þessari runuvinnslu eru nauðsynleg til að reikna afkastagetu tilfanga í gegnum tengda dagatalið.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="5ac6c-123">Farðu í **Verkefnastjórnun og bókhald** > **Reglubundið** > **Verktilföng** > **Færa inn verktilföng í öll fyrirtæki** og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="5ac6c-124">Þetta er gagnauppfærsluforskriftin fyrir almenn gögn í töflunum **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="5ac6c-125">Gildin fyrir svæðið **PSAPRojSchedRole.RootActivity** eru einnig uppfærð.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="5ac6c-126">Ef þetta er ekki keyrt birtist viðvörun þegar reynt er að keyra tilfangaáætlanir.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="5ac6c-127">Slökkva á afkastaaukningu tilfangaáætlunar</span><span class="sxs-lookup"><span data-stu-id="5ac6c-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="5ac6c-128">Farðu í **Eiginleikastjórnun** > **Allt** og leitaðu að **Virkja eiginleika afkastaaukningar fyrir áætlanagerð verktilfangs**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="5ac6c-129">Veldu eiginleikann og svo hnappinn **Óvirkja**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="5ac6c-130">Uppfærðu vafrann þinn.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-130">Refresh your browser.</span></span>
4. <span data-ttu-id="5ac6c-131">Farðu í **Verkefnastjórnun og bókhald** > **Reglubundið** > **Samstilling afkastagetu** > **Samstilla tilfangagetu samantekta**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="5ac6c-132">Á síðunni **Samstilling samantektar á afkastagetu** skal stilla **Fjarlæga fyrirliggjandi afkastagetuskrár** á **Já** til að fjarlægja fyrri gögn.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="5ac6c-133">Ef ætlunin er að búa til stigvaxandi gögn skal stilla þetta á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="5ac6c-134">Í reitnum **Tímabilskóði** skal velja tímabilið sem á að mynda gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="5ac6c-135">Ef tímabilskóði er valinn þarf ekki að skilgreina upphafs- og lokadagsetningar.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="5ac6c-136">Ef reiturinn **Tímabilskóði** er skilinn eftir auður skal velja tilteknar upphafs- og lokadagsetningar til að búa til gögn.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="5ac6c-137">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="5ac6c-138">Þetta dreifir almennum gögnum á töfluna **ResRollup** á milli allra fyrirtækja í umhverfinu og því þarf aðeins að keyra runuvinnsluna hjá einum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="5ac6c-139">Þessi runuvinnsla er nauðsynleg fyrir **Tilföng til ráðstöfunar**.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="5ac6c-140">Ef þessi runuvinnsla er ekki keyrð verða **ResRollup** gögn búið til um leið og getur það tekið tíma.</span><span class="sxs-lookup"><span data-stu-id="5ac6c-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>

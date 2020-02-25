---
title: Skjalageymsla ER-gerð áfangastaðar
description: Þetta efni veitir upplýsingar um hvernig á að stilla skjalasafn áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019828"
---
# <span data-ttu-id="a5a60-103"><a name="ArchiveDestinationType">áfangastaður skjalasafns</a></span><span class="sxs-lookup"><span data-stu-id="a5a60-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5a60-104">Hægt er að stilla skjalasafn áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl.</span><span class="sxs-lookup"><span data-stu-id="a5a60-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="a5a60-105">Byggt á ákvörðunarstað, er myndað skjal geymt sem viðhengi við skrá yfir ER-vinnslulistann.</span><span class="sxs-lookup"><span data-stu-id="a5a60-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="a5a60-106">Hægt er að nota þennan valkost til að senda myndað skjal á Microsoft SharePoint-möppu eða Microsoft Microsoft Azure Geymslu.</span><span class="sxs-lookup"><span data-stu-id="a5a60-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="a5a60-107">Stilla **Virkt** á **Já** til að senda frálag á áfangastað sem er skilgreind með völdu skjalagerðina.</span><span class="sxs-lookup"><span data-stu-id="a5a60-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="a5a60-108">einungis gerð skjals þar sem flokksins er stillt á **Skrá** eru tiltækar til vals.</span><span class="sxs-lookup"><span data-stu-id="a5a60-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="a5a60-109">Hægt er að skilgreina [gerðir skjala](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) í **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Skjalagerðir**.</span><span class="sxs-lookup"><span data-stu-id="a5a60-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="a5a60-110">Skilgreining fyrir áfangastaði rafrænnar skýrslugerðar er sú sama og skilgreiningin fyrir skjalastjórnunarkerfið.</span><span class="sxs-lookup"><span data-stu-id="a5a60-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="a5a60-111">[![Síðan Gerðir skjala](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="a5a60-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="a5a60-112">Staðsetning ákvarðar hvar skráin er vistuð.</span><span class="sxs-lookup"><span data-stu-id="a5a60-112">The location determines where the file is saved.</span></span> <span data-ttu-id="a5a60-113">Eftir að áfangastaður **skjalasafns** er virkjaður er hægt að vista niðurstöður í Vinnsluskjalasafn.</span><span class="sxs-lookup"><span data-stu-id="a5a60-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="a5a60-114">Hægt er að skoða niðurstöðurnar í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="a5a60-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="a5a60-115">Veldu gerð skjals fyrir Vinnslu skjalasafns með því að fara í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð** \> **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="a5a60-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="a5a60-116">Frekari upplýsingar er að finna í [Stilla ramma rafrænnar skýrslugerðar (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="a5a60-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="a5a60-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="a5a60-117">SharePoint</span></span>

<span data-ttu-id="a5a60-118">Hægt er að vista skrá í möppu merktu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a5a60-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="a5a60-119">Til að skilgreina sjálfgefinn þjón SharePoint ferðu á **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Færibreytur skjalastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="a5a60-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="a5a60-120">Á flipanum **SharePoint** stillirðu SharePoint-möppuna.</span><span class="sxs-lookup"><span data-stu-id="a5a60-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="a5a60-121">Síðan geturðu valið það sem möppu þar sem ER framleiðsla verður vistuð.</span><span class="sxs-lookup"><span data-stu-id="a5a60-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="a5a60-122">Staðsetning **SharePoint** verður að vera valin í þessari gerð skjals.</span><span class="sxs-lookup"><span data-stu-id="a5a60-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="a5a60-123">[![Val á SharePoint möppu](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="a5a60-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="a5a60-124">Azure-geymsla</span><span class="sxs-lookup"><span data-stu-id="a5a60-124">Azure Storage</span></span>

<span data-ttu-id="a5a60-125">Þegar staðsetning gerðar skjals er stillt á **Azure-geymsla**, er hægt að vista skrá í Azure Geymslu.</span><span class="sxs-lookup"><span data-stu-id="a5a60-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5a60-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a5a60-126">Additional resources</span></span>

- [<span data-ttu-id="a5a60-127">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a5a60-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="a5a60-128">Áfangastaðir fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a5a60-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="a5a60-129">Stilla skjalastjórnun</span><span class="sxs-lookup"><span data-stu-id="a5a60-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)

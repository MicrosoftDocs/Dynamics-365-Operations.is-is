---
title: Skjalageymsla ER-gerð áfangastaðar
description: Þetta efni veitir upplýsingar um hvernig á að stilla skjalasafn áfangastaðar fyrir hvern FOLDER- eða FILE-hluta á rafrænu skýrslugerðarsniði.
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 079eda04fcc41fc637419a83452db10b89ed1ab9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894029"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="dcde5-103">Skjalageymsla ER-gerð áfangastaðar</span><span class="sxs-lookup"><span data-stu-id="dcde5-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcde5-104">Hægt er að stilla skjalasafn áfangastaðar fyrir hveja **Möppu** eða **Skrá** hluta á rafrænu skýrslugerðarsniði sem er stillt til að búa til skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="dcde5-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="dcde5-105">Byggt á ákvörðunarstað, er myndað skjal geymt sem viðhengi við skrá yfir ER-vinnslulistann.</span><span class="sxs-lookup"><span data-stu-id="dcde5-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="dcde5-106">Til að skoða niðurstöðurnar skal fara í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Rafræn skýrslugerðarvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="dcde5-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="dcde5-107">Hægt er að nota þennan valkost til að senda myndað skjal á Microsoft SharePoint-möppu eða Microsoft Microsoft Azure Geymslu.</span><span class="sxs-lookup"><span data-stu-id="dcde5-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="dcde5-108">Stilla **Virkt** á **Já** til að senda frálag á áfangastað sem er skilgreind með völdu skjalagerðina.</span><span class="sxs-lookup"><span data-stu-id="dcde5-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="dcde5-109">einungis gerð skjals þar sem flokksins er stillt á **Skrá** eru tiltækar til vals.</span><span class="sxs-lookup"><span data-stu-id="dcde5-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="dcde5-110">Hægt er að skilgreina [gerðir skjala](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) í **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Skjalagerðir**.</span><span class="sxs-lookup"><span data-stu-id="dcde5-110">You define document [types](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="dcde5-111">Skilgreining fyrir áfangastaði rafrænnar skýrslugerðar er sú sama og skilgreiningin fyrir skjalastjórnunarkerfið.</span><span class="sxs-lookup"><span data-stu-id="dcde5-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="dcde5-112">[![Síðan Gerðir skjala](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="dcde5-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="dcde5-113">Staðsetning ákvarðar hvar skráin er vistuð.</span><span class="sxs-lookup"><span data-stu-id="dcde5-113">The location determines where the file is saved.</span></span> <span data-ttu-id="dcde5-114">Eftir að áfangastaður **skjalasafns** er virkjaður er hægt að vista niðurstöður í Vinnsluskjalasafn.</span><span class="sxs-lookup"><span data-stu-id="dcde5-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="dcde5-115">Hægt er að skoða niðurstöðurnar í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="dcde5-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="dcde5-116">Veldu gerð skjals fyrir Vinnslu skjalasafns með því að fara í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð** \> **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="dcde5-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="dcde5-117">Frekari upplýsingar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="dcde5-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="dcde5-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="dcde5-118">SharePoint</span></span>

<span data-ttu-id="dcde5-119">Hægt er að vista skrá í möppu merktu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dcde5-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="dcde5-120">Til að skilgreina sjálfgefinn þjón SharePoint ferðu á **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Færibreytur skjalastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="dcde5-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="dcde5-121">Á flipanum **SharePoint** stillirðu SharePoint-möppuna.</span><span class="sxs-lookup"><span data-stu-id="dcde5-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="dcde5-122">Síðan geturðu valið það sem möppu þar sem ER framleiðsla verður vistuð.</span><span class="sxs-lookup"><span data-stu-id="dcde5-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="dcde5-123">Staðsetning **SharePoint** verður að vera valin í þessari gerð skjals.</span><span class="sxs-lookup"><span data-stu-id="dcde5-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="dcde5-124">[![Val á SharePoint möppu](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="dcde5-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="dcde5-125">Azure-geymsla</span><span class="sxs-lookup"><span data-stu-id="dcde5-125">Azure Storage</span></span>

<span data-ttu-id="dcde5-126">Þegar staðsetning gerðar skjals er stillt á **Azure-geymsla**, er hægt að vista skrá í Azure Geymslu.</span><span class="sxs-lookup"><span data-stu-id="dcde5-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="dcde5-127">Rammi rafrænnar skýrslugerðar vistar skrár varanlega í Azure Blob geymslu ólíkt ramma Gagnastjórnunar sem notar sjö daga varðveislureglu fyrir skjöl sem þarf að vinna úr.</span><span class="sxs-lookup"><span data-stu-id="dcde5-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="dcde5-128">Frekari upplýsingar er að finna í [API til að sækja skilaboðastöðu](../data-entities/recurring-integrations.md#api-for-getting-message-status) og [Stöðuprófun API](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="dcde5-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="dcde5-129">Ótengdar skrár verða geymdar í Azure Blob geymslu sem viðhengi töflufærslna forrits eins lengi og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="dcde5-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="dcde5-130">Einni skrá verður eytt úr Azure Blob geymslu ásamt hugbúnaðartöflufærslunni sem þessi skrá var hengd við.</span><span class="sxs-lookup"><span data-stu-id="dcde5-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dcde5-131">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dcde5-131">Additional resources</span></span>

- [<span data-ttu-id="dcde5-132">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="dcde5-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="dcde5-133">Áfangastaðir fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="dcde5-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="dcde5-134">Stilla skjalastjórnun</span><span class="sxs-lookup"><span data-stu-id="dcde5-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
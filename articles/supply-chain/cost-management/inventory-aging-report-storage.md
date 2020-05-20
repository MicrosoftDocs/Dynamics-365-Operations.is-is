---
title: Skýrsla um aldursgreiningu birgða
description: Þetta efni lýsir virkni sem gerir þér kleift að keyra aldursgreiningarskýrslu birgða og gera úttakið tiltækt sem form og töflu.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e68833cc2b4430f66419a67b1cba5f6c8c209f4
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323624"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="874d8-103">Skýrsla um aldursgreiningu birgða</span><span class="sxs-lookup"><span data-stu-id="874d8-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="874d8-104">Í Microsoft Dynamics 365 Supply Chain Management er hægt að keyra skýrsluna **Geymsla aldursgreiningarskýrslu birgða** og gera niðurstöðurnar tiltækar sem skjámynd og graf.</span><span class="sxs-lookup"><span data-stu-id="874d8-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="874d8-105">Á forminu er dálkum og samanlögðum stöðum gagnvirkt breytt, allt eftir því skipulagi sem er stillt.</span><span class="sxs-lookup"><span data-stu-id="874d8-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="874d8-106">Grafið gefur sjónrænt yfirlit sem styður síun og gerir þér kleift að bora niður í smáatriði.</span><span class="sxs-lookup"><span data-stu-id="874d8-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="874d8-107">Að auki leyfir gagnaeining sem kölluð er **Skýrsla um aldursgreiningu birgða** að flytja út niðurstöður á keyrslu á skýrslu **Geymsla aldursgreiningarskýrslu birgða** á form eins og Microsoft Excel-skrá eða PDF-skrá.</span><span class="sxs-lookup"><span data-stu-id="874d8-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="874d8-108">Þessi aðferð við að keyra **Geymsla aldursgreiningarskýrslu birgða** skýrslu er gagnleg í tilfellum þegar niðurstöðurnar innihalda margar línur.</span><span class="sxs-lookup"><span data-stu-id="874d8-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="874d8-109">Til dæmis mun úttakið innihalda margar línur ef þú ert með 50.000 hluti og 300 verslanir sem eru stofnaðar sem vöruhús og þú biður um aldursgreiningu birgða eftir hlut, síðu og vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="874d8-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="874d8-110">Virkja eiginleika fyrir geymslu aldursgreiningarskýrslu birgða</span><span class="sxs-lookup"><span data-stu-id="874d8-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="874d8-111">Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="874d8-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="874d8-112">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleika og virkja hann ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="874d8-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="874d8-113">Hérna er eiginleikinn skráður sem:</span><span class="sxs-lookup"><span data-stu-id="874d8-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="874d8-114">**Eining** - Kostnaðarstjórnun</span><span class="sxs-lookup"><span data-stu-id="874d8-114">**Module** - Cost management</span></span>
- <span data-ttu-id="874d8-115">**Heiti eiginleika** - Skýrsla um aldursgreiningu birgða</span><span class="sxs-lookup"><span data-stu-id="874d8-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="874d8-116">Keyra skýrslu um aldursgreiningu birgða</span><span class="sxs-lookup"><span data-stu-id="874d8-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="874d8-117">Farðu í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla aldursgreiningarskýrslu birgða**.</span><span class="sxs-lookup"><span data-stu-id="874d8-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="874d8-118">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="874d8-118">Select **New**.</span></span>
1. <span data-ttu-id="874d8-119">Í reitinn **Kenni ferlis – Heiti** er slegið inn einkvæmt heiti fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="874d8-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="874d8-120">Veldu skýrsluna **Auðkenning - kenni** og síaðu hana eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="874d8-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="874d8-121">Framkvæmd skýrslu er alltaf gerð í runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="874d8-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="874d8-122">Eftir að runuvinnslunni er lokið er úttakið sýnt á síðunni **Geymsla aldursgreiningarskýrslu birgða**.</span><span class="sxs-lookup"><span data-stu-id="874d8-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="874d8-123">Til að skoða úttakið sem glugga með hefðbundið hnitaútlit skaltu velja **Skoða upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="874d8-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="874d8-124">Til að skoða úttakið sem uppsafnaða töflu velurðu **Skoða rit**.</span><span class="sxs-lookup"><span data-stu-id="874d8-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="874d8-125">Formið mun ekki innihalda millisamtölur sem eru skilgreindar í skýrsluútliti.</span><span class="sxs-lookup"><span data-stu-id="874d8-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="874d8-126">Gagnaeiningin **Skýrsla um aldursgreiningu birgða** gerir þér kleift að flytja niðurstöðurnar af **Geymsla aldursgreiningarskýrslu birgða** skýrslu út með því að nota síu fyrir reitinn **Kenni ferlis - Heiti** á hvaða snið sem gagnastjórnun styður.</span><span class="sxs-lookup"><span data-stu-id="874d8-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>

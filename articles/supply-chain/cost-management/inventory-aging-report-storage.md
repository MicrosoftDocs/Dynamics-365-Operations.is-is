---
title: Aldursskýrsla birgða
description: Þetta efni lýsir virkni sem gerir þér kleift að keyra aldursgreiningarskýrslu birgða og gera úttakið tiltækt sem form og töflu.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810252"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="f02a5-103">Aldursskýrsla birgða</span><span class="sxs-lookup"><span data-stu-id="f02a5-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f02a5-104">Í Microsoft Dynamics 365 Supply Chain Management geturðu keyrt skýrsluna **Aldursgreiningu birgða** og gera úttakið tiltækt sem form og töflu.</span><span class="sxs-lookup"><span data-stu-id="f02a5-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="f02a5-105">Á forminu er dálkum og samanlögðum stöðum gagnvirkt breytt, allt eftir því skipulagi sem er stillt.</span><span class="sxs-lookup"><span data-stu-id="f02a5-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="f02a5-106">Grafið gefur sjónrænt yfirlit sem styður síun og gerir þér kleift að bora niður í smáatriði.</span><span class="sxs-lookup"><span data-stu-id="f02a5-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="f02a5-107">Að auki gerir gagnaeining sem heitir **Aldursskýrsla birgða** þér kleift að flytja út niðurstöður skýrslunnar **Aldursgreining birgða** sem var keyrð á snið eins og Microsoft Excel-skjal eða PDF-skjal.</span><span class="sxs-lookup"><span data-stu-id="f02a5-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="f02a5-108">Þessi aðferð til að keyra skýrsluna **Aldursgreining birgða** er gagnlegt í tilvikum þar sem úttakið inniheldur margar línur.</span><span class="sxs-lookup"><span data-stu-id="f02a5-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="f02a5-109">Til dæmis mun úttakið innihalda margar línur ef þú ert með 50.000 hluti og 300 verslanir sem eru stofnaðar sem vöruhús og þú biður um aldursgreiningu birgða eftir hlut, síðu og vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="f02a5-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="f02a5-110">Keyra aldursskýrslu birgða</span><span class="sxs-lookup"><span data-stu-id="f02a5-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="f02a5-111">Farðu í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla aldursgreiningarskýrslu birgða**.</span><span class="sxs-lookup"><span data-stu-id="f02a5-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="f02a5-112">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f02a5-112">Select **New**.</span></span>
1. <span data-ttu-id="f02a5-113">Í reitinn **Kenni ferlis – Heiti** er slegið inn einkvæmt heiti fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="f02a5-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="f02a5-114">Veldu skýrsluna **Auðkenning - kenni** og síaðu hana eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f02a5-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="f02a5-115">Framkvæmd skýrslu er alltaf gerð í runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="f02a5-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="f02a5-116">Eftir að runuvinnslunni er lokið er úttakið sýnt á síðunni **Geymsla aldursgreiningarskýrslu birgða**.</span><span class="sxs-lookup"><span data-stu-id="f02a5-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="f02a5-117">Til að skoða úttakið sem glugga með hefðbundið hnitaútlit skaltu velja **Skoða upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="f02a5-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="f02a5-118">Til að skoða úttakið sem uppsafnaða töflu velurðu **Skoða rit**.</span><span class="sxs-lookup"><span data-stu-id="f02a5-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f02a5-119">Formið mun ekki innihalda millisamtölur sem eru skilgreindar í skýrsluútliti.</span><span class="sxs-lookup"><span data-stu-id="f02a5-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="f02a5-120">Gagnaeiningin **Aldursskýrsla birgða** gerir þér kleift að flytja úttakið úr skýrslunni **Aldursgreining birgða** með því að beita síu fyrir reitinn **Kenni ferlis – Heiti** á hvaða snið sem gagnastjórnun styður.</span><span class="sxs-lookup"><span data-stu-id="f02a5-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>

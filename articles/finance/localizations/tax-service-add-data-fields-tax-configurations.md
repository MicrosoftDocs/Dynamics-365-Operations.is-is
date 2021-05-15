---
title: Bæta við gagnareitum í skattaskilgreiningum
description: Þetta efnisatriði útskýrir hvernig á að sérsníða skattaskilgreiningar með því að bæta við gagnasvæðum.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921190"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="5024d-103">Bæta við gagnareitum í skattaskilgreiningum</span><span class="sxs-lookup"><span data-stu-id="5024d-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5024d-104">Þetta efnisatriði útskýrir hvernig á að sérstilla skattaskilgreiningar [gagnareiti sem er bætt við í skattasamþættingu](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="5024d-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="5024d-105">Sérstilla skattgagnalíkan</span><span class="sxs-lookup"><span data-stu-id="5024d-105">Customize the tax data model</span></span>

1. <span data-ttu-id="5024d-106">Í Microsoft Dynamics 365 Finance skaltu fara í **Rafræn skýrslugerð** \> **Skattaskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="5024d-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="5024d-107">Í skilgreiningartrénu velurðu **Skattgaganlíkan - Evrópa**.</span><span class="sxs-lookup"><span data-stu-id="5024d-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="5024d-108">Í aðgerðasvæðinu velurðu svo **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="5024d-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="5024d-109">Í fellilistanum velurðu **Skattskylt skjallíkan afleitt af nafni: Skattgagnalíkan -- Evrópa, Microsoft** valkostinn, slærð inn heiti fyrir nýja skattgagnalíkanið og velur **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="5024d-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="5024d-110">Veljið skattgagnalíkan sem nýverið var stofnuð, og síðan, á Aðgerðarúðu, smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5024d-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="5024d-111">Víkkið tré gagnalíkans, veljið **Línur** og svo **Ný**.</span><span class="sxs-lookup"><span data-stu-id="5024d-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="5024d-112">Í svarglugganum **Stofna hnút** skaltu slá inn nafn, tilgreina gerð atriðis og velja svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5024d-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="5024d-113">Bæta skal við öllum áskildum dálkum.</span><span class="sxs-lookup"><span data-stu-id="5024d-113">Add any required columns.</span></span>
8. <span data-ttu-id="5024d-114">Á aðgerðasvæðinu skal velja **Vista** og síðan **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="5024d-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="5024d-115">Lokaðu síðunni og skoðaðu lokaútgáfu af skattgagnalíkani þínu.</span><span class="sxs-lookup"><span data-stu-id="5024d-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="5024d-116">Sérstilla skattaskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="5024d-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="5024d-117">Í Finance er farið í **Rafræn skýrslugerð** \> **Skattaskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="5024d-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="5024d-118">Í skilgreiningartrénu velurðu **Skattaskilgreining - Evrópa**.</span><span class="sxs-lookup"><span data-stu-id="5024d-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="5024d-119">Í aðgerðasvæðinu velurðu svo **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="5024d-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="5024d-120">Í fellilistanum velurðu **Skilgreining skattþjónustu afleidd af nafni: Skattaskilgreining -- Evrópa, Microsoft** valkostinn, slærð inn heiti fyrir nýju skattaskilgreininguna og velur **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="5024d-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="5024d-121">Veljið skattaskilgreiningu sem nýverið var stofnuð, og síðan, á Aðgerðarúðu, smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5024d-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="5024d-122">Í hlutanum **Eiginleikar** í **Gagnalíkan** skal velja sérstillta skattgagnalíkanið sem var búið til áður.</span><span class="sxs-lookup"><span data-stu-id="5024d-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="5024d-123">Í reitnum **Útgáfa gagnalíkans** er lokið við að velja útgáfu af gerð skattagagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="5024d-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="5024d-124">Veljið **Bæta við** og bætið við nauðsynlegum skattalegum ráðstöfunum.</span><span class="sxs-lookup"><span data-stu-id="5024d-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="5024d-125">Á aðgerðasvæðinu skal velja **Vista** og síðan **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="5024d-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="5024d-126">Lokið síðunni og skoðið lokaútgáfu af skattgagnalíkaninu.</span><span class="sxs-lookup"><span data-stu-id="5024d-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="5024d-127">Innleiða skattaeiginleika í sérsniðinni skattaskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="5024d-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="5024d-128">Í Regulatory Configuration Service (RCS) skal fara í **Altækir eiginleikar** \> **Skattur**.</span><span class="sxs-lookup"><span data-stu-id="5024d-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="5024d-129">Veljið **Bæta við**, sláið inn upplýsingar um nýja eiginleikann og veljið svo **Búa til eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="5024d-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="5024d-130">Á flipanum **Útgáfur** skal velja eiginleikann og svo **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="5024d-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="5024d-131">Á flipanum **Almennt** í reitnum **Útgáfa skilgreiningar** skal velja sérstillta skattaskilgreiningu og útgáfu.</span><span class="sxs-lookup"><span data-stu-id="5024d-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="5024d-132">Í svarglugganum **Stjórna dálkum** skal velja haus og línudálka sem á að hafa með á sérstilltri skattaráðstöfun og velja svo rétta örvatakkann til að bæta þeim á listann **Valdir dálkar**.</span><span class="sxs-lookup"><span data-stu-id="5024d-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>

---
title: Setja upp umhverfi fyrir uppflettingar aðalgagna
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp umhverfið til að nota uppflettingarvirkni fyrir aðalgögn skattaútreiknings.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021345"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="5d796-103">Setja upp umhverfi fyrir uppflettingar aðalgagna</span><span class="sxs-lookup"><span data-stu-id="5d796-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d796-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp umhverfið til að nota uppflettingarvirkni fyrir aðalgögn skattaútreiknings.</span><span class="sxs-lookup"><span data-stu-id="5d796-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="5d796-105">Setja upp samþættingu Power Platform í Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5d796-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="5d796-106">Frekari upplýsingar er að finna í [Microsoft Power Platform samþætting - Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5d796-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="5d796-107">Setja upp Dynamics 365 Finance og Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5d796-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="5d796-108">Frekari upplýsingar er að finna í [Lausnin sótt](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Sannvottun og leyfisveiting](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="5d796-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="5d796-109">Setjið upp eftirfarandi einingar.</span><span class="sxs-lookup"><span data-stu-id="5d796-109">Set up the following entities.</span></span> <span data-ttu-id="5d796-110">Frekari upplýsingar eru í [Virkjun sýndareininga](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="5d796-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="5d796-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="5d796-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-112">CurrencyEntity</span></span>
      - <span data-ttu-id="5d796-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="5d796-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="5d796-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="5d796-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="5d796-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="5d796-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="5d796-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="5d796-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="5d796-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="5d796-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="5d796-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="5d796-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="5d796-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="5d796-123">TaxItemGroupHeading</span><span class="sxs-lookup"><span data-stu-id="5d796-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="5d796-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="5d796-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="5d796-125">Setjið upp Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="5d796-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="5d796-126">Stofnið þjónustubeiðni fyrir Microsoft til að virkja tilraunaútgáfu á eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="5d796-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="5d796-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="5d796-127">ERCdsFeature</span></span>
      - <span data-ttu-id="5d796-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="5d796-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="5d796-129">Farið á vinnusvæðið **Eiginleikastjórnun** og virkið eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="5d796-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="5d796-130">(Forútgáfa) Stuðningur við Dataverse gagnagjafa rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5d796-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="5d796-131">(Forútgáfa) Stuðningur við gagnagjafa skattþjónustu Dataverse</span><span class="sxs-lookup"><span data-stu-id="5d796-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="5d796-132">(Forskoðun) Altækir eiginleikar</span><span class="sxs-lookup"><span data-stu-id="5d796-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="5d796-133">Skráðu þig inn í RCS með stjórnandareikningi leigjanda.</span><span class="sxs-lookup"><span data-stu-id="5d796-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="5d796-134">Farðu í **Rafræn skýrslugerð** > **Tengd forrit**.</span><span class="sxs-lookup"><span data-stu-id="5d796-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="5d796-135">Veldu **Ný** til að bæta við færslu og færðu inn eftirfarandi reitarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="5d796-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="5d796-136">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="5d796-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="5d796-137">Í reitnum **Tegund** skal velja **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="5d796-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="5d796-138">Í reitinn **Forrit** skal slá inn Dataverse vefslóð.</span><span class="sxs-lookup"><span data-stu-id="5d796-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="5d796-139">Í reitinn **Leigjandi** skal slá inn leigjandann.</span><span class="sxs-lookup"><span data-stu-id="5d796-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="5d796-140">Í reitinn **Sérsniðin vefslóð** skal slá inn Dataverse vefslóðina og bæta við hana „/api/data/v9.1“.</span><span class="sxs-lookup"><span data-stu-id="5d796-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="5d796-141">Veldu **Athuga tengingu** og ljúktu við tengingarferlið.</span><span class="sxs-lookup"><span data-stu-id="5d796-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="5d796-142">[![Athuga tengihnapp](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="5d796-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="5d796-143">Farðu í **Rafræn skýrslugerð** > **Skattaskilgreiningar** og flyttu inn skattaskilgreiningar úr [Skattaskilgreiningar](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="5d796-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="5d796-144">[![Síða skattaskilgreiningar, tré skattgagnalíkans](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="5d796-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="5d796-145">Farður í **Vörpun skattskylds skjallíkans** eða **Dataverse líkanavörpun** ef þú ert að nota skilgreiningu Microsoft og í reitnum **Tengt forrit** skal velja færsluna sem var búin til í skrefi 7.</span><span class="sxs-lookup"><span data-stu-id="5d796-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="5d796-146">Stilltu **Sjálfgefið fyrir líkanavörpun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="5d796-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="5d796-147">[![Síða líkanavörpunar](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="5d796-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Setja upp umhverfi fyrir uppflettingar aðalgagna
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp umhverfið til að nota uppflettingarvirkni fyrir aðalgögn skattaútreiknings.
author: kai-cloud
ms.date: 03/31/2021
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
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869073"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="65ee7-103">Setja upp umhverfi fyrir uppflettingar aðalgagna</span><span class="sxs-lookup"><span data-stu-id="65ee7-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="65ee7-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp umhverfið til að nota uppflettingarvirkni fyrir aðalgögn skattaútreiknings.</span><span class="sxs-lookup"><span data-stu-id="65ee7-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="65ee7-105">Setja upp samþættingu Power Platform í Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="65ee7-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="65ee7-106">Frekari upplýsingar er að finna í [Microsoft Power Platform samþætting - Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="65ee7-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="65ee7-107">Setja upp Dynamics 365 Finance og Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="65ee7-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="65ee7-108">Frekari upplýsingar er að finna í [Lausnin sótt](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Sannvottun og leyfisveiting](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="65ee7-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="65ee7-109">Flytjið inn *Lausn sýndareiningar fyrir skilyrði skattþjónustu* úr [Sýndareiningu skattþjónustu](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="65ee7-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="65ee7-110">Setjið upp Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="65ee7-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="65ee7-111">Stofnið þjónustubeiðni fyrir Microsoft til að virkja tilraunaútgáfu á eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="65ee7-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="65ee7-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="65ee7-112">ERCdsFeature</span></span>
      - <span data-ttu-id="65ee7-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="65ee7-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="65ee7-114">Í Finance skal fara á vinnusvæðið **Eiginleikastjórnun** og virkja eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="65ee7-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="65ee7-115">(Forútgáfa) Stuðningur við Dataverse gagnagjafa rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="65ee7-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="65ee7-116">(Forútgáfa) Stuðningur við gagnagjafa skattþjónustu Dataverse</span><span class="sxs-lookup"><span data-stu-id="65ee7-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="65ee7-117">(Forskoðun) Altækir eiginleikar</span><span class="sxs-lookup"><span data-stu-id="65ee7-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="65ee7-118">Skráðu þig inn í RCS með stjórnandareikningi leigjanda.</span><span class="sxs-lookup"><span data-stu-id="65ee7-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="65ee7-119">Farðu í **Rafræn skýrslugerð** > **Tengd forrit**.</span><span class="sxs-lookup"><span data-stu-id="65ee7-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="65ee7-120">Veldu **Ný** til að bæta við færslu og færðu inn eftirfarandi reitarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="65ee7-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="65ee7-121">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="65ee7-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="65ee7-122">Í reitnum **Tegund** skal velja **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="65ee7-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="65ee7-123">Í reitinn **Forrit** skal slá inn Dataverse vefslóð.</span><span class="sxs-lookup"><span data-stu-id="65ee7-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="65ee7-124">Í reitinn **Leigjandi** skal slá inn leigjandann.</span><span class="sxs-lookup"><span data-stu-id="65ee7-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="65ee7-125">Í reitinn **Sérsniðin vefslóð** skal slá inn Dataverse vefslóðina og bæta við hana „/api/data/v9.1“.</span><span class="sxs-lookup"><span data-stu-id="65ee7-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="65ee7-126">Veldu **Athuga tengingu** og ljúktu við tengingarferlið.</span><span class="sxs-lookup"><span data-stu-id="65ee7-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="65ee7-127">[![Athuga tengihnapp](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="65ee7-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="65ee7-128">Farðu í **Rafræn skýrslugerð** > **Skattaskilgreiningar** og flyttu inn skattaskilgreiningar úr [Skattaskilgreiningar](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="65ee7-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="65ee7-129">[![Síða skattaskilgreiningar, tré skattgagnalíkans](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="65ee7-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="65ee7-130">Farður í **Vörpun skattskylds skjallíkans** eða **Dataverse líkanavörpun** ef þú ert að nota skilgreiningu Microsoft og í reitnum **Tengt forrit** skal velja færsluna sem var búin til í skrefi 7.</span><span class="sxs-lookup"><span data-stu-id="65ee7-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="65ee7-131">Stilltu **Sjálfgefið fyrir líkanavörpun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="65ee7-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="65ee7-132">[![Síða líkanavörpunar](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="65ee7-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

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
ms.openlocfilehash: 348643d7213b8c053d6a15b4b716a3ce75ba2fa2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346375"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Setja upp umhverfi fyrir uppflettingar aðalgagna

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp umhverfið til að nota uppflettingarvirkni fyrir aðalgögn skattaútreiknings.

1. Setja upp samþættingu Power Platform í Lifecycle Services (LCS). Frekari upplýsingar er að finna í [Microsoft Power Platform samþætting - Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Setja upp Dynamics 365 Finance og Microsoft Dataverse. Frekari upplýsingar er að finna í [Lausnin sótt](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Sannvottun og leyfisveiting](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Setjið upp eftirfarandi einingar. Frekari upplýsingar eru í [Virkjun sýndareininga](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressCityEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeading
      - VendVendorV2Entity
4. Setjið upp Dynamics 365 Regulatory Configuration Service (RCS). 
5. Stofnið þjónustubeiðni fyrir Microsoft til að virkja tilraunaútgáfu á eftirfarandi eiginleikum:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Farið á vinnusvæðið **Eiginleikastjórnun** og virkið eftirfarandi eiginleika:

      - (Forútgáfa) Stuðningur við Dataverse gagnagjafa rafrænnar skýrslugerðar
      - (Forútgáfa) Stuðningur við gagnagjafa skattþjónustu Dataverse
      - (Forskoðun) Altækir eiginleikar

5. Skráðu þig inn í RCS með stjórnandareikningi leigjanda.
6. Farðu í **Rafræn skýrslugerð** > **Tengd forrit**. 
7. Veldu **Ný** til að bæta við færslu og færðu inn eftirfarandi reitarupplýsingar. 

   - Færið inn lýsandi nafn í reitinn **Heiti**.
   - Í reitnum **Tegund** skal velja **Dataverse**.
   - Í reitinn **Forrit** skal slá inn Dataverse vefslóð.
   - Í reitinn **Leigjandi** skal slá inn leigjandann.
   - Í reitinn **Sérsniðin vefslóð** skal slá inn Dataverse vefslóðina og bæta við hana „/api/data/v9.1“.

8. Veldu **Athuga tengingu** og ljúktu við tengingarferlið. 

   [![Hnappurinn Athuga tengingu.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Farðu í **Rafræn skýrslugerð** > **Skattaskilgreiningar** og flyttu inn skattaskilgreiningar úr [Skattaskilgreiningar](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Síða skattaskilgreiningar, tré skattgagnalíkans.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Farður í **Vörpun skattskylds skjallíkans** eða **Dataverse líkanavörpun** ef þú ert að nota skilgreiningu Microsoft og í reitnum **Tengt forrit** skal velja færsluna sem var búin til í skrefi 7.
11. Stilltu **Sjálfgefið fyrir líkanavörpun** á **Já**.

   [![Síða líkanavörpunar.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Setja upp umhverfi fyrir uppflettingar aðalgagna
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp umhverfið til að nota uppflettingarvirkni fyrir aðalgögn skattaútreiknings.
author: kai-cloud
ms.date: 10/26/2021
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
ms.openlocfilehash: 901f8bcb0220355866952b68e92bc2dd906bb430
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700405"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Setja upp umhverfi fyrir uppflettingar aðalgagna

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp umhverfið til að nota uppflettingarvirkni fyrir aðalgögn skattaútreiknings.

1. Settu upp Microsoft Power Platform samþættingu í Microsoft Dynamics Lifecycle Services (LCS). Frekari upplýsingar er að finna í [Microsoft Power Platform samþætting - Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Eftir að þessu skrefi er lokið birtist heitið á Microsoft Power Platform umhverfi í hlutanum **Power Platform Samþætting**.
2. Farðu í [Microsoft Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com/environments) og veldu heiti umhverfisins. Vefslóð umhverfis er gefin upp.
3. Setja upp Dynamics 365 Finance og Dataverse. Frekari upplýsingar er að finna í [Lausn sýndareiningar sótt](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) og [Sannvottun og leyfisveiting](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Setjið upp eftirfarandi einingar. Frekari upplýsingar er að finna í [Virkja Microsoft Dataverse sýndareiningar](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

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

5. Settu upp Regulatory Configuration Service (RCS). Farðu á vinnusvæðið **Eiginleikastjórnun** og virkjaðu eftirfarandi eiginleika:

    - Stuðningur við Dataverse gagnagjafa rafrænnar skýrslugerðar
    - Stuðningur við gagnagjafa skattþjónustu Dataverse
    - Altækir eiginleikar

6. Skráðu þig inn í RCS með stjórnandareikningi leigjanda.
7. Farðu í **Rafræn skýrslugerð** > **Tengd forrit**. 
8. Veldu **Ný** til að bæta við færslu og færðu inn eftirfarandi reitarupplýsingar. 

    - Færið inn lýsandi nafn í reitinn **Heiti**.
    - Í reitnum **Tegund** skal velja **Dataverse**.
    - Í reitinn **Forrit** skal slá inn Dataverse vefslóð.
    - Í reitinn **Leigjandi** skal slá inn leigjandann.
    - Í reitinn **Sérsniðin vefslóð** skal slá inn Dataverse vefslóðina og bæta við hana „/api/data/v9.1“.

9. Veldu **Athuga tengingu** og ljúktu við tengingarferlið. 

    [![Hnappurinn Athuga tengingu.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Farðu í **Rafræn skýrslugerð** > **Skattaskilgreiningar** og flyttu inn skattaskilgreiningar úr [Skattaskilgreiningar](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Síða skattaskilgreiningar, tré skattgagnalíkans.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Farður í **Vörpun skattskylds skjallíkans** eða **Dataverse líkanavörpun** ef þú ert að nota skilgreiningu Microsoft og í reitnum **Tengt forrit** skal velja færsluna sem var búin til í skrefi 7.
12. Stilltu **Sjálfgefið fyrir líkanavörpun** á **Já**.

    [![Síða líkanavörpunar.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

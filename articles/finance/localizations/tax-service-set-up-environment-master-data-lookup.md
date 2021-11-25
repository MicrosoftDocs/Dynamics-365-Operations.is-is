---
title: Virkja aðalgagnauppflettingu fyrir skattaútreikningsstillingar
description: Þetta efnisatriði útskýrir hvernig á að setja upp og virkja uppflettivirkni skattaútreiknings aðalgagna.
author: kai-cloud
ms.date: 11/03/2021
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
ms.openlocfilehash: dafeac01aaff62cbbd5ce6ecb0af0ef111f513b2
ms.sourcegitcommit: 76fe020f9c5f4e5cc2e93f5ccb3b040f12b0363e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2021
ms.locfileid: "7749511"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Virkja aðalgagnauppflettingu fyrir skattaútreikningsstillingar 

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp og virkja uppflettivirkni skattaútreiknings aðalgagna. Fellilisti er tiltækur til að velja gildi í skattreikningsskilgreiningu fyrir reiti eins og **Reikningur söluaðila**, **·**, og **Afhendingartími**. Þessi gildi koma frá tengdu Microsoft Dynamics 365 Finance umhverfi með því að nota Microsoft Dataverse gagnaheimild.

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

    [![ Hnappurinn Athuga tengingu.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Farðu í **Rafræn skýrslugerð** > **Skattaskilgreiningar** og flyttu inn skattaskilgreiningar úr [Skattaskilgreiningar](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![ Síða skattaskilgreiningar, tré skattgagnalíkans.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Farður í **Vörpun skattskylds skjallíkans** eða **Dataverse líkanavörpun** ef þú ert að nota skilgreiningu Microsoft og í reitnum **Tengt forrit** skal velja færsluna sem var búin til í skrefi 7.
12. Stilltu **Sjálfgefið fyrir líkanavörpun** á **Já**.

    [![ Síða líkanavörpunar.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

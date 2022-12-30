---
title: Samþætta Dynamics 365 Supply Chain Management (eignastýringu) við Dynamics 365 Guides
description: Í þessari grein er útskýrt hvernig á að samþætta einingu eignastýringar í Microsoft Dynamics 365 Supply Chain Management við Dynamics 365 Guides til að nýta leiðarvísa blandaðs veruleika í daglegum þjónustu- og viðhaldsverkflæðum.
author: johanhoffmann
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d06978bcbd6205111384f5c7cefdf34fdbdbfbf5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875685"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Samþætta Dynamics 365 Supply Chain Management (eignastýringu) við Dynamics 365 Guides

[!include [banner](../includes/banner.md)]

Hægt er að samþætta eininguna **Eignastýring** í Microsoft Dynamics 365 Supply Chain Management við Dynamics 365 Guides til að nýta leiðarvísa blandaðs veruleika í daglegum þjónustu- og viðhaldsverkflæðum. Ef leiðarvísir er tengdur verkbeiðni eignastýringar, sér starfsmaður sem opnar viðhaldsgátlista verkbeiðni í farsímaforriti Supply Chain Management (Dynamics 365) að leiðarvísir er í boði. Starfsmaðurinn getur þá fundið og opnað leiðarvísinn í Dynamics 365 Guides HoloLens forritinu.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að hengja leiðarvísa við verkbeiðnir eignastýringar þarf að uppfylla þessi skilyrði:

- [Setja upp Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) útgáfa 10.0.9 eða nýrri.
- [Kveikja á tvískiptum skrifum fyrir forrit Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Kveikja á forútgáfu](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) fyrir eiginleikann **MRGuidesFeature**. (Fyrir vinnsluumhverfi þarf fyrst að senda inn þjónustubeiðni til að leigjandanum þínum verði bætt við forútgáfuhópinn.)
- [Kveikja á eftirfarandi skilgreiningarlyklum](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) á síðunni **Leyfisskilgreining**:

    - Bandaður veruleiki eignarstýringar fyrir \> eignastýringu
    - Leiðarvísir blandaðs veruleika fyrir blandaðan veruleika \>

- [Setja upp Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) útgáfa 200.0.0.96 eða nýrri.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Nota Dynamics 365 Guides með eignastýringu

Til að tengja leiðarvísi er notuð lína viðhaldsgátlista í eignastýringu. Hægt er að stofna tenginguna í gegnum sniðmát viðhaldsgátlista, gerð viðhaldsverks eða verkbeiðni af því að þetta þrennt inniheldur línur viðhaldsgátlista. Hægt er að spara tíma með því að nota sniðmát því að hægt er að tengja sniðmát við allar gerðir viðhaldsverka sem nota það. Til dæmis er leiðarvísi sem tengist viðhaldsverkgerð sjálfkrafa tengdur við allar verkbeiðnir sem heyra undir þessa verkgerð. Hins vegar er leiðarvísi sem tengist ákveðinni verkbeiðni aðeins til fyrir þá verkbeiðni.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Tengja leiðarvísi við sniðmát viðhaldsgátlista

Til að tengja leiðarvísi við sniðmát viðhaldsgátlista skal fylgja þessum skrefum.

1. Búðu til leiðarvísi með því að nota Dynamics 365 Guides tölvuna og HoloLens forritin. Nánari upplýsingar um hvernig á að búa til leiðarvísi er að finna í eftirfarandi greinum:

    - [Notaðu tölvuforritið til að búa til leiðarvísi](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Nota HoloLens-forritið til að staðsetja heilmyndirnar](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. Í Supply Chain Management skal [búa til sniðmát viðhaldsgátlista](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Tengið leiðarvísinn sem var búinn til við línu viðhaldsgátlista í nýju sniðmáti viðhaldsgátlista:

    1. Í flýtiflipanum **Línur viðhaldsgátlista** skal velja línuna sem á að tengjast leiðarvísinum.
    1. Í flýtiflipanum **Tengdir leiðarvísar** skal velja **Bæta við leiðarvísi**.

        ![Tengja leiðarvísi við línu viðhaldsgátlista.](media/am-guides-integration-add-guide.png "Tengja leiðarvísi við línu viðhaldsgátlista")

    1. Í reitnum **Heiti** skal velja leiðarvísi og síðan velja **Vista**.

        ![Velja leiðarvísi í reitnum Heiti.](media/am-guides-integration-select-guide.png "Velja leiðarvísi í reitnum Heiti")

1. Tengið sniðmát viðhaldsgátlista við gerð verks:

    1. [Búa til gerð viðhaldsverks](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) eða velja fyrirliggjandi gerð viðhaldsverks.
    1. Á aðgerðasvæðinu skal velja **Sjálfgefnar gerðir viðhaldsverks**.

        ![Hnappur fyrir sjálfgefna gerð viðhaldsverks.](media/am-guides-integration-job-defaults.png "Hnappur sjálfgildis gerða viðhaldsverks")

    1. Stofnaðu línu og veldu síðan **Vista**.

        ![Stofna línu.](media/am-guides-integration-add-line.png "Stofna línu")

    1. Á aðgerðasvæðinu skal velja **Viðhaldsgátlisti**.

        ![Viðhaldsgátlistahnappur.](media/am-guides-integration-maintenance-checklist.png "Viðhaldsgátlistahnappur")

    1. Í flýtiflipanum **Viðhaldsgátlisti** skal bæta við línu og síðan breyta gildinu í reitnum **Gerð** í **Sniðmát**.

        ![Breyta gildisgerð.](media/am-guides-integration-checklist-lines.png "Breyta gildisgerð")

    1. Í flýtiflipanum **Upplýsingar um línu**, í reitnum **Sniðmát**, skal velja sniðmátið sem þú tengdir leiðarvísinn við og velja síðan **Vista**.

        ![Velja sniðmát.](media/am-guides-integration-checklist-line-details.png "Velja sniðmát")

1. [Búa til verkbeiðni](work-orders/manually-created-workorders.md#create-work-order) og veldu síðan gerð viðhaldsverks sem notar sniðmát viðhaldsgátlista sem þú tengdir leiðarvísinn við. Leiðarvísirinn tengist sjálfkrafa verkbeiðninni.

    ![Velja gerð viðhaldsverks.](media/am-guides-integration-create-work-order.png "Velja gerð viðhaldsverks")

1. Skoðaðu leiðarvísinn sem tengist verkbeiðni og starfmönnum:

    1. Opnaðu [Fartækjavinnusvæði eignastýringar](asset-management-mobile-workspace.md) til að fá aðgang að verkbeiðninni.
    1. [Opnaðu viðhaldsgátlistann](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) fyrir verkbeiðnina.
    1. Veldu gátlistalínu til að sjá tengdan leiðarvísi.

        ![Leiðarvísir sem tengist gátlistalínu.](media/am-guides-integration-show-guide.png "Leiðbeiningar sem tengjast gátlistalínu")

    1. Opna leiðarvísi á HoloLens.

        ![Opna leiðarvísi á HoloLens.](media/am-guides-integration-hololens-select.png "Opna leiðarvísi á HoloLens")

> [!NOTE]
> Einnig er hægt að tengja leiðarvísi beint í viðhaldsgátlista verkbeiðni eða verkgerðar.

> [!IMPORTANT]
> Þekkt vandamál er til staðar þar sem sniðmát fyrir viðhaldsgátlista er tengt við sjálfgefna viðhaldsverkgerð, leiðarvísirinn sem tengist sniðmátinu birtist ekki í flýtiflipanum **Tengdir leiðarvísar** á síðunni **Sjálfgefnar gerðir viðhaldsverks**. Leiðarvísirinn birtist hins vegar eftir að verkgerð er sett á verkbeiðni í flýtiflipanum **Tengdir leiðarvísar**.

## <a name="see-also"></a>Sjá einnig

- [Tvöföld skrif – yfirlit](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Yfirlit eignastýringar](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
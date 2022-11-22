---
title: Vinna úr færslubók fjárhagsúthlutunar
description: Þessi grein útskýrir hvernig á að vinna úr úthlutunarbeiðni í Dynamics 365 Finance.
author: aprilolson
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779393"
---
# <a name="process-ledger-allocation-journal"></a>Vinna úr færslubók fjárhagsúthlutunar

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að vinna úr úthlutunarbeiðni. Nota **Ferlið úthlutunarbeiðni** síðu til að búa til úthlutunarbók sem hægt er að skoða og samþykkja áður en bókað er í fjárhag, eða bóka beint í fjárhag. Áður en hægt er að stofna úthlutunarfærslubók verður að vera að minnsta kosti ein virk úthlutunarregla fjárhags. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Í yfirlitsrúðunni, farðu í **Fjárhagur > Úthlutanir > Vinnsla úthlutunarbeiðni**.
2. Í reitnum **Regla** velurðu skrána sem óskað er eftir af fellilistanum.
3. Í reitnum **Frá og með dagsetningu** er dagsetning færð inn.

    - **Frá og með dagsetningu** er mjög mikilvægt þegar Fjárhagur er gagnagjafi fyrir regluna. Þessi dagsetning stýrir hvaða fjárhagsstöðu á að taka með í úthlutun.  
    - Í reitnum **Núll** velurðu **Stöðva**. Þetta mun stöðva úthlutunarferlið og birta skilaboð um að núll upprunaupphæð sé valin.  

4. Í reitnum **Valkostir tillögu** skal velja **Aðeins tillaga**. Veldu **Aðeins tillaga** að fara yfir og mögulega samþykkja niðurstöðuna í **Úthlutunardagbækur** áður en úthlutun er bókuð í fjárhag.  
5. Í **GL færsludagur** reit, sláðu inn dagsetningu.
6. Veljið **Í lagi**.
7. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Úthlutanir > Úthlutunarbækur**.
8. Veldu **Línur**.
9. Veldu **Bóka**.
10. Veldu **Bóka**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Vinna úr færslubók kostnaðarúthlutunar
description: Þetta efni útskýrir hvernig á að vinna úr úthlutunarbeiðni í Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d37b1a9869cc130786d0e8fde68184e04c881bad1f64c86943174213025db82
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765669"
---
# <a name="process-ledger-allocation-journal"></a>Vinna úr færslubók kostnaðarúthlutunar

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að vinna úr úthlutunarbeiðni. Notaðu síðuna Vinna úr úthlutunarbeiðni til að stofna úthlutunarbók sem hægt er að yfirfara og samþykki áður en bókað er í Fjárhag eða bóka beint í Fjárhag. Áður en hægt er að stofna úthlutunarfærslubók verður að vera að minnsta kosti ein virk úthlutunarregla fjárhags. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Úthlutanir > Vinna úthlutunarbeiðni**.
2. Í reitnum **Regla** velurðu skrána sem óskað er eftir af fellilistanum.
3. Í reitnum **Frá og með dagsetningu** er dagsetning færð inn.

    - **Frá og með dagsetningu** er mjög mikilvægt þegar Fjárhagur er gagnagjafi fyrir regluna. Þessi dagsetning stýrir hvaða fjárhagsstöðu á að taka með í úthlutun.  
    - Í reitnum **Núll** velurðu **Stöðva**. Þetta mun stöðva úthlutunarferlið og birta skilaboð um að núll upprunaupphæð sé valin.  

4. Í reitnum **Valkostir tillögu** skal velja **Aðeins tillaga**. Veldu **Aðeins tillaga** til að endurskoða og samþykkja niðurstöðu í úthlutunarbókum áður en úthlutunin er bókuð í Fjárhag.  
5. Dagsetning er rituð í reitinn Bókunardagsetning fjárhags.
6. Veljið **Í lagi**.
7. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Úthlutanir > Úthlutunarbækur**.
8. Veldu **Línur**.
9. Veldu **Bóka**.
10. Veldu **Bóka**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
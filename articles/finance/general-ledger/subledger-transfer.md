---
title: Flutningur undirbókar í fjárhag
description: Þessi grein lýsir eiginleikum sem tengjast flutningsferli undirbókar í fjárhag.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7ef93b81ce37128f7ff400eb4034ffea01756038
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779854"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Flutningur undirbókar í fjárhag

[!include [banner](../includes/banner.md)]

Þessi grein lýsir möguleikum sem tengjast reglum um að flytja runur af undirbókarfærslum.

Í útgáfu 8.1 voru gerðar breytingar til að leyfa flutning á reglum sem úreltu valkostinn **Samstillt**. Fyrir frekari upplýsingar, sjá [Fjarlægðir eða úreltir eiginleikar fyrir fjármál og rekstur](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Eftirfarandi valkostir eru í boði til að flytja runur undirbókar:

- **Ósamstilltur** - Flutningur á bókhaldsfærslum undirbókar í fjárhagsbók er áætluð strax. Fylgiskjal fjárhags verður skráð um leið og úrræði eru í boði til að afgreiða beiðnina á netþjóninum.
- **Áætluð runa** – Bókhaldsfærslur undirbókar sem þarf að flytja er bætt við vinnsluröðina í fjárhagsbók. Færslurnar í röðinni verða afgreiddar í þeirri röð sem þær eru mótteknar. Hvert fylgiskjal fjárhags mun uppfæra lykla á áætluðum tíma ef tilföng eru í boði til að afgreiða runuvinnsluna á netþjóninum.

Endurbætur voru gerðar til að auka frammistöðu félagsins **Ósamstilltur** valmöguleika. Þessi aðgerð er gerð virk undir nafni eiginleikans **Flutningur undirliða yfir í hagræðingu almenns fjárhags**.

Virknin fyrir ósamstilltan flutning á runum undirbókar hjálpar til við að flytja gögn úr undirbók í fjárhag. Með því að flokka saman safn af minni færslum og flytja færslurnar í hópum afgreiðir virknin færslur á skilvirkari hátt. Þegar færslur eru flokkaðar eru tilföng runuþjónsins notuð á skilvirkari hátt.

Ósamstilltur flutningur á undirbókarlotum krefst þess að runuþjónninn sé settur upp, á netinu og virki vegna þess að runuverkefni eru búin til til að framkvæma strax á runuþjóninum. Þegar **Flutningur undirbókar yfir í hagræðingu á afköstum aðalbókar** eiginleiki er virkur, the **Sjálfvirkni ferlisins** kerfislotuvinna nefnd **Vinnu sjálfvirkni í atkvæðagreiðslukerfi** verður einnig að vera virkt. Frekari upplýsingar er að finna í [Sjálfvirkni ferlis](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Breyting á skilvirkni á runustigi notar eina endurtekna runuvinnslu fyrir alla lögaðila í kerfinu. Á keyrslutíma er ný runuvinnsla stofnuð til að afgreiða nauðsynlegar færslur sem hafa ekki verið fluttar. Hægt er að stýra fleiri stillingum á síðunni **Sjálfvirkni ferlis** í kerfisstjórnun. Á þeirri síðu er hægt að breyta bakgrunnsvinnslunni, breyta tíðninni og skilgreina hvíldartíma.

Frekari upplýsingar um uppsetningu á sjálfvirkni ferlis er að finna í [Sjálfvirkni ferlis](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


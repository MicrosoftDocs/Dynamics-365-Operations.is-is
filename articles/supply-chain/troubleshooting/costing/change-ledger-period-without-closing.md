---
title: Viðvaranir eða villur þegar skipt er um stöðu fjárhagstímabils án lokunar birgða
description: Viðvaranir eða villur þegar skipt er um stöðu fjárhagstímabils án lokunar birgða
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476646"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Viðvaranir eða villur þegar skipt er um stöðu fjárhagstímabils án lokunar birgða

Microsoft kynnti eftirfarandi villuleit til að koma í veg fyrir vandamál sem stafa af röngu endaferli tímabils í kostnaðarútreikningi. Þegar einhver af eftirfarandi villuboðum koma upp finnur þú frekari upplýsingar í [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) um hvernig eigi að leysa úr þessum vandamálum.

- Þú ert að fara að framkvæma endurútreikning með dagsetningu %1 (02-10-2019). Síðasti skráði endurútreikningur var keyrður á fyrra tímabili með dagsetningu %2 (20-01-2019). Engin keyrsla á birgðalokun með dagsetningu %3 (31-01-2019) sem samsvarar tímabilslokum hefur verið skráð. Mundu að keyra birgðalokun frá %3 (31-01-2019) sem samsvarar lokum tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt.

- Þú ert að fara að breyta stöðu fjárhagstímabils %1 í %2. Engin lok birgðalokunaráætlunar með dagsetningu %3 samsvarandi tímabils hefur verið skráð. Munið að keyra birgðalokun frá %3 sem samsvarar lokum tímabilsins áður en stöðunni er breytt. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt. Tilkynnt frá lögaðila %4. Þetta er aðeins til upplýsinga eins og er en þú þarft að framkvæma slíka aðgerð í framtíðinni.

- Lykilskipulaginu %1 hefur verið breytt. Einn eða fleiri aðallyklar %2 eru ekki lengur til. Þessir aðallyklar eru nauðsynlegir af %3 með %4 dagsetningu. Bæta skal þessum aðallyklum við lykilskipulagið %1 áður en hægt er að halda áfram í %3 vinnslunni. Þetta er aðeins til upplýsinga eins og er en þú þarft að framkvæma slíka aðgerð í framtíðinni.

- Þú ert að fara að framkvæma birgðalokun með dagsetningu %1 (31-01-2019). Engin keyrsla á bakfærslukostnaðaraðferð útreiknings með dagsetningu %2 (31-01-2019) sem samsvarar tímabilslokum hefur verið skráð. Munið að keyra bakfærslukostnaðaraðferð með dagsetningu á %3 (31-01-2019) sem samsvarar lokun tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt.

- Þú ert að fara að framkvæma útreikning bakfærslukostnaðaraðferðar með dagsetningu %1 (28-02-2019). Síðasti skráði útreikningur bakfærslukostnaðaraðferðar var keyrður á fyrra tímabili með dagsetningu %2 (31-01-2019). Engin keyrsla á birgðalokun með dagsetningu %3 (31-01-2019) sem samsvarar lokum tímabils hefur verið skráð.

Munið að keyra birgðalokun frá %3 (31-01-2019) sem samsvarar lokum tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en birgðalokun hefur verið keyrð.
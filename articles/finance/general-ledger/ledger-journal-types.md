---
title: Færslubókargerðir fjárhags
description: Þetta grein lýsir þær gerðir færslubóka sem hægt er að setja upp fyrir fjárhagsbækur.
author: kweekley
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 883c54b84ed31384a28c31c8b814c75d340d020e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901314"
---
# <a name="ledger-journal-types"></a>Færslubókargerðir fjárhags

[!include [banner](../includes/banner.md)]

Þetta grein lýsir þær gerðir færslubóka sem hægt er að setja upp fyrir fjárhagsbækur. Nota **Dagbókarnöfn** síðu til að setja upp færslubækur sem þú getur notað í gegnum Dynamics 365 Finance.

| Færslubókargerð                      | Notkun                       | Færa inn færslur á þessari síðu                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Úthlutun                        | Stofna úthlutun færslur í færslubók. Áður en hægt er að stofna úthlutunarbók verður að stofna úthlutunarreglu í síðunni **úthlutunarregla fjárhags**      | Vinna úr beiðni um úthlutun             |
| Samþykki                          | Bóka samþykkta reikninga lánardrottna í rétta fjárhagslykla.  | Staðfestingarbók                                       |
| Bakfærsla bankaávísunar               | Bakfæra bókaða ávísun. Til að nota þessa færslubókargerð, veldu **Nota endurskoðunarferlið fyrir greiðslubakfærslur** valkosturinn á **færibreytur reiðufjár- og bankastjórnun**.   | Athuga Bakfærslur, bakfærsla Greiðslu                   |
| Ógilding bankainnborgunarseðils    | Hætta við innborgunarseðill. Til að nota þessa færslubókargerð, veldu **Nota endurskoðunarferlið fyrir greiðslubakfærslur innborgunarseðils** valkosturinn á **færibreytur reiðufjár- og bankastjórnun**.   | Ógildingar á greiðslum bankainnborgunarseðla            |
| Fjárhagsáætlun                            | Vinna úr fjárveitingar úr fjárhagsáætlun Til að nota þessa gerð færslubók, velja á **Leyfa fjárveitingu fjárhagsáætlunar** valkostinn á í **fjárhagsfæribreytur** síðu. Færslur í fjárhagsáætlunarbók hafa með upplýsingar á grundvelli fjárhagslykla sem eru skilgreindar í á **bókunarskilgreiningar** síðu.                                                        |                                                                |
| Viðskiptavinasamþykki víxils  | Stofna samþykktarfærslur viðskiptavina fyrir víxla.             | Gefa út víxlabók– endurútgefa víxlabók. |
| Greiðslusending viðskiptavinar          | Stofna greiðsluskrá víxils sem má senda til banka fyrirtækisins. Til að nota þessa gerð færslubókar, hreinsa í **Sjálfvirka jöfnun** valkostinn á í **viðskiptakrafna** **færibreytur** síðu.            | Greiðsla                                                     |
| Viðskiptavinaútgáfa víxils    | Stofna viðskiptavinaútgáfu víxils. Til að nota þessa færslubókargerð, hreinsa valkostinn **Stofna og bóka útgáfubók sjálfvirkt við bókun reikninga** á síðunni **greiðsluaðferð**   | Víxilútgáfubók                                  |
| Greiðsla viðskiptavinar                  | Stofna greiðslufærslur viðskiptavina.                             | Greiðslubók             |
| Viðskiptavinaafsögn víxils | Stofna færslur viðskiptavinaafsögn víxils.                    | Víxilafsagnabók                               |
| Viðskiptavinaendurútgáfa víxils  | Stofna færlsur viðskiptavinaendurútgáfa víxils.                     | Víxilendurútgáfubók                                |
| Viðskiptavinauppgjör víxils  | Stofna færslur viðskiptavinauppgjör víxils.                       | Jafna víxlabók                                |
| Daglega                             | Stofna daglegar færslur í almennri færslubók.                          | Almenn færslubók                                                |
| Útilokun                       | Stofna losunarfærslur í losunarbók. Til að nota þessa færslubókargerð, veldu **Nota fyrir losunarferli fjárhags** og **Nota fyrir sameiningarferli fjárhags** valkostina á síðunni **lögaðilar**. Stofna verður losunarreglu fjárhags í **losunarregla fjárhags** síður, áður en hægt er að nota þessa gerð færslubókar. | Útilokun                                                    |
| Eignaáætlun                | Stofna færslur í færslubækur eignaáætlunar.                                                                                                                                                                                                                                                                                                                 | Eignaáætlun                                             |
| Komubók                  | Skrá grunnupplýsingar um reikninga lánardrottins.                                                                                                                                                                                                                                                                                                           | Komubók                                               |
| Launagreiðsla              | Gefa út greiðslur byggðar á launayfirlitum. Hægt er að færa færslur handvirkt í þessari færslubók. Búa til launayfirlit og senda svo þær uppgjör fyrir greiðslu.                                                                                                                                                              |                                                                |
| Reglubundið                          | Stofna reglubundnar færslur fyrir tímabilsbók.                                                                                                                                                                                                                                                                                                      | Tímabilsbækur                                              |
| Bóka eignir                 | Bóka eignafærslur.                                                                                                                                                                                                                                                                                                                              | Eignir                                                   |
| Verk - Kostnaður                | Stofna útgjaldafærslur verks.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Leiðrétting skýrslugjaldmiðils     | Búðu til leiðréttingar í skýrslugjaldmiðlinum fyrir stöður á fjárhagslyklinum.               | Leiðréttingabækur skýrslugjaldmiðils                         |
| Talnagagnafærslur            | Stofna færslur fyrir vinnslu.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Greiðslusending lánardrottins            | Stofna eigin greiðsluskrá sem má senda til banka fyrirtækisins.                                                                                                                                                                                                                                                                      | Greiðslubók                                             |
| Greiðsla til lánardrottins               | Stofna færslur greiðslu til lánardrottins                                                                                                                                                                                                                                                                                                                    | Greiðslubók                                                |
| Gefa út eigin víxil lánardrottins       | Gefa út eigin víxla lánardrottins sem greiðsluhátt. Til að nota þessa færslubókargerð, hreinsa valkostinn **Stofna og bóka útgáfubók sjálfvirkt við bókun reikninga** á síðunni **greiðsluaðferð - lánardrottnar**                                                                                                                                          | Gefa út eigin víxilbók                                   |
| Reikningahópur lánardrottins utan bókunar | Stofna færslur reiknings lánardrottins sem hafa ekki enn verið bókaðar í tímabundinn komulykil.                                                                                                                                                                                                                                                             | Reikningahópur lánardrottins án bókunarupplýsinga                  |
| Reikningasafn lánardrottna               | Stofna færslur reikningasafns lánardrottna                                                                                                                                                                                                                                                                                                                    |                                                                |
| Skráning reiknings frá lánardrottni          | Bóka lánardrottnareikninga sem eru í færslubók.                                                                                                                                                                                                                                                                                                                 | Reikningabók                                                |
| Lánardrottnaendurútgáfa eigin víxils     | Endurútgefa eigin víxil sem áður hefur verið samþykktur af banka fyrirtækis þíns.                                                                                                                                                                                                                                                                      | Endurútgáfubók eigin víxla                                 |
| Lánardrottinn jafnar eigin víxil     | Stofna færslur jöfnunar lánardrottins á eigin víxli.                                                                                                                                                                                                                                                                                                          | Jafna eigin víxilbók                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

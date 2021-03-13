---
title: Endurgreiða viðskiptavini
description: Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum. Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6a3078743fc9cd43c71bc1d4531c0553ee53bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012140"
---
# <a name="reimburse-customers"></a>Endurgreiða viðskiptavini

[!include [banner](../includes/banner.md)]

Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum. Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar. 

Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.

| Skilyrði                                                            | Lýsing |
|-------------------------------------------------------------------------|-------------|
| Tilgreina lágmarks endurgreiðsluupphæð fyrir lögaðilann          | Á **Færibreytur viðskiptakrafna** síðunni, á svæðinu **Almennt** á **Lágmarks endurgreiðsla** svæðinu, færið inn lágmarksupphæð sem hægt er að endurgreiða fyrir°ofgreiðslu viðskiptavinar. |
| Valfrjálst: Bæta lánardrottnareikningi við hvern viðskiptavin sem er hægt að endurgreiða. | Á°síðunni **Viðskiptavinir** í flýtiflipanum **Ýmsar upplýsingar** á svæðinu **Lánardrottnalykill** skal°velja lánardrottnalykilinn fyrir viðskiptavin. |

Þegar endurgreiðslufærslur eru stofnaðar, er reikningur lánardrottins stofnaður fyrir upphæð kreditstöðunnar. Endurgreiðsluferlið°fjarlægir kreditstöðu fyrir viðskiptavinalykilinn og stofnar stöðu greiðslu fyrir lykil lánardrottins sem samsvarar viðskiptavininum.

1. Í viðskiptakröfur, keyrið ferlið **Endurgreiðsla**. (**Vinna úr viðskiptakröfur \> Reglubundin verkefni \> Endurgreiðsla**).
2. Til að flokka allar færslur, án tillits til fjárhagsvíddar, skal stilla valkostinn **Taka saman fyrir viðskiptavin** á **Já**. Til að flokka aðeins færslur sem eru með svipaðar fjárhagsvíddir skal stilla valkostinn á **Nei**.
3. Veljið **Hafa með viðskiptavini með útistandandi debetfærslur** til að velja viðskiptamenn sem eru með ójafnaðar debetupphæðir.
4. Til að endurgreiða tiltekna viðskiptavinalykla skal opna flýtiflipann **Færslur til að taka með** og velja **Sía** og tilgreina síðan viðskiptavinalykla í fyrirspurninni.

    Kreditupphæðir eru fluttar í lánardrottnarlykla viðskiptavinar og eru unnar eins og venjulegar greiðslur. Ef viðskiptamaður er ekki með lánardrottnarlykil er sjálfkrafa búið til númer einsskiptislánardrottins handa viðskiptamanninum.

5. Til að skoða endurgreiðslufærslur sem voru stofnaðar, skal nota skýrsluna **Endurgreiðsla** (**Viðskiptakröfur \> Fyrirspurnir og skýrslur \> Endurgreiðsluskýrsla**).
6. Í Viðskiptaskuldir, stofnið greiðslu fyrir reikninga lánardrottins sem voru stofnaðir sem afleiðing af endurgreiðsluferlinu. Upplýsingar um hvernig greiða á lánardrottnum er að finna í [Yfirlit yfir greiðslu lánardrottins](../accounts-payable/Vendor-payments-workspace.md).

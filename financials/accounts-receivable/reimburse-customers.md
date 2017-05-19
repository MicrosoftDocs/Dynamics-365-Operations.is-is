---
title: "Endurgreiða viðskiptavini"
description: "Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum. Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f8a46f5d961ff7629db7f9af8f3955ddfc338736
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="reimburse-customers"></a>Endurgreiða viðskiptavini

[!include[banner](../includes/banner.md)]


Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum. Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar. 

Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.

| Skilyrði                                                            | Lýsing                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tilgreina lágmarks endurgreiðsluupphæð fyrir lögaðilann          | Á **Færibreytur viðskiptakrafna** síðunni, á svæðinu **Almennt** á **Lágmarks endurgreiðsla** svæðinu, færið inn lágmarksupphæð sem hægt er að endurgreiða fyrir°ofgreiðslu viðskiptavinar. |
| Valfrjálst: Bæta lánardrottnareikningi við hvern viðskiptavin sem er hægt að endurgreiða. | Á°síðunni **Viðskiptavinir** í flýtiflipanum **Ýmsar upplýsingar** á svæðinu **Lánardrottnalykill** skal°velja lánardrottnalykilinn fyrir viðskiptavin.                                           |

Þegar endurgreiðslufærslur eru stofnaðar, er reikningur lánardrottins stofnaður fyrir upphæð kreditstöðunnar. Endurgreiðsluferlið°fjarlægir kreditstöðu fyrir viðskiptavinalykilinn og stofnar stöðu greiðslu fyrir lykil lánardrottins sem samsvarar viðskiptavininum.

1.  Í Viðskiptakröfur, keyrið ferlið **Endurgreiðsla**.
2.  Fylgið einu af eftirfarandi skrefum:
    -   Til þess að endurgreiða tilteknum viðskiptavini er smellt á **Velja** og reikningar viðskiptavina tilgreindir í fyrirspurn.
    -   Til þess að endurgreiða öllum viðskiptavinum er smellt á **OK**.

    Kreditupphæðir eru fluttar í lánardrottnarlykla viðskiptavinar og eru unnar eins og venjulegar greiðslur. Ef viðskiptamaður er ekki með lánardrottnarlykil er sjálfkrafa búið til númer einsskiptislánardrottins handa viðskiptamanninum.
3.  Til að skoða færslur endurgreiðslna sem voru stofnaðar, notið síðuna **Endurgreiðslur**.
4.  Í Viðskiptaskuldir, stofnið greiðslu fyrir reikninga lánardrottins sem voru stofnaðir sem afleiðing af endurgreiðsluferlinu.






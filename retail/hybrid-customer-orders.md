---
title: "Hybrid pantanir viðskiptavina"
description: "Pöntun viðskiptavinar hybrid er eina pöntun, sem inniheldur afurðir sem hægt er að framkvæma úr verslun með viðskiptavinar, ásamt afurðir sem verður tekin eða sent síðar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid pantanir viðskiptavina

Pöntun viðskiptavinar hybrid er eina pöntun, sem inniheldur afurðir sem hægt er að framkvæma úr verslun með viðskiptavinar, ásamt afurðir sem verður tekin eða sent síðar.

Í Microsoft Dynamics 365 aðgerða - Smásölu, má velja annað hvort fyrra út allar afurðir eða framkvæma valdar afurðir fyrir pöntun viðskiptavinar. Afurð sem merktar eru sem framkvæmd er sjálfkrafa reikningsfærðum línum þegar pöntun er stofnuð, vinnustöðvartímans er þetta sama pöntun sem á að taka upp eftir að pöntun er stofnuð. Upphæð til greiðslu á hybrid pantanir ákvarðast af innborgunarprósenta á að taka til að bæta og afurðalína sendingar með heildarupphæðina fyrra línur. Hybrid pantana, skiptir kerfið á milli afhendingarmáta pöntun viðskiptavinar og reiðufé og staðgreiddar ham sem hér segir:

-   Ef allar afurðirnar í körfunni eru stillt á **Framkvæma afhendingu**, pöntun verður meðhöndluð sem Reiðufjár og Staðgreiddar færslur.
-   Ef einhverjar eða allar línur í körfunni eru stillt á annað hvort **Taka** eða **senda afhendingu**, pöntun verður meðhöndluð sem færslu Viðskiptavinar.

Ef lína innkaupakörfu er valinn og **Tiltekt valin**, **Senda valið**, eða **Framkvæmd valda** er valinn eru aðeins tilteknar körfulínu sett með sem afhendingaraðferð. Í því tilfelli niðurflæði aðgerðarinnar heldur eins og venjulega. Hins vegar ef **Tiltekt valin**, **Senda valið**, eða **Framkvæmd valda** valinn án körfulínu sem verið er að velja nýja síðu opnast sem skráir allar línur innkaupakörfu. Á skjá, hægt er að velja margar línur í einu fyrir afhendingaraðferð stillingu. Þegar aðferð sem er notuð til að velja línur hnekkt allar fyrri afhendingaraðferð sem hefur verið úthlutað á línu.

<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir pantanir viðskiptavina](customer-orders-overview.md)



---
title: 'Stofna verkþáttarvensl: næsti þáttur'
description: Flæði aðgerða í lean-framleiðsluflæði er skráð með venslum verkþáttar.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cee0c75de1fee24cfb6df018de62ece102c96cc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579209"
---
# <a name="create-activity-relation---successor"></a>Stofna verkþáttarvensl: næsti þáttur

[!include [banner](../../includes/banner.md)]

Flæði aðgerða í lean-framleiðsluflæði er skráð með venslum verkþáttar. Þessi skráning sýnir hvernig á að stofna verkþáttarvensl.

Skilyrði:

- - Framleiðsluflæði og útgáfa í ham fyrir drög. 

- - Tveir verkþætti sem elta hvert annað í framleiðsluflæði eru stofnuð en ekki tengdar.


## <a name="find-the-production-flow-version"></a>Finndu útgáfu framleiðsluflæðis 
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Í listanum skal merkja valda línu.
5. Í listanum skal velja útgáfu draga.
    * Hægt er að bæta við verkþáttarvenslum við bæði drög eða virkar útgáfur framleiðsluflæðis.  

## <a name="open-the-activity-overview"></a>Opna yfirlit verkþátta
1. Smellt er á Verkþætti.
    * Athugið að skjámyndin sýnir alla verkþætti framleiðsluflæðis sem er úthlutað á þá Útgáfu framleiðsluflæðis sem unnið er í.  

## <a name="add-a-successor"></a>Bæta við arftaka
1. Smelltu á Bæta við arftaka.
2. Í reitnum Verkþáttur skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Veldu gátreitinn Skorður.
6. Í reitinn Skorðugildi skal slá inn númer.
    * Tími skorða er sá tími sem er áætlaður á milli áætlaðra loka forvera (gjalddagi og tími) og áætlaðs upphafs arftaka.  
7. Í reitinn Einingar skal slá inn gildi.
8. Færið inn tölu í reitnum Hlutfall ferlistíma.
    * Ef báðir verkþættir eru keyrðir á sama framleiðslutíma ætti hlutfall ferlistíma að vera 1. Ef forveri sem keyrist við tvöföld þjónustuhraða, hlutfall ætti að vera 2.   Hlutfall ferlistíma eru notuð til að reikna út einstaka ferlistíma fyrir verkþætti framleiðsluflæðis.  
9. Smellið á „Í lagi“.
10. Lokið síðunni.
11. Smellt er á flipann GridPanel.
12. Lokið síðunni.
13. Endurhlaðið síðuna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
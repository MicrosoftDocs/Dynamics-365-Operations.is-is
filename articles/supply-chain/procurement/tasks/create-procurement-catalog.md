--- 
title: "Stofna innkaupavörulista"
description: "Þessi verklýsing sýnir hvernig á að stofna innkaupavörulista."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a>Stofna innkaupavörulista

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innkaupavörulista. Þetta verk myndi venjulega framkvæmt af fagmanni á sviði innkaupa. Einnig muntu læra hvernig starfsmenn geta notað vörulista þegar þeir stofna beiðni. Áður en hægt er að stofna vörulista verður að vera tegundastigveldi innkaupa í kerfinu. Stigveldið er erft af nýjum vörulista, ásamt öllum afurðum sem eru í stigveldinu. Hægt er að nota þessari handbók í sýnigögnum USMF-fyrirtækisins þar sem tegundastigveldi innkaupa er tiltækt, sem og dæmi sem notað er í skrefum ferlisins.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Tryggið að til tegundastigveldi innkaupa sé til staðar.
1. Fara í Innkaup og uppruni > Innkaupaflokkar.
    * Tegundastigveldi innkaupa er tiltækt í sýnigögnum USMF-fyrirtækisins og afurðir hefur verið bætt við tegundirnar skrifstofuvélar/Tölvur. Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk þarf að aflæsa leiðarvísi fyrir verk til að fletta í gegnum tegundina. Ef stigveldi var ekki tiltæk, yrði það stofnað með því að smella á Nýtt. Einungis er hægt að gera þetta einu sinni.  
2. Lokið síðunni.

## <a name="create-a-catalog"></a>Stofna vörulista
1. Fara í Innkaup og uppruni > vörulistar > Innkaupavörulistar.
2. Smellt er á Nýtt innkaupavörulisti til að opna felligluggann.
3. Í reitinn Heiti skal slá inn gildi.
4. Smellt er á Í lagi.
5. Útvíkka 'CORP PROCUREMENT CATEGORIES', í trénu.
6. Í trénu skal víkka út 'OFFICE MACHINES'.
7. Í trénu skal velja „Tölvur“.
    * Afurðir fyrir innkaupategundina birtast á listanum. Eigi að bæta vöru við tegund þarf að gera þetta á síðunni tegundastigveldi innkaupa eða á vöruupplýsingasíðu.  
    * Sjálfgefin uppfærslugerð ákvarðar hvort nýjar afurðir sem hefur verið bætt við tegundastigveldi innkaupa eru sýnileg strax í vörulistanum. Ef gerð uppfærslu er stillt á Gagnvirkt, eru breytingar sýnileg strax. Ef gerð uppfærslu er Föst, eru nýjar afurðir einungis sýnilegt fyrir fólk á vörulista eftir að vörulista hefur verið birt aftur. Birtingaraðgerð er tiltæk í Aðgerðarúðunni efst á síðunni. Ef vörur eru fjarlægðar úr tegundastigveldi innkaupa, sést breytingu strax, án tillits til gildisins í reitnum sjálfgefin uppfærslugerð.  
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
9. Smellt er á Fela.
10. Á Aðgerðarúðu, smellið á .Yfirlit tegundar
11. Smellt er á gera óvirkt.
12. Á Aðgerðarúðu, smellið á .Yfirlit tegundar
13. Smella á Virkja.
14. Smella á Virkja vörulista
15. Lokið síðunni.

## <a name="make-the-catalog-visible"></a>Gera vörulista sýnilegan
1. Fara í Innkaup og uppruni > Uppsetning > reglur > innkaupareglur.
2. Velja innkaupastefnu USMF
    * Velja þarf innkaupastefna fyrir lögaðilann sem starfsmaðurinn sem er tengdur við þína forstillingu má panta vörur í. Í Sýnigögn USMF, er kerfisstjóranotandanum tengd við starfsmann sem kallast Julia Funderburk, og hún pantar vörur í USMF að sjálfgefnu.  
3. Í listanum skal smella á tengilinn í valinni línu.
4. Velja vörulista sem nýverið var stofnuð
5. Smellið á „Í lagi“.
6. Lokið síðunni.
7. Lokið síðunni.

## <a name="use-the-catalog"></a>Nota vörulista
1. Fara í Innkaup og uppruni > Innkaupabeiðnir > Allar Innkaupabeiðnir.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Smellið á „Í lagi“.
5. Smella á Bæta við afurðum.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Hægt er að nota tegundastigveldi vinstra megin eða sía efst á listanum til að sía vörurnar.  
7. Smellt er á Bæta við línum.
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
9. Smellt er á Bæta við línum.
10. Smellið á „Í lagi“.



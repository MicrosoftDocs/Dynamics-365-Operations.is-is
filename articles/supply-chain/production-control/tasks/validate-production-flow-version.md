---
title: Villuleita í framleiðsluflæði og útgáfu
description: Þessi verklýsing sýnir hvernig á að stofna nýtt framleiðsluflæði og fyrstu útgáfu fyrir lean-framleiðslu.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5dfd5655ecdfa74d75490b0915c4cea609baebe3
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146505"
---
# <a name="validate-a-production-flow-and-version"></a>Villuleita í framleiðsluflæði og útgáfu

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna nýtt framleiðsluflæði og fyrstu útgáfu fyrir lean-framleiðslu. Frumskilyrði: Skilgreina þarf framleiðslufæribreytur fyrir Lean-framleiðslu og mælieiningar fyrir klasatíma. Það þarf að skilgreina virðisstraum og framleiðsluflokk. Skoðið hvítblöð í Lean-framleiðslu til að kynna þér hugtökin framleiðsluflæði og verkþætti. Þetta ferli vísar í lögaðilinn USMF í sýnigögnum. Hins vegar, ef við gerum ráð fyrir að lögaðilinn sé skilgreindur fyrir Lean-framleiðslu, er hægt að nota aðra lögaðila.


## <a name="create-a-production-flow"></a>Stofna framleiðsluflæði
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
    * Virðisstraumur er rekstrareining sem nær yfir alla verkþætti og flæði virðisstraumsins.   Á þessu stigi takmarkast rekstrareiningar við lögaðila og hafa engin frekari aðgerðir.  
7. Í reitnum Framleiðsluflokkur skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal smella á tengilinn í valinni línu.
    * Framleiðsluflokkar leyfa skilgreiningu á efni, vinnu og vív-lyklum fyrir framleiðsluferli. Til að tengja bókhaldssamhengi við framleiðsluflæði verður að velja framleiðsluflokk.  
9. Smellið á „Vista“.

## <a name="create-a-production-flow-version"></a>Stofna útgáfu framleiðsluflæðis
1. Smelltu á Bæta við.
2. Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.
    * Hægt er að uppfæra lokadag útgáfu hvenær sem er, jafnvel fyrir virkar útgáfur. Notaðu gildistíma útgáfu til að áætla áfanga úr útgáfu.  
3. Smellið á „Í lagi“.
4. Í listanum skal merkja valda línu.
5. Í reitnum Eining skal slá inn gildi.
6. Velja verkeiningu.
7. Færið inn tölu í reitnum Framleiðslutími á einingu.
    * Skilgreina valinn framleiðslutíma á einingu fyrir verkstýringu á útgáfu framleiðsluflæðisins.   Framleiðslutími er skilgreindur sem magn á hvert tímabil.  Í gefnu dæmi er framleiðslutíminn 0,2 klukkustundir á 10 stykki. Fyrir vinnutíma upp á 8 klukkustundir samsvarar þetta daglegri afkastagetu fyrir 400 stykki.  
8. Í reitinn Magn á talningu skal slá inn tölu.
9. Útvíkka eða draga saman Útgáfu upplýsingahluta.
10. Í reitnum Lágmark framleiðslutíma á einingu skal færa inn tölu.
    * Lágmarksframleiðslutími á einingu verður að vera lægri en eða jafnt og meðalframleiðslutími á einingu.  
11. Í reitnum Hámark framleiðslutíma á einingu skal færa inn tölu.
    * Hámarksframleiðslutími á einingu verður að vera hærri en eða jafnt og meðalframleiðslutími á einingu.  
12. Færið inn fjölda daga á tímabili fyrir raunferlistíma
    * Tímabil fyrir raunferlistíma er sá fjöldi daga sem vinnslum er safnað saman úr raunverulega mínútu til baka til að reikna raunferlistíma. Gildinu er hægt að breyta hvenær sem er og er aðeins notað fyrir útreikning á tímum raunferlistíma.  
13. Smellið á „Vista“.


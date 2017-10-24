--- 
title: "Stofna útgáfu framleiðsluflæðis"
description: "Þetta ferli sýnir hvernig ný útgáfa framleiðsluflæðis er stofnuð."
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-flow-version"></a>Stofna útgáfu framleiðsluflæðis

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig ný útgáfa framleiðsluflæðis er stofnuð. Fyrir þetta ferli verður að skilgreina framleiðslufæribreytur fyrir lean-framleiðslu og mælieiningar fyrir klasatíma. Einnig þarf að skilgreina virðisstraum og framleiðsluflokk. Frekari upplýsingar um framleiðsluflæði og aðgerðir í lean-framleiðslu má sjá í hvítblöð um Lean-framleiðslu í Microsoft Dynamics AX. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-production-flow"></a>Stofna framleiðsluflæði
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
    * Veljið rekstrareiningu af gerðinni virðisstraumur. Virðisstraumur er rekstrareining sem nær yfir allar aðgerðir og flæði virðisstraumsins. Á þessu stigi takmarkast rekstrareiningar við lögaðila og hafa engin frekari aðgerðir.  
7. Í reitnum Framleiðsluflokkur skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal smella á tengilinn í valinni línu.
    * Veljið framleiðsluflokk fyrir framleiðsluflæðið. Framleiðsluflokkar leyfa skilgreiningu á efni, vinnu og VÍV-lyklum fyrir framleiðsluferli. Til að tengja bókhaldssamhengi við framleiðsluflæði verður að velja framleiðsluflokk.  
9. Smellið á „Vista“.

## <a name="create-a-production-flow-version"></a>Stofna útgáfu framleiðsluflæðis
1. Smelltu á Bæta við.
2. Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.
    * Ef þörf er hægt að skilgreina lokadag fyrir útgáfu. Hægt er að uppfæra hvenær sem er, jafnvel fyrir virkar útgáfur. Hægt er að nota hana til að áætla að draga smám saman úr útgáfu.  
3. Smellið á „Í lagi“.
4. Í listanum skal merkja valda línu.
5. Í reitnum Eining skal slá inn gildi.
6. Leysa breytir verkeiningu.
7. Færið inn tölu í reitnum Framleiðslutími á einingu.
    * Skilgreina framleiðslutíma á einingu fyrir útgáfuna. Skilgreina valinn framleiðslutíma á einingu fyrir verkstýringu á útgáfu framleiðsluflæðisins. Framleiðslutími er skilgreindur sem magn á hvert tímabil. Í dæminu er framleiðslutíminn 0,2 klukkustundir á 10 stykki. Fyrir vinnutíma upp á 8 klukkustundir samsvarar þetta daglegri afkastagetu fyrir 400 stykki.  
8. Í reitinn Magn á talningu skal slá inn tölu.
    * Skilgreina magn á ferli sem tengist framleiðslutíma á einingu.  
9. Víxla útvíkkun á liðnum Útgáfa upplýsinga.
10. Í reitnum Lágmark framleiðslutíma á einingu skal færa inn tölu.
    * Skilgreina lágmarksframleiðslutíma á einingu. Lágmarksframleiðslutími á einingu verður að vera lægri en eða jafnt og meðalframleiðslutími á einingu.  
11. Í reitnum Hámark framleiðslutíma á einingu skal færa inn tölu.
    * Hámarksframleiðslutími á einingu verður að vera hærri en eða jafnt og meðalframleiðslutími á einingu.  
12. Í reitinn Tímabil fyrir rauntíma ferlis (dagar) skal slá inn númer.
    * Færið inn fjölda daga á tímabili fyrir raunferlistíma. Tímabil fyrir raunferlistíma er sá fjöldi daga sem vinnslum er safnað saman úr raunverulega mínútu til baka til að reikna raunferlistíma. Gildinu er hægt að breyta hvenær sem er og er aðeins notað fyrir útreikning á tímum raunferlistíma.  
13. Smellið á „Vista“.



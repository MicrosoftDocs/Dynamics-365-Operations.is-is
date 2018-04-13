--- 
title: "Virkja prentun merkis á númeraplötu"
description: "Þetta ferli gerir sjálfvirka prentun Raðnúmerskóða fyrir sendingu gáms (SSCC) merki eftir að síðasta vara er tekin úr birgðum í tiltektarferli sölu."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>Virkja prentun merkis á númeraplötu

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli gerir sjálfvirka prentun Raðnúmerskóða fyrir sendingu gáms (SSCC) merki eftir að síðasta vara er tekin úr birgðum í tiltektarferli sölu. Hægt er að keyra þetta ferli fyrir sýnigögn fyrirtækisins USMF. Ef verið er að keyra hana með eigin gögn, þarf að hafa sett upp númeraröð fyrir númeraplötur. Þarf að setja upp merkimiði prentarinn áður en byrjað er að þetta verkefni. Fara á fyrirtækisstjórnun > Uppsetning > Prentarar á neti. Á aðgerðasvæðinu skal smellt er á Valkostum og smella svo á uppsetningarhnapp fyrir niðurhal skjals leiðarfulltrúa. Keyra uppsetningarforritið og gangið úr skugga um að þú hefur virkan prentara á neti stilltan áður en haldið er áfram með ferlið.


## <a name="set-up-the-gs1-company-prefix"></a>Setja upp GS1-fyrirtækjaforskeyti
1. Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.
2. Í svæðinu fyrir forskeyti GS1 fyrirtækis, færið inn 7 tölur fyrir GS1 númer fyrirtækis þíns .
3. Smellið á „Vista“.
4. Lokið síðunni.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Setja upp númeraröð SSCC númeraplötu
1. Fara í Fyrirtækisstjórnun > Númeraröð > Númeraröð.
2. Í reitnum Svæði skal velja valkost.
3. Í reitnum Tilvísun skal velja valkost.
4. Í reitinn Fyrirtæki skal slá inn gildi.
5. Í listanum skal merkja valda línu.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Stækka the hlutann hlutir.
8. Smellið á „Breyta“.
9. Veljið fyrstu línu í töflunni Hlutar
10. Smella á Fjarlægja.
11. Smella á Fjarlægja.
12. Smellið á „Vista“.
13. Lokið síðunni.

## <a name="create-the-document-route-layout"></a>Stofna útlit leið skjals 
1. Fara í vöruhúsakerfi > Uppsetning > Skjalaleið > Útlit skjalaleiðar.
    * Virkja SSCC útlit.  
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum Kenni útlits.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
6. Smella á Setja inn aftan við texta
7. Smellið á „Vista“.
8. Lokið síðunni.

## <a name="set-up-the-document-routing"></a>Setja upp skjalaleið
1. Fara í vöruhúsakerfi > Uppsetning >  Skjalaleið > Skjalaleið.
2. Í svæðinu gerð vinnupöntunar, skal velja valkost.
3. Smellt er á Nýtt.
4. Í reitinn vöruhús skal slá inn gildi.
5. Í reitinn Heiti skal slá inn gildi.
6. Smellt er á Nýtt.
7. Í reitinn útlit kennis skal slá inn eða velja gildi.
8. Í reitnum Heiti, Færið inn heiti prentara sem á að nota.
9. Smellið á „Vista“.
10. Lokið síðunni.

## <a name="create-mobile-device-menu"></a>Stofna Valmynd fartækja
1. Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis
2. Smellið á „Nýtt“.
3. Í svæðið heiti valmyndaratriðis, færa inn gildi.
4. Í reitinn Titill skal slá inn gildi.
5. Í reitnum hamur velurðu valkost.
6. Velja skal Já í Nota fyrirliggjandi vinnu svæðinu.
7. Velja skal Já í svæðinu Mynda númeraplötu.
8. Útvíkka hlutann vinnuklasar.
9. Smellið á „Nýtt“.
10. Færa inn gildi í reitnum Kenni Vinnuklasa .
11. Smellið á „Vista“.
12. Lokið síðunni.
13. Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmynd fartækis
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
15. Veljið, í trénu ', í trénu veldu valmyndaratriði sem var stofnuð áður.'.
16. Smella á Breyta.
17. Smellt er á örina til að bæta valmyndaratriði við valmynd.
18. Smellið á „Vista“.
19. Lokið síðunni.

## <a name="update-a-work-template"></a>Uppfæra sniðmát verks
1. Fara í vöruhúsakerfi  > Uppsetning  > Vinna  > Vinnusniðmát.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Smellið á „Breyta“.
4. Smellt er á Nýtt.
5. Í listanum skal merkja valda línu.
6. Veljið í svæðinu vinnutegund "Prenta".
7. Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Smelltu á Flytja upp.
10. Smellið á „Vista“.
11. Lokið síðunni.



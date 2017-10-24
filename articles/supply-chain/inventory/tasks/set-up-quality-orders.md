---
title: "Setja upp gæðapantanir"
description: "Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-quality-orders"></a>Setja upp gæðapantanir

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu. Ferlið er yfirleitt framkvæma með gæðastjóra. Ferlið inniheldur stofnun gæðaflokks til að skilgreina vörurnar sem á að nota sem sýni, og prófunarflokk til að flokka prófanir sem á að framkvæma á vörum í gæðaflokkinn. Hægt er að keyra þessari leiðbeiningar í sýnigögnum USMF-fyrirtækisins.


## <a name="enable-quality-management"></a>Gæðastjórnun virkjuð
1. Fara í Birgðastjórnun > Uppsetning > Birgðir og færibreytur vöruhúsakerfis.
2. Smellið á flipann gæðastjórnun.
3. Setja skal Nota gæðastjórnun valkosturinn á Já.
4. Smellt er á uppsetningu Skýrslu.
    * Á USMF, er skýrsluuppsetning fyrir gæðastjórnun er þegar skilgreind. Hafi þetta ekki verið gert myndirðu bæta við nýjum línum hér fyrir mismunandi skýrslugerðir, og veldu gerð skjals sem á að nota fyrir hverja skýrslu.  
5. Lokið síðunni.
6. Lokið síðunni.

## <a name="create-a-test"></a>Stofna próf
1. Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit > prófanir
2. Smellið á „Nýtt“.
3. Í reitinn Prófun skal færa inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Tegund skal velja „valkostur“.
    * Í þessu dæmi veljum við valkosturinn sem munu gera það mögulegt að úthluta niðurstöðurnar prófana byggt á fyrirframskilgreindu gildi.  
6. Smellið á „Vista“.
7. Lokið síðunni.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Stofna prófunarbreytur til að skilgreina hvernig prófunarniðurstöður eru skráðar
1. Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit >  prófunarbreytur
2. Smellið á „Nýtt“.
3. Í reitinn breyta skal færa inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smellið á „Vista“.
6. Smelltu á Niðurstöður.
7. Smellið á „Nýtt“.
8. Í reitinn niðurstöðu skal slá inn gildi.
9. Sláið inn gildi í reitnum „Lýsing“.
10. Í reitnum staða niðurstöðu, veljið ‚Stóðst'.
11. Smellið á „Vista“.
12. Smellið á „Nýtt“.
13. Í reitinn niðurstöðu skal slá inn gildi.
14. Sláið inn gildi í reitnum „Lýsing“.
15. Smellið á „Vista“.
16. Lokið síðunni.
17. Lokið síðunni.

## <a name="set-up-item-sampling"></a>Uppsetning vörusýna
1. Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit >  vörusýnishorn
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðið vörusýnishorn.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitinn Gildi skal slá inn númer.
    * Gildið á við um tilgreint magn sem er valin í aðliggjandi svæði.  
6. Stækka eða fella saman hlutann ferli.
7. Veljið eða hreinsið gátreitinn  Fullt lokun.
    * Ef þessi valkostur er valinn er heil lota eða pöntunarlínumagn læst ef prófun mistókst. Ef þú velur hana ekki, eru aðeins vörur í gæðapöntuninni læstar.  
8. Smellið á „Vista“.
9. Lokið síðunni.

## <a name="create-a-quality-group"></a>Stofna gæðaflokk
1. Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit > gæðaflokkar
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu gæðaflokkur.
    * Notkun lýsandi heiti sem auðkennir sem hvers konar vörum flokki inniheldur (Þín úrtaksskilyrði).  
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smellið á „Vista“.
6. Smellið á Bæta við vörum.
7. Velurðu línu vörunúmers.
    * Í þessu dæmi skal sía keyrð byggt á vörunúmer.  
8. Í reitinn Skilyrði skal slá inn gildi.
    * Ritið til dæmis T * til að sía vörunúmer sem byrja T.  
9. Smellið á „Í lagi“.
10. Smellið á „Í lagi“.
11. Smellt er á Gæðaflokkar vöru
12. Lokið síðunni.
13. Lokið síðunni.

## <a name="create-a-test-group"></a>Stofna prófunarflokk
1. Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit > prófunarflokkar
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu prófunarflokkur.
    * Gefðu prófunarflokksins heiti sem auðveldar að muna hvers konar prófanir verið er að keyra og hvaða gæðaflokk það ætti að vera tengd við. Til dæmis, það er til að nota með gæðaflokk sem velur vörur frá og með "T", hægt væri að kalla það "T vöru prófanir".  
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í svæðinu vörusýni, veljið línu vörusýnis sem var stofnuð áður.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Smelltu á Bæta við.
8. Í reitinn raðnúmer skal slá inn númer.
9. Veljið próf sem þú stofnaðir áður í svæðinu Prófun.
10. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
11. Smelltu á flipann Prufa.
12. Veljið í svæðinu Breyta prófunarbreytu sem var stofnuð áður 
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Í reitnum sjálfgefin niðurstaða skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal smella á tengilinn í valinni línu.
16. Smellið á „Vista“.
17. Lokið síðunni.

## <a name="define-when-quality-orders-will-be-created"></a>Skilgreina hvenær gæðapantanir eru stofnaðar
1. Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit >  gæðatengingar
2. Smellið á „Nýtt“.
3. Veljið valkost í svæðinu Gerð tilvísunar.
4. Í reitnum vörukóði er valið 'flokkur'.
    * Í þessu dæmi er velja "Flokkur" og nota gæðaflokkinn sem var stofnuð áður. Þú gæti einnig stillt þetta á "Töflu" til að tilgreina vörur handvirkt eða velja "Allt" til að bæta öllum vörum við gæðapöntun.  
5. Í svæðinu vara, veljið gæðaflokk sem var stofnuð áður.
    * Tiltækir valkostir í svæðinu Vöru eru háð stillingu í svæðinu fyrir vörukóði.  
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Stækka eða fella saman hlutann ferli.
8. Veljið valkost í svæðinu gerð tilviks.
    * Það er þá atburðurinn sem ræsir prófið. Tiltæk valkostir hér velta á hvaða vinnslu var valið í svæðinu gerð Tilvísunar.  
9. Í reitnum Framkvæmd skal velja valkost.
10. Stækka eða fella saman hlutann ferli gæðapöntunar.
11. Í reitnum tilvikslokun skal smella á fellilistahnappinn til að opna leitina.
    * Þetta svæði sýnir lista yfir ferli sem hægt er að læsa ef gæðapöntunin er enn opin. Valkostir fara eftir því hvað var valið í svæðinu gerð Tilviks.  
12. Í listanum skal smella á tengilinn í valinni línu.
    * Þetta mun velta á fyrri gildum sem valin voru. Veljið ef eftirfarandi ferlum verður að læsa meðan með verið er að tengja opnar gæðapantanir við upprunaskjalslínu.  
13. Víkka eða draga saman  hlutann lýsing
14. í svæðinu prófunarflokkur Veljið prófunarflokk sem var stofnuð áður 
15. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
16. Smellið á „Vista“.
17. Lokið síðunni.


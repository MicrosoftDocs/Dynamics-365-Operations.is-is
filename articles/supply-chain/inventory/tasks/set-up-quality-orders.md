---
title: Setja upp gæðapantanir
description: Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu.
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4577b8b189403b3d71eb634e159d51d2fa53ce12
ms.sourcegitcommit: 6d6aa016c4971b0673d461b82fd80b060ae5f7a1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/17/2020
ms.locfileid: "3268794"
---
# <a name="set-up-quality-orders"></a>Setja upp gæðapantanir

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu. Ferlið er yfirleitt framkvæma með gæðastjóra. Ferlið inniheldur stofnun gæðaflokks til að skilgreina vörurnar sem á að nota sem sýni, og prófunarflokk til að flokka prófanir sem á að framkvæma á vörum í gæðaflokkinn. Hægt er að keyra þessari leiðbeiningar í sýnigögnum USMF-fyrirtækisins.


## <a name="enable-quality-management"></a>Gæðastjórnun virkjuð
1. Farðu í **Skoðunarrúðu > Kerifseiningar > Birgðastýring > Uppsetning > Birgðir og færibreytur vöruhúsakerfis**.
2. Smelltu á flipann **Gæðastjórnun**.
3. Setja skal **Nota gæðastjórnun** valkosturinn á Já.
4. Smelltu á **Uppsetningu Skýrslu**. Á USMF, er skýrsluuppsetning fyrir gæðastjórnun er þegar skilgreind. Ef þetta var ekki gert myndirðu bæta við nýjum línum hér fyrir mismunandi skýrslugerðir, og veldu gerð skjals sem á að nota fyrir hverja skýrslu.  
5. Lokið síðunni.
6. Lokið síðunni.

## <a name="create-a-test"></a>Stofna próf
1. Farðu í **Birgðastjórnun > Uppsetning > gæðaeftirlit > prófanir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Prófun** skal færa inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Tegund** skal velja „valkostur“. Í þessu dæmi veljum við valkosturinn sem munu gera það mögulegt að úthluta niðurstöðurnar prófana byggt á fyrirframskilgreindu gildi.  
6. Smellt er á **Vista**.
7. Lokið síðunni.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Stofna prófunarbreytur til að skilgreina hvernig prófunarniðurstöður eru skráðar
1. Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > prófunarbreytur**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Breyta** skal færa inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Smellt er á **Vista**.
6. Smelltu á **Niðurstöður.**
7. Smellt er á **Nýtt**.
8. Í reitinn **Niðurstöðu** skal slá inn gildi.
9. Í reitinn **Lýsing** skal slá inn gildi.
10. Í reitnum **Staða niðurstöðu** veljið ‚Stóðst'.
11. Smellt er á **Vista**.
12. Smellt er á **Nýtt**.
13. Í reitinn **Niðurstöðu** skal slá inn gildi.
14. Í reitinn **Lýsing** skal slá inn gildi.
15. Smellt er á **Vista**.
16. Lokið síðunni.
17. Lokið síðunni.

## <a name="set-up-item-sampling"></a>Uppsetning vörusýna
1. Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > vörusýnishorn**.
2. Smellt er á **Nýtt**.
3. Í reitnum **vörusýnishorn** færirðu inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Gildi** skal slá inn númer. Gildið á við um tilgreint magn sem er valið í aðliggjandi reit.  
6. Stækka eða fella saman hlutann **ferli**.
7. Veljið eða hreinsið gátreitinn **Full lokun**. Ef þessi valkostur er valinn er heil lota eða pöntunarlínumagn læst ef prófun mistókst. Ef þú velur hana ekki, eru aðeins vörur í gæðapöntuninni læstar.  
8. Smellt er á **Vista**.
9. Lokið síðunni.

> [!NOTE]
> Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* bætir við nokkrum nýjum möguleikum fyrir vörusýnatöku. Það bætir við hugtakinu *umfang vörusýnatöku* og getur skilgreint heila númeraplötu sem tilgreint magn. Ef þú hefur gert þennan eiginleika virka, er frekari upplýsingar að finna í [Gæðastjórnun fyrir vöruhúsaferli](../quality-management-for-warehouses-processes.md).

## <a name="create-a-quality-group"></a>Stofna gæðaflokk
1. Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > gæðaflokkar**.
2. Smellt er á **Nýtt**.
3. Færa inn gildi í svæðinu **gæðaflokkur**. Notkun lýsandi heiti sem auðkennir sem hvers konar vörum flokki inniheldur (Þín úrtaksskilyrði).  
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Smellt er á **Vista**.
6. Smellið á **Bæta við vörum**.
7. Velurðu **línu vörunúmers**. Í þessu dæmi skal sía keyrð byggt á vörunúmer.  
8. Í reitnum **Skilyrði** skal slá inn gildi. Ritið til dæmis T * til að sía vörunúmer sem byrja T.  
9. Smellt er á **OK**.
10. Smellt er á **OK**.
11. Smelltu á **Gæðaflokkar vöru**.
12. Lokið síðunni.
13. Lokið síðunni.

## <a name="create-a-test-group"></a>Stofna prófunarflokk
1. Farðu í **Birgðastjórnun > Uppsetning > gæðaeftirlit > prófunarflokkar**.
2. Smellt er á **Nýtt**.
3. Færa inn gildi í svæðinu **prófunarflokkur**. Gefðu **prófunarflokksins** heiti sem auðveldar að muna hvers konar prófanir verið er að keyra og hvaða gæðaflokk það ætti að vera tengd við. Til dæmis, það er til að nota með gæðaflokk sem velur vörur frá og með „T”, hægt væri að kalla það „T vöru prófanir”.  
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í svæðinu **vörusýni**, veljið línu vörusýnis sem var stofnuð áður.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Smelltu á **Bæta við**.
8. Í reitinn **Raðnúmer** skal slá inn númer.
9. Í reitnum **Prófun** skal velja próf sem áður var stofnað.
10. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
11. Smelltu á flipann **Prufa**.
12. Í reitnum **Breyta** skal velja prófunarbreytu sem stofnuð var áður
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Í reitnum **sjálfgefin niðurstaða** skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal smella á tengilinn í valinni línu.
16. Smellt er á **Vista**.
17. Lokið síðunni.

## <a name="define-when-quality-orders-will-be-created"></a>Skilgreina hvenær gæðapantanir eru stofnaðar
1. Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > gæðatengingar**.
2. Smellt er á **Nýtt**.
3. Veljið valkost í svæðinu **Gerð tilvísunar**.
4. Í reitnum **vörukóði** er valið 'flokkur'. Í þessu dæmi veljum við „Flokkur” og notum gæðaflokkinn sem var stofnaður áður. Þú gæti einnig stillt þetta á "Töflu" til að tilgreina vörur handvirkt eða velja "Allt" til að bæta öllum vörum við gæðapöntun.  
5. Í svæðinu **vara**, veljið gæðaflokk sem var stofnuð áður. Tiltækir valkostir í svæðinu Vöru eru háð stillingu í svæðinu fyrir vörukóði.  
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Stækka eða fella saman hlutann ferli.
8. Í reitnum **Gerð tilviks** skal velja valkost. Það er þá atburðurinn sem ræsir prófið. Tiltæk valkostir hér velta á hvaða vinnslu var valið í svæðinu gerð Tilvísunar.  
9. Í reitnum **Framkvæmd** skal velja valkost.
10. Stækka eða fella saman hlutann **ferli gæðapöntunar**.
11. Í reitnum **tilvikslokun** skal smella á fellilistahnappinn til að opna leitina. Þetta svæði sýnir lista yfir ferli sem hægt er að læsa ef gæðapöntunin er enn opin. Valkostir fara eftir því hvað var valið í svæðinu gerð Tilviks.  
12. Í listanum skal smella á tengilinn í valinni línu. Þetta mun velta á fyrri gildum sem valin voru. Veljið ef eftirfarandi ferlum verður að læsa meðan með verið er að tengja opnar gæðapantanir við upprunaskjalslínu.  
13. Víkka eða draga saman hlutann **lýsing**.
14. í svæðinu **prófunarflokkur** Veljið prófunarflokk sem var stofnuð áður.
15. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
16. Smellt er á **Vista**.
17. Lokið síðunni.

> [!NOTE]
> Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* býður upp á viðbótareiginleika til að setja upp gæðatengingar. Hann bætir við nýju skilyrði (**Viðeigandi gerð vöruhúss**) og nýrri stillingu (**Regla um úrvinnslu gæða**). Ef þú hefur gert þennan eiginleika virka, er frekari upplýsingar að finna í [Gæðastjórnun fyrir vöruhúsaferli](../quality-management-for-warehouses-processes.md).
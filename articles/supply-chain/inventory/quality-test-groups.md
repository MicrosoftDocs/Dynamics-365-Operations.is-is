---
title: Prófunarflokkar gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig eigi að stofna prófunarflokka til að hægt sé að nota margar prófanir með gæðapöntunum í Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020a610e6a7e4d4b35ceb176d542bae32503a615
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021757"
---
# <a name="quality-management-test-groups"></a>Prófunarflokkar gæðastjórnunar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig eigi að stofna prófunarflokka til að hægt sé að nota margar prófanir með gæðapöntunum í Microsoft Dynamics 365 Supply Chain Management.

Síðan **Prófunarflokkar** er notuð til að setja upp, breyta og skoða prófunarflokka og einstakar prófanir sem er úthlutað á þá. Efri hluti síðunnar sýnir prófunarflokkana og neðri hlutinn sýnir prófin sem er úthlutað er á valinn prófunarflokk.

Nokkrum reglum er úthlutað á prófunarflokk, t.d. úrtaksáætlun, viðunandi gæðastigi og þörf fyrir eyðileggingarprófun. Þegar þú svo úthlutar stöku prófi á prófunarflokk, skilgreinirðu viðbótarupplýsingar, eins og röðina, skjölin og gildisdagsetningarnar. Fyrir magnbundna prófun innihalda upplýsingar sem eru skilgreindar einnig viðunandi mælingargildi. Upplýsingarnar eru prófunarfæribreytur og sjálfgefin útkoma fyrir eigindlega prófun.

Prófunarflokkur sem er úthlutað á gæðapöntun skilgreinir sjálfgefið safn prófana sem verður að framkvæma á tiltekinni vöru. Hins vegar er hægt að bæta við, breyta, eða eyða prófunum fyrir gæðapöntun. Niðurstöður prófana eru tilkynntar fyrir hvert próf á gæðapöntun.

Þegar prófunarflokkur er skilgreindur er valfrjálst hægt að tilgreina sýnatöku. Sýnatökur eru notaðar til að skilgreina afurðarmagnið sem þarf að prófa. Frekari upplýsingar er að finna í [Vörusýnataka gæðastjórnunar](quality-item-sampling.md). Einnig er hægt að tilgreina hvort farga eigi prófunum í prófunarflokki. Í förgunarprófi er vara sýnatöku fargað og magnið er fjarlægt úr lagerbirgðum.

## <a name="example-of-a-test-group"></a>Dæmi um prófunarflokk

Framleiðslufyrirtæki skilgreinir prófunarflokk fyrir hvert afbrigði af gæðareglum sínum. Mismunandi prófunarflokkar endurspegla mismun á úrtaksáætlunum, safn prófana sem þarf að framkvæma samtímis, viðunandi gæðastigi og öðrum stuðlum. Fyrir magnbundnar prófanir er einnig mismunur í viðunandi mælingargildum. Til að framfylgja gæðareglum úthlutar fyrirtækið prófunarflokki á hverja reglu sem er notuð til að mynda gæðapantanir sjálfkrafa á síðunni **Gæðatengingar**. Það úthlutar einnig prófunarflokki á gæðapantanir sem eru stofnaðar á handvirkan máta.

## <a name="create-a-test-group"></a>Stofna prófunarflokk

Til að búa til prófunarflokk, skal fylgja eftirfarandi skrefum.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófunarflokkar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið á efri hluta síðunnar. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Prófunarflokkur** – Færið inn einkvæmt kenni eða heiti fyrir prófunarflokkinn.
    - **Lýsing** – Færið inn nákvæma lýsingu á prófunarflokknum.
    - **Ásættanlegt gæðastig** – Færið inn heildarprósentu prófunarniðurstaða sem þurfa að standast prófun svo að prófunarsafnið teljist hafa staðist skoðun.
    - **Vörusýnataka** - Veljið vörusýnatöku. Frekari upplýsingar er að finna í [Vörusýnataka gæðastjórnunar](quality-item-sampling.md).
    - **Förgun** – Veljið þennan gátreit til að gefa til kynna að prófunarflokkurinn muni farga vörunum sem eru prófaðar.

1. Veljið flipann **Almennt** á efri hluta síðunnar á meðan nýja línan er enn valin. Sumar stillingar prófunarflokksins sem er valinn í flipanum **Yfirlit** eru endurteknar hér. Þar að auki er hægt að stilla eftirfarandi reiti fyrir hópinn:

    - **Uppfæra runueigind birgða** – Þegar þessi valkostur er stilltur á *Já* hér verður hann sjálfkrafa stilltur á *Já* fyrir öll ný próf sem bætt er við prófunarflokkinn á neðri hluta síðunnar.
    - **Uppfæra runuráðstöfun** – Þegar þessi valkostur er stilltur á *Já*, ef varan sem verið er að prófa er runustýrð, verður runuráðstöfunin sjálfkrafa uppfærð með gildinu sem valið er í reitnum **Gæðapöntun ráðstöfunarrunu sem mistókst** eða **Gæðapöntun ráðstöfunarrunu sem tókst**.
    - **Gæðapöntun ráðstöfunarrunu sem mistókst** – Veljið ráðstöfunarkóða runu sem á að úthluta þegar gæðapöntun sem inniheldur þennan prófunarflokk mistekst vegna þess að hún uppfyllir ekki AQL.
    - **Gæðapöntun ráðstöfunarrunu sem tekst** – Veljið ráðstöfunarkóða runu sem á að úthluta þegar gæðapöntun sem inniheldur þennan prófunarflokk tekst vegna þess að hún uppfyllir AQL.
    - **Uppfæra birgðastöðu** – Þegar þessi valkostur er stilltur á *Já*, ef **Birgðastaða** er virkjuð í geymsluvíddaflokknum fyrir vörunni sem er verið að prófa mun staðan verða sjálfkrafa uppfærð í stöðuna sem er valin í reitnum **Gæðapöntunarstaða mistókst** eða **Gæðapöntunarstaða tókst**.
    - **Gæðapöntunarstaða mistókst** – Veljið birgðastöðuna sem á að úthluta vörunni þegar gæðapöntun sem felur í sér þennan prófunarflokk mistekst vegna þess að hún uppfyllir ekki AQL.
    - **Gæðapöntunarstaða tókst** – Veljið birgðastöðuna sem á að úthluta vörunni þegar gæðapöntun sem felur í sér þennan prófunarflokk tekst vegna þess að hún uppfyllir AQL.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Bæta gæðaprófi við prófunarflokk

Fylgið þessum skrefum til að bæta gæðaprófi við prófunarflokk.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófunarflokkar**.
1. Á flipanum **Yfirlit** á efri hluta síðunnar er prófunarflokkurinn sem bæta á prófi við valinn.
1. Á neðri hluta síðunnar, í flipanum **Yfirlit**, skal velja **Bæta við** á tækjastikunni til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Raðnúmer** – Sláið inn heiltölu til að tilgreina röðina sem framkvæma á prófanirnar í. Próf sem eru með lægri raðnúmer verað keyrð á undan þeim sem eru með hærri raðnúmer.

        > [!NOTE]
        > Mælt er með að hafa bil á milli raðnúmera. Stillið til dæmis reitinn **Raðnúmer** á *10* fyrir fyrsta prófið og síðan auka gildið um 10 fyrir hvert próf sem bætist við. Á þennan hátt er hægt að bæta við nýjum prófum síðar án þess að þurfa að eyða og búa til línurnar aftur til að setja þær í tilætlaða röð.

    - **Prófun** – Veldu prófanirnar sem á að gera. Fyrir gæðapróf skal velja próf þar sem reiturinn **Gerð** er stilltur á *Valkostur*.
    - **Tekur gildi** – Veljið fyrstu dagsetninguna á gildistíma prófsins. Ef þetta svæði er skilið eftir autt eru engin takmörk.
    - **Gildir** – Veljið síðustu dagsetninguna á gildistíma prófsins. Ef þetta svæði er skilið eftir autt eða stillt á *Aldrei* eru engin takmörk.
    - **Ákvörðun prófunargildis** – Veljið hvernig á að ákveða AQL þegar margar niðurstöður eru skráðar fyrir sama prófið. Aðeins er hægt að velja *Handvirkt* fyrir gæðapróf. Ef eitt af hinum gildunum er valið (*Meðaltal*, *Lágmark* eða *Hámark*) birtast villuskilaboð þegar prufuflokkurinn er vistaður.
    - **Eigind** – Ef skrá á niðurstöður prófunar á runueigind skal velja eigindina hér og velja gátreitinn **Uppfæra runueigind birgða**.
    - **Uppfæra runueigind birgða** – Veljið þennan gátreit til að skrá niðurstöður prófunar fyrir runueigindina sem er valin í reitnum **Eigind**.

1. Á neðri hluta síðunnar skal velja flipann **Almennt**. Sumar stillingar prófsins sem er valið í flipanum **Yfirlit** eru endurteknar hér. Þar að auki er hægt að stilla eftirfarandi reiti fyrir prófið:

    - **Skýrsla greiningarvottorðs** – Stillið þennan valkost á *Já* til að tilgreina að niðurstöður prófunar eigi að vera prentaðar á greiningarvottorðið (CoA). Hægt er að mynda þessa skýrslu úr gæðapöntuninni.
    - **Viðbrögð við galla** – Veljið annaðhvort *Samþykkja* eða *Fella* til að tilgreina hvort prófið hafi verið í lagi eða ekki ef AQL fyrir það er ekki uppfyllt.
    - **Ásættanlegt gæðastig** – Færið inn heildarprósentu prófunarniðurstaða sem þurfa að standast prófun svo að prófið teljist hafa staðist skoðun.

1. Í neðri hluta síðunnar, á flipanum **Prófun**, skal stilla eftirfarandi reiti:

    - **Breyta** – Veljið prófunarbreytuna þar sem á að skrá niðurstöður gæðaprófunar.
    - **Sjálfgefin útkoma** – Veljið sjálfgefna útkomu sem á að skrá fyrir niðurstöður prófunar.
    - **Prófunartæki** – Veljið tækið sem á að nota fyrir prófið. Ef prófunartæki er skilgreint er það sjálfkrafa slegið inn fyrir prófið í prófunarflokknum.

1. Lokið síðunni.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Bæta magnprófi við prófunarflokk

Fylgið eftirfarandi skrefum til að bæta magnprófi við prófunarflokk.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófunarflokkar**.
1. Á flipanum **Yfirlit** á efri hluta síðunnar er prófunarflokkurinn sem bæta á prófi við valinn.
1. Á neðri hluta síðunnar, í flipanum **Yfirlit**, skal velja **Bæta við** á tækjastikunni til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Raðnúmer** – Sláið inn heiltölu til að tilgreina röðina sem framkvæma á prófanirnar í. Próf sem eru með lægri raðnúmer verað keyrð á undan þeim sem eru með hærri raðnúmer.

        > [!NOTE]
        > Mælt er með að hafa bil á milli raðnúmera. Stillið til dæmis reitinn **Raðnúmer** á *10* fyrir fyrsta prófið og síðan auka gildið um 10 fyrir hvert próf sem bætist við. Á þennan hátt er hægt að bæta við nýjum prófum síðar án þess að þurfa að eyða og búa til línurnar aftur til að setja þær í tilætlaða röð.

    - **Prófun** – Veldu prófanirnar sem á að gera. Fyrir magnpróf skal velja próf þar sem reiturinn **Gerð** er stilltur á *Brot* eða *Heiltala*.
    - **Tekur gildi** – Veljið fyrstu dagsetninguna á gildistíma prófsins. Ef þetta svæði er skilið eftir autt eru engin takmörk.
    - **Gildir** – Veljið síðustu dagsetninguna á gildistíma prófsins. Ef þetta svæði er skilið eftir autt eða stillt á *Aldrei* eru engin takmörk.
    - **Ákvörðun prófunargildis** – Veljið hvernig á að ákveða AQL þegar margar niðurstöður eru skráðar fyrir sama prófið. Þeir valkostir sem eru í boði eru *Meðaltal*, *Lágmark*, *Hámark* og *Handvirkt*.
    - **Eigind** – Ef skrá á niðurstöður prófunar á runueigind skal velja eigindina hér og velja gátreitinn **Uppfæra runueigind birgða**.
    - **Uppfæra runueigind birgða** – Veljið þennan gátreit til að skrá niðurstöður prófunar fyrir runueigindina sem er valin í reitnum **Eigind**.

1. Á neðri hluta síðunnar skal velja flipann **Almennt**. Sumar stillingar prófsins sem er valið í flipanum **Yfirlit** eru endurteknar hér. Þar að auki er hægt að stilla eftirfarandi reiti fyrir prófið:

    - **Skýrsla greiningarvottorðs** – Stillið þennan valkost á *Já* til að tilgreina að niðurstöður prófunar eigi að vera prentaðar á CoA. Hægt er að mynda þessa skýrslu úr gæðapöntuninni.
    - **Viðbrögð við galla** – Veljið annaðhvort *Samþykkja* eða *Fella* til að tilgreina hvort prófið hafi verið í lagi eða ekki ef AQL fyrir það er ekki uppfyllt.
    - **Ásættanlegt gæðastig** – Færið inn heildarprósentu prófunarniðurstaða sem þurfa að standast prófun svo að prófið teljist hafa staðist skoðun.

1. Í neðri hluta síðunnar, á flipanum **Prófun**, skal stilla eftirfarandi reiti:

    - **Hefðbundið** – Sláið inn upphæðina (heiltölu eða brot) sem vænta má úr prófunarniðurstöðum. Gildið sem fært var inn færist sjálfgefið inn í prófunarniðurstöðurnar. Að auki verður það sjálfkrafa fært inn sem sjálfgefið gildi í reitina **Lágm** og **Hám**.
    - **Lágm** – Sláið inn lágmarksgildi sem leyfilegt er fyrir prófunarniðurstöðurnar. Gildið sem fært er inn verður að vera lægra en upphæðin sem stillt er í reitnum **Hefðbundið**. Þegar reiturinn **Lágm** er uppfærður verður reiturinn **Lágmarksvikmörk (%)** sjálfkrafa uppfærður. Á sama hátt þegar reiturinn **Lágmarksvikmörk (%)** er uppfærður verður reiturinn **Lágm** sjálfkrafa uppfærður.
    - **Hám** – Sláið inn leyfilegt hámarksgildi fyrir prófunarniðurstöðurnar. Gildið sem fært er inn verður að vera hærra en upphæðin sem stillt er í reitnum **Hefðbundið**. Þegar reiturinn **Hám** er uppfærður verður reiturinn **Hámarksvikmörk (%)** sjálfkrafa uppfærður. Á sama hátt þegar reiturinn **Hámarksvikmörk (%)** er uppfærður verður reiturinn **Hám** sjálfkrafa uppfærður.
    - **Prófunartæki** – Veljið tækið sem á að nota fyrir prófið. Ef prófunartæki er skilgreint er það sjálfkrafa slegið inn fyrir prófið í prófunarflokknum.

1. Lokið síðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Prófunartæki gæðastjórnunar](quality-management-processes.md)
- [Prófanir gæðastjórnunar](quality-management-processes.md)
- [Prófunarbreytur gæðastjórnunar](quality-management-processes.md)
- [Gæðatengingar](quality-management-processes.md)
- [Runueigindir](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

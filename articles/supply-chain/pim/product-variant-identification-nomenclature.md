---
title: Nafnakerfi afurðarafbrigðisnúmera og -nafna
description: Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll].
author: t-benebo
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 14ea9bb5afe7b05f1f0392fde523a95a04a6e2ad
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569698"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Nafnakerfi afurðarafbrigðisnúmera og -nafna

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll]. Nýja nafnakerfið er með markað snið sem tekur til númers afurðarsniðmátsins, virku afurðavíddanna og skiltákna texta að eigin vali. Einnig er hægt að stofna nafnakerfi fyrir afurðaheiti. Loks er hægt að búa til nafnakerfi til að auðkenna grunnstillingar sem eru stofnaðar af skorðumiðuðum afurðarafbrigðastilli. Þessum nafnakerfi geta innihaldið eigindir að eigin vali.

Ný nafnakerfi fyrir afurðarafbrigðanúmer og afurðarafbrigðaheiti gera þér kleift að taka með hluta auðkennanna fyrir afurðarafbrigði. Slíkir hluta geta falið í sér afurðarsniðmát, númer og heiti, auðkenni afurðavídda og heiti, númeraraðir, textafasta og eigindir. Þessi virkni leyfir þér að finna á fljótan hátt tilteknar afurðarafbrigði þegar þú stofnar sölupöntun eða innkaupapöntun. Nafnakerfi fyrir bæði afurðarafbrigðanúmer og afurðarafbrigðaheiti eru stofnuð með því að nota síðuna **Nafnakerfi afurðar**. Til að opna þessa síðu er smellt á **afurðaupplýsingastjórnun,** &gt; **Uppsetning**.

## <a name="nomenclature-of-predefined-product-variants"></a>Nafnakerfi fyrirframskilgreindra afurðarafbrigða
Afurðarafbrigði eru myndaðar fyrir afurðarsniðmát í samræmi við eina af þremur afbrigðistækni:

-   Forskilgreint afbrigði
-   Skorðumiðað
-   Víddarmiðað

Hvert afurðarafbrigði hefur númer og heiti og nafnakerfi auðkennins afurðarafbrigðis leyfir þér að velja hlutana sem verða hafðir með í hverju númeri eða heiti afurðarafbrigðis. Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.

-   Númer afurðarsniðmáts
-   Heiti afurðarsniðmáts
-   Gildi númeraraðar
-   Textafasti
-   Afurðarvíddir
    -   Veljið skilgreiningarkenni eða -heiti
    -   Kenni eða heiti litar
    -   Kenni eða heiti stærðar
    -   Kenni eða heiti stílsniðs

Eftir að auðkenni nafnakerfis afurðarafbrigðis er skilgreint, er hægt að tengja það við afurðarvíddarflokk. Þá verður öllum afurðarsniðmátum sem vísa til þessa afurðarvíddarflokks úthlutað númerum afurðarafbrigða í samræmi við nafnakerfið. Nafnakerfi fyrir afurðaafbrigðaheiti er hins vegar ekki hægt að tengja við afurðavíddaflokka. Einnig má tengja nafnakerfi fyrir auðkenni afurðarafbrigðis beint við aðalsniðmát. Í því rtilviki verður afurðarafbrigðim sem tilheyra afurðasniðmátinu úthlutað afurðarafbrigðanúmerum og -heitum í samræmi við nafnakerfin.

### <a name="example"></a>Dæmi

Stuttermabolur (TS1234) er framleiddur í þremur stærðum (S, M, L) fjórum litum (Rauður, Grænn, Blár, Gulur) og tveimur sniðum (pólóbolur, vaffhálsmál). Þar af leiðir að 24 afurðarafbrigði eru möguleg (= 3 × 4 × 2). Stofnað er nafnakerfi fyrir afurðarafbrigðisnúmer sem hefur eftirfarandi hluta:

1.  Númer afurðarsniðmáts
2.  Textafasti: "-"
3.  Litur
4.  Textafasti: "-"
5.  Stærð
6.  Textafasti: "-"
7.  Stíll

Í þessu tilviki er afurðarafbrigðisnúmer fyrir rauðan, lítill pólóbol fyrir TS1234-Red-Small-Polo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Nafnakerfi skorðuskilgreininga
Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda. Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.

-   Gildi númeraraðar
-   Textafasti
-   Eigindargildi

Hver þáttur í afbrigðalíkan afurðar getur haft sitt eigið skilgreinda nafnakerfi. Aðeins má nota eigindir sem tilheyra íhlutnum. Eigindir úr undiríhlutir eða notendakröfur eru ekki nothæfar.

### <a name="example"></a>Dæmi

Afbrigðalíkan afurðar hefur rótaríhlut með tvær eigindir:

-   Efni (Plast, viður, Stáli)
-   Lengd (10... 100)

Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:

1.  Eigindargildi: Efni
2.  Textafasti: "AAA"
3.  Eigindargildi: Lengd

Í þessu tilfelli er skilgreiningarkenni fyrir viðarefni sem er 78 á lengd WoodAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Víddarbyggðrar skilgreiningar Nafnakerfis
Fyrir skorðuskilgreiningar er hægt að stofna sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda. Hægt að velja eftirfarandi hluta á síðunni **Nafnakerfi afurðar**.

-   Gildi númeraraðar
-   Textafasti
-   Afbrigðisflokksvara

Nafnakerfi skilgreiningar má skilgreina fyrir uppskrift (BOM).

### <a name="example"></a>Dæmi

Uppskrift hefur fjórar uppskriftalínur sem er skipt í tvo skilgreiningarflokka:

-   Uppskriftarlínu: M0007, Staðlaða Cabinet
    -   Afbrigðaflokkur: Cabinet
-   Uppskriftarlínu: M0008, háklassa cabinet
    -   Afbrigðaflokkur: Cabinet
-   Uppskriftarlínu: M0021, klæði framgrills
    -   Skilgreiningaflokkur: framgrill
-   Uppskriftarlínu: M0022, framgrill stál
    -   Skilgreiningaflokkur: framgrill

Stofnað er nafnakerfi skilgreiningar sem inniheldur eftirfarandi hluta:

1.  Afbrigðaflokkur: Cabinet
2.  Textafasti: "&"
3.  Skilgreiningaflokkur: framgrill

Í þessu tilfelli er skilgreiningarkenni fyrirstaðlaðan skáp sem er með framhlið úr tauklæði M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Nafnakerfi fyrir samsetningu afurðarafbrigða og skilgreininga
Þegar þú notar annaðhvort tæknina skorðumiðaðar eða víddarbyggðar skilgreiningar til að skilgreina afurðarafbrigði fyrir afurðarsniðmát, geta afurðarsniðmát fengið númer afurðarafbrigðis sem innihalda nafnakerfið úr vídd skilgreiningarinnar. Fylgja skal þessum skrefum til að skilgreina afbrigði.

1.  Skilgreina á nafnakerfi afurðarafbrigðisnúmers sem er með skilgreiningarvídd á síðunni **nafnakerfi afurðar**.
2.  Úthluta þessa nafnakerfi á afurðarvíddarflokk með skilgreiningarvídd.
3.  Skilgreina nafnakerfi skilgreiningar fyrir íhlutina eða uppskriftirnar sem verða notaðar til að skilgreina afurðarafbrigðin.

Einnig er hægt að stofna nafnakerfi fyrir afurðarafbrigðisheitin. Heiti afurðarafbrgiða er hægt að skilgreina þannig að þau innihaldi kenni eða heiti skilgreiningarinnar.

### <a name="example-for-constraint-based-configurations"></a>Dæmi um skorðuskilgreiningar

Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:

1.  Númer afurðarsniðmáts
2.  Textafasti "\_"
3.  Afbrigði

Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:

1.  Eigindargildi: Efni
2.  Textafasti: "AAA"
3.  Eigindargildi: Lengd

Hægt er að færa inn eftirfarandi gildi fyrir hluta:

-   Númer afurðarsniðmáts = **M0099**
-   Efni = **Plast**
-   Lengd = **12**

Í þessu tilviki verður afurðarafbrigðisnúmerið M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Dæmi um víddarbyggðar skilgreiningar

Í þessu dæmi er notað nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:

1.  Númer afurðarsniðmáts
2.  Textafasti "//"
3.  Afbrigði

Nafnakerfi skilgreiningar inniheldur eftirfarandi hluta:

1.  Afbrigðaflokkur: Cabinet
2.  Textafasti: "&"
3.  Skilgreiningaflokkur: framgrill

Hægt er að færa inn eftirfarandi gildi fyrir hluta:

-   Númer afurðarsniðmáts = **D0123**
-   Skápur = **M0008**
-   Framhlið = **M0022**

Í þessu tilviki verður afurðarafbrigðisnúmerið D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Árekstrar númera
Mögulegt er að setja upp afurð nafnakerfi afurðarafbrigðisnúmers sem leiðir ekki til einkvæmra númera afurðarafbrigða. Til dæmis verða númer afurðarafbrigða ekki einnkvæm ef ein virk afurðarvídd er ekki innifalin í nafnakerfi fyrir afurðarsniðmát sem notar forskilgreinda tækni til skilgreiningar afbrigða. Aðferðin til að meðhöndla árekstra er breytileg eftir tækni við skilgreiningu.

### <a name="predefined-variants"></a>Forskilgreint afbrigði

Villa mun eiga sér stað ef reynt er að handvirkt eða sjálfkrafa mynda afurðarafbrigði þar sem eitt eða fleiri afurðarafbrigði endar á því að hafa sama númer afurðarafbrigðis. Til að forðast slíkt ætti frekar að nota allar virkar afurðarvíddar í afurðavíddaflokki. Einnig er hægt að hafa með númeraröð til að tryggja enn betur að afurðarafbrigðisnúmerin séu einkvæm.

### <a name="constraint-based-configurations"></a>Skorðuskilgreiningar

Allt eftir nafnakerfinu getur kerfið reynt að úthluta númeri afurðarafbrigðis sem ekki er einkvæmt á skilgreiningu. Í slíku tilfelli mun kerfið nota númeraröð fyrir vídd skilgreiningarvíddina sem númer afurðarafbrigðis í staðinn. Ef það gerist, mun viðvörun berast. Til að forðast slíkt ætti að taka með nógu margar eigindir í nafnakerfið til að stuðla að því að tryggja einkvæm afurðarafbrigðanúmer. Einnig ætti að ganga úr skugga um að kveikt sé á valkostinum **Endurnota** fyrir íhlutinn.

### <a name="dimension-based-configurations"></a>Víddaskilgreiningar

Á einu þrefi skilgreiningarferlisins leggur kerfið til skilgreiningargildi í samræmi við nafnakerfið. Í þessu skrefi geturðu Handvirkt breytt gildi skilgreiningarinnar. Þegar skilgreining er vistuð, mun kerfið athuga hvort gildi skilgreiningar er einkvæmt. Ef gildið sem fært er inn er ekki einkvæmt verða send villuboð. Færa þarf inn gildi einkvæmrar skilgreiningar til að vista skilgreininguna.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Stofna nafnakerfi afurðarafbrigðis fyrir skilgreind afurðarafbrigði](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
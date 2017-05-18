---
title: "Nafnakerfi afurðarnúmers"
description: "Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll], fyrir marksnið sem inniheldur númer afurðarsniðmáts, virkar afurðarvíddir og skiltákn texta að eigin vali. Einnig er hægt að byggja upp nafnakerfi til að auðkenna skilgreiningar sem eru stofnaðar eru með afurðarafbrigðastilli sem byggir á skorðum. Þessum nafnakerfi geta innihaldið eigindir að eigin vali."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: deda2b7986333e0d865aa87e6b34b6acdc8f6a6d
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="product-number-nomenclature"></a>Nafnakerfi afurðarnúmers

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvernig hægt er að setja upp nafnakerfi afurðarnúmers til að skipta út föstu sniði [Númer afurðarsniðmáts - Skilgreining - Stærð - Litur - Stíll], fyrir marksnið sem inniheldur númer afurðarsniðmáts, virkar afurðarvíddir og skiltákn texta að eigin vali. Einnig er hægt að byggja upp nafnakerfi til að auðkenna skilgreiningar sem eru stofnaðar eru með afurðarafbrigðastilli sem byggir á skorðum. Þessum nafnakerfi geta innihaldið eigindir að eigin vali.

Nýja nafnakerfi afurðarafbrigðisnúmers leyfir þér að innifela hluta sem eru í auðkennum afurðarafbrigðis þíns. Þessum hlutum geta innifalið númer afurðarsniðmáts, afurðavíddir, númeraraðir, textafasta, og eiginleika. Þessi virkni leyfir þér að finna á fljótan hátt tilteknar afurðarafbrigði þegar þú stofnar sölupöntun eða innkaupapöntun.

## <a name="nomenclature-of-predefined-product-variants"></a>Nafnakerfi fyrirframskilgreindra afurðarafbrigða
Afurðarafbrigði eru myndaðar fyrir afurðarsniðmát í samræmi við eina af þremur afbrigðistækni:

-   Forskilgreint afbrigði
-   Skorðumiðað
-   Víddarmiðað

Hvert afurðarafbrigði hefur númer og auðkenni nafnakerfis afurðarafbrigðis leyfir þér að velja hlutana sem verða hafðir með í hverju númeri afurðarafbrigðis. Hægt að velja eftirfarandi hluta á **nafnakerfi afurðar** síðuna.

-   Númer afurðarsniðmáts
-   Gildi númeraraðar
-   Textafasti
-   Afurðarvíddir
    -   Grunnstilling
    -   Litur
    -   Stærð
    -   Stíll

Eftir að auðkenni nafnakerfis afurðarafbrigðis er skilgreing, er hægt að tengja það við afurðarvíddarflokk. Þar af leiðandi er öll afurðarsniðmát sem vísa til þessa afurðarvíddarflokk úthlutað númer afurðarafbrigðis í samræmi við nafnakerfið. Einnig er mögulegt að úthluta auðkenni nafnakerfis afurðarafbrigðis beint á afurðarsniðmát, en í því tilfelli verða afurðarafbrigði sem tilheyra þessu sniðmáti úthlutað númer afurðarafbrigðis í samræmi við nafnakerfið.

### <a name="example"></a>Dæmi

Stuttermabolur (TS1234) er framleidd í 3 mismunandi stærðum (S, M, L), 4 mismunandi litum (Rauður, Grænn, Blár, Gulur) og 2 stílum (Polo, V) og gefur samtals 24 mögulega afurðarafbrigði. Auðkenni nafnakerfis afurðarafbrigðis er stofnað með eftirfarandi hlutum:

1.  Númer afurðarsniðmáts
2.  Textafasti: '-'
3.  Litur
4.  Textafasti: '-'
5.  Stærð
6.  Textafasti: '-'
7.  Stíll

Númer afurðarafbrigðis fyrir Rautt, Lítil, Polo verða: TS1234-Rautt-Lítið-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nafnakerfi skorðuskilgreininga
Fyrir skorðuskilgreiningar, er hægt að byggja sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda. Hægt að velja eftirfarandi hluta á **nafnakerfi afurðar** síðuna.

-   Gildi númeraraðar
-   Textafasti
-   Eigindargildi 

Hver þáttur í afbrigðalíkan afurðar getur haft sitt eigið skilgreinda nafnakerfi. Aðeins má nota eiginleika sem tilheyra íhlutnum. Eigindir úr undiríhlutir eða notendakröfur eru ekki tiltækar.

### <a name="example"></a>Dæmi

Afbrigðalíkan afurðar hefur rótaríhlut með tvo eiginleika.

-   Efni (Plast, viður, Stáli)
-   Lengd (10... 100)

Nafnakerfi skilgreiningar er skilgreint með því að nota eftirfarandi hluta:

1.  Eigindargildi: Efni
2.  Textafasti: 'AAA'
3.  Eigindargildi: Lengd

Skilgreiningarkenni fyrir við með lengd 78 fær eftirfarandi Skilgreiningarkenni: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Víddarbyggðrar skilgreiningar Nafnakerfis
Fyrir skorðuskilgreiningar, er hægt að byggja sérhæft nafnakerfi fyrir skilgreiningu afurðarvídda. Hægt að velja eftirfarandi hluta á **nafnakerfi afurðar** síðuna.

-   Gildi númeraraðar
-   Textafasti
-   Afbrigðisflokksvara

Nafnakerfi skilgreiningar má skilgreina fyrir uppskrift (BOM).

### <a name="example"></a>Dæmi

Uppskrift hefur 4 uppskriftarlínur skipt niður í 2 afbrigðisflokka.

-   Uppskriftarlínu: M0007, Staðlaða Cabinet
    -   Afbrigðaflokkur: Cabinet
-   Uppskriftarlínu: M0008, háklassa cabinet
    -   Afbrigðaflokkur: Cabinet
-   Uppskriftarlínu: M0021, klæði framgrills
    -   Skilgreiningaflokkur: framgrill
-   Uppskriftarlínu: M0022, framgrill stál
    -   Skilgreiningaflokkur: framgrill

Nafnakerfi skilgreiningar er skilgreint með því að nota eftirfarandi hluta:

1.  Afbrigðaflokkur: Cabinet
2.  Textafasti: '&'
3.  Skilgreiningaflokkur: framgrill

Skilgreiningarkenni fyrir staðlað cabinet með klæði framgrills verður: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Nafnakerfi fyrir samsetningu afurðarafbrigða og skilgreininga
Þegar þú notar annaðhvort tæknina skorðumiðaðar eða víddarbyggðar skilgreiningar til að skilgreina afurðarafbrigði fyrir afurðarsniðmát, geta afurðarsniðmát fengið númer afurðarafbrigðis sem innihalda nafnakerfið úr vídd skilgreiningarinnar. Fylgja skal þessum skrefum til að skilgreina afbrigði:

1.  Skilgreina á nafnakerfi afurðarafbrigðisnúmers sem er með skilgreiningarvídd á síðunni **nafnakerfi afurðar** síðuna.
2.  Úthluta þessa nafnakerfi á afurðarvíddarflokk með skilgreiningarvídd.
3.  Skilgreina nafnakerfi skilgreiningar fyrir íhlutina eða uppskriftirnar sem verða notaðar til að skilgreina afurðarafbrigðin.

### <a name="example-for-constraint-based-configurations"></a>Dæmi um skorðuskilgreiningar

Í þessu dæmi, er hægt að nota nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:

1.  Númer afurðarsniðmáts
2.  Textafasti '\_'
3.  Grunnstilling

Nafnakerfi skilgreiningar getur verið úr eftirfarandi hlutum:

1.  Eigindargildi: Efni
2.  Textafasti: 'AAA'
3.  Eigindargildi: Lengd

Hægt er að færa inn eftirfarandi gildi fyrir hluta:

-   Númer afurðarsniðmáts = M0099
-   Efni = Plast
-   Lengd = 12

Númer afurðarafbrigðis verða: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Dæmi um víddarbyggðar skilgreiningar

Í þessu dæmi, er hægt að nota nafnakerfi afurðarafbrigðisnúmers sem samanstendur úr eftirfarandi hlutum:

1.  Númer afurðarsniðmáts
2.  Textafasti '//'
3.  Grunnstilling

Nafnakerfi skilgreiningar getur verið úr eftirfarandi hlutum:

1.  Afbrigðaflokkur: Cabinet
2.  Textafasti: '&'
3.  Skilgreiningaflokkur: framgrill

Hægt er að færa inn eftirfarandi gildi fyrir hluta:

-   Númer afurðarsniðmáts = D0123
-   Cabinet = M0008
-   Framgrill = M0022

Númer afurðarafbrigðis verða: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Árekstrar númera
Mögulegt er að setja upp afurð nafnakerfi afurðarafbrigðisnúmers sem leiðir ekki til einkvæmra númera afurðarafbrigða. Til dæmis, þetta gæti gerst ef ein virk afurðarvídd er ekki innifalin í nafnakerfi fyrir afurðarsniðmát sem notar forskilgreind tækni til skilgreiningar afbrigða. Árekstrar eru meðhöndluð mismunandi fyrir mismunandi skilgreiningartækni.

### <a name="predefined-variants"></a>Forskilgreint afbrigði

Villa mun eiga sér stað ef reynt er að handvirkt eða sjálfkrafa mynda afurðarafbrigði þar sem ein eða fleiri endar á því að hafa sömu númer afurðarafbrigðis. Til að forðast þetta er ætti nota allar virkar afurðarvíddir í afurðavíddaflokki, eða hafa númeraröð til að tryggja að númer afurðarafbrigðis eru einkvæm.

### <a name="constraint-based-configurations"></a>Skorðuskilgreiningar

Allt eftir nafnakerfiinu, getur kerfið reynt að úthluta númeri afurðarafbrigðis á skilgreiningu sem ekki er einkvæmt. Í þessu tilfelli mun kerfið nota númeraröð fyrir vídd skilgreiningarvíddina sem númer afurðarafbrigðis í staðinn. Ef það gerist, mun viðvörun berast. Svo hægt sé að forðast þetta er ætti hafa nógu margar eigindir í nafnakerfiinu til að tryggja einkvæmni, og að tryggja að **Endurnota** valkosturinn sé kveiktur fyrir íhlutinn.

### <a name="dimension-based-configurations"></a>Víddaskilgreiningar

Skilgreiningarferli inniheldur skref þar sem kerfið leggur til gildi skilgreiningar samkvæmt því nafnakerfi. Í þessu skrefi geturðu Handvirkt breytt gildi skilgreiningarinnar. Þegar skilgreining er vistað, mun kerfið athuga hvort gildi skilgreiningar er einkvæmt. Ef svo reynist ekki vera, birtast villuboð. Færa þarf inn gildi einkvæmrar skilgreiningar til að vista skilgreininguna.



<a name="see-also"></a>Sjá einnig
--------

[Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði (verkefnaleiðbeiningar)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[ Stofna nafnakerfi afurðarafbrigðis fyrir skilgreind afurðarafbrigði (verkefnaleiðbeiningar)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)





---
title: Hanna grunnstillingar rafrænnar skýrslugerðar til að þátta skjöl á innleið
description: Ferlið sýnir hvernig skal hanna grunnstillingar rafrænnar skýrslugerðar til að þátta móttekin rafræn skjöl.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8068850ee143540ff9f3b6222485d3ecd2a2a82020063f34cfd7b5a69826eda3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756382"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Hanna grunnstillingar rafrænnar skýrslugerðar til að þátta skjöl á innleið

[!include [banner](../../includes/banner.md)]

Ferlið sýnir hvernig skal hanna grunnstillingar rafrænnar skýrslugerðar til að þátta móttekin rafræn skjöl. Í þessu ferli mun notandi flytja inn þær grunnstillingar rafrænnar skýrslugerðar sem krafist er, sem hafa verið stofnaðar fyrir sýnifyrirtækið, Litware, Inc., og nota þær til að þátta rafræn skjöl á innleið. Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið „Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka“.

Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.

Skrefin er hægt að klára með því að nota hvaða gagnasafn sem er. Áður en hafist er handa skal hlaða niður og vista skrárnar sem eru tilteknar í efnisatriðinu ([Þátta móttekin skjöl til að uppfæra forritsgögn](../parse-incoming-electronic-documents.md)). Skrárnar eru: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk. Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu, „Stofna skilgreiningarveitu og merkja hana sem virka”.
2. Veldu Skilgreiningar skýrslugerðar.
    * Eftirfarandi aðstæður verða notaðar til að sýna möguleika á að þátta móttekin rafræn skjöl á XML-sniði: ERP umsókn () biður um gögn frá vefþjónustunni (eins og [efsta](http://efsta.org/) fjárhagsþjónusta) og þáttar innkomin svör til að uppfæra umsóknargögn í samræmi við það. Skilvirkasta leiðin til að þátta er að nota einfalt snið rafrænnar skýrslugerðar þrátt fyrir muninn í uppbyggingu móttekinna skjala á XML-sniði.

## <a name="import-and-review-er-configurations"></a>Flytja inn og fara yfir grunnstillingar rafrænnar skýrslugerðar

Flytja skla inn grunnstillingargerð rafrænnar skýrslugerðar sem inniheldur gagnalíkanið með sýnigögnum sem ætlað er að geyma upplýsingar um móttekna skrá.

1. Veldu Gengi.
2. Veldu Hlaða úr XML-skrá.
    * Veljið Fletta og veljið EFSTA model.xml skrá.
3. Veljið Í lagi.
4. Í trénu skal velja „EFSTA líkan“.
5. Veljið Hönnuður.
    * Yfirfara skipan innflutt gagnalíkans. EnumType tölusetning er skilgreind til að bera kennsl á eftirfarandi gerðir þjónustuþátta: Til að fá staðfestingu um færslusendingu, til að fá upplýsingar um síðustu færslu sem var send og til að viðurkenna óstuddar svarstegundir.
6. Stækkið „Svar“ í trénu.
    * Rótarhlutinn „Svar“ er skilgreindur til að tilgreina hvaða tegundir gagna þarf að fá frá studdu þjónustusvari til að uppfæra umsóknargögn í samræmi við það.
7. Lokið síðunni.
    * Flytja verður inn grunnstillingarsnið rafrænnar skýrslugerðar sem tilgreinir hvernig móttekið skjal verður þáttað til að vista gögn í gagnalíkani rafrænnar skýrslugerðar.
8. Veldu Gengi.
9. Veldu Hlaða úr XML-skrá.
    * Flettið og veljið EFSTA format.xml skrá.
10. Veljið Í lagi.
11. Í trénu skal víkka út „EFSTA líkan“.
12. Í trénu skal velja „EFSTA líkan\EFSTA snið“.
13. Veljið Hönnuður.
14. Veljið Víkka/draga saman.
    * CASE-sniðseiningin er notuð sem rót og inniheldur þrjár faldaða FILE-þætti, sem þýðir að þetta snið hefur verið hannað til að þátta mótteknar skrár á nokkrum sniðum.
15. Í trénu skal velja „Svör\Færslu lokið\TraC“.
    * Svarið við umbeðinni færslu hefst frá ‘TraC’ rótareiningunni.
16. Í trénu skal velja „Svör\Síðasta færslubeiðni\Tra“.
    * Athugið að svarið við síðustu umbeðinni færslu hefst frá ‘Era’ rótareiningunni.
17. Í trénu skal velja „Svör\Óvænt svar\Texti“.
    * Þriðju FILE-einingu með faldaðri TEXT-einingu hefur verið bætt við til að auðkenna allar aðrar gerðir svara sem eru frábrugðin því sem tiltekið er að ofan.
18. Velja Varpa sniði á líkan.
    * Þessi líkanavörpun inniheldur skilgreininguna á gagnaflæði til að geyma upplýsingar um þáttað móttekið skjal með því að nota hluti gagnalíkansins.
19. Veljið Hönnuður.
20. Í trénu skal víkka út „snið“.
21. Í trénu skal víkka út „snið\Svör: Tilvik(Svör)“.
    * Fara yfir uppbyggingu „format” gagnagjafa. Boðið er upp á allar þrjár tegundir svara.
22. Í trénu skal velja „snið\Svör: Tilvik(Svör)\aGerð“.
    * Afurð gagnagjafa „aType” hefur verið bætt við til að tákna svargerðina og er bundin við gagnalíkanseininguna „Type”.
23. Veljið flipann Sannprófanir.
24. Í trénu skal velja „Type = format.Responses.aType“.
    * Sannprófun rafrænnar skýrslugerðar hefur verið grunnstillt til að upplýsa notanda um aðstæður þegar svarskipulagið samræmist ekki staðfestingu um færslubeiðni eða upplýsingum um síðustu sendafærslu (óstutt svartilvik).
25. Lokið síðunni.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Keyra líkanavörpun sniða rafrænnar skýrslugerðar sem eru grunnstillt fyrir þáttun móttekinna skráa

Notandi mun keyra tilbúna líkanavörpun í prófunarskyni til að sjá hvernig grunnstillt snið rafrænnar skýrslugerð ar mun þátta móttekin þjónustusvör. Þetta skref notar mismunandi XML-skrár til að líkja eftir mismunandi tegundum svara vefþjónustu.

1. Opnið Response1.xml skrána í XML-lesforriti, svo sem eins og vafra. Þessi skrá inniheldur staðfestingarupplýsingar um loknu færsluna („TraC“ er rótareiningin).
2. Veljið Keyra.
    * Veljið Fletta og veljið Response1.xml skrá.
3. Veljið Í lagi.
    * Fara yfir myndað úttak. Kennsl hafa verið borin á svargerðina og hún þáttuð (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` merkir lokið færslutilvik).
    * Opnið Response2.xml skrána í XML-lesforriti. Þessi skrá inniheldur upplýsingar um síðustu umbeðnu færsluna (`Tra` er rótarþáttur).
4. Veljið Keyra.
    * Veljið Fletta og veljið Response2.xml skrá.
5. Veljið Í lagi.
    * Fara yfir myndað úttak. Kennsl hafa verið borin á svargerðina og hún þáttuð (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` merkir endurræsingu kerfis).
    * Opnið Response3.xml skrána í XML-lesforriti. Þessi skrá hefst úr TraZ-rótaratriði og að þessi uppbygging er ekki grunnstillt með sniði rafrænnar skýrslugerðar.
6. Veljið Keyra.
    * Veljið Fletta og veljið Response3.xml skrá.
7. Veljið Í lagi.
    * Fara yfir myndað úttak. Kennsl hafa verið borin á svargerðina og hún er ekki studd (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Samsvarandi skilaboð hafa verið sett í Infolog (í samræmi við sannprófunarstillingu rafrænnar skýrslugerðar) og flest gagnalíkan hafa ekki verið fyllt út.
    * Opnið Response4.xml skrána í XML-lesforriti. Athugið að ulínurnarUppbygging þessarar skráar er næstum því sú sama og þáttaða skráin Response1.xml, fyrir utan röð þáttaðra eininga rótareiningarinnar ‘TraC’.
8. Veljið Keyra.
    * Veljið Fletta og veljið Response4.xml skrá.
9. Veljið Í lagi.
    * Fara yfir myndað úttak. Kennsl hafa verið borin á svargerðina og hún er ekki studd (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Samsvarandi skilaboð hafa verið sett í Infolog og flest gagnalíkan hafa ekki verið fyllt út. Þessi hegðun er vegna þess að núverandi stilling þessa sniðs rafrænnar skýrslugerðar gerir ráð fyrir ákveðinni röð þáttaðra eininga rótareiningar móttekinnar skráar.
10. Lokið síðunni.
11. Í trénu skal velja „Svör\Færslu lokið\TraC“.
12. Í „Þáttunarröð faldaðra eininga“ skal velja „Einhver“.
    * Veljið Einhver í reitinum „Þáttunarröð faldaðra eininga” til að leyfa allar gerðir faldaðra eining fyrir þessa XML-rótareiningu.
13. Veljið Vista.
14. Velja Varpa sniði á líkan.
15. Veljið Keyra.
    * Veljið Fletta og veljið Response4.xml skrá.
16. Veljið Í lagi.
    * Fara yfir myndað úttak. Kennsl hafa verið borin á svargerðina og hún er jöfn og Response1.xml skrá.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
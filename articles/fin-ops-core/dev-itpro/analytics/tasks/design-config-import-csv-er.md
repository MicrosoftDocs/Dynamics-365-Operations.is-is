---
title: Hanna ER skilgreiningar til að flytja inn gögn úr ytri CSV-skrám
description: Nota skal þetta til að hanna grunnstillingar rafrænnar skýrslugerðar til að flytja inn gögn í Finance and Operations forrit úr ytri skrá á CSV-sniði.
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
ms.openlocfilehash: b42f0cf8c7260c85d405a5dfdcd50323ffee4d4528b982997a802b859ab8327b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747272"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>Hanna ER skilgreiningar til að flytja inn gögn úr ytri CSV-skrám

[!include [banner](../../includes/banner.md)]

Nota skal þetta til að hanna grunnstillingar rafrænnar skýrslugerðar til að flytja inn gögn í forritið, úr ytri skrá á CSV-sniði. Í þessu ferli mun notandi flytja inn þær grunnstillingar rafrænnar skýrslugerðar sem krafist er fyrir sýnifyrirtækið Litware, Inc. Til að ljúka þessum skrefum verður fyrst að ljúka skrefum ferlisins „Rafræn skýrslugerð Stofna grunnstillingarveitu og merkja hana sem virka“.

Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota USMF gagnasafnið.

Enn fremur þarftu að hlaða niður og vista eftirfarandi skrár staðbundið: [Dynamics 365 Finance Electronic Reporting Examples](https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Hægt er að stilla ferli á að flytja ytri skrár á XML, TXT eða CSV-sniði í töflur í forritið. Í fyrsta lagi þarf að búa til sértækt gagnalíkan til að tákna innflutt gögn, frá sjónarmiði fyrirtækis - stilling gagnalíkans rafrænnar skýrslugerðar er búin til fyrir það. Næst skal skilgreina uppbyggingu innfluttu skráarinnar sem er varpað í viðkomandi gagnalíkan sem leið til að flytja inn gögn úr skránni í sértaka gagnalíkanið - stilling sniðs rafrænnar skýrslugerðar er búið til fyrir það. Síðan þarf að víkka út stillingu gagnalíkans fyrir rafræna skýrslugerð með nýrri líkanavörpun sem lýsir því hvernig gögnin í innfluttu skránni og varanlegum gögnum úr sértæka gagnalíkaninu eru notuð til að uppfæra forritatöflurnar eða gagnaeiningar.
    * Eftirfarandi skref sýna hvernig raktar færslur ytri lánardrottins eru fluttar inn úr ytri CSV-skrá til síðari notkunar í uppgjöri lánardrottins fyrir 1099 formið.
    * Sannprófið að grunnstillingarveita fyrir sýnifyrirtækið Litware, Inc. sé tiltæk og merkt sem virk. Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Notaðu síuna '1099 Greiðslulíkan'. Ef ferlinu „Búa til nauðsynlegar skilgreiningar til að flytja inn gögn úr ytri skrá fyrir rafræna skýrslugerð (ER)“ og „1099 Greiðslulíkan“ stillingin er í boði í stillingatrénu skal sleppa öllum skrefunum í næsta undirverkefni.

## <a name="add-a-new-er-model-configuration"></a>Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð

1. Í stað þess að stofna nýtt snið til að styðja við gagnainnflutning skal hlaða skránni 1099model.xml sem áður var sótt. Þessi skrá inniheldur sérstillt gagnalíkan yfir færslur lánardrottins. Þessu gagnalíkani er þegar varpað í nauðsynleg gagnalíkan.
2. Smellt er á Skipta út.
3. Smellt er á Hlaða úr XML-skrá.
4. Smellt er á Fletta og flett á skrána 1099model.xml sem áður var sótt.
5. Smellið á „Í lagi“.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð sem styður innflutningur gagna

1. Í tré skal velja '1099 Greiðslulíkan'.
2. Smellt er á stofna skilgreiningu til að opna fellilistanum.
3. Í svæði Nýtt skal slá inn „Snið byggir á gagnalíkani 1099 Greiðslulíkan“.
4. Velja Já í svæði Styður gagnainnflutning.
5. Ýtt á ESC-lykil til að loka þessari síðu.
    * Í stað þess að stofna nýtt snið rafrænnar skýrslugerðar til að styðja við gagnainnflutning skla hlaða niðurskránni 1099formatcsv.xml sem áður var sótt. Þessi skrá inniheldur nauðsynlegt snið rafrænnar skýrslugerðar sem skilgreinir uppbyggingu móttekinnar CSV-skráar og vörpun uppbyggingarinnar í gagnalíkan yfir færslur lánardrottins.
6. Smellt er á Skipta út.
7. Smellt er á Hlaða úr XML-skrá.
    * Smellt er á Fletta og flett á skrána 1099formatcsv.xml sem áður var sótt.
8. Smellið á „Í lagi“.
9. Í trénu skal víkka út ‚1099 Greiðslulíkan'.
10. Í trénu skal velja „1099 Greiðslulíkan\Til að flytja inn færslur lánardrottna (CSV)upplýsingar“.

## <a name="review-format-settings"></a>Fara yfir stillingar sniðs

1. Smellið á Hönnuður.
2. Smellt er á Víkka/draga saman.
3. Kveikið á „Sýna upplýsingar“.
    * Uppsetta sniðið stendur fyrir væntanlegt uppbyggingu ytri skráar á CSV-sniði.
4. Í trénu skal velja „Á innleið: Skrá\Rót: Röð“.
    * Fyrir rótareininguna af gerðinni SEQUENCE hefur valkosturinn „ný lína - Windows (CR LF)“ verið valinn í reitnum „Sértákn“. Byggt á þessari stillingu verður að líta á hverja línu í þáttunarskrá sem sérstakt færslu.
5. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..*`“.
    * Fyrir eininguna Rót\Lína af gerðinni SEQUENCE hefur valkosturinn „Einn margir“ verið valinn í svæðinu „Margfeldi“. Byggt á þessari stillingu verður að minnsta kosti ein lína til staðar í þáttunarskránni.
6. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case`“.
    * Athugið að þátturinn Rót\Lína\Gerðir af gerðinni CASE hefur verið bætt við sem faldaðri einingu í röðinni Rót\Lína. Vegna þess að þessi CASE eining inniheldur 3 faldaða raðarþætti gerir þessi stilling ráð fyrir 3 mismunandi gerðum línu í þáttunarskránni.
7. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1`“.
    * Einingin Rót\Lína\Gerðir\Haus af gerðinni SEQUENCE inniheldur faldaða STRING einingu þar sem gildið hefur verið skilgreint sem fast strengjagildi. Þessi röð mun þátta hauslínuna á þáttunarskránni.
8. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)`“.
    * Einingin Rót\Lína\Gerðir\Færsla af gerðinni SEQUENCE hefur verið stillt á að þátta færslulínurnar. Athugið að stafavalkosturinn „Sérsniðið skiltákn” hefur verið stilltur sem komma. Þetta þýðir að komman verður notuð sem aðgreining fyrir þessa gerð línu í þáttunarskránni.
    * Athugið að nokkrir faldaðir þættir af mismunandi gagnagerðum hefur verið bætt við eininguna Root\Line\Types\Record fyrir þáttun færslulínanna sem aðskildir reitir. Athugaðu að valkosturinn „Notkun gæsalappa“ hefur verið stilltur sem „Ekkert“. Þetta þýðir að í þáttunarskránni verður litið svo á að allir reitir af þessari gerð hafi enga meðfylgjandi stafi.
9. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime`“.
    * Til dæmis er einingin Root\Line\Types\Record\TransactionDate af gerðinni DATETIME stillt á að fá færsludagsetningar og tímagildi úr þáttunarskrá á „M/d/yyyy“-sniði.
10. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1`“.
    * Athugið að einingin Rót\Lína\Gerðir\Færsla\Landskóði af gerðinni STRING hefur verið stillt þannig að hún hafi valkostinn „Núll einn“ í reitnum „Margfeldi“. Þessi stilling tekur gildi CountryCode reitsins í flokkalínunni sem valfrjálst.
11. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)`“.
    * Athugið að einingin Rót\Lína\Gerðir\Færsla\Athugasemd af gerðinni SEQUENCE hefur verið stillt þannig að hún hafi valkostinn „Allt“ í reitnum „Notkun gæsalappa“ og staf með tvöföldum gæsalöppum í reitnum „Gæsalappir”. Það þýðir að allir reitir af þessari gerð af línum í þáttaskránni (sem lýst er með földuðum einingum: Texti af STRING-gerð) telst vera innan gæsalappa.
12. Í trénu skal velja „`Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1`“.
    * Einingin Rót\Lína\Gerðir\Óþáttað af gerðinni SEQUENCE hefur verið stillt á að þátta færslulínurnar fyrir uppbygginguna sem passar ekki við uppbygginguna sem lýst er hér að ofan í CASE yfireiningunni.

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Fara yfir stillingu á vörpun sniðs í gagnalíkan

1. Smellt er á Varpa sniði á líkan.
    * Líkanavörpunin „Kortlagning á líkani úr CSV-sniði” lýsir gagnaflæði gagnaflutningsins frá móttekinni CSV-skrá í gagnasniðið.
2. Smellið á Hönnuður.
3. Í trénu skal víkka út „snið“.
    * Athugið að uppsett snið er sett hér fram sem íhlutur gagnaveitu.
4. Í trénu skal víkka út „snið\Á innleið: Skrá(Á innleið)“.
5. Í trénu skal víkka út „snið\Á innleið: Skrá(Á innleið)\Rót: Röð(Rót)“.
6. Í trénu skal víkka út „`format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)`“.
7. Í trénu skal víkka út „`format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)`“.
8. Í trénu skal víkka út „`format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)`“.
9. Í trénu skal víkka út „`format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data`“.
10. Í trénu skal víkka út „`format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)`“.
11. Í trénu skal velja „`format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)`“.
    * Athugið að skyldubundnar og valkvæmar sniðseiningar, á borð við TransactionDate og CountryCode, líta öðruvísi út í fyrirframskilgreindum íhluti gagnaveitu „sniðs“.
12. Í trénu skal víkka út 'Transactions = '$both''.
    * Athugið að einingar sniðsins sem skilgreinir uppbyggingu innfluttrar skrár eru festar við einingar í gagnalíkani. Út frá þessum bindingum verður innihald þessara innfluttu CSV-skráa vistað í keyrslutíma í fyrirliggjandi gagnalíkani. Athugið sérstaklega bindingu CountryRegion einingarinnar. Fyrir hverja færslueiningu í skrá á innleið sem ekki er með slíka gagnakóðagildi verður fyllt út í gagnalíkan með sjálfgefnum landskóða „USA“.
13. Kveikið á „Sýna upplýsingar“.
14. Smellt er á flipann Sannprófanir.
15. Smellið á leita.
16. Í svæðinu Finna færirðu inn „vend“.
17. Smellt er á Finna næsta.
    * Þessi vörpun sniðs gæti innihaldið notandaskilgreindar reglur til að sannprófa nákvæmni innfluttra gagna út frá viðskiptasjónarmiði. Til dæmis, út frá stillingu, fyrir hverja færslu í innfluttri skrá þar sem uppbygging passar hvorki við uppbyggingu línuhauss eða færslulínu munu myndast viðvörunarboð í upplýsingaskránni sem láta notanda vita um málið og vísa á númeraröð færslu í skránni.
18. Lokið síðunni.

## <a name="run-the-format-mapping"></a>Keyra vörpun sniðs

Til að prófa skal framkvæma sniðsvörpun með því að nota 1099entriescsv.csv-skrána sem sótt var áður. Myndað úttak birtir gögn sem verða flutt inn úr valinni CSV-skrá og fyllt út í sérstillt gagnalíkan í rauninnflutningi.

1. Smellið á „Keyra“.
    * Smellt er á Fletta og flett á csv-skrána 1099entriescsv.csv sem áður var sótt.
2. Smellið á „Í lagi“.
    * Athugaðu viðvörunarboðin um línur sem eru ekki samþykktar. Lína 4 inniheldur tekjuvirðið sem er kynnt í óviðunandi sniði en lína 7 inniheldur ekki færslutilkynninguna í tvöföldum gæsalöppum.
    * Farið yfir úttak í XML-sniði, sem stendur fyrir gögn sem hafa verið innflutt úr valinni skrá og tengd við gagnalíkan. Athugaðu að allar 7 línur af innfluttu CSV-skránni voru unnar. Reitum sem innihalda titilinn í línu 1 var sleppt, 4 færslur voru þáttaðar á réttan hátt og 2 færslur voru viðurkenndar sem ógildar.
3. Lokið síðunni.
4. Lokið síðunni.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
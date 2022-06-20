---
title: Óreikningsfærðar tekjur
description: Þessi grein útskýrir hvernig á að setja upp vörur og reikninga til að nota óinnheimtu teknaeiginleikann í innheimtu áskriftar.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b3fe58fc06df3f61433c8457b337ae895283e12b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879683"
---
# <a name="unbilled-revenue"></a>Óreikningsfærðar tekjur

Þessi grein lýsir óinnheimtu teknaeiginleikanum sem gerir þér kleift að taka með upphæðir fyrir heilar innheimtuáætlanir á efnahagsreikninginn. Þessar upphæðir eru innifaldar á óinnheimtu tekjureikningi og óinnheimtu tekjujöfnunarreikningi og samningurinn er innheimtur með raðgreiðslum.

## <a name="set-up-unbilled-revenue"></a>Settu upp óinnheimtar tekjur

Fylgdu þessum skrefum til að setja upp óinnheimtar tekjur.

- Á **Endurteknar innheimtufæribreytur samnings** síðu, stilltu reitina í **Óinnheimtar tekjur** kafla.
- Hægt er að nota óinnheimtu teknaeiginleikann fyrir hluti þar sem **Tegund vöru** reiturinn er stilltur á **Standard**. Það er einnig hægt að nota til að fresta hlutum. Til að nota óinnheimtar tekjur með skammtímaaðgerðinni skaltu setja upp skammtímavalkostina á **Endurteknar innheimtufæribreytur samnings** síðu.

Fylgdu þessum skrefum til að setja upp vörur til að nota óinnheimtar tekjur.

1. Á **Uppsetning óinnheimtutekna** síðu, á **Hlutir** flipa, veldu **Bæta við**.
2. Á nýju línunni, í **Vörukóði**, veldu vörunúmerið.
3. Í **Atriðatengsl** reit, veldu hluttengsl.
4. Endurtaktu þessi skref til að bæta við fleiri línum.
5. Veldu **Vista**.

Fylgdu þessum skrefum til að setja upp vörur og óinnheimtu tekjureikninga.

1. Á **Uppsetning óinnheimtutekna** síðu, á **Reikningar** flipa, veldu **Bæta við**.
2. Á nýju línunni, í **Vörukóði**, veldu vörunúmerið.
3. Í **Atriðatengsl** reit, veldu hluttengsl.
4. Veldu reikninga fyrir óinnheimtu tekna, óinnheimtu afslátt og óinnheimtu teknajöfnun. Til að nota skammtímareikningana verður þú að stilla **Skammtíma óinnheimt aðferð** sviði til **Rúllutímabil** eða **Fast ártal** á **Endurteknar innheimtufæribreytur samnings** síðu.
5. Endurtaktu þessi skref til að bæta við fleiri línum.
6. Veldu **Vista**.

## <a name="use-unbilled-revenue"></a>Notaðu ógreiddar tekjur

1. Á **Allar innheimtuáætlanir** síðu, búðu til innheimtuáætlun.
2. Ef varan er ekki enn sett upp til að nota óinnheimt tekjur skaltu velja **Óinnheimtar tekjur** gátreitinn á innheimtuáætlunarlínunni.
3. Stilltu **Óinnheimtar tekjur** valmöguleika til **Já**. Skoðaðu síðan og breyttu óinnheimtu tekna-, afsláttar- og óinnheimtujöfnunarreikningunum eftir þörfum.
4. Á innheimtuáætlun, skv **Óinnheimt tekjuvinnsla**, veldu **Stofna dagbókarfærslu** til að stofna upphafsbókarfærslu fyrir óinnheimtar tekjur. Þessu skrefi verður að ljúka áður en innheimtuáætlun er reikningsfærð.
5. Eftir að upphafsbókarfærslan er búin til skaltu velja **Búðu til reikning** til að stofna sölupantanir og bóka reikninga fyrir innheimtuáætlanir.
6. Eftir að reikningarnir eru bókaðir er hægt að skoða endurskoðunarupplýsingarnar á **Endurnýjun** flipi á **Allar innheimtuáætlanir** síðu.

### <a name="milestone-billing"></a>Útskrift samkvæmt þáttaskilum

Áfangareikningur virkar með óinnheimtu tekna við eftirfarandi skilyrði:

- Ef upphafsliðurinn er óinnheimtaður (þ **Óinnheimtar tekjur** gátreiturinn er valinn) og undirliðir tímamóta eru rukkaðir (the **Óinnheimtar tekjur** gátreiturinn er hreinsaður), þarf að tilgreina upphafs- og lokadagsetningar fyrir yfirvöru. Þessar dagsetningar eru notaðar til að stofna upphafsbókarfærsluna.
- Ef upphafsliðurinn er óinnheimtaður (þ **Óinnheimtar tekjur** gátreiturinn er hreinsaður) og undirliðir áfangamarkmiða eru rukkaðir (the **Óinnheimtar tekjur** gátreiturinn er valinn), verður lokadagsetningin að vera tilgreind aðeins fyrir undirliðina sem þú vilt búa til upphafsbókarfærsluna fyrir.

Hægt er að vinna úr hverri undirstöðuatriði fyrir sig. Hægt er að tilgreina lokadagsetningar þegar þú ert tilbúinn að búa til upphafsbókarfærsluna.

> [!NOTE]
> Ef upphafsbókarfærslan fyrir upphafs- eða undiratriðin hefur þegar verið stofnuð, eða reikningur hefur verið stofnaður, er ekki hægt að breyta upphafs- og lokadagsetningum.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Óinnheimtar tekjur með beinni frestun

Til að nota óinnheimtaðar tekjur með beinni frestunaráætlun skaltu fylgja þessum skrefum.

1. Á **Allar innheimtuáætlanir** síðu, búðu til innheimtuáætlun.
2. Bættu hlut við innheimtuáætlunarlínurnar.
3. Veldu **Frestun** fyrir línuna.
4. Á **Frestun viðskipta** síðu, fylgdu þessum skrefum:

    1. Stilltu **Frestað** valmöguleika til **Já**.
    2. Breyttu reikningunum eins og þú vilt.
    3. Í **Dagskrá** kafla, veldu **Bein lína**, og breyttu öðrum gildum eftir þörfum.
    4. Veldu **Í lagi**.

5. Veldu **Óinnheimtar tekjur** fyrir línuna og fylgdu síðan þessum skrefum:

    1. Stilltu **Óinnheimtar tekjur** valmöguleika til **Já**.
    2. Veldu reikninga sem á að nota fyrir tekjur, afslátt og tekjujöfnun.

6. Á innheimtuáætlun, skv **Óinnheimt tekjuvinnsla**, veldu **Stofna dagbókarfærslu**. Að öðrum kosti skaltu nota **Óreikningsfærð tekjur fjöldavinnsla** síðu til að búa til dagbókarfærsluna.
7. Frestunaráætlun er búin til. Þú getur skoðað upplýsingarnar á **Allar frestunaráætlanir** síðu. Eftir að frestunaráætlunin er búin til er hægt að breyta ýmsum gildum fyrir línuatriði innheimtuáætlunar. Til dæmis er hægt að breyta einingaverði, magni eða dagsetningum.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Óinnheimtar tekjur með frestun sem byggist á viðburðum

Fylgdu þessum skrefum til að nota óinnheimtar tekjur með frestunaráætlanir sem byggjast á viðburðum.

1. Á **Allar innheimtuáætlanir** síðu, búðu til innheimtuáætlun.
2. Bættu hlut við innheimtuáætlunarlínurnar.
3. Veldu **Frestun** fyrir línuna.
4. Á **Frestun viðskipta** síðu, fylgdu þessum skrefum:

    1. Stilltu **Frestað** valmöguleika til **Já**.
    2. Breyttu reikningunum eins og þú vilt.
    3. Í **Dagskrá** kafla, veldu **Byggt á viðburðum**, **·**, **úthlutunar**, og **Lokareikningur**.
    4. Veldu **Í lagi**.

5. Veldu **Óinnheimtar tekjur** fyrir línuna og fylgdu síðan þessum skrefum:

    - Stilltu **Óinnheimtar tekjur** valmöguleika til **Já**.
    - Veldu reikninga sem á að nota fyrir tekjur, afslátt og tekjujöfnun.

6. Á innheimtuáætlun, skv **Óinnheimt tekjuvinnsla**, veldu **Stofna dagbókarfærslu**. Að öðrum kosti skaltu nota **Óreikningsfærð tekjur fjöldavinnsla** síðu til að búa til dagbókarfærsluna.
7. Frestunaráætlun er búin til. Þú getur skoðað upplýsingarnar á **Allar frestunaráætlanir** síðu. Eftir að frestunaráætlunin er búin til er hægt að breyta ýmsum gildum fyrir línuatriði innheimtuáætlunar. Til dæmis er hægt að breyta einingaverði, magni eða dagsetningum. Frestunaráætlunin er endurreiknuð út frá nýju gildunum.

Dreifingarnar eru endurreiknaðar út frá úthlutunargerðinni sem er valin (**Hlutfall**, **·**, eða **Jafnar upphæðir**). Fyrir **Breytileg upphæð** úthlutunartegund er dreifingin endurreiknuð miðað við prósentuígildi upphafsgildis viðburðarins. Til dæmis er upprunalega einingaverðið $100.00 og prósentan af upphafsgildinu er $55.00 (55 prósent). Ef einingaverðinu er breytt í $200.00 verður breytileg upphæð viðburðarins $110.00 (enn 55 prósent).

> [!NOTE]
> Ef frestunaráætlunarlínur hafa verið viðurkenndar er ekki hægt að breyta innheimtuáætlunarlínunni. Til að breyta línunni verður þú fyrst að snúa viðurkenndu línunum við. Þá er hægt að uppfæra innheimtuáætlunarlínuna.

### <a name="unbilled-revenue-and-top-billing"></a>Óinnheimtar tekjur og toppinnheimta

Innheimtuáætlun er færð til þriggja ára og eru reikningar innheimtir árlega á þriggja ára tímabili. Öll samningsupphæðin er skráð á óinnheimtu tekjureikninginn sem árlegir reikningar eru búnir til. Mótreikningur er tekjureikningur eða frestaðar tekjureikningur.

Athugaðu að toppinnheimta og óinnheimtar tekjur vinna ekki saman, vegna þess að afstemmingarvandamál geta komið upp í fjárhag. Til dæmis, á **Uppsetning vöruhóps** síðu er liður A settur upp þannig að **Fjöldi efstu lína** reiturinn er stilltur á **2**. Á **Innheimtuáætlanir** síðu, þremur atriðum er bætt við. Allar þrjár vörurnar tilheyra vöruflokki A. Þegar upphafsbókarfærslan er stofnuð fyrir óinnheimtu teknaeiginleikann, er upphæðin fyrir allar þrjár vörurnar unnin á óinnheimtu reikninginn. Þegar reikningur fyrir innheimtuáætlun er stofnaður eru aðeins upphæðir fyrir efstu tvær liði teknar með. Þess vegna samsvarar reikningsupphæð ekki upphæðinni sem var unnin á óinnheimtu tekjureikninginn og afstemmingarvandamál eiga sér stað í fjárhag.

Ef þú vilt nota ógreiddar tekjur skaltu skilja eftir **Uppsetning vöruhóps** blaðsíða auð, eða settu upp alla vöruflokka þannig að **Fjöldi efstu lína** reiturinn er stilltur á **0** (núll). Ef þú vilt nota toppinnheimtu þá eru engar óinnheimtar tekjur tiltækar.

### <a name="examples"></a>Dæmi

Frá og með útgáfu 10.0.27 er nýr reikningur tekinn upp þegar óinnheimtar tekjur eru notaðar. Þegar upphafs **Stofna dagbókarfærslu** ferlið er bókað, er inneignin færð á nýjan óinnheimtaðan tekjujöfnunarreikning. Þessi reikningur er notaður í stað tekjureiknings, vegna þess að sama gildi verður að bakfæra þegar innheimtuáætlun er reikningsfærð. Ef gengis- eða námundunarmunur á sér stað munu upphæðir sem eru reiknaðar á tímabilinu **Búðu til reikning** ferli gæti verið öðruvísi. Þessi hegðun tryggir að nettóupphæð reikninganna sé 0 (núll).

Þetta dæmi sýnir hvernig á að nota óreikningsfærðar tekjur til að færa heildarfjárhæð samnings á efnahagsreikningi sem óreikningsfærðar tekjur. Hin hliðin á færslunni er óreikningsfærð tekjujöfnun. Þegar þú reikningsfærðu viðskiptamanninn, eru óreikningsfærðar tekjur og óreikningsfærðar tekjur bakfærðar. Tekjufærsla mun eiga sér stað annað hvort við reikningsgerð eða samkvæmt áætlun um frestun á færslu sem sett var upp.

#### <a name="assumptions"></a>Forsendur

- Þann 1. janúar á yfirstandandi ári skrifar viðskiptavinur undir þriggja ára samning um $390.
- Samningurinn felur í sér tvo hluta: leyfi og viðhaldssamning.
- Söluverð leyfisgjaldsins er $300 og verður viðskiptavinur reikningsfærður $100 1. janúar hvers samningsárs. $300 leyfisgjaldið verður tekið sem tekjur þegar samningurinn er undirritaður.
- Söluverð viðhaldsgjalds er $90 og verður viðskiptavinur reikningsfærður $30 1. janúar hvers samningsárs. $90 viðhaldsgjaldinu verður frestað og $2.50 verður viðurkennt í hverjum mánuði á gildistíma samningsins.
- Viðskiptavinurinn fær reikning $130 í upphafi (1. janúar) hvers þriggja ára samnings.

#### <a name="steps"></a>Skref

1. Setjið út vörurnar tvær sem óinnheimtar vörur. Nota **Uppsetning óinnheimtutekna** síðu til að setja upp þá hluti og reikninga sem nota óinnheimtar tekjur.
2. Í þessu dæmi er viðhaldsgjaldinu frestað. Hluturinn krefst frestunarsniðmáts, sem er sett upp á **Frestun sniðmát** síðu. Sniðmátið hefur a **Mánaðarlega** tímabilstíðni og viðurkenningartímabilslengd 36 mánuðir. Þess vegna eru tekjur á mánuði $2.50.
3. Á **Hlutum frestað sjálfgefið** síðu, stilltu **Viðhaldsgjald** sviði til **Frestunarhæfur hlutur**. Þetta skref og það næsta mun valda því að viðhaldsgjaldshluturinn verður frestað þegar hann er seldur eða innifalinn í innheimtuáætlun.
4. Veldu **Frestun vanskil** \> **Sniðmát**, og bættu við hlutnum fyrir viðhaldsgjaldið og beinlínusniðmátinu frá skrefi 2. Liðurinn viðhaldsgjald verður tengdur 36 mánaða frestunaráætlun.
5. Búðu til innheimtuáætlun sem inniheldur tvær óinnheimtu vörurnar. Innheimtuáætlun samningsins er sett upp með eftirfarandi atriðum.

    | Atriði | Upphafsdagsetning | Lokadagsetning | Upphæð | Greiðslutíðni | Frestunarliður | Óreikningsfærðar tekjur | Lýsing |
    |---|---|---|---|---|---|---|---|
    | Leyfi | Janúar 01, CY | 31. desember CY+2 | $100.00 | Árlega | Nr. | Já | Viðskiptavinurinn fær reikning $100.00 á hverju ári. Heildarfjöldi $300.00 verður fyrirfram færður sem óreikningsfærðar tekjur á efnahagsreikningi og sem tekjur af hagnaði og tapi. Hver reikningur mun lækka óinnheimta upphæð. |
    | Viðhald | Janúar 01, CY | 31. desember CY+2 | $30.00 | Árlega | Já | Já | Viðskiptavinurinn fær reikning $30.00 á hverju ári. Heildarfjöldi $90.00 verður skráður fyrirfram sem óreikningsfærðar tekjur og frestar tekjur á efnahagsreikningi. Hver reikningur mun lækka óinnheimta upphæð. Frestað tekjur verða færðar mánaðarlega á 36 mánuðum. |

6. Á **Allar innheimtuáætlanir** síðu, notaðu **Stofna dagbókarfærslu** ferli til að bóka samningsverðmæti í efnahagsreikninginn sem óreikningsfærðar tekjur.

Tvær dagbókarfærslur eru búnar til, ein fyrir hverja línu á innheimtuáætlun.

| Lykill óreikningsfærðra tekna | Ógjaldfærður mótlykill tekna | Debetupphæð | Kreditupphæð |
|---|---|---|---|
| Lykill óreikningsfærðra tekna | | $300.00 | |
| | Ógjaldfærður mótlykill tekna | | $300.00 |

| Lykill óreikningsfærðra tekna | Frestaðar tekjur | Debetupphæð | Kreditupphæð |
|---|---|---|---|
| Lykill óreikningsfærðra tekna | | $90.00 | |
| |Frestað viðhaldstekjur | | $90.00 |

Fyrsta dagbókarfærslan er bókuð á óreikningsfærðan tekjujöfnunarreikning og sú síðari er bókuð á frestað tekjureikning. Ef innheimtulínan hefur bæði óinnheimtaðar tekjur og frestar tekjur, er frestað teknareikningurinn notaður, ekki óreikningsfærða tekjujöfnunin. Samningurinn krefst þess að reikningur fyrir viðskiptavininn sé búinn til í upphafi hvers árs. Nota **Búðu til reikning** ferli til að búa til reikninginn. Þegar reikningurinn er búinn til eru eftirfarandi dagbókarfærslur búnar til.

| Aðallykill | Lykill óreikningsfærðra tekna | Debetupphæð | Kreditupphæð |
|---|---|---|---|
| Óinnheimt tekjujöfnun | | $100.00 | |
| | Lykill óreikningsfærðra tekna | | $100.00 |
| Viðskiptakröfur | | $100.00 | |
| | Tekjulykill | | $100.00 |

| Aðallykill | Lykill óreikningsfærðra tekna | Debetupphæð | Kreditupphæð |
|---|---|---|---|
| Framhaldstekjureikningur | | $30.00 | |
| | Lykill óreikningsfærðra tekna | | $30.00 |
| Viðskiptakröfur | | $30.00 | |
| | Framhaldstekjureikningur | | $30.00 |

Þessi sama dagbókarfærsla verður til með reikningum sem eru bókaðir í byrjun næstu tveggja ára. Nettóupphæð frestaðtekjureiknings verður 0 (núll), vegna þess að það er engin námundun eða gengismunur. Frestaðar tekjur verður að bakfæra nákvæmlega eins og þær voru færðar á meðan **Stofna dagbókarfærslu** ferli. Vegna þess að tekjur eru enn frestaðar og verða færðar síðar, á sér stað inneign á frestað tekjureikninginn aftur.

Í síðasta skrefi er færslubókarfærsla stofnuð í hverjum mánuði til að færa frestað viðhaldsgjaldstekjur. Dagbókarfærsluna er hægt að búa til með því að nota **Viðurkenningarvinnsla** síðu. Að öðrum kosti er hægt að búa það til með því að velja **Kannast við** fyrir línurnar á **Frestunaráætlun** síður.

| Lykill tekjufrestunar | Tekjulykill | Debetupphæð | Kreditupphæð |
|---|---|---|---|
| Frestað viðhaldstekjur | | $2.50 | |
| | Viðhaldstekjur | | $2.50 |

Þessi færslubók verður stofnuð í hvert sinn sem viðurkenningarferlið er keyrt fyrir þessa fresta vöru (alls 36 sinnum).

#### <a name="short-term-fixed-year"></a>Skammtímar: Föst ár

Þú getur notað óinnheimtar tekjur ásamt skammtímavirkninni með því að stilla **Óinnheimt til skamms tíma** sviði á **Endurteknar innheimtufæribreytur samnings** síðu. Eftirfarandi dæmi sýnir útreikninga sem eru gerðir þegar óinnheimtar tekjur eru notaðar ásamt **Fast ártal** skammtíma óinnheimt aðferð.

Innheimtuáætlun sem hefur eftirfarandi skilyrði er búin til:

- **Upphafsdagur:** 1. júní 2020
- **Loka dagsetning:** 31. desember 2021
- **Einingaverð:** $100
- **Tíðni:** Mánaðarlega

Á **Allar innheimtuáætlanir** síðu, upphafsdagbókarfærslan er búin til af **Stofna dagbókarfærslu** ferli. Núverandi skammtíma- og langtímafjárhæðir eru reiknaðar á eftirfarandi hátt:

- **Núverandi skammtíma óinnheimt tekjuupphæð:** $700
- **Núverandi langtíma óinnheimt tekjuupphæð:** $1,200

Reikningurinn er búinn til fyrir innheimtutímabilið frá 1. júní 2020 til 30. nóvember 2020. Núverandi skammtíma- og langtímafjárhæðir eru reiknaðar á eftirfarandi hátt:

- **Núverandi skammtíma óinnheimt tekjuupphæð:** $100
- **Núverandi langtíma óinnheimt tekjuupphæð:** $1,200

Reikningurinn er búinn til fyrir innheimtutímabilið frá 1. desember 2020 til og með 31. desember 2020. Núverandi skammtíma- og langtímafjárhæðir eru reiknaðar á eftirfarandi hátt:

- **Núverandi skammtíma óinnheimt tekjuupphæð:** $1,200
- **Núverandi langtíma óinnheimt tekjuupphæð:** $0

#### <a name="short-term-rolling-periods"></a>Skammtímar: Rúllutímabil

Þú getur notað óreikningsfærðar tekjur ásamt skammtímaaðgerðinni með því að stilla skammtíma óinnheimtuaðferðina á **Endurteknar innheimtufæribreytur samnings** síðu. Eftirfarandi dæmi sýnir útreikninga sem eru gerðir þegar óinnheimtar tekjur eru notaðar ásamt **Rúllutímabil** skammtíma óinnheimt aðferð.

Innheimtuáætlun sem hefur eftirfarandi skilyrði er búin til:

- **Upphafsdagur:** 1. júní 2020
- **Loka dagsetning:** 31. desember 2021
- **Einingaverð:** $100
- **Tíðni:** Mánaðarlega

Á **Allar innheimtuáætlanir** síðu, upphafsdagbókarfærslan er búin til af **Stofna dagbókarfærslu** ferli. Núverandi skammtíma- og langtímafjárhæðir eru reiknaðar á eftirfarandi hátt:

- **Núverandi skammtíma óinnheimt tekjuupphæð:** $1,200
- **Núverandi langtíma óinnheimt tekjuupphæð:** $700

Reikningurinn er búinn til fyrir innheimtutímabilið frá 1. júní 2020 til 30. nóvember 2020. Núverandi skammtíma- og langtímafjárhæðir eru reiknaðar á eftirfarandi hátt:

- **Núverandi skammtíma óinnheimt tekjuupphæð:** $1,200
- **Núverandi langtíma óinnheimt tekjuupphæð:** $100

Reikningurinn er búinn til fyrir innheimtutímabilið frá 1. desember 2020 til og með 31. desember 2020. Núverandi skammtíma- og langtímafjárhæðir eru reiknaðar á eftirfarandi hátt:

- **Núverandi skammtíma óinnheimt tekjuupphæð:** $1,200
- **Núverandi langtíma óinnheimt tekjuupphæð:** $0

### <a name="items-with-revenue-allocation"></a>Liðir með tekjuskiptingu

Tveimur hlutum sem hafa mismunandi innheimtutíðni er bætt við innheimtuáætlun. Báðir nota óinnheimtar tekjur og eru liðir sem hægt er að fresta.

- **Vörunúmer 1000:** Surface Pro 128GB

    - **Innheimtutíðni:** Einu sinni
    - **Einingaverð:** $1,500
    - **Sjálfstætt söluverð:** $1,600
    - **Samningstekjur:** $1,465.26

- **Vörunúmer S0021:** Trygging sem er seld ásamt vörunúmeri 1000

    - **Innheimtutíðni:** Mánaðarlega í 12 mánuði
    - **Einingaverð:** $20 á mánuði
    - **Sjálfstætt söluverð:** $25
    - **Samningstekjur:** $264.74

Vegna þess að báðar vörurnar nota óinnheimtar tekjur og úthlutun tekna er heildarupphæð samnings á endurnýjunarlínunni 0 (núll). The **Samningstekjur** dálki er bætt við og sýnir upphæð samningstekju.

Eftirfarandi tafla sýnir upphaflega færslubók fyrir vörurnar og reikninginn.

| Lykill óreikningsfærðra tekna | Lykill tekjufrestunar | Debetupphæð | Kreditupphæð |
|---|---|---|---|
| **Liður 1000 dagbókarfærsla** | | | |
| Debet óreikningsfærður tekjureikningur (401250) | | $1,465.26 | |
| | Tekjureikningur innheimtur (250600) | | $1,465.26 |
| **Liður 0021 Dagbókarfærsla** | | | |
| Debet óreikningsfærður tekjureikningur (401250) | | $274.74 | |
| | Tekjureikningur innheimtur (250600) | | $274.74 |
| **Reikningur** | | | |
| | Inneign á óinnheimtu tekjureikningi | | $1,465.26 |
| | Inneign á óinnheimtu tekjureikningi | | $274.74 |
| Debet AR reikningur (130100) | | $1,488.16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Breytingar á innheimtuáætlunarlínu, innheimtuupplýsingalínu eða tekjuúthlutun

Þegar einingaverði eða magni er breytt þarf að uppfæra samningstekjuupphæð fyrir hvern lið sem er hluti af tekjuúthlutuninni. Því er dagbókarfærslan endurreiknuð.

Til dæmis er einingaverði fyrir vöru 1000 breytt úr $1,500 í $1,600. Í þessu tilviki er upphæð samningstekna sjálfkrafa endurreiknuð sem $1,549.47. Samningstekjur fyrir lið S0021 eru endurreiknaðar sem $290.53.

Þegar breytingin er staðfest og framkölluð, er upphafsfærslubókarfærslum fyrir báðar færslur bakfærðar og nýjar færslubókarfærslur eru búnar til:

- **Atriði 1000:** Upprunalegri dagbókarfærslu $1,465.26 er snúið við. Ný dagbókarfærsla fyrir $1,549.47 er búin til.
- **Liður S0021:** Upprunalegri dagbókarfærslu $274.74 er snúið við. Ný dagbókarfærsla fyrir $290.53 er búin til.

#### <a name="termination"></a>Lok

Hlutur S0021 hefur upphafsdag í janúar 2020 og lokadagsetningu í desember 2020, en er sagt upp í júní 2020. Endurreikna verður samningstekjuupphæðina fyrir báða liði:

- **Atriði 1000:** Samningstekjurnar eru endurreiknaðar sem $1,567.67.
- **Liður S0021:** Samningstekjurnar eru endurreiknaðar sem $124.00.

Leiðréttingarbókarfærsla er búin til fyrir línuna sem er hætt. Dagbókarfærslunni fyrir línuna sem tilheyrir sama MEA-númeri (multiple element arrangement) er snúið við og ný dagbókarfærsla er búin til:

- **Atriði 1000:** Upprunalegri dagbókarfærslu $1,465.26 er snúið við. Leiðréttingarbókarfærsla fyrir $1,549.47 er búin til.
- **Liður S0021:** Upprunalegri dagbókarfærslu $274.74 er snúið við. Ný dagbókarfærsla fyrir $124.00 er búin til.

---
title: Tekju- og kostnaðarfrestanir í áskriftargreiðslum
description: Þessi grein útskýrir hverig á að setja upp tekju- og kostnaðarfrestanir í áskriftargreiðslum.
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
ms.openlocfilehash: 209afd08c0c7e3cbd63ed95613b1d1dec94856f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908097"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Tekju- og kostnaðarfrestanir í áskriftargreiðslum

Þessi grein útskýrir hverig á að setja upp og nota tekju- og kostnaðarfrestanir í áskriftargreiðslum. Frestunaráætlanir byggja alltaf á og eru háðar undirliggjandi upprunalegu skjali eða greiðsluáætlun. Þar sem þær eru búnar til á grundvelli sjálfgefinna gilda er ekki hægt að færa þær inn eða búa þær til sérstaklega.

Ferlið við að setja upp og nota frestun á tekjum og kostnaði á sér stað á mörgum síðum:

- Á síðunni **Færibreytur tekju- og kostnaðarfrestunar** er hægt að skilgreina kjörstillingar fyrirtækisins.
- Á síðunni **Sjálfgefnar frestanir** er hægt að setja upp sjálfgefna lykla og sniðmát sem eru notuð fyrir frestunaráætlanir.
- Á síðunum **Sniðmát frestunar** og **Frestunarsniðmát sem byggja á tilviki** er hægt að skilgreina sniðmátin sem notuð eru fyrir frestunaráætlanir.
- Á síðunni **Allar frestunaráætlanir** er hægt að skoða og breyta öllum frestunaráætlunum.

Hægt er að nota tekju- og útgjaldafrestanir með endurtekinni samningsgreiðslu.

## <a name="revenue-and-expense-deferral-parameters"></a>Færibreytur tekju- og kostnaðarfrestunar

Síðan **Færibreytur tekju- og kostnaðarfrestunar** inniheldur eftirfarandi reiti.

| Svæði | Lýsing |
|---|---| 
| Flipinn **Áætlun** | |
| Jafnt og á tímabili | <p>Tilgreindu hvort fjöldi daga í tímabili er notaður þegar upphæð á tímabil er reiknuð út fyrir frestunaráætlun:</p><ul><li>**Já** – Upphæð hvers tímabils er sú sama, óháð fjölda daga á tímabilinu. Hlutatímabilum (t.d. tímabil í upphafi eða lok frestunaráætlunar) verður skipt hlutfallslega.</li><li>**Nei** – Upphæðin er útreiknuð á grundvelli fjölda daga á hverju tímabili.</li></ul><p>Hægt er að hnekkja þessari stillingu á færslustigi.</p> |
| Valkostur frestaðs söluafsláttar | <p>Tilgreindu hvort aðskildar frestunaráætlanir séu búnar til fyrir afsláttar- og sölupöntunarupphæðir:</p><ul><li>**Aðskilin áætlun fyrir afslátt** – Afsláttarupphæðinni er haldið aðskildri frá tekjuupphæðinni.<p>Í þessu tilviki eru búnar til tvær frestunaráætlanir þegar sölupöntun er stofnuð og síðan bókuð. Afslátturinn og tekjuupphæðin verða lögð inn á mismunandi frestunarreikninga.</p></li><li>**Sameina afslátt við tekjur** – Afsláttarupphæðin er sameinuð við tekjuupphæðina. Ein frestunaráætlun er búin til og bæði afsláttarupphæðin og tekjuupphæðin eru bókaðar á sama frestunarlykilinn.<p>Í þessu tilviki er búin til ein frestunaráætlun þegar sölupöntun er stofnuð og síðan bókuð. Bæði afsláttarupphæðin og tekjuupphæðin eru bókaðar á sama frestunarlykilinn.</p></li></ul><p>**Athugaðu:** Til að nota afslátt á vörur sem nota eiginleika óreikningsfærðra tekna skal velja valkostinn **Sérstök áætlun fyrir afslátt**. Hægt er að nota afslætti á allar vörur burtséð frá því hvort eiginleikinn óreikningsfærðar tekjur er notaður. Ef valkosturinn **Sameina afslátt við tekjur** er valinn er ekki hægt að nota afslætti á vörur sem nota eiginleika óreikningsfærðra tekna.</p> |
| Frestunarvalkostur innkaupaafsláttar | <p>Veldu hvort sérstakar frestunaráætlanir eru búnar til fyrir afsláttar- og innkaupapöntunarupphæðir:</p><ul><li>**Sérstök áætlun fyrir afslátt** – Afsláttarupphæðinni er haldið aðskildri frá upphæð kostnaðar.<p>Í þessu tilviki eru búnar til tvær frestunaráætlanir þegar innkaupapöntun er stofnuð og síðan bókuð. Afsláttar- og kostnaðarupphæðir eru bókaðar á mismunandi frestunarlykla.</p></li><li>**Sameina afslátt við tekjur** – Afsláttarupphæðin er sameinuð við kostnaðarupphæðina. Ein frestunaráætlun er búin til og bæði afsláttarupphæðin og kostnaðarupphæðin eru bókaðar á sama frestunarlykilinn.<p>Í þessu tilviki er búin til ein frestunaráætlun þegar innkaupapöntun er stofnuð og síðan bókuð. Bæði afsláttarupphæðin og kostnaðarupphæðin eru bókaðar á sama frestunarlykilinn.</p></li></ul> |
| Sameina fyrri tímabil | <p>Tilgreindu hvort línur frestunaráætlunar fyrir fyrri tímabil séu sameinuð:</p><ul><li>**Já** – Ef upphafsdagur frestunar er á tímabili á undan færsludagsetninguna eru allar upphæðir á tímabilinu fyrir færsludagsetninguna sameinaðar í eina línu frestunaráætlunar.</li><li>**Nei** – Upphæðum frá öllum tímabilum er haldið aðskildum í frestunaráætlunarlínum.<p>Ef upphafsdagsetning frestunar er á sama tímabili og eða síðar en færsludagsetningin hefur þessi valkostur engin áhrif.</p></li></ul><p>Hægt er að uppfæra þessa stillingu á færslustigi.</p> |
| Sjálfgefin upphafsdagsetning frestunar | <p>Veljið regluna sem er notuð til að ákvarða upphafsdag frestunar:</p><ul><li>**Færsludagsetning** – Notaðu færsludagsetninguna sem upphafsdagsetningu.</li><li>**Upphaf yfirstandandi mánaðar** – Notaðu fyrsta dag yfirstandandi mánaðar sem upphafsdagsetningu. Ef færsludagsetningin er fyrsta dag hvers mánaðar er fyrsti dagur yfirstandandi mánaðar upphafsdagsetningin.</li><li>**Byrjun næsta mánaðar** – Notaðu fyrsta dag næsta mánaðar sem upphafsdagsetningu. Ef færsludagsetningin er þann fyrsta er færsludagsetningin notuð. Annars er fyrsti dagur næsta mánaðar notaður.</li><li>**Regla um 15** – Ef færsludagsetningin er á milli fyrsta og fimmtánda skal nota fyrsta yfirstandandi mánaðar sem upphafsdagsetningu. Ef færsludagsetningin er sextándi eða síðar skal nota fyrsta næsta mánaðar sem upphafsdagsetningu.</li></ul><p>Hægt er að breyta þessari stillingu á færslustigi.</p> |
| Aðferð skammtímafrestunar | <p>Veldu aðferð skammtímafrestunar: **Ekkert**, **Hlaupandi tímabil** eða **Fast ár**.</p><p>|
| Bókunaraðferð frestunar | <p>Veljið aðferð sem er notuð til að stofna frestunarfærslur:</p><ul><li>**Efnahagsreikningur** – Notaðu bókunaraðferð efnahagsreiknings til að stofna frestunarfærslur.</li><li>**Hagnaður og tap** – Notaðu bókunaraðferð hagnaðar og taps til að stofna frestunarfærslur. Þegar færslur eru bókaðar er hægt að fara yfir fylgiskjal reikningsins til að sjá aukafærslur sem jafna upphæðir upphaflegrar skráningar og mótlykils skráningar.</li></ul> |
| Bakfæra hagnað og tap í kreditfærslu | <p>**Athugið:** Þetta svæði er aðeins í boði þegar svæðið **Bókunaraðferð frestunar** er stillt á **Hagnaður og tap**.</p><p>Tilgreindu hvort upphæðir hagnaðar og taps séu bakfærðar þegar bakfærsla, uppsögn eða endurgreiðsla er notuð í greiðsluáætlun eða sölupöntun:</p><ul><li>**Já** – Bakfærðu upphæðir hagnaðar og taps og notaðu kreditleiðréttingarupphæð á frestunaráætlunina.<p>Ef bakfærslan gerist um miðbik greiðslutímabils eru upphæðunum skipt hlutfallslega niður.</p></li><li>**Nei** – Engin bakfærsla er stofnuð fyrir hagnað og tap þegar bakfærsla, uppsögn eða endurgreiðsla er notuð í greiðsluáætlun eða sölupöntun.</li></ul> |
| Flipinn **Viðurkenning** | |
| Bóka færslubækur sjálfvirkt | <p>Tilgreindu hvort færslur í færslubók sem eru stofnaðar af tekju- og kostnaðarfrestunum séu sjálfkrafa bókaðar:</p><ul><li>**Já** – Birta sjálfkrafa færslur í færslubók sem verða til vegna frestunar á tekjum og kostnaði.<p>**Ábending:** Með því að velja **Já** getur þú hjálpað til við að koma í veg fyrir ósamræmi í bókhaldi vegna handvirkra breytinga í fylgiskjölum.</p></li><li>**Nei** – Færslur færslubókar sem eru stofnaðar af tekju- og kostnaðarfrestunum eru ekki bókaðar sjálfkrafa. Notandi þarf að bóka færslur handvirkt.</li></ul> |
| Taka saman skráningarbók | <p>Tilgreindu hvort fylgiskjöl skráningar séu sjálfgefið sameinaðar:</p><ul><li>**Já** – Búðu til eitt fylgiskjal fyrir allar skráningarlínur sem eru með sömu dagsetninguna. Allar línur í fylgiskjali eru með sama lykilinn eru sameinaðar í eina línu.</li><li>**Nei** – Búðu til fylgiskjal fyrir hverja skráningarlínu.</li></ul><p>Hægt er að uppfæra þessa stillingu á síðunni **Úrvinnsla skráningar**.</p> |
| Sjálfgefið færslubókarnafn | Veldu heiti færslubókar fyrir færslubækur sem eru búnar til úr ferlum tekju- og kostnaðarfrestana, t.d. úrvinnslu skráningar. |
| Lýsing á færslubókarlínu skráningar | <p>Veldu lýsinguna sem birtist í línulýsingu færslubókarfylgiskjals:</p><ul><li>**Dagsetningar áætlunarlína** – Sýndu dagsetningar áætlunarlína í lýsingu færslubókarlínu.</li><li>**Upprunalegar færsluupplýsingar** – Sýndu upprunalegar færsluupplýsingar í lýsingu færslubókarlínu.<p>**Dæmi:** USMF-0001, CIV-00839, tekjur af hugbúnaði</p></li></ul> |
| Flipinn **Númeraraðir** | Notaðu þennan flipa til að stilla sjálfgefin gildi fyrir númeraröð leigusamnings. Leiðsögn fyrir myndun númeraraðar er notuð til að mynda og úthluta númeraraðir sjálfkrafa. Þú þarft ekki að breyta númeraröðinni nema þú viljir gera handvirkar breytingar á númeraröðinni. |
| Áætlunarnúmer | Númeraröðin sem er notuð fyrir frestunaráætlanir. |

## <a name="deferral-templates"></a>Sniðmát frestunar

Notaðu síðuna **Sniðmát frestunar** til að skilgreina línuleg sniðmát sem eru notuð fyrir frestunaráætlanir.

Hér eru nokkrir kostir þess að nota sniðmát:

* Lengd frestunarinnar er reiknuð sjálfkrafa.
* Þú leyfir frestunaráætlanir sem eru með tímabil þar sem skráningu er sleppt.
* Hægt er að gera frestanir sjálfvirkar með því að úthluta sniðmátinu á afurð, afurðahóp, afurðaflokk, viðskiptavini eða viðskiptavinaflokka. Úthlutun sniðmáts er gerð af síðunni **Sjálfgefnar frestanir**.

Nokkar tíðnir tímabila eru í boði fyrir sniðmát: dagleg, mánaðarleg eða reikningstímabil.

Sniðmátslínurnar samanstanda af tegund (**Skráð** eða **Sleppt**) og lengd tímabils. Línum sem er sleppt eru með 0 (núll) upphæð í línum frestunaráætlunar. Þessi hegðun getur komið sér vel ef ekki á að skrá tekjur á öllum tímabilum.

### <a name="create-a-deferral-template"></a>Stofna frestunarsniðmát

Fylgið eftirfarandi skrefum til að stofna frestunarsniðmát.

1. Á síðunni **Frestunarsniðmát** skal velja **Nýtt**.
2. Á svæðinu **Sniðmát** skal slá inn heiti.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Á svæðinu **Tímabilstíðni** skal velja tímabilstíðni.
5. Veldu **Bæta við** til að bæta línu efst á listann yfir línur eða veldu **Bæta við** til að bæta línu neðst á listann.
6. Á svæðinu **Gerð** skal velja gerð tímabils.
7. Í reitnum **Lengd tímabils** skal tilgreina lengd tímabilsins.
8. Endurtakið skref 5 til 7 fyrir hverja viðbótarlínu sem þörf er á.
9. Veldu **Vista**.

## <a name="deferral-defaults"></a>Sjálfgefnar frestanir

Notaðu síðuna **Sjálfgefnar frestanir** til að setja upp sjálfgefna frestunarlykla fyrir vörur og úthlutaðu sjálfgefnum sniðmátum á frestunarvörur. Einnig er hægt að setja upp frestunarlykla fyrir gjöld og úthluta sniðmátum á frestunargjöld.

**Fresta eftir vöru**

Fyrir færslur sem eru með vöru (t.d. sölupantanir) er hægt að úthluta lyklum og sniðmátum á tilteknar vörur og viðskiptavini. Þessar stillingar verða notaðar sem sjálfgefin gildi þegar færslu er frestað. Til að gera færslu sjálfgefið frestanlega þarf að setja upp vörurnar á síðunni **Frestanlegar vörur**.

**Fresta eftir reikningi**

Fyrir færslur sem eru ekki með vörur (t.d. almennar færslubækur) er hægt að tilgreina frestunarlykla. Þegar þessir reikningar eru notaðir á færslulínu er færslan sjálfkrafa merkt sem frestuð. Samsvarandi sniðmáti og skráningarlykli verður úthlutað á færslulínuna.

**Allar færslugerðir (til dæmis í flipum sölupöntunar, innkaupa og almennrar færslubókar)**

Lyklarnir á síðunni eru aðallyklarnir sem eru ekki með fjárhagsvíddir. Fjárhagsvíddir skráningarlykilsins eru frá viðskiptavini eða vöru, byggt á fyrirtækinu.

Hver sniðmátslína verður annaðhvort að vera með línulegt sniðmát eða sniðmát sem byggir á tilviki. Það getur ekki haft hvort tveggja.

### <a name="for-sales-orders"></a>Fyrir sölupantanir

Til að tilgreina sjálfgefin frestunargildi fyrir sölupantanir skal fylgja eftirfarandi skrefum.

1. Í flipanum **Sölupöntun** skal velja tegund frestunar.
2. Smellið á **Bæta við** til að bæta við nýrri línu.
3. Á svæðinu **Vörukóði** skal velja vörukóðann. Vörukóðinn ákvarðar hvernig sjálfgefnu frestunargildin eru notuð.
4. Tilgreinið hvernig vörukóðinn er notaður:

    * Ef reiturinn **Vörukóði** er stilltur á **Tafla** eða **Hópur** skal velja vöruvensl í reitnum **Vöruvensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Flokkur** skal velja flokkavensl í **Flokkavensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Allt** eiga sjálfgefin gildi við allar viðeigandi færslur.

5. Tilgreinið hvernig lykilkóðinn er notaður:

    * Ef reiturinn **Kóði lykils** er stilltur á **Tafla** eða **Hópur** skal velja lyklavenslin í reitnum **Lyklavensl**.
    * Ef svæðið **Kóði lykils** er stilltur á **Allt** gildir lykillinn um allar færslur.

6. Á svæðinu **Aðallykill** skal velja aðallykil fyrir frestun.
7. Ef reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** skal velja upphaflegan tekjulykil í reitnum **Upphaflegur tekjulykill** og mótlykil tekna í reitnum **Mótlykill tekna**.
8. Ef reiturinn **Aðferð skammtímafrestunar** er stilltur á **Hlaupandi tímabil** eða **Fast ár** skal velja skammtíma frestunarlykil í reitnum **Frestunarlykill til skammtíma**.
9. Hægt er að velja **Bæta við** til að bæta við nýrri línu fyrir sniðmát.
10. Á svæðinu **Vörukóði** skal velja vörukóðann.
11. Tilgreinið hvernig vörukóðinn er notaður:

    * Ef reiturinn **Vörukóði** er stilltur á **Tafla** eða **Hópur** skal velja vöruvensl í reitnum **Vöruvensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Flokkur** skal velja flokkavensl í reitnum **Flokkavensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Allt** eiga sjálfgefin gildi við allar viðeigandi færslur.

12. Tilgreinið hvernig lykilkóðinn er notaður:

    * Ef reiturinn **Kóði lykils** er stilltur á **Tafla** eða **Hópur** skal velja lyklavenslin í reitnum **Lyklavensl**.
    * Ef svæðið **Lykilkóði** er stilltur á **Allt** nær lykillinn til allra viðeigandi færslna.
    * Veldu línulegt sniðmát í reitnum **Línulegt sniðmát** eða sniðmát sem byggir á tilviki í reitnum **Sniðmát sem byggir á tilviki**.

13. Veldu **Vista**.

### <a name="for-purchase-orders"></a>Fyrir innkaupapantanir

Til að tilgreina sjálfgefin frestunargildi fyrir innkaupapantanir skal fylgja eftirfarandi skrefum.

1. Á flipanum **Innkaup** skal velja tegund frestunar.
2. Smellið á **Bæta við** til að bæta við nýrri línu.
3. Á svæðinu **Vörukóði** skal velja vörukóðann.
4. Tilgreinið hvernig vörukóðinn er notaður:

    * Ef reiturinn **Vörukóði** er stilltur á **Tafla** eða **Hópur** skal velja vöruvensl í reitnum **Vöruvensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Flokkur** skal velja flokkavensl í reitnum **Flokkavensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Allt** eiga sjálfgefin gildi við allar viðeigandi færslur.

5. Tilgreinið hvernig lykilkóðinn er notaður:

    * Ef reiturinn **Kóði lykils** er stilltur á **Tafla** eða **Hópur** skal velja lyklavenslin í reitnum **Lyklavensl**.
    * Ef svæðið **Lykilkóði** er stilltur á **Allt** nær lykillinn til allra viðeigandi færslna.

6. Á svæðinu **Aðallykill** skal velja aðallykil fyrir frestun.
7. Ef reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** skal velja upphaflegan tekjulykil í reitnum **Upphaflegur tekjulykill** og mótlykil tekna í reitnum **Mótlykill tekna**.
8. Ef reiturinn **Aðferð skammtímafrestunar** er stilltur á **Hlaupandi tímabil** eða **Fast ár** skal velja skammtíma frestunarlykil í reitnum **Frestunarlykill til skammtíma**.
9. Veljið **Bæta við** til að bæta við nýrri línu fyrir sniðmát. 
10. Á svæðinu **Vörukóði** skal velja vörukóðann.
11. Tilgreinið hvernig vörukóðinn er notaður:

    * Ef reiturinn **Vörukóði** er stilltur á **Tafla** eða **Hópur** skal velja vöruvensl í reitnum **Vöruvensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Flokkur** skal velja flokkavensl í reitnum **Flokkavensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Allt** eiga sjálfgefin gildi við allar viðeigandi færslur.

12. Tilgreinið hvernig lykilkóðinn er notaður:

    * Ef reiturinn **Lykilkóði** er stilltur á **Tafla** eða **Hópur** skal velja lyklavensl í **Lyklavensl**.
    * Ef svæðið **Lykilkóði** er stilltur á **Allt** nær lykillinn til allra viðeigandi færslna.
    * Veldu línulegt sniðmát í reitnum **Línulegt sniðmát** eða sniðmát sem byggir á tilviki í reitnum **Sniðmát sem byggir á tilviki**.

13. Veldu **Vista**.

### <a name="for-general-journals"></a>Fyrir almennar færslubækur

Til að skilgreina sjálfgefin frestunargildi fyrir almennra dagbókarfærslna skal fylgja þessum skrefum.

1. Veljið flipann **Almenn færslubók**.
2. Veljið **Bæta við** til að bæta við nýrri línu fyrir frestun.
3. Ef reiturinn **Aðferð skammtímafrestunar** er stilltur á **Hlaupandi tímabil** eða **Fast ár** skal velja skammtíma frestunarlykil í reitnum **Frestunarlykill til skammtíma**.
4. Í reitnum **Frestunarlykill** skal velja frestunarlykil.
5. Í reitnum **Skráningarlykill** skal velja skráningarlykilinn.
6. Ef reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** skal velja upphaflegan tekjulykil í reitnum **Upphaflegur tekjulykill** og mótlykil tekna í reitnum **Mótlykill tekna**.
7. Veldu línulegt sniðmát í reitnum **Línulegt sniðmát** eða sniðmát sem byggir á tilviki í reitnum **Sniðmát sem byggir á tilviki**.
8. Veldu **Vista**.

### <a name="for-free-text-invoices"></a>Allir textareikningar með frjálsum texta

Til að skilgreina sjálfgefin frestunargildi fyrir reikninga með frjálsum texta skal fylgja þessum skrefum.

1. Veljið flipann **Reikningur með frjálsum texta**.
2. Veljið **Bæta við** til að bæta við nýrri línu fyrir frestun.
3. Tilgreinið hvernig lykilkóðinn er notaður:

    * Ef reiturinn **Kóði lykils** er stilltur á **Tafla** eða **Hópur** skal velja lyklavenslin í reitnum **Lyklavensl**.
    * Ef svæðið **Lykilkóði** er stilltur á **Allt** nær lykilkóðinn til allra viðeigandi færslna.

4. Í reitnum **Frestunarlykill** skal velja frestunarlykil.
5. Ef reiturinn **Aðferð skammtímafrestunar** er stilltur á **Hlaupandi tímabil** eða **Fast ár** skal velja skammtíma frestunarlykil í reitnum **Frestunarlykill til skammtíma**.
6. Í reitnum **Skráningarlykill** skal velja skráningarlykilinn.
7. Ef reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** skal velja upphaflegan tekjulykil í reitnum **Upphaflegur tekjulykill** og mótlykil tekna í reitnum **Mótlykill tekna**.
8. Veldu línulegt sniðmát í reitnum **Línulegt sniðmát** eða sniðmát sem byggir á tilviki í reitnum **Sniðmát sem byggir á tilviki**.
9. Veldu **Vista**.

### <a name="for-invoice-journals"></a>Fyrir reikningabækur

Til að skilgreina sjálfgefin frestunargildi reikningsdagbókarfærslna skal fylgja þessum skrefum.

1. Veljið flipann **Reikningabók**.
2. Veljið **Bæta við** til að bæta við nýrri línu fyrir frestun.
3. Tilgreinið hvernig lykilkóðinn er notaður:

    * Ef reiturinn **Kóði lykils** er stilltur á **Tafla** eða **Hópur** skal velja lyklavenslin í reitnum **Lyklavensl**.
    * Ef svæðið **Lykilkóði** er stilltur á **Allt** nær lykilkóðinn til allra viðeigandi færslna.

4. Í reitnum **Frestunarlykill** skal velja frestunarlykil.
5. Ef reiturinn **Aðferð skammtímafrestunar** er stilltur á **Hlaupandi tímabil** eða **Fast ár** skal velja skammtíma frestunarlykil í reitnum **Frestunarlykill til skammtíma**.
6. Í reitnum **Skráningarlykill** skal velja skráningarlykilinn.
7. Ef reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** skal velja upphaflegan tekjulykil í reitnum **Upphaflegur tekjulykill** og mótlykil tekna í reitnum **Mótlykill tekna**.
8. Veldu línulegt sniðmát í reitnum **Línulegt sniðmát** eða sniðmát sem byggir á tilviki í reitnum **Sniðmát sem byggir á tilviki**.
9. Veldu **Vista**.

### <a name="items-that-are-deferred-by-default"></a>Vörur sem er sjálfgefið frestað

Notaðu síðuna **Vörum frestað sjálfgefið** til að skilgreina hvaða vörum er frestað sjálfgefið. Hægt er að setja upp færslutegundir sem vörurnar verða frestaðar fyrir. Hægt er að tilgreina hvort einni vöru sé frestað eða heilum vöruhópi eða vöruflokki.

Þegar vörur eru settar upp sem frestaðar skal velja sjálfgefna lykla og sniðmát á síðunni **Sjálfgefnar frestanir**. Ef lyklar og sniðmát eru ekki valin verður færslulínum þar sem þessar vörur eru færðar inn ekki frestað.

Fyrir vörur sem er frestað samkvæmt sölu- eða innkaupaflokki sem þær tengjast byggja stillingar frestunar á flokknum. Ef flokkurinn er hins vegar ekki valinn í reitnum **Flokkavensl** er frestunarstillingar flokksins sem eru hærra í röðinni notaðar. Til dæmis er hægt að bæta við söluflokknum **Heimamyndbönd** en ekki söluflokknum **Sjónvarp**. Þegar frestunarvöru er bætt við sem tengist flokknum **Sjónvarp** eru frestunarstillingar **Heimamyndbands** notaðar fyrir vöruna.

### <a name="set-up-deferred-items"></a>Setja upp frestaðar vörur

Til að setja upp vörur sem frestað er sjálfgefið skal fylgja þessum skrefum.

1. Á síðunni **Vörum frestað sjálfgefið** skal velja flipann sem þú vilt: **Sölupöntun** eða **Innkaup**.
2. Smellið á **Bæta við** til að bæta við nýrri línu.
3. Á svæðinu **Vörukóði** skal velja vörukóðann.
4. Tilgreinið hvernig vörukóðinn er notaður:

    * Ef reiturinn **Vörukóði** er stilltur á **Flokkur** eða **Tafla** skal velja vöruvensl í reitnum **Vöruvensl**.
    * Ef reiturinn **Vörukóði** er stilltur á **Flokkur** skal velja flokkavensl í reitnum **Flokkavensl**.

5. Endurtakið skref 2 til 4 fyrir hverja viðbótarlínu sem þörf er á.
6. Veldu **Vista**.

## <a name="deferred-charges"></a>Frestuð gjöld

Notaðu síðuna **Frestunargjöld** til að skilgreina hvaða gjöldum er sjálfgefið frestað.

> [!NOTE]
> * Sem stendur eru frestanleg gjöld aðeins í boði fyrir sölupantanir.
> * Aðeins er hægt að fresta gjöldum á línustigi. Til að fresta gjaldi á stigi sölupöntunarhauss er hægt að setja upp gjöld sem frestaða vöru í aðskildri línu í sölupöntuninni.
> * Til að fresta gjaldi fyrir reikning með frjálsum texta þarftu að færa inn gjaldið sem aðskilda frestaða reikningslínu.
> * Þessi aðgerð er ekki í boði fyrir studd gjöld og tekjuskiptingu.

### <a name="set-up-deferred-charges"></a>Setja upp frestuð gjöld

Fylgið þessum skrefum til að setja upp frestaðar greiðslur.

1. Á síðunni **Frestunargjöld** skal velja **Bæta við** til að bæta við nýrri línu.
2. Í reitnum **Gjaldakóði** skal velja gjaldakóðann.
3. Í reitnum **Tengsl gjalds** skal velja tengsl gjaldsins.
4. Endurtakið skref 1 til 3 fyrir hverja viðbótarlínu sem þörf er á.
5. Veldu **Vista**.

## <a name="event-based-deferral-templates"></a>Frestunarsniðmát byggð á tilviki

Notaðu síðuna **Frestunarsniðmát byggð á tilviki** til að skilgreina frestunarsniðmát sem byggja á tilviki sem hægt er að nota í frestunarfærslum og úthluta á síðunni **Sjálfgefnar frestanir**.

### <a name="create-an-event-based-template"></a>Stofna sniðmát sem byggir á tilviki

Fylgið þessum skrefum til að stofna frestunarsniðmát byggt á tilviki.

1. Á síðunni **Frestunarsniðmát byggð á tilviki** skal velja **Nýtt**.
2. Færið inn einkvæmt heiti fyrir sniðmátið á svæðinu **Sniðmát**.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **Úthlutunargerð** skal velja úthlutunargerðina:

    * **Breytileg upphæð** – Úthluta tiltekinni upphæð fyrir hverja línu sem er færð inn.
    * **Jöfn upphæð** – Úthlutaðu sömu upphæðinni á hverja línu sem er færð inn. 
    * **Prósenta** – Úthlutaðu upphæð sem byggir á prósentugildi sem er fært inn fyrir hverja línu.
    * **Prósentum lokið** – Úthlutaðu samanlögðu gildi fyrir lokið fyrir hverja línu sem er færð inn.
    * **Breytilegt magn** – Úthluta tilteknu magni fyrir hverja línu sem er slegin inn.

5. Stilltu valkostinn **Búa til aðskilin tilvik á hverja einingu** á **Já** ef þú vilt að hverri tilvikslínu sé skipt jafnt eftir fjölda eininga í reikningsfærslunni. Stilltu þetta á **Nei** ef ekki á að skipta tilvikslínunum.
6. Í reitnum **Lykill gildistíma** skal velja gildistímalykilinn.
7. Veldu **Bæta við** til að bæta línu efst á listann yfir línur eða veldu **Bæta við** til að bæta línu neðst á listann.
8. Á svæðinu **Lýsing** skal slá inn lýsingu tilviksins.
9. Ef reiturinn **Úthlutunargerð** er stilltur á **Prósenta** skal tilgreina úthlutunarprósentuna í reitnum **Úthlutunarprósenta**. Prósenta verður að vera á milli 0 (núll) og 100. Ef reiturinn **Úthlutunarprósenta** er skilinn eftir auður er álitið að prósentan sé 0. Summa allra prósenta er sýnd í reitnum **Heildarprósenta** neðst á síðunni og verður að vera samtals 100.
10. Í reitnum **Mánuðir eftir af gildistíma** skal tilgreina fjölda mánaða sem tilvikið er í gildi. Lokadagsetning gildistíma í frestunarfærslunni er sjálfkrafa slegin inn út frá þessu gildi.
11. Veldu gátreitinn **Skrá við bókun** til að sjálfkrafa skrá tekjur þegar færslan er bókuð. Ef gátreiturinn er hreinsaður þarf að skrá tekjurnar handvirkt.
12. Í reitnum **Skráningarlykill** skal velja skráningarlykilinn fyrir tilvikið ef tilvikið notar annan lykil en alla frestunaráætlunina. Þessi reitur er notaður ásamt gátreitnum **Skrá þegar bókað**.
13. Endurtakið skref 7 til 12 fyrir hverja viðbótarlínu sem þörf er á.
14. Veldu **Vista**.

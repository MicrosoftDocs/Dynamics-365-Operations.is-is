---
title: Frestun tekna og gjalda í áskriftarreikningi
description: Þessi grein útskýrir hvernig á að setja upp frestun tekna og gjalda í áskriftarreikningi.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908097"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Frestun tekna og gjalda í áskriftarreikningi

Þessi grein útskýrir hvernig á að setja upp og nota frestun tekna og kostnaðar í innheimtu áskriftar. Frestunaráætlanir eru alltaf byggðar á og eru háðar undirliggjandi upprunaskjali eða innheimtuáætlun. Vegna þess að þau eru búin til á grundvelli sjálfgefna er ekki hægt að slá þau inn eða búa þau til sérstaklega.

Ferlið við að setja upp og nota frestun tekna og kostnaðar á sér stað á mörgum síðum:

- Á **Frestun tekna og gjalda** síðu geturðu skilgreint kjörstillingar fyrirtækisins.
- Á **Frestun vanskil** síðu geturðu sett upp sjálfgefna reikninga og sniðmát sem eru notuð fyrir frestunaráætlanir.
- Á **Frestun sniðmát** og **Frestunarsniðmát sem byggir á viðburðum** síðum, getur þú skilgreint sniðmát sem eru notuð fyrir frestunaráætlanir.
- Á **Allar frestunaráætlanir** síðu geturðu skoðað og breytt hvaða frestunaráætlun sem er.

Hægt er að nota frestun tekna og gjalda ásamt endurteknum samningsreikningum.

## <a name="revenue-and-expense-deferral-parameters"></a>Færibreytur tekju- og kostnaðarfrestunar

The **Frestun tekna og gjalda** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|---|---| 
| **Dagskrá** flipa | |
| Jafnt á tímabili | <p>Tilgreindu hvort fjöldi daga á tímabili sé notaður þegar upphæð á tímabili er reiknuð út fyrir frestunaráætlun:</p><ul><li>**Já** – Upphæðin fyrir hvert tímabil er sú sama, óháð fjölda daga á tímabilinu. Hlutatímabil (svo sem tímabil í upphafi eða lok frestunaráætlunar) verða hlutfallslega.</li><li>**Nei** – Upphæðin er reiknuð út frá fjölda daga á hverju tímabili.</li></ul><p>Þú getur hnekið þessari stillingu á færslustigi.</p> |
| Valkostur frestaðs söluafsláttar | <p>Tilgreindu hvort aðskildar frestunaráætlanir séu búnar til fyrir afsláttinn og sölupöntunarupphæðirnar:</p><ul><li>**Sér áætlun fyrir afslátt** – Afsláttarupphæðinni er haldið aðskildum frá tekjuupphæðinni.<p>Í þessu tilviki eru tvær frestunaráætlanir stofnaðar þegar sölupöntun er stofnuð og síðan bókuð. Afsláttar- og tekjuupphæðir verða færðar á mismunandi frestunarreikninga.</p></li><li>**Sameina afslátt við tekjur** – Afsláttarupphæðin er sameinuð tekjuupphæðinni. Ein frestunaráætlun er stofnuð og bæði afsláttarupphæð og tekjuupphæð eru færð á sama frestunarreikning.<p>Í þessu tilviki er ein frestunaráætlun stofnuð þegar sölupöntun er stofnuð og síðan bókuð. Bæði afsláttarupphæð og tekjuupphæð eru færð á sama frestunarreikning.</p></li></ul><p>**Athugið:** Til að beita afslætti á vörur sem nota óinnheimta tekjur eiginleiki, veldu **Sérstök dagskrá fyrir afslátt** valmöguleika. Þá er hægt að beita afslætti á allar vörur, óháð því hvort óinnheimtar tekjur eru notaðar. Ef **Sameina afslátt við tekjur** valkostur er valinn, ekki er hægt að nota afslætti á vörur sem nota óinnheimt tekjur.</p> |
| Frestunarvalkostur innkaupaafsláttar | <p>Veldu hvort aðskilin frestunaráætlanir séu búnar til fyrir upphæðir afsláttar og innkaupapöntunar:</p><ul><li>**Sér áætlun fyrir afslátt** – Afsláttarupphæðinni er haldið aðskildum frá kostnaðarupphæðinni.<p>Í þessu tilviki eru tvær frestunaráætlanir stofnaðar þegar innkaupapöntun er stofnuð og síðan bókuð. Afsláttar- og kostnaðarupphæðir eru bókaðar á mismunandi frestunarreikninga.</p></li><li>**Sameina afslátt við tekjur** – Afsláttarupphæðin er sameinuð kostnaðarupphæðinni. Ein frestunaráætlun er stofnuð og bæði afsláttarupphæð og kostnaðarupphæð eru færð á sama frestunarreikning.<p>Í þessu tilviki er ein frestunaráætlun stofnuð þegar innkaupapöntun er stofnuð og síðan bókuð. Bæði afsláttarupphæð og kostnaðarupphæð eru færð á sama frestunarreikning.</p></li></ul> |
| Sameina fyrri tímabil | <p>Tilgreindu hvort frestunaráætlunarlínur fyrir fyrri tímabil séu sameinaðar:</p><ul><li>**Já** – Ef upphafsdagur frestunarinnar er á tímabili fyrir færsludagsetningu eru allar upphæðir fram yfir tímabilið færsludagsins sameinaðar á eina frestunaráætlunarlínu.</li><li>**Nei** – Upphæðum frá öllum tímabilum er haldið á aðskildum frestunaráætlunarlínum.<p>Ef upphafsdagur frestunarinnar er á sama tímabili og eða seinna tímabil en viðskiptadagsetningin hefur þessi valkostur engin áhrif.</p></li></ul><p>Þessa stillingu er hægt að uppfæra á færslustigi.</p> |
| Sjálfgefin upphafsdagsetning frestunar | <p>Veldu regluna sem er notuð til að ákvarða upphafsdag frestunaráætlunar:</p><ul><li>**Dagsetning viðskipta** – Notaðu viðskiptadagsetninguna sem upphafsdagsetningu.</li><li>**Upphaf yfirstandandi mánaðar** – Notaðu þann fyrsta í núverandi mánuði sem upphafsdagsetningu. Ef viðskiptadagsetningin er sá fyrsti hvers mánaðar er sá fyrsti í núverandi mánuði upphafsdagsetningin.</li><li>**Upphaf næsta mánaðar** – Notaðu fyrsta næsta mánaðar sem upphafsdag. Ef viðskiptadagsetningin er á þeim fyrsta er viðskiptadagsetningin notuð. Annars er fyrsti næsta mánaðar notaður.</li><li>**Regla 15** – Ef viðskiptadagsetning er á milli þess fyrsta og fimmtánda, notaðu þann fyrsta í núverandi mánuði sem upphafsdagsetningu. Ef viðskiptadagsetningin er sextándi eða síðar, skal nota fyrsta næsta mánaðar sem upphafsdag.</li></ul><p>Þú getur uppfært þessa stillingu á færslustigi.</p> |
| Aðferð skammtímafrestunar | <p>Veldu skammtíma frestun aðferð: **Enginn**, **·**, eða **Fast ártal**.</p><p>|
| Bókunaraðferð frestunar | <p>Veldu aðferðina sem er notuð til að stofna frestunarfærslur:</p><ul><li>**Efnahagsreikningur** – Notaðu efnahagsreikningsbókunaraðferðina til að stofna frestunarfærslur.</li><li>**Hagnaður og tap** – Notaðu hagnaðarbókunaraðferðina til að stofna frestunarfærslur. Þegar færslur eru bókaðar er hægt að skoða fylgiskjal reikningsins til að sjá aukafærslurnar sem jafna upphafsfærslu- og færslujöfnunarupphæðir.</li></ul> |
| Bakfæra hagnað og tap í kreditfærslu | <p>**Athugið:** Þessi reitur er aðeins tiltækur þegar **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap**.</p><p>Tilgreindu hvort hagnaðar- og tapupphæðum sé bakfært þegar bakfærsla, uppsögn eða endurgreiðsla er beitt á innheimtuáætlun eða sölupöntun:</p><ul><li>**Já** – Bakfærðu hagnaðar- og tapupphæðir og notaðu lánsfjárleiðréttingarupphæð á frestunaráætlunina.<p>Ef bakfærsla á sér stað þegar reikningstímabilið er hálfnað, eru upphæðirnar hlutfallslegar.</p></li><li>**Nei** – Engin bakfærsla er stofnuð fyrir hagnað og tap þegar bakfærsla, uppsögn eða endurgreiðsla er notuð á reikningsáætlun eða sölupöntun.</li></ul> |
| **Viðurkenning** flipa | |
| Bóka færslubækur sjálfvirkt | <p>Tilgreindu hvort færslubókarfærslur sem eru búnar til með frestun tekna og gjalda séu sjálfkrafa bókaðar:</p><ul><li>**Já** – Bókaðu sjálfkrafa færslubókarfærslur sem eru búnar til með frestun tekna og gjalda.<p>**Ábending:** Með því að velja **Já**, getur þú hjálpað til við að koma í veg fyrir ósamræmi í bókhaldi sem stafar af handvirkum breytingum á fylgiskjölum.</p></li><li>**Nei** – Færslubókarfærslur sem eru búnar til með frestun tekna og kostnaðar eru ekki sjálfkrafa bókaðar. Þú verður að bóka allar dagbækur handvirkt.</li></ul> |
| Taka saman skráningarbók | <p>Tilgreindu hvort viðurkenningarskírteini séu sjálfgefið sameinuð:</p><ul><li>**Já** – Búðu til eina skírteini fyrir allar viðurkenningarlínur sem hafa sömu dagsetningu. Allar línur í fylgiskjali sem hafa sama reikning eru sameinaðar á eina línu.</li><li>**Nei** – Búðu til skírteini fyrir hverja viðurkenningarlínu.</li></ul><p>Þú getur uppfært þessa stillingu á **Viðurkenningarvinnsla** síðu.</p> |
| Sjálfgefið færslubókarnafn | Veljið færslubókarheiti fyrir færslubækur sem eru búnar til úr frestun tekna og gjalda, eins og viðurkenningarvinnslu. |
| Lýsing á færslubókarlínu skráningar | <p>Veldu lýsinguna sem birtist í línulýsingu færslubókar fylgiskjals:</p><ul><li>**Skipuleggðu línudagsetningar** – Sýna áætlunarlínudagsetningar í færslubókarlínulýsingunni.</li><li>**Upplýsingar um upprunaviðskipti** – Sýna upprunafærsluupplýsingarnar í færslubókarlínulýsingunni.<p>**Dæmi:** USMF-0001, CIV-00839, hugbúnaðartekjur</p></li></ul> |
| **Númeraraðir** flipa | Notaðu þennan flipa til að stilla sjálfgefin gildi fyrir leigunúmeraraðir. Tölurunarhjálparforritið er notað til að búa til og úthluta númeraröðum sjálfkrafa. Þú þarft ekki að breyta númeraröðinni nema þú viljir gera handvirkar breytingar á mynduðu númeraröðunum. |
| Áætlunarnúmer | Númerið sem er röð notuð fyrir frestunaráætlanir. |

## <a name="deferral-templates"></a>Sniðmát frestunar

Nota **Frestun sniðmát** síðu til að skilgreina beinlínusniðmát sem eru notuð fyrir frestunaráætlanir.

Hér eru nokkrir kostir þess að nota sniðmát:

* Lengd frestunarinnar reiknast sjálfkrafa.
* Þú gerir ráð fyrir frestun áætlana sem hafa tímabil þar sem viðurkenning er sleppt.
* Hægt er að gera frestun sjálfvirkan með því að úthluta sniðmátinu á vöru, vöruflokk, vöruflokk, viðskiptavini eða viðskiptavinahóp. Sniðmátaúthlutun er unnin frá **Frestun vanskil** síðu.

Nokkrar tímabilstíðni eru fáanlegar fyrir sniðmát: daglega, mánaðarlega eða fjárhagstímabil.

Sniðmátslínurnar samanstanda af gerð (**Viðurkennd** eða **Sleppt**) og lengd tímabilsins. Skiptar línur hafa upphæðina 0 (núll) á frestunaráætlunarlínunum. Þessi hegðun getur verið gagnleg ef þú vilt ekki færa tekjur á öllum tímabilum.

### <a name="create-a-deferral-template"></a>Búðu til frestunarsniðmát

Til að búa til frestunarsniðmát skaltu fylgja þessum skrefum.

1. Á **Frestun sniðmát** síðu, veldu **Nýtt**.
2. Í **Sniðmát** reit, sláðu inn nafn.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í **Tímabilstíðni** reit, veldu tímabilstíðni.
5. Veldu **Bæta við** til að bæta línu efst á lista yfir línur, eða veldu **Bæta við** til að bæta línu neðst á listann.
6. Í **Tegund** reit, veldu tegund tímabils.
7. Í **Lengd tímabils** reit, tilgreinið lengd tímabilsins.
8. Endurtaktu skref 5 til 7 fyrir hverja viðbótarlínu sem þú þarft.
9. Veldu **Vista**.

## <a name="deferral-defaults"></a>Sjálfgefnar frestanir

Nota **Frestun vanskil** síðu til að setja upp sjálfgefna frestunarreikninga fyrir hluti og til að úthluta sjálfgefnum sniðmátum til frestanlegra hluta. Þú getur líka sett upp frestunarreikninga fyrir gjöld og úthlutað sniðmátum til frestunargjaldanna.

**Fresta eftir lið**

Fyrir færslur sem hafa vöru (til dæmis sölupantanir) er hægt að úthluta reikningum og sniðmátum til ákveðinna vara og viðskiptavina. Þessar stillingar verða notaðar sem sjálfgefin gildi þegar færslu er frestað. Til að gera viðskiptunum frestað sjálfgefið verður þú að setja upp hlutina á **Frestabærir hlutir** síðu.

**Fresta eftir reikningi**

Fyrir færslur sem hafa ekki vörur (til dæmis almennar færslubækur) er hægt að tilgreina frestunarreikninga. Þegar þessir reikningar eru notaðir á færslulínu er færslan sjálfkrafa merkt sem frestað. Samsvarandi sniðmát og viðurkenningarreikningi verður úthlutað á færslulínuna.

**Allar færslugerðir (til dæmis á flipunum Sölupöntun, Innkaup og Almenn færslubók)**

Reikningarnir á síðunni eru aðalreikningarnir sem hafa ekki fjárhagsvíddir. Fjárhagsvíddir viðurkenningarreikningsins eru frá viðskiptavininum eða vörunni, byggt á fyrirtækinu þínu.

Hver sniðmátslína verður að hafa annað hvort beinlínusniðmát eða sniðmát sem byggir á atburðum. Það getur ekki haft bæði.

### <a name="for-sales-orders"></a>Fyrir sölupantanir

Til að tilgreina sjálfgefin frestunargildi fyrir sölupantanir skaltu fylgja þessum skrefum.

1. Á **Sölupöntun** flipanum, veldu frestunartegundina.
2. Smellið á **Bæta við** til að bæta við nýrri línu.
3. Í **Vörukóði** reit, veldu vörukóðann. Vörukóðinn ákvarðar hvernig sjálfgefna frestuninni er beitt.
4. Tilgreindu hvernig vörukóði er notaður:

    * Ef **Vörukóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu hluttengsl í **Atriðatengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Flokkur**, veldu flokkstengsl í **Flokkstengsl**.
    * Ef **Vörukóði** reiturinn er stilltur á **Allt**, sjálfgefna gildin eiga við um allar viðeigandi færslur.

5. Tilgreindu hvernig reikningskóðinn er notaður:

    * Ef **Reikningskóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu reikningstengslin í **Reikningstengsl** sviði.
    * Ef **Reikningskóði** reiturinn er stilltur á **Allt**, reikningurinn á við um allar færslur.

6. Í **Aðalreikningur** reit, veldu aðalreikning fyrir frestunina.
7. Ef **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap**, veldu upphaflega tekjureikninginn í **Stofntekjureikningur** reit og tekjujöfnunarreikning í **Tekjujöfnunarreikningur** sviði.
8. Ef **Skammtíma frestun aðferð** reiturinn er stilltur á **Rúllutímabil** eða **Fast ártal**, veldu skammtímafrestunarreikninginn í **Skammtímafrestunarreikningur** sviði.
9. Fyrir sniðmát geturðu valið **Bæta við** til að bæta við línu.
10. Í **Vörukóði** reit, veldu vörukóðann.
11. Tilgreindu hvernig vörukóði er notaður:

    * Ef **Vörukóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu hluttengsl í **Atriðatengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Flokkur**, veldu flokkstengsl í **Flokkstengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Allt**, sjálfgefna gildin eiga við um allar viðeigandi færslur.

12. Tilgreindu hvernig reikningskóðinn er notaður:

    * Ef **Reikningskóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu reikningstengslin í **Reikningstengsl** sviði.
    * Ef **Reikningskóði** reiturinn er stilltur á **Allt**, reikningurinn á við allar viðeigandi færslur.
    * Veldu beinlínusniðmátið í **Bein lína sniðmát** reitnum eða sniðmátinu sem byggir á viðburðum í **Sniðmát sem byggir á viðburðum** sviði.

13. Veldu **Vista**.

### <a name="for-purchase-orders"></a>Fyrir innkaupapantanir

Til að tilgreina sjálfgefin frestunargildi fyrir innkaupapantanir skaltu fylgja þessum skrefum.

1. Á **Innkaup** flipanum, veldu frestunartegundina.
2. Smellið á **Bæta við** til að bæta við nýrri línu.
3. Í **Vörukóði** reit, veldu vörukóðann.
4. Tilgreindu hvernig vörukóði er notaður:

    * Ef **Vörukóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu hluttengsl í **Atriðatengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Flokkur**, veldu flokkstengsl í **Flokkstengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Allt**, sjálfgefna gildin eiga við um allar viðeigandi færslur.

5. Tilgreindu hvernig reikningskóðinn er notaður:

    * Ef **Reikningskóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu reikningstengslin í **Reikningstengsl** sviði.
    * Ef **Reikningskóði** reiturinn er stilltur á **Allt**, reikningurinn á við allar viðeigandi færslur.

6. Í **Aðalreikningur** reit, veldu aðalreikning fyrir frestunina.
7. Ef **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap**, veldu upphaflega tekjureikninginn í **Stofntekjureikningur** reit og tekjujöfnunarreikning í **Tekjujöfnunarreikningur** sviði.
8. Ef **Skammtíma frestun aðferð** reiturinn er stilltur á **Rúllutímabil** eða **Fast ártal**, veldu skammtímafrestunarreikninginn í **Skammtímafrestunarreikningur** sviði.
9. Fyrir sniðmát skaltu velja **Bæta við** til að bæta við línu. 
10. Í **Vörukóði** reit, veldu vörukóðann.
11. Tilgreindu hvernig vörukóði er notaður:

    * Ef **Vörukóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu hluttengsl í **Atriðatengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Flokkur**, veldu flokkstengsl í **Flokkstengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Allt**, sjálfgefna gildin eiga við um allar viðeigandi færslur.

12. Tilgreindu hvernig reikningskóðinn er notaður:

    * Ef **Reikningskóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu reikningstengslin í **Reikningstengsl**.
    * Ef **Reikningskóði** reiturinn er stilltur á **Allt**, reikningurinn á við allar viðeigandi færslur.
    * Veldu beinlínusniðmátið í **Bein lína sniðmát** reitnum eða sniðmátinu sem byggir á viðburðum í **Sniðmát sem byggir á viðburðum** sviði.

13. Veldu **Vista**.

### <a name="for-general-journals"></a>Fyrir almenn tímarit

Til að tilgreina sjálfgefin frestunargildi fyrir almennar dagbókarfærslur, fylgdu þessum skrefum.

1. Veldu **Almennt dagblað** flipa.
2. Fyrir frestun, veldu **Bæta við** til að bæta við línu.
3. Ef **Skammtíma frestun aðferð** reiturinn er stilltur á **Rúllutímabil** eða **Fast ártal**, veldu skammtímafrestunarreikninginn í **Skammtímafrestunarreikningur** sviði.
4. Í **Frestunarreikningur** reit, veldu frestunarreikninginn.
5. Í **Viðurkenningarreikningur** reit, veldu viðurkenningarreikninginn.
6. Ef **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap**, veldu upphaflega tekjureikninginn í **Stofntekjureikningur** reit og tekjujöfnunarreikning í **Tekjujöfnunarreikningur** sviði.
7. Veldu beinlínusniðmátið í **Bein lína sniðmát** reitnum eða sniðmátinu sem byggir á viðburðum í **Sniðmát sem byggir á viðburðum** sviði.
8. Veldu **Vista**.

### <a name="for-free-text-invoices"></a>Fyrir ókeypis textareikninga

Til að tilgreina sjálfgefin frestunargildi fyrir reikninga með frjálsum texta skaltu fylgja þessum skrefum.

1. Veldu **Ókeypis textareikningur** flipa.
2. Fyrir frestun, veldu **Bæta við** til að bæta við línu.
3. Tilgreindu hvernig reikningskóðinn er notaður:

    * Ef **Reikningskóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu reikningstengslin í **Reikningstengsl** sviði.
    * Ef **Reikningskóði** reiturinn er stilltur á **Allt**, gildir reikningskóðinn um allar viðeigandi færslur.

4. Í **Frestunarreikningur** reit, veldu frestunarreikninginn.
5. Ef **Skammtíma frestun aðferð** reiturinn er stilltur á **Rúllutímabil** eða **Fast ártal**, veldu skammtímafrestunarreikninginn í **Skammtímafrestunarreikningur** sviði.
6. Í **Viðurkenningarreikningur** reit, veldu viðurkenningarreikninginn.
7. Ef **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap**, veldu upphaflega tekjureikninginn í **Stofntekjureikningur** reit og tekjujöfnunarreikning í **Tekjujöfnunarreikningur** sviði.
8. Veldu beinlínusniðmátið í **Bein lína sniðmát** reitnum eða sniðmátinu sem byggir á viðburðum í **Sniðmát sem byggir á viðburðum** sviði.
9. Veldu **Vista**.

### <a name="for-invoice-journals"></a>Fyrir reikningabækur

Fylgdu þessum skrefum til að tilgreina sjálfgefin frestungildi fyrir færslubók reikninga.

1. Veldu **Reikningardagbók** flipa.
2. Fyrir frestun, veldu **Bæta við** til að bæta við línu.
3. Tilgreindu hvernig reikningskóðinn er notaður:

    * Ef **Reikningskóði** reiturinn er stilltur á **Tafla** eða **Hópur**, veldu reikningstengslin í **Reikningstengsl** sviði.
    * Ef **Reikningskóði** reiturinn er stilltur á **Allt**, gildir reikningskóðinn um allar viðeigandi færslur.

4. Í **Frestunarreikningur** reit, veldu frestunarreikninginn.
5. Ef **Skammtíma frestun aðferð** reiturinn er stilltur á **Rúllutímabil** eða **Fast ártal**, veldu skammtímafrestunarreikninginn í **Skammtímafrestunarreikningur** sviði.
6. Í **Viðurkenningarreikningur** reit, veldu viðurkenningarreikninginn.
7. Ef **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap**, veldu upphaflega tekjureikninginn í **Stofntekjureikningur** reit og tekjujöfnunarreikning í **Tekjujöfnunarreikningur** sviði.
8. Veldu beinlínusniðmátið í **Bein lína sniðmát** reitnum eða sniðmátinu sem byggir á viðburðum í **Sniðmát sem byggir á viðburðum** sviði.
9. Veldu **Vista**.

### <a name="items-that-are-deferred-by-default"></a>Atriði sem er frestað sjálfgefið

Nota **Hlutum frestað sjálfgefið** síðu til að skilgreina hvaða hlutum er frestað sjálfgefið. Hægt er að setja upp tegundir færslur sem hlutunum verður frestað fyrir. Hægt er að tilgreina hvort einni vöru sé frestað, eða heilum vöruflokki eða flokki.

Þegar þú setur upp hluti sem frestað skaltu velja sjálfgefna reikninga og sniðmát á **Frestun vanskil** síðu. Ef reikningar og sniðmát eru ekki valin, verður færslulínum þar sem þessar vörur eru færðar inn ekki frestað.

Fyrir vörur sem er frestað á grundvelli sölu- eða innkaupaflokks sem þær eru tengdar við, eru frestunarstillingarnar byggðar á flokknum. Hins vegar, ef flokkurinn er ekki valinn í **Flokkstengsl** reit, eru frestunarstillingar flokks sem er hærri í röð notaðar. Til dæmis bætir þú við a **Heimamyndband** söluflokkur en ekki a **Sjónvarp** söluflokkur. Þegar þú bætir við frestunaratriði sem er tengt við **Sjónvarp** flokki, frestun stillingar á **Heimamyndband** eru notuð fyrir hlutinn.

### <a name="set-up-deferred-items"></a>Settu upp frestað atriði

Til að setja upp hluti sem er frestað sjálfgefið skaltu fylgja þessum skrefum.

1. Á **Hlutum frestað sjálfgefið** síðu, veldu flipann sem þú vilt: **Sölupöntun** eða **Innkaup**.
2. Smellið á **Bæta við** til að bæta við nýrri línu.
3. Í **Vörukóði** reit, veldu vörukóðann.
4. Tilgreindu hvernig vörukóði er notaður:

    * Ef **Vörukóði** reiturinn er stilltur á **Hópur** eða **Tafla**, veldu hluttengsl í **Atriðatengsl** sviði.
    * Ef **Vörukóði** reiturinn er stilltur á **Flokkur**, veldu flokkstengsl í **Flokkstengsl** sviði.

5. Endurtaktu skref 2 til 4 fyrir hverja viðbótarlínu sem þú þarft.
6. Veldu **Vista**.

## <a name="deferred-charges"></a>Frestað gjöld

Nota **Frestunargjöld** síðu til að skilgreina hvaða gjöldum er frestað sjálfgefið.

> [!NOTE]
> * Eins og er eru frestanleg gjöld aðeins í boði fyrir sölupantanir.
> * Aðeins er hægt að fresta gjöldum á línustigi. Til að fresta gjaldi á sölupöntunarhausstigi er hægt að setja upp gjaldið sem frestað vöru á sérstakri línu í sölupöntuninni.
> * Til að fresta gjaldtöku fyrir frjálsan textareikning verður þú að slá inn gjaldið sem sérstaka frestað reikningslínu.
> * Þessi virkni er ekki í boði fyrir stuðningsgjöld og tekjuskiptingu.

### <a name="set-up-deferred-charges"></a>Settu upp frestað gjöld

Til að setja upp frestað gjöld skaltu fylgja þessum skrefum.

1. Á **Frestunargjöld** síðu, veldu **Bæta við** til að bæta við línu.
2. Í **Hleðslukóði** reit, veldu gjaldkóðann.
3. Í **Hleðslutengsl** reit, veldu hleðslutengsl.
4. Endurtaktu skref 1 til 3 fyrir hverja viðbótarlínu sem þú þarft.
5. Veldu **Vista**.

## <a name="event-based-deferral-templates"></a>Frestunarsniðmát byggð á tilviki

Nota **Frestunarsniðmát sem byggir á viðburðum** síðu til að skilgreina frestunarsniðmát sem byggir á atburðum sem þú getur notað í frestunarfærslum og úthlutað á **Frestun vanskil** síðu.

### <a name="create-an-event-based-template"></a>Búðu til sniðmát sem byggir á atburðum

Til að búa til frestunarsniðmát sem byggir á viðburðum skaltu fylgja þessum skrefum.

1. Á **Frestunarsniðmát sem byggir á viðburðum** síðu, veldu **Nýtt**.
2. Í **Sniðmát** reit, sláðu inn einstakt heiti fyrir sniðmátið.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í **Tegund úthlutunar** reit, veldu úthlutunartegund:

    * **Breytileg upphæð** – Úthlutaðu tiltekinni upphæð fyrir hverja línu sem er slegin inn.
    * **Jöfn upphæð** – Úthlutaðu sömu upphæð fyrir hverja línu sem er slegin inn. 
    * **Hlutfall** – Úthlutaðu upphæð sem byggir á prósentugildinu sem er slegið inn fyrir hverja línu.
    * **Prósenta af verklokum** – Úthlutaðu uppsafnaðu lokagildi fyrir hverja línu sem er slegin inn.
    * **Breytilegt magn** – Úthlutaðu ákveðnu magni fyrir hverja línu sem er slegin inn.

5. Stilltu **Búðu til sérstaka viðburði fyrir hverja einingu** valmöguleika til **Já** ef þú vilt að hverri atburðarlínu sé skipt jafnt eftir fjölda eininga á reikningsfærslunni. Stilltu það á **Nei** ef þú vilt ekki skipta atburðarlínunum.
6. Í **Lokareikningur** reit, veldu fyrningarreikninginn.
7. Veldu **Bæta við** til að bæta línu efst á lista yfir línur, eða veldu **Bæta við** til að bæta línu neðst á listann.
8. Í **Lýsing** reit, sláðu inn lýsingu á atburðinum.
9. Ef **Tegund úthlutunar** reiturinn er stilltur á **Hlutfall**, tilgreinið úthlutunarprósentu í **Úthlutunarprósenta** sviði. Prósentan verður að vera á milli 0 (núll) og 100. Ef þú yfirgefur **Úthlutunarprósenta** reiturinn auður er hlutfallið talið 0. Summa allra prósenta er sýnd í **Heildarhlutfall** reitinn neðst á síðunni og verður að vera 100.
10. Í **Mánuðir til að renna út** reit, tilgreinið fjölda mánaða sem viðburðurinn gildir. Lokadagsetning á frestun viðskipta er sjálfkrafa færð inn miðað við þetta gildi.
11. Veldu **Þekkja þegar það er sett inn** gátreit til að færa sjálfkrafa tekjur þegar færslan er bókuð. Ef þú skilur gátreitinn eftir skal færa tekjur handvirkt.
12. Í **Viðurkenningarreikningur** reit, veldu viðurkenningarreikning fyrir viðburðinn, ef viðburðurinn notar annan reikning en öll frestunaráætlunin. Þessi reitur er notaður ásamt **Þekkja þegar það er sett inn** gátreit.
13. Endurtaktu skref 7 til 12 fyrir hverja viðbótarlínu sem þú þarft.
14. Veldu **Vista**.

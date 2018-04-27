---
title: "Sameina birgðarunur"
description: "Þessi grein veitir upplýsingar um hvernig á að sameina tvær eða fleiri birgðarunur inn í sameinaða runu."
author: pjacobse
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f118ef38e88171ad1eac463078acf37ba4390e57
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="merge-inventory-batches"></a>Sameina birgðarunur

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um hvernig á að sameina tvær eða fleiri birgðarunur inn í sameinaða runu.

Þegar runur eru sameinaðar, geta útreikningar fínstillt einkenni og runueigindi sameinuðu rununnar. Eftir að upprunarunur eru valdar er hægt að endurskoða og breyta sameinaðri runu áður en hún er bókuð. Einnig er hægt að flytja runusameininguna í birgðabók til samþykktar. Síðan er hægt að taka birgðir frá eða bóka þær beint úr þeirri birgðabók. Þegar sameinuð runa er bókuð, eru birgðir leiðréttar fyrir upprunarunurnar uppruna og sameinuðu rununa.

## <a name="are-there-any-prerequisites"></a>Eru einhver frumskilyrði?
Já, það eru einhverjar sem verður að setja upp áður en hægt er að nota sameiningarverkfæri runu. Eftirfarandi tafla lýsir skilyrðum.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Síða</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Birgðabókanöfn</td>
<td>Það þarf að stofna færslubókarheiti af uppskriftargerð til að nota þegar bókaðar eru runusameiningar í birgðabókum. Valfrjáls kostur sem þó er mælt með: Hægt er að tilgreina að frátekningar séu sjálfkrafa framkvæmdar þegar runusameiningin er flutt í birgðabók. Annars er hætta á að breyting sé gerð á birgðum á lager eftir að sameinaðar runuupplýsingar eru settar upp og færslubókin er bókuð. Til að virkja sjálfvirka frátekningu fyrir færslubókarheiti, veljið <strong>Sjálfvirkt</strong> í svæðinu <strong><strong>Frátekning</strong></strong>.</td>
</tr>
<tr class="even">
<td>Færibreytur birgða- og vöruhúsakerfis</td>
<td>Tilgreina verður sjálfgefið heiti færslubókar fyrir færslubók birgða.</td>
</tr>
<tr class="odd">
<td>Útgefnar afurðir</td>
<td>Mælt er með stillingum fyrir vörur sem hér segir:
<ul>
<li>Til að mynda sjálfkrafa rununúmer fyrir sameinaðar runur verður að úthluta útgefinni afurð á númeraflokk rununnar. Hægt er að færa inn rununúmer handvirkt þegar stofnuð er sameinuð runa, eða velja fyrirliggjandi rununúmer. Ef fyrirliggjandi rununúmer er valið skal gæta þess að valin runa hafi ekki verið tekin með í neinum birgðafærslum.</li>
<li>Ef verið er að nota endingartíma eða best fyrir dagsetningar fyrir losaða afurð, eru dagsetningar fyrir sameinaða runu reiknaðar út samkvæmt valinu í reitnum <strong>Útreikningur dagsetningar fyrir runusameiningu</strong>. Eftirtaldir valkostir eru í boði:
<ul>
<li><strong>Fyrsta</strong> - Útreikningurinn er byggður á fyrstu dagsetningunni sem er tilgreind fyrir upphafsrunu sem er valin í runusameiningu.</li>
<li><strong>Nýjasta</strong> - Útreikningurinn er byggður á nýjustu dagsetningunni sem er tilgreind fyrir upphafsrunu sem er valin í runusameiningu.</li>
<li><strong>Handvirkt</strong> – Enginn útreikningur er gerður. Ef dagsetningin er sú sama í öllum upprunarunur mun vera stungið upp á dagsetningu. Hægt er að breyta þeirri dagsetningu. Ef dagsetning er ekki sú sama á upprunarunum er hægt að færa hana inn handvirkt.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Rununúmeraflokkur</td>
<td>Valfrjálst: Til að mynda rununúmer þegar sameinað runu er stofnað, verður að úthluta númeraflokk rununnar á losaða afurð. Annars er hægt að færa inn rununúmer handvirkt.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Hvenær myndi ég vilja sameina birgðarunur?
Eftirfarandi aðstæður eru dæmi um þegar það gæti verið gagnlegt að sameina runur:

-   Sammy er að fara gegnum vöruhúsið og tekur eftir að nokkrar runur sömu vöru eru með lítið magn. Hann bjóst við að fá margar nýjar sendingar og hann skilur að hann getur losað gólfrými með því að sameina útistandandi magn í eina runu.
-   Sammy er að taka á móti birgðum og vill sameina nýja runu með runu sem hann hefur þegar móttekið til að auka runueigindagildi núverandi runu. Með því er ný keyrsla stofnuð.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Get ég steypa runur í svæði og lögaðilum?
Nei, þú getur bara sameinað runur sem hafa sama svæði og geymsluvíddir vöruhúss í einum lögaðila. Hins vegar hægt að tilgreina á aðra staðsetning og brettakenni fyrir sameinuðu rununa.

## <a name="can-i-merge-partial-quantities"></a>Get ég sameinað hluta af magni?
Nei, það er aðeins hægt að sameina fullt runumagn. Runusameining er ætluð sem eiginleiki í birgðum, ekki eiginleiki framleiðslu.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Hvað ef runur hafa mismunandi runueigindargildi?
Þegar upprunarunur eru valdar til sameiningar í sameinuðu rununni, kannar Finance and Operations hvort einkenni eða eigindagildi eru þau sömu á öllum runum. Þegar eigindagildi er það sama er gildi lagt til fyrir sameinuðu rununa. Hægt er að breyta þessu gildi. Eigindagildi sem eru ekki eins eru höfð auð fyrir sameinaða runu og þú getur slegið inn þessi gildi handvirkt. Ef runueigind fyrir eigindargildi er heiltala eða brot, og gildi eru ekki þau sömu fyrir allar upprunarunur, er gildi reiknað með því að nota vegið meðaltal útreiknings. Útreiknað gildi er sléttuð upp eða niður að næsta hækkunin. Ef gildið er autt fyrir uppruna runu, eru runan og magn hennar ekki teknar með í útreikningnum. **Dæmi** Eftirfarandi dæmi útskýrir útreikning vegins meðaltals fyrir sameinuðu rununa. Tvær uppruna runur hafa autt gildi fyrir runueigind sem er heiltala. Eftirfarandi eigind er úthlutað á upprunarunur.

| Eigind | Lágmark | Stigvaxandi | Hámark |
|-----------|---------|-----------|---------|
| Einkunn     | 3       | 3         | 30      |

Upprunarunurnar hafa eftirfarandi eigindargildi fyrir eigindina **Einkunnaruna**.

| Runa | Magn | Eigind | Eigindargildi |
|-------|----------|-----------|-----------------|
| B1    | 10       | Einkunn     | Autt           |
| B2    | 15       | Einkunn     | 15              |
| B3    | 20       | Einkunn     | 20              |
| B4    | 25       | Einkunn     | Autt           |
| B5    | 30       | Einkunn     | 25              |

Þegar þú bætir þessum runum við sem upprunarunum, er hinni sameinuðu runu úthlutað eftirfarandi gildum.

| Runa | Magn | Eigind | Eigindargildi |
|-------|----------|-----------|-----------------|
| B6    | 100      | Einkunn     | 21              |

Gildi og magn fyrir runur B1 og B4 eru ekki teknar með í útreikningi vegins meðaltals. Því er gildi fyrir sameinuðu rununa reiknað sem hér segir.

| Gildi | Magn (þyngd)                              | Hlutfallslegt þyngd | Hlutfallslegt þyngd x Gildi                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0.230769231     | 3.461538462                                                           |
| 20    | 20                                             | 0.307692308     | 6.153846154                                                           |
| 25    | 30                                             | 0.461538462     | 11.53846154                                                           |
|       | **Samtals:** 65, sem er samtals þyngd |                 | **Samtals:** 21,5384615, sléttað í 21, (sem er næsta heiltalan) |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Hvað ef runur hafa mismunandi runudagsetningar?
Ef runur hafa mismunandi runudagsetningar, eru sumar dagsetningar reiknaðar út frá gildum í flokknum **Runudagsetningar** á flýtiflipanum **Sameinuð runa** á síðunni **Runusameining**. Kerfið reiknar gildi fyrir svæðin í flokknum **Runudagsetningar**. Þessi gildi eru meðal annars framleiðsludagsetning, lokadagsetning, ráðlagður geymslutími og best fyrir dagsetningar. Dagsetningar eru reiknaðar út frá stillingum fyrir vöru í svæðaflokkunum **Vörugögn** á síðunni **Upplýsingar um losaðar afurðir**. Hægt er að breyta gildum eða færa þau inn handvirkt. Engin útreikningur er gerður fyrir allar aðrar dagsetningar. Sama reglan er notað fyrir runueigindargildi. Ef dagsetningu er sú sama fyrir allar runur verður þessi  dagsetningin lagt til fyrir sameinuðu rununa. Ef dagsetning er ekki sú sama fyrir allar upprunarunur er dagsetning auð í sameinuðu rununni og hægt er að færa hana inn handvirkt.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Hvað ef víddir eru mismunandi runur sem ég á að sameina?
Afurðavíddir, rakningarvíddir, og geymsluvíddir eru meðhöndlaðar eins og hér segir:

-   **Afurðavíddir** - Allar afurðavíddir fyrir tiltekið atriði verða að vera þær sömu. Ekki er hægt að sameina runur yfir afurðavíddir.
-   **Rakningarvíddir** -  Nýtt rununúmer er sjálfkrafa myndað ef hópur rununúmers er tilgreindur fyrir hlutinn. Ef rununúmeraflokki er ekki úthlutað á vöru, er hægt að velja fyrirliggjandi runu eða færa inn númerið handvirkt. Raðnúmer eru fluttar úr upprunarununni í birgðabókarlínur fyrir sameinuðu rununa.
-   **Geymsluvíddir** - Geymsluvíddir svæðis og vörugeymslu verða að vera þær sömu fyrir allar upprunalotur og sameinuðu lotuna. Hins vegar er hægt að tilgreina nýtt staðsetning og brettakenni fyrir sameinuðu rununa.

## <a name="how-does-posting-work"></a>Hvernig bókun virkar?
Bókun virkar á tvo vegu, eftir því hvort verið er að nota samþykktarferli fyrir færslubækur. Hægt er að nota aðgerðirnar **Flytja í færslubók** og **Bóka runusameiningu** til að flytja runusameininguna í færslubók þar sem hægt er að staðfesta hana og bóka, eða hægt er að bóka runusameininguna beint. Helsti munurinn á þessum tveimur aðgerðum er að flutningur í færslubók bókar ekki runusameininguna. Báðar aðgerðir stofna nýja runu ef fyrirliggjandi runa er ekki valin, uppfæra allar runuupplýsingar og eigindagildi og búa til birgðabók.

-   **Flytja í færslubók** - Flytur upplýsingar um runusameiningu í nýja birgðabók. Ef verið er að setja upp sjálfvirkar frátekningar, er magnið í upprunarunum frátekið. Ekki er hægt að breyta upplýsingum um runusameininguna. Ef það þarf að breyta runusameiningunni verður að eyða færslubókinni. Hægt er að nota færslubók sem verkefni sem annar starfsmaður þarf að framkvæma síðar. Frátekning runumagns á færslubókarlínu er tryggð. Þessi úthlutun gerir gæðastjóra eða vöruhússstjóra kleift að stofna verk fyrir starfsmenn sína.
-   **Bóka runusameininguna** – Bókar runusameininguna beint. Hægt er að framkvæma þessa aðgerð þegar efnisleg sameining hefur átt sér stað.

Hægt er að samþykkja birgðabók fyrir runusameininguna úr listasíðunni **Allar runusameiningar**. Smella á **Færslubók** &gt; **Bóka**. Eftir að færslubók er bókuð, er ekki hægt að breyta upplýsingum í sameinuðu rununni Eftir að þú flytja runusameiningu í birgðabók getur þú aðeins breyta upplýsingum ef færslubókinni er eytt.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Eftir að ég sameinaði atriði fyrir þyngd afurðar, hví sé ég ekki upplýsingar um þyngd afurðar í birgðabók?
Hægt er að sameina runur af vörum í þyngd afurðar eins og öllum öðrum vörum. Hins vegar, eru upplýsingar um þyngd afurðar ekki birtar í birgðabók. Mælt er með því að staðfesta upplýsingar um þyngd afurðar áður en runusameiningin er flutt í birgðabók.


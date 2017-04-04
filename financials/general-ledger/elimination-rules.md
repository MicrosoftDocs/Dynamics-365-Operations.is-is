---
title: Losunarreglur
description: "Þetta efni veitir upplýsingar um mismunandi valkosti fyrir skýrslur um losun og losunarreglur."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Losunarreglur

Þetta efni veitir upplýsingar um mismunandi valkosti fyrir skýrslur um losun og losunarreglur.

Útilokunarfærslna er krafist þegar yfirlögaðili stundar viðskipti við einn eða fleiri undirlögaðila og notar sameinaðar fjárhagsskýrslur. Samstæðureikningsskil verða að innihalda eingöngu færslur sem verða á milli sameinaðs fyrirtækis og annarra eininga utan þess fyrirtækis. Þess vegna færslur á milli lögaðila sem eru hluti af sömu samstæðu þarf að fjarlægja eða sleppt úr fjárhag, þannig að þeir ekki að birtast á fjárhagsskýrslur. Það eru margar leiðir til að tilkynna um losun:

-   Hægt er að stofna losunarreglu og keyra á samstæðu- eða losunarfyrirtæki.
-   Fjárhagsskýrslu má nota til að sýna útilokunarlykla og víddir á tiltekinni röð eða dálki.
-   Sérstakan lögaðila má nota til að bóka færslur handvirkt til að rekja losun.

Þetta viðfangsefni leggur áherslu á losunarreglur sem eru myndaðar í samstæðu- eða losunarfyrirtæki. Þú getur sett upp losunarreglur til að búa til losunarfærslur í lögaðila sem er tilgreindur sem ákvörðunarlögaðili fyrir losun. Viðtökulögaðilann er einnig þekktur sem losunarlögaðili. Hægt er að mynda útilokunarbækur annaðhvort í samstæðuferlinu eða með því að nota tillögu útilokunarbókar. Áður en losunarreglur eru settar upp er gott að þekkja eftirfarandi hugtök:

-   **Upprunalegur lögaðili** - Lögaðili þar sem upphæðir sem á að eyða voru bókaðar.
-   **Viðtökulögaðili** – Lögaðili þar sem losunarreglur eru bókaðar.
-   **Losunarlögaðili** – Lögaðili sem er tilgreindur sem viðtökulögaðili fyrir losun.
-   **Sameinaður lögaðili** – Lögaðili sem er stofnaður til að skrá fjárhagsniðurstöður fyrir hóp lögaðila. Fjárhagsgögnin frá lögaðilar eru tekin saman inn í þennan lögaðila og fjárhagsskýrsla er stofnuð með sameinuðu gögnunum.

Eftirfarandi tafla sýnir gerðir færslna gæti þurft að losa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Færslugerð</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sölupöntunarfærsla og reikningsfærsla (miðstýrð vinnsla)</td>
<td>Að selja vöru viðskiptavina fyrir hönd annars lögaðila í þínu fyrirtæki.</td>
</tr>
<tr class="even">
<td>Sölupöntunarfærsla (innan samstæðu/innan fyrirtækis) og reikningsgerð</td>
<td>Að selja afurðir á milli lögaðila í þínu fyrirtæki.</td>
</tr>
<tr class="odd">
<td>Innkaupapantanir (miðstýrð vinnsla)</td>
<td>Þú kaupir birgðir, þjónustu, eignir, og aðrar vörur frá lánardrottni fyrir hönd annars lögaðila í þínu fyrirtæki.</td>
</tr>
<tr class="even">
<td>Birgðastjórnun (innan samstæðu/innan fyrirtækis)</td>
<td><ul>
<li>Er að flytja einum lögaðila birgðir í eignir annars lögaðila í þínu fyrirtæki.</li>
<li>Er að flytja birgðir einum lögaðila á aðra lögaðila í þínu fyrirtæki.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Birgðarakning í flutningum</td>
<td>Flytja vörur milli vöruhúsa sama lögaðila, en milli mismunandi staða landfræðilega.</td>
</tr>
<tr class="even">
<td>Miðstýrð reikningavinnsla lánadrottna</td>
<td>Skrá reikning fyrir hönd annars lögaðila í þínu fyrirtæki.</td>
</tr>
<tr class="odd">
<td>Miðstýrð greiðsluvinnsla lánadrottna</td>
<td>Greiða reikning fyrir hönd annars lögaðila í þínu fyrirtæki.</td>
</tr>
<tr class="even">
<td>Reiðufjárstjórnun og fjárstýring (miðstýrð vinnsla)</td>
<td><ul>
<li>Þú vinnur skattagreiðslur, skattaendurgreiðslur, vaxtagjöld, lán, fyrirgramgreiðslur, arðgreiðslur, og fyrirframgreiddar afnotagreiðslur eða sölulaun.</li>
<li>Borga kostnað fyrir hönd annars lögaðila í þínu fyrirtæki. Reikningurinn er færður inn í bækur á ákvörðunarstað lögaðila og hægt að jafna á milli lögaðila. Til dæmis, einn lögaðila greiðir kostnaðarskýrslu starfsmanns í annan lögaðila. Í þessu tilfelli hefur kostnaðarskýrsla starfsmanns útgjöld sem tengjast öðrum lögaðila.</li>
<li>Að færa reiðufé frá einn lögaðila í annað í þínu fyrirtæki.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Viðskiptavinir (miðstýrð vinnsla)</td>
<td>Þú færð reiðufé fyrir reikning viðskiptavinar annars lögaðila, og þú leggur þá ávísun inn á bankareikning þess lögaðila.</td>
</tr>
<tr class="even">
<td>Laun (miðstýrð vinnsla, innan samstæðu/innan fyrirtækis)</td>
<td><ul>
<li>Greidd laun annan lögaðila. Til dæmis greiðir lögaðili eigin laun fyrir starfsmenn sína en rukkar fyrir þá vinnu sem starfsmaður vann fyrir annan lögaðila þann mánuðinn. Eða, starfsmaður ynni hálfan vinnudag fyrir lögaðilann A og hálfan vinnudag fyrir lögaðilann B og fríðindin næðu yfir öll laun. Í þessum tilvikum innihalda laun starfsmanns laun frá báðum lögaðilum. Ekki aðeins laun eru bókuð, heldur einnig skattar, fríðindi, frádráttur og áfallin gjöld fyrir laun.</li>
<li>Þú flytur laun frá einni deild í annað svið eða annað.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eignir (innan samstæðu/innan fyrirtækis)</td>
<td>Flytja eignir í eignir eða birgðir annars lögaðila.</td>
</tr>
<tr class="even">
<td>Úthlutanir (innan samstæðu/innan fyrirtækis)</td>
<td>Er að vinna úthlutanir fyrirtækja. Úthlutanir sem eru aðgerðir fyrir hvern úthlutaðan lykil, óháð upprunalegri kerfiseiningu.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Dæmi
Við lögaðila, lögaðila A, selur búnað til annars lögaðila í þínu fyrirtæki B. lögaðila Eftirfarandi dæmi sýnir hvernig færslur á milli tveggja lögaðila gæti verið að losa:

-   Lögaðili A selur búnaður sem kostar 10,00 til lögaðila B fyrir 10.00.
-   Lögaðili A selur búnaður sem kostar 10,00 til lögaðila B fyrir 10,00, auk 2,00 í raunsendingarkostnað.
-   Lögaðili A selur búnaður sem kostar 10,00 til lögaðila B fyrir 15,00 og viðurkennir framlegð á sölu.
-   Lögaðili A selur búnað sem kostar 10,00 til lögaðila B fyrir 15,00 og viðurkennir helming framlegðar á sölu. Lögaðili B viðurkennir hinn helming framlegðar í sölu. Þess vegna er tekjunum skipt. Skiptar tekjur veitir hvata til að panta frá öðrum lögaðila í fyrirtækinu í stað þess að panta frá utanaðkomandi fyrirtæki.

Allar þessar færslur stofna færslur innan samstæðu sem verða bókaðar á vostro- og nostro-lykla. Þar að auki gætu þessar færslur innihaldið upphæðir álagningar eða afsláttar þegar upphæð sölu innan fyrirtækis er ekki jöfn kostnaði varanna sem verið er að selja.

## <a name="set-up-elimination-rules"></a>Setja upp losunarreglur
Þegar setja upp losunarreglur í Dynamics 365 aðgerða er mælt með því að með því að stofna fjárhagsvídd sérstaklega vegna losunar. Flestum viðskiptavinum heiti það Viðskiptafélaga Samstarfsaðila eða farið svipuð. Ef ákveðið er til að nota fjárhagsvídd síðan gætið þess að hafa aðallykla sem eiga við innan samstæðu færslur. 

Uppsetning losana finnst í svæðinu Uppsetning Sameiningar kerfiseiningar. Eftir að færa inn lýsingu fyrir reglu, verður að taka fyrirtækið sem losunarbókin verður að bóka. Þetta ætti að vera fyrirtæki sem hefur **Nota fyrir losunarferli** valdir í uppsetningu lögaðila. 

Hægt er að setja í dagsetningu sem losunarreglan verður virkur og þegar það er útrunnið, ef þörf krefur. Stilla **Virka** til **Já** ef það á að vera tiltæk í tillöguferlinu losun. Veljið færslubókarheitið sem er af **Losun**.

Eftir að hafa skilgreint í grunnatrið er hægt að skilgreina reglur raunverulegu vinnslu með því að smella á **Línur**. Það eru tveir valkostir fyrir losun, með aðgerðanna upphæð nettóbreyting eða skilgreina fasta upphæð. 

Veljið uppruna lykilinn þinn. Hægt er að nota stjörnu (\*) sem wild kort. Til dæmis 1\* væri að velja alla lykla og byrjar á 1 sem uppruna gagna fyrir úthlutun. 

Þegar búið er að velja lánardrottnalykla uppruna í **Lykill lýsing** ákvarðar lykli fyrir viðtökufyrirtækið sem er notað. Velja **Uppruna** ef óskað er að nota sama aðallykil sem skilgreind er í á **Uppruna** lykil. Ef **Notandaskilgreind**, þá þarf að tilgreina áfangalykil. 

Tilgreining víddar virkar á sama hátt. Ef **Uppruna**, hann mun nota sama vídda í áfangafyrirtækinu sem upprunafyrirtæki. Ef **Notandaskilgreind**, þarf að tilgreina víddir í áfangafyrirtækinu með því að smella á **áfangavíddir** valmyndaratriði. 

Veljið upprunavíddir og fjárhagsvíddir og gildi sem eru notaðar sem gagnagjafi losun.

## <a name="process-elimination-transactions"></a>Vinna Losunarfærslur
Tvær leiðir eru til að vinna úr losunarfærslum meðan sameina online stendur eða með því að stofna inn losunarbókina og keyra losun tillöguferlinu. Í þessum hluta áherslu á stofnun bókar og keyra ferlið losun. 

Fyrirtæki sem er skilgreind sem losunarfyrirtæki, velja **losunarbók** í kerfiseiningunni Sameiningar. Þegar búið er að velja heiti færslubókar, smellið á **Línur**. Hægt er að keyra tillöguna með því að velja á **Tillögur** valmynd og því næst **losunartillaga**.

Veljið fyrirtækið sem er uppruni uppsafnaða gagnanna og veljið síðan regluna sem á að vinna. Færið inn upphafsdagsetningu til að hefja leit að losunarupphæðir og lokadagsetningu til að lokadagur leitar fyrir losunarupphæðir. Í **bókunardagsetning Fjárhags** svæði er dagsetningin sem er notuð til að bóka færslubók í fjárhag. Eftir að smellt er á **í lagi**, hægt er að fara yfir upphæðina og bóka færslubókina.



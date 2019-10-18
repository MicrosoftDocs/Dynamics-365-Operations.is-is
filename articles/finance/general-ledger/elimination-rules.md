---
title: Losunarreglur
description: Þetta efnisatriði veitir upplýsingar um losunarreglur og mismunandi valkosti fyrir skýrslugerð um losanir.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdcfebad5329b8ac6f3507f2bc59f26cf70aae33
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186671"
---
# <a name="elimination-rules"></a>Losunarreglur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um losunarreglur og mismunandi valkosti fyrir skýrslugerð um losanir.

Útilokunarfærslna er krafist þegar yfirlögaðili stundar viðskipti við einn eða fleiri undirlögaðila og notar sameinaðar fjárhagsskýrslur. Samstæðureikningsskil verða að innihalda eingöngu færslur sem verða á milli sameinaðs fyrirtækis og annarra eininga utan þess fyrirtækis. Þess vegna verður að fjarlægja færslur á milli lögaðila sem eru hluti af sömu samstæðu eða sleppa þeim úr fjárhag svo að þær birtist ekki í fjárhagsskýrslum. Það eru margar leiðir til að tilkynna um losun:

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
Þegar losunarreglur eru settar upp er mælt með því að búin sé til fjárhagsvídd sérstaklega fyrir losun. Flestir viðskiptavinir kalla hana Viðskiptamaður eða eitthvað svipað. Ef þú ákveður að nota ekki fjárhagsvídd skaltu gæta þess að hafa aðallykla sem eru sértækir fyrir viðskipti innan samstæðu. 

Uppsetningu fyrir losun er að finna á svæðinu Setja upp í einingunni Samstæður. Eftir að þú slærð inn lýsingu fyrir regluna þarftu að velja fyrirtækið sem losunarbókin bókar í. Þetta ætti að vera fyrirtæki sem hefur **Nota fyrir losunarferli fjárhags** valið í uppsetningu lögaðila. 

Hægt er að velja dagsetninguna þegar losunarregla tekur gildi og þegar hún rennur út, ef þörf krefur. Stilla verður **Virk** á **Já** ef þú vilt að hún verði í boði í losunartillöguferlinu. Veldu heiti færslubókar sem er með færslubókargerðina **Losun**.

Eftir að þú hefur skilgreint grunnatriði er hægt að skilgreina raunverulegar úrvinnslureglur með því að smella á **Línur**. Tveir kostir eru í boði fyrir losun, að losa upphæð nettóbreytingar eða skilgreina fasta upphæð. 

Veldu upprunareikning. Hægt er að nota stjörnu (\*) sem algildistákn. Til dæmis myndi 1\* velja alla lykla sem byrja á 1 sem uppruna gagna fyrir úthlutunina. 

Þegar þú hefur valið upprunareikninga ákvarðar **Reikningslýsing** reikning viðtökufyrirtækis sem er notaður. Veldu **Uppruni** ef þú vilt nota sama aðalreikning og er skilgreindur í **Upprunareikningur**. Ef þú velur **Skilgreint af notanda** þarftu að tilgreina viðtökureikning. 

Víddarskilgreiningin virkar með sama hætti. Ef þú velur **Uppruni** notar það sömu víddir í viðtökufyrirtækinu og í upprunafyrirtækinu. Ef þú velur **Skilgreint af notanda** þarftu að tilgreina víddir í viðtökufyrirtæki með því að smella á valmyndaratriðið **Víddir viðtökustaðar**. 

Veldu upprunavíddir og fjárhagsvíddir og gildi sem eru notuð sem uppruni fyrir losunina.

## <a name="process-elimination-transactions"></a>Vinna Losunarfærslur
Tvær leiðir eru til að vinna losunarfærslur, meðan á sameiningu á netinu stendur eða með því að stofna losunarbók og keyra losunartillöguferlið. Í þessum kafla er áherslan á stofnun færslubókar og að keyra losunarferlið. 

Í fyrirtæki sem er skilgreint sem losunarfyrirtæki skal velja **Losunarbók** í einingunni Samstæður. Þegar þú hefur valið heiti færslubókar smellirðu á **Línur**. Þú getur keyrt tillöguna með því að velja valmyndina **Tillögur** og velja **Losunartillaga**.

Veldu fyrirtækið sem er uppruni sameinuðu gagnanna og veldu svo regluna sem þú vilt vinna með. Færðu inn upphafsdag til að hefja leit að losunarupphæðum, og lokadag til að ljúka leit að losunarupphæðum. Í reitnum **Bókunardagsetning fjárhags** er dagsetningin sem er notuð til að bóka færslubókina í fjárhag. Þegar smellt er á **Í lagi** er hægt að endurskoða upphæðirnar og bóka færslubókina.




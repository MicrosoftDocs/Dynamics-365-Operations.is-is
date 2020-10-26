---
title: Vöruskil sölu
description: Þetta efnisatriði veitir upplýsingar um gæðastjórnunarferli fyrir skilapantanir. Það felur í sér upplýsingar um skil viðskiptavina og áhrif þeirra á birgðamagn kostnaðarútreiknings og magn á lager.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnTable, ReturnTableListPagePreviewPane, ReturnTableReferences, SalesReturnExpiredOrdersPart, SalesReturnFindOrderFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd194042303797fe41507065d0d7e4df28309cfb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987415"
---
# <a name="sales-returns"></a>Vöruskil sölu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um gæðastjórnunarferli fyrir skilapantanir. Það felur í sér upplýsingar um skil viðskiptavina og áhrif þeirra á birgðamagn kostnaðarútreiknings og magn á lager.

Viðskiptavinir geta skilað vörum af mismunandi ástæðum. Til dæmis gæti vara verið gölluð eða hún er ekki að uppfylla væntingar viðskiptavinar. Skilaferlið hefst þegar viðskiptavinur gefur út beiðni um skil á vöru. Eftir að beiðni viðskiptavinar er móttekin er skilapöntun stofnuð.

## <a name="return-order-process"></a>Skilapantanavinnsla
Eftirfarandi mynd býður upp á yfirlit yfir skilapöntunina.  

[![Skilapantanavinnsla](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Til eru tvær gerðir skilapöntunarferlis: efnisleg skil og aðeins kredit.

-   **Efnisleg skil** – Skilapöntunin heimilar efnisleg skil á afurðum.
-   **Aðeins kredit** – Skilapöntun heimilar inneign viðskiptavinar en krefst ekki að viðskiptavinurinn skili afurðunum efnislega.

### <a name="physical-return-order-process"></a>Efnisleg skilapantanavinnsla

1.  **Stofna skilapöntun.** Formlega skjalfest heimild fyrir viðskiptavin til að skila öllum gölluðum eða óæskilegum afurðum. Skilapöntunin krefst ekki að fyrirtækið taki við skiluðum afurðum eða veiti viðskiptavininum inneign. Ef skilin eru samþykkt er hægt að heimila að skiptivara sé send áður en gallaðri vöru hefur verið skilað.
2.  **Berist vöruhúsi til skoðunar.** Ljúkið við upphaflega skoðun og villuleit á móti skilapöntunarskjali. Skilapöntun styður einnig biðgeymslu skilaðra vara til frekari skoðunar og gæðaeftirlit.
3.  **Ákvarða ráðstöfun.** Ljúktu skoðunarvinnslu og ákveddu hvað eigi að gera við skilaðar afurðir. Hluti af þessu skrefi er að ákveða hvort tekjufæra eigi viðskiptavininn, hafna skilavöru, eða samþykkja skilavöru, rýra afurðina og senda síðan staðgengsafurð til viðskiptavinarins.
4.  **Mynda fylgiseðil.** Búa til fylgiseðil og staðfesta ákvörðun ráðstöfunarkóða sem voru gerðar í skrefi 3. Ljúka ferli vörustjórnunar.
5.  **Mynda reikning.** Loka skilapöntuninni.

### <a name="credit-only-process"></a>Aðeins kreditvinnsla

1.  **Stofna skilapöntun.** Formlega skjalfest heimild fyrir viðskiptavin til að móttaka kredit án þess að skila öllum gölluðum eða óæskilegum vörum. Ráðstöfunarkóðinn **Aðeins kredit** heimilar ákvörðun þess að kreditfæra viðskiptavin án efnislegra skila.
2.  **Mynda reikning.** Búa til kreditnótu og loka svo skilapöntuninni.

## <a name="return-material-authorization"></a>Heimild skilaefnis
Return Material Authorization (RMA) vinnslu byggir á aðgerðum sölupöntun. RMA er skráð sem skilapöntun sem er stofnuð sem sölupöntun og getur verið tengd annarri sölupöntun, sem kölluð er skiptipöntun. Báðar sölupantanir tengjast upphaflegu RMA-númeri.

-   **Skilapöntun** – Til að skrá RMA þarf að stofna skilapöntun sem er sölupöntun sem er af úthlutaðri gerð, **Skilapöntun.** Allar breytingar sem gerðar eru á RMA-upplýsingum eru sjálfkrafa uppfærðar í sölupöntun. Þar til að skilapöntunin er með stöðuna **Opna**, mun hún ekki birtast á lista yfir sölupantanir. RMA er notuð til að meðhöndla komu og móttöku skilaðra vara, auk þess að heimila ráðstöfunaraðgerðina kredit aðeins (sjá kaflann **Ráðstöfunarkóðar og ráðstöfunaraðgerðir**). Öll önnur eftirfylgniferli þarf að meðhöndla í sölupöntun.
-   **Skiptipöntun** – Þegar skiptipöntun verður send til viðskiptavinarins, getur RMA innihaldið aðra tengda sölupöntun. Handvirkt er hægt að stofna skiptipöntun fyrir RMA til að styðja beinar sendingar. Einnig er hægt að stofna skiptipöntun sjálfkrafa eftir að komu, skoðun og móttöku er lokið fyrir línuatriði RMA með ráðstöfunarkóða sem segir til um endurnýjunarverð. Skiptivörupöntun hefur sömu virkni sem tengist sölupöntun. Til dæmis er hægt að nota hana til að skilgreina sérsniðna vöru sem staðgengil vöru, stofna framleiðslupöntun til að laga skilavöru, stofna innkaupapöntun beinnar afhendingar til að senda skiptihlutinn frá lánardrottni eða styðja annan tilgang.

## <a name="create-a-return-order"></a>Stofna skilapöntun
Skilapöntunarferlið hefst þegar viðskiptavinur hefur samband við fyrirtækið til að skila gallaðri eða óæskilegri vöru og/eða til að fá kreditfærslu. Eftir að fyrirtækið samþykkir skilin eru þau skráð með skilapöntun. Þessi skilapöntun verður þungamiðja fyrir innri vinnslu á skilavöru. Eftirfarandi skýringarmynd sýnir ferli til að stofna skilapöntun.  

[![Ferli fyrir stofnun skilapöntunar](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Stofna skilapöntunarhaus

Þegar vöruskilapöntun er stofnuð verður að taka upplýsingarnar í eftirfarandi töflu með.

| Svæði              | lýsing                                              | Athugasemdir                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Viðskiptavinalykill   | Tilvísun í töfluna Viðskiptavinir                       | Tilgreina þarf fyrirliggjandi viðskiptavinalykil.                                                                                                                                                                                                                                                                                                  |
| Afh.aðsetur   | Heimilisfang sem vörunni var skilað á                 | Sjálfgefið er að aðsetur fyrirtækisins er notað. Ef tiltekið vöruhús er valið í haus er afhendingaraðsetri breytt í afhendingaraðsetur vöruhússins. Hægt er að breyta þessu vistfangi á síðunni **Upplýsingar um skilapantanir**.                                                                                                  |
| Svæði/vöruhús     | Svæði eða vöruhús sem tekur við skilaðri vöru | Afhendingaraðsetrið fyrir skilapöntun er ákvarðað út frá afhendingaraðsetri svæðis eða vöruhúss.                                                                                                                                                                                                                                 |
| RMA-númer         | Tegund sem tengd er skilapöntuninni              | RMA-númer er notað sem varalykill í gegnum ferli skilapöntunar. Auðkennisnúmerið sem er úthlutað er byggt á RMA-númeraröðinni sem var sett upp á síðunni **Færibreytur viðskiptakrafa**.                                                                                                                              |
| Tímamörk           | Síðasta dagsetningin sem hægt er að skila vöru               | Sjálfgefið gildi er reiknað sem gildandi dagsetning plús gildistímabil. Til dæmis ef skil gilda aðeins í 90 daga frá dagsetningu þegar vöruskilapöntun er stofnuð og vöruskilapöntunin var stofnuð þann 1. maí, er gildið í svæðinu **30. júlí**. Gildistími er stilltur á síðunni **Færibreytur viðskiptakrafna**. |
| Ástæðukóði skila | Ástæða viðskiptavinar fyrir að skila vörunni          | Ástæðukóði er valinn í lista yfir notendaskilgreinda ástæðukóða. Hægt er að uppfæra þetta svæði hvenær sem er.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Stofna skilapöntunarlínur

Eftir að lokið hefur verið við skilahaus er hægt að stofna skilalínur með því að nota eina af eftirfarandi aðferðum:

-   Færa handvirkt inn upplýsingar um vöru, magn og aðrar upplýsingar fyrir hverja línu skila.
-   Stofna skilalínu með því að nota aðgerðina **Finna sölupöntun**. Mælt er með því að nota þessa aðgerð þegar vöruskilapöntun er stofnuð. Aðgerðin **Finna sölupöntun** kemur á tilvísun úr skilalínunni í reikningsfærða sölupöntunarlínu og sækir línuupplýsingar eins og vörunúmer, magn, verð, afslætti og kostnaðargildi úr sölulínunni. Tilvísun hjálpar til við að tryggja að þegar vörunni er skilað til fyrirtækisins sé hún metin á sama einingarkostnaði og hún var seld á. Tilvísun sannprófar einnig að skilapantanir séu ekki stofnaðar fyrir meira magn en það magn sem var selt á reikningnum.

>[Athugasemd!] Skilalínur með tilvísun í sölupöntun eru meðhöndlaðar sem leiðréttingar eða bakfærsla á sölu. Nánari upplýsingar er að finna í hlutanum „Bóka í fjárhag“ síðar í þessu efnisatriði.

### <a name="charges"></a>Gjöld

Hægt er að bæta þóknunum og gjöldum við skilapöntun með einni eða fleiri af eftirfarandi aðferðum:

-   Hægt er að bæta gjöldum handvirkt við skilapöntunarhaus, skilapöntunarlínuna eða hvort tveggja.
-   Hægt er að bæta gjöldum sjálfkrafa við haus vöruskilapöntunarinnar sem aðgerð á ástæðukóða.
-   Hægt er að bæta gjöldum sjálfkrafa við skilapöntun, byggt á ráðstöfunarkóða línunnar.

Gjöldum er sjálfkrafa bætt við eftir ástæðukóða skila eða ráðstöfunarkóða sem er úthlutað á línu. Ef ástæðukóða er breytt síðar verða gjöld á fyrirliggjandi færslu ekki fjarlægð en nýrri færslu gjalda gæti verið bætt við, byggt á nýjum ástæðukóða. Þegar gjöldum er bætt við skilapantanalínur verða gjöld sem eru reiknuð sem prósenta af línu eða pöntunargildi neikvæð þegar lína eða lína innkaupapöntunar er neikvæð, nema prósentan sé einnig neikvæð tala. Gjald sem hefur neikvætt gildi stendur fyrir kredit til viðskiptavinar.

### <a name="return-reason-codes"></a>Ástæðukóðar skila

Með því að tengja ástæðukóða skila er hægt að auðvelda greiningu á mynstrum skila. Ástæðukóðar veita upplýsingar um hvers vegna viðskiptavinur vill skila vörum. Sum fyrirtæki hafa marga ástæðukóða. Þessi fyrirtæki flokka ástæðukóða í ástæðukóðaflokka til að fá betra yfirlit og fyrir uppsafnaða skýrslugerð.

### <a name="disposition-codes-and-disposition-actions"></a>Ráðstöfunarkóðar og ráðstöfunaraðgerðir

Mikilvægt skref í skilapöntunarferli er úthlutun ráðstöfunarkóða á skilapöntunarlínu sem hluti af komuskráningu. Ráðstöfunarkóði ákvarðar eftirfarandi upplýsingar:

-   **Fjárhagsleg áhrif** – Ætti að kreditfæra viðskiptavin fyrir skilaðar vörur og öll gjöld sem bæta á við skilapöntunarlínuna?
-   **Ráðstöfun á skilaðri vöru** - Er hægt að bæta vörunni aftur í birgðir, ætti að rýra hana eða á að skila henni aftur til viðskiptavarins?
-   **Vörustjórnun skilaðrar vöru** – Ætti að gefa út skiptivöru á viðskiptavin?

Auk þess að ákvarða hvernig skilaðar vörur eru seldar geta ráðstöfunarkóðar valdið því að gjöld séu notuð í skilalínunni. Einnig er hægt að nota þá til að flokka skil til tölfræðilegrar greiningar. Ráðstöfunarkóðar eru skilgreindir sem hluti af uppsetningu skilapantana. Hins vegar verður hver ráðstöfunarkóði að vísa í eina af innbyggðum ráðstöfunaraðgerðum. Eftirfarandi tafla sýnir innbyggða ráðstöfunarkóða og aðgerðir þeirra. **Mikilvægt:** Ef ekki á að skila vöru, en enn á að kreditfæra á viðskiptavin, skal úthluta ráðstöfunarkóðanum **Aðeins kredit** á skilalínu.

<table>
<thead>
<tr class="header">
<th>Ráðstöfunarkóði</th>
<th>Fjárhagsleg áhrif</th>
<th>Áhrif fyrir vörustjórnun</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aðeins kredit</td>
<td><ul>
<li>Viðskiptavinurinn er tekjufærður fyrir söluverð að frádregnum öllum þóknunum eða gjöldum</li>
<li>Tap af rýrnun á vörunni er bókað í fjárhag.</li>
</ul></td>
<td>Ekki skal skila vörunni. Þessi ráðstöfunaraðgerð er notuð fyrir eftirfarandi tilfelli:
<ul>
<li>Nægilegt traust er á milli aðila.</li>
<li>Kostnaður skila á gölluðum vörum er hindrandi.</li>
<li>Ekki má &#39; leyfa vörurnar aftur inn í birgðir. Vegna annarra skilyrða eru efnislega skil ekki áskilin.&#39;</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredit</td>
<td><ul>
<li>Viðskiptavinurinn er tekjufærður fyrir söluverð að frádregnum öllum þóknunum eða gjöldum</li>
<li>Birgðavirði er aukið með kostnaði vörunnar sem var skilað.</li>
</ul></td>
<td>Vörunni er skilað og er bætt við aftur í birgðir.</td>
</tr>
<tr class="odd">
<td>Skrifa yfir og setja í kredit</td>
<td><ul>
<li>Viðskiptavinurinn er tekjufærður fyrir söluverð að frádregnum öllum þóknunum eða gjöldum</li>
<li>Birgðavirði er aukið með kostnaði vörunnar sem var skilað.</li>
<li>Aðskilin sölupöntun fyrir staðgengil stofnast og er meðhöndluð sérstaklega.</li>
</ul></td>
<td>Vörunni er skilað og er bætt við aftur í birgðir.</td>
</tr>
<tr class="even">
<td>Skrifa yfir og eyða</td>
<td><ul>
<li>Viðskiptavinur er tekjufærður fyrir söluverð að frádregnum öllum þóknunum eða gjöldum.</li>
<li>Tap af rýrnun á vörunni er bókað í fjárhag.</li>
<li>Aðskilin sölupöntun fyrir staðgengil stofnast og er meðhöndluð sérstaklega.</li>
</ul></td>
<td>Vörunni er skilað og hún rýrð.</td>
</tr>
<tr class="odd">
<td>Skila til viðskiptavinar</td>
<td>Ekkert, nema allar þóknanir eða gjöld.</td>
<td>Vörunni er skilað en er send viðskiptavininum aftur eftir skoðun. Þessi ráðstöfunaraðgerð gæti verið notuð ef varan hefur verið skemmd viljandi eða ef ábyrgð hennar hefur verið gerð ógild.</td>
</tr>
<tr class="even">
<td>Rýrnun</td>
<td><ul>
<li>Viðskiptavinurinn er tekjufærður fyrir söluverð að frádregnum öllum þóknunum eða gjöldum</li>
<li>Tap af rýrnun á vörunni er bókað í fjárhag.</li>
</ul></td>
<td>Vörunni er skilað eða hún rýrð.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Koma í vöruhús til skoðunar.
Áður en hægt er að taka efnislega á móti skilavöru í birgðum með því að bóka fylgiseðil, verða vörur að fara gegnum komuskráningu og valfrjálsa skoðun. Eftirfarandi mynd býður upp á yfirlit yfir komuferlið. Eftirfarandi hlutar útskýra hvert skref sem er sýnt á skýringarmyndinni.  

[![Komuferli](./media/salesreturn03.png)](./media/salesreturn03.png)  

Komuferlið hefur nokkur önnur tilbrigði sem þetta efnisatriði nær ekki yfir. Hér eru nokkur af þessum tilbrigðum:

-   Ekki skal nota listann **Komuyfirlit** til að stofna komubók. Þess í stað skal stofna komubókina handvirkt. Skilapantanir munu hafa **sölupöntun** sem tilvísun.
-   Ef verið er að nota vöruhúsakerfi, skal búa til brettaflutninga. Skilalína verður að hafa stöðuna **Komið** við brettaflutning.
-   Skrá skal komu skilavara beint úr skilapöntunarlínu, með því að nota aðgerðina **Skráning**.

Við komuferli eru skil samþætt við almenn ferli fyrir móttöku vöruhúss. Ferli komu styður einnig stofnun biðgeymslupantana fyrir skilavörur sem þurfa að gangast undir aðskilda skoðun.

### <a name="identify-products-in-the-arrival-overview-list"></a>Auðkenna afurðir í listanum yfirlit Komu

Síðan **komuyfirlit** inniheldur lista yfir öll í áætlaða innleið komur. 
>[Athugasemd!] Komur úr skilapöntunum verður að vinna aðskilið frá öðrum gerðum af færslum afhendingar. Þegar verið er að auðkenna innleið pakka á síðunni **Komuyfirlit** (til dæmis með því að nota meðfylgjandi RMA-skjal), í Aðgerðarúðunni er smellt á **Upphafskoma** til að stofna og ræsa komubók sem samsvarar komu.

### <a name="edit-the-arrival-journal"></a>Breyta færslubók

Með því að stilla á valkostinn **Stjórnun biðgeymslu** á **Já**, er hægt að stofna biðgeymslupöntun fyrir skilalínu. Ef lína hefur verið send í biðgeymslu til skoðunar, er hægt að tilgreina ráðstöfunarkóða. 
 
Ef þú stillir valkostinn **stjórnun biðgeymslu** á **Já** í birgðalíkanaflokki vörunnar verður valkosturinn **Stjórnun biðgeymslu** á síðunni **Færslubókarlínur** fyrir komubókarlínuna merktur og ekki er hægt að breyta honum. Ef línan er send í biðgeymslu, verður að tilgreina viðeigandi biðgeymsluvöruhús. 

Ef komulína er ekki send til skoðunar, verður starfsmaður komu í vöruhús að tilgreina ráðstöfunarkóða beint í komubókarlínunni og bóka síðan komubókina. Ef ekki á að úthluta sama ráðstöfunarkóða á allt magn skilalínunnar eða ef fullt magn línunnar hefur ekki verið móttekið verður að skipta línunni. Þegar skipt er upp á komubókarlínunni er einnig skipt skilalínunni (**SalesLine**) og stofnað nýtt lotukenni. Hægt er að skipta línunni með því að draga úr magni í komubókarlínunni. Þegar færslubókin er bókuð er ný skilalína stofnuð sem hefur stöðuna **Áætlað** fyrir eftirstandandi magn. Einnig er hægt að skipta línunni með því að smella á **Aðgerðir** &gt; **Skipta**.

### <a name="process-the-quarantine-order"></a>Keyra biðgeymslupöntunina

Ef skilaafurð er send til skoðunar í vöruhúsi biðgeymslu er öllum viðbótarferlum lokið í biðgeymslupöntun. Ein biðgeymslupöntun er stofnuð fyrir hverja línu komu sem er send í biðgeymslu. Ráðstöfunarkóði tilgreinir niðurstöðu ferlisins skoðun. 

Hægt er að skipta biðgeymslupöntuninni, rétt eins og hægt er að skipta komubók. Ef þú skiptir biðgeymslupöntuninni veldur það samsvarandi skiptum skilalínunnar. Eftir að ráðstöfunarkóðinn hefur verið færður inn skal ljúka biðgeymslupöntuninni með því að nota annaðhvort aðgerðina **Lok** eða aðgerðina **Bóka sem tilbúið**. Ef valið er **Bóka sem tilbúið**, stofnast ný koma í merkt vöruhús. Síðan er hægt að vinna þessa komustjórn með því að nota síðuna **Komuyfirlit**. 

Ef komn á uppruna í biðgeymslupöntun er hægt að breyta ráðstöfunarkóða sem er tengdur við skoðun. Ef biðgeymslupöntun er lokið með því að nota aðgerðina **Lok** er lotan sjálfkrafa skráð. Stundum gæti vara verið send aftur úr biðgeymslu í Sendingar- og móttökudeild. Til dæmis gæti eftirlitsaðili biðgeymslu hugsanlega ekki vitað hvar á að geyma vöru í birgðum. Í þessu tilfelli verður að uppfæra samsvarandi fylgiseðil til að vera rétt skráður og virka með ráðstöfunarkóða sem tilgreindur er vegna biðgeymslunnar. 

Hægt er að senda staðfestingu á innhreyfingu til viðskiptavinar þegar skilalína er skráð. Skýrslan **Skilastaðfesting** svipar til skilapöntunarskjalsins. Skýrslan **Skilastaðfesting** er ekki skráð í bók eða skráð annars staðar í kerfið og hún er ekki nauðsynlegt skref í ferli skilapöntunar.

## <a name="replace-a-product"></a>Skipta um afurð
Til eru tvær aðferðir til þess að stýra vöruskiptum:

-   **Fyrirframgreidd skiptivara** - Skipta út vöru áður en skilavara er fengin frá viðskiptavininum.
-   **Skiptivara eftir ráðstöfunarkóða** – Sjálfkrafa stofna nýja skiptipöntunarlínu.

### <a name="up-front-replacement"></a>Skiptivara stofnuð

Í fyrirframgreiddri skiptivöru er hægt að afhenda skiptihlutinn til viðskiptavinar áður en vörunni er skilað. Þessi aðferð er gagnleg ef t.d. varan er hluti vél sem ekki er hægt að fjarlægja nema varahlutur sé tiltækur til að koma í stað hennar, eða ef þú vilt bara að viðskiptavinurinn fái staðgengilsvöru eins fljótt og auðið er. Fyrirframgreidd skiptipöntun er óháð sölupöntun. Upplýsingar í haus eru frumstilltar frá viðskiptavininum og línuupplýsingar eru frumstilltar úr skilapöntuninni. Hægt er að breyta, vinna og eyða skiptipöntuninni óháð skilapöntuninni. Þegar skiptipöntun er eytt færðu skilaboð um að pöntunin hafi verið stofnuð sem skiptipöntun. Eftirfarandi skýringarmynd sýnir ferlið fyrir fyrirframgreidda skiptivöru.  

![Ferli fyrirframgreiddrar skiptivöru](./media/SalesReturn04.png)

Skilapöntuninin inniheldur tilvísun í skiptipöntun. Ef fyrirframgreidd skiptipöntun er stofnuð fyrir skilapöntun áður en gölluðum vörum er skilað, er hægt að velja ráðstöfunarkóða fyrir staðgengil eftir að gölluðum vörum hefur verið skilað.

### <a name="replacement-by-disposition-code"></a>Skiptivara eftir ráðstöfunarkóða

Ef þú sendir skiptivöru til viðskiptavinarins og nota ráðstöfunaraðgerðina **Skipti og rýrnun** eða **Skipti og kredit** í skilapöntuninni, skal nota ferlið sem er sýnt í eftirfarandi dæmi.  

![Ferli skiptivöru þegar ráðstöfunarkóði er notaður](./media/SalesReturn05.png)

Skiptivara verður afhent með því að nota sjálfstæða sölupöntun, sölupöntun skiptivöru. Þessi sölupöntun er stofnuð þegar fylgiseðillinn fyrir skilapöntun er myndaður. Pöntunarhaus notar upplýsingar frá viðskiptavininum sem vísað er í haus vöruskilapöntunarinnar. Línuupplýsingum er safnað úr þeim upplýsingum sem færðar eru inn á síðunni **Skiptivara**. Síðan **Skiptivara** verður að vera útfyllt fyrir línur sem hafa ráðstöfunaraðgerðirnar sem byrja á orðinu "skipta út." Hins vegar er hvorki magn eða kenni skiptivöru villuleitað eða takmarkað. Þessi hegðun heimilar fyrir þau tilvik þar sem viðskiptavinurinn vill sömu vöru en í annað afbrigði eða stærð, og einnig tilfellum þar sem viðskiptavinurinn vill allt aðra vöru. Sjálfgefið er að vara er færð inn á síðunni **Skiptivara**. Hins vegar er hægt að velja aðra vöru, svo lengi sem aðgerðin hefur verið sett upp. 

>[Athugasemd!] Hægt er að breyta og eyða skiptipöntuninni sölu eftir að hún er stofnuð.

## <a name="generate-a-packing-slip"></a>Mynda fylgiseðil
Áður en hægt er að taka á móti skilavöru í birgðum, þarf að uppfæra fylgiseðil fyrir pöntunina sem hún tilheyrir. Á sama hátt og uppfærsluferli reiknings er uppfærsla fjárhagsfærslunnar, er uppfærsluferli fylgiseðils efnisleg uppfærsla birgðafærslunnar. Með öðrum orðum, þetta ferli sendir breytingarnar í birgðum. Þegar um er að ræða skil, eru skrefin sem hafa verið úthlutuð fyrir ráðstöfunaraðgerð innleidd á meðan á fylgiseðilsuppfærslu stendur. Þegar fylgiseðillinn er myndaður á eftirfarandi tilvik sér stað:

-   Í vöruhúsinu er staðlað ferli notað til að framkvæma efnislega innhreyfingu. Fjárhagsbókanir eru myndaðar ef birgðalíkanaflokkurinn (**Bóka efnislegar birgðir**) og færibreytur viðskiptavina (**Bóka fylgiseðil í fjárhag**) eru stilltar eftir því.
-   Vörur sem eru merktar með ráðstöfunaraðgerðinni sem orðið "rýrnun" inniheldur hafa rýrnað og tap á birgðum er bókað í fjárhag.
-   Vörur sem eru merktar með ráðstöfunaraðgerðinni **Skil til viðskiptavinar** eru mótteknar og afhentar viðskiptavininum. Þessar vörur hafa engin nettóáhrif á birgðir.
-   Sölupöntun fyrir skiptivöru hefur verið stofnuð. Þessi sölupöntun byggist á upplýsingum um síðuna **Skiptivara**.

Hægt er að mynda fylgiseðil einungis fyrir línur með skilastöðuna **Skráðar**, og einungis fyrir allt magn skilalínunnar. Ef nokkrar línur í skilapöntuninni hafa stöðuna **Skráð** er hægt að mynda fylgiseðil fyrir hlutmengi lína með því að eyða öðrum línum af síðunni **Bóka fylgiseðil**. 

Hlutaafhendingar eru skilgreindar í skilapöntunarlínum, ekki vöruskilasendingum. Þess vegna, ef tekið er á móti öllu magninu sem fram kemur í einni skilapöntunarlínu en engu úr öðrum línum í skilapöntuninni, er afhendingin ekki hlutaafhending. Hins vegar, ef skilapöntunarlína segir fyrir um tíu einingar af tiltekinni vöru sem á að skila, en einungis er tekið á móti fjórum, er um að ræða hlutaafhendingu. Ef allar áætlaðar skilavörur hafa ekki borist er hægt að setja sendinguna til hliðar og bíða þar til að afgangurinn af skiluðu magni berst. Einnig er hægt að skrá og bóka hluta af magninu. Hluti ferlisins við bókun fylgiseðla er að hægt er að tengja tilvísunarnúmer fylgiseðils úr sendingarskjölum viðskiptavinar við pöntunarlínur. Þessi tenging er valfrjáls og er aðeins til tilvísunar. Hún stofnar ekki neinar færslubókarupplýsingar. 

Almennt séð er hægt að sleppa umbúðaeiningum fylgiseðils og fara beint í reikningsfærslu. Í þessu tilfelli er skrefum sem myndu hafa verið framkvæmd við myndun fylgiseðils lokið við reikningsfærslu.

## <a name="generate-an-invoice"></a>Mynda reikning
Þó að síðan **Skilapöntun** innihaldi upplýsingar og aðgerðir sem þarf til að meðhöndla sérstaka vörustjórnunarþætti skilapöntunarinnar, verður að nota síðuna **Sölupöntun** til að ljúka reikningsfærslunni. Fyrirtækið getur síðan reikningsfært skilapantanir og sölupantanir á sama tíma og sami einstaklingur getur svo lokið reikningsfærslunni, eftir þörfum. Til að skoða skilapöntun á síðunni **Sölupöntun** er smellt á tengilinn fyrir sölupöntunarnúmer til að opna tengda sölupöntun. Einnig er hægt að finna skilapöntun á síðunni **Allar sölupantanir**. Skilapantanir eru sölupantanir sem hafa pöntun af gerðinni **Skilapöntun**.

### <a name="credit-correction"></a>Kreditleiðrétting

Hluti af reikningsfærslunni er að staðfesta að gjöld séu rétt. Til að orsaka að bókanir í fjárhag verði leiðréttingar (Storno) verða að íhuga að nota valkostinn **Kreditleiðrétting** á flipanum **Annað** á síðunni **Bókun reiknings** þegar reikningur/kreditnóta er bókuð. 
>[Athugasemd!] Sjálfgefni **Kredit leiðrétting** valkosturinn er virkjaður ef á **kreditnótu sem leiðréttingu** valkostinn á í **Færibreytur viðskiptakrafna** síðu hefur verið gerður virkur. Þó er mælt með að bóka ekki með Storno.

## <a name="create-intercompany-return-orders"></a>Stofna samstæðuskilapantanir
Hægt er að ljúka skilapöntunum milli tveggja fyrirtækja innan fyrirtækisins. Eftirfarandi aðstæðuar eru studdar:

-   Einföld skil innan samstæðu milli tveggja fyrirtækja sem taka þátt í samstæðuvenslum
-   Samstæðukeðja sem er skráð þegar skilapöntun viðskiptavinar er stofnuð í fyrirtæki seljanda
-   Samstæðukeðja sem er skráð þegar skilapöntun lánardrottins er stofnuð í fyrirtæki kaupanda
-   Bein afhending sendingar skilar milli tveggja fyrirtækja sem taka þátt í samstæðuvenslum og ytri viðskiptavinar

### <a name="setup"></a>Uppsetning

Eftirfarandi dæmi lágmarksuppsetningu sem er krafist fyrir tvö fyrirtæki til að taka þátt í samstæðuvenslum og nýta viðskipti innan samstæðu.  

![Lágmarksuppsetning](./media/SalesReturn06.png)

Í eftirfarandi dæmi er CompBuy kaupandi fyrirtæki og CompSell fyrirtæki seljanda. Vanalega sendir sölufyrirtækið vörur annaðhvort til kaupandi fyrirtækis eða, í aðstæðum beinnar afhendingar sendingar, beint til endanlegs viðskiptavinar. Í CompBuy, er lánardrottinn IC\_CompSell skilgreindur sem samstæðuendastöð sem tengist fyrirtækinu CompSell. Á sama tíma í CompSell, er viðskiptavinur IC\_CompBuy skilgreindur sem samstæðuendastöð sem tengist fyrirtækinu CompBuy. Skilgreina verður upplýsingar um reglu viðeigandi aðgerðar og gildisvörpun í báðum fyrirtækjunum. Við aðstæður beinnar afhendingar sendingar, er skilapöntun innan samstæðu, sem er einnig sölupöntun innan samstæðu, stofnuð í fyrirtæki seljanda. RMA-númer skilapöntunar innan samstæðu má taka til úr RMA-númeraröð í CompSell eða hægt er að afrita það úr RMA-númer sem úthlutað er á upprunalegu skilapöntuninni í CompBuy. Stillingar RMA í aðgerðareglunni **PurchaseRequisition** í CompBuy ákvarða þessar aðgerðir. Ef vöruskilanúmerið er samstillt þarf að áætla að lágmarka hættu á númeraárekstrum ef tvö fyrirtæki nota sömu númeraröð.

### <a name="simple-intercompany-returns"></a>Einfaldar skilapantanir innan samstæðu

Aðstæðurnar fela í sér tvö fyrirtæki í sama fyrirtækis, eins og sýnt er í eftirfarandi skýringarmynd.  

![Einfaldar skilapantanir innan samstæðu](./media/SalesReturn07.png)

Hægt er að koma á pantanakeðju þegar skilapöntun lánardrottins er stofnuð í kaupandi fyrirtæki eða skilapöntun viðskiptavinar er stofnuð í fyrirtæki seljanda. Samsvarandi pöntun er stofnuð í hinu fyrirtækinu og tryggir að haus og upplýsingar um lánardrottinn skilapöntunar endurspegla stillingar á skilapöntun viðskiptavinar. Skilapöntun sem hefur verið komið getur annaðhvort tekið með eða útilokað tilvísun (**Finna sölupöntun**) í fyrirliggjandi reikningi viðskiptavinar. Fylgiseðlar og reikningar pantanna tveggja má vinna aðskilið. Til dæmis, þarf ekki að búa til fylgiseðil fyrir skilapöntun lánardrottins áður en fylgiseðill er myndaður fyrir skilapöntun viðskiptavinar.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Bein afhendingu á sendingu skilar milli þriggja aðila

Þessar aðstæður geta komið ef fyrri sölu af gerðinni **Beina afhendingu** hefur verið lokið og ef reikningur gagnvart viðskiptavinar er til staðar í fyrirtækinu sem á samskipti við viðskiptavin. Í eftirfarandi skýringarmynd hefur fyrirtækið CompBuy áður selt og reikningsfært afurðir til Extern viðskiptavinar. Afurðir voru sendar beint frá fyrirtæki CompSell viðskiptavin í gegnum keðju pantana innan samstæðu.  

![Bein afhending á sendingu skilar milli þriggja aðila](./media/SalesReturn08.png)

Ef Extern viðskiptavinurinn vill skila afurðum er skilapöntun (RMA02) stofnuð í fyrirtæki CompBuy. Til að koma á samstæðukeðjunni verður skilapöntun að vera merkt fyrir beina afhendingu. Þegar þú notar aðgerðina **Finna sölupöntun** til að taka til reikning viðskiptavinar sem á að skila, er komið á keðju pantana innan samstæðu sem samanstendur af eftirfarandi skjölum:

-   **Upphafleg skilapöntun:** RMA02 (fyrirtæki CompBuy)
-   **Innkaupapöntun:** PO02 (fyrirtæki CompBuy)
-   **Skilapöntun innan samstæðu:** RMA\_00032 (fyrirtæki CompSell)

Eftir að samstæðukeðj beinnar afhendingar hefur verið stofnuð, verða öll efnisleg meðhöndlun og vinnsla á innborgunum að vera í samhengi skilapöntunarinnar innan samstæðu, RMA\_00032 í fyrirtækinu CompSell. Ekki er hægt að móttaka afurðir í fyrirtækinu CompBuy. Þegar ráðstöfunarkóði er tengdur við skilapöntun innan samstæðu er hann samstilltur við upprunalegu skilapöntunina til að leyfa viðeigandi reikningsfærslu á upprunalegu pöntuninni.

## <a name="post-to-the-ledger"></a>Bóka í fjárhag
Bókanir í fjárhag sem eru myndaðar þegar skilapöntun er reikningsfærð verða fyrir áhrifum af nokkrum mikilvægum stillingum og færibreytum:

-   **Skilakostnaðarverð** – Fyrir birgðalíkön önnur en **Staðalkostnað** ákvarðar færibreyta **Skilakostnaðarverð** kostnað vörunnar þegar hún er samþykkt aftur í birgðir eða hún rýrnar. Til að reikna rétt verðmat birgða, er mikilvægt að stilla færibreytuna **Skilakostnaðarverð** rétt. Ef nota á aðgerðina **Finna sölupöntun** til að stofna skilapöntunarlínu sem tilvísun í reikning viðskiptavinar er gildið **Skilakostnaðarverð** jafnt kostnaðarverði vöru sem er seld. Annars er gildið kostnaðarverðs fengið úr uppsetningu á vöru eða hægt er að færa það inn handvirkt.
-   **Kreditleiðrétting/Storno** - Færibreytan **Kreditleiðrétting** á síðunni **Bókun reiknings** ákvarðar hvort bókanir eiga að vera skráðar sem jákvæðar (DR/KR) færslur eða sem leiðréttandi neikvæðar færslur.

Í dæmunum sem fylgja er kostnaðarverð skila sýndt sem **Reiknf. kostnaðarverð**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Dæmi 1: Skilapöntun vísar ekki í reikning viðskiptavinar

Skilapöntun vísar ekki í reikning viðskiptavinar Skiluð vara er kreditfærð. Færibreytan **Kreditleiðrétting** er ekki valin þegar reikningur eða kreditnóta skilapöntunar er mynduð.  

![Skilapöntun vísar ekki í reikning viðskiptavinar](./media/SalesReturn09.png)  

>[Athugasemd!] Aðalsniðmát vöruverðs er notað sem sjálfgefið gildi fyrir færibreytuna **Skilakostnaðarverð**. Sjálfgefin verð er frábrugðið kostnaðarverði við úthreyfingar birgða. Þess vegna eru áhrifin þau að stofnast hefur til taps 3. Þar að auki er skilapöntun ekki með afslátt sem var veittur viðskiptavini í sölupöntuninni. Þess vegna á of mikið kredit á sér stað.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Dæmi 2: Kreditleiðrétting er valin fyrir skilapöntun

Dæmi 2 er það sama og dæmi 1, en færibreytan **Kreditleiðrétting** er valin þegar reikningur skilapöntunar er myndaður.  

![Skilapöntun þar sem kreditleiðrétting er valin ](./media/SalesReturn10.png)  

>[Athugasemd!] Bókanir í fjárhag eru færðar inn sem neikvæðar leiðréttingar.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Dæmi 3: Skilapöntunarlínan eru stofnuð með aðgerðinni Finna sölupöntun

Í þessu dæmi er skilapöntunarlínan stofnuð með aðgerðinni **Finna sölupöntun** Færibreytan **Kreditleiðrétting** er ekki valin þegar reikningur er stofnaður.  

![Skilapöntunarlína sem er stofnuð með aðgerðinni Finna sölupöntun ](./media/SalesReturn11.png)  

>[Athugasemd!] **Afsláttur** og **Skilakostnaðarverð** eru rétt stillt. Þess vegna á sér stað nákvæm bakfærsla reiknings viðskiptavinar.




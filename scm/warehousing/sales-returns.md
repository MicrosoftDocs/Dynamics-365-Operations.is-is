---
title: "Vöruskil sölu"
description: "Þetta efni veitir upplýsingar um ferlið fyrir skilapantanir. Það felur í sér upplýsingar um skil viðskiptavina og áhrif þeirra á birgðamagn kostnaðarútreiknings og á lager."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Vöruskil sölu

Þetta efni veitir upplýsingar um ferlið fyrir skilapantanir. Það felur í sér upplýsingar um skil viðskiptavina og áhrif þeirra á birgðamagn kostnaðarútreiknings og á lager.

Viðskiptavinir geta skila vörum mismunandi ástæðum. Til dæmis gæti verið að gölluðu vöru eða það væri ekki uppfylla expectations viðskiptavinar. Skila ferlið hefst þegar viðskiptavinur gefur beiðni um skil á vöru. Eftir að beiðni viðskiptavinar er móttekin skilapöntun er stofnuð í Microsoft Dynamics 365 fyrir Aðgerðir.

## <a name="return-order-process"></a>Skilapöntunarferlið
Eftirfarandi skýringarmynd veitir yfirlit yfir ferli.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Til eru tvær gerðir skilapöntunarferlið: efnislegt skila og aðeins kredit.

-   **Efnisleg skil** – skilapöntunina heimilar efnislegt skil á afurðir.
-   **Aðeins kredit** – skilapöntunina heimilar inneign viðskiptavinar en ekki þurfa að skila viðskiptavinarins efnislega afurðir.

### <a name="physical-return-order-process"></a>Efnisleg skilapöntunarferlið

1.  **Stofna skilapöntun.** Skjalfesta formally heimild fyrir viðskiptavin sem á að skila öllum afurðum gallaðra eða óæskilegar. Skilapöntun ekki krefjast fyrirtækið samþykkja skilaðar afurðir eða veita kredit fyrir viðskiptavininn. Ef skila er hægt að heimila skiptivöru til að senda áður en gallaðra vara hefur verið skilað.
2.  **Berist vöruhúsi skoðun.** Ljúkið við upphafleg skoðun og villuleit á móti skilapöntun skjalið. Skilapöntun styður einnig biðgeymslu skilaðra vara til frekari skoðunar og gæðaeftirlit.
3.  **Ákvarða ráðstöfunarkóða.** Ljúka vinnslu skoðun og ákveða hvað eigi að gera skilaðar afurðir. Hluti af þetta skref er að ákveða hvort er tekjufæra viðskiptavininn, skila afurð, hafna eða samþykkja skila afurð, rýrnun afurðar og senda staðgengil afurðar til viðskiptavinarins.
4.  **Búa til fylgiseðil.** Búa til fylgiseðil og staðfesta ákvörðun ráðstöfunarkóða sem voru gerðar í skrefi 3. Ljúka ferli vörustjórnun.
5.  **Mynda reikning.** Vöruskilapöntuninni er lokað.

### <a name="credit-only-process"></a>Aðeins vinna kredit

1.  **Stofna skilapöntun.** Skjalfesta formally heimild fyrir viðskiptavin sem á að taka á móti kreditfærsla án þess að skila afurðum gallaðra eða óæskilegar. Í **aðeins Kredit** ráðstöfunarkóða heimilar til þess að kreditfæra viðskiptavinar án þess að efnislegar skil.
2.  **Mynda reikning.** Búa til kreditnótu og loka svo skilapöntunina.

## <a name="return-material-authorization"></a>Skila efni heimildar
Skil númer Vöruskilaheimildar (RMA) vinnslu byggir á aðgerðum sölupöntun. RMA er skráð sem skilapöntun sem er stofnuð sem sölupöntun og getur verið tengd hún kalla skiptipöntun aðra sölupöntun. Tengja báða sölupantanir upphaflegt númer Vöruskilaheimildar.

-   **Skilapöntun** – til Að skrá RMA, er að stofna skilapöntunina sem er sölupöntun sem er úthlutað gerðinni, **Skila pöntun.** Allar breytingar sem gerðar eru upplýsingar um RMA er sjálfkrafa uppfært í sölupöntun. Fyrr en skilapöntunina hefur stöðuna **Opna**, mun hún ekki birtast á lista yfir sölupantanir. RMA er notuð til að meðhöndla vörukoma og móttöku skilaðra vara auk til að heimila kredit aðeins ráðstöfunaraðgerðina (sjá kaflann **ráðstöfunarkóða og ráðstöfunaraðgerðirnar**). Þarf að meðhöndla öll önnur eftirfylgni ferli í sölupöntun.
-   **Skiptipöntun** – Þegar skiptipöntun verður send til viðskiptavinarins, sem RMA getur innihaldið önnur tengd sölupöntun. Handvirkt er hægt að stofna skiptipöntun fyrir RMA til að styðja beinar sendingar. Einnig er skiptipöntun er hægt að stofna sjálfkrafa eftir komu, skoðun og móttöku er lokið fyrir línuatriði RMA með ráðstöfunarkóða sem sem segir til um endurnýjunarverðs. Skilapöntun hefur sömu virkni sem tengist sölupöntun. Til dæmis er hægt að nota hana til að skilgreina sérsniðna vöru sem staðgengil vöru er að stofna framleiðslupöntun til að laga skilavara, stofna innkaupapöntun beinnar afhendingar til að senda skiptihlutinn frá lánardrottni eða styðja öðrum tilgangi.

## <a name="create-a-return-order"></a>Stofna skilapöntun
Skilapöntunarferlið hefst þegar viðskiptavinur tengiliði fyrirtækisins til að skila gallaðra eða óæskilegar afurð og/eða á að kreditfæra. Eftir að fyrirtækið samþykkir skila, skil skráðar með skilapöntun. Þessi skilapöntun verður focal viðtökustaðar fyrir innri vinnslu skiluðu. Eftirfarandi skýringarmynd sýnir ferli til að stofna skilapöntun.  

[![Aðferð fyrir stofnun skilapöntunar](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Stofna haus skilapöntun

Þegar vöruskilapöntun er stofnuð er upplýsingunum í eftirfarandi töflu verður að vera tekin með.

| Svæði              | lýsing                                              | Athugasemdir                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Viðskiptavinalykill   | Tilvísun í töflu Viðskiptavina                       | Gefa verður upp eldri viðskiptavinalykil.                                                                                                                                                                                                                                                                                                  |
| Afh.aðsetur   | Heimilisfang sem vörunni er skilað til                 | Aðsetur fyrirtækisins er notuð að sjálfgefnu. Ef tiltekið vöruhús er valið í haus, afhendingaraðsetur breytt í afhendingaraðsetrið vöruhússins. Hægt er að breyta þessu vistfangi á í **upplýsingar um Skilapantanir** síðu.                                                                                                  |
| Svæði/vöruhús     | Svæði eða vöruhús sem fær skiluðu | Afhendingaraðsetrið fyrir skilapöntun er ákvarðað út frá afhendingaraðsetur svæði eða vöruhús.                                                                                                                                                                                                                                 |
| RMA-númer         | Kenni sem úthlutað er fyrir skilapöntun              | Rma-númer er notað sem varalykill í gegnum ferlið skilapöntun. Rma-númer sem er úthlutað á grundvelli RMA númeraröð sem sett er upp á í **Færibreytur viðskiptakrafna** síðu.                                                                                                                              |
| Tímamörk           | Síðasta dagsetningin sem hægt er að skila vöru               | Sjálfgefið gildi er reiknuð sem gildandi dagsetning plús gildistímabil. Til dæmis ef skil gildir aðeins 90 daga frá dagsetningu þegar vöruskilapöntun er stofnuð og í vöruskilapöntunin var stofnuð á 1.maí, er gildið í svæðinu er **30 Júlí**. Gildistíma er stillt á þá **Færibreytur viðskiptakrafna** síðu. |
| Ástæðukóði skila | Ástæða viðskiptavinar fyrir skil á afurð          | Ástæðukóði er valinn í lista yfir ástæðukóða skilgreindur af notanda. Þetta svæði er hægt að uppfæra hvenær.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Stofna skilapantanalínur

Eftir að lokið skila haus, hægt er að stofna skilalínur með því að nota eina af eftirfarandi aðferðum:

-   Færa handvirkt inn upplýsingar um vöru, magn og aðrar upplýsingar fyrir hverja línu skila.
-   Stofna skilalínu með því að nota í **Finna sölupöntun** aðgerð. Mælt er með því að nota þessa aðgerð þegar vöruskilapöntun er stofnuð. Í **Finna sölupöntun** aðgerð tilvísun úr sem skilalína reikningsfærðar sölupöntunarlínu kemur víddarsamsetningar og línuupplýsingar sækir eins og vörunúmer, magn, verð, afslætti og kostnaðargildi úr sölulínunni. Tilvísun hjálpar til við að tryggja samræmda sem, þegar vörunni er skilað til fyrirtækis, hún hefur metnar á sama einingarkostnað það var seld á. Tilvísun einnig villuleitar sem skila pantanir sem ekki eru kostnaðarjafnaðar stofnaðar fyrir magnið sem er meira en magnið sem var seld á reikningnum.

**Athugasemd:** skilalínur með tilvísun í sölupöntun eru meðhöndluð sem leiðréttingar eða bakfærslu á sölu. Nánari upplýsingar, sjá hlutann "Bóka í fjárhaginn", síðar í þessu efnisatriði.

### <a name="charges"></a>Gjöld

Gjöld og gjöld er hægt að bæta við skilapöntun með eina eða fleiri af eftirfarandi aðferðum:

-   Hægt er að bæta gjöldum handvirkt við skilapöntunarhaus, skilapöntunarlínuna eða bæði.
-   Gjöld getur sé sjálfkrafa bætt við haus vöruskilapöntunarinnar sem aðgerð á ástæðukóða.
-   Gjöld getur sé sjálfkrafa bætt við skilapöntunarlínuna, byggt á ráðstöfunarkóða fyrir línuna.

Gjöld eru sjálfkrafa bætt við eftir ástæðukóða skila eða ráðstöfunarkóða sem er úthlutað á línu. Ef ástæðukóðinn er breytt síðar, gjöld á fyrirliggjandi færslu ekki fjarlægður en gæti verið að bæta við nýja færslu gjalda, byggt á nýja ástæðukóðann. Þegar skilapantanalínur gjöldum er bætt við gjöld sem eru reiknaðar sem prósenta af lína eða gildinu verður neikvætt þegar lína eða línu innkaupapöntunar er neikvætt, nema prósentan er einnig neikvæð tala. Gjald sem hefur neikvætt gildi stendur fyrir kredit til viðskiptavinar.

### <a name="return-reason-codes"></a>Ástæðukóðar skila

Með því að tengja ástæðukóða skila getur hjálpað að auðveldara að greina mynstur skila. Ástæðukóðar veita upplýsingar um hvers vegna viðskiptavinur vill skila vörum. Sum fyrirtæki hafa margar ástæðukóða. Þessi fyrirtæki flokka ástæðukóða í ástæðukóðaflokka til að fá betra yfirlit og uppsafnaða skýrslugerð.

### <a name="disposition-codes-and-disposition-actions"></a>Ráðstöfunarkóða og ráðstöfunaraðgerðirnar

Til mikilvæg skref í ferli úthlutun ráðstöfunarkóða skila pöntunarlínu sem hluti af komuskráningu er. Ráðstöfunarkóða ákvarðar eftirfarandi upplýsingar:

-   **Fjárhagsleg áhrif** – Ætti að kreditfæra viðskiptavinar fyrir skilaðar vörur og öll gjöld sem bæta á við skilapöntunarlínuna?
-   **Ráðstöfun skiluðu vöruna** -Ætti varan getur verið bætt við aftur í birgðir, ætti að rýra hana eða á hún að endurgreiða viðskiptavininum?
-   **Vörustjórnun skiluðu vöruna** – Ætti skiptivöru gefin út á viðskiptavin?

Auk þess að ákvarða hvernig skilaðar vörur eru losaðar, ráðstöfunarkóða getur valdið gjöldum sem nota skal skilalínunni. Þeir geta einnig að nota til að flokka skil til tölfræðilegrar greiningar. Ráðstöfunarkóðar eru skilgreind sem hluti af uppsetningu skilapantanir. Hins vegar hver ráðstöfunarkóða verður að vísa eina af innbyggðu ráðstöfunaraðgerðirnar. Í eftirfarandi töflu er listi yfir innbyggðu ráðstöfunarkóða og aðgerðir þeirra. **Mikilvægt:** Ef ekki á að skila vöru, en enn á að kreditfæra viðskiptavinar, sem úthluta á **aðeins Kredit** ráðstöfunarkóða skila línu.

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
<li>Viðskiptavinar tekjufærður söluverð að frádregnum allar þóknanir eða gjöld.</li>
<li>Tap frá henda vörunni er bókuð í fjárhag.</li>
</ul></td>
<td>Ekki ætti að skila vöru. Þessi ráðstöfunaraðgerð er notað fyrir eftirfarandi tilfellum:
<ul>
<li>Ekki er nægilegt trausti á milli aðila í.</li>
<li>Kostnaður skilar gallaðra vara er prohibitive.</li>
<li>Vörur ekki leyfð aftur í birgðir. Vegna önnur skilyrði, er efnislega skil ekki áskilið.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredit</td>
<td><ul>
<li>Viðskiptavinar tekjufærður söluverð að frádregnum allar þóknanir eða gjöld.</li>
<li>Birgðavirði aukið með kostnað vörunnar sem var skilað.</li>
</ul></td>
<td>Vörunni er skilað og er bætt við aftur í birgðir.</td>
</tr>
<tr class="odd">
<td>Skrifa yfir og setja í kredit</td>
<td><ul>
<li>Viðskiptavinar tekjufærður söluverð að frádregnum allar þóknanir eða gjöld.</li>
<li>Birgðavirði aukið með kostnað vörunnar sem var skilað.</li>
<li>Aðskildum sölupöntun fyrir staðgengil stofnast og er að meðhöndla sérstaklega.</li>
</ul></td>
<td>Vörunni er skilað og er bætt við aftur í birgðir.</td>
</tr>
<tr class="even">
<td>Skrifa yfir og eyða</td>
<td><ul>
<li>Viðskiptavinar tekjufærður söluverð minni neinum þóknanir eða gjöld.</li>
<li>Tap frá henda vörunni er bókuð í fjárhag.</li>
<li>Aðskildum sölupöntun fyrir staðgengil stofnast og er að meðhöndla sérstaklega.</li>
</ul></td>
<td>Vörunni er skilað og rýrnun.</td>
</tr>
<tr class="odd">
<td>Skila til viðskiptavinar</td>
<td>Ekkert, nema allar þóknanir eða gjöld.</td>
<td>Vörunni er skilað en er sent viðskiptavininum aftur eftir skoðun. Þessi ráðstöfunaraðgerð gæti verið notað ef varan hefur verið skemmt með vilja eða ef það á ábyrgð hefur verið ógilt.</td>
</tr>
<tr class="even">
<td>Rýrnun</td>
<td><ul>
<li>Viðskiptavinar tekjufærður söluverð að frádregnum allar þóknanir eða gjöld.</li>
<li>Tap frá henda vörunni er bókuð í fjárhag.</li>
</ul></td>
<td>Vörunni er skilað eða hún rýrnar.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Komu í vöruhúsi skoðun
Áður en hægt efnislega á móti skilavöru í birgðum með því að bóka fylgiseðil, vörur verða að fara gegnum komuskráningu og valfrjáls skoðun. Eftirfarandi skýringarmynd veitir yfirlit yfir ferlið komu. Í köflunum sem fylgja lýsa hvert skref sem er sýnd í skýringarmynd.  

[![Komuferli](./media/salesreturn03.png)](./media/salesreturn03.png)  

Ferlið hefur nokkur tilbrigði öðrum sem ekki eru kostnaðarjafnaðar þakin í þessu efnisatriði. Hér eru einhverjum af þessum afbrigði:

-   Ekki nota í **komuyfirlit** lista til að stofna komubók. Í stað þess að stofna handvirkt komubókina. Skila verður pantanir **sölupöntun** sem tilvísun.
-   Ef verið er að nota vöruhúsakerfi, búa til brettaflutnings. Skila línu verður að hafa stöðuna **Komið** við brettaflutning.
-   Skrá komu skilavara beint úr skilapöntunarlínu, með því að nota í **Skráning** aðgerð.

Við komuferli, skil eru samþættar við almennar ferli fyrir móttöku vöruhúss. Ferli komu styður einnig stofnun biðgeymslupantanir fyrir skilavörur sem þarf að gangast aðskildar skoðun.

### <a name="identify-products-in-the-arrival-overview-list"></a>Auðkenna afurðir í listanum yfirlit Komu

Í **komuyfirlit** síða inniheldur lista yfir öll í áætlaða innleið komur. **Athugasemd:** Komur úr skilapantanir verður unnið sér frá aðrar gerðir af færslum afhendingartími er reiknaður. Þegar verið er að auðkenna innleið pakka á í **komuyfirlit** síðuna (til dæmis með því að nota meðfylgjandi RMA skjal), í Aðgerðarúðunni er smellt á **Upphafskoma** til að stofna og ræsa komubók sem samsvarar komu.

### <a name="edit-the-arrival-journal"></a>Breyta komubókina

Með því að stilla á **stjórnun Biðgeymslu** valkosturinn að **Já**, er hægt að stofna biðgeymslupöntun fyrir skil línu. Ef lína hefur verið send í biðgeymslu til skoðunar, er hægt að tilgreina ráðstöfunarkóða. **Athugasemd:** Ef sett á **stjórnun Biðgeymslu** valkosturinn að **Já** í birgðalíkanaflokki vörunnar í **stjórnun Biðgeymslu** valkostinn á í **færslubókarlínur** síðu fyrir komubókarlínunni verður merkt og ekki er hægt að breyta. Ef línan er send í biðgeymslu, verður að tilgreina viðeigandi biðgeymsluvöruhús. Ef komulína er ekki send skoðun, verður starfsmaður komu vöruhús tilgreina ráðstöfunarkóða beint á komubókarlínunni og bókið síðan komubókina. Ef sama ráðstöfunarkóða ætti ekki að úthluta til allt magnið skilalínunnar eða fullt magn línunnar hefur ekki verið tekið á móti verður að skipta línunni. Þegar skipt er upp á komubókarlínunni eru einnig skipta skal skilalínunni (**SalesLine**) og stofna nýja lotukenni. Hægt er að skipta línunni með því að draga úr fjölda komubókarlínunni. Þegar færslubókin er bókuð er ný skila lína stofnuð sem hefur stöðuna **Áætlað** fyrir eftirstöðvar. Einnig er hægt að skipta línunni með því að smella **Aðgerðir**&gt;**Skipta**.

### <a name="process-the-quarantine-order"></a>Vinna með biðgeymslupantanir

Ef skilaðar afurðir eru send til skoðunar í biðgeymsluvöruhúsinu, allar frekari vinnslu er lokið í biðgeymslupöntun. Einn biðgeymslupöntun er stofnuð fyrir hverja línu komu sem er send í biðgeymslu. Ráðstöfunarkóða tilgreinir niðurstöðu ferlisins skoðun. Hægt er að skipta biðgeymslupöntuninni, rétt eins og hægt er að skipta í komubók. Ef að skipta biðgeymslupöntuninni veldur samsvarandi skipta skilalínunnar. Ráðstöfunarkóða sem hafa verið færðar inn, ljúka biðgeymslupöntuninni með því að nota annað hvort í **Lok** aðgerð eða **Tilbúið** aðgerð. Ef valið **Tilbúið**, stofnast ný komu í merkt vöruhús. Síðan er hægt að vinna þessa komustjórn með því að nota í **komuyfirlit** síðu. Ef komu byrjaði biðgeymslupöntun, er hægt að breyta ráðstöfunarkóða sem er tengd við skoðun. Ef biðgeymslupöntun er lokið með því að nota í **Lok** aðgerð, lotunnar er sjálfkrafa skráð. Stundum vöru gæti send aftur úr biðgeymslu í Sendingar- og móttökudeild. Til dæmis í biðgeymslu hugsanlega ekki veit hvar á að geyma vöru í birgðum. Í þessu tilfelli samsvarandi fylgiseðil verður að uppfæra rétt skráð og ráðstöfunarkóða sem tilgreindur er í biðgeymslu vegna. Hægt er að senda staðfestingu á innhreyfingu viðskiptavininum þegar sem skilalína er skráð. Í **skilum** skýrslu svipar skilapöntunarskjalið. Í **skilum** skýrslu er ekki skráðar eða annars skráðar í kerfið og honum er ekki nauðsynleg skref í ferli.

## <a name="replace-a-product"></a>Skipta um afurð
Það eru tvær aðferðir fyrir stjórnun staðgengil afurðar:

-   **Skiptivara** -skipta Út vöru áður en skiluðu er fengin frá viðskiptavininum.
-   **Endurnýjunarverð með ráðstöfunarkóða** – Sjálfkrafa stofna nýjan endurnýjunarverð pöntunarlínu.

### <a name="up-front-replacement"></a>Skiptivara stofnuð

Í skiptivara, skiptihlutinn verður afhent viðskiptavininum áður en vörunni er skilað. Þessi aðferð er gagnleg ef t.d. varan er hluti vél sem ekki er hægt að fjarlægja nema varahlut sé tiltæk til að framkvæma hennar, eða ef rétt á viðskiptavina til að hafa eins fljótt og auðið staðgengil afurðar. Skiptivara pöntun er óháð sölupöntun. Upplýsingar í haus er frumstillt frá viðskiptavininum og upplýsingar úr skilapöntuninni frumstillt. Hægt er að breyta, vinna og eyða skiptipöntuninni óháð skilapöntunina. Þegar skiptipöntun er berast pöntunin var stofnuð sem skiptipöntun. Eftirfarandi skýringarmynd sýnir ferlið fyrir skiptivara stofnuð.  

[![Ferli skiptivara](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Skilapöntun inniheldur tilvísun í skiptipöntun. Ef skiptivara pöntun er stofnuð fyrir skilapöntun áður en gallaðra vara er skilað, er hægt að velja ráðstöfunarkóða fyrir staðgengil eftir gallaðra vara hefur verið skilað.

### <a name="replacement-by-disposition-code"></a>Endurnýjunarverð með ráðstöfunarkóða

Ef að senda skiptivöru til viðskiptavinarins og nota í **Skipti og rýrnun** eða **kredit og Skipti** ráðstöfunaraðgerð í skilapöntuninni, er að nota ferlið sem er sýnd í eftirfarandi dæmi.  

[![Ferli endurnýjunarverð ráðstöfunarkóða sem er notaður](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Með því að nota við óháð sölupöntun, sölu skiptipöntun verður afhent skiptihlutinn. Þessi sölupöntun er stofnuð þegar fylgiseðillinn fyrir skilapöntun. Haus notar upplýsingar frá viðskiptavininum sem vísað er í haus vöruskilapöntunarinnar. Lína upplýsingum er safnað af upplýsingunum sem færðar eru inn í **skiptivöru** síðu. Í **skiptivöru** síðu verður að vera útfyllt fyrir línur sem hafa ráðstöfunaraðgerðirnar sem byrja orðið "skipta út." Hins vegar hvorki magn eða kenni vöru sem staðgengil er villuleitað eða takmörkuð. Þessi hegðun heimilar fyrir þau tilvik þar sem viðskiptavinurinn vill sömu vöru en í annað afbrigði eða stærð, og einnig tilfellum þar sem viðskiptavini sem vill alveg aðra vöru. Sjálfgefið, eins og vara er færð inn á við **skiptivöru** síðu. Hins vegar er hægt að velja aðra vöru, svo lengi sem aðgerðin hefur verið sett upp. **Athugasemd:** Er hægt að breyta og eyða skiptipöntuninni sölu eftir að hún er stofnuð.

## <a name="generate-a-packing-slip"></a>Búa til fylgiseðil
Áður en hægt er að taka á móti skilavöru í birgðum, þarf að uppfæra fylgiseðil fyrir pöntunina sem vörur tilheyra. Sama hátt og uppfærsluferli reiknings er uppfærsla fjárhagsfærslunnar, uppfærsla fylgiseðils efnisleg uppfærsla birgðafærslunnar er. Með öðrum orðum, þetta ferli bindur sig við breytingar á birgðum. Ef um er að ræða skil, eru skrefin sem eru úthlutuð fyrir ráðstöfunaraðgerð innleidd á meðan á fylgiseðilsuppfærslu stendur uppfærslu fylgiseðils. Þegar fylgiseðillinn er eftirfarandi tilvik á sér stað:

-   Í vöruhús, staðlað ferlinu er notuð til að framkvæma efnisleg innhreyfing. Fjárhagsbókanir eru myndaðar ef birgðir model flokk (**Bóka efnislegar birgðir**) og færibreytur viðskiptavina (**Bóka fylgiseðil í fjárhag**) stilltar eftir því.
-   Vörur sem eru merktar með ráðstöfunaraðgerðina sem orðið "rýrnun" inniheldur hafa rýrnað og tap birgðir er bókuð í fjárhag.
-   Vörur sem eru merktar með í **Skil til viðskiptavinar** ráðstöfunaraðgerð eru mótteknar og afhentar viðskiptavininum. Þessar vörur hafa nettó áhrif á birgðir.
-   Sala skiptipöntun er stofnuð. Þessi sölupöntun byggist á upplýsingum um í **skiptivöru** síðu.

Hægt er að mynda fylgiseðil einungis línur með skilastöðuna af **Skráðar**, og einungis fyrir allt magn línunnar skila. Ef nokkrum línum í skilapöntuninni í **Skráð** staða, er hægt að mynda fylgiseðil hlutmengi línum með því að eyða aðrar línur úr á **Bóka fylgiseðil** síðu. Hluta skil eru skilgreindar í skilapöntunarlínum, ekki vöruskilasendingum gefið upp. Þess vegna er tekið á móti öllu magninu sem fram kemur á einni skilapöntunarlínu en engu berst frá öðrum línum í skilapöntuninni, afhendingu ekki hlutaafhendingu. Hins vegar ef skilapöntunarlínu krefst 10 einingar af vöru á að skila, en berst aðeins fjórum eininga, afhendingu er hlutaafhendingu. Ef ekki allar áætlaðar skilavörur hafa borist og hægt er að setja sendinguna til hliðar og bíða þar til afgangurinn af skiluðu magni berist. Einnig er hægt að skrá og bóka hluta af magninu. Hluti ferlisins við bókun fylgiseðla er hægt að tengja tilvísun fylgiseðilsnúmerið sendingarskjölum viðskiptavinar við pöntunarlínur. Þessi tenging er valfrjálst og er aðeins til tilvísunar. Það ekki að stofna neinna færslubreytinga. Almennt séð, hægt er að sleppa umbúðaeiningar fylgiseðils stendur og fara beint til reikningsfærslu. Í þessu tilfelli eru skrefin sem myndi hefur verið framkvæmd er við myndun fylgiseðil umbúða lokið við reikningsfærslu.

## <a name="generate-an-invoice"></a>Mynda reikning
Þó í **Skilapöntun** síða inniheldur upplýsingar og aðgerðir sem þarf til að meðhöndla á sérstakan logistical þáttum skilapöntunarinnar, verður að nota í **sölupöntun** síðu til að ljúka reikningsfærslunni. Fyrirtækið getur síðan reikningsfæra skilapantanir og sölupantanir á sama tíma og sömu manneskjunni má ljúka reikningsfærslunni, eftir þörfum. Til að skoða skilapöntun úr á **sölupöntun** síðunni er smellt á tengilinn fyrir sölupöntunarnúmer til að opna tengd sölupöntun. Einnig er hægt að finna skilapöntun á í **Allar sölupantanir** síðu. Skila pantanir eru sölupantanir sem hafa pöntun af gerðinni **Skila pöntun**.

### <a name="credit-correction"></a>Kreditleiðrétting

Staðfestið sem hluti af reikningsfærslunni, gjöld séu rétt. Valdið því að bókanir í fjárhag til leiðréttingar (Storno) verða að íhuga að nota í **Kredit leiðrétting** valkostinn á í **Öðrum** flipanum á **Bókun reiknings** síðuna þegar reiknings/kreditnótu. **Athugasemd:** Sjálfgefnu á **Kredit leiðrétting** valkosturinn er virkjaður ef á **kreditnótu sem leiðréttingu** valkostinn á í **Færibreytur viðskiptakrafna** síðu hefur verið gerður virkur. Þó er mælt með sem er ekki bóka skilar með Storno.

## <a name="create-intercompany-return-orders"></a>Stofna samstæðupantanir skila
Hægt er að ljúka skilapantanir milli tveggja fyrirtækja innan fyrirtækisins. Eftirfarandi aðstæður eru studd:

-   Einföld skil innan samstæðu milli tveggja fyrirtækja sem taka þátt í samstæðu vensl
-   Samstæðukeðja sem er skráð þegar skilapöntun viðskiptavinar er stofnuð í fyrirtæki seljanda
-   Samstæðukeðja sem er skráð þegar skilapöntun lánardrottins er stofnuð í fyrirtæki á
-   Bein afhending sendingu skilar milli tveggja fyrirtækja sem taka þátt í samstæðu vensl og ytri viðskiptavinar

### <a name="setup"></a>Uppsetning

Eftirfarandi dæmi lágmarksuppsetningu sem er krafist fyrir tvö fyrirtæki í samstæðu vensl og nýta viðskipti innan samstæðu.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Í eftirfarandi dæmi CompBuy á fyrirtæki og CompSell er sölufyrirtækið. Vanalega er sölufyrirtækið afgreitt vörum annað hvort í fyrirtæki eða, í aðstæðum beinnar afhendingar sendingu, beint til endanlegs viðskiptavinar. Í CompBuy, lánardrottinn IC\_CompSell skilgreint sem samstæðuendastöð sem tengist fyrirtækinu CompSell. Á sama tíma í CompSell, viðskiptavinur IC\_CompBuy skilgreint sem samstæðuendastöð sem tengist fyrirtækinu CompBuy. Verður að skilgreina upplýsingar um reglu viðeigandi aðgerð og gildisvörpun í báðum fyrirtækjunum. Við aðstæður beina afhendingu sendinga skila samstæðupöntun, sem er einnig samstæðusölupöntun er stofnuð í fyrirtæki seljanda. Hægt er að taka númer Vöruskilaheimildar skilapöntun innan samstæðu úr númeraröðinni RMA í CompSell eða það er hægt að afrita úr rma-númer sem úthlutað er á upprunalegu skilapöntuninni í CompBuy. Stillingar RMA á í **PurchaseRequisition** aðgerðareglu í CompBuy ákvarða þessar aðgerðir. Ef vöruskilanúmerið samstillt að áætla minnka hættu á númer clashes ef tvö fyrirtæki nota sömu númeraröð.

### <a name="simple-intercompany-returns"></a>Einföld skil innan samstæðu

Aðstæðurnar felur í sér tvö fyrirtæki í sama fyrirtækis, eins og sýnt er í eftirfarandi skýringarmynd.  

[![Einföld skil innan samstæðu](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Hægt er að koma keðju pöntunar þegar skilapöntun lánardrottins er stofnuð í fyrirtæki eða viðskiptavinar vöruskilapöntun er stofnuð í fyrirtæki seljanda. Dynamics 365 aðgerða stofnar samsvarandi pöntun í hinu fyrirtækinu og tryggir sem haus og upplýsingar um lánardrottinn skila pöntun endurspeglar skilapöntun stillingar á viðskiptavin. Skilapöntun sem hefur verið komið getur annað hvort taka með eða útiloka tilvísun (**Finna sölupöntun**) í fyrirliggjandi reikning viðskiptavinar. Fylgiseðla og reikninga tvær pantana unnin sérstaklega. Til dæmis, þarf ekki að búa til fylgiseðil fyrir skilapöntun lánardrottins áður en búa til fylgiseðil fyrir skilapöntun viðskiptavinar.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Beina afhendingu á sendingu skilar milli þrjár aðila

Þessar aðstæður geta komið ef fyrri sölu á **Beina afhendingu** gerð hefur verið lokið og ef reikningur gagnvart viðskiptavinar til staðar í fyrirtækinu sem gagnagrunnstenginga við viðskiptavin. Í eftirfarandi skýringarmynd CompBuy fyrirtækið hefur áður seldar og reikningsfærðar afurðir til Extern viðskiptavinar. Afurðir voru sendar beint frá fyrirtæki CompSell viðskiptavin í gegnum keðju pantana innan samstæðu.  

[![Bein afhending sendingu skilar milli þrjár aðila](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Ef Extern viðskiptavinurinn vill skila afurðum er skilapöntun (RMA02) er stofnuð í fyrirtæki CompBuy. Til að koma á samstæðukeðjunni skilapöntun verður að vera merkt fyrir beina afhendingu. Þegar notuð í **Finna sölupöntun** aðgerð til að taka reikning viðskiptavinar sem á að skila, ræðst keðju pantana innan samstæðu sem samanstendur af eftirfarandi skjöl:

-   **Upphafleg skilapöntun:** RMA02 (fyrirtæki CompBuy)
-   **Innkaupapöntun:** PO02 (fyrirtæki CompBuy)
-   **Skilapöntun innan samstæðu:** RMA\_00032 (fyrirtæki CompSell)

Eftir samstæðukeðjunni bein afhending er stofnuð, efnislegar meðhöndlun og vinnslu innborganir verður að vera í samhengi skilapöntunarinnar innan samstæðu, RMA\_00032 í fyrirtækinu CompSell. Getur ekki verið móttekin afurðir í fyrirtækinu CompBuy. Ráðstöfunarkóða er tengdur við skilapöntun innan samstæðu, hún samstillt við upprunalegu skilapöntunina til reikningsfærslu viðeigandi upprunalegu pöntuninni.

## <a name="post-to-the-ledger"></a>Bóka í fjárhag
Bókanir í fjárhag sem eru myndaðar þegar skilapöntun er reikningsfærð eru verða fyrir áhrifum af nokkrum mikilvægt stillingar og færibreytur:

-   **Skilakostnaðarverð** – Fyrir birgðir líkön önnur en **staðalkostnaðar**, **Skilakostnaðarverð** færibreyta ákvarðar kostnað vörunnar þegar hún hefur samþykkt aftur í birgðir eða hún rýrnar. Til að reikna rétta verðmat birgða, er mikilvægt að setja í **Skilakostnaðarverð** færibreyta rétt. Ef nota á **Finna sölupöntun** aðgerð til að stofna skilapöntunarlínu sem tilvísun í reikning viðskiptavinar á **Skilakostnaðarverð** gildi er jafnt kostnaðarverði vöru sem er seld. Annars kostnaðarverð gildið fengið úr uppsetningu á vöru eða hægt er að færa inn handvirkt.
-   **Kreditfæra leiðrétting/Storno** - **Kredit leiðrétting** færibreyta á í **Bókun reiknings** síðu ákvarðar hvort bókun ætti að vera neikvætt, skráð sem jákvæða (DR/KR) færslur sem á að leiðrétta færslur.

Í dæmunum fylgt, kostnaðarverð skila sýndar sem **reikningsfæra kostnaðarverð**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Dæmi 1: Skilapöntunina ekki vísa reikning viðskiptavinar

Skilapöntun ekki vísa reikning viðskiptavinar. Skiluðu vöruna er tekjufærður. Í **Kredit leiðréttingu** færibreyta er ekki valinn þegar skilapöntun reikning eða kreditnótu er mynduð.  

[![Skilapöntun ekki vísa til invoic viðskiptavinar](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Athugasemd:** vöruverð sniðmát er notað sem sjálfgefið gildi fyrir á **Skilakostnaðarverð** færibreyta. Sjálfgefin verð frábrugðið kostnaðarverðið við úthreyfingar birgða. Þess vegna er implication er sem hefur verið stofnað tap 3. Þar að auki er ekki skilapöntun með afsláttar sem var gefið viðskiptavinar í sölupöntunina. Þess vegna mikils kredit á sér stað.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Dæmi 2: Kreditleiðrétting valin er fyrir skilapöntun

Dæmi 2 er sú sama og dæmi 1, en **Kredit-leiðrétting** færibreytan er valin þegar skilapöntun reikningurinn er myndaður.  

[![Þar sem valinn kreditleiðrétting skilapöntun](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Athugasemd:** bókanir í fjárhag eru færðar inn sem neikvætt leiðréttingar.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Dæmi 3: Skilapöntunarlínuna eru stofnaðar með aðgerðinni Finna sölupöntun

Í þessu dæmi er skila sölupöntunarlína er stofnuð með því að nota í **Finna sölupöntun** aðgerð. Í **Kredit leiðrétting** færibreyta er ekki valinn þegar reikningur er stofnaður.  

[![Skila pöntunarlínu sem er stofnuð með því að nota Finna sölupöntun](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Athugasemd:****Afsláttur** og **Skilakostnaðarverð** séu rétt. Þess vegna er nákvæmt bakfærslu reiknings viðskiptavinar á sér stað.



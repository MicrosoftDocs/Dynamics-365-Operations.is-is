---
title: Hvað er nýtt eða breytt í Dynamics 365 for Operations útgáfu 1611 (Nóvember 2016)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 for Operations útgáfu 1611.
author: sericks007
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b3ede085533fee1bb779ed9da899f509a77fc0c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693432"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Hvað er nýtt eða breytt í Dynamics 365 for Operations útgáfu 1611 (Nóvember 2016)

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 for Operations útgáfu 1611.

## <a name="cost-accounting"></a>Kostnaðarbókhald

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skilgreina víddir kostnaðareiningar og flytja inn víddarstök kostnaðareiningar.</td>
<td>Kostnaðareiningar eru notaðar í kostnaðarbókhaldi til að flokka kostnað og skjalfæra kostnaðarflæði. Aðalkostnaðareiningar eru fluttar inn annaðhvort með því að nota gagnatengi Microsoft Dynamics 365 for Operations til að sækja aðallykla beint úr Aðgerðum, eða með því að nota almennt gagnatengi þar sem aðallyklar eru sóttir með Microsoft Excel til að sækja úr annarri gerð upprunakerfis. Þegar aðallyklar hafa verið fluttir inn í kostnaðarbókhald eru þeir notaðir sem víddarstök kostnaðareiningar. Aukakostnaðareiningar eru notandaskilgreindur og eru notaðar í úthlutanir til að skjalfæra kostnaðarflæði.</td>
</tr>
<tr>
<td>Varpa víddum kostnaðareiningar</td>
<td>Ef ekki er hægt að samnýta aðallykla milli lögaðila vegna lögboðinna reikningsskilakrafna, er hægt að varpa þeim þegar þeir hafa verið fluttir inn í kostnaðarbókhald til að fá heildrænt yfirlit þvert á fyrirtækið.</td>
</tr>
<tr>
<td>Skilgreina víddir kostnaðahluta og flytja inn víddarstök kostnaðarhluta.</td>
<td>Kostnaðarhlutir eru allar gerðir hluta sem kostnaði er úthlutað á. Dæmigerður kostnaðarhlutur inniheldur afurðir, verk, tilföng, deildir, kostnaðarstaði og landfræðileg svæði. Hægt er nota gagnatengi Microsoft Dynamics 365 for Operations til að sækja fjárhagsvíddir og gildi úr Aðgerðum eða nota almennt gagnatengi þar sem þú getur sótt víddir og gildi í Excel úr annarri gerð upprunakerfis. Ef fjárhagsvídd kostnaðarstaðar er til dæmis notuð sem hlutavídd eru allir kostnaðarstaðir sem eru innfluttir víddarstök fyrir kostnaðarhlutinn.</td>
</tr>
<tr>
<td>Skilgreina eða flytja inn tölfræðileg víddarstök.</td>
<td>Tölfræðileg víddarstök eru mæld í ópeningalegum einingum, eins og vélastundum, fjölda starfsmanna og kvaðrötum. Þau eru notuð í yfirlitum eða sem grunnur fyrir úthlutanir og dreifingar.</td>
</tr>
<tr>
<td>Stofna veitusniðmát tölfræðiaðgerðar.</td>
<td>Tölfræðileg mælieining veitusniðmáts er notuð til að umbreyta gögnum Dynamics 365 for Operations í tölfræðilegar mælingar. Sniðmátið er síðan tengt tilteknu tölfræðilegu víddarstaki. Sniðmátin eru forstillt þannig að þau sýna aðeins töflur sem eru tengdar við fjárhagsvíddir.</td>
</tr>
<tr>
<td>Stofna fjárhag kostnaðarbókhalds.</td>
<td>Fjárhagur kostnaðarbókhalds er óháð höfuðbók sem notar eigið dagatal og gjaldmiðil. Hún gegnir mikilvægu hlutverki í vinnslu á öllum kostnaðarfærslum. Til dæmis fjárhag kostnaðarbókhalds flokkar kostnað byggðan á kostnaðareiningum sitt og birtir kostnað sem byggjast á víddum sitt eigið hlut. Hægt er að stofna eins marga fjárhagi kostnaðarbókhalds og þarf að gera skýrslu framkvæmdastjórnar frá mismunandi sjónarhornum.</td>
</tr>
<tr>
<td>Stofna stýrieiningar kostnaðar.</td>
<td>Stýrieiningar kostnaðar byggja upp kostnaðarsamsetningu og skilgreina kostnaðarflæði í fjárhag kostnaðarbókhalds. Þær verða að tengjast víddum kostnaðarhluta til að tákna víddir kostnaðarhluta í fjárhag.</td>
</tr>
<tr>
<td>Vinna úr fjárhagsfærslum.</td>
<td>Til að mæla raunafköst verður að hafa gögn. Gögnin eru flutt inn með því að nota tengibúnað sem er skilgreindur fyrir fjárhag kostnaðarbókhalds. Þegar unnið er úr fjárhagsfærslum eru gögn flutt inn stigvaxandi.</td>
</tr>
<tr>
<td>Vinna úr áætlunarfærslum.</td>
<td>Til að mæla áætluð afköst verður að hafa gögn. Gögnin eru flutt inn með því að nota tengibúnað sem er skilgreindur fyrir fjárhag kostnaðarbókhalds. Þegar unnið er úr áætlunarfærslum eru gögn flutt inn stigvaxandi.</td>
</tr>
<tr>
<td>Stofna og nota reglur kostnaðarhegðunar.</td>
<td>Notið reglu kostnaðarhegðunar til að flokka kostnað sem fastan, breytilegan eða breytilegan að hluta. Regla er reglumiðuð og dagsetningarvirk. Sjálfgefið er að allur kostnaður eru merktur sem óflokkaður þar til að reglu kostnaðarhegðunar er beitt og áhrif reglunnar reiknuð. Eftir útreikninginn er kostnaður flokkaður.</td>
</tr>
<tr>
<td>Rekja kostnað.</td>
<td>Til að hjálpa til við að skilja áhrif af kostnaðarreglum, gerir kostnaðarbókhald kleift að rekja kostnað til upprunagilda og notaðra reglna þar sem þær eiga uppruna sinn. Þessi virkni veitir fullan rekjanleika á því hvenær stofnað var til kostnaðar, hvaða kostnaðargerðir voru notaðar og hvaða reglum kostnaðarhegðunar var beitt.</td>
</tr>
<tr>
<td>Skilgreina víddastigveldi.</td>
<td>Hægt er að stofna víddastigveldi fyrir annaðhvort undirflokkun eða flokkun. Til dæmis er hægt að skilgreina undirflokkunarstigveldi sem er byggt á vídd kostnaðareiningar og stökum hennar. Til dæmis er hægt að skilgreina flokkunarstigveldi sem er byggt á vídd kostnaðarhluta og stökum hennar. Skýrslugerðarskipulag er notað í eftirfarandi aðstæðum:
<ul>
<li>Þú skilgreinir reglur fyrir úthlutun, kostnaðarhlutfall og samantekt kostnaðar.</li>
<li>Þú skoðar yfirlit með því að nota vinnusvæðið.</li>
<li>Þú skilgreinir aðgang til að skoða samantekin gögn.</li>
<li>Þú skoðar gögn í Excel.</li>
</ul></td>
</tr>
<tr>
<td>Stofna yfirlit sem hægt er að skoða á vinnusvæðinu.</td>
<td>Vinnusvæðið skal nota til að fá stutt yfirlit yfir raunkostnað og áætlaðan kostnað og einnig frávik. Hægt er að sía gögn eftir tímabili eða kostnaðarstigi. Vinnusvæðið er hannað fyrir stjórnendur sem bera ábyrgð á kostnaðarstýringu. Það er í samræmi við aðgangsreglurnar sem eru skilgreindar fyrir stigveldi vídda.</td>
</tr>
<tr>
<td>Stofna skýrslur með því að nota Excel.
<blockquote>[!NOTE] Þú verður að keyra Microsoft Excel 2016.</blockquote>
</td>
<td>Hægt er að flytja út gögn kostnaðarbókhalds beint í Excel gegnum gagnaeiningar og nota Microsoft PivotTable til að stofna skýrslur.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Útgjaldastýring

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Endurúthluta kreditkortafærslum starfsmanns sem sagt hefur verið upp. | Stundum þegar starfsmanni er sagt upp er lykill lénsþjónustu Active Directory (AD DS) hans er gerður óvirkur þegar virkar kreditkortafærslur sem verður að gjaldfæra eru fluttar inn. Áður ekki var hægt að úthluta fulltrúa kostnaðarfærslu eða tengja kreditkortafærslur við kostnaðarskýrslu. Nú er hægt að nota síðuna **Kreditkortafærslur** til að endurúthluta starfsmanni fyrir allar kreditkortafærslur þar sem tengdum starfsmanni hefur verið sagt upp störfum. Eftir endurúthlutun kreditkortafærslunnar er hægt að velja færsluna fyrir kostnaðarskýrslu og greiða hana með reglulegu ferli fyrir endurgreiðslu kostnaðarskýrslu. |
| Breyta kostnaðarskýrslu kreditkortsupplýsingar fyrir starfsmenn í bið og fyrrverandi starfsmenn. | Hægt er að breyta kreditkortaupplýsingum útgjaldastýringar fyrir starfsmenn í bið og fyrrverandi starfsmenn. Áður var aðeins hægt að breyta kreditkortaupplýsingum kostnaðar ef starfsmaðurinn er virkur starfsmaður. |
| Afrita kostnaðarskýrslu. | Nú er hægt að afrita fyrirliggjandi kostnað þegar stofnuð er ný kostnaðarskýrsla í sömu kostnaðarskýrslunni. Hægt er að afrita kostnaðarskýrslu og öll tengd útgjöld sem ekki eru á kreditkorti í nýja kostnaðarskýrslu. Það þarf samt að framkvæma allar áskildar sundurliðanir og tengja áskildar kvittanir, samkvæmt skilgreindum kostnaðarreglum og undirflokkum. Hægt er að bæta kreditkortafærslum á kostnaðarskýrslu með því að velja til að bæta við óafstemmdum kostnaði. |
| Fjöldabreyta kostnaði. | Sumum kreditkortafærslum er hugsanlega ekki varpað á kostnaðartegund eða þeim gæti verið rangt varpað þegar þær eru fluttar inn. Í þessu tilfelli þurfa starfsmenn að breyta tengdri kostnaðartegund handvirkt. Þegar óafstemmdum kostnaði er stýrt er núna hægt að fjöldabreyta kostnaðartegund fyrir valin útgjöld. Þar að auki er hægt að fjöldabreyta verkinu og viðbótarupplýsingunum þegar völdum útgjöldum fyrir tiltekna kostnaðarskýrslu er stjórnað. |
| Breyta gengi fyrir kreditkortafærslur. | Raungengið sem er notað fyrir kreditkortafærslu gæti verið annað en gengið sem er sett upp í kerfinu. Áðyr gátu starfsmenn ekki breytt gengi fyrir neinar kreditkortafærslur sem voru fluttar inn í Útgjaldastýringu. Nú er hægt að setja færibreytu á síðuna **Færibreytur útgjaldastýringar** til að leyfa að gengi sé breytt fyrir kreditkortafærslur. |
| Setja upp staðfestingu á baráttu við spillingu fyrir útgjöld. | Sumir starfsmenn fyrirtækja gætu átt viðskipti við opinbera starfsmenn og sum útgjöld sem stofnað er til sem hluta af viðskiptum gætu verið álitin vera mútur. Í Útgjaldastýringu er nú hægt að setja upp staðfestingu á baráttu við spillingu, sem er birt fyrir valdar kostnaðartegundir eins og máltíðir og gjafir. Starfsmenn verða að velja hvort útgjöld sem sett eru upp fyrir staðfestingu á baráttu gegn spillingu uppfylli skilyrðin sem eru skilgreindar af reglum fyrirtækisins. |
| Koma í veg fyrir handvirkan innslátt útgjalda fyrir tilteknar kostnaðartegundir. | Hægt er að setja upp kostnaðartegund til að tákna kreditkortafærslu sem ekki er hægt að breyta undirflokki fyrir. Dæmi um það er þóknun fyrir seinkaða greiðslu á kreditkortið. Nú er hægt að setja upp kostnaðartegund sem leyfir að útgjöld séu aðeins stofnuð með innflutningi. Þessi aðgerð kemur í veg fyrir að starfsmenn stofni útgjöld handvirkt fyrir undirflokkinn. Hún leyfir heldur ekki að undirflokknum sé breytt fyrir færslur sem hafa verið fluttar inn og sem nota þennan undirflokk. |
| Tengja inngreiðslu við mörg útgjöld. | Inngreiðsla sem hlaðið er upp í Útgjaldastýringu gæti verið tengd við mörg útgjöld. Áður þurfti að hlaða upp inngreiðslu sem var tengd mörgum útgjöldum einu sinni fyrir hver útgjöld. Núna er hægt að tengja innhreyfingu við kostnað sem hefur þegar verið hlaðið upp og tengdur öðrum kostnaði í sömu kostnaðarskýrslunni. Þar að auki, ef verið er að hlaða upp inngreiðslu í haus kostnaðarskýrslu er hægt að velja eina eða fleiri línur til að tengja við innhreyfingu. |
| Stofna framtíðardagsett útgjöld. | Þegar kostnaðarskýrslu er til dæmis afrituð kann færsludagsetning fyrir útgjöld að hafa dagsetningu í framtíðinni. Fyrri útgáfur heimila ekki framtíðardagsett útgjöld. Nú er hægt að stofna og vista kostnað sem hefur dagsetningu í framtíðinni. Hinsvegar er ekki hægt að senda framtíðardagsett útgjöld. |
| Skilgreina útgjaldaskatt fyrir ríki/hérað. | Í sumum löndum/svæðum kann kostnaður sem myndast í öðru ríki/héraði hugsanlega að falla undir annað vsk-hlutfall. Nú er hægt að setja upp skilgreiningar útgjaldaskatts á stigi ríkis/héraðs, ekki bara í stigi lands/svæðis. Ef reiturinn **Ríki/Hérað** er hafður auður á síðunni **Skattaskilgreining** á vsk-flokkurinn við öll ríki/héruð fyrir tilgreint land/svæði. |
| Setja upp kreditkortagerðir kostnaðar. | Áður var engin síða þar sem hægt var að stofna nýjar kreditkortagerðir, eins og Visa, MasterCard eða AMEX, sem er hægt er að nota með Útgjaldastýringu. Nú er hægt að stofna gerðir kreditkorts til að nota með Útgjaldastýringu. Síðan er staðsett á svæðinu **Uppsetningu** í hlutanum **Útreikningar og kóðar**. |
| Skilgreina margstiga samþykktarverkflæði fyrir kostnaðarskýrslur. | Nýtt verkflæði fyrir kostnaðarskýrslur styður margstiga samþykktarferli. Starfsmenn færa inn bráðabirgðasamþykktaraðila og endanlega samþykktaraðila þegar þeir stofna kostnaðarskýrslu. Verkflæði leiðir kostnaðarskýrsluna síðan fyrst til bráðabirgðasamþykktaraðilanna. Þegar kostnaðarskýrsla hefur verið samþykkt á þessu stigi, leiðir verkflæðið hana til endanlegra samþykktaraðila fyrir endanlega samþykkt. |
| Stofna og vinna með kostnað sem er ekki tengdur kostnaðarskýrslu. | Notandi getur nú stofnað útgjöld og viðhaldið þeim (til dæmis með því að tengja eða sundurliða innhreyfingar eða úthluta gestum) án þess að þurfa fyrst að stofna kostnaðarskýrslu. Hægt er að velja ein eða fleiri útgjöld og bæta þeim við nýja kostnaðarskýrslu, þannig að hægt sé að senda þau til samþykktar. Ný síða fyrir viðhald á kostnaði er tiltæk á **Útgjaldastýring** &gt; **Minn kostnaður** &gt; **Útgjöld**. |

## <a name="financial-management"></a>Fjármálastjórnun

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rekja eignamat með því að nota hugmyndina um eina „bók“.</td>
<td>Áður voru tvær aðskildar gerðir mats notaðar til að rekja eignir: virðislíkön og afskriftabækur. Í núgildandi útgáfu hafa þessar tvær hugmyndir verið sameinaðar í eina matshugmynd sem nefnist bækur. Bækur hafa allar aðgerðir úr bæði virðislíkönum og afskriftabókum. Til dæmis er hægt að slökkva á bókun í fjárhag. Bækur sem bóka í fjárhag eru yfirleitt notaðar fyrir fjárhagsskýrslu fyrirtækisins. Bækur sem bóka ekki í fjárhag má nota fyrir skattaskýrslugerð.</td>
</tr>
<tr>
<td>Framkvæma árslokalokun fjárhags fyrir marga lögaðila.</td>
<td>Til að flýta árslokavinnsluferlinu er nú hægt að keyra árslokalokun fyrir marga lögaðila af samnýttri síðu árslokalokana. Hægt er að skilgreina flokka lögaðila, ásamt stillingum sem ætti að halda eftir af einu ári á næsta. Einnig hafa verið gerðar aðrar viðbætur á nothæfi árslokavinnsluferlisins.</td>
</tr>
<tr>
<td>Nýttu þér viðbætur við endurmat á erlendum gjaldmiðli í fjárhag.</td>
<td>Eftirfarandi endurbætur hafa verið gerðar á fjárhagsferli fyrir endurmat á erlendum gjaldmiðli:
<ul>
<li>Gengisgerð hefur verið bætt við aðallykilinn. Þessi gerð gengis er nú notuð til að ákvarða gengi við endurmat á gjaldmiðli. Ef engin gengisgerð er skilgreind heldur ferlið áfram að nota gengisgerðina sem er skilgreind í fjárhag.</li>
<li>Núna er auðveldara að velja svið aðallykla og gjaldmiðla sem keyra á að endurmatsferli fyrir.</li>
<li>Hægt er að keyra endurmat fyrir marga lögaðila.</li>
<li>Kerfið viðheldur nú sögu um hvert endurmatsferli sem var framkvæmt, eins og það gerir fyrir endurmatsferli viðskiptakrafna (AR) og viðskiptaskulda (AP).</li>
<li>Þegar vinnslan er keyrð er nú hægt að forskoða niðurstöður endurmats. Forskoðun sýnir niðurstöður fyrir alla lögaðila sem vinnslan var keyrð fyrir. Síðan er hægt að bóka alla lögaðila eða hlutmengi þeirra, úr forskoðuninni. Einnig er hægt að flytja niðurstöðurnar í forskoðun í Excel.</li>
</ul></td>
</tr>
<tr>
<td>Skoða færslur fyrir viðbótar bókunarlög.</td>
<td>Á listasíðunni <strong>Prófjöfnuður</strong> og skýrslunni <strong>Víddarskýrsla</strong> er nú hægt að velja viðbótar bókunarlögin sem bætt hefur verið í fjárhag. Þegar viðbótar bókunarlög eru valin verða leiðréttingar fyrir þau bókunalög hafðar með í stöðunum á listasíðunni eða skýrslunni.</td>
</tr>
<tr>
<td>Tengja leiðbeinandi fylgigögn við Lokunarsniðmát fjárhagstímabils.</td>
<td>Áður var hægt að tengja fylgigögn eftir að verki var lokið. Til dæmis var hægt að tengja skýrslu sem var mynduð. Nú er einnig hægt að tengja leiðbeinandi skjal við sniðmátið. Leibeinadi skjalið er síðan afritað í hvert verk í áætlun fjárhagstímabils, þannig að eigandi verks geta skoðað leiðbeiningar um hvernig á að ljúka verkinu.</td>
</tr>
<tr>
<td>Skilgreina uppsetningu samstæðulykils af samnýttri síðu.</td>
<td><strong>Uppsetningarsíða samstæðulykils</strong> er nú samnýtt, svo að fyrirtæki geta skilgreint öll pör lögaðila sem geta átt viðskipti saman. Þar að auki, er nú hægt að færa inn færslu í upphaflegan lögaðila en ekki úr lögaðila áfangastaðar. Ef annar hvor lögaðilanna getur hafið færslu innan samstæðu, verður að skilgreina skráð gagnkvæmt par. Þess vegna er lögaðili áfangastaðar er einnig settur upp sem upphaflegur lögaðili.</td>
</tr>
<tr>
<td>Senda inn rökstuðningsskjöl fyrir fjárhagsáætlanir.</td>
<td>Hægt er að stofna rökstuðningssniðmát sem viðbótarfylgiskjal fyrir allar umbeðnar upphæðir fjárhagsáætlunar. Notendur geta fyllt út upplýsingar í sniðmátið og tengja það við fjárhagsáætlunargerðina, þannig að hægt sé að nota það á meðan samþykktarferlinu stendur.</td>
</tr>
<tr>
<td>Virkja ítarlegar reglur fyrir færslur í fjárhagsáætlunarskrá.</td>
<td>Ef ítarlegar reglur eru skilgreindar í fjárhag er hægt að nota þær reglur fyrir nýjar færslur og viðskiptafærslur í fjárhagsáætlunarskrá.</td>
</tr>
<tr>
<td>Nýttu þér aukinn sýnileika verkþáttar fyrirframgreiðslureikningsfærslu.</td>
<td>Nýja listasíðan <strong>Opna fyrirframgreiðslur</strong> veitir skyndimynd af stöðu verkþáttar fyrirframgreiðslureikningsfærslu. Síðan veitir AP-deild upplýsingar um innkaupapantanir sem hafa eftirstöðvar fyrirframgreiðslu gildi sem verða reikningsfærð, reikningsfærð gildi sem þarf að greiða og greidd reikningsgildi sem verður að nota á staðlaða reikninga. Þar að auki hjálpa viðbætur við sjálfvirka jöfnun á greiddum fyrirframgreiðslureikningum á staðlaða reikninga reikningsfærsluskrifstofufólki að gera gagnafærslu á skilvirkari hátt.</td>
</tr>
<tr>
<td>Notið vinnusvæðið <strong>Reikningsfærslur fyrir samstarf lánardrottna</strong>.</td>
<td>Nýtt vinnusvæði <strong>Reikningsfærsla</strong> á svæðinu <strong>Samstarf lánardrottna</strong> veitir ytri lánardrottnum að öruggan aðgang að þeirra eigin reikningsupplýsingum. Til dæmis geta lánardrottnar séð hvort reikningur hafi verið borgaður og senda reikninga sína. Þessi breyting stuðlar að skilvirkari og tímanlegri samskiptum við ytri lánardrottna. Þess vegna hefur reikningsfærsluskrifstofufólk færri truflanir.</td>
</tr>
<tr>
<td>Skipta um lögaðila á meðan reikningsfærslu stendur.</td>
<td>Viðbætur leyfa reikningsfærsluskrifstofufólk sem verður að færa inn reikninga fyrir marga lögaðila að breyta lögaðila af reikningsfærslusíðunum. Þessi eiginleiki sparar tíma fyrir reikningsfærsluskrifstofufólk, þar sem það þarf ekki lengur að skrá sig út úr núverandi lögaðila og inn í annan lögaðila. Bæði síðan <strong>Altæk reikningabók</strong> og <strong>Lánardrottnareikningar</strong> leyfa notendum að breyta lögaðila við innslátt gagna.</td>
</tr>
<tr>
<td>Stuðningur fyrir rafrænar skrár fyrir skattyfirvöld Bandaríkjanna (IRS) 1099 sameinuðu skráningarkerfi alríkis og ríkis</td>
<td>Þegar skilgreiningarlykillinn <strong>US</strong> er virkjaður veita 1099 rafrænt skattskilaferli viðbótaraðgerðir sem samræmast reglum IRS fyrir sameinað skráningarkerfi alríkis og ríkis. IRS þróaði þetta forrit þannig að það getur áframsent upplýsingar rafrænt til þátttakandi ríkja.</td>
</tr>
<tr>
<td>Uppgjörsviðbætur</td>
<td>Viðbætur hjálpa greiðsluskrifstofufólki að gera skilvirkari jöfnun, þar sem skrifstofufólk getur látið margar óbókaðar greiðslur vera jafnaðar við sama reikning.</td>
</tr>
<tr>
<td>Fyrirtækjakeðjusýn</td>
<td>Skrifstofufólk sem annast miðstýrðar greiðslur geta núna skoðað gjaldfallna reikninga milli fyrirtækja. Vinnusvæðin <strong>Lánardrottnagreiðslur</strong> og <strong>Viðskiptavinagreiðslur</strong> veita nú betri sýn inn í og stjórn á gjaldföllnum reikningum með því að veita leið til að skoða og sía milli fyrirtækja sem eru hluti af stigveldisskipan miðstýrðra greiðslna.</td>
</tr>
<tr>
<td>Nota skal vinnusvæðið <strong>Bankakerfi</strong>.</td>
<td>Nýja vinnusvæðið <strong>Bankakerfi</strong> auðveldar að fylgjast með bankareikningum og stöðum fyrir lögaðila. Núverandi stöður og biðstöður eru tiltækar strax fyrir alla lykla og hægt er að kafa aftur frá stöðunum í sundurliðaðar færslufylgiseðla. Einnig er hægt að sjá söguleg stöðugögn fyrir hvern bankareikning eða samantekt fyrir alla bankareikninga fyrirtækisins, bæði til skemmri og lengri tíma. Hægt er að öðlast betri innsýn í afstemmingu bankareiknings, þar sem dagsetning afstemmingar er skráð fyrir hvern bankareikning og það er einnig vísir fyrir afstemmingar sem eru í gangi.</td>
</tr>
<tr>
<td>Flytja inn rafræn bankayfirlit fyrir alla lögaðila í einu skrefi.</td>
<td>Nú er hægt að flytja inn rafræn bankayfirlit fyrir alla lögaðila í einu skrefi. Bankayfirlitsskrár geta innihaldið yfirlit umrá mörgum bankareikningum og lögaðila og zip-skrár geta innihaldið margar bankayfirlitsskrár. Hægt er að byrja afstemmingu fyrir alla skráða bankareikninga í öllum lögaðilum með því að nota eitt innflutningsferli. Þessi eiginleiki sparar tíma, því ekki þarf að skipta á milli fyrirtækja og innflutnings margra yfirlita. Einnig er hægt að keyra jöfnunarreglur sjálfvirkt gagnvart öllum innfluttum yfirlitum í hverju fyrirtæki.</td>
</tr>
<tr>
<td>Rakning virðismats</td>
<td>Ein eign getur haft margfalt verðmat fyrir mismunandi bókhaldsstaðla og einnig er hægt að bóka tengdar færslur í fjárhag. Áður var þetta verðmat rakið með því að nota annaðhvort virðislíkön eða afskriftarbækur. Núna er hægt að fylgjast með þessu verðmati sem er nú kallað bækur, með því að nota almennt safn færslubóka, fyrirspurna og skýrslna. Þessi sameinaða reynsla einfaldar innleiðingu og dregur úr fjölda viðmóta sem reglubundnar vinnslur krefjast.</td>
</tr>
<tr>
<td>Nýttu þér viðbætur við afskriftakeyrslur milli fyrirtækja.</td>
<td>Nú er hægt að hefja afskriftakeyrslu fyrir eignir þvert á alla lögaðila af einni síðu. Einnig er hægt að sjálfkrafa bóka færslubækur eftir að þær eru stofnaðar. Hægt er að senda stofnun og bókun á færslubókum í runuvinnslu, svo að afskriftir keyra í bakgrunninum. Þessar viðbætur minnka óskilvirkni, því að ekki þarf að hefja stakar afskriftarkeyrslur sérstaklega fyrir hvert og eitt fyrirtæki. Viðbótin virkjar einnig betur miðstýrða stjórnun eigna.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Mannauðsstjórnun

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stofna frammistöðubók.</td>
<td>Áður en yfirferðinni er lokið er oft safnað upplýsingum um verkþætti eða tilvik sem leiddu til árangurs þíns sem starfsmanns á endurskoðunartímabilinu. Hægt er að bæta færslu við frammistöðubókina til að skrá þær aðgerðir og tilvik. Einnig er hægt að tengjast þessar aðgerðir og tilvik við markmið eða frammistöðumat til að veita endurskoðanda meiri upplýsingar.</td>
</tr>
<tr>
<td>Stofna ítarlegri markmið.</td>
<td>Þú hefur meiri stjórn yfir efni þeirra markmiða sem þú setur. Hægt að stofna mælingar fyrir markmiðin, tengja frammistöðubókarfærslur við mælingarnar og tengja og skoða skjöl. Hægt er að geyma markmið sem sniðmát og endurnýta þau fyrir flýtiuppsetningu.</td>
</tr>
<tr>
<td>Stofna ítarlegra frammistöðumat.</td>
<td>Frammistöðumat, sem formlega þekkt sem umfjöllun, er nú orðið nógu sveigjanlegt til að styðja bæði áframhaldandi svörun og enn formlegri yfirferðir. Hægt er að sækja virk markmið og bóka athugasemdir um þau og bæta við hluta til að yfirfara hæfni þína. Viðbótarhlutar eru veittir, þar sem hægt er að bæta við eða skoða mælingar, færslur í frammistöðubók, fylgiskjöl og samþykktir sem tengjast yfirferð.</td>
</tr>
<tr>
<td>Tengja stigveldi stöðu viðbótar við verkflæði.</td>
<td>Hægt er að tengja verkflæði við stigveldi stöðu. Einnig er hægt að breyta verkflæðisskrefum til að bæta samþykktarferli þannig að það hentar fyrirtæki ykkar. Þess vegna er hægt að skilgreina virkt samþykktarskipulag sem hentar mismunandi skýrslugerðarvenslum sem fyrirtækið notar.</td>
</tr>
<tr>
<td>Verkflæðisstuðningur til að færa inn persónuleg kennisnúmer (PIN-númer) á sjálfsafgreiðslusíðum Starfsmanna.</td>
<td>Verkflæðisgeta mannauðs (Mannauður) hefur verið útvíkkuð og inniheldur nú þjónustudeild fyrir PIN-númer. Starfsmenn geta bætt við og breytt PIN-númerum sínum til að bæta skilvirkni. Hins vegar geta MA-starfsmenn yfirfarið þessar upplýsingar fyrir nákvæmni og heilleika áður en þeim er bætt við færslu starfsmanns.</td>
</tr>
<tr>
<td>Stofna markmiðssnið og nota þau til að bæta við nýjum markmiðum.</td>
<td>Hægt er að stofna markmiðssnið fyrir markmið sem eru samnýtt af mörgum starfsmönnum í fyrirtækinu. Starfsmenn bæta við sínum markmiðum úr sniðmáti, stjórnendur geta bætt við markmiðum fyrir sín teymi úr sniðmáti og teymismeðlimir MA geta bætt við markmiðum fyrir starfsmenn þvert á fyrirtækið.</td>
</tr>
<tr>
<td>Stofna markmiðahópa nota þá til að bæta við nýjum markmiðum.</td>
<td>Hægt er að bæta við markmiðssniðum við hóp og nota hann til að stofna eitt eða fleiri markmið fyrir starfsmann, teymi, stöðu, deild eða fyrirtæki.</td>
</tr>
<tr>
<td>Hafa meiri stjórn yfir endurskoðunarferlinu.</td>
<td>Hægt er að nota verkflæði til að stýra endurskoðunarferlinu. Hægt er að stofna sniðmát fyrir yfirferð og nota þau til að stofna yfirferðir. Einnig er hægt að bæta við einkunnum til að skoða.</td>
</tr>
<tr>
<td>Nota endurskoðunartímabil til að skilgreina tímaramma fyrir yfirferð.</td>
<td>Hægt er að skilgreina tímabil fyrir frammistöðumat og upphafs- og lokadagsetningar yfirferðar eru sjálfkrafa færðar inn. Hins vegar er hægt að breyta þessum sjálfgefnu dagsetningum eftir þörfum.</td>
</tr>
<tr>
<td>Opna fimm nýja Power BI efnispakka fyrir mannauð</td>
<td>Nýju efnispakkarnir gera mannauðsfyrirtækjum og mannauðsstjórum kleift að greina eftirfarandi:
<p>Mælikvarðar vinnuafls</p>
<ul>
<li>Lýðfræðileg sundurliðun eftir aldri, kyni og hjúskaparstöðu</li>
<li>Bera saman brottfallstíðni frá ári til árs og sjá lista yfir ástæður sem starfsfólk gefur fyrir því að hætta hjá fyrirtækinu</li>
<li>Skoða lista yfir opnar stöður, ásamt samanburði á opnum og lokuðum stöðum</li>
</ul>
<p>Laun og fríðindi</p>
<ul>
<li>Bera saman starfsfólk á tímakaupi og föstum launum</li>
<li>Skoða fjölda starfsmanna sem eru skráðir í tiltæk fríðindi</li>
<li>Skoða starfsmenn eftir tegund starfs</li>
</ul>
<p>Ráðning</p>
<ul>
<li>Greina umsækjendur út frá fjölda umsækjenda, hvaðan þeir koma og hvaða stöður þeir sækja um</li>
</ul>
<p>Fyrirtækjaþjálfun</p>
<ul>
<li>Námskeiðsskráning eftir staðsetningu</li>
<li>Viðvera á námskeiði eftir stöðu</li>
<li>Listi yfir starfsmenn sem eru skráðir á námskeið</li>
</ul>
<p>Hæfni og þróun starfsmanns</p>
<ul>
<li>Listi yfir hæfni sem starfsmenn búa yfir</li>
<li>Sundurliðun á hæfnistegundum hópmeðlims</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="localizations"></a>Staðfæringar

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Staðfæringar eru tiltækar fyrir 18 önnur lönd:
<ul>
<li>Austurríki</li>
<li>Belgía</li>
<li>Brasilía</li>
<li>Kína</li>
<li>Tékkland</li>
<li>Eistland</li>
<li>Finnland</li>
<li>Ungverjaland</li>
<li>Ítalía</li>
<li>Lettland</li>
<li>Litháen</li>
<li>Noregur</li>
<li>Pólland</li>
<li>Sádi-Arabía</li>
<li>Spánn</li>
<li>Svíþjóð</li>
<li>Sviss</li>
<li>Taíland</li>
</ul>
<p>Eftirfarandi lönd krefjast einnig staðfærslu Smásölu. Staðfærslu smásölu fyrir þessi lönd hefur ekki verið lokið og er áætluð aðeins fyrir H1 CY2017:</p>
<ul>
<li>Brasilía</li>
<li>Tékkland</li>
<li>Eistland</li>
<li>Ungverjaland</li>
<li>Lettland</li>
<li>Litháen</li>
<li>Malasía</li>
<li>Pólland</li>
<li>Svíþjóð</li>
</ul>
</td>
<td>Dynamics 365 for Operations er tiltækt í 18 öðrum löndum. Hluti af framlagi okkar til að gera staðfærslu auðveldari og skilgreinanlegri er að eiginleikum reglubundinnar rafrænnar skýrslugerðar hefur verið umbreytt í skilgreiningar Rafrænnar skýrslugerðar (ER) og sumum reglubundnum Microsoft SQL Server Reporting Services (SSRS) skýrslum hefur verið umbreytt í ER skilgreiningar sem nota Excel-sniðmát. Þessar aðgerðir eru sérstaklega nefndar síðar í þessari töflu.</td>
</tr>
<tr>
<td>Japan – Flokka eignir þegar skjámynd 26 og fylgjandi töflur hennar eru prentaðar.</td>
<td>Skjámynd 26 þarf að senda til hverrar borgar þar sem fyrirtækið starfar. Til að spara þér vinnu þegar skjámynd 26 er prentuð, er hægt að flokka eignir sjálfvirkt og raða þeim eftir staðsetningu.</td>
</tr>
<tr>
<td>Japan – Sjá upphæðir fyrir hraðaða og viðbótarafskrift á forstillingunni.</td>
<td>Forstillingarnar geta veitt nákvæmt mat á upphæðum fyrir hraðaða og viðbótar afskrift.</td>
</tr>
<tr>
<td>Japan – Reikna staðgreiðsluskatt jafnt og þétt.</td>
<td>Japönsk stjórnvöld krefjast þess að staðgreiðsluskattur sé reiknaður jafnt og þétt, byggt á upphæð greiðslu.</td>
</tr>
<tr>
<td>Japan – Flytja inn póstnúmeraskrá fyrir tilteknar stórar fyrirtækjabyggingar.</td>
<td>Hægt er að flytja póstnúmeraskrá sem yfirvöld veita fyrir tilteknar stórar fyrirtækjabyggingar inn í kerfið. Síðan er hægt að afleiða aðsetur af póstnúmerum.</td>
</tr>
<tr>
<td>Japan – Skilgreina aðgerðalaust tímabil fyrir eignir.</td>
<td>Aðgerðalaus tímabil leyfa notandanum að gera hlé á afskriftum eigna á tilteknu tímabili. Þessarar virkni er krafist af reglugerðinni.</td>
</tr>
<tr>
<td>Evrópa – Skilgreina skráningarnúmer virðisaukaskattsins (VSK) fyrir aðsetur aðila með skráningarramma auðkenna.</td>
<td>Hægt er að skilgreina VSK-skráningarnúmer fyrir aðsetur aðila með því að nota skráningarramma auðkenna og nýjan skráningarflokk <strong>VSK-númers</strong>.</td>
</tr>
<tr>
<td>Finnland – Skilgreina tollnúmer viðskiptavinar fyrir aðsetur aðila með því að nota skráningarramma auðkenna.</td>
<td>Hægt er að skilgreina tollnúmer viðskiptavinar fyrir aðsetur aðila með því að nota skráningarramma auðkenna og nýjan skráningarflokk <strong>Tollnúmer viðskiptavinar</strong>.</td>
</tr>
<tr>
<td>Frakkland – Prenta reikninga viðskiptavina með sniði sem er tiltekið í Frakklandi.</td>
<td>Útprentun á reikningi viðskiptavinar er leiðrétt til að uppfylla sértækar kröfur Frakklands.</td>
</tr>
<tr>
<td>Frakkland – Framfylgja samhangandi númeraröð skjala eftir fjárhagstímabili.</td>
<td>Til að uppfylla sértækum kröfum Frakklands fyrir tölusetningu reikninga viðskiptavina, er hægt að setja upp númeraraðir fyrir reikninga viðskiptavina fyrir hvert fjárhagstímabil.</td>
</tr>
<tr>
<td>Austurrísk staðfæring – ER skilgreiningar</td>
<td>
<ul>
<li>Austurrískur ESB-sölulisti - XML-snið</li>
<li>Intrastat-snið fyrir Austurríki</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Austurríki</li>
<li>ISO20022 Beingreiðslusnið fyrir Austurríki</li>
<li>Austurrískt snið EDIFACT-PAYMUL</li>
<li>Vsk-skýrsla fyrir Austurríki</li>
</ul>
</td>
</tr>
<tr>
<td>Belgíst staðfæring – ER skilgreiningar</td>
<td>
<ul>
<li>BLWI-snið fyrir Belgíu</li>
<li>ESB-sölulisti - XML-snið fyrir Belgíu</li>
<li>Eignaskýrsla fyrir Belgíu</li>
<li>Intervat-snið fyrir Belgíu</li>
<li>Intrastat-snið fyrir Belgíu</li>
<li>Veltuskýrsla reikninga fyrir Belgíu</li>
<li>Útflutningssnið fjárhagsfærslu fyrir Belgíu</li>
<li>Swift-greiðslusnið lánardrottins fyrir Belgíu</li>
<li>Innflutningssnið CODA-bankayfirlits fyrir Belgíu</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Belgíu</li>
<li>ISO20022 Beingreiðslusnið fyrir Belgíu</li>
</ul>
</td>
</tr>
<tr>
<td>Brasilísk staðfæring – ER skilgreiningar</td>
<td>
<ul>
<li>GIA SP fyrir Brasilíu</li>
<li>GIA-ST fyrir Brasilíu</li>
</ul>
</td>
</tr>
<tr>
<td>Tékknesk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>XML-snið ESB-sölulista fyrir Tékkland</li>
<li>Intrastat-snið fyrir Tékkland</li>
<li>Vsk-skýrsla fyrir Tékkland</li>
</ul>
</td>
</tr>
<tr>
<td>Kínversk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>Snið aldursskýrslu viðskiptavinar fyrir Kína</li>
<li>Viðskiptavin greiðslu skýrslusniðið analysis upphæð fyrir Kína</li>
<li>Snið Aldursskýrslu lánardrottins fyrir Kína</li>
<li>Snið greiningarskýrslu upphæðar viðskiptavinar til greiðslu fyrir Kína</li>
<li>Snið aldursgreiningar greiddrar fjárkröfu fyrir Kína</li>
<li>Snið stöðuskýrslu viðskiptavinar fyrir Kína</li>
<li>Snið fjárhagslykilsskýrslu fyrir Kína</li>
<li>Snið stöðuskýrslu lánardrottins fyrir Kína</li>
<li>GBT-skrá fyrir Kína</li>
<li>Snið fyrir útflutningsskrá Golden tax</li>
<li>Frávikaskýrslusnið framleiðslunotkunar fyrir Kína</li>
</ul>
</td>
</tr>
<tr>
<td>Eistnest staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>ESB-sölulisti - XML-snið fyrir Eistland</li>
<li>Intrastat-snið fyrir Eistland</li>
<li>Endurflokkun birgðayfirlits fyrir Eistland</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Eistland</li>
<li>Skýrsla tilkynningar um stöðu viðskiptavina fyrir Eistland</li>
<li>Vsk-skýrslu fyrir Eistland</li>
</ul>
</td>
</tr>
<tr>
<td>Finnsk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>ESB-sölulisti - TXT-snið fyrir Finnland</li>
<li>Intrastat-snið fyrir Finnland</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Finnland</li>
</ul>
</td>
</tr>
<tr>
<td>Ungversk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>ESB-sölulisti - XML-snið fyrir Ungverjaland</li>
<li>Intrastat-snið fyrir Ungverjaland</li>
<li>Intrastat-einfaldað snið fyrir Ungverjaland</li>
<li>Útflutningssniðið reikningalistanum fyrir Ungverjaland</li>
<li>Vsk-skýrsla fyrir Ungverjaland</li>
<li>Sundurliður Vsk-skýrsla fyrir Ungverjaland</li>
<li>Birgðayfirlit fyrir Ungverjaland</li>
<li>MultiCash-greiðslusnið fyrir Ungverjaland</li>
</ul>
</td>
</tr>
<tr>
<td>Ítölsk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>Intrastat-snið fyrir Ítalíu</li>
<li>Snið verkreiknings fyrir Ítalíu</li>
<li>Snið sölureiknings fyrir Ítalíu</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Ítalíu</li>
<li>ISO20022 Greiðslusnið beingreiðslu fyrir Ítalíu</li>
<li>Greiðslusnið RIBA-innheimtubréf fyrir Ítalíu</li>
<li>Skýrsla um innlendar skattafærslur fyrir Ítalíu</li>
<li>Bannskýrsla fyrir Ítalíu</li>
<li>Modello770-skýrsla fyrir Ítalíu</li>
<li>Árleg skýrsla um skattsamskipti fyrir Ítalíu</li>
</ul>
</td>
</tr>
<tr>
<td>Lettneskt staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>Notkunarskýrsla fyrir inngreiðslur (LV)</li>
<li>ESB-sölulisti - XML-snið fyrir Lettland</li>
<li>ESB-sölulisti - leiðréttingar á XML-sniði fyrir Lettland</li>
<li>Intrastat-snið (A) fyrir Lettland</li>
<li>Intrastat-snið (B) fyrir Lettland</li>
<li>Talningarlisti birgða fyrir Lettland</li>
<li>Talningaryfirlit birgða fyrir Lettland</li>
<li>Birgðahreyfing fyrir Lettland</li>
<li>Fylgiseðill fyrir innri flutning fyrir Lettland</li>
<li>Endurflokkunarskjal birgða fyrir Lettland</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Lettland</li>
<li>Vsk-skýrslu fyrir Lettland</li>
</ul>
</td>
</tr>
<tr>
<td>Litháísk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>ESB-sölulisti - XML-snið fyrir Litháen</li>
<li>Intrastat-snið fyrir Litháen</li>
<li>Birgðayfirlit fyrir Litháen</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Litháen</li>
<li>Afstemmingarskýrsla milli viðskiptavinar og lánardrottins fyrir Litháen</li>
<li>Vsk-skýrsla fyrir Litháen</li>
</ul>
</td>
</tr>
<tr>
<td>Norsk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>Snið innheimtubréfa fyrir Noreg</li>
<li>AutoGiro-greiðslusnið fyrir Noreg</li>
<li>AvtaleGiro-greiðslusnið viðskiptavinar fyrir Noreg</li>
<li>eFaktura-greiðslusnið viðskiptavinar fyrir Noreg</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Noreg</li>
<li>Greiðslusnið NETS fyrir Noreg</li>
</ul>
</td>
</tr>
<tr>
<td>Pólsk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>Intrastat-snið fyrir Pólland</li>
<li>Vöruhúsafylgiskjöl fyrir Pólland</li>
<li>Endurflokkunarskjal birgða fyrir Pólland</li>
<li>MultiCash-greiðslusnið fyrir Pólland</li>
<li>MultiCash-greiðslusnið erlendra greiðsla fyrir Pólland</li>
<li>Staðfestingarskýrsla um stöðu viðskiptavina fyrir Pólland</li>
</ul>
</td>
</tr>
<tr>
<td>Sádi-Arabísk staðfærsla – ER skilgreiningar</td>
<td>Snið úthlutunar gjalda banka LC fyrir Sádi-Arabíu</td>
</tr>
<tr>
<td>Spænsk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>ESB-sölulisti - TXT-snið fyrir Spán</li>
<li>Intrastat-snið fyrir Spán</li>
<li>Sérsníða verks snið reiknings fyrir Spán</li>
<li>Sérsníða verks snið reiknings fyrir Spán</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Spán</li>
<li>ISO20022 Greiðslusnið beingreiðslu fyrir Spán</li>
<li>Snið spænskrar VSK-skráningarbókar</li>
<li>Snið yfirlits spænskrar VSK-skráningarbókar</li>
<li>Flytja út skýrslu 347 í ASCII fyrir Spán</li>
<li>Skýrsla 347 fyrir Spán</li>
</ul>
</td>
</tr>
<tr>
<td>Sænsk staðfærsla – ER skilgreiningar</td>
<td>
<ul>
<li>Intrastat-snið fyrir Svíþjóð</li>
<li>Bankgirot Autogiro-greiðslusnið viðskiptavinar fyrir Svíþjóð</li>
<li>Bankgirot-snið greiðslna lánardrottins fyrir Svíþjóð</li>
<li>Swift-greiðslusnið lánardrottins fyrir Svíþjóð</li>
<li>SIE-útflutningssnið fyrir Svíþjóð</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Svíþjóð</li>
</ul>
</td>
</tr>
<tr>
<td>Svissnesk staðfærsla – ER skilgrieningar</td>
<td>
<ul>
<li>DebitDirect-greiðslusnið fyrir Sviss</li>
<li>LSV-greiðslusnið beingreiðslu fyrir Sviss</li>
<li>ISO20022 Greiðslusnið kreditfærslu fyrir Sviss</li>
<li>ISO20022 Greiðslusnið beingreiðslu fyrir Sviss</li>
<li>Innflutningssnið ESR-bankayfirlits fyrir Sviss</li>
</ul>
</td>
</tr>
<tr>
<td>Þýskaland – Útflutningur lánardrottnagreiðslna á DTAZV-sniði</td>
<td>Þýskaland krefst DTAZV með erlenda sniðskilgreiningu sem táknar kreditfærslu (lánardrottnagreiðslu) skilaboða samkvæmt tækniskilgreiningu greiðslna fyrir milli landamæra frá Þýskalandi á reikning erlendis eða á banka í Þýskalandi í erlendum gjaldmiðli.</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Rafræn skýrslugerð

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Grunnstilla ER skýrslur til að setja inn gögn, á nokkrum sniðum, úr geymslu Skjalastjórnunar í rafræn skilaboð sem eru mynduð. | Grunnstilltu ER skýrslur til að setja gögn inn í rafræn boð sem eru mynduð úr geymslu Skjalastjórnunar. Þar af leiðandi er hægt að bæta fylgiskjölum viðskiptaskjals við rafræn skilaboð sem eru mynduð fyrir það skjal, í samræmi við lagalegar kröfur. Eins og stendur er hægt að bæta þessum viðhengjum við á MIME-sniði við XML-skilaboð sem eru mynduð. Einnig er hægt að bæta við viðhengjum á Base64-sniði við tvíundakerfis skilaboð sem eru mynduð. |
| Skilgreindu ER-skýrslur til að mynda rafræn skjöl á Excel-, Microsoft Word eða PDF-sniði. | Eina skilgreining gerir ER-skýrslum kleift að mynda rafræn skjöl á þremur mismunandi sniðum: OpenXML-vinnublaðiði (Excel), Word og XML-gagnaeyðublöðum (XFDF) (PDF). Notendur geta valið snið með því að bæta við sniðasniðmáti við ER-skýrslu sem Excel-, Word- eða PDF-skjal. |
| Grunnstilltu ER-skýrslur til að setja gögn inn í síðuhausa og síðufætur rafrænna skjala sem eru mynduð í vinnublaði OpenXML og til að stjórna síðuskilum. | ER-skýrslur geta sett viðskiptagögn inn í síðuhausa og síðufætur og einnig stýrt því hvar síðuskil eru gerð. Þess vegna geta skýrslur stutt fasta efri og neðri hluta fyrir síður í rafræn skjölum sem eru mynduð. Þær geta einnig stutt tiltekið síðuvíxl þessara skjala, þannig að þau samræmist lagaskilyrðum. |
| Skilgreindu áfangastað ER-skýrslna þannig að úttak sé sent sem tölvupóstur og þannig að hægt sé að nota viðskiptagögn og viðskiptagrunninn sem ER-rök (segðir) til að tilgreina á keyrslutíma hvaða netfang eigi að nota. | Áður þegar ER-áfangastaður var skilgreindur, var hægt að skilgreina tölvupóstfang viðtakanda á á hönnunarstigi. Nú er hægt að skilgreina segð á ER-sniði. Síðan er hægt að velja þessa segð á áfangastað sem uppruna tölvupóstfangs fyrir hverja skilgreiningu sniðs og hvern úttaksíhlut (möppu eða skrá) sérstaklega. Þegar ER-skýrsla er í gangi er þess vegna hægt að póstsenda hverja skrá sem er mynduð til mismunandi viðtakanda og hægt er að skilgreina tölvupóstfang samkvæmt ER-rökum og viðskiptagögnum. |
| Skilgreindu áfangastað ER-skýrslna þannig að úttakið sé sent í Microsoft SharePoint-möppu sem annaðhvort ný nefnd skrá eða í nýja útgáfu af fyrirliggjandi skrá og þannig er hægt að nota viðskiptagögn í Microsoft Power BI-ramma sem annaðhvort gagnasafn eða skýrslu. | Þegar ER-skýrslur eru skilgreindar er nú auðveldlega (án kóðunar) hægt að undirbúa umbeðin viðskiptagögn svo að hægt sé að nota þau af ramma Power BI. Þegar þessar ER-skýrslur eru keyrðar er hægt að veita ramma Power BI með viðkomandi viðskiptagögnum og/eða Excel-skýrslum sem þegar eru tiltækar. Ef þú raðar skýrslukeyrslum í reglubundinn ham er hægt að koma á áætluðum sendingum á viðskiptagögnum úr Dynamics 365 for Operations í Power BI til að styðja uppfærsluáætlun á Power BI-skýrslum. |
| Skilgreindu ER-skýrslum til að nota hluta af rafræna skjalinu sem hefur þegar verið myndað sem gagnagjafi til að mynda afganginn af skjalinu. | Hægt er að skilgreina ER-skýrslur sem stofna úttak á textasniði til að gera línutalningu skjals. Síðan er hægt að nota þessar upplýsingar í öðrum hlutum skjalsins til að stofna línur sem innihalda upplýsingar um samantekt. Samantektarupplýsingar (samtölur og númer) er hægt að reikna og prenta á rafrænum skjölum sem eru mynduð án þess að krefjast frekari umbreytingar gagna. Þar af leiðandi eykur þessi eiginleiki afköst skýrslukeyrslu og hjálpar til við að haldi seinni tíma viðhaldi á skilgreindu ER-sniði. |
| Skilgreindu ER-skýrslur til að tilgreina skráarendingu fyrir rafræn skjöl sem eru mynduð á textaformi. | Hægt er að skilgreina ER-skýrslur til að stofna úttak á textasniði, þannig að hægt er að vista það sem skrá sem hefur ákveðinn nafnauka. Auk sjálfgefins .txt nafnauka er hægt að skilgreina nafnauka eins og .csv og .prn, samræmi við sniðlýsingu. |
| Stofnaðu nýjar ER-skýrslur sem byggja á tiltekinni útgáfu ER-líkans. | Áður, þegar nýtt ER-snið var stofnað, var aðeins hægt að nota allra nýjustu útgáfu af völdu ER-líkani sem staðsetningu fyrir gagnaveitu sniðs. Núna er hægt að velja allar tiltækar útgáfur valins ER-líkans. Þessi eiginleiki gerir kleift að vinna með ER-skýrslur núverandi árs og hanna nýja útgáfu ER-líkans fyrir næsta ár samhliða. |
| Leitaðu að gagnagjafa og sniðum/líkönum með texta eða völdum gjörva með einum smelli. Leysa árekstra við endurreikning grunns gagnvirkt og leysa árekstra milli skilgreininga. Skilgreina ER-skýrslur til að stofna mörg villuleitarboð um villur sem fundust áður en skýrslukeyrslan var rofin. | Nokkrar lagfæringar á notandareynslu (UX) í ER-rammanum hjálpa notendum að vinna með ER á skilvirkari og auðveldari hátt. |
| Sýna vinnusvæðið **ER** í Power BI-skýrslum. | Notendur geta skilgreint síðuna **ER-vinnusvæði** þannig að hún innihaldi ný valmyndaratriði og lifandi reiti sem keyra Power BI-skýrslur. |

## <a name="payroll"></a>Laun

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skilgreindu launafærslur og vinnslu launa með því að nota virkni sem er ígildi virkni kerfiseiningarinnar <strong>Laun</strong> í Microsoft Dynamics AX 2012 R3.</td>
<td>Nú er hægt að skilgreina og vinna bandarísk laun með því að nota eiginleikasamstæðu sem er ígildi eiginleikasamstæðunnar í AX 2012 R3.
<ul>
<li>Hægt er að skilgreina greiðsluferli og launatímabil, vinnulotur og vinnutímabil, tekjukóða og flokka tekjukóða, áætlanir, leyfisgerðir og áætlanir vegna uppsafnaðra fríðinda.</li>
<li>Einnig er hægt að setja upp áskilinn frádrátt á bæði fríðindum og sköttum og skrá launaupplýsingar fyrir stöður og starfsmenn vegna skýrslugerðar og greiningar.</li>
<li>Einnig er hægt að setja upp og stjórna frádrætti frá launum og vegna skattheimtu og fyrir öll tengd stjórnsýslugjöld.</li>
</ul>
</td>
</tr>
<tr>
<td>Fylgstu með og keyrðu launatímabilsferlið með því að nota nýja vinnusvæðið <strong>Stjórnun launa</strong>.</td>
<td>Nú er auðveldlega hægt að fylgjast með launavinnslunni. Í fljótu bragði geta launastjórar séð tekju- og launayfirlit sem krefjast athygli þeirra, svo að launakeyrslunni verður lokið og nákvæm. Vinnusvæðið <strong>Stjórnun launa</strong> gerir notendum kleift að fylgjast með og keyra upphafs-til-enda ferlum af einu vinnusvæði.</td>
</tr>
<tr>
<td>Myndaðu jákvæðar greiðsluskrár fyrir launaávísanir.</td>
<td>Það er ný viðbót við jákvæða launavirkni reiðufjár og bankastjórnunar fyrir launagreiðslur. Aðskildum valmyndaratriðum hefur verið bætt við í gegnum kjarnaferli til að virkja einangraða skilgreiningu sem er tiltekin í launum. Virkni er sú sama og kjarnauppsetning jákvæðu aðgerðinni sem var losuð í Microsoft Dynamics AX útgáfu forrits 7.0.1 (maí 2016). Vegna þessa nafnauka eru launagögn alveg einangruð frá afgangnum af jákvæðu færslunum. Þessi aðgreining tryggir að einungis notendur launaskráar fá aðgang að og sjá gögn sem tengjast launaskrá.</td>
</tr>
<tr>
<td>Flyttu inn tekjuyfirlitslínur úr ytri uppruna með því að nota nýja gagnaeiningu tekjuyfirlitslínu.</td>
<td>Mikilvæg ný gagnaeining kveikir samþættingu við ytri tíma og útreikningskerfi tekna. Gagnaeiningin flytur inn tekjuyfirlitslínur og framkvæmir öll sömu sjálfgefnu rök sem notandinn færði beint inn í tekjuyfirlitið. Eftir innflutning eru línurnar sjálfkrafa tengdar við viðeigandi fylgiskjal tekjuyfirlits. Ef fylgiskjal viðeigandi tekjuyfirlits er ekki til staðar er skjal sjálfkrafa stofnað.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Áætlanagerð

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Stilltu sjálfgefnar pantanastillingar fyrir sölu og innkaup samkvæmt öllum virkum afurðarvíddum í afurðarsniðmátinu. Þess vegna er hægt að skilgreina sjálfgefnar pantanastillingar fyrir birgðahaldseiningu (SKU) eða hluta birgðahaldseiningar. | Hægt er að tilgreina sjálfgefnar pantanastillingar sem eiga við afurðarvídd eða samsetningu afurðavídda.<p>**Dæmi**</p><p>Afurð sem nefnist pólóskyrta er seld. Þessi afurð er til í tveimur litum: Bláum og grænum. Hún er einnig er til í tveimur stærðum: Lítil og miðlungs. Litur og Stærð eru virkar afurðarvíddir fyrir pólóskyrtuna. Hægt er að læsa innkaupum á öllum grænum pólóskyrtum, án tillits til stærðar þeirra.</p> |

## <a name="product-master-data"></a>Afurðarsniðmát

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Setja upp sjálfgefnar pantanastillingar og svæðispöntunarstillingum samtímis, frá einni síðu.</td>
<td>Eiginleikinn veitir betra yfirlit yfir stillingar fyrir vöruna.</td>
</tr>
<tr>
<td>Stofnaðu nafnakerfi fyrir númer afurðarsniðmáts.</td>
<td>Hægt er að hafa með einingar eins og afurðavíddir, eiginleika og stafi geta númerum afurðarafbrigða. Þegar stofnuð er sölupöntun eða innkaupapöntun er hægt að finna tiltekið afurðarafbrigðið á fljótlegan hátt.</td>
</tr>
<tr>
<td>Leita að afurðum og afurðarafbrigðum í sölu- og innkaupaaðstæðum.</td>
<td>Þegar sölu- eða innkaupalína er stofnuð er hægt að leita að afurðum með því að nota afurðavíddir og öll afurðarnúmer nema altæk viðskiptanúmer (GTINs) og strikamerki. Þessi leit er full textaleit sem kemur í stað fyrirliggjandi leitarinnar „Byrjar á“ sem er notuð í uppflettilistum sölu og innkaupa. Þessi eiginleiki gerir kleift að finna afurðaflokka sem hafa svipaða eiginleika eða eina afurð sem hefur einkvæm einkenni. Til að kveikja á þessari aðgerð velurðu færibreytuna <strong>Kveikja á uppflettingu fyrir afurðaleit</strong> á síðunni <strong>Leitarfæribreytur</strong>.</td>
</tr>
<tr>
<td>Tilgreindu afurðarafbrigði beint þegar þú stofnar sölu- eða innkaupafærslu. Einnig er hægt að velja í lista yfir gilda víddarsamsetningar.</td>
<td>Þessi eiginleiki er endurbót á framleiðni.
<p><strong>Dæmi</strong></p>
<p>Afurð sem nefnist pólóskyrta er seld. Þessi afurð er til í tveimur litum: Bláum og grænum. Hún er einnig er til í tveimur stærðum: Lítil og miðlungs. Litur og Stærð eru virkar afurðarvíddir fyrir pólóskyrtuna. Þegar færð er inn sölulína fyrir pólóskyrtu sem er í grænum lit og af stærðinni Lítil þarf ekki að færa inn gögn í reitina <strong>Vörunúmer</strong>, <strong>Litur</strong> og <strong>Stærð</strong>. Hægt er að stofna línu með því að fylgja einu af eftirfarandi skrefum:</p>
<ul>
<li>Í reitnum <strong>Vörunúmer</strong> skal færa inn númer afurðarafbrigðis, litagildi eða stærð. Í uppflettingunni finnurðu þá tilgreindu vöruvíddasamsetningu sem á að selja og stofnar sölulínu.</li>
<li>Í reitnum <strong>Vörunúmer</strong> skal færa inn vörunúmerið. Farðu í einhvern reit afurðarvíddar. Í uppflettingunni <strong>Afurðarvídd</strong> mun notandi sjá allar losaðar víddarsamsetningar sem eiga við um pólóskyrtu. Í einu þrepi er hægt að velja afurðarafbrigði sem á að selja.</li>
</ul>
</td>
</tr>
<tr>
<td>Tilgreindu hvort afurðarnúmer birtast á síðum sem tengjast færslum.</td>
<td>Færslusíður, eins og sölupantanir og innkaupapantanir, sýna aðeins reitina <strong>Vörunúmer</strong> og <strong>Afurðarheiti</strong>. Til að sjá reitinn <strong>Afurðarnúmer</strong> skal velja færibreytuna <strong>Sýna afurðarnúmer á skjámyndum</strong> undir <strong>Færibreytur vöruupplýsingastjórnunar</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Verkefnastjórnun og bókhald

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Notaðu Valið síðar þegar verið er að bóka reikningstillögu í runu. | Bókhaldarar verks geta sett upp runuvinnslu til að sækja reikningstillögur sjálfkrafa fyrir bókun, ef þær tillögur uppfylla skilyrðin sem eru tilgreind í runuvinnslunni. Þessi eiginleiki endurbætir sjálfvirkni við bókun reiknings, þar sem runuvinnslan getur keyrt stöðugt og tekur sjálfkrafa upp tillögur fyrir bókun. |
| Búa til greiningar í Power BI skjáborði. | Efni viðskiptaupplýsinga (BI) fyrir verktengd og tilfangatengd gögn má auðveldlega stofna í Power BI skjáborði. |
| Notaðu fyrirframgreiðslur pöntun í innkaupapöntun og hafðu þær réttar í matsferli verkefnisins. | Fyrir innkaupapantanir verks verða fyrirframgreiðslur að vera unnar áður en hægt að losa sumar greiðslur til lánardrottna. Þessir fyrirframgreiðslureikningar birtast núna í verkmati/skráningarferli fyrir verk af gerðinni **Fast verð**. |
| Fá aðgang að og stjórna kostnaði og áætluðum tekjum og vöruþörfum, beint úr sundurliðun verkþátta verks (WBS). | Hægt er að stjórna kostnaðarmati, tekjumati og vöruþörfum fyrir tiltekin WBS-verk í upplýsingaglugganum fyrir það verk í WBS yfirliti áætlana. |
| Sækja fjármögnunaraðila á þóknunarbækur. | Ef samningur fyrir verk inniheldur marga fjármögnunaraðila er hægt að velja einn tiltekinn fjármögnunaraðila þegar gjöldin eru bókuð. Ef ekki er valinn ákveðinn fjármögnunaraðili eru fjármögnunarreglur sem tilgreindar eru í samningnum notaðar til að úthluta þóknun. |
| Opna verkyfirlit í Excel. | Nýjar gagnaeiningar fyrir fjárhagsuppfærslur og áætlunaruppfærslur gera kleift að opna gögn um verkyfirlit í Excel og stofna greiningar með því að nota aðgerðir í Excel. |
| Notaðu aðeins einn skilgreiningarlykill til að virkja aðgerðir fyrir verkefnastjórnun og bókhald (PMA). | Verktengdum skilgreiningarlyklum hefur verið skipt út fyrir einn skilgreiningarlykil verks sem kveikir á PMA-virkni. |

## <a name="retail-and-commerce"></a>Smásala og viðskipti

### <a name="advanced-warehouse-management-in-a-retail-store"></a>Ítarlegt vöruhúsakerfi í smásöluverslun

Smásalar geta notað lausnina Ítarlegt vöruhúsakerfi (WHS) í verslunum sínum og gert nauðsynlegar uppfærslur á aðgerðum gildandi sölustaðar (POS) til að styðja hana. Ferli lófatölvulausnar ættu að virka inni í verslun, eins og þau gera í öllum öðrum vöruhúsum. Öll núverandi birgðaferli smásöluverslunar og öll POS-ferli sem stofna eða uppfæra birgðafærslur eru uppfærð þannig að þau nota sérstakar kröfur fyrir vöruhús með vöruhúsakerfi.

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Notaðu sölustaðinn til að fletta upp tiltækum birgðu í verslunum í vöruhúsakerfi. | Þegar birgðum er flett upp ætti ferlið að vinna á sama hátt og það gerði áður. Uppflettingin ætti nú að sýna tiltækt magn á vöruhúsastigi og ætti ekki að íhuga víddirnar Staðsetningu, Birgðastöðu eða Númeraplötu. |
| Notið POS til að vinna úr innhreyfingarskjali afurða fyrir innkaupapöntun í verslun í vöruhúsakerfi. | Hægt er að móttaka flutningspantanir á sölustaðnum fyrir verslanir og vörur í vöruhúsakerfi. Notandinn ætti að geta valið staðsetningar til móttöku og ætti að geta fært inn kenni númeraplötu til að fylla sjálfkrafa út í móttökulínur. |
| Notið POS til að vinna úr innhreyfingarskjali afurða fyrir innkaupapöntun í verslun í vöruhúsakerfi. | Hægt er að móttaka flutningstillögur á sölustaðnum fyrir verslun og vörur í vöruhúsakerfi. Notandinn ætti að geta valið staðsetningar til móttöku og ætti að geta fært inn kenni númeraplötu til að fylla sjálfkrafa út í móttökulínur. |
| Nota sölustaðinn til að vinna úr sendingu afurða úr verslun í vöruhúsakerfi. | Hægt er að móttaka millifærslur á sölustaðnum fyrir verslun og vörur í vöruhúsakerfi. Notandinn ætti að geta valið staðsetningar til að senda frá, birgðastöðu á að vera sjálfkrafa mynduð og hunsa á númeraplötur. |

### <a name="enable-seamless-omni-channel-commerce"></a>Virkja snurðulaus viðskipti omni-rásar

Snurðulaus viðskipti omni-rásar vísar til stjórnunar og vinnslu pantana í verslunarhúsnæði, netverslununum, símaveri og viðskiptum í gegnum farsíma. Fyrir þessa útgáfu hafa eftirfarandi fjárfestingar verið gerðar á þessu svæði:

- Endurbætur á birtingu fyrir verslanir með rafræn viðskipti
- Nýtt neytendavænt farsímaforrit sem auðveldar notanda að finna rétta afurð, stjórnun lykils og verslun á netinu

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Neytandi: Gildandi útgáfa af neytendavænu farsímaforriti auðveldar eftirfarandi aðgerðir - afurðaleit, fletting í tegund, bæta við innkaupakörfu og gestaútskráningu. Smásalar geta einnig notað sitt eigið fyrirtækjavörumerki í forritinu og pakkað því síðan fyrir Android og iOS forritsverslanir. | Smásalar geta auðveldlega stofnað neytendavæn forrit sem gera viðskiptavinum þeirra kleift að fletta, leita að afurðum og senda afurðir sem gestur úr farsímum sínum. |
| Óskalistar viðskiptavina fyrir c‑commerce netverslanir | Óháðir lánardrottnar (ISVs) geta notað óskalistastjórn til að leyfa notendum að stofna og stjórna mörgum listum birtir í netbúðarglugga sínum og skoða/nota þessa lista á sölustaðnum. |
| Ósamstillt stofnun viðskiptavinar gegnum búðarglugga netverslunar | ISVs getur nú stofnað viðskiptavinalykla jafnvel þegar Commerce Data Exchange: Real-time Service er ekki tiltækt. |
| Birta rásarafurðir frá smásöluþjóni til verslunar þriðja aðila. | Smásöluþjónn styður nú sannvottun þjónustu-til-þjónustu. ISVs getur nýtt útgáfu rásarafurðar frá smásöluþjóni til búðarglugga þriðja aðila. |

### <a name="extensibility"></a>Stækkunarhæfni

- Commerce-keyrslutímaverk eru nú innsigluð úr Retail SDK.
- Auðveldari uppsetning og viðhald gegnum íhlutavædda Microsoft íhlutapakka og ISV-pakka fyrir sölustaði, smásöluþjón, gagnagrunna, greiðslu og vélbúnað.

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| CRT/smásöluþjónn: Smásalar eða ISVs geta útvíkkað CRT gegnum nafnaukakróka. Breytingar á innbyggðum kóðum eru ekki studdar lengur. | Til að virkja samfellda samþættingu og samfellda uppsetningu þarf að sneiða algjörlega hjá breytingum á innbyggðum kóða. Einnig til að styðja auðvelda upptöku á bráðabót án neinnar kóðasameiningar og virkjun CRT þátta. |

### <a name="personalized-product-recommendations"></a>Sérsniðnar afurðaráðleggingar

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Skoða leiðbeiningar sérsniðinnar afurðar á mörgum snertipunktum á sölustað (POS) til að ákvarða hvaða viðskiptavinur gæti haft áhuga á grundvelli innkaupaferla viðskiptavina, vara á óskalista og vara sem aðrir viðskiptavinir keyptu á netinu og í verslunum í verslunarhúsnæði | Fyrir smásala með stóra vörulista hjálpa sérsniðnar ráðleggingar viðskiptavinum með afurðaleit og virkja starfsmenn verslunarinnar með snjallri biðlaraþjónustu. Með því að sýna afurðir sem miðast við áhugamál viðskiptavinarins og innkaupavenjur geta vöruráðleggingar aðstoðað smásala við viðbótarsölu og hægt er að auka varðveislu viðskiptavina. Í Retail eru vöruráðleggingar keyrðar af vitsmunaþjónustu og Microsoft Azure vélnámi. |

### <a name="pos-task-recorder"></a>Verkskráning sölustaðar

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Smásalar geta notað verkskráningu sölustaðar til að framleiða þjálfunarefni, skýringarmyndir viðskiptaferlisvinnu (BPM), og mynda hjálparefni til að auka framleiðni og gera betri greiningu og hönnun forrita. | Til að virkja samfellda samþættingu og samfellda uppsetningu þarf að sneiða algjörlega hjá breytingum á innbyggðu. Einnig til að styðja auðvelda upptöku á bráðabót án neinnar kóðasameiningar og virkjun CRT þátta. |
| Rauntímahjálp á sölustað. | Gjaldkeri/Stjórnandi getur fengið rauntímahjálp frá POS með viðskiptaferli án þess að skipta samhengi. |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Verslunarkerfið: Útvegar snurðulausa verslunarreynslu í verslunarhúsnæði

Verslunarkerfið er uppsetningarval fyrir smásala sem hjálpar til við að keyra safn verslunaraðgerðir, hvort sem það er í sjálfri versluninni, almennu skýi Microsoft eða einkaskýi viðskiptavina. Fyrir þessa útgáfu er gildissviðið aðeins í verslun. Til að styðja betur umhverfi sem hefur hæga og óáreiðanlega nettengingu verðum við að veita valkost fyrir smásala til að nota gagnagrunn rásar og smásöluþjón í versluninni. Síðan geta þeir haldið áfram að keyra kjarnauppsetningu á viðskiptaaðstæðum sínum þó að engar tengingar séu við höfuðstöðvarnar. Byggt á mismunandi gagnapunktum, sem innihéldu umræður í verkfræðingateymi, niðurstöður úr viðskiptavinakönnunum og greiningu á keppinautnum, höfum við auðkennt eftirfarandi lausnarsvið sem tilvalda lausn fyrir okkar markþýði viðskiptavina:

- Sjálfsafgreiðslupakki er tiltækur fyrir verslunarkerfið.
- Sjálfgefin uppsetning er eins reits virkjun en sérsniðin virkjun leyfist.
- Virkja auðvelda virkjun/sjálfsafgreiðslu.
- Smásöluþjónn og gagnagrunnur verslunar eru í versluninni, ásamt Async Client þjónustu.
- Smásöluþjónn verslunarinnar hefur bein samskipti við Þjón hugbúnaðarhluta (AOS) í höfuðstöðvum fyrir verslunarkerfið.
- Styðja aðstæður milli afgreiðslustöðva þar sem engin tenging er við höfuðstöðvar.
- Retail Modern POS og Cloud POS hafa alltaf samskipti við smásöluþjón í versluninni.
- Styðja Retail Modern POS og Cloud POS þar sem engin tenging er við höfuðstöðvar.
- Styðja Retail Modern POS – tiltekin ótengdum gagnagrunni (einangra þá við hvert tilvik Retail Modern POS) þar sem engin tenging er við höfuðstöðvar.
- Sannvottun er byggð á þjónustu-til-þjónustu sem er aðeins fyrir verslunarkerfið.
- Köll Real-time Service eru ekki studd ef engin nettenging er til staðar.
- Bein tengigeta gagnagrunns Retail Modern POS við gagnagrunn rásar er ekki studd.
- Virkja fjarmælingu/eftirlit.

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Smásali hleður niður sjálfsafgreiðslu uppsetningarforriti verslunarkerfisins af síðu gagnagrunns rásar í Dynamics AX HQ og hleður niður í skilgreiningarskránni. | Smásalinn getur snurðulaust sótt sjálfsafgreiðslupakka. |
| Smásalinn setur upp verslunarkerfið með sjálfsafgreiðslu uppsetningarforritinu. | Smásaliinn getur sett upp verslunarkerfið með sjálfsafgreiðslupakkanum. |
| Tæknistjóri stillir verslunarkerfið Dynamics 365 for Operations (gagnagrunnsrás, rásarforstilling, verslun og virkjanlegir pakkar). | Tæknistjóri getur skilgreint verslunarkerfið auðveldlega og skilvirkt. |
| Smásali keyrir Retail Modern POS í verslunarhúsnæðinu og getur gert rauntíma aðgerðir, eins og gefa út gjafakort þegar tenging er til staðar. | Smásalinn getur framkvæmt rauntíma aðgerðir úr verslunarkerfinu þegar tenging er til staðar. |
| Smásali getur samstillt gögn úr verslunarkerfinu við höfuðstöðvar þegar tenging er til staðar. | Smásalinn getur samstillt við verslunarkerfi þegar tenging er til staðar. |
| Smásali getur átt örugg samskipti á milli verslunarkerfisins og höfuðstöðva. | Smásalinn getur átt örugg samskipti úr verslunarkerfinu þegar tenging er til staðar. |
| Tæknistjóri og Microsoft Operations geta fylgst með og gefið skýrslur um verslunarkerfið í verslunarhúsnæðinu (greint og gefið skýrslu um breytingar). | Tæknistjóri og Microsoft Operations geta fylgst með verslunarkerfinu á öruggan hátt og úrræðaleitað á skilvirkan hátt. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Altækur verkvangur Windows forrits fyrir Retail Modern POS

Eins og stendur er Retail Modern POS aðeins tiltækt sem Windows 8.1 forrit fyrir borðtölvur og spjaldtölvur og sem Cloud POS fyrir vafra borðtölvu eða spjaldtölvu. Í þessari útgáfu er Moderns Retail POS umreiknað í Altækan verkvang Windows (UWP) forrits. Þessi breyting mun gera Retail Modern POS kleift að keyra á öllum Windows 10-tækjum (borðtölvu, spjaldtölfu eða síma) og skipta jafnvel á milli yfirlita fyrir tæki í Continuum.

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Virkja mikilvæga virkni sölustaðar fyrir tæki með lítinn skjá. | Virkni Retail POS er tiltæk fyrir síma og önnur tæki með lítinn skjá sem keyra Windows-10. |

## <a name="supply-chain-management"></a>Afgreiðslustjórnun

### <a name="consignment-inventory"></a>Vörusendingarbirgðir

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Sem lánardrottinn geturðu geymt hráefni í vöruhúsi viðskiptavinar. Sem viðskiptavinur geturðu frestað raunverulegum innkaupum þar til að hráefnin eru nauðsynleg fyrir framleiðsluna. | Geymsla birgða með hráefni getur falið í sér gríðarlegan kostnað. Með því að nota vörusendingarbirgðir getur lánardrottinn geymt hráefni í vöruhúsi viðskiptavinar. Viðskiptavinurinn getur síðan frestað raunverulegum innkaupum þar til að hráefnin eru nauðsynleg fyrir framleiðsluna. Hráefni er pantað og móttekið með áfyllingarpöntun vörusendingar. Þessi áfyllingarpöntun skráir efnislegar færslur en hefur ekki áhrif á fjárhag. Til að greina á milli birgðavara í eigu viðskiptavinar og lánardrottins er hægt að nota birgðavídd Eiganda. Breytingar á eignarhaldi á birgðum er meðhöndlaðar af færslubókarferli sem sér um flutning á eignarhaldi hráefnis úr birgðum í eigu lánardrottins í eigu viðskiptavinar birgðir. Þetta ferli ræsir stofnun innkaupapöntunar og innhreyfingarskjal afurða.<blockquote>[!NOTE] Þessi eiginleiki takmarkast við vörusendingar hráefna til framleiðslu á innleið. Hann er ekki samþættur við vöruhúsakerfi (WHS) og flutningsstjórnun (TMS).</blockquote> |
| Sem lánardrottinn sækirðu upplýsingar um upphæð sendra birgða sem eru fluttar til viðskiptavinar. | Til að senda viðskiptavini reikning krefst lánardrottinn upplýsinga um hráefnið sem var keypt frá vörusendingarbirgðum og dagsetningu innkaupapöntunar. Lánardrottinn getur einnig að fylgst með lagerbirgðum á svæði viðskiptavinar með því að nota viðmót samvinnusvæðis lánardrottins. |
| Færðu birgðir í eigu lánardrottins með því að nota flutningabók. | Til að rekja efnislega stöðu birgða í eigu lánardrottins verður notandi að geta skráð stöðu í kerfið. Með því að nota nota flutningabók er hægt að skrá efnislega hreyfingu á birgðum, eins og hreyfingu af einni staðsetningu í vöruhúsi á aðra staðsetningu í sama vöruhúsi. |
| Leiðrétta birgðir í eigu lánardrottins með því að nota flutningabók. | Mikilvægt er að geyma lagerbirgðir kerfisins í samræmi við raunverulegar efnislegar birgðir. Birgðir í eigu lánardrottins má leiðrétta inn og út með með talningarferlum eins og magnleiðréttingu og færslubókarferli talningar. |
| Lestu meira um stuðning við vörusendingar í Dynamics 365 for Operations | Frekari upplýsingar um stuðning við ferli vörusendingar er að finna í [Vörusendingu](../../../supply-chain/inventory/consignment.md), [Uppsetningu vörusendingar](../../../supply-chain/inventory/set-up-consignment.md), [Stofna áfyllingarpöntun vörusendingar (Verkefnaleiðbeiningar)](../../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) og [Skipta um eignarhald á vörusendingabirgðum byggð á framleiðslueftirspurn (Verkefnaleiðbeiningar)](../../../supply-chain/inventory/tasks/change-ownership-consignment.md). |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Samstarf lánardrottna (áður kallað Gátt lánardrottins)

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Gera lánardrottnum mögulegt að bregðast við hverri innkaupalínu og leggja til breytingar. | Í sumum tilfellum vilja lánardrottnar samþykkja sumar innkaupapöntunarlínur en hafna öðrum. Lánardrottnar geta nú sérstaklega stjórnað innkaupapöntunarlínum. Hægt er að hafna hverri einustu línu, samþykkja hana eða samþykkja með breytingum. Til dæmis geta lánardrottnar breytt afhendingardagsetningu, skipt afhendingu og magni eða stungið upp á annarri vöru. |
| Gera lánardrottnum mögulegt að stjórna upplýsingum um tengilið. | Lánardrottnar geta viðhaldið upplýsingum um tengilið um fyrirtæki þeirra. Þessar upplýsingar innihalda nöfn, tölvupóstaðsetur og símanúmer. Aðgangur að þessari aðgerð er veittur með sérnýttu öryggishlutverki. |
| Deila skjölum sem tengjast innkaupapöntunum með lánardrottna. | Þegar samnýta þarf skjal með lánardrottni, s.s. skjal um þarfir, er handhægt að tengja skjalið við viðeigandi innkaupapöntun. Lánardrottinn getur síðan deilt athugasemdum og viðhengjum með viðskiptavinum með því að tengja skjalið við svar hans eða hennar við innkaupapöntun. Skjalastjórnun er undirliggjandi stuðningsrammi og aðeins er hægt að deila athugasemdum og viðhengjum sem eru flokkuð sem „ytri“ með lánardrottnum. |
| Ráðstafa nýjum notendum lánardrottins. | Ef lánardrottnarnir nota viðmót samvinnusvæðis lánardrottins hafa þeir snurðulausa leið til að biðja um nýja notendareikninga þegar nýir tengiliðir þarfnast aðgangs að samvinnusvæði lánardrottins. Sérfræðingar í innkaupum geta sent inn beiðni um notendareikning tengiliðs við fyrirtæki lánardrottins. Tengiliður lánardrottins sem er þegar notandi á samvinnusvæði lánardrottins getur líka sent þessa gerð beiðni. Þessi beiðni býr að lokum til nýjan notanda í Dynamics 365 for Operations sem er með öryggishlutverk tiltekins lánardrottins. Það auðveldar einnig beiðni til gáttar Microsoft Azure B2B um að veita notanda nýjan Azure Active Directory (Azure AD) notandareikning. Lánardrottnar geta einnig beðið um að tilgreindir lánardrottnalyklar notanda séu gerðir óvirkir eða að öryggishlutverkum sé breytt. |
| Fræðast nánar um stuðning við samstarf lánardrottna í Dynamics 365 for Operations. | Nánari upplýsingar um samstarf lánardrottna er að finna á [Samvinnusvæði lánardrottins við ytri lánardrottna](../../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Samvinnusvæði lánardrottins við viðskiptavini](../../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Stjórna notendum samvinnusvæðis lánardrottins](../../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Setja upp og viðhalda samvinnusvæði lánardrottins](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) og [Reikningsfærsluvinnusvæði lánardrottins](../../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). |

### <a name="intercompany-order-processing"></a>Vinnsla samstæðusölupöntunar

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skilgreindu beint í sölupöntunarlínum, hvaðan eftirspurnin ætti að koma og hvernig uppruni hennar á að vera.
<p><strong>Dæmi</strong></p>
<p>Stofna sölupöntunarlínu og tilgreina beinar afhendingar sem afhendingargerð. Aðallánardrottni er bætt við sölupöntunarlínu sem tímapunkti uppruna.</p>
</td>
<td>Flæði fyrir pöntun hefur verið bætt heilmikið. Núna er hægt að skilgreina, beint í sölupöntunarlínum, hvaðan eftirspurnin ætti að koma og hvernig uppruni hennar á að vera. Ekki þarf lengur að bíða þar til að öllum línum hefur verið bætt við sölupöntunina. Nýir valkostir á sölupöntunarlínum gera kleift að tilgreina afhendingargerð þegar lánardrottinn er tilgreindur. Þegar lánardrottinn er tengdur við sölupöntunarlínur eru pöntunarkeðjur stofnaðar fyrir afhendingu frá lánardrottni.
<ul>
<li>Lánardrottinn getur verið samstæðulánardrottinn sem notar innri innkaupapöntun og sölupöntun eða ytri lánardrottinn sem notar ytri innkaupapöntun.</li>
<li>Afhendingargerðin getur verið <strong>Bein afhending</strong> eða <strong>Lager</strong>. Afhendingargerðin <strong>Lager</strong> gefur til kynna að lánardrottinn á að afhenda í staðbundnar birgðir áður en sent er til viðskiptavinarins.</li>
</ul>
</td>
</tr>
<tr>
<td>Stofna pöntunarloforð beint úr sölupöntunarlínum.
<p><strong>Dæmi</strong></p>
<p>Stofnaðu sölupöntunarlínuna sem á uppruna frá lánardrottni í samstæðu. Farðu úr línunni. Afhendingardagsetningar eru reiknaðar út eftir tiltæki í upprunafyrirtækinu.</p>
</td>
<td>Þegar stofnaðar eru sölupöntunarlínur sem nota nýjar upprunaupplýsingarnar eru afhendingar reiknaðar samkvæmt stýringunni <strong>Afhendingardagsetningu</strong>. T.d. ef samstæðulánardrottinn er valinn er tiltækileiki í upprunafyrirtækinu reiknaður. Á þennan hátt eru pöntunarkeðjur sjálfkrafa stofnaðar, ásamt sölupöntunarlínum. Þessi virkni hjálpar til við að tryggja að afhendingardagsetningar verði sýnilegar í upprunafyrirtækinu, þannig að forstillingar tiltækt-til-loforðs (ATP) ráða við áætlaðar kröfur umleið og sölupantanir eru stofnaðar.</td>
</tr>
<tr>
<td>Yfirfarðu afurðir þvert á allar upprunastaðsetningar og veldu besta upprunavalkostinn.</td>
<td>Síðan <strong>Valkostir afhendinga</strong> hefur verið endurhönnuð og veitir nú mikilvægar upplýsingar um alla samþykkta innri og ytri lánardrottna. Þessar upplýsingar innihalda einnig upprunavalkosti fyrir innkaup lánardrottins. Þegar afhendingarmáti er valinn reiknar kerfið út hentugar afhendingardagsetningar. Hægt er að velja snurðulaust besta valkostinn fyrir viðskiptavininn og nota þennan valkost í hverri sölupöntunarlínu.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Vöruhúsaviðbætur fyrir dreifingarstöðvar með miklu magni

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Stofna vinnu eftir að vörum hefur verið pakkað á pökkunarstöð. | Þessi aðgerð er gagnleg þegar fleiri ferli eru eftir handvirka pökkunarvinnu (eins og að setja á bretti, gæðaeftirlit, sameiningu sendingar eða breytingar á hleðsluhöfnum). Nýja vinnutegundin **Tiltekt pakkaðs geymis** gerir kleift að móta þessi verk með því að nota aðskildar vinnulínur. Núna er hægt að móta pökkunarstöðvar til að mynda vinnu eftir pökkun. Þetta verk er hægt að nota til að skipuleggja hreyfingar pakkaðra birgða. |
| Flokka gáma á pökkunarstöð. | Þessi aðgerð gerir kleift að flokka marga pakka í einn gám eða númeraplötu á pökkunarstöðinni. Til dæmis getur stjórnandi netverslunar/heildsölu flokkað 100 sérpakkaða pakka í einn og sama gáminn (t.d. á bretti eða kví). Þennan gám er síðan hægt að flytja, stigbinda eða hlaða með einum vinnustaðafyrirmælum sem starfsmaður myndar með því að skanna eitt strikamerki (númeraplötu) fyrir flokkaða gáminn. Eiginleikinn dregur úr vinnufærslum fyrir flutning á mörgum minni pökkuðum gámum. Nánari upplýsingar er að finna í [Stofna valmyndaratriði fartækis fyrir samstæðu númeraplötu (verkleiðbeiningar)](../../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md). |
| Stofna reglur um losun fyrir pakkaða gáma. | Vinna sem er kveikt með því að losa gáma er hægt að stofna sem annaðhvort sjálfvirka eða handvirka. Þegar vinna er sjálfvirk er hún mynduð við lokun gáms með notkun staðsetningarleiðbeininga og ramma vinnusniðmáts. Þegar losun er handvirk getur pökkunarmaður ákveðið hvort mynda eigi vinnu fyrir einn gám eða fyrir hóp af gámum. Þessi eiginleiki dregur úr þeirri áhættu að lokaðir gámar verði teknir til og fluttir áður en þeir eru tilbúnir til flutnings af pökkunarstöðini. Hún leyfir einnig ókerfisstýrða flokkunarlosun. |
| Endurúthlutun stutttínslu | Stuðningi hefur verið bætt við fyrir ferli stutttínslu til að aðstoða samstarfsaðila sem getur ekki tekið til vörur og vill framfylgja pöntun þegar vara sem krafist er býðst á annarr staðsetningu. Hægt er að nota sjálfvirkt ferli endurúthlutunar sem notar sömu staðsetningarleiðbeiningar til að sækja vörur ef þær eru tiltækar á annarri staðsetningu. Einnig, þegar handvirk endurúthlutun er notuð, sýnir farsíminn lista yfir staðsetningar ásamt tiltæku magni. Starfsmaður í vöruhúsi getur síðan valið hvaða staðsetningar á að nota birgðir úr. Þessar tvær aðferðir er hægt að stilla sérstaklega eða sameina sem eina skipun í valmynd vöruhúsastarfsmanns. Þegar handvirk endurúthlutun er notuð getur starfsmaður vöruhússins tekið til stutttínt magn vörunnar af nokkrum staðsetningum. Frekari upplýsingar eru í [Setja upp endurúthlutun fyrir vöru með of litla tiltekt (Verkefnaleiðbeiningar)](../../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md). |
| Flyttu birgðir með tengdri vinnu. | Núna er hægt að flytja birgðir með tengdri vinnu. Þessi eiginleiki getur verið gagnlegur ef starfsmaður vill til dæmis starfsmaður hreinsa sum pláss innhliðar og flytja skráð bretti sem bíða eftir frágangi á aðra staðsetningu á innleið. Hliðið er hreinsað og getur tekið á móti fleiri vörum hleðslu og birgðir sem hafa verið fluttar eru uppfærðar með nýjum frágangsupplýsingum. Einnig er hægt að nota þessa aðgerð til að losa rými á tiltektarstaðsetningum með því að færa birgðir sem hafa tengda vinnu og stofna pláss fyrir áfyllingu. Hægt er að nota hana til að færa hleðslu af einni sviðsetningarstaðsetningu á aðra án þess að glata hleðslu vinnu sem hefur verið mynduð. Á þennan hátt getur eiginleikinn aðstoðað við stillingu tímans sem þarf til að hlaða vörubifreiðar þegar þær koma. Hægt er að færa birgðir sem hafa verið teknar frá fyrir sölupantanir, vandamál flutningspantana, móttöku flutningspantana og innkaupapantanir. Hreyfing er hindruð ef hún veldur því að línur skiptist. T.d. ef þú ert með vinnulínu fyrir 100 stykki vöru er ekki hægt að færa einungis 30 stykki þeirrar vöru á aðra staðsetningu. |
| Sameina númeraplötur sem eru með vinnu sem tengist þeim. | Hægt er að sameina númeraplötur sem eru með vinnu sem tengist þeim. Til dæmis þegar tiltekt hefur verið brotin niður í nokkur stykki vinnu getur verið gagnlegt að leyfa að númeraplötur séu sameinaðar eftir að þær eru sendar á sviðsetningarstaðsetningu. Aðeins er hægt að sameina númeraplötur ef þær eru á sömu staðsetningu, eru í sömu hleðslu og hafa sömu sendingarupplýsingar. |
| Frystu tiltektarvinnu sem er tengd við áfyllingu á línustigi. | Nú er hægt að frysta vinnu á línustigi í stað á stigi pöntunarhauss, svo að starfsmenn geta uppfyllt tiltektarlínur sem eru ekki frystar af eftirspurnaráfyllingu. Þess vegna getur heildsali sem er með stórar sölupantanir eða smásali sem er með stórar sölupantanir eða flutningspantanir áfyllingar leyft að tiltektarvinna byrji á öllum línum sem falla ekki undir áfyllingarvinnu. Síðan er hægt að ljúka tiltektarvinnu samhliða. Þessa aðgerð er hægt að skilgreina þannig að hægt sé að velja hvort eigi að frysta stig á hausstigi eða línustigi. Einnig er hægt að nota báðar aðferðir og stofna vinnusniðmát fyrir hvora aðferðina. Skilgreining hauss/línu er stillt í vinnusniðmátum, en hægt er að breyta henni beint í vinnunni sem er mynduð. |
| Hætta við vinnu með því að nota fartækið. | Núna er hægt að hætta við vinnu með því að nota fartækið, með eða án áfyllingu eftirspurnar. Áður þurfti að nota þungbiðlara. Til að virkja þessa virkni þarf að stofna valmyndaratriði fartækis með haminn stilltan á **Óbeint** og verkþáttarkóðann stilltan á **Hætta við vinnu**. |

### <a name="warehouse-operation-enhancements"></a>Endurbætur á vöruhússaðgerðum

| Það sem hægt er að gera | Hvers vegna er þetta mikilvægt? |
|-----------------|-----------------------|
| Líkön mismunandi gámagerða. | Þú gætir notað aðrar gámagerðir í vöruhúsinu til að bæta geymslu og af öðrum ástæðum. Ný eining gámagerðar hefur eðliseiginleika tegunda gáma. Núna er hægt að tengja númeraplötur við tiltekna gámagerð og nota birgðamörk staðsetningar. Til dæmis er hægt að nota þennan eiginleika til að stjórna hversu mörg bretti (eða aðrar gámagerðir) eru leyfð á tilteknum stað. Gámagerðum hefur einnig verið bætt við röðunarflokka eininga til að bæta sjálfgefnum gámagerðum við fyrir móttökuferlinu. Hægt er að nota tegundir gáma með staðsetningarleiðbeiningum á innleið og útleið. Einnig er hægt að nota þær í lagerbirgðium til aðstoðar við að ákvarða hversu margar gámagerðir eru nú geymdar á lager. Frekari upplýsingar er að finna í bloggfærslunni [Notkun númeraplötur tengist gámagerð keyra vöruhúsakerfisferli](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Þótt þessi bloggfærsla lýsi uppfærslu á Microsoft Dynamics AX 2012 hefur sama stuðningi nú verið bætt við Dynamics 365 for Operations. |
| Bakfæra sendingar. | Í vöruhúsi verður að vera hægt að meðhöndla breytingar seint. Til dæmis gætu sumar vörur verið skemmdar þannig að ekki sé hægt að senda þær. Einnig getur viðskiptavinur gert seina beiðni um að hætta við eða breyta pöntun. Dynamics 365 for Operations leyfir núna bakfærslu sendingar. Þess vegna er hægt að hætta við fylgiseðil svo að hægt sé að uppfæra hann með réttu magni síðar. Eins er hægt, í flæði á innleið, að hætta við innhreyfingarskjöl afurða þannig að hægt sé að stofna uppfærðu útgáfuna. |
| Notaðu bretti sem eru með blandaðar vörur. | Nú er hægt að móttaka og skrá „blönduð“ bretti. Blandað bretti samanstendur af mismunandi vörum sem eru settar saman á eitt bretti í eina eða fleiri innkaupapantanir eða línur. Allar skráningar er hægt að taka saman í eina yfirnúmeraplötu. Þetta ferli er virkjað í gegnum fartæki vöruhúss. T.d. þegar bretti með blönduðum vörum berst í vöruhúsið auðkennir afgreiðslumaður í móttöku vörurnar og magnið á brettinu áður en það er flutt í sérnýttar frágangsstaðsetningar. Frágangsstaðsetningar eru auðkenndar með vinnusniðmátum og staðsetningarleiðbeiningum. Ef frágangsstaðsetningar er dreifðar yfir margar vörur sem hafa fastar staðsetningar stofnar þessi eiginleiki eins margar frágangslínur vinnu og til eru mismunandi vörur á blönduðu brettinu. Þessi eiginleiki gerir skráningu og frágang á mótteknum brettum með blönduðum vörum hraðari og sveigjanlegri. Frekari upplýsingar er að finna í bloggfærslunni [Móttaka og skrá bretta af blandaðri upprunaskjalslínu með því að nota eina númeraplötu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) og upplýsingar um stuðning við blönduð bretti í [tilkynningum um nýlegar heildaruppfærslur okkar](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Þótt þessi bloggfærsla lýsi uppfærslu á AX 2012 hefur sama stuðningi nú verið bætt við Dynamics 365 for Operations. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Minniháttar umbætur á eiginleikum í birgðakeðjustjórnun

<table>
<thead>
<tr>
<th>Það sem hægt er að gera</th>
<th>Hvers vegna er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nota nýjar gagnaeiningar til að flytja gögn inn og út.</td>
<td>Hægt er að flytja gögn inn og út með því að nota þessar gagnaeiningar:
<ul>
<li>Farmreikningur</li>
<li>Samanlagðar lagerbirgðir eftir vöruhúsi og birgðastöðu</li>
<li>Birgðakostnauðr</li>
<li>Tilboð</li>
</ul>
</td>
</tr>
<tr>
<td>Stækkuð Gantt stýringin er notuð til að þróa gagnvirkar röðunaraðstæður.</td>
<td>Stækkuð Gantt stýring gerir kleift að þróa nýjar gagnvirkar röðunaraðstæður og afhenda stækkuð APIs sem er hægt að nota til að sérsníða útlit verkþátta. Hér eru sum af nýjum APIs:
<ul>
<li>Lóðrétt draga og sleppa verkþáttum</li>
<li>Bæta við/fjarlægja aðgerðir</li>
<li>Forskoðun yfir tímabil í samantektarlínu</li>
<li>Breyta lit og stíl verkþáttamarka</li>
<li>Breyta lit, -stíl eða bakgrunni texta í dreifikerfi</li>
</ul>
</td>
</tr>
<tr>
<td>Meðhöndla betur áætlanagerð efnis og tilfanga.</td>
<td>Nokkrar viðbætur hafa verið gerðar á áætlun efnis og tilfanga:
<ul>
<li>Mörk úthreyfinga eru núna meðhöndluð þegar vara er á lager.</li>
<li>Skrifa yfir afhendingardagsetningu þegar áætlaðar pantanir eru staðfestar.</li>
<li>Forgangsraða uppfyllingum pantana yfir öryggisbirgðir.</li>
<li>Koma í veg fyrir röðun áætlaðra pantana í fortíðinni.</li>
</ul>
</td>
</tr>
<tr>
<td>Tilkynna raunverulega notkun fyrir framleiðslu og skoða birgðastöðu.</td>
<td>Hægt er að skoða raunverulega notkun fyrir framleiðslu. Þar að auki hefur nýjum gátreit <strong>Birta birgðastöðu</strong> verið bætt við <strong>Hreyfingar</strong> í valmyndaratriðinu <strong>Vinnustofnun</strong> sem gerir kleift að skoða birgðastöðu.</td>
</tr>
<tr>
<td>Reikna rúmmálsþyngd ef taxtar farmflytjanda eru byggðir á rúmmálsþyngd.</td>
<td>Nýrri TMS taxtavél sem er byggð á rúmmálsþyngd hefur verið bætt við þannig að hægt er að reikna rúmmálsþyngd.</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Frekari upplýsingar

[Nýjungar eða breytingar í Finance and Operations heimasíða](whats-new-changed.md)

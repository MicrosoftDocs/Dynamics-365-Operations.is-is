---
title: Stofna greiðsluáætlun
description: Þetta efni útskýrir hvernig á að búa til, eyða og breyta innheimtuáætlunum.
author: JodiChristiansen
ms.date: 02/09/2022
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
ms.openlocfilehash: ed31dd96b0115610cfb74aed69f1acc1055bfe56
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690446"
---
# <a name="create-billing-schedules"></a>Stofna greiðsluáætlun

[!include [banner](../includes/banner.md)]

Á **Innheimtuáætlun** síðu geturðu búið til, eytt eða breytt innheimtuáætlunum. Þú getur líka skoðað listann yfir innheimtuáætlanir. Þegar þú býrð til innheimtuáætlun eru sjálfgefin gildi fyrir hana ákvörðuð af innheimtuhópnum sem er tengdur við hana. Viðbótarupplýsingar eru settar upp á **Endurteknar innheimtufæribreytur samnings** síðu.

## <a name="create-a-billing-schedule"></a>Búðu til innheimtuáætlun

Til að búa til innheimtuáætlun skaltu fylgja þessum skrefum.

1. Á **Innheimtuáætlun** síðu, veldu **Nýtt**.
2. Í **Búðu til innheimtuáætlun** valmynd, í **Innheimtuáætlunarhópur** reit, veldu innheimtuáætlunarhóp.
3. Í **Viðskiptavinareikningur** reit, veldu viðskiptavinareikning.
4. Í **Upphafsdagur** reit, veldu upphafsdagsetningu og síðan í **Fjöldi tímabila** reit, sláðu inn fjölda tímabila. The **Loka dagsetning** reiturinn er uppfærður miðað við fjölda tímabila sem þú slærð inn. Ef þú uppfærir **Lokadagur innheimtu** sviði, the **Fjöldi tímabila** reiturinn er uppfærður í **0** (núll).
5. Veldu **Í lagi**.
6. Á **Innheimtuáætlun** síðu, í **Almennt** flipa, í **Lýsing** reit, sláðu inn lýsingu á innheimtuáætlun.
7. Í **Áfangasniðmát** reit, veldu áfangasniðmát fyrir **Áfangareikningur**.

Reitir eins og **Reikningsreikningur** og **Gjaldmiðilskóði** eru uppfærðar með upplýsingum frá viðskiptavininum.

The **Innheimtutíðni** og **Innheimtubil** reitir eru sjálfkrafa stilltir, byggt á völdum innheimtuáætlunarhópi.

8. Til að búa til sérstaka reikninga skaltu stilla **Reikningur sérstaklega** valmöguleika til **Já**.
9. Til að endurnýja innheimtuáætlun sjálfkrafa eftir síðasta innheimtutímabilið skaltu stilla á **Endurnýja sjálfkrafa** valmöguleika til **Já**, og stilltu síðan **Línur til að bæta við fyrir hverja endurnýjun** sviði.

The **Færibreytur** reitir eru sjálfkrafa stilltir, byggt á gildunum á **Endurteknar innheimtufæribreytur samnings** síðu.

10. Til að mæla hlutfallslega upphæð innheimtuáætlunar skaltu stilla **Hlutfallslega hlutatímabil** valmöguleika til **Já**.
11. Til að samræma línur innheimtuáætlunar við lok mánaðar skaltu stilla **Samræma við mánuði** valmöguleika til **Já**.
12. Í **Upphafsdagur samnings** og **Lokadagur samnings** reiti skaltu slá inn upphafs- og lokadagsetningar samningsins. Þessar dagsetningar eru eingöngu til upplýsingar.

The **Greiðsla** reit sýnir greiðsluupplýsingar viðskiptavinarins frá viðskiptavininum. Þegar lína er í biðstöðu eða henni hætt er ekki hægt að breyta greiðsluupplýsingunum.

> [!NOTE]
> Þegar þú sameinar reikninga eftir hlut, verðmæti **Greiðsluskilmála**, **·**, og **Innheimtuáætlun** reitir verða að passa saman. Annars er ekki hægt að sameina reikningana.

13. Á **Heimilisfang** flipanum geturðu skoðað og uppfært **Heimilisfang afhendingar** og **Frumvarp til að ávarpa** sviðum.
14. Á **Samskiptaupplýsingar** flipanum geturðu tengt notendareikning við innheimtuáætlunina.
15. Í **Upplýsingar um tengilið** reiti geturðu slegið inn tengilið, netfang og netfang.
16. Til að fylgjast með upplýsingum um þóknun samstarfsaðila skaltu stilla **Félagsreikningur** og **Þóknunarhlutfall samstarfsaðila** sviðum. Þessir reitir eru eingöngu til upplýsinga.
17. Á **Samtals** flipanum er hægt að skoða hinar ýmsu heildartölur sem hafa verið reiknaðar út fyrir innheimtuáætlunina.
18. Á **Haltu** flipanum geturðu skoðað endurskoðunarupplýsingar um hvenær innheimtuáætlun var sett í bið þegar biðin var fjarlægð.
19. Á **Uppsögn** flipanum geturðu skoðað feril uppsagnanna sem voru settar á eða fjarlægðar úr innheimtuáætluninni.
20. Veldu **Vista**.
21. Á **Innheimtuáætlunarlínur** Flýtiflipi, veldu **Bæta við línu**.
22. Í **Vörunúmer** reit, veldu vörunúmerið. Ef varan sem er bætt við er yfirliður í tekjuskiptingu eru línurnar sjálfkrafa uppfærðar með undirliðunum. Þú getur aðeins breytt yfirliðinu í tekjuskiptingu. Allir undirliðir eru síðan uppfærðir í samræmi við það.
23. Í **Tegund vöru** reit, veldu vörutegundina.
24. Uppfærðu upphafs- og lokadagsetningar.
25. Áður en reikningarnir eru búnir til er hægt að breyta innheimtutíðni með því að uppfæra **Innheimtutíðni** sviði. Eftir að fyrsti reikningurinn fyrir innheimtuáætlunina er búinn til er ekki hægt að breyta innheimtutíðni.
26. Í **Eining** reit, veldu mælieiningu fyrir hlutinn.
27. Í **Verðlagningaraðferð** reit, veldu verðlagningaraðferð vörunnar.

The **Einingaverð** reiturinn er sjálfkrafa stilltur úr birgðum. Hins vegar geturðu uppfært það ef þú breytir verðlagningaraðferðinni í **Flat**.

## <a name="remove-a-line-item"></a>Fjarlægðu línu

Fylgdu þessum skrefum til að fjarlægja hlut úr innheimtuáætlun.

1. Á **Innheimtuáætlun** síðu, í **Dagskrá númer** reit, veldu númer innheimtuáætlunarinnar sem á að breyta.
2. Á **Innheimtuáætlunarlínur** Flýtiflipi, veldu línuna sem á að eyða og veldu síðan **Fjarlægja**.
3. Veldu **Vista**.

Restin af þessu efni lýsir aðgerðum og upplýsingum sem eru tiltækar fyrir línur á **Innheimtuáætlunarlínur** Flýtiflipi.

## <a name="billing-schedule-line-actions"></a>Aðgerðir innheimtuáætlunarlínu

Hnapparnir á **Innheimtuáætlunarlínur** Hraðflipi gerir þér kleift að beita aðgerðum á einstakar línur.

| Hnappur | Lýsing |
|--------|-------------|
| Bæta við línu | Bættu línu við innheimtuáætlunina. |
| Bæta við úr vörulista | Bættu mörgum hlutum við innheimtuáætlun með því að velja þá á lista. |
| Fjarl. | <p>Fjarlægðu valda línu úr innheimtuáætlun.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að fjarlægja yfirliðið. Öll tengd undiratriði eru síðan sjálfkrafa fjarlægð.</p> |
| Skoða greiðsluupplýsingar | Skoðaðu innheimtuupplýsingar. |
| Hætta | <p>Ljúktu völdum línum. Þessi hnappur er aðeins tiltækur þegar valdar línur hafa stöðuna **Virkur**.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að slíta yfirvörunni.</p> |
| Fjarlægja uppsögn | <p>Fjarlægðu uppsögnina úr völdum línum. Þessi hnappur er aðeins tiltækur þegar valdar línur hafa stöðuna **Hætti**.</p><p>Fyrir hluti sem eru hluti af tekjuskiptingu er aðeins hægt að fjarlægja uppsögnina úr yfirliðinu.</p> |
| Virkja förgunarbann | <p>Veldu upplýsingar til að setja valda línu í bið.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að setja yfirvöruna í bið.</p> |
| Fjarlægja biðstöðu | <p>Fjarlægðu biðina af völdum línu.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu geturðu aðeins fjarlægt bið frá yfirvöru.</p> |
| Hækkun og afsláttur | Þessi hnappur er ekki tiltækur fyrir hluti sem eru hluti af tekjuskiptingu, nema yfirliði þar sem tekjuskiptingin notar **Núll upphæð** úthlutunaraðferð. |
| Frestanir | <p>Færðu inn frestunarvalkosti fyrir valda línu.</p><p>Þessi hnappur er ekki tiltækur fyrir yfirliði í tekjuskiptingu.</p> |
| Úthlutun áfanga | <p>Skoðaðu og uppfærðu upplýsingar um áfangaúthlutun fyrir valda línu.</p><p>Þessi hnappur er aðeins tiltækur þegar innheimtuáætlunarlínan er áfangaatriði.</p> |
| Þjónusta og endurnýjun | <p>Skoðaðu og uppfærðu upplýsingar um stuðning og endurnýjun fyrir valda línu.</p><p>Þessi hnappur er aðeins tiltækur þegar innheimtuáætlunarlínan er stuðnings- eða endurnýjunaratriði.</p> |
| Sýna víddir | Sýna eða fela víddardálka sem birtast í **Innheimtuáætlunarlínur** rist. |
| Reikna út einingarverð | <p>Reiknaðu einingarverð vörunnar, þannig að viðskiptavinurinn geti greitt samningsupphæðina í áföngum (til dæmis daglega, mánaðarlega, ársfjórðungslega, hálfsárs eða árlega). Hægt er að velja samningsverð og verðtíðni.</p><p>Hægt er að skoða endurskoðunarferil breytinganna: gamla samningsverð og tíðni, nýja samningsverð og tíðni, notandann sem gerði breytinguna og dagsetningu og tíma breytingarinnar.</p> |
| Dagsetning röðunar | <p>Tilgreindu jöfnunardagsetningu fyrir endurnýjunarvörur.</p><p>Ef þú velur vöruflokk í **Atriðahópur** reit, nota allar vörur jöfnunardagsetningu fyrstu vörunnar í vöruflokknum í innheimtuáætluninni. Ef **Atriðahópur** reiturinn er auður, þú getur tilgreint jöfnunardagsetningu til að nota fyrir alla hluti.</p><p>Þessi hnappur er aðeins tiltækur þegar **Innheimtutíðni** reiturinn er stilltur á **Árlegt**.</p> |
| Óreikningsfærðar tekjur | <p>Stilltu hlutinn til að nota óinnheimta tekjur eiginleiki. Síðan er hægt að tilgreina óinnheimtu tekjur og óinnheimtu afsláttarreikninga fyrir vöruna.</p><p>Þessi hnappur er aðeins tiltækur fyrir hluti þar sem **Tegund vöru** reiturinn er stilltur á **Standard**. Það er ekki tiltækt fyrir núverandi innheimtuáætlanir eða fyrir innheimtuáætlunarlínur þar sem reikningurinn hefur þegar verið búinn til.</p> |
| Bæta við undireiningu tekjuskiptingar | <p>Veldu undirvöru til að bæta við sölupöntunina.</p><p>Þessi hnappur er aðeins tiltækur fyrir yfirvörur í tekjuskiptingu.</p> |
| Ítarlegir valkostir verðlagningar | Breyttu verðmöguleikum vöru. |

## <a name="billing-schedule-line-details"></a>Upplýsingar um innheimtuáætlunarlínu

Þegar þú velur línu í **Innheimtuáætlunarlínur** Flýtiflipi, þú getur skoðað sérstakar upplýsingar fyrir þá línu. Þessum upplýsingum er skipt á mismunandi flipa.

### <a name="general-tab"></a>Almennt

Eftirfarandi upplýsingar eru fáanlegar á **Almennt** flipa.

| Reitur eða hluti | Lýsing |
|------------------|-------------|
| Notkun | <p>Þessi hluti veitir upplýsingar um notkunaratriði. Það inniheldur eftirfarandi reiti:</p><ul><li>**Notkunarauðkenni** – Auðkenni mælisins eða notkunarhlutarins.</li><li>**Lestrarvalkostur** - Notkunarlestrarvalkosturinn: **Lestur** eða **Neysla**.</li><li>**Áætluð neysla** – Tilgreindu áætlaða notkun fyrir notkunarvöru sem hefur tímabil þar sem reikningurinn hefur ekki verið búinn til. Á **Innheimtuupplýsingar** síðu er hægt að skoða línur innheimtuupplýsinga fyrir áætlaða neyslu.</li></ul> |
| Ytri tilvísanir\* | Þessi hluti inniheldur **Ytri** og **Línunúmer** reiti, þar sem þú getur tilgreint ytri tilvísunarupplýsingar. |
| Áfangi | <p>Þessi hluti veitir upplýsingar um áfangaatriði. Það inniheldur **Áætlaður verklokadagur** reit, sem sýnir verklokadag.</li></ul> |
| Texti | Athugasemd fyrir línuna. Textinn er þýddur á sjálfgefið tungumál viðskiptavinar eða lögaðila. |
| Vöruflokkur | Vöruflokkurinn fyrir línuvöruna. |
| Dagsetning röðunar | Jöfnunardagsetning fyrir innheimtuáætlun. |

\* Þegar þú sameinar reikninga eftir liðum á **Búðu til reikning** síðu, the **Ytri tilvísun** reitir verða að passa saman. Ef jafnvel einn stafur er frábrugðinn verða vörurnar ekki sameinaðar á reikningnum. Engar löggildingarathuganir eru gerðar á hvorum reitnum í **Ytri tilvísun** kafla, og gildið í **Línunúmer** reit verður að vera jákvæð heil tala.

### <a name="address-tab"></a>Heimilisfang flipinn

Eftirfarandi upplýsingar eru fáanlegar á **Heimilisfang** flipa.

| Reitur | Lýsing |
|-------|-------------|
| Afhendingaraðsetur | <p>Veldu afhendingarfang fyrir línuvöruna. Sjálfgefið afhendingarheimilisfang er aðalafhendingarfang frá **Heimilisfang** Flýtiflipi.</p><p>Þegar þú breytir heimilisfanginu geturðu valið eftirfarandi heimilisfangsvalkosti:</p><ul><li>**Heimilisföng** – Veldu heimilisfang fyrir núverandi viðskiptavin.</li><li>**Í notkun** – Veldu heimilisfang sem er notað fyrir núverandi viðskiptavin.</li><li>**Annað heimilisfang** – Veldu heimilisfang fyrir hvaða viðskiptavinaskrá sem er.</li></ul><p>Fyrir vörur sem nota tekjuskiptingu er aðeins hægt að breyta heimilisfangi yfirvörunnar. Heimilisfang undirhlutanna samsvarar heimilisfangi foreldris og ekki er hægt að breyta því sérstaklega.</p> |
| Frumvarp til að ávarpa | <p>Veldu heimilisfang reiknings fyrir línuna. Sjálfgefið afhendingarheimilisfang er aðalafhendingarfang frá **Heimilisfang** Flýtiflipi. Þú getur breytt heimilisfanginu eftir þörfum, byggt á tilgangi tiltækra heimilisfönga:</p><ul><li>Ef ekkert af heimilisföngunum hefur þann tilgang að **Reikningur**, sjálfgefið heimilisfang reikninga er aðal heimilisfang viðskiptavinarins, óháð tilgangi.</li><li>Ef eitt eða fleiri heimilisföngin hafa þann tilgang að **Reikningur**, sjálfgefið heimilisfang reikninga er það heimilisfang sem var síðast slegið inn.</li><li>Ef eitt eða fleiri heimilisföngin hafa þann tilgang að **Reikningur**, og eitt af reikningsföngunum er stillt sem aðalheimilisfang, er sjálfgefið heimilisfang reiknings til heimilisfangið sem hefur þann tilgang að **Reikningur** og er stillt sem aðal heimilisfang.</li><li>Fyrir vörur sem nota tekjuskiptingu er aðeins hægt að breyta heimilisfangi yfirvörunnar. Heimilisfang undirhlutanna samsvarar heimilisfangi foreldris og ekki er hægt að breyta því sérstaklega.</li></ul> |

### <a name="product-tab"></a>Vöruflipi

Eftirfarandi upplýsingar eru fáanlegar á **Vara** flipa.

| Reitur eða hluti | Lýsing |
|------------------|-------------|
| Geymsluvíddir | <p>Þessi hluti sýnir geymsluupplýsingar fyrir hlutinn. Það inniheldur **Raðnúmer** reit, sem sýnir raðnúmer vörunnar.</p><p>Raðnúmerið er afritað úr upphaflegu sölupöntuninni meðan á stuðnings- og endurnýjunarferlinu stendur. Fyrir vörur sem nota tekjuskiptingu er raðnúmer yfirvöru afritað á allar undirvörur. Raðnúmerið er afritað þegar **Afritaðu raðnúmer** valkostur er stilltur á **Já** á **Endurteknar innheimtufæribreytur samnings** síðu.</li></ul> |
| Afurðarvíddir | Vöruupplýsingarnar fyrir vöruna og gildin eru sjálfkrafa uppfærð, byggt á **Afbrigðisnúmer** gildi sem er valið fyrir innheimtuáætlunarlínuna. |

### <a name="account-tab"></a>Reikningsflipi

Eftirfarandi upplýsingar eru fáanlegar á **Reikningur** flipa.

| Reitur | Lýsing |
|-------|-------------|
| Aðallykill | Aðalreikningurinn sem er stofnaður á sölulínunni. Sjálfgefið gildi er frá sölupöntuninni. Þessi reitur getur verið auður. |
| Fjárhagsstærðir hlutar | <p>Sjálfgefin fjárhagsvíddargildi, byggt á viðskiptamanna- og vörufærslunni.</p><p>Fyrir vörur sem nota tekjuskiptingu nota undirvörur fjárhagsvíddargildi viðskiptavinar og vöruskrár, eins og lýst er áðan. Ef þú verður að uppfæra fjárhagsvíddargildi undirliða geturðu flutt inn gagnaeininguna.</p> |

### <a name="renewals-tab"></a>Endurnýjunarflipi

Eftirfarandi upplýsingar eru fáanlegar á **Endurnýjun** flipa.

| Reitur | Lýsing |
|-------|-------------|
| Endurnýja sjálfkrafa | <p>Gildi sem gefur til kynna hvort innheimtuáætlunarlínan sé endurnýjuð sjálfkrafa fyrir næsta innheimtutímabil:</p><ul><li>**Já** – Innheimtuáætlunarlínan endurnýjast sjálfkrafa fyrir næsta innheimtutímabil þegar þú býrð til reikning.</li><li>**Nei** – Innheimtuáætlunarlínan endurnýjast ekki sjálfkrafa. Þú verður að endurnýja innheimtuáætlun handvirkt.</li></ul> |
| Línur til að bæta við fyrir hverja endurnýjun | Fjöldi lína sem á að bæta við endurnýjun innheimtuáætlunar. |

Að auki eru eftirfarandi hnappar fáanlegir á **Endurnýjun** flipa.

| Hnappur | Lýsing |
|--------|-------------|
| Eftirlit með bókarfærslu óreikningsfærðra tekna | Skoðaðu allar breytingar fyrir vörur sem nota óinnheimt tekjur eiginleiki. |
| Bæta við tímabili endurnýjunar | Bættu við endurnýjunartíma fyrir hlutinn. Upphafsdagur nýja endurnýjunartímabilsins er næsti dagur á eftir lokadagsetningu fyrri tíma. The **Lokadagur endurnýjunar**, **frestun**, **frestun**, **·**, og **Einingaverð** reiti er hægt að uppfæra. |
| Breyta tímabili endurnýjunar | <p>Breyta endurnýjunartíma. Fyrir upphafstímabilið er hægt að breyta upphafs- og lokadagsetningum frestunarinnar áður en upphafsbókarfærslan er stofnuð. Fyrir síðari skilmála er ekki hægt að breyta upphafsdagsetningu. Það er alltaf næsta dagsetning eftir lok fyrri kjörtímabils.</p><p>Ef endurnýjunartími er til eftir þann tíma sem þú ert að breyta er ekki hægt að breyta dagsetningum tímans. Í þessu tilviki, aðeins **Magn** og **Einingaverð** Hægt er að uppfæra reiti fyrir endurnýjunaratriðið.</p><p>Til dæmis eru þrjú hugtök til. <ul><li>Ekki er hægt að breyta fyrsta kjörtímabilinu þar sem það er þegar hafið.</li><li>Fyrir seinni tíma er aðeins hægt að breyta magni og einingarverði.</li><li>Fyrir þriðja tíma er hægt að breyta öllum gildum nema upphafsdagsetningu. Að auki er **Dagskrá frá sniðmáti** valmöguleikinn gerir þér kleift að búa til frestunaráætlun sem er byggð á sniðmátinu fyrir óinnheimtu tekjuliðinn. Þegar þessi valkostur er stilltur á **Já**, veldu frestunarsniðmátið í **Sniðmát** reit og breyttu upphafs- og lokadagsetningum frestunarinnar eftir þörfum. Síðari endurnýjunarskilmálar nota sama frestunarsniðmát. Hins vegar er hægt að breyta frestunarsniðmátinu.</p></li></ul> |

### <a name="termination-tab"></a>Uppsagnarflipi

Eftirfarandi upplýsingar eru fáanlegar á **Uppsögn** flipa.

| Reitur | Lýsing |
|-------|-------------|
| Starfslokadagur | Dagsetningin þegar innheimtuáætlunarlínunni er hætt. Sjálfgefið gildi er frá **Uppsagnardagur** reit á hausnum. Þú getur breytt gildinu eins og þú vilt. |
| Tegund uppsagnar | Uppsagnartegundin. Sjálfgefið gildi er frá **Uppsagnartegund** reit á hausnum. |

### <a name="hold-tab"></a>Haltu flipanum

Ef frestun tekna og gjalda er notuð, skal **Haltu** flipinn sýnir frestun dagsetningu.

### <a name="escalation-and-discount-tab"></a>Stækkunar- og afsláttarflipi

Eftirfarandi upplýsingar eru fáanlegar á **Stækkun og afsláttur** flipa.

| Reitur | Lýsing |
|-------|-------------|
| Hækkun | <p>Veldu hvort stigmögnun sé leyfð fyrir innheimtuáætlunarlínuna. Sérhver stigmögnunarlína úr hausnum er notuð þegar innheimtuáætlunarlínan er búin til.</p><ul><li>**Já** – Hægt er að beita stigmögnun á línuna. Þegar þessi valkostur er valinn geturðu sett upp stigmögnun fyrir innheimtuáætlunarlínur á **Stækkun og afsláttur** síðu.</li><li>**Nei** – Ekki er hægt að beita stigmögnun á línuna.</li></ul><p>Sjálfgefin stilling er byggð á **Innheimtuáætlunarhópur** valin.</p> |

### <a name="price-changes-tab"></a>Verðbreytingarflipi

Fyrir línur sem breytt er frá **Standard** verð til **Flat** verð, rist á **Verðbreytingar** flipinn inniheldur eftirfarandi dálka:

- Breyta dagsetningu
- Breytt af notanda
- Staðlað verð
- Fast verð
- Verðuppfærsla

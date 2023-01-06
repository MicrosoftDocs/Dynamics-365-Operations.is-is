---
title: Stofna greiðsluáætlun
description: Í þessari grein er útskýrt hvernig á að stofna, eyða og breyta greiðsluáætlunum.
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
ms.openlocfilehash: 1248799f92dc6cbce8528a53cc8a3012d2a67b3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903393"
---
# <a name="create-billing-schedules"></a>Stofna greiðsluáætlun

[!include [banner](../includes/banner.md)]

Á síðunni **Greiðsluáætlun** geturðu stofnað, eytt eða breytt greiðsluáætlunum. Einnig er hægt að fara yfir lista yfir greiðsluáætlanir. Þegar greiðsluáætlun er búin til eru sjálfgefin gildi fyrir hana ákveðin eftir reikningshópnum sem tengist honum. Viðbótarupplýsingar eru settar upp á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.

## <a name="create-a-billing-schedule"></a>Stofna greiðsluáætlun

Fylgið þessum skrefum til að stofna greiðsluáætlun.

1. Á síðunni **Greiðsluáætlun** skal velja **Ný**.
2. Í svarglugganum **Búa til greiðsluáætlun**, í reitnum **Greiðsluáætlunarflokkur**, skal velja greiðsluáætlunarflokk.
3. Á svæðinu **Viðskiptavinalykill** skal velja reikning viðskiptavinar.
4. Í reitnum **Upphafsdagsetning** skal velja upphafsdagsetninguna og síðan í reitinn **Fjöldi tímabila** skal færa inn fjölda tímabila. Reiturinn **Lokadagsetning** er uppfærður í samræmi við fjölda tímabila sem sleginn er inn. Ef þú uppfærir reitinn **Lokadagsetning innheimtu** er reiturinn **Fjöldi tímabila** uppfærður í **0** (núll).
5. Veldu **Í lagi**.
6. Á síðunni **Greiðsluáætlun**, á flipanum **Almennt**, á svæðinu **Lýsing**, skal slá inn lýsingu á greiðsluáætluninni.
7. Í reitnum **Sniðmát áfanga** skal velja áfangasniðmát fyrir **Áfangagreiðslu**.

Reitir eins og **Reikningslykill** og **Gjaldmiðilskóði** eru uppfærðir með upplýsingum frá viðskiptavini.

Reitirnir **Greiðslutíðni** og **Greiðslutímabil** eru sjálfkrafa stilltir út frá völdum greiðsluáætlunarflokki.

8. Til að búa til aðskilda reikninga skal stilla valkostinn **Reikningsfæra aðskilið** á **Já**.
9. Til að endurnýja greiðsluáætlun sjálfkrafa eftir síðasta tímabil reikningsfærslu skal stilla valkostinn **Endurnýja sjálfkrafa** á **Já** og síðan stilla reitinn **Línur til að bæta við fyrir hverja endurnýjun**.

Reitirnir **Færibreytur** eru sjálfkrafa stilltir út frá gildunum á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.

10. Til að hlutfallsskipta upphæðinni í greiðsluáætlun skal stilla valkostinn **Hlutfallsskipta hluta úr tímabilum** á **Já**.
11. Til að samræma upplýsingalínur greiðsluáætlunar við lok mánaðar skal stilla valkostinn **Samræma við mánuð** á **Já**.
12. Í reitina **Upphafsdagur samnings** og **Lokadagur samnings** skal færa inn upphafs- og lokadagsetningu samningsins. Þessar dagsetningar eru aðeins til upplýsingar.

Reiturinn **Greiðsla** sýnir greiðsluupplýsingar viðskiptavinar frá viðskiptavini. Ekki er hægt að breyta greiðsluupplýsingum þegar vörulína er í bið eða sagt upp.

> [!NOTE]
> Þegar reikningar eru sameinaðir eftir vöru verður virði reitanna **Greiðsluskilmálar**, **Aðferð** og **Greiðsluáætlun** að stemma. Annars er ekki hægt að sameina reikningana.

13. Í flipanum **Aðsetur** er hægt að yfirfara og uppfæra reitina **Afhendingaraðsetur** og **Reikningsaðsetur**.
14. Í flipanum **Samskiptaupplýsingar** er hægt að tengja notandareikning við greiðsluáætlunina.
15. Í reitina **Samskiptaupplýsingar** skal færa inn tengilið, netfang og veffang.
16. Til að fylgjast með upplýsingum um þóknun skal stilla reitina **Reikningur samstarfsaðila** og **Umboðslaunataxti samstarfsaðila**. Þessi svæði eru aðeins til upplýsingar.
17. Í flipanum **Samtals** er hægt að skoða ýmsar samtölur sem hafa verið reiknaðar fyrir greiðsluáætlunina.
18. Í flipanum **Bið** er hægt að skoða eftirlitsupplýsingar um hvenær greiðsluáætlunin var sett í bið og hvenær biðstaðan var fjarlægð.
19. Í flipanum **Uppsögn** er hægt að skoða feril uppsagna sem voru settar á eða fjarlægðar úr greiðsluáætluninni.
20. Veldu **Vista**.
21. Á flýtiflipanum **Greiðsluáætlunarlínur** skal velja **Bæta við línu**.
22. Veljið vörunúmerið á svæðinu **Vörunúmer**. Ef vörunni sem var bætt við er yfirvara í tekjuskiptingu eru línurnar sjálfkrafa uppfærðar með undirvörunum. Aðeins er hægt að breyta yfirvörunni í tekjuskiptingunni. Allar undirvörur eru síðan uppfærðar í samræmi.
23. Á svæðinu **Gerð vöru** skal velja gerð vöru.
24. Uppfærið upphafs- og lokadagsetningar.
25. Áður en reikningar eru búnir til er hægt að breyta greiðslutíðninni með því að uppfæra reitinn **Greiðslutíðni**. Ekki er hægt að breyta greiðslutíðninni eftir að fyrsti reikningurinn fyrir greiðsluáætlunina er búinn til.
26. Á svæðinu **Eining** skal velja mælieiningu fyrir vöruna.
27. Í reitnum **Verðlagningaraðferð** skal velja verðlagningaraðferðina fyrir vöruna.

Reiturinn **Einingarverð** er sjálfkrafa stilltur úr birgðum. Hins vegar er hægt að uppfæra hann ef verðlagningaraðferðinni er breytt í **Fast**.

## <a name="remove-a-line-item"></a>Fjarlægja línuatriði

Til að fjarlægja vöru úr greiðsluáætlun skal fylgja þessum skrefum.

1. Á síðunni **Greiðsluáætlun**, í reitnum **Áætlunarnúmer**, skal velja númer greiðsluáætlunar sem á að breyta.
2. Í flýtiflipanum **Greiðsluáætlunarlínur** skal velja línuna sem á að eyða og síðan velja **Fjarlægja**.
3. Veldu **Vista**.

Það sem eftir er af greininni lýsir aðgerðum og upplýsingum sem eru í boði fyrir línur í flýtiflipanum **Greiðsluáætlunarlínur**.

## <a name="billing-schedule-line-actions"></a>Aðgerðir greiðsluáætlunarlínu

Hnapparnir í flýtiflipanum **Greiðsluáætlunarlínur** gera þér kleift að nota aðgerðir á einstakar línur.

| Hnappur | Lýsing |
|--------|-------------|
| Bæta við línu | Bæta línu við í greiðsluáætlun. |
| Bæta við úr vörulista | Bættu mörgum vörum við greiðsluáætlun með því að velja þær í lista. |
| Fjarl. | <p>Fjarlægið völdu línuna úr greiðsluáætlun.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að fjarlægja yfirvöruna. Allar tengdar undirvörur eru síðan sjálfkrafa fjarlægðar.</p> |
| Skoða greiðsluupplýsingar | Skoðið greiðsluupplýsingarnar. |
| Hætta | <p>Afturkalla völdu línurnar. Þessi hnappur er aðeins í boði þegar valdar línur eru með stöðuna **Virkar**.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að segja upp yfirvörunni.</p> |
| Fjarlægja uppsögn | <p>Fjarlægðu uppsögnina úr völdum línum. Þessi hnappur er aðeins í boði þegar valdar línur eru með stöðuna **Sagt upp**.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að fjarlægja uppsögnina úr yfirvörunni.</p> |
| Virkja förgunarbann | <p>Veldu upplýsingar um af hverju valin lína er sett í bið.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að setja yfirvöruna í bið.</p> |
| Fjarlægja biðstöðu | <p>Fjarlægið biðina á völdu línunni.</p><p>Fyrir vörur sem eru hluti af tekjuskiptingu er aðeins hægt að fjarlægja biðstöðuna af yfirvörunni.</p> |
| Hækkun og afsláttur | Þessi hnappur er ekki í boði fyrir vörur sem eru hluti af tekjuskiptingu, nema yfirvörur þar sem tekjuskiptingin notar úthlutunaraðferðina **Núllupphæð**. |
| Frestanir | <p>Færið inn frestunarvalkosti fyrir völdu línuna.</p><p>Þessi hnappur er ekki í boði fyrir yfirvörur í tekjuskiptingu.</p> |
| Úthlutun áfanga | <p>Farðu yfir og uppfærðu upplýsingar um áfangaúthlutun fyrir valda línu.</p><p>Þessi hnappur er aðeins í boði þegar vara greiðsluáætlunarlínu er áfangavara.</p> |
| Þjónusta og endurnýjun | <p>Farðu yfir og uppfærðu upplýsingar um stuðning og endurnýjun fyrir völdu línuna.</p><p>Þessi hnappur er aðeins í boði þegar vara greiðsluáætlunarlínu er stuðnings- eða endurnýjunarvara.</p> |
| Sýna víddir | Sýndu eða feldu víddardálkana sem birtast í hnitanetinu **Greiðsluáætlunarlínur**. |
| Reikna út einingarverð | <p>Reiknaðu einingarverð vörunnar þannig að viðskiptavinurinn geti greitt samningsupphæðina í afborgunum (til dæmis daglega, mánaðarlega, ársfjórðungslega, hálfs árs fresti eða árlega). Hægt er að velja samningsverð og verðtíðni.</p><p>Hægt er að skoða færsluslóð breytinganna: gamla samningsverðið og tíðni, nýja samningsverðið og tíðni, notandann sem gerði breytinguna og dagsetningu og tíma breytingarinnar.</p> |
| Dagsetning röðunar | <p>Tilgreindu samræmingardag fyrir endurnýjunarvörurnar.</p><p>Ef valinn er vöruflokkur í reitnum **Vöruflokkur** nota allar vörur samræmingardag fyrstu vörunnar í vöruflokknum í greiðsluáætluninni. Ef reiturinn **Vöruflokkur** er auður er hægt að tilgreina samræmingardag til að nota fyrir allar vörur.</p><p>Þessi hnappur er aðeins í boði þegar reiturinn **Greiðslutíðni** er stilltur á **Árlega**.</p> |
| Óreikningsfærðar tekjur | <p>Stilltu vöruna sem á að nota eiginleika óreikningsfærðra tekna. Síðan er hægt að tilgreina óreikningsfærðar tekjur og óreikningsfærða afsláttarlykla fyrir vöruna.</p><p>Þessi hnappur er aðeins í boði fyrir vörur þar reiturinn **Vörutegund** er stilltur á **Staðlað**. Hann er ekki boði fyrir fyrirliggjandi greiðsluáætlanir eða fyrir greiðsluáætlunarlínur þar sem reikningurinn hefur þegar verið búinn til.</p> |
| Bæta við undireiningu tekjuskiptingar | <p>Veljið undiratriði til að bæta við sölupöntunina.</p><p>Þessi hnappur er aðeins í boði fyrir yfirvörur í tekjuskiptingu.</p> |
| Ítarlegir valkostir verðlagningar | Breyta verðvalkostum fyrir vöru. |

## <a name="billing-schedule-line-details"></a>Upplýsingar greiðsluáætlunarlínu

Þegar lína er valin í flýtiflipanum **Greiðsluáætlunarlínur** er hægt að skoða tilteknar upplýsingar fyrir þá línu. Þessum upplýsingum er skipt á milli mismunandi flipa.

### <a name="general-tab"></a>Almennt

Eftirfarandi upplýsingar eru tiltækar á flipanum **Almennt**:

| Svæði eða hluti | Lýsing |
|------------------|-------------|
| Notkun | <p>Í þessum hluta eru upplýsingar um notkunarvörur. Inniheldur eftirfarandi svæði:</p><ul><li>**Kennimerki notkunar** – Kennimerki mælis eða notkunarvöru.</li><li>**Lestrarvalkostur** – Lestrarvalkostur notkunar: **Lestur** eða **Notkun**.</li><li>**Áætluð notkun** – Tilgreindu áætlaða notkun fyrir notkunarvöru sem er með tímabil þar sem reikningurinn hefur ekki verið búinn til. Á síðunni **Greiðsluupplýsingar** er hægt að fara yfir línur greiðsluupplýsinga fyrir áætlaða notkun.</li></ul> |
| Ytri tilvísanir\* | Þessi hluti inniheldur reitina **Ytra** og **Línunúmer** þar sem hægt er að tilgreina ytri tilvísunarupplýsingar. |
| Áfangi | <p>Þessi hluti veitir upplýsingar um áfangaavörur. Hann inniheldur reitinn **Áætluð lokadagsetning**, sem sýnir lokadagsetningu vörunnar.</li></ul> |
| Texti | Athugasemd fyrir línuna. Textinn er þýddur á sjálfgefið tungumál viðskiptavinar eða lögaðila. |
| Vöruflokkur | Vöruflokkurinn fyrir línuatriði. |
| Dagsetning röðunar | Samræmingardagur fyrir greiðsluáætlunina. |

\* Þegar reikningar eru sameinaðir eftir vöru á síðunni **Búa til reikning** verður reiturinn **Ytri tilvísun** að passa. Ef bara einn stafur er öðruvísi verða vörurnar ekki sameinaðar á reikningnum. Engar staðfestingarathuganir eru gerðar á hvorugum reitnum í hlutanum **Ytri tilvísun** og gildið í reitnum **Línunúmer** verður að vera jákvæð heiltala.

### <a name="address-tab"></a>Aðsetursflipi

Eftirfarandi upplýsingar eru tiltækar á flipanum **Aðsetur**:

| Svæði | Lýsing |
|-------|-------------|
| Afhendingaraðsetur | <p>Veljið afhendingaraðsetur fyrir línuatriðið. Sjálfgefið afhendingaraðsetur er aðalafhendingaraðsetrið úr flýtiflipanum **Aðsetur**.</p><p>Þegar aðsetrinu er breytt er hægt að velja eftirfarandi valkosti aðseturs:</p><ul><li>**Aðsetur** – Veldu aðsetur fyrir núverandi viðskiptavin.</li><li>**Í notkun** – Veldu aðsetur sem er notað fyrir núverandi viðskiptavin.</li><li>**Annað aðsetur** – Veldu aðsetur fyrir allar færslur viðskiptavinar.</li></ul><p>Fyrir vörur sem nota tekjuskiptingu er aðeins hægt að breyta aðsetrinu fyrir yfirvöruna. Aðsetrið fyrir undirvörurnar stemmir við aðsetur yfirvöru og er ekki hægt að breyta því sérstaklega.</p> |
| Reikningsaðsetur | <p>Veldu reikningsaðsetur fyrir vörulínuna. Sjálfgefið afhendingaraðsetur er aðalafhendingaraðsetrið úr flýtiflipanum **Aðsetur**. Hægt er að breyta aðsetrinu eftir þörfum, byggt á tilgangi tiltækra aðsetra:</p><ul><li>Ef ekkert af aðsetrunum hefur tilganginn **Reikningur** er sjálfgefið reikningsaðsetur aðalaðsetrið fyrir viðskiptavininn óháð tilganginum.</li><li>Ef eitt eða fleiri aðsetranna eru með tilganginn **Reikningur** verður sjálfgefið reikningsaðsetur aðsetrið sem var síðast slegið inn.</li><li>Ef eitt eða fleiri aðsetranna eru með tilganginn **Reikningur** og eitt reikningsaðsetranna er stillt sem aðalaðsetur er sjálfgefið reikningsaðsetur aðsetrið sem er með tilganginn **Reikningur** og er stillt sem aðalaðsetrið.</li><li>Fyrir vörur sem nota tekjuskiptingu er aðeins hægt að breyta aðsetrinu fyrir yfirvöruna. Aðsetrið fyrir undirvörurnar stemmir við aðsetur yfirvöru og er ekki hægt að breyta því sérstaklega.</li></ul> |

### <a name="product-tab"></a>Afurðarflipi

Eftirfarandi upplýsingar eru tiltækar á flipanum **Afurð**:

| Svæði eða hluti | Lýsing |
|------------------|-------------|
| Geymsluvíddir | <p>Í þessum hluta eru sýndar geymsluupplýsingar fyrir vöruna. Í honum er reiturinn **Raðnúmer**, sem sýnir raðnúmer vörunnar.</p><p>Raðnúmerið er afritað úr upphaflegri sölupöntun í stuðnings- og endurnýjunarferlinu. Fyrir vörur sem nota tekjuskiptingu er raðnúmer yfirvörunnar afritað í allar undirvörur. Raðnúmerið er afritað þegar valkosturinn **Afrita raðnúmer** er stilltur á **Já** á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.</li></ul> |
| Afurðarvíddir | Upplýsingar um afurðina fyrir vöruna og gildin eru uppfærð sjálfkrafa, byggt á gildinu **Númer afbrigðis** sem er valið fyrir greiðsluáætlunarlínuna. |

### <a name="account-tab"></a>Lykilflipinn

Eftirfarandi upplýsingar eru tiltækar á flipanum **Lykill**.

| Svæði | Lýsing |
|-------|-------------|
| Aðallykill | Aðallykillinn sem er búinn til í sölulínunni. Sjálfgefið gildi er fengið frá sölupöntuninni. Svæðið getur verið autt. |
| Fjárhagsvíddir vöru | <p>Sjálfgefin fjárhagsvíddargildi byggð á viðskiptavina- og vörufærslu.</p><p>Fyrir vörur sem nota tekjuskiptingu nota undirvörurnar fjárhagsvíddargildi viðskiptavina- og vörufærslna eins og lýst var á undan. Ef uppfæra þarf fjárhagsvíddargildi undirvöru er hægt að flytja inn gagnaeininguna.</p> |

### <a name="renewals-tab"></a>Endurnýjunarflipi

Eftirfarandi upplýsingar eru tiltækar á flipanum **Endurnýjanir**:

| Svæði | Lýsing |
|-------|-------------|
| Endurnýja sjálfkrafa | <p>Gildi sem segir til um hvort greiðsluáætlunarlína sé endurnýjuð sjálfkrafa fyrir næsta greiðslutímabil:</p><ul><li>**Já** – Greiðsluáætlunarlínan er endurnýjuð sjálfkrafa fyrir næsta greiðslutímabil þegar reikningur er búinn til.</li><li>**Nei** – Greiðsluáætlunarlínur eru ekki endurnýjaðar sjálfkrafa. Þú verður að endurnýja greiðsluáætlunina handvirkt.</li></ul> |
| Línur til að bæta við fyrir hverja endurnýjun | Línufjöldinn sem á að bæta við endurnýjun greiðsluáætlunar. |

Eftirfarandi hnappar eru auk þess í boði á flipanum **Endurnýjanir**.

| Hnappur | Lýsing |
|--------|-------------|
| Eftirlit með bókarfærslu óreikningsfærðra tekna | Skoðaðu allar breytingar fyrir vörur sem nota eiginleika óreikningsfærðra tekna. |
| Bæta við tímabili endurnýjunar | Bæta við endurnýjunartímabili fyrir vöruna. Upphafsdagur nýja endurnýjunartímabilsins er næsti dagur á eftir lokadegi fyrra tímabils. Hægt er að uppfæra reitina **Lokadagsetning endurnýjunar**, **Upphafsdagsetning frestunar**, **Lokadagsetning frestunar**, **Vörumagn** og **Einingarverð**. |
| Breyta tímabili endurnýjunar | <p>Breyta tímabili endurnýjunar. Fyrir upphaflegt tímabil er hægt að breyta upphafs- og lokadagsetningum frestunar áður en upphafleg færsla færslubókar er stofnuð. Ekki er hægt að breyta upphafsdagsetningu fyrir síðari tímabil. Það er alltaf næsti dagur á eftir lok fyrra tímabils.</p><p>Ekki er hægt að breyta dagsetningum tímabils ef endurnýjunartímabil er til staðar eftir að tímabilinu er breytt. Í þessu tilviki er aðeins hægt að uppfæra reitina **Magn** og **Einingarverð** fyrir endurnýjunarvöruna.</p><p>Til dæmis eru þrjú tímabil til staðar. <ul><li>Ekki er hægt að breyta fyrsta tímabilinu því að það er þegar byrjað.</li><li>Fyrir næsta tímabil er aðeins hægt að breyta magni og einingarverði.</li><li>Fyrir þriðja tímabilið er hægt að breyta öllum gildum nema upphafsdagsetningunni. Auk þess gerir valkosturinn **Áætlun úr sniðmáti** þér kleift að búa til frestunaráætlun sem byggir á sniðmátinu fyrir vöru óreikningsfærðra tekna. Þegar þessi valkostur er stilltur á **Já** skal velja frestunarsniðmátið í reitnum **Sniðmát** og breyta upphafs- og lokadagsetningu frestunar eftir þörfum. Síðari endurnýjunartímabil nota sama frestunarsniðmátið. Hins vegar er hægt að breyta frestunarsniðmátinu.</p></li></ul> |

### <a name="termination-tab"></a>Afturköllunarflipi

Eftirfarandi upplýsingar eru tiltækar á flipanum **Afturköllun**.

| Svæði | Lýsing |
|-------|-------------|
| Starfslokadagur | Dagsetningin þegar greiðsluáætlunarlínunni er sagt upp. Sjálfgefna gildið er úr reitnum **Dagsetning uppsagnar** í hausnum. Hægt er að breyta gildinu eftir þörfum. |
| Tegund uppsagnar | Tegund afturköllunar. Sjálfgefna gildið er úr reitnum **Tegund uppsagnar** í hausnum. |

### <a name="hold-tab"></a>Biðflipinn

Ef tekju- og útgjaldafrestanir eru notaðar sýnir flipinn **Í bið** frestunardagsetninguna.

### <a name="escalation-and-discount-tab"></a>Hækkunar- og afsláttarflipi

Eftirfarandi upplýsingar eru í boði á flipanum **Hækkun og afsláttur**.

| Svæði | Lýsing |
|-------|-------------|
| Hækkun | <p>Veldu hvort hækkanir séu leyfðar fyrir greiðsluáætlunarlínuna. Allar hækkunarlínur úr hausnum eru notaðar þegar greiðsluáætlunarlínan er búin til.</p><ul><li>**Já** – Hægt er að nota hækkanir í línuna. Þegar þessi valkostur er valinn er hægt að setja upp hækkanir fyrir greiðsluáætlunarlínur á síðunni **Hækkun og afsláttur**.</li><li>**Nei** – Ekki er hægt að nota hækkanir í línu.</li></ul><p>Sjálfgefna stillingin byggir á **Greiðsluáætlunarflokknum** er sem er valinn.</p> |

### <a name="price-changes-tab"></a>Verðbreytingaflipi

Fyrir línur sem er breytt úr **Stöðluðu** verði í **Fast** verð inniheldur hnitanetið í flipanum **Verðbreytingar** eftirfarandi dálka:

- Breyta dagsetningu
- Breytt af notanda
- Staðlað verð
- Fast verð
- Verðuppfærsla

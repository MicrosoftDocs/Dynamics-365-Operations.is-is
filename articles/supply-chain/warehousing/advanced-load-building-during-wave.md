---
title: Ítarleg hleðsluáætlun í bylgju
description: Í þessu efnisatriði er að finna upplýsingar um ítarlega hleðsluáætlun bylgju, sem úthlutar sjálfkrafa sendingum á fyrirliggjandi bylgjur við bylgjukeyrslu. Þess vegna er hægt að búa til gagnlegar bylgjur sem standa fyrir flutningabíla án þess að þurfa að nota vinnusvæði hleðsluáætlunar.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e4abe1a03997853053f60c750199874a61fc68c0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006392"
---
# <a name="advanced-load-building-during-wave"></a>Ítarleg hleðsluáætlun í bylgju

[!include [banner](../includes/banner.md)]

Ítarleg hleðsluáætlun bylgju úthlutar sjálfkrafa sendingum á fyrirliggjandi bylgjur við bylgjukeyrslu. Þess vegna er hægt að búa til gagnlegar bylgjur sem standa fyrir flutningabíla án þess að þurfa að nota vinnusvæði hleðsluáætlunar. Þessi möguleiki er gagnlegur fyrirtækjum sem vilja nota hugmyndina um farm til að rekja og áforma sendingu á vörum með flutningabíl/tengivagni, en vilja ekki búa til þessa farma handvirkt á hverjum degi.

Við bylgjuvinnslu býr kerfið venjulega til nýjan farm fyrir hverja sendingu þar sem engum farmi hefur verið úthlutað. Hinsvegar, þegar kveikt er á ítarlegri hleðsluáætlun bylgju, úthlutar kerfið hverri óúthlutaðri sendingu á fyrirliggjandi farm (ef viðeigandi farmur er til) og nýir farmar eru aðeins búnir til þegar á þarf að halda. Ítarleg hleðsluáætlun bylgju býr sjálfkrafa til nýja farma samkvæmt skilyrði sem notandi skilgreinir.

Til að nota eiginleikann þarf að setja upp kerfið á eftirfarandi hátt:

- Stofna *Bylgjusniðmát* sem innihalda nýju aðferðina **buildLoads**. Þessi aðferð býður upp á ítarlega hleðsluáætlun bylgju fyrir bylgjur sem nota þessi sniðmát.
- Setjið upp *sniðmát hleðsluáætlunar*, sem hvert fyrir sig er tengt tilteknu bylgjusniðmáti og aðferð. Sniðmát hleðsluáætlunar stjórna því í hvaða farmur (fyrirliggjandi eða nýjum) hleðslulínum bylgju verður bætt við. Hægt er að tengja saman eða aðskilja sendingar út frá skilyrðum á borð við hleðslusniðmát, búnað og öðrum reitargildum í farmlínunni.
- Skilgreinið *blöndunarflokka farma* til að stjórna því hvaða vörur eigi og eigi ekki að sameina í einum farmi. Einnig skal taka fram hvort takmörkunin eigi að skila viðvörun eða villu og hvort meta skuli rúmmálstakmörkun hleðslusniðmátsins.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Kveikja á ítarlegri hleðsluáætlun bylgju í kerfinu

Áður en hægt er að nota ítarlega hleðsluáætlun bylgju verður að kveikja á tveimur eiginleikum í kerfinu. Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu þessara eiginleika og kveikja á þeim ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** eru eiginleikarnir tilgreindir á eftirfarandi hátt:

- Eiginleiki hleðslusmíðarbylgju:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Eiginleiki hleðsluáætlunarbylgju*

- Stigskóði bylgju fyrir alla stofnunina/fyrirtækið:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Stigskóði bylgju fyrir alla stofnunina/fyrirtækið*

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessa sýnikennslu með því að nota sýniskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þessa sýniútgáfu sem leiðsögn um hvernig skuli nota þennan eiginleika þegar unnið er í framleiðslukerfi. Í slíku tilfelli þarf hinsvegar að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Gangið úr skugga um að uppsetning aðstæðna feli í sér nægar birgðir

Ef unnið er með sýnigögnin **USMF** þarf fyrst að ganga úr skugga um að kerfið sé sett upp með nægum birgðum á öllum viðeigandi staðsetningum. Fyrir þessa sýniútgáfu er væntingin sú að eftirfarandi birgðir séu tiltækar í vöruhúsi *62*:

- **Atriði A0001:** 10 stykki
- **Atriði A0002:** 10 stykki
- **Atriði M9200:** 10 ea

Bæta verður atriði **M9200** við vöruhúsið. Ljúkið ferlunum í eftirfarandi undirköflum til að bæta við vörubirgðunum.

#### <a name="create-a-new-license-plate-id"></a>Búa til nýtt kenni númeraplötu

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Vöruhús** \> **Númeraplötur**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í nýja línunni, í reitnum **Númeraplata**, skal slá inn *LP6203*.
1. Veljið **Vista**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Búa til staðalkostnað fyrir vöru M9200 á svæði 6

1. Farðu í **Afurðaupplýsingastjórnun** \> **Afurðir** \> **Losaðar afurðir**.
1. Leitið að **M9200**.
1. Veljið línu vörunnar og síðan á aðgerðasvæðinu, í flipanum **Stjórnun kostnaðar**, í flokknum **Uppsetning**, skal velja **Vöruverð**.
1. Á síðunni **Vöruverð** skal velja flipann **Biðverð**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Kostnaðargerð:** *Áætlaður kostnaður*
    - **Verðtegund** *Kostnaður*
    - **Útgáfa:** *10*
    - **Svæði:** *6*
    - **Verð:** *1.60*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Virkja biðverð**.
1. Veljið flipann **Virk verð** til að staðfesta að nýja kostnaðarverðinu fyrir svæði *6* hafi verið bætt við.

#### <a name="create-inventory-in-warehouse-62"></a>Búa til birgðir í vöruhúsi 62

1. Farið í **Birgðastjórnun** \> **Færslubókarfærslur** \> **Vörur** \> **Leiðrétting birgða**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svarglugganum **Stofna birgðabók**, í flýtiflipanum **Yfirlit**, í reitnum **Vöruhús** skal slá inn *62*. Samþykkið sjálfgefin gildi í öllum hinum reitunum.
1. Veldu **Í lagi** til að loka svarglugganum.
1. Síðan **Leiðrétting birgða** opnast. Í flýtiflipanum **Færslubókarlínur** skal velja **Ný** til að bæta við línu.
1. Stilltu eftirfarandi gildi á nýju línunni. Samþykkið sjálfgefin gildi í öllum hinum reitunum.

    - **Vörunúmer:** *M9200*
    - **Staðsetning:** *bulk-003*
    - **Magn:** Breytið gildinu í *10*.

1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Villuleita** til að skima eftir villum.
1. Í svarglugganum **Athuga færslubók** skal velja **Í lagi** til að hefja athugun. Skilaboð munu birtast þegar athugun lýkur.
1. Á aðgerðasvæðinu skal velja **Bóka** til að staðfesta leiðréttingu birgða.
1. Í svarglugganum **Bóka færslubók** skal velja **Í lagi** til að hefja bókun. Skilaboð munu birtast þegar bókun lýkur.

## <a name="set-up-advanced-wave-load-building"></a>Setja upp ítarlega hleðsluáætlun bylgju

### <a name="regenerate-wave-process-methods"></a>Endurgera vinnsluaðferðir bylgju

Hugsanlega þarf að endurgera vinnsluaðferðir bylgju til að bjóða upp á aðferð hleðsluáætlunar (**buildLoads**).

1. Farið í **Vöruhúsakerfi** \> **Uppsetning** \> **Bylgjur** \> **Vinnsluaðferðir bylgju**.
2. Gangið úr skugga um að **buildLoads** sé til staðar í listanum. Ef það er ekki til staðar skal velja **Endurgera aðferðir** á aðgerðasvæðinu til að bæta því við.

### <a name="set-up-wave-templates"></a>Setja upp bylgjusniðmát

Til að nýta sér ítarlega hleðsluáætlun bylgju þarf að láta aðferðina **buildLoads** fylgja með í öllum viðeigandi [bylgjusniðmátum](tasks/configure-wave-processing.md).

1. Fara í **Vöruhúsakerfi** \> **Upspetning** \> **Bylgjur** \> **Bylgjusniðmát**.
1. Veljið bylgjusniðmát.

    Ef unnið er með sýnigögnin **USMF** skal velja sniðmátið **Sjálfgefin sending 62**.

1. Á aðgerðasvæðinu skal velja **Breyta** til að færa síðuna yfir í breytingastillingu.
1. Í flýtiflipanum **Aðferðir**, í hnitanetinu **Aðferðir sem eftir standa**, skal velja aðferðina **buildLoads**.
1. Veljið hægri örvarhnappinn til að færa **buildLoads** aðferðina yfir í hnitanetið **Valdar aðferðir**.
1. Til að úthluta gildi **Stigskóða bylgju** fyrir **buildLoads** aðferðina þarf fyrst að stofna kóða á síðunni **Stigskóðar bylgju**. Hægt er að nota hvaða gildi sem er, en munið að leggja það á minnið því að nota þarf gildið seinna. Fylgið þessum skrefum til að stofna kóða **WSC2112**:

    1. Í línunni fyrir **buildLoads** aðferðina skal hægrismella á niðurörina í reitnum **Stigskóði bylgju** og velja síðan **Skoða upplýsingar**.
    1. Á síðunni **Stigskóðar bylgju**, á aðgerðasvæðinu, skal velja **Nýr**.
    1. Í reitinn **Stigskóði bylgju** skal slá inn *WSC2112*.
    1. Í reitinn **Lýsing á bylgjustigi** skal slá inn *WSC2112*.
    1. Í reitnum **Gerð bylgjustigs** skal velja *Hleðsluáætlun*.

1. Veljið **Vista** og lokið skjámyndinni.
1. Í línunni fyrir **buildLoads** aðferðina, í reitnum **Stigskóði bylgju**, skal velja kóðann sem var stofnaður (**WSC2112**).
1. Í aðgerðarúðunni skal velja **Vista**.

> [!NOTE]
> Stigskóðar bylgju eru kóðar sem notendur geta sett upp og notað til að tengja tiltekin tilvik bylgjuaðferðar við samsvarandi sniðmát. Sniðmátin innihalda sniðmát fyrir áfyllingu, gámagerð, prentun merkimiða, byggingu álags og flokkun.
>
> Þegar bylgjuskrefakóðar eru ekki notaðir, verða notendur að slá inn frjálsan texta til að vísa í ákveðið sniðmát frá bylgjuaðferðartilvikinu. Villur koma gjarnan upp í frjálsum texta því að notendur verða að ganga úr skugga um að texti bylgjustigs sem bætt er við fyrir tiltekna bylgjustigsaðferð í bylgjusniðmáti passi nákvæmlegi texta bylgjustigs í viðtökusniðmáti.
>
> Bylgjuskrefakóðar fyrir ákveðna gerð bylgjuskrefa eru settir upp á aðskildri síðu. Fyrir hvert tilvik bylgjustigsaðferðar í bylgjusniðmáti sem krefst stigskóða bylgju, verður að velja stigskóða bylgju í fellilista. Val í fellivalmynd kemur í staðinn fyrir frjálsan texta og hjálpar til við að draga úr hættu og áhrifum mannlegra mistaka. Uppsetningarkóðar eru notaðir til að tengja bylgjuþrep aðferð í bylgjusniðmát við marksnið fyrir aðferðina.

### <a name="set-up-load-mix-groups"></a>Setja upp blöndunarflokka farms

Blöndunarflokkar farms setja reglur fyrir þær tegundir af vörum sem hægt er að sameina í einum farmi. Hægt er að setja upp eins marga blöndunarflokka farms og þörf krefur. En til að nota ítarlega hleðsluáætlun bylgju verður að vera a.m.k. einn flokkur. Fylgið þessum skrefum til að stofna blöndunarflokk farms.

1. Farið í **Vöruhúsakerfi** \> **Uppsetning** \> **Farmur** \> **Blöndunarflokkar farms**.
1. Á aðgerðasvæðinu skal velja **Nýr** til að stofna nýjan hleðsluflokk.
1. Í reitinn **Kenni blöndunarflokks farms** skal slá inn heiti fyrir nýja flokkinn.

    Ef unnið er með sýnigögnin **USMF** skal stilla eftirfarandi gildi:

    - **Kenni blöndunarflokks farms:** *TV*
    - **Lýsing:** *TV*

1. Á aðgerðasvæðinu skal velja **Vista** til bjóða upp á flýtiflipann **Skilyrði blöndunarflokks farms**.
1. Í flýtiflipanum **Skilyrði blöndunarflokks farms** skal velja **Ný** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla æskileg gildi í hverjum reit. Þessi gildi ákvarða vöruflokkana sem koma til greina fyrir hleðslublönduna.

    Ef unnið er með sýnigögnin **USMF** skal velja *Sjónvarp og myndir* í reitnum **Vöruflokkur**.

1. Á aðgerðasvæðinu skal velja **Vista** til bjóða upp á flýtiflipann **Takmarkanir á blöndunarflokki farms**.
1. Í flýtiflipanum **Takmarkanir á blöndunarflokki farms** skal velja **Ný** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla æskileg gildi í hverjum reit.

    Ef unnið er með sýnigögnin **USMF** skal stilla eftirfarandi gildi:

    - **Vöruflokkur:** *CarAudio*
    - **Aðgerð hleðsluáætlunar:** *Takmarka* (Þetta gildi mun koma í veg fyrir að vörur sem tilheyra vöruflokknum **CarAudio** verði í sömu hleðslu og vörur sem tilheyra vöruflokknum **Sjónvarp og myndir**.)

1. Haldið áfram að vinna með reglurnar þangað til öllum skilyrðum og takmörkunum hefur verið bætt við sem þarf að nota fyrir blöndunarflokk farms.

Ef verið er að vinna með sýnigögnin **USMF**, er þessari uppsetningu lokið.

### <a name="set-up-load-build-templates"></a>Setja upp sniðmát hleðsluáætlana

Setja má upp eins mörg sniðmát hleðsluáætlana og þörf er á. En til að nota ítarlega hleðsluáætlun bylgju verður að vera a.m.k. einn flokkur. Fylgið þessum skrefum til að búa til sniðmát hleðsluáætlunar.

1. Farið í **Vöruhúsakerfi** \> **Uppsetning** \> **Farmur** \> **Sniðmát hleðsluáætlunarbylgju**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi.

    | Svæði | lýsing | Gildi í sýnigögnum USMF |
    |---|---|---|
    | Raðnúmer | Röðin sem sniðmátið verður metið í. | *1* |
    | Heiti farmsniðmáts | Sláðu inn einkvæmt kennimerki fyrir farmröðunarsniðmát. Færa ætti inn heiti sniðmátsins sem var búið til eða uppfært áður í þessari uppsetningu. | *Sjálfgefin sending 62* |
    | Kóði bylgjuskrefs | Sláið inn stigskóða bylgju sem nota á til að tengja sniðmátið við bylgjuaðferð. Færa ætti inn kóðann sem var valinn fyrir **buildLoads** aðferðina þegar bylgjusniðmátið var sett upp fyrr í þessari uppsetningu. | *WSC2112* |
    | Auðkenni hleðslusniðmáts | Veljið hleðslusniðmátið sem á að nota þegar nýir farmar eru búnir til og til að samsvara við þegar úthlutað er á fyrirliggjandi farma. Hleðslusniðmátið skilgreinir leyfilega hámarksþyngd og -rúmmál fyrir alla heildarhleðsluna. | *Staðlað hleðslusniðmát* |
    | Búnaður | Búnaðurinn til að samsvara við þegar úthlutað er á fyrirliggjandi farma og til að færa inn á nýja farma sem eru búnir til. | Hafa reitinn auðann. |
    | Kenni blöndunarflokks farms | Veljið blöndunarflokk farms sem á að nota ef varan er leyfð í hleðsluna. Blöndunarflokkurinn setur reglur fyrir þær tegundir af vörum sem hægt er að sameina í einum farmi. Velja ætti einn blöndunarflokk af þeim sem voru stofnaðir fyrr í þessari uppsetningu. | *Sjónvarp* |
    | Nota opna farma | Veljið hvort bæta eigi við fyrirliggjandi opnum förmum. Eftirtaldir valkostir eru í boði:<ul><li>**Enginn** – Ekki bæta opnum förmum við fyrirliggjandi farma.</li><li>**Hvern sem er** – Bætið opnum förmum við einhvern fyrirliggjandi farm sem gilda fyrir línuna.</li><li>**Úthlutaður** – Bætið opnum förmum við þann farm sem er úthlutað á bylgjuna.</li></ul> | *Hvaða sem er* |
    | Stofna hleðslur | Tilgreinið hvort búa eigi til nýja farma ef engir fyrirliggjandi farmar uppfylla skilyrðið. | Valinn (= *Já*) |
    | Leyfa skiptingu sendingarlínu | Tilgreinið hvort megi skipta einni farmlínu niður á marga farma ef öll línan fer yfir hámarksgetu hleðslusniðmátsins. | Hreinsað (= *Nei*) |
    | Staðfesta rúmmál | Tilgreinið hvort hleðsluáætlunin eigi að athuga þyngd og rúmmál í hvert skipti sem farmlínu er bætt við, til að tryggja að farið sé eftir rúmmálsmörkum hleðslusniðmátsins. | Hreinsað (= *Nei*) |

1. Á aðgerðasvæðinu skal velja **Vista** til að bjóða upp á valkostinn **Breyta fyrirspurn**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna svarglugga til að breyta fyrirspurninni.
1. Í svarglugganum, í flipanum **Röðun**, skal velja **Bæta við** til að bæta línu við hnitanetið.
1. Í nýju línunni skal skilgreina röðunarreglurnar sem á að nota. Til dæmis skal stilla eftirfarandi gildi til að raða leitarniðurstöðum í hækkandi röð eftir pöntunarnúmeri:

    - **Tafla:** *Upplýsingar um hleðslu*
    - **Afleidd tafla:** *Upplýsingar um hleðslu*
    - **Reitur:** *Pöntunarnúmer*
    - **Leitarstefna:** *Hækkandi*

1. Veljið **Í lagi** til að vista breytingarnar og loka svarglugganum.
1. Í flýtiflipanum **Skipta samkvæmt** skal setja reglur til að stýra því hvernig hleðslum er skipt upp. Yfirleitt er skipt í sérstilltum reitum sem hafa verið framlengdir yfir í farmlínuna, t.d. **Leið**, **Leiðsögn** eða **Keyra**. Sem dæmi, til að búa til eina hleðslu á pöntunarnúmer skal velja gátreitinn **Skipta samkvæmt** fyrir línuna sem er með eftirfarandi gildum:

    - **Heiti tilvísunartöflu:** *Upplýsingar um hleðslu*
    - **Heiti tilvísunarsvæðis:** *Pöntunarnúmer*

## <a name="scenario"></a>Aðstæður

Þessar aðstæður sýna hvernig stillingarnar, sem lýst var fyrr í þessu efnisatriði, hafa áhrif á vöruhúsaaðgerðir á meðan unnið er úr sölupöntun. Þessar aðstæður nota sýnigögnin **USMF** ásamt öðrum sýnigildum sem þessar uppsetningarleiðbeiningar bjóða upp á.

### <a name="create-sales-orders"></a>Stofna sölupöntun

1. Farðu í **Sölu og markaðssetningu** \> **Sölupantanir** \> **Allar sölupantanir**.
1. Á aðgerðasvæðinu skal velja **Ný** til að opna svargluggann **Stofna sölupöntun**.
1. Í svarglugganum skal stilla eftirfarandi gildi:

    - Í flýtiflipanum **Viðskiptavinur** skal stilla reitinn **Viðskiptavinalykill** á *US-007*.
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *62*.

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Nýja sölupöntunin þín opnast. Hún ætti að innihalda nýja, auða línu í hnitanetinu í flýtiflipanum **Sölupöntunarlínur**. Í þessari nýju línu skal stilla reitinn **Vörunúmer** á *A0001* og reitinn **Magn** á *1*.
1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota**.
1. Veljið hnappinn **Loka** (**X**) efst í hægri horni síðunnar til fara aftur í sölupöntunina.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**. Kerfið stofnar sendingu og bætir henni við nýjan farm því að enginn fyrirliggjandi farmur inniheldur farmlínur með þessu pöntunarnúmeri.

    Send verða upplýsandi skilaboð sem gefa upp verkið, bylgjuna og sendinguna sem stofnuð eru fyrir þessa pöntun.

1. Til að staðfesta upplýsingar um hleðsluna, sendinguna og verkið í sölulínunni skal velja línuna og síðan, í valmyndinni **Vöruhús** fyrir ofan hnitanetið, skal velja **Upplýsingar um hleðslu**, **Upplýsingar um sendingu** eða **Upplýsingar um verk**.
1. Í sölupöntuninni sem var nýverið stofnuð, í flýtiflipanum **Sölupöntunarlínur**, skal velja **Bæta við línu** til að bæta við annarri línu.
1. Í nýju línunni skal stilla reitinn **Vörunúmer** á *A0002* og reitinn **Magn** á *1*.
1. Endurtakið línur 6 til 9 til að taka línuna frá og losa hana í vöruhúsið. Kerfið stofnar **nýja** sendingu fyrir línuna sem bætt var við. Hins vegar, því notuð er ítarleg hleðsluáætlun bylgju, bætir kerfið þessari sendingu og framlínu við fyrirliggjandi bylgju. Ef ekki væri notuð ítarleg hleðsluáætlun bylgju myndi kerfið stofna nýja hleðslu fyrir sendinguna.
1. Í sölupöntuninni sem var nýverið stofnuð, í flýtiflipanum **Sölupöntunarlínur**, skal velja **Bæta við línu** til að bæta við annarri línu.
1. Í nýju línunni skal stilla reitinn **Vörunúmer** á *M9200* og reitinn **Magn** á *1*.
1. Endurtakið línur 6 til 9 til að taka línuna frá og losa hana í vöruhúsið. Líkt og áður, stofnar kerfið **nýja** sendingu fyrir línuna sem bætt var við. En vegna þess að varan er í vöruflokknum **CarAudio** **nær varan ekki að uppfylla takmarkanirnar sem settar voru upp fyrir blöndunarflokk hleðslunnar**. Þar af leiðandi er henni **bætt við nýja hleðslu**. Ef ekki hefði verið tilgreindur blöndunarflokkur farms í sniðmáti hleðsluáætlunar, hefði þessari sendingu verið bætt við fyrstu hleðsluna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
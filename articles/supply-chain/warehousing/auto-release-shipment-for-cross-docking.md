---
title: Losa sendingu sjálfkrafa fyrir dreifingu frá dreifingarstöð
description: Þetta efni lýsir stefnu um dreifingu frá dreifingarstöð sem gerir þér kleift að sleppa sjálfkrafa eftirspurnarpöntun á lager þegar framleiðslupöntunin sem veitir eftirspurnarmagnið er tilkynnt sem lokið, þannig að magnið er fært beint frá framleiðslustað til staðsetningar á útleið.
author: omulvad
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c831030659b38b52932e504f744d24d999958a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831435"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Losa sendingu sjálfkrafa fyrir dreifingu frá dreifingarstöð

[!include [banner](../includes/banner.md)]

Þetta efni lýsir stefnu um dreifingu frá dreifingarstöð sem gerir þér kleift að sleppa sjálfkrafa eftirspurnarpöntun á lager þegar framleiðslupöntunin sem veitir eftirspurnarmagnið er tilkynnt sem lokið. Þannig er magnið sem þarf til að uppfylla eftirspurnarpöntunina fært beint frá framleiðslustaðnum á útleiðarstað.

Dreifing frá dreifingarstöð er vöruflæðisafgreiðsla þar sem magnið sem þarf til að uppfylla pöntun á útleið er beint að úthlið eða sviðsetningarsvæði pöntunarinnar frá þeim stað þar sem pöntun á innleið var móttekin. (Pöntun á innleið getur verið innkaupapöntun, flutningspöntun eða framleiðslupöntun.) Þar eð styður eiginleikinn Ítarleg dreifing frá dreifingarstöð allar framboðs- og eftirspurnarpantanir og það krefst þess að eftirspurnin verði send út áður en tækifæri til dreifingar frá dreifingarstöð er fundið hefur Sjálfvirk losun þessa eiginleika:

- Hún styður aðeins framleiðslupantanir sem birgðir og aðeins sölupantanir og flutningspantanir sem eftirspurn.
- Hægt er að hefja dreifingu frá dreifingarstöð jafnvel þó að eftirspurnarpöntun hafi ekki verið sleppt á lager áður en birgðakvittun var skráð (það er að segja, áður en framleiðslan var tilkynnt sem lokið).

Þessi virkni fyrir dreifingu frá dreifingarstöð hefur tvo kosti:

- Vöruhúsaaðgerðirnar geta sleppt því að ganga frá magn fullunninna vara í almennu geymslusvæði vöruhúss ef það magn verður aðeins sótt aftur til að uppfylla pöntun á útleið. Í staðinn er hægt að færa magnið einu sinni, frá framleiðslustaðnum til pökkunar-/flutningsstaðar. Þannig hjálpar virknin til að lágmarka þann fjölda skipta sem birgðir eru meðhöndlaðar og á endanum við að hámarka tíma- og rýmissparnað í vinnslusal vöruhúss.
- Vöruhússaðgerðirnar geta frestað losun sölupantana og flutningspantana í vöruhúsið þar til að úttak fullunninna vara fyrir tengda framleiðslupöntun er tilkynnt sem lokið. Þessi kostur gæti verið sérstaklega viðeigandi í framleiðsluumhverfi framleiðslu eftir pöntun þar sem afhendingartími framleiðslu hefur tilhneigingu til að vera lengri en afhendingartímar í umhverfi fyrir framleiðslu á lager.

## <a name="prerequisites"></a>Forkröfur

| Skilyrði | Lýsing |
|---|---|
| vara | Varan verður að vera virkur fyrir vöruhúsakerfisferli.<p>**Ath.:** Ekki er hægt að taka hluti með framleiðsluþyngd með í ferlum dreifingar frá dreifingarstöð.</p> |
| Vöruhús | Vöruhús verður að vera virkur fyrir vöruhúsakerfisferli. |
| Sniðmát dreifingar frá dreifingarstöð | Að minnsta kosti eitt sniðmát dreifingar frá dreifingarstöð sem notar stefnu um losun eftirspurnar **Við birgðakvittun** verður að vera uppsett fyrir tiltekið vöruhús. |
| Vinnuklasi | Stofna verður kenni vinnuklasa fyrir dreifingu frá dreifingarstöð fyrir verkbeiðnigerðina **Dreifing frá dreifingarstöð**. |
| Vinnusniðmát | Vinnusniðmát af verkbeiðnigerðinni **Dreifing frá dreifingarstöð** þarf til að stofna vinnu fyrir tiltekt og frágang dreifingar frá dreifingarstöð. |
| Staðsetningarleiðbeiningar | Staðsetningarleiðbeininga verkbeiðnigerðarinnar **Dreifing frá dreifingarstöð** er krafist til að leiðbeina um frágangsvinnu á þeim stöðum þar sem sölupantanamagni verður pakkað og flutt. |
| Merking milli eftirspurnarpöntunar og framleiðslupöntunar | Vöruhúsakerfið getur aðeins hrundið af stað sjálfvirkri losun á sendingu pöntunar á útleið og búið til vinnu dreifingar frá dreifingarstöð frá framleiðslustaðnum við aðgerðina Tilkynna sem lokið, ef sölupantanir og flutningspantanir eru fráteknar og merktar gegn framleiðslupöntun. |

## <a name="example-cross-docking-flow"></a>Dæmi um flæði dreifingar frá dreifingarstöð

Dæmigert flæði fyrir dreifingu frá dreifingarstöð samanstendur af eftirfarandi meginþrepum.

1. Sölupöntunaraðili stofnar sölupöntun fyrir vöru sem er framleidd eftir pöntun. Venjulega er umbeðið magn ekki til staðar og verður fyrst að vera framleitt.
2. Sölupöntunaraðili stofnar framleiðslupöntun beint úr sölupöntunarlínunni. Á þennan hátt tekur sölupöntunaraðili frá og merkir sölupöntunarmagnið á móti framleiðslupöntunarmagninu. 

    Að öðrum kosti tilgreinir framleiðslustjórinn að merkingin skuli uppfærð þegar áætlaðar pantanir eru staðfestar.

3. Framleiðslupöntunin fer í gegnum eftirfarandi skref:

    1. Framleiðslustjórinn áætlar og losar framleiðslupöntunina. (Áætlun felur í sér frátekningu á hráefni og losunin felur í sér losun í vöruhús.)
    2. Starfskraftur í vöruhúsi hefur og lýkur tiltekt hráefna af geymslustað til staðsetningar framleiðsluinntaksr, í samræmi við tiltektarvinnu framleiðslu.
    3. Virknitákn vinnslusalar byrjar framleiðslupöntunina.
    4. Í síðustu aðgerðinni notar starfssmaður á vél fartækið til að tilkynna framleiðslupöntunina sem lokið.

4. Kerfið notar uppsetninguna til að bera kennsl á tilvik dreifingar frá dreifingarstöð fyrir tvær tengdar pantanir og lýkur síðan þessum verkefnum:

    1. Losar sjálfkrafa tengda sölupöntun í vöruhús til að búa til sendingu.
    2. Stofnaðu sjálfkrafa vinnu dreifingar frá dreifingarstöð sem er með leiðbeiningar um að velja fullunnar vörur frá framleiðslustaðnum og færa þær á útleiðarstað sem staðsetningartilskipanir dreifingar frá drefingarstöð hafa úthlutað til sölupöntunarinnar.
    3. Biddu stjórnanda vélar að ljúka vinnu dreifing frá dreifingarstöð strax eftir að framleiðslupöntunin er tilkynnt sem lokið.

5. Þegar vinnu dreifingar frá dreifingarstöð er lokið og magninu er hlaðið á ökutækið staðfestir áætlunarstjóri vöruhúss á útleið sölusendinguna.

## <a name="example-scenario"></a>Dæmi

Fyrir þessa atburðarás verður þú að hafa kynningargögn sett upp og þú verður að nota kynningarfyrirtækið **USMF**.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Settu upp dreifingu frá dreifingarstöð sem notar eiginleikann Losa sendingu sjálfkrafa

#### <a name="cross-docking-template"></a>Sniðmát dreifingar frá dreifingarstöð

1. Farðu í **Vöruhúsastjórnun** \> **Uppsetning** \> **Vinna** \> **Sniðmát dreifingar frá dreifingarstöð**.
2. Veljið **Nýtt**.
3. Í reitinn **Raðarnúmer** skal rita **1**.
4. Í reitinn **Kenni dreifingar frá dreifingarstöð** skaltu rita heiti, svo sem **XDock\_RAF**.
5. Í reitnum **Stefna um losun eftirspurnar** velurðu **Við birgðakvittun**.
6. Í reitinn **Vöruhús** slærðu inn númer vöruhússins þar sem þú vilt setja upp ferli dreifingar frá dreifingarstöð. Í þessu dæmi velurðu **51**.

    > [!NOTE]
    > Um leið og þú velur **Við birgðakvittun** sem stefnu um losun eftirspurnar fyrir sniðmátið verða allir aðrir reitir á síðunni ótiltækir. Á sama hátt geturðu ekki skilgreint nein birgðatilföng. Þessi hegðun á sér stað vegna þess að dreifing frá dreifingarstöð sem notar eiginleika fyrir sjálfvirka losun sendinga styður aðeins framleiðslupantanir sem birgðatilföng og hún krefst þess að merking sé á milli sölupantana og framleiðslupantana. Ef þú velur **Á undan birgðakvittun** sem stefnu um losun eftirspurnar eru reitirnir á flipunum **Áætlun** og **Birgðatilföng** eru tiltækir og hægt er að breyta þeim.

#### <a name="work-classes"></a>Vinnuklasar

1. Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Vinna** \> **Vinnuklasar**.
2. Veljið **Nýtt**.
3. Í reitinn **Auðkenni vinnuflokks** skaltu slá inn heiti, eins og **CrossDock**.
4. Í reitnum **Gerð verkbeiðni** velurðu **dreifingu frá dreifingarstöð**.

Til að takmarka gerðir staðsetninga þar sem hægt er að setja fullbúnar vörur í dreifingu frá dreifingarstöð er hægt að tilgreina eina eða fleiri gildar tegundir staðsetninga.

#### <a name="work-templates"></a>Vinnusniðmát

1. Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Vinna** \> **Vinnusniðmát**.
2. Í reitnum **Gerð verkbeiðni** velurðu **dreifingu frá dreifingarstöð**.
3. Veljið **Nýtt**.
4. Í reitinn **Raðarnúmer** skal rita **1**.
5. Í reitinn **Vinnusniðmát** skaltu rita heiti, eins og **CrossDock\_51**.
6. Veljið **Vista**.
7. Í hlutanum **Upplýsingar vinnusniðmáts** velurðu **Nýtt**.
8. Fyrir nýju línuna skaltu í reitnum **Vinnugerð** velja **Taka til**. Í reitnum **Kenni vinnuklasa** skal velja **CrossDock**.
9. Veljið **Nýtt**.
10. Fyrir nýju línuna skaltu í reitnum **Vinnugerð** velja **Frágangur**. Í reitnum **Kenni vinnuklasa** skal velja **CrossDock**.

#### <a name="location-directives"></a>Staðsetningarleiðbeiningar

Staðlað frágangsferli fyrir fullunna vöru krefst staðsetningarleiðbeininganna **Frágangur** til að leiðbeina flutningi tiltekins framleiðslumagns að venjulegu geymslurými. Sömuleiðis verður að setja upp staðsetningarleiðbeiningar dreifingar frá dreifingarstöð **Frágangur** til að leiðbeina verkinu um að setja fullbúið magn á tilgreindan útgöngustað sem þjónustar sendingu á tengdri sölupöntun.

Hvað varðar dreifingu frá dreifingarstöð, eins og venjulegan frágang á fullunnum vörum, þarftu ekki að stofna staðsetningarleiðbeiningar fyrir frágangsaðgerðina vegna þess að frálagsstaðurinn er gefinn. Að auki er búist við að þessi frálagsstaður verði settur upp annaðhvort sem sjálfgefinn frálagsstaður í einni af tilfangatengdum skrám (það er, tilföngum, tengslum tilfangahóps eða tilfangahópnum) eða sem sjálfgefin staðsetning fullunninna vara fyrir vöruhús.

1. Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Staðsetningarleiðbeiningar**.
2. Í reitnum **Gerð verkbeiðni** velurðu **dreifingu frá dreifingarstöð**.
3. Veljið **Nýtt**.
4. Í reitinn **Raðarnúmer** skal rita **1**.
5. Í reitinn **Nafn** skal slá inn heiti, eins og **Baydoor**.
6. Í reitnum **Verkbeiðni** velurðu **Frágangur**.
7. Í reitnum **Svæði** skal velja **5**.
8. Í reitnum **Vöruhús** skal velja **51**.
9. Á flipanum **Línur** velurðu **Nýtt**.
10. Í reitinn **Til-magn** slærðu inn hámarksmagn sviðsins, eins og **1000000**.
11. Veljið **Vista**.
12. Á flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** velurðu **Nýtt**.
13. Í reitinn **Nafn** skal slá inn heiti, eins og **Baydoor**.
14. Veljið **Vista**.
15. Þú getur notað stöðluðu fyrirspurnaraðstöðuna til að takmarka frágangsstaðsetningar við einn eða fleiri ákveðna staði. Veldu **Breyta fyrirspurn** og veldu **51** sem viðmiðun fyrir reitinn **Vöruhús** í töflunni **Staðsetningar**.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Dreifa fullunnum vörum til staðsetningar á útleið.

Fylgdu þessum skrefum til að dreifa magni fullunninna vara frá dreifingastöð til staðsetningar á útleið fyrir tengda sölupöntun.

1. Farðu í **Sölu og markaðssetningu** \> **Sölupantanir** \> **Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Fyrir haus sölupöntunar velurðu viðskiptavinalykil **US-001** og vöruhús sem er sett upp fyrir dreifingu frá dreifingarstöð sem notar eiginleikann Losa sendingu sjálfkrafa.
4. Bættu við línu fyrir fullunna vöru og sláðu inn **10** sem magnið.
5. Í hlutanum **Sölupöntunarlínur** velurðu **Afurð og framboð** \> **Framleiðslupöntun**.
6. Í valmyndinni **Stofna framleiðslupöntun** skoðarðu sjálfgefin gildi og velur síðan **Stofna**. Ný framleiðslupöntun er búin til og tengd sölupöntuninni (þ.e.a.s., hún er frátekin og merkt).
7. Valfrjálst: Breyttu gildinu í reitnum **Magn** þannig að það sé hærra en það gildi sem þarf til að uppfylla sölupöntunina. Þegar greint er frá framleiðslumagni sem fullgerðu mun kerfið búa til vinnu dreifingar frá dreifingarstöð fyrir merkt magn og frágangsvinnu fyrir eftirstandandi magn samkvæmt venjulegri aðferð til að meðhöndla frágang á fullunnum vörum.

    Eins og áður var getið þarf merking að vera til staðar á milli sölupöntunar og framleiðslupöntunar. Annars virkar dreifing frá dreifingarstöð ekki. Hægt er að búa til merkingu á marga vegu:

    - Kerfið getur sjálfkrafa búið til merkingar við eftirfarandi aðstæður:

        - Framleiðslupöntun er stofnuð beint úr sölupöntunarlínunni (sjá 6. skref).
        - Áætlaðar framleiðslupantanir eru staðfestar og reiturinn **Uppfæra merkingu** er stilltur á **Staðlað**.

    - Notandinn getur búið til merkinguna handvirkt með því að opna síðuna **Merking** úr röð eftirspurnarpöntunar.

    > [!NOTE]
    > Ekki er hægt að búa til merkingu handvirkt fyrir vörur sem eru settar upp til að nota staðlað og vegið meðaltal sem birgðalíkön.

8. Á síðunni **Framleiðslupöntun**, á aðgerðarrúðunni, á flipanum **Framleiðslupöntun**, í hópnum **Ferli**, velurðu **Mat** og veldu síðan **Í lagi**. Pöntunin er metin og magn hráefnis er frátekið fyrir framleiðsluna.
9. Í aðgerðarúðunni, á flipanum **Framleiðslupöntun**, í hópnum **Ferli**, velurðu **Losa**, og síðan velurðu **Í lagi**. Tiltektarvinna vöruhúss er búin til fyrir hráefnin.
10. Opnaðu og skoðaðu verkið. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Almennt** skaltu velja **Upplýsingar um vinnu**. Skráið niður vinnukennið.
11. Skráðu þig inn í farsímaforrit vöruhúsakerfis til að keyra verk í vöruhúsi 51.
12. Fara til **Framleiðsla** \> **Framleiðslutiltekt**.
13. Sláðu inn vinnukennið til að hefja og ljúka við hráefnistiltektina. 

    Eftir að verkið er tilkynnt sem lokið er magn hráefna fáanlegt á inntaksstað framleiðslunnar (**005** í USMF kynningargagna) og framkvæmd framleiðslupöntunar getur byrjað.

14. Á síðunni **Framleiðslupöntun**, á aðgerðarrúðunni, á flipanum **Framleiðslupöntun**, í hópnum **Ferli**, velurðu **Hefja** og veldu síðan **Í lagi**.
15. Í forritinu ferðu í **Framleiðsla** \> **RAF og frágangur**.
16. Í reitinn **Vörukenni** slærðu inn framleiðslupöntunarnúmerið og aðrar skyldubundnar upplýsingar og velur síðan **Í lagi**.

Athugaðu að eftirfarandi atburðir eiga sér stað:

- Losun í vöruhús virkjast fyrir tengda sölupöntun.
- Sendingar- og dreifingarvinna frá dreifingarstöð er stofnuð og byggist á losuninn. Þessi vinna leiðbeinir starfsmanni í vöruhúsi með að velja það magn sem þarf til að uppfylla sölupöntunarlínuna og setja það á staðsetningu á útleið sem tilgreind er í leiðbeiningum um dreifingu frá dreifingarstöð.
- Ef magn framleiðslupöntunar er meira en það magn sem þarf í sölupöntuninni er regluleg frágangsvinna stofnuð. Þessi vinna leiðbeinir starfsmanni vöruhúss með að taka frá magn af fullunnum vörum sem er eftirstandandi eftir dreifingu frá dreifingarstöð og færa það í venjulega geymslu, samkvæmt staðsetningarleiðbeiningunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Sveigjanleg frátektarregla á vídd vöruhúsastigs
description: Þetta efni lýsir stefnuskrá fyrir birgða sem láta fyrirtæki sem selja vörur sem eru rekin með runur og reka flutninga sína sem aðgerðir með WMS-virka áskilja sértækar runur fyrir sölupantanir viðskiptavina, jafnvel þó að pöntunarveldið sem er tengt vörunum banni ekki fyrirvara á tilteknum runum.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c0baf96315dd9fe6bc1984d337fd1c50ae47016a
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031044"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Sveigjanleg frátektarregla á vídd vöruhúsastigs

[!include [banner](../includes/banner.md)]

Þegar stigveldi birgða fyrirvara á „hópnum hér að neðan\[staðsetningu\]„ gerð er tengd vörum, fyrirtækjum sem selja vöru sem er rekin með hópum og rekur flutninga sína sem aðgerðir sem eru gerðar virkar fyrir Microsoft Dynamics 365 Warehouse Management System (WMS) getur ekki pantað sértæka runu af þessum vörum fyrir sölupantanir viðskiptavina. Þetta efnisatriði lýsir stefnuskráningu birgða sem gerir þessum fyrirtækjum kleift að panta sértækar runur, jafnvel þegar vörurnar eru tengdar „hópi hér að neðan\[staðsetningu\]" stigveldi fyrirvara.

## <a name="inventory-reservation-hierarchy"></a>Frátekningarstigveldi birgða

Þessi hluti dregur saman núverandi stigveldi birgða fyrirvara. Það beinir sjónum að því hvernig meðhöndlaðir eru hlutar í hópum og raðnúmerum.

Stigveldi birgðapöntunar ræður því að hvað varðar geymsluvíddir ber eftirspurnarpöntunin nauðsynlegar víddir á staðsetningu, vörugeymslu og birgðastöðu, en rökfræði vörugeymslu er ábyrg fyrir því að tengja staðsetningu við umbeðið magn og panta staðsetningu. Með öðrum orðum, í samskiptum milli eftirspurnarpöntunar og vörugeymslu er gert ráð fyrir að eftirspurnarpöntunin gefi til kynna hvar pöntunin verður að vera send frá (það er, hvaða staður og vörugeymsla). Vöruhúsið treystir síðan á rökfræði þess til að finna nauðsynlegt magn í húsnæði vörugeymslu.

Hins vegar, til að endurspegla rekstrarlíkan fyrirtækisins, eru mælingar á stærð (runu og raðnúmer) háð meiri sveigjanleika. Stigveldi birgðapöntunar rúmar atburðarás þar sem eftirfarandi skilyrði eiga við:

- Fyrirtækið treystir á vörugeymslu sína til að stjórna töku á magni sem hefur lotu eða raðnúmer eftir að magnið hefur fundist í geymsluhúsnæðinu. Oft er vísað til þessa líkans *Hópur-neðan\[staðsetningu\]*. Það er venjulega notað þegar framleiðslueining vöru eða raðnúmer er ekki mikilvægt fyrir viðskiptavini sem setja eftirspurnina hjá sölufyrirtækinu.
- Ef lotu- eða raðnúmer eru hluti af pöntunarlýsingu viðskiptavinarins og þau eru skráð í eftirspurnarpöntun, eru vörugeymsluaðgerðirnar sem finna magn í vöruhúsinu takmarkaðar af sérstökum númerum sem óskað er eftir og hafa ekki leyfi til að breyta þeim. Vísað er til þessa líkans *Hópur-ofan\[staðsetningu\]*.

Í þessum atburðarásum er áskorunin sú að aðeins er hægt að úthluta einum birgða pöntunarveldi fyrir hverja vöru sem gefin er út. Þess vegna, fyrir WMS til að meðhöndla rakta hluti, eftir að stigveldi verkefnisins ákvarðar hvenær á að panta lotu eða raðnúmer (annað hvort þegar eftirspurnarpöntunin er tekin eða meðan á pökkunarvinnu vörugeymslu stendur), er ekki hægt að breyta þessari tímasetningu í auglýsingu -hoc grundvöllur.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Sveigjanlegur fyrirvari fyrir hluti sem rekja má hóp

### <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Í þessari atburðarás notar fyrirtæki birgðarstefnu þar sem fullunnum vörum er rakið eftir lotunúmerum. Þetta fyrirtæki notar einnig WHS vinnuálag. Vegna þess að þetta vinnuálag hefur vel útbúna röksemdafærslu til að skipuleggja og keyra vörugeymslu og flutningsaðgerðir fyrir hluti sem eru búnir til í hópum eru flestir fullbúnir hlutir tengdir „hópur hér að neðan\[staðsetningu\]" stigveldi birgða fyrirvara. Kosturinn við þessa tegund rekstraruppsetningar er að ákvörðunum (sem eru í raun fyrirvara um fyrirvaralausar ákvarðanir) um hvaða runur á að velja og hvar eigi að setja þær í vörugeymslunni er frestað þangað til að vörugeymsla hefst. Þeir eru ekki gerðir þegar pöntun viðskiptavinarins er sett.

Þó að „hópurinn hér að neðan\[staðsetningu\]„ Pöntunarveldi þjónar vel markmiðum fyrirtækisins, margir af rótgrónum viðskiptavinum fyrirtækisins þurfa sömu lotu og þeir keyptu áður þegar þeir panta vörur. Þess vegna er fyrirtækið að leita að sveigjanleika í meðhöndlun reglna um röðun pöntunar svo að eftir atvikum viðskiptavina eftir sama hlut, gerist eftirfarandi hegðun:

- Hægt er að skrá lotunúmer og panta þegar pöntunin er tekin af söluaðilanum og ekki er hægt að breyta því við vörugeymslu og / eða taka af öðrum kröfum. Þessi hegðun hjálpar til við að tryggja að lotunúmerið sem var pantað er sent til viðskiptavinarins.
- Ef lotunúmerið er ekki mikilvægt fyrir viðskiptavininn, þá geta vörugeymsluaðgerðir ákvarðað lotunúmer meðan á vinnu stendur, eftir að skráning og pöntun sölupöntunar hefur verið gert.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Leyfa fyrirvara um ákveðna lotu í sölupöntuninni

Til að koma til móts við æskilegan sveigjanleika í hegðun hóps fyrirvara fyrir hluti sem eru tengdir „hópur hér að neðan\[staðsetningu\]" stigveldi birgða fyrirvara, birgðasali verður að velja **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn fyrir **Hópnúmer** stig á **Stigveldi birgða fyrirvara** síðu.

![Stigveldi fyrir birgðafrátektir gert sveigjanlegt](media/Flexible-inventory-reservation-hierarchy.png)

Þegar stigið **Rununúmer** í stigveldinu er valið, allar víddir yfir því stigi og upp í gegnum **Staðsetning** stig verður sjálfkrafa valið. (Sjálfgefið að allar víddir yfir **Staðsetning** stig eru valin.) Þessi hegðun endurspeglar rökfræði þar sem allar víddir á bilinu milli lotunúmers og staðsetningar eru einnig sjálfkrafa fráteknar eftir að þú hefur pantað tiltekið lotunúmer á pöntunarlínunni.

> [!NOTE]
> Gátreiturinn **Leyfa fyrirvara á pöntunarbeiðni** á aðeins við um stig stigveldis sem er undir staðsetningu víddar vörugeymslu.
>
> **Rununúmer** er eina stigið í stigveldinu sem er opið fyrir sveigjanlega pöntunarstefnu. Með öðrum orðum, þú getur ekki valið gátreiturinn **Leyfa fyrirvara á pöntunarbeiðni** fyrir **Staðsetning**, **Númeraplata**, eða **Raðnúmer** stigi.
>
> Ef pöntunarveldið þitt inniheldur röð raðnúmera (sem verður alltaf að vera undir **Rununúmer** stig), og ef þú hefur kveikt á lotusértækum fyrirvara fyrir lotunúmerið mun kerfið halda áfram að sjá um röðun og tína aðgerðir á raðnúmerum, byggt á reglunum sem eiga við um „Rað-neðan\[staðsetningu\]" fyrirvara stefnu.

Hvenær sem er geturðu leyft lotusértæka pöntun fyrir núverandi „runu hér að neðan\[staðsetningu\]" pöntunarveldi í uppsetningu þinni. Þessi breyting mun ekki hafa áhrif á neina fyrirvara og opna vöruhúsavinnu sem voru búin til áður en breytingin átti sér stað. Hins vegar **Leyfa fyrirvara á pöntunarbeiðni** Ekki er hægt að hreinsa gátreitinn ef birgðafærslur á **Frátekið pantað**, **Frátekin líkamleg**, eða **Pantaði** útgáfutegund er til fyrir einn eða fleiri hluti sem eru tengdir því pöntunarveldi.

> [!NOTE]
> Ef núverandi fyrirvaralegveldi hlutar leyfir ekki forskrift lotur í pöntuninni, þá geturðu endurúthlutað því í pöntunarveldi sem gerir kleift að skilgreina lotu, að því tilskildu að stigskipulag stigveldisins sé það sama í báðum stigveldum. Nota **Breyta pöntunarveldi fyrir hluti** virka til að framkvæma endurúthlutun. Þessi breyting gæti skipt máli þegar þú vilt koma í veg fyrir sveigjanlegan pöntunarhluta fyrir hlutmengi af hlutum sem eru rekin í hópum en leyfa það fyrir restina af vöruframboði.

Óháð því hvort þú hefur valið **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn, ef þú vilt ekki panta sérstakt lotunúmer fyrir hlutinn á pöntunarlínu, þá er sjálfgefin rökfræði aðgerða vörugeymsla sem gildir fyrir „Hóp hér að neðan\[staðsetningu\]" fyrirkomulag stigveldi mun enn eiga við.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Pantaðu tiltekið lotunúmer fyrir pöntun viðskiptavina

Eftir hlut sem er rekja hópur er „Hópur hér að neðan\[staðsetningu\]„ Stigveldi birgðapöntunar er sett upp til að leyfa fyrirvara á tilteknum lotunúmerum á sölupöntunum, sölupöntunaraðilar geta tekið pantanir viðskiptavina fyrir sama hlut á einn af eftirfarandi leiðum, allt eftir beiðni viðskiptavinarins:

- **Sláðu inn pöntunarupplýsingar án þess að tilgreina lotunúmer** - Þessa nálgun ætti að nota þegar framleiðslulota vöru er ekki mikilvæg fyrir viðskiptavininn. Allir núverandi ferlar sem tengjast meðhöndlun pöntunar af þessari gerð kerfisins eru óbreytt. Engin viðbótarsjónarmið eru nauðsynleg af hálfu notenda.
- **Sláðu inn pöntunarupplýsingar og pantaðu tiltekið lotunúmer** - Þessa aðferð ætti að nota þegar viðskiptavinurinn óskar eftir ákveðinni lotu. Venjulega munu viðskiptavinir biðja um ákveðna lotu þegar þeir eru að panta vöru sem þeir keyptu áður. Þessari tegund af sértækum pöntunum er vísað til *pöntunarbundinn fyrirvara*.

Eftirfarandi reglur eru í gildi þegar magn er afgreitt og lotunúmer er skuldbundið til sérstakrar pöntunar:

- Til að leyfa fyrirvara á ákveðnu lotunúmeri fyrir hlut undir „Hópur hér að neðan\[staðsetningu\]" pöntunarstefna, kerfið verður að panta allar víddir upp í gegnum staðsetningu. Þetta svið inniheldur venjulega stærð skírteinisins.
- Staðsetningartilskipanir eru ekki notaðar þegar val á vinnu er búið til fyrir sölulínu sem notar pöntunarbundna hópapöntun.
- Við vinnslu vörugeymslu á vinnu fyrir pöntunarbundna lotur er hvorki notanda né kerfinu heimilt að breyta lotunúmerinu. (Þessi vinnsla felur í sér meðhöndlun undantekninga.)

Eftirfarandi dæmi sýnir flæði frá enda til enda.

## <a name="example-scenario"></a>Dæmi

Fyrir þetta dæmi verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a>Setjið upp stigveldi birgða fyrirvara til að leyfa ákveðna pöntun

1. Fara til **Vöruhúsastjórnun** \> **Skipulag** \> **Birgðir \> Pöntunarveldi**.
2. Veljið **Nýtt**.
3. Í reitnum **Heiti** skaltu slá inn nafn (til dæmis **BatchFlex**).
4. Í reitinn **Lýsing** slærðu inn lýsingu (t.d. **Hópur fyrir neðan sveigjanlegan**).
5. Í reitinn **Valinn**, veldu **Raðnúmer** og **Eigandi** og veldu síðan vinstri örvarhnappinn til að færa þá í reitinn **Tiltækt**.
6. Veljið **Í lagi**.
7. Í röðinni fyrir **Hópnúmer** víddarstig, veldu **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn. Stigin **Númeraplata** og **Staðsetning** eru sjálfkrafa valin og þú getur ekki hreinsað gátreitina fyrir þá.
8. Veljið **Vista**.

### <a name="create-a-new-released-product"></a>Stofna nýja útgefna afurð

1. Stilltu þrjár aðalgagnabreytur vörunnar með því að nota þessi gildi:

    - Í reitnum **Geymsluvíddarflokkur** velurðu **Ware**.
    - Í reitnum **Rakningarvíddarflokkur** velurðu **Batch-Phy**.
    - Í skjámyndinni **Frátektastigveldi** velurðu **BatchFlex**.

2. Búðu til tvö lotunúmer, svo sem **B11** og **B22**.
3. Bættu magni hlutar við á lager með því að nota eftirfarandi gildi.

    | Vöruhús | Rununúmer | Staðsetning | Númeraplata | Magn |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Enginn          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a>Slá inn upplýsingar um sölupöntun

1. Farðu í **Sölu og markaðssetningu** \> **Sölupantanir** \> **Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Í sölupöntunarhausnum, í reitnum **Viðskiptavinur reikningur** slærðu inn **US-003**.
4. Bættu við línu fyrir nýja vöru og sláðu inn **10** sem magnið. Gangið úr skugga um að reiturinn **Vöruhús** er stillt á **24**.
5. Á flýtiflipanum **Sölupöntunarlínur**, veldu **Birgðir** og síðan, í hópnum **Viðhalda**, veldu **Hópapöntun**. Síðan **Hópapöntun** sýnir lista yfir lotur sem hægt er að panta fyrir pöntunarlínuna. Fyrir þetta dæmi sýnir það magn af **20** fyrir lotunúmer **B11** og magn af **10** fyrir lotunúmer **B22**. Athugaðu að **Hópapöntun** síðu er ekki hægt að nálgast frá línu ef hluturinn á þeirri línu er tengdur „Hópur hér að neðan\[staðsetningu\]" pöntunarveldi nema að það sé sett upp til að leyfa ákveðna pöntun.

    > [!NOTE]
    > Til að panta ákveðna lotu fyrir sölupöntun verður þú að nota síðuna **Hópapöntun**.
    >
    > Ef þú slærð inn lotunúmerið beint á sölupöntunarlínunni mun kerfið haga sér eins og þú hafir slegið inn sérstakt lotugildi fyrir hlut sem er háð „hópnum hér að neðan\[staðsetningu\]" fyrirvara stefnu. Þegar þú vistar línuna færðu viðvörunarskilaboð. Ef þú staðfestir að tilgreina skuli lotunúmerið beint á pöntunarlínunni verður línan ekki meðhöndluð samkvæmt reglulegri vörugeymslu stjórnunar.
    >
    > Ef þú áskilur magnið af síðunni **Fyrirvari**, engin sérstök lota verður frátekin og framkvæmd vörugeymsluaðgerða fyrir línuna mun fylgja þeim reglum sem gilda undir „Hópur hér að neðan\[staðsetningu\]" fyrirvara stefnu.

    Almennt virkar þessi síða og er samspiluð á sama hátt og hún virkar og er samspiluð þeim með atriðum sem hafa tilheyrandi frátektarveldi „Hópurinn hér að ofan\[staðsetningu\]" gerð. Eftirfarandi undantekningar eiga þó við:

    - Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** sýnir lotunúmerin sem eru frátekin fyrir pöntunarlínuna. Runugildin í töflunni verða sýnd allan uppfærsluferil pöntunarlínunnar, þ.mt vinnslustig vörugeymslu. Aftur á móti, á flýtiflipanum **Yfirlit**, venjulegur pöntunarlínupöntun (það er fyrirvari sem er gerður fyrir málin fyrir ofan **Staðsetning** stig) er sýnt í töflunni upp að því marki þegar vörugeymsla er búin til. Vinnuaðilinn tekur svo við línupöntuninni og línupöntunin birtist ekki lengur á síðunni. Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** hjálpar til við að ábyrgjast að sölupöntunaraðili getur skoðað lotunúmerin sem voru skuldbundin pöntun viðskiptavinarins hvenær sem er á líftíma hans, upp í gegnum reikninga.
    - Auk þess að panta sértæka lotu getur notandi valið handvirkt sértækan stað og framleiðslueiningar plötunnar í stað þess að láta kerfið velja þá sjálfkrafa. Þessi hæfileiki tengist hönnun pöntunarbundins fyrirkomulags fyrir pöntun. Eins og nefnt var áður, þegar rununúmer er tekið frá fyrir vöru undir „Hópur hér að neðan\[staðsetningu\]" pöntunarstefna, kerfið verður að panta allar víddir upp í gegnum staðsetningu. Þess vegna mun vörugeymsla hafa sömu geymsluvíddir og notendurnir sem unnu með pantanirnar áskildu og það gæti ekki alltaf táknað geymslu hlutarins sem er þægilegt eða jafnvel mögulegt fyrir tínaaðgerðir. Ef pöntunaraðilar eru meðvitaðir um takmarkanir vörugeymslu, gætu þeir viljað handvirkt velja tiltekna staði og leyfismerki þegar þeir panta hóp. Í þessu tilfelli verður notandinn að nota **Sýna mál** virkni á síðuhausnum og verður að bæta við staðsetningu og kennitala í ristina á flýtiflipanum **Yfirlit**.

6. Á **Hópapöntun** síðu, veldu línuna fyrir hópinn **B11** og veldu síðan **Varalína**. Það er engin tiltekin rökfræði til að úthluta staðsetningum og skiltum við sjálfvirka fyrirvara. Þú getur slegið inn magnið handvirkt í reitinn **Frátekning**. Taktu eftir því að á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu**, hópur **B11** er sýnt sem **Skuldbundinn**.

    ![Að fremja ákveðið lotunúmer í sölupöntunarlínu á síðu síðu frátektar á runu](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Bókun magns á sölupöntunarlínu er hægt að gera í mörgum lotum. Sömuleiðis er hægt að panta sömu lotu gagnvart mörgum stöðum og skiltum (ef leyfisplötur eru virkar fyrir staðina).
    >
    > Pöntun á tiltekinni lotu fyrir magnið á sölupöntunarlínu getur einnig verið að hluta. Til dæmis er hægt að panta heildarmagn 100 eininga þannig að ákveðin lota er skuldbundin til 20 eininga en 80 einingar eru fráteknar á staðnum og vörugeymslustigi fyrir alla tiltæka lotu. Í þessu tilfelli mun WMS sjá um tínaaðgerðir með því að nota tvær aðskildar vinnulínur.

7. Farðu í **Afurðaupplýsingastjórnun** \> **Afurðir** \> **Losaðar afurðir**. Veldu hlutinn þinn og veldu síðan **Stjórna birgðum** \> **Skoða** \> **Færslur**.

    ![Pöntunarbundin fyrirvara sem birgðafærslugerð](media/Inventory-transactions-for-order-committed-reservation.png)

8. Skoðaðu birgðafærslur hlutarins sem tengjast pöntun sölupöntunarlínunnar.

    - Viðskipti þar sem **Tilvísun** reiturinn er stilltur á **Sölupöntun** og **Mál** reiturinn er stilltur á **Frátekin líkamleg** táknar pöntunarlínu fyrirvara fyrir birgðavíddir fyrir ofan **Staðsetning** stigi. Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir staða, vörugeymsla og birgðastaða.
    - Viðskipti þar sem reiturinn **Tilvísun** er stilltur á **Pöntunarbundna frátekt** og reiturinn **Úthreyfing** er stilltur á **Frátekið á lager** táknar pöntunarlínu frátektar fyrir tiltekna runu og annar birgðavíddir fyrir ofan hana. Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir rununúmer og staðsetning. Í þessu dæmi er staðsetningin **Magn-001**.

9. Veldu á sölupöntunarhaus **Vöruhús** \> **Aðgerðir** \> **Losa í vöruhús**. Pöntunarlínan hefur verið sett í bylgju og álag og vinna búin til.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Farið yfir og unnið úr vöruhúsagerð sem er með pöntunarbundna lotunúmer

1. Á flýtiflipanum **Sölupöntunarlínur**, veldu **Vöruhús** \> **Upplýsingar um vinnu**.

    Vinnan sem annast tínsluaðgerðina fyrir magn magn sem skuldbundið sig til sölupöntunarlínunnar hefur eftirfarandi einkenni:

    - Til að búa til vinnu notar kerfið vinnusniðmát en ekki staðsetningartilskipanir. Öllum stöðluðum stillingum sem eru skilgreindar fyrir vinnusniðmát, svo sem hámarksfjölda vallína eða ákveðin mælieining, verður beitt til að ákvarða hvenær ný vinna ætti að búa til. Hins vegar er ekki tekið tillit til reglnanna sem eru tengdar staðsetningarleiðbeiningum til að bera kennsl á valstöðum, vegna þess að pöntunin sem framin er fyrir pöntunin tilgreinir þegar allar birgðarvíddirnar. Þessar birgðastærðir innihalda mál á lagergeymslu stigsins. Þess vegna erfðir verkið þessar víddir án þess að þurfa að hafa samráð um staðsetningartilskipanir.
    - Hópnúmerið er ekki sýnt á velja línunni (eins og á við um vinnulínuna sem er búin til fyrir hlut sem er með tilheyrandi „hópur hér að ofan\[staðsetningu\]„ fyrirvara stigveldi.) Í staðinn eru„ frá “lotunúmerinu og öllum öðrum geymsluvíddum sýndar á verkbirgðir vinnu línunnar sem vísað er til úr tilheyrandi birgðafærslum.

        ![Vörugeymslufærsla vegna vinnu sem er upprunnin í pöntunarbundinni frátekt](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Eftir að vinna er búin til, birgðir hlutarins þar sem **Tilvísun** reiturinn er stilltur á **Pöntunarbundin frátekt** er fjarlægður. Birgðafærslan þar sem **Tilvísun** reiturinn er stilltur á **Vinna** geymir nú líkamlegan fyrirvara á öllum birgðastærðum magnsins.

        Vöruhúsaaðgerðir geta haldið áfram til að sjá um framkvæmd verksins á venjulegan hátt. Leiðbeiningarnar í farsímanum munu hins vegar leiðbeina starfsmanni að velja ákveðið lotunúmer. Í vöruhúsumhverfi þar sem staðsetningar eru stjórnaðar með leyfi fyrir skiltum, eftir að starfsmaður hefur náð staðsetningu sem geymir sömu framleiðslulotu á mörgum skiltum, þá getur hann eða hún valið af hvaða skilti sem er ekki þegar frátekinn (til dæmis með annarri pöntun- skuldbundinn fyrirvara eða vinnu sem er upprunnin í fyrirvara af þeirri gerð.)

        Ef það reynist óframkvæmanlegt að velja frá þeim stað sem er tilgreindur á vinnulínunni geta rekstraraðilar vörugeymslu notað eina af eftirfarandi aðgerðum til að beina því að velja ákveðna lotu frá þægilegri stað:

        - Staðallinn **Hnekkja staðsetningu** aðgerð í farsíma (að því tilskildu að starfsmaður vörugeymslu **Leyfa val á staðsetningu staðsetningu** stilling er virk)
        - Aðgerðin **Breyta staðsetningu** á **Upplýsingar um vinnulista** síðu. 

2. Ljúktu við að velja og setja verkið í farsímann.

    Magnið **10** fyrir lotunúmer **B11** er nú valinn í sölupöntunarlínuna og settur í **Afgreiðsluhurð** staðsetningu. Á þessum tímapunkti er það tilbúið að hlaða það á vörubílinn og senda á heimilisfang viðskiptavinarins.

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a>Undanþágumeðhöndlun á vöruhúsavinnu sem er með pöntunarbundin lotunúmer

Vörugeymsla til að velja pöntunarbundin lotunúmer er háð sömu stöðluðu meðhöndlun undantekninga vörugeymslu og aðgerðum og venjuleg vinna. Almennt er hægt að hætta við opna verkið eða vinnu línuna, það er hægt að trufla það vegna þess að notendastaður er fullur, það er hægt að velja hann stutt og það er hægt að uppfæra hann vegna hreyfingar. Sömuleiðis er hægt að draga úr valinni vinnu sem þegar hefur verið lokið eða hægt er að snúa verkinu við.

Eftirfarandi lykilregla er notuð við allar þessar undantekningarmeðferðaraðgerðir: aldrei er hægt að skipta um lotunúmer sem var frátekið fyrir viðskiptavininn fyrir annað lotunúmer, en hægt er að breyta geymsluvíddum hans (staðsetningu og kennitala) með annað hvort handvirkri uppfærslu af notanda eða sjálfvirka uppfærslu af kerfinu. Sjálfvirka uppfærslan er byggð á sömu handahófi úthlutun geymsluvíddar og gilti þegar ákveðin lota var sjálfkrafa frátekin en engar geymsluvíddir voru tilgreindar.

### <a name="example-scenario"></a>Dæmi

Dæmi um þessa atburðarás er ástand þar sem verið er að velja áður lokið verk með því að nota virknina **Draga úr völdu magni**. Þetta dæmi heldur áfram með fyrra dæminu í þessu efni.

1. Farðu í **Vöruhúsakerfi** \> **Hleðslur** \> **Virkar hleðslur**.
2. Veldu álag sem var búið til í tengslum við sendingu sölupöntunar þinnar.
3. Af flýtiflipanum **Hlaðið pöntunarlínum**, veldu **Draga úr völdum magni**.
4. Á **Draga úr völdum magni** síðu, í **Færa á staðsetningu** reit, veldu **FL-001**.
5. Í reitnum **Flytja á númeraplötu** velurðu **LP33**.
6. Í hnitanetinu í reitnum **Magn birgða til að afturkalla tiltekt á** sláðu inn **10**.
7. Veljið **Í lagi**.

Hér eru niðurstöður úr aðgerð til að afturkalla tiltekt:

- Staða fyrri lokaðs verks er stillt á **Hætt við**.
- Nýtt verk af gerðinni **Birgðahreyfing** er búin til fyrir óvalið magn af **10** fyrir lotunúmer **B11**. Þessi vinna táknar hreyfingu frá **Afgreiðsluhurð** staðsetningu til númeraplötu **LP33** á staðsetningu **FL-001**. Staðan er stillt á **Lokað**.
- Kerfið áskilur aftur lotunúmerið sem upphaflega var pantað og úthlutar auðkenni staðsetningar og korts. (Þetta ferli jafngildir því að keyra virknina **Frátektarlína** fyrir pöntunarlínuna fyrir tiltekið lotunúmer). Fyrir vikið, hópur **B11** er sýnt sem framið á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu** af **Runufrátekt** síðu og **Frátekt** reiturinn inniheldur magn af **10** fyrir lotunúmer **B11**. Að auki, er **Staðsetning** reiturinn stilltur á **FL-001**, og **Númeraplata** reiturinn er stilltur á **LP11**. (Þú getur bætt þessum reitum við töfluna ef þeir eru ekki sýnilegir.)

Eftirfarandi töflur veita yfirlit sem sýnir hvernig kerfið meðhöndlar pöntunarbundna lotu fyrirvara fyrir sérstakar vörugeymsluaðgerðir. Til að túlka innihaldið í töflunum, gerðu ráð fyrir að hver vörugeymslaaðgerð sé keyrð í samhengi við núverandi vörugeymsluverk sem er upprunnin í pöntunarbundinni lotu fyrirvara, eða að framkvæmd hverrar vörugerðaraðgerðar hefur áhrif á vinnu af þeirri gerð.

> [!NOTE]
> Í þessum töflum gefur dálkurinn „Hópmagn er fáanlegt“ til kynna hvort magn af framleiðslulotu er til viðbótar við það magn sem er annað hvort þegar frátekið fyrir núverandi pöntunarbundna fyrirvara eða þegar er frátekið af vörugeymsluverkinu sem kemur frá fyrirvörum af þeirri gerð.

#### <a name="override-the-pick-location-on-the-open-work"></a>Yfirskrifa tínslustaðsetningu í opinni vinnu

<table>
<thead>
<tr>
<th>Færibreyta lykiluppsetningar</th>
<th>Runumagn er fáanlegt</th>
<th>Lykilþrep notenda</th>
<th>Vinna vöruhúss</th>
<th>Pantanaskuldbundin hópapöntun</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Valkosturinn <strong>Leyfa val á staðsetningu staðsetningu</strong> er virkur á starfsmanninum.</td>
<td>Já</td>
<td>
<ol>
<li>Veldu <strong>Hnekkja staðsetningu</strong> valmyndaratriði í Warehouse Mmobile App (WMA) þegar þú byrjar að tína vinnu.</li>
<li>Veldu <strong>Stinga upp</strong>.</li>
<li>Staðfestu nýja staðsetninguna sem lagt er til með tilliti til framboðs í fjölda magns.</li>
</ol>
</td>
<td>Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:
<ul>
<li>Staðsetningin á velja línunni er uppfærð á nýjan stað. (Ef staðsetningin er stjórnað með leyfismerki er úthlutað af handahófi leyfismerki fyrir vörubirgðafærsluna og starfsmaðurinn getur valið úr hvaða skilti sem er með tiltækt magn.)</li>
<li>Ef magnið er að finna á fleiri en einni leyfisplötu á nýjum stað, er upprunalegu vallínunni skipt í margar línur sem passa við hvern kennitala.</li>
</ul>
</td>
<td>Á ekki við</td>
</tr>
<tr>
<td>Nr</td>
<td>
<ol>
<li>Veldu <strong>Hnekkja staðsetningu</strong> valmyndaratriði í WMA þegar þú byrjar að tína vinnu.</li>
<li>Færa handvirkt inn staðsetningu.</li>
</ol>
</td>
<td>Aðgerðin <strong>Hnekkja staðsetningu</strong> er ekki möguleg. Það mistekst og villu er hent.</td>
<td>Á ekki við</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Fullur hnappur - Skiptu vinnulínu vegna flæða á staðsetningu notandans

<table>
<thead>
<tr>
<th>Færibreyta lykiluppsetningar</th>
<th>Runumagn er fáanlegt</th>
<th>Lykilþrep notenda</th>
<th>Vinna vöruhúss</th>
<th>Pantanaskuldbundin hópapöntun</th>
</tr>
</thead>
<tbody>
<tr>
<td>Valkosturinn <strong>Leyfa verkaskiptingu</strong> er virkur í valmyndaratriðinu fyrir farsíma.</td>
<td>Á ekki við</td>
<td>
<ol>
<li>Veldu <strong>Fullt</strong> valmyndaratriði í WMA þegar þú vinnur úr tínsluvinnu.</li>
<li>Í <strong>Veldu fjölda</strong> reitinn, sláðu inn hluta magns af nauðsynlegu valinu til að gefa til kynna fullan afköst.</li>
</ol>
</td>
<td>
<ul>
<li>Í núverandi vinnu er magnið uppfært í það magn sem eftir verður sem þarf að velja.</li>
<li>Ný verk fyrir valið magn er búið til og lokað.</li>
</ul></td>
<td>Á ekki við</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Draga úr valið magn af fullunninni vinnu (úr álagi)

<table>
<thead>
<tr>
<th>Færibreyta lykiluppsetningar</th>
<th>Runumagn er fáanlegt</th>
<th>Lykilþrep notenda</th>
<th>Vinna vöruhúss</th>
<th>Pantanaskuldbundin hópapöntun</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Á ekki við</td>
<td>Já</td>
<td>
<ol>
<li>Opnaðu <strong>Draga úr völdum magni</strong> síðu frá hleðslulínunni.</li>
<li>Færa skal inn fullt magn til að afturkalla tiltekt á.</li>
<li>Veldu „færa til“ staðsetningu / kennitala.</li>
</ol>
</td>
<td>
<ul> 
<li>Vinna sem er tengd hleðslulínunni fellur niður.</li>
<li>Ný verk fyrir birgðahreyfingar er búið til og lokað.</li>
</ul>
</td>
<td>Magnið er aftur frátekið fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>Sjá fyrri línuna.</td>
<td>Magnið er aftur frátekið fyrir sömu framleiðslulotu og fyrir sama stað og skírteini (ef staðsetningin er stjórnað með skiltum) sem var slegið inn við upptöku.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Færa vöru til innan vöruhúss

> [!NOTE]
> Þessi vörugeymsla á aðeins við um flutninga á **Vinnusköpunarferli** tegund, ekki til hreyfingar eftir sniðmáti.

<table>
<thead>
<tr>
<th>Færibreyta lykiluppsetningar</th>
<th>Runumagn er fáanlegt</th>
<th>Lykilþrep notenda</th>
<th>Vinna vöruhúss</th>
<th>Pantanaskuldbundin hópapöntun</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Valkostur <strong>Leyfa flutning birgða með tilheyrandi vinnu</strong> er virkur á starfsmanninum.</td>
<td>Já</td>
<td>
<ol>
<li>Hefja hreyfingu á WMA.</li>
<li>Sláið inn staðsetningar „frá” og „til”.</li>
</ol></td>
<td>
<ul>
<li>Í allri núverandi vinnu sem hefur áhrif á flutninginn, er staðsetningin valin uppfærð á nýja „til“ staðinn.</li>
<li>Ný verk fyrir birgðahreyfingar er búið til og lokað.</li>
</ul>
</td>
<td>Allir núverandi fyrirvarar sem hafa áhrif á magnhreyfingu frá tilteknum stað eru aftur áskilnir fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>Sjá fyrri línuna.</td>
<td>Allur fyrirliggjandi fyrirvari sem hefur áhrif á magnhreyfingu frá tilteknum stað er aftur áskilinn fyrir sömu framleiðslulotu og fyrir nýja „til“ staðsetningar og kennitala (ef staðsetningin er stjórnað með skiltum).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Bakfærðu tiltekið magn af fullunninni vinnu (úr álagi eða bylgju)

<table>
<thead>
<tr>
<th>Færibreyta lykiluppsetningar</th>
<th>Runumagn er fáanlegt</th>
<th>Lykilþrep notenda</th>
<th>Vinna vöruhúss</th>
<th>Pantanaskuldbundin hópapöntun</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Á ekki við</td>
<td>Já</td>
<td>
<ol>
<li>Opnaðu <strong>Bakfæra vinnu</strong> síðu.</li>
<li>Veldu beiðnissíðuna <strong>Skildu hluti eftir núverandi staðsetningu</strong> kostur.</li>
</ol>
</td>
<td>Öll vinna sem er tengd hleðslunni fellur niður.</td>
<td>Magnið er aftur frátekið fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>Sjá fyrri línuna.</td>
<td>Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var eftir við afturköllun.</td>
</tr>
<tr>
<td>Já</td>
<td>
<ol>
<li>Opnaðu <strong>Bakfæra vinnu</strong> síðu.</li>
<li>Veldu beiðnissíðuna <strong>Úthluta vörum á þessa staðsetningu</strong> kostur.</li>
</ol>
</td>
<td>
<ul>
<li>Núgildandi vinna er afturkölluð.</li>
<li>Ný verk fyrir birgðahreyfingar er búið til og lokað.</li>
</ul>
</td>
<td>Magnið er aftur frátekið fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>Sjá fyrri línuna.</td>
<td>Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var úthlutað á við bakfærslu.</td>
</tr>
<tr>
<td>Já/nei</td>
<td>
<ol>
<li>Opnaðu <strong>Bakfæra vinnu</strong> síðu.</li>
<li>Veldu beiðnissíðuna <strong>Færa vörur á þessa staðsetningu</strong> kostur.</li>
</ol>
</td>
<td>Bakfærsla er ekki studd.</td>
<td>Á ekki við</td>
</tr>
<tr>
<td>Já/nei</td>
<td>
<ol>
<li>Opnaðu <strong>Bakfæra vinnu</strong> síðu.</li>
<li>Veldu beiðnissíðuna <strong>Færa vörur byggt á staðsetningartilskipunum</strong> kostur.</li>
</ol>
</td>
<td>Bakfærsla er ekki studd. </td>
<td>Á ekki við</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Veldu stutt skammt - Skráðu magnið sem ekki finnast líkamlega á staðnum / leyfismerkinu meðan þú framkvæmir tínaverk

<table>
<thead>
<tr>
<th>Færibreyta lykiluppsetningar</th>
<th>Runumagn er fáanlegt</th>
<th>Lykilþrep notenda</th>
<th>Vinna vöruhúss</th>
<th>Pantanaskuldbundin hópapöntun</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>.</td>
<td>Já</td>
<td>
<ol>
<li>Veldu <strong>Of lítil tiltekt</strong> valmyndaratriði í WMA þegar þú keyrir tínsluvinnu.</li>
<li>Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</li>
<li>Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Núverandi verk er lokað og valið magn er 0 (núll).</li>
<li>Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</li>
</ul>
</td>
<td>Magnið er aftur frátekið fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>
<ul>
<li>Of lítil tiltekt-aðgerðin mistekst og villu er hent.</li>
<li>Núverandi verk er áfram opið.</li>
</ul>
</td>
<td>Á ekki við</td>
</tr>
<tr>
<td rowspan='2'>Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>.</td>
<td>Já</td>
<td>
<ol>
<li>Veldu <strong>Of lítil tiltekt</strong> valmyndaratriði í WMA þegar þú keyrir tínsluvinnu.</li>
<li>Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</li>
<li>Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Núverandi verk er lokað og valið magn er 0 (núll).</li>
<li>Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</li>
</ul>
</td>
<td>Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru endurfráteknar fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>Sjá fyrri línuna.</td>
<td>Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru fjarlægðar.</td>
</tr>
<tr>
<td>Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei/Já</strong>. Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</td>
<td>Já</td>
<td>
<ol>
<li>Veldu <strong>Of lítil tiltekt</strong> valmyndaratriði í WMA þegar þú keyrir tínsluvinnu.</li>
<li>Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</li>
<li>Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</li>
<li>Veldu staðsetningu / kennitala á listanum.</li>
</ol>
</td>
<td>
<ul>
<li>Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:
<ul>
<li>Tínslulínan er lokuð og valið magn er 0 (núll).</li>
<li>Hætt er við að söluréttarlínuna.</li>
<li>Ný tiltektarlína er búin til. Það notar staðsetningu / númeraplötu sem notandinn valdi.</li>
<li>Ný söluréttarlína er búin til.</li>
</ul>
</li>
<li>Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</li>
</ul>
</td>
<td>Á ekki við</td>
</tr>
<tr>
<td>Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>. Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</td>
<td>Nr</td>
<td>
<ol>
<li>Veldu <strong>Of lítil tiltekt</strong> valmyndaratriði í WMA þegar þú keyrir tínsluvinnu.</li>
<li>Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</li>
<li>Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</li>
</ol>
</td>
<td>Of lítil tiltekt-aðgerðin mistekst og villu er hent.</td>
<td>Á ekki við</td>
</tr>
<tr>
<td>Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>. Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</td>
<td>Nr</td>
<td>
<ol>
<li>Veldu <strong>Of lítil tiltekt</strong> valmyndaratriði í WMA þegar þú keyrir tínsluvinnu.</li>
<li>Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</li>
<li>Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</li>
<li>Veldu staðsetningu / kennitala á listanum.</li>
</ol>
</td>
<td>
<ul>
<li>Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:
<ul>
<li>Tínslulínan er lokuð og valið magn er 0 (núll).</li>
<li>Hætt er við að söluréttarlínuna.</li>
</ul>
</li>
<li>Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</li>
</ul>
</td>
<td>Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil/númeraplötu eru fjarlægðar.</td>
</tr>
<tr>
<td>Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Sjálfvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já/Nei</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já/Nei</strong>.</td>
<td>Á ekki við</td>
<td>
<ol>
<li>Veldu <strong>Of lítil tiltekt</strong> valmyndaratriði í WMA þegar þú keyrir tínsluvinnu.</li>
<li>Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</li>
<li>Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með sjálfvirkri endurúthlutun</strong>.</li>
</ol>
</td>
<td>Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</td>
<td>Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Breyta á birgðastöðunni

> [!NOTE]
> Þessa vörugeymsluaðgerð er hægt að framkvæma frá mörgum inngangspunktum. Dæmið sem sýnt er hér notar **Breyting á birgðum** aðgerð á **Á lager eftir birgðageymslu** síðu.

<table>
<thead>
<tr>
<th>Færibreyta lykiluppsetningar</th>
<th>Runumagn er fáanlegt</th>
<th>Lykilþrep notenda</th>
<th>Vinna vöruhúss</th>
<th>Pantanaskuldbundin hópapöntun</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Á <strong>Vöruhús</strong> flipanum, í <strong>Vöruhús</strong> skrá, er <strong>Fjarlægja frátektir og merkingar</strong> reiturinn stilltur á <strong>Frátektir</strong> eða <strong>Merkingar og fyrirvarar</strong>.</td>
<td>Já</td>
<td>
<ol>
<li>Veldu tiltekna staðsetningu.</li>
<li>Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</li>
<li>Veldu <strong>Breyting á birgðastöðu</strong>.</li>
<li>Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</li>
</ol>
</td>
<td>Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</td>
<td>
<ul>
<li>Magnið er aftur frátekið fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</li>
<li>Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</li>
<li>Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</li>
</ul>
</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</td>
<td>
<ul>
<li>Pöntunin er fjarlægð.</li>
<li>Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</li>
<li>Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Á flipanum <strong>Vöruhús</strong>, í skránni <strong>Vöruhús</strong>, er reiturinn <strong>Fjarlægja frátektir og merkingar</strong> stilltur á <strong>Ekkert</strong>.</td>
<td>Já</td>
<td>
<ol>
<li>Veldu tiltekna staðsetningu.</li>
<li>Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</li>
<li>Veldu <strong>Breyting á birgðastöðu</strong>.</li>
<li>Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</li>
</ol>
</td>
<td>Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</td>
<td>Magnið er aftur frátekið fyrir sömu lotu. Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</td>
</tr>
<tr>
<td>Nr</td>
<td>Sjá fyrri línuna.</td>
<td>Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</td>
<td>Breytingar á birgðastöðu eru ekki leyfðar.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Takmarkanir

- Sveigjanleiki vörugeymsluvíddar pöntunaraðgerða styður ekki eftirfarandi eiginleika:

    - Stjórnun framleiðsluþyngdar
    - Efnislega neikvæð birgðastaða
    - Frátekt gegn pöntuðu framboði
    - Flytja pantanir og hráefni tína

- Reglugerð um gámasamstæðu fyrir pökkun með tilskipunareiningunni hefur takmarkanir. Fyrir pöntunarbundna fyrirvara mælum við með að þú notir ekki sniðmát fyrir gámagerð þar sem **Pakkning eftir tilskipunareining** reiturinn er virkur. Í núverandi hönnun eru staðsetningartilskipanir ekki notaðar þegar vörugeymsla er búin til. Þess vegna er aðeins lægsta einingin í einingaröðarhópnum (birgðaeiningin) beitt á gámabylgjuskrefinu.

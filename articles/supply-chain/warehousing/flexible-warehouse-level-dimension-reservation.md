---
title: Sveigjanleg frátektarregla á vídd vöruhúsastigs
description: Þetta efni lýsir stefnuskrá fyrir birgða sem láta fyrirtæki sem selja vörur sem eru rekin með runur og reka flutninga sína sem aðgerðir með WMS-virka áskilja sértækar runur fyrir sölupantanir viðskiptavina, jafnvel þó að pöntunarveldið sem er tengt vörunum banni ekki fyrirvara á tilteknum runum.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0fe4b377ec80601f616f81f71222129256dfd448
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474941"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Sveigjanleg frátektarregla á vídd vöruhúsastigs

[!include [banner](../includes/banner.md)]

Þegar frátekningarstigveldi birgða af gerðinni *Runa fyrir neðan\[staðsetningu\]* tengist afurðum, geta fyrirtæki, sem selja runuraktar afurðir og keyra vörustjórnun sína sem aðgerðir sem eru virkjaðar fyrir Microsoft Dynamics 365 vöruhúsakerfið, ekki tekið frá tilteknar runur þeirra afurða fyrir sölupantanir viðskiptavina.

Á svipaðan hátt er ekki hægt að taka frá sérstakar númeraplötur fyrir afurðir í sölupöntunum þegar þessar afurðir eru tengdar við sjálfgefið frátekningarstigveldi.

Þetta efnisatriði lýsir frátekningarreglu birgða sem gerir þessum fyrirtækjum kleift að taka frá ákveðnar runur eða númeraplötur, jafnvel þegar afurðirnar eru tengdar frátekningarstigveldi *Runa fyrir neðan\[staðsetningu\]*.

## <a name="inventory-reservation-hierarchy"></a>Frátekningarstigveldi birgða

Þessi hluti dregur saman núverandi stigveldi birgða fyrirvara.

Frátekningarstigveldi birgða boðar, hvað varðar geymsluvíddir, að eftirspurnarpöntunin geymi áskildar víddir svæðis, vöruhúss og birgðastöðu. Í öðrum orðum eru áskildar víddir allar víddirnar fyrir ofan vídd staðsetningar í frátekningarstigveldinu á meðan regla vöruhúss ber ábyrgð á úthlutun staðsetningar á umbeðið magn og frátekningu staðsetningarinnar. Í samskiptum milli eftirspurnarpöntunarinnar og vöruhúsaaðgerðanna er búist við að eftirspurnarpöntunin gefi til kynna hvaðan senda á pöntunina frá (þ.e. hvaða svæði og vöruhúsi). Vöruhúsið treystir síðan á rökfræði þess til að finna nauðsynlegt magn í húsnæði vörugeymslu.

Hins vegar, til að endurspegla rekstrarlíkan fyrirtækisins, eru mælingar á stærð (runu og raðnúmer) háð meiri sveigjanleika. Stigveldi birgðapöntunar rúmar atburðarás þar sem eftirfarandi skilyrði eiga við:

- Fyrirtækið reiðir sig á vöruhúsaaðgerðir sínar til að stjórna tiltekt á magni sem er með runu- eða raðnúmer *eftir* að magnið finnst í geymsluplássi vöruhúss. Oft er vísað í þetta líkan sem *Runa fyrir neðan\[staðsetningu\]* eða *Raðnúmer fyrir neðan\[staðsetningu\]*. Það er venjulega notað þegar framleiðslueining vöru eða raðnúmer er ekki mikilvægt fyrir viðskiptavini sem setja eftirspurnina hjá sölufyrirtækinu.
- Fyrirtækið reiðir sig á vöruhúsaaðgerðir sínar til að stjórna tiltekt á magni sem er með runu- eða raðnúmer *áður en* magnið finnst í geymsluplássi vöruhúss. Ef runu- eða raðnúmer er nauðsynlegt sem hluti af forskrift viðskiptavinapöntunar eru þau skráð í eftirspurnarpöntunina og vöruhúsaaðgerðirnar sem finna magnið í vöruhúsinu mega ekki breyta þeim. Þetta líkan er kallað *Runa fyrir ofan\[staðsetningu\]* eða *Raðnúmer fyrir ofan\[staðsetningu\]*. Þar sem víddirnar fyrir ofan staðsetningu eru tilteknu kröfurnar fyrir eftirspurnirnar sem þarf að uppfylla mun regla vöruhúss ekki úthluta þeim. Þessar víddir **verða** alltaf að vera tilgreindar í eftirspurnarpöntuninni eða tengdum frátekningum.

Í þessum atburðarásum er áskorunin sú að aðeins er hægt að úthluta einum birgða pöntunarveldi fyrir hverja vöru sem gefin er út. Þess vegna, fyrir WMS til að meðhöndla rakta hluti, eftir að stigveldi verkefnisins ákvarðar hvenær á að panta lotu eða raðnúmer (annað hvort þegar eftirspurnarpöntunin er tekin eða meðan á pökkunarvinnu vörugeymslu stendur), er ekki hægt að breyta þessari tímasetningu í auglýsingu -hoc grundvöllur.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Sveigjanlegur fyrirvari fyrir hluti sem rekja má hóp

### <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Í þessari atburðarás notar fyrirtæki birgðarstefnu þar sem fullunnum vörum er rakið eftir lotunúmerum. Þetta fyrirtæki notar einnig WMS vinnuálag. Þar sem þetta vinnuálag er með vel útbúna reglu fyrir áætlanagerð og keyrslu tiltekta og sendingaraðgerða fyrir runuvirkar vörur, tengjast flestar tilbúnu afurðirnar frátekningarstigveldi birgða fyrir *Runa fyrir neðan\[staðsetningu\]*. Kosturinn við þessa tegund rekstraruppsetningar er að ákvörðunum (sem eru í raun fyrirvara um fyrirvaralausar ákvarðanir) um hvaða runur á að velja og hvar eigi að setja þær í vörugeymslunni er frestað þangað til að vörugeymsla hefst. Þeir eru ekki gerðir þegar pöntun viðskiptavinarins er sett.

Þótt frátekningarstigveldið *Runa fyrir neðan\[staðsetningu\]* þjónar viðskiptamarkmiðum fyrirtækisins, þurfa margir af viðskiptavinum fyrirtækisins sömu rununa og þeir keyptu áður þegar þeir pöntuðu afurðirnar aftur. Þess vegna er fyrirtækið að leita að sveigjanleika í meðhöndlun reglna um röðun pöntunar svo að eftir atvikum viðskiptavina eftir sama hlut, gerist eftirfarandi hegðun:

- Hægt er að skrá lotunúmer og panta þegar pöntunin er tekin af söluaðilanum og ekki er hægt að breyta því við vörugeymslu og / eða taka af öðrum kröfum. Þessi hegðun hjálpar til við að tryggja að lotunúmerið sem var pantað er sent til viðskiptavinarins.
- Ef lotunúmerið er ekki mikilvægt fyrir viðskiptavininn, þá geta vörugeymsluaðgerðir ákvarðað lotunúmer meðan á vinnu stendur, eftir að skráning og pöntun sölupöntunar hefur verið gert.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Leyfa fyrirvara um ákveðna lotu í sölupöntuninni

Til að koma til móts við æskilegan sveigjanleika í hegðun runufrátekningar fyrir vörur sem tengjast *Runu fyrir neðan\[staðsetningu\]* í frátekningarstigveldi birgða, verða birgðastjórar að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stigið **Rununúmer** á síðunni **Frátekningarstigveldi birgða**.

![Gera frátekningastigveldi birgða sveigjanlegt.](media/Flexible-inventory-reservation-hierarchy.png)

Þegar stigið **Rununúmer** í stigveldinu er valið, allar víddir yfir því stigi og upp í gegnum **Staðsetning** stig verður sjálfkrafa valið. (Sjálfgefið að allar víddir yfir **Staðsetning** stig eru valin.) Þessi hegðun endurspeglar rökfræði þar sem allar víddir á bilinu milli lotunúmers og staðsetningar eru einnig sjálfkrafa fráteknar eftir að þú hefur pantað tiltekið lotunúmer á pöntunarlínunni.

> [!NOTE]
> Gátreiturinn **Leyfa fyrirvara á pöntunarbeiðni** á aðeins við um stig stigveldis sem er undir staðsetningu víddar vörugeymslu.
>
> **Rununúmer** og **Númeraplata** eru einu stigin í stigveldinu sem eru opin fyrir sveigjanlegu frátekningarreglunni. Með öðrum orðum er ekki hægt að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stig **Staðsetningar** eða **Raðnúmers**.
>
> Ef frátekningarstigveldið inniheldur vídd rununúmersins (sem verður alltaf að vera fyrir neðan stigið **Rununúmer**) og ef kveikt hefur verið á runumiðaðri frátekt fyrir rununúmerið mun kerfið halda áfram að vinna með aðgerðir rununúmerafrátekningar og tiltektar samkvæmt reglunum sem eiga við um frátekningarregluna *Raðnúmer fyrir neðan\[staðsetningu\]*.

Hægt er að leyfa runumiðaða frátekningu hvenær sem er fyrir fyrirliggjandi frátekningarstigveldið *Runa fyrir neðan\[staðsetningu\]* í uppsetningunni. Þessi breyting mun ekki hafa áhrif á neina fyrirvara og opna vöruhúsavinnu sem voru búin til áður en breytingin átti sér stað. Hins vegar **Leyfa fyrirvara á pöntunarbeiðni** Ekki er hægt að hreinsa gátreitinn ef birgðafærslur á **Frátekið pantað**, **Frátekin líkamleg**, eða **Pantaði** útgáfutegund er til fyrir einn eða fleiri hluti sem eru tengdir því pöntunarveldi.

> [!NOTE]
> Ef núverandi fyrirvaralegveldi hlutar leyfir ekki forskrift lotur í pöntuninni, þá geturðu endurúthlutað því í pöntunarveldi sem gerir kleift að skilgreina lotu, að því tilskildu að stigskipulag stigveldisins sé það sama í báðum stigveldum. Nota **Breyta pöntunarveldi fyrir hluti** virka til að framkvæma endurúthlutun. Þessi breyting gæti skipt máli þegar þú vilt koma í veg fyrir sveigjanlegan pöntunarhluta fyrir hlutmengi af hlutum sem eru rekin í hópum en leyfa það fyrir restina af vöruframboði.

Hvort sem þú hefur valið gátreitinn **Leyfa frátekt á eftirspurnarpöntun** eða ekki, ef þú vilt ekki taka frá ákveðið rununúmer fyrir vöruna í pöntunarlínu mun sjálfgefin regla vöruhúsaaðgerðar sem gildir fyrir *Runa fyrir neðan\[staðsetningu\]* í frátekningarstigveldi samt eiga við.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Pantaðu tiltekið lotunúmer fyrir pöntun viðskiptavina

Þegar *Runa fyrir neðan\[staðsetningu\]* í frátekningarstigveldi birgða fyrir runurakta vöru er sett upp til að leyfa frátekningu á ákveðnum rununúmerum í sölupöntunum, geta úrvinnsluaðilar sölupöntunar tekið viðskiptavinapantanir fyrir sömu vöruna á einn af eftirfarandi hátt, eftir því hver beiðni viðskiptavinarins er:

- **Sláðu inn pöntunarupplýsingar án þess að tilgreina lotunúmer** - Þessa nálgun ætti að nota þegar framleiðslulota vöru er ekki mikilvæg fyrir viðskiptavininn. Allir núverandi ferlar sem tengjast meðhöndlun pöntunar af þessari gerð kerfisins eru óbreytt. Engin viðbótarsjónarmið eru nauðsynleg af hálfu notenda.
- **Sláðu inn pöntunarupplýsingar og pantaðu tiltekið lotunúmer** - Þessa aðferð ætti að nota þegar viðskiptavinurinn óskar eftir ákveðinni lotu. Venjulega munu viðskiptavinir biðja um ákveðna lotu þegar þeir eru að panta vöru sem þeir keyptu áður. Þessari tegund af sértækum pöntunum er vísað til *pöntunarbundinn fyrirvara*.

Eftirfarandi reglur eru í gildi þegar magn er afgreitt og lotunúmer er skuldbundið til sérstakrar pöntunar:

- Til að leyfa frátekningu á ákveðnu rununúmeri fyrir vörur undir frátekningarreglunni *Runa fyrir neðan\[staðsetningu\]* verður kerfið að taka frá allar víddir upp í gegnum staðsetningu. Þetta svið inniheldur venjulega stærð skírteinisins.
- Staðsetningartilskipanir eru ekki notaðar þegar val á vinnu er búið til fyrir sölulínu sem notar pöntunarbundna hópapöntun.
- Við vinnslu vörugeymslu á vinnu fyrir pöntunarbundna lotur er hvorki notanda né kerfinu heimilt að breyta lotunúmerinu. (Þessi vinnsla felur í sér meðhöndlun undantekninga.)

Eftirfarandi dæmi sýnir flæði frá enda til enda.

## <a name="example-scenario-batch-number-allocation"></a>Sýniaðstæður: Úthlutun rununúmers

Fyrir þetta dæmi verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Setjið upp stigveldi birgða fyrirvara til að leyfa ákveðna pöntun

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

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Slá inn upplýsingar um sölupöntun

1. Farðu í **Sölu og markaðssetningu** \> **Sölupantanir** \> **Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Í sölupöntunarhausnum, í reitnum **Viðskiptavinur reikningur** slærðu inn **US-003**.
4. Bættu við línu fyrir nýja vöru og sláðu inn **10** sem magnið. Gangið úr skugga um að reiturinn **Vöruhús** er stillt á **24**.
5. Á flýtiflipanum **Sölupöntunarlínur**, veldu **Birgðir** og síðan, í hópnum **Viðhalda**, veldu **Hópapöntun**. Síðan **Hópapöntun** sýnir lista yfir lotur sem hægt er að panta fyrir pöntunarlínuna. Fyrir þetta dæmi sýnir það magn af **20** fyrir lotunúmer **B11** og magn af **10** fyrir lotunúmer **B22**. Athugaðu að síðuna **Frátekt á runu** er ekki hægt að opna úr línu ef varan í þeirri línu tengist frátekningarstigveldinu *Runa fyrir neðan\[staðsetningu\]* nema hún sé sett upp til að leyfa runumiðaða frátekningu.

    > [!NOTE]
    > Til að panta ákveðna lotu fyrir sölupöntun verður þú að nota síðuna **Hópapöntun**.
    >
    > Ef rununúmerið er slegið beint inn í sölupöntunarlínuna mun kerfið taka því eins og þú hafir slegið inn sérstakt runugildi fyrir vörur sem heyrir undir frátekningarregluna *Runa fyrir neðan\[staðsetningu\]*. Þegar þú vistar línuna færðu viðvörunarskilaboð. Ef þú staðfestir að tilgreina skuli lotunúmerið beint á pöntunarlínunni verður línan ekki meðhöndluð samkvæmt reglulegri vörugeymslu stjórnunar.
    >
    > Ef magnið er frátekið á síðunni **Frátekning** verður engin sérstök runa tekin frá og framkvæmd vöruhúsaaðgerða fyrir línuna mun fylgja reglunum sem heyra undir frátekningarregluna *Runa fyrir neðan\[staðsetningu\]*.

    Almennt séð virkar þessi síða og er notuð á sama hátt og fyrir vörur sem eru með tengt frátekningarstigveldi af gerðinni *Runa fyrir ofan\[staðsetningu\]*. Eftirfarandi undantekningar eiga þó við:

    - Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** sýnir lotunúmerin sem eru frátekin fyrir pöntunarlínuna. Runugildin í hnitanetinu verða sýnd í gegnum allan uppfyllingartíma pöntunarlínunnar, þar á meðal stig vöruhúsavinnslunnar. Aftur á móti, á flýtiflipanum **Yfirlit**, venjulegur pöntunarlínupöntun (það er fyrirvari sem er gerður fyrir málin fyrir ofan **Staðsetning** stig) er sýnt í töflunni upp að því marki þegar vörugeymsla er búin til. Vinnuaðilinn tekur svo við línupöntuninni og línupöntunin birtist ekki lengur á síðunni. Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** hjálpar til við að ábyrgjast að sölupöntunaraðili getur skoðað lotunúmerin sem voru skuldbundin pöntun viðskiptavinarins hvenær sem er á líftíma hans, upp í gegnum reikninga.
    - Auk þess að panta sértæka lotu getur notandi valið handvirkt sértækan stað og framleiðslueiningar plötunnar í stað þess að láta kerfið velja þá sjálfkrafa. Þessi hæfileiki tengist hönnun pöntunarbundins fyrirkomulags fyrir pöntun. Eins og minnst var á hér á undan, þegar rununúmer er tekið frá fyrir vöru samkvæmt frátekningarreglunni *Runa fyrir neðan\[staðsetningu\]* verður kerfið að taka frá allar víddir upp í gegnum staðsetninguna. Þess vegna mun vörugeymsla hafa sömu geymsluvíddir og notendurnir sem unnu með pantanirnar áskildu og það gæti ekki alltaf táknað geymslu hlutarins sem er þægilegt eða jafnvel mögulegt fyrir tínaaðgerðir. Ef pöntunaraðilar eru meðvitaðir um takmarkanir vörugeymslu, gætu þeir viljað handvirkt velja tiltekna staði og leyfismerki þegar þeir panta hóp. Í þessu tilfelli verður notandinn að nota **Sýna mál** virkni á síðuhausnum og verður að bæta við staðsetningu og kennitala í ristina á flýtiflipanum **Yfirlit**.

6. Á **Hópapöntun** síðu, veldu línuna fyrir hópinn **B11** og veldu síðan **Varalína**. Það er engin tiltekin rökfræði til að úthluta staðsetningum og skiltum við sjálfvirka fyrirvara. Þú getur slegið inn magnið handvirkt í reitinn **Frátekning**. Taktu eftir því að á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu**, hópur **B11** er sýnt sem **Skuldbundinn**.

    ![Að staðfesta ákveðið rununúmer í sölupöntunarlínu á síðu frátektar á runu.](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Bókun magns á sölupöntunarlínu er hægt að gera í mörgum lotum. Sömuleiðis er hægt að panta sömu lotu gagnvart mörgum stöðum og skiltum (ef leyfisplötur eru virkar fyrir staðina).
    >
    > Pöntun á tiltekinni lotu fyrir magnið á sölupöntunarlínu getur einnig verið að hluta. Til dæmis er hægt að panta heildarmagn 100 eininga þannig að ákveðin lota er skuldbundin til 20 eininga en 80 einingar eru fráteknar á staðnum og vörugeymslustigi fyrir alla tiltæka lotu. Í þessu tilfelli mun WMS sjá um tínaaðgerðir með því að nota tvær aðskildar vinnulínur.

7. Farðu í **Afurðaupplýsingastjórnun** \> **Afurðir** \> **Losaðar afurðir**. Veldu hlutinn þinn og veldu síðan **Stjórna birgðum** \> **Skoða** \> **Færslur**.

    ![Frátekning á ráðstafaðri pöntun sem birgðafærslugerð.](media/Inventory-transactions-for-order-committed-reservation.png)

8. Skoðaðu birgðafærslur hlutarins sem tengjast pöntun sölupöntunarlínunnar.

    - Viðskipti þar sem **Tilvísun** reiturinn er stilltur á **Sölupöntun** og **Mál** reiturinn er stilltur á **Frátekin líkamleg** táknar pöntunarlínu fyrirvara fyrir birgðavíddir fyrir ofan **Staðsetning** stigi. Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir staða, vörugeymsla og birgðastaða.
    - Viðskipti þar sem reiturinn **Tilvísun** er stilltur á **Pöntunarbundna frátekt** og reiturinn **Úthreyfing** er stilltur á **Frátekið á lager** táknar pöntunarlínu frátektar fyrir tiltekna runu og annar birgðavíddir fyrir ofan hana. Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir rununúmer og staðsetning. Í þessu dæmi er staðsetningin **Magn-001**.

9. Veldu á sölupöntunarhaus **Vöruhús** \> **Aðgerðir** \> **Losa í vöruhús**. Pöntunarlínan hefur verið sett í bylgju og álag og vinna búin til.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Farið yfir og unnið úr vöruhúsagerð sem er með pöntunarbundna lotunúmer

1. Á flýtiflipanum **Sölupöntunarlínur**, veldu **Vöruhús** \> **Upplýsingar um vinnu**.

    Vinnan sem annast tínsluaðgerðina fyrir magn magn sem skuldbundið sig til sölupöntunarlínunnar hefur eftirfarandi einkenni:

    - Til að búa til vinnu notar kerfið vinnusniðmát en ekki staðsetningartilskipanir. Öllum stöðluðum stillingum sem eru skilgreindar fyrir vinnusniðmát, svo sem hámarksfjölda vallína eða ákveðin mælieining, verður beitt til að ákvarða hvenær ný vinna ætti að búa til. Hins vegar er ekki tekið tillit til reglnanna sem eru tengdar staðsetningarleiðbeiningum til að bera kennsl á valstöðum, vegna þess að pöntunin sem framin er fyrir pöntunin tilgreinir þegar allar birgðarvíddirnar. Þessar birgðastærðir innihalda mál á lagergeymslu stigsins. Þess vegna erfðir verkið þessar víddir án þess að þurfa að hafa samráð um staðsetningartilskipanir.
    - Lotunúmerið er ekki sýnt í tiltektarlínunni (eins og er gert fyrir vinnulínuna sem er stofnuð fyrir vöru sem er með tengt frátekningarstigveldi *Runa fyrir ofan\[staðsetningu\]*.) Í staðinn eru „frá“ rununúmerið og allar aðrar geymsluvíddir sýndar í birgðafærsluvinnu vinnulínunnar sem vísar er í úr tengdum birgðafærslum.

        ![Birgðafærsla vöruhúss fyrir vinnu sem kemur úr frátekningu á ráðstafaðri pöntun.](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Eftir að vinna er búin til, birgðir hlutarins þar sem **Tilvísun** reiturinn er stilltur á **Pöntunarbundin frátekt** er fjarlægður. Birgðafærslan þar sem **Tilvísun** reiturinn er stilltur á **Vinna** geymir nú líkamlegan fyrirvara á öllum birgðastærðum magnsins.

        Vöruhúsaaðgerðir geta haldið áfram til að sjá um framkvæmd verksins á venjulegan hátt. Leiðbeiningarnar í farsímanum munu hins vegar leiðbeina starfsmanni að velja ákveðið lotunúmer. Í vöruhúsaumhverfum þar sem staðsetningar eru númeraplötustýrðar, eftir að starfsmaður kemur á staðsetningu sem geymir rununa á mörgum númeraplötum, getur hann valið úr einhverri númeraplötu sem ekki er þegar frátekin (til dæmis með annarri frátekningu á ráðstafaðri pöntun eða vinnu sem verður til út frá frátekningu að þessari gerð.)

        Ef það reynist óframkvæmanlegt að velja frá þeim stað sem er tilgreindur á vinnulínunni geta rekstraraðilar vörugeymslu notað eina af eftirfarandi aðgerðum til að beina því að velja ákveðna lotu frá þægilegri stað:

        - Staðallinn **Hnekkja staðsetningu** aðgerð í farsíma (að því tilskildu að starfsmaður vörugeymslu **Leyfa val á staðsetningu staðsetningu** stilling er virk)
        - Aðgerðin **Breyta staðsetningu** á **Upplýsingar um vinnulista** síðu. 

2. Ljúktu við að velja og setja verkið í farsímann.

    Magnið **10** fyrir lotunúmer **B11** er nú valinn í sölupöntunarlínuna og settur í **Afgreiðsluhurð** staðsetningu. Á þessum tímapunkti er það tilbúið að hlaða það á vörubílinn og senda á heimilisfang viðskiptavinarins.

## <a name="flexible-license-plate-reservation"></a>Sveigjanleg frátekning númeraplötu

### <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Í þessum aðstæðum notar fyrirtæki vöruhúsakerfi og vinnuferli og sér um hleðsluáætlun á stigi einstakra bretta/gáma utan Supply Chain Management áður en vinna er stofnuð. Þessir gámar eru táknaðir með númeraplötum í birgðavíddunum. Fyrir þessa nálgun þarf þar af leiðandi að úthluta sérstökum númeraplötum fyrirfram á sölupöntunarlínur áður en tiltekt er gerð. Fyrirtækið leitar að sveigjanleika í því hvernig reglur um frátekningu númeraplötu eru meðhöndlaðar, þannig að eftirfarandi hegðun eigi sér stað:

- Hægt er að skrá og taka frá númeraplötu þegar pöntunin er tekin af úrvinnsluaðila sölumála og ekki er hægt að taka hana af öðrum eftirspurnum. Þessi hegðun hjálpar til við að tryggja að númeraplatan sem var áætluð sé send til viðskiptavinarins.
- Ef númeraplötunni hefur ekki þegar verið úthlutað á sölupöntunarlínu, getur starfsmaður í vöruhúsi valið númeraplötu meðan á tiltekt stendur, þegar búið er að ljúka skráningu sölupöntunar og frátekningu.

### <a name="turn-on-flexible-license-plate-reservation"></a>Kveikja á sveigjanlegri frátekningu númeraplötu

Áður en hægt er að nota sveigjanlega frátekningu númeraplötu, þarf að kveikja á tveimur eiginleikum í kerfinu. Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim ef þörf krefur. Kveikja verður á eiginleikunum í eftirfarandi röð:

1. **Heiti eiginleika:** *Sveigjanleg frátekt á vídd vöruhúsastigs*
1. **Heiti eiginleika:** *Sveigjanleg frátekt á númeraplötu ráðstafaðrar pöntunar*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Taka frá tiltekna númeraplötu í sölupöntuninni

Til að virkja frátekningu á númeraplötu í pöntun þarf að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stigið **Númeraplata** á síðunni **Frátekningarstigveldi birgða** fyrir stigveldið sem tengist viðkomandi vöru.

![Síða frátekningarstigveldis birgða fyrir sveigjanlegt frátekningarstigveldi númeraplötu.](media/Flexible-LP-reservation-hierarchy.png)

Hægt er að virkja frátekningu á númeraplötu í pöntuninni hvenær sem er í uppsetningunni. Þessi breyting hefur ekki áhrif á neinar frátekningar eða opna vöruhúsavinnu sem var stofnuð áður en breytingin var gerð. Hins vegar er ekki hægt að hreinsa gátreitinn **Leyfa frátekt á eftirspurnarpöntun** ef opnar birgðafærslur á útleið sem eru með úthreyfingarstöðuna *Í pöntun*, *Frátekið pantað* eða *Frátekið efnislegt magn* eru til fyrir eina eða fleiri vörur sem tengjast þessu frátekningarstigveldi.

Jafnvel ef gátreiturinn **Leyfa frátekt á eftirspurnarpöntun** er valinn fyrir stigið **Númeraplata** er enn mögulegt að *ekki* taka frá tiltekna númeraplötu í pöntuninni. Í slíku tilfelli gilda sjálfgefin rök vöruhúsaaðgerða fyrir frátekningarstigveldið.

Til að taka frá tiltekna númeraplötu þarf að nota [OData-ferli](../../fin-ops-core/dev-itpro/data-entities/odata.md). Í forritinu er hægt að gera þessa frátekningu beint úr sölupöntun með því að nota valkostinn **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu** fyrir skipunina **Opna í Excel**. Í einingagögnunum sem opnuð eru í Excel-innbótinni þarf að færa inn eftirfarandi frátektartengd gögn og síðan velja **Birta** til að senda gögnin aftur í Supply Chain Management:

- Tilvísun (eingöngu gildið *Sölupöntun* er stutt.)
- Pöntunarnúmer (gildið er hægt að fá úr lotu.)
- Lotukenni
- Númeraplata
- Magn

Ef taka þarf frá tiltekna númeraplötu fyrir runurakta vöru skal nota síðuna **Frátekt á runu**, eins og lýst er í hlutanum [Færa inn upplýsingar um sölupöntun](#sales-order-details).

Þegar sölupöntunarlína sem notar frátekt á númeraplötu ráðstafaðrar pöntunar er unnin af vöruhúsaaðgerðum, eru staðsetningarleiðbeiningar ekki notaðar.

Ef vinnuliður vöruhúss samanstendur af línum sem jafngilda heilu bretti og eru með númeraplöturáðstafað magn, er hægt að fínstilla tiltektina með því að nota valmyndaratriði fartækis þar sem valkosturinn **Meðhöndla eftir númeraplötu** er stilltur á *Já*. Starfsmaður í vöruhúsi getur síðan skannað númeraplötu til að ljúka tiltekt í stað þess að þurfa að skanna vörurnar úr vinnunni hver á eftir annarri.

![Valmyndaratriði fartækis þar sem valkosturinn „Meðhöndla eftir númeraplötu" er stilltur á „Já“.](media/Handle-by-LP-menu-item.png)

Vegna þess að virknin **Meðhöndla eftir númeraplötu** styður ekki vinnu sem nær yfir mörg bretti, er betra að vera með aðskilinn vinnulið fyrir mismunandi númeraplötur. Til að nota þessa aðferð skal bæta reitnum **Númeraplötukenni ráðstafaðrar pöntunar** sem vinnuhausaskil á síðunni **Vinnusniðmát**.

> [!NOTE]
> Fyrir stofnferli á vinnu ráðstafaðrar pöntunar, verður gildinu „birgðavíddir ráðstafaðrar pöntunar“ úthlutað á vinnulínur tiltektar og ekki verið mögulegt að skoða gildið á númeraplötunni með beinum hætti. Aðeins *Notandastýrt* ferli er stutt þegar valmyndaratriði fartækis er sett upp.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Dæmi: Setja upp og vinna úr frátekt á númeraplötu ráðstafaðrar pöntunar

Þessi atburðarás sýnir hvernig á að setja upp og vinna úr frátekt á númeraplötu ráðstafaðrar pöntunar.

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Þessi atburðarás vísar í gildi og færslur sem eru innifalin í stöðluðum sýnigögnum sem boðið er upp á fyrir Supply Chain Management. Ef ætlunin er að fara í gegnum atburðarásina með því að nota gildin sem hér eru gefin skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett. Þar að auki skal stilla lögaðilann á **USMF** áður en hafist er handa.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Stofna frátekningarstigveldi birgða sem leyfir frátekningu á númeraplötu

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> Frátekningarstigveldi**.
1. Veljið **Nýtt**.
1. Í reitinn **Heiti** skal slá inn gildi (til dæmis *FlexibleLP*).
1. Í reitinn **Lýsing** skal færa inn gildi (til dæmis *Sveigjanleg frátekning á númeraplötu*).
1. Í listanum **Valið** skal velja **Rununúmer**, **Raðnúmer** og **Eigandi**.
1. Veljið hnappinn **Fjarlægja** ![Ör til baka.](media/backward-button.png) til að flytja valdar færslur í listann **Tiltækt**.
1. Veldu **Í lagi**.
1. Í línunni fyrir víddarstigið **Númeraplata** skal velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun**. Stigið **Staðsetning** er valið sjálfkrafa og ekki er hægt að hreinsa gátreitinn fyrir það.
1. Veljið **Vista**.

### <a name="create-two-released-products"></a>Stofna tvær útgefnar afurðir

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svarglugganum **Ný útgefin afurð** skal stilla eftirfarandi gildi:

    - **Afurðarnúmer:** *Item1*
    - **Vörunúmer:** *Item1*
    - **Vörulíkanaflokkur:** *FIFO*
    - **Vöruflokkur:** *Hljóð*
    - **Geymsluvíddarflokkur:** *Afurð*
    - **Rakningarvíddarflokkur:** *Enginn*
    - **Frátekningarstigveldi:** *FlexibleLP*

1. Veljið **Í lagi** til að stofna afurðina og loka svarglugganum.
1. Nýja afurðin opnast. Í flýtiflipanum **Vöruhús** skal stilla reitinn **Auðkenni röðunarflokks einingar** á *ea*.
1. Endurtakið fyrri skref til að stofna aðra afurð sem er með sömu stillingar, en stillið reitina **Afurðarnúmer** og **Vörunúmer** á *Item2*.
1. Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Skoða**, skal velja **Lagerbirgðir**. Veljið síðan **Leiðrétting á magni**.
1. Leiðréttið lagerbirgðir nýju varanna eins og tilgreint er í eftirfarandi töflu.

    | vara  | Vöruhús | Staður | Númeraplata | Magn |
    |-------|-----------|----------|---------------|----------|
    | VARA1 | 24        | FL-010   | LP01          | 10       |
    | VARA1 | 24        | FL-011   | LP02          | 10       |
    | VARA2 | 24        | FL-010   | LP01          | 5        |
    | VARA2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > Stofna þarf tvær númeraplötur og nota staðsetningar sem leyfa blandaðar vörur, svo sem *FL-010* og *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Stofna sölupöntun og taka frá tiltekna númeraplötu

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *24*

1. Veljið **Í lagi** til að loka svarglugganum **Stofna sölupöntun** og opnið nýju sölupöntunina.
1. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:

    - **Vörunúmer:** *Item1*
    - **Magn:** *10*

1. Bæta við annarri sölupöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *Item2*
    - **Magn:** *5*

1. Veljið **Vista**.
1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Uppsetning**, skal skrá hjá sér gildið **Lotukenni** fyrir hverja línu. Þessi gildi eru nauðsynleg þegar tilteknar númeraplötur eru teknar frá.

    > [!NOTE]
    > Til að taka frá tiltekna númeraplötu þarf að nota gagnaeininguna **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu**. Til að taka frá runurakta vöru á tiltekinni númeraplötu er einnig hægt að nota síðuna **Frátekt á runu**, eins og lýst er í hlutanum [Færa inn upplýsingar um sölupöntun](#sales-order-details).
    >
    > Ef númeraplata er færð beint inn í sölupöntunarlínuna og hún síðan staðfest í kerfinu, verður vinnsla vöruhúsakerfis ekki notuð fyrir línuna.

1. Veljið **Opna í Microsoft Office**, veljið **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu** og hlaðið niður skránni.
1. Opnið niðurhalaða skrá í Excel og veljið **Virkja breytingar** svo að Excel-innbótin geti keyrt.
1. Ef verið er að keyra í Excel-innbót í fyrsta sinn, er valið **Treysta þessari innbót**.
1. Ef beðið er um að skrá sig inn skal velja **Innskráningu**, og síðan skrá sig inn með því að nota sömu innskráningarupplýsingar og eru notuð til að skrá sig inn í Supply Chain Management.
1. Til að taka frá vöru á tiltekinni númeraplötu, í Excel-innbótinni, skal velja **Ný** til að bæta við frátektarlínu og stilla síðan eftirfarandi gildi:

    - **Lotukenni:** Færið inn gildið fyrir **Lotukenni** sem fannst sölupöntunarlínuna fyrir *Item1*.
    - **Númeraplata:** *LP02*
    - **ReservedInventoryQuantity:** *10*

1. Veljið **Ný** til að bæta við annarri frátektarlínu og stillið eftirfarandi gildi:

    - **Lotukenni:** Færið inn gildið fyrir **Lotukenni** sem fannst sölupöntunarlínuna fyrir *Item2*.
    - **Númeraplata:** *LP02*
    - **ReservedInventoryQuantity:** *5*

1. Í Excel-innbótinni skal velja **Birta** til að senda gögnin aftur í Supply Chain Management.

    > [!NOTE]
    > Frátektarlínan birtist aðeins í kerfinu ef birtingu er lokið án villna.

1. Farið aftur í Supply Chain Management. 
1. Til að yfirfara frátekningu vörunnar, í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Birgðir**, skal velja **Vinna með \> Frátekning**. Athugið að fyrir sölupöntunarlínuna fyrir *Item1* eru birgðir upp á *10* teknar frá og fyrir sölupöntunarlínuna fyrir *Item2*, eru birgðir upp á *5* teknar frá.
1. Til að fara yfir birgðafærslur sem tengjast frátekningu sölupöntunarlínu, í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Birgðir**, skal velja **Skoða \> Færslur**. Athugið að tvær færslur eru tengdar frátekningunni: ein þar sem reiturinn **Tilvísun** er stilltur á *Sölupöntun* og ein þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun*.

    > [!NOTE]
    > Færsla þar sem reiturinn **Tilvísun** er stilltur á *Sölupöntun* sýnir frátekningu pöntunarlínu fyrir birgðavíddir sem eru fyrir ofan stigið **Staðsetning** (svæði, vöruhús og birgðastaða). Færsla þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun* sýnir frátekningu pöntunarlínu fyrir tiltekna númeraplötu og staðsetningu.

1. Til að losa sölupöntunina, á aðgerðasvæðinu, í flipanum **Vöruhús**, í flokknum **Aðgerðir**, skal velja **Losa í vöruhús**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Yfirfara og vinna úr vöruhúsavinnu með úthlutaðar númeraplötur ráðstafaðrar pöntunar

1. Í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Vöruhús**, skal velja **Upplýsingar um vinnu**.

    Þar sem frátekning er gerð fyrir tiltekna runu, notar kerfið ekki staðsetningarleiðbeiningar þegar það stofnar vinnu fyrir sölupöntunina sem notar frátekningu númeraplötu. Vegna þess að frátekning ráðstafaðrar pöntunar tilgreinir allar birgðavíddir, þ.á.m. staðsetningu, þarf ekki að nota staðsetningarleiðbeiningar vegna þess að birgðavíddir eru aðeins færðar inn í vinnuna. Þær eru sýndar í hlutanum **Úr birgðavíddum** á síðunni **Birgðafærslur vinnu**.

    > [!NOTE]
    > Þegar búið er að stofna vinnu, er birgðafærsla vörunnar þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun* fjarlægð. Birgðafærslan þar sem reiturinn **Tilvísun** er stilltur á *Vinna* inniheldur nú efnislega frátekningu fyrir allar birgðavíddir magns.

1. Í fartækinu skal ljúka tiltekt og frágangi vinnunnar með því að nota valmyndaratriði þar sem gátreiturinn **Meðhöndla eftir númeraplötu** er valið.

    > [!NOTE]
    > Aðgerðin **Meðhöndla eftir númeraplötu** sér um að vinna úr allri númeraplötunni. Ef nauðsynlegt er að vinna úr hluta númeraplötunnar, er ekki hægt að nota þessa aðgerð.
    >
    > Mælt er með því að aðskilin vinna sé búin til fyrir hverja númeraplötu. Til að ná þessu fram skal nota eiginleikann **Vinnuhausaskil** á síðunni **Vinnusniðmát**.

    Númeraplata *LP02* er nú tínd fyrir sölupöntunarlínur og komið fyrir á staðsetningunni *Útskot*. Á þessu stigi má hlaða og senda hana til viðskiptavinarins.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Meðhöndlun undantekninga á vöruhúsavinnu sem er með rununúmer ráðstafaðra pantana

Vörugeymsla til að velja pöntunarbundin lotunúmer er háð sömu stöðluðu meðhöndlun undantekninga vörugeymslu og aðgerðum og venjuleg vinna. Almennt er hægt að hætta við opna verkið eða vinnu línuna, það er hægt að trufla það vegna þess að notendastaður er fullur, það er hægt að velja hann stutt og það er hægt að uppfæra hann vegna hreyfingar. Sömuleiðis er hægt að draga úr valinni vinnu sem þegar hefur verið lokið eða hægt er að snúa verkinu við.

Eftirfarandi lykilregla er notuð við allar þessar undantekningarmeðferðaraðgerðir: aldrei er hægt að skipta um lotunúmer sem var frátekið fyrir viðskiptavininn fyrir annað lotunúmer, en hægt er að breyta geymsluvíddum hans (staðsetningu og kennitala) með annað hvort handvirkri uppfærslu af notanda eða sjálfvirka uppfærslu af kerfinu. Sjálfvirka uppfærslan er byggð á sömu handahófi úthlutun geymsluvíddar og gilti þegar ákveðin lota var sjálfkrafa frátekin en engar geymsluvíddir voru tilgreindar.

### <a name="example-scenario"></a>Dæmi

Dæmi um þessa atburðarás er ástand þar sem verið er að velja áður lokið verk með því að nota virknina **Draga úr völdu magni**. Þetta dæmi gerir ráð fyrir því að skrefunum sem lýst er í [Sýniaðstæður: Úthlutun rununúmers](#Example-batch-allocation) sé lokið. Það heldur áfram þar sem frá var horfið í því dæmi.

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
<li>Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í farsímaforriti vöruhúsakerfis þegar tiltektarverk er hafið.</li>
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
<td>Ekki tiltækt</td>
</tr>
<tr>
<td>Nei</td>
<td>
<ol>
<li>Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í farsímaforriti vöruhúsakerfis þegar tiltektarverk er hafið.</li>
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
<td>Ekki tiltækt</td>
<td>
<ol>
<li>Veljið valmyndaratriðið <strong>Fullt</strong> í farsímaforriti vöruhúsakerfis þegar tiltektarverk er hafið.</li>
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
<td>Nei</td>
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
<li>Hefja færslu í farsímaforriti vöruhúsakerfis.</li>
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
<td>Nei</td>
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
<td>Nei</td>
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
<td>Nei</td>
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
<li>Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</li>
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
<td>Nei</td>
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
<li>Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</li>
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
<td>Nei</td>
<td>Sjá fyrri línuna.</td>
<td>Sjá fyrri línuna.</td>
<td>Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru fjarlægðar.</td>
</tr>
<tr>
<td>Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei/Já</strong>. Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</td>
<td>Já</td>
<td>
<ol>
<li>Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</li>
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
<td>Nei</td>
<td>
<ol>
<li>Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</li>
<li>Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</li>
<li>Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</li>
</ol>
</td>
<td>Of lítil tiltekt-aðgerðin mistekst og villu er hent.</td>
<td>Á ekki við</td>
</tr>
<tr>
<td>Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>. Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</td>
<td>Nei</td>
<td>
<ol>
<li>Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</li>
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
<td>Ekki tiltækt</td>
<td>
<ol>
<li>Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</li>
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
<td>Nei</td>
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
<td>Nei</td>
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

## <a name="see-also"></a>Sjá einnig

- [Rununúmer í Vöruhúsakerfi](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [Frátekning sömu runu fyrir sölupöntun](../sales-marketing/reserve-same-batch-sales-order.md)
- [Taka til elstu runu í fartæki](pick-oldest-batch.md)
- [Staðfesting lotu og númeraplötu](batch-and-license-plate-confirmation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Vöruhúsafgreiðsla á farmi á innleið fyrir innkaupapantanir
description: Þetta efni lýsir afgreiðsluferli vöruhúss fyrir farma á innleið fyrir innkaupapantanir.
author: omulvad
manager: tfehr
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 41a05bcd0148d0a553cb50575cae47f48397ae9b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430659"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Vöruhúsafgreiðsla á farmi á innleið fyrir innkaupapantanir

Þetta efni lýsir afgreiðsluferli vöruhúss fyrir farma á innleið fyrir innkaupapantanir.

Fyrir hvern farm á innleið ætti kerfið þitt nú þegar að innihalda tengda sölupöntun og hún gæti einnig innihaldið tengda forskrift og/eða flutningsáætlun farms. Nánari upplýsingar um hvernig á að stofna og stjórna farmi á innleið, sjá [Viðskiptaferli: Áætlun flutningsstjórnunar fyrir farma á innleið](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Yfirlit: Hvernig farmar á innleið er stofnaðir, skráðir og mótteknir

Eftirfarandi mynd sýnir dæmigert flæði til að meðhöndla farma á innleið sem er með innkaupapöntunarmagn þegar þeir berast í vöruhúsið.

![Ferlið við meðhöndlun farms á innleið](media/inbound-process.png "Ferlið við meðhöndlun farms á innleið")

1. **Lánardrottinn staðfestir innkaupapöntunina.**

    Ferlið hefst þegar innkaupapöntun er sett inn í kerfið og síðan afhent lánardrottni, sem staðfestir pöntunina. Innkaupapöntunin verður að vera til áður en hægt er að stofna farmskrá. Hins vegar er hægt að stofna farm á innleið jafnvel þó að pöntunin hafi ekki verið staðfest. Fyrir frekari upplýsingar, sjá [Samþykkja og staðfesta innkaupapantanir](../procurement/purchase-order-approval-confirmation.md).

1. **Farmskrá á innleið er stofnuð til að áætla komuna og innihald hennar.**

    Farmskrá á innleið táknar sendingu lánardrottins á einni eða fleiri innkaupapöntunum. Búist er við að farmurinn berist til vöruhússins sem ein efnisleg flutningseining (eins og flutningabíll). Farmskrá á innleið er notuð í skipulagsskyni og gerir samræmingaraðila flutninga kleift að fylgjast með framvindu farmsins frá lánardrottni. Hann er einnig notaður til að skrá magn pöntunarlínum og stjórna framvindu með aðgerðum vöruhúss, svo sem komu- og frágangsvinnu. Hægt er að búa til farm annaðhvort sjálfkrafa eða handvirkt og þeir geta verið byggðar á annaðhvort innkaupapöntun eða ítarlegri tilkynningu um sendingu (ASN) frá lánardrottni. Fyrir frekari upplýsingar, sjá [Stofna eða breyta farmi á innleið](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Lánardrottinn staðfestir sendingu farms.**

    Þegar lánardrottinn sendir farminn staðfestir flutningsstjórinn í móttöku vöruhússins sendingu farmsins. Ef móttökufyrirtækið notar eininguna **Flutningsstjórnun** mun staðfesting á sendingu á innleið kalla fram önnur ferli við stjórnun álags sem eru tengd farmi á innleið. Fyrir frekari upplýsingar, sjá [Staðfesta farm fyrir sendingu](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Farmurinn berst í vöruhús og starfsmenn skrá magn.**

    Þegar flutningabifreið kemur á móttökusvæði vöruhússins skrá starfsmenn vöruhússins álagsmagnið. Þegar einingin **Vöruhúsastjórnun** er notuð gera starfsmenn skráninguna með því að nota fartæki. Fyrir frekari upplýsingar, sjá [Innhreyfingarskjal afurða gegn innkaupapöntunum - skráning](../procurement/product-receipt-against-purchase-orders.md#registration) og hlutann [Skrá vörumagn sem berst í farmi á innleið](#register-item-quantities-arriving).

1. **Skráð álagsmagn er bókað gegn innkaupapöntunum.**

    Þegar álagsmagnið hefur verið skráð sem komið verður það magn að vera innhreyfingarskjal afurða–bókað í birgðabók fyrirtækisins til að skrá efnislega hlutafjáraukningu. Fyrir frekari upplýsingar, sjá [Innhreyfingaskjal afurða gegn innkaupapöntunum - innhreyfingarskjal afurða](../procurement/product-receipt-against-purchase-orders.md#product-receipt) og [Bóka skráða afurðamagn gegn innkaupapöntunum](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Skráðu vörumagn sem berst í farmi á innleið

Microsoft Dynamics 365 Supply Chain Management styður nokkrar rekstraraðferðir við skráningu á komu pantaðra vara. Þess vegna geturðu stillt kerfið þannig að það passi við sérstakar viðskiptakröfur þínar. Þessi hluti lýsir því hvernig á að skrá vörumagn á innleið með því að nota fartæki þegar kveikt er á ítarlegri vöruhússtjórnun í kerfinu. Hins vegar er annað flæði til sem byggist á því að nota komubókar vöru í stað fartækis. Nánari upplýsingar um það flæði er að finna í [Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók vöru](tasks/register-items-advanced-warehousing.md).

Þegar farmur á innleið berst fyrst í vöruhúsið verða starfsmenn vöruhússins að skrá það vörumagnið sem er innifalið í sendingunni. Yfirleitt nota þeir lófatölvuskanna. Þetta verkflæði er aðeins tiltækt ef eftirfarandi vörur eru til staðar í kerfinu:

- **Farmskrá á innleið sem lýsir vörumagni sem búist er við í sendingu**

    Yfirleitt staðfestir lánardrottinn farmskrá á innleið áður en sendingin berst í vöruhúsið. Þess vegna hefur farmurinn stöðuna _Sent_. Samt sem áður geta starfsmenn vöruhúss einnig skráð vörumagn fyrir farma sem hafa stoðuna _Opið_ eða _Móttekið_.

- **Valmynd fartækis sem er stillt til að styðja við móttöku farms**

    [Vöruhúsaforritið](install-configure-warehousing-app.md) fyrir fartæki styður eftirfarandi stofnun verka:

    - Móttaka farmvöru
    - Móttaka og frágangur farmvöru
    - Móttekin blönduð númeraplata þar sem reiturinn **Auðkennisaðferð línu upprunaskjals** fyrir valmyndaratriði farsíma er stilltur á _Móttaka farmvöru_. Fyrir frekari upplýsingar, sjá [Móttaka blandaðrar númeraplötu](mixed-license-plate-receiving.md).
    - Móttekin blönduð númeraplata og frágangur þar sem reiturinn **Auðkennisaðferð línu upprunaskjals** fyrir valmyndaratriði farsíma er stilltur á _Móttaka farmvöru_. Fyrir frekari upplýsingar, sjá [Móttaka blandaðrar númeraplötu](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Burtséð frá ferlinu mun kerfið mynda vinnu til að taka magn sem er skráð á móttökustaðnum og ganga frá því á venjulegum geymslustað. Þegar ferlið _Móttaka og frágangur farmvöru_ eða _Móttaka og frágangur blandaðrar númeraplötu_ er notað mun starfsmaðurinn sem skráði farmmagnið einnig fá leiðbeiningar úr tækinu um að gera frágangsvinnuna sem hluta af skráningarverkinu. Aftur á móti fyrir ferlin _Móttaka farmvöru_ og _Móttaka blandaðrar númeraplötu_ er forsendan sú að frágangsvinna verður unnin aðskilið frá skráningarverkinu.

- **Vinnusniðmát sem skilgreinir tínslu- og frágangsvinnu fyrir komandi farma**

    Þessi vara er tengdur fyrri vörum. Þú verður að hafa að minnsta kosti eitt vinnusniðmát fyrir vinnupöntunargerðina _innkaupapöntun_ og hún verður að innihalda mengi gerða tínslu-/frágansvinnu.

Fartækið leiðbeinir starfsmanni í vöruhússmóttökunni í gegnum flæðið fyrir skráningu farmmagns. Að lágmarki inniheldur þetta flæði eftirfarandi skref fyrir hvert farmkenni:

1. Færru inn farmkennið.
2. Færið inn vörunúmer fyrir móttekna vöru.
3. Sláðu inn magn þess vörunúmers sem er móttekið.
4. Sláðu inn númeraplötunúmer fyrir upphafsstað vörunnar ef kerfið er ekki sett upp til að mynda þetta númer sjálfkrafa.
5. Ýttu á **Í lagi**.

Þegar starfsmaðurinn hefur lokið þessum skrefum gerir kerfið eftirfarandi uppfærslur á viðeigandi einingum að því tilskildu að magn innkaupapöntunarlínu hafi borist í einum farmi og allt farmmagn hafi verið skráð:

| Eining | Uppfærslur | Nóta |
|---|---|---|
| Sækja | Reiturinn **Magn stofnaðrar vinnu** í farmlínunni er uppfærður til að sýna skráð magn. | Gildið **Farmstaða** verður áfram _Sent_ eða _Opið_ ef engin sendingarstaðfesting hefur verið keyrð fyrir farminn. Ef að minnsta kosti ein lína frágangs hefur verið hafin er henni breytt í _Í vinnslu_. |
| Birgðafærsla innkaupapöntunar sem tengt farmmagn hefur verið skráð fyrir |<p>Eftirfarandi svæði eru uppfærð:</p><ul><li>Reiturinn <b>Innhreyfing</b> er stilltur á <i>Skráð.</i></li><li>Reiturinn <b>Staðsetning</b> er uppfærður með staðsetningarkóða fyrir móttökusvæðið. (Þessi kóði er tilgreindur í reitnum <b>Sjálfgefin staðsetning innhreyfinga</b> fyrir hvert vöruhús.)</li><li>Reiturinn <b>Númeraplata</b> er uppfærður með númeraplötunúmerinu sem var slegið inn eða myndað við skráninguna.</li><li>Reiturinn <b>Farmkenni</b> er uppfærður með númeri farmsins sem magnið hefur verið skráð á. (Sjá athugasemdina.)</li></ul> | Hæfni til að tengja á milli birgðafærslna innkaupapöntunar og magninu sem er skráð gegn farminum var kynnt í útgáfu 10.0.9 sem valfrjáls eiginleiki sem heitir _Tengja birgðafærslu innkaupapöntunar við farm_. Þessi eiginleiki er sérstaklega gagnlegur fyrir aðgerðaflæði þar sem ein pöntun á keyptum vörum er afhent sem margir farmar, eða þegar álag inniheldur magn fyrir margar innkaupapantanir. |
| Vöruhúsafrágangur | Vinna er stofnuð á grundvelli vinnusniðmáts, til að leiðbeina starfsmanni að færa skráð magn af móttökustað yfir á venjulegan geymslustað. | Val á geymslustað er stjórnað af tilskipun frágangsstaðsetningar. Ef engin staðsetningartilskipun hefur verið skilgreind er frágangsstaðsetning vinnunnar tóm. |

Athugaðu að starfsmenn vöruhúsa geta skráð innhreyfingu innkaupapöntunar með einu eða fleiri tengdum förmum án þess að nota ferlið _Móttaka farmvöru_. Eftirtaldar aðferðir eru tiltækar:

- **Í fartækinu:** Notaðu ferlin _Móttaka innkaupapöntunarlínu_ og _Móttaka og frágangur innkaupapöntunarlínu_. (Ef fleiri en einn farmur er til fyrir magn innkaupapöntunarlínunnar getur starfsmaðurinn ekki notað ferlið _Móttaka innkaupapöntunarlínu_. Þess í stað verðar starfsmanni gefinn fyrirmæli um að nota aðgerðina sem tengist ferlinu _Móttaka farmvöru_.)
- **Á biðlaranum:** Notaðu komu komubók vöru.
- **Á biðlaranum:** Notaðu aðgerðina **Skráning** sem hægt er að nálgast úr innkaupapöntunarlínunni.

> [!NOTE]
> Ef innkaupapöntunarkvittun er skráð með einhverjum af fyrri aðferðum er enginn tengill búinn til milli innkaupafyrirmæla og álagsins, jafnvel þó kveikt sé á eiginleikanum _Tengja birgðafærslu innkaupapöntunar við farm_. Ein undantekning frá þessari reglu er þegar þú notar valkostinn **Móttaka innkaupapöntunarlínu** og aðeins einn farmur hefur aðra stöðu en _Móttekið_ fyrir pöntunarlínuna.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Meðhöndla misræmi við skráningu farms á innleið

Starfsmenn vöruhúsa geta gert hlutfallslega skráningu á móttöku farms. Hver hlutfallsleg skráning á móttöku farms skapar síðan sérstaka birgðafærslu sem hefur móttökustöðuna _Skráð_ fyrir skráð magn og lotukennið vísar til upphaflegrar innkaupapöntunarlínu.

#### <a name="load-under-receiving"></a>Undirmóttaka farms

Þegar farmur berst, ef vörumagn er minna en það magn sem fram kemur á farmskránni, geta starfsmenn vöruhúsa unnið beint á biðlaranum til að viðurkenna þetta misræmi með því að minnka magnið á farmlínunni þannig að það passi við raunverulegt magn sem barst og var skráð.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Ofmóttaka farms

Ofmóttaka á sér stað þegar farmur berst og vörumagn fer yfir áætlað magn farmlína. Þú getur stjórnað því hvort og að hve miklu leyti ofmóttaka er leyfð við skráningu álags.

Notaðu reitinn **Ofmóttaka farms** fyrir viðeigandi valmyndaratriði farsíma til að stjórna því sem gerist þegar starfskraftur vöruhúss reynir að skrá ofafhendingu. Þessi reitur er tiltækur fyrir valmyndaratriði fartækja sem nota eftirfarandi gerðir af vinnusköpunarferlum:

- Móttaka farmvöru
- Móttaka og frágangur farmvöru
- Móttekin blönduð númeraplata (þegar reiturinn **Auðkennisaðferð línu upprunaskjals** er stilltur á _Móttaka farmvöru_).
- Móttekin blönduð númeraplata og frágangur (þegar reiturinn **Auðkennisaðferð línu upprunaskjals** er stilltur á _Móttaka farmvöru_).

Eftirfarandi tafla útskýrir valkosti sem eru tiltækir fyrir reitinn **Ofmóttaka farms**.

| Virði | lýsing |
|---|---|
| Leyfa | Starfsmenn geta skráð móttöku magns sem fer yfir það óskráða magn sem eftir er fyrir valinn farm, en aðeins ef samtals skráður magn er ekki meira en magn innkaupapöntunarlínunnar sem er tengt farminum (eftir leiðréttingu fyrir prósentu ofafhendingar) . |
| Útiloka | <p>Starfsmenn geta ekki skráð móttöku magns sem er meira en eftirstandandi óskráð magn fyrir valinn farm (eftir leiðréttingu fyrir hlutfall ofafhendingar). Starfsmaður sem reynir að skrá móotökurnar mun fá villu og getur ekki haldið áfram fyrr en viðkomandi skráir magn sem er jafnt eða minna en það sem eftir er af óskráðu álagsmagni.</p><p>Sjálfgefið er að gildi ofafhendingarhlutfalls á farmlínu sé afritað úr tengdri innkaupapöntunarlínu. Þegar reiturinn <b>Ofmóttaka farms</b> er stilltur á <i>Loka fyrir</i> notar kerfið prósentugildi ofafhendingar til að reikna út heildarmagn sem hægt er að skrá fyrir farmlínu. Samt sem áður er hægt að skrifa yfir það gildi fyrir einstaka farma eftir þörfum. Þessi hegðun verður viðeigandi við móttöku flæðis þar sem sumu eða öllu umframmagninu sem táknar hlutfall ofarhendingar pöntunarlínunnar er dreift óhóflega á marga farma. Eftirfarandi er dæmi um aðstæður:</p><ul><li>Það er margir farmar fyrir eina innkaupapöntunarlínu.</li><li>Innkaupapöntunarlínan er með ofafhendingarhlutfall sem er hærra en 0 (núll).</li><li>Magn hefur þegar verið skráð á móti einum eða fleiri farmi án þess að taka tillit til hlutfalls ofafhendingar.</li><li>Magnið ofafhendingar berst í síðasta farminum.</li></ul><p>Í þessari atburðarás er aðeins hægt að nota fartæki til að skrá umframmagn fyrir síðasta farm ef umsjónarmaður vöruhúss eykur hlutfall ofafhendingar fyrir viðkomandi farmlínu úr sjálfgefnu gildi í gildi sem er nógu stórt til að full ofafhending geti vera skráð með endanlegum farmi.</p> |
| Eingöngu útiloka fyrir lokaðar hleðslur | Starfsmenn geta ofmóttekið magn úr farmlínum fyrir opna farma, en ekki fyrir farma sem hafa stöðuna _Móttekið_. |

> [!NOTE]
> Sjálfgefið gildi í reitnum **Ofmóttaka farms** er _Leyfa_. Þegar þetta gildi er notað passar hegðunin við venjulega hegðun sem var tiltæk áður en eiginleikinn _Ofmóttaka á farmmagni_ var kynntur í útgáfu 10.0.11.

### <a name="put-away-the-registered-quantities"></a>Ganga frá skráðu magni

Þegar skráningu er lokið í fartækinu uppfærir aðgerðin _Skráningar á móttöku magns_ skrár birgða og vöruhúss til að gefa til kynna að magnið sé nú á móttökusvæðinu og að hægt sé að panta það. Hins vegar krefst vörugeymsla fyrirtækisins venjulega að magnið verði flutt af móttökusvæðinu í venjulegt vöruhús, svo að síðari tínsluferli geti átt sér stað. Leiðbeiningar um frágang eru teknar í frágangsvinnunni sem myndast sjálfkrafa þegar farmur á innleið er skráður sem móttekinn.

Þegar starfsmaður vöruhússins hefur lokið frágangsvinnunni skráir kerfið og rekur niðurstöðuna með því að uppfæra uppfærslur nokkurra eininga, eins og dregið er saman í eftirfarandi töflu.

| Eining | Uppfærslur | Nóta |
|---|---|---|
| Sækja | <p>Eftirfarandi svæði eru uppfærð:</p><ul><li>Gildinu <b>Farmstöðu</b> er breytt í <i>Í vinnslu</i>.</li><li>Gildinu <b>Vinnustaða</b> er breytt í <i>100,00% vinnu lokið</i>.</li></ul> | Gildinu **Farmstaða** er breytt í _Í vinnslu_ þegar starfsmaðurinn byrjar frágangsverkið í að minnsta kosti einni línu af frágangsvinnu. |
| Birgðafærslur á vinnu sem gengið hefur verið frá tengdu magni fyrir | Reitirnir **Móttaka** og **Staðsetning** og aðrir viðeigandi reitir eru uppfærðir til að endurspegla flutning frá móttökustað til geymslustaðar. | Gildið **Móttökustaða** í birgðafærslu innkaupapöntunar er áfram _Skráð_. |
| Vöruhúsafrágangur | Gildið **Vinnustaða** hefur breyst í _Lokað_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Bóka skráð afurðamagn gegn innkaupapöntunum

Eftir að afurðamagn á innleið er skráð í kerfið verða þau tiltæk fyrir frátekningu í tengslum við sölu og aðrar innri aðgerðir og á útleið. Hins vegar uppfærir kerfið ekki enn birgðareikninga (tímabundna). Þessi uppfærsla getur aðeins átt sér stað þegar aðgerðateymið birtir skráð innhreyfingarskjöl afurða.

Til að opna síðu þar sem þeir geta bókað innhreyfingarskjal afurða geta meðlimir aðgerðateymisins fylgst _einu_ af þessum skrefum:

- Opnaðu viðeigandi farmskrá og veldu síðan aðgerðina **Innhreyfingarskjal afurða**.
- Farðu í **Vöruhúsastjórnun \> Reglubundin verk \> Uppfærðu innhreyfingarskjöl afurða** og síðan, í reitnum **Kenni farms**, tilgreinirðu farm sem á að bóka.
- Opnaðu viðeigandi innkaupapöntun og veldu síðan aðgerðina **Innhreyfingarskjal afurða**.
- Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Móttaka afurða \> Bókunarvinnsla Innhreyfingarskjals afurða**.

Aðgerðin **Innhreyfingarskjal afurða** sem er í boði á síðunni **Farmur** (og á samsvarandi síðu uppfærsluvinnslunna **Uppfæra innhreyfingarskjöl afurða**) getur aðeins uppfært magn kvittunar vöru á innkaupapöntunarmagni sem hafa stöðuna _Skráð_. Hins vegar getur aðgerðin **Innhreyfingarskjal afurða** sem er í boði á síðunni **Innkaupapöntun** innihaldið magn í báðum vinnslustöðum (_Pantað_ og _Skráð_). Hún getur einnig stjórnað umfangi bókunar innhreyfingarskjala afurða með fleiri færibreytum, eins og _Magn sem móttaka á nú_ og _Skráð magn og þjónusta_.

Aðeins pantanir sem hafa stöðuna _Staðfest_ er hægt að bóka innhreyfingarskjal afurða. Fyrir innkaupapantanir sem ekki eru staðfestar mun aðgerðin **Innhreyfingarskjal afurða** birtast sem ekki tiltæk.

### <a name="post-registered-quantities-from-the-load-page"></a>Settu skráð magn af farmsíðunni

Til að bóka innhreyfingarskjal afurða af síðunni **Farmur** verða eftirfarandi forsendur að vera til staðar:

- Farmurinn verður að hafa að minnsta kosti eina magneiningu sem hefur stöðuna _Skráð_.
- Farmstaðan verður að vera _Sent_.
- Innkaupapöntunin sem er tengd farminum verður að hafa stöðu _Staðfest_.

> [!NOTE]
> Ef farmstaðan hefur ekki verið stillt á _Sent_, mun kerfið staðfesta álagið sjálfkrafa áður en það keyrir uppfærslu á innhreyfingarskjali afurðar. (Farmstaðan er stillt á _Sent_ þegar notandi skráir sendingu farmsins á innleið.)

Til að bóka innhreyfingarskjal afurða á komuskráningum sem tengjast völdum farmi velur starfsmaðurinn aðgerðina **Innhreyfingarskjal afurða** á síðunni **Farmur**. Síðan sem opnuð er hefur eftirfarandi lykilupplýsingar:

- Reiturinn **Magn** í kaflanum **Færibreytur** á flipanum **Stillingar** sýnir _skráð magn_. Engir aðrir kostir eru í boði hér.
- Taflan á flipanum **Yfirlit** sýnir allar innkaupapantanir sem fylgja með völdum farmi.
- Taflan á flýtiflipanum **Línur** sýnir allar pöntunarlínur sem eru með skráð magn.

> [!NOTE]
> Magn fyrir pöntunarlínur sem birtast á flipanum **Lína** er reiknað á annan hátt, eftir því hvort aðgerðin _Leyfa mörg innhreyfingarskjöl á farm_ er fáanleg og kveikt á henni í útgáfu þinni af Supply Chain Management.
>
> | Útgáfa | Útreikningur |
> |---|---|
> | Útgáfur fyrir útgáfu 10.0.10 og nýrri útgáfur þar sem ekki er kveikt á eiginleikanum _Leyfa mörg innhreyfingarskjöl á farm_ | Línumagnið er samtals allt skráð magn _fyrir þá innkaupapöntunarlínu_, óháð því hvort skráning var gerð á mörgum farmi, óháð álagi, úr farsíma eða frá viðskiptavininum. |
> | Útgáfa 10.0.10 og nýrri þar sem kveikt er á eiginleikanum _Leyfa mörg innhreyfingarskjöl á farm_ | Línumagnið er samtals allt skráð magn _fyrir farmskrá_ sem aðgerðin **Bókun innhreyfingarskjals afurða** var hafin úr. |

Þegar notandinn velur **Í lagi** til að staðfesta bókun innhreyfingarskjals afurða gerir kerfið eftirfarandi lykiluppfærslur um viðeigandi eininga.

| Eining | Uppfærslur |
|---|---|
| Birgðafærsla á innkaupapöntuninni þar sem línumagn hefur verið innifalið í bókunarumfanginu | <p>Eftirfarandi reitir eru uppfærðir (en hafðu í huga að það eru líka margar aðrar uppfærslur):</p><ul><li>Reiturinn <b>Innhreyfing</b> er stilltur á <i>Móttekið</i>.</li><li>Reiturinn <b>Efnisleg dagsetning</b> er uppfærður með dagsetningu bókunar.</li></ul> |
| Farmur sem notandinn bókaði innhreyfingarskjal afurða frá | Uppfærslur á hleðslunni fara eftir útgáfu sem er notuð og stillingu reitsins **Leyfa mörg innhreyfingarskjöl á farm**. Reglunum er lýst í töflunni sem birtist síðar í þessum kafla. |

Reiturinn **Leyfa mörg innhreyfingarskjöl á farm** gerir fyrirtækjum kleift að velja stefnu fyrir móttöku farms á innleið. Það fer eftir rekstrarstreymi þeirra, en fyrirtæki gætu valið að leyfa eða banna margar bókanir innhreyfingarskjala afurða fyrir sama farm. Við mælum með að flutningsstjórinn stilli reitinn **Leyfa mörg innhreyfingarskjöl á farm** að einu af eftirfarandi gildum:

- **Nei** - Veldu þetta gildi ef móttökustarfsmenn vöruhúss skrá alltaf allt pöntunarmagn sem kemur með hverri hleðslu innan tiltekins tímaramma. Ef eitthvað farmmagn er ekki skráð, gerir kerfið ráð fyrir að það hafi ekki komið eða ekki verið í farminum og ætti því ekki að teljast hluti af farminum. Bókuninnhreyfingarskjals afurða sem keyrð er úr farmi notar sömu forsendu. Til viðbótar við uppfærslu innhreyfingarskjals afurða á öllu skráðu magni (meginhlutverk þess) tilkynnir það farminn sem lokinn og lokað fyrir viðbótarvinnslu. Í þessu tilfelli er magn allra farmlínanna sjálfkrafa uppfært í skráð magn, öllum farmlínum án skráðs magns verður eytt og farmstaðan breytist í _Móttekið_.
- **Já** - Veldu þetta gildi ef móttökustarfsmaður vöruhúss þarf meiri tíma til að skrá allt magn á farminn sem barst, en á meðan verður þú að bóka innhreyfingarskjal afurða á magni sem þegar hefur verið skráð. Í þessu tilfelli mun flutningsstjórinn vilja halda farmi opnum jafnvel eftir að bókunarvinnsla innhreyfingarskjals afurða er keyrð, svo að hægt sé að skrá eftirstöðvamagn og uppfæra innhreyfingarskjal afurða stöðugt til höfuðbókar.
- **Kvaðning** - Veldu þetta gildi ef farmmóttökuhættir þínir eru blandaðir og ákvörðun er nauðsynleg í hvert skipti sem bókun innhreyfingarskjals afurða er keyrð.

Eftirfarandi tafla dregur saman áhrif af stillingunni **Leyfa mörg innhreyfingarskjöl á farm**.

| Leyfa mörg innhreyfingarskjöl á farm | Magn farms | Hleðslustaða | Nóta |
|---|---|---|---|
| Þegar þessi reitur er ekki til (útgáfur fyrir 10.0.10) | <p>Farmmagnið er stillt þannig að það jafngildir skráðu magni.</p><p>Ef farmmagnið er uppfært í 0 (núll), sem þýðir að engin skráning hefur verið gerð, er farmlínunni eytt.</p><p>Ef engar farmlínur eru í farminum er farminum eytt.</p> | _Móttekið_ | Ef margir farmar eru til staðar fyrir skráð magn pöntunarlínunnar er aðeins staða farmsins sem innhreyfinarskjali var bókað úr uppfærð í _Móttekið_. |
| Ekkert | <p>Farmmagnið er stillt þannig að það jafngildir skráðu magni sem er tengt við farmkennið.</p><p>Ef ekkert farmkenni er skráð fyrir birgðafærslu passar hegðunin við hegðun í útgáfum á undan 10.0.10.</p> | _Móttekið_ | |
| Já | Engar uppfærslur | _Móttekið_, ef heildarmagn farmmagns er jafnt eða meira en farmmagnið | |
| Já | Engar uppfærslur | _Sent_ eða _Í vinnslu_, ef heildarmagn farmmagns er minna en farmmagnið | |

Þegar reiturinn **Farmstaða** hefur verið stilltur á _Móttekið_ er ekki hægt að gera fleiri bókanir innhreyfingarskjala afurða fyrir þann farm. Samt sem áður getur starfskrafturinn skráð eftirstöðvar pöntunarinnar á móti mótteknum farmi við eftirfarandi skilyrði. (Fyrir frekari upplýsingar, sjá hlutann [Ofmóttaka farms](#load-over-receiving) fyrr í þessu efni.)

- Útgáfan af Supply Chain Management er eldri en útgáfa 10.0.11.
- Kveikt er á eiginleikanum _Ofmóttaka farmmagns_ og reiturinn **Farmlínumagn ofmóttöku** í valmyndaratriði fartækisins fyrir móttökuaðgerð farmvörunnar er stilltur á _Leyfa_.

Til að bóka innhreyfingarskjal afurða á viðbótar skráðu farmmagni á móti farmi sem hefur stöðuna _Móttekið_ verður notandinn að keyra bókunaraðgerðina úr tengdri innkaupapöntun.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Settu skráð magn af síðunni Innkaupapöntun

Til að bóka innhreyfingarskjal afurða á skráðu magni af síðunni **Innkaupapöntun** lýkur notandanum eftirfarandi verkum áður en viðkomandi velur aðgerðina **Innhreyfingarskjal afurða**:

- Stilltu reitinn **Magn** í kaflanum **Færibreytur** á flipanum **Stillingar** á _Skráð magn_.
- Í reitinn **Innhreyfingarskjal afurðar** slærðu inn þau númer innkaupapantana sem eru innifalin í bókuninni.

> [!NOTE]
> Línumagnið sem verður innifalið í bókunarumfanginu er samtals allt skráð magn fyrir pöntunarlínuna, óháð því hvort magnskráning var gerð á mörgum förmum, óháð álagi, úr farsíma eða af biðlaranum. Sama regla gildir þegar bókun innhreyfingarskjals afurða er keyrð úr farmi, ef það er gert þar sem reiturinn **Leyfa mörg innhreyfingarskjöl á farm** er annaðhvort er ekki tiltækur eða virkur.

Þegar notandinn velur **Í lagi** til að staðfesta bókun innhreyfingarskjals afurða gerir kerfið eftirfarandi lykiluppfærslur um viðeigandi eininga.

| Eining | Uppfærslur |
|---|---|
| Birgðafærsla á innkaupapöntuninni þar sem línumagn hefur verið innifalið í bókunarumfanginu | <p>Eftirfarandi reitir eru uppfærðir (en hafðu í huga að það eru líka margar aðrar uppfærslur):</p><ul><li>Reiturinn <b>Innhreyfing</b> er stilltur á <i>Móttekið</i>.</li><li>Reiturinn <b>Efnisleg dagsetning</b> er uppfærður með bókunaraðgerð innhreyfingarskjals afurða.</li></ul> |
| Sækja | Uppfærslur á förmum fara eftir því hvort reiturinn **Leyfa mörg innhreyfingarskjöl á farm** er tiltækur og virkur. Reglunum er lýst í næstu töflu. |

Eftirfarandi tafla dregur saman áhrif af stillingunni **Leyfa mörg innhreyfingarskjöl á farm**.

| Leyfa mörg innhreyfingarskjöl afurða fyrir hvern farm | Magn farms | Hleðslustaða | Nóta |
|---|---|---|---|
| Þegar þessi reitur er annaðhvort óvirkur eða ekki tiltækur (í útgáfum fyrir 10.0.10) | Engar uppfærslur | Engar uppfærslur eru gerðar. (Staðan er enn _Opið_, _Sent_ eða _Í vinnslu_ .) | Þar sem bókun á innhreyfingarskjali afurða var hafin úr innkaupapöntun hafa uppfærslurökin ekki upplýsingar um tengsl milli skráðs magns innan gildissviðs þess og farms sem skráningin var skráð á móti. Þess vegna getur hún ekki valið farm fyrir stöðuuppfærsluna. |
| Gert virkt | Engar uppfærslur | <p>Ein af eftirfarandi aðgerðum á sér stað:</p><ul><li>Stöðunni er breytt í <i>Móttekið</i> ef samtals móttekið og keypt magn af birgðafærslum innkaupapöntunar er meira en eða jafnt magni farmsins sem þeim tengist.</li><li>Staðan helst <i>Opið</i>, <i>Sent</i> eða <i>Í vinnslu</i> ef fyrri skilyrðin eru ekki uppfyllt fyrir allar línurnar í farminum.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Veldu viðeigandi bókunarvalkost fyrir innhreyfingarskjal afurða fyrir flutningaaðgerðir þínar

Eins og áður var lýst býður kerfið upp á tvo valkosti fyrir bókun á innhreyfingarskjali afurða. Hægt er að nálgast valkostina á eftirfarandi stöðum:

- Á síðunni **Farmur** eða af valmyndinni **Vöruhúsastjórnun \> Reglubundin verk** sem uppfærsluvinnsla
- Á síðunni **Innkaupapöntun** eða af valmyndinni **Innkaup og aðföng \> Innkaupapantanir \> Móttaka afurða** sem uppfærsluvinnsla

Fyrirtækjum sem nota álag til að áætlan og stjórna flutningum og meðhöndlun vöruhúsa á pöntunun á innleið er bent á að nota eftirfarandi aðgerðir sem eru hannaðar til að vinna með álag:

- **Móttaka farmvöru** aðgerðir í vöruhúsafartækjum þeirra,til að skrá komu magn vörunnar gegn álaginu
- **Bókun innhreyfingarskjals afurða** aðgerðir sem eru hafnar frá álagi til að uppfæra birgðahöfuðbókina

> [!NOTE]
> Hægt er að nota aðrar magnskráningar og bókunaraðgerðir innhreyfingarskjala afurða til að styðja samsvarandi rekstrarferli á innleið. Hins vegar, ef þú notar þær til skiptis með eða í staðinn fyrir sérstaka álagsáhersluaðgerðir gætir þú sett gagnanákvæmni farmskránna í hættu og þar með talið samfelldni stjórnunarflæðis álags.

## <a name="example-scenarios"></a>Dæmi um aðstæður

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Undirbúðu kerfið þitt til að keyra dæmi um aðstæður

Til að vinna í gegnum dæmi um aðstæður sem lýst er í þessum hluta verður þú fyrst að ganga úr skugga um að kveikt sé á öllum nauðsynlegum eiginleikum í kerfinu þínu. Nauðsynleg kynningargögn verða einnig að vera tiltæk í kerfinu.

#### <a name="turn-on-the-required-features"></a>Kveiktu á nauðsynlegum eiginleikum

Þessar aðstæður krefjast eiginleikans _Margar bókanir innhreyfingarskjala afurða á farm_ og forsendueiginleika hans. Stjórnendur geta kveikt á þessum eiginleikum með því að fylgja þessum skrefum.

1. Opnaðu vinnusvæðið **Eiginleikastjórnun**. (Nánari upplýsingar um hvernig á að finna og nota þetta vinnusvæði er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) .)

1. Kveiktu á eiginleikanum _Tengja birgðafærslu innkaupapöntunar við farm_, sem er skráður á eftirfarandi hátt:

    - **Eining:** _Vöruhúsakerfi_
    - **Heiti eiginleika:** _Tengja birgðafærslu innkaupapöntunar við farm_

1. Kveiktu á eiginleikanum _Margar bókanir innhreyfingarskjala afurða á farm_, sem er skráður á eftirfarandi hátt:

    - **Eining:** _Vöruhúsakerfi_
    - **Heiti eiginleika:** _Margar bókanir innhreyfingarskjala afurða á farm_

#### <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að vinna í gegnum þessar atburðarásir með því að nota tilgreind sýnishornagögn og -gildi verður þú að nota kerfi þar sem stöðluð kynningargagna eru sett upp. Þú verður einnig að velja lögaðilann **USMF** áður en þú byrjar.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Bættu við valmyndaratriði fyrir móttöku farmvara þegar fartæki er notað

Áður en starfsmaður vöruhúss getur notað fartæki til að skrá birgðir á innleið sem eru tengdar við álag verður þú að búa til valmyndaratriði fartækis í þeim tilgangi.

Í þessum hluta muntu búa til valmyndaratriði fartækis og bæta því við núverandi valmynd. Starfskraftur í vöruhúsi getur síðan valið valmyndaratriði í vöruhúsaforritinu.

1. Farðu í **Vöruhúsastjórnun \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis** og gakktu úr skugga um að valmynd fartækisins innihaldi valmyndaratriði sem hefur eftirfarandi stillingar:

    - **Máti:** _Vinna_
    - **Vinnusköpunarferli:** _Móttaka farmvöru_
    - **Mynda númeraplötu:** _Já_

    Þú getur haft allar aðrar stillingar sem sjálfgefin gildi.

    ![Stillingar valmyndaratriðis fartækis](media/inbound-mobile-menu-items.png "Stillingar valmyndaratriðis fartækis")

    Nánari upplýsingar um hvernig skuli setja upp valmyndaratriði fartækja, sjá [Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md).

2. Þegar þú hefur lokið uppsetningu á valmyndaratriðinu ferðu í **Vöruhúsastjórnun \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis** og bætir því við valmyndaskipulag fyrir fartækisin.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>Dæmi atburðarás 1: Skráðu farm þar sem sumar vörur vantar

Þessi atburðarás sýnir hvernig hægt er að skrá magn fyrir farm á innleið þar sem ekki er allt vænt magn til staðar. Hún sýnir síðan hvernig á að bóka innhreyfingarskjal afurða fyrir innkaupapöntunina.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Stofnaðu farm til að skipuleggja móttöku innkaupapöntunar

Í þessu ferli muntu stofna innkaupapöntun handvirkt og tengdan farm. Þú munt síðan uppfæra farminn til að líkja eftir því að það hafi verið sent af lánardrottninum (sem uppfærir farmstöðuna). Vöruhússkipuleggjendur geta síðan síað farma eftir **Farmstöðu** til að finna væntanlega farma á innleið.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Veljið **Nýtt**.
1. Í valmyndinni **Stofna innkaupapöntun** stillirðu reitinn **Lánardrottnalykill** á _1001_.
1. Veldu **Í lagi** til að loka svarglugganum og stofna innkaupapöntunina.
1. Nýja innkaupapöntunin er þegar með línu undir **Innkaupapöntunarlínur**. Stilltu eftirfarandi gildi fyrir þessa línu:

    - **Vörunúmer:** _A0001_
    - **Vöruhús:** _24_
    - **Magn:** _10_

1. Á aðgerðasvæðinu, í flipanum **Innkaup**, skal velja **Aðgerðir \> Staðfesta**. Pöntunarstaðan er núna _Staðfest_.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Aðgerðir \> Vinnusvæði hleðsluáætlunar**.
1. Á síðunni **Vinnusvæði hleðsluáætlunar**, í aðgerðarglugganum, á flipanum **Framboð og eftirspurn**, velurðu **Bæta við \> Í nýja hleðslu**.
1. Í valmyndinni **Úhlutun farmsniðmáts** stillirðu reitinn **Sniðmátskenni farms** á _20 'gámur_.
1. Veldu **Í lagi** til að loka svarglugganum og fara til baka á vinnusvæðið.
1. Í hlutanum **Farmar** velurðu **Farmkenni** til að opna nýstofnaðan farm.
1. Skoðaðu upplýsingar um farmhaus og -línu og taktu eftir eftirfarandi atriðum:

    - Á flýtiflipanum **Farmur** er reiturinn **Farmstaða** stilltur á _Opið_.
    - Í hlutanum **Farmlínur** er ein lína þar sem reiturinn **Magn** er stilltur á _10_ og reiturinn **Magn vinnusköpunar** er stilltur á _0_ (núll).

    ![Upplýsingar um hleðslu](media/inbound-load-details.png "Upplýsingar um hleðslu")

1. Í aðgerðaglugganum, á flipanum **Senda og móttaka**, velurðu **Staðfesta \> Sending á innleið**. Taktu eftir að **Farmstaða** hefur breyst í _Sent_.
1. Skrifaðu hjá þér gildið **Kenni farms**, svo að þú getir notað það í næsta ferli.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Skráð móttöku magns sem barst í farminum

Þegar farmurinn berst á móttökusvæði vöruhússins skráir móttökustarfsmaður farmmagn á fartæki.

1. Notaðu farsímann þinn til að skrá þig inn í vörhús 24. (Í stöðluðum kynningargögnum skráirðu þig inn með því að nota _24_ sem notandakenni og _1_ sem lykilorð.)
1. Veldu valmyndaratriðið _Móttaka farmvöru_ sem þú bjóst til fyrir þessa atburðarás.
1. Fylgdu leiðbeiningunum um færslu gagna á skjánum til að slá inn eftirfarandi gildi. (Röðin getur verið breytileg, allt eftir því hvaða fartæki eða hermi þú notar.)

    - **Farmur** - Sláðu inn kenni farms sem þú bjóst til í fyrra ferlinu.
    - **Vara** - Sláðu inn _A0001_ sem er varan sem er vænst fyrir þennan farm.
    - **Magn** - Sláðu inn _9_ sem raunverulegt magn sem er til staðar í farminum. Athugið að þetta magn er minna en áætlað magn.

1. Haltu áfram að fara í gegnum verkflæðið, láttu alla aðra reiti vera auða eða stilltu á sjálfgefin gildi, þar til tækið þitt upplýsir þig um að verkinu sé lokið.

Farmmóttökuverkinu er nú lokið og móttökustarfsmaður getur haldið áfram í næsta verkefni sitt. Samt sem áður munu móttökustarfsmenn vöruhúsa endurskoða farmskrána og geta séð að móttekið magn var minna en áætlað magn. Þeir munu síðan ljúka eftirfarandi ferli með því að nota vefþjóninn.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Finndu álagið sem þú hefur nýlega fengið á listanum. (Þú gætir þurft að velja gátreitinn **Sýning lokuð** til að fela farma á innleið sem hafa farmstöðuna _Sent_ .) Veldu síðan tengilinn í dálkinum **Kenni farms** til að opna farminn.
1. Í farmskránni skaltu taka eftir að gildið **Farmstaða** er áfram _Sent_, en gildið **Magn stofnaðrar vinnu** í farmlínunni hefur breyst í _9_.
1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Finndu kaupin sem þú hefur nýlega á listanum og veldu síðan hlekkinn í dálkinum **Innkaupapöntun** til að opna pöntunina.
\
1. Á flýtiflipanum **Innkaupapöntunarlínur** velurðu **Birgðir \> Skoðun \> Færslur**.
1. Skoðaðu upplýsingarnar um innkaupapöntunarfærslunar tvær. (Þú gætir þurft að sérsníða síðuna **Birgðafærslur** til að sjá reitinn **Kenni farms** í hnitanetinu.) Þú ættir að sjá tvær færslur:

    - Viðskiptin sem hafa innhreyfingarskjal í stöðunni _Skráð_ táknar skráningarmagnið _9_ sem var keyrt gegn ákveðnu álagi með því að nota fartækið. **Kenni farms** er tengt viðkomandi færslu.
    - Færslan sem er með innhreyfingu í stöðunni _Pantað_ táknar eftirstandandi óskráð magn pöntunarlínunnar upp á _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Bókaðu innhreyfingarskjal afurða á skráðu farmmagni gegn innkaupapöntunum

Í þessu ferli muntu bóka innhreyfingarskjal afurða á birgðirnar sem þú skráðir fyrir farm. Fyrir vikið bætast viðteknar birgðir og tengdur kostnaður við fjárhag fyrirtækisins.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Finndu álagið sem þú hefur fengið á listanum. (Þú gætir þurft að velja gátreitinn **Sýning lokuð** til að fela farma á innleið sem hafa farmstöðuna _Sent_ .) Veldu síðan tengilinn í dálkinum **Kenni farms** til að opna farminn.
1. Í aðgerðaglugganum, á flipanum **Senda og móttaka**, velurðu **Móttaka \> Innhreyfingarskjal**. Ef þú færð kvaðningu um að staðfesta aðgerðina velurðu **Já**.
1. Í svarglugganum **Bókun innhreyfingarskjals afurða**, á flýtiflipanum **Línur**, skaltu skoða hnitanetið. Þú ættir að sjá innkaupapöntunarlínuna sem magnið hefur verið skráð á gegn völdum farmi.

    > [!NOTE]
    > Í útgáfum þar sem eiginleikinn _Margar bókanir innhreyfingarskjala afurða á farm_ er ekki tiltækur eða er ekki virkur verður sjálfgefið magn sem er sýnt í hnitanetinu **Farmlínur** heildarmagnið sem hefur verið skráð yfir alla farma sem eru tengdir innkaupapöntunarlínunni.

1. Í flýtiflipanum **Yfirlit** skaltu skoða reitinn **Innhreyfingarskjal afurða** í hnitanetinu. Taktu eftir því að það er að stillt á númer sem inniheldur kenni valins farms.
1. Veldu **Í lagi** til að senda innhreyfingarskjal afurða og loka valmyndinni **Bókun innhreyfingarskjals afurða**.
1. Þú ert komin/n aftur í upplýsingar um farminn. Athugið eftirfarandi punkta:

    - Reiturinn **Farmstaða** er nú stilltur á _Móttekið_.
    - Á farmlínunni hefur gildið **Magn** fyrir farminn breyst úr _10_ í _9_ stk. til að passa við skráð magn, en gildið **Magn vinnusköpunar** helst sem _9_.

Ef innkaupateymið býst ekki við að lánardrottinn afhendi eftirstandandi pöntunarmagn 1, getur það lokað pöntuninni með því að uppfæra afhendingarafgang línunnar í _0_. Hins vegar, ef fljótlega kemur í ljós að varan sem vantar barst í upphafsfarminum geta starfsmenn vöruhússins framkvæmt eina af eftirfarandi aðgerðum:

- Skrá magnið á sama farm. Í þessu tilfelli verður reiturinn **Farmstaða** endurstilltur á _Sent_ og gildið **Magn vinnusköpunar** verður uppfært í _10_. Þetta val er aðeins í boði við eftirfarandi aðstæður:

    - Eiginleikinn _Ofmóttaka farmmagns_ er ekki til eða er ekki virkur.
    - Eiginleikinn _Ofmóttaka á farmmagni_ er tiltæk og virkjuð og reiturinn **Farmlínumagn yfirmóttöku** er stilltur á _Leyfa_.

- Bætið magninu við nýjan eða fyrirliggjandi farm og vinnið það á venjulegan hátt.
- Skráðu þig og/eða taktu á móti magninu á þann hátt sem felur ekki í sér meðhöndlun farms.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>Dæmi um atburðarás 2: Skráið magn sem berst á marga farma á innleið þar sem sumar vörur vantar

Í þessari atburðarás verður sendingu á innleið sem er tengd stakri innkaupapöntunarlínu skipt í tvennt. Til dæmis gæti innkaupapöntunarlínu verið skipt upp í marga farma vegna efnislegra farmskorða á þyngd og/eða rúmmál.

Þessi atburðarás sýnir einnig hvernig á að vinna úr mörgum bókunum innhreyfingarskjal afurða fyrir sama farm. Þú munt skrá magn sem berst í mörgum förmum á innleið, en magnið passar ekki við áætlað magn. Kostnaðaruppfærslurnar sem eiga sér stað í gegnum bókun innhreyfingarskjal afurða verða gerðar mörgum sinnum fyrir sama farm.

#### <a name="set-up-load-receiving-policies"></a>Setja upp innhreyfingarskjal afurða

Í þessari aðferð muntu gera virkja bókun margra innhreyfingarskjala afurða úr sama farmi.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Á flipanum **Farmar** stillirðu reitinn **Leyfa mörg innhreyfingarskjöl á farm** á _Já_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Stofnaðu tvo farma til að skipuleggja móttöku innkaupapöntunar

Í þessu ferli muntu stofna innkaupapöntun handvirkt og tvo farma. Þú munt síðan uppfæra hvern farm handvirkt til að líkja eftir því að það hafi verið sent af lánardrottninum (sem uppfærir farmstöðuna). Vöruhússkipuleggjendur geta síðan síað farma eftir **Farmstöðu** til að finna væntanlega farma á innleið.

Þú munt einnig læra hvernig á að stilla innkaupapöntunarlínuna þannig að þú getur fengið magn sem er 20 prósent meira en það magn sem er tilgreint fyrir línuna.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Veljið **Nýtt**.
1. Á flýtiflipanum **Lánardrottinn** stillirðu reitinn **Lánadrottinslykill** á _1001_ og veldu síðan **Í lagi**.
1. Nýja innkaupapöntunin þín er opnuð og inniheldur auða línu í hnitanetinu **Innkaupapöntunarlínur**. Stilltu eftirfarandi gildi fyrir þessa pöntunarlínu:

    - **Vörunúmer:** _A0001_
    - **Vöruhús:** _24_
    - **Magn:** _10_

1. Á flýtiflipanum **Línulýsing**, á flipanum **Afhending**, stillirðu reitinn **Ofafhending** á _20_.
1. Á aðgerðasvæðinu, í flipanum **Innkaup**, skal velja **Aðgerðir \> Staðfesta**. Pöntunarstaðan er núna _Staðfest_.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Aðgerðir \> Vinnusvæði hleðsluáætlunar**.
1. Á síðunni **Vinnusvæði hleðsluáætlunar**, í aðgerðarglugganum, á flipanum **Framboð og eftirspurn**, velurðu **Bæta við \> Í nýja hleðslu**.
1. Í valmyndinni **Úhlutun farmsniðmáts** stillirðu reitinn **Sniðmátskenni farms** á _20 'gámur_. Á flipanum **Upplýsingar** breytirðu gildinu **Magn** úr _10_ í _5_ til að bæta við hluta magns innkaupapöntunarlínunnar.
1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum.
1. Endurtaktu skref 8 til 10 til að stofna annan farm. Í þetta sinn ætti reiturinn **Magn** þegar að vera stilltur á _5_.
1. Á síðunni **Vinnusvæði hleðsluáætlunar**, í hnitanetinu **Farmar**, velurðu gildið **Kenni farms** fyrir fyrsta farminn sem þú bjóst til. Síðan **Farmupplýsingar** birtist og sýnir valið álag. Fylgið eftirfarandi skrefum:

    1. Í aðgerðaglugganum, á flipanum **Senda og móttaka**, velurðu **Staðfesta \> Sending á innleið**.
    1. Taktu eftir að gildið **Farmstaða** hefur breyst í _Sent_.
    1. Veldu lokunarhnappinn til að fara aftur á síðuna **Vinnusvæði hleðsluáætlunar**.

1. Endurtaktu fyrra skrefið fyrir seinni farminn sem þú bjóst til.
1. Gerðu athugasemd um **Kenni farms** gildin tvö sem birtast í hnitanetinu **Farmar**.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Skráðu hlutfallslega móttöku á magni sem barst í fyrsta farmi og bókaðu skráð farmmagn

Þegar farmar berast á móttökusvæði vöruhússins skráir móttökurstarfsmaður farmmagn á fartæki. Skráðar birgðir sem eru tengdar farmi eru síðan uppfærðar í fjárhag fyrirtækisins með því að bóka innhreyfingarskjali afurðar fyrir innkaupapöntun, byggð á farminum.

Þetta ferli sýnir hvernig móttökustarfsmaður skráir farmmagn í fartæki.

1. Notaðu farsímann þinn til að skrá þig inn í vörhús 24. (Í stöðluðum kynningargögnum skráirðu þig inn með því að nota _24_ sem notandakenni og _1_ sem lykilorð.)
1. Veldu valmyndaratriðið _Móttaka farmvöru_ sem þú bjóst til fyrir þessa atburðarás.
1. Fylgdu leiðbeiningunum um færslu gagna á skjánum til að slá inn eftirfarandi gildi. (Röðin getur verið breytileg, allt eftir því hvaða fartæki eða hermi þú notar.)

    - **Farmur** - Sláðu inn fyrsta kenni farms sem þú bjóst til í fyrra ferlinu.
    - **Vara** - Sláðu inn _A0001_ sem er varan sem er vænst fyrir þennan farm.
    - **Magn** - Sláðu inn _3_. Athugið að þetta magn er minna en áætlað magn. Í þessu tilfelli, ímyndaðu þér að þú sem móttökustarfsmaður hafir ekki tíma til að skrá allt magn fyrir þennan farm. Seinna í þessu ferli muntu skrá eftirstandandi hluti með því að endurtaka þetta skref og stilla reitinn **Magn** á _2_.

1. Haltu áfram að fara í gegnum verkflæðið, láttu alla aðra reiti vera auða eða stilltu á sjálfgefin gildi, þar til tækið þitt upplýsir þig um að verkinu sé lokið.
1. Í vefbiðlaranum ferðu í **Vöruhúsakerfi \> Farmar \> Allir farmar**.
1. Í listanum finnurðu farminn sem þú hefur nýlega fengið og velur gildið **Kenni farms** til að opna farminn. Taktu eftir að gildið **Farmstaða** er áfram _Sent_, en gildið **Magn stofnaðrar vinnu** í farmlínunni hefur breyst í _3_.
1. Í aðgerðaglugganum, á flipanum **Senda og móttaka**, velurðu **Móttaka \> Innhreyfingarskjal**. Ef þú færð kvaðningu um að staðfesta aðgerðina velurðu **Já**.
1. Í valmyndinni **Bókun innhreyfingaskjals** skoðarðu en breytir ekki gildunum sem eru sýnd og velur síðan **Í lagi**.
1. Þú ert komin/n aftur á síðuna **Farmupplýsingar** fyrir valin farm. Athugið eftirfarandi punkta:

    - Reiturinn **Farmstaða** helst stilltur á _Sent_.
    - Í farmlínunni helst gildið **Magn** fyrir farminn _5_ stk., sem er upphaflegt farmmagn og gildið **Magn vinnusköpunar** helst _3_.

1. Ljúktu skráningu á eftirstandandi magni á þessum farmi með því að endurtaka þetta ferli. Hins vegar skaltu í skrefi 3 stilla reitinn **Magn** á _2_.

Móttökuverkinu fyrir fyrsta farminn er nú lokið. Tvær færslubækur innhreyfingarskjala afurða hafa verið stofnaðar, ein fyrir hvora af uppfærslunum tveimur á færslubókum innhreyfingarskjala afurða sem þú keyrðir.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Skráðu móttöku magns sem barst í öðrum farmi og gerðu grein fyrir ofafhentu magni

Fyrir þessa atburðarás mun móttökustarfsmaður skrá magn á innleið sem er umfram það magn sem er í farminum. Ofmóttaka verður leyfð vegna þess að kerfið er sett upp til að leyfa ofafhendingu.

1. Notaðu farsímann þinn til að skrá þig inn í vörhús 24. (Í stöðluðum kynningargögnum skráirðu þig inn með því að nota _24_ sem notandakenni og _1_ sem lykilorð.)
1. Veldu valmyndaratriðið _Móttaka farmvöru_ sem þú bjóst til fyrir þessa atburðarás.
1. Fylgdu leiðbeiningunum um færslu gagna á skjánum til að slá inn eftirfarandi gildi. (Röðin getur verið breytileg, allt eftir því hvaða fartæki eða hermi þú notar.)

    - **Farmur** - Sláðu inn annað farmkenni sem þú bjóst til fyrr.
    - **Vara** - Sláðu inn _A0001_ sem er varan sem er vænst fyrir þennan farm.
    - **Magn** - Sláðu inn _7_, sem er eftirstandandi magn sem lánardrottinn hefur leyfi til að afhenda sem hluta af heildarinnkaupapöntunarmagni 12 (þar sem 10 er upphaflegt pöntunarmagn og 2 er leyfilegt magn ofafhendingar upp á 20 prósent). Mundu að 5 stk hafa þegar verið skráð gegn fyrsta farmi.

Annar farmurinn hefur nú verið uppfærður með magninu 7 og er hægt að fá uppfæra eftir innhreyfingarskjali afurða miðað við þetta magn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
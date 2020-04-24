---
title: Úrvinnsla á framleiðsluþyngd afurðar með vöruhúsakerfi
description: Þetta efnisatriði lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinna verður framkvæmd í vöruhúsinu.
author: perlynne
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 5a751b360b2da8f786dd7b8d139e1a0a44052894
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211975"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Úrvinnsla á framleiðsluþyngd afurðar með vöruhúsakerfi

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Útsetning eiginleika

Til að nota vöruhúsakerfi til að vinna úr framleiðsluþyngdum afurða þarftu að nota skilgreiningarlykil leyfis til að kveikja á virkninni. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**. Síðan í flipanum **Skilgreiningarlyklar** skal stækka **Viðskipti \> Vöruhúsakerfi og flutningsstjórnun** og velja gátreitinn fyrir **Framleiðsluþyngd fyrir vöruhús**.

> [!NOTE]
> Einnig verður að vera kveikt á skilgreiningarlyklunum **Vöruhúsakerfi og flutningsstjórnun** og **Vinnsludreifing \> framleiðsluþyngd**. Til að stilla stillingarlykla fyrir framleiðsluþyngd, verður þú einnig að kveikja á aðgerðinni með því að nota vinnusvæðið **Eiginleikastjórnun**. Aðalaðgerðin sem verður að vera kveikt á er **Úrvinnsla á framleiðsluþyngd afurðar með vöruhúsakerfi**. Tveir tengdir en valfrjálsir eiginleikar sem þú gætir viljað kveikja á eru **Birgðastöðubreytingar fyrir framleiðsluþyngdarafurðir** og **Nota fyrirliggjandi merki framleiðsluþyngdar þegar framleiðslupantanir eru tilkynntar sem lokið**.

Eftir að kveikt er á skilgreiningarlyklinum, þegar þú býrð til útgefna afurð, getur þú valið **Framleiðsluþyngd**. Þú getur einnig tengt útgefna afurð við geymsluvíddarflokk sem færibreytan **Nota ferli vöruhúsakerfis** er valin fyrir.

Áður en þú getur notað afurðina í Vöruhúsakerfi þarftu að gera nokkrar afurðamiðaðar grunnuppsetningar fyrir framleiðsluþyngd:

- Skilgreindu umreikning nafnþyngdar milli framleiðsluþyngdareiningu (kassi) og birgðaeiningar (kílógramm \[kg\]) sem hluta af skilgreiningu á umreikningi eininga.
- Skilgreindu lágmark og hámark fyrir vikmörk þyngdar sem hluta af uppsetningu framleiðsluþyngdareiningar.
- Setja upp einingarröðunarflokk þar sem framleiðsluþyngdareiningin er skilgreind sem minnsta birgðahaldseiningin (SKU).
- Setja upp reglu um meðhöndlun vöru með framleiðsluþyngd.

Nánari upplýsingar er að finna í [Uppsetning og viðhald á vörum fyrir framleiðsluþyngd](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Leiðréttingar á færslu

Vegna þess að þyngd birgða þegar þær koma inn í vöruhús getur verið frábrugðin þyngdinni þegar birgðir eru losaðar út úr vöruhúsinu, verður úrvinnsla á framleiðsluþyngd afurðar að leiðrétta birgðirnar.

> [!NOTE]
> Verkþáttur fartækis mun aðeins virkja færsluleiðréttingar ef aðferð þyngdarfráviks á útleið við meðhöndlunarstefnu framleiðsluþyngdar hlutar er **Leyfa þyngdarafbrigði**.

**Dæmi 1**

Við framleiðsluferlið **Bóka sem tilbúið** er þyngd númeraplötu á innleið sem inniheldur átta kassa af framleiðsluþyngdarafurð skráð sem 80,1 kg. Númeraplatan er síðan geymd á svæði fullunninnar vöru, og á meðan á geymslutíma stendur, tapast einhver þyngd út í umhverfið.

Síðar, sem hluti af tiltektarferli sölupöntunar, er þyngd sömu númeraplötunnar skráð sem 79,8 kg. Í kerfinu er þar af leiðandi þyngdarmunur sem hluti af efnislegri víddasamstæðu.

Í þessu tilfelli leiðréttir kerfið sjálfkrafa mismuninn með því að bóka færslu fyrir 0,3 kg sem vantar upp á.

**Dæmi 2**

Í skilgreiningu sinni er afurð sett upp til að þola lágmarksþyngd sem nemur 8 kg og hámarksþyngd sem nemur 12 kg fyrir framleiðsluþyngdareininguna **Kassi**.

Þú ert með tvo kassa af afurðinni og þeir eru með skráða þyngd 16 kg. Ef starfsmaður í vöruhúsi tínir og vigtar annan kassann og þyngdin er 9 kg, þá mun hinn kassinn sem er eftir fá þyngdina 7 kg. Hins vegar, vegna þess að 7 kg er undir lágmarksþyngdinni, gerir kerfið sjálfvirka leiðréttingu til að auka þyngd lagerbirgða um 1 kg.

Til að setja upp lyklana sem þessar leiðréttingar eru bókaðar á skal fara í **Kostnaðarstjórnun \> Uppsetning á reglum fjárhagssamþættingar \> Bókun**. Síðan í flipanum **Birgðir** skal skilgreina eftirfarandi lykla:

- Taplykill sökum þyngdar afurðar
- Hagnaðarlykill sökum þyngdar afurðar

## <a name="catch-weight-item-handling-policy"></a>Stefna um meðhöndlun vöru með framleiðsluþyngd

Reglan um meðhöndlun á vöru með framleiðsluþyngd skilgreinir tvö grunnflæði vöruhúsakerfis fyrir vörurnar: þegar þyngd vörunnar er sótt, og hvernig hún er sótt.

Þú getur skilgreint hvenær þyngd er sótt fyrir úrvinnslu á sölu- og flutningspöntunum. Þyngd er hægt að sækja í öðru hvoru af eftirfarandi ferlum:

- **Tiltekt** - Þyngd er sótt við upphaflegu vinnulínu tiltektar fyrir vinnupöntun.
- **Pökkun** - Þyngd er sótt við handvirka pökkun. (Þú verður að senda vörurnar á pökkunarstöð.)

Ef raunveruleg þyngd er sótt á pökkunarstöðinni við pökkunarferli gáms, eru starfsmenn í vöruhúsi ekki beðnir um að sækja þyngdina við tiltekt. Í staðinn er meðalþyngd efnislegra birgða notuð sem þyngd tíndra birgða sem fara á pökkunarsvæðið. Þetta hugtak á einnig við um framleiðsluþyngdaratriði sem eru rakin með merkjum. Fyrir atriði sem eru rakin með merkjum ákvarða þessar breytur hvenær merkið er tekið. Merkið er hægt að taka annaðhvort við tínslu með því að nota fartækið eða við handvirka pökkun.

> [!NOTE]
> Vegna þess að valkosturinn **Pökkun** veldur því að birgðir eru uppfærðar með meðaltali tiltekinnar þyngdar gæti það kallað fram misræmi sem gæti valdið leiðréttingu á hagnaði/tapi framleiðsluþyngdar og/eða mun á lagerbirgðaþyngd og merki framleiðsluþyngdar.

Fyrir innri vöruhúsakerfisferli, eins og talning og leiðréttingar geturðu skilgreint hvort sækja eigi þyngdina eða ekki. Ef hún er ekki sótt er nafnþyngdin notuð. Aðrir valkostir gera þér kleift að ná þyngd á hverja einingu framleiðsluþyngdar og fyrir talningarmagn.

Þú getur einnig skilgreint hvernig þyngdin er sótt. Í einum af tveimur helstu flæðunum er fylgst með merkjum fyrir framleiðsluþyngd og þau notuð til að sækja þyngdina. Í hinu flæðinu er ekki fylgst með merkjum fyrir framleiðsluþyngd.

- **Já** - Varan notar merki fyrir framleiðsluþyngd. Hvert merkjanúmer táknar eina framleiðsluþyngdareiningu (kassi) og þyngd og aðrar upplýsingar eru tengdar við merkið. Fyrir ferli á útleið er þyngdin sem tengist merkinu notuð.
- **Nei** - Varan notar ekki merki fyrir framleiðsluþyngd. Vigtunarferlin fyrir inn- og útleið byggjast á raunverulegri þyngd sem er sótt í hverju ferli fyrir sig.

Ferlið til að fylgjast með merkjum fyrir framleiðsluþyngd er hægt að nota fyrir vörur þar sem þyngdin breytist ekki á geymslutímanum. Þyngdin verður aðeins sótt meðan á vöruhúsaferli á innleið stendur yfir. Á meðan vöruhúsaferli á útleið stendur yfir verður framleiðsluþyngd bara skönnuð og þyngdirnar sem tengjast merkjunum verða notuð við færsluferli á útleið.

Önnur mikilvæg færibreyta sem tengist vinnslu framleiðsluþyngdarmerka er **Rakningaraðferð merkjavíddar framleiðsluþyngdar**. Hægt er að rekja merki annaðhvort að hluta eða rekja það að fullu. Ef merki er rakið að hluta, rekur það afurðarvíddir, rakningarvíddir og stöðu birgða. Ef merki er rakið að fullu, rekur það afurðarvíddir, rakningarvíddir og **allar** geymsluvíddir.

Að auki, þegar atriði er rakið með merkum er til breytan **Aðferð við að sækja merkimiða á útleið**. Þú getur stillt þessa færibreytu þannig að alltaf verði beðið um merkið við útleiðarviðskipti úr fartækinu. Einnig er hægt að stilla færibreytuna þannig að aðeins sé beðið um merki þegar þess er krafist. Til dæmis eru fimm framleiðsluþyngdarmerki í birgðum á tilteknum leyfismerki og þú hefur gefið til kynna að þú viljir velja öll fimm merkin af leyfismerkinu. Í þessu tilfelli, ef breytan **Aðferð við að sækja merkimiða á útleið** er stillt á **Biðja aðeins um merki þegar þörf er á** eru fimm merkin sjálfkrafa valin. Þú þarft ekki að skanna hvert merki. Ef færibreytan er stillt á **Biðja alltaf um merki** verður þú að skanna hvert merki, jafnvel þó að öll fimm merkin séu valin.

> [!NOTE]
> Að jafnaði eru merkin tekin og uppfærð aðeins úr valmyndaratriðunum í fartækinu. Engu að síður eru nokkrar aðstæður þar sem merkimiðar eru teknar annars staðar (til dæmis frá handvirku pökkunarstöðinni). Almennt ætti þó að nota valmyndaratriðin í fartækinu fyri alla verkþætti vöruhúss ef merkingar eru notaðar.

### <a name="how-to-capture-catch-weight"></a>Hvernig á að sækja framleiðsluþyngd

**Þegar rakning á merki framleiðsluþyngdar er notað**, verður alltaf að stofna merki fyrir hverja framleiðsluþyngdareiningu sem tekið er á móti, og öll merki verða alltaf að tengjast þyngd.

Til dæmis er **Kassi** framleiðsluþyngdareiningin og þú tekur á móti vörubretti með átta kössum. Í þessu tilfelli verður að búa til átta einkvæm merki fyrir framleiðsluþyngd og tengja verður þyngd við hvert merki. Það fer eftir framleiðsluþyngd afurðar á innleið, annaðhvort er hægt að sækja þyngd fyrir alla átta kassana og svo er meðalþyngd úthlutað á hvern kassa, eða hægt er að sækja þyngd fyrir hvern kassa fyrir sig.
Þegar þú notar eiginleikann **Nota fyrirliggjandi merki framleiðsluþyngdar þegar framleiðslupantanir eru tilkynntar sem lokið** þar sem ferlið er virkjað í valmyndaratriði í fartæki, verða birgðir uppfærðar miðað við fyrirliggjandi upplýsingar um merki framleiðsluþyngdar. Fyrir vikið biður Vörugeymsluforritið ekki um að safna gögnum um merki framleiðsluþyngdar sem hluta af framleiðsluskýrslu sem fullgerðri aðgerð.

**Þegar rakning á merki fyrir framleiðsluþyngd er ekki notuð** er hægt að sækja þyngdina fyrir hverja víddasamstæðu (til dæmis fyrir hverja númeraplötu og rakningarvídd). Að öðrum kosti er hægt að sækja þyngdina sem byggist á samanlögðu stigi, svo sem fimm númeraplötur (vörubretti).

Fyrir aðferði við að ná þyngd á útleið gerir valkosturinn **Á hverja framleiðsluþyngdareiningu** þér kleift að tilgreina að vigtunin eigi að fara fram fyrir hverja framleiðsluþyngdareiningu (til dæmis í hvern reit). Valkostuirnn **Fyrir hverja tiltektareiningu** gerir þér kleift að tilgreina að þyngdin skuli tekin út frá magni sem verður valið (til dæmis þrír reitir). Athugaðu að fyrir tiltektarferli framleiðslulínu og innri hreyfingarferli verður meðalþyngd notuð ef valkosturinn **Ekki sótt** er notaður.

Margar aðferðir við þyngdartöku eru skilgreindar í meðhöndlunarstefnu framleiðsluþyngdaratriðis. Hver færibreyta þyngdartökuaðferðar er notuð af ýmsum færslum. Eftirfarandi tafla dregur saman hvaða breytur eru notaðar af hvaða færslum.

| Aðferð                                     | Færsla                                |
|--------------------------------------------|--------------------------------------------|
| Aðferð til að sækja þyngd á útleið           | Tiltekt sölu, Flutningstiltekt            |
| Aðferð til að sækja þyngd framleiðslutiltektar | Framleiðslutiltekt, framleiðslunotkun |
| Aðferð til að sækja hreyfingu á þyngd           | Hreyfing                                   |
| Hvenær á að sækja leiðréttingu á þyngd       | Leiðréttingar, Talning                      |
| Aðferð til að sækja talningu þyngdar           | Talning                                   |
| Aðferð til að sækja flutningsþyngd vöruhúss | Flutningur í vöruhús                         |

Til að hindra tiltektarferli vöruhúsakerfis frá því að sækja þyngdir sem leiða til leiðréttinga á hagnaði/tapi framleiðsluþyngdar, er hægt að nota aðferð þyngdarfráviks á útleið. Aðferð þyngdarfráviks á útleið gildir við eftirfarandi ferla fartækis: sölutiltekt, flutningstiltekt, framleiðslutiltekt, hreyfingar, talningu og vöruhúsaflutninga. Þú getur notað valkostinn **Takmarka frávik í þyngd** ef þyngd framleiðsluþyngdaratriðis sveiflast ekki við geymslu í vöruhúsinu og ef ekki er þörf á leiðréttingum á hagnaði/tapi framleiðsluþyngdar. Þú getur aðeins notað valkostinn **Leyfa frávik í þyngd** ef þyngdin getur sveiflast og ef þörf er á leiðréttingu á hagnaði/tapi þegar sveiflur í þyngdar eru skráðar.

## <a name="unsupported-scenarios"></a>Óstuddar aðstæður

Ekki öll verkflæði styðja úrvinnslu á afurð í framleiðsluþyngd með vöruhúsakerfi. Eftirfarandi takmarkanir gilda nú. Þær eiga við um alla hluti framleiðsluþyngdar, óháð því hvort þeir eru merktir.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Grunnstilling á framleiðsluþyngd fyrir vöruhúsakerfisferla

- Ein úrvinnsluformúla er studd fyrir afurðir í framleiðsluþyngd (ekki uppskrift).
- Ekki er hægt að tengja afurðir í framleiðsluþyngd við rakningarvíddarflokk með því að nota eigandavídd.
- Afurðir í framleiðsluþyngd er ekki hægt að nota sem þjónustur.
- Hægt er að nota afurðir í framleiðsluþyngd sem „vörur á lager“ eingöngu sem hluti af vörulíkanaflokki.
- Ekki er hægt að nota afurðir í framleiðsluþyngd saman með virkni til að rekja „Virkt í söluferli“.
- Ekki er hægt að nota afurðir í framleiðsluþyngd saman með virkni til að sækja raðnúmer. Þess vegna er ekki hægt að flytja afurðir frá „auðu“ til raðnúmers sem hluta af tiltektar-/pökkunarferlinu.
- Ekki er hægt að nota afurðir í framleiðsluþyngd saman með virkni til að skrá raðnúmer fyrir notkun.
- Ekki er hægt að nota afurðir í framleiðsluþyngd sem eru með afbrigði virkt saman með virkni til að umbreyta mælieiningu afbrigðis.
- Ekki er hægt að merkja afurðir í framleiðsluþyngd sem „afurðasett“ Commerce.
- Aðeins er hægt að nota afurðir í framleiðsluþyngd með einingaröðunarflokki sem er með afgreiðslueiningar fyrir framleiðsluþyngd og sem er með framleiðsluþyngdareininguna sem lægstu röðina.
- Fyrir afurðir í framleiðsluþyngd er hægt að umbreyta birgðaeiningunni í framleiðsluþyngdareiningu eingöngu ef umbreytingin býr til nafnmagn sem er meira en 1.
- Uppsetning strikamerkja fyrir afurðir í framleiðsluþyngd styður ekki uppsetningu breytilegrar þyngdar.

### <a name="order-processing"></a>Vinnsla pantana

- Stofnun á tilkynningu um sendingu (ASN/pakkaskipan) styður ekki þyngdarupplýsingar.
- Vinna verður með pöntunarmagnið samkvæmt framleiðsluþyngdareiningunni.

### <a name="inbound-warehouse-processing"></a>Vöruhúsavinnsla á innleið

- Móttaka á númeraplötum krefst þess að þyngdum sé úthlutað við skráningu, því að þyngdarupplýsingar eru ekki studdar sem hluti af tilkynningu um sendingu. Þegar merkjaferli fyrir framleiðsluþyngd er notuð verður merkjanúmerið að vera úthlutað handvirkt fyrir hverja þyngdareiningu. Móttaka á blönduðum númeraplötum er ekki studd fyrir afurðir í framleiðsluþyngd.
- Vinna gæðaprófunar á innleið er ekki studd fyrir framleiðsluþyngd afurða. Ef hún er stillt verður gæðaeftirlitsvinnu sleppt.

### <a name="inventory-and-warehouse-operations"></a>Aðgerðir birgða og vöruhúss

- Handvirk stofnun á biðgeymslupöntunum er ekki studd fyrir afurðir í framleiðsluþyngd.
- Handvirkur flutningur birgða sem tengist opnu verki er ekki studdur fyrir afurðir í framleiðsluþyngd.
- Hleðsla númeraplötu til að frumstilla vöruhúsabirgðir er ekki studd fyrir afurðir í framleiðsluþyngd.
- Jöfnunarferli virkra efna í uppskrift er ekki stutt fyrir afurðir í framleiðsluþyngd.
- Meðhöndlun á neikvæðri birgðastöðu er ekki studd fyrir afurðir í framleiðsluþyngd.
- Ekki er hægt að nota birgðamerkingu fyrir afurðir í framleiðsluþyngd.

### <a name="outbound-warehouse-processing"></a>Vöruhúsavinnsla á útleið

- Virkni fyrir klasatiltekt er ekki studd fyrir afurðir í framleiðsluþyngd.
- Tiltektar- og pökkunarvinnsla vöruhúss er ekki studd fyrir afurðir í framleiðsluþyngd.
- Fyrir afurðir í framleiðsluþyngd er hægt að keyra vinnu sjálfkrafa sem er skilgreind í vinnusniðmáti.
- Fyrir afurðir í framleiðsluþyngd styður kerfið ekki handvirka vinnslu pökkunarstöðva þar sem tiltektarvinna pökkunargáms er stofnuð eftir að gámum er lokað.
- Virkni fyrir skönnun á stykki fyrir stykki er ekki studd fyrir afurðir í framleiðsluþyngd.

### <a name="production-processing"></a>Framleiðsluvinnsla

- Fyrir aflaþyngdarafurðir eru aðeins runupantanir fyrir formúluafurðir studdar.
- Kanban-virkni er ekki studd fyrir afurðir í framleiðsluþyngd.
- Fyrir afurðir í framleiðsluþyngd er ekki hægt að skrá raðnúmer á undan notkun.
- Virknin til að bakfæra númeraplötur er ekki studd úr framleiðslu fyrir afurðir í framleiðsluþyngd.
- Fyrir afurðir í framleiðsluþyngd er hægt að skrá skýrslugerð sem lokið eftir raðnúmeri.

### <a name="transportation-management-processing"></a>Vinnsla flutningsstjórnunar

- Vinnsla á vinnusvæði hleðsluáætlunar er ekki studd fyrir afurðir í framleiðsluþyngd.
- Flutningsbeiðnilínur eru ekki studdar fyrir afurðir í framleiðsluþyngd.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Aðrar takmarkanir og hegðun við vinnslu í vöruhúsakerfi á afurðum með framleiðsluþyngd

- Í tiltektarferlum, þegar notandinn er ekki beðinn um að bera kennsl á rakningarvíddir, miðast þyngdarúthlutunin við meðalþyngd. Þessi hegðun kemur fram þegar til dæmis samsetning af rakningarvíddum er notuð í sömu staðsetningunni og, eftir að notandi vinnur úr tiltekt, er aðeins eitt rakningarvíddargildi eftir í staðsetningunni.
- Þegar birgðir eru fráteknar fyrir afurð í framleiðsluþyngd sem er stillt fyrir vöruhúsakerfisferli, er frátektin gerð með hliðsjón af lágmarksþyngd sem er skilgreind, jafnvel þó að þetta magn sé síðasta afgreiðslumagnið á lager. Þessi hegðun er frábrugðin hegðun fyrir vörur sem eru ekki stilltar fyrir vöruhúsakerfisferli. Það er ein undantekning frá þessari takmörkun. Fyrir framleiðslutiltekt, þegar síðasta meðhöndlunarmagn afurðar sem er stjórnað með raðnúmeri er valið, er raunveruleg þyngd notuð.
- Ferli sem nota þyngdina sem hluta af útreikningi á afköstum (bylgjuþröskuldar, hámarkshlé vinnu, hámark af gámum, afkastagetu staðsetningar o.s.frv.) nota ekki raunþyngd birgðanna. Þess í stað eru ferlarnir byggðir á efnislegri meðhöndlunarþyngd sem er skilgreind fyrir afurðina.
- Almennt er Commerce-virknin ekki studd fyrir afurðir í framleiðsluþyngd.
- Fyrir afurðir framleiðsluþyngdar er ekki hægt að uppfæra birgðastöðu úr **Breyting á stöðu vöruhúsa**.

### <a name="catch-weight-tags"></a>Merki framleiðsluþyngdar

Merki framleiðsluþyngdar getur verið stofnað með því að nota ferli vöruhúsaforrits, stofnað handvirkt í skjámyndinni, eða stofnað með því að nota gagnaeiningarferli. Ef merki framleiðsluþyngdar er tengt við upprunaskjalslínu á innleið, t.d. innkaupapöntunarlínu, verður merkið skráð. Ef línan er notuð til vinnslu á útleið verður merkið uppfært eins og það er sent.

Auk þeirra takmarkana sem nú eiga við um afurðir framleiðsluþyngdar, hafa merktar afurðir framleiðsluþyngdar aðrar takmarkanir sem nú gilda.

- Allar handvirkar uppfærslur á birgðum (það er að segja uppfærslur sem ekki eru gerðar með fartæki) verða að innihalda samsvarandi handvirkar uppfærslur á tengdum merkjum framleiðsluþyngdar vegna þess að þessar uppfærslur eru ekki gerðar sjálfkrafa. Til dæmis munu handvirkar leiðréttingarbækur uppfæra birgðir en ekki tengd merki framleiðsluþyngdar.
- Þú verður að uppfæra merki framleiðsluþyngdar handvirkt til að endurspegla áfyllingarhreyfingar. Þetta er vegna þess að kerfið getur ekki náð þyngdum við vinnslu áfyllingarvinnu og skráir því meðalþyngd í staðinn.
- Móttaka á blandaðri númeraplötu er ekki studd eins og er fyrir merktar framleiðsluþyngdarvörur.
- Með vinnslu á móttöku söluskilapöntunar er hægt að skrá merki framleiðsluþyngdar. Ferlið staðfestir þó ekki að skilamerkið sé sama merki og upphaflega var sent fyrir sölupöntun.
- Valmyndaratriðið fyrir fartæki sem er með verkþáttakóðann **Skrá efnisnotkun** styður ekki eins og stendur við skráningu merkja framleiðsluþyngdar.
- Þó að talningarferlar séu studdir fyrir merkt atriði framleiðsluþyngdar eru þeir takmarkaðir. Til dæmis er hægt að nota valmöguleika farstækjanna til að telja merkt atriði framleiðsluþyngdar og meðalþyngd er notuð. Hins vegar eru merki framleiðsluþyngdar ekki uppfærð sjálfkrafa með talningarfærslunni. Eftir að talningarfærslunni er lokið verður að uppfæra merki framleiðsluþyngdar handvirkt svo þau endurspegli birgðir. Ef hlutir sem ekki voru upphaflega á staðsetningu eru taldir inn á þá staðsetningu er nafnþyngd notuð.
- Samstæða númeraplatna styður ekki hluti með merkta framleiðsluþyngd eins og stendur.
- Bakfærð vinnuvirkni er ekki studd fyrir hluti framleiðsluþyngdar sem eru rakin með númerum.

> [!NOTE]
> Undanfarandi upplýsingar um merki framleiðsluþyngdar eru aðeins gildar ef afurð framleiðsluþyngdar er með rakningaraðferð merkjavíddar framleiðsluþyngdar sem er rakin að fullu (það er, ef færibreytan **Rakningaraðferð merkjavíddar framleiðsluþyngdar** í meðhöndlunarstefnu hlutar framleiðsluþyngdar er stillt á **Afurðarvíddir, rakningarvíddir og allar geymsluvíddir**). Ef hluti framleiðsluþyngdar er aðeins rakinn með merki að hluta (það er, ef færibreyta **Rakningaraðferð merkjavíddar framleiðsluþyngdar** á meðhöndlunarstefnu vöru framleiðsluþyngdar er stillt á **Afurðavíddir, rakningarvíddir og birgðastaða**), gilda frekari takmarkanir. Vegna þess að skyggni tapast milli merkisins og birgða í þessu tilfelli eru nokkrar viðbótaraðstæður ekki studdar.

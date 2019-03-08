---
title: Úrvinnsla á framleiðsluþyngd afurðar með vöruhúsakerfi
description: Þetta efnisatriði lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinna verður framkvæmd í vöruhúsinu.
author: perlynne
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 5161860e3b1c5b0ae795d109159268be085ec5af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "334060"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Úrvinnsla á framleiðsluþyngd afurðar með vöruhúsakerfi
[!include [preview banner](../../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

**Útsetning eiginleika**

Til að nota vöruhúsakerfi til að vinna úr framleiðsluþyngdum afurða þarftu að nota skilgreiningarlykil leyfis til að kveikja á virkninni. (Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**. Síðan í flipanum **Skilgreiningarlyklar** skal stækka **Viðskipti \> Vöruhúsakerfi og flutningsstjórnun** og velja gátreitinn fyrir **Framleiðsluþyngd fyrir vöruhús**).

> [!NOTE]
> Bæði skilgreiningarlykillinn **Vöruhúsakerfi og flutningsstjórnun** og skilgreiningarlyklarnir **Vinnsludreifing framleiðsluþyngdar** verður einnig að vera kveikt á.

Eftir að kveikt er á skilgreiningarlyklinum, þegar þú býrð til útgefna afurð, getur þú valið **Framleiðsluþyngd**. Þú getur einnig tengt útgefna afurð við geymsluvíddarflokk sem færibreytan **Nota ferli vöruhúsakerfis** er valin fyrir.

Áður en þú getur notað afurðina í Vöruhúsakerfi þarftu að gera nokkrar afurðamiðaðar grunnuppsetningar fyrir framleiðsluþyngd:

- Skilgreindu umreikning nafnþyngdar milli framleiðsluþyngdareiningu (kassi) og birgðaeiningar (kílógramm \[kg\]) sem hluta af skilgreiningu á umreikningi eininga.
- Skilgreindu lágmark og hámark fyrir vikmörk þyngdar sem hluta af uppsetningu framleiðsluþyngdareiningar.
- Setja upp einingarröðunarflokk þar sem framleiðsluþyngdareiningin er skilgreind sem minnsta birgðahaldseiningin (SKU).
- Setja upp reglu um meðhöndlun vöru með framleiðsluþyngd.

Nánari upplýsingar er að finna í [Uppsetning og viðhald á vörum fyrir framleiðsluþyngd](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Leiðréttingar á færslu

Vegna þess að þyngd birgða þegar þær koma inn í vöruhús getur verið frábrugðin þyngdinni þegar birgðir eru losaðar út úr vöruhúsinu, verður úrvinnsla á framleiðsluþyngd afurðar að leiðrétta birgðirnar.

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

Ef raunveruleg þyngd er sótt á pökkunarstöðinni við pökkunarferli gáms, verða starfsmenn í vöruhúsi ekki beðnir um að sækja þyngdina við tiltekt. Í staðinn verður meðalþyngd efnislegra birgða notuð sem þyngd tíndra birgða sem fara á pökkunarsvæðið.

Fyrir innri vöruhúsakerfisferli, eins og talning og leiðréttingar, er mögulegt að skilgreina hvort sækja eigi þyngdina eða ekki. Ef hún verður ekki sótt verður nafnþyngdin notuð.

Þú getur einnig skilgreint hvernig þyngdin er sótt. Í einum af tveimur helstu flæðunum er fylgst með merkjum fyrir framleiðsluþyngd og þau notuð til að sækja þyngdina. Í hinu flæðinu er ekki fylgst með merkjum fyrir framleiðsluþyngd.

- **Já** - Varan notar merki fyrir framleiðsluþyngd. Hvert merkjanúmer táknar eina framleiðsluþyngdareiningu (kassi) og þyngd og aðrar upplýsingar eru tengdar við merkið. Fyrir ferli á útleið er þyngdin sem tengist merkinu notuð.
- **Nei** - Varan notar ekki merki fyrir framleiðsluþyngd. Vigtunarferlin fyrir inn- og útleið byggjast á raunverulegri þyngd sem er sótt í hverju ferli fyrir sig.

Ferlið til að fylgjast með merkjum fyrir framleiðsluþyngd er hægt að nota fyrir vörur þar sem þyngdin breytist ekki á geymslutímanum. Þyngdin verður aðeins sótt meðan á vöruhúsaferli á innleið stendur yfir. Á meðan vöruhúsaferli á útleið stendur yfir verður framleiðsluþyngd bara skönnuð og þyngdirnar sem tengjast merkjunum verða notuð við færsluferli á útleið.

### <a name="how-to-capture-catch-weight"></a>Hvernig á að sækja framleiðsluþyngd

Þegar rakning á merki framleiðsluþyngdar er notað, verður alltaf að stofna merki fyrir hverja framleiðsluþyngdareiningu sem tekið er á móti, og öll merki verða alltaf að tengjast þyngd.

Til dæmis er **Kassi** framleiðsluþyngdareiningin og þú tekur á móti vörubretti með átta kössum. Í þessu tilfelli verður að búa til átta einkvæm merki fyrir framleiðsluþyngd og tengja verður þyngd við hvert merki. Það fer eftir framleiðsluþyngd afurðar á innleið, annaðhvort er hægt að sækja þyngd fyrir alla átta kassana og svo er meðalþyngd úthlutað á hvern kassa, eða hægt er að sækja þyngd fyrir hvern kassa fyrir sig.

Þegar rakning á merki fyrir framleiðsluþyngd er ekki notuð er hægt að sækja þyngdina fyrir hverja víddasamstæðu (til dæmis fyrir hverja númeraplötu og rakningarvídd). Að öðrum kosti er hægt að sækja þyngdina sem byggist á samanlögðu stigi, svo sem fimm númeraplötur (vörubretti).

Fyrir aðferðir til að sækja þyngd á útleið er hægt að skilgreina hvort vigtun er gerð fyrir hverja framleiðsluþyngdareiningu (það er fyrir hvern kassa) eða hvort þyngdin sé tekin miðað við magnið sem verður tínt (t.d. þrír kassar). Athugaðu að fyrir tiltektarferli framleiðslulínu verður meðalþyngd notuð ef valkosturinn **Ekki sótt** er notaður.

## <a name="supported-scenarios"></a>Studdar aðstæður

Ekki öll verkflæði styðja úrvinnslu á afurð í framleiðsluþyngd með vöruhúsakerfi. Eftirfarandi takmarkanir gilda nú.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Grunnstilling á framleiðsluþyngd fyrir vöruhúsakerfisferla

- Fyrir afurðir í framleiðsluþyngd er ekki hægt að breyta geymsluvíddarflokknum fyrir vörur (þannig að hægt sé að nota vöruhúsakerfisferlana fyrir þær).
- Ein úrvinnsluformúla er studd fyrir afurðir í framleiðsluþyngd (ekki uppskrift).
- Ekki er hægt að tengja afurðir í framleiðsluþyngd við rakningarvíddarflokk með því að nota eigandavídd.
- Afurðir í framleiðsluþyngd er ekki hægt að nota sem þjónustur.
- Hægt er að nota afurðir í framleiðsluþyngd sem „vörur á lager“ eingöngu sem hluti af vörulíkanaflokki.
- Ekki er hægt að nota afurðir í framleiðsluþyngd saman með virkni til að rekja „Virkt í söluferli“.
- Ekki er hægt að nota afurðir í framleiðsluþyngd saman með virkni til að sækja raðnúmer. Þess vegna er ekki hægt að flytja afurðir frá „auðu“ til raðnúmers sem hluta af tiltektar-/pökkunarferlinu.
- Ekki er hægt að nota afurðir í framleiðsluþyngd saman með virkni til að skrá raðnúmer fyrir notkun.
- Ekki er hægt að nota afurðir í framleiðsluþyngd sem eru með afbrigði virkt saman með virkni til að umbreyta mælieiningu afbrigðis.
- Ekki er hægt að merkja afurðir í framleiðsluþyngd sem „afurðasett“ smásölu.
- Aðeins er hægt að nota afurðir í framleiðsluþyngd með einingaröðunarflokki sem er með afgreiðslueiningar fyrir framleiðsluþyngd og sem er með framleiðsluþyngdareininguna sem lægstu röðina.
- Fyrir afurðir í framleiðsluþyngd er hægt að umbreyta birgðaeiningunni í framleiðsluþyngdareiningu eingöngu ef umbreytingin býr til nafnmagn sem er meira en 1.
- Uppsetning strikamerkja fyrir afurðir í framleiðsluþyngd styður ekki uppsetningu breytilegrar þyngdar.
 
### <a name="order-processing"></a>Vinnsla pantana

- Vinnsla samstæðusölupöntunar er ekki studd.
- Stofnun á tilkynningu um sendingu (ASN/pakkaskipan) styður ekki þyngdarupplýsingar.
- Vinna verður með pöntunarmagnið samkvæmt framleiðsluþyngdareiningunni.
 
### <a name="inbound-warehouse-processing"></a>Vöruhúsavinnsla á innleið

- Móttaka á númeraplötum krefst þess að þyngdum sé úthlutað við skráningu, því að þyngdarupplýsingar eru ekki studdar sem hluti af tilkynningu um sendingu. Þegar merkjaferli fyrir framleiðsluþyngd er notuð verður merkjanúmerið að vera úthlutað handvirkt fyrir hverja þyngdareiningu. Móttaka á blönduðum númeraplötum er ekki studd fyrir afurðir í framleiðsluþyngd.
- Móttaka blandaðra númeraplata er ekki studd fyrir afurðir með framleiðsluþyngd.
 
### <a name="inventory-and-warehouse-operations"></a>Aðgerðir birgða og vöruhúss

- Handvirk stofnun á biðgeymslupöntunum er ekki studd fyrir afurðir í framleiðsluþyngd.
- Handvirkur flutningur birgða sem tengist verki er ekki studdur fyrir afurðir í framleiðsluþyngd.
- Samstæðumyndun á númeraplötum er ekki studd fyrir afurðir í framleiðsluþyngd.
- Breytingar á birgðastöðu vöruhúss sem hluti af reglubundnu verki eru ekki studdar fyrir afurðir í framleiðsluþyngd.
- Breytingar á birgðastöðu sem eru skilgreindar af fyrirspurn eru ekki studdar fyrir afurðir í framleiðsluþyngd. (Breytingar á birgðastöðu gæðapöntunar eru ekki heldur studdar.)
- Ekki er hægt að breyta birgðastöðu fyrir afurðir í framleiðsluþyngd á síðunni **Á lager eftir staðsetningu**.
- Ekki er hægt að breyta birgðastöðunni fyrir afurðir í framleiðsluþyngd sem hluti af hreyfingarverki vöruhúsaforrits.
- Hleðsla númeraplötu til að frumstilla vöruhúsabirgðir er ekki studd fyrir afurðir í framleiðsluþyngd.
- Jöfnunarferli virkra efna í uppskrift er ekki stutt fyrir afurðir í framleiðsluþyngd.
- Meðhöndlun á neikvæðri birgðastöðu er ekki studd fyrir afurðir í framleiðsluþyngd.
- Ekki er hægt að nota birgðamerkingu fyrir afurðir í framleiðsluþyngd.
 
### <a name="outbound-warehouse-processing"></a>Vöruhúsavinnsla á útleið

- Virkni fyrir klasatiltekt er ekki studd fyrir afurðir í framleiðsluþyngd.
- Tiltektar- og pökkunarvinnsla vöruhúss er ekki studd fyrir afurðir í framleiðsluþyngd.
- Ekki er hægt að ljúka vinnu fyrir afurðir í framleiðsluþyngd á síðunni **Vinna**.
- Fyrir afurðir í framleiðsluþyngd er hægt að keyra vinnu sjálfkrafa sem er skilgreind í vinnusniðmáti.
- Virknin til að bakfæra vinnu er ekki studd fyrir afurðir í framleiðsluþyngd.
- Fyrir afurðir í framleiðsluþyngd, handvirk vinnsla pökkunarstöðvar þar sem vinna er stofnuð eftir að gámar eru lokaðir er ekki studd.
- Virkni fyrir skönnun á stykki fyrir stykki er ekki studd fyrir afurðir í framleiðsluþyngd.
 
### <a name="production-processing"></a>Framleiðsluvinnsla

- Fyrir aflaþyngdarafurðir eru aðeins runupantanir fyrir formúluafurðir studdar.
- Kanban-virkni er ekki studd fyrir afurðir í framleiðsluþyngd.
- Fyrir afurðir í framleiðsluþyngd er ekki hægt að skrá raðnúmer á undan notkun.
- Virknin til að bakfæra númeraplötur er ekki studd fyrir afurðir í framleiðsluþyngd.
- Fyrir afurðir í framleiðsluþyngd er hægt að skrá skýrslugerð sem lokið eftir raðnúmeri.

### <a name="transportation-management-processing"></a>Vinnsla flutningsstjórnunar

- Vinnsla á vinnusvæði hleðsluáætlunar er ekki studd fyrir afurðir í framleiðsluþyngd.
- Flutningsbeiðnilínur eru ekki studdar fyrir afurðir í framleiðsluþyngd.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Aðrar takmarkanir og hegðun við vinnslu í vöruhúsakerfi á afurðum með framleiðsluþyngd

- Þegar merki framleiðsluþyngdar eru sóttar sem hluti af vinnslu vöruhúsaforrits getur notandinn ekki hætt í verkflæðinu.
- Í tiltektarferlum, þegar notandinn er ekki beðinn um að bera kennsl á rakningarvíddir, miðast þyngdarúthlutunin við meðalþyngd. Þessi hegðun kemur fram þegar til dæmis samsetning af rakningarvíddum er notuð í sömu staðsetningunni og, eftir að notandi vinnur úr tiltekt, er aðeins eitt rakningarvíddargildi eftir í staðsetningunni.
- Þegar birgðir eru fráteknar fyrir afurð í framleiðsluþyngd sem er stillt fyrir vöruhúsakerfisferli, er frátektin gerð með hliðsjón af lágmarksþyngd sem er skilgreind, jafnvel þó að þetta magn sé síðasta afgreiðslumagnið á lager. Þessi hegðun er frábrugðin hegðun fyrir vörur sem eru ekki stilltar fyrir vöruhúsakerfisferli.
- Ferli sem nota þyngdina sem hluta af útreikningi á afköstum (bylgjuþröskuldar, hámarkshlé vinnu, hámark af gámum, afkastagetu staðsetningar o.s.frv.) nota ekki raunþyngd birgðanna. Þess í stað eru ferlarnir byggðir á efnislegri meðhöndlunarþyngd sem er skilgreind fyrir afurðina.
- Almennt er smásöluvirknin ekki studd fyrir afurðir í framleiðsluþyngd.
 
### <a name="catch-weight-tags"></a>Merki framleiðsluþyngdar

Virkni fyrir merki framleiðsluþyngdar er aðeins studd eins og er sem hluti af eftirfarandi aðstæðum:

- Við vinnslu á innkaupapöntunum sem vöruhúsaforritið tekur á móti.
- Við vinnslu á móttöku á farmi í gegnum vöruhúsaforrit.
- Fyrir móttöku á númeraplötu sem tengist farmi innkaupapöntunar er krafist þyngdarúthlutunar í móttökuferlinu. Hins vegar, fyrir móttöku flutningspöntunar, er þyngdin úr sendingargögnum fyrir flutningspöntunina notuð.
- Fyrir móttöku á vöru og línu flutningspöntunar sem kemur frá vöruhúsi sem er ekki með vöruhúsakerfisferli.
- Vinnslan fyrir móttöku á söluskilapöntun getur skráð merki framleiðsluþyngdar, en vinnslan verður ekki sannprófuð ef merkin eru sömu merkin sem voru upphaflega send fyrir tiltekna sölupöntunarlínu.
- Við vinnslu á birgðastöðubreytingu með því að nota vöruhúsaforritið.
- Þegar vöruhúsaflutningur er gerður með því að nota vöruhúsaforritið.
- Við vinnslu leiðréttingar á inn- og útleið í gegnum vöruhúsaforritið.
- Þegar unnið er úr tiltektarvinnu fyrir sölu- og flutningspantanir. (Athugaðu að ekki er hægt að skrá merki framleiðsluþyngdar fyrir tiltekt á íhlutum framleiðslu.)
- Þegar tínt magn er minnkað í farmlínum, óháð því hvort gámar eru notaðir.
- Þegar afurðir eru pakkaðar í gáma á pökkunarstöð.
- Þegar gámar eru enduropnaðir.
- Þegar formúluafurðir eru skráðar sem búnar með því að nota vöruhúsaforritið.
- Þegar unnið er úr flutningsförmum með því að nota vöruhúsaforritið.

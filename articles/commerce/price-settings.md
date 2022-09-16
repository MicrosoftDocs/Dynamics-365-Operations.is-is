---
title: Verðstillingar
description: Þessi grein lýsir hinum ýmsu stillingum fyrir verðlagningu og afsláttarstjórnun í Microsoft Dynamics 365 Commerce höfuðstöðvar.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 79130e0ef285d6bd5e544f2d6a6368c0393fa7fa
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474043"
---
# <a name="pricing-settings"></a>Verðstillingar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir hinum ýmsu stillingum fyrir verðlagningu og afsláttarstjórnun í Microsoft Dynamics 365 Commerce höfuðstöðvar. Þessar stillingar gera fyrirtækjum kleift að skilgreina verðlagshegðun í viðskiptalausn sinni til að mæta sérstökum viðskiptaþörfum.

## <a name="company-level-pricing-settings"></a>Verðstillingar á fyrirtækisstigi

Flestar verðstillingar eru á fyrirtækisstigi og er að finna á **Viðskiptabreytur \> Verð og afslættir** í höfuðstöðvum verslunar.

### <a name="best-price-and-compound-concurrency-control-model"></a>Stýrilíkan fyrir besta verð og samvinnslu samsetningar

The **Besta verð og samsett samhliða stjórnunarlíkan** stilling ákvarðar hvernig verðlagningarvélin vinnur úr mörgum afslætti inn **besta verðið** eða **efnasamband** samhliða ham. 

Ef færibreytan er stillt á **Besta verðið og samsett innan forgangs, aldrei blandað þvert á forgangsröðun**, allt **efnasamband** afslættir sem hafa sama verðlagningarforgang eru samsettir. Samsett niðurstaða keppir síðan við hvaða **besta verðið** afslættir sem hafa sama verðforgang, besta verðið er notað og allir afslættir sem hafa lægri verðforgang eru hunsaðir.

Ef færibreytan er stillt á **Besta verðið aðeins innan forgangs, alltaf samsett þvert á forgangsröðun**, allt **efnasamband** Afslættir eru meðhöndlaðir sem **besta verðið** afslætti. Innan verðlagsforgangs vinnur aðeins einn afsláttur. Ef sá eini afsláttur er a **besta verðið** eða **efnasamband** afsláttur, hann er samsettur með öllu til viðbótar **besta verðið** eða **efnasamband** afslætti sem hafa lægri verðlagningu.

### <a name="discount-compound-behavior"></a>Hegðun afsláttarsamsetningar

The **Afsláttur samsett hegðun** stilling ákvarðar hvernig verðlagningarvélin reiknar út marga samsetta afslætti.

Ef færibreytan er stillt á **Samsett**, einn afsláttur er lagður ofan á annan með uppsöfnuðum hætti. Ef það er stillt á **Samsett á upprunalegu verði**, allir afslættir eru meðhöndlaðir óháð hver öðrum og beitt á sama upprunalega verðinu.

Til dæmis, þú vilt blanda saman 10 prósent afslætti og 20 prósent afslætti fyrir vöru sem hefur upphaflegt verð $100. Ef þú stillir **Afsláttur samsett hegðun** breytu til **Samsett**, lokaverðið verður $72 ($100&times; 90%&times; 80%). Ef þú stillir það á **Samsett á upprunalegu verði**, lokaverðið verður $70 ($100 – $10 – $20).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Gerðu samkeppni á milli einkaviðmiðunar og annarra reglubundinna afslátta

Ef **Gerðu samkeppni á milli einkaviðmiðunar og annarra reglubundinna afslátta** breytu er stillt á **Já**, verðlagningarvélin lætur einkaafslátt keppa við einkaafslátt sem ekki er viðmiðunarmörk. Forgangur verðlagningar gildir enn. Hegðun hjá **besta verðið** og **efnasamband** viðmiðunarafsláttur er óbreyttur. Með öðrum orðum, þeir keppa ekki við afslætti sem ekki eru viðmiðunarmörk.

### <a name="manual-line-discount-and-system-discount"></a>Handvirkur línuafsláttur og kerfisafsláttur

The **Handvirkur línuafsláttur og kerfisafsláttur** stilling ákvarðar hvernig verðlagningarvélin notar handvirkan línuafslátt og kerfisafslátt á sömu línu. Hægt er að bæta handvirka línuafsláttinum ofan á kerfisafsláttinn, eða hann getur komið í stað kerfisafsláttar. Þegar handvirkur línuafsláttur og kerfisafsláttur eru sameinaðar, virðir útreikningsrökfræðin **Afsláttur samsett hegðun** stilling. Handvirkur heildarafsláttur sem gildir fyrir alla pöntunina virðir ekki þá stillingu.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Halda atriðum á sömu sölulínu fyrir sléttun afsláttarverðs

Stundum er ekki hægt að deila upphæð magnafsláttar jafnt með uppfylltu magni (til dæmis ef afsláttarupphæðin er $10 af fyrir þrjár keyptar einingar). Í þessum tilvikum er **Haltu hlutum á sömu sölulínu til að námundun afsláttarverðs** stilling ákvarðar hvernig verðlagningarvélin á við og dreifir afsláttarupphæðinni. Ef færibreytan er stillt á **Já**, afsláttarupphæðin er notuð í heild og er ekki skipt. Ef það er stillt á **Nei**, er afsláttarupphæðinni deilt yfir uppfyllt magn og námundað. Til dæmis er afsláttarupphæð $10 off fyrir þrjár einingar skipt í $3.33 off fyrir eina einingu, $3.33 off fyrir aðra einingu og $3.34 off fyrir þriðju einingu.

### <a name="apply-discounts-to-key-in-price-products"></a>Notaðu afslætti til að slá inn verðvörur

The **Notaðu afslætti til að slá inn verðvörur** stilling ákvarðar hvort hægt sé að nota afslætti ásamt „innkeyrsluverði“ sem eru færð inn í sölustað (POS). The **Sláðu inn verð** stilling í vörustillingunni ákvarðar hvort og hvernig vara styður innkeyrsluverð.

### <a name="apply-discounts-to-price-overrides"></a>Gefa afslátt á verðhnekkingu

The **Notaðu afslætti á verðhækkun** stilling ákvarðar hvort hægt sé að nota afslætti ásamt verðhækkunum.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Dreifðu afslætti fyrir ódýrustu afslætti

Fyrir blanda afslætti sem nota „ódýrasta“ útreikningsgerðina, er **Dreifðu afslætti fyrir ódýrustu afslætti** stilling ákvarðar hvort verðlagningarvélin dreifir afsláttinum yfir línur.

Ef færibreytan er stillt á **Nei**, afslátturinn gildir aðeins á ódýrustu línurnar. Til dæmis, fyrir „kauptu 2 fáðu 1 ókeypis“ afslætti í bland og samsvörun, verður ódýrasta hluturinn ókeypis og hinir tveir hlutirnir verða áfram á fullu verði. Í þessu tilviki mun viðskiptavinur sem skilar báðum vörunum á fullu verði samt fá þriðju vöruna ókeypis. Þessi atburðarás gæti valdið tjóni fyrir söluaðilann.

Ef færibreytan er stillt á **Já**, verðlagningarvélin dreifir afsláttinum á allar viðeigandi línur. Þessi stilling getur hjálpað til við að draga úr tapi á ávöxtun.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Reikna verð og afslætti með mörgum línum handvirkt

The **Reiknaðu marglínuverð og afslætti handvirkt** stilling stjórnar því hvort verðlagningarvélin notar seinkað verð og afsláttarútreikning fyrir POS forritið og rás símaversins. Ef færibreytan er stillt á **Já**, reiknar verðlagningarvélin ekki samstundis út fjöllínuafslátt (svo sem magnafslátt, þröskuldaafslátt og blöndunarafslátt) þegar sölupöntun er búin til eða henni breytt í POS forritinu eða rás símaversins.

> [!NOTE]
> Í Commerce útgáfu 10.0.30 og eldri, **Reiknaðu marglínuverð og afslætti handvirkt** stilling stjórnar aðeins rás símaversins. Sérstakt **Reiknaðu marga vöruafslátt handvirkt** stilling í virknisniðinu stjórnar hegðun verðútreiknings í POS forritinu. Í Commerce útgáfu 10.0.31 eru þessar tvær stillingar sameinaðar í eina stillingu á fyrirtækisstigi.

### <a name="retention-period-in-days"></a>Varðveislutími í dögum

The **Varðveislutími í dögum** stilling gefur til kynna hversu mörgum dögum eftir fyrningardagsetningu (ef fyrningardagsetning er stillt) eða óvirka dagsetningu (ef fyrningardagsetning er ekki tilgreind) ætti að eyða afslátt kerfisbundið. Ef færibreytan er stillt á **0** (núll), engin sjálfvirk eyðing á sér stað.

> [!NOTE]
> Í Commerce útgáfu 10.0.30 og eldri er þessi stilling nefnd **Fjöldi daga sem útrunninn afsláttur ætti að vera eytt eftir**.

### <a name="coupon-bar-code"></a>Strikamerki afsláttarmiða

The **Strikamerki afsláttarmiða** stilling ákvarðar hvaða tiltekna strikamerki er notað til að búa til afsláttarmiða strikamerki. Notendur geta valið einn af fyrirfram skilgreindum strikamerkjum sem eru stilltir á **Strikamerki uppsetning** síðu. Fyrir frekari upplýsingar um strikamerki og strikamerkisgrímur, sjá [Settu upp strikamerki](set-up-bar-codes.md) og [Settu upp strikamerkisgrímur](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Afsláttarmiðakóða verður að nota handvirkt til að skila færslum

The **Afsláttarmiðakóða verður að nota handvirkt til að skila færslum** stillingin á aðeins við um skilafærslur sem engin sölukvittun er veitt fyrir. Stilltu færibreytuna á **Nei** ef afsláttarmiðakóðar ættu sjálfkrafa að vera notaðir við viðskiptin. Stilltu það á **Já** ef afsláttarmiðakóða þarf að bæta handvirkt við færsluna.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Nota uppsetningu sölusamninga fyrir fyrirtækið

Fyrir pantanir milli fyrirtækja (B2B), ef **Notaðu sölusamninga sem settir eru upp fyrir fyrirtækið** breytu er stillt á **Já**, notar verðlagningarvélin sölusamninga sem eru skilgreindir fyrir fyrirtækið í stigveldi viðskiptavina til að ákvarða samningsbundið verð. Ef færibreytan er stillt á **Nei**, eða ef stigveldi viðskiptavina er ekki skilgreint, leitar verðlagningarvélin að sölusamningum sem eru skilgreindir fyrir notandann til að ákvarða samningsbundið verð. Fyrir frekari upplýsingar um stigveldi viðskiptavina fyrir B2B rafræn viðskipti, sjá [Stjórna B2B viðskiptafélögum með því að nota stigveldi viðskiptavina](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Verðstillingar á rásarstigi

Eftirfarandi stillingar gera fyrirtækjum kleift að stjórna verðlagshegðun í tilteknum sölurásum.

### <a name="enable-order-price-control"></a>Virkja verðstýringu pöntunar

The **Virkja pöntunarverðstýringu** breytu er staðsett á **Almennt** Flýtiflipi á **Uppsetning símavera** síðu. Stillingin ákvarðar hvort verðlagningarvélin framfylgir takmörkun á verðhækkunaraðgerðum í símaveri. Það virkar í tengslum við **Leyfa verðleiðréttingu** stilling á vörustigi.

Ef slökkt er á verðstýringu pöntunar getur hvaða símaver sem er notandi gert verðbreytingar á sölulínum í símaveri rás, óháð því hvort samsvarandi vörur leyfa verðleiðréttingu.

Ef kveikt er á verðstýringu pöntunar eru aðeins vörur þar sem **Leyfa verðleiðréttingu** breytu er stillt á **Já** gera ráð fyrir verðhækkunum í sölupöntunum símavera og þarf að gefa upp ástæðukóða á samsvarandi sölulínum. Notandi símaver getur aðeins breytt söluverði upp að **Kostnaðarálagningarprósenta** gildi sem er skilgreint á **Verslun og verslun \> Rásaruppsetning \> Uppsetning símavera \> Hneka heimildir**. Ef verðhækkun fer yfir það hlutfall verður notandinn að senda inn beiðni sem er síðan unnin í gegnum fyrirfram skilgreint viðskiptaflæði til yfirferðar og samþykkis. Fyrir frekari upplýsingar um Commerce verkflæði, sjá [Yfirlit yfir verkflæðiskerfi](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Verðstillingar á vörustigi

Eftirfarandi stillingar framfylgja verðlagningarreglum á vörustigi og er að finna á fyrirtæki **Vörustillingar** síðu.

### <a name="allow-price-adjust"></a>Leyfa verðleiðréttingar

Ef **Leyfa verðleiðréttingu** breytu er stillt á **Já**, er hægt að beita verðhnekki á vöruna í sölupöntunum símavera.

### <a name="key-in-price"></a>Slá inn verð

The **Sláðu inn verð** stilling ákvarðar hvort innkeyrsluverð sé skylt þegar vöru er bætt við sölufærslu í POS. Það skilgreinir einnig samsvarandi takmarkanir á verðgildi.

### <a name="zero-price-valid"></a>Núllverð leyfilegt

The **Núll verð í gildi** stilling ákvarðar hvort fyrirframskilgreint, kerfisreiknað eða handvirkt leiðrétt söluverð fyrir vöru geti verið 0 (núll). Stilltu færibreytuna á **Já** ef núllverð er leyfilegt. Þessa stillingu er einnig hægt að tilgreina á flokkastigi úr vörustigveldi Commerce.

### <a name="prevent-all-discounts"></a>Koma í veg fyrir alla afslætti

Með því að stilla **Komið í veg fyrir alla afslætti** breytu til **Já**, þú kemur í veg fyrir að allar tegundir afslætti (þar á meðal handvirkir afslættir) séu notaðir á vöru. Þessa stillingu er einnig hægt að tilgreina á flokkastigi úr vörustigveldi Commerce.

> [!NOTE]
> Þessi stilling takmarkar ekki aðgerðina til að hnekkja verði, vegna þess að sú aðgerð setur verðið og er ekki meðhöndluð sem afsláttur.

### <a name="prevent-manual-discounts"></a>Koma í veg fyrir handvirka afslætti

Með því að stilla **Komið í veg fyrir handvirkan afslátt** breytu til **Já**, þú kemur í veg fyrir að handvirkur línu- eða færsluafsláttur sé notaður á vöru. Enn er hægt að nota alla aðra afslætti. Þessa stillingu er einnig hægt að tilgreina á flokkastigi úr vörustigveldi Commerce.

> [!NOTE]
> Þessi stilling takmarkar ekki aðgerðina til að hnekkja verði, vegna þess að sú aðgerð setur verðið og er ekki meðhöndluð sem afsláttur.

### <a name="prevent-retail-discounts"></a>Loka á smásöluafslætti

Ef **Komið í veg fyrir smásöluafslátt** breytu er stillt á **Já**, **·**, **·**, **·**, **saman** og **sendingarkostnaður** Ekki er hægt að nota afslátt á vöru. Enn er hægt að beita öllum öðrum afslætti (þar á meðal handvirkum afslætti).

### <a name="prevent-tender-based-discounts"></a>Loka á afslætti í útboðum

Ef **Koma í veg fyrir útboðsbundna afslætti** breytu er stillt á **Já**, a **útboðsmiðað** Ekki er hægt að nota afslátt á vöru. Enn er hægt að beita öllum öðrum afslætti (þar á meðal handvirkum afslætti).

Söluaðilar velja oft að útiloka sumar vörur, eins og nýjar vörur eða eftirspurnar vörur, frá vörubundnum afslætti (svo sem einföldum afslætti og magnafslætti). Hins vegar gætu þeir samt viljað beita tilboðsbundnum afslætti ef viðskiptavinur greiðir með því að nota valið tilboð. Til að ná þessum árangri geta smásalar stillt á **Komið í veg fyrir alla afslætti** og **Koma í veg fyrir útboðsbundna afslætti** breytur til **Nei**, og **Komið í veg fyrir smásöluafslátt** og **Komið í veg fyrir handvirkan afslátt** breytur til **Já**.

## <a name="deprecated-or-removed-settings"></a>Úreltar eða fjarlægðar stillingar

Eftirfarandi verðstillingar hafa verið fjarlægðar eða fyrirhugað er að fjarlægja þær úr Dynamics 365 Commerce.

| Stilling | Ástæða afskriftar eða fjarlægingar | Staða afskriftar eða fjarlægingar |
|---------|-----------------------------------|-------------------------------|
| Meðhöndlun afslátta sem skarast | Við gáfum upp þessa stillingu í viðskiptabreytum til að stjórna því hvernig verðlagningarvélin leitar að og ákvarðar bestu afsláttarsamsetninguna til að nota. The **Besti afslátturinn** valkostur þvingar í gegnum allar mögulegar afsláttarsamsetningar við verðútreikning. The **Besti árangur** valmöguleiki er bjartsýni valkostur sem notar heuristic reiknirit og jaðargildisröðunaraðferð til að forgangsraða, meta og ákvarða bestu samsetninguna tímanlega. The **Jafnvægi útreikningur** valmöguleiki í kóðagrunni virkar á sama hátt og **Besti árangur**. Því er þetta í raun tvískiptur valkostur. Til að hjálpa til við að bæta árangur hefur verðlagningarvélin verið uppfærð þannig að hún notar eingöngu **Besti árangur** sem staðalvalkostur. Þess vegna á þessi stilling ekki lengur við. | Úrelt í útgáfu 10.0.21 og verður fjarlægt í október 2022. |
| Leyfa verðbreytingum til að hækka vöruverð | Við settum upp þessa stillingu til að stjórna því hvort verðleiðréttingaraðgerðin geti hækkað vöruverð. Ef slökkt er á færibreytunni geta fyrirtæki notað verðleiðréttingaraðgerðina aðeins til að stilla einingarverð vöru þannig að það sé lægra en grunnverð og söluverð viðskiptasamnings. Við úreltum þessa stillingu vegna þess að verðleiðréttingaraðgerðin hefur verið uppfærð þannig að hún styður tvíhliða aðlögun (hækka eða lækka) úr kassanum. | Úrelt í útgáfunni 10.0.30 og verður fjarlægt í október 2023. |
| Virkja verðskýrslu fyrir smásöluverslun | Við útveguðum þessa stillingu til að stjórna því hvort **Verðskýrsla** aðgerð er tiltæk til notkunar á stillingasíðu verslunarinnar. Við úreltum þessa stillingu vegna þess að stillingarsíða verslunarinnar hefur verið uppfærð þannig að hún veitir alltaf **Verðskýrsla** sem staðlað fall. | Úrelt í útgáfu 10.0.31 og verður fjarlægt í október 2023. |
| Notaðu dagsetninguna í dag til að reikna út verð | The Dynamics 365 Supply Chain Management verðlagningarvél styður verðútreikning sem byggir á umbeðnum sendingardegi eða umbeðnum móttökudagsetningu ásamt dagsetningu dagsins í dag. Verðlagsvélin Commerce styður aðeins verðútreikning sem er byggður á dagsetningu í dag. Fyrir viðskiptavini sem nota bæði birgðakeðjustjórnun og viðskiptamöguleika, gáfum við þessa stillingu og mæltum með því að viðskiptavinir stilltu hana alltaf á **Já**, svo að verðlagsvélarnar tvær geti unnið saman. Við úreltum þessa stillingu vegna þess að hún breytir ekki útreikningshegðuninni í grundvallaratriðum og er því óþarfi. | Úrelt í útgáfu 10.0.31 og verður fjarlægt í október 2023. |
| Hámarksverð | Við gáfum upp þessa stillingu í virknisniðinu til að stjórna því hvort aðeins sé hægt að selja vörur sem eru með söluverð sem er undir tilgreindu hámarksverði í gegnum POS í tilteknum verslunum. Við úreltum þessa stillingu vegna lítillar eiginleikanotkunar. | Úrelt í útgáfu 10.0.31 og verður fjarlægt í október 2023. |
| Gefa afslátt á einingarverð | Þessari stillingu var ætlað að stýra því hvort verð og afslættir eru námundaðir á einingarverðsstigi eða sölulínustigi við verðútreikning. Við úreltum það vegna þess að það er hvergi neytt í núverandi kóðagrunni. | Úrelt í útgáfu 10.0.31 og verður fjarlægt í október 2023. |
| Reikna handvirkt afslátt af mörgum vörum | Við gáfum upp þessa stillingu til að stjórna því hvort verðlagningarvélin noti seinkaðan verðútreikning fyrir rás smásöluverslunar. Ef færibreytan er stillt á **Já**, reiknar verðlagningarvélin ekki samstundis út marglínuafslátt (svo sem magnafslátt, þröskuldaafslátt og blöndunarafslátt) þegar sölupöntun er búin til eða henni breytt í POS forritinu. Við ákváðum að sameina þessa stillingu með svipaðri stillingu í Commerce breytum til að gera allsherjarstýringu. | Úrelt í útgáfu 10.0.31 og verður fjarlægt í október 2023. |

Fyrir heildarlista yfir fjarlæga eða úrelta eiginleika í Dynamics 365 Commerce, sjá [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]

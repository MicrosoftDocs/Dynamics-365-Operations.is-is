---
title: Sjálfvirk uppgjör fjárhagsbóka
description: Þessi grein veitir upplýsingar um sjálfvirka fjárhagsuppgjörsferlið.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9707761"
---
# <a name="automate-ledger-settlements"></a>Sjálfvirk uppgjör fjárhagsbóka

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics 365 Fjármál útgáfa 10.0.31, the **Sjálfvirka uppgjörsferli fjárhagsbókhalds** eiginleiki er fáanlegur í **Eiginleikastjórnun**  vinnurými. Þú getur virkjað **Sjálfvirka uppgjörsferli fjárhagsbókhalds** eiginleiki aðeins ef **Meðvitund milli uppgjörs fjárhags og ársloka** eiginleiki hefur verið virkjaður.

Fjárhagsuppgjör er ferlið við að passa saman debet- og kreditfærslur í aðalbókinni. Fyrirtæki sem framkvæma fjárhagsuppgjörsaðgerðir á endurtekinni áætlun geta nú gert ferlið sjálfvirkt. Meðan á sjálfvirku fjárhagsuppgjörsferlinu stendur er aðeins hægt að passa debetfærslu og kreditfærslu sjálfkrafa ef upphæðir þeirra í bókhaldsgjaldmiðli eru jafnar.Til dæmis, debetupphæð $1.00 er hægt að passa sjálfkrafa við kreditupphæð $1.00. Hins vegar er ekki hægt að samræma debetgildi $1.00 sjálfkrafa við tvær inneignir, sem hver um sig er metin á $0.50. Hlutasamsvörun fjárhæða fjárhagsfærslu er ekki studd.

Sjálfvirkni fjárhagsuppgjörs skilgreinir eftirfarandi upplýsingar:

- Þegar fjárhagsuppgjör eru keyrð
- Hvaða viðmið eru notuð til að passa við skuldfærslur og inneignir sem hægt er að gera sjálfkrafa upp
- Í hvaða röð eru unnar upplýsingar um fjárhagsuppgjör

## <a name="define-the-occurrence-of-ledger-settlements"></a>Skilgreina tilvik fjárhagsuppgjöra

Sjálfvirkni fjárhagsuppgjörs notar sjálfvirkniramma ferlisins. Mismunandi viðskiptaferli nota þennan ramma til að skilgreina endurtekningu á völdu ferli. Fyrir fjárhagsuppgjör, farðu til  **Kerfisstjórnun \> Uppsetning \> Sjálfvirkni ferla** eða **Aðalbók \> Uppsetning höfuðbókar \> Sjálfvirkni ferla**.

Fyrst skaltu velja **Búðu til nýja ferli sjálfvirkni** valmöguleika og veldu **Fjárhagsuppgjör**. Töframaður leiðir þig síðan í gegnum ferlið við að setja upp sjálfvirknina.

## <a name="general-page"></a>Almenna síðan

Á **Almennt**  síðu hjálparinnar, sláðu inn nafn fjárhagsuppgjörsins sem þú ert að búa til. Til dæmis, ef samsvarandi skuldfærslur og inneignir eru gerðar upp á mánudegi skaltu slá inn lýsandi heiti eins og **LedgerSettle\_ mán**. Nafnið sem þú slærð inn birtist í **Sjálfvirkniregla** dálki á **Fjárhagsuppgjör**  síðu.

Stillingar sem eftir eru á síðunni eru almennar og skilgreina tilvikamynstur fyrir þessa útgáfu af fjárhagsuppgjörum. Til dæmis, ef tilvik er fyrir mánudag, getur þú skilgreint það þannig að það keyrir vikulega og þú getur valið mánudag sem vikudag þegar það keyrir. Einnig er hægt að færa inn snemmbúna tímaáætlun, t.d. 02:00, þannig að sjálfvirkniferlinu verði lokið fyrir upphaf næsta viðskiptadags. Við mælum með því að þú tímasetur sjálfvirkni ferlisins þannig að hún fari fram utan venjulegs vinnutíma. Þannig hjálpar þú til við að draga úr áhrifum á bókhaldsfólk þitt á vinnudeginum.

Fyrir frekari upplýsingar um aðra reiti á **Almennt**  síðu, sjá skjöl um sjálfvirkni ferlisins.

## <a name="ledger-settlements-match-criteria-page"></a>Fjárhagsuppgjör samsvarar viðmiðunarsíðu

Næsta síða í töframanninum er **Fjárhagsuppgjör passa við viðmið**  síðu. Það er notað til að skilgreina helstu reikninga sem eru innifalin í sjálfvirkni ferlisins og viðmiðin sem eru notuð til að ákvarða samsvarandi skuldfærslur og inneignir.

### <a name="account-selection"></a>Val á lykli

Helstu reikningar sem þú hefur áður skilgreint sem fjárhagsuppgjörsreikninga fyrir lögaðilann eru sýndir. (Þú skilgreinir aðalreikninga sem fjárhagsuppgjörsreikninga á **Aðalbók \> Uppsetning höfuðbókar \> Fjárhagsfæribreytur \> Fjárhagsuppgjör** .)

### <a name="main-account-and-posting-layer"></a>Aðalreikningur og færslulag

The  **Aðalreikningur** og **Færslulag**  gildi eru nauðsynleg samsvörunarviðmið. The **Aðalreikningur** og **Færslulag** gildi fjárhagsdebetfærslunnar og kreditfærslunnar verða að vera jöfn til að passa saman við sjálfvirka fjárhagsuppgjörsferli.

### <a name="posting-type"></a>Bókunargerð

Veldu **Tegund færslu** valmöguleika ef fjárhagsdebet- og kreditfærslur verða að hafa sömu bókunartegund til að passa saman við sjálfvirka fjárhagsuppgjörsferli.

### <a name="financial-dimensions"></a>Fjárhagsvíddir

Veldu **Fjárhagsstærðir** valmöguleika ef debet- og kreditfærslur fjárhagsbókar verða að hafa sömu fjárhagsvíddir til að passa við sjálfvirka fjárhagsuppgjörsferli. Þegar þessi valkostur er valinn verður að velja skilyrði fyrir fjárhagsvíddargildi í **Tiltækar fjárhagsvíddir** lista. The **Tiltækar fjárhagsvíddir** listi inniheldur ekki aðalreikningsvíddina, vegna þess að það er sjálfkrafa krafist sem hluti af samsvörunarskilyrðunum.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Skoðaðu niðurstöður sjálfvirkni fjárhagsuppgjörs

Eftir að sjálfvirkniröð fjárhagsuppgjörs er stofnuð eru tilvik fyrir hverja uppgjör fjárhagsuppgjörs sýnd í vikulegri sjálfvirkni vinnslu. Þar að auki er staða hvers tilviks sýnd. Eftirfarandi stöður eru notaðar:

- **Tímaáætlun**  – Sjálfvirknin er áætluð, en hún hefur ekki enn keyrt.
- **Framkvæmd** – Sjálfvirknin er í gangi.
- **Villa**  – Sjálfvirknin hefur keyrt en villa kom upp. Þú getur skoðað villurnar með því að velja **Skoða niðurstöður**  takki.
- **Lokið**  – Sjálfvirknin hefur gengið vel. Hægt er að skoða niðurstöður uppgjörs á **Fjárhagsuppgjör** síðu.

Til að skoða samsvarandi niðurstöður skaltu fara á **Aðalbók \> Reglubundin verkefni \> Fjárhagsuppgjör**. The **Sjálfvirkniregla** sviði á **Fjárhagsuppgjör** síða sýnir heiti sjálfvirka fjárhagsuppgjörsáætlunarverksins sem var notað til að jafna færsluna. Misheppnaðar uppgjörstilraunir munu ekki uppfæra **Sjálfvirkniregla** gildi. Ef þú bakfærir færslu handvirkt sem áður tókst að gera upp með sjálfvirkniferlinu, **Sjálfvirkniregla** gildi verður fjarlægt.

The **Dagsetning ákveðin** reiturinn fyrir samsvarandi færslur sýnir dagsetninguna þegar sjálfvirkniferlið var framkvæmt.

## <a name="editing-a-ledger-settlement-automation"></a>Breyting á sjálfvirkni fjárhagsuppgjörs

Sjálfvirkniramminn ferli gerir þér kleift að breyta röðinni og tilvikunum sem eru búnar til fyrir fjárhagsuppgjörið. Seríunni er hægt að breyta úr annaðhvort **Sjálfvirkni ferlisins**  síðu eða vinnslusjálfvirkni vikunnar. Til dæmis, ef stjórnandi ákveður að framkvæma fjárhagsuppgjör á miðvikudag í stað mánudags, getur hann fundið atvik í vikuyfirliti og valið **Skoða/breyta – Röð**.

Ef þú breytir röð ertu beðinn um að tilgreina hvort breytingin eigi að vera á öllum fyrirliggjandi tilvikum eða aðeins á nýjum tilvikum. Sögulegir atburðir sem þegar hafa stöðu **Lokið**, eða sem endaði á an **Villa**  stöðu, verður ekki breytt.

Einnig er hægt að bæta við nýju tilviki eða breyta fyrirliggjandi tilviki. Til dæmis, næsta fjárhagsuppgjörstilvik er áætlað að keyra miðvikudaginn 1. janúar, en þessi dagsetning er frídagur. Þú getur breytt tilvikinu úr annaðhvort **Sjálfvirkni ferlisins**  síðu eða vinnslusjálfvirkni vikunnar. Síðan er opnuð sem sýnir áætlunarupplýsingar og samsvörunarviðmið. Hér er hægt að breyta áætluðum tíma og dagsetningu. Þú getur líka breytt samsvörunarviðmiðunum, ef breytinga er þörf. 

Einnig er hægt að óvirkja tilvik eða röð tilvika. Til að slökkva á atviki og stöðva vinnslu fyrir það skaltu velja það í vikulegri sjálfvirkni vinnslu og velja síðan **Slökkva**. Þú getur slökkt á röð á **Sjálfvirkni ferlisins**  síðu.

## <a name="security-for-ledger-settlement-automation"></a>Öryggi fyrir sjálfvirkni fjárhagsuppgjörs

The **Viðhalda stillingum sjálfvirkrar röðar fjárhagsuppgjörs** skylda hefur verið bætt við hlutverk bókhaldsstjóra og bókhaldsstjóra og **Skoða stillingar sjálfvirkrar röðar fjárhagsuppgjörs** skylda hefur verið bætt við hlutverk endurskoðanda, bókhaldsstjóra og bókhaldsstjóra fyrir sjálfvirknivæðingu fjárhagsuppgjörs. Þessar skyldur eru sjálfgefnar öryggisstillingar, en þeim er hægt að breyta miðað við kröfur fyrirtækisins þíns.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Almennar færibreytur höfuðbókar fyrir sjálfvirkni fjárhagsuppgjörs

The **Uppgjör dæmigerð jafnvægi** reiturinn gefur til kynna í hvaða röð sjálfvirka fjárhagsuppgjörið verður unnið í. Til að setja upp eða skoða **Uppgjör dæmigerð jafnvægi** gildi, farðu til **Aðalbók \> Uppsetning \> Fjárhagsfæribreytur**, og veldu **Fjárhagsuppgjör** flipa.

Ef **Debet** er valið byrjar sjálfvirkt uppgjörsferli fjárhagsbókar á debethlið og leitar að samsvarandi inneign. Ef **Inneign** er valið byrjar sjálfvirkt uppgjörsferli fjárhagsbókar á kredithlið og leitar að samsvarandi skuldfærslum. Þessi valkostur ætti að endurspegla dæmigerða stöðu aðalreikningsins.

## <a name="processing-a-ledger-settlement-automation"></a>Vinnsla sjálfvirkni uppgjörs fjárhags

Þegar sjálfvirknin er keyrð velur kerfið fjárhagsfærslur fyrir aðallykla sem eru skilgreindir fyrir sjálfvirkni vinnsluröðina. Það pantar færslurnar eftir dagsetningu með því að nota dagsetningarbil frá upphafi reikningsárs til dagsins þegar sjálfvirkni ferlisins er keyrt. Það passar út frá tilgreindum samsvörunarviðmiðum. Heildargildi bókhaldsgjaldmiðilsupphæða debet og inneign verða að passa saman til að hægt sé að gera upp.

Á meðan verið er að vinna úr aðalreikningi vegna tilviks sjálfvirkni fjárhagsuppgjörs geturðu ekki birt hann í **Fjárhagsuppgjör** síðu. Þú verður að bíða þar til sjálfvirkniferlinu er lokið. Við mælum með að þú skipuleggur sjálfvirkni ferlisins til að keyra utan vinnutíma til að koma í veg fyrir árekstra.

Sjálfvirkniferlið mun innihalda allar færslur sem uppfylla skilyrðin, nema færslur sem hafa verið handvirkt merktar til uppgjörs á **Fjárhagsuppgjör** síðu.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Bakfærsla á viðskiptum sem eru gerð upp með sjálfvirkniferlinu

Hægt er að bakfæra uppgjör sem var gert með sjálfvirku fjárhagsjöfnunarferlinu. Þegar færslu sem var gerð upp með sjálfvirkniferlinu er snúið við, er **Sjálfvirkniregla** gildi verður fjarlægt.

---
title: Viðmót efnismeðhöndlunarbúnaðar (MHAX)
description: Þetta efnisatriði lýsir því hvernig á að setja upp viðmót efnismeðhöndlunarbúnaðar (MHAX) þannig að hægt sé að tengjast við ytra efnismeðhöndlunarkerfi (MH).
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4c04b8a9574bb6f34b56b4a7462882f1885f1178
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695592"
---
# <a name="material-handling-equipment-interface-mhax"></a>Viðmót efnismeðhöndlunarbúnaðar (MHAX)

[!include [banner](../../includes/banner.md)]

Hægt er að nota *viðmót efnismeðhöndlunarbúnaðar* (MHAX) til tengja ytri efnismeðhöndlunarkerfi (MH) við vöruhús sem er stjórnað af ítarlegu vöruhúsakerfi (WMS) í Microsoft Dynamics 365 Supply Chain Management. Viðmótið á milli WMS og MH-kerfa samanstendur af tveimur biðröðum: ein fyrir tilvik á útleið (WMS to MH) og ein fyrir tilvik á innleið (MH til WMS). WMS-kerfið myndar tilvik á útleið út frá vinnulínum sem eru stofnaðar þegar ýmsar vinnur eru stofnaðar og framkvæmdarferlar. MH-kerfið athugar síðan reglulega WMS-kerfið fyrir nýjum tilvikum og vinnur úr svörunum. Þegar MH-kerfið hefur lokið við meðhöndlun tilvikanna í samræmi við verkleiðbeiningar, sendir það tilvik á innleið, svo sem vinnulínulok og of lítil tiltekt.

Eftirfarandi mynd sýnir ýmsar einingar og röðina sem unnið er úr í þegar MHAX-samþættingu er notuð.

![MHAX-hlutir og samskipti.](media/mhax-components.png "MHAX-hlutir og samskipti")

Hér er útskýring á samskiptum sem birtast í fyrri mynd:

1. Þegar verk er stofnað eða framkvæmt eru tilvik á útleið búin til í biðröð á útleið.
2. MH-búnaðurinn tengist við þjónustu MH-búnaðar, athugar með ný tilvik sem tengjast honum og vinnur úr þeim tilvikum.
3. Þegar MH-búnaðurinn er tilbúinn til að tilkynna til baka tengist hann við þjónustuna aftur og sendir inn tilvik á innleið. Úrvinnsla biðraðar vinnur strax úr þessum tilvikum.
4. Byggt á gögnum tilviks á innleið, gæti úrvinnsla biðraðar keyrt fyrirliggjandi vinnu, breytt henni eða stofnað nýja vinnu.

## <a name="turn-on-the-mhax-feature"></a>Kveikja á MHAX-eiginleikanum

Áður en hægt er að nota MHAX-eiginleikann verður að kveikja á bæði eiginleikann og skilgreiningarlyklinum.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
2. Á vinnusvæðinu **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** skal kveikja á eiginleikanum sem heitir *Viðmót efnismeðhöndlunarbúnaðar*.
3. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
5. Stækkið **Viðskipti \> Vöruhúsakerfi og flutningsstjórnun** og veljið siðan gátreitinn **Viðmót efnismeðhöndlunarbúnaðar**.
6. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>Stilla færibreytur MHAX

Stilla verður nokkrar færibreytur á síðunni **Færibreytur fyrir viðmót efnismeðhöndlunarbúnaðar** til að grunnstilla eiginleikann.

1. Farið í **Viðmót efnismeðhöndlunarbúnaðar \> Uppsetning \> Færibreytur fyrir viðmót efnismeðhöndlunarbúnaðar**.
2. Á flipanum **Almennt** skal stilla eftirfarandi reiti:

    - **Notandakenni** – Veljið starfskraft. Þessi starfsmaður verður notaður til að keyra allar vinnuaðgerðir (tiltekt og frágang) sem eru unnar í gegnum biðröð á innleið.
    - **Virkja skilaboðakenni á innleið** – Þegar þessi valkostur er stilltur á *Já*, ef tvítekið skilaboðakenni á innleið er móttekið verður skilaboðunum hafnað og villuboð segja að skilaboðin séu þegar til. Þegar þessi valkostur er stilltur á *Nei* verður tvítekin skilaboðakenni á innleið leyfð.

3. Í flipanum **Númeraraðir** skal velja númeraraðir fyrir allt kerfið sem á að nota til að mynda einkvæm auðkenni fyrir atriði í biðröð á innleið, atriði í biðröð á útleið og vinnulínupör.

## <a name="outbound-events"></a>Tilvik á útleið

Á tilteknum tímapunktum í stofnun vinnu eða framkvæmd vinnu ákveður kerfið hvort það verði að mynda tilvik á útleið til að senda til MH-kerfisins. Ef áskrift er skilgreind fyrir tiltekinn tímapunkt í vinnslu vöruhúss mun kerfið mynda tilvikið samkvæmt uppsetningu áskriftarinnar.

### <a name="structure-of-outbound-events"></a>Skipulag tilvika á útleið

Hvert tilvik á útleið er auðkennt sérstaklega með biðraðarkenni á útleið. Færslugerðin á útleið ákvarðar gerð tilviksins. Vöruhúsið og auðkenni áskriftarinnar sem myndar tilvikið eru einnig skráð í tilvikið.

Til að færa gögn yfir í MH-kerfið inniheldur tilvikið á útleið 10 svæði fyrir gögn (**data01** til **data10**). Þessi gagnasvæði eru með beina vörpun í fyrirliggjandi gagnagrunnssvæði. Nánar tiltekið, þau eru dregin úr svæðum í töflum vinnulínu og vinnuhauss. Velja má svæðin að vild. Þau eru sett upp þegar áskrift er stofnuð.

Fyrir utan gagnasvæðin tíu sem eru með beina vörpun í fyrirliggjandi gagnagrunnssvæði, getur tilvikið innihaldið frekari gagnasvæði sem er þekkt sem *innihald*. Innihald þessa svæðis er myndað af sérsniðnum X++ kóða sem er þekktur sem *myndun innihald*. Öll myndun innihalds sem á að nota er sett upp í áskriftinni.

Til að tryggja að MH-kerfið fái hvert biðraðarkenni á útleið eitt í einu, er stöðureitur notaður til að tilgreina hvort tilvik sé tilbúið til að vera sent til ytra kerfisins eða hvort það sé þegar búið að senda það.

### <a name="outbound-queue-subscriptions"></a>Áskriftir biðraðar á útleið

Áður en einhver tilvik eru mynduð verður að setja upp áskrift til að segja MHAX-eiginleikanum hvort og hvernig eigi að mynda tilvikin. Mynduð tilvik eru merkt af kennimerki áskriftar. Þess vegna geta mörg MH-kerfi tengst sama WMS-kerfinu en haldið tilvikum sínum aðskildum. Þegar MHAX-þjónustan er athuguð fyrir nýjum tilvikum, er áskrift einn af tiltækum valmöguleikum til að sækja tilvikin.

Til að stofna áskrift skal fara í **Viðmót efnismeðhöndlunarbúnaðar \> Uppsetning \> Áskriftir**. Fyrir hverja áskrift eru eftirfarandi færibreytur í boði:

- **Áskriftarkenni** – Einkvæmt heiti sem auðkennir áskriftina.
- **Lýsing** – Frjáls textalýsing áskriftarinnar.
- **Vöruhús** – Ákveðið vöruhús sem sía á tilvik eftir.
- **Færslugerð á útleið** – Gerð tilvika sem áskriftin á að innihalda.
- **Myndun innihalds** – Valfrjáls viðbót kóða sem getur fært viðbótarupplýsingar inn í reitinn **Innihald** í tilviki á útleið.

Hægt er að tengja fyrirspurn við hverja áskrift. Þessi fyrirspurn síar vinnulínur og hausa til að takmarka enn frekar vinnuna sem notar áskriftina til að mynda tilvik. Til að bæta fyrirspurn við áskrift skal velja gátreitinn **Keyra fyrirspurn** fyrir viðeigandi áskrift á síðunni **Áskriftir** og síðan velja **Breyta fyrirspurn** á aðgerðasvæðinu. Hefðbundinn fyrirspurnarritill Supply Chain Management birtist.

Þar að auki inniheldur áskriftin *áskriftarvörpun* sem varpar reitum úr annaðhvort vinnuhausnum eða vinnulínunni í einhver eða öll 10 lausu gagnasvæðin í tilvikinu á útleið eftir þörfum. Til að skila upplýsingum til MHAX-þjónustunnar er færslukenni vinnulínunnar yfirleitt haft með eða *pörunarkenni vinnulínunnar*. (Pörunarkenni vinnulínunnar er nýr eiginleiki sem gerir kerfinu kleift að nota eina skilaskipun til að vinna úr tiltektar- og frágangslínum.) Reitirnir sem eftir standa fara eftir notkunartilfellinu. Nokkur dæmi eru gefin síðar í þessu efnisatriði.

Til að setja upp áskriftarvörpun skal velja viðeigandi áskrift á síðunni **Áskriftir** og síðan velja **Áskriftarvörpun** á aðgerðasvæðinu. Í svarglugganum **Áskriftarvörpun** sem birtist er hægt að úthluta töflu og reit fyrir hvert tiltækt gagnasvæði eftir þörfum.

### <a name="outbound-event-types"></a>Gerðir tilvika á útleið

Þessi hluti lýsir mismunandi gerðum tilvika sem eru í boði. (Gerðir tilvika eru einnig þekktar sem *færslugerðir*.) Þar er einnig útskýrt hvenær hver gerð tilviks er stofnuð í WMS-kerfinu.

#### <a name="work-creation-events"></a>Tilvik vinnustofnunar

Tilvik vinnustofnunar eru stofnað eftir að forritið býr til vinnu. Þessi hegðun á við um flestar gerðir af vinnustofnunarferlum, þá helst stofnun tiltektar og áfyllingarvinnu. Almennt, ef vinna er stofnuð í *Opinni* stöðu, sem gefur til kynna að starfsmaður getur hafið keyrslu á vinnunni, verður tilvik vinnustofnunar myndað. Auk þess verða tilvik vinnustofnunar mynduð fyrir grunnhreyfingarvinnu (ekki hreyfingu af völdum sniðmátsvinnu) jafnvel þótt sú vinna sé ekki stofnuð sem opin vinna.

Eftirtektarverð undantekning á þessari hegðun er regluleg talningarvinna sem er ekki studd sem stendur. Birgðatalningar í MH-kerfinu er utan sviðs MHAX og niðurstöður talninga þarf að flytja inn í birgðatalningarbók.

Þegar vinna hefur verið stofnuð vinnur MHAX-þjónustan úr vinnulínum sem eru myndaðar og úthlutar pörunarkenni vinnulínu á allar myndaðar vinnulínur fyrir hvern vinnuhaus. Markmiðið er að flokka allar vinnulínur tiltektar með heppnuðum frágangi undir eitt pörunarkenni vinnulínu. (Flokkarnir samsvara pörunum tiltektar/frágangs í vinnusniðmátum.) Á þennan hátt er hægt að nota eitt auðkenni til að tilkynna vinnulok fyrir allar tiltektar- og frágangslínur sem eiga við. Flokkunarferlið hefst á fyrstu línunni og heldur síðan áfram með sama kenninu þar til kemur að heppnuðu pari af vinnulínum frágangs/tiltektar. Hlaupandi auðkenni er úthlutað til frágangslínu þess pars. Nýtt auðkenni er síðan notað fyrir tiltektarlínu næsta pars. Þetta ferli heldur áfram þar til það hefur unnið úr öllum línum sem tilheyra vinnuhausnum.

Sem sérstakur eiginleiki fyrir tilvik vinnustofnunar, ef valkosturinn **Lokuð bylgja** er stilltur á *Já* í vinnuhausnum, munu tilvikin sem eru mynduð fá stöðuna *Lokað fyrir* í staðinn fyrir hefðbundnu stiöðuna *Tilbúin* sem er notuð til að senda þau í MH-kerfið. Flaggið **Lokuð bylgja** í vinnuhausnum gefur til kynna að vinnuhausinn sé ekki tilbúinn fyrir starfsmenn til að keyra hugsanlega vegna ókláraðrar áfyllingarvinnu. Þegar flaggið **Lokuð bylgja** er hreinsuð verður opnað fyrir tilvik sem þegar hafa verið mynduð og eru tiltæk fyrir MH-kerfið til að sækja úr biðröðinni.

#### <a name="work-initiation-events"></a>Tilvik vinnuræsingar

Tilvik vinnuræsingar fara í gang þegar staða vinnu breytist úr *Opin* í *Í vinnslu* meðan á uppfærslu vinnu stendur.

#### <a name="work-completion-events"></a>Tilvik vinnuloka

Tilvik vinnuloka fara í gang þegar staða vinnu breytist úr *Í vinnslu* í *Lokað* meðan á uppfærslu vinnu stendur.

#### <a name="work-cancellation-events"></a>Tilvik vinnuafturköllunar

Tilvik vinnuafturköllunar fara í gang þegar staða vinnu breytist úr einhverri stöðu annarri en *Hætt við* í *Hætt við* meðan á uppfærslu vinnu stendur. Að auki er öllum öðrum tilvikum sem tengjast vinnuhausnum eytt úr biðröð fyrir allar áskriftir. Á þennan hátt koma ytri kerfi í veg fyrir úrvinnslu tilvika sem ekki er þörf á.

#### <a name="pickput-completion-events"></a>Tilvik tiltektar-/frágangsloka

Tilvik tiltektar-/frágangsloka fara í gang þegar staða tiltektar-/frágangslínu breytist úr *Í vinnslu* í *Lokað* meðan á uppfærslu vinnulínu stendur.

### <a name="monitor-the-outbound-queue"></a>Fylgst með biðröð á útleið

Til að fara yfir biðröð á útleið skal fara í **Viðmót efnismeðhöndlunarbúnaðar \> Almennt \> Biðröð á útleið**. Síðan **Biðröð á útleið** birtir öll atriði í biðröð á útleið og stöðu þeirra. Veljið atriði í biðröð til að skoða upplýsingar þess. Þessar upplýsingar fela í sér færslugerð atriðisins, áskriftina sem er notuð og gildi fyrir hvert gagnasvæði (**data01** til **data10**) og innihaldið.

### <a name="clean-up-the-outbound-queue"></a>Hreinsun biðraðar á útleið

Að lokum mun biðröðin á útleið smám saman fyllast af atriðum biðraðar sem er þegar búið að senda. Til að fjarlægja þessar vörur skal fara í **Viðmót efnismeðhöndlunarbúnaðar \> Reglubundnar vinnslur \> Hreinsun \> Hreinsun biðraðar á útleið**.

## <a name="inbound-events"></a>Tilvik á innleið

Þessi hluti lýsir ýmsum gerðum tilvika á innleið sem MH-kerfið getur tilkynnt aftur til WMS-kerfisins. Þar er einnig útskýrt að MH-kerfið þurfi að útvega gögn og hvað hvert tilvik á innleið gerir í WMS-kerfinu.

### <a name="structure-of-inbound-events"></a>Skiplag tilvika á innleið

Þegar tilvik á innleið eru sent þarf ytra kerfið að útvega færslugerðina á innleið ásamt allt að 10 færibreytum (**data01** til **data10**). Valfrjáls villuleit tryggir að MHAX-þjónustan hafi ekki fengið sama tilvikið á innleið oftar en einu sinni. Til að virkja þessa villuleit þarf hvert tilvik á innleið að hafa einkvæmt skilaboðakenni. Ef tekið er við tvíteknu skilaboðakenni og ef valkosturinn **Virkja skilaboðakenni á innleið** er stillt á *Já* á síðunni **Færibreytur fyrir viðmót efnismeðhöndlunarbúnaðar** verður skilaboðunum hafnað. Villuboð gefa til kynna að skilaboðin séu þegar til staðar.

Til viðbótar við gagnasvæði á innleið úthlutar kerfið einkvæmu kenni biðraðar á innleið á tilvikið.

### <a name="inbound-event-types"></a>Gerðir tilvika á innleið

Þessi hluti útskýrir gerðir tilvika á innleið (færslugerðir) sem eru studdar og gögnin sem þarf að útvega fyrir tilvik sem á að vinna úr.

#### <a name="work-confirm-events"></a>Tilvik vinnustaðfestingar

Tilvik vinnustaðfestingar krefst þess að gagnasvæði á innleið innihaldi eftirfarandi upplýsingar:

- **data01** – Auðkenni fyrir vinnulínupar.
- **data02** – Færslukenni vörulínu (`RecId` gildi).

    > [!NOTE]
    > *Annaðhvort* reiturinn **data01** *eða* reiturinn **data02** verða að vera til staðar.

- **data03** – Auðkenni númeraplötunnar sem á að tína úr.
- **data04** – Auðkenni númeraplötu markmiðs í vinnuhausnum.

Ef auðkenni vinnulínupars er útvegað verður öll tiltekt, frágangur eða sérsniðnar vinnulínur merktar með auðkenni vinnulínuparsins og sem eru með stöðuna *Opin* eða *Í vinnslu* keyrð eitt af öðru. Ef færslukenni vinnulínu (`RecId` gildi) er útvegað verður vinnulínan að vera tiltekt, frágangur eða sérsniðin vinnulína sem er með stöðuna *Opin* eða *Í vinnslu*.

Tiltektarlínur frá númeraplötustýrðum staðsetningum krefjast þess að **data03** tilgreinni númeraplötuna sem á að tína úr, óháð því hvort línurnar séu merktar af færslukenni vinnulínunnar eða pörunarkenni vinnulínunnar. Reiturinn **data04** verður að tilgreina númeraplötu markmiðs í vinnuhaus fyrir tiltektina.

Frágangslínur taka ekki við ekki frekari upplýsingar. Þær eru aðeins keyrðar út frá núverandi staðsetningu vinnulínunnar og marknúmeraplötu vinnunnar. Ef gera þarf fráganginn á annari staðsetningu skal breyta staðsetningu vinnulínunnar eins og lýst er í hlutanum [Hnekkja tilvikum](#override-events) síðar í þessu efnisatriði.

Sérsniðnar vinnulínur hvorki þurfa né styðja við frekari upplýsingar í tilvikinu á innleið.

#### <a name="short-pick-events"></a>Tilvik of lítillar tiltektar

Tilvik of lítillar tiltektar krefst þess að gagnasvæði á innleið innihaldi eftirfarandi upplýsingar:

- **data02** – Auðkenni vinnufærslu (`RecId` gildi).
- **data03** – Auðkenni númeraplötunnar sem á að tína úr.
- **data04** – Magn sem á að taka til.
- **data05** – Undantekningarkóði of lítillar tiltektar.
- **data06** – Auðkenni númeraplötu markmiðs í vinnuhausnum.

> [!NOTE]
> Reiturinn **data01** er ekki notaður fyrir tilvik of lítilla tiltekta.

Þetta tilvik líkist tilviki vinnustaðfestingar, en á aðeins við um tiltektarlínur.

#### <a name="override-events"></a><a id="override-events"></a>Tilvik hnekkinga

Hnekkingartilvik krefjast þess að gagnasvæði á innleið innihaldi eftirfarandi upplýsingar:

- **data01** – Auðkenni vinnufærslu (`RecId` gildi).
- **data02** – Nýja staðsetningarauðkennið.

Vinnulínan verður annaðhvort að hafa stöðuna *Opin* eða *Í vinnslu* og nýja staðsetningin verður að vera til.

#### <a name="license-plate-receipt-events"></a>Tilvik númeraplötumóttöku

Tilvik númeraplötumóttöku krefjast þess að gagnasvæði á innleið innihaldi eftirfarandi upplýsingar:

- **data01** – Auðkenni númeraplötunnar á innleið sem á að móttaka.

Kerfið framkvæmir móttökuaðgerð númeraplötu sem byggir á númeraplötunni sem er gefin upp sem gildið fyrir reitinn **data01**.

### <a name="monitor-the-inbound-queue"></a>Fylgst með biðröð á innleið

Til að fara yfir biðröð á innleið skal fara í **Viðmót efnismeðhöndlunarbúnaðar \> Almennt \> Biðröð á innleið**. Síðan **Biðröð á innleið** birtir öll atriði í biðröð á innleið og stöðu þeirra. Veljið atriði í biðröð til að skoða upplýsingar þess. Þessar upplýsingar fela í sér færslugerð atriðisins, skilaboðakennið og gildi fyrir hvert gagnasvæði (**data01** til **data10**).

Ef villa eða önnur gerð kladdaatriðis kom upp á meðan unnið var úr tilvikum á innleið, er hægt að skoða kladdann með því að velja **Villukladdi** á aðgerðasvæðinu.

### <a name="inbound-event-processing"></a>Vinnsla á tilviki á innleið

Tilvik á innleið eru fyrst skrifuð í gagnagrunninn og síðan eru þau strax keyrð (samtímis). Ef villa kemur upp við vinnslu er tilvikið enn skrifað í biðröðina, en staðan er stillt á *Með villu*. MHAX-þjónustan skilar villuboðum til MH-kerfisins og geymir villukladdann í tilviksfærslu á innleið til að skoða síðar.

Hægt er að endurvinna tilvik sem eru með stöðuna *Með villu* síðar ef ástæða villunnar er löguð. Til að endurvinna þau skal fylgja þessum skrefum:

- Farið í **Viðmót efnismeðhöndlunarbúnaðar \> Almennt \> Biðröð á innleið**. Veljið viðeigandi biðröð á innleið og veljið síðan **Endurvinna** á aðgerðasvæðinu.
- Farið í **Viðmót efnismeðhöndlunarbúnaðar \> Almennt \> Endurvinna biðröð á innleið með villum**. Venjulegur svargluggi runuvinnslu birtist. Þar er hægt að setja upp færslusíu og tímasetja eða keyra runuvinnslu til að vinna aftur úr biðröðinni.

Allar vinnuaðgerðir (tiltekt og frágangur) eru keyrðar með starfsmanni sem valinn er í reitnum **Notandakenni** á síðunni **Færibreytur fyrir viðmót efnismeðhöndlunarbúnaðar**.

### <a name="clean-up-the-inbound-queue"></a>Hreinsun biðraðar á innleið

Að lokum mun biðröðin á innleið smám saman fyllast af atriðum biðraðar sem er þegar búið að vinna úr. Til að fjarlægja þessi atriði skal fara í **Viðmót efnismeðhöndlunarbúnaðar \> Reglubundnar vinnslur \> Hreinsun \> Hreinsun biðraðar á innleið**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Fá flýtiyfirlit með því að nota biðraðarstjórann

Til að fá flýtiyfirlit yfir allar aðgerðir sem tengjast biðröðum á innleið og útleið skal fara í **Viðmót efnismeðhöndlunarbúnaðar \> Vinnusvæði \> Biðraðarstjóri**. Síðan **Biðraðarstjóri** býður upp á safn af flipum og reitum sem er hægt að nota til að fylgjast með og fletta í biðröðum. Þar er einnig að finna gagnlega tengla á flestar aðrar síður sem minnst er á í þessu efnisatriði.

## <a name="connect-to-the-mhax-service"></a>Tengjast MHAX-þjónustu

MHAX er innleitt sem sérsniðin þjónusta. Þess vegna er hún aðgengileg í gegnum SOAP- og REST-köll. Hér eru vistföng SOAP- og REST-endastöðva:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Sækja skilaboð úr biðröð á útleið

Til að sækja skilaboð úr biðröð á útleið skal nota eina af eftirfarandi aðferðum:

- Notið `readOutboundSubscriptionQueue` til að sækja tilvikin samkvæmt áskriftarkenninu.
- Notið `readOutboundWarehouseQueue` til að sækja tilvikin samkvæmt gerð tilviksins og vöruhúsakennisins yfir margar áskriftir.

---
title: Ítarleg sjálfvirk gjöld fyrir omni-rás
description: Þetta efnisatriði lýsir möguleikunum til að stjórna gjaldfærslum vegna annarra gjalda fyrir pantanir Commerce-rásar með því að nota eiginleika fyrir ítarleg sjálfvirk gjöld.
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: ef6396ec66a0f96ba97b176c46bf70d83a080883cf496312398f14dce3ad9758
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743432"
---
# <a name="omni-channel-advanced-auto-charges"></a>Ítarleg sjálfvirk gjöld fyrir omni-rás

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um stillingar og uppsetningu á eiginleika ítarlegra sjálfvirkra gjalda sem eru í boði í Dynamics 365 for Retail útgáfu 10.0.

Þegar eiginleikinn fyrir ítarlega sjálfvirk gjöld er virkjaður geta pantanir, sem eru stofnaðar í hvaða studdu Commerce rás sem er (sölustaður (POS), símaver og á netinu), nýtt sér stillingarnar [sjálfvirk gjöld](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) sem eru skilgreind í ERP-forritinu fyrir gjöld sem tengjast bæði haus og línustigi.

Í útgáfum á undan Retail útgáfu 10.0, eru stillingar fyrir [sjálfvirk gjöld](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) eingöngu aðgengileg með pöntunum sem eru stofnaðar í rás rafrænna viðskipta og eða símavers. Í útgáfum 10.0 og nýrri geta pantanir stofnaðar á sölustað notað stillingar sjálfvirkra gjalda. Þannig er hægt að bæta mismunandi gjöldum við sölufærslur með kerfisbundnum hætti.

Þegar notaðar eru útgáfur eldri en útgáfa 10.0 er POS-notandi beðinn um að færa inn sendingargjald handvirkt við stofnun á POS-færslunni „senda allt“ eða „senda valið“. Þótt möguleikinn á ýmsum gjöldum í forritinu er nýttur hvað varðar hvernig gjöldin eru skrifuð á pöntunina, er ekki boðið upp á neinn kerfisbundinn útreikning -- útreikningurinn reiðir sig á innslátt notanda til að ákvarða gildi gjaldanna. Eingöngu er hægt að bæta gjöldunum við sem einni „sendingu“ sem tengist gjaldakóða og ekki er hægt að lagfæra eða breyta honum svo auðveldlega í sölustað eftir að gjöldin eru stofnuð.

Notkun á handvirkri kvaðningu til að bæta sendingargjöldum við er enn í boði í útgáfum 10.0 og síðar. Ef fyrirtæki virkjar ekki færibreytuna **Ítarleg sjálfvirk gjöld** helst óbreytt að sölustaður biðji um handvirkan innslátt á gjöldum.

Með eiginleika ítarlegra sjálfvirkra gjalda geta POS-notendur haft kerfisbundinn útreikning fyrir öll skilgreind gjöld sem byggjast á töflum fyrir uppsetningu á sjálfvirkum gjöldum. Að auki geta notendur bætt við eða breytt ótakmörkuðum fjölda viðbótargjalda og þóknana fyrir allar sölufærslur sölustaðar í haus eða línustigi (fyrir staðgreiðslu við afhendingu eða pöntun viðskiptavinar).

## <a name="enable-advanced-auto-charges"></a>Virkja ítarleg sjálfvirk gjöld

Á síðunni **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur Commerce** skal fara í flipann **Pantanir viðskiptavinar**. Í flýtiflipanum **Gjöld** skal stilla **Nota ítarleg sjálfvirk gjöld** á **Já**.

![Færibreyta ítarlegra sjálfvirkra gjalda.](media/advancedchargesparameter.png)

Þegar ítarleg sjálfvirk gjöld eru virkjuð verða notendur ekki lengur beðnir um að slá inn sendingargjald handvirkt á afgreiðslukassa þegar þeir stofna viðskiptavinapöntunina „senda allt“ eða „senda valið“. Gjaldfærslur vegna pantana sölustaðar eru reiknaðar kerfisbundið og þeim bætt við POS-færslu (ef samsvarandi tafla sjálfvirkra gjalda passar við skilyrði pöntunarinnar sem er stofnuð eða finnst). Notendur geta einnig bætt við eða viðhaldið gjöldum hauss eða línustigs handvirkt í gegnum nýlega viðbættum POS-aðgerðum sem hægt er að bæta við skjáútlit sölustaðar.

Þegar ítarleg sjálfvirk gjöld eru virkjuð eru núverandi **Commerce færibreytur** fyrir **Sendingargjaldakóða** og **Endurgreiða sendingargjöld** ekki lengur notaðar. Þessar færibreytur eiga aðeins við ef færibreytan **Nota ítarleg sjálfvirk gjöld** er stillt á **Nei**.

Áður en þessi aðgerð er virkjuð skal tryggja að starfsmaður hafi verið prófaður og fengið þjálfun, því að virkjaði eiginleikinn mun breyta flæði viðskiptaferlisins um hvernig sending eða önnur gjöld eru reiknuð út og bætt við sölupantanir sölustaðar. Gakktu úr skugga um að þú hafir skilið áhrif flæðiferlisins á stofnun færslna fyrir sölustað. Fyrir pantanir í símaveri og rafrænum viðskiptum eru áhrifin vegna virkjunar á ítarlegum sjálfvirkum gjöldum í lágmarki. Forrit símavers og rafrænna viðskipta verður áfram með sömu hegðunina og áður sem tengjast töflum sjálfvirkra gjalda til að reikna út viðbótarþóknanir pöntunar. Notendur símaversrásar munu áfram geta breytt handvirkt öllum sjálfvirkum gjöldum sem kerfið reiknar í haus og línustigi, eða bætta handvirkt við viðbótargjöldum í haus eða línustigi.

## <a name="add-pos-operations"></a>Bæta við POS-aðgerð

Til að ítarleg sjálfvirk gjöld virki almennilega í forritaumhverfi sölustaðar, hefur nýjum POS-aðgerðum verið bætt við. Þessum aðgerðum verður að bæta við [Skjáútlit sölustaðar](/dynamics365/unified-operations/retail/pos-screen-layouts) og sett upp í tæki sölustaðar þegar þú setur upp ítarleg sjálfvirk gjöld. Ef þessum aðgerðum er ekki bætt við geta notendur ekki stjórnað eða unnið með ýmis gjöld í POS-færslum og geta á engan hátt leiðrétt eða breytt gildum gjaldanna sem eru reiknuð út kerfisbundið samkvæmt stillingum sjálfvirkra gjalda. Að lágmarki er ráðlagt að setja upp aðgerðina **Stjórna gjöldum** í POS-útliti.

Nýju aðgerðirnar eru sem hér segir.

- **142 - Stjórna gjöldum** - Notaðu þessa aðgerð til gera POS-notendum kleift að skoða og breyta ýmsum gjöldum fyrir POS-færslu sem var annaðhvort bætt við handvirkt eða kerfisbundið í gegnum útreikninga sjálfvirkra gjalda.
- **141 - Bæta við gjöldum í haus** - Notaðu þessa aðgerð til að gera notandanum kleift að bæta handvirkt ýmsum gjöldum á hausstigi við einhverja sölufærslu sölustaðar (og veldu gjaldakóðann sem á að nota).
- **140 - Bæta við gjöldum í línu** - Notaðu þessa aðgerð til að gera notandanum kleift að bæta handvirkt ýmsum gjöldum á línustigi við einhverja sölufærslulínu sölustaðar (og veldu gjaldakóðann sem á að nota).
- **143 - Endurreikna gjöld** - Notaðu þessa aðgerð til að framkvæma fullan endurútreikning á gjöldunum fyrir sölufærsluna. Öll fyrri sjálfvirk gjöld sem hafa verið yfirskrifuð af notanda verða reiknuð út aftur samkvæmt núgildandi stillingum á körfu.

Eins og með allar POS-aðgerðir, er hægt að gera öryggisstillingar til að sækjast eftir samþykki yfirmanns til þess að geta framkvæmt aðgerðina.

Mikilvægt er að hafa í huga að einnig sé hægt að bæta við ofangreindum POS-aðgerðum við POS-útlitið, jafnvel þótt færibreytan **Nota ítarleg sjálfvirk gjöld** sé gerð óvirk. Í þessari atburðarás munu fyrirtæki enn fá frekari ávinning af því að geta séð viðbótargjöld sem bætt er við handvirkt og breytt þeim með því að nota aðgerðina **Stjórna gjöldum**. Notendur geta einnig notað aðgerðirnar **Bæta við gjöldum í haus** og **Bæta við gjöldum í línu** fyrir POS-færslur jafnvel þegar færibreytan **Nota ítarleg sjálfvirk gjöld** er gerð óvirk. Aðgerðin **Endurreikna gjöld** hefur minni virkni ef hún er notuð þegar **Nota ítarleg sjálfvirk gjöld** er gert óvirkt. Í þessari atburðarás yrði ekkert endurreiknað og öllum gjöldum sem yrði bætt handvirkt við færsluna myndu vera endurstillt á $0,00.

## <a name="use-case-examples"></a>Dæmi um notkunartilfelli

Í þessum hluta eru sýnd dæmi um notkunartilfelli til að auðvelda þér að skilja stillinguna og notkun á sjálfvirkum gjöldum og ýmsum gjöldum í samhengi við pantanir rásar. Þessi dæmi sýna hegðun forritsins þegar færibreytan **Nota ítarleg sjálfvirk gjöld** hefur verið virkjuð.

### <a name="auto-charges-header-charges-example"></a>Dæmi um hausgjöld sjálfvirkra gjalda

#### <a name="use-case-scenario"></a>Atburðarás notkunar

Smásali vill bæta gjöldum við sjálfvirkt fyrir farm þegar færslur eru stofnaðar í Commerce-rás sem krefst sendingar á afurðum til viðskiptavinar. Smásali býður upp á tvo afhendingarmáta: Land og flug. Ef viðskiptavinur kýs afhendingu á landi og virði pöntunar er minna en $100 vill smásalinn rukka viðskiptavininn um farmgjald sem nemur $10.00. Ef virði pöntunar er yfir $100 og viðskiptavinurinn velur flutning á landi, verður hann ekki rukkaður um nein aukaleg farmgjöld. Ef viðskiptavinurinn velur flugið sem afhendingarmáta fyrir allar pantanir, verður hann rukkaður um farmgjald sem nemur $20.00, óháð heildarvirði pöntunar.

#### <a name="setup-and-configuration"></a>Uppsetning og skilgreining

Þessi atburðarás krefst skilgreiningar á tveimur töflum sjálfvirkra gjalda.

Farðu í **Viðskiptakröfur \> Uppsetning gjalda \> Sjálfvirk gjöld**.

Skilgreindu tvö mismunandi sjálfvirk gjöld á hausstigi. Skilgreindu eitt fyrir flutningsmátann „land“ og annað fyrir flutningsmátann „flug“. Fyrir þessa atburðarás skaltu skilgreina að nota eigi þau fyrir „Allir viðskiptavinir“.

Fyrir sendingargjöld á landi, í línuhlutanum á síðunni **Sjálfvirk gjöld** skaltu skilgreina gjald sem verður notað fyrir pantanir á milli $0,01 og $100 sem $10.00. Búðu til aðra gjaldalínu til að gefa til kynna að pantanir sem eru yfir $100,01 verði án gjalds.

![Dæmi um tvær sjálfvirkar gjaldatöflur.](media/headerchargesexample.png)

Fyrir sendingargjöld í flugi, í línuhlutanum í skjámynd sjálfvirkra gjalda, skaltu skilgreina gjald sem nemur $20.00 sem verður notað fyrir allar pantanir (fyrir virði á bilinu $0,01 til $9.999.999).

Sendu breytingarnar á Commerce Scale Unit/gagnagrunn rásar þannig að POS geti nýtt þær með því að keyra vinnsluna **1040 dreifingaráætlun**.

#### <a name="sales-processing-for-this-scenario"></a>Söluferli fyrir þessa atburðarás

Eftir að skilgreiningarskrefunum hér að ofan er lokið og breytingar hafa verið settar á gagnagrunn rásar, munu allar viðskiptavinapantanir eða sölufærslur, sem stofnaðar eru í rás POS, símavers eða í rafrænna viðskipta sem eru með afhendingaraðferðirnar „land“ eða „flug“ stilltar á hausstigi, nýta sér þessi gjöld og nota þau sjálfvirkt fyrir söluna.

Á þessum tíma eiga gjöldin við um allar sölufærslur sem eru stofnaðar innan lögaðilans sem nýta þessa afhendingarmáta, fyrst að enga virkni er hægt að tilgreina þar sem skilgreining sjálfvirks gjalds eigi aðeins við um tiltekna sölurás.

Fyrir aðstæður POS og rafrænna viðskipta, vegna þess að það er engin „haus“ sérstaklega skilgreindur í þessum pöntunum, verða gjöld hausstigs aðeins notuð ef allar sölulínur í færslunni eru stilltar þannig að þær eru sendar með nákvæmlega sama afhendingarmátanum. Ef það eru „blandaðir afhendingarmátar“ fyrir uppfyllingu á færslum sem eru stofnaðar af POS eða rafrænum viðskiptum, verða aðeins sjálfvirk gjöld línustigs tekin til greina og notuð.

Í atburðarásum símavers, er notandinn með stjórn á stillingu afhendingarmátans í pöntunarhaus. Gjöld í hausstigi verða því notuð fyrir þessar pantanir jafnvel þótt sumar sölulínurnar hafa verið skilgreindar til að nota annan afhendingarmáta. Gjöld á hausstigi fyrir símaverspantanir munu alltaf byggjast á afhendingarmátanum sem er skilgreindur stigi pöntunarhauss fyrir sölupöntunina.

### <a name="auto-charges-line-charges-example"></a>Dæmi um línugjöld sjálfvirkra gjalda

#### <a name="use-case-scenario"></a>Atburðarás notkunar 

Smásali vill bæta viðbótargjaldi við viðskiptavininn fyrir stofngjöld þegar viðskiptavinurinn kaupir ákveðna tegund af tölvu. Þessi tölva krefst aukalegra áskildra uppsetningaraðgerða sem söluaðilinn framkvæmir fyrir viðskiptavininn. Söluaðili hefur upplýst viðskiptavininn um að það verði viðbótarþóknun fyrir þessa uppsetningu. Söluaðili kýs að halda gjaldi sem tengist þessari þóknun aðskildu frá söluverði vörunnar út af fjárhagsskýrslugerð. Viðskiptavinurinn verður rukkaður um uppsetningargjald sem nemur $19,99 þegar þessi tiltekna tölva er keypt í hvaða rás sem er.

#### <a name="setup-and-configuration"></a>Uppsetning og skilgreining

Þessi atburðarás krefst skilgreiningar á töflu sjálfvirks gjalds fyrir eitt línustig.

Farðu í **Viðskiptakröfur \> Uppsetning gjalda \> Sjálfvirk gjöld**.

Stilltu fellivalmyndina **Stig** á **Lína** og búðu til nýja færslu sjálfvirkra gjalda fyrir alla viðskiptavini og fyrir tiltekna vöru eða vöruflokk þar sem stofngjöldin vera innheimt.

![Dæmi um sjálfvirka gjaldatöflu með eitt línustig.](media/linechargesexample.png)

Sendu gjöldin í Commerce Scale Unit/gagnagrunn rásar þannig að POS geti nýtt þær með því að keyra vinnsluna **1040 dreifingaráætlun**.

#### <a name="sales-processing-for-this-scenario"></a>Söluferli fyrir þessa atburðarás

Eftir að skilgreiningarskrefunum hér að ofan er lokið og breytingar hafa verið settar á gagnagrunn rásar, munu allar viðskiptavinapantanir eða sölufærslur, sem stofnaðar eru í rás POS, símavers eða í rafrænna viðskipta sem eru með þessa vöru í pöntuninni ræsa línustigsgjald sem verður bætt kerfisbundið við samtölu pöntunar.

Á þessum tíma eiga gjöldin við um allar sölulínur sem passa við skilgreiningu á sjálfvirkum gjöldum línustigs innan lögaðilans, fyrst að það er engin virkni til að skilgreininga sjálfvirk gjöld línustigs sem á eingöngu að nota fyrir tiltekna sölurás.

### <a name="manual-header-charges-example"></a>Dæmi um handvirk hausgjöld

#### <a name="use-case-scenario-description"></a>Lýsing á atburðarás notkunar

Söluaðili gerir undantekningu frá dæmigerðum ferlum með því að bjóða upp á sérstaka heimsendingu á vörum til viðskiptavina sem panta vörur í versluninni. Söluaðilinn og viðskiptavinurinn hafa samþykkt að viðskiptavinurinn greiði til viðbótar $25 meðhöndlunargjald fyrir þessa þjónustu. Viðtakandi pöntunar þarf að bæta þessu viðbótargjaldi við færsluna. Vegna þess að gjaldið er yfirbreiðslugjald og ekki tengt við eina vöru á pöntuninni, verður hausgjald notað.

#### <a name="setup-and-configuration"></a>Uppsetning og skilgreining

Gakktu úr skugga um að gjaldakóðinn sem verður notaður í þessari atburðarás hafi verið rétt stilltur með því að fara í **Viðskiptakröfur \> Uppsetning gjalda \> Gjöld** til að skilgreina viðeigandi gjaldakóða fyrir þessa atburðarás.

![Dæmi um gjöld.](media/chargesexample.png)

Ef gjaldið telst vera „sending“ tengt gjaldi í þeim tilgangi að senda tengda afslætti eða kynningar skal stilla **Sendingargjald** í gjaldakóðanum á **Já**. Ef einnig er leyft kerfisbundið að endurgreiða þetta gjald við vinnslu á færsluskilum í POS-forritinu skal stilla **Endurgreiðanlegt** á **Já**. Flaggið **Endurgreiðanlegt** á einungis við þegar færibreytan **Nota ítarleg sjálfvirk gjöld** er stillt á **Já**.

Sendu gjöldin í Commerce Scale Unit/gagnagrunn rásar þannig að POS geti nýtt þær með því að keyra vinnsluna **1040 dreifingaráætlun**.

Aðgerðin **Bæta við hausgjaldi** verður að vera skilgreind í [Skjáútlit sölustaðar](/dynamics365/unified-operations/retail/pos-screen-layouts) þannig að hnappur sem er aðgengilegur notandanum úr POS getur kallað á þessa aðgerð (aðgerð 141). Dreifa verður breytingunum á skjáútliti til rásar og einnig í gegnum virkni dreifingaráætlunarinnar.

#### <a name="sales-processing-of-manual-header-charges"></a>Söluferli fyrir handvirk hausgjöld

Til að framkvæma atburðarásina í POS-forritinu mun POS-notandinn stofna sölufærslu eins og venjulega, bætir vörum og öðrum skilgreiningum við söluna. Áður en greiðsla er innheimt ætti notandinn að framkvæma aðgerðina **Bæta við hausgjaldi** sem mun biðja notandann um að velja gjaldakóða og slá inn gildi fyrir gjöldin. Þegar notandi hefur lokið við ferlið verður gjaldinu bætt við sölupöntunina sem gjald á hausstigi.

Hægt er að nota þetta ferli símaverinu með því að nota núverandi eiginleikann **Gjöld** sem finnst í flipanum **Selja** á tækjastikunni. Á síðunni **Viðhalda gjöldum** getur notandinn bætt nýrri gjaldalínu við pöntunarhausinn.

### <a name="manual-line-charges-example"></a>Dæmi um handvirk línugjöld

#### <a name="use-case-scenario"></a>Atburðarás notkunar

Viðskiptavinur hefur óskað eftir því að tvær af fimm vörum í sölupöntuninni hans verði pakkaðar inn í gjafapappír. Söluaðilinn býður upp á þessa þjónustu gegn gjaldi sem nemur $2,00 á vöru. Viðtakandi pöntunar verður að bæta þessum gjöldum við tilgreindar vörur sem þarf að pakka inn í gjafapappír.

#### <a name="setup-and-configuration"></a>Uppsetning og skilgreining

Gakktu úr skugga um að gjaldakóðinn sem verður notaður í þessari atburðarás hafi verið rétt stilltur með því að fara í **Viðskiptakröfur \> Uppsetning gjalda \> Gjöld** til að skilgreina viðeigandi gjaldakóða fyrir þessa atburðarás.

Ef gjaldið telst vera „sending“ tengt gjaldi í þeim tilgangi að senda tengda afslætti eða kynningar skal stilla **Sendingargjald** í gjaldakóðanum á **Já**. Ef einnig er leyft kerfisbundið að endurgreiða gjaldið við vinnslu á færsluskilum í POS-forritinu skal stilla **Endurgreiðanlegt** á **Já**. Flaggið **Endurgreiðanlegt** á einungis við þegar færibreytan **Nota ítarleg sjálfvirk gjöld** er stillt á **Já**.

Sendu gjöldin í Commerce Scale Unit/gagnagrunn rásar þannig að POS geti nýtt þær með því að keyra vinnsluna **1040 dreifingaráætlun**.

Aðgerðin **Bæta við línugjaldi** verður að vera skilgreind í [Skjáútlit sölustaðar](/dynamics365/unified-operations/retail/pos-screen-layouts) þannig að hnappur sem er aðgengilegur notandanum úr POS getur kallað á þessa aðgerð (aðgerð 140). Dreifa verður breytingunum á skjáútliti til rásar og einnig í gegnum virkni dreifingaráætlunarinnar.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Söluferli fyrir handvirkt línugjald

Til að framkvæma atburðarásina í POS-forritinu mun POS-notandinn stofna sölufærslu eins og venjulega, bætir vörum og öðrum skilgreiningum við söluna. Áður en greiðsla er innheimt ætti notandinn að velja tiltekna línu þar sem gjaldið mun eiga við úr vörulista sölustaðar og framkvæma aðgerðina **Bæta við gjaldi**. Notandinn verður beðinn um að velja gjaldakóða og slá inn gildi fyrir gjöldin. Þegar notandi hefur lokið við ferlið verður gjaldið tengt við línuna og bætt við samtölu pöntunar sem gjald á línustigi. Notandinn getur endurtekið ferlið til að bæta við viðbótarlínugjöldum við aðrar vörulínur í færslunni ef þörf krefur.

Sama ferli er hægt að beita í símaverinu með því að nota eiginleikann „viðhalda gjöldum“ sem er að finna í fellivalmyndinni **Fjármál** í hlutanum **Sölupöntunarlínur** á síðunni **Sölupöntun**. Að velja þennan kost mun opna síðuna **Viðhalda gjöldum** þar sem notandinn getur bætt nýju línutengdu gjaldi við færsluna.

## <a name="additional-features"></a>Viðbótareiginleikar

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Breytingargjöld á sölufærslu sölustaðar

Bæta ætti **Stjórna gjöldum** aðgerðinni (142) við [Skjáútlit sölustaðar](/dynamics365/unified-operations/retail/pos-screen-layouts) svo að notandi geti skoðað og breytt eða hnekkt kerfisreiknuðum eða handstofnuðum gjöldum á haus- eða línustigi. Ef aðgerðinni er ekki bætt við, munu notendur ekki geta leiðrétt gildi fyrir gjöld í POS-færslunni og munu þeir ekki geta skoðað upplýsingar um gjöldin, svo sem gerð gjaldakóða sem bundin er við gjaldið.

Á síðunni **Stjórna gjöldum** í POS getur notandinn skoðað bæði upplýsingar um gjöld á haus- og línustigi. Notandinn getur notað virknina **Breyta** sem er í boði á þessari síðu til að gera breytingar á upphæðinni sem er innheimt á tiltekinni gjaldalínu. Þegar skrifað er handvirkt yfir gjaldalínu verður hún ekki kerfisbundið endurreiknuð nema notandinn hefji aðgerðina **Endurreikna gjöld**.

Ef búið er að skilgreina **Ástæðukóði fyrir hnekkingu gjalds** á uppsetningarsíðunni **Færibreytur Commerce** verður notandinn beðinn um að útvega ástæðukóða þegar gjöld hafa verið leiðrétt í POS-forritinu.

Ef ástæðukóðar hafa verið sóttir fyrir yfirskrifuð gjöld verður ný skýrsla einni í boði til að yfirfara og gera úttekt á þessum hnekkingum. Skýrsluna er hægt að finna í **Retail og Commerce \> Fyrirspurnir og skýrslur \> Ferill fyrir hnekkingu gjalda**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Endurgreiðsla á gjöldum í skilafærslu POS

Ef færibreytan **Nota ítarleg sjálfvirk gjöld** er stillt á **Já** verður núverandi færibreyta Commerce fyrir **Endurgreiða sendingargjöld** ekki lengur tiltæk. Til að tilgreina hvaða gjöld skal kerfisbundið endurgreiða til viðskiptavinar þegar ítarleg sjálfvirk gjöld eru notuð, skaltu vera viss um að tengdur gjaldakóði hafi verið skilgreindur sem **Endurgreiðanlegur** á uppsetningarsíðunni **Gjaldakóði**. Gakktu úr skugga um að stillingarnar hafi verið samstilltar við gagnagrunna Commerce-rásar í gegnum vinnslu áætlanadreifingar.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Endurgreiðsla gjalda í færslu skilapöntunar

Gjöld endurgreiðast ekki kerfisbundið til **Skilapantana** sem eru stofnaðar í Commerce. Notendur þurfa að velja valkostinn **Afrita gjöld** þegar þeir stofna **Skilapöntun**. Ef **Afrita gjöld** er ekki valið verða gjöld úr upprunalegri sölufærslu ekki endurgreidd sjálfkrafa. Ef **Afrita gjöld** er valið verða öll gjöld afrituð í skilapöntun og notandinn getur breytt eða fjarlægt gjöld handvirkt sem hann vill ekki að verði endurgreidd. Skilapöntunarferli símavers samþykkir ekki eins og er flaggið **Endurgreiðanlegt** í uppsetningunni **Gjaldakóði**.

### <a name="configuring-pos-receipts-to-show-charges"></a>Skilgreina POS-móttökur til að sýna gjöld

Eftirfarandi þáttum móttöku hefur verið bætt við móttökulínu og síðufót til að styðja virknina fyrir ítarleg sjálfvirk gjöld.

- **Sendingargjöld línu** - Þennan línustigsþátt er hægt að nota til að rifja upp tiltekna gjaldakóða sem hafa verið notaðir í sölulínunni. Eingöngu gjaldakóðar sem hafa verið flaggaðir sem **Sendingar** gjöld á síðunni **Gjaldakóði** verða sýndir hér.
- **Önnur línugjöld** - Þennan línustigsþátt er hægt að nota til að rifja upp tiltekna gjaldakóða, sem tengjast ekki sendingu, sem hafa verið notaðir í sölulínunni. **Önnur línugjöld** eru gjaldakóðar þar sem flaggið **Sending** á síðunni **gjaldakóði** hefur ekki verið virkjað.
- **Upplýsingar um sendingargjöld pöntunar** - Þessi þáttur á stigi síðufótar birtir lýsingarnar á gjaldakóðum sem eru notaðir í pöntuninni sem hefur verið flögguð sem **Sendingar** gjöld á uppsetningarsíðunni **Gjaldakóði**.
- **Sendingargjöld pöntunar** - Þessi þáttur á stigi síðufótar sýnir dollaraverðgildi á gjöldunum sem tengjast sendingu.
- **Upplýsingar um önnur gjöld pöntunar** - Þessi þáttur á stigi síðufótar birtir lýsinguna á gjaldakóðum sem eru notaðir í pöntuninni sem hefur ekki verið flögguð sem gjöld sem tengjast sendingu.
- **Önnur gjöld pöntunar** - Þessi þáttur á stigi síðufótar birtir dollaraverðgildi annarra gjalda sem tengjast ekki sendingu.

Mælt er með því að fyrirtækið bæti einnig við reitum með frjálsum texta á síðufót kvittunar til þess að skilgreina svæðin þar sem gjöldin verða tekin saman.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Komið í veg fyrir að gjöld verði reiknuð þar til POS pöntuninni er lokið

Sum fyrirtæki kunna að vilja bíða þar til notandinn hefur lokið við að bæta öllum sölulínunum við POS-færsluna áður en gjöld eru reiknuð út. Til að koma í veg fyrir útreikning á gjöldum þar sem vörum er bætt við POS-færsluna, skal kveikja á færibreytunni **Handvirkur útreikningur gjalda** í **Virknireglu** sem verslunin notar. Að virkja þessa færibreytu krefst þess að POS-notandi noti aðgerðina **Reikna út samtölu** þegar hann hefur lokið við að bæta afurðunum við POS-færsluna. Aðgerðin **Reikna út samtölur** ræsir þá útreikninginn á öllum sjálfvirkum gjöldum fyrir pöntunarhausinn eða línur eins og við á.

### <a name="charges-override-reports"></a>Skýrslur vegna hnekkingar gjalda

Ef notendur handvirkt hunsa reiknuð gjöld eða bæta gjaldi handvirkt við færsluna, verða þessi gögn tiltæk til endurskoðunar í skýrslunni **Ferill fyrir hnekkingu gjalda**. Skýrsluna er hægt að skoða úr **Retail og Commerce \> Fyrirspurnir og skýrslur \> Ferill fyrir hnekkingu gjalda**. Mikilvægt er að hafa í huga að gögnin sem eru nauðsynleg fyrir þessa skýrslu eru flutt frá gagnagrunni rásar inn í höfuðstöðvar í gegnum „P“ vinnslur dreifingaráætlunar. Þess vegna er ekki hægt að fá upplýsingar um hnekkingar sem hafa nýlega verið gerðar í POS í þessari skýrslu fyrr en þessi vinnsla hefur hlaðið upp færslugögnum verslunar í höfuðstöðvar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Kveikja á og grunnstilla sjálfvirk gjöld eftir rás](auto-charges-by-channel.md)

[Skipta gjöldum í haus í hlutfalli við samsvarandi sölulínur](pro-rate-charges-matching-lines.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: "Skilgreining og viðhald rásabiðlara, afgreiðslukassa og vélbúnaðarstöðva"
description: "Þessi efnisgrein fjallar um hvernig á að tengja jaðartæki við Retail POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 800e5c139b54541a179a336c8247eaa6017201d8
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Skilgreining og viðhald rásabiðlara, afgreiðslukassa og vélbúnaðarstöðva

[!include[banner](includes/banner.md)]


Þessi efnisgrein fjallar um hvernig á að tengja jaðartæki við Retail POS.

**Athugasemd:** Til að fá tilteknar leiðbeiningar, sjá [vélbúnaðarstöð smásölu og uppsetning](retail-hardware-station-configuration-installation.md) og [Retail Modern POS niðurhal/uppsetning í sjálfsafgreiðslu, og virkjun tækja fyrir Modern POS og Cloud POS](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Lykilþættir
Nokkra þætti eru notaðar til að skilgreina sambönd milli verslunar, afgreiðslukassa á sölustað (POS) eða rásir innan verslunarinnar og jaðartæki smásölu sem þessum afgreiðslukassa eða rásir nota til að vinna úr færslum. Þessi hluti lýsir hverjum þætti og útskýrir hvernig nota eigi hann við nýtingu í smásöluverslun.

### <a name="pos-registers"></a>Afgreiðslukassar

Fletting: Smella á **Smásala og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning POS** &gt; **Afgreiðslukassar**. Afgreiðslukassi er eining sem er notuð til að skilgreina eiginleika tiltekins tilviks af sölustað. Þessir eiginleikar taka til vélbúnaðarsniðs eða uppsetningar fyrir jaðarbúnað í smásölu sem verður notaður hjá afgreiðslukassanum, verslunina sem afgreiðslukassinn er varpaður á, og sjónræn upplifun fyrir notandann sem skráir sig inn í þann kassa.

### <a name="devices"></a>Tæki

Fletting: Smella á **Smásala og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning POS** &gt; **Tæki**. Tæki er eining sem stendur fyrir efnislegt tilvik tækis sem er varpað í afgreiðslukassa. Þegar tæki er stofnað, er það varpað á afgreiðslukassa. Tækjaeiningin rekur upplýsingar um þegar afgreiðslukassi er virkjaður, gerð biðlara sem verið er að nota og forritapakka sem hefur verið virkjað á tiltekna tæki. Tæki geta verið tvenns konar: **Nútíma Retail POS afgreiðslukassar** (MPOS) eða **Sölustaður smásöluskýs** (sölukerfi í skýinu).

#### <a name="mpos"></a>MPOS

MPOS er forrit fyrir POS-biðlara sem er uppsett á Windows 8.1 eða nýrri Stýrikerfum fyrir PC. Ef **Nútíma Retail POS afgreiðslukassar** hugbúnaðargerð er varpað á tæki, er hægt að tilgreina niðurhalspakka fyrir tiltekna tækið. Hægt er að breyta niðurhalspakka til að hafa mismunandi útgáfur af uppsetningarpakka. Getan til að nota mismunandi pakka veitir sveigjanleika í tilfellum þar sem mismunandi afgreiðslukassar þurfa ólíkar samþættingar. MPOS er notað með innbyggt vélbúnaðarstöð.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS er POS fyrir vafra. Þar sem hún er keyrð í vafranum þarf Cloud POS ekki Windows 8.1 eða nýrri stýrikerfi fyrir PC. Ef **Cloud POS fyrir smásölu** hugbúnaðargerð er varpað á tiltekna tæki í bakskrifstofunni, er hægt að nota það tæki í gegnum vafrá án þess að þurfi að setja upp eða hala niður pakka. Cloud POS krefst vélbúnaðarstöð til að nota vélbúnað sem er meiri en bara strikamerkjaskönnun byggt á lyklaborðstengingu.

### <a name="hardware-profile"></a>Vélbúnaðarregla

Fletting: Smella á **Viðskipti** &gt; **Uppsetningu rásar** &gt; **Uppsetning POS** &gt; **Forstillingar POS** &gt; **Vélbúnaðarreglur**. Vélbúnaðarregla tilgreinar vélbúnaðinum sem tengdur er við afgreiðslukassa eða vélbúnaðarstöð. Vélbúnaðarregluna er einnig notuð til að tilgreina færibreytur greiðslumiðlara sem á að nota í samskiptum við þróunartól greiðsluhugbúnaðarins (SDK). (Greiðsu SDK er notuð sem hluti af vélbúnaðarstöðinni).

### <a name="hardware-station"></a>Vélbúnaðarstöð

Fletting: Smellt er á **Smásölu og viðskipti** &gt; **miðlunarleiðir** &gt; **smásöluverslanir** &gt; **allar smásöluverslanir**. Veljið verslun og smellið svo á flipann **vélbúnaðarstöðvar**. Vélbúnaðarstöð er tilvik af viðskiptagrunninn sem keyrir jaðartæki sölustaðar. Vélbúnaðarstöð er sjálfkrafa sett upp ásamt MPOS. Einnig er hægt að setja upp vélbúnaðarstöð sem stakan sjálfstæðan íhlut, og fá aðgagng með MPOS eða Cloud POS í gegnum vefþjónusta. Vélbúnaðarstöð þarf að skilgreina á stigi rásar.

### <a name="hardware-station-profile"></a>Forstilling Hardware Station

Fletting: Smella á **Viðskipti** &gt; **Uppsetningu rásar** &gt; **Uppsetning POS** &gt; **Forstillingar POS** &gt; **Vélbúnaðarstöðvarreglur**. Á meðan vélbúnaðarstöðin sjálf er skilgreind á stigi rásar og tekur einnig til upplýsinga sem tengjast einstökum tilvikum, eins og vefslóð fyrir vélbúnaðarstöð, inniheldur regla vélbúnaðarstöðvar upplýsingar sem geta verið staðbundnar eða samnýttar á milli margra vélbúnaðarstöðva. Staðbundnar upplýsingar innifela gáttina sem á að nota, pakka vélbúnaðarstöðvar, og vélbúnaðarregluna. Staðbundnar upplýsingar innifela einnig lýsingu á gerð vélbúnaðarstöðvar sem er verið að nota, eins og **Útskráningu**eða **Skil**, allt eftir því hvaða vélbúnaður er nauðsynlegur fyrir hverja tiltekna vélbúnaðarstöð.

## <a name="scenarios"></a>Sviðsmyndir
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS með tengda jaðartæki

[![Venjulegt, fastur sölustaður](./media/traditional-300x279.png)](./media/traditional.png) 

Til að tengja MPOS við jaðarbúnað smásölustaðar í hefðbundnu, föstum aðstæðum sölustaðar, farðu fyrst í afgreiðslukassann sjálfan, og úthlutaðu vélbúnaði á hann. Þú getur fundið afgreiðslukassa á **Smásala og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **afgreiðslukassar**. Eftir að vélbúnaðarregluna hefur verið úthlutað skal samstilla breytingar í gagnagrunn rásar með dreifingaráætlun "Afgreiðslukassa". Þú getur fundið dreifingaráætlanir á **Smásölu og viðskipti** &gt; **upplýsingatækni í smásölu** &gt; **dreifingaráætlun**. Næst skal setja upp "staðbundna" vélbúnaðarstöð á rásinni. Smellt er á **Smásölu og viðskipti** &gt; **miðlunarleiðir** &gt; **smásöluverslanir** &gt; **allar smásöluverslanir**. Svo á **vélbúnaðarstöðvar** flýtiflipi, smellið á **Bæta við** til að bæta við vélbúnaðarstöð. Færa inn lýsingu, færa inn **localhost** sem hýsilheiti, og samstilla síðan breytingar á smásölurásar með því að nota dreifingaráætlunina "Skilgreining Rásar". Þú getur fundið dreifingaráætlanir á **Smásölu og viðskipti** &gt; **upplýsingatækni í smásölu** &gt; **dreifingaráætlun**. Að lokum, í MPOS, notið **Velja vélbúnaðarstöð** aðgerð til að velja á **localhost** vélbúnaðarstöð. Stilla vélbúnaðarstöð á **Virkt**. Vélbúnaðarregluna sem notað er í þessum aðstæðum ætti að koma úr afgreiðslukassanum sjálfum. vélbúnaðarreglu er ekki þörf í þessu dæmi. **Athugasemd:** Sumar breytingar á forstillingu vélabúnaðar, eins og breytingar á á peningaskúffur, krefjast þess að ný vakt sé opnuð eftir að breytingar hafa verið samstilltar við rásina. **Athugasemd:** Cloud POS verður að nota sjálfstæða vélbúnaðarstöð til samskipta við jaðartæki í smásölu.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS eða Cloud POS með sjálfstæðri vélbúnaðarstöð
[![Deildur jaðarbúnaður](./media/shared-300x254.png)](./media/shared.png)

Í þessu dæmi er sjálfstæðri vélbúnaðarstöð deilt á meðal MPOS og cloud POS biðlara. Þessar Aðstæðurnar krefjast þess að stofnuð sé vélbúnaðarreglu til að tilgreina niðurhalspakka, gátt, og vélbúnaðarreglu sem vélbúnaðarstöðin notar. Hægt er að finna reglu vélbúnaðarstöðvarinnar á **Smásölu og viðskiptum** &gt; **Rásaruppsetningu** &gt; **Uppsetning sölustaðar** &gt; **Forstilling sölustaðar** &gt; **reglur vélabúnaðarstöðvar**. Eftir að búið er að stofna reglur vélbúnaðarstöðvar, flettu í tiltekna smásölurás (**Smásölu og viðskipti** &gt; **Rásir** &gt; **Smásöluverslanir** &gt; **Allar smásöluverslanir**), og bæta við nýju vélbúnaðarstöðvar. Varpa þessi nýja vélbúnaðarstöð vélbúnaðarregluna sem áður var stofnuð. Næst skal veita lýsingu sem hjálpar gjaldkerinn að tilgreina vélbúnaðarstöð. Í **hýsilheiti** svæðinu, færið inn Vefslóð hýsilvélar með eftirfarandi sniði: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Skipta út **&lt;Vélarheiti:Gátt&gt;** með raunverulega vélarheiti vélbúnaðarstöðvar og gáttinni sem er tiltekin í reglu vélbúnaðarstöðvar.) Fyrir sjálfstæða vélbúnaðarstöð, ætti einnig að tilgreina kenni fyrir rafrænu kortamillifærsluna (EFT). Þetta gildi auðkennir afgreiðslustöð kortamillifærslu sem er tengd við vélbúnaðarstöð þegar greiðslutengillinn hefur samskipti við greiðsluþjónustuaðila. Næst, frá raunverulega vél vélbúnaðarstöðvarinnar, skal fara í rásina, og velja vélbúnaðarstöð. Smellið á **niðurhleðsla**, og setja upp vélbúnaðarstöðina. Næst, úr MPOS eða Cloud POS, skal nota  **Velja vélbúnaðarstöð** aðgerð til að velja vélbúnaðarstöð sem áður var sett upp. Veljið **Para** til að koma á öruggu sambandi á milli sölustaðar og vélbúnaðarstöðvar. Þetta skref verður að ljúka einu sinni fyrir hverja samsetningu Sölustaðar og vélbúnaðarstöðvar. Eftir að vélbúnaðarstöðin er pöruð saman,  er sama aðgerð notuð til að gera vélbúnaðarstöðina virka á meðan hún er notaður. Fyrir þessar aðstæður ætti vélbúnaðarstöðin að vera úthlutuð á reglu vélbúnaðarstöðvar frekar en á afgreiðslukassann sjálfan. Ef af einhverjum ástæðum að vélbúnaðarstöðin hefur ekki vélbúnaðarreglu beint úthlutað, þá er vélbúnaðarreglan sem er úthlutað á afgreiðslukassann notuð.

## <a name="client-maintenance"></a>Viðhald biðlara
### <a name="registers"></a>Afgreiðslukassar

Afgreiðslukassar stjórnað að mestu leyti í gegnum afgreiðslukassa sjálfum og einnig með reglum sem er úthlutað á afgreiðslukassa. Eigindir sem tengjast einstaka afgreiðslukassa er stjórnað á stigi afgreiðslukassa. Eigindirnar taka til verslunarinnar þar sem þeir eru notaðir, númer afgreiðslukassa, lýsingu og í kenni afgreiðslustöðvar KORTAMILLIFÆRSLU sem er tiltekið fyrir afgreiðslukassann sjálfan.

### <a name="pos-profiles"></a>Forstillingar sölustaðar

Hægt er að finna POS-reglur á **Smásölu og viðskiptum** &gt; **Rásaruppsetningu** &gt; **Uppsetning sölustaðar** &gt; **POS-reglur**. Það er gagnlegt til að stjórna mörgum þáttum afgreiðslukassa gegnum forstillingar, þar sem hægt er að deila forstillingar milli marga afgreiðslukassa. Forstillingar má annað hvort varpa á einstaka afgreiðslukassa eða, ef forstillingu er virkt í allri verslun, á smásöluverslun. Eftirfarandi kaflar lýsa forstillingar sölustaðar og hvernig þær eru notaðar.

#### <a name="offline-profile"></a>Ótengt snið

Ótengt snið er stillt á stigi verslana. Hann er notaður til að tilgreina stillingar fyrir upphalsfærslur sem eru framkvæmd á afgreiðslukassa á meðan sem sá afgreiðslukassi er ekki tengdur við gagnagrunn rásar.

#### <a name="functionality-profile"></a>Virkniregla

Virkniforstilling er stillt á stigi verslana. Hann er notaður til að tilgreina stillingar fyrir alla verslun um aðgerðir sem hægt er að framkvæma á Sölustað.  Eftirfarandi virkni er stjórnað með virkniforstillingunni. Þessum möguleikum er raðað með flýtiflipum.

-   Flýtiflipinn **Almennt**
    -   Alþjóðlega staðlastofnunin (ISO)
    -   Stofna viðskiptavin án tengingar
    -   Kvittunarforstilling fyrir tölvupóst
    -   Sannvottun innskráningar lykilstarfsmanna
-   **Aðgerðir** Flýtiflipi:
    -   Stjórnun innskráningar og aukin innskráning.
    -   Þættir tengdir Fjárhag og gjaldmiðli á sölustað, eins og getan til að slá inn verð og hvort aukastafa er krafist fyrir minniháttar gjaldmiðli.
    -   Virkjun tímaskráningar gegnum Sölustað.
    -   Hvernig afurðir og greiðslur birtist á sölustað og á kvittunum.
    -   Stjórnun á Lok vinnudags
    -   Færibreytur fyrir varðveislu gagnagrunnsfærslna rásar.
    -   Hvernig viðskiptavinum er flett upp og stofnaðar úr sölustað.
    -   Hvernig Reiknaður er afsláttur.
-   **Upphæð** flýtiflipi:
    -   Hámarks og lágmarks verð sem eru leyfð.
    -   Notkun Afsláttar og útreikningur.
-   **upplýsingakóðar** flýtiflipi
    -   Allar hliðar á því hvernig upplýsingakóðum eru meðhöndlaðar á Sölustaðnum. Nánari upplýsingar eru í [upplýsingakóðum](info-codes-retail.md).
-   **Kvittananúmer** flýtiflipi´
    -   Tilgreina síur fyrir kvittananúmer, sem gæti innihaldið hluta fyrir verslunarnúmer, númer afgreiðslustöðvar, fasta, og hvort sala, skil, sölupantanir og tilboð skuli prentuð á aðskildum röðum, eða hvort það megi vera í sömu röðinni.

#### <a name="receipt-profiles"></a>Forstillingar innhreyfingar

Kvittunarforstillingar eru tengdar í prentara með vélbúnaðarreglu. Þær eru notaðar til að tilgreina gerðir kvittana sem eru prentaðar á tiltekna prentara. Forstillingar innihalda stillingar fyrir snið kvittunar, og stillingar sem ákvarða hvort kvittunin er alltaf prentuð, eða hvort gjaldkeri er beðinn um að ákveða hvort þarf að prenta kvittunina. Mismunandi prentarar gætu notað mismunandi kvittunarforstillingar. Til dæmis, prentara 1 er stöðluð hitaprentari, og er því með minni snið kvittunar. Hins vegar er prentara 2 kvittanaprentari í fullri stærð sem er notaður til að prenta aðeins kvittanir fyrir pöntun viðskiptavinar, sem krefst meira pláss.

#### <a name="hardware-profiles"></a>Vélbúnaðarreglur

Vélbúnaðarreglur eru útskýrð sem íhlutur fyrir uppsetningu biðlara fyrr í þessum grein. Vélbúnaðarreglur er úthlutað beint á afgreiðslukassa eða vélbúnaðarreglu. Þær eru notaðar til að tilgreina gerðir tækja sem tiltekin afgreiðslukassi eða vélbúnaðarstöð notar. Vélbúnaðarreglur eru einnig notaðar til að tilgreina stillingar KORTAMILLIFÆRSLU sem eru notaðar til að eiga samskipti við greiðslu SDK.

#### <a name="visual-profiles"></a>Sjónrænar reglur

Sjónrænar reglur eru úthlutaðar á stigi afgreiðslukassa. Þær eru notaðar til að tilgreina þema fyrir tiltekinn afgreiðslukassa. Forstillingar innihalda stillingar fyrir þá gerð forrits sem er notuð (MPOS eða Cloud POS) , áherslulitur og þema, leturkerfi, bakgrunnur innskráningar og bakgrunnur sölustaðar.

### <a name="custom-fields"></a>Sérstillt svæði

Hægt er að stofna sérstillt svæði til að bæta við svæðum sem ekki fylgja beint úr kassanum fyrir sölustaðinn. Sjá frekari upplýsingar um hvernig á að nota sérstillt svæði í [Vinna með sérstillt svæði blogg](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Tungumálatexti

Hægt er að hnekkja sjálfgefnum strengir á sölustað með því að nota textafærslur tungumáls. Til að hnekkja streng á sölustað, bæta við nýrri textalínu tungumáls. Tilgreina svo Kenni, sjálfgefna strenginn sem á að hnekkja, og texta sem á að birtast á Sölustað í stað sjálfgefinn streng.

### <a name="hardware-station-profiles"></a>Forstillingar Hardware Station

Reglur vélbúnaðarstöðvar eru útskýrð fyrr í þessum grein. Þær eru notaðar til að úthluta upplýsingum til vélbúnaðarstöðva sem tengjast ekki ákveðnum tilvikum.

### <a name="channel-reports-configuration"></a>Skilgreining skýrslna fyrir rás

Þú setur upp skýrslur sem eru tiltækar á smásölurása á á **forstilling fyrir skýrslur smásölurásar** síðu. Hægt er að stofna nýjar skýrslur með því að veita XML-skilgreiningu fyrir skýrslu og úthluta skýrslunni á tiltekinn heimildaflokk á sölustað.

### <a name="devices"></a>Tæki

Tæki eru útskýrð fyrr í þessum grein. Þær eru notaðar til að stjórna virkjun á tilteknum afgreiðslukassa. Tæki eru einnig notaðar til að tilgreina forrit sem er notað fyrir tiltekinn afgreiðslukassa og uppsetningarpakka sem á að nota til að setja upp MPOS biðlara. Hér eru virkjunarstöður tækis:

-   **Í bið** – tækið er tilbúin til að vera virkjað.
-   **Virkt** – tækið hefur verið gert virkt.
-   **Óvirkt** – tækið hefur verið gert óvirkt, annað hvort í bakvinnslunni eða gegnum Sölustað.
-   **Óvirkur** – tækið hefur verið gerð óvirk.

Viðbótarupplýsingar tengdar virkjun inniheldur starfsmaður sem breytti virkjunarstöðu tækis, tímastimpil fyrir virkjuninni, og hvort grunnstilling tækis hefur verið villuleitað.

### <a name="client-data-synchronization"></a>gagnasamstilling biðlara

Allar breytingar á biðlara Sölustaðar, nema breytingar á virkjunarstöðu tækis, verður að samstilla í gagnagrunn rásar til að taka gildi. Til að samstilla breytingar á gagnagrunni rásar, fara í **Smásölu og viðskipti** &gt; **upplýsingatækni í smásölu** &gt; **dreifingaráætlun**, og keyra nauðsynlega dreifingaráætlun. Vegna Breytinga á biðlaranum, ætti að keyra "afgreiðslukassar" og "skilgreiningu rásar " dreifingaráætlanir.




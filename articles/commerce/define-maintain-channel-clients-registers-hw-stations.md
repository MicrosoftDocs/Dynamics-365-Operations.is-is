---
title: Tengja jaðarbúnað við sölustað (POS)
description: Þessi grein fjallar um hvernig á að tengja jaðartæki við Retail POS þinn.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ffee75e1713c7c9d31b1d023cd055c2f1a3fc43d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897109"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Tengja jaðarbúnað við sölustað (POS)

[!include [banner](includes/banner.md)]

Þessi grein fjallar um hvernig á að tengja jaðartæki við Retail POS þinn.

> [!NOTE]
> Fyrir sérstakar leiðbeiningar um uppsetningu skal sjá [Stilla og setja upp Retail vélbúnaðarstöð](retail-hardware-station-configuration-installation.md) og [Stilla, setja upp og virkja Modern POS (MPOS)](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Lykilþættir

Nokkra þætti eru notaðar til að skilgreina sambönd milli verslunar, afgreiðslukassa á sölustað (POS) eða rásir innan verslunarinnar og jaðartæki sem þessum afgreiðslukassa eða rásir nota til að vinna úr færslum. Þessi hluti lýsir hverjum þætti og útskýrir hvernig nota eigi hann við nýtingu í verslun.

### <a name="pos-registers"></a>Afgreiðslukassar

Leiðsögn: Smelltu á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Afgreiðslukassar**.

Afgreiðslukassi er eining sem er notuð til að skilgreina eiginleika tiltekins tilviks af sölustað. Þessir eiginleikar taka til vélbúnaðarsniðs eða uppsetningar fyrir jaðarbúnað sem verður notað hjá afgreiðslukassanum, verslunina sem afgreiðslukassinn er varpaður á og sjónræna upplifun fyrir notandann sem skráir sig inn í þann kassa.

### <a name="devices"></a>Tæki

Leiðsögn: Smelltu á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Tæki**.

Tæki er eining sem stendur fyrir efnislegt tilvik tækis sem er varpað í afgreiðslukassa. Þegar tæki er stofnað, er það varpað á afgreiðslukassa. Tækjaeiningin rekur upplýsingar um þegar afgreiðslukassi er virkjaður, gerð biðlara sem verið er að nota og forritapakka sem hefur verið virkjað á tiltekna tæki. Tæki geta verið tvenns konar: **Nútíma Retail POS afgreiðslukassar** (MPOS) eða **Sölustaður smásöluskýs** (sölukerfi í skýinu).

#### <a name="mpos"></a>MPOS

MPOS er forrit fyrir POS-biðlara sem er uppsett á Windows 8.1 eða nýrri Stýrikerfum fyrir PC. Ef **Nútíma Retail POS afgreiðslukassar** hugbúnaðargerð er varpað á tæki, er hægt að tilgreina niðurhalspakka fyrir tiltekna tækið. Hægt er að breyta niðurhalspakka til að hafa mismunandi útgáfur af uppsetningarpakka. Getan til að nota mismunandi pakka veitir sveigjanleika í tilfellum þar sem mismunandi afgreiðslukassar þurfa ólíkar samþættingar. MPOS er notað með innbyggt vélbúnaðarstöð.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS er POS fyrir vafra. Þar sem hún er keyrð í vafranum þarf Cloud POS ekki Windows 8.1 eða nýrri stýrikerfi fyrir PC. Ef **Cloud POS fyrir smásölu** hugbúnaðargerð er varpað á tiltekna tæki í Bakvinnslu, er hægt að nota það tæki í gegnum vafrá án þess að þurfi að setja upp eða hala niður pakka. Cloud POS krefst vélbúnaðarstöð til að nota vélbúnað sem er meiri en bara strikamerkjaskönnun byggt á lyklaborðstengingu.

### <a name="hardware-profile"></a>Vélbúnaðarregla

Leiðsögn: Farðu á **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**.

Vélbúnaðarsnið auðkennir vélbúnaðinn sem er tengdur við POS skrá í gegnum samþætta eða sameiginlega vélbúnaðarstöð. Vélbúnaðarregluna er einnig notuð til að tilgreina færibreytur greiðslumiðlara sem á að nota í samskiptum við þróunartól greiðsluhugbúnaðarins (SDK). Greiðslu SDK er notað sem hluti af vélbúnaðarstöðinni.

### <a name="hardware-station"></a>Vélbúnaðarstöð

Leiðsögn: Farðu á **Verslun og verslun \> Rásir \> Búðir \> Allar verslanir**, veldu verslun og veldu síðan **Vélbúnaðarstöðvar** Flýtiflipi.

Vélbúnaðarstöð er tilvik af viðskiptagrunninn sem keyrir jaðartæki sölustaðar. Vélbúnaðarstöð er sjálfkrafa sett upp ásamt MPOS. Einnig er hægt að setja upp vélbúnaðarstöð sem stakan sjálfstæðan íhlut, og fá aðgagng með MPOS eða Cloud POS í gegnum vefþjónusta. Vélbúnaðarstöð þarf að skilgreina á stigi rásar.

## <a name="scenarios"></a>Aðstæður

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS með tengda jaðartæki

[![Venjulegt, fastur sölustaður.](./media/traditional-300x279.png)](./media/traditional.png)

Til að tengja MPOS við jaðarbúnað smásölustaðar í hefðbundnu, föstum aðstæðum sölustaðar, farðu fyrst í afgreiðslukassann sjálfan, og úthlutaðu vélbúnaði á hann. Þú getur fundið afgreiðslukassa á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Afgreiðslukassar**. 

Eftir að vélbúnaðarreglunni hefur verið úthlutað skal samstilla breytingar í gagnagrunn rásar með dreifingaráætlun **Afgreiðslukassa**. Þú getur fundið dreifingaráætlanir á **Retain og Commerce** &gt; **Upplýsingatækni í Retail og Commerce** &gt; **Dreifingaráætlun**. 

Næst skaltu setja upp sérstaka vélbúnaðarstöð á rásinni. Fara til **Verslun og verslun \> Rásir \> Búðir \> Allar verslanir**, og veldu verslun. 

Síðan, á **Vélbúnaðarstöðvar** Flýtiflipi, veldu **Bæta við** að bæta við vélbúnaðarstöð. Veldu **Hollur** sem tegund vélbúnaðarstöðvar, og sláðu síðan inn lýsingu. The **Vélbúnaðarsnið** má skilja reitinn eftir auð, vegna þess að vélbúnaðarsniðið sem er notað í þessari atburðarás kemur frá POS skránni sjálfri. Samstilltu síðan breytingarnar við rásina með því að nota **Rásarstillingar** dreifingaráætlun. Þú getur fundið dreifingaráætlanir á **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**. 

Að lokum, í MPOS, notaðu **Veldu vélbúnaðarstöð** aðgerð til að velja vélbúnaðarstöðina sem passar við gildið sem þú slóst inn áður fyrir lýsinguna og stilltu vélbúnaðarstöðina á **Virkur**. 

> [!NOTE]
> - Sumar breytingar á forstillingu vélabúnaðar, eins og breytingar á peningaskúffum, krefjast þess að ný vakt sé opnuð eftir að breytingar hafa verið samstilltar við rásina.
> - Cloud POS verður að nota sjálfstæða vélbúnaðarstöð til samskipta við jaðartæki.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS eða Cloud POS með sjálfstæðri vélbúnaðarstöð

[![Deildur jaðarbúnaður.](./media/shared-300x254.png)](./media/shared.png)

Í þessari atburðarás er sjálfstæðri vélbúnaðarstöð deilt á milli MPOS og Cloud POS viðskiptavina. Þessi atburðarás krefst þess að þú býrð til sameiginlega vélbúnaðarstöð og tilgreinir niðurhalspakka, gátt og vélbúnaðarsnið sem vélbúnaðarstöðin notar. Þú skilgreinir nýja vélbúnaðarstöð með því að velja **vélbúnaðarstöðvarnar** Flýtiflipi í tiltekinni rás (**Verslun og verslun \> Rásir \> Búðir \> Allar verslanir**) og bæta við nýrri vélbúnaðarstöð af **Samnýtt** tegund. 

Næst skal veita lýsingu sem hjálpar gjaldkerinn að tilgreina vélbúnaðarstöð. Í **hýsilheiti** svæðinu, færið inn vefslóð hýsilvélar á eftirfarandi sniði: `https://<MachineName:Port>/HardwareStation`. (Skipta út **&lt; Vélarheiti: Port&gt;** með raunverulegu heiti vélbúnaðarstöðvarinnar.) Fyrir sjálfstæða vélbúnaðarstöð ættir þú einnig að tilgreina auðkenni rafrænnar millifærslu (EFT) útstöðvar. Þetta gildi auðkennir afgreiðslustöð kortamillifærslu sem er tengd við vélbúnaðarstöð þegar greiðslutengillinn hefur samskipti við greiðsluþjónustuaðila. 

Næst, frá vélinni sem mun hýsa vélbúnaðarstöðina, farðu á rásina í höfuðstöðvum og veldu vélbúnaðarstöðina. Veldu síðan **Sækja** til að hlaða niður vélbúnaðarstöðinni og setja upp vélbúnaðarstöðina. Fyrir frekari upplýsingar um hvernig á að setja upp vélbúnaðarstöð, sjá [Stilltu og settu upp Retail vélbúnaðarstöð](retail-hardware-station-configuration-installation.md). 

Næst, úr MPOS eða Cloud POS, skal nota **Velja vélbúnaðarstöð** aðgerð til að velja vélbúnaðarstöð sem áður var sett upp. Veljið **Para** til að koma á öruggu sambandi á milli sölustaðar og vélbúnaðarstöðvar. Þetta skref verður að ljúka einu sinni fyrir hverja samsetningu Sölustaðar og vélbúnaðarstöðvar. 

Eftir að vélbúnaðarstöðin er pöruð saman, er sama aðgerð notuð til að gera vélbúnaðarstöðina virka á meðan hún er notaður. Fyrir þessa atburðarás ætti að úthluta vélbúnaðarsniðinu við sameiginlegu vélbúnaðarstöðina í stað skrárinnar sjálfrar. Ef ekkert vélbúnaðarsnið er beint úthlutað á vélbúnaðarstöð af einhverjum ástæðum verður vélbúnaðarsniðið sem er úthlutað á skrána notað.

## <a name="client-maintenance"></a>Viðhald biðlara

### <a name="registers"></a>Afgreiðslukassar

Afgreiðslukassar stjórnað að mestu leyti í gegnum afgreiðslukassa sjálfum og einnig með reglum sem er úthlutað á afgreiðslukassa. Eigindir sem tengjast einstaka afgreiðslukassa er stjórnað á stigi afgreiðslukassa. Eigindirnar taka til verslunarinnar þar sem þeir eru notaðir, númer afgreiðslukassa, lýsingu og í kenni afgreiðslustöðvar KORTAMILLIFÆRSLU sem er tiltekið fyrir afgreiðslukassann sjálfan.

### <a name="pos-profiles"></a>Forstillingar sölustaðar

Þú getur fundið reglur afgreiðslukassa á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Forstilling sölustaðar**. Það er gagnlegt til að stjórna mörgum þáttum afgreiðslukassa gegnum forstillingar, þar sem hægt er að deila forstillingar milli marga afgreiðslukassa. Forstillingar má annaðhvort varpa á einstaka afgreiðslukassa eða, ef forstillingu er virkt í allri verslun, á verslun. Eftirfarandi kaflar lýsa forstillingar sölustaðar og hvernig þær eru notaðar.

#### <a name="offline-profile"></a>Ótengt snið

Ótengt snið er stillt á stigi verslana. Hann er notaður til að tilgreina stillingar fyrir upphalsfærslur sem eru framkvæmd á afgreiðslukassa á meðan sem sá afgreiðslukassi er ekki tengdur við gagnagrunn rásar.

#### <a name="functionality-profile"></a>Virkniregla

Virkniforstilling er stillt á stigi verslana. Hann er notaður til að tilgreina stillingar fyrir alla verslun um aðgerðir sem hægt er að framkvæma Í POS. Eftirfarandi virkni er stjórnað með virkniforstillingunni. Þessum möguleikum er raðað með flýtiflipum.

- Flýtiflipinn **Almennt**

    - Alþjóðlega staðlastofnunin (ISO)
    - Stofna viðskiptavin án tengingar
    - Kvittunarforstilling fyrir tölvupóst
    - Sannvottun innskráningar lykilstarfsmanna

- **Aðgerðir** Flýtiflipi:

    - Stjórnun innskráningar og aukin innskráning.
    - Þættir tengdir Fjárhag og gjaldmiðli á sölustað, eins og getan til að slá inn verð og hvort aukastafa er krafist fyrir minniháttar gjaldmiðli.
    - Virkjun tímaskráningar gegnum Sölustað.
    - Hvernig afurðir og greiðslur birtist á sölustað og á kvittunum.
    - Stjórnun á Lok vinnudags
    - Færibreytur fyrir varðveislu gagnagrunnsfærslna rásar.
    - Hvernig viðskiptavinum er flett upp og stofnaðar úr sölustað.
    - Hvernig Reiknaður er afsláttur.

- **Upphæð** flýtiflipi:

    - Hámarks og lágmarks verð sem eru leyfð.
    - Notkun Afsláttar og útreikningur.

- **upplýsingakóðar** flýtiflipi

    - Allar hliðar á því hvernig upplýsingakóðum eru meðhöndlaðar á Sölustaðnum. Nánari upplýsingar er að finna í [Upplýsingakóðar og upplýsingakóðaflokkar](info-codes-retail.md).

- **Kvittananúmer** flýtiflipi´

    - Tilgreindu innhreyfingarnúmeragrímur, sem gætu falið í sér hluta fyrir verslunarnúmer, útstöðvarnúmer, fasta og hvort sala, skil, sölupantanir og tilboð séu prentaðar í aðskildum röðum eða hvort þær fylgja allar sömu röð.

#### <a name="receipt-profiles"></a>Forstillingar kvittunar

Kvittunarsnið er úthlutað til prentara innan vélbúnaðarsniðsins. Þær eru notaðar til að tilgreina gerðir kvittana sem eru prentaðar á tiltekna prentara. Forstillingar innihalda stillingar fyrir snið kvittunar, og stillingar sem ákvarða hvort kvittunin er alltaf prentuð, eða hvort gjaldkeri er beðinn um að ákveða hvort þarf að prenta kvittunina. Mismunandi prentarar gætu notað mismunandi kvittunarforstillingar. Til dæmis, prentara 1 er stöðluð hitaprentari, og er því með minni snið kvittunar. Hins vegar er prentara 2 kvittanaprentari í fullri stærð sem er notaður til að prenta aðeins kvittanir fyrir pöntun viðskiptavinar, sem krefst meira pláss. Fyrir frekari upplýsingar, sjá [Stilltu kvittunarsnið](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Vélbúnaðarreglur

Vélbúnaðarreglur eru útskýrð sem íhlutur fyrir uppsetningu biðlara fyrr í þessum grein. Vélbúnaðarsnið er úthlutað beint á POS skrána eða á sameiginlega vélbúnaðarstöð og eru notuð til að tilgreina gerðir tækja sem ákveðin POS skrá eða vélbúnaðarstöð notar. Vélbúnaðarreglur eru einnig notaðar til að tilgreina stillingar KORTAMILLIFÆRSLU sem eru notaðar til að eiga samskipti við greiðslu SDK.

#### <a name="visual-profiles"></a>Sjónrænar reglur

Sjónræn snið eru notuð til að tilgreina þema fyrir tiltekna skrá og er úthlutað á skráarstigi. Snið inniheldur stillingar fyrir tegund forrits sem er notuð (MPOS eða Cloud POS), hreim lit og þema, leturgerð, bakgrunn innskráningarsíðunnar og POS bakgrunnur. Fyrir frekari upplýsingar, sjá [Búðu til sjónræna snið á sölustað (POS).](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Sérstillt svæði

Hægt er að stofna sérstillt svæði til að bæta við svæðum sem ekki fylgja beint úr kassanum fyrir sölustaðinn. Sjá frekari upplýsingar um hvernig á að nota sérstillt svæði í [Vinna með sérstillt svæði blogg](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Tungumálatexti

Hægt er að hnekkja sjálfgefnum strengir á sölustað með því að nota textafærslur tungumáls. Til að hnekkja streng á sölustað, bæta við nýrri textalínu tungumáls. Tilgreina svo Kenni, sjálfgefna strenginn sem á að hnekkja, og texta sem á að birtast á Sölustað í stað sjálfgefinn streng.

### <a name="channel-reports-configuration"></a>Skilgreining skýrslna fyrir rás

Þú setur upp skýrslur sem eru tiltækar á rásinni á síðunni **Forstilling fyrir skýrslur rásar**. Hægt er að stofna nýjar skýrslur með því að veita XML-skilgreiningu fyrir skýrslu og úthluta skýrslunni á tiltekinn heimildaflokk á sölustað.

### <a name="devices"></a>Tæki

Tæki eru útskýrð fyrr í þessum grein. Þær eru notaðar til að stjórna virkjun á tilteknum afgreiðslukassa. Tæki eru einnig notaðar til að tilgreina forrit sem er notað fyrir tiltekinn afgreiðslukassa og uppsetningarpakka sem á að nota til að setja upp MPOS biðlara. Hér eru virkjunarstöður tækis:

- **Í bið** – tækið er tilbúin til að vera virkjað.
- **Virkt** – tækið hefur verið gert virkt.
- **Óvirkt** – tækið hefur verið gert óvirkt, annaðhvort í Bakvinnslu eða gegnum Sölustað.
- **Óvirkur** – tækið hefur verið gerð óvirk.

Viðbótarupplýsingar tengdar virkjun inniheldur starfsmaður sem breytti virkjunarstöðu tækis, tímastimpil fyrir virkjuninni, og hvort grunnstilling tækis hefur verið villuleitað.

### <a name="client-data-synchronization"></a>gagnasamstilling biðlara

Allar breytingar á biðlara Sölustaðar, nema breytingar á virkjunarstöðu tækis, verður að samstilla í gagnagrunn rásar til að taka gildi. Til að samstilla breytingar á gagnagrunni rásar, fara í **Retail og Commerce** &gt; **Upplýsingatækni í Retail og Commerce** &gt; **Dreifingaráætlun**, og keyra nauðsynlega dreifingaráætlun. Fyrir breytingar á biðlaranum, ætti að keyra dreifingaráætlanir **Afgreiðslukassa** og **Skilgreiningar rásar**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina og setja upp Retail Hardware Station](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

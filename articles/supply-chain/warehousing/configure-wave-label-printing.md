---
title: Prentun bylgjumerkis
description: Þetta efnisatriði lýsir prentun bylgjumerkja og útskýrir hvernig á að setja hana upp.
author: GarmMSFT
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fe04b841dbb3bb237de53f74d73f2b3f9162ae6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840438"
---
# <a name="wave-label-printing"></a>Prentun bylgjumerkis

[!include [banner](../includes/banner.md)]

Prentun bylgjumerkja býður upp á aðra leið til að prenta merki með því að kynna nýja aðferð bylgjuskrefs sem gerir þér kleift að búa til og prenta merki beint úr bylgjusniðmátinu meðan á bylgjuframkvæmd stendur. Þess vegna verða merkin þegar tiltæk áður en starfsmenn keyra verkbeiðnina í fartæki. Starfsmenn geta síðan hengt nauðsynleg merki við meðan tiltekt er í gangi í staðinn fyrir að gera það eftir á.

Prentun bylgjumerkis notar Zebra forritunarmál til að búa til útlit merkja. Útlit merkis skiptist í þrjá hluta (síðuhaus, meginmál og síðufót) til að bjóða upp á merki sem eru með endurtekið skipulag. Sniðmát bylgjumerkja segja kerfinu hvaða útlit merkis á að nota. Notendur geta tilgreint hvaða prentari er notaður. Þeir geta einnig prentað merki á nokkrum prenturum á sama tíma eftir þörfum. Síðan **Ferill bylgjumerkis** sýnir skrá yfir öll merki sem hafa verið búin til með því að nota þessa uppsetningu.

Þú getur flokkað saman merki út frá vinnuhausum, þú getur prentað sundurliðunarmerki fyrir hvern vinnuhaus og þú getur prentað merki fyrir gámainnihald, merkimiða á pakkningar og svipuð merki.

> [!NOTE]
> Þessi virkni kemur ekki í stað núverandi prentunarvirkni merkimiða sem byggir á skjalaleið.

Prentun bylgjumerkis býður upp á eftirfarandi viðbætur:

- Prentaðu merkimiða í samræmi við kassafjölda í einni vinnulínu, án þess að nota gámun. („Kassi“ er eining sem er úthlutað á röðunarflokkslínu einingar.)
- Prentaðu nokkrar mismunandi merkjaraðir (til dæmis merki fyrir kassa og bretti).
- Hafðu með tölusetningu merkis (til dæmis 1/124, 2/124, ... 124/124) og skilgreindu svið tölusetningar (til dæmis vinnulínu, hleðslínu eða sendingu).
- Stofnaðu og prentaðu auðkenni farmbréfs á merki áður en farmbréfið er búið til.
- Búðu til einkvæmt raðnúmer vörusendingar (SSCC) fyrir hvern kassa og láttu það fylgja með hverjum merkimiða.
- Búðu til númeraröð sem fylgir GS1 fyrir auðkenni farmbréfa og raðnúmera vörusendinga.
- Prentaðu aftur merkimiða úr bæði fartækjum og fjölhæfum biðlara.
- Ógiltu merki (til dæmis í stuttum tiltektum) og prentaðu þau aftur.
- Hreinsa feril bylgjumerkis.
- Endurbætur á skipulagi skjalaleiða er deilt á milli skipulags skjalaleiðar og útlits bylgjumerkis. (Frekari upplýsingar er að finna í [Skipulag skjalaleiðar fyrir númeraplötur](../warehousing/document-routing-layout-for-license-plates.md).)

Þessar endurbætur gera það skilvirkara að merkja kassa fyrir röðun á bretti. Þær gagnast sérstaklega fyrirtækjum sem senda til stórra smásala sem staðfesta sjálfkrafa innhreyfingar pantana með því að skanna hvern kassa fyrir sig.

> [!NOTE]
> Þú getur innleitt stillingar atburðarásina sem lýst er í þessu efnisatriði annaðhvort hvort fyrir sig eða í samsetningu, fer allt eftir kröfum fyrirtækisins. Þú getur hannað nokkur sniðmát bylgjumerkis sem virka í röð (eins og sýnt er í atburðarás 3). Til dæmis er hægt að nota atburðarás 1 til að prenta kassamiða og atburðarás 2 til að prenta brettamiða (ef bretti á lager eru mismunandi að stærð og samsetningu).

## <a name="turn-on-the-wave-label-printing-feature"></a>Kveikja á prentunareiginleika bylgjumerkis

Áður en hægt er að nota eiginleikann *Prentun bylgjumerkis* verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Prentun bylgjumerkis*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Atburðarás 1: Prentun bylgjumerkis þar sem eitt bylgjumerki er búið til

Þessi atburðarás sýnir hvernig fyrirtæki getur prentað merkimiða fyrir stóran smásöluaðila sem staðfestir sjálfkrafa innhreyfingar pöntunar með því að skanna hvern kassa fyrir sig.

Þessi atburðarás sýnir verkflæðið frá upphafi til enda.

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Ganga skal úr skugga um að aðferð bylgjumerkis sé tiltæk

Þú gætir þurft að endurgera aðferðir bylgjuferlisins til að gera prentunaraðferð bylgjumerkis tiltæka.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.
1. Staðfestu að **waveLabelPrinting** sé á listanum. Ef svo er ekki skal velja **Endurgera aðferðir** á aðgerðasvæðinu til að bæta því við.

### <a name="configure-a-wave-template"></a>Skilgreina bylgjusniðmát

Bylgjusniðmát leyfa þér að tengja sérstök tilvik af bylgjuaðferðum við samsvarandi sniðmát bylgjumerkis.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Veldu sniðmát, t.d. **62 Sjálfgefin sending**.
1. Í flýtiflipanum **Aðferðir** skal færa aðferðina **Prentun bylgjumerkis** í dálkinn **Valdar aðferðir**.
1. Í dálknum **Valdar aðferðir** skal velja aðferðina **Prentun bylgjumerkis** og stilla reitinn **Kóði bylgjuskrefs** á *PrintLabel*. Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Búa til útlit bylgjumerkis

Útlit merkimiðans stýrir því hvaða upplýsingar eru prentaðar á merkimiðann og hvernig þær eru settar fram. Hér færir þú inn ZPL-kóðann sem er sendur á prentarann.

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Útlit bylgjumerkja**.
1. Búið til færslu sem er með eftirfarandi stillingum:

    - **Útlitskenni merkis:** *Pakki*
    - **Lýsing:** *Pakki (SSCC)*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.

    Síðan **Línustillingar bylgjumerkis** birtist. Hér er hægt að skilgreina breytilega hluta merkingarinnar.

1. Bætið við línu sem er með eftirfarandi stillingum:

    - **Línukenni:** *WaveLabel*
    - **Töfluheiti línu:** *WHSWaveLabel*
    - **Upphafsstaða línu:** *0*

        Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.

    - **Línuhæð:** *0*

        Þessi reitur skilgreinir hæð hverrar línu (í punktum), í samræmi við ZPL-staðalinn. Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða. Fyrst að það er aðeins ein lína í þessu dæmi, er hægt að stilla gildið á *0* (núll).

    - **Línur á síðu:** *1*

        Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.

        > [!NOTE]
        > Þessi uppsetning leiðir til þess að aðskilinn ZPL-merkimiði er prentaður fyrir hverja færslu í töflu bylgjumerkja.

1. Lokið síðunni.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Svæði:** *Gerð vinnu*
    - **Skilyrði:** *Tiltekt*

    Þessi fyrirspurn tryggir að aðeins vinnulínur af tiltektargerð verði prentaðar á merkimiðann, ekki vinnulínur frágangs.

1. Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það.
1. Lokið svarglugga fyrirspurnarritils.
1. Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**. Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus. Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál. Eftirfarandi er dæmi.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót. Eftirfarandi er dæmi.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Þessi uppsetning prentar eitt eintak af hverjum merkimiða. Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf. Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.

Nú er merkimiðinn tilbúinn til notkunar.

### <a name="create-a-wave-label-type"></a>Stofna bylgjusniðmátsgerð

Gerðir bylgjumerkis eru notaðar til að tengja sniðmát bylgjumerkis við einingu í línur röðunarflokkseininga.

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Gerðir bylgjumerkja**.
1. Bætið við gerð bylgjumerkis sem er með eftirfarandi stillingum:

    - **Merkimiðagerð:** *Pakki*
    - **Lýsing:** *Pakki*

### <a name="set-up-unit-sequence-groups"></a>Setja upp röðunarflokka eininga

Næst skal setja upp röðunarflokk einingar fyrir gerð bylgjumerkisins.

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Röðunarflokkar einingar**.
1. Veljið flokkinn **Ea Box PL**.
1. Fyrir línuna **Kassi** skal stilla reitinn **Gerð bylgjustigs** á *Kassi*.

### <a name="create-a-wave-label-template"></a>Stofna sniðmát bylgjumerkis

Næst skal stofna sniðmát bylgjumerkis fyrir gerð bylgjumerkisins.

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Sniðmát bylgjumerkja**.
1. Bætið við bylgjustigssniðmáti og stillið eftirfarandi gildi í hausnum:

    - **Heiti sniðmátsmerkis:** *Merkimiðar kassa*
    - **Lýsing:** *Merkimiðar kassa*
    - **Kóði bylgjuskrefs:** *PrintLabel*
    - **Vöruhús:** *62*

1. Í flýtiflipanum **Almennt** skal stilla reitinn **Gerð bylgjumerkis** á *Kassi*.
1. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við nýrri línu sem er með eftirfarandi stillingum:

    - **Útlitskenni merkis:** *Pakki*
    - **Heiti prentara:** Veljið viðeigandi ZPL-prentara.
    - **Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)

1. Í aðgerðarúðunni skal velja **Vista**.
1. Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**. Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:

    - **Tafla:** *Sendingar*
    - **Afleidd tafla:** *Sendingar*
    - **Reitur:** *Reikningsnúmer*
    - **Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.

    Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils.

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils fyrir allt merkjasniðmát.
1. Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal bæta við línu sem er með eftirfarandi stillingar:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Reitur:** *Tilvísunarkenni hleðslulínu (færslukenni)*
    - **Leitarstefna:** *Hækkandi*

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Skilaboðagluggi biður um að endurstillingaraðgerð flokkunar verði staðfest. Veldu **Já** til að halda áfram.
1. Á aðgerðasvæðinu skal velja **Sniðmátsflokkur bylgjumerkis**.
1. Í svarglugganum **Sniðmátsflokkur bylgjumerkis** skal velja línuna þar sem reiturinn **Heiti tilvísunarreits** er stillt á *Tilvísunarkenni hleðslulínu* og síðan velja gátreitinn **Smíðakenni merkis** fyrir þessa línu.

    > [!NOTE]
    > Þessi uppsetning býr til eina merkimiðaröð („Kassi 1 af X“) fyrir hverja hleðslulínu í gegnum bylgjuna, óháð uppsetningu vinnuflokkunar. Hægt er að prenta þessa röðun merkimiða á útlit merkimiðans.

### <a name="configure-number-sequence-extensions"></a>Skilgreina viðbætur númeraraðar

Viðbætur númeraraðar stjórna GS1-reglufylgni tiltekinna númeraraða. Þessi skilgreining er valfrjáls fyrir núverandi atburðarás. Nánari upplýsingar og leiðbeiningar um skilgreiningar er að finna í [Skilgreina viðbætur númeraraðar](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Stofna sölupöntun og losa hana í vöruhúsið.

1. Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.
1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *62*

1. Bætið við tveimur sölupöntunarlínum sem eru með eftirfarandi stillingum:

    - Sölupöntun lína 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *9024*
        - **Eining:** *ea* (9024 ea = 376 Kassi = 47 PL)

    - Sölupöntun lína 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *9016*
        - **Eining:** *ea* (9016 ea = 322 Kassi = 46 PL)

    > [!NOTE]
    > Vörurnar og magnið sem er gefið upp hér er aðeins notað sem dæmi. Nota verður röðunarflokk einingar sem var skilgreindur áður, viðeigandi umreikninga eininga úr *ea* í *Kassi* í *PL* verður að vera skilgreint fyrir þær og þær að vera með birgðastöðu í vöruhúsi *62*. Frekari upplýsingar er að finna í [Mælieining og birgðareglur](unit-measure-stocking-policies.md).

1. Velja sölupöntunarlínu 1. Því næst skal, í hlutanum **Sölupöntunarlína**, í valmyndinni **Birgðir**, velja **Frátekningar**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** og loka svo síðunni.
1. Endurtakið skref 4 og 5 fyrir sölupöntunarlínu 2.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Eftirfarandi tilvik gerast:

    - Kerfið vinnur úr stofnaðri sendingu með því að nota sniðmátið sem felur í sér prentunarstig merkisins. Útlit merkisins verður notað til að skilgreina snið merkisins og niðurstaðan verður merki sem prentað er á prentara sem valinn er í sniðmáti merkis.
    - Bylgjumerki eru búin til og prentuð. Fjöldi merkimiða verður sá sami og kassafjöldinn (í þessu dæmi, 376 kassamerki fyrir línu 1 og 322 kassamerki fyrir línu 2).
    - Nýtt auðkenni farmbréfs er búið til fyrir sendingarnar. Ef þú skilgreindir viðbætur númeraraðarinnar mun auðkenni bylgjumerkis fylgja **SSCC-18** númerasniðinu. 

Hægt er að skoða og endurprenta bylgjumerki á eftirfarandi síðum. Á aðgerðasvæði hverrar síðu, í flipanum **Sendingar**, í flokknum **Tengdar upplýsingar**, skal velja **Bylgjumerki**.

- Allar sendingar \> Upplýsingar sendingar
- Allar hleðslur \> Upplýsingar um hleðslu
- Allar bylgjur
- Bylgjumerki
- Ferill bylgjumerkis

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Atburðarás 2: Prentun bylgjumerkis fyrir gámun (án færslna bylgjumerkis)

Þessi atburðarás gerir þér kleift að prenta bylgjumerki þegar þú notar gámun til að sjálfkrafa skipta upp vörum í kassa og þarf þar af leiðandi ekki færslu bylgjumerkis. Í þessu tilfelli virkar gámakennið sem staðgengill fyrir SSCC.

Hér er helsti munurinn á þessari atburðarás og atburðarás 1:

- **Sniðmát bylgjumerkja:** Ekki er valin gerð bylgjumerkis í sniðmáti bylgjumerkis og ekki þarf flokkun merkjasmíðar. Annars verður sniðmát bylgjumerkis skilgreint og tengt við bylgjusniðmátið á sama hátt og lýst er í atburðarás 1. Skilja verður gerð bylgjumerkis eftir autt til að koma í veg fyrir bylgjumerki verði búin til.
- **Útlit bylgjumerkja:** Þú munt skilgreina stillingar línuútlits bylgjumerkis fyrir vinnulínur í staðinn fyrir færslur bylgjumerkis. Skilgreina verður línustillinguna fyrir útlit merkis með því að nota töfluna **WHSWorkLine** í staðinn fyrir töfluna **WHSWaveLabel**. Stillingin **Línur á síðu** stjórnar fjölda lína sem verða í meginmálinu. 

Þessi skilgreining er einnig hentug fyrir atburðarásir fyrirtækis þar sem margvíslegar vörur eru pakkaðar í einn merktan kassa eða raðað á bretti og þetta pökkunarferli er hægt að skilgreina eftir vinnustofnun (t.d. vinna sem er flokkuð eftir sendingu).

Þessi atburðarás sýnir verkflæðið frá upphafi til enda.

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Ganga skal úr skugga um að aðferð bylgjumerkis sé tiltæk

Þú gætir þurft að endurgera aðferðir bylgjuferlisins til að gera prentunaraðferð bylgjumerkis tiltæka.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.
1. Staðfestu að **waveLabelPrinting** sé á listanum. Ef svo er ekki skal velja **Endurgera aðferðir** á aðgerðasvæðinu til að bæta því við.

### <a name="set-up-a-wave-template"></a>Velja bylgjusniðmát

Bylgjusniðmát leyfa þér að tengja sérstök tilvik af bylgjuaðferðum við samsvarandi sniðmát bylgjumerkis.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Veljið sniðmát, t.d. **63 Gámun**.
1. Í flýtiflipanum **Aðferðir** skal færa aðferðina **Prentun bylgjumerkis** í dálkinn **Valdar aðferðir**.
1. Í dálknum **Valdar aðferðir** skal velja aðferðina **Prentun bylgjumerkis** og stilla reitinn **Kóði bylgjuskrefs** á *PrintLabel*. Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Búa til útlit bylgjumerkis

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Útlit bylgjumerkja**.
1. Búið til færslu sem er með eftirfarandi stillingum:

    - **Útlitskenni merkis:** *Pakki*
    - **Lýsing:** *Pakki (SSCC)*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.

    Síðan **Línustillingar bylgjumerkis** birtist. Hér er hægt að skilgreina breytilega hluta merkingarinnar.

1. Bætið við línu sem er með eftirfarandi stillingum:

    - **Línukenni:** *WorkLine*
    - **Töfluheiti línu:** *WHSWorkLine*
    - **Upphafsstaða línu:** *500*

        Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.

    - **Línuhæð:** *-50*

        Þessi reitur skilgreinir hæð hverrar raðar. Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða.

    - **Línur á síðu:** *5*

        Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.

        > [!NOTE]
        > Þessi uppsetning prentar nokkur ZPL-merki á hverja vinnu þar sem hver síða getur innihaldið allt að fimm vinnulínur. Til dæmis, ef merkimiði er prentaður fyrir gám sem hefur 12 línur, verða þrír merkimiðar prentaðir. Ef þú vilt prenta sérstaka merkimiða fyrir hverja tiltektarlínu skaltu stilla þetta gildi á *1*.

1. Lokið síðunni.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Svæði:** *Gerð vinnu*
    - **Skilyrði:** *Tiltekt*

1. Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það.
1. Lokið svarglugga fyrirspurnarritils.
1. Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**. Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus. Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál. Eftirfarandi er dæmi.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót. Eftirfarandi er dæmi.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Þessi uppsetning prentar eitt eintak af hverjum merkimiða. Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf. Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.

Nú er merkimiðinn tilbúinn til notkunar.

### <a name="create-a-wave-label-template"></a>Stofna sniðmát bylgjumerkis

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Sniðmát bylgjumerkja**.
1. Bætið við bylgjustigssniðmáti og stillið eftirfarandi gildi í hausnum:

    - **Heiti á sniðmáti merkis:** *Merkimiðar gáms*
    - **Lýsing:** *Merkimiðar gáms*
    - **Kóði bylgjuskrefs:** *PrintLabel*
    - **Vöruhús:** *63*

1. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við línu sem er með eftirfarandi stillingum:

    - **Útlitskenni merkis:** *Gámur*
    - **Heiti prentara:** Veljið viðeigandi ZPL-prentara.
    - **Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)

1. Í aðgerðarúðunni skal velja **Vista**.
1. Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**. Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:

    - **Tafla:** *Sendingar*
    - **Afleidd tafla:** *Sendingar*
    - **Reitur:** *Reikningsnúmer*
    - **Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.

    Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils.

### <a name="configure-number-sequence-extensions"></a>Skilgreina viðbætur númeraraðar

Viðbætur númeraraðar stjórna GS1-reglufylgni tiltekinna númeraraða. Þessi skilgreining er valfrjáls fyrir núverandi atburðarás. Nánari upplýsingar og leiðbeiningar um skilgreiningar er að finna í [Skilgreina viðbætur númeraraðar](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Stofna sölupöntun og losa hana í vöruhúsið.

1. Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.
1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *63*

1. Bæta við fimm sölupöntunarlínum::

    - Sölupöntun lína 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *10*

    - Sölupöntun lína 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *20*

    - Sölupöntun lína 3:

        - **Vörunúmer:** *L0006*
        - **Magn:** *20*

    - Sölupöntun lína 4:

        - **Vörunúmer:** *L0100*
        - **Magn:** *40*

    - Sölupöntun lína 5:

        - **Vörunúmer:** *L0101*
        - **Magn:** *50*

    > [!NOTE]
    > Vörurnar og magnið sem er gefið upp hér er aðeins notað sem dæmi. Þær verða að hafa birgðir í tilgreindu vöruhúsi.

1. Velja sölupöntunarlínu 1. Því næst skal, í hlutanum **Sölupöntunarlína**, í valmyndinni **Birgðir**, velja **Frátekningar**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** og loka svo síðunni.
1. Endurtakið skref 4 og 5 fyrir hverja sölupöntunarlínu.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Eftirfarandi tilvik gerast:

    - Kerfið vinnur úr stofnaðri sendingu með því að nota sniðmátið sem felur í sér prentunarstig merkisins. Útlit merkisins verður notað til að skilgreina snið merkisins og lokaniðurstaðan verður merki með fimm línum sem prentað er á prentara sem valinn er í sniðmáti merkis.
    - Nýtt auðkenni farmbréfs er búið til fyrir sendingarnar. Ef þú skilgreindir viðbætur númeraraðarinnar mun auðkenni bylgjumerkis fylgja **SSCC-18** númerasniðinu. 

Hægt er að endurprenta þessi bylgjumerki með því að fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Ferill bylgjumerkis**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Atburðarás 3: Prentun bylgjumerkis fyrir merki með mörg lög

Þessi atburðarás sýnir hvernig nota á prentunarvirkni bylgjumerkis þegar vöruhúsaferlin krefjast margra laga af merkimiðum. Til dæmis gæti þurft að prenta sérstaka merkimiða fyrir kassa og bretti og hugsanlega þarf að prenta sundurliðunarmerki fyrir heila sendingu. Sundurliðunarmerki eru sérstök gerð af merkimiða sem hægt er að nota til að skilja í sundur rúllur og gáma, t.d. merkimiða fyrir sendingarkennið og strikamerki, þannig að hægt sé að raða merkimiðunum auðveldlega eftir að þeir hafa verið prentaðir.

Helsti munurinn á skilgreiningu þessarar atburðarásar og skilgreiningar atburðarásar 1, fyrir utan þá staðreynd að sundurliðunarmerki eru virkjuð, er sá að margar gerðir bylgjumerkis verða að tengjast sniðmátum bylgjumerkja og línum röðunarflokkseininga. Til að ná fram þessari skilgreiningu þarf að setja upp eftirfarandi þætti fyrir þessa atburðarás:

- **Aðferðir bylgjuúrvinnslu:** Þú merkir aðferð bylgjumerkis sem „endurtakanleg,“ bætir henni tvisvar sinnum (eða oftar) við bylgjusniðmátið og stillir ólíka bylgjuskrefakóða.
- **Sniðmát bylgjumerkja:** Þú skilgreinir sniðmát bylgjumerkja og tengir þau við bylgjusniðmátið. Hvert sniðmát bylgjumerkis er með sína eigin gerð af bylgjumerki.
- **Útlit bylgjumerkja:** Þú býrð til mörg útlit bylgjumerkis. Það verður sérstakt merkimiðaútlit fyrir hvert „lag“ af merkimiðum og það verður einnig útlit sundurliðunarmerkis.

Þessi atburðarás sýnir verkflæðið frá upphafi til enda.

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.

### <a name="set-up-a-wave-process-method"></a>Setja upp aðferð bylgjuúrvinnslu

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.
1. Staðfestu að **waveLabelPrinting** sé á listanum. Ef svo er ekki skal velja **Endurgera aðferðir** á aðgerðasvæðinu til að bæta því við.
1. Fyrir aðferðina **waveLabelPrinting** skal velja gátreitinn **Gera aðferð þannig að unnt sé að endurtaka hana**.

### <a name="set-up-a-wave-template"></a>Velja bylgjusniðmát

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
2. Veldu sniðmát, t.d. **62 Sjálfgefin sending**.
3. Í flýtiflipanum **Aðferðir** skal færa aðferðina **Prentun bylgjumerkis** í dálkinn **Valdar aðferðir**.
4. Í dálknum **Valdar aðferðir** skal úthluta gildi **Bylgjuskrefakóða**, t.d. *Kassi*, á aðferðina **Prentun bylgjumerkis**. Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).
5. Færið aðferðina **Prentun bylgjumerkis** yfir í dálkinn **Valdar aðferðir** í annað skiptið.
6. Í dálknum **Valdar aðferðir** skal úthluta öðru gildi **Bylgjuskrefakóða**, t.d. *Bretti*, á aðra aðferð **Prentun bylgjumerkis**. Frekari upplýsingar um bylgjuskrefakóða er að finna í [Kóðar bylgjuskrefs](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Stofna þrenns konar útlit bylgjumerkis

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Útlit bylgjumerkja**.
1. Búið til færslu sem er með eftirfarandi stillingum:

    - **Útlitskenni merkis:** *Pakki*
    - **Lýsing:** *Pakki (SSCC)*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.

    Síðan **Línustillingar bylgjumerkis** birtist. Hér er hægt að skilgreina breytilega hluta merkingarinnar.

1. Bætið við línu sem er með eftirfarandi stillingum:

    - **Línukenni:** *WaveLabel*
    - **Töfluheiti línu:** *WHSWaveLabel*
    - **Upphafsstaða línu:** *0*

        Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.

    - **Línuhæð:** *0*

        Þessi reitur skilgreinir hæð hverrar línu (í punktum), í samræmi við ZPL-staðalinn. Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða. Fyrst að það er aðeins ein lína í þessu dæmi, er hægt að stilla gildið á *0* (núll).

    - **Línur á síðu:** *1*

        Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.

        > [!NOTE]
        > Þessi uppsetning leiðir til þess að aðskilinn ZPL-merkimiði er prentaður fyrir hverja færslu í töflu bylgjumerkja.

1. Lokið síðunni.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Svæði:** *Gerð vinnu*
    - **Skilyrði:** *Tiltekt*

    Þessi fyrirspurn tryggir að aðeins vinnulínur af tiltektargerð verði prentaðar á merkimiðann, ekki vinnulínur frágangs.

1. Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það. 
1. Lokið svarglugga fyrirspurnarritils.
1. Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**. Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus. Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál. Eftirfarandi er dæmi.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót. Eftirfarandi er dæmi.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Þessi uppsetning prentar eitt eintak af hverjum merkimiða. Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf. Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.

1. Nú er fyrsti merkimiðinn tilbúinn til notkunar.
1. Búið til aðra útlitsfærslu sem er með eftirfarandi stillingar:

    - **Útlitskenni merkis:** *Bretti*
    - **Lýsing:** *Bretti*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Línustillingar bylgjumerkis**.

    Síðan **Línustillingar bylgjumerkis** birtist. Hér er hægt að skilgreina breytilega hluta merkingarinnar.

1. Bætið við línu sem er með eftirfarandi stillingum:

    - **Línukenni:** *WaveLabel*
    - **Töfluheiti línu:** *WHSWaveLabel*
    - **Upphafsstaða línu:** *0*

        Þessi reitur skilgreinir lóðréttu stöðuna þar sem línan byrjar á merkimiðanum.

    - **Línuhæð:** *0*

        Þessi reitur skilgreinir hæð hverrar línu (í punktum), í samræmi við ZPL-staðalinn. Hæð línunnar er jákvæð fyrir lárétta merkimiða og neikvæð fyrir lóðrétta merkimiða. Fyrst að það er aðeins ein lína í þessu dæmi, er hægt að stilla gildið á *0* (núll).

    - **Línur á síðu:** *1*

        Þessi reitur skilgreinir fjölda lína sem hægt er að prenta á hvern merkimiða.

        > [!NOTE]
        > Þessi uppsetning leiðir til þess að sérstakur ZPL-merkimiði er prentaður fyrir hverja færslu í töflu bylgjumerkja.

1. Lokið síðunni.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils á flipanum **Svið** skal bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Svæði:** *Gerð vinnu*
    - **Skilyrði:** *Tiltekt*

    Þessi fyrirspurn tryggir að aðeins vinnulínur af tiltektargerð verði prentaðar á merkimiðann, ekki vinnulínur frágangs.

1. Ef ætlunin er að geta prentað auðkenni farmbréfsins, skal í flipanum **Samtengingar** velja töfluna **Vinnulínur** og tengja töfluna **Sendingar** við það.
1. Lokið svarglugga fyrirspurnarritils.
1. Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**. Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn kóða fyrir nauðsynlegan síðuhaus. Ef til dæmis Zebra-prentari er notaður er hægt að nota eftirfarandi kóða.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Í hlutanum **Hluti meginmáls**, í reitinn **Meginmál merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegt meginmál. Eftirfarandi er dæmi.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. Í hlutanum **Hluti síðufóts**, í reitinn **Síðufótur merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðufót. Eftirfarandi er dæmi.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Þessi uppsetning prentar eitt eintak af hverjum merkimiða. Ef þörf er á fleiri eintökum (til dæmis eitt eintak fyrir hverja hlið brettisins) skal stilla gildið **n** fyrir hlutann **\^PQn** í síðufætinum á þann fjölda eintaka sem þarf. Til dæmis, til að prenta fjögur eintök af hverjum merkimiða skal gefa upp **\^PQ4**.

1. Nú er næsti merkimiði tilbúinn til notkunar.
1. Búið til þriðju útlitsfærslu sem er með eftirfarandi stillingar:

    - **Útlitskenni merkis:** *Sundurliðun*
    - **Lýsing:** *Sundurliðunarmerki*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Í flýtiflipanum **Textaútlit prentara** eru þrír hlutar þar sem hægt er að skrifa prentarakóða: **Hluti síðuhauss**, **Hluti meginmáls** og **Hluti síðufóts**. Í hlutanum **Hluti síðuhauss**, í reitinn **Síðuhaus merkis**, skal færa inn ZPL-kóða fyrir nauðsynlegan síðuhaus. Eftirfarandi er dæmi.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Að þessu sinni er ekki þörf á meginmáli. Færið þess vegna nauðsynlegan texta inn í hlutann **Hluti síðufóts**. Eftirfarandi er dæmi.

    ```plaintext
    ^XZ
    ```

    Nú er þriðji merkimiðinn tilbúinn til notkunar.

    > [!NOTE]
    > Þessi þriðji merkimiði er sundurliðunarmerki sem verður notað til að aðskilja rúllur.

### <a name="create-two-wave-label-types"></a>Búa til tvær gerðir bylgjumerkis

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Gerðir bylgjumerkja**.
1. Búið til færslu sem er með eftirfarandi stillingum:

    - **Merkimiðagerð:** *Pakki*
    - **Lýsing:** *Pakki*

1. Búið til aðra færslu sem er með eftirfarandi stillingum:

    - **Merkimiðagerð:** *Bretti*
    - **Lýsing:** *Bretti*

### <a name="set-up-unit-sequence-groups"></a>Setja upp röðunarflokka eininga

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Röðunarflokkar einingar**.
1. Veljið eða stofnið flokk **Ea Kassi PL**.
1. Fyrir línuna **Kassi** skal stilla reitinn **Gerð bylgjustigs** á *Kassi*.
1. Fyrir línuna **PL** skal stilla reitinn **Gerð bylgjustigs** á *Bretti*.

### <a name="create-wave-label-templates"></a>Stofna sniðmát bylgjumerkja

1. Fara skal í **Vöruhúsakerfi \> Uppsetning \> Skjalasendingar \> Sniðmát bylgjumerkja**.
1. Stofna sniðmát merkimiða sem er með eftirfarandi stillingum:

    - **Heiti sniðmátsmerkis:** *Merkimiðar kassa*
    - **Lýsing:** *Merkimiðar kassa*
    - **Kóði bylgjuskrefs:** *Pakki*
    - **Vöruhús:** *62*

1. Í flýtiflipanum **Almennt**, í reitnum **Gerð bylgjumerkis**, skal velja gildi á borð við *Kassi*.
1. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við línu sem er með eftirfarandi stillingum:

    - **Útlitskenni merkis:** *Pakki*
    - **Heiti prentara:** Veljið viðeigandi ZPL-prentara.
    - **Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)

1. Í aðgerðarúðunni skal velja **Vista**.
1. Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**. Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:

    - **Tafla:** *Sendingar*
    - **Afleidd tafla:** *Sendingar*
    - **Reitur:** *Reikningsnúmer*
    - **Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.

    Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils.

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils fyrir allt merkjasniðmát.
1. Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal bæta við línu sem er með eftirfarandi stillingar:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Reitur:** *Tilvísunarkenni hleðslulínu (færslukenni)*
    - **Leitarstefna:** *Hækkandi*

1. Bætið við annarri línu sem er með eftirfarandi stillingum:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Reitur:** *Auðkenni sendingar*
    - **Leitarstefna:** *Hækkandi*

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Skilaboðagluggi biður um að endurstillingaraðgerð flokkunar verði staðfest. Veldu **Já** til að halda áfram.
1. Á aðgerðasvæðinu skal velja **Sniðmátsflokkur bylgjumerkis**.
1. Í svarglugganum **Sniðmátsflokkur bylgjumerkis**, fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stilltur á *Auðkenni sendingar*, skal stilla eftirfarandi gildi:

    - **Prenta sundurliðunarmerki:** Veljið þennan gátreit.
    - **Útlitskenni merkis:** Veljið sundurliðunarmerki. (Til dæmis velja merkjaútlitið *Sundurliðun* sem búið var til fyrr í þessari atburðarás.)
    - **Heiti prentara:** Veljið prentarann fyrir sundurliðunarmerkið. (Venjulega, í þeim tilgangi að skipta niður merkimiðarúllum, ætti að velja sama prentarann og er valinn í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis**. Hins vegar eru aðrar atburðarásir mögulegar.)

1. Fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stillt á *Tilvísunarkenni hleðslulínu* skal velja gátreitinn **Smíðakenni merkis**.

    > [!NOTE]
    > Þessi uppsetning býr til eina merkimiðaröð („Kassi 1 af X“) fyrir hverja hleðslulínu í gegnum bylgjuna, óháð uppsetningu vinnuflokkunar. Hægt er að prenta þessa númeraröð merkimiða á útlit merkimiða. Að auki verða merkimiðar fyrir mismunandi sendingar aðskildir með völdum sundurliðunarmiða.

1. Smellið á **Í lagi** til að loka svarglugganum **Sniðmátsflokkur bylgjumerkis**.
1. Búið til annað sniðmát merkimiða sem er með eftirfarandi stillingum:

    - **Heiti á sniðmáti merkis:** *Brettamiðar*
    - **Lýsing:** *Merkimiðar brettis*
    - **Kóði bylgjuskrefs:** *Bretti*
    - **Vöruhús:** *62*

1. Í flýtiflipanum **Almennt**, í reitnum **Gerð bylgjumerkis**, skal velja gildi á borð við *Bretti*.
1. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal bæta við línu sem er með eftirfarandi stillingum:

    - **Útlitskenni merkis:** *Bretti*
    - **Heiti prentara:** Veljið viðeigandi ZPL-prentara.
    - **Keyra fyrirspurn:** *Já* (Þessi stilling er valfrjáls, en mælt er með henni til að hámarka afköst.)

1. Í aðgerðarúðunni skal velja **Vista**.
1. Valfrjálst: Ef verið er að setja upp merkimiða sem hannaður er með ákveðinn viðskiptavin í huga, þarf að búa til fyrirspurn til að finna lykil viðskiptavinarins. Í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis** skal velja **Breyta fyrirspurn**. Því næst, í svarglugga fyrirspurnarritils í flipanum **Svið**, skal bæta við línu sem er með eftirfarandi stillingar:

    - **Tafla:** *Sendingar*
    - **Afleidd tafla:** *Sendingar*
    - **Reitur:** *Reikningsnúmer*
    - **Skilyrði:** Sláið inn viðeigandi númer viðskiptavinalykils.

    Þegar því er lokið skal velja **Í lagi** til að loka svarglugga fyrirspurnarritils. 

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils fyrir allt merkjasniðmát.
1. Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal bæta við línu sem er með eftirfarandi stillingar:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Reitur:** *Tilvísunarkenni hleðslulínu (færslukenni)*
    - **Leitarstefna:** *Hækkandi*

1. Bætið við annarri línu sem er með eftirfarandi stillingum:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Reitur:** *Auðkenni sendingar*
    - **Leitarstefna:** *Hækkandi*

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Skilaboðagluggi biður um að endurstillingaraðgerð flokkunar verði staðfest. Veldu **Já** til að halda áfram.
1. Á aðgerðasvæðinu skal velja **Sniðmátsflokkur bylgjumerkis**.
1. Í svarglugganum **Sniðmátsflokkur bylgjumerkis**, fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stilltur á *Auðkenni sendingar*, skal stilla eftirfarandi gildi:

    - **Prenta sundurliðunarmerki:** Veljið þennan gátreit.
    - **Útlitskenni merkis:** Veljið sundurliðunarmerki. (Til dæmis velja merkjaútlitið *Sundurliðun* sem búið var til fyrr í þessari atburðarás.)
    - **Heiti prentara:** Veljið prentarann fyrir sundurliðunarmerkið. (Venjulega, í þeim tilgangi að skipta niður merkimiðarúllum, ætti að velja sama prentarann og er valinn í flýtiflipanum **Sniðmátsupplýsingar bylgjumerkis**. Hins vegar eru aðrar atburðarásir mögulegar.)

1. Fyrir línuna þar sem reiturinn **Heiti tilvísunarreits** er stillt á *Tilvísunarkenni hleðslulínu* skal velja gátreitinn **Smíðakenni merkis**.

    > [!NOTE]
    > Þessi uppsetning býr til eina merkimiðaröð („Kassi 1 af X“) fyrir hverja hleðslulínu í gegnum bylgjuna, óháð uppsetningu vinnuflokkunar. Hægt er að prenta þessa númeraröð merkimiða á útlit merkimiða. Að auki verða merkimiðar fyrir mismunandi sendingar aðskildir með völdum sundurliðunarmiða.

### <a name="configure-number-sequence-extensions"></a>Skilgreina viðbætur númeraraðar

Viðbætur númeraraðar stjórna GS1-reglufylgni tiltekinna númeraraða. Þessi skilgreining er valfrjáls fyrir núverandi atburðarás. Nánari upplýsingar og leiðbeiningar um skilgreiningar er að finna í [Skilgreina viðbætur númeraraðar](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Stofna sölupöntun og losa hana í vöruhúsið.

1. Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.
1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *62*

1. Bæta við tveimur sölupöntunarlínum:

    - Sölupöntun lína 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *9024*
        - **Eining:** *ea* (9024 ea = 376 Kassi = 47 PL)

    - Sölupöntun lína 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *9016*
        - **Eining:** *ea* (9016 ea = 322 Kassi = 46 PL)

    > [!NOTE]
    > Vörurnar og magnið sem er gefið upp hér er aðeins notað sem dæmi. Nota verður röðunarflokk einingar sem var skilgreindur áður, viðeigandi umreikninga eininga úr *ea* í *Kassi* í *PL* verður að vera skilgreint fyrir þær og þær að vera með birgðastöðu í vöruhúsi *62*. Frekari upplýsingar er að finna í [Mælieining og birgðareglur](unit-measure-stocking-policies.md).

1. Velja sölupöntunarlínu 1. Því næst skal, í hlutanum **Sölupöntunarlína**, í valmyndinni **Birgðir**, velja **Frátekningar**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** og loka svo síðunni.
1. Endurtakið skref 4 og 5 fyrir sölupöntunarlínu 2.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Eftirfarandi tilvik gerast: 

    - Kerfið vinnur úr stofnaðri sendingu með því að nota sniðmátið sem felur í sér prentunarstig merkisins. Útlit merkisins verður notað til að skilgreina snið merkisins og niðurstaðan verður merki sem prentað er á prentara sem valinn er í sniðmáti merkis.
    - Bylgjumerki eru búin til og prentuð. Fjöldi merkimiða verður sá sami og kassafjöldinn (í þessu dæmi, 376 kassamerki fyrir línu 1 og 322 kassamerki fyrir línu 2, 47 PL-miðar fyrir línu 1, 47 PL-miðar fyrir línu 2 og tveir sundurliðunarmiðar sem eru með auðkenni sendingarinnar).
    - Nýtt auðkenni farmbréfs er búið til fyrir sendingarnar. Ef þú skilgreindir viðbætur númeraraðarinnar mun auðkenni bylgjumerkis fylgja **SSCC-18** númerasniðinu. 

Hægt er að skoða og endurprenta bylgjumerki á eftirfarandi síðum:

- Allar sendingar \> Upplýsingar sendingar
- Allar hleðslur \> Upplýsingar um hleðslu
- Allar bylgjur
- Bylgjumerki
- Ferill bylgjumerkis

Fyrir flestar af þessum síðum er hægt að finna viðeigandi virkni með því að velja **Bylgjumerki** í flokknum **Tengdar upplýsingar** í flipanum **Sendingar** á aðgerðasvæðinu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Endurprenta og ógilda bylgjumerki](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
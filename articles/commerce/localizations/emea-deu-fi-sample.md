---
title: Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Þýskaland
description: Þetta efni veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Þýskaland í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 65315a9fd6bc1af26bc225220e096aee4da09be2
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388160"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Þýskaland

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Þetta efni veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Þýskaland í Microsoft Dynamics 365 Commerce.

Til að uppfylla staðbundnar fjárhagslegar kröfur fyrir sjóðvélar í Þýskalandi, er Microsoft Dynamics 365 Commerce virkni fyrir Þýskaland felur í sér sýnishorn af samþættingu sölustaðarins (POS) við ytri skattskráningarþjónustu. Sýnið framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Það er byggt á [EFR (rafræn ríkisfjármálaskrá)](https://www.efsta.eu/de/fiskalloesungen/deutschland) lausn frá [EFSTA](https://www.efsta.eu/de/) og gerir samskipti við EFR þjónustuna í gegnum HTTPS samskiptareglur. EFR þjónustan ætti að vera hýst annað hvort á Retail Hardware stöðinni eða sérstakri tölvu sem hægt er að tengja við frá Vélbúnaðarstöðinni. Sýnishornið er gefið í formi frumkóða og er hluti af Retail hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá EFSTA. Fyrir upplýsingar um hvernig á að fá EFR lausnina og reka hana, hafðu samband [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Sviðsmyndir

Eftirfarandi aðstæður falla undir samþættingarúrtak ríkisskráningarþjónustu fyrir Þýskaland.

### <a name="sales-operations"></a>Söluaðgerðir

- **Skráning staðgreiðslusölu og skila í skattskráningarþjónustu:**

    Skráning á sölustarfsemi felur í sér eftirfarandi skref:

    1. Skráning viðskipta hefst

        Upphaf hvers viðskipta er skráð í tæknilega öryggisþátt (TSE) sem er tengdur EFR þjónustunni. Sem afleiðing af skráningu úthlutar TSE viðskiptakenni (TID).

    2. Skráningu viðskipta lýkur

        Þegar færslu er lokið á POS er hún skráð með því að nota sama TID og var úthlutað við skráningu færslunnar. Á því augnabliki eru ítarleg færslugögn send til ríkisskráningarþjónustunnar. Þessi gögn innihalda upplýsingar um sölulínur og upplýsingar um afslætti, greiðslur og skatta.

    3. Sækja svar frá skattaskráningarþjónustunni

        Öryggisgögn berast frá TSE sem hluti af svari og eru vistuð í viðskiptunum í rásargagnagrunninum. Öryggisgögnin samanstanda af eftirfarandi upplýsingum:

        - TID
        - Dagsetning og tími þegar viðskiptin hefjast
        - Dagsetning og tími viðskiptaloka
        - Undirskriftarteljari
        - Athugaðu gildi
        - Raðnúmer TSE

- **Skráning pantana viðskiptavina í ríkisskráningarþjónustu:** Skráningarferlið er það sama og ferlið fyrir staðgreiðslusölu og skil.
- **Skráning starfsemi sem felur í sér gjafakort og innborgun:** Skráningarferlið er það sama og ferlið fyrir staðgreiðslusölu og skil.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Að tilkynna notendum um bilanir í fjárhagsskráningu

Það eru tvær leiðir sem fjárhagsskráningarþjónustan getur tilkynnt notendum um bilanir sem áttu sér stað við fjárhagsskráninguna:

- Prentaðu viðbótarupplýsingar úr svarinu í **Upplýsingaskilaboð** reit á kvittunum.
- Sýna tilkynningar frá ríkisfjármálaþjónustunni sem notendaskilaboð á POS.

    > [!NOTE]
    > Þetta tilkynningakerfi krefst þess að **Sýna tilkynningar um skattaskráningu** breytu á **Tæknisnið fyrir tengi** kveikt á síðunni.

#### <a name="printing-receipts"></a>Prentun kvittana

Skylt er að prenta kvittanir í Þýskalandi. Allar kvittanir verða að innihalda að minnsta kosti eftirfarandi upplýsingar:

- Nafn og heimilisfang félagsins
- Upplýsingar um vörur, þar á meðal verð þeirra og magn
- Upplýsingar um greiðslur sem bárust
- Upplýsingar um skatta, þar á meðal heildarupphæðir á skatthlutfall
- Öryggisgögn:

    - TID
    - Dagsetning og tími þegar viðskiptin hefjast
    - Dagsetning og tími viðskiptaloka
    - Undirskriftarteljari
    - Athugaðu gildi
    - Raðnúmer TSE

- Upplýsingaskilaboð

> [!NOTE]
> Einnig er hægt að prenta QR kóða á kvittanir. Þó að QR kóðinn sé valfrjáls er mjög mælt með honum. Fyrir frekari upplýsingar um hvernig á að fá QR kóða sem hluta af svari frá ríkisfjármálaskráningarþjónustunni, sjá "EFR Guide\[ DE\] " skjal sem er birt á [EFSTA skjöl](https://public.efsta.net/efr/) vefsíðu.
>
> The **Upplýsingaskilaboð** reitinn á kvittunum sýnir tilkynningu frá ríkisskráningarþjónustunni. Til dæmis, ef undirskriftarbúnaður er bilaður, er hægt að prenta sérstakan texta á kvittun.

#### <a name="voided-suspended-and-recalled-transactions"></a>Ógilt, stöðvuð og innkölluð viðskipti

- Ógild viðskipti eru skráð sem beiðni um að slíta viðskiptum í ríkisskráningarþjónustunni.
- Frestað viðskipti eru skráð sem beiðni um að slíta viðskiptum í ríkisskráningarþjónustunni.
- Innköllun á stöðvuðum færslum er skráð sem upphaf nýrrar færslu í ríkisskráningarþjónustunni.

### <a name="non-sales-transactions-and-shift-closing"></a>Ósöluviðskipti og vaktalokun

Eftirfarandi færslur sem ekki eru í sölu eru skráðar sem ófjárhagslegar aðgerðir í skattskráningarþjónustunni með því að nota **NFS** tag:

- Skilgreina upphafsupphæð
- Skiptimyntarfærsla
- Skiptimynt fjarlægð
- Peningaflutningur í öryggisskáp
- Peningaflutningur í banka
- Tekjulyklar
- Kostnaðarlyklar

The **Lokaðu vakt** rekstur er einnig skráður sem rekstur utan ríkisfjármála í skráningarþjónustu ríkisfjármála með því að nota **NFS** merki.

### <a name="data-export-and-audit"></a>Gagnaútflutningur og endurskoðun

Öll viðskipti verða að vera undirrituð af TSE til að tryggja heiðarleika þeirra, áreiðanleika og heilleika og til að koma í veg fyrir meðferð skráðra gagna.

> [!WARNING]
> Aðeins er hægt að nota vottaðan TSE. Fyrir upplýsingar um tegundir og gerðir TSE sem eru studdar í EFR lausninni, sjá "EFR Guide\[ DE\] " skjal sem er birt á [EFSTA skjöl](https://public.efsta.net/efr/) vefsíðu. Fyrir upplýsingar um hvernig á að velja og fá TSE, hafðu samband við [EFSTA](https://www.efsta.eu/at/kontakt).

Reglur í Þýskalandi krefjast stuðnings við DSFinV-K útflutninginn. Hægt er að koma DSFinV-K útflutningi af stað í EFR lausninni. Fyrir frekari upplýsingar um DSFinV-K útflutninginn, sjá "EFR Guide\[ DE\] " skjal sem er birt á [EFSTA skjöl](https://public.efsta.net/efr/) vefsíðu.

### <a name="limitations-of-the-sample"></a>Takmarkanir úrtaksins

Skattaskráningarþjónustan styður aðeins aðstæður þar sem söluskattur er innifalinn í verði. Þess vegna er **Verð eru með söluskatti** valkostur verður að vera stilltur á **Já** fyrir bæði verslanir og viðskiptavini.

Fjármálaþjónustan styður ekki aðstæður þar sem fleiri en einn söluskattskóði er notaður á sömu færslulínuna.

Ríkisfjármálasamþættingarramminn styður ekki sölutilboð. Þess vegna er þessi starfsemi ekki skráð í ríkisfjármálum.

## <a name="set-up-commerce-for-germany"></a>Settu upp Commerce fyrir Þýskaland

Þessi hluti lýsir viðskiptastillingum sem eru sértækar og mælt er með fyrir Þýskaland. Fyrir frekari upplýsingar um uppsetningu, sjá [Heimasíða verslunar](../index.md).

Til að nota virkni sem er sértæk fyrir Þýskaland verður þú að tilgreina eftirfarandi stillingar.

- Í aðal heimilisfangi lögaðilans, stilltu **Land/svæði** sviði til **DEU** (Þýskaland).
- Í POS virknisniði hverrar verslunar sem er staðsett í Þýskalandi, stilltu **ISO kóða** sviði til **DE** (Þýskaland).

Þú verður einnig að tilgreina eftirfarandi stillingar fyrir Þýskaland. Vertu viss um að keyra viðeigandi dreifingarstörf eftir að þú hefur lokið uppsetningunni.

### <a name="set-up-vat-per-german-requirements"></a>Settu upp virðisaukaskatt samkvæmt þýskum kröfum

Þú verður að búa til VSK-kóða, VSK-flokka og VSK-flokka vöru. Þú verður einnig að setja upp upplýsingar um söluskatt fyrir vörur og þjónustu. Fyrir frekari upplýsingar um hvernig á að setja upp og nota söluskattseiginleika, sjá [Söluskattyfirlit](../../finance/general-ledger/indirect-taxes-overview.md).

Á sölukvittunum er hægt að prenta styttan kóða fyrir VSK-kóða (til dæmis "A" eða "B"). Til að gera þessa virkni aðgengilega skaltu stilla **Kóði fyrir prentun** sviði á **Vöruskattskóðar** síðu.

### <a name="set-up-stores"></a>Settu upp verslanir

Á **Allar verslanir** síðu, uppfærðu upplýsingar um verslunina. Nánar tiltekið skaltu stilla eftirfarandi færibreytur:

- Í **Vöruskattshópur** reit, tilgreinið vsk-flokkinn sem ætti að nota fyrir sölu til sjálfgefna viðskiptamanns.
- Stilltu **Verð eru með söluskatti** valmöguleika til **Já**.
- Stilltu **Nafn** reit við nafn fyrirtækis. Þessi breyting hjálpar til við að tryggja að nafn fyrirtækis komi fram á sölukvittun. Að öðrum kosti er hægt að bæta nafni fyrirtækis við útlit sölukvittana sem texta í frjálsu formi.
- Stilltu **Skattkennisnúmer (TIN)** reit á kennitölu fyrirtækisins. Þessi breyting hjálpar til við að tryggja að kenninúmer fyrirtækisins komi fram á sölukvittun. Að öðrum kosti er hægt að bæta kennitölu fyrirtækisins við útlit sölukvittana sem texta í frjálsu formi.

### <a name="set-up-functionality-profiles"></a>Settu upp virknisnið

Settu upp POS virkniprófíla. Á **Númer kvittunar** Flýtiflipi, settu upp númer kvittunar með því að búa til eða uppfæra færslur fyrir **Útsala**, **·**, og **Til baka** tegundir kvittunarfærslur.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Stilltu sérsniðna reiti þannig að hægt sé að nota þá á kvittunarsniði fyrir sölukvittanir

Þú getur stillt tungumálatextann og sérsniðna reiti sem eru notaðir í POS kvittunarsniðum. Sjálfgefið fyrirtæki notandans sem býr til kvittunaruppsetninguna ætti að vera sami lögaðili og tungumálatextauppsetningin er búin til. Að öðrum kosti ætti að búa til sömu tungumálatexta bæði í sjálfgefnu fyrirtæki notanda og lögaðila verslunarinnar sem uppsetningin er búin til fyrir.

Á **Tungumálatexti** síðu, bætið við eftirfarandi skrám fyrir merki sérsniðnu reitanna fyrir kvittunarútlit. Athugið að **Tungumálakenni**, **·**, og **Texti** gildin sem eru sýnd í töflunni eru aðeins dæmi. Þú getur breytt þeim til að uppfylla kröfur þínar. Hins vegar er **Textaauðkenni** gildi sem þú notar verða að vera einstök og þau verða að vera jöfn eða hærri en 900001.

Bættu eftirfarandi POS-merkjum við **POS** kafla í **Tungumálatexti** síðu.

| Kenni tungumáls | Textakenni | Texti                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR-kóði                               |
| en-US       | 900002  | Færslukenni                        |
| en-US       | 900003  | Tax Retail Print Code                 |
| en-US       | 900004  | Skattupphæð (sala)                    |
| en-US       | 900005  | Skattgrundvöllur (sala)                     |
| en-US       | 900006  | Upphafsdagsetning og tími færslu           |
| en-US       | 900007  | Lokadagsetning og tími færslu             |
| en-US       | 900008  | Raðnúmer öryggisþáttarins |
| en-US       | 900009  | Undirskriftarteljari                     |
| en-US       | 900010  | Athugaðu gildi                           |
| en-US       | 900011  | Upplýsingaskilaboð                          |

Á **Sérsniðnir reitir** síðu skaltu bæta við eftirfarandi færslum fyrir sérsniðna reiti fyrir útlit kvittunar. Athugið að **Textaauðkenni fyrir texta** gildi verða að samsvara **Textaauðkenni** gildi sem þú tilgreindir á **Tungumálatexti** síðu.

| Heiti                            | Gerð    | Textakenni myndatexta |
|---------------------------------|---------|-----------------|
| QRCODE\_ DE                      | Innhreyfing | 900001          |
| VIÐSKIPTI\_ DE               | Innhreyfing | 900002          |
| RETAIL PRINTCODE\_ DE             | Innhreyfing | 900003          |
| SÖLUFÆRÐ\_ DE              | Innhreyfing | 900004          |
| SÖLUGRUNDUR\_ DE               | Innhreyfing | 900005          |
| TRANSACTION STARTDATETIME\_ DE    | Innhreyfing | 900006          |
| VIÐSKIPTI ENDDATETIME\_ DE      | Innhreyfing | 900007          |
| ÖRYGGISÞÆTTI RÖÐANÚMER\_ DE | Innhreyfing | 900008          |
| MYNDATEXTI\_ DE                 | Innhreyfing | 900009          |
| SKILTIÐ\_ DE                        | Innhreyfing | 900010          |
| UPPLÝSINGAR\_ DE                 | Innhreyfing | 900011          |

> [!NOTE]
> Það er mikilvægt að þú tilgreinir rétt sérsniðin svæðisheiti eins og þau eru skráð í töflunni á undan. Rangt sérsniðið heiti svæðis mun valda því að gögn vantar í kvittanir.

### <a name="configure-receipt-formats"></a>Stilltu kvittunarsnið

Breyttu gildinu fyrir hvert kvittunarsnið sem þarf **Prenthegðun** sviði til **Alltaf að prenta**.

Í kvittunarsniðshönnuður skaltu bæta eftirfarandi sérsniðnum reitum við viðeigandi kvittunarhluta. Athugaðu að svæðisnöfn samsvara tungumálatextanum sem þú skilgreindir í fyrri hlutanum.

- **Fyrirsögn:** Bættu við eftirfarandi reitum:

    - **Nafn verslunar** og **Skattkennisnúmer** reiti, sem notaðir eru til að prenta nafn fyrirtækis og kennitölu á kvittanir. Að öðrum kosti er hægt að bæta nafni fyrirtækis og kennitölu við útlitið sem texta í frjálsu formi.
    - **Heimilisfang verslunar**, **·**, **24H**, **·**, og **Skráningarnúmer** sviðum.

- **Línur:** Bættu við eftirfarandi reitum:

    - **Nafn hlutar** sviði
    - **Magn** sviði
    - **Heildarverð með sköttum** sviði
    - **Tax Retail Print Code** reitinn, sem er notaður til að prenta skammstafaðan kóða sem samsvarar vsk-kóðanum sem á við vöruna

- **Fótur:** Bættu við eftirfarandi reitum:

    - Greiðslureitir, þannig að greiðsluupphæðir fyrir hvern greiðslumáta eru prentaðar. Til dæmis, bæta við **Nafn tilboðs** og **Útboðsfjárhæð** reiti í eina línu í útlitinu.
    - Reitir í **Skatta sundurliðun** vallarhópur. Öll reiti í þessum reitahópi verður að prenta á eina aðskilda línu.

        - **Skattkenni** reit, sem er staðall reitur sem gerir kleift að prenta vsk-yfirlit fyrir hvern vsk-kóða. Reitinum verður að bæta við nýja línu.
        - **Skattprósenta** reit, sem er staðalreitur sem er notaður til að prenta virkt skatthlutfall fyrir vsk-kóðann.
        - **Skattgrundvöllur (sala)** reitinn, sem er notaður til að prenta út heildarsöluupphæð kvittunarinnar í reiðufé fyrir vsk kóða. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.
        - **Skattupphæð (sala)** reit, sem er notaður til að prenta út skattupphæð kvittunar fyrir staðgreiðslu fyrir vsk-kóðann.
        - **Tax Retail Print Code** reitinn, sem er notaður til að prenta skammstafaðan kóða sem samsvarar vsk-kóðanum.

    - Reitir sem innihalda örugg færslugögn sem er skilað af skattskráningarþjónustunni:

        - **Auðkenni viðskipta** reit, sem auðkennir númer reiðufjárfærslunnar í ríkisskráningarþjónustunni
        - **Upphafstími viðskipta** sviði
        - **Lokadagsetning viðskipta** sviði
        - **Raðnúmer öryggisþáttarins** sviði
        - **Undirskriftarteljari** sviði
        - **Athugaðu gildi** sviði
        - **QR kóða** reitinn, sem er notaður til að prenta tilvísunina í skráða staðgreiðslufærslu í formi QR kóða

        > [!NOTE]
        > The **QR kóða** gildi er sótt úr svari fjárlagaskrár. EFR skilar QR kóða í svari sínu aðeins ef gildið á **Eiginleikar** reitinn í EFR uppsetningunni er lýst í EFSTA skjölunum. QR kóða sniðið í **Eiginleikar** reitinn í EFR stillingunni verður að vera stilltur á **BMP**.

    - **Upplýsingaskilaboð** reit, þannig að hægt sé að birta tilkynningarskilaboð frá ríkisskráningarþjónustu á kvittunum. Til dæmis, ef undirskriftarbúnaður er bilaður, er hægt að prenta sérstakan texta á kvittun.

Fyrir frekari upplýsingar um hvernig á að vinna með kvittunarsnið, sjá [Setja upp og hanna kvittunarsnið](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Settu upp ríkisfjármálasamþættingu fyrir Þýskaland

Samþættingarúrtak ríkisskráningarþjónustu fyrir Þýskaland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Efr** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Þýskaland (arfleifð)](emea-deu-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md):

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu einnig eftir stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta samþættingarsýni fyrir ríkisskráningarþjónustu](#set-up-the-registration-process).
1. [Stilltu stillingar fyrir villumeðferð](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Villumeðhöndlunargeta ríkisfjármálasamþættingarrammans gæti ekki verið að fullu í samræmi við staðbundnar fjármálareglur.
    >
    > - Við mælum með að þú yfirgefur **Halda áfram á villu** valmöguleika á **Skráningarferli í ríkisfjármálum** slökkt á síðunni, vegna þess að allar færslur verða að vera rétt skráðar, jafnvel þó að fyrsta tilraun til skattskráningar hafi ekki tekist.
    > - Áður en þú kveikir á **Sleppa** eða **Merktu sem skráð** valmöguleika á **Skráningarferli í ríkisfjármálum** síðu, ættir þú að ræða þessar breytingar á skattaskráningarferlinu við skattaráðgjafa þinn eða skattstofu á staðnum.

1. [Virkja handvirka framkvæmd frestaðrar fjárhagsskráningar](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Settu upp skráningarferlið

Til að virkja skráningarferlið skaltu fylgja þessum skrefum til að setja upp höfuðstöðvar Commerce. Fyrir frekari upplýsingar, sjá [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Sæktu stillingarskrár fyrir fjárhagsskjalaveituna og fjárhagstengið:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína (til dæmis, **[útgáfa/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Opið **src \> Fiscal Integration \> Efr**.
    1. Sæktu stillingarskrá ríkisskjalaveitunnar á **Stillingar \> Skjalaveitendur \> DocumentProviderFiscalEFRSampleGermany.xml** (til dæmis, [skrána til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Sæktu stillingarskrá fjárhagstengis á **Stillingar \> Tengi \> Tengi EFRSample.xml** (til dæmis, [skrána til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrá ríkisskjalaveitu:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Stillingar\\ DocumentProviderFiscalEFRSampleGermany.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Framlenging.EFRSample\\ Stillingar\\ Tengi EFRSample.xml
    > 
    > Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingarskrá fjárhagsskjalaveitunnar sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú sóttir áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tengi virkni snið**. Búðu til nýtt virknisnið fyrir tengi. Veldu skjalaveituna og tengið sem þú hleður inn áðan. Uppfærðu [gagnakortastillingar](#default-data-mapping) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýtt tæknisnið fyrir tengi og veldu fjárhagstengi sem þú hleður inn áðan. Uppfærðu [tengistillingar](#fiscal-connector-settings) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**. Stofna nýjan fjárhagstengihóp fyrir virknisniðið tengi sem þú bjóst til áður.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**. Búðu til nýtt fjárhagsskráningarferli og fjárhagsskráningarferlisþrep og veldu fjárhagstengihópinn sem þú stofnaðir áðan.
1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veldu virknisnið sem er tengt við verslunina þar sem skráningarferlið á að virkja. Á **Skráningarferli í ríkisfjármálum** Flýtiflipi, veldu fjárhagsskráningarferlið sem þú bjóst til áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Veldu vélbúnaðarsnið sem er tengt við vélbúnaðarstöðina sem fjárhagsprentarinn verður tengdur við. Á **Jaðartæki í ríkisfjármálum** Flýtiflipi, veldu tæknisniðið sem þú bjóst til áðan.
1. Opnaðu dreifingaráætlun (**Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**), og veldu störf **1070** og **1090** að flytja gögn í rásargagnagrunninn.

#### <a name="default-data-mapping"></a>Sjálfgefin gagnakortlagning

Eftirfarandi sjálfgefna gagnavörpun er innifalin í uppsetningu fjárhagsskjalaveitu sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Kortlagning útboðstegunda** – Kortlagning greiðslumáta við gildi á **BorgaG** (greiðsluhópur) eigind í beiðnum sem sendar eru til ríkisfjármála. Hér er sjálfgefið kortlagning:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Fyrsti hluti hvers pars táknar greiðslumáta sem er settur upp fyrir verslunina. Annar þátturinn táknar samsvarandi greiðsluhóp sem er studdur af EFR skattaskráningarþjónustunni. Fyrir frekari upplýsingar um greiðsluhópa sem EFR styður fyrir Þýskaland, sjá [EFR tilvísun](https://public.efsta.net/efr/).

    Sýnishorn af greiðslumáta samsvarar greiðslumáta verslunar sem eru stilltir í stöðluðum kynningargögnum.

    | Greiðslumáti | Heiti greiðsluháttar |
    |----------------|---------------------|
    | 1              | Reiðufé                |
    | 2              | Athuga               |
    | 3              | Spjald                |
    | 4              | Viðskiptavinalykill    |
    | 5              | Annað               |
    | 6              | Gjaldmiðill            |
    | 7              | Fylgiskjal             |
    | 8              | Gjafakort           |
    | 9              | Fjarlægja skiptimynt |
    | 10             | Vildarkort       |
    | 11             | Ávísanir sem ekki eru á staðnum    |

    Þess vegna verður þú að breyta sýnishorninu í samræmi við greiðslumáta sem eru stilltar í forritinu þínu.

- **Láttu gögn viðskiptavina fylgja með** – Ef kveikt er á þessari færibreytu munu beiðnir til fjárhagsþjónustunnar innihalda upplýsingar um viðskiptavini, svo sem nöfn og heimilisföng, í þeim tilvikum þar sem viðskiptavinur er bætt við færslu.
- **Kortlagning virðisaukaskatts (VSK) taxta** – Kortlagning skattprósentugilda sem eru sett upp fyrir vsk-kóða við gildi á **TaxG** (skattflokkur) eigind í beiðnum sem sendar eru til ríkisskattstjóra. Hér er sjálfgefið kortlagning:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Fyrsti þátturinn í hverju pari táknar virðisaukaskattsflokk sem er studdur af EFR skattaskráningarþjónustunni. Annar þátturinn táknar samsvarandi virðisaukaskattshlutfall. Fyrir frekari upplýsingar um virðisaukaskattshópa sem EFR styður fyrir Þýskaland, sjá [EFR tilvísun](https://public.efsta.net/efr/).

- **Skattflokkur fyrir gjafakort og innlán** - Verðmæti **TaxG** eiginleiki í beiðnum sem sendar eru til ríkisfjármála, byggt á rekstri sem felur í sér gjafakort eða innborgun. Hér er sjálfgefið kortlagning:

    ```
    G
    ```

- **Skattflokkur undanþeginn virðisaukaskatti** - Verðmæti **TaxG** eigind í beiðnum sem sendar eru til ríkisfjármála, byggt á rekstri sem er undanþeginn skattskyldu. Hér er sjálfgefið kortlagning:

    ```
    F
    ```

> [!NOTE]
> Skattstillingar í sjálfgefnum gagnakortlagningu eru ábyrgar fyrir samsvörun skattstillinga í kerfinu og skattflokka í EFR þjónustunni. Skattflokka er aðeins hægt að prenta á kvittanir ef **Kóði fyrir prentun** reiturinn er stilltur á **Vöruskattskóðar** síðu.

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru innifalin í fjárhagstengistillingunni sem er hluti af fjárhagssamþættingarsýninu:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum, sem fjárhagstengi bíður eftir svari frá fjárhagsskráningarþjónustunni.
- **Sýna tilkynningar um skattaskráningu** – Þessi fáni stjórnar hvort tilkynningar sem skattskráningarþjónustan skilar eigi að vera sýndar rekstraraðila.

### <a name="configure-channel-components"></a>Stilltu rásaríhluti

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Þýskaland (arfleifð)](emea-deu-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

#### <a name="set-up-the-development-environment"></a>Settu upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og stækka sýnishornið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla. Veldu rétta útgáfu útibús í samræmi við SDK/forritsútgáfu þína. Fyrir frekari upplýsingar, sjá [Sæktu smásölu SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu EFR lausnina kl **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ Efr\\ EFR.sln**, og byggja það.
1. Settu upp viðskiptatímaviðbætur:

    1. Finndu CRT uppsetningarforrit fyrir viðbót:

        - **Eining viðskiptaskala:** Í **Efr\\ ScaleUnit\\ ScaleUnit.EFR.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ScaleUnit.EFR.Installer** uppsetningarforrit.
        - **Staðbundið CRT á Modern POS:** Í **Efr\\ ModernPOS\\ ModernPOS.EFR.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ModernPOS.EFR.Installer** uppsetningarforrit.

    1. Byrjaðu á CRT uppsetningarforrit fyrir viðbót frá skipanalínunni:

        - **Eining viðskiptaskala:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Settu upp fjárhagslega tengiviðbætur:

    Þú getur sett upp fjárhagstengiviðbætur á [Vélbúnaðarstöð](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eða the [POS skrá](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Settu upp vélbúnaðarstöðvarviðbætur:

        1. Í **Efr\\ Vélbúnaðarstöð\\ HardwareStation.EFR.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.EFR.Installer** uppsetningarforrit.
        1. Byrjaðu uppsetningarforritið frá skipanalínunni með því að keyra eftirfarandi skipun.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Settu upp POS viðbætur:

        1. Opnaðu sýnishorn af POS fjárhagstengislausn á **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ PosFiscalConnectorSample\\ Contoso.PosFiscalConnectorSample.sln**, og byggja það.
        1. Í **PosFiscalConnectorSample\\ StoreCommerce.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer** uppsetningarforrit.
        1. Byrjaðu uppsetningarforritið frá skipanalínunni með því að keyra eftirfarandi skipun.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgdu skrefunum í [Settu upp smíðisleiðslu fyrir sýnishorn fjárhagslega samþættingar](fiscal-integration-sample-build-pipeline.md) til að búa til og gefa út Cloud Scale Unit og sjálfsafgreiðslupakka fyrir fjárhagslega samþættingarúrtakið. The **EFR build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarúrtak ríkisskráningarþjónustu fyrir Þýskaland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Efr** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ríkisfjármálaskjalaveitanda, sem er framlenging á CRT, og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Þýskaland (arfleifð)](emea-deu-fi-sample-sdk.md). Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

### <a name="crt-extension-design"></a>CRT framlengingarhönnun

Tilgangur framlengingarinnar sem er ríkisfjármálaskjalaveita er að búa til þjónustusértæk skjöl og annast svör frá ríkisskráningarþjónustunni.

#### <a name="request-handler"></a>Beiðni um stjórnanda

Það er einn meðhöndlun beiðna fyrir skjalaveituna, **DocumentProviderEFRFiscalDEU**. Þessi meðhöndlun er notuð til að búa til fjárhagsskjöl fyrir fjárhagsskráningarþjónustuna. Það er erft frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í ríkisskráningarþjónustunni.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Þessi beiðni skilar svarinu ásamt víðtækum gögnum.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagsskjalaveituna er staðsett á **src\\ Fiscal Integration\\ Efr\\ Stillingar\\ Skjalaveitendur\\ DocumentProviderFiscalEFRSampleGermany.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera það kleift að stilla stillingar ríkisfjármálaskjalaveitunnar frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur framlengingarinnar sem er fjárhagstengi er að hafa samskipti við skattskráningarþjónustuna.

Viðbygging Vélbúnaðarstöðvarinnar er **HardwareStation.Extension.EFRSample**. Það notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar við skattskráningarþjónustuna. Það sér einnig um svör sem berast frá ríkisskráningarþjónustu.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **EFRHandler** meðhöndlun beiðna er inngangsstaður fyrir meðhöndlun beiðna til skattskráningarþjónustunnar. Þessi meðhöndlari er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem tilgreint er í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ FiscalIntegration\\ Efr\\ Stillingar\\ Tengi\\ Tengi EFRSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera kleift að stilla stillingar á fjárhagstenginu frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="pos-fiscal-connector-extension-design"></a>Hönnun POS fjárhagstengisframlengingar

Tilgangur POS fjárhagstengiviðbótar er að hafa samskipti við fjárhagsskráningarþjónustuna frá POS. Það notar HTTPS samskiptareglur fyrir samskipti.

#### <a name="fiscal-connector-factory"></a>Fiskal tengiverksmiðju

Fjárhagstengjaverksmiðjan kortleggur nafn tengisins við útfærslu fjárhagstengisins og er staðsett í **Pos.Extension\\ Tengi\\ FiscalConnectorFactory.ts** skrá. Nafn tengisins ætti að passa við nafn fjárhagstengis sem er tilgreint í höfuðstöðvum Commerce.

#### <a name="efr-fiscal-connector"></a>EFR fjárhagslega tengi

Fjárhagstenging EFR er staðsett í **Pos.Extension\\ Tengi\\ Efr\\ EfrFiscalConnector.ts** skrá. Það útfærir **IFiscalConnector** viðmót sem styður eftirfarandi beiðnir:

- **FiscalRegisterSubmitDocumentClientRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **FiscalRegisterIsReadyClientRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **FiscalRegisterInitializeClientRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **src\\ Fiscal Integration\\ Efr\\ Stillingar\\ Tengi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir fjárhagstengi kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum, sem tengið bíður eftir svari frá skattskráningarþjónustunni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

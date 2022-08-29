---
title: Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Austurríki
description: Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Austurríki í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: da4deb37b260ffa2a68e2a36aef01965cbf098b2
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313802"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Austurríki

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Austurríki í Microsoft Dynamics 365 Commerce.

Til að uppfylla staðbundnar fjárhagslegar kröfur fyrir sjóðvélar í Austurríki, er Dynamics 365 Retail virkni fyrir Austurríki felur í sér sýnishorn af samþættingu sölustaðarins (POS) við ytri skattaskráningarþjónustu. Sýnið framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Það er byggt á [EFR (rafræn ríkisfjármálaskrá)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) lausn frá [EFSTA](https://www.efsta.eu/at/) og gerir samskipti við EFR þjónustuna í gegnum HTTPS samskiptareglur. EFR þjónustan ætti að vera hýst á annaðhvort verslunarvélbúnaðarstöðinni eða sérstakri vél sem hægt er að tengja við frá vélbúnaðarstöðinni. Sýnishornið er gefið í formi frumkóða og er hluti af Commerce hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá EFSTA. Fyrir upplýsingar um hvernig á að fá EFR lausnina og reka hana, hafðu samband [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Aðstæður

Eftirfarandi aðstæður falla undir samþættingarúrtak ríkisskráningarþjónustu fyrir Austurríki:

- Skráning reiðufjárviðskipta í ríkisskráningarþjónustu:

    - Sendu nákvæmar viðskiptagögn til ríkisskráningarþjónustunnar. Þessi gögn innihalda upplýsingar um sölulínur og upplýsingar um afslætti, greiðslur og skatta.
    - Fangaðu svar frá ríkisfjármálaskráningarþjónustunni. Þetta svar inniheldur stafræna undirskrift og tengil á skráða færslu.
    - Skráðu skatta og kortaðu þá á skattanúmer skattskráningarþjónustunnar.
    - Prentaðu QR kóðann fyrir skráða færslu á kvittuninni.

- Skráning gjafakortastarfsemi og innlána viðskiptavina sem færslur sem ekki eru reiðufé í skráningarþjónustu ríkisfjármála:

    - Gefðu út eða bættu peningum við gjafakort.
    - Skráðu innborgun viðskiptavinareiknings.
    - Skráðu innborgun viðskiptavinarpöntunar.

- Skráning ósöluviðskipta og atburða sem færslu utan reiðufé í skráningarþjónustu ríkisfjármála:

    - Opin vakt og Loka vakt
    - Upphafsupphæð, flotfærsla og brottnám tilboðs
    - Verðhnekking
    - Skattahnekking
    - Prenta afrit af kvittun
    - Opna skúffu
    - Prenta X-skýrslu
    - Prenta Z-skýrslu

- Prentun dagslokaskýrslna (X/Z skýrslur) sem hafa Austurríkissértæka reiti:

    - Heildarfjöldi vara eða þjónustu sem var afhent viðskiptavinum
    - Sundurliðun sölu eftir skatthlutfalli
    - Sundurliðun greiðslna eftir gjaldkera/sjóðsstjóra
    - Verðafslættir og skil sem draga úr daglegri sölu
    - Engin sala (gjafir)

- Villumeðferð, svo sem eftirfarandi valkostir:

    - Reyndu aftur fjárhagsskráningu ef hægt er að reyna aftur, eins og ef fjárhagsskráningarþjónustan er ekki tiltæk, er ekki tilbúin eða svarar ekki.
    - Fresta skattskráningu.
    - Slepptu skattaskráningu eða merktu færsluna sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Athugaðu framboð á fjárhagsskráningarþjónustu áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="gift-cards"></a>Gjafakort

Samþættingarsýnishorn ríkisskráningarþjónustu innleiðir eftirfarandi reglur sem tengjast gjafakortum:

- Útiloka sölulínur sem tengjast *Gefðu út gjafakort* og *Bæta við gjafakort* rekstur úr staðgreiðslu. Í stað þess að skrá þessar línur sem hluta af staðgreiðslufærslu skaltu skrá þær sem sérstaka færslu sem ekki er reiðufé í ríkisskráningarþjónustunni.
- Ekki prenta sundurliðun skattaflokka og QR kóða á kvittun ef kvittunin samanstendur eingöngu af gjafakortalínum.
- Prentaðu heildarupphæð gjafakorta sem eru gefin út eða endurgjaldfærð í færslu aðskilið frá færsluupphæðinni í reiðufé á kvittuninni.
- Vistaðu reiknaðar leiðréttingar á greiðslulínum í rásargagnagrunninum með tilvísun í samsvarandi fjárhagsfærslu.
- Greiðsla með gjafakorti telst venjuleg greiðsla.

### <a name="customer-deposits-and-customer-order-deposits"></a>Innlán viðskiptavina og pantanir viðskiptavina

Samþættingarúrtak ríkisskráningarþjónustunnar innleiðir eftirfarandi reglur sem tengjast innlánum viðskiptavina og innborgunum viðskiptavina:

- Skráðu viðskipti sem ekki eru reiðufé ef viðskiptin eru innborgun viðskiptavina.
- Skráðu færslu sem ekki er reiðufé ef færsla inniheldur aðeins innborgun viðskiptavinapöntunar eða endurgreiðslu innborgunar viðskiptavinarpöntunar.
- Dragðu innborgunarupphæð viðskiptavinarpöntunar frá greiðslulínum þegar blandað viðskiptavinapöntun er stofnuð.
- Vistaðu reiknaðar leiðréttingar á greiðslulínum í rásargagnagrunninum með tilvísun í fjárhagsfærslu fyrir blandaða viðskiptavinapöntun.

### <a name="limitations-of-the-sample"></a>Takmarkanir úrtaksins

Skattskráningarþjónustan styður aðeins aðstæður þar sem söluskattur er innifalinn í verðinu. Þess vegna er **Verð er með söluskatti** valkostur verður að vera stilltur á **Já** fyrir bæði verslanir og viðskiptavini.

## <a name="set-up-commerce-for-austria"></a>Settu upp Commerce fyrir Austurríki

Þessi hluti lýsir viðskiptastillingum sem eru sértækar og mælt er með fyrir Austurríki. Fyrir frekari upplýsingar um uppsetningu, sjá [Heimasíða verslunar](../index.md).

Til að nota Austurríkissértæka virkni verður þú að tilgreina eftirfarandi stillingar:

- Í aðal heimilisfangi lögaðila, stilltu **Land/svæði** sviði til **AUT** (Austurríki).
- Í POS virkniprófílnum í hverri verslun sem er staðsett í Austurríki skaltu stilla **ISO kóða** sviði til **AT** (Austurríki).

Þú verður einnig að tilgreina eftirfarandi stillingar fyrir Austurríki. Athugaðu að þú verður að keyra viðeigandi dreifingarverk eftir að þú hefur lokið uppsetningunni.

### <a name="enable-features-for-austria"></a>Virkjaðu eiginleika fyrir Austurríki

Þú verður að virkja eftirfarandi eiginleika í **Eiginleikastjórnun** vinnusvæði:

- (Austurríki) Virkja fleiri endurskoðunartilvik á sölustað
- (Austurríki) Virkja viðbótarupplýsingar í uppgjörum í dagslok á sölustað

### <a name="set-up-vat-per-austrian-requirements"></a>Settu upp virðisaukaskatt samkvæmt austurrískum kröfum

Þú verður að búa til VSK-kóða, VSK-flokka og VSK-flokka vöru. Þú verður einnig að setja upp upplýsingar um söluskatt fyrir vörur og þjónustu. Fyrir frekari upplýsingar um hvernig á að setja upp og nota söluskattseiginleika, sjá [Söluskattyfirlit](../../finance/general-ledger/indirect-taxes-overview.md).

Á sölukvittunum er hægt að prenta út styttan kóða fyrir vsk-kóða (til dæmis "A" eða "B"). Til að gera þessa virkni aðgengilega skaltu stilla **Prentaðu kóða** sviði á **Vöruskattskóðar** síðu.

### <a name="set-up-stores"></a>Settu upp verslanir

Á **Allar verslanir** síðu, uppfærðu upplýsingar um verslunina. Nánar tiltekið skaltu stilla eftirfarandi færibreytur:

- Í **Vöruskattshópur** reit, tilgreinið vsk-flokkinn sem á að nota fyrir sölu til sjálfgefna viðskiptamanns.
- Stilltu **Verð eru með söluskatti** valmöguleika til **Já**.
- Stilltu **Nafn** reit við nafn fyrirtækis. Þessi breyting hjálpar til við að tryggja að nafn fyrirtækis komi fram á sölukvittun. Að öðrum kosti er hægt að bæta nafni fyrirtækis við útlit sölukvittana sem texta í frjálsu formi.
- Stilltu **Skattkennisnúmer (TIN)** reit á kennitölu fyrirtækisins. Þessi breyting hjálpar til við að tryggja að kenninúmer fyrirtækisins komi fram á sölukvittun. Að öðrum kosti er hægt að bæta kennitölu fyrirtækis við útlit sölukvittana sem texta í frjálsu formi.

### <a name="set-up-functionality-profiles"></a>Virknireglur settar upp

Settu upp POS virknisnið:

- Á **Númer kvittunar** Flýtiflipi, settu upp númer kvittunar með því að búa til eða uppfæra færslur fyrir **Útsala**, **·**, og **Til baka** gerðir kvittunarfærslu.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Stilltu sérsniðna reiti þannig að hægt sé að nota þá á kvittunarsniði fyrir sölukvittanir

Þú getur stillt tungumálatextann og sérsniðna reiti sem eru notaðir í POS kvittunarsniðum. Sjálfgefið fyrirtæki notandans sem býr til kvittunaruppsetninguna ætti að vera sami lögaðili og tungumálatextauppsetningin er búin til. Að öðrum kosti ætti að búa til sömu tungumálatexta bæði í sjálfgefnu fyrirtæki notanda og lögaðila verslunarinnar sem uppsetningin er búin til fyrir.

Á **Tungumálatexti** síðu, bætið við eftirfarandi færslum fyrir merki sérsniðnu reitanna fyrir kvittunarútlit. Athugið að **Tungumálakenni**, **·**, og **Texti** gildi sem eru sýnd í töflunni eru aðeins dæmi. Þú getur breytt þeim til að uppfylla kröfur þínar. Hins vegar er **Textakenni** gildi sem þú notar verða að vera einstök og þau verða að vera jöfn eða hærri en 900001.

Bættu eftirfarandi POS merkimiðum við **POS** kafla af **Tungumálatexti** af borðinu:

| Kenni tungumáls | Textakenni | Texti                      |
|-------------|---------|---------------------------|
| is       | 900001  | QR-kóði                   |
| is       | 900002  | Stöðugt númer         |
| is       | 900003  | Tax Retail Print Code     |
| is       | 900004  | Samtala (sala)             |
| is       | 900005  | Heildarskattur (sala)         |
| is       | 900006  | Samtals með skatti (sölu) |
| is       | 900007  | Skattupphæð (sala)        |
| is       | 900008  | Skattgrundvöllur (sala)         |

Á **Sérsniðnir reitir** síðu, bætið við eftirfarandi færslum fyrir sérsniðna reiti fyrir móttökuútlit. Athugið að **Auðkenni textatexta** gildi verða að samsvara **Textakenni** gildi sem þú tilgreindir á **Tungumálatexti** síða:

| Nafn                 | Gerð    | Textakenni myndatexta |
|----------------------|---------|-----------------|
| QRCODE               | Innhreyfing | 900001          |
| STAÐFULLT     | Innhreyfing | 900002          |
| RETAIL PRINTCODE      | Innhreyfing | 900003          |
| SÖLUSAML           | Innhreyfing | 900004          |
| SÖLUTAKUR        | Innhreyfing | 900005          |
| SALESTOTALIÐ AÐFALDIÐ VAXA | Innhreyfing | 900006          |
| SÖLUVAGN       | Innhreyfing | 900007          |
| SÖLUGRUNDUR        | Innhreyfing | 900008          |

> [!NOTE]
> Það er mikilvægt að þú tilgreinir rétt sérsniðin svæðisheiti, eins og skráð er í töflunni á undan. Rangt sérsniðið heiti svæðis mun valda því að gögn vantar í kvittanir.

### <a name="configure-receipt-formats"></a>Stilltu kvittunarsnið

Fyrir hvert áskilið kvittunarsnið, breyttu gildinu **Prenthegðun** sviði til **Alltaf að prenta**.

Í kvittunarsniðshönnuður skaltu bæta eftirfarandi sérsniðnum reitum við viðeigandi kvittunarhluta. Athugaðu að svæðisnöfn samsvara tungumálatextanum sem þú skilgreindir í fyrri hlutanum.

- **Fyrirsögn:** Bættu við eftirfarandi reitum:

    - **Nafn verslunar** og **Skattkennisnúmer** reiti, sem notaðir eru til að prenta fyrirtækisnafn og kennitölu á kvittanir. Að öðrum kosti er hægt að bæta nafni fyrirtækis og kennitölu við útlitið sem texta í frjálsu formi.
    - **Heimilisfang verslunar**, **·**, **24H**, **·**, og **Skráningarnúmer** sviðum.
    - **Stöðugt númer** reiti, til að auðkenna númer reiðufjárfærslunnar í skattaskráningarþjónustunni.

- **Línur:** Bættu við eftirfarandi reitum:

    - **Nafn hlutar**.
    - **Magn**.
    - **Heildarverð með sköttum**.
    - **Tax Retail Print Code**, sem er notað til að prenta skammstafaðan kóða sem samsvarar vsk-kóðanum sem á við vöruna.

- **Fótur:** Bættu við eftirfarandi reitum:

    - Greiðslureitir, þannig að greiðsluupphæðir fyrir hvern greiðslumáta eru prentaðar. Til dæmis, bæta við **Nafn tilboðs** og **Útboðsfjárhæð** reiti í eina línu í útlitinu.
    - **Sala alls** reithópur:

        - **Samtals (sala)** reitinn, sem er notaður til að prenta út heildarsöluupphæð kvittunarinnar í reiðufé. Upphæðin er án skatts. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.
        - **Samtals með skatti (sölu)** reitinn, sem er notaður til að prenta út heildarsöluupphæð kvittunarinnar í reiðufé. Upphæðin inniheldur skatt. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.
        - **Heildarskattur (sala)** reitinn, sem er notaður til að prenta út heildarskattupphæð kvittunarinnar fyrir staðgreiðslusölu. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.

    - **Skatta sundurliðun** vallarhópur. Öll reiti í þessum reitaflokki verður að prenta á eina aðskilda línu.

        - **Skattkenni** reit, sem er staðall reitur sem gerir kleift að prenta vsk-yfirlit fyrir hvern vsk-kóða. Reiturinn verður að bæta við nýja línu.
        - **Skattprósenta** reit, sem er staðalreitur sem er notaður til að prenta virkt skatthlutfall fyrir vsk-kóðann.
        - **Skattgrundvöllur (sala)** reitinn, sem er notaður til að prenta út heildarsöluupphæð kvittunarinnar í reiðufé fyrir vsk-kóðann. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.
        - **Skattupphæð (sala)** reitinn, sem er notaður til að prenta út skattupphæð kvittunarinnar fyrir staðgreiðslusölu fyrir vsk-kóðann.
        - **Tax Retail Print Code** reitinn, sem er notaður til að prenta skammstafaðan kóða sem samsvarar vsk-kóðanum.

    - **QR kóða** reitinn, sem er notaður til að prenta tilvísunina í skráða staðgreiðslufærslu í formi QR kóða.

        > [!NOTE]
        > The **QR kóða** gildi er sótt í svar fjárhagsskrár. EFR skilar QR kóða í svari sínu aðeins ef gildið á **Eiginleikar** reitnum í EFR uppsetningunni er lýst í EFSTA skjölunum. QR kóða sniðið í **Eiginleikar** reitinn í EFR stillingunni verður að vera stilltur á **BMP**.

Fyrir frekari upplýsingar um hvernig á að vinna með kvittunarsnið, sjá [Setja upp og hanna kvittunarsnið](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Settu upp ríkisfjármálasamþættingu fyrir Austurríki

Samþættingarsýni skattaskráningarþjónustu fyrir Austurríki er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Commerce SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Efr** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. The [sýnishorn](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) samanstendur af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Commerce SDK, sjá [Sæktu Commerce SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Samþættingarsýnishorn ríkisskráningarþjónustu fyrir Austurríki er fáanlegt í Commerce SDK frá og með Commerce útgáfu 10.0.29. Í Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Austurríki (arfleifð)](emea-aut-fi-sample-sdk.md).

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md):

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu líka eftir stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta samþættingarsýni fyrir ríkisskráningarþjónustu](#set-up-the-registration-process).
1. [Stilltu stillingar fyrir villumeðferð](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Virkja handvirka framkvæmd frestaðrar fjárhagsskráningar](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Settu upp skráningarferlið

Til að virkja skráningarferlið skaltu fylgja þessum skrefum til að setja upp höfuðstöðvar Commerce. Fyrir frekari upplýsingar, sjá [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Sæktu stillingarskrár fyrir fjárhagsskjalaveituna og fjárhagstengið:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína.
    1. Opið **src \> Fiscal Integration \> Efr**.
    1. Opið **Stillingar \> Skjalaveitendur**, og hlaðið niður stillingarskrám fjárhagsskjalaveitunnar: 

        - DocumentProviderFiscalEFRSampleAustria.xml
        - DocumentProviderNonFiscalEFRSampleAustria.xml

    1. Sæktu stillingarskrá fjárhagstengis á **Stillingar \> Tengi \> TengiEFRSample.xml**.

    > [!NOTE]
    > Í Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrár fyrir ríkisfjármálaskjalaveitu:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Stillingar
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Framlenging.EFRSample\\ Stillingar

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingarskrám fyrir fjárhagsskjalaveitu sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tengi virkni snið**. Búðu til tvö ný virknisnið fyrir tengi, eitt fyrir hverja fjárhagsskjalaveitu sem þú hleður inn áðan, og veldu fjárhagstengi sem þú hleður inn áður. Uppfærðu [gagnakortastillingar](#default-data-mapping) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýtt tæknisnið fyrir tengi og veldu fjárhagstengi sem þú hleður inn áðan. Uppfærðu [tengistillingar](#fiscal-connector-settings) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**. Búðu til tvo nýja fjárhagstengihópa, einn fyrir hvern virknisnið tengis sem þú bjóst til áður.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**. Búðu til nýtt fjárhagsskráningarferli og tvö fjárhagsskráningarferlisþrep og veldu fjárhagstengiflokkana sem þú stofnaðir áðan.
1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veldu virknisnið sem er tengt við verslunina þar sem skráningarferlið á að virkja. Á **Skráningarferli í ríkisfjármálum** Flýtiflipi, veldu fjárhagsskráningarferlið sem þú bjóst til áðan. Til að virkja skráningu ófjárhagslegra atburða á POS, á **Aðgerðir** Flýtiflipi, undir **POS**, stilltu **Endurskoðun** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Veldu vélbúnaðarsnið sem er tengt við vélbúnaðarstöðina sem fjárhagsskráningarþjónustan verður tengd við. Á **Jaðartæki í ríkisfjármálum** Flýtiflipi, veldu tæknisniðið sem þú bjóst til áðan.
1. Opnaðu dreifingaráætlun (**Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**), og veldu störf **1070** og **1090** að flytja gögn í rásargagnagrunninn.

#### <a name="default-data-mapping"></a>Sjálfgefin gagnakortlagning

Eftirfarandi sjálfgefna gagnavörpun er innifalin í uppsetningu fjárhagsskjalaveitu sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Kortlagning virðisaukaskatts (VSK) taxta** – Kortlagning skattprósentugilda sem eru sett upp fyrir vsk-kóða við gildi á **TaxG** (skattflokkur) eigind í beiðnum sem sendar eru til ríkisskattstjóra. Hér er sjálfgefið kortlagning:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Fyrsti þátturinn í hverju pari táknar virðisaukaskattsflokk sem er studdur af EFR skattaskráningarþjónustunni. Annar þátturinn táknar samsvarandi virðisaukaskattshlutfall. Fyrir frekari upplýsingar um virðisaukaskattshópa sem EFR styður fyrir Austurríki, sjá [EFR tilvísun](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru innifaldar í fjárhagstengistillingunni sem er hluti af fjárhagssamþættingarsýninu:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Tímamörk tækisins** – Tíminn, í millisekúndum, sem fjárhagstengi bíður eftir svari frá fjárhagsskráningarþjónustunni.
- **Sýna tilkynningar um skattaskráningu** – Þessi fáni stjórnar hvort tilkynningar sem skattskráningarþjónustan skilar skuli birtar rekstraraðila.

### <a name="configure-channel-components"></a>Stilltu rásaríhluti

> [!NOTE]
> - Samþættingarsýnishorn ríkisskráningarþjónustu fyrir Austurríki er fáanlegt í Commerce SDK frá og með Commerce útgáfu 10.0.29. Í Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Austurríki (arfleifð)](emea-aut-fi-sample-sdk.md).
> - Viðskiptasýni sem eru notuð í umhverfi þínu eru ekki sjálfkrafa uppfærð þegar þú notar þjónustu- eða gæðauppfærslur á Commerce íhlutum. Þú verður að uppfæra nauðsynleg sýni handvirkt.

#### <a name="set-up-the-development-environment"></a>Settu upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og stækka úrtakið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína. Fyrir frekari upplýsingar, sjá [Sæktu Commerce SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu EFR lausnina kl **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ Efr\\ EFR.sln**, og byggja það.
1. Settu upp CRT viðbætur:

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

    1. Settu upp viðbætur fyrir vélbúnaðarstöð:

        1. Í **Efr\\ Vélbúnaðarstöð\\ HardwareStation.EFR.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.EFR.Installer** uppsetningarforrit.
        1. Byrjaðu uppsetningarforritið frá skipanalínunni með því að keyra eftirfarandi skipun.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Settu upp POS viðbætur:

        1. Opnaðu sýnishorn af POS fjárhagstengislausn á **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ PosFiscalConnectorSample\\ Contoso.PosFiscalConnectorSample.sln**, og byggja það.
        1. Í **PosFiscalConnectorSample\\ StoreCommerce.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer** uppsetningarforrit.
        1. Byrjaðu uppsetningarforritið frá skipanalínunni sem keyrir eftirfarandi skipun.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgdu skrefunum í [Settu upp byggingarleiðslu fyrir fjárhagslega samþættingarsýni](fiscal-integration-sample-build-pipeline.md) til að búa til og gefa út Cloud Scale Unit og sjálfsafgreiðslupakka fyrir fjárhagslega samþættingarúrtakið. The **EFR build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarsýni skattaskráningarþjónustu fyrir Austurríki er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Commerce SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Efr** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ríkisfjármálaskjalaveitanda, sem er framlenging á CRT, og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Commerce SDK, sjá [Sæktu Commerce SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Samþættingarsýnishorn ríkisskráningarþjónustu fyrir Austurríki er fáanlegt í Commerce SDK frá og með Commerce útgáfu 10.0.29. Í Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Austurríki (arfleifð)](emea-aut-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun 

Tilgangur framlengingarinnar sem er ríkisfjármálaskjalaveita er að búa til þjónustusértæk skjöl og annast svör frá ríkisskráningarþjónustunni.

#### <a name="request-handler"></a>Beiðni um stjórnanda

Það eru tveir beiðnaraðilar fyrir skjalaveitendur:

- **DocumentProviderEFRFiscalAUT** – Þessi meðhöndlun er notuð til að búa til fjárhagsskjöl fyrir fjárhagsskráningarþjónustuna.
- **DocumentProviderEFRNonFiscalAUT** – Þessi meðhöndlun er notuð til að búa til skjöl sem ekki eru skattaleg skjöl fyrir skattaskráningarþjónustuna.

Þessir meðhöndlarar eru í arf frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í skattaskráningarþjónustuna.
- **GetNonFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal sem ekki er ríkisfjármál ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í skattaskráningarþjónustuna.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er, eru eftirfarandi atburðir studdir: sala, prentun X skýrslu, prentun Z skýrslu, innlán viðskiptavinareikninga, pöntun viðskiptavina, endurskoðunarviðburðir og færslur sem ekki eru sölu.
- **Get FiscalRegisterResponseToSaveDocumentProviderRequest** – Þessi beiðni skilar svari frá ríkisskráningarþjónustunni. Þetta svar er sett í röð til að mynda streng þannig að það sé tilbúið til vistunar.

#### <a name="configuration"></a>Skilgreining

Stillingarskrárnar fyrir ríkisfjármálaskjalaveituna eru staðsettar í **src\\ Fiscal Integration\\ Efr\\ Stillingar\\ Skjalaveitendur** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla:

- **DocumentProviderFiscalEFRSampleAustria** – Stillingarskrá fyrir fjárhagsskjalaveituna fyrir fjárhagsskjöl.
- **DocumentProviderNonFiscalEFRSampleAusturríki** – Stillingarskrá fyrir ríkisfjármálaskjalaveituna fyrir skjöl sem ekki eru ríkisfjármálaskjöl.

Tilgangur þessara skráa er að gera það kleift að stilla stillingar birgðafjárhagsskjala frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangurinn með framlengingunni á fjárhagstenginu er að hafa samskipti við skattskráningarþjónustuna. Vélbúnaðarstöðvarviðbótin notar HTTP og HTTPS samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar við skattskráningarþjónustuna. Það annast einnig svör sem berast frá ríkisskráningarþjónustu.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **EFRHandler** meðhöndlun beiðna er inngangsstaður fyrir meðhöndlun beiðna til skattskráningarþjónustunnar.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem er tilgreint í höfuðstöðvum Commerce.

Fjárhagstengingin styður eftirfarandi beiðnir:

- **SubmitDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ Fiscal Integration\\ Efr\\ Stillingar\\ Tengi\\ TengiEFRSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera kleift að stilla stillingar á fjárhagstenginu frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="pos-fiscal-connector-extension-design"></a>Framlengingarhönnun POS fjárhagstengis

Tilgangur POS fjárhagstengingarviðbótar er að hafa samskipti við fjárhagsskráningarþjónustuna frá POS. Það notar HTTPS samskiptareglur fyrir samskipti.

#### <a name="fiscal-connector-factory"></a>Fiskal tengiverksmiðju

Fjárhagstengjaverksmiðjan kortleggur nafn tengisins við útfærslu fjárhagstengisins og er staðsett í **Pos.Extension\\ Tengi\\ FiscalConnectorFactory.ts** skrá. Nafn tengisins ætti að passa við nafn fjárhagstengis sem tilgreint er í höfuðstöðvum Commerce.

#### <a name="efr-fiscal-connector"></a>EFR fjárhagslega tengi

Fjárhagstenging EFR er staðsett í **Pos.Extension\\ Tengi\\ Efr\\ EfrFiscalConnector.ts** skrá. Það útfærir **IFiscalConnector** viðmót sem styður eftirfarandi beiðnir:

- **FiscalRegisterSubmitDocumentClientRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **FiscalRegisterIsReadyClientRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **FiscalRegisterInitializeClientRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **src\\ Fiscal Integration\\ Efr\\ Stillingar\\ Tengi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir fjárhagslega tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum, sem tengið mun bíða eftir svari frá skattskráningarþjónustunni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

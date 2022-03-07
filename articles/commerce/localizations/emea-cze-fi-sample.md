---
title: Samþættingarsýni skattaskráningarþjónustu fyrir Tékkland
description: Þetta efni veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Tékkland í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 990de96f57f4a22b4d58da5f970b1b96f5fc21f5
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077091"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Samþættingarsýni skattaskráningarþjónustu fyrir Tékkland

[!include[banner](../includes/banner.md)]

Þetta efni veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Tékkland í Microsoft Dynamics 365 Commerce.

Til að uppfylla staðbundnar fjárhagslegar kröfur fyrir sjóðvélar í Tékklandi, skal Dynamics 365 Commerce virkni fyrir Tékkland felur í sér sýnishorn af samþættingu sölustaðarins (POS) við utanaðkomandi skattaskráningarþjónustu. Sýnið framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Það er byggt á [EFR (rafræn ríkisfjármálaskrá)](https://efsta.org/sicherheitsloesungen/) lausn frá [EFSTA](https://efsta.org/) og gerir samskipti við EFR þjónustuna í gegnum HTTPS samskiptareglur. EFR þjónustan tryggir rafræna söluskráningu (EET - Elektronická evidence tržeb), þ.e. sendingu sölugagna á netinu til skattyfirvalda í ríkisfjármálum.

EFR þjónustan ætti að vera hýst á annaðhvort Commerce vélbúnaðarstöðinni eða sérstakri vél sem hægt er að tengja við frá vélbúnaðarstöðinni. Sýnishornið er gefið í formi frumkóða og er hluti af Retail hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá EFSTA. Fyrir upplýsingar um hvernig á að fá EFR lausnina og reka hana, hafðu samband [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Sviðsmyndir

Eftirfarandi sviðsmyndir falla undir samþættingarúrtak ríkisskráningarþjónustu fyrir Tékkland.

- Skráning reiðufjárviðskipta í ríkisskráningarþjónustu.

    - Sendu nákvæmar viðskiptagögn til ríkisskráningarþjónustunnar. Þessi gögn innihalda upplýsingar um sölulínur og upplýsingar um afslætti, greiðslur og skatta. Ríkisskráningarþjónustan sendir gögnin ennfremur til vefþjónustu skattyfirvalda og fær frá henni staðfestingu sem inniheldur auðkenni viðskiptanna.
    - Fangaðu svar frá skattaskráningarþjónustunni. Þetta svar inniheldur fjárhagsleg gögn eins og auðkenniskóða ríkisfjármála og öryggiskóða viðskiptanna o.s.frv.
    - Prentaðu fjárhagsgögnin fyrir skráða færslu á kvittuninni.

- Skráning gjafakortastarfsemi og innlána viðskiptavina í skráningarþjónustu ríkisfjármála.

    - Gefðu út eða bættu peningum við gjafakort.
    - Skráðu innborgun á viðskiptareikning.
    - Búðu til viðskiptavinapöntun og skráðu innborgun fyrir pöntunina.
    - Breyttu pöntun viðskiptavinar og hnekktu innborgun fyrir pöntunina.
    - Hætta við pöntun viðskiptavinar og endurgreiða innborgun fyrir pöntunina.

- Villumeðferð, svo sem eftirfarandi valkostir.

    - Reyndu aftur fjárhagsskráningu ef hægt er að reyna aftur, eins og ef fjárhagsskráningarþjónustan er ekki tiltæk, er ekki tilbúin eða svarar ekki.
    - Fresta skattskráningu.
    - Slepptu skattaskráningu eða merktu viðskiptin sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Athugaðu framboð á fjárhagsskráningarþjónustunni áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="gift-cards"></a>Gjafakort

Samþættingarsýnishorn ríkisskráningarþjónustu innleiðir eftirfarandi reglur sem tengjast gjafakortum.

- Sölulínur sem tengjast *Gefa út gjafakort* eða *Bæta við gjafakort* aðgerðir í sölufærslu eru merktar með sérstökum eiginleikum þegar viðskiptin eru skráð í ríkisskráningarþjónustu.
- Greiðsla með gjafakorti telst venjuleg greiðsla og merkt með sérstökum eiginleikum þegar viðskiptin eru skráð í skráningarþjónustu ríkisskattstjóra.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Innlán á reikningi viðskiptavina og pöntun viðskiptavina

Samþættingarsýnishorn fjárhagsskráningarþjónustu innleiðir eftirfarandi reglur sem tengjast innlánum viðskiptavinareikninga og innlánum viðskiptavinapöntunar.

- Færsla sem tengist innborgun viðskiptavinareiknings eða innborgun viðskiptavinarpöntunar er skráð í fjárhagsskráningarþjónustuna sem einlínufærsla og er merkt með sérstökum eiginleikum. Innlánsvirðisaukaskattsflokkurinn er tilgreindur í þessari línu.
- Þegar blendingur viðskiptavinarpöntun er búin til, það er viðskiptavinapöntun sem inniheldur vörur sem viðskiptavinurinn getur framkvæmt úr versluninni, svo og vörur sem verða sóttar eða sendar síðar, þá er færslan skráð í skattskráningarþjónustunni. inniheldur línur fyrir þær vörur sem gerðar eru, auk línu fyrir innborgun pöntunar.
- Greiðsla af viðskiptareikningi telst venjuleg greiðsla og merkt með sérstökum eiginleikum þegar viðskiptin eru skráð í ríkisskráningarþjónustuna.
- Innborgunarupphæð viðskiptavinapöntunar sem er notuð á pöntun viðskiptavinar *Taktu upp* rekstur telst regluleg greiðsla og merkt með sérstökum eiginleikum þegar viðskiptin eru skráð í ríkisskráningarþjónustu.

### <a name="offline-registration"></a>Ónettengd skráning

Ef skattaskráningarþjónustan tekst ekki að senda færslugögn til ríkisskattavefþjónustu skattyfirvalda (til dæmis vegna svarfrests) og að fá staðfestingu frá vefþjónustunni (þ.e. auðkenniskóða færslunnar), það býr til staðbundna undirskrift fyrir viðskiptin og inniheldur hana og sérstakan villukóða í svarinu. Fjármálaskráningarþjónustan sendir færslur aftur í upprunalegri röð í bakgrunni um leið og nettengingin er endurheimt.

### <a name="limitations-of-the-sample"></a>Takmarkanir úrtaksins

Skattskráningarþjónustan styður aðeins aðstæður þar sem söluskattur er innifalinn í verðinu. Þess vegna er **Verð er með söluskatti** valkostur verður að vera stilltur á **Já** fyrir bæði verslanir og viðskiptavini.

## <a name="set-up-commerce-for-the-czech-republic"></a>Settu upp Commerce fyrir Tékkland

Þessi hluti lýsir viðskiptastillingum sem eru sértækar og mælt er með fyrir Tékkland. Fyrir frekari upplýsingar, sjá [Heimasíða verslunar](../index.md).

Til að nota tékkneska sérstaka virkni verður þú að tilgreina eftirfarandi stillingar.

- Í aðal heimilisfangi lögaðilans, stilltu **Land/svæði** sviði til **CZE** (Tékkland).
- Í POS virknisniði hverrar verslunar sem er staðsett í Tékklandi, stilltu **ISO kóða** sviði til **CZ** (Tékkland).

Þú verður einnig að tilgreina eftirfarandi stillingar fyrir Tékkland. Athugaðu að þú verður að keyra viðeigandi dreifingarverk eftir að þú hefur lokið uppsetningunni.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Settu upp VSK í samræmi við kröfur Tékklands


Þú verður að búa til VSK-kóða, VSK-flokka og VSK-flokka vöru. Þú verður einnig að setja upp upplýsingar um söluskatt fyrir vörur og þjónustu. Fyrir frekari upplýsingar um hvernig á að setja upp og nota söluskattseiginleika, sjá [Söluskattyfirlit](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Settu upp verslanir

Á **Allar verslanir** síðu, uppfærðu upplýsingar um verslunina. Nánar tiltekið skaltu stilla eftirfarandi færibreytur.

- Í **Vöruskattshópur** reit, tilgreinið vsk-flokkinn sem ætti að nota fyrir sölu til sjálfgefna viðskiptamanns.
- Stilltu **Verð eru með söluskatti** valmöguleika til **Já**.
- Stilltu **Nafn** reit við nafn fyrirtækis. Þessi breyting hjálpar til við að tryggja að nafn fyrirtækis komi fram á sölukvittun. Að öðrum kosti er hægt að bæta nafni fyrirtækis við útlit sölukvittana sem texta í frjálsu formi.
- Stilltu **Skattkennisnúmer (TIN)** reit á kennitölu fyrirtækisins. Þessi breyting hjálpar til við að tryggja að kenninúmer fyrirtækisins komi fram á sölukvittun. Að öðrum kosti er hægt að bæta kennitölu fyrirtækis við útlit sölukvittana sem texta í frjálsu formi.

### <a name="set-up-functionality-profiles"></a>Settu upp virknisnið

Settu upp POS virkniprófíla.

- Á **Númer kvittunar** Flýtiflipi, settu upp númer kvittunar með því að búa til eða uppfæra færslur fyrir **Útsala**, **·**, og **Til baka** tegundir kvittunarfærslu.

### <a name="set-up-registration-numbers"></a>Settu upp skráningarnúmer

1. Fara til **Stjórn stofnunarinnar \> Heimilisfangabók \> Skráningargerðir \> Skráningargerðir**. Búðu til nýja skráningartegund. Tilgreindu **Land/svæði** sviði til **CZE** (Tékkland) og takmarka það við stofnunina.
2. Fara til **Stjórn stofnunarinnar \> Heimilisfangabók \> Skráningargerðir \> Skráningarflokkar**. Búðu til nýjan skráningarflokk. Veldu skráningartegundina úr fyrra skrefi og stilltu **Skráningarflokkur** til **Auðkenni viðskiptaforsendna**.
3. Farið í **Fyrirtækisstjórnun \> Fyrirtæki \> Rekstrareiningar**. Veldu einingu sem tengist versluninni fyrir hverja verslun sem staðsett er í Tékklandi. Á **Heimilisfang** Flýtiflipi stækkaðu **Fleiri valkostir** fellilistanum og veldu **Ítarlegri**. 
4. Á opnuðu **Stjórna heimilisföngum** síðu sem þú verður að tilgreina eftirfarandi stillingu.

    - Á **Heimilisfang** Flýtiflipi stillir **Land/svæði** sviði til **CZE**.
    - Á **Skráningarauðkenni** Flýtiflipi búa til nýja færslu. Veldu skráningartegundina sem var búin til áður og stilltu skráningarnúmerið.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Stilltu sérsniðna reiti þannig að hægt sé að nota þá á kvittunarsniði fyrir sölukvittanir

Þú getur stillt tungumálatextann og sérsniðna reiti sem eru notaðir í POS kvittunarsniðum. Sjálfgefið fyrirtæki notandans sem býr til kvittunaruppsetninguna ætti að vera sami lögaðili og tungumálatextauppsetningin er búin til. Að öðrum kosti ætti að búa til sömu tungumálatexta bæði í sjálfgefnu fyrirtæki notanda og lögaðila verslunarinnar sem uppsetningin er búin til fyrir.

Á **Tungumálatexti** síðu, bætið við eftirfarandi skrám fyrir merki sérsniðnu reitanna fyrir kvittunarútlit. Athugið að **Tungumálakenni**, **·**, og **Texti** gildin sem eru sýnd í töflunni eru aðeins dæmi. Þú getur breytt þeim til að uppfylla kröfur þínar. Hins vegar er **Textaauðkenni** gildi sem þú notar verða að vera einstök og þau verða að vera jöfn eða hærri en 900001.

Bættu eftirfarandi POS-merkjum við **POS** kafla af **Tungumálatexti** frá borði:

| Kenni tungumáls | Textakenni | Texti                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID provozovny/pokladny |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Uppl                   |
| en-US       | 900006  | Raðnúmer        |

Á **Sérsniðnir reitir** síðu skaltu bæta við eftirfarandi færslum fyrir sérsniðna reiti fyrir útlit kvittunar. Athugið að **Textaauðkenni fyrir texta** gildi verða að samsvara **Textaauðkenni** gildi sem þú tilgreindir á **Tungumálatexti** síða:

| Heiti                 | Gerð    | Textakenni myndatexta |
|----------------------|---------|-----------------|
| TLT                  | Innhreyfing | 900001          |
| SEC                  | Innhreyfing | 900002          |
| SKILTIÐ                 | Innhreyfing | 900003          |
| FJÁRSLAG               | Innhreyfing | 900004          |
| UPPLÝSINGAR                 | Innhreyfing | 900005          |
| STAÐFULLT     | Innhreyfing | 900006          |

> [!NOTE]
> Það er mikilvægt að þú tilgreinir rétt sérsniðin svæðisheiti eins og þau eru skráð í töflunni á undan. Rangt sérsniðið heiti svæðis mun valda því að gögn vantar í kvittanir.

### <a name="configure-receipt-formats"></a>Stilltu kvittunarsnið

Fyrir hvert áskilið kvittunarsnið, breyttu gildinu **Prenthegðun** sviði til **Alltaf að prenta**.

Í hönnuður kvittunarsniðs skaltu bæta eftirfarandi sérsniðnum reitum við viðeigandi kvittunarhluta. Athugaðu að svæðisnöfn samsvara tungumálatextanum sem þú skilgreindir í fyrri hlutanum.

- **Fyrirsögn:** Bættu við eftirfarandi reitum.

    - **Nafn verslunar** og **Skattkennisnúmer** : þessir reitir eru notaðir til að prenta nafn fyrirtækis og kennitölu á kvittanir. Að öðrum kosti er hægt að bæta nafni fyrirtækis og kennitölu við útlitið sem texta í frjálsu formi.
    - **Heimilisfang verslunar**, **·**, **24H**, **·**, og **Skráningarnúmer**.
    - **Raðnúmer** : þessi reitur auðkennir númer reiðufjárfærslunnar í skattaskráningarþjónustunni.

- **Línur:** Bættu við eftirfarandi reitum.

    - **Vöruheiti**
    - **Magn**
    - **Heildarverð með sköttum**

- **Fótur:** Bættu við eftirfarandi reitum.

    - Greiðslureitir, þannig að greiðsluupphæðir fyrir hvern greiðslumáta eru prentaðar. Til dæmis, bæta við **Nafn tilboðs** og **Útboðsfjárhæð** reiti í eina línu í útlitinu.
    - **ID provozovny/pokladny** : þessi reitur prentar út auðkenni atvinnuhúsnæðis og sjóðsvélar.
    - **BKP** : þessi reitur prentar út öryggiskóða skattgreiðanda sem er úthlutað af skattskráningarþjónustunni.
    - **FIK** : Þessi reitur prentar út ríkisauðkenniskóða færslunnar sem er úthlutað af vefþjónustu skattyfirvalda ef netskráning gengur vel.
    - **PKP** : þessi reitur prentar út undirskriftarkóða skattgreiðanda sem er búinn til af skattaskráningarþjónustunni ef um er að ræða ónettengda skráningu.
    - **Upplýsingar** : þessi reitur prentar út viðbótarupplýsingarnar frá skattaskráningarþjónustunni.

Fyrir frekari upplýsingar um hvernig á að vinna með kvittunarsnið, sjá [Setja upp og hanna kvittunarsnið](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Settu upp ríkisfjármálasamþættingu fyrir Tékkland

Samþættingarsýni skattaskráningarþjónustu fyrir Tékkland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Efr** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Tékkland (arfleifð)](emea-cze-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md):

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu einnig eftir þeim stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta samþættingarsýni fyrir ríkisskráningarþjónustu](#set-up-the-registration-process).
1. [Stilltu stillingar fyrir villumeðferð](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Virkja handvirka framkvæmd frestaðrar fjárhagsskráningar](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Settu upp skráningarferlið

Til að virkja skráningarferlið skaltu fylgja þessum skrefum til að setja upp höfuðstöðvar Commerce. Fyrir frekari upplýsingar, sjá [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Sæktu stillingarskrár fyrir fjárhagsskjalaveituna og fjárhagstengið:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína (til dæmis, **[útgáfa/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Opið **src \> Fiscal Integration \> Efr**.
    1. Sæktu stillingarskrá ríkisskjalaveitunnar á **Stillingar \> Skjalaveitendur \> DocumentProviderFiscalEFRSampleCzech.xml** (til dæmis, [skrána til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)).
    1. Sæktu stillingarskrá fjárhagstengis á **Stillingar \> Tengi \> Tengi EFRSample.xml** (til dæmis, [skráin til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrá ríkisskjalaveitu:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Stillingar\\ DocumentProviderFiscalEFRSampleCzech.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Framlenging.EFRSample\\ Stillingar\\ Tengi EFRSample.xml
    > 
    > Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingaskrá fjárhagsskjalaveitunnar sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú sóttir áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tengi virka snið**. Búðu til nýtt virknisnið fyrir tengi. Veldu skjalaveituna og tengið sem þú hleður inn áðan. Uppfærðu [gagnakortastillingar](#default-data-mapping) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýja tæknisnið fyrir tengi og veldu fjárhagstengi sem þú hleður inn áðan. Uppfærðu [tengistillingar](#fiscal-connector-settings) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**. Stofna nýjan fjárhagstengihóp fyrir virknisniðið tengi sem þú bjóst til áður.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**. Búðu til nýtt fjárhagsskráningarferli og fjárhagsskráningarferlisþrep og veldu fjárhagstengihópinn sem þú stofnaðir áðan.
1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veldu virknisnið sem er tengt við verslunina þar sem skráningarferlið á að virkja. Á **Skráningarferli í ríkisfjármálum** Flýtiflipi, veldu fjárhagsskráningarferlið sem þú bjóst til áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Veldu vélbúnaðarsnið sem er tengt við vélbúnaðarstöðina sem fjárhagsprentarinn verður tengdur við. Á **Jaðartæki í ríkisfjármálum** Flýtiflipi, veldu tæknisniðið sem þú bjóst til áðan.
1. Opnaðu dreifingaráætlun (**Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**), og veldu störf **1070** og **1090** að flytja gögn í rásargagnagrunninn.

#### <a name="default-data-mapping"></a>Sjálfgefin gagnakortlagning

Eftirfarandi sjálfgefna gagnavörpun er innifalin í uppsetningu fjárhagsskjalaveitu sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Kortlagning virðisaukaskatts (VSK) taxta** – Kortlagning skattprósentugilda sem eru sett upp fyrir vsk-kóða við gildi á **TaxG** (skattflokkur) eigind í beiðnum sem sendar eru til ríkisskattstjóra. Hér er sjálfgefið kortlagning:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Fyrsti þátturinn í hverju pari táknar virðisaukaskattsflokk sem er studdur af EFR skattaskráningarþjónustunni. Annar þátturinn táknar samsvarandi virðisaukaskattshlutfall. Fyrir frekari upplýsingar um virðisaukaskattshópa sem EFR styður fyrir Tékkland, sjá [EFR tilvísun](https://public.efsta.net/efr/).

- **Sjálfgefin vsk hópkortlagning** – Allar virðisaukaskattsupphæðir sem ekki er hægt að kortleggja á einhvern af fyrirfram ákveðnum virðisaukaskattsflokkum verða færðar til sjálfgefna (grunn) VSK hópsins. Hér er sjálfgefið kortlagning:

    ```
    A
    ```

- **Kortlagning innlánsvirðisaukaskatts** – Innborgunarupphæðir viðskiptavina og innborgunarupphæðir viðskiptavinapöntunar verða færðar til VSK-hópsins. Hér er sjálfgefið kortlagning:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru innifalin í fjárhagstengistillingunni sem er hluti af fjárhagssamþættingarsýninu:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum, sem fjárhagstengi bíður eftir svari frá fjárhagsskráningarþjónustunni.

### <a name="configure-channel-components"></a>Stilltu rásaríhluti

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Tékkland (arfleifð)](emea-cze-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

#### <a name="set-up-the-development-environment"></a>Settu upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og stækka sýnishornið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla. Veldu rétta útgáfu útibús í samræmi við SDK/forritsútgáfu þína. Fyrir frekari upplýsingar, sjá [Sæktu smásölu SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
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

1. Settu upp vélbúnaðarstöðvarviðbætur:

    1. Í **Efr\\ Vélbúnaðarstöð\\ HardwareStation.EFR.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.EFR.Installer** uppsetningarforrit.
    1. Byrjaðu uppsetningarforritið frá skipanalínunni:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgdu skrefunum í [Settu upp smíðisleiðslu fyrir sýnishorn fjárhagslega samþættingar](fiscal-integration-sample-build-pipeline.md) að búa til og gefa út Cloud Scale Unit og sjálfsafgreiðslupakka fyrir samþættingarúrtakið í ríkisfjármálum. The **EFR build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarsýni skattaskráningarþjónustu fyrir Tékkland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Efr** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ríkisfjármálaskjalaveitanda, sem er framlenging á CRT, og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarúrtak í ríkisfjármálum fyrir Tékkland (arfleifð)](emea-cze-fi-sample-sdk.md). Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur framlengingarinnar sem er ríkisfjármálaskjalaveita er að búa til þjónustusértæk skjöl og sjá um svör frá ríkisskráningarþjónustunni.

#### <a name="request-handler"></a>Beiðni um stjórnanda

Það er einn **DocumentProviderEFRFiscalCZE** beiðni meðhöndlun fyrir skjalaveitanda, sem er notað til að búa til fjárhagsskjöl fyrir skattskráningarþjónustuna.

Þessi meðhöndlari er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir.

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í ríkisskráningarþjónustunni.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er eru eftirfarandi viðburðir studdir: sala, innlán á viðskiptareikningi og innborgun viðskiptavinarpöntunar.
- **Get FiscalRegisterResponseToSaveDocumentProviderRequest** – Þessi beiðni skilar svari frá skattskráningarþjónustunni. Þetta svar er sett í röð til að mynda streng þannig að það sé tilbúið til vistunar.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir ríkisfjármálaskjalaveituna er staðsett á **src\\ FiscalIntegration\\ Efr\\ Stillingar\\ Skjalaveitendur\\ DocumentProviderFiscalEFRSampleCzech.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera það kleift að stilla stillingar ríkisfjármálaskjalaveitunnar frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur framlengingarinnar sem er fjárhagstengi er að hafa samskipti við skattskráningarþjónustuna. Vélbúnaðarstöðvarviðbótin notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar við skattskráningarþjónustuna. Það sér einnig um svör sem berast frá ríkisskráningarþjónustu.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **EFRHandler** meðhöndlun beiðna er inngangsstaður fyrir meðhöndlun beiðna til skattskráningarþjónustunnar.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem tilgreint er í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir.

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ Fiscal Integration\\ Efr\\ Stillingar\\ Tengi\\ Tengi EFRSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera kleift að stilla stillingar á fjárhagstenginu frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

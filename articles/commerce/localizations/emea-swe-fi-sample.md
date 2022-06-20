---
title: Dæmi um samþættingu stjórntækja fyrir Svíþjóð
description: Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Svíþjóð í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 11ce0b146f2e64092b0d03dc7416660d76380cd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885403"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Dæmi um samþættingu stjórntækja fyrir Svíþjóð

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Svíþjóð í Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Þessi sýnishorn fjárhagslega samþættingarvirkni kemur í stað fyrri [sýnishorn fyrir POS samþættingu við stjórneiningar fyrir Svíþjóð](retail-sdk-control-unit-sample.md). Fyrra sýnishornið nýtir sér ekki [ramma um samþættingu ríkisfjármála](./fiscal-integration-for-retail-channel.md) og verður úrelt í síðari uppfærslum. Til að fá upplýsingar um hvernig á að flytja úr fyrra úrtakinu yfir í úrtakið sem samsvarar Dynamics 365 Commerce útgáfu **10.0.22 og fyrr**, sjá [Flutningur frá fyrra samþættingarúrtaki](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Viðskiptavirknin fyrir Svíþjóð felur í sér sýnishorn af samþættingu sölustaðarins (POS) við Svíþjóðarsértæk skattatæki sem eru þekkt sem *stjórneiningar*. Þetta sýnishorn framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Gert er ráð fyrir að stýrieining sé líkamlega tengd við vélbúnaðarstöð sem POS er parað við. Sem dæmi notar þetta sýnishorn forritunarviðmót (API) á [CleanCash Tegund A](https://www.retailinnovation.se/produkter) stýrieining frá Retail Innovation HTT AB. Útgáfa 1.1.4 af CleanCash API er notuð.

Sýnishornið er gefið í formi frumkóða og er hluti af Retail hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá Retail Innovation HTT AB. Fyrir upplýsingar um hvernig á að ná í stýrieininguna og stjórna henni, hafðu samband við [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Aðstæður

Samþættingarsýni stjórneininga fyrir Svíþjóð inniheldur eftirfarandi eiginleika:

- Sölu-, skila- og kvittunarafrit eru sjálfkrafa skráð í stjórneiningu sem er tengd við vélbúnaðarstöðina sem er pöruð við POS.
- Stýrikóði og framleiðslunúmer stýrieiningarinnar fyrir skráð viðskipti eru tekin úr stjórneiningunni og vistuð í viðskiptunum. Þessi gögn eru einnig nefnd a *viðbrögð í ríkisfjármálum*. Viðbrögð ríkisfjármála má sjá á **Verslunarviðskipti** síðu.
- Hægt er að bæta sérsniðnum reitum fyrir stýrikóðann og framleiðslunúmer stýrieiningarinnar við kvittunarútlit. Þannig geturðu prentað fjárhagslegt svar fyrir færslu á kvittun.
- Fjárhagslegt svar fyrir færslu er sýnt á **Rafræn dagbók (Svíþjóð)** skýrslu rásarinnar.
- Nokkrir valkostir til að meðhöndla villu eru í boði. Hér eru nokkur dæmi:

    - Reyndu aftur fjárhagsskráningu, ef hægt er að reyna aftur. Þú getur reynt aftur fjárhagsskráningu ef, til dæmis, stjórneiningin er ekki tengd, er ekki tilbúin eða svarar ekki.
    - Fresta skattskráningu.
    - Slepptu skattaskráningu eða merktu viðskiptin sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Staðfestu framboð á stýrieiningunni áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="limitations-of-the-sample"></a>Takmarkanir úrtaksins

Samþættingarsýnishorn stýrieininga fyrir Svíþjóð styður sem stendur ekki atburðarás viðskiptavinapöntunar.

## <a name="setting-up-the-integration-with-control-units"></a>Uppsetning samþættingar við stýrieiningar

Fyrir frekari upplýsingar um uppsetninguna sem þarf fyrir Svíþjóð, sjá [Uppsetning viðskipta fyrir Svíþjóð](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Stilla kvittanir fyrir Svíþjóð

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Stilltu sérsniðna reiti þannig að hægt sé að nota þá á kvittunarsniði fyrir sölukvittanir

Þú getur stillt tungumálatextann og sérsniðna reiti sem eru notaðir í POS kvittunarsniðum. Sjálfgefið fyrirtæki notandans sem býr til kvittunaruppsetninguna ætti að vera sami lögaðili og tungumálatextauppsetningin er búin til. Að öðrum kosti ætti að búa til sömu tungumálatexta bæði í sjálfgefnu fyrirtæki notanda og lögaðila verslunarinnar sem uppsetningin er búin til fyrir.

Á **Tungumálatexti** síðu, bætið við eftirfarandi skrám fyrir merki sérsniðnu reitanna fyrir kvittunarútlit. Athugið að **Tungumálakenni**, **·**, og **Texti** gildin sem eru sýnd í töflunni eru aðeins dæmi. Þú getur breytt þeim til að uppfylla kröfur þínar. Hins vegar er **Textaauðkenni** gildi sem þú notar verða að vera einstök og þau verða að vera jöfn eða hærri en 900001.

Bættu við eftirfarandi POS-merkjum í **POS** kafla í **Tungumálatexti** síðu.

| Kenni tungumáls | Textakenni | Texti                  |
|-------------|---------|-----------------------|
| is       | 900001  | Skráðu stjórnkóða |
| is       | 900002  | Skráðu tæki       |

Á **Sérsniðnir reitir** síðu skaltu bæta við eftirfarandi færslum fyrir sérsniðna reiti fyrir útlit kvittunar. Athugið að **Textaauðkenni fyrir texta** gildi verða að samsvara **Textaauðkenni** gildi sem þú tilgreindir á **Tungumálatexti** síðu.

| Nafn                         | Gerð    | Textakenni myndatexta |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Innhreyfing | 900001          |
| SE_FISCALREGISTERID          | Innhreyfing | 900002          |

> [!NOTE]
> Það er mikilvægt að þú tilgreinir rétt sérsniðin svæðisheiti eins og þau eru skráð í töflunni hér að ofan. Rangt sérsniðið heiti svæðis mun valda því að gögn vantar í kvittanir.

#### <a name="configure-receipt-formats"></a>Stilltu kvittunarsnið

Breyttu gildinu fyrir hvert kvittunarsnið sem þarf **Prenthegðun** sviði til **Alltaf að prenta**.

Í kvittunarsniðshönnuður skaltu bæta eftirfarandi sérsniðnum reitum við **Fótur** kafla. Athugaðu að svæðisnöfn samsvara tungumálatextanum sem þú skilgreindir í fyrri hluta þessarar greinar.

- **Skráðu stjórnkóða** – Þessi reitur prentar stjórnkóðann.
- **Skráðu tæki** – Þessi reitur prentar út framleiðslunúmer stýrieiningarinnar.

Fyrir frekari upplýsingar um hvernig á að vinna með kvittunarsnið, sjá [Kvittunarsniðmát og prentun](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Settu upp ríkisfjármálasamþættingu fyrir Svíþjóð

Samþættingarúrtak stjórneiningar fyrir Svíþjóð er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ CleanCash** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)](emea-swe-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md).

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu einnig eftir þeim stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta samþættingarsýni stjórneininga](#set-up-the-registration-process).
1. [Stilltu stillingar fyrir villumeðferð](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Virkja handvirka framkvæmd frestaðrar fjárhagsskráningar](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Settu upp skráningarferlið

Til að virkja skráningarferlið skaltu fylgja þessum skrefum til að setja upp höfuðstöðvar Commerce. Fyrir frekari upplýsingar, sjá [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Sæktu stillingarskrár fyrir fjárhagsskjalaveituna og fjárhagstengið:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína (td, **[útgáfa/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Opið **src \> Fiscal Integration \> CleanCash**.
    1. Sæktu stillingarskrá ríkisskjalaveitunnar á **CommerceRuntime \> DocumentProvider.CleanCashSample \> Stillingar \> DocumentProviderFiscalCleanCashSample.xml** (til dæmis, [skrána til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Sæktu stillingarskrá fjárhagstengis á **Vélbúnaðarstöð \> Connector.CleanCashSample \> Stillingar \> ConnectorCleanCashSample.xml** (til dæmis, [skráin til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrá ríkisskjalaveitu:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extensions.DocumentProvider.CleanCashSample\\ Stillingar\\ DocumentProviderFiscalCleanCashSample.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Framlenging.CleanCashSample\\ Stillingar\\ ConnectorCleanCashSample.xml
    > 
    > Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingaskrá fjárhagsskjalaveitunnar sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú sóttir áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tengi virka snið**. Búðu til nýtt virknisnið fyrir tengi. Veldu skjalaveituna og tengið sem þú hleður inn áðan. Uppfærðu [gagnakortastillingar](#default-data-mapping) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýja tæknisnið fyrir tengi og veldu fjárhagstengi sem þú hleður inn áðan. Uppfæra stillingar tengisins eftir [þörfum](#fiscal-connector-settings).
6. Fara í **Uppsetningu \> fjárhagssamþættingar fjárhagssamþættingar \> fjárhagstengsla í smásölu og Commerce \> Channel**. Stofna nýjan fjárhagstengiflokk fyrir virknireglu tengisins sem var stofnuð áður.
7. Fara í **uppsetningu á fjárhagssamþættingu \>\> fjárhagssamþættingar \> fjárhags**. Stofna nýtt fjárhagsskráningarferli og skref fjárhagsskráningarferlis og velja fjárhagstengiflokkinn sem var stofnaður áður.
8. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veljið virknireglu sem er tengd versluninni þar sem virkja á skráningarferlið. Á flýtiflipanum **Fjárhagsskráningarferli** skal velja fjárhagsskráningarferlið sem var stofnað áður.
9. Fara í **Retail and Commerce \> Channel setup \> POS uppsetning \> POS-forstillinga \> Vélbúnaðarforstillingar**. Velja vélbúnaðarforstillingu sem er tengd vélbúnaðarstöðinni sem strimlaprentarinn verður tengdur við. Á flýtiflipanum **Útlimir** fjárhags skal velja tækniforstillingu tengisins sem var stofnuð áður.
10. Opnið dreifingaráætlunina (**Retail and Commerce Retail og Commerce \> Retail og Commerce IT \> Distribution schedule)** og veljið vinnslur **1070** og **1090** til að flytja gögn í rásargagnagrunninn.

#### <a name="default-data-mapping"></a>Sjálfgefin gagnavörpun

Eftirfarandi sjálfgefin gagnavörpun er innifalin í skilgreiningu fjárhagsskjalaveitunnar sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Kortlagning virðisaukaskatts (VSK) kóða** – Þessi kortlagning stillir tækjasértæka virðisaukaskattskóða (VSK) á samsvarandi söluskattskóða. VSK-kóðavörpun ætti að hafa eftirfarandi snið:

    ```
    1 : code1 ; 2 : code2
    ```

    Hér er útskýring á þessu sniði:

    - *1* og *2* eru tækjasértækir VSK-kóðar.
    - Semíkomma (;) er notað sem skil.
    - *kóða1* og *kóða2* eru söluskattskóðar sem eru stilltir í höfuðstöðvum Commerce. Þú verður að breyta sýnishorninu í samræmi við skattkóðana sem eru stilltir í forritinu þínu.

    Stýrieiningar styðja allt að fjóra mismunandi VSK-kóða. Þess vegna gæti VSK kóða kortlagningin verið sett upp á eftirfarandi hátt:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Hægt er að kortleggja marga VSK-kóða á sama tækjasértæka VSK-kóða.

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru teknar með í skilgreiningu fjárhagstengisins sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Tengingarstrengur** – Tengingarstillingar stjórneiningar.
- **Tímamörk** – Tíminn, í millisekúndum, sem rekillinn bíður eftir svari frá stjórneiningunni.

### <a name="configure-channel-components"></a>Skilgreina rásaríhluti

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)](emea-swe-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

#### <a name="set-up-the-development-environment"></a>Setja upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og lengja sýnið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður lausnageymslunni [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Veldu rétta útgáfu útgáfu útibús í samræmi við SDK / umsóknarútgáfuna þína. Frekari upplýsingar er að finna í [Download Retail SDK sýni og tilvísunarpakkar frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu samþættingarlausn stjórneiningar kl **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ CleanCash\\ CleanCash.sln**, og byggja það.
1. Setja upp CRT viðbætur:

    1. Finndu uppsetningarforrit viðbótarinnar CRT:

        - **Eining viðskiptaskala:** Í **CleanCash\\ ScaleUnit\\ ScaleUnit.CleanCash.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ScaleUnit.CleanCash.Installer** uppsetningarforrit.
        - **Staðbundið CRT á Modern POS:** Í **CleanCash\\ ModernPOS\\ ModernPOS.CleanCash.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ModernPOS.CleanCash.Installer** uppsetningarforrit.

    2. Ræsa uppsetningarforrit viðbótarinnar CRT úr skipanalínunni:

        - **Mælieining viðskiptakvarða:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á modern POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Setja upp viðbætur vélbúnaðarstöðvar:

    1. Í **CleanCash\\ Vélbúnaðarstöð\\ HardwareStation.CleanCash.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.CleanCash.Installer** uppsetningarforrit.
    1. Ræsa uppsetningarforrit viðbótarinnar úr skipanalínunni:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgið skrefunum í [Setja upp byggingarpípu fyrir fjárhagssamþættingarsýni](fiscal-integration-sample-build-pipeline.md) til að búa til og losa skýjaskalaeininguna og virkjanlega sjálfsafgreiðslupakka fyrir fjárhagssamþættingarsýnið. The **CleanCash build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-the-extensions"></a>Hönnun viðbætur

Samþættingarúrtak stjórneiningar fyrir Svíþjóð er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ CleanCash** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Sýnið [samanstendur af veitu fjárhagsskjala](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services), sem er viðbót við CRT og fjárhagstengi, sem er viðbót við vélbúnaðarstöð Commerce. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)](emea-swe-fi-sample-sdk.md). Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

### <a name="crt-extension-design"></a>CRT viðaukahönnun

Tilgangur viðbótarinnar sem er fjármálaskjalsveita er að búa til þjónustutengd skjöl og meðhöndla svör frá stjórneiningunni.

#### <a name="request-handler"></a>Biðja um rekil

Það er einn **DocumentProviderCleanCash** beiðnistjóri fyrir skjalaveituna. Þessi rekill er notaður til að búa til fjárhagsskjöl fyrir stjórneininguna.

Þessi rekill erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti tengiskjalsveitunnar sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal á að mynda. Það skilar þjónustutengdu skjali sem ætti að skrá í stjórneininguna.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir tilvik sem á að gerast áskrifandi að. Eins og er eru söluviðburðir og endurskoðunarviðburðir studdir.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagsskjalaveituna er staðsett á **src\\ Fiscal Integration\\ CleanCash\\ CommerceRuntime\\ DocumentProvider.CleanCashSample\\ Stillingar\\ DocumentProviderFiscalCleanCashSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur þessarar skrár er að virkja stillingar fyrir skjalaveituna sem skilgreina á úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar.

### <a name="hardware-station-extension-design"></a>Viðaukahönnun vélbúnaðarstöðvar

Tilgangur nafnaukans sem er fjárhagstengi er að hafa samskipti við stjórneininguna. Það notar HTTP-samskiptareglurnar til að senda skjöl sem viðbótin CRT myndar til stjórneiningarinnar. Hún sér einnig um svörin sem berast frá stjórneiningunni.

#### <a name="request-handler"></a>Biðja um rekil

**CleanCashHandler** beiðnistjórinn er inngangsstaður fyrir meðhöndlun beiðna í stjórneininguna.

Rekillinn erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti fjárhagstengisins sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **SubmitDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til stjórnstöðvarinnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð við heilsufarsskoðun á stjórneiningunni.
- **InitializeFiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla stjórneininguna.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ Fiscal Integration\\ CleanCash\\ Vélbúnaðarstöð\\ Connector.CleanCashSample\\ Stillingar\\ ConnectorCleanCashSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að virkja stillingar fyrir fjárhagstengið sem skilgreina á úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

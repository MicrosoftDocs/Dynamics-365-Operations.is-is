---
title: Dæmi um samþættingu stjórntækja fyrir Svíþjóð
description: Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Svíþjóð í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 3376e6a901b692371a44b5c74c1e6b4afd0cd573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275067"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Dæmi um samþættingu stjórntækja fyrir Svíþjóð

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Svíþjóð í Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Þessi sýnishorn fjárhagslega samþættingarvirkni kemur í stað fyrri [sýnishorn fyrir POS samþættingu við stjórneiningar fyrir Svíþjóð](retail-sdk-control-unit-sample.md). Fyrra sýnishornið nýtir sér ekki [ramma um samþættingu ríkisfjármála](./fiscal-integration-for-retail-channel.md) og verður úrelt í síðari uppfærslum. Til að fá upplýsingar um hvernig á að flytja úr fyrra úrtakinu yfir í úrtakið sem samsvarar Dynamics 365 Commerce útgáfu **10.0.22 og fyrr**, sjá [Flutningur frá fyrra samþættingarúrtaki](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Viðskiptavirknin fyrir Svíþjóð felur í sér sýnishorn af samþættingu sölustaðarins (POS) við Svíþjóðarsértæk skattatæki sem eru þekkt sem *stjórneiningar*. Þetta sýnishorn framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Gert er ráð fyrir að stjórneining sé líkamlega tengd við vélbúnaðarstöð sem POS er parað við. Sem dæmi notar þetta sýnishorn forritunarviðmót (API) á [CleanCash Tegund A](https://www.retailinnovation.se/produkter) stýrieining frá Retail Innovation HTT AB. Útgáfa 1.1.4 af CleanCash API er notuð.

Sýnishornið er gefið í formi frumkóða og er hluti af Retail hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá Retail Innovation HTT AB. Fyrir upplýsingar um hvernig á að ná í stjórneininguna og stjórna henni, hafðu samband við [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Aðstæður

Samþættingarsýni stjórneininga fyrir Svíþjóð inniheldur eftirfarandi eiginleika:

- Sölu-, skila- og kvittunarafrit eru sjálfkrafa skráð í stjórneiningu sem er tengd vélbúnaðarstöðinni sem er pöruð við POS.
- Stýrikóði og framleiðslunúmer stýrieiningarinnar fyrir skráð viðskipti eru tekin úr stjórneiningunni og vistuð í viðskiptunum. Þessi gögn eru einnig nefnd a *viðbrögð í ríkisfjármálum*. Viðbrögð ríkisfjármála má sjá á **Verslunarviðskipti** síðu.
- Hægt er að bæta sérsniðnum reitum fyrir stjórnkóðann og framleiðslunúmer stýrieiningarinnar við kvittunarútlit. Þannig er hægt að prenta fjárhagslegt svar fyrir færslu á kvittun.
- Fjárhagslegt svar fyrir færslu er sýnt á **Rafræn dagbók (Svíþjóð)** rás skýrslu.
- Nokkrir valkostir til að meðhöndla villu eru í boði. Hér eru nokkur dæmi:

    - Reyndu aftur fjárhagsskráningu, ef hægt er að reyna aftur. Þú getur reynt aftur fjárhagsskráningu ef, til dæmis, stjórneiningin er ekki tengd, er ekki tilbúin eða svarar ekki.
    - Fresta skattskráningu.
    - Slepptu skattaskráningu eða merktu færsluna sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Staðfestu að stjórneiningin sé tiltæk áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="limitations-of-the-sample"></a>Takmarkanir úrtaksins

Samþættingarsýni stjórneininga fyrir Svíþjóð styður ekki eins og er pöntunarsviðsmyndir viðskiptavina.

## <a name="setting-up-the-integration-with-control-units"></a>Uppsetning samþættingar við stýrieiningar

Fyrir frekari upplýsingar um uppsetninguna sem þarf fyrir Svíþjóð, sjá [Uppsetning viðskipta fyrir Svíþjóð](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Stilla kvittanir fyrir Svíþjóð

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Stilltu sérsniðna reiti þannig að hægt sé að nota þá á kvittunarsniði fyrir sölukvittanir

Þú getur stillt tungumálatextann og sérsniðna reiti sem eru notaðir í POS kvittunarsniðum. Sjálfgefið fyrirtæki notandans sem býr til kvittunaruppsetninguna ætti að vera sami lögaðili og tungumálatextauppsetningin er búin til. Að öðrum kosti ætti að búa til sömu tungumálatexta bæði í sjálfgefnu fyrirtæki notanda og lögaðila verslunarinnar sem uppsetningin er búin til fyrir.

Á **Tungumálatexti** síðu, bætið við eftirfarandi færslum fyrir merki sérsniðnu reitanna fyrir kvittunarútlit. Athugið að **Tungumálakenni**, **·**, og **Texti** gildi sem eru sýnd í töflunni eru aðeins dæmi. Þú getur breytt þeim til að uppfylla kröfur þínar. Hins vegar er **Textakenni** gildi sem þú notar verða að vera einstök og þau verða að vera jöfn eða stærri en 900001.

Bættu við eftirfarandi POS-merkjum í **POS** kafla í **Tungumálatexti** síðu.

| Kenni tungumáls | Textakenni | Texti                  |
|-------------|---------|-----------------------|
| is       | 900001  | Skráðu stýrikóða |
| is       | 900002  | Skráðu tæki       |

Á **Sérsniðnir reitir** síðu, bætið við eftirfarandi færslum fyrir sérsniðna reiti fyrir móttökuútlit. Athugið að **Auðkenni textatexta** gildi verða að samsvara **Textakenni** gildi sem þú tilgreindir á **Tungumálatexti** síðu.

| Nafn                         | Gerð    | Textakenni myndatexta |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Innhreyfing | 900001          |
| SE_FISCALREGISTERID          | Innhreyfing | 900002          |

> [!NOTE]
> Það er mikilvægt að þú tilgreinir rétt sérsniðin svæðisheiti eins og þau eru skráð í töflunni hér að ofan. Rangt sérsniðið heiti svæðis mun valda því að gögn vantar í kvittanir.

#### <a name="configure-receipt-formats"></a>Stilltu kvittunarsnið

Breyttu gildinu fyrir hvert kvittunarsnið sem þarf **Prenthegðun** sviði til **Alltaf að prenta**.

Í kvittunarsniðshönnuður skaltu bæta eftirfarandi sérsniðnum reitum við **Fótur** kafla. Athugaðu að svæðisnöfn samsvara tungumálatextanum sem þú skilgreindir í fyrri hluta þessarar greinar.

- **Skráðu stýrikóða** – Þessi reitur prentar stjórnkóðann.
- **Skráðu tæki** – Þessi reitur prentar framleiðslunúmer stýrieiningarinnar.

Fyrir frekari upplýsingar um hvernig á að vinna með kvittunarsnið, sjá [Kvittunarsniðmát og prentun](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Settu upp ríkisfjármálasamþættingu fyrir Svíþjóð

Samþættingarúrtak stjórneiningar fyrir Svíþjóð er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ CleanCash** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)](emea-swe-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md).

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu einnig eftir stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta samþættingarsýni stjórneininga](#set-up-the-registration-process).
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
    1. Sæktu stillingarskrá fjárhagstengis á **Vélbúnaðarstöð \> Connector.CleanCashSample \> Stillingar \> ConnectorCleanCashSample.xml** (til dæmis, [skrána til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrá ríkisskjalaveitanda:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extensions.DocumentProvider.CleanCashSample\\ Stillingar\\ DocumentProviderFiscalCleanCashSample.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Extension.CleanCashSample\\ Stillingar\\ ConnectorCleanCashSample.xml
    > 
    > Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingarskrá fjárhagsskjalaveitunnar sem þú sóttir áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tengi virkni snið**. Búðu til nýtt virknisnið fyrir tengi. Veldu skjalaveituna og tengið sem þú hleður inn áðan. Uppfærðu [gagnakortastillingar](#default-data-mapping) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýtt tæknisnið fyrir tengi og veldu fjárhagstengi sem þú hleður inn áðan. Uppfærðu [tengistillingar](#fiscal-connector-settings) eins og krafist er.
6. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**. Stofna nýjan fjárhagstengihóp fyrir virknisniðið tengi sem þú bjóst til áður.
7. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**. Stofna nýtt fjárhagsskráningarferli og fjárhagsskráningarferlisþrep og velja fjárhagstengihópinn sem þú stofnaðir áðan.
8. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veldu virknisnið sem er tengt við verslunina þar sem skráningarferlið á að virkja. Á **Skráningarferli í ríkisfjármálum** Flýtiflipi, veldu fjárhagsskráningarferlið sem þú bjóst til áðan.
9. Fara til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Veldu vélbúnaðarsnið sem er tengt við vélbúnaðarstöðina sem fjárhagsprentarinn verður tengdur við. Á **Jaðartæki í ríkisfjármálum** Flýtiflipi, veldu tæknisniðið sem þú bjóst til áðan.
10. Opnaðu dreifingaráætlun (**Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**), og veldu störf **1070** og **1090** að flytja gögn í rásargagnagrunninn.

#### <a name="default-data-mapping"></a>Sjálfgefin gagnakortlagning

Eftirfarandi sjálfgefna gagnavörpun er innifalin í uppsetningu fjárhagsskjalaveitu sem er veitt sem hluti af fjárhagssamþættingarsýninu:

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

Eftirfarandi stillingar eru innifaldar í fjárhagstengistillingunni sem er hluti af fjárhagssamþættingarsýninu:

- **Tengingarstrengur** – Tengistillingar stýrieiningarinnar.
- **Hlé** – Tíminn, í millisekúndum, sem ökumaður bíður eftir svari frá stjórneiningunni.

### <a name="configure-channel-components"></a>Stilltu rásaríhluti

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)](emea-swe-fi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

#### <a name="set-up-the-development-environment"></a>Settu upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og stækka úrtakið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína. Fyrir frekari upplýsingar, sjá [Sæktu smásölu SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu samþættingarlausn stjórneiningar kl **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ CleanCash\\ CleanCash.sln**, og byggja það.
1. Settu upp CRT viðbætur:

    1. Finndu CRT uppsetningarforrit fyrir viðbót:

        - **Eining viðskiptaskala:** Í **CleanCash\\ ScaleUnit\\ ScaleUnit.CleanCash.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ScaleUnit.CleanCash.Installer** uppsetningarforrit.
        - **Staðbundið CRT á Modern POS:** Í **CleanCash\\ ModernPOS\\ ModernPOS.CleanCash.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ModernPOS.CleanCash.Installer** uppsetningarforrit.

    2. Byrjaðu á CRT uppsetningarforrit fyrir viðbót frá skipanalínunni:

        - **Eining viðskiptaskala:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á Modern POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Settu upp viðbætur fyrir vélbúnaðarstöð:

    1. Í **CleanCash\\ Vélbúnaðarstöð\\ HardwareStation.CleanCash.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.CleanCash.Installer** uppsetningarforrit.
    1. Byrjaðu uppsetningarforritið frá skipanalínunni:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgdu skrefunum í [Settu upp byggingarleiðslu fyrir fjárhagslega samþættingarsýni](fiscal-integration-sample-build-pipeline.md) til að búa til og gefa út Cloud Scale Unit og sjálfsafgreiðslupakka fyrir fjárhagslega samþættingarúrtakið. The **CleanCash build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-the-extensions"></a>Hönnun viðbygginga

Samþættingarúrtak stjórneiningar fyrir Svíþjóð er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ CleanCash** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ríkisfjármálaskjalaveitanda, sem er framlenging á CRT, og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)](emea-swe-fi-sample-sdk.md). Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

### <a name="crt-extension-design"></a>CRT framlengingarhönnun

Tilgangur framlengingarinnar sem er ríkisfjármálaskjalaveita er að búa til þjónustusértæk skjöl og sjá um svör frá stjórneiningunni.

#### <a name="request-handler"></a>Beiðni um stjórnanda

Það er einn **DocumentProviderCleanCash** meðhöndlun beiðni fyrir skjalaveitanda. Þessi meðhöndlun er notuð til að búa til fjárhagsskjöl fyrir stýrieininguna.

Þessi stjórnandi er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í stjórneininguna.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er eru söluviðburðir og endurskoðunarviðburðir studdir.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagsskjalaveituna er staðsett á **src\\ Fiscal Integration\\ CleanCash\\ CommerceRuntime\\ DocumentProvider.CleanCashSample\\ Stillingar\\ DocumentProviderFiscalCleanCashSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur þessarar skráar er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur framlengingarinnar sem er fjárhagstengi er að hafa samskipti við stjórneininguna. Það notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar við stjórneininguna. Það sér einnig um svör sem berast frá stjórnstöðinni.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **CleanCashHandler** meðhöndlun beiðna er inngangsstaðurinn fyrir meðhöndlun beiðna til stjórnunareiningarinnar.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **SubmitDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til stjórnstöðvarinnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun á stjórneiningunni.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla stjórneininguna.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ Fiscal Integration\\ CleanCash\\ Vélbúnaðarstöð\\ Connector.CleanCashSample\\ Stillingar\\ ConnectorCleanCashSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir fjárhagslega tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

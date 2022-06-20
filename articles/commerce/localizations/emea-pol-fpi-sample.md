---
title: Dæmi um samþættingu strimlaprentara fyrir Pólland
description: Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Pólland í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: e71d7b342789e4cf2e7644a46bc847087063fc78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876950"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Dæmi um samþættingu strimlaprentara fyrir Pólland

[!include[banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Pólland í Microsoft Dynamics 365 Commerce.

The Dynamics 365 Commerce virkni fyrir Pólland felur í sér sýnishorn af samþættingu sölustaðarins (POS) við fjárhagsprentara. Sýnið framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og styður POSNET THERMAL HD 2.02 samskiptareglur fyrir fjármálaprentara frá [Posnet Polska SA](https://www.posnet.com.pl) Sýnishornið gerir samskipti við fjárhagsprentara sem er tengdur í gegnum COM tengi með því að nota innfæddan hugbúnaðarrekla. Það var útfært og prófað með því að nota hugbúnaðarhermi sem Posnet útvegaði fyrir Posnet Thermal HD FV EJ skattaprentara. Sýnishornið er gefið í formi frumkóða og er hluti af Retail hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá Posnet. Fyrir upplýsingar um hvernig á að fá fjárhagsprentarann og stjórna honum, hafðu samband [Posnet Polska SA](https://www.posnet.com.pl)

## <a name="scenarios"></a>Aðstæður

Eftirfarandi aðstæður falla undir samþættingarsýni prentara fyrir Pólland:

- Sölusviðsmyndir:

    - Prentaðu út ríkiskvittun fyrir staðgreiðslusölu og skil.
    - Taktu svar frá fjárhagsprentaranum og geymdu það í rásargagnagrunninum.
    - Skattar:

        - Kort að skattkóðum skattaprentara (deildir).
        - Flytja kortlögð skattgögn yfir í skattprentara.

    - Greiðslur:

        - Kort að greiðslumáta fjármálaprentara.
        - Prentaðu greiðslur á ríkiskvittun.
        - Prentaðu breytingarupplýsingar.

    - Prentlínuafslættir.
    - Gjafakort:

        - Útiloka útgefna/endurgjaldfærða gjafakortalínu frá skattakvittun fyrir sölu.
        - Prentaðu greiðslu sem notar gjafakort sem venjulegan greiðslumáta.

    - Prentaðu ríkisreikninga fyrir pöntunaraðgerðir viðskiptavina:

        - Fjárhagskvittun er ekki prentuð fyrir innborgun viðskiptavinarpöntunar.
        - Prenta út reikningskvittun fyrir útfærslulínur af blendingspöntun viðskiptavinar.
        - Prenta fjárhagskvittun fyrir afhendingaraðgerðina fyrir pöntun viðskiptavinar.
        - Prentaðu út reikningskvittun fyrir skilapöntun.

    - Prentaðu út [Upplýsingar um viðskiptavin](emea-pol-customer-information.md) sem er tilgreint fyrir sölufærslur á ríkiskvittun. Dæmi um þessar upplýsingar er VSK-númer viðskiptavinarins.

- Uppgjör dagsloka (fjárhagsskýrslur X og fjárhagslegar Z skýrslur).
- Villumeðferð, svo sem eftirfarandi valkostir:

    - Reyndu aftur fjárhagsskráningu ef hægt er að reyna aftur, eins og ef fjárhagsprentarinn er ekki tengdur, er ekki tilbúinn eða svarar ekki, prentarinn er uppur af pappír eða það er pappírsstopp.
    - Fresta skattskráningu.
    - Slepptu skattaskráningu eða merktu viðskiptin sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Athugaðu hvort fjárhagsprentarinn sé tiltækur áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="gift-cards"></a>Gjafakort

Fjárhagsprentarasamþættingarsýnishornið útfærir eftirfarandi reglur sem tengjast gjafakortum:

- Útiloka sölulínur sem tengjast *Gefa út gjafakort* og *Bæta við gjafakort* rekstur frá ríkiskvittun.
- Ekki prenta út greiðslukvittun ef hún samanstendur eingöngu af gjafakortalínum.
- Dragðu heildarupphæð gjafakorta sem eru gefin út eða endurgjaldfærð í færslu frá greiðslulínum fjárhagskvittunar.
- Vistaðu reiknaðar leiðréttingar á greiðslulínum í rásargagnagrunninum með tilvísun í samsvarandi fjárhagsfærslu.
- Greiðsla með gjafakorti telst venjuleg greiðsla.

### <a name="customer-deposits-and-customer-order-deposits"></a>Innlán viðskiptavina og pantanir viðskiptavina

Fjárhagsprentarasamþættingarsýnishornið útfærir eftirfarandi reglur sem tengjast innlánum viðskiptavina og innborgunum viðskiptavina:

- Ekki prenta út ríkisreikning ef viðskiptin eru innborgun viðskiptavina.
- Ekki prenta út reikningskvittun ef færsla inniheldur aðeins innborgun viðskiptavinapöntunar eða endurgreiðslu innborgunar viðskiptavinarpöntunar.
- Prenta upphæð áður greiddrar innborgunar á fjárhagskvittun fyrir pöntun viðskiptavinar.
- Dragðu innborgunarupphæð viðskiptavinarpöntunar frá greiðslulínum þegar blandað viðskiptavinapöntun er stofnuð.
- Vistaðu reiknaðar leiðréttingar á greiðslulínum í rásargagnagrunninum með tilvísun í fjárhagsfærslu fyrir blendingapöntun viðskiptavinar.

### <a name="limitations-of-the-sample"></a>Takmarkanir úrtaksins

- Skattaprentarinn styður aðeins aðstæður þar sem söluskattur er innifalinn í verðinu. Þess vegna er **Verð er með söluskatti** valkostur verður að vera stilltur á **Já** fyrir bæði verslanir og viðskiptavini.
- Daglegar skýrslur (fjárhags X og fjárhagsáætlun Z) eru prentaðar með því að nota innbyggða *Vaktaskýrsla* sniði.
- Prentun strikamerkis á skattakvittanir er talin hugsanleg sérsníða, vegna þess að þessi eiginleiki er ekki studdur í innbyggðu sniðunum og aðeins hægt að útfæra hann með því að nota sérhannaðar **Ofur-snið** skýrslu.
- Fjárhagsprentarinn styður ekki blandaðar færslur. The **Bannað að blanda saman sölu og skilum í einni kvittun** valkostur ætti að vera stilltur á **Já** í POS virknisniðum.

## <a name="set-up-fiscal-integration-for-poland"></a>Settu upp ríkisfjármálasamþættingu fyrir Pólland

Samþættingarsýni prentara fyrir Pólland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Posnet** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (arfleifð)](emea-pol-fpi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md).

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu einnig eftir þeim stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta sýnishorn af samþættingu prentara](#set-up-the-registration-process).
1. [Stilltu stillingar fyrir villumeðferð](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Settu upp fjárhagslegar X/Z skýrslur frá POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Virkja handvirka framkvæmd frestaðrar fjárhagsskráningar](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Settu upp skráningarferlið

Til að virkja skráningarferlið skaltu fylgja þessum skrefum til að setja upp höfuðstöðvar Commerce. Fyrir frekari upplýsingar, sjá [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Sæktu stillingarskrár fyrir fjárhagsskjalaveituna og fjárhagstengið:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína (td, **[útgáfa/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Opið **src \> Fiscal Integration \> Posnet**.
    1. Sæktu stillingarskrá ríkisskjalaveitunnar á **CommerceRuntime \> DocumentProvider.PosnetSample \> Stillingar \> DocumentProviderPosnetSample.xml** (til dæmis, [skráin til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)).
    1. Sæktu stillingarskrá fjárhagstengis á **Vélbúnaðarstöð \> ThermalDeviceSample \> Stillingar \> TengiPosnetThermalFVEJ.xml** (til dæmis, [skráin til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrá ríkisskjalaveitu:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extension.DocumentProvider.PosnetSample\\ Stillingar\\ DocumentProviderPosnetSample.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Extension.Posnet.ThermalDeviceSample\\ Stillingar\\ TengiPosnetThermalFVEJ.xml
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

- **Vörpun** VSK-taxta (VSK) taxta – Vörpun skattprósentugilda sem eru sett upp fyrir VSK-kóðana í strimlaprentara sem eru sértækir VSK-taxtar. Hér er sjálfgefin vörpun:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Fyrsti íhluturinn í hverju pari stendur fyrir VSK-hlutfallsnúmer sem er skilgreint í strimlaprentaranum. Annar íhluturinn stendur fyrir samsvarandi VSK-hlutfall. Nánari upplýsingar um skilgreiningu VSK-hlutfalls strimlaprentara er að finna í fylgigögnum með POSNET-rekli.

- **Vörpun** greiðslumáta – Vörpun greiðsluaðferða sem eru skilgreindar fyrir verslunina í greiðsluskjámyndir sem eru studdar af strimlaprentaranum. Hér er sjálfgefin vörpun:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Fyrsti íhluturinn í hverju pari stendur fyrir greiðslumáta sem er settur upp fyrir verslunina. Annar íhluturinn stendur fyrir samsvarandi greiðsluskjámynd sem strimlaprentarinn styður. Nánari upplýsingar um greiðsluskjámyndir sem strimlaprentarinn styður er að finna í fylgigögnum MEÐ POSNET-rekli. Breyta verður sýnishornsvörpuninni í samræmi við greiðsluaðferðirnar sem eru skilgreindar í forritinu.

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru teknar með í skilgreiningu fjárhagstengisins sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Tengistrengur** – Strengur sem lýsir upplýsingum um tenginguna við tækið á sniði sem styður ökumanninn. Fyrir frekari upplýsingar, sjá POSNET ökumannsskjölin.
- **Samstilling dagsetningar og tíma** – Gildi sem tilgreinir hvort samstilla þarf dagsetningu og tíma prentarans við tengda vélbúnaðarstöðina.
- **Tímamörk tækisins** – Tíminn, í millisekúndum, sem ökumaðurinn bíður eftir svari frá tækinu. Fyrir frekari upplýsingar, sjá POSNET ökumannsskjölin.

### <a name="configure-channel-components"></a>Skilgreina rásaríhluti

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (arfleifð)](emea-pol-fpi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

#### <a name="set-up-the-development-environment"></a>Setja upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og lengja sýnið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður lausnageymslunni [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Veldu rétta útgáfu útgáfu útibús í samræmi við SDK / umsóknarútgáfuna þína. Frekari upplýsingar er að finna í [Download Retail SDK sýni og tilvísunarpakkar frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnið samþættingarlausn strimlaprentara í **Dynamics365Commerce.Solutions\\ FiscalIntegration\\ Posnet Posnet\\ posnet.sln** og byggið hana upp.
1. Setja upp CRT viðbætur:

    1. Finndu uppsetningarforrit viðbótarinnar CRT:

        - **Commerce Scale Unit:** Í Posnet **ScaleUnit\\ ScaleUnit.Posnet.Installer\\ bin\\ Debug\\ net461\\ möppunni er mappan ScaleUnit.Posnet.Installer** fundin **·**.
        - **Local CRT á Modern POS:** Í **Posnet\\ ModernPOS\\ ModernPOS.Posnet.Installer\\ bin\\ Debug\\ net461** möppunni skaltu finna ModernPOS.Posnet.Installer **uppsetningarforritið**.

    1. Ræsa uppsetningarforrit viðbótarinnar CRT úr skipanalínunni:

        - **Mælieining viðskiptakvarða:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á modern POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Setja upp viðbætur vélbúnaðarstöðvar:

    1. Í möppunni Posnet HardwareStation **HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\ bin\\ Debug\\ net461\\ er mappan HardwareStation.PosnetThermalFVFiscalPrinter.Installer installer\\ fundin**.**·**
    1. Ræsa uppsetningarforrit viðbótarinnar úr skipanalínunni:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgið skrefunum í [Setja upp byggingarpípu fyrir fjárhagssamþættingarsýni](fiscal-integration-sample-build-pipeline.md) til að búa til og losa skýjaskalaeininguna og virkjanlega sjálfsafgreiðslupakka fyrir fjárhagssamþættingarsýnið. YAML-skráin **Posnet build-pipeline.yml** sniðmát er að finna í möppunni **Pípa\\ YAML_Files** í geymslunni [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarsýni prentara fyrir Pólland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Posnet** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Sýnið [samanstendur af veitu fjárhagsskjala](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services), sem er viðbót við CRT og fjárhagstengi, sem er viðbót við vélbúnaðarstöð Commerce. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (arfleifð)](emea-pol-fpi-sample-sdk.md). Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur viðbyggingarinnar sem er fjárhagsskjalaveita er að búa til prentarasértæk skjöl og meðhöndla svör frá fjárhagsprentaranum. Þessi viðbót býr til sett af prentara-sértækum skipunum á JavaScript Object Notation (JSON) sniði sem eru skilgreindar af POSNET forskrift 19-3678.

#### <a name="request-handler"></a>Biðja um rekil

The **DocumentProviderPosnetProtocol** meðhöndlun beiðni er inngangsstaður beiðninnar um að búa til skjöl frá fjárhagsprentaranum.

Rekillinn erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti tengiskjalsveitunnar sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal á að mynda. Það skilar prentarasértæku skjali sem ætti að vera skráð í fjárhagsprentara.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir tilvik sem á að gerast áskrifandi að. Eins og er eru eftirfarandi atburðir studdir: sala, prentun X skýrslu og prentun Z skýrslu.

#### <a name="configuration"></a>Skilgreining

Skilgreiningarskráin fyrir fjárhagsskjalsveituna er staðsett í **src\\ FiscalIntegration\\ Posnet\\ CommerceRuntime\\ DocumentProvider.PosnetSample\\ Configuration\\ DocumentProviderPosnetSample.xml** í geymslunni [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tilgangur skrárinnar er að gera kleift að skilgreina stillingar fjárhagsskjalsveitunnar úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar.

### <a name="hardware-station-extension-design"></a>Viðaukahönnun vélbúnaðarstöðvar

Tilgangur viðbótarinnar sem er fjárhagstengi er að hafa samskipti við fjárhagsprentarann. Þessi viðbót kallar á aðgerðir POSNET bílstjórans til að senda inn skipanir sem CRT framlenging myndar á fjárhagsprentarann. Það sér einnig um villur í tæki.

#### <a name="request-handler"></a>Biðja um rekil

The **FiscalPrinterHandler** meðhöndlun beiðna er inngangsstaðurinn til að meðhöndla beiðnina til ríkisútlæga tækisins.

Rekillinn erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti fjárhagstengisins sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til prentara og skilar svari frá fjármálaprentara.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun tækisins.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla prentara.

#### <a name="configuration"></a>Skilgreining

Skilgreiningarskráin fyrir fjárhagstengið er staðsett í src **FiscalIntegration\\ Posnet\\ HardwareStation\\ ThermalDeviceSample\\ Configuration\\ ConnectorPosnetThermalFVEJ.xml\\ í lausnageymslunni**[Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Tilgangur skrárinnar er að gera kleift að skilgreina stillingar fjárhagstengisins úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

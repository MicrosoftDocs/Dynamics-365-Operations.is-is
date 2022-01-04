---
title: Dæmi um samþættingu strimlaprentara fyrir Pólland
description: Þetta efni gefur yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Pólland í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 1b3d7d59494b215ae47f710e200e7e0c57e4ca29
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944866"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Dæmi um samþættingu strimlaprentara fyrir Pólland

[!include[banner](../includes/banner.md)]

Þetta efni gefur yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Pólland í Microsoft Dynamics 365 Commerce.

The Dynamics 365 Commerce virkni fyrir Pólland felur í sér sýnishorn af samþættingu sölustaðarins (POS) við fjárhagsprentara. Sýnið framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og styður POSNET THERMAL HD 2.02 samskiptareglur fyrir fjármálaprentara frá [Posnet Polska SA](https://www.posnet.com.pl) Sýnishornið gerir samskipti við fjárhagsprentara sem er tengdur í gegnum COM tengi með því að nota innfæddan hugbúnaðarrekla. Það var útfært og prófað með því að nota hugbúnaðarhermi sem Posnet útvegaði fyrir Posnet Thermal HD FV EJ skattaprentara. Sýnishornið er gefið í formi frumkóða og er hluti af Retail hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá Posnet. Fyrir upplýsingar um hvernig á að fá fjárhagsprentarann og stjórna honum, hafðu samband [Posnet Polska SA](https://www.posnet.com.pl)

## <a name="scenarios"></a>Sviðsmyndir

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
    - Slepptu fjárhagslegri skráningu eða merktu færsluna sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Athugaðu hvort fjárhagsprentarinn sé tiltækur áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="gift-cards"></a>Gjafakort

Fjárhagsprentarasamþættingarsýnishornið útfærir eftirfarandi reglur sem tengjast gjafakortum:

- Útiloka sölulínur sem tengjast *Gefa út gjafakort* og *Bæta við gjafakort* rekstur frá ríkiskvittun.
- Ekki prenta út greiðslukvittun ef hún samanstendur eingöngu af gjafakortalínum.
- Dragðu heildarupphæð gjafakorta sem eru gefin út eða endurgjaldfærð í færslu frá greiðslulínum fjárhagskvittunar.
- Vistaðu reiknaðar leiðréttingar á greiðslulínum í rásargagnagrunninum með tilvísun í samsvarandi fjárhagsfærslu.
- Greiðsla með gjafakorti telst venjuleg greiðsla.

### <a name="customer-deposits-and-customer-order-deposits"></a>Innlán viðskiptavina og pantanir viðskiptavina

Fjárhagsprentarasamþættingarsýnishornið útfærir eftirfarandi reglur sem tengjast innlánum viðskiptavina og innlánum viðskiptavinapöntunar:

- Ekki prenta út ríkisreikning ef viðskiptin eru innborgun viðskiptavina.
- Ekki prenta út reikningskvittun ef færsla inniheldur aðeins innborgun viðskiptavinapöntunar eða endurgreiðslu innborgunar viðskiptavinarpöntunar.
- Prenta upphæð áður greiddrar innborgunar á fjárhagskvittun fyrir pöntun viðskiptavinar.
- Dragðu innborgunarupphæð viðskiptavinarpöntunar frá greiðslulínum þegar blandað viðskiptavinapöntun er stofnuð.
- Vistaðu reiknaðar leiðréttingar á greiðslulínum í rásargagnagrunninum með tilvísun í fjárhagsfærslu fyrir blandaða viðskiptavinapöntun.

### <a name="limitations-of-the-sample"></a>Takmarkanir úrtaksins

- Skattaprentarinn styður aðeins aðstæður þar sem söluskattur er innifalinn í verðinu. Þess vegna er **Verð er með söluskatti** valkostur verður að vera stilltur á **Já** fyrir bæði verslanir og viðskiptavini.
- Daglegar skýrslur (fjárhags X og fjárhagsáætlun Z) eru prentaðar með því að nota innbyggða *Vaktaskýrsla* sniði.
- Prentun strikamerkis á skattakvittanir er talin hugsanleg sérsníða, vegna þess að þessi eiginleiki er ekki studdur í innbyggðu sniðunum og aðeins hægt að útfæra hann með því að nota sérhannaðar **Ofur-snið** skýrslu.
- Fjárhagsprentarinn styður ekki blandaðar færslur. The **Bannað að blanda saman sölu og skilum í einni kvittun** valkostur ætti að vera stilltur á **Já** í POS virknisniðum.

## <a name="set-up-fiscal-integration-for-poland"></a>Settu upp ríkisfjármálasamþættingu fyrir Pólland

Samþættingarsýni prentara fyrir Pólland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Posnet** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (gamalt)](emea-pol-fpi-sample-sdk.md).
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
    > - **Stillingarskrá fyrir ríkisfjármálaskjalaveitu:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extension.DocumentProvider.PosnetSample\\ Stillingar\\ DocumentProviderPosnetSample.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Extension.Posnet.ThermalDeviceSample\\ Stillingar\\ TengiPosnetThermalFVEJ.xml
    > 
    > Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingaskrá fjárhagsskjalaveitunnar sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú sóttir áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tengi virka snið**. Búðu til nýtt virknisnið fyrir tengi. Veldu skjalaveituna og tengið sem þú hleður inn áðan. Uppfærðu [gagnakortastillingar](#default-data-mapping) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýja tæknisnið fyrir tengi og veldu fjárhagstengi sem þú hleður inn áðan. Uppfærðu [tengistillingar](#fiscal-connector-settings) eins og krafist er.
6. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**. Stofna nýjan fjárhagstengihóp fyrir virknisniðið tengi sem þú bjóst til áður.
7. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**. Búðu til nýtt fjárhagsskráningarferli og fjárhagsskráningarferlisþrep og veldu fjárhagstengihópinn sem þú stofnaðir áðan.
8. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veldu virknisnið sem er tengt við verslunina þar sem skráningarferlið á að virkja. Á **Skráningarferli í ríkisfjármálum** Flýtiflipi, veldu fjárhagsskráningarferlið sem þú bjóst til áðan.
9. Fara til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Veldu vélbúnaðarsnið sem er tengt við vélbúnaðarstöðina sem fjárhagsprentarinn verður tengdur við. Á **Jaðartæki í ríkisfjármálum** Flýtiflipi, veldu tæknisniðið sem þú bjóst til áðan.
10. Opnaðu dreifingaráætlun (**Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**), og veldu störf **1070** og **1090** að flytja gögn í rásargagnagrunninn.

#### <a name="default-data-mapping"></a>Sjálfgefin gagnakortlagning

Eftirfarandi sjálfgefna gagnavörpun er innifalin í uppsetningu fjárhagsskjalaveitu sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Kortlagning virðisaukaskatts (VSK) taxta** – Kortlagning skattprósentugilda sem eru sett upp fyrir virðisaukaskattskóða við skattaprentarasértæka virðisaukaskattshlutföll. Hér er sjálfgefna kortlagning:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Fyrsti íhluturinn í hverju pari táknar virðisaukaskattshlutfallsnúmer sem er stillt í fjárhagsprentaranum. Annar þátturinn táknar samsvarandi virðisaukaskattshlutfall. Fyrir frekari upplýsingar um virðisaukaskattsuppsetningu skattaprentara, sjá POSNET ökumannsskjölin.

- **Kortlagning útboðstegunda** – Kortlagning greiðslumáta sem eru stilltir fyrir verslunina við greiðslueyðublöð sem eru studd af fjárhagsprentaranum. Hér er sjálfgefna kortlagning:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Fyrsti hluti hvers pars táknar greiðslumáta sem er settur upp fyrir verslunina. Annar hluti táknar samsvarandi greiðslueyðublað sem er stutt af fjárhagsprentaranum. Fyrir frekari upplýsingar um greiðslueyðublöð sem fjárhagsprentari styður, sjá POSNET ökumannsskjölin. Þú verður að breyta sýnishorninu í samræmi við greiðslumáta sem eru stilltar í forritinu þínu.

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru innifalin í fjárhagstengistillingunni sem er hluti af fjárhagssamþættingarsýninu:

- **Tengistrengur** – Strengur sem lýsir upplýsingum um tenginguna við tækið á sniði sem styður ökumanninn. Fyrir frekari upplýsingar, sjá POSNET ökumannsskjölin.
- **Samstilling dagsetningar og tíma** – Gildi sem tilgreinir hvort samstilla þarf dagsetningu og tíma prentarans við tengda vélbúnaðarstöðina.
- **Tímamörk tækisins** – Tíminn, í millisekúndum, sem ökumaðurinn bíður eftir svari frá tækinu. Fyrir frekari upplýsingar, sjá POSNET ökumannsskjölin.

### <a name="configure-channel-components"></a>Stilltu rásaríhluti

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (gamalt)](emea-pol-fpi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

#### <a name="set-up-the-development-environment"></a>Settu upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og stækka sýnishornið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla. Veldu rétta útgáfu útibús í samræmi við SDK/forritsútgáfu þína. Fyrir frekari upplýsingar, sjá [Sæktu smásölu SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu prentarasamþættingarlausnina á **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ Posnet\\ Posnet.sln**, og byggja það.
1. Settu upp CRT viðbætur:

    1. Finndu CRT uppsetningarforrit fyrir viðbót:

        - **Eining viðskiptaskala:** Í **Posnet\\ ScaleUnit\\ ScaleUnit.Posnet.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ScaleUnit.Posnet.Installer** uppsetningarforrit.
        - **Staðbundið CRT á Modern POS:** Í **Posnet\\ ModernPOS\\ ModernPOS.Posnet.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ModernPOS.Posnet.Installer** uppsetningarforrit.

    1. Byrjaðu á CRT uppsetningarforrit fyrir viðbót frá skipanalínunni:

        - **Eining viðskiptaskala:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á Modern POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Settu upp viðbætur fyrir vélbúnaðarstöð:

    1. Í **Posnet\\ Vélbúnaðarstöð\\ HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.PosnetThermalFVFiscalPrinter.Installer** uppsetningarforrit.
    1. Byrjaðu uppsetningarforritið frá skipanalínunni:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgdu skrefunum í [Settu upp smíðisleiðslu fyrir sýnishorn fjárhagslega samþættingar](fiscal-integration-sample-build-pipeline.md) að búa til og gefa út Cloud Scale Unit og sjálfsafgreiðslupakka fyrir samþættingarúrtakið í ríkisfjármálum. The **Posnet build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarsýni prentara fyrir Pólland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ Posnet** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) ríkisfjármálaskjalaveitanda, sem er framlenging á CRT, og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (gamalt)](emea-pol-fpi-sample-sdk.md). Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur viðbyggingarinnar sem er fjárhagsskjalaveita er að búa til prentarasértæk skjöl og meðhöndla svör frá fjárhagsprentaranum. Þessi viðbót býr til sett af prentara-sértækum skipunum á JavaScript Object Notation (JSON) sniði sem eru skilgreindar af POSNET forskrift 19-3678.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **DocumentProviderPosnetProtocol** meðhöndlun beiðni er inngangsstaður beiðninnar um að búa til skjöl frá fjárhagsprentaranum.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar prentarasértæku skjali sem ætti að vera skráð í fjárhagsprentara.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er eru eftirfarandi atburðir studdir: sala, prentun X skýrslu og prentun Z skýrslu.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagsskjalaveituna er staðsett á **src\\ Fiscal Integration\\ Posnet\\ CommerceRuntime\\ DocumentProvider.PosnetSample\\ Stillingar\\ DocumentProviderPosnetSample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera það kleift að stilla stillingar ríkisfjármálaskjalaveitunnar frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur viðbótarinnar sem er fjárhagstengi er að hafa samskipti við fjárhagsprentarann. Þessi viðbót kallar á aðgerðir POSNET bílstjórans til að senda inn skipanir sem CRT framlenging myndar á fjárhagsprentarann. Það sér einnig um villur í tæki.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **FiscalPrinterHandler** meðhöndlun beiðna er inngangsstaðurinn til að meðhöndla beiðnina til ríkisútlæga tækisins.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem tilgreint er í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til prentara og skilar svari frá fjármálaprentara.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun tækisins.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla prentara.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ Fiscal Integration\\ Posnet\\ Vélbúnaðarstöð\\ ThermalDeviceSample\\ Stillingar\\ TengiPosnetThermalFVEJ.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera kleift að stilla stillingar á fjárhagstenginu frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

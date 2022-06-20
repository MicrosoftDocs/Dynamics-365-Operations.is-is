---
title: Dæmi um samþættingu strimlaprentara fyrir Ítalíu
description: Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Ítalíu í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 2aa1851fe5fe447ba2dd4640be9881b37e54216e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909391"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Dæmi um samþættingu strimlaprentara fyrir Ítalíu

[!include[banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Ítalíu í Microsoft Dynamics 365 Commerce.

Viðskiptavirknin fyrir Ítalíu inniheldur sýnishorn af samþættingu sölustaðarins (POS) við skattprentara. Sýnið framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) þannig að það virki með [Epson FP-90III röð](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) prentara frá Epson, og það gerir samskipti við fjárhagsprentara í vefþjónsham í gegnum EpsonFPMate vefþjónustuna sem notar Fiscal ePOS-Print API. Sýnið styður aðeins Registratore Telematico (RT) ham. Sýnishornið er gefið í formi frumkóða og er hluti af Retail hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá Epson. Fyrir upplýsingar um hvernig á að fá fjárhagsprentarann og stjórna honum, hafðu samband [Epson Italia SpA](https://www.epson.it)

## <a name="scenarios"></a>Aðstæður

Eftirfarandi aðstæður falla undir samþættingarsýni prentara fyrir Ítalíu:

- Sölusviðsmyndir:

    - Prentaðu út ríkiskvittun fyrir staðgreiðslusölu og skil.
    - Taktu svar frá fjárhagsprentaranum og geymdu það í rásargagnagrunninum.
    - Skattar:

        - Kort að skattkóðum skattaprentara (deildir).
        - Flytja kortlögð skattgögn yfir í skattprentara.
        - Prentaðu skatta á skattskvittun.

    - Greiðslur:

        - Kort að greiðslumáta fjármálaprentara.
        - Prentaðu greiðslur á ríkiskvittun.
        - Prentaðu breytingarupplýsingar.

    - Prentlínuafslættir.
    - Gjafakort:

        - Útiloka útgefna/endurhlaða gjafakortalínu frá skattakvittun fyrir sölu.
        - Prentaðu greiðslu sem notar gjafakort sem venjulegan greiðslumáta.

    - Prentaðu ríkisreikninga fyrir pöntunaraðgerðir viðskiptavina:

        - Fjárhagskvittun er ekki prentuð fyrir innborgun viðskiptavinarpöntunar.
        - Prenta út reikningskvittun fyrir flutningslínur í blendingspöntun viðskiptavinar.
        - Prenta fjárhagskvittun fyrir afhendingaraðgerðina fyrir pöntun viðskiptavinar.
        - Prentaðu út reikningskvittun fyrir skilapöntun.

    - Prentaðu strikamerki fyrir kvittunarnúmerið á reikningskvittun.
    - Prentaðu út [Upplýsingar um viðskiptavin](emea-ita-customer-information.md) sem er tilgreint fyrir sölufærslur á ríkiskvittun. Dæmi um þessar upplýsingar er happdrættiskóði viðskiptavinarins. 

- Uppgjör dagsloka (fjárhagsskýrslur X og fjárhagslegar Z skýrslur).
- Villumeðferð, svo sem eftirfarandi valkostir:

    - Reyndu aftur fjárhagsskráningu ef hægt er að reyna aftur, eins og ef fjárhagsprentari er ekki tengdur, er ekki tilbúinn eða svarar ekki, prentarinn er uppiskroppa með pappír eða það er pappírsstopp.
    - Fresta skattskráningu.
    - Slepptu skattaskráningu eða merktu viðskiptin sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Athugaðu hvort fjárhagsprentarinn sé tiltækur áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="gift-cards"></a>Gjafakort

Fjárhagsprentarasamþættingarsýnishornið útfærir eftirfarandi reglur sem tengjast gjafakortum:

- Útiloka sölulínur sem tengjast *Gefa út gjafakort* og *Bæta við gjafakort* rekstur frá ríkiskvittun.
- Ekki prenta út ríkiskvittun ef hún samanstendur eingöngu af gjafakortalínum.
- Dragðu heildarupphæð gjafakorta sem eru gefin út eða endurhlaðin í færslu frá greiðslulínum fjárhagskvittunar.
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
- Daglegar skýrslur (fjárhags X og fjárhagsáætlun Z) eru prentaðar með því að nota sniðið sem er fellt inn í fastbúnað fjárhagsprentarans.
- Fjárhagsprentarinn styður ekki blandaðar færslur. The **Bannað að blanda saman sölu og skilum í einni kvittun** valkostur ætti að vera stilltur á **Já** í POS virknisniðum.
- Sýnið styður aðeins samþættingu við fjárhagsprentara sem virkar í Registratore Telematico (RT) ham.

## <a name="set-up-fiscal-integration-for-italy"></a>Settu upp ríkisfjármálasamþættingu fyrir Ítalíu

Samþættingarsýni prentara fyrir Ítalíu er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ EpsonFP90III Dæmi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)](emea-ita-fpi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md).

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu einnig eftir þeim stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta sýnishorn af samþættingu prentara](#set-up-the-registration-process).
1. [Settu upp fjárhagstexta fyrir afslætti](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Stilltu stillingar fyrir villumeðferð](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Settu upp fjárhagslegar X/Z skýrslur frá POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Virkja handvirka framkvæmd frestaðrar fjárhagsskráningar](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Settu upp virkni fyrir stjórnun viðskiptavinaupplýsinga í POS](emea-ita-customer-information.md#setup).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Settu upp skráningarferlið

Til að virkja skráningarferlið skaltu fylgja þessum skrefum til að setja upp höfuðstöðvar Commerce. Fyrir frekari upplýsingar, sjá [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Sæktu stillingarskrár fyrir fjárhagsskjalaveituna og fjárhagstengið:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína (td, **[útgáfa/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Opið **src \> Fiscal Integration \> EpsonFP90III Dæmi**.
    1. Sæktu stillingarskrá ríkisskjalaveitunnar á **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Stillingar \> DocumentProviderEpsonFP90IIISample.xml** (til dæmis, [skráin til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Sæktu stillingarskrá fjárhagstengis á **Vélbúnaðarstöð \> EpsonFP90III FiscalDeviceSample \> Stillingar \> Tengi EpsonFP90IIISample.xml** (til dæmis, [skráin til útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrá ríkisskjalaveitu:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extension.DocumentProvider.EpsonFP90IIISample\\ Stillingar\\ DocumentProviderEpsonFP90IIISample.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Viðbót.EpsonFP90IIIFiscalDeviceSample\\ Stillingar\\ Tengi EpsonFP90IIISample.xml
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

- **Kortlagning útboðstegunda** – Kortlagning greiðslumáta sem eru stilltir fyrir verslunina við greiðslutegundir sem fjárhagsprentari styður. Eftirfarandi dæmi sýnir sjálfgefna vörpun.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Hér er útskýring á eigindunum í þessari kortlagningu:

    - **Greiðslumáti í verslun** er greiðslumáti sem settur er upp fyrir verslunina á **Verslun og verslun \> Rásaruppsetning \> Greiðslumáta \> Greiðslumáta**.
    - **PrinterPayment Type** og **PrinterPayment Index** eru samsvarandi greiðslutegund og vísitala sem eru skilgreind í Epson skattaprentaraskjölunum.
    - **Innborgunaraðferð** er notað til að tilgreina greiðslutegund og vísitölu prentara fyrir þann hluta pöntunarupphæðar viðskiptavinar sem er jafnaður með innborgun viðskiptavinarpöntunar.

    Eftirfarandi tafla sýnir hvernig sýnishornsvörpun greiðslumáta samsvarar greiðslumáta verslunar sem eru stilltir í stöðluðum kynningargögnum.

    | Greiðslumáti | Heiti greiðsluháttar |
    |----------------|---------------------|
    | 1              | Reiðufé                |
    | 3              | Spjald                |
    | 4              | Viðskiptavinalykill    |
    | 6              | Gjaldmiðill            |
    | 8              | Gjafakort           |

    Breyta verður sýnishornsvörpuninni í samræmi við greiðsluaðferðirnar sem eru skilgreindar í forritinu.

- **Strikamerkistegund fyrir kvittunarnúmer** – Tegund strikamerkis sem er notað til að sýna kvittunarnúmer á reikningskvittun. Sjálfgefin kortlagning er **KÓÐI128**.
- **Prentaðu fjárhagsgögn í kvittunarhaus** – Ef kveikt er á þessari færibreytu verða upplýsingar um verslun prentaðar á fjárhagskvittun. Þessar upplýsingar innihalda nafn verslunarinnar, heimilisfang og skattanúmer og nafn gjaldkera.
- **Kortlagning ríkisprentaradeildar** – Kortlagning deilda skattprentara að virðisaukaskattshlutföllum (virðisaukaskatti), tegundum sem eru undanþegnir virðisaukaskatti og vörutegundum. Eftirfarandi dæmi sýnir sjálfgefna vörpun.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Hér er útskýring á eigindunum í þessari kortlagningu:

    - **virðisaukaskattur** er studd VSK-hlutfall sem er stillt sem VSK-kóði. Gildið í vörpunni hefur tvo aukastafi en engin aukastafaskil. Til dæmis, **2200** táknar 22 prósent, og **1000** stendur fyrir 10 prósent.
    - **VATEexemptNature** á aðeins við í þeim tilvikum þar sem virðisaukaskattshlutfallið er 0 (núll), þar með talið tilvik þar sem enginn skattur er. Eins og er, **VATEexemptNature** er aðeins stutt fyrir gjafakort og gildið í kortlagningunni ætti að samsvara gildinu **VATEexemptNatureForGiftCard** eign í XML stillingarskránni.
    - **Vörugerð** er tegund vörunnar. Verðmæti á **0** táknar vörur og verðmæti **1** táknar þjónustu.
    - **Deildarnúmer** er númer deildarinnar sem er stillt í prentaranum og samsvarar þremur fyrri eiginleikum.

    Þú verður að breyta sýnishorninu í samræmi við virðisaukaskattshlutföllin sem eru stillt í forritinu þínu og samsvarandi deildum sem eru stilltar í fjárhagsprentaranum þínum.

- **VSK undanþegið eðli fyrir gjafakort** – VSK undanþegið eðli sem ætti að gilda þegar gjafakort er gefið út eða endurfyllt. Gildið ætti að samsvara einhverri færslu í kortlagningu fjárhagsprentaradeildar. Sjálfgefin kortlagning er **NS**.
- **Virkja ókeypis hluti** – Ef kveikt er á þessari færibreytu er sérstakur *omaggio* tegund afsláttarleiðréttingar fyrir vörur sem eru með 100 prósent afslátt er virkjuð.
- **Upplýsingakóði fyrir uppruna skila** – Upplýsingakóðinn sem er notaður til að fanga uppruna skilafærslu ef engin upprunaleg sölukvittun fylgir. Þessi breytu er notuð ásamt **Upplýsingakóði fyrir upprunalega söludagsetningu** og **Skila upprunakortlagningu** færibreytur til að búa til rétt skilaboð í fjárhagskvittun um uppruna skilafærslu ef engin upprunaleg sölufærsla er til. 

    Þessi upplýsingakóði ætti að vera stilltur til að gera notandanum kleift að velja eða slá inn einn af mögulegum uppruna skila í verslunum þínum. Til dæmis er hægt að stilla það sem lista yfir undirkóða (svo sem **Til baka af síðunni** eða **Til baka frá söluturni**). The **Skila upprunakortlagningu** færibreyta er síðan notuð til að þýða gildi upplýsingakóðans í skipun fyrir fjárhagsprentarann.

    Upplýsingakóðinn sem er valinn fyrir **Upplýsingakóði fyrir uppruna skila** ætti að vera stilltur sem skyldubundinn upplýsingakóði sem er rekinn einu sinni í hverja sölufærslu. Það ætti að vera úthlutað sem **Skila vöru** upplýsingakóði í POS-virkniprófílnum, þannig að hann er ræstur þegar **Skila vöru** rekstur er keyrður.

    Ekkert sjálfgefið gildi er tilgreint fyrir þessa vörpun. Þú verður að velja upplýsingakóða sem er stilltur í forritinu þínu.

- **Upplýsingakóði fyrir upprunalega söludagsetningu** – Upplýsingakóðinn sem er notaður til að fanga upprunalega söludagsetningu fyrir skilafærslu ef engin upprunaleg sölukvittun fylgir. Þessi breytu er notuð ásamt **Upplýsingakóði fyrir uppruna skila** og **Skila upprunakortlagningu** færibreytur til að búa til rétt skilaboð í fjárhagskvittun um uppruna skilafærslu ef engin upprunaleg sölufærsla er til.

    Upplýsingakóðinn ætti að vera stilltur þannig að **Inntakstegund** reiturinn er stilltur á **Dagsetning**. Hann ætti að vera stilltur sem skyldubundinn upplýsingakóði sem er rekinn einu sinni í hverja sölufærslu. Það ætti einnig að vera úthlutað sem **Tengdur upplýsingakóði** fyrir upplýsingakóðann sem er valinn fyrir **Upplýsingakóði fyrir uppruna skila** færibreytu, þannig að upplýsingakóðarnir tveir eru sendir hver á eftir öðrum.

    Ekkert sjálfgefið gildi er tilgreint fyrir þessa vörpun. Þú verður að velja upplýsingakóða sem er stilltur í forritinu þínu.

- **Skila upprunakortlagningu** – Kortlagning á uppruna skila sem er notuð til að prenta uppruna skilafærslu ef engin upprunaleg sölukvittun fylgir. Þessi breytu er notuð ásamt **Upplýsingakóði fyrir uppruna skila** og **Upplýsingakóði fyrir upprunalega söludagsetningu** færibreytur til að búa til rétt skilaboð í fjárhagskvittun um uppruna skilafærslu ef engin upprunaleg sölufærsla er til. Eftirfarandi dæmi sýnir sjálfgefna vörpun.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Hér er útskýring á eigindunum í þessari kortlagningu:

    - **ReturnOrigin** er einn af mögulegum uppruna skila í verslunum þínum. Gildið ætti að samsvara gildinu á **Upplýsingakóði fyrir uppruna skila** breytu.
    - **PrinterReturnOrigin** er einn af þeim skilaupprunum sem fjárhagsprentari samþykkir (**POS**, **·**, eða **ND**).
    - **PrinterReturnOriginWithout Fiscal Data** er skilauppruni sem fjárhagsprentari samþykkir og samsvarar skilafærslu sem er tengd upprunalegri sölufærslu sem hefur ekki tengd fjárhagsgögn vegna þess að hún var ekki skráð í gegnum fjárhagsprentara. Í þessu tilviki er upprunalega söludagsetningin auðkennd sem dagsetning upphaflegu sölufærslunnar.

Eftirfarandi sjálfgefna gagnakortanir eru úreltar og eru aðeins geymdar vegna bakábaks eindrægni:

- Kortlagning virðisaukaskatts (VSK) kóða
- Greiðslugerð innborgunar

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru teknar með í skilgreiningu fjárhagstengisins sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Heimilisfang endapunkts** – Vefslóð prentarans.
- **Samstilling dagsetningar og tíma** – Gildi sem tilgreinir hvort samstilla þarf dagsetningu og tíma prentarans við tengda vélbúnaðarstöðina.

### <a name="configure-channel-components"></a>Skilgreina rásaríhluti

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)](emea-ita-fpi-sample-sdk.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

#### <a name="set-up-the-development-environment"></a>Setja upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og lengja sýnið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður lausnageymslunni [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Veldu rétta útgáfu útgáfu útibús í samræmi við SDK / umsóknarútgáfuna þína. Frekari upplýsingar er að finna í [Download Retail SDK sýni og tilvísunarpakkar frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu fjárhagslega prentara samþættingarlausnina á **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ EpsonFP90III Dæmi\\ EpsonFP90IIISample.sln**, og byggja það.
1. Setja upp CRT viðbætur:

    1. Finndu uppsetningarforrit viðbótarinnar CRT:

        - **Eining viðskiptaskala:** Í **EpsonFP90III Dæmi\\ ScaleUnit\\ ScaleUnit.EpsonFP90III.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ScaleUnit.EpsonFP90III.Installer** uppsetningarforrit.
        - **Staðbundið CRT á Modern POS:** Í **EpsonFP90III Dæmi\\ ModernPOS\\ ModernPOS.EpsonFP90III.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ModernPOS.EpsonFP90III.Installer** uppsetningarforrit.

    1. Ræsa uppsetningarforrit viðbótarinnar CRT úr skipanalínunni:

        - **Mælieining viðskiptakvarða:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á modern POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Setja upp viðbætur vélbúnaðarstöðvar:

    1. Í **EpsonFP90III Dæmi\\ Vélbúnaðarstöð\\ HardwareStation.EpsonFP90III.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.EpsonFP90III.Installer** uppsetningarforrit.
    1. Ræsa uppsetningarforrit viðbótarinnar úr skipanalínunni:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgið skrefunum í [Setja upp byggingarpípu fyrir fjárhagssamþættingarsýni](fiscal-integration-sample-build-pipeline.md) til að búa til og losa skýjaskalaeininguna og virkjanlega sjálfsafgreiðslupakka fyrir fjárhagssamþættingarsýnið. The **EpsonFP90III build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarsýni prentara fyrir Ítalíu er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ EpsonFP90III Dæmi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Sýnið [samanstendur af veitu fjárhagsskjala](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services), sem er viðbót við CRT og fjárhagstengi, sem er viðbót við vélbúnaðarstöð Commerce. Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þetta fjárhagslega samþættingarúrtak. Þú verður að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)](emea-ita-fpi-sample-sdk.md). Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur viðbyggingarinnar sem er fjárhagsskjalaveita er að búa til prentarasértæk skjöl og meðhöndla svör frá fjárhagsprentaranum.

#### <a name="request-handler"></a>Biðja um rekil

The **DocumentProvider EpsonFP90III** meðhöndlun beiðni er inngangsstaður beiðninnar um að búa til skjöl frá fjárhagsprentaranum.

Rekillinn erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti tengiskjalsveitunnar sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal á að mynda. Það skilar prentarasértæku skjali sem ætti að vera skráð í fjárhagsprentara.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir tilvik sem á að gerast áskrifandi að. Eins og er eru eftirfarandi atburðir studdir: sala, prentun X skýrslu og prentun Z skýrslu.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagsskjalaveituna er staðsett á **src\\ Fiscal Integration\\ EpsonFP90III Dæmi\\ CommerceRuntime\\ DocumentProvider.EpsonFP90IIISample\\ Stillingar\\ DocumentProviderEpsonFP90IIISample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar.

### <a name="hardware-station-extension-design"></a>Viðaukahönnun vélbúnaðarstöðvar

Tilgangur viðbótarinnar sem er fjárhagstengi er að hafa samskipti við fjárhagsprentarann. Þessi viðbót notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar á fjárhagsprentarann. Það sér einnig um svör sem berast frá fjármálaprentara.

#### <a name="request-handler"></a>Biðja um rekil

The **EpsonFP90III Dæmi** meðhöndlun beiðna er inngangsstaðurinn fyrir meðhöndlun beiðni til ríkisútlæga tækisins.

Rekillinn erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti fjárhagstengisins sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til prentara og skilar svari frá fjármálaprentara.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun tækisins.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla prentara.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ Fiscal Integration\\ EpsonFP90III Dæmi\\ Vélbúnaðarstöð\\ EpsonFP90III FiscalDeviceSample\\ Stillingar\\ Tengi EpsonFP90IIISample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

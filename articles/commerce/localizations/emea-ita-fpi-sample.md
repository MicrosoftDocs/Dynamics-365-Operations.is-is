---
title: Dæmi um samþættingu strimlaprentara fyrir Ítalíu
description: Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Ítalíu í Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-01
ms.openlocfilehash: 6ad97e87e4114a8f2250d0ba4880b7a466b3689e
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631397"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Dæmi um samþættingu strimlaprentara fyrir Ítalíu

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein veitir yfirlit yfir úrtak ríkisfjármálasamþættingar fyrir Ítalíu í Microsoft Dynamics 365 Commerce.

Viðskiptavirknin fyrir Ítalíu inniheldur sýnishorn af samþættingu sölustaðarins (POS) við fjárhagsprentara. Sýnið framlengir [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) þannig að það virki með [Epson FP-90III röð](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) prentara frá Epson, og gerir samskipti við fjárhagsprentara í vefþjónsham í gegnum EpsonFPMate vefþjónustuna sem notar Fiscal ePOS-Print API. Sýnið styður aðeins Registratore Telematico (RT) ham. Sýnishornið er gefið í formi frumkóða og er hluti af Commerce hugbúnaðarþróunarsettinu (SDK).

Microsoft gefur ekki út vélbúnað, hugbúnað eða skjöl frá Epson. Fyrir upplýsingar um hvernig á að fá fjárhagsprentarann og stjórna honum, hafðu samband [Epson Italia SpA](https://www.epson.it)

## <a name="scenarios"></a>Aðstæður

Eftirfarandi aðstæður falla undir samþættingarsýni prentara fyrir Ítalíu:

- Sölusviðsmyndir:

    - Prentaðu út ríkiskvittun fyrir sölu og skil.
    - Taktu svar frá fjárhagsprentaranum og geymdu það í rásargagnagrunninum.
    - Skattar:

        - Kort að skattanúmerum skattaprentara (deildir).
        - Flytja kortlögð skattagögn til fjárhagsprentarans.
        - Prentaðu skatta á ríkisskattskvittun.

    - Greiðslur:

        - Kort að greiðslumáta fjármálaprentara.
        - Prentaðu greiðslur á ríkiskvittun.
        - Prentaðu breytingarupplýsingar.

    - Prentlínuafsláttur.
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

    - Reyndu aftur fjárhagsskráningu ef hægt er að reyna aftur, eins og ef fjárhagsprentarinn er ekki tengdur, er ekki tilbúinn eða svarar ekki, prentarinn er uppiskroppa með pappír eða það er pappírsstopp.
    - Fresta skattskráningu.
    - Slepptu skattaskráningu eða merktu færsluna sem skráða og láttu upplýsingakóða fylgja með til að fanga ástæðu bilunarinnar og viðbótarupplýsingar.
    - Athugaðu framboð fjárhagsprentarans áður en ný sölufærsla er opnuð eða sölufærslu er lokið.

### <a name="gift-cards"></a>Gjafakort

Fjárhagsprentarasamþættingarsýnishornið útfærir eftirfarandi reglur sem tengjast gjafakortum:

- Útiloka sölulínur sem tengjast *Gefðu út gjafakort* og *Bæta við gjafakort* rekstur frá ríkiskvittun.
- Ekki prenta út greiðslukvittun ef hún samanstendur eingöngu af gjafakortalínum.
- Dragðu heildarupphæð gjafakorta sem eru gefin út eða endurhlaðin í færslu frá greiðslulínum fjárhagskvittunarinnar.
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
- Daglegar skýrslur (fjárhags X og fjárhagsáætlun Z) eru prentaðar með því að nota sniðið sem er fellt inn í fastbúnað fjárhagsprentarans.
- Fjárhagsprentarinn styður ekki blandaðar færslur. The **Bannað að blanda saman sölu og skilum í einni kvittun** valkostur ætti að vera stilltur á **Já** í POS virknisniðum.
- Sýnishornið styður aðeins samþættingu við fjárhagsprentara sem virkar í Registratore Telematico (RT) ham.

## <a name="set-up-fiscal-integration-for-italy"></a>Settu upp ríkisfjármálasamþættingu fyrir Ítalíu

Samþættingarsýni prentara fyrir Ítalíu er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Commerce SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ EpsonFP90III Dæmi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. The [sýnishorn](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) samanstendur af ríkisfjármálaskjalaveitu, sem er framlenging á viðskiptatímanum (CRT), og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Commerce SDK, sjá [Sæktu Commerce SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Samþættingarsýni prentara fyrir Ítalíu er fáanlegt í Commerce SDK frá og með Commerce útgáfu 10.0.29. Í Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)](emea-ita-fpi-sample-sdk.md).

Ljúktu við uppsetningarskref fjárhagssamþættingar eins og lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md).

1. [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taktu líka eftir stillingum fyrir fjárhagsskráningarferlið sem eru [sérstaklega fyrir þetta sýnishorn af samþættingu prentara](#set-up-the-registration-process).
1. [Settu upp fjárhagstexta fyrir afslætti](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Stilltu stillingar fyrir villumeðferð](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Settu upp fjárhagslegar X/Z skýrslur frá POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Virkja handvirka framkvæmd á frestað fjárhagsskráningu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Settu upp virkni fyrir stjórnun viðskiptavinaupplýsinga í POS](emea-ita-customer-information.md#setup).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Settu upp skráningarferlið

Til að virkja skráningarferlið skaltu fylgja þessum skrefum til að setja upp höfuðstöðvar Commerce. Fyrir frekari upplýsingar, sjá [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Sæktu stillingarskrár fyrir fjárhagsskjalaveituna og fjárhagstengið:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína.
    1. Opið **src \> Fiscal Integration \> EpsonFP90III Dæmi**.
    1. Sæktu stillingarskrá ríkisskjalaveitunnar á **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Stillingar \> DocumentProviderEpsonFP90IIISample.xml**.
    1. Sæktu stillingarskrá fjárhagstengis á **Vélbúnaðarstöð \> EpsonFP90III FiscalDeviceSample \> Stillingar \> Tengi EpsonFP90IIISample.xml**.

    > [!NOTE]
    > Fyrir Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Stillingarskrárnar fyrir þetta fjárhagslega samþættingarsýni eru staðsettar í eftirfarandi möppum í Retail SDK á VM þróunaraðila í LCS:
    >
    > - **Stillingarskrá ríkisskjalaveitanda:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extension.DocumentProvider.EpsonFP90IIISample\\ Stillingar\\ DocumentProviderEpsonFP90IIISample.xml
    > - **Stillingarskrá fjárhagstengis:** RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð\\ Viðbót.EpsonFP90IIIFiscalDeviceSample\\ Stillingar\\ Tengi EpsonFP90IIISample.xml

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingaskrá fjárhagsskjalaveitunnar sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Virknisnið fyrir tengi**. Búðu til nýtt virknisnið fyrir tengi. Veldu skjalaveituna og tengið sem þú hleður inn áðan. Uppfærðu [gagnakortastillingar](#default-data-mapping) eins og krafist er.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýtt tæknisnið fyrir tengi og veldu fjárhagstengi sem þú hleður inn áðan. Uppfærðu [tengistillingar](#fiscal-connector-settings) eins og krafist er.
6. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**. Stofna nýjan fjárhagstengihóp fyrir virknisniðið tengi sem þú bjóst til áður.
7. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**. Búðu til nýtt fjárhagsskráningarferli og fjárhagsskráningarferlisþrep og veldu fjárhagstengihópinn sem þú stofnaðir áðan.
8. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veldu virknisnið sem er tengt við verslunina þar sem skráningarferlið á að virkja. Á **Skráningarferli í ríkisfjármálum** Flýtiflipi, veldu fjárhagsskráningarferlið sem þú bjóst til áðan.
9. Fara til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Veldu vélbúnaðarsnið sem er tengt við vélbúnaðarstöðina sem fjárhagsprentarinn verður tengdur við. Á **Jaðartæki í ríkisfjármálum** Flýtiflipi, veldu tæknisniðið sem þú bjóst til áðan.
10. Opnaðu dreifingaráætlun (**Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**), og veldu störf **1070** og **1090** að flytja gögn í rásargagnagrunninn.

#### <a name="default-data-mapping"></a>Sjálfgefin gagnakortlagning

Eftirfarandi sjálfgefna gagnavörpun er innifalin í uppsetningu fjárhagsskjalaveitu sem er veitt sem hluti af fjárhagssamþættingarsýninu:

- **Kortlagning útboðstegunda** – Kortlagning greiðslumáta sem eru stilltir fyrir verslunina við greiðslutegundir sem fjárhagsprentari styður. Eftirfarandi dæmi sýnir sjálfgefna kortlagningu.

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
    - **PrinterPayment Type** og **PrinterPayment Index** eru samsvarandi greiðslutegund og vísitala sem eru skilgreind í Epson fjármálaprentaraskjölunum.
    - **Innborgunaraðferð** er notað til að tilgreina greiðslutegund og vísitölu prentara fyrir þann hluta pöntunarupphæðar viðskiptavinar sem er jafnaður með pöntun viðskiptavinar.

    Eftirfarandi tafla sýnir hvernig sýnishornsvörpun greiðslumáta samsvarar greiðslumáta verslunar sem eru stilltir í stöðluðum kynningargögnum.

    | Greiðslumáti | Heiti greiðsluháttar |
    |----------------|---------------------|
    | 1              | Reiðufé                |
    | 3              | Spjald                |
    | 4              | Viðskiptavinalykill    |
    | 6              | Gjaldmiðill            |
    | 8              | Gjafakort           |

    Þú verður að breyta sýnishorninu í samræmi við greiðslumáta sem eru stilltar í forritinu þínu.

- **Strikamerkistegund fyrir kvittunarnúmer** – Tegund strikamerkis sem er notað til að sýna kvittunarnúmer á reikningskvittun. Sjálfgefin kortlagning er **KÓÐI128**.
- **Prentaðu fjárhagsgögn í kvittunarhaus** – Ef kveikt er á þessari færibreytu verða upplýsingar um verslun prentaðar á fjárhagskvittun. Þessar upplýsingar innihalda nafn verslunarinnar, heimilisfang og skattanúmer og nafn gjaldkera.
- **Kortlagning ríkisprentaradeildar** – Kortlagning deilda skattprentara að virðisaukaskattshlutföllum (virðisaukaskatti), tegundum sem eru undanþegnir virðisaukaskatti og vörutegundum. Eftirfarandi dæmi sýnir sjálfgefna kortlagningu.

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
- **Virkja ókeypis hluti** – Ef kveikt er á þessari færibreytu er sérstakur *omaggio* afsláttarleiðréttingartegund fyrir vörur sem eru með 100 prósent afslátt er virkjuð.
- **Upplýsingakóði fyrir uppruna skila** – Upplýsingakóðinn sem er notaður til að fanga uppruna skilafærslu ef engin upprunaleg sölukvittun fylgir. Þessi breytu er notuð ásamt **Upplýsingakóði fyrir upprunalega söludagsetningu** og **Skila upprunakortlagningu** færibreytur til að búa til rétt skilaboð í fjárhagskvittun um uppruna skilafærslu ef engin upprunaleg sölufærsla er til. 

    Þessi upplýsingakóði ætti að vera stilltur til að gera notandanum kleift að velja eða slá inn einn af mögulegum uppruna skila í verslunum þínum. Til dæmis er hægt að stilla það sem lista yfir undirkóða (svo sem **Til baka af síðunni** eða **Til baka frá söluturni**). The **Skila upprunakortlagningu** færibreyta er síðan notuð til að þýða gildi upplýsingakóðans í skipun fyrir fjárhagsprentarann.

    Upplýsingakóðinn sem er valinn fyrir **Upplýsingakóði fyrir uppruna skila** ætti að vera stilltur sem skyldubundinn upplýsingakóði sem er rekinn einu sinni í hverja sölufærslu. Það ætti að vera úthlutað sem **Skila vöru** upplýsingakóði í POS-virkniprófílnum, þannig að hann er ræstur þegar **Skila vöru** rekstur er keyrður.

    Ekkert sjálfgefið gildi er tilgreint fyrir þessa vörpun. Þú verður að velja upplýsingakóða sem er stilltur í forritinu þínu.

- **Upplýsingakóði fyrir upprunalega söludagsetningu** – Upplýsingakóðinn sem er notaður til að fanga upprunalega söludagsetningu fyrir skilafærslu ef engin upprunaleg sölukvittun fylgir. Þessi breytu er notuð ásamt **Upplýsingakóði fyrir uppruna skila** og **Skila upprunakortlagningu** færibreytur til að búa til rétt skilaboð í fjárhagskvittun um uppruna skilafærslu ef engin upprunaleg sölufærsla er til.

    Upplýsingakóðinn ætti að vera stilltur þannig að **Tegund inntaks** reiturinn er stilltur á **Dagsetning**. Hann ætti að vera stilltur sem skyldubundinn upplýsingakóði sem er rekinn einu sinni í hverja sölufærslu. Það ætti einnig að vera úthlutað sem **Tengdur upplýsingakóði** fyrir upplýsingakóðann sem er valinn fyrir **Upplýsingakóði fyrir uppruna skila** færibreytu, þannig að upplýsingakóðarnir tveir eru sendir hver á eftir öðrum.

    Ekkert sjálfgefið gildi er tilgreint fyrir þessa vörpun. Þú verður að velja upplýsingakóða sem er stilltur í forritinu þínu.

- **Skila upprunakortlagningu** – Kortlagning á uppruna skila sem er notuð til að prenta uppruna skilafærslu ef engin upprunaleg sölukvittun fylgir. Þessi breytu er notuð ásamt **Upplýsingakóði fyrir uppruna skila** og **Upplýsingakóði fyrir upprunalega söludagsetningu** færibreytur til að búa til rétt skilaboð í fjárhagskvittun um uppruna skilafærslu ef engin upprunaleg sölufærsla er til. Eftirfarandi dæmi sýnir sjálfgefna kortlagningu.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Hér er útskýring á eigindunum í þessari kortlagningu:

    - **ReturnOrigin** er einn af mögulegum uppruna skila í verslunum þínum. Gildið ætti að samsvara gildi á **Upplýsingakóði fyrir uppruna skila** breytu.
    - **PrinterReturnOrigin** er einn af þeim skilaupprunum sem fjárhagsprentarinn samþykkir (**POS**, **·**, eða **ND**).
    - **PrinterReturnOriginWithoutFiscal Data** er skilauppruni sem fjárhagsprentari samþykkir og samsvarar skilafærslu sem er tengd upprunalegri sölufærslu sem hefur ekki tengd fjárhagsgögn vegna þess að hún var ekki skráð í gegnum fjárhagsprentara. Í þessu tilviki er upprunalega söludagsetningin auðkennd sem dagsetning upphaflegu sölufærslunnar.

Eftirfarandi sjálfgefna gagnakortanir eru úreltar og eru aðeins geymdar vegna bakábaks samhæfni:

- Kortlagning virðisaukaskatts (VSK) kóða
- Greiðslugerð innborgunar

#### <a name="fiscal-connector-settings"></a>Stillingar fjárhagstengis

Eftirfarandi stillingar eru innifaldar í fjárhagstengistillingunni sem er hluti af fjárhagssamþættingarsýninu:

- **Heimilisfang endapunkts** – Vefslóð prentarans.
- **Samstilling dagsetningar og tíma** – Gildi sem tilgreinir hvort samstilla þarf dagsetningu og tíma prentarans við tengda vélbúnaðarstöðina.

### <a name="configure-channel-components"></a>Stilltu rásaríhluti

> [!NOTE]
> - Samþættingarsýni prentara fyrir Ítalíu er fáanlegt í Commerce SDK frá og með Commerce útgáfu 10.0.29. Í Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)](emea-ita-fpi-sample-sdk.md).
> - Viðskiptasýni sem eru notuð í umhverfi þínu eru ekki sjálfkrafa uppfærð þegar þú notar þjónustu- eða gæðauppfærslur á Commerce íhlutum. Þú verður að uppfæra nauðsynleg sýni handvirkt.

#### <a name="set-up-the-development-environment"></a>Settu upp þróunarumhverfið

Til að setja upp þróunarumhverfi til að prófa og stækka úrtakið skaltu fylgja þessum skrefum.

1. Klóna eða hlaða niður [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla. Veldu rétta útgáfuútgáfu í samræmi við SDK/forritsútgáfu þína. Fyrir frekari upplýsingar, sjá [Sæktu Commerce SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu fjárhagslega prentarasamþættingarlausnina á **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ EpsonFP90III Dæmi\\ EpsonFP90IIISample.sln**, og byggja það.
1. Settu upp CRT viðbætur:

    1. Finndu CRT uppsetningarforrit fyrir viðbót:

        - **Eining viðskiptaskala:** Í **EpsonFP90III Dæmi\\ ScaleUnit\\ ScaleUnit.EpsonFP90III.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ScaleUnit.EpsonFP90III.Installer** uppsetningarforrit.
        - **Staðbundið CRT á Modern POS:** Í **EpsonFP90III Dæmi\\ ModernPOS\\ ModernPOS.EpsonFP90III.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ModernPOS.EpsonFP90III.Installer** uppsetningarforrit.

    1. Byrjaðu á CRT uppsetningarforrit fyrir viðbót frá skipanalínunni:

        - **Eining viðskiptaskala:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á Modern POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Settu upp viðbætur fyrir vélbúnaðarstöð:

    1. Í **EpsonFP90III Dæmi\\ Vélbúnaðarstöð\\ HardwareStation.EpsonFP90III.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **HardwareStation.EpsonFP90III.Installer** uppsetningarforrit.
    1. Byrjaðu uppsetningarforritið frá skipanalínunni:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgdu skrefunum í [Setja upp byggingarleiðslu fyrir fjárhagslega samþættingarsýni](fiscal-integration-sample-build-pipeline.md) að búa til og gefa út Cloud Scale Unit og sjálfsafgreiðslupakka fyrir samþættingarúrtakið í ríkisfjármálum. The **EpsonFP90III build-pipeline.yml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarsýni prentara fyrir Ítalíu er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Commerce SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ EpsonFP90III Dæmi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. The [sýnishorn](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) samanstendur af ríkisfjármálaskjalaveitu, sem er framlenging á CRT, og fjárhagstengi, sem er framlenging á Commerce Hardware Station. Fyrir frekari upplýsingar um hvernig á að nota Commerce SDK, sjá [Sæktu Commerce SDK sýnishorn og tilvísunarpakka frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Samþættingarsýni prentara fyrir Ítalíu er fáanlegt í Commerce SDK frá og með Commerce útgáfu 10.0.29. Í Commerce útgáfu 10.0.28 eða eldri, verður þú að nota fyrri útgáfu af Retail SDK á VM þróunaraðila í LCS. Fyrir frekari upplýsingar, sjá [Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)](emea-ita-fpi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur viðbyggingarinnar sem er fjárhagsskjalaveita er að búa til prentarasértæk skjöl og meðhöndla svör frá fjárhagsprentaranum.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **DocumentProvider EpsonFP90III** meðhöndlun beiðni er inngangsstaður beiðninnar um að búa til skjöl frá fjárhagsprentaranum.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar prentarasértæku skjali sem ætti að vera skráð í fjárhagsprentara.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er eru eftirfarandi atburðir studdir: sala, prentun X skýrslu og prentun Z skýrslu.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagsskjalaveituna er staðsett á **src\\ Fiscal Integration\\ EpsonFP90III Dæmi\\ CommerceRuntime\\ DocumentProvider.EpsonFP90IIISample\\ Stillingar\\ DocumentProviderEpsonFP90IIISample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur viðbótarinnar sem er fjárhagstengi er að hafa samskipti við fjárhagsprentarann. Þessi viðbót notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar á fjárhagsprentarann. Það sér einnig um svör sem berast frá fjármálaprentara.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **EpsonFP90III Dæmi** meðhöndlun beiðna er inngangsstaðurinn til að meðhöndla beiðni til ríkisútlæga tækisins.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **SubmitDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til prentara og skilar svari frá fjármálaprentara.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun tækisins.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla prentara.

#### <a name="configuration"></a>Skilgreining

Stillingarskrá fyrir fjárhagstengið er staðsett á **src\\ Fiscal Integration\\ EpsonFP90III Dæmi\\ Vélbúnaðarstöð\\ EpsonFP90III FiscalDeviceSample\\ Stillingar\\ Tengi EpsonFP90IIISample.xml** í [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

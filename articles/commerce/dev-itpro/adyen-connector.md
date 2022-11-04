---
title: Yfirlit Dynamics 365 Payment Connector fyrir Adyen
description: Þessi grein veitir yfirlit yfir Microsoft Dynamics 365 greiðslutengi fyrir Adyen.
author: rassadi
ms.date: 10/27/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 931fc69cda8daa2e06b6f1155fbf0369fd2bca55
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728295"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Yfirlit Dynamics 365 Payment Connector fyrir Adyen

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir Microsoft Dynamics 365 greiðslutengi fyrir Adyen og inniheldur alhliða lista yfir studda eiginleika og virkni. Tengdar greinar fjalla um Adyen skráningu, uppsetningu tengisins, algengar spurningar og leiðbeiningar um bilanaleit fyrir nokkur algeng vandamál.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | Lýsing |
|---|---|
| Greiðslutengill | Framlenging sem auðveldar samskipti á milli Microsoft Dynamics 365 Commerce (og tengdir íhlutir) og greiðsluþjónustu. Tengið sem lýst er í þessari grein var útfært með því að nota staðlaða greiðsluhugbúnaðarþróunarbúnaðinn (SDK). |
| Kort til staðar | Vísar til greiðsluviðskipta þar sem líkamlegt kort er framvísað og notað á tengi greiðslustöðvar við Dynamics 365 sölustað. |
| Kort ekki til staðar | Vísar til greiðsluviðskipta þar sem líkamlegt kort er ekki til staðar, svo sem rafræn viðskipti eða símaver. Í þessum tilfellum eru greiðslutengdar upplýsingar færðar inn handvirkt annaðhvort á vefsvæði rafrænna viðskipta, símaversflæði eða á sölustað eða greiðslustöð. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Styður eiginleikar, virkni, útgáfur og útstöðvar

Dynamics 365 Payment Connector fyrir Adyen sem er útúr kassanum notar staðlaða greiðslu SDK. Þess vegna hefur það ekki sérstaka möguleika sem eru ekki einnig í boði fyrir önnur greiðslutengi.

### <a name="supported-versions"></a>Studdar útgáfur

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 studdar útgáfur
Fyrsta aðila út-af kassa Dynamics 365 Payment Connector fyrir Adyen er studdur í Microsoft Dynamics 365 Finance útgáfa 8.1.3 (janúar 2019) eða síðar, og í Microsoft Dynamics 365 Retail útgáfu 8.1.3 eða nýrri. Hins vegar geta þriðju aðilar enn þróað önnur greiðslutengi fyrir Adyen fyrir fyrri útgáfur af Microsoft Dynamics 365.

#### <a name="supported-adyen-firmware-versions"></a>Styður Adyen vélbúnaðarútgáfur

Listinn hér að neðan lýsir lágmarks- og hámarksútgáfum Adyen vélbúnaðar sem eru studdar fyrir hverja útgáfu af Microsoft Dynamics 365 Retail POS.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS útgáfa 10.0.25
| Lágmarks Adyen fastbúnaðarútgáfa | Hámarks Adyen fastbúnaðarútgáfa |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS útgáfa 10.0.26
| Lágmarks Adyen fastbúnaðarútgáfa | Hámarks Adyen fastbúnaðarútgáfa |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS útgáfa 10.0.27
| Lágmarks Adyen fastbúnaðarútgáfa | Hámarks Adyen fastbúnaðarútgáfa |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS útgáfa 10.0.28
| Lágmarks Adyen fastbúnaðarútgáfa | Hámarks Adyen fastbúnaðarútgáfa |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS útgáfa 10.0.29
| Lágmarks Adyen fastbúnaðarútgáfa | Hámarks Adyen fastbúnaðarútgáfa |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS útgáfa 10.0.30
| Lágmarks Adyen fastbúnaðarútgáfa | Hámarks Adyen fastbúnaðarútgáfa |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen gæti gefið út minniháttar útgáfuuppfærslur eftir að Microsoft hefur prófað helstu útgáfuna. Svo lengi sem meiriháttar útgáfa er studd er í lagi að hafa minniháttar útgáfuuppfærslur innan sömu aðalútgáfunnar. Þessar uppfærslur eru venjulega mjög markvissar lagfæringar og standast ekki mælistikuna fyrir fulla endurprófun, svo framarlega sem sama aðal fastbúnaðarútgáfan var áður prófuð. Uppfærslur ættu ekki að fara yfir hámarks Adyen fastbúnaðarútgáfu sem skráð er í skjölum. 
>
> Flutningur frá Adyen fastbúnaðarútgáfu fyrr en útgáfu 53 í útgáfu 53 krefst POS KB **4577957** fyrir mánaðarlegar uppfærslur á Commerce, útgáfur 10.0.11 til 10.0.14. Ef ein af þessum útgáfum er í notkun og inniheldur ekki flýtileiðréttinguna mun eftir uppfærsla á greiðslustöðinni aðeins leyfa greiðslur í gegnum NFC. Með því að nota flýtileiðréttinguna á POS leysir þetta vandamál. Ef POS útgáfan er eldri en útgáfa 10.0.11 skaltu leggja fram stuðningsbeiðni og taka fram að lagfæring fyrir KB **4577957** er krafist fyrir MPOS sem er ekki í notkun.
> 
> Fyrir Adyen vélbúnaðarútgáfur 59p7 til 62p9, the **gjafakort útborgun** aðgerð biður um PIN-færslu tvisvar í tilfellum þar sem gjafakortið er slegið inn handvirkt. Þetta tölublað er ekki afritað þegar gjafakortinu er strjúkt. Adyen er að rannsaka málið. 

### <a name="supported-payment-terminals"></a>Stuðlar greiðslustöðvar
Dynamics 365 Payment Connector fyrir Adyen nýtir sér tækjabúnaðinn [Adyen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api). Það styður allar greiðslustöðvar sem þetta forritunarviðmót (API) styður. Til að fá heildarlista yfir studdar greiðslustöðvar, farðu á [Adyen POS útstöðvar](https://www.adyen.com/pos-payments/terminals) síðu.

### <a name="supported-payment-instruments"></a>Stutt greiðslumiðlar

#### <a name="supported-debit-and-credit-cards"></a>Stuðningur við debet- og kreditkort

| Vörumerki | Vöruvíddasamsetning | Kort til staðar | Rafræn viðskipti | Símaver |
|---|---|:-:|:-:|:-:|
| MasterCard | Kredit | ✔ | ✔ | ✔ |
| MasterCard | Debet | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank bónus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro Bretlandi | ✔ | ✔ | ✔ |
| VISA | Kredit | ✔ | ✔ | ✔ |
| VISA | Debet | ✔ | ✔ | ✔ |
| VISA | Alpha Bank bónus | ✔ | ✔ | ✔ |
| VISA | Android Borga | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia kort | ✔ | ✔ | ✔ |
| AMEX | Kredit | ✔ | ✔ | ✔ |
| AMEX | Debet | ✔ | ✔ | ✔ |
| AMEX | Android Borga | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX auglýsing | ✔ | ✔ | ✔ |
| AMEX | AMEX neytandi | ✔ | ✔ | ✔ |
| AMEX | AMEX fyrirtæki | ✔ | ✔ | ✔ |
| AMEX | AMEX smáfyrirtæki | ✔ | ✔ | ✔ |
| Uppgötva | Staðlað | ✔ | ✔ | ✔ |
| Uppgötva | Android Borga | ✔ |  |  |
| Uppgötva | Apple Pay | ✔ |  |  |
| Uppgötva | Samsung Pay | ✔ |  |  |
| Diners   | Staðlað | ✔ | ✔ | ✔ |
| Dineromail | Staðlað | ✔ | ✔ | ✔ |
| JCB | Staðlað | ✔ | ✔ | ✔ |
| Union Pay\* | Staðlað | ✔ |  |  |
| Interac debet\* | Staðlað | ✔ |  |  |

\* Interac og Union Pay endurtekið kortalyki eru ekki veitt af Adyen, svo ekki er hægt að styðja þau fyrir færslur sem ekki eru til staðar.

#### <a name="supported-gift-cards"></a>Stuðningur við gjafakort
| Áætlun | Kort til staðar | Kort ekki til staðar |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Til að styðja við þessi ytri gjafakortakerfi í gegnum Dynamics 365 Payment Connector fyrir Adyen, verður þú að ljúka við viðbótarskref. Fyrir frekari upplýsingar, sjá [Stuðningur við ytri gjafakort](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Stuðningur veski

| Áætlun | Kort til staðar | Kort ekki til staðar |
|---|---|---|
| Alipay | Stuðningi verður bætt við í framtíðarútgáfu. | Nr. |
| WeChat | Stuðningi verður bætt við í framtíðarútgáfu. | Nr. |

#### <a name="supported-card-present-input-methods"></a>Stuðningur kort til staðar innsláttaraðferðir
| Inntaksaðferð | Stutt | Athugasemdir |
|---|:-:|---|
| Dýfa | ✔ | |
| Kortalestur | ✔ | |
| Bankaðu á | ✔ | |
| Handvirk innslátt í gegnum POS UI. |  | Ekki stutt eins og er |
| Handvirk innkoma í gegnum greiðslustöð. | ✔ | Styður handvirka innslátt kredit-, debet- og gjafakorta með pinnafærslu. | 


#### <a name="supported-card-present-countries"></a>Stuðningur kort til staðar lönd

Eftirfarandi lönd eru með viðskiptaíhluti tiltæka og kortastuðning frá Adyen. Fyrir núverandi alþjóðlegt framboð á verslun, heimsækja [Alþjóðleg framboð síða](/dynamics365/get-started/availability).

| Land | Stutt |
| --- | :-: |
| Ástralía | ✔ |
| Austurríki | ✔ |
| Belgía | ✔ |
| Kanada | ✔ |
| Tékkland | ✔ |
| Danmörk | ✔ |
| Eistland | ✔ |
| Finnland | ✔ |
| Frakkland | ✔ |
| Þýskaland | ✔ |
| Hong Kong (sérstjórnarsvæði) | ✔ |
| Ungverjaland | ✔ |
| Ísland | ✔ |
| Írland | ✔ |
| Ítalía | ✔ |
| Japan | Framtíðarútgáfa |
| Lettland | ✔ |
| Litháen | ✔ |
| Malasía | ✔ |
| Holland | ✔ |
| Nýja-Sjáland | ✔ |
| Noregur | ✔ |
| Pólland | ✔ |
| Singapúr | ✔ |
| Sviss | ✔ |
| Spánn | ✔ |
| Svíþjóð | ✔ |
| Sviss | ✔ |
| Bretland | ✔ |
| Bandaríkin | ✔ |
| Brasilía | Framtíðarútgáfa |

#### <a name="supported-card-not-present-countries"></a>Stuðningskort eru ekki til staðar í löndum

Eftirfarandi lönd eru studd af Adyen fyrir færslur sem ekki eru til staðar. [Hafðu samband við Adyen](https://www.adyen.com/contact/sales) fyrir upplýsingar um stuðning fyrir tiltekið land. Fyrir núverandi alþjóðlegt framboð á verslun, heimsækja [Alþjóðleg framboð síða](/dynamics365/get-started/availability).

| Land | 
| --- |
| Argentína |
| Armenía |
| Ástralía |
| Austurríki |
| Barein |
| Belgía |
| Brasilía |
| Búlgaría |
| Kanada |
| Síle |
| Kína |
| Kólumbía |
| Króatía |
| Kýpur |
| Tékkland  |
| Danmörk |
| Egyptaland |
| Eistland |
| Finnland |
| Frakkland |
| Georgía |
| Þýskaland |
| Gíbraltar |
| Grikkland |
| Guernsey |
| Hong Kong (sérstjórnarsvæði) |
| Ungverjaland |
| Ísland |
| Indland |
| Indónesía |
| Írland |
| Mön |
| Ísrael |
| Ítalía |
| Japan |
| Jersey |
| Suður-Kórea |
| Kúveit |
| Lettland |
| Litháen |
| Lúxemborg |
| Malasía |
| Malta |
| Mexíkó |
| Marokkó |
| Holland |
| Nýja-Sjáland |
| Noregur |
| Perú |
| Pólland |
| Portúgal |
| Katar |
| Rúmenía |
| Sádi-Arabía |
| Serbía |
| Singapúr |
| Slóvakía |
| Slóvenía |
| Suður-Afríka |
| Spánn |
| Svíþjóð |
| Sviss |
| Taívan |
| Tansanía |
| Taíland |
| Tyrkland |
| Sameinuðu arabísku furstadæmin (UAE) |
| Bretland |
| Bandaríkin þar á meðal Puerto Rico  |

#### <a name="supported-dynamics-365-payment-features"></a>Styður Dynamics 365 greiðslueiginleikar

Eftirfarandi tafla sýnir mengi eiginleika sem Dynamics 365 Payment Connector fyrir Adyen styður. Þessir eiginleikar nota endurbætur sem voru kynntar í SDK greiðslum og sumum íhlutum í desember 2018. Þau eru ekki eingöngu fyrir Dynamics 365 Payment Connector fyrir Adyen. Fyrir frekari upplýsingar um hvernig á að nota þessar endurbætur fyrir annan greiðslutengi, sjá [Búðu til enda-til-enda greiðslusamþættingu fyrir greiðslustöð](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Áætlun | Kort til staðar | Kort ekki til staðar |
|---|:-:|:-:|
| [Útborgun gjafakortsstaða](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Tvítekin greiðsluvernd](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Omni Channel Tokenization | ✔ | ✔ |
| Tengdar endurgreiðslur | ✔<br>(Byrjar á 10.0.1) | ✔<br>(Byrjar á 10.0.1) |
| [Sparaðu netgreiðslur](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Byrjar á 10.0.2) | 
| [Ytri gjafakort fyrir símaver og rafræn viðskipti](./gift-card.md) | ✔<br>(Byrjar á 10.0.10) | 
| [SCA greiðslutilvísun](../adyen_redirect.md) | | ✔<br>(Byrjar á 10.0.12) |
| [Sérnýttar greiðslustöðvar og kvaðningar fyrir prentara og peningaskúffu](../pos-multi-hws.md) | ✔<br>(Byrjar á 10.0.12) | |
| [SDK-stigi veltistuðningur í gegnum Adyen tengið](tipping.md) | ✔<br>(Byrjar á 10.0.14) | |
| [Stigvaxandi upptaka fyrir reikningsfærslu pantana](incremental-capture.md) |  | ✔<br>(Byrjar á 10.0.18) |
| [Veski Greiðslur](../wallets.md) |  | ✔<br>(Byrjar á 10.0.20) |
| [Google Pay með Adyen](google-pay-adyen.md) |  | ✔<br>(Byrjar á 10.0.27) |

## <a name="next-steps"></a>Næstu skref

Fyrir upplýsingar um skráningu á og stilla Dynamics 365 Payment Connector fyrir Adyen, sjá [Dynamics 365 Payment Connector fyrir Adyen uppsetningu](adyen-connector-setup.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp Dynamics 365 Payment Connector fyrir Adyen](adyen-connector-setup.md)

[Algengar spurningar um Dynamics 365 Payment Connector fyrir Adyen](adyen-connector-faq.md)

[Úrræðaleit fyrir Dynamics 365 Payment Connector fyrir Adyen](adyen-connector-troubleshoot.md)

[Algengar spurningar um greiðslur](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]

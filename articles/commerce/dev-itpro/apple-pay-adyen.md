---
title: Settu upp Apple Pay með Adyen inn Dynamics 365 Commerce
description: Þessi grein lýsir því hvernig á að setja upp Apple Pay með Adyen í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780208"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Settu upp Apple Pay með Adyen inn Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein lýsir því hvernig á að setja upp Apple Pay með Adyen í Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | Lýsing |
|---|---|
| Apple Pay | Einnig þekktur sem Apple Pay „hnappurinn“, Apple Pay er veskisgreiðslutilboð sem er stutt í gegnum Adyen tengið. Það gerir upplifun viðskiptavina og samþættingu kleift sem er studd af Microsoft Dynamics 365 Apple Pay tengi. |
| Veski | Greiðslutegund sem inniheldur ekki hefðbundna greiðslueiginleika, eins og bankakenninúmer (BIN) svið og gildistíma sem eru notuð til að greina á milli kredit- og debetkortategunda. |

Dynamics 365 Commerce býður upp á samþættingu úr kassa fyrir Apple Pay þegar Adyen greiðslugáttarþjónustan er notuð. Apple Pay er greiðslumáti með stafrænu veski sem notar Apple Pay söluaðilareikning í samræmi við Adyen greiðsluþjónustuna. Þegar hann er stilltur er Apple Pay hnappurinn valinn greiðslumáti sem er hluti af pöntunarsíðu netverslunar. Apple Pay hnappurinn er aðeins sýndur sem greiðslumöguleiki fyrir studd Apple Pay tæki. Þegar notendur velja **Apple Pay** í studdum vafra eða tæki er þeim vísað til Apple Pay þjónustunnar til að ganga frá greiðslu beint. Þeim er síðan skilað í netverslunina til að ljúka pöntunum.

Tilvísun Dynamics 365 Payment Connector for Apple Pay tengi er notað til viðbótar við Dynamics 365 Payment Connector fyrir Adyen til að virkja Apple Pay og kreditkortagreiðslur á vefsvæði. Apple Pay er einnig hægt að stilla til notkunar í verslunum sem hafa Adyen greiðslustöðvar sem nota Dynamics 365 Payment Connector fyrir Adyen með Commerce sölustaðnum (POS). Í þessu tilviki sér Dynamics 365 Payment Connector fyrir Adyen um töppun Apple Payment tækisins í gegnum flugstöðina.

## <a name="prerequisites"></a>Forkröfur

Apple kaupmannsreikningur er nauðsynlegur til að nota Apple Pay með Adyen í Commerce. Fyrir upplýsingar um hvernig á að setja upp Apple Pay á prófunarsvæðinu þínu, sjá [Apple Pay Drop-in samþætting](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Fyrir upplýsingar um hvað á að gera þegar þú ert tilbúinn að fara í notkun í framleiðsluumhverfi þínu, sjá [Fer í beinni](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Apple Pay greiðslumátinn verður einnig að vera samþættur Adyen reikningnum þínum. Adyen getur hjálpað þér að setja upp greiðslumátann og getur einnig hjálpað til við að tryggja að lénunum sem þú notar vottorðið fyrir sé úthlutað til notkunar með vottorðinu.

Til að virkja endurbættan veskiseiginleikafánann í höfuðstöðvum Commerce, farðu á **Vinnurými \> Eiginleikastjórnun**, og leitaðu að **Aukinn stuðningur við veski og endurbætur á greiðslum** eiginleiki. Veldu eiginleikann og veldu síðan **Virkja**. Eftir að aðgerðin hefur verið virkjað skaltu keyra **1110** dreifingaráætlun til að gera breytinguna aðgengilega á öllum rásum.

## <a name="map-the-apple-pay-payment-method"></a>Kortleggðu Apple Pay greiðslumátann

Apple Pay er greiðslumáti með stafrænu veski. Fyrir upplýsingar um hvernig á að setja upp greiðslukortlagningu fyrir Apple Pay, sjá [Greiðslustuðningur fyrir veski](../wallets.md).

Til að kortleggja Apple Pay greiðslumáta í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Fara til **Verslun og verslun \> Rásaruppsetning \> Greiðslumáta \> Tegundir korta**.
1. Veldu **Nýtt** til að bæta við línu fyrir Apple Pay og stilltu eftirfarandi gildi:

    - **auðkenni:** ApplePay
    - **Rafræn greiðsluheiti:** Apple Pay
    - **Tegund:** Veski
    - **Útgefandi:** Epli

1. Veldu **Kortlagning örgjörva** að opna **Greiðslukortlagningaraðferðir örgjörva** valmynd. The **Ókortlagðar greiðslumáta örgjörva** dálkurinn sýnir studdar greiðslumáta fyrir hvert tiltækt tengi (Adyen, PayPal og Apple).
1. Kortleggðu studdu greiðslumáta sem þú vilt fyrir báða **Dynamics 365 greiðslutengi fyrir Adyen** tengi (til notkunar á POS) og **Dynamics 365 greiðslutengi fyrir Apple Pay** tengi (fyrir netrásina).
1. Fyrir hverja kortlagningarlínu, í **Ókortlagðar greiðslumáta örgjörva** dálk, veldu línuna til að styðja og veldu síðan **Bæta við** til að færa valið í **Kortlagðar greiðslumáta örgjörva** dálki.
1. Veldu **Allt í lagi**, og síðan, á **Tegundir korta** síðu, veldu **Vista**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Settu upp Apple Pay vottorðið fyrir síðuna þína

Fyrir hverja síðu verður þú að hlaða upp lénstengingarskránni (einnig þekkt sem Apple Pay vottorðið) eins og lýst er í [Adyen Apple Pay skjöl](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). Þú getur notað Commerce site builder til að hlaða upp lénstengingarskránni á Media Library fyrir síðuna þína.

Til að setja upp Apple Pay vottorðið í vefsíðugerð skaltu fylgja þessum skrefum.

1. Sæktu skírteinið (lénstengingarskrá) frá [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Bættu .txt endingunni við lénstengingarskrána.
1. Í vefsíðugerð, [hlaða upp](../upload-serve-static-files.md) lénstengingarskrána í Media Library síðunnar þinnar.
1. Fara til **vefslóðir**.
1. Veljið **Nýtt \> Ný vefslóð**.
1. Í **Ný vefslóð** valmynd, veldu **Media Library eign**.
1. Í **URL slóð** reit, sláðu inn slóð vefslóðarinnar (ef hún er ekki þegar slegin inn). Sláðu inn eftirfarandi Apple streng á eftir lénsgrunnslóðinni:`<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Veljið **Næst**. Fjölmiðlabókasafnið sýnir allar upphlaðnar fjölmiðlaeignir **skjal** (.txt) gerð.
1. Veldu lénstengingarskrána sem ætti að birta fyrir beiðnir á vefslóðina sem þú skilgreindir áður.
1. Velja **Stofna**.

Á þessu stigi hefur vefslóðin sem var stofnuð stöðuna drög. Birtu slóðina til að ljúka ferlinu. Skránni sem vefslóðin bendir á verður ekki skilað fyrr en vefslóðin er birt.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Stilltu Commerce netverslun fyrir Apple Pay

Til að stilla Commerce netverslun fyrir Apple Pay skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásir \> Netverslanir**.
1. Veldu **Auðkenni smásölurásar** gildi netverslunarrásar síðunnar þinnar.
1. Á **Greiðslureikningar** flýtiflipann, bættu við **Dynamics 365 greiðslutengi fyrir Adyen** tengi, ef það er ekki þegar sett upp, með því að fylgja leiðbeiningunum í [Settu upp Dynamics 365 Payment Connector fyrir Adyen](adyen-connector-setup.md).
1. Eftir að Adyen tengið hefur verið stillt skaltu velja **Bæta við** að bæta við **Dynamics 365 greiðslutengi fyrir Apple Pay** tengi.
1. Færðu inn gildi fyrir eignir tengisöluaðila.

    | Eiginleiki               | Lýsing | Áskilið | Sjálfkrafa stillt | Sýnisgildi |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Samsetningarheiti          | Heiti samsetningar fyrir Dynamics 365 Payment Connector fyrir Apple Pay. | Já | Já | Tvöfaldur nafn |
    | Auðkenni þjónustureiknings     | Einkvæmt auðkenni uppsetningar sölueiginleika. Þetta auðkenni er stimplað á greiðslufærslur og auðkennir sölueiginleikana sem eftirvinnsluferli (eins og reikningagerð) ættu að nota. | Já | Já | Guid |
    | Auðkenni söluaðilareiknings    | Sláðu inn einstakt Adyen kaupmannsauðkenni. Þetta gildi er gefið upp þegar þú skráir þig hjá Adyen eins og lýst er í [Skráðu þig hjá Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Já | Nr. | MerchantIdentifier |
    | API lykill í skýinu          | Sláðu inn Adyen Cloud API lykilinn. Þú getur fengið þennan lykil með því að fylgja leiðbeiningunum í [Hvernig á að sækja API lykilinn](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Já | Nr. | abcdefg |
    | Gateway umhverfi    | Farðu inn í Adyen hlið umhverfið til að kortleggja á. Möguleg gildi eru **Próf** og **Lifa**. Þú ættir að stilla þennan reit á **Lifa** aðeins fyrir framleiðslutæki og viðskipti. | Já | Já | Í beinni |
    | Studdir gjaldmiðlar   | Sláðu inn gjaldmiðlana sem tengið á að vinna úr. Í kortatilvikum getur Adyen stutt fleiri gjaldmiðla í gegnum [kraftmikla gjaldmiðilsbreytingu](https://www.adyen.com/pos-payments/dynamic-currency-conversion) eftir að viðskiptabeiðnin er send í greiðslustöðina. Hafðu samband við Adyen þjónustudeild til að fá lista yfir studda gjaldmiðla. | Já | Já | USD; EUR |
    | Studdir greiðslumátar | Sláðu inn tilboðsgerðirnar sem tengið á að vinna úr. | Já | Já | ApplePay |

1. Eftir að upplýsingar um söluaðila hafa verið færðar inn skaltu keyra **1070** rás stillingar dreifingaráætlun starf.

## <a name="configure-commerce-pos-for-apple-pay"></a>Stilltu Commerce POS fyrir Apple Pay

POS stillingin notar stillingar vélbúnaðarsniðsins **EFT þjónusta** reit fyrir Dynamics 365 Payment Connector fyrir Adyen. Í höfuðstöðvum Commerce skaltu stilla EFT þjónustuna fyrir Dynamics 365 Payment Connector fyrir Adyen eins og lýst er í [Settu upp Dynamics 365 POS vélbúnaðarprófílhluta](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Gakktu úr skugga um að þú bætir við **ApplePay** á lista yfir útboðstegundir í **Stuðlar útboðsgerðir** sviði. Notaðu semíkommur (;) til að aðgreina tilboðsgerðir í listanum.

Örgjörvakortlagningin fyrir Adyen tengið mun fanga veskiskortategundirnar sem eru notaðar af Apple Pay á POS flugstöðinni.

### <a name="configure-content-security-policies-in-site-builder"></a>Stilltu efnisöryggisstefnur í vefsíðugerð

Áður en þú stillir brotin þín eða síður til að nota Apple Pay, verður þú að tryggja að innihaldsöryggisstefnur (CSP) séu stilltar í Commerce site builder fyrir síðuna þína.

Fylgdu þessum skrefum til að stilla efnisöryggisstefnur í vefsíðugerð.

1. Farið í **Svæðisstillingar \> Viðbætur**.
1. Á **Innihaldsöryggisstefna** flipa, veldu **Bæta við** að bæta við línu sem hefur`https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` til **barn-src**, **-src**, **-src**, **-src**, **-src**, og **style-src** köflum.
1. Þegar þú hefur lokið skaltu velja **Vista og birta** að framfylgja breytingunum.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Settu upp Apple Pay sem greiðslumöguleika fyrir afgreiðslu

Fylgdu þessum skrefum til að setja upp Apple Pay sem greiðslumöguleika fyrir greiðslu á síðu (ekki hraðgreiðslu) síðunnar þinnar.

1. Í Site Builder, farðu á **Brot**, og veldu útskráningarbrot síðunnar þinnar.
1. Veljið **Breyta**.
1. Í **Gámur afgreiðsluhluta** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Apple Pay** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista**.
1. Veldu **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.

Stillingar fyrir **Apple Pay** einingin er innbyggð í eininguna og tengist uppsettu Dynamics 365 Payment Connector fyrir Apple Pay tengið sem er sett upp fyrir netrásina í höfuðstöðvum Commerce.

### <a name="apple-pay-payment-behavior"></a>Apple Pay greiðsluhegðun

The **Apple Pay** greiðsluhnappur er aðeins sýndur á studdum Apple Pay tækjum (iPhone, iPad og Safari vöfrum sem styðja Apple Pay). Ef notandi er ekki að nota eitt af þessum tækjum, **Apple Pay** greiðsluhnappur er falinn.

Þegar notandi velur **Apple Pay** greiðsluhnappur, an **Apple Pay** svarglugginn birtist. Þar getur notandinn auðkennt gegn Apple Pay tækinu sínu eða vafranum. The **Apple Pay** svarglugginn sýnir yfirlit yfir pöntunarupphæðina og greiðslumátann sem notandinn hefur stillt fyrir Apple Wallet sitt. Notandinn getur skoðað þessar upplýsingar og síðan valið **Borga** til að ganga frá greiðslunni. Eftir að greiðslu er lokið er notanda vísað á **Pöntun lokið** síða sem sýnir nákvæma pöntunaryfirlit fyrir lokið viðskipti.

## <a name="additional-resources"></a>Frekari upplýsingar

[Algengar spurningar um greiðslur](payments-retail.md)

[Greiðsluferliseining](../add-checkout-module.md)

[Greiðslueining](../payment-module.md)

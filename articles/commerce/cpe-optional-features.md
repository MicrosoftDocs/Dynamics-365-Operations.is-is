---
title: Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla valfrjálsa eiginleika Microsoft Dynamics 365 Commerce matsumhverfis.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6f7ba7e6de3791720458b509059f008423c73a82
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413054"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að grunnstilla valfrjálsa eiginleika Microsoft Dynamics 365 Commerce matsumhverfis.

## <a name="prerequisites"></a>Forkröfur

Ef þú vilt meta viðskipti tölvupóstsaðgerða verður að uppfylla eftirfarandi forsendur:

- Þú ert með tiltækan tölvupóstþjón (Simple Mail Transfer Protocol \[SMTP\] Server) sem hægt er að nota úr Microsoft Azure áskriftinni þar sem þú úthlutaði matsumhverfi.
- Þú ert með gilt lénsheiti (FQDN)/IP-tölu netþjónsins, SMTP-gáttarnúmer og staðfestingu upplýsingar tiltækar.

## <a name="configure-the-image-back-end"></a>Stilla bak myndarinnar

### <a name="find-your-media-base-url"></a>Finndu grunnvefslóð miðla

> [!NOTE]
> Áður en þú getur klárað þessa aðferð verður þú að klára skrefin í [Settu upp síðuna þína í Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).

1. Skráðu þig inn á Commerce-vefsmið með því að nota slóðina sem þú skráðir þegar þú ræstir e-Commerce á meðan úthlutun stóð (sjá [Frumstilla rafræn viðskipti](provisioning-guide.md#initialize-e-commerce)).
1. Opnið svæðið **Fabrikam**.
1. Á valmyndinni til vinstri skal velja **Efnissafn**.
1. Veldu einhverja staka myndeign.
1. Í eiginleikaeftirlitinu til hægri skaltu finna eiginleikann **Opinber vefslóð**. Gildið er vefslóð. Eftirfarandi er dæmi:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Skiptu út síðasta auðkenni í slóðinni (**MA1nQC** í dæminu hér að undan) með strengnum **search?fileName=**. Svona lítur vefslóðarsýnishornið út þegar þessi breyting er gerð:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Þessi slóð er grunnvefslóð miðla þinna. Skrifaðu það hjá þér.

### <a name="update-the-media-base-url"></a>Uppfærðu grunnvefslóð miðla

1. Skráðu þig inn á Commerce Headquarters.
1. Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Rásaforstillingar**.
1. Veljið **Breyta**.
1. Undir **Forstillingareiginleikum** skiptirðu út gildinu fyrir eiginleikann **Grunnvefslóð miðlaþjóns** með þeirri grunnvefslóð miðla sem þú stofnaðir áður.
1. Veldu rásina sem kallast **scXXXXXXXXX**.
1. Undir **Forstillingareiginleikar** velurðu **Bæta við**.
1. Veldu fyrir eignina sem var bætt við **Grunnvefslóð miðlaþjóns** sem eiginleikalykill. Sem eiginleikagildi skaltu slá inn grunnvefslóð miðla sem þú bjóst til áður.
1. Veljið **Vista**.

## <a name="configure-and-test-the-email-server"></a>Stilla og prófa póstþjóninn

> [!NOTE]
> SMTP-miðlarinn eða tölvupóstþjónustan sem þú slærð inn hér verða að vera aðgengileg innan Azure áskriftarinnar sem þú notar fyrir umhverfið.

1. Skráðu þig inn á Commerce Headquarters.
1. Notaðu valmyndina hér til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur tölvupósts**.
1. Á flipanum **SMTP-stillingar**, í reitnum **Þjónn fyrir sendan póst**, slærðu inn FQDN eða IP-tölu SMTP-netþjónsins eða tölvupóstþjónustunnar.
1. Í reitnum **SMTP-númer tengis** slærðu inn númer tengisins. (Ef þú ert ekki að nota Secure Sockets Layer \[SSL\] er sjálfgefið númer tengis **25**.)
1. Ef staðfesting er nauðsynleg skal slá inn gildi í reitina **Notandanafn** og **Lykilorð**.
1. Veljið **Vista**.
1. Veldu **Endurnýja**.
1. Á flipanum **Prufupóstur**, í reitnum **Tölvupóstveita**, velurðu **SMTP**.
1. Í reitinn **Senda til** slærðu inn netfangið sem prufupóstfangið skal afhent á.
1. Veldu **Senda prufupóst**.

## <a name="configure-email-templates"></a>Stilla tölvupóstsniðmát

Uppfæra verður tölvupóstsniðmátið fyrir hvert færslutilvik sem þú vilt senda tölvupóst með gildu netfangi sendanda.

1. Skráðu þig inn á Commerce Headquarters.
1. Notaðu valmyndina hér til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis**.
1. Veldu **Sýna lista**.
1. Fyrir hvert sniðmát á listanum skal fylgja eftirfarandi skrefum:

    1. Í reitinn **Netfang sendanda** slærðu inn netfang sendanda.
    1. Valfrjálst: Í reitinn **Nafn sendanda** slærðu inn nafnið sem ætti að nota sem nafn sendandans.

1. Veljið **Vista**.

## <a name="customize-email-templates"></a>Sérstilla sniðmát fyrir tölvupóst

Þú gætir viljað aðlaga tölvupóstsniðmátin þannig að þau noti mismunandi myndir. Eða þú gætir viljað uppfæra tengla í sniðmátunum þannig að þeir vísi í matsumhverfi. Þetta ferli útskýrir hvernig á að hala niður sjálfgefnu sniðmátunum, aðlaga þau og uppfæra sniðmátin í kerfinu.

1. Í vefvafra skal sækja upp [Microsoft Dynamics 365 Commerce Evaluation sjálfgefin zip-skrá fyrir tölvupóstsniðmát](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) í staðbundnu tölvunni. Þessi skrá inniheldur eftirfarandi HTML skjöl:

    - Eining pöntunarsniðmáts
    - Gefa út sniðmát gjafakorts
    - Nýtt pöntunarsniðmát
    - Umbúðapöntunarsniðmát
    - Tiltektarpöntunarsniðmát

1. Sérsniðið sniðmátin með texta- eða HTML-ritil. Sjá lista yfir [studd tákn](#supported-tokens-in-the-email-template) seinna í þessu efni.
1. Innskráning í Commerce.
1. Notaðu valmyndina til vinstri til að fara í **Einingar \> Fyrirtækisstjórnun \> Uppsetning \> Sniðmát tölvupósts fyrirtækis**.
1. Stækkaðu listann vinstra megin til að sjá öll sniðmát.
1. Fylgdu þessum skrefum fyrir hvert sniðmát sem þú vilt aðlaga:

    1. Veldu sniðmátið á listanum.
    1. Undir **Innihald tölvupóstskilaboða** velurðu viðeigandi tungumálarútgáfu af listanum. (Sjálfgefið tungumál er **en-us**).
    1. Undir **Efni tölvupóstskilaboða** velurðu **Breyta**. Glugginn **Hlaða upp sniðmáti fyrir tölvupóst** birtist.
    1. Veldu **Fletta** og finndu HTML-skjalið sem hefur sérsniðna innihaldið.
    1. Veldu **Hlaða upp**. Sniðmátinu er hlaðið inn í kerfið og forskoðun birtist.
    1. Veljið **Í lagi**.
    1. Valfrjálst: Sérsníða eiginleikann **Efni** í sniðmátinu.
    1. Veljið **Vista**.

### <a name="supported-tokens-in-the-email-template"></a>Studd tákn í tölvupóstsniðmátinu

Þegar tölvupóstur er gerður er þessum táknum skipt út fyrir raungildi sem eiga við viðskiptavin og pöntun viðskiptavinar.

#### <a name="sales-order"></a>Sölupöntun

Eftirfarandi tákn eiga við um heildarsölupöntunina.

| Heiti táknsins | Tákn |
|-------------------|-------|
| Pöntunarnúmer      | %salesid% |
| Nafn viðskiptavinar   | %customername% |
| Afh.aðsetur  | %deliveryaddress% |
| Póstfang greiðanda   | %customeraddress% |
| Pöntunardagsetning        | %shipdate% |
| Afhendingarmáti     | %modeofdelivery% |
| Afsláttur          | %discount% |
| Virðisaukaskattur         | %tax% |
| Heildarupphæð pöntunar       | %total% |

#### <a name="sales-line"></a>Sölulínur

Eftirfarandi táknum er skipt út með gildum fyrir hverja vöru í röðinni.

> [!NOTE]
> Settu táknið **Vörulisti - byrja** í byrjun HTML-bálksins sem er endurtekinn fyrir hverja vöru og settu táknið **Vörulisti - ljúka** í lok bálksins.

| Heiti táknsins      | Tákn |
|------------------------|-------|
| Afurðalisti - hefja   | \<!--%tablebegin.salesline% --\> |
| Afurðalisti - lok     | \<!--%tableend.salesline%--\> |
| Afurðarnafn           | %lineproductname% |
| lýsing            | %lineproductdescription% |
| Magn               | %linequantity% |
| Einingaverð línu        | %lineprice% (staðfesta) |
| Heildarfjöldi línuatriða        | %linenetamount% |
| línuafsláttur          | %linediscount% |
| Sendingardagsetning              | %lineshipdate% |
| Innkaupaaðferð     | %linedeliverymode% |
| afhendingaraðsetur       | %linedeliveryaddress% |
| Sölueining línunnar | %lineunit% |

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Úthluta Dynamics 365 Commerce matsumhverfi](provisioning-guide.md)

[Stilla Dynamics 365 Commerce matsumhverfi](cpe-post-provisioning.md)

[Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi](cpe-bopis.md)

[algengar spurningar um Dynamics 365 Commerce matsumhverfi](cpe-faq.md)

[Microsoft Dynamics Lifecycle Services (LSC)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
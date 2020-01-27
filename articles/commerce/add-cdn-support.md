---
title: Bæta við stuðningi fyrir efnisbirtingarnet (CDN)
description: Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2d64f0de5287a764cb2e40b99a08084494bf53c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945629"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Bæta við stuðningi fyrir efnisbirtingarnet (CDN)

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.

## <a name="overview"></a>Yfirlit

Þegar þú setur upp umhverfi rafrænna viðskipta í Dynamics 365 Commerce geturðu stillt það til að virka með CDN-þjónustunni. 

Hægt er að virkja sérsniðið lén þitt í úthlutunarferlinu fyrir umhverfi þitt með rafræn viðskipti. Einnig er hægt að nota þjónustubeiðni til að setja hana upp eftir að úthlutunarferlinu er lokið. Úthlutunarferlið fyrir umhverfi rafrænna viðskipta býr til hýsingarheiti sem er tengt umhverfinu. Þetta hýsingarheiti er með eftirfarandi sniði, þar sem *rafræn viðskipti-leigjanda-heiti* er heiti umhverfisins:

&lt;rafræn viðskipti-leigjanda-heiti&gt;.commerce.dynamics.com

Hýsingarheiti eða endastöð sem er mynduð í úthlutunarferlinu styður aðeins SSL-skírteini (Secure Sockets Layer) fyrir \*.commerce.dynamics.com. Það styður ekki SSL fyrir sérsniðin lén. Þess vegna verður þú að segja upp SSL fyrir sérsniðin lén í CDN og framsenda umferð frá CDN til hýsingarheitsins eða endapunktsins sem Commerce myndaði. 

Að auki er *tölfræðin* (JavaScript eða Cascading Style Sheets \[CSS\]-skrár) frá Commerce sýnd frá þeim endapunkti sem Commerce myndaði (\*.commerce.dynamics.com). Aðeins er hægt að afrita tölfræðina í skyndiminni ef hýsingarheiti eða endapunktur sem Commerce myndaði er sett á bak við CDN.

## <a name="set-up-ssl"></a>Setja upp SSL

Til að hjálpa til við að tryggja að SSL sé sett upp og að tölfræði sé vistuð í skyndiminni verður að stilla CDN þannig að það sé tengt við hýsingarheitið sem Commerce myndaði fyrir umhverfi þitt. Þú verður einnig að vista eftirfarandi mynstur fyrir tölfræði í skyndiminni: 

/\_msdyn365/\_scnr/\*

Eftir að þú hefur úthlutað Commerce-umhverfi þínu á sérsniðna lénið sem er veitt, eða eftir að þú hefur gefið sérsniðna lénið fyrir umhverfi þitt með því að nota þjónustubeiðni, skaltu beina sérsniðna léninu á hýsingarheitið eða endapunktinn sem Commerce myndaði.

Eins og áður var getið styður myndað hýsingarheiti eða endapunktur aðeins SSL-skírteini fyrir \*.commerce.dynamics.com. Það styður ekki SSL fyrir sérsniðin lén.

## <a name="cdn-services"></a>CDN-þjónusta

Hægt er að nota hvaða CDN-þjónustu sem er með Commerce-umhverfi. Hér eru tvö dæmi:

- **Microsoft Azure Útidyraþjónusta** - Azure CDN-lausnin. Fyrir frekari upplýsingar um Azure útidyraþjónustu, sjá [Þjónustuskjöl Azure Front Service](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** - Sjá frekari upplýsingar í [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>Uppsetning CDN

Uppsetningarferli CDN samanstendur af þessum almennu skrefum:

1. Bæta við framvinnsluhýsli.
1. Stilltu bakvinnslusafn.
1. Settu upp reglur fyrir beina og skyndiminni.

### <a name="add-a-front-end-host"></a>Bæta við framvinnsluhýsli

Hægt er að nota hvaða CDN þjónustu sem er, en til dæmis í þessu efni er Azure Front Door Service notað. 

Upplýsingar um hvernig á að setja upp Azure Front Door Service, sjá [Stuttur leiðarvísir: Búðu til útidyr fyrir víðfáanlegt altækt vefforrit](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Stilla bakvinnslusafn í Azure Front Door Service

Til að stilla bakvinnslusafn í Azure Front Door Service skaltu fylgja þessum skrefum.

1. Bæta við **&lt;ecom-leigjandi-nafn&gt;.commerce.dynamics.com** í bakvinnslusafn sem sérsniðinn hýsil sem er með tóma fyrirsögn bakvinnsluhýsingar.
1. Undir **Heilbrigðiseftirlit**, í reitnum **Slóð**, skaltu slá inn **/keepalive**.
1. Í reitinn **Millibil (sekúndur)** skaltu slá inn **255**.
1. Undir **Álagsjöfnun** skaltu skilja eftir sjálfgefin gildi.

Eftirfarandi mynd sýnir valmyndina **Bæta við bavinnslusafni** í Azure Front Door Service.

![Bæta við valmynd bakvinnslusafns](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Settu upp reglur í Azure Front Door Service

Fylgdu þessum skrefum til að setja upp beinareglu í Azure Front Door Service.

1. Bæta við beinareglu.
1. Í reitinn **Heiti** skal færa inn **sjálfgildi**.
1. Í reitnum **Samþykkt samskiptaregla** velurðu **HTTP og HTTPS**.
1. Í reitnum **Framvinnsluhýslar** skaltu slá inn **dynamics-ecom-tenant-name.azurefd.net**.
1. Undir **Mynstur til að passa** skaltu slá inn efri reitinn **/\***.
1. Undir **Upplýsingar um beini** stillirðu valkostinn **Gerð beinis** á **Áfram**.
1. Í reitnum **Bakvinnslusafn** velurðu **ecom-backend**.
1. Í reitahópnum **Samskiptareglur framsendingar** velurðu valkostinn **Jafna beiðni**. 
1. Stilltu valkostinn **Umrita vefslóð** á **Óvirkt**.
1. Stilltu valkostinn **Biðminnisvistun** á **Óvirkt**.

Fylgdu þessum skrefum til að setja upp biðminnisreglu í Azure Front Door Service.

1. Bæta við biðminnisreglu.
1. Í reitinn **Heiti** skal færa inn **tölfræði**.
1. Í reitnum **Samþykkt samskiptaregla** velurðu **HTTP og HTTPS**.
1. Í reitnum **Framvinnsluhýslar** skaltu slá inn **dynamics-ecom-tenant-name.azurefd.net**.
1. Undir **Mynstur til að passa**, í efri reitnum, **/\_msdyn365/\_scnr/\***.
1. Undir **Upplýsingar um beini** stillirðu valkostinn **Gerð beinis** á **Áfram**.
1. Í reitnum **Bakvinnslusafn** velurðu **ecom-backend**.
1. Í reitahópnum **Samskiptareglur framsendingar** velurðu valkostinn **Jafna beiðni**.
1. Stilltu valkostinn **Umrita vefslóð** á **Óvirkt**.
1. Stilltu valkostinn **Biðminnisvistun** á **Óvirkt**.
1. Í reitnum **Skyndiminnishegðun fyrirspurnstrengja** velurðu **Vista hverja einstaka vefslóð í skyndiminni**.
1. Í reitahópnum **Breytileg þjöppun** velurðu valkostinn **Virkt**.

Eftirfarandi mynd sýnir valmyndina **Bæta við reglu** í Azure Front Door Service.

![Bættu við regluglugga](./media/CDN_CachingRule.png)

Eftir að þessari upphafsstillingu hefur verið komið á, verður þú að bæta sérsniðna léninu við stillingarnar fyrir Azure Front Door Service. Til að bæta við sérsniðna léninu (t.d. `www.fabrikam.com`), verður þú að stilla Canonical Name (CNAME) fyrir lénið.

Eftirfarandi mynd sýnir valmyndina **CNAME grunnstilling** í Azure Front Door Service.

![Valmyndin CNAME grunnstilling](./media/CNAME_Configuration.png)

> [!NOTE]
> Ef lénið sem þú munt nota er þegar virkt og lifandi, hafðu samband við stuðning til að virkja þetta lén með Azure Front Door Service til að setja upp próf.

Þú getur notað Azure Front Door Service til að stjórna skírteininu, eða þú getur notað þitt eigið skírteini fyrir sérsniðna lénið.

Eftirfarandi mynd sýnir valmyndina **Sérsniðin lén HTTPS** í Azure Front Door Service.

![Sérsniðin lén HTTPS valmynd](./media/Custom_Domain_HTTPS.png)

CDN ætti nú að vera rétt stillt þannig að það sé hægt að nota það með Commerce síðunni þinni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýju vefsvæði fyrir rafræn viðskipti](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Stjórna robots.txt-skrám](manage-robots-txt-files.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)

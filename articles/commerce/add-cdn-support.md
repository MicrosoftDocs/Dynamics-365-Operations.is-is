---
title: Bæta við stuðningi fyrir efnisbirtingarnet (CDN)
description: Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936831"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Bæta við stuðningi fyrir efnisbirtingarnet (CDN)

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.

Þegar búið er að setja upp rafrænt viðskiptaumhverfi í Dynamics 365 Commerce er hægt að skilgreina það til að vinna með CDN-þjónustunni. 

Hægt er að virkja sérsniðið lén meðan á úthlutunarferlinu stendur fyrir rafræna viðskiptaumhverfið. Einnig er hægt að nota þjónustubeiðni til að setja hana upp eftir að úthlutunarferlinu er lokið. Úthlutunarferlið fyrir rafræna viðskiptaumhverfið myndar hýsingarheiti sem er tengt við umhverfið. Þetta hýsilsheiti er með eftirfarandi sniði, þar sem \<*e-commerce-tenant-name*\> er heiti umhverfisins:

&lt;rafræn viðskipti-leigjanda-heiti&gt;.commerce.dynamics.com

Hýsingarheiti eða endastöð sem er mynduð í úthlutunarferlinu styður aðeins SSL-skírteini (Secure Sockets Layer) fyrir \*.commerce.dynamics.com. Það styður ekki SSL fyrir sérsniðin lén. Þess vegna verður þú að segja upp SSL fyrir sérsniðin lén í CDN og framsenda umferð frá CDN til hýsingarheitsins eða endapunktsins sem Commerce myndaði. 

Að auki er *tölfræðin* (JavaScript eða Cascading Style Sheets \[CSS\]-skrár) frá Commerce sýnd frá þeim endapunkti sem Commerce myndaði (\*.commerce.dynamics.com). Aðeins er hægt að afrita tölfræðina í skyndiminni ef hýsingarheiti eða endapunktur sem Commerce myndaði er sett á bak við CDN.

## <a name="set-up-ssl"></a>Setja upp SSL

Eftir að þú hefur úthlutað Commerce-umhverfi þínu á sérsniðna lénið sem er veitt, eða eftir að þú hefur gefið sérsniðna lénið fyrir umhverfi þitt með því að nota þjónustubeiðni, þarf að vinna með Commerce nýliðunarteyminu til að áætla DNS breytingarnar.

Eins og áður var getið styður myndað hýsingarheiti eða endapunktur aðeins SSL-skírteini fyrir \*.commerce.dynamics.com. Það styður ekki SSL fyrir sérsniðin lén.

## <a name="cdn-services"></a>CDN-þjónusta

Hægt er að nota hvaða CDN-þjónustu sem er með Commerce-umhverfi. Hér eru tvö dæmi:

- **Microsoft Azure Útidyraþjónusta** - Azure CDN-lausnin. Fyrir frekari upplýsingar um Azure útidyraþjónustu, sjá [Þjónustuskjöl Azure Front Service](/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** - Sjá frekari upplýsingar í [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>Uppsetning CDN

Uppsetningarferli CDN samanstendur af þessum almennu skrefum:

1. Bæta við framvinnsluhýsli.
1. Skilgreina bakvinnsluhóp.
1. Setja upp reglur fyrir leiðir.

### <a name="add-a-front-end-host"></a>Bæta við framvinnsluhýsli

Hægt er að nota hvaða CDN þjónustu sem er, en til dæmis í þessu efni er Azure Front Door Service notað. 

Upplýsingar um hvernig á að setja upp Azure Front Door Service, sjá [Stuttur leiðarvísir: Búðu til útidyr fyrir víðfáanlegt altækt vefforrit](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Skilgreina bakvinnsluhóp í Azure Front Door Service

Til að skilgreina bakvinnsluhóp í Azure Front Door Service skal fylgja þessum skrefum.

1. Bætið **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** við bakvinnsluhóp sem sérsniðinn hýsil sem er með bakvinnsluhaus sem er sá sami og **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.
1. Undir **Álagsjöfnun** skaltu skilja eftir sjálfgefin gildi.
1. Óvirkja ástandsskoðun fyrir bakvinnsluhóp.

Eftirfarandi mynd sýnir svargluggann **Bæta við bakvinnslu** í Azure Front Door Service með hýsilheiti bakvinnslu slegið inn.

![Bæta við valmynd bakvinnslusafns](./media/CDN_BackendPool.png)

Eftirfarandi mynd sýnir svargluggann **Bæta við bakvinnslu** í Azure Front Door Service með sjálfgefin gildi álagsjöfnunar.

![Svarglugginn „Bæta við bakvinnslu“ heldur áfram](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Gangið úr skugga um að **Heilbrigðiseftirlit** þegar eigin Azure Front Door Service er sett upp fyrir Commerce.


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


> [!WARNING]
> Ef lénið sem notað verður er þegar virkt og komið í notkun skal stofna þjónustubeiðni úr reitnum **Stuðningur** í [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) til að fá aðstoð vegna næstu skrefa. Frekari upplýsingar er að finna í [Fá stuðning fyrir Finance and Operations-forrit eða Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Ef lénið er nýtt og er ekki lén sem þegar er komið í virka notkun, er hægt að bæta sérsniðna léninu við skilgreininguna fyrir Azure Front Door Service. Þannig getur vefumferð beinst að vefsvæðinu í gegnum tilvik Azure Front Door. Til að bæta við sérsniðna léninu (t.d. `www.fabrikam.com`), verður þú að stilla Canonical Name (CNAME) fyrir lénið.

Eftirfarandi mynd sýnir valmyndina **CNAME grunnstilling** í Azure Front Door Service.

![Valmyndin CNAME grunnstilling](./media/CNAME_Configuration.png)

Þú getur notað Azure Front Door Service til að stjórna skírteininu, eða þú getur notað þitt eigið skírteini fyrir sérsniðna lénið.

Eftirfarandi mynd sýnir valmyndina **Sérsniðin lén HTTPS** í Azure Front Door Service.

![Sérsniðin lén HTTPS valmynd](./media/Custom_Domain_HTTPS.png)

Ítarlegar leiðbeiningar um hvernig skuli bæta sérsniðnu léni við Azure Front Door er að finna í [Bæta sérsniðnu léni við Front Door](/azure/frontdoor/front-door-custom-domain).

CDN ætti nú að vera rétt stillt þannig að það sé hægt að nota það með Commerce síðunni þinni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Valkostir innleiðingar á efnisbirtingarneti](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
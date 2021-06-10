---
title: Kökusamræmi
description: Þetta efnisatriði lýsir atriðum fyrir reglufylgni fyrir kökur og sjálfgefnum reglum sem teknar eru með í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/21/2021
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
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088388"
---
# <a name="cookie-compliance"></a>Reglufylgni köku

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir atriðum fyrir reglufylgni fyrir kökur og sjálfgefnum reglum sem teknar eru með í Microsoft Dynamics 365 Commerce.

Persónuvernd er mikilvægur þáttur þegar rekja á tækni sem hefur áhrif á viðskiptavini rafrænna viðskipta. Vegna staðla um samræmi við friðhelgi einkalífs, svo sem Almennu persónuverndarreglugerðina (GDPR) í Evrópusambandinu (ESB), verður að hafa í huga rafræn viðmiðunarreglur varðandi friðhelgi einkalífs fyrir alla vefi sem eru virkir í dag. Vegna þess að mörg svæði rafrænna viðskipta eru sjálfgefið aðgengileg á heimsvísu er mikilvægt að þú hafir farið yfir staðla viðmiðunar fyrir rafræn viðskipti.

Til að læra meira um grundvallarreglurnar sem Microsoft notar fyrir samræmi við vafrakökur skaltu fara á [Microsoft Trust Center](https://www.microsoft.com/trust-center). Á þeirri síðu geturðu einnig fengið frekari upplýsingar um svæði þar sem farið er eftir lögum og persónuvernd.

Eftirfarandi tafla sýnir núverandi tilvísunarlista yfir smákökur settur inn af Dynamics 365 Commerce vefsvæðum.

| Heiti köku                               | Notkun                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Geymið sannvottunarköku Microsoft Azure Active Directory (Azure AD) fyrir staka innskráningu (SSO). Geymir dulkóðaðar aðalupplýsingar notanda (nafn, eftirnafn, netfang). |
| &#95;msdyn365___cart&#95;                           | Geymið auðkenni körfu sem notað er til að sækja lista yfir vörur sem bætt er við körfutilvik. |
| &#95;msdyn365___ucc&#95;                            | Samþykktarrakning á reglufylgni köku.                          |
| ai_session                                  | Greinir hversu margar lotur notandavirkni hafa tekið með ákveðnar síður og eiginleika forritsins. |
| ai_user                                     | Greinir hversu margir notuðu forritið og eiginleika þess. Notendur eru taldir með nafnlausum auðkennum. |
| b2cru                                       | Geymir gagnvirkt framsenda vefslóð.                              |
| JSESSIONID                                  | Notað af greiðslutengli Adyen til að vista notandalotu.       |
| OpenIdConnect.nonce.&#42;                       | Sannvottun                                               |
| x-ms-cpim-cache:.&#42;                          | Notað til að viðhalda stöðu beiðninnar.                      |
| x-ms-cpim-csrf                              | Merki fyrirspurnafölsunar á milli svæða (CRSF) notað til að verjast CRSF.     |
| x-ms-cpim-dc                                | Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar. |
| x-ms-cpim-rc.&#42;                              | Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar. |
| x-ms-cpim-slice                             | Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Notað til að viðhalda SSO-lotunni.                        |
| x-ms-cpim-trans                             | Notað til að rekja færslur (fjöldi opinna flipa sem sannvottar vefsvæði viðskipta við neytanda (B2C)), þar með talið núverandi færslu. |
| \_msdyn365___muid_                            | Notað ef tilraun er virkjuð fyrir umhverfið; notað sem userId í tilraunaskyni. |
| \_msdyn365___exp_                             | Notað ef tilraun er virkjuð fyrir umhverfið; notað til að mæla álagsjöfnun afkasta.         |
| d365mkt                                       | Notað ef staðsetningarmiðuð greining til að fylgjast með IP-tölu notanda fyrir tillögur um staðsetningu verslunar er virkjuð í vefsmið Commerce á **Stillingar svæðis > Almennt > Virkja staðsetningarmiðaða greiningu á verslun**.      |

Ef notandi svæðis velur einhvern tengil á samfélagsmiðil innan svæðis munu kökurnar í eftirfarandi töflu einnig vera raktar í vafranum.


| Lén                      | Kaka               | lýsing                                                  | Uppruni                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Samstillir auðkenni LinkedIn auglýsinga                                      | LinkedIn-straumur og merki innsýnar                                |
| .linkedin.com               | li_sugr                  | Kennimerki vafra                                           | Merki LinkedIn-innsýnar ef IP-tala er ekki í uppgefnu landi |
| .linkedin.com               | BizographicsOptOut       | Ákvarðar stöðu afþökkunar fyrir rakningu þriðja aðila.              | Stýringar LinkedIn-gests og afþökkunarsíður atvinnugreinar           |
| .linkedin.com               | \_guid                    | Vafraauðkenni fyrir Google auglýsingar.                            | LinkedIn-straumur                                                |
| .linkedin.com               | li_oatml                 | Óbeint auðkenni meðlims fyrir breytingarakningu, ný markmið og greiningar. | Merki LinkedIn-auglýsinga og innsýnar                                |
| Ýmis lén fyrsta aðila | li_fat_id                | Óbeint auðkenni meðlims fyrir breytingarakningu, ný markmið og greiningar. | Merki LinkedIn-auglýsinga og innsýnar                                |
| .adsymptotic.com            | U                        | Kennimerki vafra                                           | Merki LinkedIn-innsýnar ef IP-tala er ekki í uppgefnu landi |
| .linkedin.com                | bcookie                  | Auðkenni vafraköku                                            | Beiðnir til LinkedIn                                         |
| .linkedin.com                | bscookie                 | Örugg vafraköka                                        | Beiðnir til LinkedIn                                         |
| .linkedin.com               | lang                     | Lotur sjálfgefinn landsstaðall og tungumál.                                 | Beiðnir til LinkedIn                                         |
| .linkedin.com                | lidc                     | Notað fyrir leiðir.                                             | Beiðnir til LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Kaka áhorfendastjórnanda Adobe                                                     | Stilla fyrir samstillingu auðkennis                                              |
| .linkedin.com               | \_ga                      | Google Analytics kaka                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analytics kaka                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analytics kaka                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Kaka inniheldur notandakenni þess sem er skráður inn.  |   Facebook                                                           |
| .facebook.com               | datr                     | Notað til að auðkenna vafrann sem er notaður til að tengjast við Facebook óháð því hver innskráður notandi er. | Facebook                                                             |
| .facebook.com               | wd                       | Geymir víddir vafraglugga og er notað af Facebook til að fínstilla birtingu síðunnar. | Facebook                                                             |
| .facebook.com               | xs                       | Tveggja stafa tala sem táknar lotunúmerið. Seinni hluti gildisins er leynilykill lotu. |  Facebook                                                            |
| .facebook.com               | fr                       | Inniheldur einkvæman vafra og notandakenni, notað fyrir markmiðaðar auglýsingar. |  Facebook                                                            |
| .facebook.com               | sb                       | Notað til að bæta Facebook vinatillögur.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Kaka inniheldur notandakenni þess sem er skráður inn.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Kaka inniheldur notandakenni þess sem er skráður inn.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Kaka inniheldur síður þegar notandi velur Pinterest-hnappinn.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Kaka inniheldur síður þegar notandi velur Pinterest-hnappinn.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Inniheldur notandakenni og tímastimpilinn þegar kakan var búin til. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Kaka inniheldur síður þegar notandi velur Pinterest-hnappinn.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Kaka inniheldur síður þegar notandi velur Pinterest-hnappinn.      | Pinterest                                                             |
| .pinterest.com              | Staðbundin geymsla            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Þjónustuaðilar          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Samþykki fyrir kökur á svæði notanda á vefsvæði e-Commerce 

Ef eiginleiki einingu rafrænna viðskipta notar köku sem ekki er nauðsynleg þarf að sækja samþykki notanda áður en kakan er rakin. Til að leyfa notendum vefsvæðis að veita samþykki fyrir kökur á svæði rafrænna viðskipta verður höfundur síðu að bæta við og grunnstilla samþykkiseining köku í hauseiningu síðu til að tryggja að beðið sé um samþykki og það móttekið. Gefa þarf notendasamþykki vefsvæðis áður en hægt er að nota eiginleika eða einingu án nauðsynlegrar köku á síðu svæðis.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgengiseiginleikar og -geta](accessibility.md)

[Yfirlit yfir reglufylgni](compliance-overview.md)

[Bæta við persónuverndarstefnusíðu](add-privacy-page.md)

[Skipta um notandakenni sem tengjast röktum efnisbreytingum](replace-IDs-tracked-changes.md)

[Eining kökusamþykkis](cookie-consent-module.md) 
 
[Eining síðuhauss](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

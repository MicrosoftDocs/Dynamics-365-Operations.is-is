---
title: Reglufylgni köku
description: Þessi grein lýsir sjónarmiðum um samræmi við vafrakökur og sjálfgefna reglur sem eru innifalin í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 20bdc6466c5d89709f8ba790eb567bd7d8bbb15c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273613"
---
# <a name="cookie-compliance"></a>Reglufylgni köku

[!include [banner](includes/banner.md)]

Þessi grein lýsir sjónarmiðum um samræmi við vafrakökur og sjálfgefna reglur sem eru innifalin í Microsoft Dynamics 365 Commerce.

Persónuvernd er mikilvægur þáttur þegar rekja á tækni sem hefur áhrif á viðskiptavini rafrænna viðskipta. Vegna staðla um samræmi við friðhelgi einkalífs, svo sem Almennu persónuverndarreglugerðina (GDPR) í Evrópusambandinu (ESB), verður að hafa í huga rafræn viðmiðunarreglur varðandi friðhelgi einkalífs fyrir alla vefi sem eru virkir í dag. Vegna þess að mörg svæði rafrænna viðskipta eru sjálfgefið aðgengileg á heimsvísu er mikilvægt að þú hafir farið yfir staðla viðmiðunar fyrir rafræn viðskipti.

Til að læra meira um grundvallarreglurnar sem Microsoft notar fyrir samræmi við vafrakökur skaltu fara á [Microsoft Trust Center](https://www.microsoft.com/trust-center). Á þeirri síðu geturðu einnig fengið frekari upplýsingar um svæði þar sem farið er eftir lögum og persónuvernd.

Eftirfarandi tafla sýnir núverandi tilvísunarlista yfir smákökur settur inn af Dynamics 365 Commerce vefsvæðum.

| Heiti köku                               | Notkun                                                        | Líftími |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Cookies                             | Geymið sannvottunarköku Microsoft Azure Active Directory (Azure AD) fyrir staka innskráningu (SSO). Geymir dulkóðaðar aðalupplýsingar notanda (nafn, eftirnafn, netfang). | Seta |
| \_msdyn365___karfa_                           | Geymið auðkenni körfu sem notað er til að sækja lista yfir vörur sem bætt er við körfutilvik. | Seta |
| \_msdyn365___Greiðsluferli_karfa_                           | Geymið auðkenni körfu í greiðsluferli sem notað er til að sækja lista yfir vörur sem bætt er við körfutilvik greiðsluferlis. | Seta |
| \_msdyn365___ucc_                            | Samþykktarrakning á reglufylgni köku.                          | 1 ár |
| ai_session                                  | Greinir hversu margar lotur notandavirkni hafa tekið með ákveðnar síður og eiginleika forritsins. | 30 mínútur |
| ai_user                                     | Greinir hversu margir notuðu forritið og eiginleika þess. Notendur eru taldir með nafnlausum auðkennum. | 1 ár |
| b2cru                                       | Geymir gagnvirkt framsenda vefslóð.                              | Seta |
| JSESSIONID                                  | Notað af greiðslutengli Adyen til að vista notandalotu.       | Seta |
| OpenIdConnect.nonce.&#42;                       | Sannvottun                                               | 11 mínútur |
| x-ms-cpim-cache:.&#42;                          | Notað til að viðhalda stöðu beiðninnar.                      | Seta |
| x-ms-cpim-csrf                              | Merki fyrirspurnafölsunar á milli svæða (CRSF) notað til að verjast CRSF.     | Seta |
| x-ms-cpim-dc                                | Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar. | Seta |
| x-ms-cpim-rc.&#42;                              | Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar. | Seta |
| x-ms-cpim-slice                             | Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar. | Seta |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Notað til að viðhalda SSO-lotunni.                        | Seta |
| x-ms-cpim-trans                             | Notað til að rekja færslur (fjöldi opinna flipa sem sannvottar vefsvæði viðskipta við neytanda (B2C)), þar með talið núverandi færslu. | Seta |
| \_msdyn365___muid_                            | Notað ef tilraun er virkjuð fyrir umhverfið; notað sem notandakenni í tilraunaskyni. | 1 ár |
| \_msdyn365___exp_                             | Notað ef tilraun er virkjuð fyrir umhverfið; notað til að mæla álagsjöfnun afkasta.         | 1 klukkustund |
| d365mkt                                       | Notað ef staðsetningarmiðuð greining til að fylgjast með IP-tölu notanda fyrir tillögur um staðsetningu verslunar er virkjuð í vefsmið Commerce á **Stillingar svæðis \> Almennt \> Virkja staðsetningarmiðaða greiningu á verslun**.      | 1 klukkustund |
| \_msdyn365___tuid_                           | Notað aðeins ef tilraunir eru virkjaðar fyrir umhverfi; býr til GUID til að nota sem notandaauðkenni. Gildi breytist ef innskráningarstaða breytist.      | 1 ár |
| \_msdyn365___aud_0                          | Vistar hlutagildi sem markmið notar og er aðeins notað ef markmið er stillt á síðu eða brot sem notandi vefsvæðis óskar eftir. Köku er aðeins komið fyrir þegar hlutagildi koma frá þriðja aðila.      | 7 dagar |
| \_msdyn365___aud_1                           | Vistar hlutagildi sem markmið notar og er aðeins notað ef markmið er stillt á síðu eða brot sem notandi vefsvæðis óskar eftir. Köku er aðeins komið fyrir þegar hlutagildi koma frá þriðja aðila.      | 7 dagar |
| \_msdyn365___aud_2                           | Vistar hlutagildi sem markmið notar og er aðeins notað ef markmið er stillt á síðu eða brot sem notandi vefsvæðis óskar eftir. Köku er aðeins komið fyrir þegar hlutagildi koma frá þriðja aðila.      | 7 dagar |
| d365gi                                       | Þessi vafrakaka geymir landfræðileg staðsetningargögn þegar landfræðileg staðsetningarþjónusta þriðja aðila er notuð.      | 1 dagur |

Ef notandi svæðis velur einhvern tengil á samfélagsmiðil innan svæðis munu kökurnar í eftirfarandi töflu einnig vera raktar í vafranum.


| Lén                      | Kaka               | lýsing                                                  | Uppruni                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Samstillir auðkenni LinkedIn auglýsinga                                      | LinkedIn-straumur og merki innsýnar                                |
| .linkedin.com               | li_sugr                  | Kennimerki vafra                                           | LinkedIn Insight merki ef IP-tala er ekki í tilteknu landi |
| .linkedin.com               | BizographicsOptOut       | Ákvarðar stöðu afþökkunar fyrir rakningu þriðja aðila.              | Stýringar LinkedIn-gests og afþökkunarsíður atvinnugreinar           |
| .linkedin.com               | \_guid                    | Vafraauðkenni fyrir Google auglýsingar.                            | LinkedIn-straumur                                                |
| .linkedin.com               | li_oatml                 | Óbeint auðkenni meðlims fyrir breytingarakningu, ný markmið og greiningar. | Merki LinkedIn-auglýsinga og innsýnar                                |
| Ýmis lén fyrsta aðila | li_fat_id                | Óbeint auðkenni meðlims fyrir breytingarakningu, ný markmið og greiningar. | Merki LinkedIn-auglýsinga og innsýnar                                |
| .adsymptotic.com            | U                        | Kennimerki vafra                                           | LinkedIn Insight merki ef IP-tala er ekki í tilgreindu landi |
| .linkedin.com                | bcookie                  | Auðkenni vafraköku                                            | Beiðnir til LinkedIn                                         |
| .linkedin.com                | bscookie                 | Örugg vafraköka                                        | Beiðnir til LinkedIn                                         |
| .linkedin.com               | lang                     | Lotur sjálfgefinn landsstaðall og tungumál.                                 | Beiðnir til LinkedIn                                         |
| .linkedin.com                | lidc                     | Notað fyrir leiðir.                                             | Beiðnir til LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Adobe kex áhorfendastjóra                                                     | Stilla fyrir samstillingu auðkennis                                              |
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


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Samþykki vefköku notenda á netverslunarsíðu 

Ef eiginleiki eða eining á netviðskiptasíðu notar ónauðsynleg vafraköku, verður að fá samþykki síðunotanda áður en kexið er rakið. Til að leyfa notendum vefsins að veita samþykki fyrir fótspor á netverslunarsíðunni verður höfundur vefsvæðis að bæta við og stilla samþykkiseiningu fyrir vafrakökur í hausseiningu síðunnar til að tryggja að beðið sé um samþykki og móttekið. Gefa þarf notendasamþykki vefsvæðis áður en hægt er að nota eiginleika eða einingu án nauðsynlegrar köku á síðu svæðis.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgengiseiginleikar og -geta](accessibility.md)

[Yfirlit yfir reglufylgni](compliance-overview.md)

[Bæta við persónuverndarstefnusíðu](add-privacy-page.md)

[Skipta um notandakenni sem tengjast röktum efnisbreytingum](replace-IDs-tracked-changes.md)

[Eining kökusamþykkis](cookie-consent-module.md) 
 
[Eining síðuhauss](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

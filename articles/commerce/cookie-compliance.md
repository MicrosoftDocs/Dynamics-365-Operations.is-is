---
title: Kökusamræmi
description: Þetta efni lýsir forsendum varðandi samræmi við vafrakökur og sjálfgefnar reglur sem fylgja Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446914"
---
# <a name="cookie-compliance"></a>Kökusamræmi

[!include [banner](includes/banner.md)]

Þetta efni lýsir forsendum varðandi samræmi við vafrakökur og sjálfgefnar reglur sem fylgja Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

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

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgengiseiginleikar og -geta](accessibility.md)

[Yfirlit yfir reglufylgni](compliance-overview.md)

[Bæta við persónuverndarstefnusíðu](add-privacy-page.md)

[Skipta um notandakenni sem tengjast röktum efnisbreytingum](replace-IDs-tracked-changes.md)

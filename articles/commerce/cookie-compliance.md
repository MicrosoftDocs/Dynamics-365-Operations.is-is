---
title: Kökusamræmi
description: Þetta efnisatriði lýsir atriðum fyrir reglufylgni fyrir kökur og sjálfgefnum reglum sem teknar eru með í Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10a58cf7197d2a8596107a42174b35350e72ae11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215698"
---
# <a name="cookie-compliance"></a>Reglufylgni köku

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir atriðum fyrir reglufylgni fyrir kökur og sjálfgefnum reglum sem teknar eru með í Microsoft Dynamics 365 Commerce.

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
---
title: Búðu til B2C forrit
description: Þessi grein lýsir því hvernig á að búa til viðskipta-til-neytenda (B2C) forrit í Microsoft Azure gátt.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785814"
---
# <a name="create-a-b2c-application"></a>Búðu til B2C forrit

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til viðskipta-til-neytenda (B2C) forrit í Microsoft Azure gátt.

Þegar B2C leigjandinn þinn hefur verið búinn til, býrðu til B2C forrit innan nýja Azure Active Directory (Azure AD) leigjanda til að hafa samskipti við Commerce.

Til að stofna B2C forrit skal fylgja þessum skrefum.

1. Í Azure-gáttinni skal velja **Skráning forrita** og því næst velja **Ný skráning**.
1. Undir **Heiti** skal slá inn heiti sem gefa á þessu Azure AD B2C forriti.
1. Undir **Studdar reikningsgerðir** skal velja **Reikningar í einhverjum kenniveitanda eða fyrirtækjaskrá (til að auðkenna notendur með notandaflæðum)**.
1. Fyrir **Framsenda URI** skal færa inn sérstakar svarslóðir af gerðinni **Vefur**. Sjáðu [Svarslóðir](#reply-urls) hér að neðan til að fá upplýsingar um svarslóðir og hvernig eigi að forsníða þær. Sláðu inn tilvísunarvefslóð/svarslóð til að virkja áframsendingar frá Azure AD B2C aftur á síðuna þína þegar notandi staðfestir. Hægt er að bæta við svarslóðinni meðan á skráningarferlinu stendur eða hægt er að bæta við síðar með því að velja **Bættu við tilvísunarvefslóð** hlekkur frá **Yfirlit** valmynd í B2C forritinu **Yfirlit** kafla.
1. Fyrir **Heimildir** skal velja **Veita kerfisstjóra samþykki að heimildum openid og offline_access**.
1. Veldu **Skrá**.
1. Veldu nýstofnaða forritið og farðu að **Auðkenning** matseðill. 
1. Ef svarslóð er slegin inn, undir **Óbeint styrki og blendingsflæði** veldu bæði **Aðgangstákn** og **Auðkennismerki** valkosti til að virkja þá fyrir forritið og veldu síðan **Vista**. Ef svarslóð var ekki slegin inn við skráningu er einnig hægt að bæta henni við á þessari síðu með því að velja **Bættu við vettvangi**, að velja **vefur**, og sláðu síðan inn tilvísunar-URI forritsins. The **Óbeint styrki og blendingsflæði** kafla verður þá tiltækt til að velja bæði **Aðgangstákn** og **Auðkennismerki** valkosti.
1. Farið í valmyndina **Yfirlit** í Azure-gáttinni og afritið **Forritskennið (biðlarakennið)**. Skrifið hjá ykkur þetta auðkenni fyrir síðari uppsetningarskref (vísað í það síðar sem **GUID biðlara**).

Fyrir frekari tilvísun í forritsskráningu í Azure AD B2C skal skoða [Ný upplifun forritsskráninga fyrir Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Svarslóðir

Svarvefslóðir eru mikilvægar þar sem þær gefa upp heimildarlista skilalén þegar vefsvæðið kallar á Azure AD B2C til að sannvotta notanda. Þetta heimilar endursendingu staðfests notanda til baka á lén sem hann er að skrá sig inn á (vefsvæðið þitt). 

Í reitnum **Svarslóð** á skjánum **Azure AD B2c - Forrit \> Nýtt forrit** þarftu að bæta við aðskildum línum fyrir bæði lén vefsvæðisins og (þegar umhverfi þitt er útvegað) Commerce-myndaðri vefslóðinni. Þessar vefslóðir verða alltaf að nota gilt slóðarsnið og verða að vera eingöngu grunnslóðir (engin skástrik eða slóðir fyrir aftan). Strengurinn ``/_msdyn365/authresp`` þarf síðan að vera bætt aftan við grunnslóðina, eins og í eftirfarandi dæmum.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Lénið ætti að passa fullkomlega við lén rafrænna viðskipta. Ef um er að ræða mörg lén þarf að bæta við þessari vefslóð fyrir hvert lén.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að setja upp B2C leigjanda í Commerce skaltu halda áfram að [Búðu til stefnu um notendaflæði](create-user-flow-policies.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md)

[Stofna notandaflæðisstefnu](create-user-flow-policies.md)

[Bæta við kennitöluveitendum (valfrjálst)](add-social-identity-providers.md)

[Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md)

[Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði](config-b2c-tenant-site-builder.md)

[Frekari B2C upplýsingar](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

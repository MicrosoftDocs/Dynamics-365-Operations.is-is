---
title: Viðskiptaspjall við Power Virtual Agents mát
description: Þessi grein lýsir viðskiptaspjallinu við Power Virtual Agents eining sem samþættir Microsoft Power Virtual Agents með Dynamics 365 Commerce vefsíður.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690953"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Viðskiptaspjall við Power Virtual Agents mát

[!include [banner](includes/banner.md)]

Þessi grein lýsir viðskiptaspjallinu við Power Virtual Agents eining sem samþættir Microsoft Power Virtual Agents með Dynamics 365 Commerce vefsíður.

Viðskiptaspjallið við Power Virtual Agents eiginleiki gerir viðskiptavinum Dynamics 365 rafræn viðskipti kleift að nota Power Virtual Agents chatbot getu til að takast á við fyrirspurnir sínar. Frá og með Dynamics 365 Commerce 10.0.30 útgáfu, er hægt að fella þennan eiginleika inn á vefsvæði rafrænna viðskipta með því að nota viðskiptaspjallið með Power Virtual Agents eining sem er hluti af Commerce einingasafninu.

Viðskiptaspjallið við Power Virtual Agents eiginleiki hjálpar fyrirtækjum að ná eftirfarandi markmiðum:

- Auka persónulega þátttöku við neytendur sína og bæta varðveislu.
- Auka þjónustu við viðskiptavini með samþættingu sjálfsafgreiðsluspjallbotna.
- Auka heildaránægju viðskiptavina og auka því sölu.

> [!NOTE]
> Til að fræðast um muninn á Dynamics 365 alhliða þjónustu við viðskiptavini og Power Virtual Agents umsóknir, sjá [Yfirlit yfir viðskiptaspjalleiningar](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a> Forsendur fyrir notkun Power Virtual Agents

Til að nota viðskiptaspjallið með Power Virtual Agents eiginleika, þú verður fyrst að búa til a Power Virtual Agents chatbot fyrir netverslunarvefsíðuna þína. Fyrir leiðbeiningar, sjá [Búðu til kraftmikinn sýndarumboðsmann](/power-virtual-agents/authoring-first-bot).

Eftir að þú stillir spjallbotninn verður þú að afrita gildin fyrir **Bota auðkenni** og **Auðkenni leigjanda** færibreytur chatbot til að stilla upplifun Commerce spjallsins. Fyrir upplýsingar um hvernig á að afrita þessi gildi, sjá [Sæktu þína Power Virtual Agents bot breytur](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Stilltu netverslunarsíðuna þína 

Ein leið sem mælt er með til að innleiða spjallupplifunina fyrir netverslunarsíðuna þína er að bæta viðskiptaspjallinu við Power Virtual Agents mát í samnýtta hausbrotið sem er notað á síðunum þínum.

Fylgdu þessum skrefum til að bæta spjalleiningunni við haus síðunnar þinnar í Commerce site builder.

1. Í Commerce site builder fyrir síðuna þína, farðu á **Brot**.
1. Veljið **Nýtt**.
1. Í **Veldu brot** valmynd, veldu **Viðskiptaspjall við Power Virtual Agents** mát, sláðu inn heiti fyrir brotið og veldu síðan **Allt í lagi**.
1. Í yfirlitsskjánum skaltu velja **Msdyn365 pva spjalltengi** rifa.
1. Fylgdu þessum skrefum í eiginleikarúðunni til hægri:

    1. Undir **Bot færibreytur**, í **Bot Framework Webchat Chat CDN URL** reit, skildu eftir sjálfgefið gildi (td`https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. Í **Bot Framework Direct Line Auðkenningarslóð** reit, skildu eftir sjálfgefið gildi (td`https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. Í **Bota auðkenni** reit, sláðu inn Power Virtual Agents **Bota auðkenni** gildi sem þú afritaðir í [Forsendur fyrir notkun Power Virtual Agents](#prereq) kafla.
    1. Í **Auðkenni leigjanda** reit, sláðu inn **Auðkenni leigjanda** gildi sem þú afritaðir.

1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.
1. Fara til **Brot**, og opnaðu hausbrotið fyrir síðuna þína.
1. Í **Sjálfgefinn gámur** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við broti**.
1. Í **Veldu einingar** valmynd, veldu spjallbrotið sem þú bjóst til áðan og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.

## <a name="proactive-chat-parameters"></a>Fyrirbyggjandi spjallfæribreytur

Fyrir heildarlista yfir fyrirbyggjandi spjallstillingarfæribreytur, sjá [Viðskiptaspjallseining fyrirbyggjandi spjallfæribreytur](chat-proactive-chat-parameters.md).

> [!NOTE]
> Eins og er,Power Virtual Agents styður ekki Azure Active Directory B2C (Azure AD B2C) auðkenning. Það styður aðeins nafnlaus Retail Cloud Scale Unit (RCSU) símtöl til að fá vöruframboð eða hafa samskipti við önnur nafnlaus API. Símtöl í staðfest API í gegnum Power Virtual Agents spjallbotar krefjast skýrrar innskráningar viðskiptavina.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir eiginleika viðskiptaspjalls](commerce-chat-overview.md)

[Viðskiptaspjall með alhliða rás fyrir þjónustudeild](commerce-chat-module.md)

[Viðskiptaspjallseining fyrirbyggjandi spjallfæribreytur](chat-proactive-chat-parameters.md)

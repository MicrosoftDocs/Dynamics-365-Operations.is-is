---
title: Viðskiptaspjall með alhliða rás fyrir þjónustudeild
description: Þessi grein lýsir verslunarspjalli með fjölrás fyrir þjónustu við viðskiptavini í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: e4a004b929138f0a04c19d6a94278cfad6e83303
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346096"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Viðskiptaspjall með alhliða rás fyrir þjónustudeild

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir *Viðskiptaspjall við alhliða rás fyrir þjónustu við viðskiptavini* mát í Microsoft Dynamics 365 Commerce.

Í útgáfu Commerce útgáfu 10.0.29 hefur nýrri Commerce Chat with Omnichannel for Customer Service einingu verið bætt við Commerce einingasafnið. Viðskiptaspjalleiginleikinn veitir viðskiptavinum rafrænna viðskipta spjallmöguleika Dynamics 365 Omnichannel for Customer Service, sem felur í sér stuðning umboðsmanna í beinni til að aðstoða við að svara fyrirspurnum viðskiptavina, veita þjónustu við viðskiptavini og auðvelda sölu fyrir viðskiptavini.

Viðskiptaspjallaðgerðin gerir smásöluaðilum kleift að ná þessum markmiðum:

- Auka persónulega samskipti við viðskiptavini til að hjálpa til við að bæta viðskiptavinahald.
- Bættu þjónustu við viðskiptavini með samþættingu mannlegra umboðsmanna og sjálfsafgreiðsluspjallbotna.
- Hjálpaðu umboðsmönnum að öðlast reynslu með rauntíma viðskiptavinaprófíl, pöntun og innkaupagögnum sem knýja áfram rekstrarumbætur og þátttöku.
- Bættu heildaránægju viðskiptavina til að auka sölu.

Eftirfarandi möguleikar eru fáanlegir sem hluti af viðskiptaspjalleiginleikanum:

- Viðskiptaspjall við alhliða rás fyrir þjónustu við viðskiptavini
- Viðbót á **Símamiðstöð viðskipta** sem forritaflipi í umboðsupplifuninni í Dynamics 365 Omnichannel for Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Forsendur fyrir alhliða þjónustu fyrir þjónustu við viðskiptavini

Sem forsenda verður þú að stilla spjallið í græjunni fyrir umsjón með þjónustu við viðskiptavini og fá nokkrar færibreytur til að stilla upplifun viðskiptaspjallsins. Fyrir leiðbeiningar, sjá [Stilltu spjallrás](/dynamics365/customer-service/set-up-chat-widget).

Eftir að þú stillir spjallið í Omnichannel for Customer Service Administration græjunni færðu skriftu sem líkist eftirfarandi dæmi.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Afritaðu þetta handrit, því þú þarft gildin í því til að stilla spjalleininguna.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Viðskiptaspjall við alhliða rás fyrir þjónustu við viðskiptavini skyldureitir

Eftirfarandi tafla sýnir skriftugildin úr græjunni Umnichannel for Customer Service Administration sem þarf til að stilla Commerce Chat with alchannel for Customer Service eininguna.

| Búnaður eign | Lýsing |
| ------------- |--------------|
| Uppruni skriftu | Verðmæti **src** í forskrift spjallgræjunnar. |
| Auðkenni gagnaforrits | Verðmæti **gagna-app-auðkenni** í forskrift spjallgræjunnar. |
| Auðkenni gagnastofnunar | Verðmæti **data-org-id** í forskrift spjallgræjunnar. |
| Slóð gagnastofnunar | Verðmæti **data-org-url** í forskrift spjallgræjunnar. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Stilltu upplifun Commerce spjallsins fyrir netverslunarsíðuna þína

Ein leið sem mælt er með til að innleiða spjallupplifunina fyrir netverslunarsíðuna þína er að bæta viðskiptaspjallinu með alhliða þjónustueiningunni við samnýtt hausbrot sem er notað á síðum rafrænna viðskiptasíðunnar þinna.

Fylgdu þessum skrefum til að bæta spjalleiningunni við haushluta síðunnar þinnar í Commerce site builder.

1. Farðu í Site builder fyrir síðuna þína **Brot**.
1. Veljið **Nýtt**.
1. Í **Veldu brot** valmynd, veldu **Viðskiptaspjall við alhliða rás fyrir þjónustu við viðskiptavini** mát, sláðu inn heiti fyrir brotið og veldu síðan **Allt í lagi**.
1. Í yfirlitsskjánum skaltu velja **Msdyn365 cs spjalltengi** rifa.
1. Í **Spjall eiginleikar** rúðu til hægri, fylgdu þessum skrefum:

    1. Í **Handritsheimild** reit, sláðu inn **src** gildi sem þú fékkst úr handritinu Omnichannel for Customer Service.
    1. Í **Auðkenni gagnaforrits** reit, sláðu inn **gagna-app-auðkenni** gildi sem þú fékkst úr handritinu Omnichannel for Customer Service.
    1. Í **Auðkenni gagnastofnunar** sviði, the **data-org-id** gildi sem þú fékkst úr handritinu Omnichannel for Customer Service.
    1. Í **Slóð gagnastofnunar** reit, sláðu inn **data-org-url** gildi sem þú fékkst úr handritinu Omnichannel for Customer Service.

    ![Að búa til brot á viðskiptaspjalleiningunni í Commerce site builder.](media/Commerce-chat-creating-new-fragment.png)

1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.
1. Fara til **Brot**, og opnaðu hausbrotið fyrir síðuna þína.
1. Í **Sjálfgefinn gámur** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við broti**.
1. Í **Veldu einingar** valmynd, veldu spjallbrotið sem þú bjóst til áðan og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Bættu við höfuðstöðvum viðskipta sem umsóknarflipa fyrir alhliða þjónustu við viðskiptavini

Þú getur bætt við umsóknarflipa fyrir höfuðstöðvar viðskipta í Omnichannel fyrir þjónustu við viðskiptavini. Umboðsmenn í beinni geta síðan notað notendaviðmótið fyrir upplifun umnichannels fyrir þjónustufulltrúa til að fá auðveldlega aðgang að Dynamics 365 Commerce Þjónustueining sem inniheldur samhengisupplýsingar fyrir viðskiptavininn ásamt upplýsingum um sölupantanir hans. Að auki geta þjónustufulltrúar lagt inn nýjar pantanir, hafið skil og staðfest upplýsingar um pöntunarstöðu.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Búðu til nýjan forritaflipa sem hleður höfuðstöðvum Commerce í iFrame mát 

Til að búa til nýjan forritaflipa sem hleður höfuðstöðvum Commerce í iFrame mát, fylgdu þessum skrefum.

1. Opnaðu [Power Apps Framleiðandi gátt](https://make.powerapps.com).
1. Í yfirlitsrúðunni til vinstri velurðu **Forrit**.
1. Veldu **Stjórnendamiðstöð þjónustuvers**.
1. Fara til **Reynsla umboðsmanns**.
1. Fyrir **Sniðmát fyrir forritsflipa**, veldu **Stjórna**.
1. Búðu til nýjan umsóknarflipa í **Vefsíða þriðja aðila** tegund. Fyrir leiðbeiningar, sjá [Hafa umsjón með sniðmátum fyrir forritsflipa](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. Undir **Færibreytur**, í **Gildi** sviði á **slóð** færibreytu, sláðu inn eftirfarandi vefslóð, þar sem`<YourOrganizationHeadquartersURL>` og`<LegalEntityname>` er skipt út fyrir viðeigandi gildi. Umnichannel þjónustuver les **{AccountNumber}** úr spjallsamhenginu. Því farðu **{AccountNumber}** eins og er.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Skildu eftir **Gildi** sviði á **gögn** færibreyta auð.

![Að búa til forritsflipa í Dynamics 365 Omnichannel Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Virkja nýjan umsóknarflipa fyrir umboðsmenn viðskiptavina í Dynamics 365 Omnichannel for Customer Service

Til að virkja nýjan forritaflipa fyrir umboðsmenn viðskiptavina í Dynamics 365 Omnichannel for Customer Service, fylgdu þessum skrefum.
    
1. Opnaðu [Power Apps Framleiðandi gátt](https://make.powerapps.com).
1. Í yfirlitsrúðunni til vinstri velurðu **Forrit**.
1. Veldu **Stjórnendamiðstöð þjónustuvers**.
1. Fara til **Þjónustudeild \> Vinnustraumar**.
1. Opnaðu vinnustrauminn sem þú hefur búið til fyrir umboðsmenn þína og síðan undir **Ítarlegar stillingar**, veldu **Sessions sjálfgefið**.
1. Undir **Forritsflipar**, veldu **Bæta við núverandi forritaflipa**, og bættu síðan við nýja forritaflipanum sem þú bjóst til áðan. Þetta skref tryggir að forritsflipi sem hleður höfuðstöðvum Commerce í iFrame eining mun birtast þegar umboðsmaður fær spjallsímtal frá e-verslunarvefsíðunni þinni.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Bættu við samhengisbreytum í Dynamics 365 Omnichannel for Customer Service

Til að bæta við samhengisbreytum í Dynamics 365 Omnichannel for Customer Service skaltu fylgja þessum skrefum.

1. Opnaðu [Power Apps Framleiðandi gátt](https://make.powerapps.com).
1. Í yfirlitsrúðunni til vinstri velurðu **Forrit**.
1. Veldu **Stjórnendamiðstöð þjónustuvers**.
1. Fara til **Þjónustudeild \> Vinnustraumar**.
1. Opnaðu vinnustrauminn sem þú hefur búið til fyrir umboðsmenn þína og síðan undir **Ítarlegar stillingar**, farðu í **Samhengisbreyta** kafla.
1. Veldu **Breyta**, og bæta svo við **Reikningsnúmer** sem samhengisbreytu af **texti** tegund. Þessi breyta mun hjálpa höfuðstöðvum Commerce að hlaða upplýsingar viðskiptavina með samsvarandi reikningsnúmerum.

> [!NOTE]
> Ef þú vilt lesa netföng og nöfn innskráðra notenda frá rafrænni viðskiptarás geturðu bætt við **Tölvupóstur** og **Nafn** sem samhengisbreytur á **texti** gerð, til viðbótar við **Reikningsnúmer** samhengisbreytu.

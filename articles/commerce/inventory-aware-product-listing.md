---
title: Birgðameðvituð vöruskráning
description: Þessi grein lýsir því hvernig fyrirtæki geta stillt vöruskráningarsíður á sínum Microsoft Dynamics 365 Commerce e-verslun vefsíða þannig að þeir séu meðvitaðir um birgðahald.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: e33a4dd8650ee2e371c51c5a19e955f2d2bdade2
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405518"
---
# <a name="inventory-aware-product-listing"></a>Birgðameðvituð vöruskráning

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein lýsir því hvernig fyrirtæki geta stillt vöruskráningarsíður á sínum Microsoft Dynamics 365 Commerce e-verslun vefsíða þannig að þeir séu meðvitaðir um birgðahald. Vöruskráningarsíður innihalda áfangasíður fyrir flokka og leitarniðurstöðusíður.

Kaupendur búast almennt við að vöruuppgötvun á netverslunarvefsíðu sé meðvituð um birgðahald, svo að þeir geti ákveðið hvað þeir eigi að gera ef vara er ekki til á lager. The [Bókasafn viðskiptaeininga](starter-kit-overview.md) flokka- og leitarniðurstöðueiningar er hægt að stilla til að fella inn birgðagögn. Á þennan hátt geta þeir veitt eftirfarandi reynslu:

- Sýndu merkimiða á birgðastigi við hlið afurða.
- Fela vörur sem eru ekki á lager af vörulistanum.
- Færðu vörur sem eru ekki á lager neðst á vörulistasíðum.
- Styðja vörusíun sem byggir á birgðum.

Til að virkja þessa upplifun verður þú fyrst að virkja **Aukin vöruuppgötvun rafræn viðskipti til að vera meðvituð um birgðahald** þáttur í höfuðstöðvum Commerce.

> [!NOTE]
> Í Commerce útgáfu 10.0.29 og síðar er **Aukin vöruuppgötvun rafræn viðskipti til að vera meðvituð um birgðahald** eiginleiki er sjálfgefið virkur.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Settu upp vörueiginleika fyrir framboð á birgðum

Birgðameðvituð vöruskráning notar ramma vörueiginleika. Sem forsenda verður að búa til sérstaka vörueigind til að fanga birgðatilboðsgögn.

Til að setja upp vörueiginleika fyrir birgðatilboð í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Fara til **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Vörur og lager \> Fylltu vörueiginleika með birgðastigi**.
1. Í **Fylltu vörueiginleika með birgðastigi** valmynd, í **Vörueiginleiki og tegundarheiti** reit, sláðu inn sérsniðið heiti fyrir sérstaka vörueigind sem verður búin til til að fanga birgðagögn.
1. Í **Birgðaframboð byggt á** reit, veldu þá magntegund sem útreikningur birgðastigs ætti að byggja á: **Í boði líkamlegt** eða **Samtals í boði**.
1. Stilltu **Lotuvinnsla** valmöguleika til **Já**.
1. Veldu **Í lagi**.

> [!NOTE]
> Til að fá samræmdan útreikning á birgðastigi á síðum rafrænnar viðskiptavefsíðu þinnar skaltu ganga úr skugga um að þú veljir sömu magntegund í báðum **Birgðaframboð byggt á** sviði fyrir **Fylltu vörueiginleika með birgðastigi** starfið og **Birgðastig miðað við** stilling í Commerce site builder.

Eftir að sérstök vörueigin er búin til er næsta skref að stilla eigindina fyrir netrásina.

Til að stilla eigindina fyrir netrásina í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.
1. Veldu netrásina til að virkja birgðaupplifun vöruskráningar fyrir.
1. Veldu og opnaðu tengdan eigindahóp og bættu síðan nýju vörueigindinni við hann.
1. Fara til **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**, og keyra **1150** (**Vörulisti**) starf. Við mælum með að þú tímasetur þetta verk sem runuferli sem keyrir á sömu tíðni og **Fylltu vörueiginleika með birgðastigi** starf.

> [!NOTE]
> Í Commerce útgáfu 10.0.26 og eldri, eftir að þú hefur bætt vörueigindinni til framboðs birgða við eigindahóp, verður þú einnig að velja **Stilltu lýsigögn eiginda**, og kveiktu síðan á **Sýna eigind á rás**, **að sækja**, **að betrumbæta**, og **Hægt að spyrjast fyrir** valkosti fyrir nýja vörueiginleikann.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Stilltu birtingarhegðun fyrir vörur sem eru ekki á lager á vöruskráningarsíðum

Eftir að öllum fyrri stillingarskrefum er lokið munu hreinsunaraðilar á flokka- og leitarniðurstöðusíðum hafa síuvalkost sem byggir á birgðum. Merki á birgðastigi mun birtast fyrir hverja vöruflís sem birtist á síðunni.

Flokkurinn og leitarniðurstöðusíðan sýnir vörur á aðalstigi, ekki vöruafbrigðisstigi. Birgðastigið sem birtist við hlið hverrar vöru er uppsafnað birgðastig sem ákvarðast af birgðastigi allra afbrigða vörunnar. Birgðastig afbrigðis er reiknað út frá birgðum á lager af því afbrigði í sjálfgefnu vöruhúsi netrásarinnar í höfuðstöðvum Commerce. Birgðastig aðalvöru hefur tvö möguleg gildi sem tákna stöðu á lager og upplausn. Aðalvara telst uppselt þegar öll afbrigði hennar eru ekki til á lager. Að öðrum kosti telst varan vera á lager. Merkið fyrir gildið er sótt í [birgðastig](inventory-buffers-levels.md) skilgreiningu. Ef ekkert birgðastig er skilgreint eru sjálfgefnu merkimiðarnir (á ensku).**Laus** og **Uppselt**.

Þú getur stillt **Birgðastillingar fyrir vörulistasíður** stilling í Commerce site builder til að stjórna því hvernig flokkurinn og leitarniðurstöðusíðan birtir vörur sem eru ekki á lager. Nánari upplýsingar er að finna í [Nota birgðastillingar](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]

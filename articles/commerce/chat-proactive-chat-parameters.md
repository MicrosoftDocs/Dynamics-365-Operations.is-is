---
title: Viðskiptaspjallseining fyrirbyggjandi spjallfæribreytur
description: Þessi grein lýsir fyrirbyggjandi spjallfæribreytum Commerce spjalleininga í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690952"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Viðskiptaspjallseining fyrirbyggjandi spjallfæribreytur

[!include [banner](includes/banner.md)]

Þessi grein lýsir fyrirbyggjandi spjallfæribreytum viðskiptaspjallsins með alhliða rás fyrir þjónustu við viðskiptavini og viðskiptaspjallsins með Power Virtual Agents spjalleiningar í Microsoft Dynamics 365 Commerce.

## <a name="proactive-chat-properties"></a>Fyrirbyggjandi spjalleiginleikar

Fyrirbyggjandi spjalleiginleikarnir eru staðsettir á eiginleikarúðunni í viðskiptaspjallinu við alhliða rás fyrir þjónustu við viðskiptavini og viðskiptaspjall við Power Virtual Agents einingar í Commerce site builder.

> [!NOTE]
> Sjálfgefið er að allir fyrirbyggjandi spjalleiginleikar sem eru skráðir hér eru auðir. Við mælum með að þú lærir meira um þessa eiginleika og stillir þá aðeins eftir þörfum. Þessi nálgun mun hjálpa til við að draga úr röngum fyrirbyggjandi spjalli sem koma af stað.

### <a name="proactive-chat"></a>Fyrirbyggjandi spjall

| Vinalegt heiti | Lýsing | Sjálfgildi |
|---------------|-------------|---------------|
| Virkt | Taktu fyrirbyggjandi þátt í viðskiptavinum, byggt á mismunandi kveikjum. | Óvirkt |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. | Autt |

### <a name="wait-time-proactive-chat"></a>Biðtími (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Biðtími (sek) | Tíminn (í sekúndum) sem notendur vefsvæðisins eyða á vefsíðusíðu áður en fyrirbyggjandi spjall fer af stað. |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="number-of-page-visits-proactive-chat"></a>Fjöldi síðuheimsókna (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Fjöldi síðuheimsókna | Fjöldi síðuheimsókna áður en fyrirbyggjandi spjall er sett af stað. Notendur síðunnar verða fyrst að samþykkja hvetninguna í samþykkisborði fyrir vafrakökur. |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="specific-pages-proactive-chat"></a>Sérstakar síður (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Síður | Listi yfir þær síður sem koma af stað fyrirbyggjandi spjalli þegar þær eru heimsóttar. |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="from-specific-pages-proactive-chat"></a>Frá tilteknum síðum (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Síður | Listi yfir þær síður sem koma af stað fyrirbyggjandi spjalli þegar notendur flakka frá þeim. |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="specific-countryregion-proactive-chat"></a>Tiltekið land/svæði (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Landsnúmer | Notendur sem heimsækja frá tilgreindum löndum eða svæðum munu koma af stað fyrirbyggjandi spjalli. Lands-/svæðiskóðar ættu að vera tveir hástafir (td.**BNA**). |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="date-range-proactive-chat"></a>Dagabil (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Upphafsdagur (dd/mm/áááá) | Dagsetningin á eða eftir sem fyrirbyggjandi spjall verður sett af stað. |
| Lokadagsetning (dd/mm/áááá) | Dagsetningin sem fyrirbyggjandi spjall verður sett af stað eða fyrir. |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="total-amount-in-cart-proactive-chat"></a>Heildarupphæð í körfu (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Lágmark | Lágmarksfjárhæð (meðtalin) í innkaupakörfunni sem mun koma af stað fyrirbyggjandi spjalli þegar notendur heimsækja körfusíðuna. |
| Hámark | Hámarksfjárhæð (meðtalin) í innkaupakörfunni sem mun koma af stað fyrirbyggjandi spjalli þegar notendur heimsækja körfusíðuna. |
|Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Heildarfjöldi hluta í körfu (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Lágmark | Lágmarksfjöldi vara (meðtalinn) í innkaupakörfunni sem kallar á fyrirbyggjandi spjall þegar notendur heimsækja körfusíðuna. |
| Hámark | Hámarksfjöldi vara (meðtalinn) í innkaupakörfunni sem kallar á fyrirbyggjandi spjall þegar notendur heimsækja körfusíðuna. |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

### <a name="specific-products-in-cart-proactive-chat"></a>Sérstakar vörur í körfu (fyrirbyggjandi spjall)

| Vinalegt heiti | Lýsing |
|---------------|-------------|
| Vöruauðkenni/SKU | Listi yfir vöruauðkenni/birgðahaldseininga (SKU) númer sem koma af stað fyrirbyggjandi spjalli þegar notendur heimsækja körfusíðuna. |
| Spjallkveðja | Kveðjuskilaboðin sem eru notuð þegar fyrirbyggjandi spjall hefur verið sett af stað. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir eiginleika viðskiptaspjalls](commerce-chat-overview.md)

[Viðskiptaspjall með alhliða rás fyrir þjónustudeild](commerce-chat-module.md)

[Viðskiptaspjall við Power Virtual Agents mát](chat-module-pva.md)

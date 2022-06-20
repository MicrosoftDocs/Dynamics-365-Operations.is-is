---
title: Tilraunir í Dynamics 365 Commerce
description: Tilraunir gera þér kleift að stofna, breyta og stjórna síðuútliti og meðhöndla efni í vefsmiðnum. Stuðningur fyrir tilraunir er virkjaður fyrir síður rafrænna viðskipta og eininga innan síðu.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946215"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Tilraunir í Dynamics 365 Commerce
Notið tilraunir í Dynamics 365 Commerce til að sannprófa tilgátur um árangur af síðum rafrænna viðskipta og takið ákvarðanir sem styðjast við gögn. Commerce styður A/B-prófun á síðum, einingum og brotum og gerir notanda kleift að mæla áhrif fyrirhugaðra breytinga á vefsvæði notanda.

Hægt er að búa til, breyta og stjórna síðu og meðhöndlun efnis sem þekkist sem **afbrigði** í Commerce vefsmið. Commerce samþættast við þjónustu þriðja aðila sem hægt er að nota til að búa til tilraunir og úthluta meðhöndlun. Flæði rauntímatilvika sem sótt eru í Commerce virkja greiningar sem skilgreina niðurstöður tilraunarinnar í þjónustu þriðja aðila. Síðan er hægt að nota þessar greiningar til að samþykkja eða hafna tilgátunni.

## <a name="set-up-prerequisites"></a>Uppsetningarforkröfur

1. **Fá rétta útgáfu af Commerce** - Uppfærið einingasafnið, stækkunarhæfni hugbúnaðarþróunarsafns (SDK) fyrir netrás og Commerce Scale Unit í Commerce útgáfu 10.0.3 eða nýrri.
1. **Setja upp tengil tilraunar** - Tengill tilraunar gerir Commerce kleift að tengjast við þjónustu þriðja aðila til að sækja lista yfir tilraunir og ákvarða hvenær sýna á notanda tilraun. Hægt er að kaupa tengil frá þriðja aðila af [AppSource](https://appsource.microsoft.com). Fylgja skal leiðbeiningum um uppsetningu útgefandans. Einnig er hægt að nota prufutengilinn úr Commerce til að prófa verkflæði tilraunarinnar án þess að þurfa að skilgreina ytri þjónustu. Frekari upplýsingar er að finna í [Skilgreina og virkja tengla](e-commerce-extensibility/connectors.md). 
1. **Kveiktu á fána tilraunaeiginleika í Commerce** - Þú getur virkjað tilraunir á leigjandastigi með því að fara á **Stillingar leigjanda \> Eiginleikar**, eða á vefsvæðinu með því að fara á **Vefstillingar \> Eiginleikar**. Kveiktu á **Tilraunir** flagga til að byrja að búa til einingaafbrigði. Ef slökkt er á þessu flaggi verða ekki frekari tilraunir sýndar notendum og allar breytingaraðgerðir verða fjarlægðar innan vefhönnuðar.
    
## <a name="experimentation-lifecycle"></a>Stuðningstími tilraunar

Uppsetning tilraunar, stofnun afbrigða og keyrsla tilraunar er endurtekið ferli. Skýringarmyndin hér á eftir sýnir stuðningstíma tilraunarinnar í Commerce og þjónustu þriðja aðila. 

[ ![Stuðningstími tilraunar.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Til að læra meira um hvert skref í tilraunaferlinu skaltu skoða eftirfarandi greinar.
- [Auðkenna tilgátu og ákvarða mælieiningar fyrir tilraun](experimentation-identify.md)
- [Setja upp tilraun](experimentation-setup.md)
- [Tengja og breyta tilraun](experimentation-connect-edit.md)
- [Forskoða og birta tilraun](experimentation-preview-publish.md)
- [Keyra og fylgjast með tilraun](experimentation-run-monitor.md)
- [Kynna afbrigði og ljúka tilraun](experimentation-review-complete.md)

> [!NOTE]
> Til að sjá hvar tilraun er í ferlinu skal velja **Tilraunir** í vinstra yfirlitssvæði á vefsmið. Listi yfir tilraunir er sýndur með stöðu hverrar tilraunar í bæði Commerce og þjónustu þriðja aðila. Frekari upplýsingar er að finna í [Fara yfir stöðu tilraunar](experimentation-status.md).

## <a name="next-step"></a>Næsta skref
[Auðkenna tilgátu og ákvarða árangursmælingar fyrir tilraun](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

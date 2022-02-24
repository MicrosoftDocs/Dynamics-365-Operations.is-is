---
title: Tilraunir í Dynamics 365 Commerce
description: Tilraunir gera þér kleift að stofna, breyta og stjórna síðuútliti og meðhöndla efni í vefsmiðnum. Stuðningur fyrir tilraunir er virkjaður fyrir síður rafrænna viðskipta og eininga innan síðu.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 85eb7a661cc66c42699797cca4fa6820941de7c0
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413298"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Tilraunir í Dynamics 365 Commerce
Notið tilraunir í Dynamics 365 Commerce til að sannprófa tilgátur um árangur af síðum rafrænna viðskipta og takið ákvarðanir sem styðjast við gögn. Commerce styður A/B-prófun á síðum, einingum og brotum og gerir notanda kleift að mæla áhrif fyrirhugaðra breytinga á vefsvæði notanda.

Hægt er að búa til, breyta og stjórna síðu og meðhöndlun efnis sem þekkist sem **afbrigði** í Commerce vefsmið. Commerce samþættast við þjónustu þriðja aðila sem hægt er að nota til að búa til tilraunir og úthluta meðhöndlun. Flæði rauntímatilvika sem sótt eru í Commerce virkja greiningar sem skilgreina niðurstöður tilraunarinnar í þjónustu þriðja aðila. Síðan er hægt að nota þessar greiningar til að samþykkja eða hafna tilgátunni.

## <a name="set-up-prerequisites"></a>Uppsetningarforkröfur
1. **Fá rétta útgáfu af Commerce** - Uppfærið einingasafnið, stækkunarhæfni hugbúnaðarþróunarsafns (SDK) fyrir netrás og Commerce Scale Unit í Commerce útgáfu 10.0.3 eða nýrri.
1. **Setja upp tengil tilraunar** - Tengill tilraunar gerir Commerce kleift að tengjast við þjónustu þriðja aðila til að sækja lista yfir tilraunir og ákvarða hvenær sýna á notanda tilraun. Hægt er að kaupa tengil frá þriðja aðila af [AppSource](https://appsource.microsoft.com). Fylgja skal leiðbeiningum um uppsetningu útgefandans. Einnig er hægt að nota prufutengilinn úr Commerce til að prófa verkflæði tilraunarinnar án þess að þurfa að skilgreina ytri þjónustu. Frekari upplýsingar er að finna í [Skilgreina og virkja tengla](e-commerce-extensibility/connectors.md). 
1. **Kveikja á flöggum tilraunaeiginleika í Commerce** - Hægt er að virkja tilraunir á leigjandastigi með því að fara í **Stillingar leigjanda > Eiginleikar** eða á stigi vefsvæðis í **Stillingar vefsvæðis > Eiginleikar**.
    - Virkjið flaggið **Tilraun** til að búa til tilraunaafbrigði af einingum innan síðu án þess að hafa áhrif á eða afrita annað efni sem er ekki hluti af tilrauninni. Þetta tryggir að áframhaldandi uppfærslur efnis utan tilraunarinnar haldist samstilltar á meðan á tilraunaferlinu stendur. Ef slökkt er á þessu flaggi verða ekki frekari tilraunir sýndar notendum og allar breytingaraðgerðir verða fjarlægðar innan vefhönnuðar.
    - Virkjið flaggið **Gera tilraun á síðum eða brotum** til að keyra tilraunir á síðu eða síðubroti. Þetta býr til fullt afrit af tilviki allrar síðunnar eða brotsins fyrir allar einingar innan síðunnar eða brotsins. Notið þessa stillingu ef á að prófa heildstæða breytingar á efni, eða þar sem samstilling efnis sem er í breytingu þvert yfir tilvik er ekki áhyggjuefni. Ef slökkt er á þessu flaggi kemur það í veg fyrir stofnun eða breytingu á nýjum tilraunum á síðum eða brotum.
    > [!NOTE]
    > Flaggið **Tilraun** þarf einnig að virkja fyrir virknina **Gera tilraun á síðum eða brotum** til að það virki.
    
## <a name="experimentation-lifecycle"></a>Stuðningstími tilraunar
Uppsetning tilraunar, stofnun afbrigða og keyrsla tilraunar er endurtekið ferli. Skýringarmyndin hér á eftir sýnir stuðningstíma tilraunarinnar í Commerce og þjónustu þriðja aðila. 

[ ![Stuðningstími tilraunar](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Til að fá frekari upplýsingar um hvert skref í tilraunaferlinu skal skoða eftirfarandi efnisatriði.
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

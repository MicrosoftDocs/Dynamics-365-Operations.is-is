---
title: Færibreytur fyrir umsjón hönnunarbreytinga
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla eiginleika umsjónar hönnunarbreytinga fyrir Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 106c3a79236bcb8112ecbd48e29f3f5f3148a867
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7581009"
---
# <a name="engineering-change-management-parameters"></a>Færibreytur fyrir umsjón hönnunarbreytinga

[!include [banner](../includes/banner.md)]

Síðan **færibreytur fyrir umsjón hönnunarbreytinga** inniheldur uppsetningarfæribreytur sem breyta sjálfgefinni hegðun varðandi losun afurðaskipulagsins og breytingaferla í umsjón fyrir hönnunarbreytingar.

## <a name="open-the-engineering-change-management-parameters-page"></a>Opna síðu færibreyta fyrir umsjón hönnunarbreytinga

Til að opna síðuna **Breyta færibreytum fyrir umsjón hönnunarbreytinga** er farið í **Umsjón hönnunarbreytinga \> Uppsetning \> Færibreytur fyrir umsjón hönnunarbreytinga**. Síðan er hægt að stilla svæðin eins og lýst er í hlutunum hér á eftir í þessu efnisatriði.

## <a name="release-control-tab"></a>Flipinn Stjórnun losunar

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flipanum **Stjórnun losunar** á síðunni **Færibreytur fyrir umsjón hönnunarbreytinga**. Þessi svæði hafa áhrif á losunarferli afurðarskipulags.

| Svæði | lýsing |
|---|---|
| Regla vörunúmers | Veldu hvernig á að skilgreina afurðarnúmerið þegar afurðin er losuð til lögaðila. Veldu *Afurðarnúmer hönnunar* ef afurðarnúmer móttökulögaðilans á að samsvara afurðarnúmerinu í hönnunarfyrirtækinu. Veldu *Staðbundna vörunúmeraröð* ef afurðin á að taka næsta númer í númeraröðinni fyrir afurðarnúmer í móttökulögaðilanum. |
| Regla um heiti uppskriftar | Veldu hvernig heiti uppskriftar (BOM) er skilgreint þegar afurðin er móttekin (losuð) á lögaðila. Veldu annað hvort *Heiti hönnunar* eða *Móttaka afurðarnúmers*. |
| Regla um heiti leiðar | Veldu hvernig á að skilgreina leiðarheitið þegar leið afurðar er móttekin (losuð) í lögaðila. Veldu annað hvort *Heiti hönnunar* eða *Móttaka afurðarnúmers*. |
| Keyra athugun á uppskrift | Veldu hvort keyra eigi BOM-athugun verður keyrð þegar afurðin er móttekin (losuð) í lögaðila. |
| Losunarhegðun óvirkra uppskrifta | Veldu hvort hægt er að losa afurð ef hún er með óvirka BOM. Veldu *Samþykkja*, *Aðeins viðvörun*, eða *Ekki leyft*. |
| Losunarhegðun óvirkrar leiðar | Veldu hvort hægt er að losa afurð ef hún hefur óvirka leið. Veldu *Samþykkja*, *Aðeins viðvörun*, eða *Ekki leyft*.|
| Samþykki afurðar | Veldu hvort skref til viðbótar sé áskilið til að fá samþykki áður en hægt er að losa afurðina í lögaðilanum. Veljið *Handvirkt* til að bæta við samþykktarskrefið. Í þessu tilfellum sýnir síðan **Opna losanir afurðar** afurðirnar. Veldu *Sjálfvirkt* til að sýna afurðina beint á síðunni **Losaðar afurðir** í móttökulögaðilanum strax eftir að afurðin er losuð ásamt skipulagi afurðarlosunar. |

## <a name="engineering-change-management-tab"></a>Flipi umsjónar hönnunarbreytinga

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk á flipanum **Umsjón hönnunarbreytinga** á síðunni **Færibreytur fyrir umsjón hönnunarbreytinga**. Þessar stillingar hafa áhrif á umsjónarferli hönnunarbreytinga.

| Svæði | lýsing |
|---|---|
| Tegund | Sjálfgefni flokkurinn sem verður notaður þegar beiðni um hönnunarbreytingu er búin til. |
| Forgangur | Sjálfgefni forgangurinn sem verður notaður þegar hönnunarbreyting er búin til. |
| Alvarleikaregla | Veldu hvernig á að stofna alvarleika vegna hönnunarbreytingapöntunar. Veldu *Handvirkt* ef búist er við því að gildi sé slegið inn í svæðið **Alvarleiki**. Veldu *Reikna* til að láta kerfið reikna út gildi svæðisins **Alvarleika** þegar þú velur að **Reikna út alvarleika** á aðgerðasvæði hönnunarbreytingapöntunarinnar. Í slíku tilviki notar kerfið alvarleikareglurnar sem eru skilgreindar á síðunni **Stilla alvarleikareglu**. Veldu *Reikna sjálfkrafa* til að gildi svæðisins **Alvarleiki** sé reiknað sjálfkrafa og útfyllt samkvæmt stillingum alvarleikareglu. |
| Endurútgefa afurðir sem verða fyrir áhrifum | Þetta svæði á við þegar þú losar afurðir aftur með hönnunarbreytingarpöntun. Þú getur valið hvort leggja eigi til allar afurðir eða viðkomandi afurðir í svarglugganum **Losanir**. |
| Uppskriftarþrep sem á að gefa út | Dýpt BOM-stigsins sem skal sleppa. Þegar fleiri stig eru til staðar í BOM (þ.e. ef uppskriftin er dýpri) en gildið sem er tilgreint hér, verður aðeins losað um stigin samkvæmt tilgreindu gildi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
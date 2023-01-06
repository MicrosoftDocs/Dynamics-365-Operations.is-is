---
title: Setja upp skattakóða
description: Í þessari grein er útskýrt hvernig á að setja upp skattkóða í Skattaútreikningsþjónustu.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 1bc250716763ce9d8e25c8850c8a3676bf65fb0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862929"
---
# <a name="set-up-tax-codes"></a>Setja upp skattakóða

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp skattkóða í Skattaútreikningsþjónustu. Það felur í sér uppsetningu fyrir einfaldar aðstæður til að fá skattkóðann til að virka og upplýsingar um ítarlega skattkóðavirkni fyrir flóknar aðstæður.

> [!IMPORTANT]
> Uppsetning skattkóða í skattaútreikningsþjónustunni er óháð lögaðila. Aðeins er hægt að ljúka við þessa uppsetningu í Regulatory Configuration Service (RCS) einu sinni. Skattkóðar eru sjálfkrafa samstilltir við Microsoft Dynamics 365 Finance þegar skattútreikningsþjónustan er virkjuð fyrir valinn lögaðila í Finance.

## <a name="simple-setup"></a>Einföld uppsetning

Fylgdu þessum skrefum til að nota skattkóða í einföldum aðstæðum, til dæmis aðstæðum þar sem aðeins eitt skatthlutfall er.

1. Skrá inn á [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Farið í **Vinnusvæði** \> **Altækir eiginleikar** \> **Skattaútreikningur**.
3. Veljið eiginleikann og útgáfuna sem á að setja upp og veljið svo **Breyta**.
4. Í flipanum **Almennt** skal velja **Útgáfa skilgreiningar**.
5. Í flipanum **Skattkóðar** skal velja **Bæta við** og slá inn skattkóðann og lýsingu.
6. Veljið **Uppruni útreiknings**. Uppruni útreiknings er flokkur af aðferðum sem skilgreindar eru í útgáfu skattaskilgreiningar sem þú valdir. Í þessu einfalda tilfelli skaltu velja **Eftir nettóupphæð**.
7. Veldu **Vista**. Fleiri reitir verða tiltækir samkvæmt uppruna útreiknings sem var valinn.
8. Á flýtiflipanum **Verð** skal velja **Bæta við** til að bæta við einu skatthlutfalli fyrir þennan skattkóða.
9. Veldu **Vista**.

## <a name="calculation-origin"></a>Uppruni útreiknings

Upprunaútreikningur skilgreinir hvernig skattgrunnupphæð og skattupphæð eru reiknaðar út. Það er skilgreint af skattaskilgreiningum á vinnusvæðinu **Rafræn skýrslugerð**. Eftirtalin gildi eru tiltæk á svæðinu **Uppruni útreiknings**:

- Eftir nettóupphæð
- Eftir brúttóupphæð
- Eftir magni
- Eftir framlegð
- Skattur á skatt

### <a name="by-net-amount"></a>Eftir nettóupphæð

Ef valið er **Eftir nettóupphæð** í reitnum **Uppruni útreiknings** er skattupphæðin reiknuð sem prósenta af innkaupa- og söluupphæð, útilokar alla aðra skattkóða.

Til dæmis er skatthlutfallið 25 prósent, reikningslínan sýnir magn 10 vara sem kosta 1,00 hver og viðskiptavinurinn fær 10% línuafslátt. Í þessu tilviki eru upphæðir reiknaðar út á eftirfarandi hátt:

- **Nettóupphæð:** (10 × 1,00) – 10 prósent = 9,00 
- **Söluskattur:** 9,00 × 25 prósent = 2,25 
- **Heildarupphæð reiknings:** 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Eftir brúttóupphæð

Ef valið er **Eftir brúttóupphæð** í reitnum **Uppruni útreiknings** er skattupphæðin reiknuð sem prósenta af brúttóupphæð sölu. Brúttóupphæð er nettólínuupphæð plús allir skattar og gjöld línunnar, nema einn skattur þar sem svæðið **Uppruni útreiknings** er stilltur á **Eftir brúttóupphæð**.

Skattyfirvöld hafa t.d. lagt sérstök gjöld á vöru. Upphæð gjaldanna er bætt við nettóupphæðina áður en skattur er reiknaður út. Eftirfarandi skattkóðar eru notaðir:

- **Gjald 1** – Hlutfallið er 10 prósent og útreikningsaðferðin **Eftir nettóupphæð** er notuð.
- **Gjald 2** – Hlutfallið er 20 prósent, og **Eftir nettóupphæð** útreikningsaðferð er notað.
- **Skatthlutfall** – Hlutfallið er 25 prósent og útreikningsaðferðin **Eftir brúttóupphæð** er notuð.

Ef nettóupphæðin er 10,00 er gjald 1 upphæðin 1,00 (10,00 × 10 prósent) og gjald 2 upphæðin er 2,00 (10,00 × 20 prósent). Í þessu tilviki eru upphæðir reiknaðar út á eftirfarandi hátt: 

- **Brúttóupphæð:** Nettóupphæð + upphæð Gjalds 1 + upphæð Gjalds 2 = 10,00 + 1,00 + 2,00 = 13,00 
- **Skattupphæð:** 13,00 × 25 prósent = 3,25 
- **Heildargjöld og -skattur:** 1,00 + 2,00 + 3,25 = 6,25 
- **Heildarupphæð reiknings:** 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Eftir magni

Ef valið er **Eftir magni** í reitnum **Uppruni útreiknings** er skattupphæðin reiknuð sem föst upphæð á einingu og margfaldað með magninu sem fært er inn í skjalalínuna. Upphæðin á einingu er tilgreind á flýtiflipanum **Verð**.

Til dæmis er skattkóðinn settur upp sem 1,20 fyrir hverja einingu. Á sölureikningslínu eru seldar 25 einingar af vöru. Í þessu tilfelli er skattupphæðin reiknuð sem 25 × 1,20 = 30,00.

### <a name="by-margin"></a>Eftir framlegð

Ef valið er **Eftir framlegð** í reitnum **Uppruni útreiknings** er skattupphæðin reiknuð sem prósenta af söluframlegðinni. Söluálagningin er söluupphæðin að frádreginni kostnaðarupphæðinni. Þessi útreikningsaðferð á einungis við um sölufærslur.

Til dæmis er skatthlutfallið 25 prósent, reikningslínan sýnir magn 10 vara sem kosta 10,00 hver og kostnaður á vöru er 6. Í þessu tilviki eru upphæðir reiknaðar út á eftirfarandi hátt:

- **Álagning:** 10 × ( 10,00 – 6,00) = 40,00
- **Skattupphæð:** 40,00 × 25 prósent = 10,00
- **Heildarupphæð reiknings:** 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Skattur á skatt

Ef valið er **Skattur á skatt** í reitnum **Uppruni útreiknings** er söluskatturinn reiknaður sem prósenta af öllum öðrum skattupphæðum í sömu skjalalínunni.

Til dæmis eru eftirfarandi skattkóðar notaðir:

- **Gjald 1** – Hlutfallið er 10 prósent og útreikningsaðferðin **Eftir nettóupphæð** er notuð.
- **Gjald 2** – Hlutfallið er 20 prósent, og **Eftir nettóupphæð** útreikningsaðferð er notað.
- **Skattur á gjald** – Hlutfallið er 25 prósent og notast er við útreikningsaðferðina **Skattur á skatt**.

Í þessu tilviki eru upphæðir reiknaðar út á eftirfarandi hátt:

- **Nettóupphæð:** 10,00 
- **Gjald 1:** 10,00 × 10 prósent = 1,00 
- **Gjald 2:** 10,00 × 20 prósent = 2,00 
- **Skattur á gjald:** 3,00 × 25 prósent = 0,75
- **Heildarskattur:** 1,00 + 2,00 + 0,75 = 3,75 
- **Heildarupphæð reiknings:** 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Ítarleg virkni

Þessi hluti útskýrir ítarlega virkni skattkóðauppsetningar fyrir flóknar aðstæður.

### <a name="tax-exemption"></a>Skattundanþága

Ef valkosturinn **Er undanskilið** er stilltur á **Já** í flýtiflipanum **Almennt** verður skattupphæðinni alltaf hnekkti í 0 (núll) óháð raunverulegu skatthlutfalli.

Þú getur stillt svæðið **Undanþágukóði** til að tilgreina ástæðu fyrir undanþágunni. 

Þú getur virkjað uppflettingu aðalgagna fyrir reitinn **Undanþágukóði**. Með þeim hætti er hægt að velja á milli undanþágukóðagilda sem eru skilgreind í Finance. Upplýsingar um hvernig á að virkja uppflettingu aðalgagna er að finna í [Virkja uppflettingu aðalgagna fyrir skattaútreikningsstillingar](tax-service-set-up-environment-master-data-lookup.md).

Til dæmis er skatthlutfallið 25 prósent og valkosturinn **Er undanskilið** stilltur á **Já** í skattkóðanum. Reikningslínan sýnir magn 10 vara sem kosta 1,00 hver og viðskiptavinurinn fær 10 prósent línuafslátt. Í þessu tilviki eru upphæðir reiknaðar út á eftirfarandi hátt:

- **Nettóupphæð:** (10 × 1,00) – 10 prósent = 9,00 
- **Virðisaukaskattur:** 0,00 
- **Heildarupphæð reiknings:** 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Neysluskattur

Ef valkosturinn **Er notkunarskattur** er stilltur á **Já** í flýtiflipanum **Almennt** verður skattupphæðin bókuð á lykilinn **Útskattur** í staðinn fyrir **Safnlykil lánardrottins**.

Til dæmis er skatthlutfallið 25 prósent og valkosturinn **Er notkunarskattur** er stilltur á **Já** í skattkóðanum. Reikningslínan sýnir magn 10 vara sem kosta 1,00 hver og viðskiptavinurinn fær 10 prósent línuafslátt. Í þessu tilviki eru upphæðir reiknaðar út á eftirfarandi hátt:

- **Nettóupphæð:** (10 × 1,00) – 10 prósent = 9,00 
- **Neysluskattur:** 9,00 × 25 prósent = 2,25
- **Heildarupphæð reiknings:** 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Ef bæði valkosturinn **Er undanskilið** og valkosturinn **Er notkunarskattur** er stilltur á **Já** í skattkóða verður kóðinn skráður sem undanþeginn skatti fyrir sölufærslur og notkunarskattur fyrir innkaupafærslur.

### <a name="reverse-charges"></a>Bakfærð gjöld

Ef valkosturinn **Er bakfært gjald** er stilltur á **Já** í flýtiflipanum **Almennt** er hægt að skilgreina skatthlutfallið sem neikvætt. Fyrir aðstæður bakfærðs gjalds er mælt með að settir séu upp tveir skattkóðar: einn sem er með jákvætt skatthlutfall og annan sem er með neikvætt skatthlutfall. Báðir skattkóðarnir ættu að hafa sama hlutfallið og stilla ætti valkostinn **Er bakfært gjald** á **Já** í skattkóðanum sem er með neikvætt skatthlutfall. Frekari upplýsingar um lausn bakfærðs gjalds í Finance er að finna í [Virkni bakfærðs gjalds fyrir skema VSK/VÞS](emea-reverse-charge.md).

Til dæmis eru tveir skattkóðar ákvarðaðir á einni reiknislínu. Eitt skatthlutfall er 25%. Annað skatthlutfall er -25 prósent og valkosturinn **Er bakfært gjald** er stilltur á **Já** í öðrum skattkóðanum. Reikningslínan sýnir magn 10 vara sem kosta 1,00 hver. Í þessu tilfelli eru upphæðirnar reiknaðar á eftirfarandi hátt:

- **Nettóupphæð:** (10 × 1,00) 10,00 prósent 
- **Skattkóði 1:** 10,00 × 25 prósent = 2,50
- **Skattkóði 2:** 10 × -25 prósent = -2,50
- **Heildarupphæð reiknings:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Undanskilið úr útreikningi grunnupphæðar

Ef valkosturinn **Undanskilja úr útreikningi grunnupphæðar** er stilltur á **Já** í flýtiflipanum **Almennt** er reiknuð skattupphæð skattkóðans undanskilin frá skattgrunnupphæðinni fyrir aðra útreikninga á skattkóða í aðstæðum með verði.

Frekari upplýsingar eru í [Reikna skatt ofan á verð þegar „Verð eru með sköttum“ er virkt](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Hlutföll

Í flýtiflipanum **Hlutfall** er hægt að skilgreina mismunandi skatthlutföll fyrir mismunandi bil af skattgrunnupphæðum. Til að reikna út skattupphæðina notar skattaútreikningsþjónustan alltaf hlutfallið sem passar við skattgrunnupphæðina.

Til dæmis er hægt að skilgreina skatthlutfall eins og sýnt er í eftirfarandi töflu.

| Lágmarksupphæð | Hámarksupphæð | Skatthlutfall   |
| -------------- | -------------- | ---------- |
| 0              | 1.000          | 10 prósent |
| 1.000          | 5.000          | 15 prósent |
| 5.000          | 10,000         | 20 prósent |
| 10,000         | 0              | 30 prósent |

Í þessu tilfelli er skattupphæðin reiknuð á eftirfarandi hátt:

- Ef skattgrunnupphæðin er 300,00 er skatthlutfallið 10 prósent og skattupphæðin er 300,00 x 10 prósent = 30,00.
- Ef skattgrunnupphæðin er 3.000,00 er skatthlutfallið 15 prósent og skattupphæðin er 3.000,00 x 15 prósent = 450,00.
- Ef skattgrunnupphæðin er 6.000,00 er skatthlutfallið 20 prósent og skattupphæðin er 6.000,00 x 10 prósent = 1.200,00.
- Ef skattgrunnupphæðin er 20.000,00 er skatthlutfallið 30 prósent og skattupphæðin er 20.000,00 x 30 prósent = 6.000,00.

> [!NOTE]
> Ef skattgrunnupphæðin getur samsvarað bæði hámarksupphæð í einni línu og lágmarksupphæð í annarri línu mun grunnurinn nota skatthlufallið sem samsvarar lágmarksgrunnupphæðinni. Ef skattgrunnupphæðin er til dæmis 1.000,00 er skatthlutfallið 15 prósent og skattupphæðin er 1.000,00 x 15 prósent = 150,00.

### <a name="limits"></a>Mörk

Í flýtiflipanum **Mörk** er hægt að skilgreina skattmörk til að hnekkja reiknaðri skattupphæð ef skattupphæðin fellur fyrir innan bilsins lágmark/hámark.

- Ef reiknuð skattupphæð er hærri en eða jafnt og hámarksskattupphæð sem er skilgreind í flýtiflipanum **Mörk** mun lokaskattupphæðin vera jafnt og hámarksskattupphæðin.
- Ef reiknuð skattupphæð er minni en lágmarksskattupphæðin sem er skilgreind í flýtiflipanum **Mörk** er lokaskattupphæðin 0 (núll).

Skattleysismörkin eru til dæmis grunnstillt á eftirfarandi hátt:

- **Lágmarksskattupphæð:** 100 
- **Hámarksskattupphæð:** 1000

Ef reiknuð skattupphæð er 2.000 er endanleg skattupphæð 1.000.

Ef reiknuð skattupphæð er 500 er endanleg skattupphæð 500.

Ef reiknuð skattupphæð er 80 er endanleg skattupphæð 0 (núll).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

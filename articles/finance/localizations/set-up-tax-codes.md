---
title: Settu upp skattakóða
description: Þetta efnisatriði útskýrir hvernig á að setja upp skattkóða í skattreikningsþjónustunni.
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
ms.openlocfilehash: 8bdb194e7d8b704d1e58d3c25bf2e1f6bff1ba00
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883904"
---
# <a name="set-up-tax-codes"></a>Settu upp skattakóða

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp skattkóða í skattaútreikningsþjónustunni. Það felur í sér uppsetningu fyrir einfalda atburðarás til að láta skattkóðann virka og upplýsingar um háþróaða skattakóðavirkni fyrir flóknar aðstæður.

> [!IMPORTANT]
> Uppsetning skattkóða í skattútreikningsþjónustunni er lögaðili-agnostic. Þú getur klárað þessa uppsetningu í Regulatory Configuration Service (RCS) aðeins einu sinni. Skattkóðar eru sjálfkrafa samstilltir við Microsoft Dynamics 365 Finance þegar þú virkjar skattreikningsþjónustuna fyrir valinn lögaðila í Fjármálum.

## <a name="simple-setup"></a>Einföld uppsetning

Fylgdu þessum skrefum til að nota skattkóða í einfaldri atburðarás, eins og atburðarás þar sem aðeins er eitt skatthlutfall.

1. Skrá inn [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Fara til **Vinnurými** \> **Hnattvæðingareiginleikar** \> **Skattútreikningur**.
3. Veldu eiginleikann og útgáfuna sem þú vilt setja upp og veldu **Breyta**.
4. Á **Almennt** flipa, veldu **Stillingarútgáfa**.
5. Í flipanum **Skattkóðar** skal velja **Bæta við** og slá inn skattkóðann og lýsingu.
6. Veldu **Uppruni útreiknings**. Uppruni útreiknings er hópur aðferða sem eru skilgreindar í skattstillingarútgáfunni sem þú valdir. Fyrir þessa einföldu atburðarás skaltu velja **Eftir nettóupphæð**.
7. Veldu **Vista**. Fleiri reitir verða tiltækir, byggt á uppruna útreikningsins sem þú valdir.
8. Á **Verð** Flýtiflipi, veldu **Bæta við** að bæta við einu skatthlutfalli fyrir þennan skattakóða.
9. Veldu **Vista**.

## <a name="calculation-origin"></a>Uppruni útreiknings

Uppruni útreiknings skilgreinir hvernig skattstofnfjárhæð og skattfjárhæð eru reiknuð út. Það er stillt með skattstillingu í **Rafræn skýrslugerð** vinnurými. Eftirfarandi gildi eru fáanleg í **Uppruni útreiknings** reit:

- Eftir nettóupphæð
- Eftir brúttóupphæð
- Eftir magni
- Eftir framlegð
- Skattur á skatt

### <a name="by-net-amount"></a>Eftir nettóupphæð

Ef þú velur **Eftir nettóupphæð** í **Uppruni útreiknings** reitnum er skattupphæðin reiknuð sem hlutfall af innkaupa- eða söluupphæð, að undanskildum öðrum skattkóðum.

Til dæmis er skatthlutfallið 25 prósent, reikningslínan sýnir magn af 10 vörum á 1,00 hver og viðskiptavinurinn fær 10 prósenta línuafslátt. Í þessu tilviki eru upphæðir reiknaðar á eftirfarandi hátt:

- **Virði:** (10 × 1,00) – 10 prósent = 9,00 
- **Söluskattur:** 9,00 × 25 prósent = 2,25 
- **Heildarupphæð reiknings:** 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Eftir brúttóupphæð

Ef þú velur **Með brúttóupphæð** í **Uppruni útreiknings** reit er skattfjárhæð reiknuð sem hlutfall af brúttósöluupphæð. Brúttóupphæðin er nettóupphæð línunnar auk allra skatta og gjalda fyrir línuna nema skatturinn þar sem **Uppruni útreiknings** reiturinn er stilltur á **Með brúttóupphæð**.

Til dæmis hefur skattyfirvöld lagt sérstaka tolla á hlut. Tollfjárhæðirnar bætast við nettóupphæðina áður en skattur er reiknaður. Eftirfarandi skattakóðar eru notaðir:

- **Skylda 1** – Gengið er 10 prósent, og **Eftir nettóupphæð** reikningsaðferð er notuð.
- **Skylda 2** – Gengið er 20 prósent, og **Eftir nettóupphæð** reikningsaðferð er notuð.
- **Skatthlutfall** - Hlutfallið er 25 prósent, og **Með brúttóupphæð** reikningsaðferð er notuð.

Ef nettóupphæðin er 10,00 er tollur 1 upphæð 1.00 (10.00 × 10 prósent) og tollur 2 upphæð 2.00 (10.00 × 20 prósent). Í þessu tilviki eru upphæðir reiknaðar á eftirfarandi hátt: 

- **Brúttóupphæð:** Nettóupphæð + Tollur 1 upphæð + Tollur 2 upphæð = 10,00 + 1,00 + 2,00 = 13,00 
- **Skattupphæð:** 13,00 × 25 prósent = 3,25 
- **Heildargjöld og skattar:** 1,00 + 2,00 + 3,25 = 6,25 
- **Heildarupphæð reiknings:** 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Eftir magni

Ef þú velur **Eftir magni** í **Uppruni útreiknings** reitnum er skattupphæðin reiknuð sem föst upphæð á hverja einingu og margfölduð með því magni sem fært er inn á skjalalínuna. Upphæð á hverja einingu er tilgreind á **Verð** Flýtiflipi.

Til dæmis er skattanúmerið sett upp sem 1,20 á hverja einingu. Á sölureikningslínu eru seldar 25 einingar af vöru. Í þessu tilviki er skattupphæðin reiknuð sem 25 × 1,20 = 30,00.

### <a name="by-margin"></a>Eftir framlegð

Ef þú velur **Með framlegð** í **Uppruni útreiknings** reit er skattupphæð reiknuð sem hlutfall af söluframlegð. Söluframlegð er söluupphæð að frádregnum kostnaðarupphæð. Þessi útreikningsaðferð á aðeins við um sölufærslur.

Til dæmis er skatthlutfallið 25 prósent, reikningslínan sýnir magn af 10 hlutum á 10,00 hver og kostnaður á hverja vöru er 6. Í þessu tilviki eru upphæðir reiknaðar á eftirfarandi hátt:

- **Söluhlutfall:** 10 × ( 10.00 – 6.00) = 40.00
- **Skattupphæð:** 40,00 × 25 prósent = 10,00
- **Heildarupphæð reiknings:** 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Skattur á skatt

Ef þú velur **Skattur á skatt** í **Uppruni útreiknings** reitnum er söluskatturinn reiknaður sem hlutfall af öllum öðrum skattupphæðum á sömu skjalalínu.

Til dæmis eru eftirfarandi skattakóðar notaðir:

- **Skylda 1** – Gengið er 10 prósent, og **Eftir nettóupphæð** reikningsaðferð er notuð.
- **Skylda 2** – Gengið er 20 prósent, og **Eftir nettóupphæð** reikningsaðferð er notuð.
- **Skattur á toll** - Hlutfallið er 25 prósent, og **Skattur á skatt** reikningsaðferð er notuð.

Í þessu tilviki eru upphæðir reiknaðar á eftirfarandi hátt:

- **Virði:** 10.00 
- **Skylda 1:** 10,00 × 10 prósent = 1,00 
- **Skylda 2:** 10,00 × 20 prósent = 2,00 
- **Skattur á toll:** 3,00 × 25 prósent = 0,75
- **Heildarskattur:** 1,00 + 2,00 + 0,75 = 3,75 
- **Heildarupphæð reiknings:** 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Háþróuð virkni

Þessi hluti útskýrir nokkra háþróaða virkni skattkóðauppsetningar fyrir flóknar aðstæður.

### <a name="tax-exemption"></a>Skattundanþága

Ef þú stillir **Er undanþegin** valmöguleika til **Já** á **Almennt** Flýtiflipa, skattupphæðinni verður alltaf hnekkt í 0 (núll), óháð raunverulegu skatthlutfalli.

Þú getur stillt **Undanþágukóði** reit til að tilgreina ástæðu undanþágunnar. 

Þú getur virkjað aðalgagnaleit fyrir **Undanþágukóði** sviði. Þannig geturðu valið meðal undanþágukóðagilda sem eru skilgreind í Finance. Fyrir upplýsingar um hvernig á að virkja aðalgagnaleit, sjá [Virkja aðalgagnaleit fyrir skattaútreikningsstillingar](tax-service-set-up-environment-master-data-lookup.md).

Til dæmis er skatthlutfallið 25 prósent og **Er undanþegin** valkostur er stilltur á **Já** á skattalögum. Reikningslínan sýnir magn af 10 hlutum á 1,00 hver og viðskiptavinurinn fær 10 prósent línuafslátt. Í þessu tilviki eru upphæðir reiknaðar á eftirfarandi hátt:

- **Virði:** (10 × 1,00) – 10 prósent = 9,00 
- **Söluskattur:** 0,00 
- **Heildarupphæð reiknings:** 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Neysluskattur

Ef þú stillir **Er Notkunarskattur** valmöguleika til **Já** á **Almennt** Flýtiflipi, skattupphæðin verður færð á **Notaðu gjaldskyldan skatt** reikning í stað **Samantekt söluaðila** reikning.

Til dæmis er skatthlutfallið 25 prósent og **Er Notkunarskattur** valkostur er stilltur á **Já** á skattalögum. Reikningslínan sýnir magn af 10 hlutum á 1,00 hver og viðskiptavinurinn fær 10 prósent línuafslátt. Í þessu tilviki eru upphæðir reiknaðar á eftirfarandi hátt:

- **Virði:** (10 × 1,00) – 10 prósent = 9,00 
- **Notaðu skatt:** 9,00 × 25 prósent = 2,25
- **Heildarupphæð reiknings:** 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Ef bæði **Er undanþegin** valmöguleika og **Er Notkunarskattur** valkostur er stilltur á **Já** á skattanúmeri verður kóðinn viðurkenndur sem skattfrjáls fyrir söluviðskipti og nota skatt fyrir kaupviðskipti.

### <a name="reverse-charges"></a>Bakfærð gjöld

Ef þú stillir **Er Reverse Charge** valmöguleika til **Já** á **Almennt** Flýtiflipa, skatthlutfallið er hægt að stilla sem neikvætt. Fyrir öfuga gjaldfærslu mælum við með því að þú setjir upp tvo skattkóða: einn sem hefur jákvætt skatthlutfall og einn sem hefur neikvætt skatthlutfall. Báðir skattakóðar ættu að hafa sama taxtagildi og **Er Reverse Charge** valkostur ætti að vera stilltur á **Já** á skattalögum sem hefur neikvæða skatthlutfall. Frekari upplýsingar um lausn bakfærðs gjalds í Finance er að finna í [Virkni bakfærðs gjalds fyrir skema VSK/VÞS](emea-reverse-charge.md).

Til dæmis eru tveir skattakóðar ákvarðaðir á einni reikningslínu. Eitt skatthlutfall er 25 prósent. Annað skatthlutfall er -25 prósent, og **Er Reverse Charge** valkostur er stilltur á **Já** á öðrum skattalögum. Reikningslínan sýnir magn af 10 hlutum á 1,00 hver. Í þessu tilviki eru upphæðirnar reiknaðar á eftirfarandi hátt:

- **Virði:** (10 × 1,00) = 10,00 
- **Skattkóði 1:** 10,00 × 25 prósent = 2,50
- **Skattkóði 2:** 10 × -25 prósent = -2,50
- **Heildarupphæð reiknings:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Útilokun frá grunnfjárhæðarútreikningum

Ef þú stillir **Útiloka frá grunnfjárhæðarútreikningi** valmöguleika til **Já** á **Almennt** Flýtiflipi, reiknuð skattupphæð skattkóðans er undanskilin frá skattstofnupphæðinni fyrir aðra útreikninga skattkóða í atburðarásinni með verð.

Fyrir frekari upplýsingar, sjá [Reiknaðu skatt af verði þegar Verð eru með sköttum er virkt](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Hlutföll

Á **Gefa** Flýtiflipa, þú getur skilgreint mismunandi skatthlutföll fyrir mismunandi svið skattstofnaupphæða. Til að reikna út skattfjárhæð notar Skattútreikningsþjónustan alltaf það hlutfall sem samsvarar skattstofnfjárhæðinni.

Til dæmis gætu skatthlutföll verið stillt eins og sýnt er í eftirfarandi töflu.

| Lágmarksupphæð | Hámarksupphæð | Skatthlutfall   |
| -------------- | -------------- | ---------- |
| 0              | 1.000          | 10 prósent |
| 1.000          | 5.000          | 15 prósent |
| 5.000          | 10,000         | 20 prósent |
| 10,000         | 0              | 30 prósent |

Í þessu tilviki er skattfjárhæð reiknuð á eftirfarandi hátt:

- Ef skattstofnfjárhæðin er 300,00 er skatthlutfallið 10 prósent og skattupphæðin er 300,00 × 10 prósent = 30,00.
- Ef skattstofnfjárhæð er 3.000,00 er skatthlutfallið 15 prósent og skattfjárhæðin er 3.000,00 × 15 prósent = 450,00.
- Ef skattstofnfjárhæðin er 6.000,00 er skatthlutfallið 20 prósent og skattfjárhæðin er 6.000,00 × 10 prósent = 1.200,00.
- Ef skattstofnupphæðin er 20,000.00 er skatthlutfallið 30 prósent og skattupphæðin er 20,000.00 × 30 prósent = 6.000,00.

> [!NOTE]
> Ef skattstofnfjárhæð getur jafnast við bæði hámarksfjárhæð á annarri línu og lágmarksfjárhæð á hinni línunni mun stofninn nota það skatthlutfall sem samsvarar lágmarksgrunnfjárhæðinni. Til dæmis, ef skattstofnupphæðin er 1000,00, þá er skatthlutfallið 15 prósent og skattupphæðin er 1.000,00 × 15 prósent = 150,00.

### <a name="limits"></a>Mörk

Á **Takmörk** Flýtiflipa, þú getur skilgreint skattamörk til að hnekkja reiknaðri skattupphæð ef skattupphæðin fellur innan lágmarks/hámarksbilsins.

- Ef reiknuð skattupphæð er hærri en eða jöfn hámarksskattupphæðinni sem er stillt á **Takmörk** Flýtiflipi, endanleg skattupphæð er jöfn hámarksskattupphæð.
- Ef útreiknuð skattupphæð er lægri en lágmarksskattupphæðin sem er stillt á **Takmörk** Flýtiflipi, endanleg skattupphæð er 0 (núll).

Til dæmis eru skattamörk stillt á eftirfarandi hátt:

- **Lágmarksupphæð skatta:** 100 
- **Hámarksskattupphæð:** 1.000

Ef útreiknuð skattfjárhæð er 2.000 er endanleg skattupphæð 1.000.

Ef útreiknuð skattupphæð er 500 er lokaskattsupphæðin 500.

Ef útreiknuð skattfjárhæð er 80 er lokaskattsupphæðin 0 (núll).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

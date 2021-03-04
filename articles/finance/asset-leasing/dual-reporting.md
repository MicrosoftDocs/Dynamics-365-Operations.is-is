---
title: Tvískipt skýrslugjöf
description: Þetta efnisatriði leiðir notandann í gegnum dæmi sem sýnir hvernig hægt er að uppfylla skilyrði bæði um skýrslugerð samkvæmt alþjóðlegum reikningsskilastaðli (IFRS) og lögboðinnar skýrslugerðar um eignaleigu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444567"
---
# <a name="dual-reporting"></a>Tvískipt skýrslugjöf

[!include [banner](../includes/banner.md)]

Þetta efnisatriði leiðir notandann í gegnum dæmi sem sýnir hvernig hægt er að uppfylla skilyrði bæði um skýrslugerð samkvæmt alþjóðlegum reikningsskilastaðli (IFRS) og lögboðinnar skýrslugerðar um eignaleigu. Þekking á bókunarlögum í Microsoft Dynamics 365 Finance er áskilin og auðveldar skilning á dæminu.

## <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir leigusamning sem fellur undir ítalska lögboðna skýrslugerð með því að nota bæði aðferð reiðufjáraðferðar og IFRS-skýrslugerðar. Fyrirtækið verður að stofna þrjár bækur til að uppfylla skilyrði ítalskra laga og skilyrði IFRS 16. Ein bók er áskilin fyrir IFRS 16, ein bók er áskilin fyrir lögboðnar kröfur og ein bók er áskilin til að bakfæra lögboðnar bókanir sjálfkrafa. Bækurnar eru settar upp eins og sýnt er í eftirfarandi töflu.

**IFRS 16 bók**

IFRS 16 bókin er sett upp þannig að hún samræmist IFRS 16 bókhaldsstaðli. Allar færslur sem eru bókaðar í þessari bók verða bókaðar í sérsniðið lag.

| Nafn                                    | lýsing    |
|-----------------------------------------|----------------|
| Gerð bókar                               | Alþjóðlegur reikningsskilastaðall 16        |
| Bókarlýsing                        | Alþjóðlegur reikningsskilastaðall 16        |
| Bókunarlag                           | Sérsniðið lag 1 |
| Gerð leigu                              | Finance        |
| Bókhaldsrammi                    | Alþjóðlegur reikningsskilastaðall 16        |
| Uppsetning leigutíma / nýtingartíma         | 0,00           |
| Uppsetning á núvirði / Gangvirði eignar | 0,00           |
| Skammtímaþröskuldur                    | 12             |
| Mörk verðlítillar eignar                     | 5,000.00       |
| Greiða lánardrottni                           | Ekkert             |

**Lögboðin bók**

Lögboðna bókin er reiðufjársbók þar sem fyrirtækið bókar leigukostnaðinn sem reiðufjárupphæðina sem er greidd mánaðarlega fyrir leigu. Þessi bók myndar hvorki afnotarétt af eign né leiguskuldbindingu.

| Nafn                                    | lýsing |
|-----------------------------------------|-------------|
| Gerð bókar                               | Lögboðið   |
| Bókarlýsing                        | Staðbundið GAAP  |
| Bókunarlag                           | Núverandi     |
| Gerð leigu                              | Sjálfvirk   |
| Bókhaldsrammi                    | Grundvöllur reiðufjár  |
| Uppsetning leigutíma / nýtingartíma         | 0,00        |
| Uppsetning á núvirði / Gangvirði eignar | 0,00        |
| Skammtímaþröskuldur                    | 0           |
| Mörk verðlítillar eignar                     | 0           |
| Greiða lánardrottni                           | Ekkert          |

**Lögboðin bakfærslubók**

Lögboðin bakfærslubók er sett upp á sama hátt og lögboðna bókin.

| Nafn                                    | lýsing                    |
|-----------------------------------------|--------------------------------|
| Gerð bókar                               | Lögboðin - Bakfærsla           |
| Bókarlýsing                        | Bók til að bakfæra lögboðna bók |
| Bókunarlag                           | Sérsniðið lag 1                 |
| Gerð leigu                              | Sjálfvirk                      |
| Bókhaldsrammi                    | Grundvöllur reiðufjár                     |
| Uppsetning leigutíma / nýtingartíma         | 0,00                           |
| Uppsetning á núvirði / Gangvirði eignar | 0,00                           |
| Skammtímaþröskuldur                    | 0                              |
| Mörk verðlítillar eignar                     | 0                              |
| Greiða lánardrottni                           | Ekkert                             |

Í þessu dæmi er búið að stofna leigusamning með eftirfarandi stillingar á flipunum **Almennt** og **Greiðsluáætlunarlínur**.

**Almennt**

| Svæði                      | Virði            |
|----------------------------|------------------|
| Vextir á nýju lánsfé | 5%               |
| Upphafsdagsetning          | 1/1/2020         |
| Leigusamningsflokkur                | Byggingar        |
| Lánardrottinn                     | 1001             |
| Gangvirði eignarinnar    | 245,000          |
| Nýtingartími eignar          | 120              |
| Tegund afborgunar               | Venjulegar afborganir |
| Samsett tímabil       | Mánaðarlega          |

**Flipi greiðsluáætlunarlína**

| Svæði             | Virði      |
|-------------------|------------|
| Upphafsdagsetning        | 1/1/2020   |
| Tímabil   | Mánuðir     |
| Tímabil           | 24         |
| Lokadagsetning          | 31/12/2020 |
| Greiðslutíðni | Mánaðarlega    |
| Upphæð greiðslu    | 1.000      |

Til að gera ráð fyrir þessum leigusamningi samkvæmt tveimur römmum er notað núverandi bókunarlag og sérsniðið bókunarlag. Eftirfarandi tafla sýnir dæmi um hverja áskilda bókarfærslu til að birta fjármál á réttan hátt samkvæmt hverjum reikningsskilastaðli fyrir sig. Ítarleg lýsing á hverri bókarfærslu fyrir fyrsta mánuð leigusamningsins er veitt eftir á.

<table>
<thead>
<tr>
<th rowspan='3'>Reikningsnúmer</th>
<th rowspan='3'>lýsing</th>
<th colspan='3'>Lögboðin bók (núverandi lag)</th>
<th rowspan='3'>Núverandi lag samtals</th>
<th>Bakfærslubók (sérsniðið lag)</th>
<th colspan='4'>IFRS 16 bók (sérsniðið lag)</th>
<th rowspan='3'>Núgildandi lag + sérsniðið lag alls</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Leigukostnaður</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Bankaþóknun</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>VSK útgjöld</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Millireikningur</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Viðskiptaskuldir</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Afnotaréttur af eign</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Skylda fjármögnunarleigusamnings</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22.794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21.888,87</td>
</tr>
<tr>
<td>8</td>
<td>Vaxtakostnaður</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Innlausn</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Afskriftakostnaður</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Uppsöfnuð afskrift</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Eins og taflan hér á undan sýnir eru þrjár bækur áskildar til skráningar bæði samkvæmt lögboðinni skýrslugerð og IFRS-skýrslugerð.

- Lögboðna bókin skráir leigugreiðsluna samkvæmt reglum fyrir reiðufjársbókhald samkvæmt núverandi lagi.
- Lögboðna bakfærslubókin bakfærir lögboðnu bókarfærslurnar.
- IFRS 16 bókin stofnar áskildar bókarfærslur samkvæmt IFRS 16.

Aðeins þarf að færa inn leigu einu sinni. Síðan er hægt að opna síðuna **Bækur** til að skoða allar bækurnar sem eru tengdar leigusamningnum.

> [!NOTE]
> Þegar búið er að stofna bækurnar verður að tengja allar þrjár við sömu leiguskrána.

Fyrsta bókarfærslan skráir kostnað leigusamningsins samkvæmt lögboðnu bókinni. Hægt er að stofna greiðslurnar annaðhvort í runu eða með því að velja greiðsluáætlunina í lögboðnu bókinni.

Í þessu dæmi er eftirfarandi bókarfærsla gerð fyrir lögboðnu bókina úr greiðsluáætlun.

### <a name="lease-payment--1312020--je-100"></a>Leigugreiðsla – 31/1/2020 – JE 100

| Lykilgerð | Reikningsnúmer | Lag   | Lýsing á lykli | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 1              | Núverandi | Leigukostnaður       | 1,000.00 |          |
| Ledger       | 4              | Núverandi | Millireikningur    |          | 1,000.00 |

Afgreiðslumaður viðskiptaskulda notar staðlaða Dynamics 365-virkni til að stofna reikning til að greiða fyrir leigusamning utan eignarleigu. Hins vegar, í stað þess að velja **Leigukostnað** sem debetlykil velur afgreiðslumaður viðskiptaskulda millireikning til að mynda eftirfarandi færslu.

### <a name="ap-process--1312020--je-110"></a>AP-ferli – 31/1/2020 – JE 110

| Lykilgerð | Reikningsnúmer | Lag   | Lýsing á lykli | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 4              | Núverandi | Millireikningur    | 1,000.00 |          |
| Ledger       | 2              | Núverandi | Bankaþóknun            | 3.00     |          |
| Ledger       | 3              | Núverandi | VSK útgjöld         | 5.00     |          |
| Lánardrottinn       | 5              | Núverandi | Viðskiptaskuldir    |          | 1,008.00 |

Þegar yfirlitið er gefið út til lánardrottins er reglubundna greiðsluferlinu fylgt eftir. Eftirfarandi bókarfærsla er mynduð við þetta ferli.

### <a name="cash-payment--1312020--je-120"></a>Reiðufjárgreiðsla – 31/1/2020 – JE 120

| Lykilgerð | Reikningsnúmer | Lag   | Lýsing á lykli | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Lánardrottinn       | 5              | Núverandi | Viðskiptaskuldir    | 1,008.00 |          |
| Banki         | 9              | Núverandi | Innlausn                |          | 1,008.00 |

Á þessu stigi er búið að reikna þetta út samkvæmt lögboðnum skýrslukröfum og hægt er að búa til prófjöfnuð með því að nota núgildandi lag. Kerfið skilar prófjöfnuði sem inniheldur eftirfarandi tölur.

<table>
<thead>
<tr>
<th rowspan='3'>Reikningsnúmer</th>
<th rowspan='3'>lýsing</th>
<th colspan='3'>Lögboðin bók (núverandi lag)</th>
<th rowspan='3'>Núverandi lag samtals</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Leigukostnaður</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Bankaþóknun</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>VSK útgjöld</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Millireikningur</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Viðskiptaskuldir</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Afnotaréttur af eign</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Skylda fjármögnunarleigusamnings</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Vaxtakostnaður</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Innlausn</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Afskriftakostnaður</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Uppsöfnuð afskrift</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Ef ætlunin er að nota tölur IFRS 16 til að keyra sama prófjöfnuð verður að bakfæra færslur lögboðinnar færslubókar og bóka IFRS 16-færslurnar. Til að bakfæra lögboðnu færslubókarfærslur, inniheldur þetta dæmi lögboðna bakfærslubók með sömu uppsetningu og lögboðin færslubók en með gagnstæða bókunarreglu. Lögboðna bókin er t.d. *skuldfærð* kostnaðarlykill leigusamnings en bakfærslubókin *kreditfærir* slíkan lykil. Þessi vensl eru skilgreind á auðveldan hátt í bókunarlyklum eignarleigu á síðunni **Færibreytur fyrir eignarleigu** (**Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**).

Þegar sama ferlið sem notað var fyrir lögboðnu bókina er notað fyrir bakfærslubókina er eftirfarandi bókarfærsla mynduð. Munurinn er sá að bakfærslubókin bókar bakfærslurnar úr lögboðnu bókinni. Bakfærslurnar eru einnig gerðar í sérstillta laginu. Þegar verið er að keyra prófjöfnuð á núverandi lagi eru færslur bakfærslubókarinnar ekki teknar með.

### <a name="lease-payment--1312020--je-130"></a>Leigugreiðsla – 31/1/2020 – JE 130

| Lykilgerð | Reikningsnúmer | Lag  | Lýsing á lykli | Debet    | Kredit   |
|--------------|----------------|--------|---------------------|----------|----------|
| Ledger       | 4              | Sérsniðinn | Millireikningur    | 1,000.00 |          |
| Ledger       | 1              | Sérsniðinn | Leigukostnaður       |          | 1,000.00 |

Nú þegar búið er að útiloka færslur lögboðnu bókarinnar verður að bóka allar áskildar bókarfærslur samkvæmt IFRS 16 í IFRS 16-bókinni. Þessar færslur fela í sér fyrstu viðurkenningu á afnotarétt af eign og ábyrgðina og færslu vaxta og afskrifta.

### <a name="initial-recognition--112020--je-140"></a>Upphafleg viðurkenning – 1/1/2020 – JE 140

| Lykilgerð | Reikningsnúmer | Lag  | Lýsing á lykli      | Debet     | Kredit    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Ledger       | 6              | Sérsniðinn | Afnotaréttur af eign                | 22,793.90 |           |
| Ledger       | 7              | Sérsniðinn | Skylda fjármögnunarleigusamnings |           | 22,793.90 |

Leigugreiðslan er bókuð á sama hátt og aðrar leigugreiðslur. Ástæðan fyrir því að nota millireikning er að tryggja að reiðufé sé aðeins kreditfært í eitt skipti.

### <a name="lease-payment--1312020--je-150"></a>Leigugreiðsla – 31/1/2020 – JE 150

| Lykilgerð | Reikningsnúmer | Lag  | Lýsing á lykli      | Debet    | Kredit   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Ledger       | 7              | Sérsniðinn | Skylda fjármögnunarleigusamnings | 1,000.00 |          |
| Ledger       | 4              | Sérsniðinn | Millireikningur         |          | 1,000.00 |

Bókarfærsla vaxtakostnaðar er mynduð úr afskriftaráætlun leiguskuldbindingar.

### <a name="interest-expense--1312020--je-160"></a>Vaxtakostnaður – 31/1/2020 – JE 160

| Lykilgerð | Reikningsnúmer | Lag  | Lýsing á lykli      | Debet | Kredit |
|--------------|----------------|--------|--------------------------|-------|--------|
| Ledger       | 8              | Sérsniðinn | Vaxtakostnaður         | 94.97 |        |
| Ledger       | 7              | Sérsniðinn | Skylda fjármögnunarleigusamnings |       | 94.97  |

Bókarfærsla afskriftakostnaðar er mynduð úr afskriftaráætlun eignar.

### <a name="depreciation-expense--1312020--je-170"></a>Afskriftarkostnaður – 1/31/2020 – JE 170

| Lykilgerð | Reikningsnúmer | Lag  | Lýsing á lykli      | Debet  | Kredit |
|--------------|----------------|--------|--------------------------|--------|--------|
| Ledger       | 10             | Sérsniðinn | Afskriftakostnaður     | 949.75 |        |
| Ledger       | 11             | Sérsniðinn | Uppsöfnuð afskrift |        | 949.75 |

Eftir að allar þessar bókarfærslur hafa verið stofnaðar og bókaðar birtast eftirfarandi gildi „Sérsniðins lags 1“. Athugaðu að í síðasta dálkinum er innifalið bankagjald, virðisaukaskattur (VSK), útgjöld og minnkun reiðufjár frá fyrra lagi, en bókarfærslur lögboðinnar skýrslugerðar eru ekki innifaldar. Þar af leiðir áttu kost á tvískiptri skýrslugjöf. Á þessu stigi þarf fyrirtækið aðeins að keyra prófjöfnuð sinn og sameina núverandi lag og sérsniðna lagið til að búa til IFRS-prófjöfnuð.

| Lykill nr. | lýsing              | Lögboðin bók\-Núverandi lag\-JE\-100\-Dr \(Cr\) | Lögboðin bók\-Núverandi lag\-JE\-110\-Dr \(Cr\) | Lögboðin bók\-Núverandi lag\-JE\-120\-Dr \(Cr\) | Núverandi lag \- Samtals | - | Bakfærslubók\-Sérsniðið lag\-JE\-130\-Dr \(Cr\) | IFRS 16 bók\-Sérsniðið lag\-JE\-140\-Dr \(Cr\) | IFRS 16 bók\-Sérsniðið lag\-JE\-150\-Dr \(Cr\) | IFRS 16 bók\-Sérsniðið lag\-JE\-160\-Dr \(Cr\) | IFRS 16 bók\-Sérsniðið lag\-JE\-170\-Dr \(Cr\) | Sérsniðið lag \+ Núgildandi lag \- Samtals |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Leigukostnaður            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1.000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Bankaþóknun                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | VSK útgjöld              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Millireikningur         | \-1.000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1.000                                           |                                                | \-1.000                                        |                                                |                                                | 0\.00                                   |
| 5          | Viðskiptaskuldir         |                                                   | \-1.008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | Afnotaréttur af eign                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Skylda fjármögnunarleigusamnings |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22.794                                       | 1.000                                          | \-94\.97                                       |                                                | \-21.888\.87                            |
| 8          | Vaxtakostnaður         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Innlausn                     |                                                   |                                                   | \-1.008\.00                                       | \-1.008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1.008\.00                             |
| 10         | Afskriftakostnaður     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Uppsöfnuð afskrift |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
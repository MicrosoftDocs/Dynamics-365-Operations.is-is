---
title: Draga úr afnotarétti af eignum
description: Þessi grein virkninni sem skráir virðisrýrnun og leiðréttir afskriftaráætlun eigna fyrir efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) rekstrarleigusamninga.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f953b3a351859c6becba10a129bbb17b49be6290
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894114"
---
# <a name="impair-right-of-use-assets"></a>Draga úr afnotarétti af eignum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þegar bókfært verð afnotaréttar af eign er ekki endurheimtanlegt verður hugsanlega að prófa hvort virðisrýrnun verði á eigninni. Þegar ákvarðað er að virðisrýrnun verði á eigninni getur eignarleiga skráð virðisrýrnun og leiðrétt afskriftaráætlunina samkvæmt því. Þessi grein lýsir virkninni sem skráir virðisrýrnun og leiðréttir afskriftaráætlun fyrir efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) rekstrarleigusamninga. Sama aðferð gildir einnig fyrir leigusamning samkvæmt alþjóðlegum reikningsskilastaðli 16 (IFRS 16).

Eftirstöðvar afnotaréttar af eign verða afskrifaðar á samkvæmt línulegri aðferð fyrir fjölda tímabila sem eftir eru, óháð því hvort leigusamningurinn var flokkaður sem fjármögnunarleigusamningur samkvæmt IFRS 16 eða rekstrarleigusamningur samkvæmt ASC 842.

## <a name="impair-an-rou-asset"></a>Virðisrýrnun afnotaréttar af eign

1. Opnið leigusamninginn með virðisrýrnun og veljið **Bækur**.
2. Veldu **Virðisrýrnun** á aðgerðasvæðinu.
3. Í svarglugganum sem birtist, í reitnum **Upphæð virðisrýrnunar** skal færa inn upphæð virðisrýrnunar eignarinnar. Sláðu inn jákvætt gildi ef draga á úr afnotarétti af eign.
4. Færið inn dagsetninguna þegar bóka á virðisrýrnunarfærsluna í reitnum **Færsludagsetning**.
5. Í svæðið **Tímabil sem eftir eru** skal færa inn eftirstandandi fjölda mánaða til afskrifta.
6. Veljið valkostinn **Forskoða** til að skoða tillögu um eignastöðu og fjárhagsfærslu áður en þær eru búnar til eða birtar.
7. Stillið valkostinn **Loka bók** á **Já** til að loka leigubókinni. Þú getur afturkallað þessa aðgerð með því að nota **Enduropna losunarstöðu**. Ekki er hægt að bóka færslur á lokaða leigusamninga og ekki er unnt að breyta lokuðum leigusamningum. 
8. Veljið **Bóka** til að stofna eða bóka virðisrýrnunarfærsluna.

    > [!NOTE]
    > Eftir að færslan um virðisrýrnun er bókuð er stofnuð ný bókaútgáfa.

    > Ef leiga er flokkaður sem rekstrarleiga verða mánaðarlegar afskriftir eftir skerðingu reiknaðar með línulegum afskriftum.

9. Til að skoða virðisrýrnun afskriftaráætlunar eignar skal opna afskriftaráætlun eigna fyrir viðkomandi leigubók. Eignin verður nú afskrifuð samkvæmt línulegri aðferð á mánaðarfjöld sem þú slóst inn í svæðið **Tímabil sem eru eftir**.
10. Til að skoða bókarfærslu kostnaðar virðisrýrnunar skal velja **Færslubók eignarleigu** á aðgerðasvæðinu í leigubók virðisrýrnunarinnar. Kerfið stofnar bókarfærslu sem debetfærir bókunarlykil virðisrýrnunarkostnaðar og kreditfærir bókunarlykil leigueignarinnar. 
11. Til að skoða nýtt bókfært virði afnotaréttar af eign skal velja **Eignarfærslur** á aðgerðarsvæði leigubókarinnar.

## <a name="example-of-rou-asset-impairment"></a>Dæmi um virðisrýrnun afnotaréttar af eign

Í þessu dæmi er leigusamningurinn ekki sérhæfð eign sem ekki krefst flutnings á eignarhaldi né veitir leigjanda kost á að kaupa.

### <a name="setup"></a>Setja upp

Eftirfarandi töflur sýna gildin sem eru stillt á flipunum **Almennt** og **Greiðsluáætlunarlínur** fyrir leigusamninginn sem er notaður í þessu dæmi.

**Almennt**

| Svæði                      | Virði            |
|----------------------------|------------------|
| Gangvirði eignarinnar    | 600,000          |
| Vextir á nýju lánsfé | 7%               |
| Samsett tímabil       | Árlega         |
| Nýtingartími eignar (mánuðir) | 600              |
| Tegund afborgunar               | Venjulegar afborganir |
| Upphafsdagsetning          | 01/01/2019       |

**Flipi greiðsluáætlunarlína**

| Svæði             | Virði      |
|-------------------|------------|
| Upphafsdagsetning        | 1/1/2019   |
| Tímabil   | Mánaðarlega    |
| Tímabil           | 120        |
| Lokadagsetning          | 31/12/2028 |
| Greiðslutíðni | Árlega   |
| Upphæð greiðslu    | 10,000     |

### <a name="steps"></a>Skref

1. Þegar lokið er við að stofna leigusamninginn eins og lýst er fyrr í þessari grein er leigubókin opnuð og greiðsluáætlunin staðfest. Bókið síðan upphaflegu skráninguna í færslubókina. Upphaflegur afnotaréttur af eign og leiguskuldbinding ættu að vera 70.235,81 USD. Í þessu dæmi var leigusamningurinn flokkaður sem rekstrarleiga samkvæmt ASC 842.
2. Keyrið runubókarferlið þrisvar sinnum til að herma eftir framrás þriggja ára vegna leigugreiðslna, vaxtakostnaðar og afskriftarkostnaðar.
3. Þegar keyrslu allra þriggja runuvinnslanna er lokið skal opna leigubókina að nýju og opna síðan töflur skulda og eignarfærslna til að skoða núverandi bókfært virði afnotaréttar af eign og leiguskuldbindingar. Eftir þrjú ár ætti virði skuldarinnar að vera um -53.893,00 USD og virði eignarinnar að vera u.þ.b. 53.893,00 USD. 

    Eftir þrjú ár gerir fyrirtækið prófanir á virðisrýrnun og kemst að þeirri niðurstöðu að virðisrýrnun afnotaréttar af eign sé 35.000 USD. Nú verður þú að skrá þessa virðisrýrnun.
    
4. Opnaðu leigubókina og veldu síðan **Virðisrýrnun** á aðgerðasvæðinu.
5. Færa skal inn eftirfarandi upplýsingar á síðunni **Færibreyta virðisrýrnunar**.

    | Svæði                  | Virði    |
    |------------------------|----------|
    | Upphæð virðisrýrnunar      | 35,000   |
    | Færsludagsetning       | 1/1/2022 |
    | Eftirstandandi tímabil      | 84       |
    | Bóka                   | Já      |
    | Forskoða fyrir bókun | Nei       |
    | Loka bók             | Nei       |

6. Bókarfærsla virðisrýrnunar hefur verið stofnuð og bókuð. Til að skoða hana skal opna leigubók eignarinnar í leigubókinni. Athugaðu að upphæð virðisrýrnunarinnar var debetfærð á bókunarlykil fyrir virðisrýrnun kostnaðar og kreditfærð á bókunarlykil afnotaréttar af eign.

7. Hægt er að skoða heildaráhrif virðisrýrnunarinnar í töflum skulda og eignafærslna. Taktu eftir að kostnaður virðisrýrnunar hefur lækkað fyrir afnotaréttinn af eign en bókfært virði leiguskuldbindingarinnar hefur ekki breyst.

Virðisrýrnunin hefur ein áhrif til viðbótar sem þú ættir að hafa í huga. Vegna þess að upphæð afnotaréttar af eign er nú mun lægri en leiguskuldbindingin verður að afskrifa upphæðina á annan hátt en áður. Nánar tiltekið, nú er eignin afskrifuð með línulegri aðferð í eftirstandandi 84 mánuði leigutímans, sem hefst á færsludagsetningunni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

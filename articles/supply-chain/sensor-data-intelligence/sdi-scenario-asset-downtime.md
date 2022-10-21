---
title: Aðstæður fyrir niðurtíma eignar
description: Þessi grein lýsir atburðarás eigna í miðbæ, sem gerir þér kleift að nota skynjaragögn til að fylgjast með framboði eigna þinna.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689430"
---
# <a name="the-asset-downtime-scenario"></a>Aðstæður fyrir niðurtíma eignar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Atburðarás eigna niðritímans myndar færslu um viðhaldsniðurtíma ef ekkert merki er móttekið frá vél innan skilgreinds tímaþröskulds frá því að síðasta merki var móttekið. Atburðarásin krefst þess að þú setjir vélina þína með skynjara sem sendir reglulega merki til Azure IoT Hub þíns meðan vélin er í gangi, en sendir ekki merki þegar vélin er ekki í gangi.

## <a name="set-up-the-asset-downtime-scenario"></a>Settu upp atburðarás eigna í miðbæ

Fylgdu þessum skrefum til að setja upp *niðurtími eigna* atburðarás í Supply Chain Management.

1. Fara til **Eignastýring \> Uppsetning \> Sensor Data Intelligence \> Sviðsmyndir** að opna **Sviðsmyndir** síðu.
2. Í **Niðurtími eigna** atburðarás kassi, veldu **Stilla** til að opna uppsetningarhjálpina fyrir þessa atburðarás.
3. Á **Skynjarar** síðu, veldu **Nýtt** til að bæta skynjara við ristina. Stilltu síðan eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn auðkenni skynjarans sem þú ert að nota. (Ef þú ert að nota Raspberry PI Azure IoT Online Simulator og hefur sett hann upp eins og lýst er í [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md), koma inn *AssetDownTime* .)
    - **Lýsing á skynjara** – Sláðu inn lýsingu á skynjaranum.

4. Endurtaktu fyrra skref fyrir hvern viðbótarskynjara sem þú vilt bæta við núna. Þú getur komið aftur og bætt við fleiri skynjurum hvenær sem er.
5. Veljið **Næst**.
6. Á **Kortlagning viðskiptaskráa** síðu, í **Skynjarar** kafla, veldu skrána fyrir einn af skynjurunum sem þú varst að bæta við.
7. Í **Kortlagning viðskiptaskráa** kafla, veldu **Nýtt** til að bæta línu við ristina.
8. Á nýju röðinni skaltu stilla **Viðskiptaskrá** reitnum við auðlindina sem þú notar valinn skynjara til að fylgjast með. (Ef þú ert að nota kynningargögnin skaltu velja *AK-101, lofthnífur fyrir línu 1* .)
9. Veljið **Næst**.
10. Á **þröskuldur niðurtíma eigna** síðu, tilgreindu hversu lengi eftir síðasta merkið kerfið ætti að bíða áður en það sendir tilkynningu um niðurtíma eigna. Það eru tvær leiðir til að skilgreina þröskuldinn:

    - **Sjálfgefinn þröskuldur (mínútur)** – Stilltu þennan reit til að skilgreina sjálfgefna þröskuldinn. Þetta gildi á við um allar auðlindir þar sem **Tilkynningaþröskuldur (mínútur)** reiturinn er stilltur á tvær mínútur eða minna. Lágmarksgildið er *2* (mínútur).
    - **Þröskuldur til að ákvarða vél svarar ekki (mínútur)** – Fyrir hverja tilföng í hnitanetinu þar sem þú vilt ekki nota sjálfgefna þröskuldinn skaltu slá inn hnekkjagildi í þessum reit. Tilföng sem eru stillt á að nota þröskuld upp á tvær mínútur eða minna munu nota **Sjálfgefinn þröskuldur (mínútur)** stilling í staðinn.
11. Veljið **Næst**.
12. Á **Virkjaðu skynjara** síðu, í hnitanetinu, veldu skynjarann sem þú setur upp og veldu síðan **Virkjaðu**. Fyrir hvern virkan skynjara í ristinni birtist gátmerki í **Virkur** dálki.
13. Veljið **Ljúka**.

## <a name="work-with-the-asset-downtime-scenario"></a>Vinna með atburðarás eigna

Ef ekkert skynjaramerki er móttekið frá eign innan viðmiðunarmarksins sem skilgreint er í sviðsmyndastillingunni mun kerfið búa til niðurtímaskrá viðhalds fyrir þá eign. Stjórnendur ættu að endurskoða niðurtímaskrárnar reglulega (til dæmis einu sinni á hverri vinnuvakt) og nota viðeigandi ástæðukóða og lokatíma fyrir hverja niðurtímaskráningu. Fylgdu þessum skrefum til að skoða viðhaldsniðurtímaskrár fyrir eign:

1. Fara til **Eignastýring > Eignir > Allar eignir**.
2. Finndu og veldu eignina sem þú vilt skoða. (Ef þú ert að nota kynningargögnin skaltu velja *AK-101* .)
3. Á aðgerðarrúðunni, opnaðu **Eign** flipa og, frá **Vinnupöntun** hópur, veldu **Niðurtími viðhalds** til að opna síðuna fyrir viðhaldsniðurtímaskrár fyrir valda eign.

---
title: Aðstæður fyrir niðurtíma eignar
description: Þessi grein lýsir aðstæðum fyrir niðurtíma eignar, sem gerir þér kleift að nota skynjaragögn til að fylgjast með stöðu eignanna þinna.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689430"
---
# <a name="the-asset-downtime-scenario"></a>Aðstæður fyrir niðurtíma eignar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Aðstæður fyrir niðurtíma eignar búa til færslu fyrir niðurtíma vegna viðhalds ef ekkert merki er móttekið frá vél innan skilgreindra tímamarka frá því að síðasta merkið var móttekið. Aðstæðurnar krefjast þess að þú tengir vélina við skynjara sem sendir merki með reglulegu millibili á Azure IoT Hub á meðan vélin er í gangi, en sendir ekki merki þegar vélin er ekki í gangi.

## <a name="set-up-the-asset-downtime-scenario"></a>Setja upp aðstæður fyrir niðurtíma eignar

Fylgdu þessum skrefum til að setja upp aðstæður fyrir *niðurtíma eignar* í Supply Chain Management.

1. Farðu í **Eignastýring \> Uppsetning \> Sensor Data Intelligence \> Aðstæður** til að opna síðuna **Aðstæður**.
2. Í aðstæðureitnum **Niðurtími eignar** skal velja **Skilgreina** til að opna uppsetningarleiðsögnina fyrir þessar aðstæður.
3. Á síðunni **Skynjarar** skal velja **Nýtt** til að bæta skynjara við hnitanetið. Stillið svo eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn kenni skynjarans sem þú ert að nota. (Ef þú notar Raspberry PI Azure IoT Online Simulator og hefur sett það upp eins og lýst er í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md), sláðu inn *AssetDownTime*.)
    - **Lýsing á skynjara** – Færið inn lýsingu á skynjari.

4. Endurtaka á fyrra skref fyrir hvern skynjara sem þú vilt bæta við. Hægt er að koma aftur og bæta við fleiri skynjurum hvenær sem er.
5. Veljið **Næst**.
6. Á síðunni **Vörpun viðskiptafærslu**, í hlutanum **Skynjarar**, skaltu velja færslu fyrir einn af skynjurunum sem þú varst að bæta við.
7. Í hlutanum **Vörpun viðskiptafærslu** skal velja **Ný** til að bæta línu við hnitanetið.
8. Á nýju línunni, stilltu reitinn **Viðskiptafærsla** á tilfangið sem þú notar valinn skynjara til að fylgjast með. (Ef þú notar sýnigögn skaltu velja *AK-101, Lofthnífur fyrir línu 1*.)
9. Veljið **Næst**.
10. Á síðunni **niðurtímamörk eignar** skaltu skilgreina hversu lengi kerfið á að bíða eftir síðasta merkið áður en það sendir tilkynningu um niðurtíma eignar. Tvær leiðir eru til að skilgreina þröskuldinn:

    - **Sjálfgefinn þröskuldur (mínútur)** – Stilltu þennan reit til að skilgreina sjálfgefinn þröskuld. Þetta gildi á við um öll tilföng þar sem reiturinn **Þröskuldur tilkynningar (mínútur)** er stilltur á tvær mínútur eða minna. Lágmarksgildi er *2* (mínútur).
    - **Þröskuldur til að ákvarða að vél bregðist ekki við (mínútur)** – Fyrir hvert tilfang í hnitanetinu þar sem ekki á að nota sjálfgefinn þröskuld skal færa inn hnekkingargildi í þennan reit. Tilföng sem eru stillt á að nota þröskuld sem er tvær mínútur eða styttri munu nota stillinguna **Sjálfgefinn þröskuldur (mínútur)** í staðinn.
11. Veljið **Næst**.
12. Á síðunni **Virkja skynjara**, í hnitanetinu, veldu skynjarann sem þú settir upp og veldu síðan **Virkja**. Fyrir hvern virkan skynjara í hnitanetinu birtist gátmerki í dálkinum **Virkur**.
13. Veljið **Ljúka**.

## <a name="work-with-the-asset-downtime-scenario"></a>Vinna með aðstæður fyrir niðurtíma eigna

Ef ekkert skynjaramerki berst frá eign innan þröskuldsins sem skilgreindur er í sviðsmyndastillingunni, mun kerfið búa til skráningu niðurtíma vegna viðhalds fyrir þessa eign. Stjórnendur ættu að fara reglulega yfir færslur niðurtíma (til dæmis einu sinni á hverri vinnuvakt) og nota viðeigandi ástæðukóða og lokatíma fyrir hverja niðurtímaskráningu. Fylgið eftirfarandi leiðbeiningum til að skoða færslu niðurtíma vegna viðhalds fyrir eign:

1. Farðu í **Eignastýring > Eignir > Allar eignir**.
2. Finndu og veldu eignina sem þú vilt skoða. (Ef þú notar sýningargögnin skaltu velja *AK-101*.)
3. Á aðgerðasvæðinu skal opna flipann **Eign** og í hópnum **Verkbeiðni** skal velja **Niðurtími vegna viðhalds** til að opna síðuna fyrir niðurtímafærslur vegna viðhalds fyrir völdu eignina.

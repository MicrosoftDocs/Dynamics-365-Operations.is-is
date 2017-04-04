---
title: "Kostnaðarhlutir"
description: "Þetta grein veitir upplýsingar um kostnaðarhlutum og útskýrir hvernig kostnaði og magni eru uppsafnað. Kostnaðarhlutar er einingar sem kostnaður og magn er safnað upp fyrir. Eining kostnaðarhlutar geta verið annað hvort afurðarafbrigði eða afurð, eins og afbrigði stíls og litar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8043c81057b5bb79f405642b199f80fc2fbcd8d4
ms.lasthandoff: 03/31/2017


---

# <a name="cost-objects"></a>Kostnaðarhlutir

Þetta grein veitir upplýsingar um kostnaðarhlutum og útskýrir hvernig kostnaði og magni eru uppsafnað. Kostnaðarhlutar er einingar sem kostnaður og magn er safnað upp fyrir. Eining kostnaðarhlutar geta verið annað hvort afurðarafbrigði eða afurð, eins og afbrigði stíls og litar.  

<a name="cost-objects"></a>Kostnaðarhlutir
------------

Síðan **Kostnaðarhlutir** inniheldur lista yfir alla kostnaðarhluti sem eru skráðir á afurð. Kostnaðarhlutir eru skilgreindir með gögnum úr eftirfarandi upprunum:

-   Vara
-   Afurðavíddaflokkur
-   Geymsluvíddarflokkur
-   Rakningarvíddarflokkur

**Ábending:** Kostnaðarhlutur stendur fyrir aðeins fyrir kostnaðareiningu af gerðinni **Bein efni**. Kostnaðarhlutur og birgðahlutur eru ólíkir á þann hátt að kostnaður hlutar er skilgreindur með birgðavíddum sem eru valdar fyrir fjárhagslegar birgðar. Til dæmis, hefur vara eftirfarandi skilgreiningu:

-   **Svæði:** Efnislegar birgðir = Já, Fjárhagslegar birgðir = Já
-   **Vöruhús:** Efnislegar birgðir = Já, Fjárhagslegar birgðir = Nei
-   **Rununr.:** Efnislegar birgðir = Já, Fjárhagslegar birgðir = Nei

Eftirfarandi tafla sýnir hvað er kostnaðarhlutur og hvað birgðahlutur.

| Gerð hlutar      | Vörunúmer | Svæði | Vöruhús | Rununr. |
|------------------|-------------|------|-----------|-----------|
| Kostnaðarhlutur      | x           | x    |           |           |
| Birgðahlutur | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Uppsöfnun á kostnaði og magni
-   Gildið í reitnum **Gildi** er samtala eftirfarandi gilda:
    -   Efnisleg kostnaðarupphæð
    -   Fjárhagsleg kostnaðarupphæð
    -   Leiðréttingar
-   Gildið í reitnum **Magn** er samtala eftirfarandi gilda:
    -   Móttekið
    -   Frádregið
    -   Bókað magn
-   Reiturinn **Meðaleiningarkostnaður** er reiknaður reitur. Gildið er reiknað með því að deila gildinu **Gildi** með gildinu **Magn**.

**Athugasemd:** á ** Taka efnislegt virði ** færibreyta hefur engin áhrif á fyrri útreikningi.

<a name="see-also"></a>Sjá einnig
--------

[Product dimension group](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Storage dimension group](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Tracking dimension group](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Hvað er nýtt eða breytt í Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[Cost entries](cost-entries.md)



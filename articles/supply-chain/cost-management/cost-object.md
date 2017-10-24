---
title: "Kostnaðarhlutir"
description: "Þetta grein veitir upplýsingar um kostnaðarhlutum og útskýrir hvernig kostnaði og magni eru uppsafnað. Kostnaðarhlutar er einingar sem kostnaður og magn er safnað upp fyrir. Eining kostnaðarhlutar geta verið annað hvort afurðarafbrigði eða afurð, eins og afbrigði stíls og litar."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 2549ace837fcdfb9f927e6b486b6a94566bcbbd2
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="cost-objects"></a>Kostnaðarhlutir

[!include[banner](../includes/banner.md)]


Þetta grein veitir upplýsingar um kostnaðarhlutum og útskýrir hvernig kostnaði og magni eru uppsafnað. Kostnaðarhlutar er einingar sem kostnaður og magn er safnað upp fyrir. Eining kostnaðarhlutar geta verið annað hvort afurðarafbrigði eða afurð, eins og afbrigði stíls og litar.  

## <a name="cost-objects"></a>Kostnaðarhlutir

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

**Ábending:** Færibreytan **Taka efnislegt virði með** hefur engin áhrif á fyrri útreikninga.

<a name="see-also"></a>Sjá einnig
--------

[Afurðavíddaflokkur](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Geymsluvíddarflokkur](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Rakningarvíddarflokkur](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Nýjungar eða breytingar](../../fin-and-ops/get-started/whats-new-changed.md)

[Kostnaðarfærslur](cost-entries.md)





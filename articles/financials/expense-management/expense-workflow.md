---
title: "Verkflæði kostnaðar"
description: "Í þessu efnisatriði er útskýrt hvernig hægt er að nota verkflæðiskerfi í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til að setja upp og fara yfir ferli við kostnaðarskýrslur í Kostnaðarstýring."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d60d2f462a1fd27d4655e68aab7f96fb28a34b77
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="expense-workflow"></a>Verkflæði kostnaðar

[!include[banner](../includes/banner.md)]

Hægt er að nota verkflæðiskerfi í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til að setja upp og fara yfir ferli við kostnaðarskýrslur í Kostnaðarstýring. Hægt er að setja upp verkflæði sem notar eftirfarandi viðmiðanir til að ákvarða hver samþykkir kostnaðarskýrslur:

- Starfsmaðurinn sem sér um stigveldi og fyrirfram skilgreind samþykkistakmörk
- Marglaga samþykki sem styður millisamþykktaraðila og lokasamþykktaraðila
- Fjárhagsvíddir ábyrgð verka
- Úthlutanir á tiltekna notendur og notendaflokka

Hægt er að stofna verkflæðissamþykki fyrir kostnaðarskýrslur, ferðabeiðnir, fyrirframgreiðslur og endurgreiðslu virðisaukaskatts.

**Dæmi**

Eftirfarandi ferli er dæmi um verkflæðisferli kostnaðarstýringar fyrir kostnaðarskýrslu.

1. Starfsmaður stofnar og vistar kostnaðarskýrslu.
2. Starfsmaðurinn sendir kostnaðarskýrslu til samþykktar. Samþykktaraðili er auðkenndur á grundvelli reglna sem voru skilgreindar þegar verkflæðið var sett upp.
3. Samþykktaraðili fær tilkynningu um að kostnaðarskýrsla sé tilbúin til samþykktar. Samþykktaraðili fer yfir kostnaðarskýrsluna og staðfestir að eftirfarandi skilyrði séu uppfyllt:

    - Kostnaðurinn brýtur ekki í bága við kostnaðarreglur. Ef kostnaður brýtur gegn reglu staðfestir samþykktaraðilinn að kostnaðarskýrslan innihalda gilda réttlætingu viðskipta.
    - Rafrænar kvittanir fylgja með kostnaðarskýrslu.

4. Samþykktaraðili samþykkir kostnaðarskýrsluna.
5. Kostnaðarskýrslan er úthlutuð á gjaldkera til bókunar.
6. Eitt af eftirfarandi skrefum á sér stað, eftir því hvort sjálfvirk bókun sé stillt:

    - Ef sjálfvirk bókun er stillt er kostnaðarskýrslan meðhöndluð til greiðslu og staða kostnaðarskýrslunnar er uppfærð.
    - Ef sjálfvirk bókun er ekki stillt staðfestir gjaldkeri að allar upprunalega kvittanir hafi verið sendar og að kvittanir séu í samræmi við kostnaðinn á kostnaðarskýrslunni. Allir skattkóðar sem eru færðar á kostnaðarskýrsluna verða einnig að vera staðfestir sem réttar.

Þegar þessar kröfur eru uppfylltar er kostnaðarskýrslan bókuð.

Eftir að kostnaðarskýrslan er bókuð er greiðsla heimiluð fyrir kostnaðarskýrsluna og starfsmaðurinn fær endurgreiðslu.


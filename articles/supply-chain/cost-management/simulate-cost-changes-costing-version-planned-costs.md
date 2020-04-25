---
title: Herma kostnaðarbreytingu með útgáfu kostnaðarútreiknings fyrir áætlaðan kostnað
description: Þessi grein útskýrir hvernig er hægt að herma eftir áhrifum kostnaðarbreytinga á útreiknaðan kostnað framleiddrar vöru með sérstakri kostnaðarútgáfu fyrir áætlaðan kostnað.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6e1d52f48a6b7675fb16ccc5ecd9ba7cd25ac8b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214459"
---
# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Herma kostnaðarbreytingu með útgáfu kostnaðarútreiknings fyrir áætlaðan kostnað

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig er hægt að herma eftir áhrifum kostnaðarbreytinga á útreiknaðan kostnað framleiddrar vöru með sérstakri kostnaðarútgáfu fyrir áætlaðan kostnað.

Hægt er að herma eftir áhrifum kostnaðarbreytinga á útreiknaðan kostnað framleiddrar vöru með sérstakri útgáfu af kostnaðarútreikningi fyrir áætlaðan kostnað. Notið þessa aðskildu útgáfu kostnaðarútreikningsins til að færa inn biðkostnaðarfærslur sem endurspegla stigvaxandi kostnaðarbreytingar og til að reikna út kostnaðaráhrif á framleiddar vörur. Þar sem varaúrræði virks kostnaðar er notaður í uppskriftarútreikningunum þarf einungis að færa stigvaxandi kostnaðarbreytingarnar inn.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Leiðbeiningar við skilgreiningu á hermdri kostnaðarútgáfu.
Notið eftirfarandi leiðbeiningar við skilgreiningu á hermdri kostnaðarútgáfu.

-   Úthlutið kostnaðargerð **áætlaðs kostnaðar**.
-   Úthlutið kostnaðarútgáfunni auðskiljanlegt auðkenni, til dæmis **hermun**.
-   Tryggja þarf að kostnaðarfærslur séu teknar með.
-   Leyfið færslur kostnaðar. Lokið ekki á færslu kostnaðar í bið.
-   Að leyfa kostnaðarfærslur fyrir öll svæði. Ef svæði er úthlutað takmarkast kostnaðarfærslur við það svæði.
-   Komið í veg fyrir að biðkostnaður verði virkur. Aðeins þarf að færa inn biðkostnað fyrir kostnaðarfærslur í hermdri kostnaðarútgáfu.
-   Ekki færa inn upphafsdagsetningu. Útreikningsdagsetning verður færð inn fyrir hvern uppskriftarútreikning sem notar hermda kostnaðarútgáfu.
-   Gefið til kynna að varaúrræðið sé **nú í gildi**. Varaúrræðið leyfir færslu stigvaxandi kostnaðarbreytinga fyrir hermun en notar hinsvegar núverandi virkan kostnað sem uppruna allra annarra kostnaðarfærslna. Við gerum ráð fyrir því að allur virkur kostnaður sé til fyrir allar aðrar kostnaðarfærslur.
-   Gefið til kynna kostnaðarverðslíkan af **kostnaðarverði útgáfu** en ekki takmarka útreikninga. Til dæmis getur hermun líka notast við kostnaðarverðslíkan **útreikningsflokks uppskriftar** til að gefa til kynna uppruna gagna kostnaðarframlegðar fyrir keyptar vörur.
-   Gefið til kynna **margstiga** niðurbrotsham en ekki takmarka útreikninga. Hermun getur notað aðra niðurbrotshami.

## <a name="costing-versions"></a>Kostnaðarútgáfa
Eftirfarandi dæmi sýna notkun hermdra kostnaðarútgáfa til að herma eftir áhrifum kostnaðarbreytinga. Áður en hermd kostnaðarbreyting er færð inn þarf að eyða kostnaðarfærslum í biðstöðu í hermdri kostnaðarútgáfu, til að byrjað sé frá grunni. Notið skjámyndina **vöruverð** til að skoða og eyða biðkostnaðarfærslum sem eru tengdar vöruverðum og verðum kostnaðartegunda.

-   Herma eftir kostnaðarbreytingu á keyptri vöru. Til dæmis gæti kostnaðarbreytingin endurspeglað kostnaðaraukningu eða -lækkun sem búist er við á mikilvægu keyptu efni. Til að skilgreina ólíkan kostnað keyptrar vöru er síðan **vöruverð** notuð til að færa inn biðkostnaðarfærslu í hermdri kostnaðarútgáfu.
-   Herma eftir kostnaðarbreytingu á kostnaðartegund. Til dæmis gæti kostnaðarbreytingin endurspeglað hækkun eða lækkun sem búist er við á launatöxtum eða á tímavinnutöxtum fyrir rekstrartilföng. Til að skilgreina ólíkan kostnað kostnaðartegundar er skjámyndin **verð kostnaðartegundar** notuð til að færa inn biðkostnaðarfærslu í hermdri kostnaðarútgáfu.
-   Herma eftir kostnaðarbreytingu í reikniformúlu óbeins kostnaðar. Til dæmis gæti kostnaðarbreytingin endurspeglað viðbúna hækkun eða lækkun á framleiðslurekstrarkostnaði. Til að skilgreina breytinguna í reikniformúlu óbeins kostnaðar skal nota síðuna **uppsetning kostnaðarskjals** til að færa inn biðkostnaðarfærslu í hermdri kostnaðarútgáfu og til að villuleita og vista breytinguna.

Eftir að hermdu kostnaðarbreytingarnar hafa verið færðar inn skal reikna út kostnað þeirra framleiddu vara sem verða fyrir mestum áhrifum af kostnaðarbreytingunum. Notið síðuna **Útreikningur** fyrir hermda kostnaðarútgáfu og tilgreinið þær völdu framleiddu vörur sem verða fyrir áhrifum af kostnaðarbreytingunum. Uppskriftarútreikningarnir eiga við um allar framleiddar vörur nema tilteknar vörur séu valdar. Einnig er hægt að nota valkost uppskriftarútreiknings fyrir uppfærslur „þar sem er notað“. Skoðið kostnaðarfærslur vara í hermdri kostnaðarútgáfu til að greina hvernig hermdar kostnaðarbreytingar höfðu áhrif á kostnað valdra framleiddra vara. Nota skal **vöruverð** síðu og **Reikna vörukostnað** síðu til að skoða og greina kostnaðinn.




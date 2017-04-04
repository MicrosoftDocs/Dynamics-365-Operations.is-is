---
title: "Brot á endurskoðun og tilvik"
description: "Þessi grein útskýrir hvernig endurskoðunarmál eru stofnuð vegna brota á reglum endurskoðunarstefnu Þetta felur einnig í sér upplýsingar um mismunandi leiðir sem endurskoðunarstefnur nota dagsetningabil skjalavals."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 77f72c9414f1fad720055e58e3f704b9c713072f
ms.lasthandoff: 03/31/2017


---

# <a name="audit-policy-violations-and-cases"></a>Brot á endurskoðun og tilvik

Þessi grein útskýrir hvernig endurskoðunarmál eru stofnuð vegna brota á reglum endurskoðunarstefnu Þetta felur einnig í sér upplýsingar um mismunandi leiðir sem endurskoðunarstefnur nota dagsetningabil skjalavals.

<a name="how-audit-cases-are-generated"></a>Hvernig endurskoðunarmál eru stofnuð
-----------------------------

Endurskoðunarstefnur eru notaðar til að auðkenna kostnaðarskýrslur, innkaupapantanir og reikninga lánardrottna sem ekki samræmast viðskiptareglum sem þú tilgreinir og skilgreina sem reglur endurskoðunarstefnu. 

Endurskoðunarreglur eru keyrðar í runuham. Þegar endurskoðunarregla er keyrð eru allar stefnureglur sem eru hluti þeirrar reglu keyrðar á sama tíma.

Hver stefnuregla metur safn skjala. Stefnureglan velur skjöl sem eru í dagsetningabili skjalavals og sem samsvara tilgreindum skilyrðum. Til dæmis gæti ein stefnuregla valið kostnaðarskýrslur sem hafa máltíðir sem fara fram yfir 50,00. Önnur stefnuregla gæti valið reikninga lánardrottna sem eru til greiðslu til tiltekins lánardrottins. Fyrir hvert skjal sem er valið í safninu er brot myndað. Það brot er færsla um að tiltekið skjal, eins og reikningur 12345, samræmist ekki stefnureglunni. 

Margar endurskoðunarfærslur eru flokkaðar saman og tengdar endurskoðunarmálum. Að sjálfgefnu eru mál fyrir hverja endurskoðunarreglu flokkuð eftir reglu endurskoðunarstefnu. Ef þess er óskað er hægt að velja önnur flokkunarskilyrði með því að nota síðuna **Flokkunarskilyrði tilvika**. Til dæmis er hægt að flokka kostnaðarhausa með Kenni og lánardrottinn verkreikninga með lánardrottnalykil. Í þessu tilfelli eru allar kostnaðarskýrslu haus brota sem hafa sama Verkkenni verða flokkaðar í sama og allir reikningar lánardrottins sem hafa sama lánardrottnalykil verða flokkaðar í sama. 

> [!NOTE]
> Fyrir reglur endurskoðunarstefnu sem byggja á við **Tvítekin** gerð er fyrirspurn brot ekki eru kostnaðarjafnaðar flokkaðar eftir reglu eða skilyrðin sem eru tilgreind í á **Case flokkunarskilyrði** síðu. Þessi í stað eru þau flokkuð eftir þeim skilyrðum sem eru búin til í reglu endurskoðunarstefnu. Til dæmis, ef stefnureglan metur kostnaðarskýrslur fyrir tvítekinn kostnað upp á sömu upphæð, kenni söluaðila og dagsetningu, verður allur kostnaður sem hefur sama gildi í þessum reitum eitt tilvik. Öll útgjöld sem hafa mismunandi gildi verða aðskilin tilvik.

Þegar endurskoðunarmál hafa verið mynduð eru þau meðhöndluð með því að nota dæmigert ferli málastjórnunar.

## <a name="document-selection-date-ranges"></a>Dagsetningabil skjalavals
Þegar endurskoðunarstefna er keyrð velur hver regla skjöl af þeirri tilgreindu gerð sem hefur dagsetningu sem er í dagsetningabili skjalavals. Dagsetningabil skjalavals er tilgreint á síðunni **Aukavalkostir**. Mörg skjöl hafa fleiri en eina dagsetningu sem tengjast þeim. Dagsetningareiturinn sem regla endurskoðunarstefnu notar er tilgreindur á síðunni **Stefnureglugerð**.

Hér eru nokkrar aðrar leiðir þar sem endurskoðunarreglan notar dagsetningabil skjalavals:

-   Regla notar útgáfu hverrar stefnureglu sem gildir á síðasta degi dagsetningabils skjalavals. Hægt er að skoða virku dagsetningarnar fyrir hverja stefnureglu á listasíðunni **Endurskoðunarstefnur**.
-   Stefnan notar fyrirtækishnúta sem eru tengdir reglunni síðasta daginn í dagsetningabili skjalavals. Aðeins fyrirtækishnútar sem eru tengdir við regluna birtast á listasíðunni **Endurskoðunarstefnur**.
-   Fyrir stefnureglur sem eru byggðar á fyrirspurnargerðinni **Listaleit** metur stefnan skjöl fryir vaktaðar einingar sem eru virkar á síðasta degi dagsetningabils skjalavals.


Nánari upplýsingar, sjá [stefnureglum Endurskoðunar](audit-policy-rules.md)



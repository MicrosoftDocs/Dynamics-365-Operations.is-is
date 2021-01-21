---
title: Líftímastöður afurðar og færslur
description: Þetta efnisatriði útskýrir hvernig skal stjórna hvaða færslur eru leyfðar fyrir hverja líftímastöðu sem hönnunarafurð fer í gegnum á líftíma hennar.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 69ee39479424c1b629388c18e8bfefd023036d22
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430785"
---
# <a name="product-lifecycle-states-and-transactions"></a>Líftímastöður afurðar og færslur

[!include [banner](../includes/banner.md)]

Um leið og hönnunarafurð fer í gegnum líftíma sinn er mikilvægt að geta stjórnað hvaða færslur eru leyfðar fyrir hverja líftímastöðu. Til dæmis ætti ekki að setja óþroskaðar afurðir á sölupöntun. Einnig er hægt að stjórna innflæði umræddrar vöru ef hún nálgast lok líftímastöðu sinnar.

Hvað breytingar á líftímastöðu hönnunarafurðar varða, eru slíkar breytingar tengdar við hönnunarútgáfur afurðarinnar. Þar af leiðandi er einnig hægt að tengja líftímastöðu afurðarinnar við hönnunarútgáfur. Þegar líftímastaða afurðar er tengd við hönnunarútgáfu er hægt að nota líftímastöðu til að hafa eftirlit með því hvaða færslur eru leyfðar fyrir hönnunarútgáfuna.

## <a name="create-and-manage-product-lifecycle-states"></a>Búa til og stjórna líftímastöðu afurðar

Til að vinna með líftímastöðu afurðar er farið í **Umsjón hönnunarbreytinga \> Uppsetning \> Líftímastaða afurðar**. Fylgið svo einu af eftirfarandi skrefum.

- Til að stofna nýja líftímastöðu skal velja **Nýtt** á aðgerðasvæðinu og stilla síðan svæðin eins og lýst er í eftirfarandi undirköflum.
- Til að breyta fyrirliggjandi líftímastöðu skal velja hana á aðgerðarsvæðinu, velja **Breyta** á aðgerðasvæðinu og stilla síðan reitina eins og lýst er í eftirfarandi undirköflum.
- Til að eyða fyrirliggjandi líftímastöðu skal velja hana á aðgerðasvæðinu og velja svo **Eyða** á aðgerðasvæðinu.

> [!NOTE]
> Hönnunarafurðir nota sömu líftímastöður og staðlaðar afurðir (ekki hönnunarafurðir). Einnig er hægt að opna **Líftímastaða afurðar** sem er lýst í þessu efnisatriði með því að opna **Afurðaupplýsingastjórnun \> Uppsetning \> Líftímastaða afurðar**. Frekari upplýsingar um líftímastöður afurðar, bæði fyrir hönnunarafurðir og staðlaðar afurðir, er að finna í [Yfirliti líftímastöðu afurðar](../pim/product-lifecycle.md).

### <a name="header"></a>Haus

Stilltu eftirfarandi svæði á haus líftímastöðu afurðar.

| Svæði | lýsing |
|---|---|
| Ríki | Sláðu inn heiti líftímastöðu afurðarinnar. |
| lýsing | Sláðu inn lýsingu á líftímastöðu afurðarinnar. |

### <a name="general-fasttab"></a>Flýtiflipinn Almennt

Stilltu eftirfarandi svæði á flýtiflipanum **Almennt**.

| Svæði | lýsing |
|---|---|
| Sjálfgefið þegar losað er til lögaðila | Fyrir staðlaðar afurðir skal stilla þennan valkost á *Já* ef þessi líftímastaða skal gilda fyrir allar sjálfgefnar afurðir þegar þær eru fyrst losaðar. Stillið á *Nei* ef þessi líftímastaða verður notuð handvirkt síðar.<p>Þessi stilling á ekki við um hönnunarafurðir. Líftímastaða útgáfu hönnunarafurðar eftir að hún er stofnuð í hönnunarfyrirtækinu er tilgreind í viðkomandi flokki breytinga á hönnun. Þegar afurðin er losuð til rekstrarfyrirtækis er líftímastaða afurðarinnar afrituð. Nánar tiltekið, þegar hönnunarafurð er losuð til rekstrarfyrirtækis hefur hún sömu líftímastöðu og hún hafði í hönnunarfyrirtækinu. Hægt er að skrifa yfir líftímastöðuna í rekstrarfyrirtækinu.</p> |
| Er virk fyrir áætlunargerð | Stillið þennan valkost á *Já* til að taka með afurðir sem hafa þessa líftímastöðu í útreikningum á stigi aðaláætlanagerðar og uppskriftar. Stillið hana á *Nei* til að taka ekki með afurðir sem eru í þessari líftímastöðu í útreikningum. |

### <a name="enabled-business-processes-fasttab"></a>Flýtiflipi virkjaðra viðskiptaferla

Notaðu flýtiflipann **Virkjaðir viðskiptaferlar** til að stjórna hvaða tiltæku viðskiptaferli má nota fyrir afurðir í núverandi líftímastöðu. Ferlin sem eru skráð á þessum flipa finnast sjálfkrafa á eftirfarandi hátt:

- Í fyrsta skipti sem ný líftímastaða er vistuð, hleður síðan viðskiptaferlin sem eru tiltæk sem stendur.
- Þegar nýjum viðskiptaferlum er bætt við kerfið getur þú uppfært listann á flýtiflipanum **Virkjaðir viðskiptaferlar** fyrir núverandi líftímastöðu með því að velja **Leita að uppfærslum** á aðgerðasvæðinu.

Eftirfarandi reitir eru tiltækir fyrir hvert ferli sem er skráð á flýtiflipann **Virkjaðir viðskiptaferlar**.

| Svæði | lýsing |
|---|---|
| Vinna | Þessi skrifvarða svæði sýnir heiti fyrirliggjandi viðskiptaferlis. |
| Úrvinnslusvæði | Þetta skrifvarða svæði sýnir heiti fyrirliggjandi vinnslusvæðis. |
| Tryggingasamningur | Veldu eitt af eftirfarandi gildum til að stjórna hvort og hvernig núverandi ferli verður heimilað fyrir afurðir með eftirfarandi líftímastöðu:<ul><li>**Virkjað** – Viðskiptaferlið er leyft.</li><li>**Lokað** – Ferlið er ekki leyft. Þegar notandi reynir að nota ferlið fyrir afurð með þessa líftímastöðu, stöðvar kerfið slíkt og birtir villu þess í stað. Þú ætlar t.d. að útiloka kaup á afurðum sem eru við lok líftíma.</li><li>**Virkjað með viðvörun** – Ferlið er leyft en viðvörun birtist. Þú vilt t.d. setja frumgerð afurðar á framleiðslupöntun sem er stofnuð af deild rannsóknar- og þróunarsviðsins. Hins vegar ættu aðrar deildir að fá að vita að þær eiga ekki að hefja framleiðslu á afurðinni strax.</li></ul> |

Þegar þú bætir við fleiri reglum um líftímastöðu sem sérstillingar er hægt að skoða þessar reglur í notandaviðmótinu (UI) með því að velja **Uppfæra ferli** á efra svæðinu. Hnappurinn **Uppfæra ferli** er aðeins tiltækur fyrir stjórnendur.
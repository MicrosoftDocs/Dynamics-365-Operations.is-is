---
title: Bókunaraðferðir frestunar
description: Þessi grein lýsir muninum á bókunaraðferð frestunar fyrir tekju- og kostnaðarfrestanir í áskriftargreiðslu.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017475"
---
# <a name="deferral-posting-methods"></a>Bókunaraðferðir frestunar

Þessi grein lýsir muninum á bókunaraðferð frestunar fyrir tekju- og kostnaðarfrestanir í áskriftargreiðslu.

Á síðunni **Færibreytur tekju- og kostnaðarfrestunar** eru valkostir fyrir bókunaraðferðir frestunar **Efnahagsreikningur** og **Hagnaður og tap**. Dæmið í þessari grein mun hjálpa til við að útskýra muninn á þessum tveimur aðferðum og ástæður þess að þú gætir notað aðra aðferðina eða hina.

Aðferðin **Efnahagsreikningur** notar aðeins tvo lykla. Því er minni uppsetning nauðsynleg. Aðferðin **Hagnaður og tap** er með tvo viðbótarlykla, **Upphafleg skráning** og **Mótbókun skráningar** fyrir tekjur, afslætti og kostnað eftir því hver færslugerðin er. Þessir lyklar eru settir upp á síðunni **Sjálfgefnar frestanir** (**Áskriftargreiðsla \> Tekju- og kostnaðarfrestanir \> Uppsetning**). Þótt dæmið sé um frestaðar tekjur er hægt að nota sömu hugmynd fyrir frestaða afslætti og frestaðan kostnað.

## <a name="example"></a>Dæmi

Sölureikningur 1 er með USD 3.000 í heildartekjur og frestaðar tekjur. Eftirfarandi töflur sýna dreifingarnar þegar þessi sölureikningur er bókaður.

**Aðferð efnahagsreiknings**

| Gerð | Lykill | Debet | Kredit|
|---|---|---|---|
| Debet | Viðskiptakröfur | 3,000.00 | |
| Kredit | Frestaðar tekjur | | 3,000.00 |

**Aðferð hagnaðar og taps**

| Gerð | Lykill | Debet | Kredit |
|---|---|---|---|
| Debet | Viðskiptakröfur | 3,000.00 | |
| Debet | Mótbókun tekjuskráningar | 3,000.00 | |
| Kredit | Frestaðar tekjur | | 3,000.00 |
| Kredit | Upphafleg tekjuskráning | | 3,000.00 |

Sölureikningur 2 er með USD 2.000 í heildartekjur og er ekki með frestaðar tekjur.

| Gerð | Lykill | Upphæð |
|---|---|---|
| Debet | Viðskiptakröfur | 3,000.00 |
| Kredit | Tekjur | 3,000.00 |

**Samtölur fyrir sölureikning 1 og 2 samanlagðar í aðferð efnahagsreiknings**

| Lykill | Debet | Kredit |
|---|---|---|
| Viðskiptakröfur | 5,000.00 | |
| Tekjur | | 2,000.00 |
| Frestaðar tekjur | | 3,000.00 |

Þegar aðferðin **Efnahagsreikningur** er notuð er ekki auðvelt að sjá brúttótekjur fyrir tímabil. Hluti teknanna er bókaður á lykilinn **Frestaðar tekjur**. Hafðu í huga að eftir því sem tekjur eru skráðar fyrir hvert tímabil eru margar debet- og kreditfærslur á lyklinum **Frestaðar tekjur**. Brúttótekjum fyrir tiltekið tímabil verður blandað við inn-/útfærslur tekjuskráningar.

**Samtala hagnaðar og taps fyrir sölureikning 1 og 2 samanlagt**

| Lykill | Debet | Kredit |
|---|---|---|
| Viðskiptakröfur | 5,000.00 | |
| Tekjur | | 5,000.00 |
| Tekjujöfnun | 3,000.00 | |
| Frestaðar tekjur | | 3,000.00 |

Allar tekjur fara í **Tekjulykilinn** fyrir hagnað og tap. Þá eru frestaðar tekjur færðar úr rekstraryfirlitinu yfir í efnahagsreikning. Auðvelt er að sjá brúttótekjur því að allt er bókað á lykilinn **Tekjur**. Hins vegar er hluta af þessum brúttótekjum frestað. Hún er því færð á **Frestaðar tekjur** reikninginnfærð síðar.

Í aðferðinni **Hagnaður og tap** er hægt að skoða lykilinn **Tekjur** og lykilinn **Mótbókun tekna** til að sjá brúttótekjur upp á $5.000 og nettótekjur (nettó af frestuðu) upp á $2.000. Þótt aðferðin **Hagnaður og tap** geti gert skýrslugerðina auðveldari þarf að setja upp fleiri lykla.

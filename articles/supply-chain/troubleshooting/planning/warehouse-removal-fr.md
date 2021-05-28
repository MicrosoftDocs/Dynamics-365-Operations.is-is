---
title: Ekki er hægt að fjarlægja vídd eftirspurnarspár vöruhúss úr spárlínum.
description: Ekki er hægt að fjarlægja vídd eftirspurnarspár vöruhúss úr spárlínum.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026612"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Ekki er hægt að fjarlægja vídd eftirspurnarspár vöruhúss úr spárlínum.

KB númer: 4614408

## <a name="symptoms"></a>Einkenni

Þetta vandamál kemur upp þegar víddin **Vöruhús** er ekki úthlutuð á flipanum **Spávíddir** á síðunni **færibreyta Eftirspurnarspár**. Engu að síður er dálkurinn **Vöruhús** sýndur á **Eftirspurnarspá** síðunni (**Aðaláætlanagerð \> Spá \> Handvirk spáeining \> Eftirspurnarspárlínur**).

## <a name="resolution"></a>Upplausn

Stillingarnar á flipanum **Spávíddir** á síðunni **Færibreyta eftirspurnarspár** hafa ekki áhrif á síðuna **Eftirspurnarspá**. Þeir stjórna grunnspánni sem myndast og kemur fram í leiðréttu eftirspurnarspánni. Hins vegar stjórna þeir ekki víddum sem krafist er fyrir „raunverulega“ eftirspurnarspá. Með því að heimila færslurnar sem birtast á síðunni **Leiðrétt eftirspurnarspá** getur þú breytt þeim í „raunverulegar“ spárfærslur fyrir spárlíkan. Það líkan er síðan hægt að nota í aðaláætlanagerð.

Á síðunni **Eftirspurnarspá** eru víddirnar fyrir „raunverulega“ spá sem birtar eru á eftirspurnarspálínunum hluti af birgðavíddum. (Þessi hegðun líkist hegðun sölupöntunarlína.) Ef kerfið er ekki sett upp til að nota **Vöruhús** sem skylduvídd fyrir birgðir er hægt að sérstilla síðuna til að fela dálkinn.

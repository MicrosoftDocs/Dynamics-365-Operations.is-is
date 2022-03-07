---
title: Framleiðslupantanir ekki sýndar á síðunni Merking
description: Sumar framleiðslupantanir eru ekki sýndar á síðunni Merking. Þetta efnisatriði útskýrir afurðarafbrigðin þrjú sem eru ekki tiltæk fyrir merkingu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476606"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Framleiðslupantanir eru ekki sýndar á síðunni Merking

## <a name="symptoms"></a>Einkenni

Þegar unnið er með leynilega framleiðslu eru sumar framleiðslupantanir ekki sýndar á síðunni **Merking**.

## <a name="resolution"></a>Lausn

Ekki er hægt að merkja vörur sem hafa eftirfarandi stillingar. Þess vegna birtast þær ekki á síðunni **Merking**:

- Afurðirnar eru skilgreindar sem afurðir af gerðinni *þyngd afurðar*.
- Þær eru virkjaðar fyrir ítarlegt vöruhúsaferli.
- Þeim er grunnstillt til að stjórna reglunni *Staðalkostnaður*.

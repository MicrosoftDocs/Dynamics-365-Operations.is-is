---
title: Ekki er hægt að hætta við fylgiseðil eftir að hann hefur verið bókaður úr pöntun
description: Þegar tiltektar- og afhendingarferlin eru virkjuð fyrir vöruhúsakerfi er ekki hægt að hætta við fylgiseðil þegar búið er að bóka hann í sölupöntun. Á þessari síðu er boðið upp á hjáleið.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476713"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Ekki er hægt að hætta við fylgiseðil eftir að hann hefur verið bókaður úr sölupöntun

## <a name="symptoms"></a>Einkenni

Þegar tiltektar- og afhendingarferlin eru virkjuð fyrir ítarlegt vöruhúsakerfi er ekki hægt að hætta við fylgiseðil þegar búið er að bóka hann í sölupöntun.

## <a name="resolution"></a>Lausn

Til að leiðrétta bókaða fylgiseðla fyrir vörur sem eru virkar í vöruhúsakerfi þarf bókunin að gerast í hleðslunni, ekki pöntuninni. Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.  

Sölupöntun sem hefur verið tínd og send í gegnum vöruhúsakerfisferla er almennt hægt að uppfæra fylgiseðil fyrir í hleðslunni eða sendingunni og sjálfu sölupöntunarskjalinu. Ef fylgiseðill í sölupöntun er hinsvegar uppfærður úr sölupöntunarskjalinu, verður samt ekki hægt að afturkalla fylgiseðil úr hleðslunni eða sölupöntuninni. Þess vegna er mælt með því að bókun fylgiseðilsins sé notuð úr hleðslunni. Í þessu tilfellum er bakfærslan sem verður að vera gerð úr hleðslunni gerð virk.

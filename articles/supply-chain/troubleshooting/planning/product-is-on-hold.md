---
title: Afurð er í bið fyrir færslur
description: Þegar áætlaðar pantanir eru festar koma upp villuboð sem gefa til kynna að vara er í bið fyrir færslur.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752611"
---
# <a name="product-is-on-hold-for-transactions"></a>Afurð er í bið fyrir færslur

Villukóði SYS13295

## <a name="symptoms"></a>Einkenni

Þegar áætlaðar pantanir eru festar koma upp eftirfarandi villuboð:

> Varan %1 er lokuð vegna færslna í %2.

## <a name="cause"></a>Orsök

Þegar útilokuðum vörum er lýst notar kerfið hugtökin *útilokað*, *stöðvað* og *í bið* sitt á hvað. Þessi villa þýðir að varan er stillt sem **Stöðvuð** í sjálfgefnum pöntunarstillingum.

Ef vara er útilokuð og henni er bætt við innkaupapöntunarlínu eða sölupöntunarlínu koma upp viðvörunarboð. Þegar vara er útilokuð er ekki hægt að breyta birgðafærslum sem tengjast innkaupapöntunarlínunni eða sölupöntunarlínunni (til dæmis þegar fylgiseðill eða reikningur er bókaður). Hægt er að útiloka keypta vöru og selja vöru á sama tíma. Í þessu tilfelli er gátreiturinn **Stöðvað** valinn í innkaupapöntun, en varan er ekki útilokuð í birgðum eða í sölupöntun.

Hér eru nokkur skilyrði sem geta orðið til þess að lokað verði á sölu á vörunúmeri:

- Vara er enn í þróun eða framleiðslu. Þess vegna viltu ekki að hún sé seld eða tekin frá.
- Þú hefur móttekið margar gallaðar vörur og laga verður gallana áður en hægt er að selja vöruna.

Í tilvikum af þessu tagi er hægt að loka á vöruna þar til leyst hefur verið úr vandamálinu.

Ef lokað er á vöru og skilapöntunarlína er stofnuð birtast skilaboð. Ekki er hægt að loka á röð eða lotu vöru. Ef loka þarf hluta vöru er það hægt með því að flytja birgðir eða með því að loka á heildarbirgðir vörunnar yfir það tímabil.

## <a name="resolution"></a>Lausn

- Opnið síðuna **Sjálfgefnar pöntunarstillingar** fyrir vöruna og hreinsið gátreitinn **Stöðvað**.

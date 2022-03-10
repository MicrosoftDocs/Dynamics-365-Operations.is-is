---
title: Tengd forrit
description: Þetta efnisatriði útskýrir hvernig á að setja upp tengd forrit í rafrænum reikningum.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371921"
---
# <a name="connected-applications"></a>Tengd forrit

[!include [banner](../includes/banner.md)]

Tengd forrit eru tilvik Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management sem þú gætir viljað ná í gegnum Regulatory Configuration Service (RCS). Í gegnum tengdu forritin geturðu stillt hluta af hnattvæðingareiginleikum þínum í fjármála- eða framboðskeðjustjórnun til að láta rafræna reikningagerð virka.

Þegar þú notar hnattvæðingareiginleikann þinn er hægt að birta uppsetningarupplýsingarnar sem eiga við um fjármála- eða framboðskeðjustjórnunarforritið þitt beint frá RCS í viðeigandi tengda forritið.

Framboð á færibreytum Finance eða Supply Chain Management í RCS er gagnlegt þegar þú ert með mörg forritsumhverfi, eins og notendaviðurkenningarprófun (UAT) og framleiðsluumhverfi, og þú vilt halda uppsetningunni stöðugri með því að nota sömu færibreyturnar í mismunandi umhverfi.

## <a name="create-a-connected-application"></a>Búa til tengt forrit

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á **Umhverfisuppsetning** síðu, á aðgerðarrúðunni, veldu **Tengd forrit**.
4. Veljið **Nýtt** til að stofna tengt forrit.
5. Í reitinn **Heiti** skal færa inn heiti forritsins sem á að tengja.
6. Í reitnum **Tegund** skal velja **Dynamics 365 Finance**.
7. Í **Umsókn** reit, sláðu inn vefslóð umhverfisins til að tengjast.
8. Í **Leigjandi** reit, sláðu inn leigjanda umhverfisins.
9. Veldu **Vista**.
10. Á aðgerðasvæðinu skal velja **Athuga tengingu** til að prófa tenginguna við umhverfið. Lokið því næst síðunni.

## <a name="link-connected-applications-to-environments"></a>Tengja tengd forrit við umhverfi

1. Á **Umhverfisuppsetning** síðu, veldu **Nýtt** til að tengja tengdu forriti við umhverfi.
2. Í reitnum **Tengt forrit** skal velja tengt forrit.
3. Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi.
4. Veljið **Vista** og lokið síðan skjámyndinni.

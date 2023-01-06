---
title: Tengd forrit
description: Þessi grein útskýrir hvernig á að setja upp tengd forrit í rafrænni reikningsfærslu.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: aa6c80914301cc0403974a6acc5e95ff61c9c1a7
ms.sourcegitcommit: a5a4c45bb265758c6e5c3483c8552503b1799a89
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524690"
---
# <a name="connected-applications"></a>Tengd forrit

[!include [banner](../includes/banner.md)]

Tengd forrit eru tilvik Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management sem þú gætir viljað nálgast í gegnum Regulatory Configuration Service (RCS). Í gegnum tengd forrit er hægt að skilgreina hluta af eiginleika rafrænnar reikningsfærslu í Finance eða Supply Chain Management til að fá rafræna reikningsfærslu til að virka.

Þegar þú setur inn altækan eiginleika er hægt að birta uppsetningarupplýsingarnar sem eiga við viðkomandi Finance- eða Supply Chain Management-forrit beint frá RCS í viðeigandi tengt forrit.

Staða færibreyta Finance eða Supply Chain Management í RCS er gagnlegt þegar nokkur forritsumhverfi eru til staðar, svo sem samþykkisprófun notenda (UAT) og framleiðsluumhverfi, og þú vilt halda uppsetningunni stöðugri með því að setja sömu færibreytur inn í mismunandi umhverfi.

## <a name="create-a-connected-application"></a>Búa til tengt forrit

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Tengdir tenglar**, skal velja **Uppsetning á umhverfi**.
3. Á síðunni **Uppsetning umhverfis**, á aðgerðasvæðinu, skal velja **Tengd forrit**.
4. Veljið **Nýtt** til að stofna tengt forrit.
5. Í reitinn **Heiti** skal færa inn heiti forritsins sem á að tengja.
6. Í reitnum **Gerð** skal velja **Dynamics 365 Finance**.
7. Í reitinn **Forrit** skal færa inn vefslóð fyrir umhverfið sem á að tengjast við.
8. Í reitinn **Leigjandi** skal færa inn leigjanda umhverfisins.
9. Veldu **Vista**.
10. Á aðgerðasvæðinu skal velja **Athuga tengingu** til að prófa tenginguna við umhverfið. Lokið því næst síðunni.

## <a name="link-connected-applications-to-environments"></a>Tengja tengd forrit við umhverfi

1. Á síðunni **Uppsetning umhverfis** skal velja **Nýtt** til að úthluta tengdu forriti á umhverfi.
2. Í reitnum **Tengt forrit** skal velja tengt forrit.
3. Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi.
4. Veljið **Vista** og lokið síðan skjámyndinni.

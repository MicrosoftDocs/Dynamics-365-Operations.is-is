---
title: Tengd forrit
description: Þessi grein útskýrir hvernig á að setja upp tengd forrit í rafrænum reikningum.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524690"
---
# <a name="connected-applications"></a>Tengd forrit

[!include [banner](../includes/banner.md)]

Tengd forrit eru dæmi um Microsoft Dynamics 365 Fjármál og Dynamics 365 Supply Chain Management sem þú gætir viljað ná í gegnum Regulatory Configuration Service (RCS). Með tengdu forritunum geturðu stillt hluta af hnattvæðingareiginleikanum þínum í fjármála- eða framboðskeðjustjórnun til að láta rafræna reikningagerð virka.

Þegar þú notar hnattvæðingareiginleikann þinn er hægt að birta uppsetningarupplýsingarnar sem eiga við um fjármála- eða framboðskeðjustjórnunarforritið þitt beint frá RCS í viðeigandi tengda forritið.

Framboð á færibreytum Finance eða Supply Chain Management í RCS er gagnlegt þegar þú ert með mörg forritsumhverfi, eins og notendaviðurkenningarprófun (UAT) og framleiðsluumhverfi, og þú vilt halda uppsetningunni stöðugri með því að nota sömu færibreyturnar í mismunandi umhverfi.

## <a name="create-a-connected-application"></a>Búa til tengt forrit

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Í **Hnattvæðingareiginleiki** vinnurými, í **Tengdir tenglar** kafla, veldu **Umhverfisuppsetning**.
3. Á **Umhverfisuppsetning** síðu, á aðgerðarrúðunni, veldu **Tengd forrit**.
4. Veljið **Nýtt** til að stofna tengt forrit.
5. Í reitinn **Heiti** skal færa inn heiti forritsins sem á að tengja.
6. Í **Tegund** reit, veldu **Dynamics 365 Finance**.
7. Í **Umsókn** reit, sláðu inn vefslóð umhverfisins til að tengjast.
8. Í **Leigjandi** reit, sláðu inn leigjanda umhverfisins.
9. Veldu **Vista**.
10. Á aðgerðasvæðinu skal velja **Athuga tengingu** til að prófa tenginguna við umhverfið. Lokið því næst síðunni.

## <a name="link-connected-applications-to-environments"></a>Tengja tengd forrit við umhverfi

1. Á **Umhverfisuppsetning** síðu, veldu **Nýtt** til að tengja tengdu forriti við umhverfi.
2. Í reitnum **Tengt forrit** skal velja tengt forrit.
3. Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi.
4. Veljið **Vista** og lokið síðan skjámyndinni.

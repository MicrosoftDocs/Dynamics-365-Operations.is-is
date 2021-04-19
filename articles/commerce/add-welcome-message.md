---
title: Bæta við opnunarkveðju
description: Þetta efni lýsir því hvernig opnunarkveðju er bætt við Microsoft Dynamics 365 Commerce vefsvæði.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797384"
---
# <a name="add-a-welcome-message"></a>Bæta við opnunarkveðju

[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig opnunarkveðju er bætt við Microsoft Dynamics 365 Commerce vefsvæði.

Móttökuskilaboð á vefsíðu rafrænna viðskipta geta tilkynnt gestum um áframhaldandi útsölu, uppfærslur á vefnum eða framboð á árstíðabundnum línum. Móttökuskilaboðin eru stillt með því að nota viðvörunareininguna.

Viðvörunareiningunni ætti að bæta við hólfið **Villu-/upplýsingaskilaboð** í fyrirsagnarbrotinu. Viðvörunareiningin gerir þér kleift að tilgreina textann sem er sýndur, textalitinn og jöfnunina. Það gerir þér einnig kleift að tilgreina hvort gestir á vefnum geti hafnað skilaboðunum.

Þegar móttökuskilaboðum er bætt við samnýtt fyrirsagnarbrot verða þau sýnd á hverri síðu sem notar sniðmátið þar sem það samnýtta fyrirsagnarbrot er notað.

Fylgdu þessum skrefum til að bæta við móttökuskilaboðum á svæðið.

1. Opnaðu síðuna þína á svæðissmið Commerce.
1. Veldu **Brot**.
1. Veldu fyrirsagnarbrot til að bæta skilaboðunum við.
1. Stækkaðu í útlínutrénu **Villu-/upplýsingaskilaboð**.
1. Veldu viðvörunareininguna og veldu síðan **Í lagi**. Ef viðvörunareining er ekki enn til, veldu fyrst hnappinn fyrir úrfellingarmerki (**...**) **Villu-/upplýsingaboð** og veldu síðan **Bæta við einingu**.
1. Í eiginleikaglugganum til hægri, á flipanum **Gögn** velurðu **Bæta við gagnagjafa** og velur síðan **Innihald**.
1. Í reitinn **Inntakstexti** slærðu inn texta móttökuskilaboðanna.
1. Smelltu á **Vista**, veldu **Ljúka við breytingar** til að athuga hausbrotið og smelltu síðan á **Birta** til að birta það. 

Móttökuskilaboðin birtast nú efst á hverri síðu svæðis sem notar valið fyrirsagnarbrot.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Unnið með CSS hnekkiskrám](css-override-files.md)

[Bæta við táknmynd](add-favicon.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

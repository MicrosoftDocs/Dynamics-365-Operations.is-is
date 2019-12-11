---
title: Bæta við opnunarkveðju
description: Þetta efnisatriði lýsir því hvernig á að bæta móttökuskilaboðum við Microsoft Dynamics 365 Commerce vefsvæði.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697383"
---
# <a name="add-a-welcome-message"></a>Bæta við opnunarkveðju

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að bæta móttökuskilaboðum við Microsoft Dynamics 365 Commerce vefsvæði.

## <a name="overview"></a>Yfirlit

Móttökuskilaboð á vefsíðu rafrænna viðskipta geta tilkynnt gestum um áframhaldandi útsölu, uppfærslur á vefnum eða framboð á árstíðabundnum línum. Móttökuskilaboðin eru stillt með því að nota viðvörunareininguna.

Viðvörunareiningunni ætti að bæta við hólfið **Villu-/upplýsingaskilaboð** í fyrirsagnarbrotinu. Viðvörunareiningin gerir þér kleift að tilgreina textann sem er sýndur, textalitinn og jöfnunina. Það gerir þér einnig kleift að tilgreina hvort gestir á vefnum geti hafnað skilaboðunum.

Þegar móttökuskilaboðum er bætt við samnýtt fyrirsagnarbrot verða þau sýnd á hverri síðu sem notar sniðmátið þar sem það samnýtta fyrirsagnarbrot er notað.

Fylgdu þessum skrefum til að bæta við móttökuskilaboðum á svæðið.

1. Í Dynamics 365 Commerce, farðu á vefsíðuna.
1. Veldu **Brot**.
1. Veldu fyrirsagnarbrot til að bæta skilaboðunum við.
1. Stækkaðu í útlínutrénu **Villu-/upplýsingaskilaboð**.
1. Veldu viðvörunareininguna.

    Ef viðvörunareining er ekki ennþá til skaltu velja úrfellingarhnappinn (**...**) við hliðina á **Villu-/upplýsingaskilaboð** og velja síðan **Bæta við einingu**. Veldu viðvörunareininguna og veldu síðan **Í lagi**.

1. Í eiginleikaglugganum til hægri, á flipanum **Gögn** velurðu **Bæta við gagnagjafa** og velur síðan **Innihald**.
1. Í reitinn **Inntakstexti** slærðu inn texta móttökuskilaboðanna.
1. Vistaðu fyrirsagnarbrotið, skráðu það inn og gefðu það út.

Móttökuskilaboðin birtast nú efst á hverri síðu svæðis sem notar valið fyrirsagnarbrot.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Bæta við táknmynd](add-favicon.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)


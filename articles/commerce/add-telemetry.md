---
title: Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar
description: Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a5f82426d87cd2e0faa0195a841899bb03f9df08
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697337"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.

## <a name="overview"></a>Yfirlit

Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning. Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics. Flestir vefgreiningarpakkar krefjast þess að þú bætir við skriftarkóða biðlarans í **\<höfuð\>**-þáttinn í HTML fyrir allar síður á vefsvæðinu.

> [!NOTE]
> Leiðbeiningarnar í þessu efni eiga einnig við um aðra sérsniðna virkni biðlara sem Microsoft Dynamics 365 Commerce býður ekki staðbundið.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Stofnaðu endurnýtanlegt brot fyrir skriftarkóðann

Eftir að þú hefur stofnað brot fyrir skriftarkóðann er hægt að nota það á allar síður á vefsvæðinu.

1. Farðu í **Brot \> Ný síðubrot**.
2. Veldu **Ytri forskrift**, sláðu inn heiti fyrir brotið og veldu síðan **Í lagi**.
3. Í brotastigveldinu velurðu undireininguna **innsetning forskriftar** brotsins sem þú varst að búa til.
4. Í eiginleikaglugganum til hægri bætirðu við forskrift biðlara og stillir aðra stillingarvalkosti eins og þörf krefur.

## <a name="add-the-fragment-to-templates"></a>Bættu brotunum við sniðmát

1. Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.
2. Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.
3. Veldu úrfellingarhnappinn (**...**) fyrir hólfið **HTML-haus** og veldu síðan **Bæta við broti**.
4. Veldu brotið sem þú bjóst til fyrir forskriftakóðann.
5. Vista sniðmáti og skráðu það inn.

> [!NOTE]
> Eftir að því er lokið verður að birta brotið og sniðmátið. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Bæta við táknmynd](add-favicon.md)

[Bæta við opnunarkveðju](add-welcome-message.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)


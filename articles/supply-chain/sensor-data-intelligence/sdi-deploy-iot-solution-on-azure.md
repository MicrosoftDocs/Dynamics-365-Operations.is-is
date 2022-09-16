---
title: Settu upp IoT lausn á Azure
description: Sensor Data Intelligence notar gögn frá skynjurum sem eru tengdir við Microsoft Azure. Þessi grein útskýrir hvernig á að setja upp Internet of Things (IoT) lausn á Azure áskriftinni þinni.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 284aba91aa436ed1dfc02b5a93b4358ffc518017
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429018"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Settu upp IoT lausn á Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensor Data Intelligence notar gögn frá skynjurum sem eru tengdir við Microsoft Azure. Til að gera Azure kleift að sækja gögn frá skynjurunum þínum og deila þeim með Dynamics 365 Supply Chain Management, þú verður að setja upp Internet of Things (IoT) lausn á Azure áskriftinni þinni. Eftirfarandi byggingarskýringarmynd gefur yfirlit yfir lausnina og íhluti hennar.

![Sensor Data Intelligence byggingarlistarmynd.](media/sdi-architecture.png "Sensor Data Intelligence byggingarlistarmynd")

Fylgdu þessum skrefum til að dreifa nauðsynlegum tilföngum á Azure.

1. Skráðu þig inn á Supply Chain Management sem stjórnandi.
1. Fara til **Kerfisstjórnun \> Uppsetning \> Sensor Data Intelligence \> Dreifðu og tengdu Azure auðlindir** til að opna dreifingarhjálpina.
1. Á **Velkominn** síðu, lestu upplýsingarnar og veldu síðan **Næst**.
1. Á **Settu sýnishornið af IoT lausninni í Azure** síðu, lestu upplýsingarnar og síðan í **Leiðbeiningar** kafla, veldu **Dreifa**.
1. Nýr vafraflipi er opnaður og þú ert fluttur á Azure gáttina svo þú getir notað Azure tilföngin. Ef þú ert beðinn um það skaltu skrá þig inn með því að nota skilríkin þín fyrir Azure áskriftina þína.
1. Á **Sérsniðin uppsetning** síðu, í **Áskrift** reit, veldu áskriftina þína.
1. Undir **Auðlindahópur** reit, veldu **Búa til nýtt** til að búa til tilfangahóp fyrir Azure íhlutina sem þú munt dreifa.
1. Í fellivalmyndinni sem birtist, í **Nafn** reit, sláðu inn heiti fyrir nýja tilfangahópinn (til dæmis, *IoT kynningu*). Veljið síðan **Í lagi**.
1. Stilltu eftirfarandi svæði:

    - **Auðlindahópur** – Veldu tilfangahópinn sem þú bjóst til.
    - **Svæði** – Veldu svæði, helst svæðið þar sem Supply Chain Management umhverfið þitt er notað. Hafðu í huga að Azure svæði eru með mismunandi verðlagningu. Þú getur skoðað áætlaðan kostnað fyrir þitt svæði með því að nota [Sensor Data Intelligence verðreiknivél](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **Vefslóð framboðs keðjustjórnunarumhverfis** – Sláðu inn slóðina fyrir Supply Chain Management umhverfið þitt.
    - **Endurnotaðu núverandi Azure IoT Hub** – Skildu þennan gátreit ómerktan.

1. Veldu **Næst: Endurskoða + Búa til**.
1. Á **Sérsniðin uppsetning** síðu, staðfestu að staðfestingin hafi staðist og veldu síðan **Búa til**.
1. The **Dreifing er í gangi** síða fylgist með framvindu dreifingar þinnar. Dreifingarferlið getur tekið allt að 30 mínútur. Þegar **Dreifing er í gangi** síðu gefur til kynna að dreifingunni sé lokið skaltu velja tengilinn fyrir nafn tilfangahópsins til að opna síðu sem sýnir lista yfir tilföng sem eru notuð í hópnum.
1. Í tilfangalistanum, finndu skrána þar sem **Tegund** reiturinn er stilltur á *Stjórnað auðkenni*. Í **Nafn** dálk, veldu nafnið til að opna upplýsingasíðuna fyrir tilfangið.
1. Afritaðu gildið í **Auðkenni viðskiptavinar** reitinn (til dæmis með því að velja **Afritaðu á klemmuspjald** takki).
1. Farðu aftur á vafraflipann þar sem Supply Chain Management er í gangi, *en ekki loka flipanum fyrir Azure gáttina*. The **Settu sýnishornið af IoT lausninni í Azure** Wizard síða ætti enn að vera opin. 
1. Veljið **Næst**.
1. Á **Tengdu Azure auðlindir** síðu, í **Azure AD Auðkenni umsóknar viðskiptavinar** reit, líma á **Auðkenni viðskiptavinar** gildi sem þú afritaðir.
1. Farðu aftur á vafraflipann þar sem Azure gáttin er opin, *en ekki loka flipanum fyrir Supply Chain Management*. Upplýsingarasíðan fyrir tilfangið ætti enn að vera opin.
1. Veldu vafra **Til baka** hnappinn til að fara aftur í lista yfir tilföng í nýja tilfangahópnum.
1. Í tilfangalistanum, finndu skrána þar sem **Tegund** reiturinn er stilltur á *Azure Cache fyrir Redis*. Í **Nafn** dálk, veldu nafnið til að opna upplýsingasíðuna fyrir tilfangið.
1. Í vinstri yfirlitsrúðunni, veldu **Aðgangslyklar**.
1. Á **Aðgangslyklar** síðu, afritaðu gildið sem er sýnt fyrir **Aðaltengingarstrengur (StackExchange.Redis)** (til dæmis með því að velja **Afritaðu á klemmuspjald** takki).
1. Farðu aftur á vafraflipann þar sem Supply Chain Management er í gangi. The **Tengdu Azure auðlindir** síðan ætti enn að vera opið.
1. Í **Redis metraverslun tengistrengur** reit, líma á **Aðaltengingarstrengur (StackExchange.Redis)** gildi sem þú afritaðir.
1. Veljið **Ljúka**.

Azure auðlindir fyrir Sensor Data Intelligence eru nú notaðar í Azure áskriftinni þinni.

> [!NOTE]
> Hvenær sem er er hægt að skoða eða breyta tengingarupplýsingunum sem eru vistaðar í Supply Chain Management með því að opna **Sensor Data Intelligence færibreytur** síðu. Fyrir frekari upplýsingar, sjá [Sensor Data Intelligence færibreytur](sdi-parameters.md).

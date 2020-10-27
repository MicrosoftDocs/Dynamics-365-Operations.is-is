---
title: Setja upp Azure-tilföng fyrir IoT-gervigreind
description: Þetta efnisatriði útskýrir hvernig á að stofna og skilgreina Microsoft Azure-tilföng sem krafist er fyrir IoT-gervigreind.
author: ''
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bbac1676d28c7285c19ed48f77426a37ce123a29
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982895"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Setja upp Azure-tilföng fyrir IoT-gervigreind

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna og skilgreina Microsoft Azure-tilföng sem krafist er fyrir IoT-gervigreind.

## <a name="create-azure-resources"></a>Stofna Azure-tilföng

Fylgdu þessum skrefum til að búa til IoT-miðstöð, Redis-skyndiminni og lyklageymslu sem hægt er að opna með Microsoft Dynamics 365 Supply Chain Management.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Gangið úr skugga um að forritskenni Microsoft Dynamics ERP Microservices fyrir fyrsta aðila sé í leigjanda

Til að staðfesta að forritskennið fyrir Microsoft Dynamics ERP Microservices forrit fyrir fyrsta aðila sé í leigjandanum skal fylgja þessum skrefum.

1. Skráðu þig inn á Azure-gáttina á <https://portal.azure.com>.
2. Opnið **Azure Active Directory**.
3. Opnaðu **Enterprise-forrit**.
4. Í reitnum **Gerð forrits** skal velja **Microsoft-forrit**.
5. Í leitarreitinn skal færa inn **Microsoft Dynamics ERP Microservices**.
6. Gangið úr skugga um að **Microsoft Dynamics ERP Microservices** sé á listanum. Önnur forrit eru með svipuð heiti. Þess vegna skal ganga úr skugga um að rétt forrit sé fundið. Forritskenni er **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Ef forritið er ekki á listanum verður að bæta því við leigjandann þinn:

    1. Í Azure-gáttinni, á tækjastikunni, skal velja hnappinn til að opna Azure Cloud Shell.
    2. Keyrið skipunina **Install-Module AzureAD**. Sláið inn **Y** til að setja upp eininguna.
    3. Keyrið skipunina **Get-InstalledModule -Name "AzureAD"** til að staðfesta að einingin sé uppsett.
    4. Keyrið skipunina **Connect-AzureAD -Confirm** til að keyra auðkenninguna.
    5. Keyrið skipunina **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Nú er hægt að endurtaka skref 1 til 6 til að staðfesta að forritskennið sé í leigjandanum.

### <a name="create-a-key-vault-resource"></a>Stofna tilföng lyklageymslu

Til að búa til tilföng lyklageymslu skal fylgja þessum skrefum.

1. Í Azure-gátt skal búa til eða fara í tilfangaflokk.
2. Veljið **Bæta við**.
3. Á leitarreit á síðunni **Nýtt** skal slá inn **Lyklageymsla**. Veldu síðan **Búa til**.
4. Á síðunni **Búa til lyklageymslu**, í reitnum **Heiti lyklageymslu** skaltu slá inn heiti.
5. Farið yfir sjálfgildi og veljið síðan **Fara yfir + Búa til**.
6. Velja **Stofna**.

Lyklageymslan er búin til í bakgrunni.

### <a name="create-an-iot-hub-resource"></a>Búa til tilföng á IoT-miðstöð

Til að búa til tilföng á IoT-miðstöð skal fylgja þessum skrefum.

1. Stofna eða fara í tilfangaflokk.
2. Veljið **Bæta við**.
3. Á leitarreitnum á síðunni **Nýtt** skaltu slá inn **IoT-miðstöð**. Veldu síðan **Búa til**.
4. Sláðu inn heiti í reitinn **Heiti IoT-miðstöðvar**.
5. Farið yfir sjálfgildi og veljið síðan **Fara yfir + Búa til**.
6. Velja **Stofna**.

IoT-miðstöð er stofnuð í bakgrunni.

> [!NOTE]
> Mælt er með því að aðeins sé búið að stofna eitt tilföng fyrir IoT-miðstöð fyrir hvert umhverfi.

### <a name="create-a-redis-cache-resource"></a>Stofna tilföng fyrir Redis-skyndiminni

Til að stofna tilföng fyrir Redis-skyndiminni skal fylgja þessum skrefum.

1. Stofna eða fara í tilfangaflokk.
2. Veljið **Bæta við**.
3. Á leitarreitnum á síðunni **Nýtt** skaltu slá inn **Azure-skyndiminni fyrir Redis**. Veldu síðan **Búa til**.
4. Í reitinn **DNS-heiti** skal færa inn heiti.
5. Farið yfir sjálfgefin gildi og veljið síðan **Stofna**.

Skyndiminni Redis er búið til í bakgrunni.

> [!NOTE]
> Við mælum með því að aðeins eitt Redis skyndiminni sé stofnað fyrir hvert umhverfi.

Öll tilföng hafa nú verið stofnuð.

## <a name="configure-the-azure-resources"></a>Skilgreina Azure-tilföngin

### <a name="configure-the-iot-hub"></a>Skilgreina IoT-miðstöð

Til að skilgreina IoT-miðstöð skaltu fylgja þessum skrefum.

1. Í tilföngum skal velja tilföng IoT-miðstöðvar.
2. Á vinstri yfirlitssvæði skal velja **Innbyggðar endastöðvar**.
3. Undir **neytendahópar** skal líma eftirfarandi neytendahópa. Þessir neytendahópar samsvara aðstæðum „úr kassanum“.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Stilla lyklageymslu

Til að skilgreina lyklageymsluna skal fylgja þessum skrefum.

1. Í tilföngum skal velja tilföng lyklageymslunnar.
2. Á vinstri yfirlitssvæði skal velja **Access-reglur**.
3. Veljið **Bæta við aðgangsreglu**.
4. Á síðunni **Bæta við aðgangsreglu**, í reitinum **Heimildir leyniorðs**, skal velja **Sækja** og **Listi**.
5. Smelltu á **Velja aðalreikning**.
6. Í svarglugganum **Aðalreikningur** skal leita að og velja **Microsoft Dynamics ERP Microservices**. Veljið síðan **Velja**.
7. Veljið **Bæta við**.
8. Veljið **Vista**.

Forritið hefur nú aðgang að leyniorðum í lyklageymslunni.

### <a name="save-the-iot-hub-connection-string-secret"></a>Vista leyniorð fyrir tengistreng IoT-miðstöðvar

Fylgdu þessum skrefum til að vista leyniorðið fyrir tengistreng IoT-miðstöðvar.

1. Í tilföngum skal velja tilföng IoT-miðstöðvar.
2. Á vinstri yfirlitssvæði skal velja **Innbyggðar endastöðvar**.
3. Afritið gildið í reitnum **Endastöð samhæf miðstöð tilviks**.
4. Opnaðu tilföng lyklageymslu.
5. Á vinstra yfirlitssvæðinu skal velja **Leyniorð**.
6. Veljið **Mynda/Flytja inn**.
7. Færið inn lýsandi nafn í reitinn **Heiti**.
8. Í reitnum **Gildi** skal líma gildi endastöðvar sem var afritað áður.
9. Velja **Stofna**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Vista leyniorð tengistrengs Redis-skyndiminnis

Til að vista leyniorðið fyrir tengistreng Redis-skyndiminnis skal fylgja þessum skrefum.

1. Í tilföngum skal velja tilfang Redis-skyndiminnis.
2. Veljið **Aðgangslyklar**.
3. Afritið gildið í reitnum **Aðaltengistrengur**.
4. Opnaðu tilföng lyklageymslu.
5. Á vinstra yfirlitssvæðinu skal velja **Leyniorð**.
6. Veljið **Mynda/Flytja inn**.
7. Færið inn lýsandi nafn í reitinn **Heiti**.
8. Í reitnum **Gildi** skal líma tengistrenginn sem var afritaður áður.
9. Velja **Stofna**.

> [!NOTE]
> Þegar einn af tengistrengnum er uppfærður þarf einnig að uppfæra leynigildin.

Nú er úthlutun nauðsynlegra Azure-tilfanga lokið. Næsta skref er að [setja upp IoT-gervigreind viðbótina í Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).

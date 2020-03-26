---
title: Tvöfaldur skrifa uppsetning frá Lifecycle Services
description: Þetta efni útskýrir hvernig á að setja upp tvískipt tengsl milli nýs umhverfis Finance and Operations og nýs umhverfis Common Data Service úr Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 75765c0cc03c64030fac6bc656f57a143828b85b
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112459"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Tvöfaldur skrifa uppsetning frá Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þetta efni útskýrir hvernig á að setja upp tvískipt tengsl milli nýs umhverfis Finance and Operations og nýs umhverfis Common Data Service úr Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forkröfur

Þú verður að vera stjórnandi til að setja upp tvískipt tengingu.

+ Þú verður að hafa aðgang að leigjandanum.
+ Þú verður að vera stjórnandi í bæði umhverfi Finance and Operations og umhverfi Common Data Service.

## <a name="set-up-a-dual-write-connection"></a>Setja upp tvískipt tengingu

Fylgið eftirfarandi skrefum til að setja tvískipta tengingu.

1. Í LCS skaltu fara í verkið.
2. Veldu **Stilla** til að beita nýju umhverfi.
3. Veldu útgáfuna. 
4. Veldu grannfræði. Ef aðeins ein grannfræði er tiltæk er hún sjálfkrafa valin.
5. Ljúktu við fyrstu skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.
6. Á flipaum **Common Data Service** fylgirðu einu af eftirfarandi skrefum:

    - Ef umhverfið Common Data Service er þegar veitt fyrir leigjanda þinn getur þú valið það.

        1. Stillið valkostinn **Stilla Common Data Service** á **Já**.
        2. Í reitnum **Aðgengilegt umhverfi** velurðu umhverfið sem á að samþætta við Finance and Operations-gögnin þín. Listinn inniheldur öll umhverfi þar sem þú hefur stjórnunarréttindi.
        3. Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.

        ![Flipinn Common Data Service þegar umhverfið Common Data Service er þegar veitt fyrir leigjandann](../dual-write/media/lcs_setup_1.png)

    - Ef leigjandi þinn er ekki þegar með Common Data Service umhverfi verður nýtt umhverfi veitt.

        1. Stillið valkostinn **Stilla Common Data Service** á **Já**.
        2. Slá inn heiti fyrir umhverfi Common Data Service.
        3. Veldu svæðið til að dreifa umhverfinu á.
        4. Veldu sjálfgefið tungumál og gjaldmiðil fyrir umhverfið.

            > [!NOTE]
            > Þú getur ekki breytt tungumálinu og gjaldmiðlinum seinna.

        5. Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.

        ![Common Data Service flipann þegar leigjandi þinn er ekki þegar með Common Data Service umhverfi](../dual-write/media/lcs_setup_2.png)

7. Ljúktu við eftirstandandi skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.
8. Þegar umhverfið hefur stöðuna **Uppsett** skaltu opna síðuna umhverfisupplýsingar. Hlutinn **Common Data Service upplýsingar um umhverfi** sýnir nöfn í Finance and Operations umhverfi og Common Data Service umhverfi sem eru tengd.

    ![Common Data Service kafla um umhverfisupplýsingar](../dual-write/media/lcs_setup_3.png)

9. Stjórnandi í Finance and Operations umhverfi verður að skrá sig inn á LCS og velja **Hlekkur á CDS fyrir forrit** til að ljúka við tengilinn. Umhverfisupplýsingasíðan sýnir upplýsingar um tengilið stjórnanda.

    Eftir að hlekknum er lokið er staðan uppfærð til **Umhverfistengingu lokið**.

10. Til að opna vinnusvæðið **Sameining gagna** í Finance and Operations umhverfi og stjórna sniðmátunum sem eru í boði, veldu **Hlekkur á CDS fyrir forrit**.

    ![Hlekkur á hnappinn CDS for Apps í Common Data Service kafla um umhverfisupplýsingar](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Þú getur ekki aftengt umhverfi með því að nota LCS. Til að aftengja umhverfi skaltu opna vinnusvæðið **Gagnasamþætting** í Finance and Operations umhverfi og veldu síðan **Aftengja**.

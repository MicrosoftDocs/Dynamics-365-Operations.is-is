---
title: Uppsetning tvöfaldra skrifa úr Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp tengingu tvöfaldrar skráningar úr Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567721"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Uppsetning tvöfaldra skrifa úr Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efni útskýrir hvernig á að setja upp tvískipt tengsl milli nýs umhverfis Finance and Operations og nýs umhverfis Dataverse úr Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forkröfur

Þú verður að vera stjórnandi til að setja upp tvískipt tengingu.

+ Þú verður að hafa aðgang að leigjandanum.
+ Þú verður að vera stjórnandi í bæði umhverfi Finance and Operations og umhverfi Dataverse.

## <a name="set-up-a-dual-write-connection"></a>Setja upp tvískipt tengingu

Fylgið eftirfarandi skrefum til að setja tvískipta tengingu.

1. Í LCS skaltu fara í verkið.
2. Veldu **Stilla** til að beita nýju umhverfi.
3. Veldu útgáfuna. 
4. Veldu grannfræði. Ef aðeins ein grannfræði er tiltæk er hún sjálfkrafa valin.
5. Ljúktu við fyrstu skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.
6. Á flipaum **Dataverse** fylgirðu einu af eftirfarandi skrefum:

    - Ef umhverfið Dataverse er þegar veitt fyrir leigjanda þinn getur þú valið það.

        1. Stillið valkostinn **Stilla Dataverse** á **Já**.
        2. Í dálkinum **Tiltæk umhverfi** skal velja umhverfið sem á að samþætta við Finance and Operations gögnin. Listinn inniheldur öll umhverfi þar sem þú hefur stjórnunarréttindi.
        3. Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.

        ![Flipinn Dataverse þegar umhverfið Dataverse er þegar veitt fyrir leigjandann](../dual-write/media/lcs_setup_1.png)

    - Ef leigjandi þinn er ekki þegar með Dataverse umhverfi verður nýtt umhverfi veitt.

        1. Stillið valkostinn **Stilla Dataverse** á **Já**.
        2. Slá inn heiti fyrir umhverfi Dataverse.
        3. Veldu svæðið til að dreifa umhverfinu á.
        4. Veldu sjálfgefið tungumál og gjaldmiðil fyrir umhverfið.

            > [!NOTE]
            > Þú getur ekki breytt tungumálinu og gjaldmiðlinum seinna.

        5. Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.

        ![Dataverse flipann þegar leigjandi þinn er ekki þegar með Dataverse umhverfi](../dual-write/media/lcs_setup_2.png)

7. Ljúktu við eftirstandandi skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.
8. Þegar umhverfið hefur stöðuna **Uppsett** skaltu opna síðuna umhverfisupplýsingar. Kaflinn **Power Platform Samþætting** sýnir heiti Finance and Operations umhverfisins og Dataverse umhverfis sem er tengt.

    ![Power Platform Hluti samþættingar](../dual-write/media/lcs_setup_3.png)

9. Stjórnandi í Finance and Operations umhverfi verður að skrá sig inn á LCS og velja **Hlekkur á CDS fyrir forrit** til að ljúka við tengilinn. Umhverfisupplýsingasíðan sýnir upplýsingar um tengilið stjórnanda.

    Eftir að hlekknum er lokið er staðan uppfærð til **Umhverfistengingu lokið**.

10. Til að opna vinnusvæðið **Sameining gagna** í Finance and Operations umhverfi og stjórna sniðmátunum sem eru í boði, veldu **Hlekkur á CDS fyrir forrit**.

    ![Tengill á CDS fyrir forritahnapp í Power Platform samþættingarhlutanum](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Þú getur ekki aftengt umhverfi með því að nota LCS. Til að aftengja umhverfi skaltu opna vinnusvæðið **Gagnasamþætting** í Finance and Operations umhverfi og veldu síðan **Aftengja**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
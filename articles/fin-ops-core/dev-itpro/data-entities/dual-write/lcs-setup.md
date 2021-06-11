---
title: Uppsetning tvöfaldra skrifa úr Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp tengingu tvöfaldrar skráningar úr Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103570"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Uppsetning tvöfaldra skrifa úr Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að virkja tvöfalda skráningu úr Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forkröfur

Ljúka verður við Power Platform samþættinguna eins og lýst er í eftirfarandi efnum:

+ [Power Platform Samþætting - Virkja við uppsetningu umhverfis](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform samþætting - Setja upp eftir uppsetningu umhverfis](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Setja upp tvöfalda skráningu fyrir ný Dataverse umhverfi

Fylgið þessum skrefum til að setja upp tvöfalda skráningu af LCS-síðunni **Upplýsingar um umhverfi**:

1. Á síðunni **Upplýsingar um umhverfi** skal stækka hlutann **Power Platform Samþætting**.

2. Veljið hnappinn **Notkun tvöfaldrar skráningar**.

    ![Power Platform samþætting](media/powerplat_integration_step2.png)

3. Farið yfir skilmálana og veljið því næst **Skilgreina**.

4. Veldu **Í lagi** til að halda áfram.

5. Hægt er að fylgjast með framvindunni með því að endurhlaða upplýsingasíðu umhverfis með reglulegu millibili. Uppsetning tekur yfirleitt innan við 30 mínútur.  

6. Þegar uppsetningunni er lokið koma upp skilaboð þar sem látið er vita hvort ferlið hafi tekist eða ef villa kom upp. Ef uppsetningin mistókst birtast tengd villuboð. Þú verður að laga allar villur sem kunna að vera til staðar áður en þú ferð í næsta skref.

7. Veljið **Tengja við Power Platform umhverfi** til að búa til tengingu milli Dataverse og núverandi gagnagrunna umhverfis. Þetta tekur yfirleitt innan við 5 mínútur.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Tengill á Power Platform-umhverfið":::

8. Þegar tengingin er komin verður tengill sýndur. Notið tengilinn til að skrá ykkur inn á stjórnunarsvæði tvöfaldrar skráningar í Finance and Operations umhverfinu. Þaðan er hægt að setja upp einingavarpanir.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Setja upp tvöfalda skráningu fyrir fyrirliggjandi Dataverse umhverfi

Til að setja upp tvöfalda skráningu fyrir fyrirliggjandi Dataverse umhverfi þarf að stofna Microsoft [þjónustubeiðni](../../lifecycle-services/lcs-support.md). Beiðnin verður að innihalda:

+ Finance and Operations umhverfiskennið.
+ Heiti umhverfis í Lifecycle Services.
+ Fyrirtækiskennið Dataverse eða umhverfiskennið Power Platform úr Power Platform stjórnendamiðstöðinni. Í beiðninni skal biðja um að kennið verði tilvikið sem notað er fyrir Power Platform samþættingu.

> [!NOTE]
> Þú getur ekki aftengt umhverfi með því að nota LCS. Til að aftengja umhverfi skaltu opna vinnusvæðið **Gagnasamþætting** í Finance and Operations umhverfi og veldu síðan **Aftengja**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

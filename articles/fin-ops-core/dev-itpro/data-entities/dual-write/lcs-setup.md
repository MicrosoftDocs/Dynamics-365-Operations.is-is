---
title: Uppsetning tvöfaldra skrifa úr Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp tengingu tvöfaldrar skráningar úr Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 060734154607263b5fed80b21fc9355b513ea26e3b1be88498310905531dceaa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729044"
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

    ![Power Platform Samþætting.](media/powerplat_integration_step2.png)

3. Farið yfir skilmálana og veljið því næst **Skilgreina**.

4. Veldu **Í lagi** til að halda áfram.

5. Hægt er að fylgjast með framvindunni með því að endurhlaða upplýsingasíðu umhverfis með reglulegu millibili. Uppsetning tekur yfirleitt innan við 30 mínútur.  

6. Þegar uppsetningunni er lokið koma upp skilaboð þar sem látið er vita hvort ferlið hafi tekist eða ef villa kom upp. Ef uppsetningin mistókst birtast tengd villuboð. Þú verður að laga allar villur sem kunna að vera til staðar áður en þú ferð í næsta skref.

7. Veljið **Tengja við Power Platform umhverfi** til að búa til tengingu milli Dataverse og núverandi gagnagrunna umhverfis. Þetta tekur yfirleitt innan við 5 mínútur.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Tengill á Power Platform-umhverfið.":::

8. Þegar tengingin er komin verður tengill sýndur. Notið tengilinn til að skrá ykkur inn á stjórnunarsvæði tvöfaldrar skráningar í Finance and Operations umhverfinu. Þaðan er hægt að setja upp einingavarpanir.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Setja upp tvöfalda skráningu fyrir fyrirliggjandi Dataverse umhverfi

Til að setja upp tvöfalda skráningu fyrir fyrirliggjandi Dataverse umhverfi þarf að stofna Microsoft [þjónustubeiðni](../../lifecycle-services/lcs-support.md). Beiðnin verður að innihalda:

+ Finance and Operations umhverfiskennið.
+ Heiti umhverfis í Lifecycle Services.
+ Fyrirtækiskennið Dataverse eða umhverfiskennið Power Platform úr Power Platform stjórnendamiðstöðinni. Í beiðninni skal biðja um að kennið verði tilvikið sem notað er fyrir Power Platform samþættingu.

> [!NOTE]
> Þú getur ekki aftengt umhverfi með því að nota LCS. Til að aftengja umhverfi skaltu opna vinnusvæðið **Gagnasamþætting** í Finance and Operations umhverfi og veldu síðan **Aftengja**.

## <a name="linking-mismatch"></a>Linking mismatch

Mögulegt er að LCS-umhverfi þitt sé tengt við eitt Dataverse tilvik en umhverfi tvöfaldrar skráningar er tengt við annað Dataverse tilvik. Þetta misræmi í tengingu getur valdið óvæntri hegðun og það gæti endað með því að gögn verði send í rangt umhverfi. Það umhverfi sem mælt er með að nota fyrir tvöfalda skráningu er það sem er búið til sem hluti af Power Platform samþættingu og til lengri tíma litið verður þetta eina leiðin til að koma á tengli milli umhverfa.

Ef umhverfið þitt er með misræmi í tengingu sýnir LCS viðvörun á upplýsingasíðu umhverfisins svipað og „Microsoft hefur greint að umhverfið þitt er tengt í gegnum tvöfalda skráningu við annan viðtökustað en er tilgreindur í Power Platform samþættingu, sem ekki er mælt með“:

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform misræmi í tengli samþættingar.":::

Ef þessi villa kemur upp eru tvær leiðir í boði eftir því hverjar þarfir þínar eru:

+ [Aftengja og endurtengja umhverfi fyrir tvöföld skrif (endurstilla eða breyta tengingu)](relink-environments.md#scenario-reset-or-change-linking) eins og tilgreint á upplýsingasíðu LCS-umhverfisins. Þetta er ákjósanlegur valkostur vegna þess að þú getur keyrt hann án notendaþjónustu Microsoft.  
+ Ef þú vilt halda tenglinum í tvöföldum skrifum geturðu beðið notendaþjónustu Microsoft um hjálp við að breyta Power Platform samþættingu til að nota fyrirliggjandi Dataverse umhverfið eins og fjallað er um í hlutanum hér á undan.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

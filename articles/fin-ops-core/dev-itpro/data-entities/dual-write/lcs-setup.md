---
title: Uppsetning tvöfaldra skrifa úr Lifecycle Services
description: Í þessari grein er útskýrt hvernig á að setja upp tengingu tvöfaldrar skráningar úr Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: laswenka
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: dda0b20492a109e4c3781db520ac19c325e0b403
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289179"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Uppsetning tvöfaldra skrifa úr Lifecycle Services

[!include [banner](../../includes/banner.md)]



Í þessari grein er útskýrt hvernig á að virkja tvöfalda skráningu úr Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forkröfur

Viðskiptavinir verða að ljúka við Power Platform samþættinguna eins og lýst er í eftirfarandi efnum:

- Ef þú notar ekki Microsoft Power Platform og vilt stækka umhverfi fjármála- og reksturs með því að bæta við verkvangsmöguleikum skaltu skoða [Power Platform Samþætting - Virkja við uppsetningu umhverfis](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Ef þú ert þegar með Dataverse og Power Platform umhverfi og vilt tengja þau við umhverfi fjármála- og reksturs skaltu skoða [Power Platform samþætting - Virkja eftir uppsetningu umhverfis](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Setja upp tvöfalda skráningu fyrir ný eða fyrirliggjandi Dataverse-umhverfi

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

8. Þegar tengingin er komin verður tengill sýndur. Notið tengilinn til að skrá ykkur inn á stjórnunarsvæði tvöfaldrar skráningar í umhverfi fjármála- og rekstursnu. Þaðan er hægt að setja upp einingavarpanir.

## <a name="linking-mismatch"></a>Linking mismatch

Möguleiki er á því að umhverfi tvöfaldrar skráningar sé tengt við Dataverse tilvik á meðan LCS er ekki uppsett fyrir Power Platform samþættingu. Þetta tengingarmisræmi getur valdið óvæntri hegðun. Mælt er með því að upplýsingar um LCS-umhverfi stemmi við það sem þú tengist í tvöfaldri skráningu þannig að viðskiptatilvik, sýndartöflur og viðbætur geta notað sömu tenginguna.

Ef umhverfið þitt er með misræmi í tengingu sýnir LCS viðvörun sem er svipuð eftirfarandi dæmi á upplýsingasíðu umhverfisins svipað og „Microsoft hefur greint að umhverfið þitt er tengt í gegnum tvöfalda skráningu við annan viðtökustað en er tilgreindur í Power Platform samþættingu, sem ekki er mælt með:“

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform misræmi í tengli samþættingar.":::

Ef þú færð þessa viðvörun skaltu prófa eina af eftirfarandi lausnum:

- Ef LCS-umhverfið þitt hefur aldrei verið sett upp fyrir Power Platform samþættingu geturðu tengst Dataverse tilvikinu sem er skilgreint í tvöfaldri skráningu með því að fylgja leiðbeiningunum í þessari grein.
- Ef LCS-umhverfið þitt hefur þegar verið sett upp fyrir Power Platform samþættingu ættirðu að aftengja tvöfalda skráningu og endurtengja hana við umhverfi sem LCS tilgreinir með því að nota [Aðstæður: Endurstilla eða breyta tengingu](relink-environments.md#scenario-reset-or-change-linking).

Áður var í boði að velja handvirka þjónustubeiðni en það var áður en valkostur 1 var til.  Microsoft styður ekki lengur handvirkar endurtengingarbeiðnir í gegnum þjónustubeiðnir.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


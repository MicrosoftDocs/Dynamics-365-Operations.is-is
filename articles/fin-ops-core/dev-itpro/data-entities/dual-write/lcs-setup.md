---
title: Uppsetning tvöfaldra skrifa úr Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp tengingu tvöfaldrar skráningar úr Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 53e82fbf8cff834c9eb0d14a0597561158b85fa1
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783202"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Uppsetning tvöfaldra skrifa úr Lifecycle Services

[!include [banner](../../includes/banner.md)]



Í þessu efnisatriði er útskýrt hvernig á að virkja tvöfalda skráningu úr Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forkröfur

Viðskiptavinir verða að ljúka við Power Platform samþættingu eins og lýst er í eftirfarandi efnisatriðum:

- Ef þú notar ekki ennþá Microsoft Power Platform og vilt stækka fjármála- og rekstrarumhverfið þitt með því að bæta við vettvangsgetu, sjá [Power Platform Samþætting - Virkja á uppsetningu umhverfisins](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Ef þú hefur nú þegar Dataverse og Power Platform umhverfi, og vilja tengja þau við fjármála- og rekstrarumhverfi, sjá [Power Platform samþætting - Virkja eftir uppsetningu umhverfisins](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Settu upp tvískrift fyrir nýja eða núverandi Dataverse umhverfi

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

8. Þegar tengingin er komin verður tengill sýndur. Notaðu hlekkinn til að skrá þig inn á tvískrifa stjórnunarsvæðið í Finance and Operations umhverfinu. Þaðan er hægt að setja upp einingavarpanir.

## <a name="linking-mismatch"></a>Linking mismatch

Það er mögulegt að tvískrifaumhverfið þitt sé tengt við a Dataverse dæmi á meðan LCS er ekki sett upp fyrir Power Platform sameining. Þetta ósamræmi við tengingar getur valdið óvæntri hegðun. Mælt er með því að upplýsingar um LCS umhverfi passi við það sem þú ert tengdur við í tvískrift svo að sömu tengingin sé hægt að nota fyrir viðskiptaviðburði, sýndarborð og viðbætur.

Ef umhverfið þitt hefur ósamræmi við tengingar sýnir LCS viðvörun sem líkist eftirfarandi dæmi á upplýsingasíðu umhverfisins þíns: "Microsoft hefur uppgötvað að umhverfið þitt er tengt með Dual-write á annan áfangastað en tilgreint er í Power Platform Samþætting, sem ekki er mælt með.“

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform misræmi í tengli samþættingar.":::

Ef þú færð þessa viðvörun skaltu prófa eina af eftirfarandi lausnum:

- Ef LCS umhverfið þitt hefur aldrei verið sett upp fyrir Power Platform samþættingu, þú getur tengst við Dataverse tilvik sem er stillt í tvískrift með því að fylgja leiðbeiningunum í þessari grein.
- Ef LCS umhverfið þitt er þegar sett upp fyrir Power Platform samþættingu ættir þú að aftengja tvískrift og endurtengja hana við þann sem LCS tilgreinir með því að nota [Atburðarás: Núllstilla eða breyta tengingu](relink-environments.md#scenario-reset-or-change-linking).

Í fortíðinni var handvirkur stuðningsmiði valkostur í boði, en það var áður en valkostur 1 hér að ofan var til.  Microsoft styður ekki lengur handvirkar endurtengingarbeiðnir í gegnum stuðningsmiða.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

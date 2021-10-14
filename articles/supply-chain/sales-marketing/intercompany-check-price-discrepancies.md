---
title: Villuleita verðmisræmi í samstæðupöntunum
description: Í þessu efnisatriði er útskýrt hvernig á að athuga verðmisræmi í samstæðupöntun
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9a0ba4980f8acf56d84dc865094b405b7402ad5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548323"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Villuleita verðmisræmi í samstæðupöntunum

[!include [banner](../../includes/banner.md)]

Hægt er að nota þetta ferli til að kanna verðmisræmi í samstæðupöntunum.

1. Farðu í **Innkaup og aðföng \> Reglubundið \> Tiltekt \> Athuga verðmisræmi í samstæðupöntun**.
1. Setja upp runuvinnslu, ef þörf er á, og síðan **Í lagi** velja til að kanna verð og afslætti fyrir samstæðusölupantanir og innkaupapantanir. Annars skal velja **Hætta við** til að loka síðunni án þess að framkvæma athugunina.

    > [!TIP]
    > Ef vandamál eru með samstillingu eða úthreyfingar með verð, verða þau skráð í upplýsingaskilaboð sem á að birta. Hægt er að prenta upplýsingaboðin til viðmiðunar.

1. Í upplýsingaboðinu skal velja viðeigandi línu til að opna pöntunina í núverandi lögaðila. Opnaðu pöntunina í tengda lögaðilanum með því að velja **Innan samstæðu** og síðan **Innkaupapöntun innan samstæðu** eða **Sölupöntun innan samstæðu**.

    > [!NOTE]
    > Ef leyfa á uppfærslu samstæðupöntunar:
    >
    > 1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
    > 1. Á aðgerðasvæðinu skal velja flipann **Almennt** og síðan velja **Innan samstæðu**.
    > 1. Á síðunni **Innan samstæðu** skal velja **Innkaupapöntunarreglur** eða **Sölupöntunarreglur**.
    > 1. Veldu **Leyfa breytingar á verði** og **Leyfa breytingar á afslætti** á báðum svæðum.

1. Opnið viðkomandi samstæðupöntun þar sem á að halda verðinu.
1. Fyrir hverja pöntunarlínu skal breyta reitnum **Einingarverð** fyrir línuna, og breyta henni síðan í upphaflega gildið. Breyttu reitnum **Afsláttur** fyrir línuna fram og til baka og breyttu viðeigandi reitunum **Gjöld á innkaupum** eða **Sölugjöld** fram og til baka. Þegar gildunum er breytt fram og aftur verður samstilling verðs, afslátta og gjalda úr þessari samstæðufyrirtækislínu í tilvísuðu samstæðupöntunarlínuna svo að þær verða sjálfvirkt samstilltar.

    > [!NOTE]
    > Þessi samstilling gildir aðeins ef samstæðusölupöntunin hefur ekki verið reikningsfærð. Ef samstæðupöntunin hefur verið reikningsbókuð og reikningabók viðskiptavinar stofnuð verður að gera breytingar beint í samstæðuinnkaupapöntunarlínunum með því að gera verð, afslætti og gjöld jöfn því sem er í reikningabók samstæðuviðskiptavinar. Ef þetta er ekki gert er ekki hægt að reikningsbóka samstæðupöntunarlínuna því það verður misræmi í pöntunarsamtölunum.

1. Endurtakið ferlið þar til allar samstæðuinnkaupa- og sölupantanir hafa verið samstilltar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

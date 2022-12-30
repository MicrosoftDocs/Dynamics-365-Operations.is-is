---
title: Villuleita verðmisræmi í samstæðupöntunum
description: Þessi grein útskýrir hvernig á að athuga verðmisræmi í samstæðupöntun
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ca27e86545ba8179c595e55487dbbf49cd9ec528
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890684"
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

---
title: Umsjón reikninga fyrir B2B-vefsvæði fyrir rafræn viðskipti
description: Þessi grein lýsir reikningsstjórnunargetu Microsoft Dynamics 365 Commerce viðskiptavefsíður fyrir viðskipti (B2B) fyrir rafræn viðskipti.
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fa6b81187481a6b7f47ea02291e5a581052d6c7b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854927"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Umsjón reikninga fyrir B2B-vefsvæði fyrir rafræn viðskipti

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir reikningsstjórnunargetu Microsoft Dynamics 365 Commerce viðskiptavefsíður fyrir viðskipti (B2B) fyrir rafræn viðskipti.

Það er algengt að fyrirtæki sem sjá um B2B viðskipti taka við pöntunum á inneign viðskiptavina og senda síðan reikning til viðskiptavina eftir að þeir uppfylla pöntunina. Greiðsluskilmálar eru skilgreindir fyrir viðskiptavini og það gæti verið einhver afsláttur til að hvetja viðskiptavini til að greiða á réttum tíma eða fyrir tíma. Til að auka líkurnar á að greiðslur berist á réttum tíma, leyfa B2B rafræn viðskipti viðskiptavinum að skoða alla reikninga sína. Viðskiptavinur getur auðveldlega síað reikningana til að skoða greidda, ógreidda og hlutagreidda reikninga ásamt gjalddaga.

![Reikningasíða á B2B vefsíðu.](../media/ViewInvoices.png)

> [!NOTE]
> Innskráður notandi getur aðeins skoðað og greitt eigin reikninga. Ef fyrirtækisreikningur er stilltur á **Reikningsreikningur** fellivalmynd á **Reikningur og afhending** Flýtiflipa viðskiptavinaskrár í höfuðstöðvum Commerce, notandinn mun geta skoðað og greitt reikninga fyrir fyrirtækisreikninginn.

Á **Reikningar** síðu á B2B vefsíðu, getur notandi valið ógreiddan eða að hluta greiddan reikning og síðan valið **Borga reikning**. Valinn reikningur er settur í körfuna og notandi getur haldið áfram með greiðslu. Notandi getur síðan ákveðið hvort hann greiðir alla upphæð reikningsins eða hlutafjárhæð. Notandinn getur ekki notað inneignargreiðslumáta til að greiða fyrir reikninga.

> [!NOTE]
> Einungis er hægt að bæta reikningum í körfuna ef engir hlutir eru í henni. Aftur á móti er aðeins hægt að bæta vörum í körfuna ef engir reikningar eru í henni. Microsoft ætlar að fjarlægja þessa takmörkun í framtíðarútgáfum viðskipta.

![Körfusíðu á B2B vefsíðu.](../media/PayInvoice.png)

Á **Reikningar** síðu getur notandi einnig valið **Óska eftir reikningi** við hlið reiknings. Þannig getur notandinn óskað eftir því að fá upplýsingar um reikninginn sendar á skráð netfang.

![Beiðni um reikningsglugga.](../media/RequestInvoice2.png)

Eftir að notandi hefur óskað eftir reikningi er beiðnin færð á **B2B beiðnir** kafla í **Minn reikningur** síðu. Síðan, eftir **P-0001** og **Samstilltu pantanir og rásbeiðnir** störf eru keyrð í höfuðstöðvum Commerce, reikningspósturinn er ræstur og staða B2B beiðninnar er merkt sem lokið.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

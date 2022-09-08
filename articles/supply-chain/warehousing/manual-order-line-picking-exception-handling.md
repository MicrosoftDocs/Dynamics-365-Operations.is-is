---
title: Meðhöndla handvirkt undantekningar frá sölu og flutningslínutínslu
description: Þessi grein lýsir því hvernig stjórnendur geta handvirkt valið (eða afvalið) birgðafærslur til að laga vandamál sem stafa af skemmdum sölu- og millifærslupöntunargögnum.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404428"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Meðhöndla handvirkt undantekningar frá sölu og flutningslínutínslu

[!include [banner](../includes/banner.md)]

Handvirk meðhöndlun á undantekningum frá sölu- og flutningslínutínslu gerir stjórnendum kleift að laga vandamál sem stafa af skemmdum sölu- og flutningspöntunargögnum. Það gerir traustum notendum kleift að velja handvirkt (eða aftína) birgðafærslur sem tengjast sölu- og millifærslupöntunarlínum á meðan vöruhúsaferli eru þegar í gangi.

Virknin sem lýst er hér ætti aðeins að nota í þeim tilfellum þar sem kerfið getur ekki klárað að vinna úr vöruhúsaferlum á venjulegan hátt. Sjálfgefið er að aðeins notendur sem hafa kerfisstjórahlutverk mega nota það. Hins vegar geturðu veitt aðgang að því með því að úthluta *Veldu sölulínur handvirkt* forréttindi til annarra hlutverka eins og þú þarfnast.

## <a name="turn-on-this-feature-for-your-system"></a>Kveikja á þessum eiginleika fyrir kerfið

Áður en þú getur notað eiginleikana sem lýst er í þessari grein verður að kveikja á þeim í kerfinu þínu. Stjórnendur geta notað [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) stillingar til að athuga stöðu eiginleika og kveikja á þeim. Í **Eiginleikastjórnun** vinnusvæði, eru eiginleikarnir skráðir með eftirfarandi nöfnum:

- *Handvirk tiltektarþjónusta sölulínu fyrir stjórnanda eða aðra trausta notendur*<br>(Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur og ekki hægt að slökkva á honum.)
- *Handvirk tiltektarþjónusta flutningslínu fyrir stjórnanda eða aðra trausta notendur*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Leiðrétta færslur sem tengjast sölu- eða millifærslupöntunarlínum

Notaðu eftirfarandi ferli til að leiðrétta færslur sem tengjast sölu- eða millifærslupöntunarlínum.

1. Fylgdu einu af þessum skrefum, allt eftir tegund pöntunar sem þú verður að leiðrétta:

    - Til að leiðrétta færslu sem tengist sölupöntun er farið á **Vöruhússtjórnun \> Reglubundin verkefni \> Hreinsaðu til \> Veldu sölulínu handvirkt**.
    - Til að leiðrétta færslu sem tengist millifærslupöntun, farðu á **Vöruhússtjórnun \> Reglubundin verkefni \> Hreinsaðu til \> Veldu flutningslínur handvirkt**.

1. Á **Veldu sölulínur handvirkt** eða **Veldu flutningslínur handvirkt** síðu, notaðu síurnar efst á ristinni til að finna línuna sem þú ert að leita að og veldu síðan markpöntunarlínuna í efri hnitanetinu.
1. Nota **Birgðaviðskipti**, **·**, **og** **Gámalínur** flipa í neðri hlutanum til að skoða frekari upplýsingar um valda línu. Upplýsingarnar á þessum flipum gefa grunnyfirlit yfir tengd vöruhúsaferli og stöðu þeirra.
1. Á aðgerðarrúðunni velurðu **Velja** til að opna valda pöntunarlínu á **Velja** síðu fyrir birgðafærslur. Þú getur lokið þessu skrefi jafnvel fyrir pöntunarlínur sem þegar hafa verið losaðar í vöruhúsið. (Venjulega er ekki hægt að opna pöntunarlínur sem hafa verið losaðar í vöruhúsið á **Velja** síðu.)

    > [!NOTE]
    > Þú gætir fengið ýmsar viðvaranir þegar þú opnar **Velja** síðu. Gríptu til allra aðgerða sem þessar viðvaranir mæla með. Til dæmis gætir þú fengið viðvörun um pöntunarlínur sem eru tengdar vöruhúsavinnu. Í þessu tilviki er skynsamlegt að reyna að hætta við verkið með því að nota staðalinn [hætta við vinnu](cancel-warehouse-work.md) virkni áður en þú gerir handvirka leiðréttingu.

1. Veldu línuna í **Viðskipti** rist og veldu síðan **Bæta við tínslulínu** á **Viðskipti** tækjastiku.
1. Valin lína er færð í **Að velja línur** rist. Stilltu viðeigandi gildi fyrir alla dálka sem vantar nauðsynlegar upplýsingar. (Til dæmis, tilgreindu staðsetningu og númeraplötu sem hlutinn ætti að vera valinn af.)
1. Veldu **Staðfestu að velja allt** á **Að velja línur** tækjastiku.

## <a name="correct-load-line-quantities"></a>Rétt magn hleðslulína

Notaðu eftirfarandi aðferð til að leiðrétta magn hleðslulínu.

1. Fylgdu einu af þessum skrefum, allt eftir tegund pöntunar sem þú verður að leiðrétta:

    - Til að leiðrétta færslu sem tengist sölupöntun er farið á **Vöruhússtjórnun \> Reglubundin verkefni \> Hreinsaðu til \> Veldu sölulínu handvirkt**.
    - Til að leiðrétta færslu sem tengist millifærslupöntun, farðu á **Vöruhússtjórnun \> Reglubundin verkefni \> Hreinsaðu til \> Veldu flutningslínur handvirkt**.

1. Á **Veldu sölulínur handvirkt** eða **Veldu flutningslínur handvirkt** síðu, notaðu síurnar efst á ristinni til að finna línuna sem þú ert að leita að og veldu síðan markpöntunarlínuna í efri hnitanetinu.
1. Á **Hleðslulínur** flipann í neðri hlutanum, veldu **Leiðréttu hleðslulínur handvirkt** á tækjastikunni.
1. Á **Leiðréttu hleðslulínur handvirkt** síðu, í **Birgðaviðskipti** hnitanet, skoðaðu birgðafærslurnar sem tengjast völdum hleðslulínu.
1. Í efri ristinni skaltu leiðrétta hleðslulínumagnið í eftirfarandi dálkum eftir þörfum:

    - **Magn stofnaðrar vinnu**
    - **Tiltekið magn**
    - **Áætlað magn til dreifingar frá dreifingarstöð**

    Kerfið mun staðfesta allar breytingar sem þú gerir á þessum dálkum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

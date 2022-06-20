---
title: Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar
description: Þessi grein lýsir því hvernig á að bæta handritakóða við biðlarahlið við vefsíðurnar þínar til að styðja við söfnun á fjarmælingum viðskiptavinarhliðar.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 262216ee99d52e3d53f5f5dae663104bb79757c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852842"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að bæta handritakóða við biðlarahlið við vefsíðurnar þínar til að styðja við söfnun á fjarmælingum viðskiptavinarhliðar.

Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning. Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics. Flestir vefgreiningarpakkar krefjast þess að bætt sé við skriftarkóða biðlaramegin í einingu **\<head\>** í HTML fyrir allar síður á vefsvæðinu þínu.

> [!NOTE]
> Leiðbeiningarnar í þessari grein eiga einnig við um aðra sérsniðna virkni viðskiptavinarhliðar sem Microsoft Dynamics 365 Commerce býður ekki upp á native.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Stofnaðu endurnýtanlegt brot fyrir skriftarkóðann

Brot gerir þér kleift að endurnýta innfelldan eða ytri skriftarkóða á öllum síðum á svæðinu, óháð sniðmátinu sem er notað.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Búa til endurnýtanlegt brot fyrir innbyggðan skriftarkóða

Til að búa til endurnýtanlegt brot fyrir innbyggðan skriftarkóðann í svæðasmíði skal fylgja þessum skrefum.

1. Farðu í **Brot** og veldu síðan **Nýtt**.
1. Í svarglugganum **Nýtt brot** skal velja **Innfelld forskrift**.
1. Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.
1. Undir broti sem þú bjóst til skaltu velja **Sjálfgefin innfelld eining forskriftar**.
1. Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins. Stilltu síðan aðra valkosti eins og þú þarft.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Búa til endurnýtanlegt brot fyrir ytri skriftarkóða

Til að búa til endurnýtanlegt brot fyrir ytri skriftarkóða í svæðasmíði skal fylgja þessum skrefum.

1. Farðu í **Brot** og veldu síðan **Nýtt**.
1. Í svarglugganum **Nýtt brot** skal velja **Ytri forskrift**.
1. Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.
1. Í brotinu sem þú býrð til skaltu velja **Sjálfgefin ytri eining forskriftar**.
1. Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar. Stilltu síðan aðra valkosti eins og þú þarft.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

> [!NOTE]
> Ef öryggisregla fyrir efni (CSP) er virkjuð fyrir svæðið þitt, skaltu ganga úr skugga um að öllum ytri vefslóðum sé bætt við CSP-leiðbeininguna **script-src** í svæðishönnuð Commerce. Frekari upplýsingar er að finna í [Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Bæta við broti sem inniheldur skriftarkóða í sniðmát

Til að bæta við hluta sem inniheldur skriftarkóða í sniðmát í svæðasmíði skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.
1. Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.
1. Í **HTML-haus** skaltu velja hnapp úrfellingarmerkis (**...**) og svo **Bæta við broti**.
1. Veldu brotið sem þú bjóst til fyrir forskriftakóðann.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Bæta ytri eða innbyggðri forskrift beint við sniðmát

Ef ætlunin er að setja innfellda eða ytri forskrift beint inn í safn af síðum sem eru stýrðar með einu sniðmáti þarf ekki að búa fyrst til brotið.

### <a name="add-an-inline-script-directly-to-a-template"></a>Bæta innbyggðri forskrift beint við sniðmát

Fylgdu þessum skrefum til að bæta innbyggðri forskrift beint við sniðmát í vefsvæðishönnuði.

1. Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.
1. Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.
1. Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Í valmyndinni **Bæta við einingu** velurðu **Innbyggð forskrift**.
1. Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins. Stilltu síðan aðra valkosti eins og þú þarft.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

### <a name="add-an-external-script-directly-to-a-template"></a>Bæta ytri forskrift beint við sniðmát

Fylgdu þessum skrefum til að bæta ytri forskrift beint við sniðmát í vefsvæðishönnuði.

1. Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.
1. Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.
1. Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Í valmyndinni **Bæta við einingu** velurðu **Ytri forskrift**.
1. Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar. Stilltu síðan aðra valkosti eins og þú þarft.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Unnið með CSS hnekkiskrám](css-override-files.md)

[Bæta við táknmynd](add-favicon.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

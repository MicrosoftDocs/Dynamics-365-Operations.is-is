---
title: Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar
description: Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686815"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.

## <a name="overview"></a>Yfirlit

Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning. Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics. Flestir vefgreiningarpakkar krefjast þess að bætt sé við skriftarkóða biðlaramegin í einingu **\<head\>** í HTML fyrir allar síður á vefsvæðinu þínu.

> [!NOTE]
> Leiðbeiningarnar í þessu efni eiga einnig við um aðra sérsniðna virkni biðlara sem Microsoft Dynamics 365 Commerce býður ekki staðbundið.

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a>Stofnaðu endurnýtanlegt síðubrot fyrir forskriftarkóðann

Síðubrot gerir þér kleift að endurnýta innbyggðan eða ytri forskriftarkóða á öllum síðum á vefsvæði þínu, óháð sniðmátinu sem þeir nota.

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a>Stofna endurnýtanlegt síðubrot fyrir innbyggðan forskriftarkóðann

Fylgdu þessum skrefum til að búa til endurnýtanlegt blaðsíðubrot fyrir innbyggðan forskriftarkóðann.

1. Farðu í **Brot** og veldu síðan **Nýtt**.
1. Í svarglugganum **Nýtt síðubrot** skal velja **Innfelld forskrift**.
1. Undir **Heiti síðubrots** skal slá inn heiti brotsins og síðan velja **Í lagi**.
1. Undir síðubrotinu sem þú stofnaðir velurðu eininguna **Sjálfgefin innbyggð forskrift**.
1. Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins. Stilltu síðan aðra valkosti eins og þú þarft.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a>Stofna endurnýtanlegt síðubrot fyrir ytri forskriftarkóðann

Fylgdu þessum skrefum til að búa til endurnýtanlegt blaðsíðubrot fyrir ytri forskriftarkóðann.

1. Farðu í **Brot** og veldu síðan **Nýtt**.
1. Í svarglugganum **Nýtt síðubrot** skal velja **Ytri forskrift**.
1. Undir **Heiti síðubrots** skal slá inn heiti brotsins og síðan velja **Í lagi**.
1. Undir síðubrotinu sem þú stofnaðir velurðu eininguna **Sjálfgefin ytri forskrift**.
1. Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar. Stilltu síðan aðra valkosti eins og þú þarft.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a>Bættu síðubroti sem inniheldur forskriftakóða í sniðmát

Fylgdu þessum skrefum til að bæta við síðubroti sem inniheldur forskriftarkóða í sniðmát í vefsvæðishönnuði.

1. Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.
1. Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.
1. Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við síðubroti**.
1. Veldu brotið sem þú bjóst til fyrir forskriftakóðann.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Velja **Birta**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Bæta ytri eða innbyggðri forskrift beint við sniðmát

Ef þú vilt setja innbyggðar eða ytri forskriftir beint inn í mengi af síðum sem er stjórnað af einu sniðmáti þarftu ekki að búa til síðubrot fyrst.

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

[Bæta við opnunarkveðju](add-welcome-message.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

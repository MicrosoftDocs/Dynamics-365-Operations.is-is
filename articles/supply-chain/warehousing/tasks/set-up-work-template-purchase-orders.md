---
title: Setja upp vinnusniðmát fyrir innkaupapantanir
description: Þessi grein lýsir því hvernig á að setja upp einfalt vinnusniðmát til að nota þegar þú setur frá mótteknum hlutum.
author: Mirzaab
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee6bc896a979c326001e1596e4a463753005fabf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877364"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Setja upp vinnusniðmát fyrir innkaupapantanir

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp einfalt vinnusniðmát til að nota þegar þú setur frá mótteknum hlutum. Vinnusniðmát ákvarða safn leiðbeiningarnar sem birtast starfsmanns vöruhús í farsíma þegar fluttar eru vörur frá móttöku svæði. Hægt er að nota þessi ferli með gögn sem eru nefnd í sýnigögn fyrirtækisins USMF. Áður en byrjað er í þessari handbók, stofna kenni vinnuhóps. Í þessu dæmi er kenni vinnuhóps kallað inn í Á innleið notað. Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.

1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vinna > Vinnusniðmát**.
2. Í reitnum **Gerð verkbeiðni** velurðu **Innkaupapantanir**.

## <a name="create-a-work-template-header"></a>Stofna haus fyrir sniðmát verks
1. Veljið **Nýtt**.
2. Í reitinn **Raðnúmer** skal slá inn númer. Þetta er númeraröð sem vinnusniðmát eru metnar fyrir. Hægt er að breyta röð, ef þörf krefur.  
3. Í reitnum **Vinnusniðmát** skal færa inn gildi. Þetta er einkvæmt kenni fyrir sniðmátið.  
4. Í reitinn **Lýsing vinnusniðmáts** skal færa inn gildi.
    - Valkosturinn **Gildir** verður ekki athugaður fyrr en þú hefur lokið við allar upplýsingar sem þörf er á í sniðmátinu og hefur valið **Vista**.  
    - Verkbeiðni af gerðinni **Innkaupapöntun** er ekki hægt að vinna sjálfkrafa, hafðu því valkostinn **Vinna sjálfkrafa** stilltan á **Nei**.  
5. Í reitinn **Kenni vinnuhóps** skal færa inn gildi. Hægt er að nota kenni vinnuhópa til að skipuleggja vinnu í flokka. Gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem er stofnuð með þessu sniðmáti.  
6. Í svæðinu **Vinnuforgangur** færirðu inn `1`. Þetta tilgreinir mikilvægi vinnu og gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem eru stofnaðir með þessu sniðmáti.  
7. Veljið **Vista**. Vista verður haus vinnusniðmáts áður en hnappurinn **Breyta fyrirspurn** verður tiltækur.  

## <a name="set-up-the-query-for-the-work-template"></a>Setja upp fyrirspurn fyrir vinnusniðmátið
1. Veldu **Breyta fyrirspurn**. Við setjum takmörkun þannig að sniðmátið getur einungis verið notuð í ákveðnu vöruhúsi.  
2. Veljið **Bæta við**.
3. Í reitnum **Reitur** í nýju línunni slærðu inn `warehouse`.
4. Í reitnum **Skilyrði** skal slá inn gildi.
5. Veljið **Í lagi**.
6. Velja skal **Já**.

## <a name="set-work-template-details"></a>Stilla upplýsingar vinnusniðmáts
1. Veljið **Nýtt**.
2. Í reitnum **Vinnutegund** velurðu **Tína**.
3. í reitinn **Kenni vinnuklasa** slærðu inn `purchase`. Vinnuklasa sem valin er hér verður sjálfkrafa í öllum vinnulínum af gerðinni Tiltekt sem eru stofnaðir með þessu sniðmáti. Vinnuklasinn er ekki hægt að hnekkja frá vinnu pöntunarlínur. Vinnuklasar eru notaðir til að beina og/eða takmarka gerð vinnupöntunarlínur sem starfsmanns vöruhús getur vinna í farsíma.  
4. Veljið **Nýtt**.
5. Í reitnum **Verkbeiðni** velurðu **Frágangur**.
6. Í reitinn **Kenni vinnuklasa** skal færa inn gildi. Tiltekt og frágangs leiðbeiningar eru stilltar. Tiltektar-/frágangspör verða að hafa sama vinnuklasa. Notið sama vinnuklasa sem fram voru lögð fyrir tiltektarfyrirmæli.  
7. Veljið **Vista**. Athugaðu að núna er merkt í gátreitinn **Gildir**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
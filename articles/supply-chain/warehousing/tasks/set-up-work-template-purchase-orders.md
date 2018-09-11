--- 
title: "Setja upp vinnusniðmát fyrir innkaupapantanir"
description: "Þetta ferli leggur áherslu á setja upp einfaldar vinnusniðmáts sem nota á þegar taka á frá mótteknar vörur."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Setja upp vinnusniðmát fyrir innkaupapantanir

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leggur áherslu á setja upp einfaldar vinnusniðmáts sem nota á þegar taka á frá mótteknar vörur. Vinnusniðmát ákvarða safn leiðbeiningarnar sem birtast starfsmanns vöruhús í farsíma þegar fluttar eru vörur frá móttöku svæði. Hægt er að nota þessi ferli með gögn sem eru nefnd í sýnigögn fyrirtækisins USMF. Áður en byrjað er í þessari handbók, stofna kenni vinnuhóps. Í þessu dæmi er kenni vinnuhóps kallað inn í Á innleið notað. Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.

1. Fara í vöruhúsakerfi  > Uppsetning  > Vinna  > Vinnusniðmát.
2. Í reitnum Verkbeiðni velurðu „Innkaupapantanir“.

## <a name="create-a-work-template-header"></a>Stofna haus fyrir sniðmát verks
1. Smellið á „Nýtt“.
2. Í reitinn raðnúmer skal slá inn númer.
    * Þetta er númeraröð sem vinnusniðmát eru metnar fyrir. Hægt er að breyta röð, ef þörf krefur.  
3. Færa inn gildi í reitnum Vinnusniðmát.
    * Þetta er einkvæmt kenni fyrir sniðmátið.  
4. Færa inn gildi í reitnum lýsingu Vinnusniðmáts.
    * Gildur valkostur ekki athugaður þar til þú hefur verið lokið allar upplýsingar sem þörf er á í sniðmáti og ert búinn að smellt á Vista.  
    * Vinnupöntun af gerðinni Innkaupapöntun er ekki hægt að vinna sjálfkrafa, hafðu því valkostinn vinna sjálfkrafa stillt á nei.  
5. Færa inn gildi í reitnum Kenni Vinnuhóp .
    * Hægt er að nota kenni vinnuhópa til að skipuleggja vinnu í flokka. Gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem er stofnuð með þessu sniðmáti.  
6. Í svæðinu forgangur Vinnu, færið inn '1'.
    * Þetta tilgreinir mikilvægi vinnu og gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem eru stofnaðir með þessu sniðmáti.  
7. Smellið á „Vista“.
    * Vista verður haus vinnusniðmáts áður en að Breyta Fyrirspurn hnappurinn verður tiltækur.  

## <a name="set-up-the-query-for-the-work-template"></a>Setja upp fyrirspurn fyrir vinnusniðmátið
1. Smellt er á Breyta fyrirspurn.
    * Við setjum takmörkun þannig að sniðmátið getur einungis verið notuð í ákveðnu vöruhúsi.  
2. Smelltu á Bæta við.
3. Í listanum skal merkja valda línu.
4. Í svæði Svæðið, færa inn "vöruhúsið".
5. Í reitinn Skilyrði skal slá inn gildi.
6. Smellið á „Í lagi“.
7. Smella á Já.

## <a name="set-work-template-details"></a>Stilla upplýsingar vinnusniðmáts
1. Smellið á „Nýtt“.
2. Veljið í svæðinu vinnutegund 'Taka'.
3. í Kenni Vinnuklasa svæðið  færðu inn 'innkaupa'.
    * Vinnuklasa sem valin er hér verður sjálfkrafa í öllum vinnulínum af gerðinni Tiltekt sem eru stofnaðir með þessu sniðmáti. Vinnuklasinn er ekki hægt að hnekkja frá vinnu pöntunarlínur. Vinnuklasar eru notaðir til að beina og/eða takmarka gerð vinnupöntunarlínur sem starfsmanns vöruhús getur vinna í farsíma.  
4. Smellið á „Nýtt“.
5. Í reitnum Vinnutegund velurðu ‚Frágangur‘.
6. Færa inn gildi í reitnum Kenni Vinnuklasa .
    * Tiltekt og frágangs leiðbeiningar eru stilltar. Tiltektar-/frágangspör verða að hafa sama vinnuklasa. Notið sama vinnuklasa sem fram voru lögð fyrir tiltektarfyrirmæli.  
7. Smellið á „Vista“.
    * Athugið að Gilt gátreitinn er nú merkt.  



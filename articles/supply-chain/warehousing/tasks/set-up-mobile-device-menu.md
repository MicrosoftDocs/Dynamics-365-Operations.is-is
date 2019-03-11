---
title: Setja upp valmyndaratriði fartækis til að ljúka vinnu af gerðinni innkaupapöntun
description: Þessi verklýsing sýnir hvernig á að setja upp valmyndaratriði fartækis.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 326a0039d2769ee5f459a87c302c93604d2379aa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "337556"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Setja upp valmyndaratriði fartækis til að ljúka vinnu af gerðinni innkaupapöntun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp valmyndaratriði fartækis. Í þessu dæmi er Þetta valmyndaratriði notuð til að framkvæma vinnu með gerðinni innkaupapöntun. Vinnuklasi sem er tengdur við valmyndaratriði ákvarðar hvaða vinna er gild. Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF. Þetta ferli er yfirleitt framkvæmt af stjórnandi vöruhúss.


## <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis
1. Fara í valmyndaratriði fartækis
2. Smellið á „Nýtt“.
3. Í svæðið heiti valmyndaratriðis, færa inn gildi.
    * Færa skal inn einkvæmt gildi. Til dæmis væri hægt að slá inn flutningur pöntunar. Muna skal gildi, Þú þarft það síðar.  
4. Í reitinn Titill skal slá inn gildi.
    * Þetta er titillinn sem birtist í fartækinu. Til dæmis væri hægt að slá inn ‚flutningur pöntunar‘.  
5. Í reitnum Stilling velurðu „Vinna“.
6. Velja skal Já í Nota fyrirliggjandi vinnu svæðinu.
    * Valmyndaratriði fartækis er notuð til að framkvæma fyrirliggjandi vinnu. Þess vegna verður að setja þetta gildi á Já.  
    * Birta stöðusvæði birgða ákvarðar hvort birgðastöðu á lager birtist vöruhús starfsmann í fartækinu.  
7. Í svæðinu Stýrt af, velja 'Kerfisflokkun'.
    * Þegar eitthvað er valið í reitnum Stýrt af, birtast viðbótarreitir í hlutanum Almennt á þessari síðu. Svæði sem birtast velta á því hvað er var valið. Þegar er valið Kerfisflokkun, er bætt við tvö ný svæði. Þær eru útskýrt hér að neðan  
8. Í kerfisflokkunarsvæði, veljið 'WorkPoolId'.
    * Þegar starfsmenn vöruhúss þetta valmyndaratriði opnar, þær verður beðnir um að skanna auðkenni vinnuhóps. Öll vinna pantanir með þetta Auðkenni vinnuhóps og opna vinnupöntunar línur með einni af vinnuklösum sem bætt er við þetta valmyndaratriði verður ýtt til notanda.  
9. Færa inn gildi í svæði merki kerfisflokkunar.
    * Textinn sem birtist fartækjanotandanum Til dæmis væri hægt að slá inn vinnuhópur.  
10. Velja Já í Hnekkingu númeraplötu við frágang svæðið .
    * Þessi valkostur gerir starfsmenn vöruhúss kleift að hnekkja marknúmeraplötunni þegar vörur eru settar á staðsetningu númeraplötustýrða.  
11. Velja skal Já í svæði frágangur Hóps.
    * Ef allar línur fyrir Frágangur á vinnupöntun deila sama staðsetningu, fær notandi einn sameinað Frágangur fyrirmæli fyrir allar línur.  
    * Endurskoðunarsniðmátskennið: endurskoðunarsniðmát fyrir vinnu gerir kleift að tilgreina að vinnuferli fyrir valmyndaratriði ætti að rjúfa þannig að annað aðgerð hægt að keyra. Til dæmis, ef þetta valmyndaratriði er fyrir vinnu á innleið gæti endurskoðunarsniðmátið krafist að starfsmaður athugi hitastig. Punktur ferlið rofin er tilgreindur fyrir endurskoðunarsniðmátið og getur til dæmis þegar vinna er hafin eða er lokið, eða þegar breytir stöðu hennar.  
12. Útvíkka hlutann vinnuklasar.
13. Smellið á „Nýtt“.
14. Í svæðinu auðkenni vinnuklasa, færðu inn 'innkaup'.
    * Vinnuhópinn takmarkar vinnu sem hægt er að nota valmyndaratriði fyrir. Í þessu tilfelli verður að nota hana fyrir opnar vinnupöntunarlínur sem hafa Innkaup vinnuklasi kenni.  
15. Smellið á „Vista“.

## <a name="set-up-work-confirmation"></a>Setja upp vinnustaðfestingu
1. Smellt er á Uppsetning verkstaðfestingar
2. Veljið í svæðinu vinnutegund 'Taka'.
3. Velja Sjálfvirkt staðfesta gátreitinn.
    * Leiðbeining fyrir vinnu með vinnugerð Tiltekt verður sjálfkrafa staðfestar. Þessi fyrirmæli verða ekki sýnd notandanum.  
4. Smellið á „Nýtt“.
5. Í reitnum Vinnutegund velurðu ‚Frágangur‘.
6. Veljið gátreitinn fyrir staðfestingu á Staðsetningu.
    * Starfsmaður í vöruhúsi er beðinn um að framkvæma staðfestingu skönnun staðsetningu þegar varan er sett niður.  
7. Smellið á „Vista“.
8. Lokið síðunni.
9. Lokið síðunni.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Bæta valmyndaratriði við valmynd fartækis
1. Fara í valmyndina Fartæki
2. Smellið á „Breyta“.
3. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Heiti með gildinu 'á innleið'.
    * Óskað er að finna valmynd að nota fyrir valmyndaratriði á innleið. Í USMF, þessi reitur er kallaður á innleið.  
4. Í trénu skal velja „gildi“.
5. Smella á ör sem vísar til hægri.
6. Smellið á „Vista“.
7. Lokið síðunni.


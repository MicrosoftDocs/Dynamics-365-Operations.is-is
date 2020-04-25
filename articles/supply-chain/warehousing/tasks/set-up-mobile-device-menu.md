---
title: Setja upp valmyndaratriði fartækis til að ljúka vinnu af gerðinni innkaupapöntun
description: Þetta efni sýnir hvernig á að setja upp valmyndaratriði fartækis.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 905094ae4e76fadbebea1892ec20427f32e3e71d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216828"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Setja upp valmyndaratriði fartækis til að ljúka vinnu af gerðinni innkaupapöntun

[!include [banner](../../includes/banner.md)]

Þetta efni sýnir hvernig á að setja upp valmyndaratriði fartækis. Í þessu dæmi er Þetta valmyndaratriði notuð til að framkvæma vinnu með gerðinni innkaupapöntun. Vinnuklasi sem er tengdur við valmyndaratriði ákvarðar hvaða vinna er gild. Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF. Þetta ferli er yfirleitt framkvæmt af stjórnandi vöruhúss.


## <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis
1. Farðu í **Valmyndaratriði farsíma** með því að slá það inn í leitarstikuna.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti valmyndaratriðis** skal færa inn gildi. Færa skal inn einkvæmt gildi. Til dæmis væri hægt að slá inn `POMove`. Muna skal gildi, Þú þarft það síðar.  
4. Í reitinn **Titill** skal slá inn gildi. Þetta er titillinn sem birtist í fartækinu. Til dæmis væri hægt að slá inn `PO Move`.  
5. Í reitnum **Stilling** velurðu **Vinna**.
6. Velja skal **Já** í reitnum **Nota fyrirliggjandi vinnu**.
    - Valmyndaratriði fartækis er notuð til að framkvæma fyrirliggjandi vinnu. Þess vegna verður að setja þetta gildi á **Já**.  
    - Reiturinn **Birta birgðastöðu** ákvarðar hvort birgðastaða á lager verður birt starfskrafti í vöruhúsi í fartækinu.  
7. Í reitnum **Stýrt af** velurðu **Kerfisflokkun**. Þegar eitthvað er valið í reitnum **Stýrt af** birtast viðbótarreitir í hlutanum **Almennt** á þessari síðu. Svæði sem birtast velta á því hvað er var valið. Þegar er valið **Kerfisflokkun** er tveimur nýjum reitum bætt við. Þær eru útskýrt hér að neðan  
8. Í reitnum **kerfisflokkun** skaltu velja **WorkPoolId**. Þegar starfsmenn vöruhúss þetta valmyndaratriði opnar, þær verður beðnir um að skanna auðkenni vinnuhóps. Öll vinna pantanir með þetta Auðkenni vinnuhóps og opna vinnupöntunar línur með einni af vinnuklösum sem bætt er við þetta valmyndaratriði verður ýtt til notanda.  
9. Í reitinn **Merki kerfisflokkunar** skal færa inn gildi. Textinn sem birtist fartækjanotandanum Til dæmis væri hægt að slá inn **vinnuhópur**.  
10. Velja **Já** í reitnum **Hnekkja númeraplötu við frágang**. Þessi valkostur gerir starfsmenn vöruhúss kleift að hnekkja marknúmeraplötunni þegar vörur eru settar á staðsetningu númeraplötustýrða.  
11. Velja skal **Já** í reitnum **Frágangur hóps**.
    - Ef allar línur fyrir Frágangur á vinnupöntun deila sama staðsetningu, fær notandi einn sameinað Frágangur fyrirmæli fyrir allar línur. 
    - Endurskoðunarsniðmátskennið: endurskoðunarsniðmát fyrir vinnu gerir kleift að tilgreina að vinnuferli fyrir valmyndaratriði ætti að rjúfa þannig að annað aðgerð hægt að keyra. Til dæmis, ef þetta valmyndaratriði er fyrir vinnu á innleið gæti endurskoðunarsniðmátið krafist að starfsmaður athugi hitastig. Punktur ferlið rofin er tilgreindur fyrir endurskoðunarsniðmátið og getur til dæmis þegar vinna er hafin eða er lokið, eða þegar breytir stöðu hennar.  
12. Útvíkkaðu hlutann **Vinnuklasar**.
13. Veljið **Nýtt**.
14. í reitinn **Kenni vinnuklasa** slærðu inn `Purchase`. Vinnuhópinn takmarkar vinnu sem hægt er að nota valmyndaratriði fyrir. Í þessu tilfelli verður að nota hana fyrir opnar vinnupöntunarlínur sem hafa Innkaup vinnuklasi kenni.  
15. Veljið **Vista**.

## <a name="set-up-work-confirmation"></a>Setja upp vinnustaðfestingu
1. Veldu **Uppsetning vinnustaðfestingar**.
2. Í reitnum **Vinnutegund** velurðu **Tína**.
3. Veldu gátreitinn **Staðfesta sjálfvirkt**. Leiðbeining fyrir vinnu með vinnugerð Tiltekt verður sjálfkrafa staðfestar. Þessi fyrirmæli verða ekki sýnd notandanum.  
4. Veljið **Nýtt**.
5. Í reitnum **Vinnutegund** velurðu ‚Frágangur‘.
6. Veljið gátreitinn **Staðfesting staðsetningar**. Starfsmaður í vöruhúsi er beðinn um að framkvæma staðfestingu skönnun staðsetningu þegar varan er sett niður.  
7. Veljið **Vista**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Bæta valmyndaratriði við valmynd fartækis
1. Farðu í valmyndina **Fartæki** með því að slá það inn í leitarstikuna.
2. Veljið **Breyta**.
3. Nota flýtiafmörkun til að finna færslur Til dæmis, sía í reitnum **Heiti** með gildinu **á innleið**. Óskað er að finna valmynd að nota fyrir valmyndaratriði á innleið. Í USMF er þetta kallað **á innleið**.  
4. Í trénu skal velja **gildi**.
5. Veldu örina sem vísar til hægri.
6. Veljið **Vista**.
7. Lokið síðunni.

---
title: Setja upp aðskilnaður á skyldum
description: Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688174"
---
# <a name="set-up-segregation-of-duties"></a>Setja upp aðskilnaður á skyldum

[!include [banner](../../includes/banner.md)]

Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum. Þetta hugtak er kallað Aðskilnaður á skyldum. Til dæmis gætirðu viljað að sama manneskjan staðfesti ekki bæði móttöku á vörum og vinni úr greiðslu til lánardrottins. Aðskilnaður á skyldum hjálpar við að minnka áhætta á svikum og það hjálpar einnig við að greina villur. Þú getur einnig notað aðskilnað á skyldum til að lögbinda reglur um innra eftirlit. Ljúktu við eftirfarandi ferli til að stofna reglu. Þú verður að vera kerfisstjóri til að ljúka ferlinu. Sýnigögn gögn fyrirtækisins til að stofna þetta ferli er DAT. 

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Reglur varðandi aðskilnaði á skyldum.**
2. Smellt er á **Nýtt**.
3. Í reitinn **Nafn** skal skrá inn gildi fyrir regluna.
4. Í reitnum **Fyrsta skylda** skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Veljið fyrstu skyldu sem er stýrt af reglunni.
6. Í reitnum **Önnur skylda** skal smella á fellilistahnappinn til að opna leitina. 
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Veljið aðra skyldu sem er stýrt af reglunni.
10. Í reitnum **Villustig** skal velja valkost. Veljið villustig áhættu sem gerist þegar sama notandi eða hlutverk framkvæmir báðar skyldur.  
11. Í reitinn **Öryggishætta** skal slá inn gildi. Færið inn lýsingu á áhættu.  
12. Í reitinn **Mótvægisaðgerðir öryggis** skal slá inn gildi. Færið inn lýsingu á aðgerðum sem eru teknar til að minnka þá áhættu. Til dæmis er hægt að draga úr hættunni með framkvæmd ítarlegri yfirferða á ferlinu, með framkvæmd á mánaðarlegri rekstraryfirferð eða með því að samnýta tilföng með öðrum deildum.     
13. Smellt er á **Vista**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
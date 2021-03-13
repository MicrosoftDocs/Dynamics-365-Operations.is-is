---
title: Úthlutun og hnekking virðisaukaskatts
description: Þetta ferli sýnir hvernig á að úthluta VSK-flokkur á viðskiptarásir.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c6e1de5046a3ce5d896ba3686a28d6d474d4268
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020729"
---
# <a name="sales-tax-assignment-and-overrides"></a>Úthlutun og hnekking virðisaukaskatts

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að úthluta VSK-flokkur á viðskiptarásir. Hún á fer einnig í gegnum ferlið við að stofna nýja hnekking virðisaukaskatts og úthluta henni á fyrirliggjandi hnekkingarflokkur virðisaukaskatts. Þetta ferli notar sýnigögn fyrirtæki USRT.

1. Fara í Retail og Commerce > Rásir > Verslanir > Allar verslanir.
2. Á listanum, smella á tengil fyrir kenni rásar fyrir „Houston”.
3. Smella á Breyta.
    * VSK-flokk reiturinn inniheldur lista yfir VSK-flokka fyrir núverandi fyrirtæki. Núverandi úthlutaður flokkur er almennur "Texas VSK-flokkur". Einnig eru til vsk-flokkar fyrir „Washington" og "Washington, King County.“ Vsk-flokkar geta verið með viðeigandi skatta fyrir mörg sveitarfélög.  
    * Reiturinn "hnekking virðisaukaskatts" er þar sem hægt er að varpa hnekkingarflokka söluskatts á rásinni. Hægt er að nota hnekkingarflokkur virðisaukaskatts til að flokka saman hnekkingar söluskatts sem starfa fyrir margar verslanir. Frekar en að úthluta handvirkt hnekkingum virðisaukaskatts einum í einum, er hægt að stofna flokkinn og úthluta beint á rásirnar til að spara tíma.  
4. Smelltu á Vista.
5. Lokið síðunni.
6. Fara í Retail og Commerce > Uppsetning rásar > VSK > VSK hnekkja.
7. Smellið á „Nýtt“.
8. Í reitnum hnekking virðisaukaskatts, gefðu nafn fyrir nýju hnekkinguna þína.
9. Í reitinn Lýsing er færð stutt lýsing á hnekkingunni.
10. Stilla stöðu á "Virkja".
11. Stækka eða fella saman hlutann Hnekkja.
12. Veljið valkost í svæðinu tegund.
    * Vsk-flokka vöru er hægt að nota til að hnekkja skatti fyrir tilteknar vörur sem tilheyrir þeim flokki. T.d. er matvara yfirleitt skattlögð öðruvísi en efnislegar vörur og eru líklega með sinn eigin vsk-flokk. Vsk-flokkar eru flokkar skatta sem eiga við tiltekinni rás. Til dæmis ef rás selur bæði í smásölu og milli fyrirtækja, gætu mismunandi vsk-flokka verið notaðir. Allar viðeigandi skatta myndi vera varpað á vsk-flokki.  
    * Nú er hægt að velja á "Frá" og "Til" skatta eða "Frá skattflokki" og "Til skattflokks" til að stofna hnekkingu virðisaukaskatts. "Frá" reiturinn tilgreinir skatta eða skattflokk sem á að hnekkja. Hnekking samkvæmt VSK-flokkur vöru veitir aðra valkosti en hnekking eftir VSK-flokkur. Hnekkingar virðisaukaskatts má setja upp til að hnekka sköttum á heilum færslum eða á tilteknum línum í færslu.  
13. Smelltu á Vista.
14. Lokið síðunni.
15. Fara í Retail og Commerce > Uppsetning rásar > VSK > VSK hnekkja flokkar.
    * Í þessu skrefi muntu úthluta nýstofnuð hnekkingu vsk á hnekkingarflokkur virðisaukaskatts sem er úthlutað á Houston rásina.  
16. Smellið á „Breyta“.
17. Útvíkka eða draga saman hlutann Setja upp.
18. Smelltu á Bæta við.
19. Í reitnum hnekking virðisaukaskatts skal smella á fellilistahnappinn til að opna leitina.
20. Veldu Hnekking virðisaukaskatts sem þú stofnaðir áður, úr listanum.
21. Í listanum skal smella á tengilinn í valinni línu.
22. Smellið á „Vista“.


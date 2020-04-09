---
title: Skilgreina samfelldniáætlanir
description: Þetta efnisatriði fer í gegnum uppsetningu samfelldniáætlanir (einnig þekkt sem endurteknar pantanir).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06fd1e23ad84fdc5e94e309717d5a96fbff45035
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140900"
---
# <a name="define-continuity-schedules"></a>Skilgreina samfelldniáætlanir

[!include [banner](../includes/banner.md)]

Þetta efnisatriði fer í gegnum uppsetningu samfelldniáætlanir (einnig þekkt sem endurteknar pantanir). Þessi aðferð notar sýnifyrirtækið USRT.


## <a name="create-continuity-program"></a>Stofna samfelldniáætlun
1. Fara í Retail og Commerce > Samfelldni > Samfelldniáætlanir.
2. Smellið á Nýtt.
3. Í reitinn kenni áætlunar, skal færa inn kenni samfelldniáætlunar.
4. Í reitnum upphaf pöntunar, veljið 'Fyrsta tilvik'.
    * Ef viðskiptavinur útbýr nýja pöntun fyrir samfelldniáætlanirnar, eru tveir valmöguleikar sem afurðin verður send fyrir: 1. Fyrsta tilvik: fyrsta afurð í samfelldniáætlun verður send.  2. Núverandi tilvik: núverandi vöru verður send. Til dæmis: þegar þrír mánuðir eru liðnir á áætlunina, fær viðskiptavinurinn þriðjung áætlunar.  
5. Velja 'Já' til að spyrja um upphafsdagsetning pöntunar.
6. Smellið á „Bæta við línu“.
7. Í svæðið númer sláið inn vörunúmerið fyrir fyrstu afurðarinnar ('0013').
8. Sláðu inn 'CP'.
9. Sláið inn dagsetningu þegar fyrstu afurð verða tiltækar til pöntunar.
10. Smella á bæta Við línu.
11. Í svæðið númers, færðu inn '0014'.
12. Í reitnum kóði dagsetningabils, hreinsa gildi þannig að svæðið er autt.
    * Hreinsa dagsetningarbil fyrir þetta ferli. Stilla verður dagsetningin sem stigvaxandi frá upphafsdagsetningu fyrstu vörunnar.  
13. Hér er fært inn millibilið sem vörur eru sendar á. Sláðu inn '30'.
    * Fyrir mánaðarlega áætlun, verður að færa inn 30 dagar fyrir bilið.  
14. Smellið á „Bæta við línu“.
15. Í svæðið númers, færðu inn '0015'.
16. Sláðu inn "Síðast".
17. Smellið á „Vista“.

## <a name="assign-to-continuity-item"></a>Úthlutið samfelldnivöru
1. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
2. Veldu afurð '0016'.
    * Fyrir þetta ferli, veljið vörunúmerið 0016. Yfirleitt hefurðu stofnað útgefna afurð sem notar aukalega samfelldni viðskiptagrunns þegar hún er sett í sölupöntun í símaveri.  
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smellið á „Breyta“.
5. Stækka eða fella saman hlutann Selja
6. Hér færirðu inn samfelldniáætlanirnar sem þessi afurð stendur fyrir. Færa inn Kenni áætlunar sem búið var til áður.
    * Þegar varan er seld í þjónustumiðstöð, er notuð viðbótar viðskiptagrunnur af hendi hins valda samfelldniáætlanirnar.  
7. Smellið á „Vista“.


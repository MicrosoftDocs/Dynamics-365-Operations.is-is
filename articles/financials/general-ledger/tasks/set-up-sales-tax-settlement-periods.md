---
title: Setja upp virðisaukaskatttímabil
description: Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur.
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "326194"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Setja upp virðisaukaskatttímabil

[!include [task guide banner](../../includes/task-guide-banner.md)]

Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur. Hægt er að keyra jöfnunarferli fyrir jöfnunartímabil fyrir tiltekin dagsetningarbil. Allar skattkóði sem tengist jöfnunartímabil verða jafnaðar. Eftir að setja upp tengd virðisaukaskattsyfirvald er skattskuld bókuð í annað hvort lánardrottinn eða fjárhagslykil.



Þetta verkefni notar USMF-sýnifyrirtækið.



1. Fara á Skattur > Óbeinir skattar > Virðisaukaskattur > VSK-uppgjörstímabil.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum jöfnunartímabil.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í yfirvalds svæði, velurðu virðisaukaskattsyfirvald sem tekur við skýrslan og greiðsla sem eru stofnaðar fyrir jöfnunartímabil.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum greiðsluskilmálar skal smella á fellilistahnappinn til að opna leitina.
    * Tengdar virðisaukaskattsyfirvald má setja upp sem lánardrottinn og virðisaukauppgjör mun stofna opnum lánardrottnareikningi. Greiðsluskilmálar skilgreina Gjalddaga fyrir the opinn reikningur lánardrottins.  
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Velja gerð fyrir tímabilum jöfnunartímabils.
12. Færið inn fjölda eininga fyrir tímabilið á hvert tímabil. Til dæmis ársfjórðungur hefur 3 mánuði.
13. Velja eða hreinsa Nota runuvinnslu fyrir gátreit fyrir virðisaukauppgjör.
    * Hægt er að vinna úr jöfnunarferlið fyrir tímabil sem runuvinnslu í bakgrunni. Þetta er ráðlagt fyrir mikinn fjölda skattafærslur innan tímabil.  
14. Veldu eða hreinsaðu gátreitinn „Koma í veg fyrir að mótfærsluskattafærslur myndist“.
    * Sjálfgefið framleiðir kerfið upp á mótfærsluskattafærslur við uppgjörsferlið, sem getur valdið frammistöðuvandamálum ef fjöldi skattafærslna er innan tímabils. Veljið þennan gátreit til að koma í veg fyrir að mótfærsluskattafærslur myndist.
15. Útvíkka flipanum tímabilum.
16. Smelltu á Bæta við.
17. Í listanum skal merkja valda línu.
18. Dagsetning er rituð í reitinn Frá dags.
19. Í reitinn Til dagsetningar skal slá inn dagsetningu.
20. Smellt er á Nýtt tímabil.
    * Þegar hefur verið fært inn fyrsta tímabilið, hægt að stofna ný tímabil sjálfkrafa. Hægt er að koma aftur og bæta við nýrri tímabilum eftir þörfum.  
21. Lokið síðunni.


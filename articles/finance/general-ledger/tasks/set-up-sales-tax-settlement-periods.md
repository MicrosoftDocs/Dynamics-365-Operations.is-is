---
title: Setja upp VSK-uppgjörstímabil
description: Þetta efni útskýrir hvernig á að setja upp uppgjörstímabil virðisaukaskatts í Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5972c44261a6ebd49df0fcbcef9a8c60aaa487e2
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144721"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Setja upp VSK-uppgjörstímabil

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að setja upp uppgjörstímabil virðisaukaskatts. Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur. Hægt er að keyra jöfnunarferli fyrir jöfnunartímabil fyrir tiltekin dagsetningarbil. Allar skattkóði sem tengist jöfnunartímabil verða jafnaðar. Eftir að setja upp tengd virðisaukaskattsyfirvald er skattskuld bókuð í annað hvort lánardrottinn eða fjárhagslykil.

Þetta verkefni notar USMF-sýnifyrirtækið.

1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Skattur > Óbeinir skattar > Virðisaukaskattur- > VSK-uppgjörstímabil**.
2. Veljið **Nýtt**.
3. Í reitinn **Uppgjörstímabil** skal færa inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Yfirvöld** velurðu virðisaukaskattsyfirvald sem tekur við skýrslan og greiðsla sem eru stofnaðar fyrir jöfnunartímabil.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í reitnum **Greiðsluskilmálar** velurðu skrána sem óskað er eftir af fellilistanum. Tengdar virðisaukaskattsyfirvald má setja upp sem lánardrottinn og virðisaukauppgjör mun stofna opnum lánardrottnareikningi. Greiðsluskilmálar skilgreina Gjalddaga fyrir the opinn reikningur lánardrottins.  
8. Velja gerð fyrir tímabilum jöfnunartímabils.
9. Færið inn fjölda eininga fyrir tímabilið á hvert tímabil. Til dæmis ársfjórðungur hefur 3 mánuði.
10. Velja eða hreinsa gátreitinn **Nota runuvinnslu fyrir virðisaukauppgjör**. Hægt er að vinna úr jöfnunarferlið fyrir tímabil sem runuvinnslu í bakgrunni. Þetta er ráðlagt fyrir mikinn fjölda skattafærslur innan tímabil.  
    > [!NOTE]
    > Sem stendur er ekki stutt á Spáni, Japan og Hollandi.
11. Veldu eða hreinsaðu gátreitinn **Koma í veg fyrir að mótfærsluskattafærslur myndist**. Sjálfgefið framleiðir kerfið upp á mótfærsluskattafærslur við uppgjörsferlið, sem getur valdið frammistöðuvandamálum ef fjöldi skattafærslna er innan tímabils. Veljið þennan gátreit til að koma í veg fyrir að mótfærsluskattafærslur myndist.
12. Útvíkkaðu flipann **Tímabil**.
13. Veljið **Bæta við**.
14. Í reitnum **Frá dags.** skal færa inn dagsetningu.
15. Í reitnum **Til dags.** færirðu inn dagsetningu.
16. Veldu **Nýtt afmörkunartímabil**. Þegar hefur verið fært inn fyrsta tímabilið, hægt að stofna ný tímabil sjálfkrafa. Hægt er að koma aftur og bæta við nýrri tímabilum eftir þörfum.  
17. Lokið síðunni.


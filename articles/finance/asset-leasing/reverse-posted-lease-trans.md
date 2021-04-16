---
title: Bakfæra bókaðar leigufærslur
description: Þetta efnisatriði útskýrir hvernig á að bakfæra bókuð leiguviðskipti. Hægt er að bakfæra allar færslur sem eru stofnaðar í gegnum Eignaleigu.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 955b4f71f5698cf2f482129f00c676d70f6cef9b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823048"
---
# <a name="reverse-posted-lease-transactions"></a>Bakfæra bókaðar leigufærslur

[!include [banner](../includes/banner.md)]

Hægt er að bakfæra allar færslur sem eru stofnaðar í gegnum Eignaleigu. Færslur sem eru bakfærðar gegnum Eignaleigu uppfæra gögn leigusamnings. Þar af leiðandi uppfæra þau einnig bókfært virði leiguskuldbindingarinnar og afnotarétt af eign.

Til að stofna bakfærslu fyrir leigu skal fylgja þessum skrefum.

1. Á annað hvort **eignafærslur** síðu eða **skuldafærslum** síðu, veljið færsluna og veljið svo **Bakfæra**.
2. Í svarglugganum sem birtist er hægt að breyta dagsetningunni þegar bakfærsla verður bókuð. Sjálfgefið er að reiturinn **Dagsetning** er stilltur á bókunardagsetningu færslunnar sem var valin. Ekki er hægt að bóka bakfærsluna á undan upphaflegu bókunardagsetningu valdrar færslu.
3. Veljið **Í lagi**. Færslubókarfærsla er bókuð sem bakfærir færslunni sem var valin. Bakfærslan er sýnd í **Eignafærslum** eða **skuldafærslum** síðu og nettósamtala núverandi stöðu sem birtist á síðunni er uppfærð.

Þegar valið er **Rakning bakfærslu** birtist svargluggi sem sýnir bæði upprunalegu færslurnar og bakfærðu færslurnar ásamt tengdu númeri sem er þekkt sem *rakningarnúmer*. Til að gera bakfærslurnar auðveldari að skilja og bæta sýnileika er einnig hægt að rekja bakfærslur með því að nota leiguáætlanir.

**Nýjasta færslubókarnúmer** í reitnum **Áætlun** sýnir færslubókarnúmer færslna. Þegar færsla er bakfærð er þessi reitur uppfærður með færslubókarnúmeri bakfærslu. Þar að auki er gátreiturinn **Bakfært** valinn til að gefa til kynna að færslan sé bakfærð og reiturinn **Bókað** er valinn.

## <a name="revoke-a-reversed-transaction"></a>Afturkalla bakfærða færslu

Til að afturkalla bakfærða færslu skal fylgja þessum skrefum.

1. Á annaðhvort síðunni **Áætlun** eða **Færslur** skal velja upprunalegu færsluna.
2. Fylgið einu af eftirfarandi skrefum:

    - Ef færslan var valin á **Áætlun** síðu skal fylgja skrefunum til að stofna færslubók í [stofna mánaðarlegar færslubókarfærslur í runu](create-monthly-journals-batch.md). Notandi þarf að bóka færslubókina handvirkt.
    - Ef færslan var valin á **Færslur** síðunni skal velja **Bakfæra**. Þú færð skilaboð sem segir til um að afturköllun sé afturkölluð fyrir fyrri bakfærslu og að þú getir breytt bókunardagsetningunni fyrir þessa afturköllun. Hins vegar hafa almennar viðskiptaprófanir áhrif á dagsetningarnar sem hægt er að færa inn í reitinn **Dagsetning**. 

3. Veljið **Í lagi**. Færslubókarfærsla er bókuð sem bakfærir færslunni sem var valin. Bakfærslan er sýnd á **Færslur** síðunni og núverandi staða nettósamtölu er endurheimt aftur í það sem hún var fyrir fyrstu bakfærsluna. Þess vegna hafa áhrifin sem bakfærslan hafði á stöðuna verið neituð.

Þegar valið er **Rekja bakfærslu** birtist svargluggi sem sýnir bæði upprunalegu færslurnar og bakfærðu færslurnar ásamt tengdu rakningarnúmeri.

Einnig er hægt að rekja afturköllun með því að nota viðeigandi **Áætlanir** síðu. Reiturinn **Bakfæra** er hreinsaður, en reitnum **Bókuð færslubók** er valinn. Þar að auki er reiturinn **Nýjasta færslubókarnúmerið** uppfærður með færslubókarnúmeri afturköllunar og **Færslubókarnúmer** reiturinn er uppfært með númeri bakfærslubókar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Greiðsluspár viðskiptavinar
description: Þetta efnisatriði lýsir getu greiðsluspár sem geta hjálpað notendum við að skilja betur dæmigerðar greiðsluvenjur viðskiptavinar. Þessi eiginleiki getur einnig komið í veg fyrir aðstæður þar sem innheimtuferli er hafið fyrr en annars væri byrjað á því.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f3d6f328ff3fd4da6ad3e7d4f3f751d3be692736
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713191"
---
# <a name="customer-payment-predictions"></a>Greiðsluspár viðskiptavinar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir getu greiðsluspár sem geta hjálpað notendum við að skilja betur dæmigerðar greiðsluvenjur viðskiptavinar. Þessi eiginleiki getur einnig komið í veg fyrir aðstæður þar sem innheimtuferli er hafið fyrr en annars væri byrjað á því.

## <a name="overview"></a>Yfirlit

Fyrirtækjum finnst oft krefjandi að spá fyrir um hvenær viðskiptavinir greiða reikninga sína. Þessi skortur á innsæi getur valdið eftirfarandi vandamálum:

- Minna nákvæm sjóðstreymispá
- Innheimtuferli sem byrja of seint
- Pantanir sem eru losaðar til viðskiptavinna sem kunna að greiða ekki

Greiðsluspár viðskiptavina hjálpa fyrirtækjum að spá fyrir um hvenær reikningur viðskiptavinar verður greiddur. Þess vegna er hægt að búa til innheimtuáætlanir sem þar sem líkurnar á greisðlu á réttum tíma eru auknar.

## <a name="predictions"></a>Spár

Greiðsluspár gera fyrirtækjum kleift að bæta viðskiptaferli sitt með því að hjálpa þeim að bera kennsl á reikninga sím líklegt er að séu greiddir seint. Fyrirtæki geta notað þessar upplýsingar til að grípa til aðgerða sem bæta líkurnar á því að reikningar verði greiddir á réttum tíma.

Greiðsluspár viðskiptavinar eiginleikinn notar vélnámslíkan til að spá betur fyrir um það hvenær viðskiptavinur mun greiða útistandandi reikning. Þetta vélnámslíkan inniheldur sögulega reikninga, greiðslur og gögn viðskiptavinar.

Aðgerðin úthlutar þremur greiðslulíkum fyrir hvern opinn reikning:

- Líkur á því að greiðslan berist á réttum tíma
- Líkur á því að greiðslan berist seint
- Líkur á því að greiðslan berist mjög seint

Þessi eiginleiki veitir einnig samandregið yfirlit yfir áætlaðar greiðslur.

[![Samanlögð sýn á spá um greiðslur.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Hverjum reikningi er úthlutað líkum á greiðslum á réttum tíma. Reikningar þar sem líkur á greiðslu á réttum tíma eru undir 50 prósent hafa rauðan hring til að gefa til kynna að innheimtufulltrúi ætti að líta á þá.

[![Listi yfir greiðslulíkur.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Greiðsluspá viðskiptavinar eiginleikinn veitir einnig samhengisupplýsingar til að útskýra spár. Þessar upplýsingar innihalda helstu þætti sem höfðu áhrif á spárnar, núverandi stöðu viðskipta við viðskiptavininn og upplýsingar um sögulega greiðsluhegðun viðskiptavinarins.

Í mörgum fyrirtækjum hefur innheimtuferlið verið viðbragðsþáttur. Með öðrum orðum hefst innheimtuferlið ekki fyrr en reikningar eru gjaldfallnir. Greiðsluspá viðskiptavinar gerir fyrirtækjum kleift að grípa fyrr til aðgerða vegna innheimtu. Þeir verða ekki lengur að bíða þess að færsla gjaldfalli til að hefja innheimtuferlið. Í staðinn geta þeir notað greiðsluspárgetuna til að ákvarða hvort fyrirbyggjandi innheimta muni bæta líkurnar á því að fá greitt á réttum tíma.

## <a name="methodology"></a>Aðferð

Það hefur yfirleitt reynst erfitt að þróa og nota gervigreindarlausn (AI). Þær hafa kallað á gagnavísindaVinnslan hefur krafist teymis sem inniheldur gögn vísindamanna, efnisorð (SMEs) og verkfræðinga, sem vinna með tíma til að móta, þróa, nota og viðhalda nothæfri AI-lausn. Greiðsluspá viðskiptavina gerir það auðvelt að dreifa og nota gervigreindarlausn í Microsoft Dynamics 365 Fjármál. Microsoft er að forpakka gervigreindarlausnir sem eru byggðar ofan á Microsoft AI Builder. Af þeim sökum geta notendur virkjað AI-lausnina með einum músarsmelli til að nýta kosti hugvitsamlegra spáa. Ef þú ert ekki sáttur við nákvæmni spár getur stórnotandi (aftur með einum músarsmelli) slegið inn AI Builder framlengingarupplifun, og veldu síðan eða hreinsaðu reitina sem eru notaðir til að búa til spár. Þegar þú ert tilbúinn getur þú „þjálfað“ líkanið og birt breytingarnar. Nýlega þjálfað líkanið verður sjálfkrafa tekið upp til að búa til spár í Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

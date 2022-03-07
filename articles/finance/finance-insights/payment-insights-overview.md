---
title: Greiðsluspár viðskiptavinar (forskoðun)
description: Þetta efnisatriði lýsir getu greiðsluspár sem geta hjálpað notendum við að skilja betur dæmigerðar greiðsluvenjur viðskiptavinar. Þessi eiginleiki getur einnig komið í veg fyrir aðstæður þar sem innheimtuferli er hafið fyrr en annars væri byrjað á því.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 398320726a5749f80584ba281095a5dbd668ae87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241339"
---
# <a name="customer-payment-predictions-preview"></a>Greiðsluspár viðskiptavinar (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði lýsir getu greiðsluspár sem geta hjálpað notendum við að skilja betur dæmigerðar greiðsluvenjur viðskiptavinar. Þessi eiginleiki getur einnig komið í veg fyrir aðstæður þar sem innheimtuferli er hafið fyrr en annars væri byrjað á því.

## <a name="overview"></a>Yfirlit

Fyrirtækjum finnst oft krefjandi að spá fyrir um hvenær viðskiptavinir greiða reikninga sína. Þessi skortur á innsæi getur valdið eftirfarandi vandamálum:

- Minna nákvæm sjóðstreymispá
- Innheimtuferli sem byrja of seint
- Pantanir sem eru losaðar til viðskiptavinna sem kunna að greiða ekki

Greiðsluspá viðskiptavinar (forskoðun) hjálpar fyrirtækjum að spá fyrir um hvenær reikningur viðskiptavinar verður greiddur. Þess vegna er hægt að búa til innheimtuáætlanir sem þar sem líkurnar á greisðlu á réttum tíma eru auknar.

## <a name="predictions"></a>Spár

Greiðsluspár gera fyrirtækjum kleift að bæta viðskiptaferli sitt með því að hjálpa þeim að bera kennsl á reikninga sím líklegt er að séu greiddir seint. Fyrirtæki geta notað þessar upplýsingar til að grípa til aðgerða sem bæta líkurnar á því að reikningar verði greiddir á réttum tíma.

Greiðsluspár viðskiptavinar eiginleikinn notar vélnámslíkan til að spá betur fyrir um það hvenær viðskiptavinur mun greiða útistandandi reikning. Þetta vélnámslíkan inniheldur sögulega reikninga, greiðslur og gögn viðskiptavinar.

Aðgerðin úthlutar þremur greiðslulíkum fyrir hvern opinn reikning:

- Líkur á því að greiðslan berist á réttum tíma
- Líkur á því að greiðslan berist seint
- Líkur á því að greiðslan berist mjög seint

Þessi eiginleiki veitir einnig samandregið yfirlit yfir áætlaðar greiðslur.

[![Samanlögð sýn á spá um greiðslur](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Hverjum reikningi er úthlutað líkum á greiðslum á réttum tíma. Reikningar þar sem líkur á greiðslu á réttum tíma eru undir 50 prósent hafa rauðan hring til að gefa til kynna að innheimtufulltrúi ætti að líta á þá.

[![Listi yfir greiðslulíkur](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Greiðsluspá viðskiptavinar eiginleikinn veitir einnig samhengisupplýsingar til að útskýra spár. Þessar upplýsingar innihalda helstu þætti sem höfðu áhrif á spárnar, núverandi stöðu viðskipta við viðskiptavininn og upplýsingar um sögulega greiðsluhegðun viðskiptavinarins.

Í mörgum fyrirtækjum hefur innheimtuferlið verið viðbragðsþáttur. Með öðrum orðum hefst innheimtuferlið ekki fyrr en reikningar eru gjaldfallnir. Greiðsluspá viðskiptavinar gerir fyrirtækjum kleift að grípa fyrr til aðgerða vegna innheimtu. Þeir verða ekki lengur að bíða þess að færsla gjaldfalli til að hefja innheimtuferlið. Í staðinn geta þeir notað greiðsluspárgetuna til að ákvarða hvort fyrirbyggjandi innheimta muni bæta líkurnar á því að fá greitt á réttum tíma.

## <a name="methodology"></a>Aðferð

Það hefur yfirleitt reynst erfitt að þróa og nota gervigreindarlausn (AI). Þær hafa kallað á gagnavísindaVinnslan hefur krafist teymis sem inniheldur gögn vísindamanna, efnisorð (SMEs) og verkfræðinga, sem vinna með tíma til að móta, þróa, nota og viðhalda nothæfri AI-lausn. Greiðsluspá viðskiptavinar auðveldar uppsetningu og notkun á AI lausn í Microsoft Dynamics 365 Finance. Microsoft er með innifaldar AI-lausnir sem eru byggðar ofan á Microsoft AI Builder. Af þeim sökum geta notendur virkjað AI-lausnina með einum músarsmelli til að nýta kosti hugvitsamlegra spáa. Ef notandi er ekki ánægður með nákvæmni spáa getur yfirnotandi (aftur með einum smelli) farið inn í viðbótina AI Builder og síðan valið eða afvalið reitina sem notaðir eru til að mynda spár. Þegar þú ert tilbúinn getur þú „þjálfað“ líkanið og birt breytingarnar. Nýþjálfaða líkanið verður sjálfkrafa valið til að mynda spár í Dynamics 365 Finance.

## <a name="release-details"></a>Upplýsingar um losun

Almenn forskoðun Fjármálainnsýnar er í boði fyrir uppsetningar í Bandaríkjunum, Evrópu og Bretlandi. Microsoft er að bæta við stuðningi fyrir fleiri svæði.

Aðeins ætti að kveikja á opinberum forskoðunaraðgerðum í sandkassaumhverfi í lagi 2. Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru hugsanlega ekki hægt að flytja yfir í vinnsluumhverfi. Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
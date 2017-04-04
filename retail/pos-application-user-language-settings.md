---
title: "POS forritið og stillingar notandatungumáls"
description: "Þetta efnisatriði lýsir hvernig á að breyta stillingum tungumál í Skýinu POS og Retail Modern POS (MPOS)."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>POS forritið og stillingar notandatungumáls

Þetta efnisatriði lýsir hvernig á að breyta stillingum tungumál í Skýinu POS og Retail Modern POS (MPOS).

<a name="overview"></a>Yfirlit
========

Retail Modern POS (MPOS) og Skýið POS styður umhverfi þar sem stillingum tungumáls og þýðingar getur misjafnar stillingar verslun og notanda. Til dæmis gæti verslunarinnar vera staðsett í svæði þar sem Enska er algengasta þeirra viðskiptavina, en sumir starfsmenn stilltu sem nota forritið með Frönsku þýðingar.

## <a name="data-language"></a>Gagnamál
Óháð stillingum notanda, MPOS- og Skýi POS verður alltaf nota verslunarinnar tungumál stillingar til að ákvarða þýðingar notuð fyrir gögn. Þetta verður tryggja að notendur og viðskiptavinir verða hafi samræmd reynslu.  Dæmi um gagna eru:

-   Vörur
-   Eigindi og gildi
-   Flokkaheiti
-   Prentaðar eða senda færslukvittanir í tölvupósti
-   Heiti greiðsluhátta
-   Línubirting skilaboða

Tungumál verslunarinnar verður einnig notuð fyrir aðallykil innskráningu skjánum Sölustaður, þar sem notandinn er ekki þekkt áður en skráð er. Ef inn þýðingu er ekki tiltækur fyrir tungumálið verslunarinnar Sölustaðnum snúa tungumáli fyrirtækisins.

### <a name="configuring-the-stores-language-setting"></a>Skilgreining tungumálastillingar verslunarinnar

Tungumálastilling verslunarinnar stillt úr **Allar smásöluverslanir** á í **Retail Store** síðuna undir ** Almennt &gt;Svæðisstillingar &gt;Tungumál. ** Nota skal niður til að velja tungumál fyrir hverja verslun.

## <a name="user-interface-language"></a>Tungumál notandaviðmóts
Tungumálastilling POS notanda ákvarðar þýðingar notaður í forritinu notendaviðmótinu. Þar á meðal allar merki valmyndir og birtir sem teljast gögn. Einn undantekningin er textinn sem birtist á Sölustað hnappahnita. Hnappahnit ekki styðja þýðingar, svo þær ætíð texta sem skilgreind er á hnappinn. Til að styðja þýdd hnappa, verður að hafa til að afrita og vinna með aðskildum hnappahnit og úthluta þeim á notendur eftir þörfum.

### <a name="configuring-the-users-language-setting"></a>Skilgreining tungumálastillingar notanda

Tungumálastilling POS notanda stillt úr **Allir starfsmenn** á í **Starfsmanns** síðuna undir **Retail &gt;Tungumál**.  Það er ekki stillt á flipanum aðal Forstillingu.  Þessi stilling notar ekki Sölustaðar. Ef tungumál notanda er ekki stillt eða það er stillt á tungumál þar sem þýðingar eru ekki tiltækar, mun Sölustaðnum snúa til baka í tungumál verslunarinnar.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Tungumál UI** ** **      | **Gagnamál (afurðir, snið kvittunar, línuskjá o.s.frv.)** |
| **Fyrirtæki** | Sjálfgefinn                    | Sjálfgefinn                                                           |
| **Verslun**   | Hnekkir fyrirtæki          | Hnekkir fyrirtæki                                                 |
| **User**    | Hnekkir verslun eða fyrirtæki | Aldrei                                                             |





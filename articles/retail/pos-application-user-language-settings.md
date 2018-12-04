---
title: "Sölustaðarforrit (POS) og stillingar notandatungumáls"
description: "Þetta efnisatriði lýsir hvernig á að breyta tungumálastillingum í Cloud POS og Retail Modern POS (MPOS)."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 1ea4309d57a7b6b4ca4ae3fdd995c95d93c5c080
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Sölustaðarforrit (POS) og stillingar notandatungumáls

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að breyta tungumálastillingum í Cloud POS og Retail Modern POS (MPOS).

## <a name="overview"></a>Yfirlit
Retail Modern POS (MPOS) og Cloud POS styður umhverfi þar sem stillingar tungumáls og þýðinga kunna að vera mismunandi milli stillinga verslunar og notanda. Til dæmis gæti verslunin verið staðsett á svæði þar sem enska er algengust meðal viðskiptavina þeirra, en sumir starfsmenn kjósa heldur að nota forritið með frönskum þýðingum.

## <a name="data-language"></a>Gagnamál
Óháð stillingum notanda munu MPOS- og Cloud POS alltaf nota tungumálastillingar verslunar til að ákvarða þýðingar sem eru notaðar fyrir gögn. Þetta mun tryggja að notendur og viðskiptavinir hafi samræmda reynslu.  Dæmi um gögn eru:

-   Vörur
-   Eigindi og gildi
-   Flokkaheiti
-   Prentaðar eða senda færslukvittanir í tölvupósti
-   Heiti greiðsluhátta
-   Línubirting skilaboða

Tungumál verslunarinnar verður einnig notað fyrir aðalinnskráningarskjá POS, þar sem notandinn er ekki þekktur áður en hann skráir sig inn. Ef þýðing er ekki tiltæk fyrir tungumálið verslunarinnar mun POS snúa aftur í tungumál fyrirtækisins.

### <a name="configuring-the-stores-language-setting"></a>Skilgreining tungumálastillingar verslunarinnar

Tungumálastillingar verslunarinnar eru stilltar í **Allar smásöluverslanir** á síðunni **Smásöluverslun** undir **Almennt&gt; Svæðisstillingar &gt; Tungumál. ** Nota skal fellilista til að velja tungumál fyrir hverja verslun.

## <a name="user-interface-language"></a>Tungumál notandaviðmóts
Tungumálastilling POS notanda ákvarðar þýðingarnar sem eru notaðar í notandaviðmóti forritsins. Það tekur til allra merkja, valmynda og lista sem teljast ekki vera gögn. Ein undantekning er textinn sem birtist á hnappahnitum POS. Hnappahnit styðja ekki þýðingar, svo þau munu ætíð sýna textann eins og hann er skilgreindur á hnappnum. Til að styðja þýdda hnappa, verður að að afrita og vinna með aðskilin hnappahnit og úthluta þeim á notendur eftir þörfum.

### <a name="configuring-the-users-language-setting"></a>Skilgreining tungumálastillingar notanda

Tungumálastilling POS notanda er stillt í **Allir starfsmenn** á síðunni **Starfsmaður** undir **Smásala &gt; Tungumál**.  Hún er ekki stillt á fliptanum Aðalforstillingu.  Þessi stilling er ekki notuð af POS. Ef tungumál notanda er ekki stillt eða það er stillt á tungumál þar sem þýðingar eru ekki tiltækar, mun Sölustaðnum snúa til baka í tungumál verslunarinnar.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **UI-tungumál** ** **      | **Gagnamál (afurðir, snið kvittunar, línuskjá o.s.frv.)** |
| **Fyrirtæki** | Sjálfgefinn                    | Sjálfgefinn                                                           |
| **Verslun**   | Hnekkir fyrirtæki          | Hnekkir fyrirtæki                                                 |
| **Notandi**    | Hnekkir verslun eða fyrirtæki | Aldrei                                                             |







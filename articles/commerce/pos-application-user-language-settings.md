---
title: Sölustaðarforrit (POS) og stillingar notandatungumáls
description: Þessi grein lýsir því hvernig á að breyta tungumálastillingum í Modern POS (MPOS) og Cloud POS.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.industry: Retail
ms.search.form: HcmWorker, RetailStoreTable
ms.openlocfilehash: 663e9a3558bd4d0556644fe5ad6f7f832a18ded5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288380"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Sölustaðarforrit (POS) og stillingar notandatungumáls

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að breyta tungumálastillingum í Modern POS (MPOS) og Cloud POS.

## <a name="overview"></a>Yfirlit
Modern POS (MPOS) og Cloud POS styður umhverfi þar sem stillingar tungumáls og þýðinga kunna að vera mismunandi milli stillinga verslunar og notanda. Til dæmis gæti verslunin verið staðsett á svæði þar sem enska er algengust meðal viðskiptavina þeirra, en sumir starfsmenn kjósa heldur að nota forritið með frönskum þýðingum.

## <a name="data-language"></a>Gagnamál

Óháð stillingum notanda munu MPOS og Cloud POS alltaf nota tungumálastillingar verslunar til að ákvarða þýðingar sem eru notaðar fyrir gögn. Þetta mun tryggja að notendur og viðskiptavinir hafi samræmda reynslu. Dæmi um gögn eru:

- Vörur
- Eigindi og gildi
- Flokkaheiti
- Prentaðar eða senda færslukvittanir í tölvupósti
- Heiti greiðsluhátta
- Línubirting skilaboða

Tungumál verslunarinnar verður einnig notað fyrir aðalinnskráningarskjá POS, þar sem notandinn er ekki þekktur áður en hann skráir sig inn. Ef þýðing er ekki tiltæk fyrir tungumál verslunarinnar mun POS snúa aftur í tungumál fyrirtækisins.

### <a name="configuring-the-stores-language-setting"></a>Skilgreining tungumálastillingar verslunarinnar

Tungumálastillingar verslunarinnar eru stilltar í **Allar verslanir** á síðunni **Verslun** undir **Almennt &gt; Svæðisstillingar &gt; Tungumál**. Nota skal fellilista til að velja tungumál fyrir hverja verslun.

## <a name="user-interface-language"></a>Tungumál notandaviðmóts

Tungumálastilling POS notanda ákvarðar þýðingarnar sem eru notaðar í notandaviðmóti forritsins. Það tekur til allra merkja, valmynda og lista sem teljast ekki vera gögn. Ein undantekning er textinn sem birtist á hnappahnitum POS. Hnappahnit styðja ekki þýðingar, svo þau munu ætíð sýna textann eins og hann er skilgreindur á hnappnum. Til að styðja þýdda hnappa, verður að að afrita og vinna með aðskilin hnappahnit og úthluta þeim á notendur eftir þörfum.

### <a name="configuring-the-users-language-setting"></a>Skilgreining tungumálastillingar notanda

Tungumálastilling POS notanda er stillt í **Allir starfsmenn** á síðunni **Starfsmaður** undir **Retail og Commerce &gt; Tungumál**. Hún er ekki stillt á flipa Aðalforstillingar. Þessi stilling er ekki notuð af POS. Ef tungumál notanda er ekki stillt eða það er stillt á tungumál þar sem þýðingar eru ekki tiltækar, mun sölustaðurinn fara aftur í tungumál verslunarinnar.

| &nbsp;      | UI-tungumál                | Gagnamál (afurðir, snið kvittunar, línuskjá o.s.frv.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Fyrirtæki** | Sjálfgefinn                    | Sjálfgefinn                                                       |
| **Verslun**   | Hnekkir fyrirtæki          | Hnekkir fyrirtæki                                             |
| **Notandi**    | Hnekkir verslun eða fyrirtæki | Aldrei                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]

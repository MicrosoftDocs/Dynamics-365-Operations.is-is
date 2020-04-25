---
title: Uppfæra fjárhagsáætlanir viðhalds
description: Þetta efni útskýrir hvernig á að uppfæra fjárhagsáætlun viðhalds í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e43abd4644eec8c91606ec48bbecf30f12600856
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205277"
---
# <a name="update-maintenance-budgets"></a>Uppfæra fjárhagsáætlanir viðhalds

[!include [banner](../../includes/banner.md)]

 

Síðan **Fjárhagsáætlunarlínur viðhalds** sýnir allar fjárhagsáætlunarlínur sem eru stofnaðar fyrir fjárhagsáætlunina sem er valin á síðunni **Fjárhagsáætlanir viðhalds**. (Sjá frekari upplýsingar [Stofna fjárhagsáætlanir viðhalds](create-maintenance-budget.md).) Þú getur endurútreiknað og aðlagað fjárhagsáætlunarlínur viðhalds þar til fjárhagsáætlun viðhalds er samþykkt. Eftir að fjárhagsáætlunartímabilið er liðið og kostnaður hefur verið bókaður í eignastjórnun geturðu einnig uppfært fjárhagsáætlunarlínurnar með raunkostnaði.

## <a name="recalculate-a-maintenance-budget"></a>Endurreikna fjárhagsáætlun viðhalds

Hægt er að endurútreikna fjárhagsáætlun viðhalds á síðunni **Fjárhagsáætlunarlínur viðhalds**. Þegar þú endurútreiknar fjárhagsáætlun viðhalds er núverandi fjárhagsliðum eytt og nýr útreikningur gerður.

1. Á síðunni **Fjárhagsáætlunarlínur viðhalds** velurðu **Endurreikna**.
2. Í glugganum **Endurreikna fjárhagsáætlun** gerirðu nauðsynlegar breytingar fyrir nýja útreikninginn og velur síðan **Í lagi**.

Nýjar fjárhagsáætlunarlínur eru búnar til samkvæmt gildunum sem þú stillir.

## <a name="adjust-budget-lines"></a>Leiðrétta fjárhagsáætlunarlínur

Í staðinn fyrir að endurreikna alla fjárhagsáætlun viðhalds geturðu breytt völdum línum sem tengjast kostnað fjárhagsáætlunar.

1. Á síðunni **Fjárhagsáætlunarlínur viðhalds** skaltu velja línurnar til að uppfæra kostnaðar fjárhagsáætlunar fyrir.
2. Veldu **Leiðrétta**.
3. Til að bæta við upphæð við valdar línur skaltu velja gátreitinn **Bæta við kostnaði** og slá síðan inn gildi í reitinn **Bæta við gildi**.
4. Til að margfalda fjárhagsáætlunarkostnað á völdum fjárhagsáætlunarlínum með stuðli skaltu velja gátreitinn **Margfalda kostnað** og slá inn þáttinn í **Margfalda gildi**.

    Til dæmis ef þú slærð inn **1,2** í reitinn **Margfalda gildi** hækkarðu kostnað fjárhagsáætlunar á völdum línum um 20 prósent. Ef þú slærð inn **0,7** lækkar þú kostnað fjárhagsáætlunar á völdum línum um 30 prósent.

5. Veljið **Í lagi**.

Valdar fjárhagsáætlunarlínur eru uppfærðar í samræmi við gildin sem þú stillir í 3. eða 4. þrepi.

## <a name="update-actual-costs"></a>Uppfæra raunkostnað

Eftir að dagsetningarnar í fjárhagsáætlunarlínunum eru liðnar og raunkostnaður hefur verið bókaður í eignastjórnun geturðu einnig uppfært raunkostnað á fjárhagsáætlun viðhalds.

1. Á síðunni **Fjárhagsáætlunarlínur viðhalds** velurðu **Uppfæra kostnað**.
2. Í glugganum **Reikna raunkostnað** velurðu **Í lagi**.

Reitirnir **Raunkostnaður** á fjárhagsáætlunarlínunum eru uppfærðir ef raunkostnaður hefur verið bókaður. Nýjar fjárhagsáætlunarlínur gætu verið búnar til ef nýjar eignategundir hafa verið búnar til síðan þú stofnaðir fjárhagsáætlunina og ef þessar eignategundir hafa verið notaðar á eignir sem búið er að búa til vierkbeiðnir fyrir og tengdur kostnaður hefur verið bókaður fyrir. Nýjar fjárlagalínur sýna aðeins raunkostnað vegna þess að enginn fjárhagsáætlunarkostnaður var reiknaður fyrir þá.

> [!NOTE]
> Til að sjá yfirlit yfir raunkostnað skipt í forvarnar-, úrbóta- og fjárfestingarkostnað er hægt að gera útreikning fyrir sama tímabil á síðunni **Stýring eignakostnaðar**. 

## <a name="manually-add-budget-lines"></a>Bæta fjárhagsáætlunarlínum handvirkt við

Á síðunni **Fjárhagsáætlunarlínur viðhalds** er hægt að bæta við nýrri fjárhagsáætlunarlínu handvirkt með því að velja **Nýtt** og síðan val á línunni. Hér eru nokkur dæmi um aðstæður þar sem þessi aðferð gæti verið gagnleg:

- Þú veist að endurnýjun sumra eigna er sem stendur á áætlunarstig, en tengdar vinnslur hafa ekki enn verið stofnaðar í eignastýringu. Samt sem áður viltu að fjárhagsáætlunarkostnaðar fyrir þessar vinnslur verði tekin með í fjárhagsáætlun viðhalds.
- Nýjar eignir eða eignategundir hafa verið búnar til síðan þú gerðir fjárhagsáætlun viðhalds en viðhaldsáætlanir hafa ekki enn verið settar upp fyrir þessar eignir eða eignategundir. Samt sem áður viltu að fjárhagsáætlunarkostnaður fyrir þessar eignagerðir verði tekinn með í fjárhagsáætlun viðhalds.

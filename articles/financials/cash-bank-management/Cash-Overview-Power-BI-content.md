---
title: Yfirlit yfir reiðufé Power BI efni
description: Þetta efnisatriði lýsir sjóðsyfirlitinu Power BI efni. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið.
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5dccb5c5c6c336607603dfc7a935c039e5ac4aa5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "318650"
---
# <a name="cash-overview-power-bi-content"></a>Yfirlit yfir reiðufé Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir **sjóðsyfirlitinu** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Sjóðsyfirlit** Power BI efni var búið til fyrir einstaklinga sem bera ábyrgð á reiðufé í fyrirtæki sínu. **Sjóðsfjáryfirlit** Power BI efni veitir innsýn í sjóðstreymið þitt. Það gefur einnig spár sem geta hjálpað þér við að taka betri ákvarðanir og þannig auka heilbrigði sjóðstreymisins. Hægt er að greina reiðufé eftir lögaðila, gjaldmiðli og bankareikningi til að öðlast betri skilning á tekjuafgangi og halla.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni

Skýrslur úr **Sjóðsyfirlit** Power BI efni eru birtar á vinnusvæðunum **Sjóðsyfirlit** og **Bankastjórnun**.

Til að skoða sjóðstreymisspáskýrslur með gögnum verður fyrst að keyra spáútreikningsferli með því að nota aðgerðina **Reikna sjóðstreymisspár** á Reiðufjár- og bankastjórnunarsvæðinu.  Þetta þarf að gera fyrir hvert fyrirtæki í spánni.  Svo þarf að endurnýja uppsöfnuðu mælinguna LedgerCovLiquidityMeasurement á síðuni **Einingaverslun**.  

Til glöggvunar geturðu bætt við sýnigögnum fyrir sjóðstreymisspá með því að nota síðuna **Mynda gögn** í Sýnigagnaeiningunni.  Þessi forskrift setur gögn inn í sjóðstreymisspátöflurnar til að færa hratt inn upplýsingar sem nauðsynlegar eru fyrir skýrslur.  Þessi eining er aðeins tiltæk ef þú hefur safnlíkan sýnigagna virkjað í umhverfinu. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðar með í Power BI efni
Eftirfarandi tafla veitir upplýsingar um einingarnar sem finna má á hverri síðu skýrslunnar í **Sjóðsyfirlit** Power BI-efni .

| Skýrsla                                | Innihald |
|---------------------------------------|----------|
| Yfirlit yfir reiðufé - öll fyrirtæki         | <ul><li>Inn- og útstreymi í gjaldmiðli kerfisins</li><li>Áætluð gengisstaða</li><li>Heildarupphæð bankainnistæðu í gjaldmiðli kerfisins</li><li>Staða eftir lögaðila</li><li>Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins</li></ul> |
| Yfirlit yfir reiðufé - núverandi fyrirtæki       | <ul><li>Inn- og útstreymi í bókhaldsgjaldmiðli</li><li>Áætluð gengisstaða</li><li>Heildarupphæð bankainnistæðu í bókhaldsgjaldmiðli</li><li>Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins</li></ul> |
| Sjóðstreymisspá - öll fyrirtæki    | <ul><li>Inn- og útstreymi í gjaldmiðli kerfisins</li><li>Samantekt á daglegri spá</li><li>Upplýsingar um spá</li></ul> |
| Sjóðstreymisspá - núverandi fyrirtæki | <ul><li>Inn- og útstreymi í bókhaldsgjaldmiðli</li><li>Samantekt á daglegri spá</li><li>Upplýsingar um spá</li></ul> |
| Gengisspá                     | <ul><li>Áætluð gengisstaða</li><li>Dagleg gengissamantekt</li><li>Upplýsingar um spá</li></ul> |
| Bankainnistæður                         | <ul><li>Heildarupphæð bankainnistæðu í gjaldmiðli kerfisins</li><li>Staða eftir lögaðila</li><li>Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins</li><li>Staða eftir bankareikningi</li><li>Staða eftir gjaldmiðlum</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi tafla sýnir einingar sem **Sjóðsyfirlit** Power BI efni byggist á.

| Eining                                                                          | Innihald |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Fyrirtæki til að sía skýrsla eftir |
| LedgerCovLiquidityMeasurement\_Date                                             | Dagsetningar sem hægt er að sía skýrslur eftir |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Raunveruleg staða samanborið við síðustu áætluðu bankainnistæðu |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Upplýsingar um áætlaðar færslur |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Samantekt sjóðinnstreymis útstreymis og stöðu með bókhaldsgjaldmiðli hvers fyrirtækis |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Samantekt sjóðinnstreymis, útstreymis og stöðu með kerfisgjaldmiðli fyrir öll fyrirtæki |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Samantekin nettó færsluupphæð og staða gjaldmiðla með færslugjaldmiðli |



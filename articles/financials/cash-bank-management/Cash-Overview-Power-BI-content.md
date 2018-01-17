---
title: "Power BI efnisatriði, Yfirlit yfir reiðufé"
description: "Þetta efnisatriði lýsir yfirliti yfir reiðufé í Benefits Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið."
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 5d02a009ca988f91a212e467d4f9784248bbae76
ms.contentlocale: is-is
ms.lasthandoff: 12/19/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI efnisatriði, Yfirlit yfir reiðufé

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir **Yfirliti yfir reiðufé** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Yfirlit yfir reiðufé** í Power BI var stofnað fyrir einstaklinga sem bera ábyrgð á lausafé í fyrirtækjum. **Yfirlit yfir reiðufé** í Power BI efni veitir innsýn í sjóðstreymi þitt. Það gefur einnig spár sem geta hjálpað þér við að taka betri ákvarðanir og þannig auka heilbrigði sjóðstreymisins. Hægt er að greina reiðufé eftir lögaðila, gjaldmiðli og bankareikningi til að öðlast betri skilning á tekjuafgangi og halla.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni

Skýrslur úr **Sjóðsyfirlit** Power BI efni eru birtar á vinnusvæðunum **Sjóðsyfirlit** og **Bankastjórnun**.

Til að skoða sjóðstreymisspáskýrslur með gögnum verður fyrst að keyra spáútreikningsferli með því að nota aðgerðina **Reikna sjóðstreymisspár** á Reiðufjár- og bankastjórnunarsvæðinu.  Þetta þarf að gera fyrir hvert fyrirtæki í spánni.  Svo þarf að endurnýja uppsöfnuðu mælinguna LedgerCovLiquidityMeasurement á síðuni **Einingaverslun**.  

Til glöggvunar geturðu bætt við sýnigögnum fyrir sjóðstreymisspá með því að nota síðuna **Mynda gögn** í Sýnigagnaeiningunni.  Þessi forskrift setur gögn inn í sjóðstreymisspátöflurnar til að færa hratt inn upplýsingar sem nauðsynlegar eru fyrir skýrslur.  Þessi eining er aðeins tiltæk ef þú hefur safnlíkan sýnigagna virkjað í umhverfinu. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni
Eftirfarandi tafla veitir upplýsingar um mælikvarðana sem eru á hverri skýrslusíðu í **Yfirlit yfir reiðufé** í Power BI.

| Skýrsla                                | Innihald |
|---------------------------------------|----------|
| Yfirlit yfir reiðufé - öll fyrirtæki         | <ul><li>Inn- og útstreymi í gjaldmiðli kerfisins</li><li>Áætluð gengisstaða</li><li>Heildarupphæð bankainnistæðu í gjaldmiðli kerfisins</li><li>Staða eftir lögaðila</li><li>Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins</li></ul> |
| Yfirlit yfir reiðufé - núverandi fyrirtæki       | <ul><li>Inn- og útstreymi í bókhaldsgjaldmiðli</li><li>Áætluð gengisstaða</li><li>Heildarupphæð bankainnistæðu í bókhaldsgjaldmiðli</li><li>Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins</li></ul> |
| Sjóðstreymisspá - öll fyrirtæki    | <ul><li>Inn- og útstreymi í gjaldmiðli kerfisins</li><li>Samantekt á daglegri spá</li><li>Upplýsingar um spá</li></ul> |
| Sjóðstreymisspá - núverandi fyrirtæki | <ul><li>Inn- og útstreymi í bókhaldsgjaldmiðli</li><li>Samantekt á daglegri spá</li><li>Upplýsingar um spá</li></ul> |
| Gengisspá                     | <ul><li>Áætluð gengisstaða</li><li>Dagleg gengissamantekt</li><li>Upplýsingar um spá</li></ul> |
| Bankainnistæður                         | <ul><li>Heildarupphæð bankainnistæðu í gjaldmiðli kerfisins</li><li>Staða eftir lögaðila</li><li>Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins</li><li>Staða eftir bankareikningi</li><li>Staða eftir gjaldmiðlum</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi tafla sýnir einingar sem efnispakkinn **Yfirlit yfir reiðufé** í Power BI var byggður á.

| Eining                                                                          | Innihald |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Fyrirtæki til að sía skýrsla eftir |
| LedgerCovLiquidityMeasurement\_Date                                             | Dagsetningar sem hægt er að sía skýrslur eftir |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Raunveruleg staða samanborið við síðustu áætluðu bankainnistæðu |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Upplýsingar um áætlaðar færslur |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Samantekt sjóðinnstreymis útstreymis og stöðu með bókhaldsgjaldmiðli hvers fyrirtækis |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Samantekt sjóðinnstreymis, útstreymis og stöðu með kerfisgjaldmiðli fyrir öll fyrirtæki |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Samantekin nettó færsluupphæð og staða gjaldmiðla með færslugjaldmiðli |




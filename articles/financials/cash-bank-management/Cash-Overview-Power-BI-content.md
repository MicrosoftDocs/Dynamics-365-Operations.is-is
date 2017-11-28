---
title: "Power BI efnisatriði, Yfirlit yfir reiðufé"
description: "Þetta efnisatriði lýsir yfirliti yfir reiðufé í Benefits Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið."
author: saraschi2
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fdcd3083f475967ec2e5f94dad850a1bf98c864a
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI efnisatriði, Yfirlit yfir reiðufé

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir **Yfirliti yfir reiðufé** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Yfirlit yfir reiðufé** í Power BI var stofnað fyrir einstaklinga sem bera ábyrgð á lausafé í fyrirtækjum. **Yfirlit yfir reiðufé** í Power BI efni veitir innsýn í sjóðstreymi þitt. Það gefur einnig spár sem geta hjálpað þér við að taka betri ákvarðanir og þannig auka heilbrigði sjóðstreymisins. Hægt er að greina reiðufé eftir lögaðila, gjaldmiðli og bankareikningi til að öðlast betri skilning á tekjuafgangi og halla.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni

Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) eru skýrslur úr **Sjóðstreymi** Power BI efni birtar á vinnusvæðunum **Sjóðstreymi** og **Bankakerfi**.

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

## <a name="extending-the-power-bi-content"></a>Stækkun efnis Power BI
Hægt er að veita þeim sem ekki skrá sig inn í Dynamics 365 framúrskarandi greiningu með því að nota þá efnispakka sem bjóðast í Lifecycle Services (LCS). Hægt er að breyta þessum efnispökkum þannig að þeir innihaldi skýrslur eða myndræna framsetningu og afhenda svo leigjanda Power BI.com til greiningar. 

Hægt er að finna efni **Yfirlits yfir reiðufé** í Power BI í safninu Samnýttar eignir í LCS. Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

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

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reiknuðu mælieiningar eru síðan notaðar til að reikna út myndrit og gera skýrslur sem eru notaðar í **Yfirliti yfir reiðufé** í Power BI. Eigi að framkvæma frekari útreikninga í skýrslum og mælaborði má sækja og breyta Power BI-skránni úr LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að búa til efnið. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.



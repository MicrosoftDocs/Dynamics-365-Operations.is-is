---
title: "fjárhagsskýrslur Prófjafnaðar"
description: "Þessi grein lýsir sjálfgefnum skýrslum fyrir prófjöfnuði. Hún lýsir einnig einingum sem tengjast þessum skýrslum og hvernig hægt er að breyta skýrslum eftir þörfum."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 86e8e91f2af474999d89bb63ac9e2afad7843c8a
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="trial-balance-financial-reports"></a>fjárhagsskýrslur Prófjafnaðar

[!include[banner](../includes/banner.md)]


Þessi grein lýsir sjálfgefnum skýrslum fyrir prófjöfnuði. Hún lýsir einnig einingum sem tengjast þessum skýrslum og hvernig hægt er að breyta skýrslum eftir þörfum. 

<a name="default-trial-balance-reports"></a>Skýrslur fyrir sjálfgefinn prófjöfnuð
-----------------------------

Þrjár prófjöfnuðarskýrslur eru tiltækar Fjárhagsskýrslugerð í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

| Sjálfgefin skýrsla                                 | Það sem hún gerir                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ítarlegur prófjöfnuður - Sjálfgefið               | Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa debet- og kreditfærslur og nettó stöðu þessara færslna ásamt færsludagsetningu, fylgiskjali og lýsingu færslubókar.                  |
| Samantekt á prófjöfnuði - Sjálfgefið                | Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra.                                        |
| Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin | Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra fyrir núgildandi ár og síðastliðið ár. |

## <a name="building-blocks"></a>Einingar
Fjárhagsskýrslur prófjöfnuðar nota eftirfarandi grunneiningar.

| Sjálfgefin skýrsla                                 | Skilgreining línu          | Skilgreining dálks                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Ítarlegur prófjöfnuður - Sjálfgefið               | prófjöfnuður - sjálfgefið | Ítarlegur prófjöfnuður - Sjálfgefið               |
| Samantekt á prófjöfnuði - Sjálfgefið                | prófjöfnuður - sjálfgefið | Samantekt á prófjöfnuði - Sjálfgefið                |
| Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin | prófjöfnuður - sjálfgefið | Samantekt á Prófjöfnuði frá Ári til Árs – Sjálfgefin |

### <a name="row-definition"></a>Skilgreining línu

Línuskilgreining, Prófjöfnuð – Sjálfgefið, inniheldur eina línu sem sækir allar aðallykla. Þess vegna getur hver sem er búið til skýrslu án þess að þurfa að gera neinar breytingar. Þegar skýrslan er skoðuð er kafað í eina línu til að sjá upplýsingar um hvern reikning. Hægt er að breyta línuskilgreiningu þannig að hún felur í sér nánari upplýsingar. til að breyta Prófjöfnuð – Sjálfgefna línuskilgreiningu þannig að hún felur í sér raðir fyrir alla lykla. Fylgið eftirfarandi skrefum

1.  Smellt er á **breyta** og svo á **Setja inn línur úr víddum**. **Setja inn línur úr víddum** skipunin gerir kleift að velja hvaða víddir óskað er að hafa í línuskilgreiningunni. Fyrir þessa línuskilgreiningu muntu nota **Aðallykil**.
2.  Gangið úr skugga um **Aðallykill** innihaldi öll og-merki og velja **í lagi**.

Línuskilgreining inniheldur nú alla aðallykla fyrir þinn sjálfgefna lögaðila.

### <a name="column-definition"></a>Skilgreining dálks

Hver skýrslu prófjöfnuðar notar mismunandi dálkskilgreiningu. Þessar dálkaskilgreiningar innihalda mismunandi gerðir dálka á að veita mismunandi stig upplýsinga og fjárhagsgögn.

-   **Ítarlegur prófjöfnuður - Sjálfgefnar gerðir dálka:**
    -   **DESC** – Lýsing úr línuskilgreiningunni.
    -   **ACCT** – Kóðar lykils
    -   **ATTR (3)** – Eigindir:
        -   Færsludagsetning
        -   Fylgiskjal
        -   Lýsing færslubókar
    -   **FD** – Fjárhagsgögn sem inniheldur aðeins debet
    -   **FD** – fjárhagsgögn sem inniheldur aðeins kredit
    -   **CALC** – Nettó mismunur
-   **Samantekt á prófjöfnuði - Sjálfgefnar gerðir dálka:**
    -   **ACCT** – Kóðar lykils
    -   **DESC** – Lýsing úr línuskilgreiningunni.
    -   **ATTR** – Eigind:
        -   Fylgiskjal
    -   **FD** – upphafsstaða fjárhagsgagna
    -   **FD** – Fjárhagsgögn sem inniheldur aðeins debet
    -   **FD** – fjárhagsgögn sem inniheldur aðeins kredit
    -   **CALC** – Nettó mismunur
    -   **CALC** – Lokastaða
-   **Samantekt á Prófjöfnuði frá Ári til Árs – Sjálfgefin**
    -   **ACCT** – Kóðar lykils
    -   **DESC** – Lýsing úr línuskilgreiningunni.
    -   **ATTR** – Eigind
        -   Fylgiskjal
    -   **FD** – upphafsstaða fjárhagsgagna fyrir gildandi ár
    -   **FD** – Fjárhagsgögn sem inniheldur aðeins debet fyrir gildandi ár
    -   **FD** – Fjárhagsgögn sem inniheldur aðeins kredit fyrir gildandi ár
    -   **CALC** – Nettó mismunur
    -   **CALC** – Lokastaða
    -   **FD** – Fjárhagsgögn sem inniheldur aðeins debet fyrir síðasta ár
    -   **FD** – Fjárhagsgögn sem inniheldur aðeins kredit fyrir síðasta ár

 

<a name="see-also"></a>Sjá einnig
--------

[Fjárhagsskýrslugerð](financial-reporting-getting-started.md)

[Skoða fjárhagsskýrslur](view-financial-reports.md)

[Dynamics Financial Reporting-blogg](http://blogs.msdn.com/b/dynamics_financial_reporting/)




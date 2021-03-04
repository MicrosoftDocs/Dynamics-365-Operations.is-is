---
title: Fjárhagsskýrslur efnahagsreikninga
description: Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga. Hún lýsir einnig einingum sem tengjast þessum skýrslum.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96552447182f3692a19d4cfd962afbcb28e5508
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444450"
---
# <a name="balance-sheet-financial-reports"></a>Fjárhagsskýrslur efnahagsreikninga

[!include [banner](../includes/banner.md)]

Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga. Hún lýsir einnig einingum sem tengjast þessum skýrslum. 

<a name="default-balance-sheet-reports"></a>Sjálfgefnar skýrslur efnahagsreikninga
-----------------------------

Það eru tvær sjálfgefnar skýrslur efnahagsreikninga. Í einni skýrslunni er köflunum staflað. Í hinni skýrslunni eru kaflarnir hlið við hlið.

| Sjálfgefin skýrsla                       | Það sem hún gerir                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Efnahagsreikningur - Sjálfgefið              | Veitir yfirsýn yfir fjárhagslega stöðu fyrirtækisins fyrir árið.                                                                 |
| Efnahagsreikningur hlið við Hlið – Sjálfgefin | Veitir yfirsýn yfir fjárhagslega stöðu fyrirtækisins fyrir árið. Eignir og skuldir og eigið fé hluthafa er hlið við hlið. |

## <a name="building-blocks"></a>Einingar
Fjárhagsskýrslur efnahagsreikninga nota eftirfarandi grunneiningar.

| Sjálfgefin skýrsla                       | Skilgreining línu                       | Skilgreining dálks             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Efnahagsreikningur - Sjálfgildi              | Efnahagsreikningur - Sjálfgildi              | YTD og frávik - Sjálfgildi    |
| Efnahagsreikningur hlið við Hlið – Sjálfgefin | Efnahagsreikningur hlið við Hlið – Sjálfgefin | Dálkurinn Það sem af er ári - Sjálfgildi |

### <a name="row-definition"></a>Skilgreining línu

Línuskilgreiningar fyrir báðar skýrslur efnahagsreikninga innihalda hluta fyrir hvern hluta venjulegs efnahagsreiknings. Hlið við hlið skýrslan inniheldur dálkaskil, þannig að skuld og eigið fé eiganda birtast við eigna. Víddin Tegund aðallykils er notuð til að búa til báðar línuskilgreiningar. Þess vegna getur hver sem er myndað skýrslu án þess að þurfa að gera neinar breytingar.

### <a name="column-definition"></a>Skilgreining dálks

Dálkskilgreiningar innihalda mismunandi gerðir dálka til að veita mismunandi stig upplýsinga og fjárhagsgagna.

-   **YTD og frávik - Sjálfgefnar gerðir dálka:**
    -   **DESC** – Lýsing úr línuskilgreiningunni.
    -   **FD** – Fjárhagsgögn til dags. fyrir gildandi ár
    -   **FD** – Fjárhagsgögn til dags. fyrir síðasta ár
    -   **CALC** – Frávik frá frádregnu síðasta ári frá þessu ári

<!-- -->

-   **Dálkurinn Það sem af er ári - Sjálfgildi:**
    -   **DESC** – Lýsing úr línuskilgreiningunni.
    -   **FD** – Fjárhagsgögn til dags. fyrir gildandi ár



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlitssíða fjárhagsskýrslugerðar](financial-reporting-getting-started.md)

[Skoða fjárhagsskýrslur](view-financial-reports.md)

[Dynamics Financial Reporting-blogg](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Fjárhagsskýrslugerð"
description: "Þetta efnisatriði lýsir hvar á að fá aðgang að fjárhagsskýrslu í Microsoft Dynamics 365 fyrir Aðgerðir og hvernig á að nota fjárhagslegar skýrslugerðarkosti. Hún inniheldur lýsingu á sjálfgefið fjárhagsskýrslur sem eru gefin."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Fjárhagsskýrslugerð

Þetta efnisatriði lýsir hvar á að fá aðgang að fjárhagsskýrslu í Microsoft Dynamics 365 fyrir Aðgerðir og hvernig á að nota fjárhagslegar skýrslugerðarkosti. Hún inniheldur lýsingu á sjálfgefið fjárhagsskýrslur sem eru gefin.

<a name="accessing-financial-reporting"></a>Aðgangur að fjárhagsskýrslugerð
-----------------------------

Hægt er að finna í **fjárhagsskýrslugerð** valmynd í eftirfarandi setur í Dynamics 365 aðgerða:

-   **Fjárhagur**&gt;**Fyrirspurnir og skýrslur**
-   **Fjárhagsáætlun**&gt;**Inquires og skýrslur**&gt;**grunnáætlanagerð**
-   **Fjárhagsáætlun**&gt;**Fyrirspurnir og skýrslur**&gt;**fjárhagsáætlunargerðar**
-   **Fjárhagsáætlun**&gt;**Fyrirspurnir og skýrslur**&gt;**fjárhagsáætlunarstýringu**
-   Samstæður

Til að stofna og búa til fjárhagsskýrslur fyrir lögaðila, verður að setja upp eftirfarandi upplýsingar fyrir lögaðilann:

-   Fjárhagsdagatal
-   Fjárhagur
-   Bókhaldslykill
-   Gjaldmiðill

Fjárhagsleg skýrslugerð aðgerðir eru tiltækar fyrir notendur sem hafa fengið viðeigandi réttindi og skyldur úthlutað gegnum öryggishlutverk þeirra. Eftirfarandi kaflar telja upp þessi réttindi og skyldur, ásamt tengdum hlutverkum.

### <a name="duties"></a>Skyldur

| Merki skyldu                            | Lýsing                                                             | AOT-heiti                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna og framkvæma stjórnunarverk. | FinancialReportsSecurityMaintain |
| Vinna með fjárhagsskýrslur            | Hanna og vinna með fjárhagsskýrslur.                                  | FinancialReportsMaintain         |
| Mynda fjárhagsskýrslur            | Mynda og uppfæra fjárhagsskýrslur.                                 | FinancialReportsGenerate         |
| Yfirfara fjárhagslega frammistöðu          | Yfirfara og greina fjárhagslega frammistöðu.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Heimildir

| Merki réttinda                       | Lýsing                                                             | AOT-heiti                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna og framkvæma stjórnunarverk. | FinancialReportsSecurityMaintain |
| Vinna með fjárhagsskýrslur            | Hanna og vinna með fjárhagsskýrslur.                                  | FinancialReportsMaintainReports  |
| Mynda fjárhagsskýrslur            | Mynda og uppfæra fjárhagsskýrslur.                                 | FinancialReportsGenerateReports  |
| Skoða fjárhagsskýrslur                | Skoða fjárhagsskýrslur.                                                 | FinancialReportsView             |

### <a name="roles"></a>Hlutverk

| Merki réttinda                       | Tollar                                  | Hlutverk                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna | Öryggisstjóri                                                          |
| Vinna með fjárhagsskýrslur            | Vinna með fjárhagsskýrslur            | Fjármálastjóri Bókhaldsstjóri Yfirmaður Bókhalds, Stjórnanda Fjárhagsáætlunar |
| Mynda fjárhagsskýrslur            | Mynda fjárhagsskýrslur            | Stjórnarformaður, Framkvæmdastjóra, Bókhaldara                                                            |
| Skoða fjárhagsskýrslur                | Yfirfara fjárhagslega frammistöðu          | Ekki úthlutað                                                                   |

Eftir að°notanda er bætt við eða hlutverki er breytt, á notandinn að geta opnað fjárhagsskýrslugerð innan nokkrar mínútur. **Athugasemd:** hlutverki sysadmin er bætt við öll hlutverk í fjárhagsskýrslum.

## <a name="default-reports"></a>Sjálfgefnar skýrslur
Fjárhagsskýrslugerð veitir 22 sjálfgefnar fjárhagsskýrslur. Hvert skýrslan notar tegundir aðallykils sjálfgefna Dynamics 365 fyrir Aðgerðir. Hægt er að nota þessar skýrslur eins og þær eru eða sem byrjunarreit fyrir fjárhagsskýrslugerð. Auk venjulegra fjárhagsskýrslna svo sem tekjuyfirlits og efnahagsreikninga, innihalda þessar sjálfgefnu skýrslur sem sýna mismunandi gerðir af fjárhagsskýrslum sem hægt er að stofna. Hver skýrslu í eftirfarandi töflu tengla í Office blandaðs Tilboðs framsetningu um skýrsluna.

| Sjálfgefin skýrsla                                                                                         | lýsing                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | Skoða arðsemisgreiningu fyrirtækis síðustu 12 mánuði í einum dálki.                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | Skoða arðsemisgreiningu°fyrirtækis síðustu 12 mánuði, hvern mánuð fyrir sig. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla fyrir upprunalega fjárhagsáætlun°og bera saman endurskoðaða fjárhagsáætlun við rauntölur sem hefur frávik.                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður í skýrslugjaldmiðli og innlendum gjaldmiðli með nánari færsluupplýsingar eins og auðkenni, notanda sem síðast breytti gögnum, dagsetning síðustu breytingar og auðkenni færslubókarinnar. |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Skoða°upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir opnunar- og lokunarstöður, og debet og kredit stöður fyrir gildandi tímabil og ár með nánari færsluupplýsingar eins og fylgiskjal.                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið.                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | Skoða fjárhagslega stöðu fyrirtækisins og arðsemi ársins hlið við hlið.                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | Fá yfirlit yfir lausafé sem er að koma inn og fara út úr fyrirtækinu.                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Skoða opna stöðu og verkþáttar upplýsingar fyrir alla lykla.                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa debet- og kreditfærslur og nettó stöðu þessara færslna ásamt færsludagsetningu, fylgiskjali og lýsingu færslubókar.                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | Fá innsýn í kostnað fyrir síðustu 12 ársfjórðungar síðustu þriggja ára.                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Sjá°yfirlit yfir fjárhagstexta varðandi stöður og verkþætti fyrir eign, skuld, eigið fé eiganda, tekjur, kostnaður, hagnaður eða tap.                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Skoða arðsemi fyrirtækisins fyrir gildandi tímabil og°ár til dagsetningar.                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður, með nánari færsluupplýsingar eins og færsludagsetningu, færslubókarnúmer, fylgiskjal, bókunargerð og rakningarnúmer.                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | Skoða greiðsluþol,arðsemi og skilvirkni fyrirtækisins fyrir gildandi ár.                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | Fá innsýn í útgjöld fyrir hvern af síðustu 12 mánuðum. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Skoða arðsemisgreiningu fyrirtækisins ársfjórðungslega á síðastliðnu ári og ári til dagsetningar.                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið. Þessi skýrsla sýnir eignir og skuldir og eigið fé hluthafa hlið við hlið.                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra.                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með þeirra nettó mismunur fyrir gildandi og fyrri ár.                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | Fá innsýn í sölu- og afslætti fyrir hverja viku í mánuði. Þessi skýrsla inniheldur fjögurra vikna samtölu.                                                                                                                                                                                                              |
| [Tiltækt Fjármagn fjárhagsáætlunar - Sjálfgildi](https://mix.office.com/watch/15hcpezcbx7tv)                         | Skoða ítarlegar endurskoðaðri raunútgjöld, frátektir fjárhagsáætlunar og tiltækt fjármagn fjárhagsáætlunar fyrir lykla                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Opna fjárhagsskýrslur
Þegar smellt°er á **fjárhagsskýrslugerð** valmynd, birtist listi yfir sjálfgefnar fjárhagsskýrslur fyrir fyrirtækið. Síðan er hægt að opna og breyta skýrslu. Velja heiti skýrslu til að opna sjálfgefnu skýrslurnar. Í fyrsta sinn sem skýrsla er opnað, er hún sjálfvirkt mynduð fyrir fyrri mánuð. Til dæmis, ef skýrslu er opnuð í fyrsta sinn Ágúst 2016 skýrslan er mynduð fyrir 31. Júlí 2016. Eftir að skýrsla er opnuð er hægt að hefja skoðun á henni með þvi að kafa niður í sértæka gagnahluta og breyta valkostum skýrslu.

## <a name="creating-and-modifying-financial-reports"></a>Stofna og breyta fjárhagsskýrslum
Af listanum yfir fjárhagsskýrslur er hægt að stofna nýja skýrslu eða breyta fyrirliggjandi skýrslu. Ef notandi hafi viðeigandi heimildir, hægt er að stofna nýja fjárhagsskýrslu með því að smella **Nýtt** í Aðgerðarúðunni. Skýrslan hönnuður forriti er hlaðið niður skal tækis. Eftir að hönnuður skýrslu er ræst er hægt að stofna nýja skýrslu. Þegar búið er að vista nýja skýrslu birtist hún í lista yfir fjárhagsskýrslur. Listinn sýnir einungis skýrslur sem voru stofnaðar fyrir fyrirtæki sem verið er að nota í Dynamics 365 fyrir Aðgerðir. Nánari upplýsingar um ferlið stofna og breyta fjárhagsskýrslur í Dynamics 365 aðgerða eru í þessum [blog bókar](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) úr Dynamics fjárhagslegar reporting blog. **Athugasemd:** tölvu sem er að hlaða niður skýrslu hönnuður biðlara á verður að hafa útgáfu 4.6.2 af Microsoft .NET Framework uppsett. Hægt er að sækja þessa útgáfu af Microsoft .NET Framework og sett upp frá [hér](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Ef verið er að nota Króm verður að setja upp ClickOnce nafnauka til að sækja skýrslu hönnuður biðlara. Ef verið er að keyra incognito ham gangið úr skugga um að nafnauka ClickOnce er virk fyrir incognito ham. Einnig er hægt að breyta skýrslu sem birtist í lista yfir fjárhagsskýrslur. Þegar svæði umhverfis heiti skýrslunnar er valið, er smellt á **Breyta**°í Aðgerðarúðunni. Skýrsluhönnunarforritið er ræst.

<a name="see-also"></a>Sjá einnig
--------

[View financial reports](view-financial-reports.md)

[Dynamics Financial Reporting-blogg](http://blogs.msdn.com/b/dynamics_financial_reporting/)



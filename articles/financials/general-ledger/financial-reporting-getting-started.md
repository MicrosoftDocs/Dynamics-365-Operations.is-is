---
title: "Fjárhagsskýrslugerð"
description: "Þetta efnisatriði lýsir hvar á að nálgast fjárhagslega skýrslugerð í Microsoft Dynamics 365 for Finance and Operations og hvernig á að nota möguleika fjárhagsskýrslugerð. Inniheldur lýsing á sjálfgefið fjárhagsskýrslur sem er veitt."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 5de1f5b40af076173dd0b38c6f6110f83c04528a
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="financial-reporting"></a>Fjárhagsskýrslugerð

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir hvar á að nálgast fjárhagslega skýrslugerð í Microsoft Dynamics 365 for Finance and Operations og hvernig á að nota möguleika fjárhagsskýrslugerð. Inniheldur lýsing á sjálfgefið fjárhagsskýrslur sem er veitt.

<a name="accessing-financial-reporting"></a>Aðgangur að fjárhagsskýrslugerð
-----------------------------

Hægt er að finna valmyndina **Fjárhagsskýrslugerð** á eftirfarandi stöðum í Finance and Operations:

-   **Fjárhagur** &gt; **Fyrirspurnir og skýrslur**
-   **Fjárhagsgerð** &gt; **Fyrirspurnir og skýrslur** &gt; **grunnáætlanagerð**
-   **Fjárhagsáætlun** &gt; **Fyrirspurnir og skýrslur** &gt; **Fjárhagsáætlunargerð**
-   **Fjárhagsáætlun** &gt; **Fyrirspurnir og skýrslur** &gt; **Fjárhagsáætlunarstýring**
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
| Vinna með fjárhagsskýrslur            | Vinna með fjárhagsskýrslur            | Aðalbókari, yfirmaður bókhalds, fjármálastjóri, stjórnandi fjárhagsáætlunar |
| Mynda fjárhagsskýrslur            | Mynda fjárhagsskýrslur            | Forstjóri, framkvæmdastjóri, bókhaldari                                                            |
| Skoða fjárhagsskýrslur                | Yfirfara fjárhagslega frammistöðu          | Ekki úthlutað                                                                   |

Eftir að°notanda er bætt við eða hlutverki er breytt, á notandinn að geta opnað fjárhagsskýrslugerð innan nokkrar mínútur. **Athugasemd:** Hlutverkið sysadmin er bæta við öll hlutverk í fjárhagsskýrslugerð.

## <a name="default-reports"></a>Sjálfgefnar skýrslur
Fjárhagsskýrslugerð veitir 22 sjálfgefnar fjárhagsskýrslur. Hver skýrsla notar sjálfgefnar tegundir aðallykils í Finance and Operations. Hægt er að nota þessar skýrslur eins og þær eru eða sem byrjunarreit fyrir fjárhagsskýrslugerð. Auk venjulegra fjárhagsskýrslna svo sem tekjuyfirlits og efnahagsreikninga, innihalda þessar sjálfgefnu skýrslur sem sýna mismunandi gerðir af fjárhagsskýrslum sem hægt er að stofna. Hvert skýrsla í eftirfarandi tafla tengja við Office Mix kynning um skýrsla.

| Sjálfgefin skýrsla                                                                                         | lýsing                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 mánaða rúlla tekjuyfirlit í einum dálki – Sjálfgefið](https://mix.office.com/watch/76kc7bm3wnt1) | Skoða arðsemisgreiningu fyrirtækis síðustu 12 mánuði í einum dálki.                                                                                                                                                                                                                                      |
| [12 mánaða Leitni Tekjuyfirlits – Sjálfgefið](https://mix.office.com/watch/12brmfge5p8r)                 | Skoða arðsemisgreiningu°fyrirtækis síðustu 12 mánuði, hvern mánuð fyrir sig. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                             |
| [Rauntölur samanb. v. áætlun - Sjálfgefið](https://mix.office.com/watch/fi439lkwr0no)                                | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla fyrir upprunalega fjárhagsáætlun°og bera saman endurskoðaða fjárhagsáætlun við rauntölur sem hefur frávik.                                                                                                                                                                          |
| [Endurskoðun upplýsinga - Sjálfgefið](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður í skýrslugjaldmiðli og innlendum gjaldmiðli með nánari færsluupplýsingar eins og auðkenni, notanda sem síðast breytti gögnum, dagsetning síðustu breytingar og auðkenni færslubókarinnar. |
| [Stöðulisti - sjálfgefið](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Skoða°upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir opnunar- og lokunarstöður, og debet og kredit stöður fyrir gildandi tímabil og ár með nánari færsluupplýsingar eins og fylgiskjal.                                                                    |
| [Efnahagsreikningur - Sjálfgefið](https://mix.office.com/watch/zkgq0u7visw9)                                   | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið.                                                                                                                                                                                                                                                             |
| [Efnahagsreikningur og Tekjuyfirlit Hlið við Hlið - Sjálfgefið](https://mix.office.com/watch/zkgq0u7visw9) | Skoða fjárhagslega stöðu fyrirtækisins og arðsemi ársins hlið við hlið.                                                                                                                                                                                                                              |
| [Sjóðstreymi - Sjálfgefið](https://mix.office.com/watch/jd3go9pz6390)                                       | Fá yfirlit yfir lausafé sem er að koma inn og fara út úr fyrirtækinu.                                                                                                                                                                                                                                   |
| [Ítarleg JE og TB yfirlit– Sjálfgefið](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Skoða opna stöðu og verkþáttar upplýsingar fyrir alla lykla.                                                                                                                                                                                                                                                      |
| [Ítarlegur prófjöfnuður - Sjálfgefið](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa debet- og kreditfærslur og nettó stöðu þessara færslna ásamt færsludagsetningu, fylgiskjali og lýsingu færslubókar.                                                                                                                                  |
| [Útgjöld þriggja ára á ársfjórðungslegum grundvelli – Sjálfgefið](https://mix.office.com/watch/gwm4zu7tmtj8)             | Fá innsýn í kostnað fyrir síðustu 12 ársfjórðungar síðustu þriggja ára.                                                                                                                                                                                                                                   |
| [Fjárhagstextar JE og TB yfirlit – Sjálfgefið](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Sjá°yfirlit yfir fjárhagstexta varðandi stöður og verkþætti fyrir eign, skuld, eigið fé eiganda, tekjur, kostnaður, hagnaður eða tap.                                                                                                                                                                           |
| [Rekstrarreikningur – Sjálfgefin](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Skoða arðsemi fyrirtækisins fyrir gildandi tímabil og°ár til dagsetningar.                                                                                                                                                                                                                                   |
| [Fjárhagshreyfingalisti - Sjálfgefið](https://mix.office.com/watch/19h9v2rmh48vy)                        | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður, með nánari færsluupplýsingar eins og færsludagsetningu, færslubókarnúmer, fylgiskjal, bókunargerð og rakningarnúmer.                                                                            |
| [Hlutfallstölur – Sjálfgefin](https://mix.office.com/watch/b08hfc5h92me)                                          | Skoða greiðsluþol,arðsemi og skilvirkni fyrirtækisins fyrir gildandi ár.                                                                                                                                                                                                                           |
| [Samantekt á útgjöldum 12 mánaða - Sjálfgefið](https://mix.office.com/watch/iywod5qmqhz7)                       | Fá innsýn í útgjöld fyrir hvern af síðustu 12 mánuðum. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                                       |
| [Samantekt á tekjuyfirliti ársfjórðungs - Sjálfgefið](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Skoða arðsemisgreiningu fyrirtækisins ársfjórðungslega á síðastliðnu ári og einnig ári til dagsetningar.                                                                                                                                                                                                                   |
| [Efnahagsreikningur hlið við Hlið – Sjálfgefin](https://mix.office.com/watch/zkgq0u7visw9)                      | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið. Þessi skýrsla sýnir eignir og skuldir og eigið fé hluthafa hlið við hlið.                                                                                                                                                                                |
| [Samantekt á prófjöfnuði - Sjálfgefið](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra.                                                                                                                                                                  |
| [Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun- og lokun stöður og debet og kredit stöður með nettó mismun þeirra yfir núgildandi ár og fyrra ár.                                                                                                                           |
| [Vikulegar Sölur- og Afslættir - Sjálfgefið](https://mix.office.com/watch/112ng0hy5de0j)                     | Fá innsýn í sölu- og afslætti fyrir hverja viku í mánuði. Þessi skýrsla inniheldur fjögurra vikna samtölu.                                                                                                                                                                                                              |
| [Fjármagn fjárhagsáætlunar tiltækt - sjálfgefinn](https://mix.office.com/watch/15hcpezcbx7tv)                         | Skoða sundurliðað samanburður af endurskoðað fjárhagsáætlun, raunútgjöld, frátekt fjárhagsáætlunar og fjármagn fjárhagsáætlunar tiltækt fyrir allir reikningar                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Opna fjárhagsskýrslur
Þegar smellt°er á **fjárhagsskýrslugerð** valmynd, birtist listi yfir sjálfgefnar fjárhagsskýrslur fyrir fyrirtækið. Síðan er hægt að opna og breyta skýrslu. Velja heiti skýrslu til að opna sjálfgefnu skýrslurnar. Í fyrsta sinn sem skýrsla er opnað, er hún sjálfvirkt mynduð fyrir fyrri mánuð. Til dæmis, ef skýrsla er opnuð í fyrsta sinn í Ágúst 2016 er hún mynduð fyrir 31. Júlí 2016. Eftir að skýrsla er opnuð er hægt að hefja skoðun á henni með þvi að kafa niður í sértæka gagnahluta og breyta valkostum skýrslu.

## <a name="creating-and-modifying-financial-reports"></a>Stofna og breyta fjárhagsskýrslum
Af listanum yfir fjárhagsskýrslur er hægt að stofna nýja skýrslu eða breyta fyrirliggjandi skýrslu. Ef notandi hefur viðeigandi heimildir, er hægt að stofna nýja fjárhagsskýrslu með því að smella á **Nýtt** í Aðgerðarúðunni. Skýrsluhönnunarforriti er hlaðið niður á tækið og opnast síðan. Eftir að skýrsluhönnun opnast er hægt að stofna nýja skýrslu. Þegar búið er að vista nýja skýrslu birtist hún í lista yfir fjárhagsskýrslur. Listinn sýnir einungis skýrslur sem voru stofnaðar fyrir fyrirtæki sem verið er að nota í Finance and Operations. Frekari upplýsingar um ferli að stofna og breyta fjárhagsskýrslur í Finance and Operations er að sjá í þessum [bloggfærslum](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) á Dynamics-fjárhagsskýrslublogginu. **Athugasemd:** Tölvan sem þú ert að hlaða niður skýrsluhönnunarbiðlara verður að vera með uppsetta útgáfa 4.6.2. af Microsoft .NET Framework. Þessa útgáfa af Microsoft .NET Framework er hægt að sækja og setja upp [hér](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Ef verið er að nota Chrome, verður að setja upp ClickOnce-viðauka til að sækja skýrslu hönnuðurbiðlara. Ef verið er að nota Chrome í huliðsstillingu, ganga úr skugga um að ClickOnce viðbót sé einnig virkur fyrir huliðsstillingu. Einnig er hægt að breyta skýrslu sem birtist í lista yfir fjárhagsskýrslur. Þegar svæði umhverfis heiti skýrslunnar er valið, er smellt á **Breyta**°í Aðgerðarúðunni. Skýrsluhönnunarforritið er ræst.

<a name="see-also"></a>Sjá einnig
--------

[Skoða fjárhagsskýrslur](view-financial-reports.md)

[Dynamics Financial Reporting-blogg](http://blogs.msdn.com/b/dynamics_financial_reporting/)





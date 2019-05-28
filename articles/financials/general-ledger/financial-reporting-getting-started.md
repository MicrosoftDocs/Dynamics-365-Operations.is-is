---
title: Fjárhagsskýrslugerð
description: Þetta efnisatriði lýsir hvar á að opna fjárhagslegar skýrslugerð í Microsoft Dynamics 365 for Finance and Operations og hvernig á að nota möguleika fjárhagsskýrslugerð. Inniheldur lýsing á sjálfgefið fjárhagsskýrslur sem er veitt.
author: aprilolson
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: c6d504a7b0640f45de4aa9f8fb60d2b1d37818bb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550306"
---
# <a name="financial-reporting"></a>Fjárhagsskýrslugerð

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvar á að opna fjárhagslegar skýrslugerð í Microsoft Dynamics 365 for Finance and Operations og hvernig á að nota möguleika fjárhagsskýrslugerð. Inniheldur lýsing á sjálfgefið fjárhagsskýrslur sem er veitt.

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
Fjárhagsskýrslugerð veitir 22 sjálfgefnar fjárhagsskýrslur. Hver skýrsla notar sjálfgefnar tegundir aðallykils í Finance and Operations. Hægt er að nota þessar skýrslur eins og þær eru eða sem byrjunarreit fyrir fjárhagsskýrslugerð. Auk venjulegra fjárhagsskýrslna svo sem tekjuyfirlits og efnahagsreikninga, innihalda þessar sjálfgefnu skýrslur sem sýna mismunandi gerðir af fjárhagsskýrslum sem hægt er að stofna. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Sjálfgefin skýrsla                                                                                         | Lýsing                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 mánaða rúlla tekjuyfirlit í einum dálki – Sjálfgefið | Skoða arðsemisgreiningu fyrirtækis síðustu 12 mánuði í einum dálki.                                                                                                                                                                                                                                      |
| 12 mánaða Leitni Tekjuyfirlits – Sjálfgefið                 | Skoða arðsemisgreiningu°fyrirtækis síðustu 12 mánuði, hvern mánuð fyrir sig. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                             |
| Rauntölur samanb. v. áætlun - Sjálfgefið                                | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla fyrir upprunalega fjárhagsáætlun°og bera saman endurskoðaða fjárhagsáætlun við rauntölur sem hefur frávik.                                                                                                                                                                          |
| Endurskoðun upplýsinga - Sjálfgefið                                  | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður í skýrslugjaldmiðli og innlendum gjaldmiðli með nánari færsluupplýsingar eins og auðkenni, notanda sem síðast breytti gögnum, dagsetning síðustu breytingar og auðkenni færslubókarinnar. |
| Stöðulisti - sjálfgefið                                   | Skoða°upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir opnunar- og lokunarstöður, og debet og kredit stöður fyrir gildandi tímabil og ár með nánari færsluupplýsingar eins og fylgiskjal.                                                                    |
| Efnahagsreikningur - Sjálfgefið                                   | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið.                                                                                                                                                                                                                                                             |
| Efnahagsreikningur og Tekjuyfirlit Hlið við Hlið - Sjálfgefið | Skoða fjárhagslega stöðu fyrirtækisins og arðsemi ársins hlið við hlið.                                                                                                                                                                                                                              |
| Sjóðstreymi - Sjálfgefið                                       | Fá yfirlit yfir lausafé sem er að koma inn og fara út úr fyrirtækinu.                                                                                                                                                                                                                                   |
| Ítarleg JE og TB yfirlit– Sjálfgefið                      | Skoða opna stöðu og verkþáttar upplýsingar fyrir alla lykla.                                                                                                                                                                                                                                                      |
| Ítarlegur prófjöfnuður - Sjálfgefið                         | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa debet- og kreditfærslur og nettó stöðu þessara færslna ásamt færsludagsetningu, fylgiskjali og lýsingu færslubókar.                                                                                                                                  |
| Útgjöld þriggja ára á ársfjórðungslegum grundvelli – Sjálfgefið             | Fá innsýn í kostnað fyrir síðustu 12 ársfjórðungar síðustu þriggja ára.                                                                                                                                                                                                                                   |
| Fjárhagstextar JE og TB yfirlit – Sjálfgefið            | Sjá°yfirlit yfir fjárhagstexta varðandi stöður og verkþætti fyrir eign, skuld, eigið fé eiganda, tekjur, kostnaður, hagnaður eða tap.                                                                                                                                                                           |
| Rekstrarreikningur – Sjálfgefin                                | Skoða arðsemi fyrirtækisins fyrir gildandi tímabil og°ár til dagsetningar.                                                                                                                                                                                                                                   |
| Fjárhagshreyfingalisti - Sjálfgefið                        | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður, með nánari færsluupplýsingar eins og færsludagsetningu, færslubókarnúmer, fylgiskjal, bókunargerð og rakningarnúmer.                                                                            |
| Hlutfallstölur – Sjálfgefin                                          | Skoða greiðsluþol,arðsemi og skilvirkni fyrirtækisins fyrir gildandi ár.                                                                                                                                                                                                                           |
| Samantekt á útgjöldum 12 mánaða - Sjálfgefið                       | Fá innsýn í útgjöld fyrir hvern af síðustu 12 mánuðum. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                                       |
| Samantekt á tekjuyfirliti ársfjórðungs - Sjálfgefið               | Skoða arðsemisgreiningu fyrirtækisins ársfjórðungslega á síðastliðnu ári og einnig ári til dagsetningar.                                                                                                                                                                                                                   |
| Efnahagsreikningur hlið við Hlið – Sjálfgefin                      | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið. Þessi skýrsla sýnir eignir og skuldir og eigið fé hluthafa hlið við hlið.                                                                                                                                                                                |
| Samantekt á prófjöfnuði - Sjálfgefið                          | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra.                                                                                                                                                                  |
| Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin           | Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun- og lokun stöður og debet og kredit stöður með nettó mismun þeirra yfir núgildandi ár og fyrra ár.                                                                                                                           |
| Vikulegar Sölur- og Afslættir - Sjálfgefið                     | Fá innsýn í sölu- og afslætti fyrir hverja viku í mánuði. Þessi skýrsla inniheldur fjögurra vikna samtölu.                                                                                                                                                                                                              |
| Fjármagn fjárhagsáætlunar tiltækt - sjálfgefinn                         | Skoða sundurliðað samanburður af endurskoðað fjárhagsáætlun, raunútgjöld, frátekt fjárhagsáætlunar og fjármagn fjárhagsáætlunar tiltækt fyrir allir reikningar                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Opna fjárhagsskýrslur
Þegar smellt°er á **fjárhagsskýrslugerð** valmynd, birtist listi yfir sjálfgefnar fjárhagsskýrslur fyrir fyrirtækið. Síðan er hægt að opna og breyta skýrslu. Velja heiti skýrslu til að opna sjálfgefnu skýrslurnar. Í fyrsta sinn sem skýrsla er opnað, er hún sjálfvirkt mynduð fyrir fyrri mánuð. Til dæmis, ef skýrsla er opnuð í fyrsta sinn í Ágúst 2016 er hún mynduð fyrir 31. Júlí 2016. Eftir að skýrsla er opnuð er hægt að hefja skoðun á henni með þvi að kafa niður í sértæka gagnahluta og breyta valkostum skýrslu.

## <a name="creating-and-modifying-financial-reports"></a>Stofna og breyta fjárhagsskýrslum
Af listanum yfir fjárhagsskýrslur er hægt að stofna nýja skýrslu eða breyta fyrirliggjandi skýrslu. Ef notandi hefur viðeigandi heimildir, er hægt að stofna nýja fjárhagsskýrslu með því að smella á **Nýtt** í Aðgerðarúðunni. Skýrsluhönnunarforriti er hlaðið niður á tækið og opnast síðan. Eftir að skýrsluhönnun opnast er hægt að stofna nýja skýrslu. Þegar búið er að vista nýja skýrslu birtist hún í lista yfir fjárhagsskýrslur. Listinn sýnir einungis skýrslur sem voru stofnaðar fyrir fyrirtæki sem verið er að nota í Finance and Operations. 

> [!NOTE] 
> Tölvan sem þú ert að hlaða niður skýrsluhönnunarbiðlara verður að vera með uppsetta útgáfu 4.6.2 af Microsoft .NET Framework. Hægt er að sækja og setja upp þessa útgáfu af Microsoft .NET Framework úr [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Ef verið er að nota Chrome, verður að setja upp ClickOnce-viðauka til að sækja skýrslu hönnuðurbiðlara. Ef verið er að nota Chrome í huliðsstillingu, ganga úr skugga um að ClickOnce viðbót sé einnig virkur fyrir huliðsstillingu. Einnig er hægt að breyta skýrslu sem birtist í lista yfir fjárhagsskýrslur. Þegar svæði umhverfis heiti skýrslunnar er valið, er smellt á **Breyta**°í Aðgerðarúðunni. Skýrsluhönnunarforritið er ræst.

## <a name="additional-resources"></a>Frekari upplýsingar
- [Skoðun fjárhagsskýrslna](view-financial-reports.md)




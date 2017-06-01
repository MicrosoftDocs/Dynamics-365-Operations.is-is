---
title: "Nýjungar eða breytingar í Dynamics AX forritaútgáfu 7.0.1 (maí 2016)"
description: "Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í núverandi útgáfu Microsoft Dynamics AX 7.0.1. Þessi útgáfa var losuð í Maí 2016 og byggingarnúmer af 7.0.1265.23014."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8b58cb4f9de393b3f381dbe0aa4330d5ebd62795
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Nýjungar eða breytingar í Dynamics AX forritaútgáfu 7.0.1 (maí 2016)

[!include[banner](../includes/banner.md)]


Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í núverandi útgáfu Microsoft Dynamics AX 7.0.1. Þessi útgáfa var losuð í Maí 2016 og byggingarnúmer af 7.0.1265.23014.

<a name="electronic-reporting-er"></a>Rafræn skýrslugerð (ER)
-------------------------

|                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvað hægt er að gera?**                                                                                                                                                                   | **Hví er þetta mikilvægt?**                                                                                                                                                                                                                                                                                                                             |
| Skilgreina keyrslu tími svarglugga til að búa til Rafræna skýrslugerð skýrslur (ER), þannig að notendur geta valið fjárhagsvíddirnar sem þær vilja.                                     | Í keyrslutíma, í svarglugganum fyrir keyrð ER skýrslan notendur geta valið margar fjárhagsvíddir. Upplýsingar um valda fjárhagsvíddir verður birt í rafræna skjalið sem er mynduð.                                                                                                                              |
| Skilgreina aðgang að mörgum fjárhagsvíddir meðan hönnun ER skýrsla með einni vörpun í æskilega gagnagjafa.                                                  | Hægt er að nota sama skýrsluskilgreiningar ER til að mynda rafræn skjöl sem sýna færslugögnum með upplýsingar um fjárhagsvíddir, burtséð frá fjölda fjárhagsvíddirnar sem eru valdar af notandanum eða skilgreind fyrir núgildandi lögaðila eða tilvik.                                             |
| Stilla skýrslu ER að færa gögn í dálkum sjálfvirkt myndað af rafræna skjalið sem er stofnun í OPENXML vinnublaði.                                           | ER skýrslan hægt að færa inn gögn í OPENXML vinnublaðs sem er mynduð með gagnaspeglun láréttur dálka. Þess vegna er hægt að endurnota sama skýrsluskilgreiningar ER til að mynda rafrænu skjölin sem hafa mismunandi fjölda dálka sem sjálfvirkt myndaðan.                                                                                 |
| Skilgreina ER áfangastaði sem úttaks niðurstaða snið beint er til ákveðna áfangastað: skráin, tölvupósti eða safn (Microsoft SharePoint-möppu eða Geymslu Microsoft Azure). | Áður þegar ER skilgreining sem keyrði skilaboðagluggi birtist sem aðgerð notanda sem þarf til að vista eða opna skrá. Hægt er að forskilgreina áfangastað fyrir hverja skilgreiningarsnið og íhlut úttaks þess (möppu eða í skrá) sér. Notendur sem eru veittar viðeigandi aðgangsheimildir einnig er hægt að breyta stillingar fyrir áfangastað á keyrslutíma. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail
|                                |                                                                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvað hægt er að gera?**           | **Hví er þetta mikilvægt?**                                                                                                                                                              |
| Nota Google Chrome vafra. | Smásala nú hægt að hefja Sölukerfi úr skýi úr vafra Chrome og getur reynslu allar aðgerðir sem er tiltækt í Microsoft Edge og Internet Explorer útgáfu sölukerfi í skýinu. |

## <a name="financial-reporting"></a>Fjárhagsskýrslugerð
|                                                                     |                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvað hægt er að gera?**                                                | **Hví er þetta mikilvægt?**                                                                                                                                                                                                                                                                                         |
| Endurbyggja Fjárhagslegar skýrslugerðar gögn torg.                          | Þegar Dynamics AX gagnagrunnar eru færðir á milli umhverfa eða aðrar breytingar gerðar á umhverfinu gæti þurft að endurbyggja gagnagrunn Fjárhagslegar skýrslu. Windows PowerShell forskrift er nú veitt til að endurbyggja gagnagrunninum fyrir þig.                                                                |
| Ekki lengur hægt að velja skýrsluhönnun valkostina sem ekki eru gilda. | Nokkrar skýrsluhönnun valkostina sem voru notaðir í útgáfur markaðinn í Management reporter ekki nota í þessari útgáfu Dynamics AX. Þessir valkostir voru tengdir fjárhagslega skýrsluhönnun, úttak og tengingu. Þessir valkostir hafa verið fjarlægðir úr fjárhagsskýrsluhönnuði til að koma í veg fyrir að notandavillur. |

## <a name="financial-management"></a>Fjármálastjórnun
|                                                            |                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------|
| **Hvað hægt er að gera?**                                       | **Hví er þetta mikilvægt?**                                       |
| Mynda jákvæðar greiðsluskrár fyrir greiðslur viðskiptaskuldir. | Mynda jákvæðar skrár til að hjálpa að koma í veg fyrir ávísanafals. |

## <a name="warehouse-and-production"></a>Vöruhús og framleiðsla
|                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvað hægt er að gera?**                                                                                                                                                                                                                                                                                                                                                                    | **Hví er þetta mikilvægt?**                                                                                                                                                                                                                                                                                                                                                                                                              |
| Skilgreina vöruhús vinnu reglu sem stýrir stofnun vinnu fyrir safn af afurðum á tiltekna staði.                                                                                                                                                                                                                                                                          | Ferli vöruhúsa ekki alltaf hafa vinnu. Með því að nota nýju vinnustefnu vöruhúss , getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.                                                                                                                                                                                                     |
| Tilgreina að staðsetningu framleiðslufrálags ekki númeraplötustýrð.                                                                                                                                                                                                                                                                                                               | Getur tilgreina að staðsetningu framleiðslufrálags ekki númeraplötustýrð. Til dæmis er þessi eiginleiki gagnlegt þegar þarfarakningu framleiðslupöntun skráir sem tilbúna beint á staðsetningu sem er eins og staðsetning framleiðsluinntaks framleiðslupöntunar niður á við vörur.                                                                                                                                                     |
| Styðja Uppskriftir sem innihalda vörur með mismunandi afurðavíddir fyrir sömu vöruna.                                                                                                                                                                                                                                                                                                     | Þegar ein eða margar afurðarvíddum í framleiðslu er hægt að láta aðstæðum þar sem óskað er að framleiða vöru, annan vöruvíddasamsetning sömu vöru á grundvelli. Nánari upplýsingar er að finna í [þessari blogg](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).                                                                  |
| Framleiðslupantanir með hringvirkni á fyrsta stigi um Uppskriftir þeirra eru undanskildar úr útreikning Uppskriftar fyrir efni eftirspurnarstjórnunar stigs.                                                                                                                                                                                                                                     | Ekki er hægt að úthluta rétt uppskriftarstig afurðarafbrigði fyrir framleiðslupantanir sem veldur hringvirkni í stigveldi Uppskriftalínunnar.                                                                                                                                                                                                                                                                                                  |
| Reikna aðskilin uppskriftarstig fyrir áætlun efnistilfanga og kostnaðarútreikning: • Efni eftirspurnarstjórnunar, stig í Uppskrift er reiknuð í nýja **ReqItemLevel** töfluna. Framleiðslupantanir sem lokið eru hunsaðar við útreikning. • útreikningi framleiðslukostnaðar uppskriftarstig er reiknaður út á **InventTable**. Framleiðslupantanir sem lokið eru teknar með við útreikning. | • Þegar efni eftirspurnarstjórnunar, til dæmis áætlun röðun og niðurbrot, áætlanagerð er keyrð aðeins uppskriftarstig sem eru notuð fyrir efni eftirspurnarstjórnunar þarf að endurreikna. Með öðrum orðum, það er engin þörf á að reikna uppskriftarstig er notað fyrir útreikning kostnaðar. • Þegar í gangi  kostnaðarútreiknings aðgerðir, til dæmis birgðalokun, aðeins uppskriftarstig sem eru notaðar við útreikning framleiðslu kostnaðarútreiknings þarf að endurreikna. |

 

<a name="see-also"></a>Sjá einnig
--------

[Hvað er nýtt eða breytt](whats-new-changed.md)

[Nýjar eða uppfærðar verkefnaleiðbeiningar (maí 2016)](new-updated-task-guides-available-may-2016.md)





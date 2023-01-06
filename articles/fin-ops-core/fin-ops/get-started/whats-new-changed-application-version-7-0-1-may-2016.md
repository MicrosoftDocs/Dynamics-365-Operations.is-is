---
title: Hvað er nýtt og hvað hefur breyst í Dynamics AX forritaútgáfa 7.0.1 (maí 2016)
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýjar eða breyttar í Microsoft Dynamics AX umsókn útgáfu 7.0.1. Þessi útgáfa var losuð í Maí 2016 og byggingarnúmer af 7.0.1265.23014.
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 94cebad528facc5537226a3faa5ea9be8448092e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267201"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Hvað er nýtt og hvað hefur breyst í Dynamics AX forritaútgáfa 7.0.1 (maí 2016)

[!include [banner](../includes/banner.md)]

Þessi grein lýsir eiginleikum sem eru annað hvort nýjar eða breyttar í Microsoft Dynamics AX umsókn útgáfu 7.0.1. Þessi útgáfa var losuð í Maí 2016 og byggingarnúmer af 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Rafræn skýrslugerð (ER)

| Hvað hægt er að gera? | Hví er þetta mikilvægt? |
|------------------|------------------------|
| Skilgreina keyrslu tími svarglugga til að búa til Rafræna skýrslugerð skýrslur (ER), þannig að notendur geta valið fjárhagsvíddirnar sem þær vilja. | Í keyrslutíma, í svarglugganum fyrir keyrð ER skýrslan notendur geta valið margar fjárhagsvíddir. Upplýsingar um valda fjárhagsvíddir verður birt í rafræna skjalið sem er mynduð. |
| Skilgreina aðgang að mörgum fjárhagsvíddir meðan hönnun ER skýrsla með einni vörpun í æskilega gagnagjafa. | Hægt er að nota sama skýrsluskilgreiningar ER til að mynda rafræn skjöl sem sýna færslugögnum með upplýsingar um fjárhagsvíddir, burtséð frá fjölda fjárhagsvíddirnar sem eru valdar af notandanum eða skilgreind fyrir núgildandi lögaðila eða tilvik. |
| Stilla skýrslu ER að færa gögn í dálkum sjálfvirkt myndað af rafræna skjalið sem er stofnun í OPENXML vinnublaði. | ER skýrslan hægt að færa inn gögn í OPENXML vinnublaðs sem er mynduð með gagnaspeglun láréttur dálka. Þess vegna er hægt að endurnota sama skýrsluskilgreiningar ER til að mynda rafrænu skjölin sem hafa mismunandi fjölda dálka sem sjálfvirkt myndaðan. |
| Skilgreina ER áfangastaði sem úttaks niðurstaða snið beint er til ákveðna áfangastað: skráin, tölvupósti eða safn (Microsoft SharePoint-möppu eða Geymslu Microsoft Azure). | Áður þegar ER skilgreining sem keyrði skilaboðagluggi birtist sem aðgerð notanda sem þarf til að vista eða opna skrá. Hægt er að forskilgreina áfangastað fyrir hverja skilgreiningarsnið og íhlut úttaks þess (möppu eða í skrá) sér. Notendur sem eru veittar viðeigandi aðgangsheimildir einnig er hægt að breyta stillingar fyrir áfangastað á keyrslutíma. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS - Microsoft Dynamics AX smásala

| Hvað hægt er að gera? | Hví er þetta mikilvægt? |
|------------------|------------------------|
| Nota Google Chrome vafra. | Smásala nú hægt að hefja Sölukerfi úr skýi úr vafra Chrome og getur reynslu allar aðgerðir sem er tiltækt í Microsoft Edge og Internet Explorer útgáfu sölukerfi í skýinu. |

## <a name="financial-reporting"></a>Fjárhagsskýrslugerð

| Hvað hægt er að gera? | Hví er þetta mikilvægt? |
|------------------|------------------------|
| Endurbyggja Fjárhagslegar skýrslugerðar gögn torg. | Þegar Dynamics AX gagnagrunnar eru færðir á milli umhverfa eða aðrar breytingar gerðar á umhverfinu gæti þurft að endurbyggja gagnagrunn Fjárhagslegar skýrslu. Windows PowerShell forskrift er nú veitt til að endurbyggja gagnagrunninum fyrir þig. |
| Ekki lengur hægt að velja skýrsluhönnun valkostina sem ekki eru gilda. | Nokkrar skýrsluhönnun valkostina sem voru notaðir í útgáfur markaðinn í Management reporter ekki nota í þessari útgáfu Dynamics AX. Þessir valkostir voru tengdir fjárhagslega skýrsluhönnun, úttak og tengingu. Þessir valkostir hafa verið fjarlægðir úr fjárhagsskýrsluhönnuði til að koma í veg fyrir að notandavillur. |

## <a name="financial-management"></a>Fjármálastjórnun

| Hvað hægt er að gera? | Hví er þetta mikilvægt? |
|------------------|------------------------|
| Mynda jákvæðar greiðsluskrár fyrir greiðslur viðskiptaskuldir. | Mynda jákvæðar skrár til að hjálpa að koma í veg fyrir ávísanafals. |

## <a name="warehouse-and-production"></a>Vöruhús og framleiðsla

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skilgreina vöruhús vinnu reglu sem stýrir stofnun vinnu fyrir safn af afurðum á tiltekna staði.</td>
<td>Ferli vöruhúsa innihalda ekki alltaf vinnu. Með því að nota nýju vinnustefnu vöruhúss , getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.</td>
</tr>
<tr>
<td>Tilgreina að staðsetningu framleiðslufrálags ekki númeraplötustýrð.</td>
<td>Getur tilgreina að staðsetningu framleiðslufrálags ekki númeraplötustýrð. Til dæmis er þessi eiginleiki gagnlegt þegar þarfarakningu framleiðslupöntun skráir sem tilbúna beint á staðsetningu sem er eins og staðsetning framleiðsluinntaks framleiðslupöntunar niður á við vörur.</td>
</tr>
<tr>
<td>Styðja Uppskriftir sem innihalda vörur með mismunandi afurðavíddir fyrir sömu vöruna.</td>
<td>Þegar ein eða margar afurðarvíddum í framleiðslu er hægt að láta aðstæðum þar sem óskað er að framleiða vöru, annan vöruvíddasamsetning sömu vöru á grundvelli. Nánari upplýsingar er að finna í <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">þessari blogg</a>.</td>
</tr>
<tr>
<td>Framleiðslupantanir með hringvirkni á fyrsta stigi um Uppskriftir þeirra eru undanskildar úr útreikning Uppskriftar fyrir efni eftirspurnarstjórnunar stigs.</td>
<td>Ekki er hægt að úthluta rétt uppskriftarstig afurðarafbrigði fyrir framleiðslupantanir sem veldur hringvirkni í stigveldi Uppskriftalínunnar.</td>
</tr>
<tr>
<td>Reikna uppskriftarstig aðskildar fyrir áætlun tilfanga efni og kostnaður útreiknings:
<ul>
<li>Fyrir áætlun efnistilfanga eru uppskriftarstig reiknuð út í nýju töflunni <strong>ReqItemLevel</strong>. Framleiðslupantanir sem lokið eru hunsaðar við útreikning.</li>
<li>Fyrir útreikning framleiðslukostnaðar eru uppskriftarstig reiknuð út í <strong>InventTable</strong>. Framleiðslupantanir sem lokið eru teknar með við útreikning.</li>
</ul>
</td>
<td>
<ul>
<li>Þegar áætlun efnistilfanga er keyrð, til dæmis áætlun röðunar og niðurbrots á aðaláætlanagerð, þarf einungis að endurreikna uppskriftarstig sem eru notuð fyrir áætlun efnistilfanga. Með öðrum orðum, það er engin þörf á að reikna uppskriftarstig er notað fyrir útreikning kostnaðar.</li>
<li>Þegar keyrðar eru aðgerðir kostnaðarútreiknings, til dæmis birgðalokunar, þarf einungis að endurreikna uppskriftarstig sem eru notuð við útreikning framleiðslukostnaðar.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Frekari upplýsingar

[Nýjungar eða breytingar á heimasíðu fjármála- og reksturs ](whats-new-changed.md)

[Nýjar eða uppfærðar verkefnaleiðbeiningar (maí 2016)](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

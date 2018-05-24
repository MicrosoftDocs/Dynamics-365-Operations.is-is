---
title: "Grunnstilla útlit afgreiðsluskjás fyrir POS"
description: "Þetta efnisatriði veitir upplýsingar um útlit afgreiðsluskjás á sölustað í Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9082c156fde52aa0c822f8e4753de816f8cc0558
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="configure-screen-layouts-for-pos"></a>Skilgreining skjáútlits fyrir sölustað

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um útlit afgreiðsluskjás á sölustað í Microsoft Dynamics 365 for Retail.

Hægt er að skilgreina notendaviðmót Microsoft Dynamics 365 for Retail á sölustað með samsetningu á sjónrænum reglum og útliti afgreiðsluskjás, úthlutað á verslanir, afgreiðslukassa, og/eða notendur.

## <a name="visual-profile"></a>Sjónræn regla
Sjónrænum reglum er úthlutað á afgreiðslukassa og eru notaðir til að tilgreina sjónrænar einingar sem eru tilgreindar fyrir afgreiðslukassa og samnýttar yfir notendur. Notendur sem skráir sig inn á afgreiðslukassa hefur sama þema, liti og myndir. 

**Reglunúmer** - Reglunúmerið er einkvæmt auðkenni fyrir Sjónræna reglu. 

**Lýsing** - Lýsingin gerir kleift að tilgreina auðskilið nafn sem hjálpar til við að auðkenna rétta reglu í hverju tilviki.

**Þema** -Notendur geta valið á milli ljósra eða dökkra forritsþema. Þessar stillingar hafa áhrif á letursliti og bakgrunnsliti liti í gegnum forritið.

**Áherslulitur** - Áherslulitur er notaður í gegnum allt POS til að aðgreina eða merkja tilteknar einingar sjónrænna þátta, skipunarhnappa eða tengla. Þessar einingar eru yfirleitt aðgerðir.

**Litur hauss** - Litur hauss leyfir notandanum að skilgreina lit blaðsíðuhauss til að uppfylla vörumerkjaþarfir smásala. Þessi eiginleiki er aðeins tiltækur í Dynamics 365 for Retail útgáfu 1611.

**Bakgrunnsmynd innskráningar** - Notendur geta tilgreint bakgrunnsmynd fyrir innskráningarskjá. Skráarstærð bakgrunnsmynda á að vera eins lítil og hægt er, þar sem geymsla og uppflutningu á stórum skrám geta haft áhrif á virkni forritsins og afköst.

**Bakgrunnur forritsins** - POS getur einnig notað mynd sem bakgrunnur í öllu kerfinu í stað þema með heilum lit. Líkt og með bakgrunn innskráningar er mælt með að hafa skráarstærð eins litla og hægt er.

## <a name="screen-layouts"></a>Útlit afgreiðsluskjás
Skilgreining á útliti afgreiðsluskjás ákvarðar aðgerðir, efni og staðsetningu notandaviðmótsstýringa í upphafsskjá POS og færsluskjánum. 

**Upphafsskjár**- Í flestum tilvikum er upphafsskjár síðan sem notendur sjá þegar þeir skrá sig fyrst inn á Sölustað. Upphafsskjár getur verið samsettur af vörumerkjamynd og hnappahnitum sem veita aðgang að aðgerðum POS. Aðgerðir sem eiga sérstaklega við gildandi færslu eru yfirleitt settar hér. 

**Færsluskjár** - Færsluskjár er aðalskjárinn í POS fyrir vinnslu á sölufærslum og pantanir. Hægt er að skilgreina færsluskjáinn með útlitshönnuður afgreiðsluskjás. 

**Sjálfgefinn upphafsskjár** - Sumir smásalar vilja að gjaldkeri fari beint á færsluskjá eftir innskráningu. Stillingin Sjálfgefinn upphafsskjár gerir notendum kleift að stilla þetta fyrir hvert útlit afgreiðsluskjás.

### <a name="assignment"></a>Verkefni

Hægt er að úthluta útliti afgreiðsluskjás á verslunar-, afgreiðslukassa- eða notandastigi. Úthlutun notanda hnekkir úthlutun afgreiðslukassa og geymslu og afgreiðslukassaúthlutun hnekkir úthlutun verslunar. Í einfalt dæmi þar sem allir notendur notað sama útlit, afgreiðslukassa eða hlutverk, er aðeins hægt að stilla útlit skjásins í verslun. Í tilfellum þar sem tilteknar afgreiðslukassar eða notendur þurfa sérstillt útlit er hægt að úthluta þeim eftir þörfum.

### <a name="layout-sizes"></a>Útlitsstærðir

Þessi eiginleiki er aðeins tiltækur í Dynamics 365 for Retail útgáfu 1611. Vegna þess að í mörgum tilvikum er hægt að nota útlit afgreiðsluskjás yfir margar skjástærðir og -úrlausnir geta notendur skilgreint snið og innihald fyrir hvern þeirra. POS-forritið mun sjálfkrafa velja nálægustu útlitsstærð fyrir tækið við ræsingu. Útlit skjás getur einnig innihaldið skilgreiningar fyrir bæði full og minni tæki. Þessi skilgreining leyfir að notanda sé úthlutað á einn skjá sem mun virka í mismunandi stærðar- og skjámyndaþáttum innan verslunarinnar. 

**Modern POS - Full** - Fullt útlit er yfirleitt best notað fyrir stærri skjái eins og PC-tölvuskjái eða spjaldtölvur. Notendur geta valið hvaða viðmótseiningar eru hafðar með, ákvarðað stærð þeirra og staðsetningu þeirra og skilgreint ítarlega eiginleika þeirra. Full útlit styðja bæði þversniðis- og langsniðsskilgreiningar. 

**Modern POS - Compact** - Smækkað útlit er yfirleitt best notað fyrir síma eða litlar spjaldtölvur. Hönnunarmöguleikar takmarkast við smækkuð tæki. Notendur geta skilgreint dálka og svæði fyrir móttöku- og samtölurúður.

### <a name="screen-layout-designer"></a>Útlitshönnuður afgreiðsluskjás

Skilgreina verður hverja útlitsstærð innan skjáútlits með útlitshönnuði afgreiðsluskjás. Hönnuðurinn gerir notendum kleift að tilgreina og skilgreina viðmótseiningar á færsluskjánum. Útlitshönnuður afgreiðsluskjás notar ClickOnce til að sækja, setja upp og ræsa nýjustu útgáfu forritsins í hvert sinn sem notandi tengist henni. Gætið þess að athuga kröfur fyrir vafra til að nota ClickOnce — sumar vafrar, eins og Chrome, krefjast viðauka. 

**Talnaborð** - Talnaborð er aðalnotendainnsetning á færsluskjár POS. Hægt er að skilgreina það til að sýna allt takkaborðið á skjánum, sem er tilvalið fyrir snertiskjái, eða aðeins inntakssvæði, sem hægt er að nota með tengdu lyklaborði. Stillingar talnaborðsins eru aðeins tiltækar í fullu útliti. Í Dynamics 365 for Retail útgáfu 1611 er smækkað útlit alltaf með fullt talnaborð tiltækt á færsluskjánum.

**Samtölugluggi** - Hægt er að skilgreina samtöluglugga í annaðhvort einn eða tvo dálka til þess að sýna svæði eins og lína talningu, afsláttarupphæð, gjöld, millisamtala og skatts. Í Dynamics 365 for Retail útgáfu 1611 styður smækkað útlit aðeins einn samtöludálk. 

**Kvittun** - Kvittunargluggi afurða inniheldur sölulínur, greiðslulínur og afhendingarupplýsingar fyrir afurðir og þjónustu sem er unnin í POS. Notendur geta tilgreint dálka, breiddir og staðsetningu. Í smækkuðu útliti í Dynamics 365 for Retail útgáfu 1611 er einnig hægt að skilgreina viðbótarupplýsingar sem munu birtast á línunni undir aðallínunni. 

**Viðskiptamannaspjald** - Viðskiptamannaspjald sýnir upplýsingar um viðskiptavin sem tengist færslunni. Hægt er að skilgreina viðskiptamannaspjaldið til að fela eða sýna viðbótarupplýsingar. 

**Flipastýring** - Flipastýring getur verið staðsett á skjánum og aðrar stýringar borð við talnaborð, viðskiptamannaspjald, eða hnappahnit má setja inn á flipann. Flipastýring er geymir sem hjálpar notendum að koma meira efni á skjáinn. Flipastýring sem er aðeins tiltæk fyrir fullt útlit. 

**Mynd** - Myndstýringuna má nota til að sýna merki verslunar eða aðra vörumerkjamynd á færsluskjánum. Myndstýring er aðeins tiltæk fyrir fullt útlit. 

**Afurðir sem mælt er með** - Ef þetta er skilgreint fyrir umhverfið mun stýring ráðlagðra afurða sýna afurðatillögur byggðar á forritun vélar. Stýring ráðlagðra afurða er aðeins tiltæk fyrir fullt útlit í Dynamics 365 for Retail útgáfu 1611. **Sérstillt stýring**- Sérstillt stýring þjónar sem frátakari innan útlits skjásins sem gerir notendum kleift að taka frá pláss fyrir sérsniðið efni. Sérstillt stýring er aðeins tiltæk fyrir fullt útlit.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Uppsetning útlitshönnunarbúnaðar Retail POS](install-pos-layout-designer.md)





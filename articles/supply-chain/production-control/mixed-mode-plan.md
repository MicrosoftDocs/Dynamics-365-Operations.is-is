---
title: "Áætlanagerð blandaðrar stillingar: Sameina afmarkaða, ferli og lean uppruna"
description: "Þessi grein veitir upplýsingar um áætlanagerð í blönduðum ham. Með áætlanagerð í blönduðum ham geturðu mótað birgðakeðju þína á grundvelli efnisflæðis. Microsoft Dynamics 365 for Finance and Operations tryggir að efnisflæði fylgi þínum líkönum, óháð framboðsreglu sem er valin (kanban, framleiðslupantanir, innkaupapantanir, runupantanir eða flutningspantanir)."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 9dbbe540c919d27bafcc10614f308e5b6ba313f1
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Áætlanagerð blandaðrar stillingar: Sameina afmarkaða, ferli og lean uppruna

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um áætlanagerð í blönduðum ham. Með áætlanagerð í blönduðum ham geturðu mótað birgðakeðju þína á grundvelli efnisflæðis. Microsoft Dynamics 365 for Finance and Operations tryggir að efnisflæði fylgi þínum líkönum, óháð framboðsreglu sem er valin (kanban, framleiðslupantanir, innkaupapantanir, runupantanir eða flutningspantanir). 

Hægt er að velja heildar stefnunn fyrir útvegun afurðar óháð uppbyggingu vöru.  

Til dæmis er hægt að hafa kanban-stýringu í samsetningunni, þar sem efni eru fengin úr uppruna fyrir samsetningarsvæði samkvæmt framleiðslupöntunum, kanban, flutningum, runu pöntunum, eða hvaða annarri samsetningu sem er viðeigandi fyrir eðli aðfangakeðju þinnar, en enn er hægt að hafa fullan sýnileika á milli aðfanga. Þessi eiginleiki leiðir til mestu hagræðingar í ferlum aðfangakeðju og aukins sýnileika í birgðakeðju þinni.  

Nákvæmnistig aðfangastefnu sem eru notaðar í aðalröðun fer eftir geymsluvíddunum sem eru virkjaðar sem þakningarvíddir. Til að virkja aðalröðun til að stjórna áfyllingu og framboði mismunandi gerða staðsetninga (til dæmis með því að aðgreina á framleiðslugólf fyrir mismunandi framleiðslueiningar, eða með því að aðgreina mismunandi gerðir af efni og fullbúnar vörur vöruhúsa) er mælt er með því virkja Svæði og Vöruhús sem þakningarvíddir. Einnig er hægt að sleppa Vöruhúsi sem þekjuvídd. Í því tilfelli, þegar þú notar ítarlega vöruhúsastjórnun , eru allar hreyfingar innan vöruhúss stýrt af vöruhúsavinnu, en allar hreyfingar milli vöruhúsa er stýrt af úttektarkanbönum.

## <a name="supply-policies"></a>Framboðsreglur
Áætlanagerð blandaðrar stillingar í Finance and Operations stýrir því hvernig afurð er veitt og, samkvæmt framboði, hvernig afleiddar kröfur (notkun vara úr \[uppskrift\]) eru gefnar út. samkvæmt Gerð pöntunar, finnur kerfið sjálfkrafa uppruna efnis til samræmis við þarfir.  

Hægt er að skilgreina framboðsreglur á stigi afurðar eða á hvaða nákvæmnisstigi sem styður kröfur þínar. Þú skilgreinir nákvæmnisstig framboðsreglna á  **Sjálfgefnar pöntunarstillingar** síðu.  

Hægt er að stýra framboðsreglum eftir afurð, vöruvíddum (afbrigði, lit og stærð), svæði og vöruhúsi. Þessari uppsetningu er gerð á í **Vöruþekja** síðu.  

Sjálfgefin pöntunargerð stýrir því hvaða pöntun aðaláætlanagerð myndar.  

Óháð því hvernig birgðakeðjan er mótuð, styður Finance and Operations þína blöndu af framboðsreglum. Hægt er að hafa framleiðslupantanir sem eru fundnar úr uppruna úr kanbönum. Einnig er hægt að hafa runupöntun sem krefst afurðar sem er veitt með flutningum eða kanban.  

Finance and Operations tryggir að efnisflæði fari eftir líkaninu.  

Vöruhús fyrir tiltekt efnis er úthlutað gagnvirkt á keyrslutíma, eftir að framboðsregla hefur verið skilgreint.  

Yfirleitt, eru kanban ekki stofnuð fyrir framtíðardagsetningar, þar sem kanban hefur stuttan líftíma. Til að viðhalda fullri yfirsýn yfir aðfangakeðja, höfum við kynnt nýtt hugtak í áætlanagerð "áætluð Kanban," sem er notað til að reikna afleiddar kröfur og hjálpar að tryggja að kröfurnar eru fundnar í uppruna byggt á sömu rökum sem er notað þegar raunverulegur Kanban er stofnaður.  

Sömu rök eru til staðar fyrir allar aðrar gerðir framboðsreglna. Þess vegna er lengri tíma efnisáætlanagerð byggð á sömu rökfræði sem þú býst við keyrslu með raunverulegum pöntunum eftir að framleiðsla og framboð eru samþykktar.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Úthlutunarregla krossframboðs efnis - -Notkun tilfangs á uppskriftir
Notkun tilfanga er mikilvæg aðgerð. notkun tilfangs virkjar vöruhús fyrir tínslu efnis til að vera valinn gagnvirkt, byggt á framboðreglu (gerð pöntunar), og gerir einnig viðhald á grunngögnum auðveldara.  

Notkun tilfanga krefst þess að vöruhúsi sem efni eru tínd úr sé úthlutað byggt á því hvernig afurðin er veitt. Með öðrum orðum, , kerfið finnur á keyrslutíma tilföng sem á að nota fyrir framleiðslu. Samkvæmt þessum tilföngum finnur kerfið síðan tiltektarvöruhús.  

Fyrir vinnu sem er óháð í framboðsreglu, þarf ekki að breyta upplýsingum um Uppskrift ef birgðum er breytt. Fyrir tilfallandi breytingar tryggir Finance and Operations að efni eru fundin í uppruna úr réttu vöruhúsi.

## <a name="process-manufacturing--the-production-type"></a>Vinnsluframleiðsla - gerð framleiðslu
Fyrir fullan sveigjanleika í blandaðri stillingu, mælum við með að nota uppskrift sem gerð framleiðslu fyrir allar afurðir. Hægt er að nota framleiðslupantanir, flutningspantanir, kanban eða innkaupapantanir til að útvega vöru. Fyrir Vinnsluframleiðslu, þarf að nota gerð framleiðslu **Formúlu**, **aukaafurð**, **hliðarafurð**, eða **áætlunarvara**. Kanban og framleiðslupöntun er ekki hægt að nota fyrir þessar gerðir framleiðslu.




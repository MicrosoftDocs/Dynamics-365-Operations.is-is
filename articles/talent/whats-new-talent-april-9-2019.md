---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (9. apríl 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a4d4de6cf28e24d1265395d6440df85edf71a0d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897857"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (9. apríl 2019)

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) samþætting við „tilkynna um vandamál“
Í Attract og Onboard munu vandamál sem notandi notar í gegnum eiginleika vandamálatilkynningar nú sjálfkrafa stofna þjónustuvandamál í LCS-verki viðskiptavinar. Stjórnendur geta þá flokkað vandamálin og sent þau inn til Microsoft þegar þörf krefur. Þetta er í samræmi við hvernig Core HR annast stuðning á vandamálum notanda.

### <a name="relevance-search"></a>Samsvörun í leit
Í hæfileikasöfnum er nú hægt að leita í öllum gagnagrunninum yfir umsækjendur að ákveðinni hæfni, nafni eða menntun. Ekki þarf lengur að tilgreina hvaða hluta af notandaupplýsingum umsækjanda á að leita í gegnum. Attract leitar í öllum notandaupplýsingunum og undirstrikar allar samsvaranir sem finnast. Attract leitar einnig í öllum skjölum sem til eru um umsækjanda og raðar leitarniðurstöðunum á snjallan hátt. Að auki er hægt að sía niðurstöðurnar eftir uppruna eða hvort þau eru annars flokks. Frekari upplýsingar er að finna í [Leita og skoða forstillingar umsækjenda](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Tillögur viðfangs
Attract getur hjálpað til við að koma leitinni að starfi af stað um leið og þú virkjar það í að koma með snjallar tillögur að umsækjendum úr gagnagrunni umsækjenda í fyrirtækinu þínu. Tillögurnar innihalda upplýsingar um hæfni og menntun sem borið er kennsl á við leit á viðeigandi viðföngum. Þessar tillögur birtast í flipanum **Viðföng** undir starfi ef þú virkjar það á meðan ráðningarferli starfs er í gangi. Frekari upplýsingar er að finna í [Tillögur viðfangs](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Hvenær spyrill er laus
Þeir sem sjá um áætlanagerð spyrils geta brátt séð stöðurnar **Ekki á skrifstofu, er að vinna annars staðar** fyrir spyrla, til að auðvelda að finna tíma sem getur hentað betur fyrir spyrlana.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Viðtalsreynsla umsækjanda: Vista dagatalsboð
Umsækjendur geta nú sótt og vistað viðtalsviðburðinn sinn í persónulegt dagatal með því að nota .ics-skrá sem er hengd við tölvupóst með samantekt á viðtali sem var send á umsækjandann.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) samþætting við vandamálatilkynningu
Í Attract og Onboard munu vandamál sem notandi notar í gegnum eiginleika vandamálatilkynningar nú sjálfkrafa stofna þjónustuvandamál í LCS-verki viðskiptavinar. Stjórnendur geta þá flokkað vandamálin og sent þau inn til Microsoft þegar þörf krefur. Þetta er í samræmi við hvernig Core HR annast stuðning á vandamálum notanda.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR
Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Hleðsla á rangri upphæð fyrir prósentu á breytilegri grunnáætlun
Útgáfa þessarar viku leiðréttir vandamál þegar hlaðið er breytilegum launum með því að nota prósentu af grunnáætlunum.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Dagsetningarval á síðasta vinnudegi virkar ekki rétt
Þessi breyting leiðréttir vandamálið: Þegar notendur breyta **Lokadagur ráðningar** og velja dagsetninguna með því að nota dagatalsstýringu, er degi bætt við valið.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Takmarka gerðir starfsmannaaðgerða eftir aðgerðinni sem er valin
Þessi breyting takmarkar gerðir aðgerða sem birtast þegar tilteknar aðgerðir eru framkvæmdar. Til dæmis þegar óskað er eftir nýrri stöðu, birtast aðeins nýju stöðuaðgerðirnar í listanum yfir aðgerðir til að velja. Áður birtust bæði nýjar og breyttar aðgerðir. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Flutningur starfsmanns með laun í annan lögaðila
Þessi útgáfa gerir kleift að laun hætti í öðrum lögaðila ef flutningurinn er fyrir flutning milli fyrirtækja.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Ekki er hægt að velja laun fyrir framtíðarráðningu við flutning
Þegar starfsmaður er fluttur til nýs lögaðila er nú hægt að stilla laun fyrir nýja lögaðilann meðan á flutningsferlinu stendur.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Notandi getur ekki úthlutað launum meðan stöðuverkefni er í gangi
Að bæta við nýju stöðuverkefni núna leyfir uppsetningu á föstum launafærslum. 

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Leyfa að tilgreina ástæðukóða fyrir leyfisgerðir
Fyrirtæki gætu þurft frekari upplýsingar um frítímabeiðnir. Nú er hægt að tilgreina ástæðukóða fyrir leyfisgerðir og gert starfsmönnum kleift að velja ástæðukóða fyrir frítímabeiðnir.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Fara fram á ástæðukóða fyrir ákveðnar leyfisgerðir á frítímabeiðnum
Fyrirtæki gætu krafist ástæðukóða fyrir ákveðna leyfisgerðir þegar starfsfólk sendir inn frítíma. Þetta gæti verið vegna stefnu fyrirtækis eða út af reglugerðum. Nú er hægt að tilgreina hvers konar leyfisgerðir þurfa ástæðukóða og nú er hægt að krefja starfsfólk um að gefa upp ástæðukóða fyrir leyfisgerðina út af frítímabeiðni þeirra.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Bjóða upp á færslulista leyfa og fjarvista fyrir mannauðsstjóra
Að fylgjast með frítíma starfsmanns og skilja hvernig frítími er reiknaður hjálpar ekki aðeins mannauðsstjóra við að svara spurningum starfsmanns en tryggir einnig nákvæma frítímainneign starfsmanna. Mannauðsstjóri er nú með nýja sýn á færslunum (styrkir, uppsafnanir, leiðréttingar og beiðnir) til að sjá ástæðurnar á bak við stöðurnar. 

## <a name="coming-soon"></a>Væntanlegt

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Umbætur á notendaviðmótinu fyrir tvítekningu á athugun starfsmanns
Með þessari breytingu er borið kennsl á tvítekningar á meðan þú færir inn heiti á reitum og staða sýnir hversu margar tvítekningar fundust. Þú getur valið tengilinn sem gefinn er upp til að opna nýja síðu til að meta hvort nota skuli samsvörun sem borin var kennsl á. Til að forðast að trufla gagnafærslu, opnast tvítekin skjámynd ekki sjálfkrafa.

###  <a name="email-support-for-alerts"></a>Tölvupóstur út af viðvörunum
Með verkvangsuppfærslu 25 fyrir Finance and Operations geta notendur stofnað viðvörunarreglur sem senda sjálfkrafa tilkynningar í tölvupósti á tengiliði þegar þær ræsast út af tilviki. 

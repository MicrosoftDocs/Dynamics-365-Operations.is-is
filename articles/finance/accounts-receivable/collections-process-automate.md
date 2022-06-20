---
title: Sjálfvirkni innheimtuferla
description: Þessi grein lýsir ferlinu við að setja upp innheimtuferlisaðferðir sem auðkenna sjálfkrafa reikninga viðskiptavina sem krefjast áminningar í tölvupósti, innheimtuaðgerða eða innheimtubréfs til að senda til viðskiptavinarins.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9ec749db197b4d04ee2e99ac7a16f4f2120c6707
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946179"
---
# <a name="collections-process-automation"></a>Sjálfvirkni innheimtuferla

[!include [banner](../includes/banner.md)]

Þessi grein lýsir ferlinu við að setja upp innheimtuferlisaðferðir sem auðkenna sjálfkrafa reikninga viðskiptavina sem krefjast áminningar í tölvupósti, innheimtuaðgerða (svo sem símtals) eða innheimtubréfs sem á að senda til viðskiptavinarins. 

Fyrirtæki eyða oft verulegum tíma í að rannsaka skýrslur um aldursgreindar stöður, viðskiptavinalykla og opna reikninga til að finna út hvaða viðskiptavini ætti að hafa samband við vegna opins reiknings eða reikningsstöðu. Þessi rannsókn tekur tíma frá innheimtufulltrúanum sem fer í samskipti við viðskiptavini um að safna gjaldföllnum greiðslum eða ráða fram úr ágreiningi vegna reikninga. Sjálfvirkni innheimtuferlis gerir þér kleift að setja upp stjórnunartengda nálgun á innheimtuferlinu. Þetta hjálpar til við að beita innheimtuaðgerðum með stöðugum hætti með því að bjóða upp á sérsniðnar áminningar í tölvupósti eða forritað ferli til að senda innheimtubréf. 

## <a name="collections-process-setup"></a>Uppsetning innheimtuferlis
Hægt er að nota síðuna **Uppsetning innheimtuferlis** (**Skuldir og innheimta > Uppsetning > Uppsetning innheimtuferlis**) til að búa til sjálfvirkt innheimtuferli sem tímasetur aðgerðir, sendir tölvupósta og stofnar og sendir innheimtubréf til viðskiptavina. Skref ferlisins byggja á fremsta eða elsta opna reikningnum. Hvert skref notar þennan reikning til að ákvarða hvaða samskipti eða aðgerð á að fara fram varðandi tiltekinn viðskiptavin.  

Innheimtuhópar senda yfirleitt út tilkynningu með góðum fyrirvara sem tengist ákveðnum útistandandi reikningi þannig að viðskiptavinur er látinn vita þegar reikningur er að falla á gjalddaga. Valið **Aðgerð fyrir ítrekun** er hægt að stilla til að leyfa að bregðast við einu skrefi í hverju stigveldi ferlis fyrir hvern reikning þegar tímasetning reiknings nær því skrefi.

### <a name="process-hierarchy"></a>Stigveldi ferlis
Hverjum viðskiptavinahóp er aðeins hægt að úthluta á eitt stigveldi ferlis. Stigveldisstaðan í þessu skrefi segir til um hvaða ferli mun hafa forgang ef viðskiptavinur er hafður með í fleiri en einum hóp sem hefur verið úthlutað ferlisstigveldi. Hópkennið ákvarðar hvaða viðskiptavinum verður úthlutað á ferlið. Hvert stigveldi sem er sett upp er aðeins hægt að úthluta á eitt sjálfvirkniferli.

Rólegir dagar eru notaðir til að tryggja að sjálfvirka ferlið hafi ekki of oft samband við viðskiptavin. Til dæmis, ef rólegir dagar eru stilltir á tvo, mun sjálfvirka ferlið ekki hafa samband við viðskiptavin í að minnsta kosti tvo daga, jafnvel þótt upprunalegi fremsti reikningurinn hafi verið gerður upp að fullu. 

Til að útiloka viðskiptavini frá sjálfvirka ferlinu, ef aldursstaða viðskiptavinar eða reikningsupphæð er minni en skilgreint gildi, skal velja **Aldursstaða viðskiptavinar minni en** eða **Reikningsupphæð lægri en** í reitnum **Útiloka úr ferli** og færa inn gildi upphæðar.

Merktu **Nota spá** til að stofna innheimtuaðgerðir með því að nota greiðsluspár viðskiptavinar. Aðgerðirnar sem búnar eru til munu nota aðgerðarsniðmátið úr **Greiðsluspám** á síðunni **Færibreytur viðskiptakrafna**, í flipanum **Sjálfvirkni innheimtuferlis**. 

### <a name="process-details"></a>Upplýsingar um ferli
Smelltu á **Nýtt** til að bæta upplýsingum um nýtt ferli við stigveldið. **Lýsing** er notuð til að auðkenna tilgang eða heiti skrefsins í stigveldinu. Veldu **Gerð aðgerðar** til að skilgreina skrefið sem býr til aðgerð, sendir tölvupóst eða stofnar innheimtubréf. 

- **Viðskiptaskjalið** skilgreinir sniðmátið sem notað er til að stofna gerð aðgerðar. Þetta skjal getur verið verkþáttarsniðmát, tölvupóstssniðmát eða innheimtubréf sem er sent á hvern viðskiptavin. Sjálfvirkni innheimtuferlis býr aðeins til innheimtubréf á hvern viðskiptavin óháð því hvernig aðrar innheimtufæribreytur eru stilltar.
- **Þegar** skilgreinir skref ferlis sem á sér stað á undan eða eftir elsta gjalddaga reiknings og er notað saman með tölunni sem er sýnd í dálknum **Dagar í tengslum við gjalddaga reiknings**. 
- Merktu við valkostinn **Aðgerð fyrir ítrekun** til að búa til aðgerð fyrir hvern reikning í einu skrefi í stigveldi úrvinnslu. Aðgerðir fyrir ítrekun eru yfirleitt tilkynning með góðum fyrivara sem tengist útistandandi reikningum þannig að hægt sé að tilkynna viðskiptavini þegar reikningur er að falla á gjalddaga. Aðgerð fyrir ítrekun er aðeins hægt að merkja fyrir einn verkþátt í hverju stigveldi. Þegar gerð tölvupóstsaðgerðar er valin verður viðtakandinn notaður til að skilgreina hvort tölvupóstskeyti er sent til viðskiptavinar, söluhóps eða tengiliðar innheimtufulltrúa. 
- Gildið í reitnum **Viðskiptatengiliður** mun síðan ákvarða hvaða tengiliður úr þessum reikningi viðskiptavinar komi til með að fá samskiptaboðin.

### <a name="business-document-details"></a>Upplýsingar um viðskiptaskjal
Upplýsingar um viðskiptaskjal eru mismunandi eftir gerð aðgerðar sem er valin í upplýsingum um ferlið. Þegar gerð aðgerðar er verkþáttur verða upplýsingar um verkþáttarsniðmát sýndar. Þessar upplýsingar fela í sér heiti verkþáttarsniðmáts, gerð verkþáttar sem verður stofnuð, tilgang verkþáttarins, fjölda daga sem áætlað er að ljúka verkþættinum og upplýsingar um verkþáttinn. Þessi verkþáttur tengist síðan við fremsta reikninginn sem segir viðtakanda aðgerðarinnar að hann sé nauðsynlegur til að ljúka aðgerðinni.

Ef gerð aðgerðar er tölvupóstur í upplýsingum um ferli mun þessi hluti innihalda tvo flýtiflipa. Sá fyrsti er notaður til að skilgreina sniðmátskennið, lýsingu tölvupósts, sjálfgefið tungumál, notandanafn sem verður úthlutað á tölvupóstskilaboðin sem eru send sjálfkrafa og netföng þeirra sem senda tölvupóstinn. Sá seinni mun leyfa að meginmál tölvupóstsins verði stofnað eftir að gildin í reitunum **Tungumál** og **Efni** eru vistuð með því að velja **Breyta**. Þetta opnar glugga sem leyfir að hlaðið sé upp HTML-efni. 

> [!Note]
> Þú getur vistað tölvupóstskeyti í Outlook sem inniheldur meginmál samskiptanna á HTML-sniði. Síðan er hægt að hlaða upp skilaboðunum til að innleiða sniðmátið. <br> <br> Ef gerð aðgerðar fyrir innheimtubréf er valin verður ekki upplýsingahluti um viðskiptaskjal á uppsetningarsíðu.

Notið hnappinn **Ferill innheimtuferlis** til að skoða nýjasta ferilinn fyrir valið stigveldi ferlis. 

Smelltu á aðgerðina **Úthlutun innheimtuferlis** til að skoða viðskiptavini sem er úthlutað á innheimtuferli. Notaðu **Forskoða úthlutun viðskiptavinar** til að skoða stigveldið sem úthlutað er tilteknum viðskiptavini. Notaðu **Forskoða úthlutun ferlis** til að forskoða viðskiptavinina sem verður úthlutað á stigveldi þegar það er keyrt. Smellið á **Handvirk úthlutun** til að skoða viðskiptavini sem búið er að úthluta handvirkt á ferli eða veljið viðskiptavini sem á að úthluta í ferli.

Smellið á aðgerðina **Hermun aðgerðar** til að forskoða aðgerðir sem verða stofnaðar ef valin sjálfvirkni ferlisins er keyrð á þessum tíma. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

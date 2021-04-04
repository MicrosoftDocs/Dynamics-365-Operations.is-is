---
title: Sjálfvirkni innheimtuferlis
description: Þetta efnisatriði lýsir því hvernig á að setja upp aðferðir innheimtuferlis sem sjálfkrafa auðkenna reikninga viðskiptavina sem krefjast áminningar í tölvupósti, innheimtuaðgerðar eða innheimtubréfs sem á að senda viðskiptavininum.
author: panolte
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a5f5d65f3f757163b22d35c3c99b4d6b7fbdfafb
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582752"
---
# <a name="collections-process-automation"></a>Sjálfvirkni innheimtuferla

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp aðferðir innheimtuferlis sem sjálfkrafa auðkenna reikninga viðskiptavina sem krefjast áminningar í tölvupósti, innheimtuaðgerðar (svo sem símtals) eða innheimtubréfs sem á að senda viðskiptavininum. 

Fyrirtæki eyða verulegum tíma í að rannsaka skýrslur um aldursgreindar stöður, viðskiptavinalykla og opna reikninga til að finna út hvaða viðskiptavini ætti að hafa samband við vegna opins reiknings eða reikningsstöðu. Þessi rannsókn tekur tíma frá innheimtufulltrúanum sem fer í samskipti við viðskiptavini um að safna gjaldföllnum greiðslum eða ráða fram úr ágreiningi vegna reikninga. Sjálfvirkni innheimtuferlis gerir þér kleift að setja upp stjórnunartengda nálgun á innheimtuferlinu. Þetta hjálpar til við að beita innheimtuaðgerðum með stöðugum hætti með því að bjóða upp á sérsniðnar áminningar í tölvupósti eða forritað ferli til að senda innheimtubréf. 

## <a name="collections-process-setup"></a>Uppsetning innheimtuferlis
Hægt er að nota síðuna **Uppsetning innheimtuferlis** (**Skuldir og innheimta > Uppsetning > Uppsetning innheimtuferlis**) til að búa til sjálfvirkt innheimtuferli sem tímasetur aðgerðir, sendir tölvupósta og stofnar og sendir innheimtubréf til viðskiptavina. Skref ferlisins byggja á fremsta eða elsta opna reikningnum. Hvert skref notar þennan reikning til að ákvarða hvaða samskipti eða aðgerð á að fara fram varðandi tiltekinn viðskiptavin.  

Innheimtuhópar senda yfirleitt út tilkynningu með góðum fyrirvara sem tengist ákveðnum útistandandi reikningi þannig að viðskiptavinur er látinn vita þegar reikningur er að falla á gjalddaga. Valið **Aðgerð fyrir ítrekun** er hægt að stilla til að leyfa að bregðast við einu skrefi í hverju stigveldi ferlis fyrir hvern reikning þegar tímasetning reiknings nær því skrefi.

### <a name="process-hierarchy"></a>Stigveldi ferlis
Hverjum viðskiptavinahóp er aðeins hægt að úthluta á eitt stigveldi ferlis. Stigveldisstaðan í þessu skrefi segir til um hvaða ferli mun hafa forgang ef viðskiptavinur er hafður með í fleiri en einum hóp sem hefur verið úthlutað ferlisstigveldi. Hópkennið ákvarðar hvaða viðskiptavinum verður úthlutað á ferlið. 

Rólegir dagar eru notaðir til að tryggja að sjálfvirka ferlið hafi ekki of oft samband við viðskiptavin.  Til dæmis, ef rólegir dagar eru stilltir á tvo, mun sjálfvirka ferlið ekki hafa samband við viðskiptavin í að minnsta kosti tvo daga, jafnvel þótt upprunalegi fremsti reikningurinn hafi verið gerður upp að fullu. 

Til að útiloka viðskiptavini frá sjálfvirka ferlinu, ef staða á lykli eða reikningi er minni en skilgreint gildi, skal stilla reitinn **Útiloka úr ferli** á **Já** og færa inn gildi upphæðar.

## <a name="process-details"></a>Upplýsingar um ferli
**Lýsing** er notuð til að auðkenna tilgang eða heiti skrefsins í stigveldinu.

**Gerð aðgerðar** skilgreinir hvort skrefið búi til aðgerð, sendi tölvupóst eða búa til innheimtubréf.

**Viðskiptaskjal** skilgreinir sniðmátið sem notað er til að stofna gerð aðgerðar.  Þetta getur verið verkþáttarsniðmát, tölvupóstssniðmát eða innheimtubréf á hvern viðskiptavin. 

Hægt er að stofna gerðir aðgerða annaðhvort fyrir eða eftir gjalddaga reiknings, á grundvelli stillingarinnar sem er sýnd í dálknum **Dagar í tengslum við gjalddaga reiknings**.

Þegar gerð tölvupóstsaðgerðar er valin verður viðtakandinn notaður til að skilgreina hvort um sé að ræða viðskiptavin, söluhóp eða tengilið innheimtufulltrúa. Gildið í reitnum **Viðskiptatengiliður** mun síðan ákvarða hvaða tengiliður úr þessum reikningi viðskiptavinar komi til með að fá samskiptaboðin.

## <a name="business-document-details"></a>Upplýsingar um viðskiptaskjal
Upplýsingar um viðskiptaskjal eru mismunandi eftir gerð aðgerðar sem er valin í upplýsingum um ferlið.  Þegar gerð aðgerðar er verkþáttur verða upplýsingar um verkþáttarsniðmát sýndar.  Þessar upplýsingar fela í sér heiti verkþáttarsniðmáts, gerð verkþáttar sem verður stofnuð, tilgang verkþáttarins, fjölda daga sem áætlað er að ljúka verkþættinum og upplýsingar um verkþáttinn.  Þessi verkþáttur tengist síðan við fremsta reikninginn sem segir viðtakanda aðgerðarinnar að hann sé nauðsynlegur til að ljúka aðgerðinni.

Ef gerð aðgerðar er tölvupóstur í upplýsingum um ferli mun þessi hluti innihalda tvo flýtiflipa.  Sá fyrsti er notaður til að skilgreina sniðmátskennið, lýsingu tölvupósts, sjálfgefið tungumál, notandanafn sem verður úthlutað á tölvupóstskilaboðin sem eru send sjálfkrafa og netföng þeirra sem senda tölvupóstinn. Sá seinni mun leyfa að meginmál tölvupóstsins verði stofnað eftir að gildin í reitunum **Tungumál** og **Efni** eru vistuð með því að velja **Breyta**.  Þetta opnar glugga sem leyfir að hlaðið sé upp HTML-efni. Einnig er hægt að slá inn skilaboðin sem eru búin til handvirkt í neðri kassanum vinstra megin í glugganum.  

> [!Note]
> Hægt er að vista Outlook tölvupóst með samskiptunum í meginmálinu á HTML-sniði. Síðan er hægt að hlaða upp til að innleiða sniðmátið. <br> <br> Ef gerð aðgerðar fyrir innheimtubréf er valin verður ekki upplýsingahluti um viðskiptaskjal á skjámynd uppsetningar.


## <a name="fasttab-reference"></a>Vísun í flýtiflipa
Í eftirfarandi töflum eru síðurnar og reitirnir sýndir þar sem hægt er að komast í tiltekna flýtiflipa, ásamt lýsingu á upplýsingunum í þeim flipa. 

### <a name="process-hierarchy"></a>Stigveldi ferlis

|     Síða                                                  |     Svæði                         |     lýsing                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |                                   |     Stofnið og stjórnið innheimtuferlum sem byggja á úthlutunum viðskiptavinahópa.                                                                                                                             |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |     Stigveldi                     |     Skilgreinir forgang sjálfvirks ferlis við úthlutun viðskiptavinar ef þeir tilheyra mörgum hópum.                                                                                                   |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |     Kenni hóps                       |     Fyrirspurnir sem skilgreina flokk viðskiptamannafærsla.                                                                                                                                                        |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |     Hvíldardagar                    |     Takmarka hversu oft hægt er að ljúka ferlisstigi. Til dæmis, ef tveir rólegri dagar eru stilltir gerist næsta skref ferlisins ekki í að minnsta kosti tvo daga ef fremsti reikningurinn breytist.     |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |     Útiloka úr ferli        |     Með því að velja annaðhvort **Aldursstaða viðskiptavinar minni en** eða **Reikningsupphæð lægri en** verður viðskiptavinur útilokaður frá sjálfvirka ferlinu ef skilyrði eru ekki uppfyllt.                                   |

### <a name="process-details"></a>Upplýsingar um ferli
|     Síða                                                  |     Svæði                                         |      lýsing                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |                                                   |     Skilgreina skrefin sem eru tekin út frá fremsta innkaupareikningi.                                                                                                |
|                                                           |     lýsing                                   |     Reitur fyrir frjálsan texta sem notaður er til að gefa upp heiti og/eða lýsingu á skrefinu.                                                                           |
|                                                           |     Gerð aðgerðar                                   |     Verkþáttur, tölvupóstur eða innheimtubréf sem verður stofnað af skrefi ferlisins.                                                                     |
|                                                           |     Viðskiptaskjal                           |     Skilgreinir sniðmát verkþáttar eða tölvupósts sem er notað við skref ferlisins.                                                                        |
|                                                           |     Hvenær                                          |     Skilgreinir hvort úrvinnsluskrefið eigi sér stað fyrir eða eftir gjalddaga fremsta reiknings ásamt reitnum **Dagar í tengslum við gjalddaga reiknings**.        |
|                                                           |     Dagar í tengslum við gjalddaga reiknings        |     Ásamt reitnum **Hvenær** skilgreinir hann tímasetningu skrefsins í ferlinu.                                                                          |
|                                                           |     Aðgerð fyrir ítrekun                                   |     Þetta val gerir kleift að stilla og keyra eitt skref í hverju stigveldi ferlis á móti hverjum reikningi þegar hann nær skilyrði tímasetningarinnar.                                                |
|                                                           |     Viðtakandi                                     |     Gefur til kynna hvort tölvupóstur verði sendur til viðskiptavinar, söluhóps eða tengiliðs innheimtuaðila.                                                   |
|                                                           |     Viðskiptatengiliður                    |     Ákvarðar hvaða netfang viðtakanda er notað í tölvupóstsamskiptum.                                                                                 |

### <a name="business-process-activity-template-details"></a>Upplýsingar um sniðmát fyrir verkþátt viðskiptaferlis 
|     Síða                                                  |     Svæði                     |      lýsing                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |                               |     Hluti uppsetningarferlisins sem auðkennir upplýsingar um verkþáttarsniðmátið.                                                                      |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |     Sniðmát verkþáttar       |     Tilgreinir gerð, tilgang, fjölda daga til að ljúka, og veitir upplýsingar um verkþáttinn sem verður stofnaður við skref verkþáttarferlis.       |

### <a name="business-document-email-template-details"></a>Upplýsingar um sniðmát fyrir tölvupóst viðskiptaskjals 
|     Síða                                                  |     Svæði     |      lýsing                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Uppsetning innheimtuferlis <br> Sjálfvirkni ferlis       |               |     Tilgreinir lýsingu á tölvupósti, sjálfgefið tungumál, heiti sendanda og netfang sem verður stofnað í skrefi fyrir ferli tölvupósts.        |


### <a name="collections-history"></a>Innheimtusaga 
|     Síða                              |     Svæði     |      lýsing                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Uppsetning innheimtuferlis       |               |     Skoðið nýjasta ferilinn fyrir valið stigveldi ferlis.       |

### <a name="collection-process-assignment"></a>Úthlutun innheimtuferlis
|     Síða                              |     Svæði     |      lýsing                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Uppsetning innheimtuferlis       |               |     Skoðið viðskiptavini sem er úthlutað á innheimtuferli.  
|     Handvirk úthlutun               |               |     Skoðið viðskiptamenn sem búið er að úthluta handvirkt á ferli eða veljið viðskiptavini sem á að úthluta í ferli. |
|     Forskoða úthlutun ferlis      |               |     Forskoðið viðskiptavinina sem verður úthlutað á áætlun þegar hún er keyrð.   |
|     Forskoða úthlutun viðskiptavinar     |               |     Skoðið stefnu sem tilteknum viðskiptamanni hefur verið úthlutað.    |
 
 ### <a name="process-simulation"></a>Hermun aðgerðar
|     Síða                              |     Svæði     |      lýsing                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|    Hermun aðgerðar                 |               |     Forskoðið aðgerðirnar sem verða stofnaðar ef valin sjálfvirkni ferlisins er keyrð á þessum tíma. |

### <a name="parameters"></a>Færibreytur
|     Síða                                                                  |     Svæði                                             |      lýsing                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Færibreytur viðskiptakrafna > Sjálfvirkni innheimtuferlis     |     Hlutfall viðskiptavina í hverju runuverki          |     Stilling til að ákvarða fjölda runuverka fyrir hvert sjálfvirkt ferli.                                          |
|     Færibreytur viðskiptakrafna > Sjálfvirkni innheimtuferlis     |     Bóka innheimtubréf sjálfkrafa           |     Gerðir aðgerða fyrir innheimtubréf munu birta bréfið meðan sjálfvirknin er í gangi.                                      |
|     Færibreytur viðskiptakrafna > Sjálfvirkni innheimtuferlis     |     Stofna verkþætti fyrir sjálfvirkni                |     Stofnið og lokið verkþáttum fyrir gerðir aðgerðar sem ekki eru verkþáttargerðar til að skoða öll sjálfvirku skrefin sem eru tekin á reikningi.        |
|     Færibreytur viðskiptakrafna > Sjálfvirkni innheimtuferlis     |     Dagar sem geyma á sjálfvirkni innheimtuferlis     |     Skilgreinir fjölda daga sem innheimtuferill er geymdur.                                                       |
|     Færibreytur viðskiptakrafna > Sjálfvirkni innheimtuferlis     |     Útiloka reikning eftir virkjun síðasta skref ferlis    |     Reikningur sem nær til síðasta skrefs innheimtuferlisins verður ekki notaður til að búa til gerðir sjálfvirkniaðgerða í framtíðinni. Næstelsti reikningurinn ákvarðar næsta sjálfvirkniskref til að tryggja að sjálfvirkniaðgerðir fyrir innheimtuferlið haldi áfram.                                                        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

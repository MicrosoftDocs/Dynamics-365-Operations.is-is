---
title: "Verkskráning og hjálp fyrir sölustað"
description: "Þetta efnisatriði lýsir hvernig á að nota verkskráningu í tungumálastillingum í Cloud POS og Retail Modern POS."
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 12aa71843fa8b22eb7ae688ed3600168760d90da
ms.contentlocale: is-is
ms.lasthandoff: 03/08/2018

---

# <a name="task-recorder-and-help-for-pos"></a>Verkskráning og hjálp fyrir sölustað

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að nota verkskráningu í tungumálastillingum í Cloud POS og Retail Modern POS.

<a name="overview"></a>Yfirlit
--------

Verkskráning í Retail Modern POS or Cloud POS er ný lausn sem var þróuð með áherslu á mikla viðbragðsflýti. Hún býður upp á sveigjanleg forritaskil (API) sem eykur þenslugetu og auðveldar snurðulausa samþættingu við neytendur skráninga verkferla. Að auki hefur samþætting verkskráningar við viðskiptaferlavinnslutólið (BPM) í Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) verið þróuð áfram. Notendur geta því haldið áfram að búa til efnismiklar skýringarmyndir verkferla úr skráningum til að greina og þróa forrit sín.

## <a name="architecture"></a>Högun
Verkskráning getur skráð aðgerðir notanda í biðlara af mikilli nákvæmni. Hver stjórntakki er stilltur til að tilkynna verkskráningu um allar framkvæmdar aðgerðir notanda. Stjórntakkinn tillkynnir verkskráningu að tilvik hafi átt sér stað og kemur til skila öllum veigamiklum upplýsingum um samsvarandi rauntímaaðgerð notanda. Þessar upplýsingar úr verkskráning geta safnað gerðum notandaaðgerða (svo sem smellum á hnappa, færslu gilda eða flettingum) og öllum gögnum sem tengjast notandaaðgerða (svo sem gildum og gerð innsláttargagna, samhengi skjámynda eða samhengi færslna). Verkskráning viðheldur upplýsingum af nægilegri nákvæmni til að tryggja að afspilun upptökunnar geti framkvæmt skráðar aðgerðir nákvæmlega eins og notandinn framkvæmdi þær. (Afspilunareiginleikinn hefur ekki enn verið innleiddur í Retail Modern POS eða Cloud POS.)

## <a name="basic-configuration"></a>Einföld grunnstilling
Fylgið eftirfarandi skrefum til að virkja verkskráningu á sölustað:

1.  Smelltu á **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Afgreiðslukassar**.
2.  Smellið á afgreiðslukassa til að kveikja á verkskráningu.
3.  Á flipanum **Afgreiðslukassi** á flýtiflipanum **Almennt** skal stilla valkostinn **Kveikja á verkskráningu** á **Já**.
4.  Smellt er á **Vista**.
5.  Farðu í **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlun**.
6.  Veljið verkið **Afgreiðslukassar (1090)** og smellið svo á **keyra núna**.

## <a name="create-a-recording"></a>Stofna skráningu
Fylgið þessum skrefum til að stofna nýja skráningu með því að nota Verkskráningu.

1.  Ræsa Retail Modern POS eða Cloud POS, og skrá inn.
2.  Á síðunni **Stillingar** í hlutanum **Verkskráning** er smellt á **Opna verkskráningu**. Rúðan **Verkskráning** birtist. Hægt er að smella á hnappinn **Loka** (**X**) í efra hægra horni til að loka rúðunni **Verkskráning** áður en byrjað er á nýrri skráningu. Endurtakið skref 2 til að opna rúðuna aftur.
[![Rúðan Verkskráning birtist](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3.  Sláið inn nafn og lýsingu fyrir skráninguna, og smellið á **Ræsa**. Skráningarlotan hefst um leið og smellt er á **Ræsa**.

**Athugið:** Ef smellt er á hnappinn **Loka** (**X**) í efra hægra horni á meðan skráning er í gangi er rúðunni fyrir **Verkskráningu** lokað en skráningarlotunni er ekki hætt. Til að enduropna rúðuna fyrir verkskráningu skal smella á hnappinn **Hjálp** (spurningamerki) efst á skjánum. 

[![Spurningarmerki](./media/help.jpg)](./media/help.jpg)

4.  Eftir að smellt er á **Ræsa** fer Verkskráning í skráningarstillingu. Rúðan **Verkskráning** sýnir upplýsingar og stjórntakka sem tengjast skráningarferlinu.
5.  Framkvæmið aðgerðirnar sem á að framkvæma í notandaviðmóti (UI) Retail Modern POS eða Cloud POS.
6.  Smellið á **Stöðva** til að stöðva skráninguna.

## <a name="download-options"></a>Niðurhalsvalkostir
Þegar búið er að ljúka lotunni birtast nokkrir valkostir birtast til að hægt sé að hala niður skráningunni. 
[![Valkostir við niðurhal](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Vista í þessari tölvu

Verkskráningarpakkann er hægt að nota til að spila verkefnaleiðbeiningar, vinna með upptökuna eða breyta færslum upptökunnar. (Þessi eiginleiki er ekki enn innleiddur í Retail Modern POS og Cloud POS.)

### <a name="export-as-word-document"></a>Flytja út sem Word-skjal

Hægt er að vista skráningu sem Microsoft Word-skjal. Skjalið inniheldur skráð skref og skjámyndirnar sem voru vistaðar.

### <a name="save-as-developer-recording"></a>Vista sem skráningu þróunaraðila

Óunnin upptökuskráin nýtist vel í þróunarsviðsmyndum, t.d. við myndun prófunarkóða. (Þessi eiginleiki er ekki enn innleiddur.)

## <a name="recording-controls"></a>Stýringar verkskráningar
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a>[![Stýringar verkskráningar](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Stöðva

Smellið á **Stöðva** til að stöðva skráninguna. Athugið að hægt er að byrja aftur á lotu eftir að hún hefur verið stöðvuð. Því skal ganga úr skugga um að skráningunni sé lokið áður en henni er hætt.

### <a name="pause"></a>Hlé

Smellt er á **Hlé** til að stöðva skráninguna tímabundið (gera hlé) og halda áfram við aðgerðina. Skrefin sem framkvæmd eru eftir að smellt er á **Hlé** eru ekki skráð..

### <a name="continue"></a>Halda áfram

Smellið á **Halda áfram** til að halda áfram með skráningarlotuna eftir að hlé var gert á henni.

### <a name="capture-screenshots"></a>Taka skjámyndir

Verkskráning getur tekið skjámyndir af notendaviðmóti Retail Modern POS á meðan þú skráir viðskiptaferli. Til að kveikja á eiginleikanum til að taka skjámyndir skal stilla valkostinn **Taka skjámynd** á **Já** og svo framkvæma upptökuna. Þegar upptökunni er lokið skal smella á **Stopp** og hlaða niður Word-skjalinu. Skjalið mun innihalda skrefin með viðeigandi skjámyndum.

#### <a name="note"></a>Athugið
> Virknin Taka skjámynd er ekki studd í Cloud POS.

### <a name="start-task-and-end-task"></a>Hefja verk og Ljúka verki

Hægt er að tilgreina upphaf og endi mengis skrefa sem flokkuð eru saman í hópa með því að nota hnappana **Hefja verk** og **Ljúka** **verki**. Smellið á **Hefja verk** til að bæta við „Hefja verk“-skrefi og framkvæmið svo skrefið sem á að taka með í hópnum. Þegar búið er að framkvæma skrefin fyrir þennan hóp er smellt á **Ljúka verki**. Verk hjálpa þér að skipuleggja verkferlin þín. Verk er hægt að falda innan annarra verka. Þannig verður auðveldara að skipuleggja mjög löng og flókin viðskiptaferli.

## <a name="adding-annotations"></a>Athugasemdum bætt við
Athugasemd er viðbótartexti sem bætt er við skref í skráningu. Til dæmis er hægt að nota athugasemdir til að gefa notandanum skýrara samhengi eða leiðbeiningar. Hægt er að bæta við athugasemdir á undan or á eftir a skref.athugasemdum á undan eða á eftir þrepi. Hægt er að bæta við athugasemd í hvaða skrefi sem er með því að smella á hnappinn **Breyta** (blýantstákn) hægra megin við skrefið. 

[![Breyta hnappi fyrir þrep](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Textar og athugasemdir

Hægt er að nota reitina **Textar** og **Athugasemdir** til að bæta við texta sem ætti að tengja við skref í Verkefnaleiðbeiningum.
[![Reitirnir Texti og Athugasemdir](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Texti

Texti sem færður er inn í reitinn **Texti** birtist *fyrir ofan* texta fyrir skref í Verkefnaleiðbeiningum. Þessi staðsetning er fyrir textann sem notandinn að lesa áður en hann eða hún lýkur við skrefið.

#### <a name="notes"></a>Athugasemdir

Texti sem færður er inn reitinn **Texti** birtist *undir* texta um skref í Verkefnaleiðbeiningum. Til að lesa textann fyrir athugasemdina þarf notandinn að víkka texta um skref í sprettiglugga. Þessi staðsetning er fyrir valfrjálst lesefni eða aðrar upplýsingar sem gætu verið gagnlegar fyrir notandann en sem notandinn þarf ekki nauðsynlega að lesa áður en hann eða hún lýkur við aðgerðina.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Hjálp á Retail Modern POS og Cloud POS
Til að sýna þínar eigin sérsniðnu verkskráningar í rúðunni Hjálp fyrir Hjálp á Retail Modern POS og Cloud POS þannig að hægt er að skoða þær sem texta eða skoða texta þarf að vista verkskráninguna í eigin BPM-safni og síðan uppfæra færibreytur Hjálparkerfis til að vísa í BPM-safnið þitt. Nánari upplýsingar, sjá [ tengja hjálparkerfisins ](../fin-and-ops/get-started/help-connect.md). Retail Modern POS og Cloud POS Help leita í LCS í rauntíma. Leitin er gerð í öllum BPM-söfnum sem valin eru í færibreytum fyrir Hjálparkerfi Microsoft Dynamics 365 for Retail og leitin birtir viðeigandi niðurstöður. Til að komast í valmyndina **Hjálp** er smellt á hnappinn **Hjálp** (spurningamerki) efst á skjánum og síðan er heiti verkferlisins slegið inn í leitargluggann og smellt á hnappinn Leita. 

[![Hnappurinn Hjálp](./media/help.jpg)](./media/help.jpg) 

Þegar smellt er á Verkefnaleiðberiningar í leitarniðurstöðum er hægt að skoða þrepin sem hjálparefni eða flytja út þrepin í Word-skjal. 
#### <a name="note"></a>Nóta
> Hjálp í Retail POS Nútímaleg og sölukerfi í SKÝINU verður ekki reitsins verkefni leiðbeiningunum samkvæmt hvaða skjámynd sem er notað eða afskriftareglur er að gera aðgerðina. Hafa við vinnslu nafn í reitnum leit og smellið síðan á **Leit**.



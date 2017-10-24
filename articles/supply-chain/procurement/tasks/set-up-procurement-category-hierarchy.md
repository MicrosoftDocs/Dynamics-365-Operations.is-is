--- 
title: Setja upp stigveldi innkaupategundar
description: "Þetta ferli sýnir hvernig á að stofna nýja hnúta í tegundastigveldi innkaupa og hvernig á að skilgreina innkaupategund sem nota á í innkaupaferli."
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Setja upp stigveldi innkaupategundar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að stofna nýja hnúta í tegundastigveldi innkaupa og hvernig á að skilgreina innkaupategund sem nota á í innkaupaferli. Þessum verkefnum myndi venjulega að framkvæma af Innkaupastjóra. Áður en hægt er að hefja ferlið, verður að vera tegundastigveldi af gerðinni Innkaup. Ef verið er að nota sýnigögn fyrirtæki er hægt að keyra þetta ferli í USMF fyrirtæki.


## <a name="add-a-new-procurement-category"></a>Bæta við nýrri innkaupategund
1. Fara í Innkaup og uppruni > .. > Innkaupaflokkar.
2. Smella á Breyta tegundastigveldi.
    * Núverandi tegundastigveldi birtist vinstra megin á síðunni. Verið er að breyta stigveldi.  
3. Smellt er á Nýr tegundahnútur.
    * Kerfið velur topphnútinn sjálfgefið. Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk, er hægt að smella á hnappinn Aflæsa og velja annan yfirhnút til að setja inn nýjan hnútinn þinn. Þegar því er lokið, skal loka aftur leiðarvísi fyrir verk og smellið síðan á Nýjan tegundahnút.  
4. Í reitinn Heiti skal slá inn gildi.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Í reitinn stutt heiti skal slá inn gildi.
    * Stutt heiti er valfrjálst. Það verður birt í uppflettingu tegunda ásamt heiti flokks.  
7. Smellið á „Vista“.

## <a name="add-products-to-your-new-procurement-category"></a>Bæta afurðum við nýja innkaupategund
1. Fara í Innkaup og uppruni > .. > Innkaupaflokkar.
    * Velja hnút sem var nýlega bætt við. Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk gæti þurft að aflæsa leiðarvísi fyrir verk til að velja hnútinn.  
2. Víxla útvíkkun á liðnum afurð.
3. Smella á bæta við til að tengja afurðir við innkaupategund.
4. Velja afurð sem á að bæta við innkaupategund.
5. Smellið á örina til að velja afurðina.
6. Veljið aðra afurð til að bæta við innkaupategundina.
7. Smellið á örina til að velja afurðina.
8. Smellið á „Í lagi“.

## <a name="add-approved-and-preferred-vendors"></a>Bæta við samþykktum og æskilegum lánardrottnum
1. Víxla útvíkkun á liðnum lánardrottinn.
2. Smelltu á Bæta við.
    * Hægt er að bæta lánardrottni við innkaupategund og tilgreina hvort lánardrottinn sé útvalinn eða aðeins samþykktur fyrir flokkinn. Þegar lánardrottni er eytt úr tegund, er sögulegum færslum með lánardrottininn í tegundinn ekki eytt.   
3. Finna lánardrottins sem óskað er að bæta við tegund.
4. Smellið á örina til að velja lánardrottinn.
5. Smellt er á Í lagi.
6. Veldu lánardrottnalínuna sem á að breyta.
7. Í reitnum Staða lánardrottins skal velja valkost.
    * Stillingin val lánardrottna í tegundarstefnureglu stjórnar því hvort æskilegt, samþykkt eða alla lánardrottna eru tiltækir á innkaupabeiðnum.   

## <a name="add-additional-information-to-the-category"></a>Bæta við frekari upplýsingum við tegund
1. Víxla útvíkkun á hlutanum matsviðmiðaflokkur lánardrottins.
    * Þessi flipi gerir mögulegt að skilgreina hvaða skilyrði lánardrottna í innkaupategund á að gefa einkunn gagnvart. Til að gera þetta myndirðu smella á bæta Við og veljið síðan matsviðmiðunarflokkur lánardrottins sem inniheldur skilyrðin sem óskað er eftir.  
2. Víxla útvíkkun á liðnum Spurningalisti.
    * Þessi flipi gerir mögulegt að bæta spurningalistum sem mun birtast í beiðninni, svo lengi sem stillt er á gerð Verkþáttar „Innkaupabeiðni". Umsækjandinn þarf svo að fylla út spurningalista áður en þeir senda innkaupabeiðni fyrir tiltekna vöru eða afurðir í innkaupategund.  
3. Víxla útvíkkun á hlutanum VSK-flokkur vöru.
4. Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.
5. Velja VSK-flokk.
6. Víxla útvíkkun á liðnum tegundasíða.
    * Tegundarsíður eru stofnaðar í síðu tegundastigveldis. Þær innihalda upplýsingar um innkaupategundina, eins og upplýsingar um tegund afurða í flokknum, myndir af afurðum í flokki eða tilkynningar um að afsláttur sé í boði í flokknum. Upplýsingarnar í tegundasíðu birtist á innkaupabeiðnum.  
7. Lokið síðunni.



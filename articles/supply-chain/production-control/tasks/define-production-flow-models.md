--- 
title: "Skilgreina líkön framleiðsluflæðis"
description: "Framleiðsluflæðislíkön lýsa því hvernig afkastageta vinnuflokkur lean-framleiðsla er reiknaður og honum viðhaldið."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7850a121ca06f25f6c532e49e18c0b6811bd7455
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="define-production-flow-models"></a>Skilgreina líkön framleiðsluflæðis

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Framleiðsluflæðislíkön lýsa því hvernig afkastageta vinnuflokkur lean-framleiðsla er reiknaður og honum viðhaldið. Þess vegna er skilgreiningu á framleiðsluflæðislíkan skilyrði fyrir skilgreiningar vinnuflokkana. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="define-a-production-flow-model"></a>Skilgreina líkan framleiðsluflæðis. 
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæðilíkön.
2. Smellið á „Nýtt“.
3. Færið inn Kenni fyrir framleiðsluflæðislíkan á í svæði líkan framleiðsluflæðis.
4. Veljið valkost í svæðinu gerð Líkans.
    * Til eru tvær gerðir líkan: gerð Gegnumstreymi og gerð Tíma. Fyrir gerð Gegnumstreymi er afkastagetu vinnuflokkana sem nota þessa framleiðsluflæðislíkan verður sýnd og reiknuð í magni afurðar. Fyrir Tíma, afkastageta vinnuflokkana sem notar þessa framleiðsluflæðislíkan verður sýnd og reiknuð í klukkustundum. Athugið að ekki er hægt að breyta þessum eiginleika fyrir fyrirliggjandi framleiðsluflæðislíkan. Eftir vinnuflokks með frátekna afkastagetu er ekki hægt að breyta gerð líkan framleiðsluflæðis.  
5. Fjöldi daga í hverju EPE ferli er færður inn.
    * Bilið lýsir tímabilið þegar öllum hlutum sem framleidd eru af framleiðsluflæðis eða vinnuflokki mun minnst einu sinni vera framleitt. Því styttra sem epe-ferli er, því sveigjanlegri framleiðsluferlið er. Ef epe-Ferli = 0 verða öll eftirspurn framleiða í sama dag. Epe-Ferli er notað til að raða lean-vinnslukenni verks. Þegar vinnsluröðun á vinnuflokkinn með EPE-Ferli = 5, áætlunarferlið leitar að afkastagetu vinnuflokksins á skiladag - EPE- ferli (5 daga fram að skiladag) til að tryggja að hægt er að framleiða vöru í því ferli. Afhendingartími birgða fyrir afurðar er yfirleitt sá sami eða hærri en epe-Ferli tengdar framleiðsluferlis.  
6. Veljið valkost í svæðinu tímabilsgerð áætlunargerðar
    * Eftir vinnuflokks með frátekna afkastagetu er ekki hægt að breyta gerð tímabilsgerð áætlunar. Aðeins er hægt að velja framleiðsluflæðislíkön með sama tímabilsgerð fyrir þessa tilteknu vinnuflokkur.  
7. Færið inn tölu í tímamörk Áætlanagerðar.
    * Tímamörk áætlanagerðar lýsir fjölda daga þar sem hægt er að gera frátekningar á afkastagetu fyrir tengdar vinnuflokkana. Færið inn fjölda daga í tímamörk Áætlanagerðar.   Kanban-ferlisvinnsla sem falla fyrir utan þetta tímabil er ekki áætluð með sjálfvirkri áætlun. Tímamörk áætlanagerðar sem er yfirleitt tvisvar sinnum meðaltal afhendingartíma fyrir vörur sem framleiddar eru í framleiðslu flæði eða vinnuflokk. EPE-Ferli á ekki vera meira en helmingur tímamörk áætlunargerðar.     
8. Veljið valkost í reitnum viðbrögð við skorti á Afkastagetu .
    * Valkostirnir eru: Fresta - Frestun fullt eftirspurn röðunartilviksins á næsta tiltæka framleiðslu dag með tiltæk afköst. Hætta við - Ljúka sjálfvirk áætlun fyrir röðunartilvik og hafa tengd verk án áætlunar.   Bæta við umbeðinn dag - Áætla umbeðin verk fyrir umbeðið tímabil. Þetta leggur of mikið álag á reitnum fyrir þennan dag og krefst þess að skipuleggjara endurskoða og framkvæma handvirk samskipti.   Dreifa á tiltækt tímabil - Dreifa á mismunandi verk röðunartilviksins á allir dagar tiltæk framleiðslu, byrja á fyrsta tiltæk degi. Lágmarks magn til dreifingar er magn kanban-vinnsla. Dreifingu úthlutar lágmarks áætlunarmagn (kanban-magn) í hverjum degi með nægilegt gegnumstreymi.  



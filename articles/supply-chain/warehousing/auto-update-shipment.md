---
title: Sjálfvirkar uppfærslur á sendingu
description: Þetta efni veitir yfirlit yfir virkni sem veitir sjálfvirkar uppfærslur fyrir sendingar.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7fa2684340f5ce45b99ff9aee9937071f936b81a
ms.sourcegitcommit: 2bc8e760c7a82572c7eafd51f2e57ef11b4ca98b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2020
ms.locfileid: "3900987"
---
# <a name="shipment-auto-updates"></a>Sjálfvirkar uppfærslur á sendingu

[!include [banner](../includes/banner.md)]

Sjálfvirk uppfærsla flutnings uppfærir sjálfkrafa magn (bæði eykur og lækkar) á álagslínu sem er tengd sendingu, eftir að álagið hefur verið losað í vöruhús. Áfram er kveikt á þessari virkni þar til álagslínan á sendingu eða álagi er unnin í bylgju. Þegar það er notað geta pöntunaruppfærslur sjálfkrafa streymt til vörugeymslu, án þess að þurfa handvirkar íhlutanir, þar til vinna vörugeymslu er búin til.

Þegar virkni sjálfvirkrar uppfærslu sendingar er ekki notuð minnkar aðeins magn sjálfkrafa þar til vinna vörugeymslu er búin til. Notendur verða að uppfæra eða eyða línum handvirkt og síðan verða þeir að gefa út línur ef pöntunarmagn er aukið eða nýjum pöntunarlínum bætt við. Með því að nota sjálfvirka uppfærslu sendingar geta fyrirtæki snurðulaust veitt uppfærslur til vöruhúss án þess að þurfa að hafa áhyggjur af því að skyldar sendingar og álag munu ekki endurspegla uppfærslur pöntunarlínunnar.

Sendingarvirkni sjálfvirkrar uppfærslu á bæði við um sölupöntunarlínur og flutningspöntunarlínur og kveikt er á því fyrir tiltekið vöruhús. Þess vegna geta fyrirtæki beitt mismunandi reglum um sjálfvirka uppfærslu á sendingum í vöruhús, allt eftir þörfum. Sjálfgefið er að stefnu um sjálfvirka uppfærslu sendingar á magni lækkar er beitt fyrir öll vöruhús sem nota vörugeymsluferli. Þegar þessi sjálfgefna reglustilling er notuð, minnkar aðeins magn sjálfkrafa streymi í sendingu og álag þar til að vinna vörugeymslu er stofnað. Þessi hegðun líkist hegðuninni sem var notuð áður en virkni sjálfvirkrar uppfærslu sendingar var kynnt.

## <a name="main-elements-of-the-functionality"></a>Helstu þættir virkninnar

Sendingarvirkni sjálfvirku uppfærslunnar byggist fyrst og fremst á stöðu sendingar til að ákvarða hvort breyta eigi magni á álagslínu þegar breyting er gerð á sölupöntunarlínu eða millifærslupöntunarlínu. Það treystir einnig fyrst og fremst á stöðu sendingar til að ákvarða hvenær ný álagslína ætti sjálfkrafa að bæta við núverandi álag. Þegar staða sendingar er **Bylgjað** eða hærri, engin sjálfvirk uppfærsla á sér stað.

Einnig er litið á bylgjustöðu fyrir sjálfvirkar uppfærslur. Þegar bylgja sem tengist álagslínunni hefur stöðuna **Biðstaða**, **Í gangi**, **Losað**, **Tekið til**, eða **Sent**, ef notandi reynir að minnka magnið á álagslínu (með magnlækkun í sölupöntunarlínunni eða millifærslupöntunarlínunni), eru eftirfarandi villuboð sýnd: „Ekki er hægt að fjarlægja frátekningar vegna þess að vinna hefur verið stofnuð sem treystir á frátekningar.“ Þar að auki, þegar bylgjan er með eina af áðurnefndum bylgjustöðum, ef notandi reynir óbeint að auka magn hleðslulínunnar með því að auka magn í sölupöntunarlínunni eða flutningspöntunarlínunni, er magnið í hleðslulínunni ekki sjálfkrafa aukið. Í þessu tilfelli verður að uppfæra álagslínuna handvirkt.

## <a name="scenarios"></a>Sviðsmyndir

Sendingarvirkni sjálfvirku uppfærslunnar styður fjórar aðstæður: bæta við nýrri pöntunarlínu, auka magn á pöntunarlínu, minnka magn í pöntunarlínu og fjarlægja pöntunarlínu.

- **Bæta við nýrri pöntunarlínu** - Þegar reiturinn **Uppfæra sendingu sjálfvirkt** á flýtiflipanum **Vöruhús** á síðunni **Vöruhús** (**Vöruhúsastjórnun \> Uppsetning \> Vöruhús \> Vöruhús**) er stilltur á **Alltaf**, ef sending er til fyrir pöntunina og nýrri pöntunarlínu er bætt við sölupöntun eða flutningspöntun eftir að álag hefur þegar verið búið til fyrir sölupöntunina, er núverandi álag ekki uppfært. Ný álagslína sem hefur enga tilvísun til núverandi álags er búin til og tengd núverandi sendingu. Nýju línunni er bætt við álagið og hún losuð.
- **Auka magnið á pöntunarlínu** - Þegar reiturinn **Uppfæra sendingu sjálfvirkt** er stilltur á **Alltaf**, ef sending er til fyrir pöntunina, og magnið á núverandi sölupöntunarlínu eða flutningspöntunarlínu er aukið eftir að þegar hefur verið búið til álag fyrir sölupöntunina, er álagslínan aukin með sama magni og pöntunarlínan. Ef álaginu var sleppt, en engin vinna búin til, er álagslínan aukin um sama magn og pöntunarlínan.
- **Lækka magn í pöntunarlínu** - Þegar reiturinn **Uppfæra sendingu sjálfvirkt** er stilltur á **Alltaf** eða **Á magnlækkun**, ef sending er til fyrir pöntunina og magnið á núverandi sölupöntunarlínu eða flutningspöntunarlínu er minnkað eftir að álag hefur þegar verið búið til fyrir sölupöntunina er magnið á tilheyrandi álagslínu uppfært til að passa, nema magn á þeirri álagslínu sé þegar samsvarandi eða minna en nýja magnið á pöntunarlínunni. Í því tilfelli hefur álagslínan ekki áhrif. Ef álaginu var sleppt, en engin vinna búin til, er magnið á tengdri álagslínu uppfært til að passa, nema magnið á álagslínunni sé þegar samsvarandi eða sé minna en nýja magnið á pöntunarlínunni. Í því tilfelli verður álagslínan fyrir áhrifum.
- **Fjarlægja pöntunarlínu** - Þegar reiturinn **Uppfæra sendingar sjálfvirkt** er stilltur á **Alltaf** eða **Á magnlækkun**, ef notandi reynir að fjarlægja pöntunarlínu sem álagslína er til fyrir, birtast villuboð.

## <a name="example-scenario"></a>Dæmi

Fyrir þessa atburðarás verður þú að hafa kynningargögn sett upp og þú verður að nota kynningarfyrirtækið **USMF**.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Kveiktu á sjálfvirkri uppfærslu sendingar

Til að kveikja á sjálfvirkri uppfærslu sendingar skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
2. Veldu vöruhús **24**.
3. Á flýtiflipanum **Vöruhús** í reitnum **Uppfæra sendingu sjálfvirkt** skaltu breyta gildinu úr **Á magnlækkun** í **Alltaf**.

Eftir að þú breytir gildi í **Alltaf** endurspeglast allar hækkanir eða lækkanir á magni á sölupöntunarlínum og flutningspöntunarlínum, og viðbót við nýjar línur, í sendingum og álagi fyrir valið vöruhús, miðað við áður nefndar uppfærsluhömlur.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Breyttu bylgjusniðmátinu þannig að álagslínur séu ekki unnar sjálfkrafa

Fylgdu þessum skrefum til að stilla bylgjusniðmátið þannig að það vinni ekki sjálfkrafa álagslínur.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
2. Veldu bylgjusniðmátið **24 sendingarsjálfgildi**.
3. Veljið **Breyta**.
4. Á flýtiflipanum **Almennt** skaltu stilla valkostinn **Gera stofnun bylgju sjálfvirka** á **Já** og ganga úr skugga um að allir aðrir valkostir séu stilltir á **Nei**.

Það er mikilvægt að engin vinna verði sjálfkrafa búin til og gefin út sem hluti af bylgjusköpunarferlinu. Eftir að vinna er búin til sem tengist álagslínunni sem var búin til fyrir sölupöntunarlínuna er álagslínan ekki lengur sjálfkrafa uppfærð ef magni á sölupöntunarlínunni er breytt.

### <a name="create-a-sales-order"></a>Stofna sölupöntun

Til að stofna sölupöntun, skal fylgja eftirfarandi skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
2. Veldu viðskiptavin **US-003**.
3. Stofnaðu línu fyrir vörunúmer **A0001**.
4. Færðu inn magnið **10**. (Gakktu úr skugga um að þú notir vöruhús **24**.)
5. Veljið **Vista**.
6. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**. Sending og bylgja eru stofnaðar.

Vegna þess að þú breyttir bylgju sniðmátinu í fyrra ferlinu, er ekkert álag eða vinna búin til. Sendingarstaðan er **Opið**, og staða bylgju er **Stofnað**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Lækkaðu magnið í línu sölupöntunar

Fylgdu þessum skrefum til að minnka magnið í sölupöntunarlínu.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
2. Veldu sölupöntunina sem þú varst að losa í vöruhúsið.
3. Veldu sölupöntunarlínuna. Í reitnum **Magn** skaltu breyta gildinu úr **10** í **8**.
4. Veldu af sölupöntunarlínunni **Vöruhús \> Upplýsingar um sendingu**. Á síðunni **Upplýsingar um sendingu**, á flýtiflipanum **Álagslínur**, endurspeglar magnið breytinguna á sölupöntunarlínunni.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Auktu magnið í línu sölupöntunar

Fylgdu þessum skrefum til að auka magnið í sölupöntunarlínu.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
2. Veldu sölupöntunina sem þú losaðir áður í vöruhúsið.
3. Breyttu línumagninu úr **8** í **12**.
4. Veljið **Vista**.
5. Farðu til baka á síðuna **Allar sölupantanir** og veldu sölupöntunina aftur.
5. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Tengdar upplýsingar** skaltu velja **Upplýsingar um sendingu**. Á síðunni **Upplýsingar um sendingu**, á flýtiflipanum **Álagslínur**, endurspeglar magnið breytinguna á sölupöntunarlínunni.

Þrátt fyrir að magnið á álagslínunni hafi verið aukið úr 8 í 12 eru aðeins átta hlutir fráteknir nema kveikt sé á sjálfvirkri frátekningu. Vegna þess að magnið sem var bætt við núverandi sendingu hefur ekki verið frátekið, ef bylgjan er unnin á þessum tímapunkti, án frátekningar, er vinna aðeins búin til fyrir það magn sem þegar hefur verið frátekið.

> [!NOTE]
> Þegar magn á pöntunarlínu er minnkað hefur ekki áhrif á magn álagslínunnar ef það er þegar samsvarandi eða er minna en nýja magnið á pöntunarlínunni. Þegar magn á pöntunarlínu er aukið er álagslínan aukin um sama magn og pöntunarlínan. Ef magnið á pöntunarlínunni er frábrugðið magninu á álagslínunni helst mismunurinn áfram.

### <a name="add-a-sales-order-line"></a>Bæta við sölupöntunarlínu

Fylgið eftirfarandi skrefum til að bæta við sölupöntunarlínu.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
2. Veldu sölupöntunina sem þú losaðir áður í vöruhúsið.
3. Stofnaðu línu fyrir vörunúmer **A0002**.
4. Í **Magn** reitinn er fært inn **10**. (Gakktu úr skugga um að þú notir vöruhús **24**.) Nýju línunni er sjálfkrafa bætt við núverandi sendingu.
5. Veljið **Vista**.
6. Farðu til baka á síðuna **Allar sölupantanir** og veldu sölupöntunina aftur.
7. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Tengdar upplýsingar** skaltu velja **Upplýsingar um sendingu**. Á síðunni **Upplýsingar um sendingu**, á flýtiflipanum **Álagslínur**, skaltu taka eftir annarri álagslínunni.

Vegna þess að sölupöntunarlínan sem þú varst að bæta við núverandi sendingu hefur ekki verið frátekin, ef bylgjan er unnin á þessum tímapunkti er vinna aðeins búin til fyrir magnið á fyrstu sölupöntunarlínunni og fyrstu álagslínunni.

### <a name="process-a-wave"></a>Vinnsla bylgju

Til að vinna úr bylgjunni skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
2. Veldu bylgjuna sem búinn var til áður.
3. Í Aðgerðasvæði, á flipanum **Bylgja** í hópnum **Bylgja** skal velja **Ferli**.

Bylgjan er unnin og býr til vinnu fyrir frátekið magn á álagslínunum. Sendingarstaðan er uppfærð úr **Opið** í **Bylgjað**. Þegar staða sendingar er uppfærð í **Bylgjað** hafa engar breytingar sem eiga sér stað, svo sem lækkun eða aukning á línumagni eða viðbót nýrra lína við sölupöntunina, áhrif á núverandi álagslínur sem tengjast bylgjaðri sendingu.

Ef sending hefur stöðuna **Bylgjað** eða hærra endurspeglast uppfærslur á magni á sölupöntunarlínu ekki í eða eru staðfestar gegn álagslínu sem er tengd sendingunni. Breytingar á magni á álagslínu verða að vera gerðar beint á álagslínuna.

Fullgilding er gerð eftir að vinna hefur verið gerð fyrir álagslínuna og gerð frátekning. Lækkun á magni á sölupöntunarlínunni er síðan sannprófuð gegn frátekningu á vinnulínu.

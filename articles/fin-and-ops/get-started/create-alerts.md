---
title: "Viðvörunarreglur stofnaðar"
description: "Þetta efnisatriði veitir upplýsingar um viðvaranir og útskýrir hvernig á að búa til viðvörunarreglu svo þú fáir tilkynningu um tilvik eins og dagsetningu sem kemur eða tilgreinda breytingu sem á sér stað."
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 78e1e6f7be04e1d4fecae080cbd4a285358590fb
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="create-alert-rules"></a>Viðvörunarreglur stofnaðar

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Hafist handa

Áður en þú setur upp viðvörunarreglu skaltu ákveða hvenær eða í hvaða aðstæðum þú vilt fá viðvaranir. Þegar þú veist hvaða tilvik þú vilt fá tilkynningu um skaltu finna, í Microsoft Dynamics 365 for Finance and Operations, síðuna með gögnunum sem eru þess valdandi að tilvikið birtist. Atvikið getur verið dagsetning sem kemur eða tilteknar breytingar sem eiga sér stað. Þess vegna verður þú að finna síðuna þar sem dagsetningin er tilgreind eða hvar reiturinn er sem breytist eða hvar nýja færslan birtist sem er búin til. Eftir að þú hefur þessar upplýsingar er hægt að búa til viðvörunarregluna.

Þegar þú býrð til viðvörunarreglu skilgreinirðu skilyrðin sem þarf að uppfylla áður en kveikt er á viðvörun. Þú getur hugsað um skilyrði sem samsvörun milli tilviks sem á sér stað og uppfyllingu á tilgreindum skilyrðum. Þegar tilvik á sér stað byrjar kerfið að framkvæma eftirlit samkvæmt skilyrðum sem sett eru upp í Finance and Operations.

## <a name="events"></a>Tilvik

Tilvikið sem kveikir á viðvörunarreglu getur verið dagsetning sem kemur eða tiltekin breyting sem á sér stað. Kveikjur fyrir tilvik eru skilgreindar á flýtiflipanum **Láta mig vita þegar** í svarglugganum **Búa til viðvörunarreglu**. Tilvikin sem eru tiltæk fyrir tiltekinn reit fer eftir kveikjunni sem er valin.

Til dæmis, ef þú ert að setja upp viðvörunarreglu fyrir reitinn **Upphafsdagur** eru tilvik lokadags við hæfi. Þess vegna er gerð tilviksins **er komin á tíma eftir** í boði fyrir þann reit. Hins vegar, fyrir reit eins og **Kostnaðarstaður** er lokadagur tilviks ekki viðeigandi. Þess vegna er gerð tilviksins **er komin á tíma eftir** ekki í boði. Þess í stað er gerð tilviksins **hefur breyst** í boði.

## <a name="event-types"></a>Gerð tilvika

Þrjár gerðir af tilvikum geta komið fram:

- **Tilvik af gerðinni búa til og eyða** - Þessi tilvik kveikja á viðvörun þegar færsla er búin til eða henni eytt.
- **Tilvik af gerðinni uppfærsla** - Þessi tilvik kveikja á viðvörun þegar gögn í tilteknum reit breytast.
- **Tilvik af gerðinni lokadagur** - Þessi tilvik kveikja á viðvörun þegar dagsetning kemur.
    
Breytingar sem eiga sér stað geta byrjað af notanda. Til dæmis breytir notandi afhendingardegi á innkaupapöntun. Að öðrum kosti geta breytingar komið fram sem hluti af ferli. Til dæmis breytist reiturinn **Staða** á síðu til að endurspegla líftíma mismunandi ferla í kerfinu.

## <a name="conditions"></a>Skilyrði

Á flýtiflipanum **Láta mig vita um** í svarglugganum **Búa til viðvörunarreglu** er hægt að nota skilyrði til að stjórna því þegar þú færð viðvörðun um tilvik.

Til dæmis getur þú tilgreint að kerfið eigi að láta þig vita þegar staða innkaupapantana breytist, en aðeins ef staðan passar við tiltekið safn skilyrða. Þú vilt sérstklega fá viðvörun þegar staða innkaupapöntunar er stillt á **Móttekin**. Þessi breyting á stöðu er tilvikið sem kallar fram viðvörunina.

Næst verður þú að ákveða hvaða innkaupapantanir þú vilt fá viðvaranir um. Til dæmis getur þú valið einn af eftirtöldum valkostum. Þessir valkostir skilgreina skilyrðin á viðvörunarreglunni.

- **Núverandi valin færsla** - Þú færð viðvörun þegar staða tiltekinnar innkaupapöntunar breytist í **Móttekin**.
- **Allar færslur** - Þú færð viðvörun þegar staða innkaupapöntunar breytist fyrir vöru á virka síðuyfirlitinu. Þú getur notað ítarlegu síuna sem er tiltæk á síðunni til að búa til reglur fyrir tiltekið safn af færslum. Til dæmis getur þú búið til viðvörun sem kviknar á fyrir allar innkaupapantanir fyrir viðskiptavini í tilteknum viðskiptavinaflokki.
    
## <a name="expiry-of-rule"></a>Fyrning reglu

Á flýtiflipanum **Láta mig vita þangað til** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hversu lengi viðvörunarreglan á að vera virk.

## <a name="alert-contents"></a>Efni viðvörunar

Á flýtiflipanum **Láta mig vita með** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina efnistexta og textaskilaboð sem viðvörunarskilaboðin eiga að nota.

## <a name="user-id"></a>Kenni notanda

Á flýtiflipanum **Láta mig vita með** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hvaða notandi eigi að fá viðvörunarskilaboðin. Að sjálfgefnu er notandakenni þitt valið. Þessi valkostur er takmarkaður við stjórnendur fyrirtækis.

## <a name="create-an-alert-rule"></a>Búa til viðvörunarreglu

1. Opnaðu síðuna sem inniheldur gögnin sem á að fylgjast með.
2. Á aðgerðasvæðinu, á flipanum **Valkostir**, í flokknum **Deila** skal velja **Búa til viðvörunarreglu**.
3. Í svarglugganum **Búa til viðvörunarreglu**, í reitnum **Reitur** skal velja reitinn sem á að fylgjast með.
4. Í reitnum **Tilvik** skal velja gerð tilviks.
5. Á flýtiflipanum **Láta mig vita af** skal velja valkost.
6. Ef viðvörunarreglan verður óvirk á tilteknum degi skaltu velja lokadag á flýtiflipanum **Láta mig vita þangað til**.
7. Á flýtiflipanum **Láta mig vita með**, í reitnum **Efni** skal samþykkja sjálfgefna fyrirsögn efnis fyrir tölvupóstinn eða færa inn nýtt efni. Textinn er notaður í efnislínu fyrirsagnarfyrir tölvupóst sem berst þegar viðvörun er gefin.
8. Í reitnum **Skilaboð** skal færa inn valfrjáls skilaboð. Textinn er notaður sem skilaboðin sem er tekið á móti þegar viðvörun er ræst.
9. Veldu **Í lagi** til að vista stillingarnar og búa til viðvörunarregluna.


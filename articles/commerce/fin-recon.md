---
title: Fjárhagsafstemming í smásöluverslunum
description: Þetta efnisatriði útskýrir fjárhagsafstemmingu í smásöluverslunum fyrir sölustaði fyrir Microsoft Dynamics 365 Commerce.
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 99c238ecfbb6cb29f4fefefdca32525b99a01dc8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251332"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Fjárhagsafstemming í smásöluverslunum

[!include [banner](includes/banner.md)]

Í Microsoft Dynamics 365 Commerce, útgáfu 10.0.10 og nýrri, gerir virknin, sem biðlari sölustaðar býður upp á fyrir ferli í lok dags í smásöluverslunum, afgreiðslufólki og verslunarstjórum kleift að framkvæma lokaaðgerðir dagsins. Til dæmis getur það framkvæmt talningu skiptimyntar, lokað vakt blindandi, afstemmt færslur vaktar og lokað vöktum. Hins vegar er enginn möguleiki í sölustað til að ljúka fjárhagsupplýsingum fyrir vaktir, svo hægt sé að nota þær til að bóka fjárhaginn í Commerce Headquarters. Venjulega er það á herðum verslunarstjóra að ljúka þessu verki. Áður en þeir geta stimplað sig út af vakt, verða þeir að yfirfara upplýsingarnar, gera leiðréttingar ef þess gerist þörf og ljúka samtölum fyrir þá vakt. Lokasamtölurnar á síðan að bóka í fjárhagseiningum í Commerce Headquarters.

Að auki, í Commerce útgáfu 10.0.10 og nýrri, geta verslunarstjórar yfirfarið og gert leiðréttingar á uppgjörslínum í Commerce Headquarters. Möguleikinn er hinsvegar takmarkaður og verslunarstjórar hafa sjaldan aðgang að biðlara Commerce Headquarters. Þar að auki er aðeins hægt að framkvæma yfirferð og leiðréttingu fjárhagsuppgjörs smásölu þegar uppgjörin eru búin til í Commerce Headquarters. Þetta ferli gerist hinsvegar oftast að næturlagi. Þar af leiðandi verða verslunarstjórar að bíða eftir útskráningu af vakt þegar fjárhagsuppgjör smásölu er búið til í Commerce Headquarters.

Í útgáfu 10.0.11 og nýrri af Commerce geta verslunarstjórar yfirfarið, leiðrétt og lokið vöktunum sínum í biðlara sölustaðar upp á eigin spýtur. Þessi gögn eru síðan notuð til að búa til og bóka fjárhagsuppgjör smásölu í Commerce Headquarters.

> [!NOTE]
> Virknin sem tengist fjárhagsafstemmingu í smásöluverslunum virkar aðeins ef kveikt er á stofnferli pöntunar sem byggir á hlutastraumi. Frekari upplýsingar er að finna í [Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Uppsetning fjárhagsafstemmingar

Fylgið eftirfarandi skrefum til að nota virkni fjárhagsafstemmingar.

1. Á vinnusvæðinu **Eiginleikastjórnun**, skal kveikja á eiginleikanum **Smásöluuppgjör - hlutastraumur**.
1. Í virknireglu sölustaðar fyrir viðeigandi verslun, skal stilla valkostinn **Virkja fjárhagslega afstemmingu í verslun** á **Já**.

## <a name="more-information-about-financial-reconciliation"></a>Frekari upplýsingar um fjárhagsafstemmingu

Þegar kveikt er á virkni fjárhagsafstemmingar eru einhverjar færibreyturnar sem eru skilgreindar í flýtiflipanum **Uppgjör/lokun** á síðunni **Smásöluverslanir** í Commerce Headquarters samstilltar við gagnagrunnsrásina. Sama safni af útreikningsskilyrðum og mörkum upphæðar sem er notað fyrir smásöluuppgjör er framfylgt.

Þegar aðgerðin **Loka vakt** er sett af stað staðfestir kerfið að upphæðir reiknaðar af kerfinu og uppgefnar upphæðir passi. Ef það er munur, og mismunurinn fer yfir skilgreind mörk, er notandinn látinn vita og getur hann gert nauðsynlegar leiðréttingar.

Hægt er að gera leiðréttingar fyrir hvern greiðslumáta. Þegar greiðslumáti er valinn getur notandinn skoðað samtölur fyrir mismunandi færslugerðir og breytt samtölunum fyrir tiltekna færslugerð. Við breytingar sýnir kerfið upprunalega útreiknaða upphæð og hnekkta upphæð fyrir þá færslugerð. Notandinn getur einnig geymt athugasemdir sem hluti af breytingarferlinu. Athugasemdirnar er hægt að nota fyrir endurskoðun.

Notendur geta hunsað kvaðningar og skilaboð um staðfestingu og haldið áfram og lokað vaktinni. Hins vegar, ef notandi hunsar kvaðningar um staðfestingu, koma sömu vandamálin upp og verður að laga þegar vaktin bókar fjárhagsuppgjörin í Commerce Headquarters.

Aðgerðin **Loka vakt** á sölustað staðfestir einnig að allar færslur í ótengdum gagnagrunni eru samstilltar við gagnagrunnsrásina. Ef einhverjar færslur eru ekki samstilltar fær notandinn viðvörunarboð vegna þess að þessar aðstæður geta valdið því að upphæðir kerfisins verði reiknaðar á rangan hátt. Í slíkum tilfellum getur notandinn lokið aðgerðinni **Loka vakt** og reynt að samstilla ótengdar færslurnar við gagnagrunnsrásina. Að öðrum kosti getur notandinn leiðrétt handvirkt upphæðir sem kerfið reiknar út til að gera grein fyrir færslunum sem eru ekki samstillar, þannig að lokið sé við rétt safn af fjármálatölum og það bókað. 

Þegar uppgjörsbókun hlutastraums er notuð, þannig að bókun á færslum er aðskilin frá bókun á fjárhag, er hægt að velja um að leiðrétta upphæðir reiknaðar af kerfinu fyrir ótengdar færslurnar sem vantar upp á. Á þennan hátt er tryggt að gert sé grein fyrir fjárhagsstöðunni og hún bókuð rétt, óháð færslunum sem vantar. Hægt er að samstilla ótengdar færslur við gagnagrunnsrásina og Commerce Headquarters og síðan bóka seinna, aðskilið frá fjárhagsbókunum.

Upplýsingar um fjárhagsafstemmingu fyrir vakt eru samstilltar við Commerce Headquarters með því að nota P-verk.

Fjárhagsuppgjör smásölu í Commerce Headquarters reikna ekki út samtölur til að sýna upplýsingar í uppgjörslínunum. Þess í stað eru lokaupphæðir í biðlara sölustaðar notaðar til að búa til og bóka fjárhagsuppgjör smásölu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
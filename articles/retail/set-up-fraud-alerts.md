---
title: "Setja upp viðvaranir vegna svika"
description: "Í þessu efnisatriði er útskýrt hvernig á að setja upp reglur viðvörun viðskiptavinar þjónustu biðlaraþjónustu hugsanlega sviksamleg upplýsinga þegar pantanir eru unnar. Hægt er að skilgreina ákveðna kóða sem nota á til að sjálfvirkt eða handvirkt setja grunsamlegar pantanir í bið."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Uppsetning svikaviðvarana

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp skilyrði og reglur til að setja sviksamlegar sölupantanir í bið þar til frekari skoðun hefur farið fram. Skoðunarvirkni tengd svikum er notuð til að ákvarða réttmæti upplýsinga í sölupöntun. Ef upplýsingar í sölupöntun virðist vafasamar miðað við svik viðmiðanir og reglur stofnunarinnar, er hægt að setja pöntunina í bið til að fá frekari skoðun hjá stjórnanda.

> [!NOTE]
> Þennan eiginleiki er eingöngu hægt að nota með úrvinnslu sölupöntunar á rás símavers smásölu. 

Þegar rás símavers er skilgreind verður að stilla **Virkja lok pöntunar** á **Já**. Þegar lok pöntunar eru virkjuð getur notendur skoðað samantekt pöntunar og smellt á **Senda inn** til að ljúka pöntuninni. Notendur munu einnig fá valkosti til að setja sölupantanir sem eru í svikaskoðun handvirkt í bið. Sölupantanir sem notandi lætur vita af gegnum símaver eru settar í ferli tengt reglum og skilyrðum svika á meðan innsendingarúrvinnslunni stendur.

Það eru tvær tegundir af svikaskilyrðum sem kerfið muni vísa til þegar athugað er hvort pöntun ætti að vera haldið eftir og hún sett í svikaskoðun:

-   **Fastar reglur** nota tiltekið gildi, eins og símanúmer sem hefur verið sett á svartan lista eða netfang sem hefur verið flaggað vegna sviksamlegra færslna í fortíðinni. Á síðunni **Föst sviksamleg gögn** er hægt að bæta við upplýsingum um svik handvirkt eða með því að flytja inn gögn þar sem stig eru meðfylgjandi sviksamlegum upplýsingum. Ef kveikt er á svikakönnun, mun sérhver sölupöntun sem færð er inn borin saman við föstu gögnin. Ef gögnin finnast í annaðhvort innheimtu- eða afhendingaraðsetur viðskiptavinarins eða ef gögnin eru að finna í afhendingaraðsetri á sölulínunni verða stig allra einstakrar samsvörunar lögð saman.  
-   **Gagnvirkar reglur** er búnar til úr breytum og skilyrðum sem eru skilgreind fyrir þessar breytur. Með gagnvirkum reglum er hægt að athuga önnur skilyrði sem ekki eru skilgreind í kyrrstæðum reglum. Hægt er að nota flóknari „OG/EÐA“ yfirlýsingar til skoða margskonar aðstæður til að ákvarða hvort jákvæð samsvörun sé á milli regluskilyrða og sölupöntunar sem lögð er fram. Til dæmis, ef notandi vill halda eftir og setja í svikaskoðun pantanir fyrir viðskiptavini sem eru bundnir við tiltekið viðskiptavina hópvirði og sem pöntuðu ákveðna vöru, yrðu skilyrði fyrir að staðfesta viðskiptavin og staðfesta vörur skilgreind á síðunni **Reglur** með „OG“ skilyrði. Röðin myndi falla í bið vegna svika aðeins ef báðir skilyrðin voru sönn og ef stigagildi sem er úthlutað til reglunnar setti heildar svikastigafjölda pöntunarinnar yfir lágmarks svikastigafjölda eins og skilgreint er í færibreytum Símavers.

Notandi símavers getur einnig handvirkt lagt pöntun inn í biðröð pantana sem eru í bið vegna svika. Ef notandinn sem færir inn pöntunina telur að viðskiptavinurinn sem leggur pöntunina gæti verið grunsamlegur og vill að einhver annar fari yfir pöntunarstaðfestinguna áður en hún er unnin, þá getur notandinn sem færir inn pöntunina valið **Handvirkt í bið vegna svika** valmöguleikann í fellivalmyndinni **Í bið** á síðunni **Samantekt sölupantana** (þetta birtist eftir að **Ljúka** pöntun virknin er kölluð fram). Notandinn verður hvattur til að færa inn athugasemd til að útskýra frekar hvers vegna þeir telja að pöntunin sé sviksamleg svo að sá sem fer yfir málið hafi meira samhengi.

Allar pantanir sem haldið er eftir í gegnum handvirkt í bið vegna svika eða með kerfisbundinni útreikningi á svikastigafjölda munu birtast á **Pantanir í bið** síðunni, þar sem pöntunin er hægt að endurskoða og síðan annaðhvort hætt við eða sleppt til vinnslu.

> [!NOTE]
> Notkun margra reglna eða of flókinna reglna mun leiða til slæmrar frammistöðu kerfis þegar sölupantanir eru send inn. Svik viðvörun eiginleikinn hefur ekki verið fínstilltur til að geta afgreitt mikið magn fastra svikagagnafærslna og margar virkar reglur. Mikilvægt er að hafa í huga að sérhver regla er metin meðan á innsendingarvirkni sölupöntunarfærslna í símaver stendur. Reglurnar eru metnar í samræmi við sölupöntunarhausinn og allar pöntunarlínur. Því fleiri reglur og því flóknari sem regluyfirlýsingarnar eru, því lengri tíma tekur úrvinnslan. Ef þú ert með fjölda línuatriða í pöntun þinni, fjölda virkra reglna og fastgagnafærslur, getur þetta kerfisbundna ferli við að endurskoða og staðfesta öll gögnin og reikna svikatölur haft veruleg áhrif á afköst.  Stofnanir sem nota þessa eiginleika ættu alltaf að prófa og staðfesta að vinnslutími innsendingar á pöntun sé viðunandi áður en reglubreytingar eða föst svikaskilyrði eru sett í notkun í framleiðsluumhverfinu.


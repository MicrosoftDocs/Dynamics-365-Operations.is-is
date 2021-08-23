---
title: Setja upp og vinna með viðvaranir vegna svika fyrir símaver
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp reglur viðvörun viðskiptavinar þjónustu biðlaraþjónustu hugsanlega sviksamleg upplýsinga þegar pantanir eru unnar. Þú getur skilgreint tiltekna kóða sem eru notaðir til að sjálfkrafa eða handvirkt setja grunsamlegar pantanir í bið.
author: josaw1
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e692d43b8c2648a424ff3b4fdc9d0cf16d0e03702d6a237f71caaf49646c5ec3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763669"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Setja upp og vinna með viðvaranir vegna svika fyrir símaver

[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að setja upp viðmiðanir og reglur til að setja hugsanlega sviksamlega sölupantanir í bið til frekari endurskoðunar. Eiginleikinn fyrir svikaathugun er notuð til að ákvarða réttmæti upplýsinganna í sölupöntun. Ef upplýsingar í sölupöntun virðist vafasamar, miðað við svik viðmiðanir og reglur stofnunarinnar, er hægt að setja pöntunina í bið til frekari endurskoðunar. Í þessu tilfelli er ekki hægt að gefa út pöntunina í vörugeymsluna til frekari vinnslu fyrr en biðin hefur verið hreinsað.

> [!NOTE]
> Þessi eiginleiki er aðeins hægt að nota með sölupöntunarvinnslu fyrir Commerce-rás símavers.

## <a name="turning-on-the-fraud-check-feature"></a>Kveikja á eiginleika fyrir svikaathugun

Til að nota eiginleika fyrir svikaathugun verður þú að stilla **Virkja lok pöntunar** valmöguleikann á rásinni á **Já** þegar símaversrásin er [skilgreind](/dynamics365/unified-operations/retail/set-up-order-processing-options). Þegar kveikt er á lokum pöntunar, verða notendur símavers að velja **Ljúka** á sölupöntunarsíðunni fyrir allar sölupantanir sem eru búnar til. Ljúka aðgerðin veldur því að **Sölupöntunarsamantekt** síðan opnast. Eftir að notendur hafa slegið inn nauðsynleg greiðslugögn á **Sölupöntunarsamantekt** síðunni skal velja **Senda inn** til að ljúka pöntuninni. Þegar pöntunin er send inn er kveikt á svikaathuguninni og allir reglur sem eru virkir í kerfinu eru sjálfkrafa sannprófaðar.

Notendur símavers geta einnig handvirkt sett sölupantanir í bið til að gera svikakönnun áður en þeir velja **Senda inn**. Til að setja sölupöntun handvirkt í bið, á **Sölupöntunarsamantekt** síðunni skaltu velja **Í bið** \> **Handvirk bið vegna svika**. Þú ert þá beðinn um að slá inn athugasemd til að útskýra ástæður þínar fyrir að setja pöntunina í bið. Þessi athugasemd munu birtast í [Pantanir í bið](/dynamics365/unified-operations/retail/work-with-order-holds) vinnusvæði til að veita samhengi við notandann sem skoðar pantanir sem eru í bið til að ákvarða hvort pöntunin skuli losuð.

Til viðbótar við að grunnstilla **Virkja lok pöntunar** valkost á rásinni, verður þú að grunnstilla eiginleika svikaathugunar í færibreytur símavers. Farið í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning símavers** \> **Færibreytur símavers**. Á **Færibreytur símavers** síðunni, á **Biðstöður** flipanum, stilltu **Svikaathugun** valkosturinn á **Já**.

Á **Biðstöður** flipanum ættir þú einnig að skilgreina þá [Biðkóðar](/dynamics365/unified-operations/retail/work-with-order-holds) sem verður beitt í pöntun sem er annaðhvort handvirkt eða sjálfkrafa sett í bið til svikaathugunar. Stilltu biðkóðana í **Handvirk bið sökum svika** og **Biðkóði sökum svika** reitina. Þú gætir þótt gagnlegt að búa til tvo einstaka biðkóða, þannig að notendur sem vinna í vinnusvæði fyrir bið geta auðveldlega afmarkað og greint sjálfvirka bið frá handvirkri bið.

Til að eiginleikinn fyrir svikaathugun sé skilvirkur, verður þú einnig að stilla **Lágmarksfjöldi stiga** reitinn. Sérhver svikaviðmiðun og regla sem er skilgreind í kerfinu hefur ákveðinn fjölda stiga. Þegar sölupöntun er skoðuð fyrir sviksamsvörun, ef ein eða fleiri samsvörun finnast, eru stigin bætt saman til að gefa pöntunina heildarfjölda svikastiga. Ef heildarfjöldi svikastiga fyrir pöntun fer yfir gildi **Lágmarksfjöldi stiga** reitsins er pöntunin sjálfkrafa sett í bið. Þú getur valið aðra stigatengda reiti á **Biðstöður** flipanum til að skilgreina tölvupóstsskorið, símaskorið, póstnúmeraskorið og útvíkkað póstnúmeraskorið. Ef þú tilgreinir ekki skor fyrir neina af þessum föstu svikaviðmiðum þegar þú skilgreina þær á **Föst svikaviðmið** síðunni mun kerfið ákvarða skorin með því að nota sjálfgefið skor sem þú tilgreinir á **Biðtímar** flipanum á **Færibreytur símavers** síðunni.

Að lokum skaltu nota **Gerð athugasemdar svik** reitinn til að tilgreina þá tegund skjals sem ætti að nota þegar notendur slá inn athugasemdir þegar þeir setja pöntun handvirkt í bið fyrir svik endurskoðun. Oftast er þetta reit sett á **Athugasemd**.

## <a name="defining-fraud-criteria-and-rules"></a>Skilgreina svikaviðmið og reglur

Kerfið vísar til tvær tegundir af svikaviðmiðum til að ákvarða hvort pöntun verði sett í bið fyrir svik endurskoðun:

- **Föst svikagögn** nota tiltekið gildi, eins og símanúmer sem hefur verið sett á svartan lista eða netfang sem hefur verið flaggað vegna sviksamlegra færslna í fortíðinni. Til að setja upp föst svikagögn, farðu í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning símavers** \> **Svik** \> **Föst svikagögn**. Á **Föst svikagögn** síðunni er hægt að bæta svikaviðmiðum handvirkt eða með gagnainnflutningi. Skor er fest við sviksamlegar upplýsingar. Ef kveikt er á eiginleika fyrir svikaathugun, mun sérhver sölupöntun sem færð er inn borin saman við föstu gögnin. Ef gögnin er að finna í annaðhvort greiðsluaðsetri viðskiptavinarins eða afhendingaraðsetri sem er tengt við pöntunarhausinn eða ef gögnin finnast á afhendingaraðsetri sem tengjast einhverjum af línum sölupöntunarinnar, er skor fyrir einstæða samsvörun bætt saman og borinn saman við **Lágmarksfjöldi stiga** gildi til að ákvarða hvort pöntunin ætti að vera í bið.

- **Svikareglur** samanstanda af notendaskilgreindum breytur og skilyrðum sem eru skilgreind fyrir þessar breytur. Til að búa til reglur skaltu fara í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning símavers** \> **Svik** \> **Reglur**. Svikareglur leyfa fyrirtækinu að grunnstilla flóknara regluverk sem getur innihaldið **OG** eða **EÐA** staðhæfingar til að meta margvíslegar skilyrði. Til dæmis vill notandi allar pantanir fyrir viðskiptavini sem tilheyra tilteknum hópi viðskiptavina og sem pantaði tiltekna vöru til að setja í bið fyrir svikaleit. Í þessu tilviki, skilyrði til að sannprófa viðskiptavininn og vörur eru skilgreindar á **Reglur** síðu, og OG ástand er notað. Röð er því aðeins sett í bið ef báðir aðstæður eru sönn og ef gildi skors sem er úthlutað til þessa reglu, auk gildi skors annarra reglna sem pöntunin samsvarar, veldur því að heildarfjöldi svikastiga pöntunarinnar fer yfir **Lágmarksfjöldi stiga** gildið sem er skilgreint á **Færibreytur símavea** síðu.

> [!NOTE]
> Mörg reglur eða of flóknar reglur munu hafa áhrif á afköst kerfisins þegar sölupantanir eru sendar inn. Eiginleikinn fyrir svikaathugun hefur ekki verið fínstilltur til að geta afgreitt mikið magn fastra svikagagnafærslna og margar virkar reglur. Mundu að hver regla er metin þegar notendur símavers velja **Senda inn** á meðan sölupöntunarfærslu stendur. Reglurnar eru metnar í samræmi við sölupöntunarhausinn og allar pöntunarlínur. Því fleiri reglur sem eru til staðar og því flóknari sem regluyfirlýsingarnar eru, því lengri tíma tekur úrvinnslan. Ef fjöldi línuatriða eru í pöntun, og fjöldi virkra reglna og fastgagnafærslur, getur þetta sjálfvirka ferli við að endurskoða og staðfesta öll gögnin og reikna svikatölur haft veruleg áhrif á afköst. Stofnanir sem nota þessa eiginleika ættu alltaf að prófa og staðfesta að vinnslutími fyrir innsendingu á pöntun er ásættanlegt áður en þær virkja nokkrar breytingar á reglur eða föst svikaviðmið í framleiðslu umhverfið.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Bera kennsl á pantanir sem eru í bið vegna svikakönnunar

Þegar notendur símavers senda inn sölupöntun, ef pöntunin passar við svikaviðmiðanir eða reglur, og ef skorið fer yfir lágmarkið fá notendur viðvörunarboð sem kveða á um að pöntunin hafi verið sett í bið. Notendur geta lokað þessum skilaboðum vegna þess að þær eru aðeins til upplýsinga. Notendur geta mögulega miðlað þessum upplýsingum til viðskiptavina. Fyrirtækið ætti að ákvarða samskiptareglur sem notendur fylgja við þessar aðstæður.

Pöntunin er vistuð, en **Ekki setja í ferli** flaggið er stillt á hana. Þetta flagg hjálpar til við að tryggja að pöntunin verði ekki sleppt í vörugeymsluna. Hvenær sem er, geta notendur skoðað stillinguna fyrir **Ekki setja í ferli** flaggið fyrir hvaða sölupöntun sem er á **Ítarleg staða** síðunni. Þessi síða er hægt að opna frá **Allar sölupantanir** og **Notendaþjónusta** síður. Kerfið uppfærir einnig gildi **Ítarleg staða** reitinn fyrir pöntunina til **Í bið sökum svika**.

Til að skoða og stjórna pöntununum sem eru í bið fyrir svikakönnun skaltu fara í **Retail og Commerce** \> **Viðskiptavinir** \> **Pantanir í bið**. Á síðunni **Pantanir í bið** skal velja færslu í listanum og smella svo á **Pöntun í bið** til að sjá frekari upplýsingar sem innihalda ástæðuupplýsingar. Á flipanum **Upplýsingar um svik** er hægt að skoða kerfisbundin svikaviðmið sem fundust fyrir pöntunina og stigin sem voru notuð. Ef pöntunin var sett í bið handvirkt er hægt að skoða allar athugasemdir sem notandinn sem setti pöntunina í bið sló inn með því að skoða **Athugasemdir um svik** hlutann í flýtiflipanum **Athugasemdir**.

Frekari upplýsingar um hvernig á að vinna með pantanir í bið er að finna í [Pantanir í bið](/dynamics365/unified-operations/retail/work-with-order-holds).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Breyta bókhalds- eða skýrslugjaldmiðli
description: Þetta efnisatriði útskýrir hvernig á að breyta bókhalds- eða skýrslugjaldmiðli eða bæta skýrslugjaldmiðli við fjárhagsuppsetningu.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1fd641d4f60d8ff9710c89f43777f7fd8f378dbc6c73d773ac103f9d9f68e60e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770594"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Breyta bókhalds- eða skýrslugjaldmiðli

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að breyta bókhalds- eða skýrslugjaldmiðli eða bæta skýrslugjaldmiðli við fjárhagsuppsetningu.

## <a name="symptom"></a>Einkenni

Þú vilt breyta bókhalds- eða skýrslugjaldmiðli eða bæta skýrslugjaldmiðli við fjárhagsuppsetningu. Þetta á sér yfirleitt stað við eftirfarandi aðstæður:

- Rangur bókhalds- eða skýrslugjaldmiðill var tilgreindur þegar lögaðili var settur upp. Nú viltu breyta þeim gjaldmiðli.
- Skýrslugjaldmiðill var tilgreindur þegar lögaðili var settur upp en fyrirtækið vilja nú fjarlægja skýrslugjaldmiðilinn.
- Fyrirtækið er að uppfæra eða flytja sig yfir í Microsoft Dynamics 365 Finance og vill breyta bókhalds- eða skýrslugjaldmiðlinum.

Samtök sem notuðu ekki áður möguleikann á tvöföldum gjaldmiðli vill byrja að nota hann. Þetta vandamál á sér yfirleitt stað við eftirfarandi aðstæður.

- Enginn skýrslugjaldmiðill var tilgreindur þegar lögaðili var settur upp. (Skýrslugjaldmiðill er valfrjáls.) Þú vilt nú bæta við skýrslugjaldmiðli.

## <a name="resolution"></a>Lausn

Mikilvægast er að hafa í huga hvort einhverjar færslur (raunverulegar eða fjárhagslegar) hafi verið bókaðar í lögaðilanum fyrir fjárhagsuppsetninguna. **Ekki er hægt að skipta um bókhalds- eða skýrslugjaldmiðil, eða bæta við skýrslugjaldmiðli, ef einhverjar færslur (raunverulegar eða fjárhagslegar) hafa verið bókaðar í lögaðilanum.** Fylgdu skrefunum í einum af eftirtöldum köflum, eftir því hvort færslur hafa verið bókaðar.

### <a name="no-transactions-have-been-posted"></a>Engar færslur hafa verið bókaðar

1. Í lögaðilanum sem þú ert að uppfæra gjaldmiðla fyrir skaltu fara í **Fjárhagur \> Fjárhagsuppsetning \> Fjárhagur**.
2. Á síðunni **Fjárhagur** skaltu velja **Breyta**.
3. Á flýtiflipanum **Gjaldmiðill** skal velja bókhaldsgjaldmiðil og skýrslugjaldmiðil sem á að nota fyrir lögaðilann.
4. Veldu **Vista**.

Ef reitirnir fyrir bókhaldsgjaldmiðilinn og skýrslugjaldmiðilinn eru ekki tiltækir á síðunni **Fjárhagur** hefur ein færsla eða fleiri (raunverulegar eða fjárhagslegar) verið bókaðar í lögaðilanum. Því er ekki hægt að breyta gjaldmiðlunum. Í þessu tilviki skaltu fylgja skrefunum í næsta kafla.

### <a name="transactions-have-been-posted"></a>Færslur hafa verið bókaðar

**Ef færslur hafa verið bókaðar í lögaðila er eina leiðin til að breyta eða bæta við bókhalds- og skýrslugjaldmiðlum að stofna nýjan lögaðila með rétta gjaldmiðla.** Til að auðvelda þetta ferli leyfir gagnastjórnun kerfisins þér að afrita uppsetningarskrár og aðalskrár úr núverandi lögaðila til nýs lögaðila.

Breytingar á bókhalds- og skýrslugjaldmiðlum taka gildi alls staðar. Þær hafa ekki aðeins áhrif á Fjárhag heldur einnig allar undirbækur (viðskiptakröfur, viðskiptaskuldir, birgðir, verk o.s.frv.), allar lausnir óháðra hugbúnaðarsala og allar viðbætur sem þú hefur gert sem geyma fjárhæðir.

Villur geta hæglega komið upp í ferlinu sem finnur og umreiknar hverja einustu fjárhæð í annan gjaldmiðil. Því mun hönnunarteymið ekki samþykkja forskrift sem breytir eða bætir við bókhalds- og skýrslugjaldmiðlum. Auk þess, þótt verkfæri sem áður var í boði í Microsoft Dynamics AX 2012 leyfði þér að breyta eða bæta við bókhalds- og skýrslugjaldmiðlum, var notkun þess hætt í bæði AX 2012 R3 og Finance.

Fylgdu þessum skrefum til að afrita uppsetningu og aðalgögn úr núverandi lögaðila í nýjan lögaðila.

1. Opnaðu **Vinnusvæði \> Gagnastjórnun**.
2. Veldu **Sniðmát** undir flokknum **Innflutningur/útflutningur**.
3. Gakktu úr skugga um að sniðmát séu tiltæk. Ef engin sniðmát eru í boði skaltu velja **Hlaða sjálfgefnum sniðmátum** og hinkra á meðan sniðmátin eru búin til.
4. Farðu aftur á vinnusvæðið **Gagnastjórnun**.
5. Veldu **Afrita yfir í lögaðila**.
6. Færðu inn heiti og lýsingu flokksins.
7. Í reitnum **Upprunalögaðili** skaltu velja lögaðilann sem afrita á gögn úr.
8. Í flýtiflipanum **Marklögaðilar** skaltu velja **Stofna lögaðila** til að stofna nýjan lögaðila sem þú getur afritað gögn upprunalögaðilans í. Veldu **Velja fyrirliggjandi** til að afrita gögn í lögaðila sem er til staðar.
9. Valfrjálst: Stilltu reitinn **Afrita númeraraðir** á **Já**. (Mælt er með þessu skrefi þegar gögnin eru afrituð.)
10. Í **Valdar einingar** svæðinu skaltu velja **Bæta við sniðmáti**.
11. Velja sniðmátin sem á að nota. Tillögur að sniðmátum fyrir nýjan lögaðila eru m.a. **025 - Fjárhagur** og **Fjármál**. Við ráðleggjum þér að fara yfir öll hin sniðmátin sem eru í boði til að finna út hvort einhver þeirra uppfylli kröfur þínar.
12. Veldu **Afrita í lögaðila** til að hefja runuvinnslu sem býr til valdar einingar og afritar þær í marklögaðilann.
13. Eftir að ferlinu er lokið, en áður en færslur eru bókaðar, skaltu fara í fjárhaginn og uppfæra bókhalds- og skýrslugjaldmiðla eins og lýst var fyrr í þessu efnisatriði.

Ef þú stofnaðir nýjan lögaðila svo þú getir breytt bókhalds- eða skýrslugjaldmiðli skaltu ganga úr skugga um að upphafsstöðurnar séu umreiknaðar úr gjaldmiðlum gamla lögaðilans og yfir í nýju gjaldmiðlana.

Í [Afrita yfir í lögaðila](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017) má finna myndskeið sem sýnir fyrri skref.

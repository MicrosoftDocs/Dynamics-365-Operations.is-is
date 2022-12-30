---
title: Eftirspurnarstýrð áætlanagerð
description: Greinin lýsir því hvernig á að búa til áætlaðar pantanir fyrir vörur sem eru settar upp sem aftengingarpunktar.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740303"
---
# <a name="demand-driven-planning"></a>Eftirspurnarstýrð áætlanagerð

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Greinin lýsir því hvernig á að búa til áætlaðar pantanir fyrir vörur sem eru settar upp sem aftengingarpunktar.

## <a name="net-flow-and-qualified-demand"></a>Nettóflæði og hæf eftirspurn

Meðan á aðalskipulagi stendur beitir kerfið hugtakinu *nettóflæði* til að ákvarða virkt magn í lagerbirgðum byggt á raunverulegum lagerbirgðum, auk birgða sem eru í pöntun (fyrirliggjandi birgðapantanir sem hafa ekki enn borist), að frádregnu því sem nefnt er *viðurkennd eftirspurn* (viðurkennd sala á næstunni), eins og sýnt er á eftirfarandi mynd. Þegar kerfið er að ákveða hvaða öryggisbirgðasvæði vara tilheyrir og hvað pantað magn á að vera mun það meta nettóflæði, ekki raunverulegar lagerbirgðir.

![Dæmi um nettóflæðirit.](media/ddmrp-net-flow-example.png "Dæmi um nettóflæðirit")

Þegar áætluð pöntun er ræst í áætlunarkeyrslu verður pantað magn hámarksstaða mínus nettóflæði. Til að úthluta forgangsröðun notar kerfið virknina [forgangsröðuð áætlanagerð](priority-based-planning.md) í staðinn fyrir þarfadagsetningar. DDMRP (Demant Driven Material Requirements Planning) úthlutar forgangi áætlaðrar pöntunar miðað við pantað magn sem hlutfall af hámarksbirgðum. Á fyrri myndinni er pantað magn 53 prósent af hámarksmagninu. Því verður forgangsröðin fyrir áfyllingu 53. (Í þessu samhengi er 0 í hæsta forgangi, og 100 í lægsta forgangi.)

*Viðurkennd eftirspurn* er fyrri eftirspurn, auk eftirspurnar dagsins í dag, og hæf mörk aukningar í framtíðinni. Eftirfarandi mynd sýnir dæmi um eftirspurnarstig fyrir daginn í dag (12. júní) og næstu þrjá daga. DDMRP gerir þér kleift að setja mörk fyrir aukningu til að greina eftirspurn sem er umfram venjulegar væntingar. Ef þröskuldurinn er stilltur á 25 stykki uppfylla tvær af þeim dagsetningum sem sýndar eru á myndinni skilyrði um aukningu marka. Þú verður að úthluta þröskuldi fyrir mörk aukningar fyrir hverja vöru fyrir sig með því að nota síðuna **Vöruþekja** eins og lýst er í [Setja upp öryggisbirgðir fyrir vöru aftengingarpunkts](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Dæmi um nothæft eftirspurnarreiknirit](media/ddmrp-net-qualified-demand-example.png "Dæmi um nothæft eftirspurnarreiknirit")

Að því gefnu að eftirspurnin sé ekki til staðar getur þú bætt eftirspurninni í dag (18) við mörk aukninganna tveggja (29 og 26) til að fá hæfilega eftirspurn upp á 73. Jafnvel þó að eftirspurn sé fyrir 23. júní skaltu taka eftir því að hún er ekki tekin með í nettóflæðisútreikninginn vegna þess að DDMRP kemur skipulagðri röðun af stað á annan hátt en hefðbundnir þekjuhópar fyrir áætlun.

## <a name="generating-planned-orders-with-ddmrp"></a>Bý til áætlaðar pantanir með DDMRP

Meðan á áætlanakeyrslu stendur mun kerfið búa til nýja áætlaða pöntun ef nettóflæði fyrir hlut fer niður fyrir endurpöntunarmarkið. Þegar DDMRP er notað verður yfirleitt gerð áætlunarkeyrsla á hverju degi. Þess vegna ertu aðallega að athuga birgðastig þitt einu sinni á dag til að ákvarða hvaða hluti þarf að fylla á.

Eftirfarandi mynd sýnir dæmi um aðstæður þar sem þú ert með pöntun fyrir 18 stykkjum 20. júní, 29 stykki 21. júní, 26 stykki 22.júní og 20 stykki 23. júní. Vegna þess að mörk aukningar eru stillt á 25 stykki er tveimur þessara fyrirmæla flaggað sem mörkum. Það eru 220 stykki af þessari vöru í birgðum.

![Áætlanadæmi 1.](media/ddmrp-planning-example-1.png "Áætlanadæmi 1")

Ef þú keyrir aðalskipulagið núna mun það búa til áætlaða röð ef nettóflæðið reynist fara niður fyrir endurpöntunarmarkið (219 stykki í þessu dæmi).

![Áætlanadæmi 2.](media/ddmrp-planning-example-2.png "Áætlanadæmi 2")

Þetta dæmi býr til áætlaða innkaupapöntun fyrir magn upp á 130, sem jafngildir hámarksstöðu mínus nettóflæði. Áætlaðri pöntun er úthlutað forgangi upp á 53,07, byggt á prósentuhlutfalli hennar af hámarksmagninu. Þar sem þessi gildi fundust 20. júní býr kerfið til skipulagða pöntun sem er dagsett 20. júní auk aftengda afhendingartímans fyrir vöruna (fimm virkir dagar í þessu dæmi). Vegna þess að fimm virkir dagar eru ein vika frá deginum í dag er fyrirhuguð pöntun dagsett 27. júní.

> [!NOTE]
> Aðalskipulag reiknar aðeins aftengda hluti með því að nota DDMRP. Öll önnur atriði eru reiknuð með því að nota staðlaða efnisþarfaáætlanir (MRP).

---
title: Árslokalokun
description: Þetta efnisatriði lýsir áskilinni uppsetningu og skrefum til að keyra lokun árslokaferlis fjárhags.
author: kweekley
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdb81df1701851330b0501c03e41eb10e639bc77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842321"
---
# <a name="year-end-close"></a>Árslokalokun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir áskilinni uppsetningu og skrefum til að keyra lokun árslokaferlis fjárhags. 

Við lok fjárhagsársins, þarf að keyra árslokalokun til að flytja opnunarstöður á nýtt ár. Flest fyrirtæki keyrir loka árslokaferlið mörgum sinnum. Fyrsta skiptið væri að sækja stöður sem eru færðar inn í nýtt fjárhagsár. Síðan er hægt að keyra árslokaferlið aftur, sem oft er nauðsynlegt til að flytja stöður úr leiðréttingarfærslum í nýja fjárhagsárið. 

Við árslokaferlið er hægt að stofna tvær gerðir færslna. Opnunarfærsla er alltaf mynduð og er notuð til að stofna opnunarstöður á nýtt fjárhagsár. Opnunarfærslan sýnir stöður fjárhagslykils í efnahagsreikningi á nýju fjárhagsári og stöðu úr lykilsstöðum rekstrarlykla í fjárhagslykli óráðstafaðs eigin fjár á nýju fjárhagsári. Valfrjálst er að stofna lokunarfærslu til að færa stöðu í rekstrarlyklum niður núll í fjárhagsárinu sem verið er að loka.

## <a name="prepare-to-run-the-year-end-close"></a>Undirbúa keyrslu á árslokalokun
Áður en árslokalokunarferlið er keyrt skal staðfesta stillingar fyrir eftirfarandi: 

Á síðunni **Aðallykill**:

-   Sannprófa að **Aðallykilgerð** hefur verið skilgreind rétt fyrir hvern aðallykil. Aðallykilgerðin er notuð til að ákvarða hvort stöðu aðallykils verður að vera tekin áfram sem opnunarstaða eða lokaða óráðstafað eigið fé inn á Opnunarfærslu.
-   Svæðið **Opnunarlykillinn** má nota til að flytja stöðu aðallykils í nýjan aðallykil við árslokalokun. Nýi aðallykillinn er færður inn í svæðinu **Opnunarlykill**. Vanalega verður þetta notað fyrir aðallykla efnahagsreikninga þegar aðallykill er óvirkur og nýr aðallykill er notaður fyrir nýtt fjárhagsár.

Á síðunni **fjárhagsfæribreytur** undir **Lok fjárhagsárs**:

-   Valkosturinn **Eyða árslokafærslum** er notaður til að tilgreina hvort eyða eigi kerfismyndaðri opnunarfærslu úr fyrri árslokalokun þegar árslokalokun er keyrð á ný. Ef þessi valkostur er stilltur á **Já** er fyrri opnunarfærslu eytt og ný opnunarfærsla stofnuð á grundvelli gildandi staða. Ef þessi valkostur er stilltur á **Nei** helst fyrri opnunarfærsla og viðbótar opnunarfærsla er stofnuð til að flytja stöður áfram úr leiðréttingarfærslum sem bókaðar eru eftir að fyrri árslokalokun.
-   Valkosturinn **Stofna lokunarfærslur við flutning** er notaður til að stofna lokunarfærslur í fjárhagsárinu sem verið er að loka til að færa stöðu í rekstrarlykla í núll. Ef þessi valkostur er stilltur á **Já** eru bæði opnunarfærsla og Lokunarfærsla stofnuð. Ef þessi valkostur er stilltur á **Nei** er aðeins opnunarfærsla stofnuð í næsta fjárhagsári til að flytja stöður. Rekstrarstöður verða eftir við lok fjárhagsársins.
-   Valkosturinn **Stilla stöðu fjárhagsárs lokað varanlega** er notaður til að stilla fjárhagsár á varanlega lokaða stöðu. Nota skal þessa stillingu varlega, því öll tímabil með varanlega lokaðri stöðu er ekki hægt að enduropna, sem kemur í veg fyrir að leiðréttingar séu bókaðar á fjárhagsár. Bestu starfsvenjur eru að stilla þetta á **Nei**.
-   Valkosturinn **Tiltaka þarf fylgiskjalsnúmer** er notaður til að skilgreina hvort númer fylgiskjals er krafist þegar árslokalokun er keyrð. Bestu starfsvenjur eru að krefjast númers fylgiskjals til að auðvelt sé að finna Opnunarfærslu.

Á síðunni **fjárhagsdagatöl**:

-   Næsta fjárhagsár verður að vera til áður en árslokalokun eru keyrð. Næsta fjárhagsárs er krafist til að stofna upphafsstöður í opnunartímabili.

Á síðunni **Dagbækur fjárhags**:

-   Valfrjálst: Hvert fjárhagstímabil fyrir fjárhagsárið lokað má stilla á **Í bið** til að koma í veg fyrir að nýjar færslur séu færðar inn. Þegar leiðréttingarfærslur eru auðkenndar er hægt að enduropna biðtímabilin til að bóka leiðréttingarfærslur, jafnvel þó að árslokalokunarferlið hafi þegar verið keyrt.

## <a name="define-year-end-close-templates"></a>Skilgreina sniðmát árslokalokunar
Eftir að kerfið hefur verið skilgreint er hægt að keyra árslokalokunarferlið. Á síðunni **Árslokalokun** er hægt að skilgreina sniðmát fyrir hóp lögaðila sem á að keyra árslokalokun fyrir. Sniðmátið verður endurnýtt við hverja árslokalokun, en er hægt að breyta ef fyrirtækið breytist. 

Fyrst skal skilgreina **Flokksheiti** fyrir sniðmátið og velja fjárhagsdagatalið. Heiti flokksins ætti að auðkenna hóp með lögaðila.  Til dæmis er hægt að setja upp sniðmátin samkvæmt landafræði, með sérstaka flokka stofnaða fyrir lögaðila í Norður-Ameríku, EMEA lögaðila og APAC lögaðila. 

Næst er hægt að bæta lögaðila við sniðmátið. Hægt er að bæta lögaðilum við með því að velja annaðhvort lögaðila eða með því að velja stigveldi fyrirtækis. Ef stigveldi fyrirtækisins er valið verður aðeins lögaðilum innan stigveldis sem nota valið fjárhagsdagatal bætt við sniðmátið. Ef lögaðilar eru notaðir til að bæta við sniðmát er aðeins hægt að bæta við lögaðilum með sama fjárhagsdagatal. Sama fjárhagsdagatals er krafist vegna þess að árslokalokun er keyrð með því að velja fjárhagsár, sem geta verið breytileg frá einu dagatali til annars. 

Þegar lögaðila hefur verið bætt við skal aðallykla skilgreina óráðstafaðs eigin fjár fyrir hvern lögaðila. Svæðið **Dagsetning síðastu árslokalokunar** verður að vera uppfært í hvert sinn sem árslokalokun er keyrð fyrir lögaðila. 

Flipinn **Fjárhagsvídd** er notaður til að skilgreina hvaða fjárhagslegar víddir verða notaðar í Opnunarfærslu. Athugið stillingarnar sem verið er að skilgreina eiga aðeins við lögaðila sem var valinn í hnitanetinu **Lögaðila**. Endurtaka verður uppsetningu fyrir hvern lögaðila í hnitanetinu. 

**Flytja víddir efnahagsreikningur** er notuð til að skilgreina hvort fjárhagsvíddir í færslur bókaðar á efnahagslykla ætti að viðhalda á Opnunarfærslu. Bestu starfsvenjur eru að stilla þennan valkost á **Já**. **Flytja víddir rekstur** er notað til að skilgreina hvaða fjárhagsvíddir á færslunum sem bókaðar eru sem rekstrarreikningur verða fluttar í aðallykilinn óráðstafað eigið fé. Fyrst þarf að auðkenna fjárhagsvíddir sem eiga við valinn lögaðila. Þetta myndi fela í sér allar fjárhagsvíddir sem voru bókaðar á móti árinu, jafnvel þótt fjárhagsvíddin sé ekki hluti af virku lykilskipulagi. Næst skal skilgreina hverja vídd sem annaðhvort **Loka einni** eða **Loka öllum**.  Sjálfgildi er **Loka öllum**, sem viðheldur upphaflegum fjárhagsvíddagildum úr bókuðum færslum og notar þau fyrir stofnun á opnunarstöðum fyrir tekjulykil. Aðskildar upphafsstöður óráðstafaðs eigin fjár verða stofnaðar fyrir hverja einkvæma samsetningu fjárhagsvíddargilda. Ef **Loka einni** er valinn eru allar færslur sem eru bókaðar með þeirri fjárhagsvídd dregnar saman í upphafsstöðu óráðstafaðs eigin fjár fyrir upphafsstöðu víddargildisins færðar inn í svæði eftir **Loka einni**. Til dæmis, látum sem allar færslur fyrir fjárhagsár hafi verið bókaðar með lykilskipulagi aðallykils - Deild. Í fjárhagsvíddinni Deild í sniðmátinu er valið **Loka einni** og 100 er fært inn sem gildi. Ef heildartekjur af öllum færslum sem bókaðar eru á deildir 200, 300 og 400 er $100.000 verður ein opnunarstaða stofnuð fyrir Óráðstafað eigið fé - 100. Ef þú velur **Loka einni** og hefur gildi fjárhagsvídda autt verða allar færslur bókaðar í óráðstafað eigið fé með það víddargildi autt. 

Ferli árslokalokunar fylgja ekki lykilskipulagi. Þetta er vegna þess að lykilskipulag getur breyst á meðan fjárhagsári stendur og ekki er alltaf hægt að auðkenna viðkomandi lykilskipulag vegna þessara breytinga.  Þegar opnunarfærslur eru stofnaðar verða stöður teknar fram með fjárhagsvíddir eins og skilgreindar í sniðmáti árslokalokunar. Upphafsstöðufærslur gætu innihaldið fjárhagsvíddir sem eru ekki lengur í gildandi lykilskipulagi og hlutasamsetningar sem eru ekki lengur gild í núgildandi lykilskipulagi. Ef fyrirtækið vill útiloka fjárhagsvídd fyrir upphafsstöðu varðveitts tekjukóða skal stilla fjárhagsvídd á **Loka einni** og hafa víddargildin auð.

## <a name="run-the-year-end-close-process"></a>Keyra árslokalokunarferlið
Eftir að sniðmát árslokalokunar eru stofnuð, er ferli árslokalokunar ræst með því að velja **Keyra fjárhagslokun** í Aðgerðarúðunni. Veldu annaðhvort allt eða hlutmengi lögaðila úr sniðmátinu sem á að keyra árslokalokunina úr. Þegar árslokalokun er keyrð í fyrsta skipti á fjárhagsári muntu líklega velja alla lögaðila til að stofna upphafsstöður fyrir alla lögaðila. Ef árslokalokun er keyrð aftur má velja að keyra vinnslu fyrir aðeins þá lögaðila sem leiðréttingarfærslur voru bókaðar fyrir. 

Veldu fjárhagsár sem keyra á ferli árslokalokunar gegn. Ef fleiri en eitt lokunartímabil er til á síðasta tímabili fjárhagsársins, verður svæðið **Heiti tímabils** tiltækt svo að hægt sé að velja á hvaða lokunartímabil á að bóka lokunarfærsluna ef uppsetning er skilgreind til að stofna Lokunarfærslu. 

Færið inn númer fylgiskjals, sem kann að vera áskilið eða ekki, allt eftir uppsetningu í færibreytum fjárhags. Nota verður sama fylgiskjalsnúmer fyrir alla lögaðila sem voru valdir fyrir ferli árslokalokunar. Númeraröð er ekki notuð til að mynda þetta fylgiskjalsnúmer. Bestu starfsvenjur eru að færa inn fylgiskjalsnúmer, jafnvel þótt að það sé ekki áskilið. Færa inn fylgiskjalsnúmer gerir auðveldara að finna færsluna Opnunarstöður á nýju fjárhagsári. Ef ekki er fært inn númer fylgiskjals verður fylgiskjalið autt fyrir Opnunarfærslu. 

Ef óskað er að bakfæra fyrri árslokalokun fyrir valið fjárhagsár, skal stilla **Afturkalla fyrri lokun** á **Já**. Árslokalokun verður bakfærð en hægt er að endurkeyra ferlið hvenær sem er. Ef árslokalokun er bakfærð verður **Dagsetning síðustu árslokalokunar** ekki tiltæk. 

Ferlið Árslokalokunin er sjálfgefið keyrt í runuham. Bestu starfsvenjur eru að keyra ferlið í runustillingu til að leyfa notanda að fara aftur í aðrar aðgerðir. Þegar ferli árslokalokunar er lokið verður **Dagsetning síðustu árslokalokunar** uppfært með dagsetningu lotu.

Fyrir nánari upplýsingar, sjá [Loka fjárhag í lok tímabils](close-general-ledger-at-period-end.md) og [Loka reikningsárinu](tasks/close-fiscal-year.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
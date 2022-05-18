---
title: Árslokalokun
description: Þetta efnisatriði lýsir áskilinni uppsetningu og skrefum til að keyra lokun árslokaferlis fjárhags.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 247c3286124da946937c8afd248a275e5a745044
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725234"
---
# <a name="year-end-close"></a>Árslokalokun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir áskilinni uppsetningu og skrefum til að keyra lokun árslokaferlis fjárhags.

Við lok fjárhagsársins, þarf að keyra árslokalokun til að flytja opnunarstöður á nýtt ár. Flest fyrirtæki keyrir loka árslokaferlið mörgum sinnum. Fyrsta keyrslan færir stöðurnar inn á nýja fjárhagsárið. Hægt er síðan að endurkeyra ferlið eins oft og þörf krefur flytja stöður úr leiðréttingarfærslum inn á nýja fjárhagsárið.

Við árslokaferlið er hægt að stofna tvær gerðir færslna. Opnunarfærsla er alltaf mynduð og er notuð til að stofna opnunarstöður á nýtt fjárhagsár. Opnunarfærslan sýnir stöður fjárhagslykils í efnahagsreikningi á nýju fjárhagsári og stöðu úr lykilsstöðum rekstrarlykla í fjárhagslykli óráðstafaðs eigin fjár á nýju fjárhagsári. Valfrjálst er að stofna lokunarfærslu til að færa stöðu í rekstrarlyklum niður núll í fjárhagsárinu sem verið er að loka.

## <a name="prepare-to-run-the-year-end-close"></a>Undirbúa keyrslu á árslokalokun

Áður en árslokalokunarferlið er keyrt skal staðfesta stillingar fyrir eftirfarandi:

Á síðunni **Aðallykill**:

- Sannprófaðu að reiturinn **Aðallyklagerð** sé rétt stilltur fyrir hvern aðallykil. Aðallyklagerðin sker úr um hvort staða aðallykils verður að vera tekin áfram sem opnunarstaða eða lokuð inn í óráðstafað eigið fé í opnunarfærslunni.
- Staðan á aðallyklinum getur verið flutt á nýjan aðallykil í árslokalokuninni. Færðu inn nýja aðallykilinn í reitinn **Opnunarlykill**. Vanalega er þessi reitur notaður fyrir aðallykla efnahagsreikninga þegar aðallykill er óvirkur og nýr aðallykill er notaður fyrir nýtt fjárhagsár.

Á síðunni **fjárhagsfæribreytur** undir **Lok fjárhagsárs**:

- Valkosturinn **Eyða fyrirliggjandi árslokafærslum þegar ári er lokað aftur** er notaður til að tilgreina hvort eyða eigi kerfismyndaðri opnunarfærslu úr fyrri árslokalokun þegar árslokalokun er keyrð á ný. Ef þessi valkostur er stilltur á **Já** er fyrri opnunarfærslu og valfrjálsri lokunarfærslu eytt og ný opnunar- eða lokunarfærsla er stofnuð á grundvelli gildandi staða. Ef þessi valkostur er stilltur á **Nei** helst fyrri opnunarfærsla og valfrjáls lokunarfærsla, og viðbótar opnunar- eða lokunarfærsla er stofnuð til að flytja stöðurnar áfram úr leiðréttingarfærslum sem bókaðar eru eftir fyrri árslokalokun.
- The **Búðu til lokafærslur meðan á flutningi stendur** valkostur er notaður til að búa til lokafærslur á því reikningsári sem verið er að loka, til að færa innstæður allra aðalreikninga í 0 (núll). Ef þessi valkostur er stilltur á **Já** eru bæði opnunarfærsla og lokunarfærsla stofnaðar. Ef þessi valkostur er stilltur á **Nei** er aðeins opnunarfærsla stofnuð á næsta fjárhagsári til að flytja stöðurnar. Innstæður aðalreikninga standa eftir í lok reikningsárs.
- Valkosturinn **Stilla stöðu fjárhagsárs lokað varanlega** er notaður til að stilla fjárhagsár á varanlega lokaða stöðu. Notaðu þennan valkost vandlega vegna þess að ekki er hægt að enduropna tímabil sem eru með varanlega lokaða stöðu. Þar af leiðandi er ekki hægt að bóka leiðréttingar á fjárhagsárið. Best er að stilla þennan valkost á **Nei**.
- Valkosturinn **Fylla verður út fylgiskjalsnúmer** hefur verið fjarlægður. Nú er krafist fylgiskjals þegar ferli árslokalokunar er keyrt. Þá er fylgiskjalsnúmerið slegið inn handvirkt.

Á síðunni **fjárhagsdagatöl**:

- Næsta fjárhagsár verður að vera til áður en árslokalokun er keyrð. Annars er ekki hægt að stofna upphafsstöður á opnunartímabilinu.

Á síðunni **Dagbækur fjárhags**:

- Valfrjálst: Hvert fjárhagstímabil fyrir fjárhagsárið sem verið er að loka má stilla á **Í bið** til að koma í veg fyrir að nýjar færslur séu færðar inn. Þegar leiðréttingarfærslur eru auðkenndar er hægt að enduropna biðtímabilin svo að hægt sé að bóka leiðréttingarfærslur, jafnvel þó að árslokalokunarferlið hafi þegar verið keyrt.

Á síðunni **Uppsetning sniðmáts árslokalokunar**:

- Þegar kveikt er á eiginleikanum **Endurbætur á árslokum fjárhags** er ferlið við að setja upp sniðmát árslokalokunar aðskilið frá ferlinu við að keyra árslokalokunina. Hægt er að skilgreina sniðmátið á síðunni **Uppsetning sniðmáts árslokalokunar** (**Fjárhagur \> Fjárhagsuppsetning \> Uppsetning sniðmáts árslokalokunar**) eða hægt er að opna það í ferli árslokalokunar.

## <a name="define-year-end-close-templates"></a>Skilgreina sniðmát árslokalokunar

Eftir að kerfið hefur verið skilgreint er hægt að keyra árslokalokunarferlið. Á síðunni **Uppsetning sniðmáts árslokalokunar** er hægt að skilgreina sniðmát fyrir hóp lögaðila sem á að keyra ferli árslokalokunar fyrir. Sniðmátið verður endurnýtt við hverja árslokalokun, en er hægt að breyta ef fyrirtækið breytist.

Fyrst skal stilla reitinn **Flokksheiti** fyrir sniðmátið og velja fjárhagsdagatalið. Heiti flokksins ætti að auðkenna hóp lögaðila sem er meðtalinn. Þegar þú ákveður hópa lögaðila skaltu hafa í huga að lögaðilar geta aðeins verið með í sama hópi ef sama fjárhagsdagatalið er valið fyrir þá. Til dæmis er hægt að setja upp sniðmátin samkvæmt landfræðilegri staðsetningu og aðskilda hópa er hægt að búa til fyrir lögaðila í Norður-Ameríku, lögaðila í Evrópu, Mið-Austurlönd og Afríku (EMEA) og lögaðila Asíu og Eyjaálfu (APAC).

Næst er hægt að bæta lögaðila við sniðmátið. Hægt er að bæta lögaðilum við með því að velja annaðhvort lögaðila eða með því að velja stigveldi fyrirtækis. Ef stigveldi fyrirtækisins er valið verður aðeins lögaðilum innan stigveldis sem nota valið fjárhagsdagatal bætt við sniðmátið. Ef lögaðilar eru notaðir til að bæta við sniðmát er aðeins hægt að bæta við lögaðilum með sama fjárhagsdagatal. Sama fjárhagsdagatals er krafist vegna þess að árslokalokun er keyrð með því að velja fjárhagsár, sem geta verið breytileg frá einu dagatali til annars.

Þegar lögaðila hefur verið bætt við skal aðallykla skilgreina óráðstafaðs eigin fjár fyrir hvern lögaðila.

Flipinn **Fjárhagsvídd** er notaður til að skilgreina hvaða fjárhagslegar víddir verða notaðar í opnunarfærslunni. Athugaðu að uppsetningin í þessum flipa á aðeins við um lögaðilann sem er valinn í hnitanetinu **Lögaðilar**. Endurtaka þarf uppsetninguna fyrir hvern lögaðila í hnitanetinu.

Valkosturinn **Flytja víddir efnahagsreiknings** er notaður til að tilgreina hvort halda eigi við fjárhagsvíddum í færslum sem eru bókaðar á efnahagsreikninga í opnunarfærslunni. Best er að stilla þennan valkost á **Já**. Stillingin fyrir víddir efnahagsreiknings hefur ekki áhrif á núverandi stöður í fjárhagslyklum óráðstafaðs eigið fé. Þessar stöður ákvarðast af þeim víddum hagnaðar og taps sem eru skilgreindar í næsta hluta. Til dæmis var fjárhagsárið 2019 fyrsta árið sem var lokað og valkosturinn **Loka öllu** var notaður til að velja víddirnar **Deild** og **Kostnaðarstaður** fyrir lokun. Í þessu tilviki var stofnaður sérstakur lykill fyrir óráðstafað eigið fé fyrir hverja samsetningu deildar og kostnaðarstaðar. Þegar árslokalokun er keyrð fyrir fjárhagsár 2020 helst óráðstafað eigið fé frá síðasta ári nákvæmlega eins og þegar það var bókað, jafnvel þótt **Flytja víddir efnahagsreiknings** er stillt á **Nei**. Stöður sem eru bókaðar á órástöfuðu eigin fé frá síðustu árslokalokunum er aldrei breytt.

Hlutinn **Flytja víddir hagnaðar og taps** er notaður til að tilgreina hvaða fjárhagsvíddir í færslunum sem bókaðar eru á rekstrarreikninga verða fluttar í aðallykil óráðstafaðs eigin fé. Fyrst þarf að auðkenna fjárhagsvíddir sem eiga við valinn lögaðila. Þessar fjárhagsvíddir fela í sér allar fjárhagsvíddir sem var bókað á móti á árinu, jafnvel þótt fjárhagsvíddin sé ekki hluti af virku lykilskipulagi. Næst skal skilgreina hverja vídd sem annaðhvort **Loka einni** eða **Loka öllum**. Sjálfgefni valkosturinn er **Loka öllu**. Þessi valkostur viðheldur upphaflegum fjárhagsvíddargildum úr bókuðum færslum og notar þær til að stofna opnunarstöður fyrir lykil óráðstafaðs eigin fjár. Aðskildar upphafsstöður óráðstafaðs eigin fjár verða stofnaðar fyrir hverja einkvæma samsetningu fjárhagsvíddargilda. Ef **Loka einni** er valinn eru allar bókaðar færslur sem eru með þá fjárhagsvídd dregnar saman í upphafsstöðu óráðstafaðs eigin fjár fyrir víddargildið sem er fært inn í reitinn sem birtist eftir **Loka einni**. Til dæmis voru allar færslur fyrir fjárhagsárið bókaðar með lykilskipulaginu **Aðallykill - Deild**. Fyrir fjárhagsvíddina **Deild** í sniðmátinu, er **Loka einni** valið og **100** er fært inn sem víddargildið. Ef heildartekjur af öllum færslum sem bókaðar eru í deildir 200, 300 og 400 er $100.000 verður ein opnunarstaða stofnuð fyrir **Óráðstafað eigið fé - 100**. Ef þú velur **Loka einni** en skilur gildi fjárhagsvíddar eftir autt verða allar færslur bókaðar í óráðstafað eigið fé og víddargildið verður autt.

## <a name="run-the-year-end-close-process"></a>Keyra árslokalokunarferlið

Eftir að sniðmát árslokalokunar eru stofnuð er hægt að ræsa ferli árslokalokunar á síðunni **Árslokalokun** (**Fjárhagur \> Tímabil lokunar \> Árslokalokun**). Áður en árslokalokun er keyrð er hægt að bæta við nýju sniðmáti árslokalokunar eða breyta fyrirliggjandi sniðmáti með því að velja **Uppsetning sniðmáts árslokalokunar** til að opna uppsetningarsíðuna fyrir sniðmátin.

Veldu sniðmát árslokalokunar og á aðgerðasvæðinu skal síðan velja **Keyra árslokalokun**. Veldu annaðhvort alla lögaðila eða undirsafn lögaðila úr sniðmátinu sem árslokalokunin er keyrð fyrir. Ef árslokalokun er keyrð í fyrsta skipti á fjárhagsári muntu líklega velja alla lögaðila til að stofna upphafsstöður fyrir þá alla. Ef þú hefur áður keyrt árslokalokun gætirðu viljað keyra hana aftur fyrir eingöngu lögaðilana sem leiðréttingarfærslur voru bókaðar fyrir.

Næst skal velja fjárhagsárið til að keyra ferli árslokalokunar fyrir. Ef fleiri en eitt lokunartímabil er til á síðasta tímabili fjárhagsársins verður reiturinn **Heiti tímabils** aðgengilegur. Síðan er hægt að velja lokunartímabilið sem á að nota til að bóka lokunarfærsluna ef uppsetningin er skilgreind til að stofna lokunarfærslu.

Því næst skal færa inn fylgiskjalsnúmer. Sama fylgiskjalsnúmerið verður notað fyrir alla lögaðilana sem þú hefur valið fyrir ferli árslokalokunar. Fylgiskjalsnúmerið er ekki búið til með því að nota númeraröð.

Ferli árslokalokunar keyrir sjálfgefið í runustillingu. Því er hægt að snúa sér að öðrum verkum eftir að það hefur verið sett af stað.

Ekki er alltaf hægt að auðkenna viðeigandi lykilskipulag vegna þess að það getur breyst á fjárhagsári. Ferli árslokalokunar fylgir þar af leiðandi ekki lykilskipulagi. Þegar opnunarfærslur eru stofnaðar verða stöður dregnar fram með fjárhagsvíddum eins og það er skilgreint í sniðmáti árslokalokunar. Upphafsstöðufærslur geta innihaldið fjárhagsvíddir sem eru ekki lengur í gildandi lykilskipulagi og hlutasamsetningar sem eru ekki lengur gildar í núgildandi lykilskipulagi. Ef fyrirtækið vill útiloka fjárhagsvídd fyrir upphafsstöðu óráðstafaðs eigin fjár skal stilla fjárhagsvíddina á **Loka einni** og skilja víddargildið eftir autt.

Eftir að ferlinu er lokið er útbúin færsla fyrir hverja samsetningu lögaðila og fjárhagsárs. Þú munt aðeins sjá færslur fyrir lögaðila sem þú hefur aðgang að. Hver færsla inniheldur dagsetningu og tíma kerfisins þegar ferlið var keyrt og beinan tengil á fylgiskjöl sem voru búin til fyrir árslokalokunina.

[![Skrár búnar til á flýtiflipa árslokalokunarferils á síðu árslokalokunar](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Ef þú endurkeyrir árslokalokun sérðu eina eða margar færslur fyrir hverja samsetningu af lögaðila og fjárhagsári eftir því hver stillingin er í valkostinum **Eyða fyrirliggjandi árslokafærslum þegar ári er lokað aftur** á síðunni **Færibreytur fjárhags**:

- Ef valkosturinn er stilltur á **Já** er fylgiskjali frá fyrri árslokalokun eytt. Færslan er merk **Frátekin** og stimpluð með dagsetningu og tíma þegar bakfærslan var gerð. Þar að auki er tengillinn á fylgiskjalsnúmerið fjarlægður. Þegar árslokalokuninni er lokið verður ný færsla stofnuð fyrir nýja fylgiskjalið sem er búið til.
- Ef valkosturinn er stilltur á **Nei** helst færslan fyrir fyrri árslokalokun áfram, ásamt tenglinum á fylgiskjalið. Í hvert sinn sem árslokalokunin er keyrð aftur verður ný færsla stofnuð ásamt tengli á nýju fylgiskjölin.

## <a name="reverse-the-year-end-close-process"></a>Bakfæra ferli árslokalokunar

Á síðunni **Árslokalokun** er hægt að bakfæra árslokalokun. Velja skal færslu fyrir samsetningu lögaðila og fjárhagsárs sem þarf að bakfæra og velja svo **Bakfæra árslokalokun**. Bakfærsluferlið eyðir öllum fylgiskjölum opnunar og lokunar sem voru búin til fyrir fjárhagsárið. Færslan er merk **Frátekin** og stimpluð með dagsetningu og tíma þegar bakfærslan var gerð. Þar að auki er tengillinn á fylgiskjalsnúmerið fjarlægður. Rétt eins og með ferli árslokalokunar keyrir bakfærslan í runustillingu.

Gátreiturinn **Sýna bakfært** sem er tiltækur fyrir ofan hnitanetið gerir þér kleift að fela eða sýna færslurnar fyrir bakfærsluferli árslokalokunar. Þegar búið er keyra ferlið **Bakfæra árslokalokun** gæti þurft að velja gátreitinn **Sýna bakfært** til að sjá færsluna. Hægt er að setja viðbótarsíur til að skoða aðrar upplýsingar.

[![Notkun gátreitsins „Sýna bakfært“ til að sjá færslur fyrir bakfærsluferli árslokalokunar á síðu árslokalokunar](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Fyrir nánari upplýsingar, sjá [Loka fjárhag í lok tímabils](close-general-ledger-at-period-end.md) og [Loka reikningsárinu](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Frestunarfærslur í „Áskriftargreiðslur“
description: Í þessari grein er lýst ýmsum færslum sem hægt er að nota í frestunarfærslum sem hluti af frestunum á tekjum og útgjöldum í áskriftargreiðslum.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c3862f1a250bf8e56303975b5c6a3560cd84c1e7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872587"
---
# <a name="deferral-default-transactions"></a>Sjálfgefnar frestunarfærslur

Þessi grein lýsir færslunum sem leyfa frestanir á tekjum og útgjöldum. Frestunaráætlanir byggja alltaf á og eru háðar upprunalegu skjali eða greiðsluáætlun. Frestunaráætlanir eru búnar til samkvæmt sjálfgefnum gildum og ekki er hægt að færa þær inn eða búa þær sérstaklega til.

## <a name="sales-order-transaction-deferral"></a>Frestun sölupöntunfærslu

Notaðu síðuna **Frestanir** eða **Stofna kreditnótu** til að færa inn eða breyta færibreytum frestana fyrir sölupöntunarlínu.

> [!NOTE]
> Þegar sölupöntun er stofnuð úr greiðsluáætlun eru öll gildi á síðunni **Frestanir** eða **Búa til kreditnótu** skrifvarin og ekki er hægt að breyta færibreytum frestunar. Nota skal síðuna **Breyta áætlun** til að breyta gildunum.

### <a name="edit-deferral-options"></a>Breyta valkostum frestunar

Til að breyta valkostum frestunar fyrir línu skal fylgja þessum skrefum.

1. Stofnið sölupöntunarfærslu.
2. Veljið línuna og síðan **Frestanir**.
3. Á síðunni **Frestunarfærsla** þarf að stilla valkostinn **Frestun** á **Já**. Breyta öðrum svæðum eftir þörfum.
4. Til að forskoða frestunaráætlunina skaltu velja **Forskoða**.
5. Ef gerðar voru breytingar á frestunarfærslu skal velja **Í lagi** og fara aftur á færslusíðuna.
6. Staðfestið og bókið færsluna.

Þegar færslan er bókuð skal opna síðuna **Allar frestunaráætlanir** til að skoða frestunaráætlun.

### <a name="create-a-credit-note"></a>Stofna kreditnótu

Til að stofna kreditnótu, skal fylgja eftirfarandi skrefum.

1. Stofnið sölupöntunarfærslu.
2. Í hlutanum **Sölupöntunarlínur** skal velja vöruna sem á að búa til kreditnótu fyrir.
3. Veldu **Sölupöntunarlína** \> **Ný** og veldu svo **Kreditnóta**.
4. Veljið **Frestanir**.
5. Á síðunni **Frestun sölupöntunfærslu** skal stilla valkostinn **Laga fyrirliggjandi áætlun** á **Já** fyrir vöruna.
6. Í reitnum **Breytt áætlun** skal velja frestunaráætlunina sem kreditnótan á að tilheyra.
7. Uppfærðu reitina **Endurreikna dagsetningu** og **Lokadagsetning** eftir þörfum.
8. Veldu **Í lagi**.
9. Kláraðu bókun sölupöntunarfærslunnar.

### <a name="purchase-orders-and-purchase-invoices"></a>Innkaupapantanir og innkaupareikningar

Ef nota á frestunaraðgerðina fyrir innkaupapöntun skal búa til reikninginn fyrst. Notaðu síðan síðuna **Reikningar frá lánardrottni í bið** til að breyta eða bæta við frestunarvörum. Ekki er hægt að breyta eða bæta við frestunum á innkaupapöntun.

1. Notaðu síðuna **Reikningar frá lánardrottni í bið** til að slá inn reikning lánardrottins.

    Þegar lína er færð inn er frestunin sjálfkrafa stillt fyrir vöruna eða innkaupategundina sem var valin. Þessi frestun byggir á uppsetningu frestunar á síðunni **Sjálfgefin gildi frestunar**. Hægt er að breyta eða bæta við frestunum á dreifingarstiginu.

3. Í innkaupalínunni skal velja **Fjármál \> Dreifa upphæðum**.
4. Fyrir hverja dreifingarupphæð skal velja **Frestanir**. Þegar reikningur er bókaður er búin til frestunaráætlun fyrir hverja dreifingu sem frestun er sett fyrir.

### <a name="tax"></a>Skattur

Í sumum tilvikum er hægt að endurgreiða skattupphæðina að fullu eða að hluta. Ef skattupphæð frestanlegrar línu inniheldur óendurgreiðanlega upphæð er óendurgreiðanleg skattupphæð tekin með í upphæð frestunaráætlunar þegar reikningurinn er bókaður.

### <a name="variance"></a>Frávik

Ef upphæðin í reikningslínu lánardrottins er frábrugðin upphæðinni í innkaupapöntunarlínunni eru fráviksdreifingar búnar til. Ef línunni er frestað er fjárhagslykillinn fyrir þessar dreifingar stilltur á frestunarlykil og upphæðirnar eru innifaldar í frestanlegri upphæð áætlunar þegar reikningurinn er bókaður. Þessar dreifingar kallast **Verðfrávik** og **Kostnaðarfrávik**.

### <a name="general-journals-and-invoice-journals"></a>Almennar færslubækur og reikningabækur

Notaðu síðuna **Frestanir** til að færa inn færibreytur frestunar fyrir línur færslubókarfylgiskjals. Einnig er hægt að forskoða frestunaráætlun fyrir línulegar frestanir. Þegar lína er færð inn er frestunin sjálfkrafa stillt samkvæmt uppsetningu frestunarlykla á síðunni **Sjálfgefin gildi frestunar**. Hægt er að breyta valkostum frestunar handvirkt fyrir hverja línu. Þegar færslubókarfylgiskjalið er bókað er frestunaráætlunin búin til.

#### <a name="post-and-transfer"></a>Bóka og flytja

Til að bóka færslubókarfylgiskjalið skal nota skipunina **Bóka og flytja**. Frestunarvalkostirnir fylgja línunni sem fylgiskjalið á við um. Fyrir fylgiskjöl með engum villum er frestunaráætlun búin til ef henni er frestað. Fyrir fylgiskjal með villu og er flutt eru allir frestunarvalkostir einnig fluttir með því.

#### <a name="tax"></a>Skattur

Í sumum tilvikum er hægt að endurgreiða skattupphæðina að fullu eða að hluta. Ef skattupphæð frestanlegrar línu inniheldur óendurgreiðanlega upphæð er óendurgreiðanleg skattupphæð tekin með í upphæð frestunaráætlunar þegar reikningurinn er bókaður.

## <a name="free-text-invoice-transaction-deferral"></a>Frestun reiknings með frjálsum texta

Notaðu síðuna **Frestanir** til að færa inn færibreytur frestunar fyrir dreifingu á reikningslínu með frjálsum texta. Þegar dreifing er færð inn er frestunin sjálfkrafa stillt samkvæmt stillingum frestunar á síðunni **Sjálfgefin gildi frestunar**.

## <a name="fields"></a>Svæði

Síðan **Frestunarfærsla** inniheldur eftirfarandi reiti.

| Svæði | Lýsing |
|-------|-------------|
| Frestað | <p>Tilgreinið hvort línan sé frestun.</p><ul><li>**Já** – línan er frestun.</li><li>**Nei** – línan er ekki frestun.</li></ul><p>Þegar þessi valkostur er stilltur á **Já** er valkosturinn **Laga fyrirliggjandi áætlun** ekki í boði. Fyrir vörur og gjöld sem eru þegar sett upp sem frestað er þessi valkostur stilltur á **Já**. Fyrir vörur og gjöld sem eru ekki sett upp sem sjálfgefið frestað skal stilla þennan valkost á **Já**.</p> |
| Breyta fyrirliggjandi áætlun | <p>Tilgreindu hvort línan sé leiðrétting á fyrirliggjandi frestunaráætlun:</p><ul><li>**Já** – Nýja sölulínan er leiðrétting á fyrirliggjandi frestunaráætlun. Í þessu tilfelli er hægt að velja frestunaráætlun í reitnum **Leiðrétta áætlun**.</li><li>**Nei** – Nýja sölulínan er ekki leiðrétting á fyrirliggjandi frestunaráætlun.</li></ul><p>Þegar þessi valkostur er stilltur á **Já** er valkosturinn **Frestað** ekki í boði.</p> |
| Breytt áætlun | <p>Veldu frestunaráætlunina sem línan er að breyta. Öll gildi á síðunni eru síðan uppfærð með gildunum úr upphaflegu frestunaráætluninni. Ekki er hægt að breyta þeim gildum.</p><p>Þessi reitur er aðeins í boði þegar valkosturinn **Breyta fyrirliggjandi áætlun** er stilltur á **Já**.</p> |
| Dagsetning endurútreiknings | <p>Tilgreindu upphafsdagsetningu tímabilsins sem á að endurreikna eftirstandandi upphæð úr. Sjálfgefin dagsetning er dagsetning næsta óskráða tímabils.</p><p>Þessi reitur er aðeins í boði þegar valkosturinn **Breyta fyrirliggjandi áætlun** er stilltur á **Já**.</p> |
| Lokadagsetning | <p>Lokadagsetningin gæti eða gæti ekki verið uppfærð eftir því hver gerð frestunar er:</p><ul><li>Fyrir línulega frestun skal tilgreina nýja lokadagsetningu fyrir áætlunina. Fyrirliggjandi lokadagsetning frestunaráætlunar er sjálfgefna gildið.</li><li>Fyrir frestun sem tengist tilviki skal tilgreina lokadagsetningu fyrir línu kredittilviks. Þessi dagsetning getur verið auð.</li></ul><p>Þessi reitur er aðeins í boði þegar valkosturinn **Breyta fyrirliggjandi áætlun** er stilltur á **Já**.</p> |
| Númer greiðsluáætlunar | <p>Númer greiðsluáætlunarinnar.</p><p>Þetta svæði er aðeins í boði fyrir endurteknar greiðsluáætlanir samnings.</p> |
| Leiðréttingaraðferð frestunar | <p>Frestaða leiðréttingaraðferðin. Gildið stemmir við gildið á síðunni **Vinnsla fjöldauppsagnar** fyrir áætlun endurtekinnar samningsgreiðslu.</p><p>Þetta svæði er aðeins í boði fyrir endurteknar greiðsluáætlanir samnings.</p> |
| **Lyklar – Tekjur** | |
| Lykill frestunar | <p>Frestunarlyklar, sem er bókunarlykillinn sem birtist á síðunni **Sölupöntun**.</p><p>Ef línunni er ekki frestað er reiturinn auður. Í þessu tilfelli er bókunarlykillinn sjálfgefinn tekjulykill.</p> |
| Skráningarlykill | <p>Tilgreindu lykilinn sem er notaður þegar frestun er skráð. Þessi lykill verður að vera annar en frestunarlykillinn.</p><p>Þegar valkosturinn **Frestað** er upphaflega stilltur á **Já** eru víddargildin sem notuð eru í frestunarlyklinum afrituð í skráningarlykilinn. Ef víddin í frestunarlyklinum er ekki til fyrir skráningarlykilinn er hún hunsuð.</p> |
| Lykill upphaflegrar skráningar | <p>Velja lykilinn fyrir upphaflegu tekjuskráninguna. Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** á síðunni **Færibreytur tekju- og kostnaðarfrestana**.</p> |
| Mótlykill skráningar | <p>Velja lykilinn fyrir jöfnun tekjuskráningu. Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** á síðunni **Færibreytur tekju- og kostnaðarfrestana**.</p> |
| **Lyklar – Afsláttur** | Þessi hluti birtist aðeins fyrir frestaðar vörur. Er falið fyrir frestuð gjöld. |
| Lykill frestunar | <p>Tilgreinið lykilnúmer afsláttarfrestunar. Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þetta svæði er aðeins í boði þegar reiturinn **Frestunarvalkostur afsláttar** er stilltur á **Sérstök áætlun fyrir afslátt** á síðunni **Færibreytur tekju- og kostnaðarfrestunar** og afsláttur er notaður í línunni.</p> |
| Skráningarlykill | <p>Tilgreinið lykilnúmer afsláttarskráningar Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þetta svæði er aðeins í boði þegar reiturinn **Frestunarvalkostur afsláttar** er stilltur á **Sérstök áætlun fyrir afslátt** á síðunni **Færibreytur tekju- og kostnaðarfrestunar** og afsláttur er notaður í línunni.</p> |
| Lykill upphaflegrar skráningar | <p>Veldu lykilinn fyrir fyrstu afsláttargreiningu. Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** á síðunni **Færibreytur tekju- og kostnaðarfrestana** og afsláttur er notaður í línunni.</p> |
| Mótlykill skráningar | <p>Velja lykilinn fyrir jöfnun tekjuskráningu. Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** á síðunni **Færibreytur tekju- og kostnaðarfrestana** og afsláttur er notaður í línunni.</p> |
| **Lyklar – Notkun** | Þessi hluti birtist aðeins fyrir frestaðar vörur. Er falið fyrir frestuð gjöld. |
| Lykill frestunar | <p>Tilgreinið lykilnúmer notkunarfrestunar.</p><p>Fyrir staðlaðar afurðir eru útbúnar tvær frestunaráætlanir:</p><ul><li>**Stöðluð sala** – Tekjuáætlun sem er með kreditstöðu. Í þessu tilviki skal velja lykil fyrir frestun á notkun.</li><li>**Notkun** – Kostnaðaráætlun notkunar (kostnaður seldra vara \[COGS\]) sem er með debetstöðu. Í þessu tilviki skal velja lykil fyrir skráningu á notkun.</li></ul><p>Þegar reikningurinn er bókaður er notkunarupphæðin bókuð á tiltekinn frestunarlykil notkunar. Þessir reitir eru ekki í boði fyrir þjónustuvörur.</p> |
| Skráningarlykill | Tilgreinið lykilnúmer notkunarskráningar. |
| Lykill upphaflegrar skráningar | <p>Tilgreindu lykilinn fyrir upphaflega upphæð notkunarskráningar. Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** á síðunni **Færibreytur tekju- og kostnaðarfrestana**.</p> |
| Mótlykill skráningar | <p>Tilgreindu lykilinn fyrir jöfnunarupphæð notkunarskráningar. Sjálfgildið er af síðunni **Sjálfgefnar frestanir**.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Bókunaraðferð frestunar** er stilltur á **Hagnaður og tap** á síðunni **Færibreytur tekju- og kostnaðarfrestana**.</p> |
| **Tímasetja** | |
| Gerð áætlunar | <p>Veldu tegund frestunaráætlunar: **Línuleg** (sjálfgefið) eða **Byggt á tilviki**.</p><p>Valkostirnir sem birtast á síðunni byggja á tegund frestunaráætlunar sem þú velur.</p><p>Ef sjálfgefið sniðmát er stillt á síðunni **Sjálfgefnar frestanir** fyrir færslulínuna er tegund frestunaráætlunar byggð á gerð sniðmáts sem er valið.</p> |
| **Áætlun - Bein lína** | |
| Sameina fyrri tímabil | <p>Tilgreindu hvort þú vilt sameina línur frestunaráætlunar fyrir eldri tímabil:</p><ul><li>**Já** – Sameinaðu línur frestunaráætlunar fyrir eldri tímabil.</li><li>**Nei** – Ekki sameina línur frestunaráætlunar fyrir eldri tímabil.</li></ul><p>Sjálfgefna gildið er af síðunni **Færibreytur tekju- og kostnaðarfrestana**.</p> |
| Jafnt og á tímabili | <p>Tilgreindu hvort fjöldi daga í hverju tímabili er jafn eða breytilegur eftir tímabili:</p><ul><li>**Já** – sérhvert tímabil hefur sama dagafjölda.</li><li>**Nei** – tímabil hafa ekki sama dagafjölda.</li></ul><p>Þegar þessi valkostur er stilltur á **Nei** er fjöldi daga í tímabili tekinn til greina þegar upphæðin á hverju tímabili fyrir frestunaráætlun er reiknuð.</p><p>Sjálfgefna gildið er af síðunni **Færibreytur tekju- og kostnaðarfrestana**.</p> |
| Áætlun úr sniðmáti | <p>Tilgreindu hvort frestunaráætlunin sé búin til samkvæmt sniðmáti eða lokadagsetningu:</p><ul><li>**Já** – Frestunaráætlunin er búin til samkvæmt sniðmáti.</li><li>**Nei** – Frestunaráætlunin er búin til samkvæmt lokadagsetningu.</li></ul> |
| Sniðmát | Veljið sniðmát frestunar. |
| Hnekkja upphafsdagsetningu | <p>Tilgreinið hvort þið viljið skrifa yfir upphafsdagsetningu:</p><ul><li>**Já** – Hnekktu upphafsdagsetningu með dagsetningu sem færð er inn í reitinn **Upphafsdagsetning**.</li><li>**Nei** – Upphafsdagsetning er reglan **Sjálfgefin upphafsdagsetning frestunar** sem er notuð á dagsetningu reiknings sem tilgreind er á síðunni **Bókun reiknings**. Hægt er að stilla þetta á síðunni **Færibreytur tekju- og kostnaðarfrestana**.</li></ul> |
| Upphafsdagsetning frestunar | Tilgreinið upphafsdagsetningu frestunar. Færsludagsetningin er sjálfgefið gildi. |
| Lokadagsetning frestunar | <p>Lokadagsetning frestunarinnar.</p><p>Þessi dagsetning er sjálfkrafa reiknuð samkvæmt sniðmáti frestunar. Ef ekkert sniðmát er valið þarf að færa dagsetninguna inn handvirkt.</p> |
| **Áætlun – Byggt á tilviki** | |
| Sniðmát | <p>Veljið sniðmát byggt á tilviki. Þetta svæði er valkostur.</p><p>Ef sniðmát er valið skrifa gildin úr sniðmátinu yfir öll gögn tengd tilviki og tilvikslínur.</p> |
| Úthlutunargerð | <p>Veljið úthlutunargerð fyrir tilvikslínur.</p><ul><li>**Breytilegar upphæðir** – Sérstök úthlutunarupphæð er færð inn fyrir hverja línu.</li><li>**Jafnar upphæðir** – Upphæðinni er úthlutað jafnt fyrir hverja línu.</li><li>**Prósenta** – Upphæð er úthlutað samkvæmt prósentugildinu sem er fært inn fyrir hverja línu.</li><li>**Prósentum lokið** – Uppsafnað lokagildi er slegið inn fyrir hverja línu.</li><p>**Breytilegt magn** – Tiltekið úthlutunarmagn er slegið inn fyrir hverja línu.</li></ul><p>**Athugasemd:** Ef velja á **Prósentum lokið** verða dagsetningarnar að vera í hækkandi röð.</p> |
| **Búa til aðskilin tilvik á hverja einingu** | |
| Lýsing | <p>Tilgreina skal hvort eigi að aðskilja tilvik eftir einingu:</p><ul><li>**Já** – Aðskildu tilvikslínurnar þannig að ein lína er fyrir hvert magn.<p>Til dæmis eru þrjár tilvikslínur og reikningurinn er með magn upp á fjóra. Í þessu tilviki verður frestunaráætlunin með 12 línur.</p></li><li>**Nei** – Ekki aðskilja tilvikslínurnar.</li></ul> |
| Lykill gildistíma | <p>Veldu lykilinn sem er notaður til að skrá útrunnar línur. Þú getur valið lykilinn eftir að frestunaráætlunin er búin til.</p><p>Ef gildisdagsetningin er ákveðin fyrir tilvik, meðan á skráningarferlinu stendur, fer skráningarupphæðin gildistímalykilinn í staðinn fyrir skráningarlykilinn.</p> |
| **Áætlun – Línur byggðar á tilviki** | |
| Lýsing | Lýsing á tilvikinu. |
| Lokadagsetning frestunar | <p>Veljið lokadagsetningu viðburðarins.</p><p>**Athugaðu:** Ef valin er lokadagsetning er reiturinn **Gildisdagsetning** hreinsaður. Þú getur ekki notað bæði lokadagsetningu og síðasta gildisdag.</p> |
| Lokadagur | <p>Veljið lokadagsetningu viðburðarins.</p><p>**Athugaðu:** Ef valin er lokadagsetning er reiturinn **Gildisdagsetning** hreinsaður. Þú getur ekki notað bæði lokadagsetningu og síðasta gildisdag.</p> |
| Magn | <p>Tilgreinið úthlutunarmagnið. Sjálfgefið gildi fyrir allar línur er **0** (núll). Ef magnið er uppfært verður heildarmagn allra línanna að vera jafnt og eða minna en magnið sem er tilgreint fyrir vörulínuna í sölupöntuninni.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Úthlutunargerð** er stilltur á **Breytilegt magn**.</p><p>Ef magni vörulínunnar í sölupöntuninni er breytt þannig að það er minna en upprunalegt magn og reikningur er búinn til, þá eru færri tilvikstengdar línur búnar til. Heildarmagn úthlutunar fer ekki yfir magnið sem er tilgreint í upprunalegri sölupöntun eða greiðsluáætlun.</p> |
| Úthlutunarhlutfall | <p>Tilgreinið úthlutunarhlutfallið. Ef reiturinn **Úthlutunargerð** er stilltur á **Prósenta** eða **Prósentum lokið** er hægt að færa prósentu inn handvirkt. Annars reiknast það sjálfkrafa.</p><p>Ef reiturinn **Úthlutunargerð** er stilltur á **Prósenta** verður samtala prósentanna að vera 100.</p> |
| Upphæð | <p>Tilgreinið úthlutunarupphæðina. Ef reiturinn **Úthlutunargerð** er stilltur á **Breytilegar upphæðir** eða **Prósentum lokið** er hægt að færa upphæðina inn handvirkt.</p><p>Ef reiturinn **Úthlutunargerð** er stilltur á **Prósentum lokið** og upphæð er færð inn hér verður gildið í reitnum **Prósentum lokið** reiknað út sjálfkrafa.</p><p>Vegna sléttunar stemmir reiknuð upphæð ef til vill ekki við það sem er slegið inn handvirkt. Ef þú þarft nákvæma upphæð skal stilla reitinn **Úthlutunargerð** á **Breytilegar upphæðir**.</p> |
| Hlutfall lokinna leikja | <p>Tilgreinið hlutfall frágengins. Gildið verður að vera milli 0 (núll) og 100.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Úthlutunargerð** er stilltur á **Hlutfall frágengins**.</p> |
| Lokaupphæð | <p>Reiknuð heildarupphæð fyrir allar línur í frestunaráætlun.</p><p>Ef reiturinn **Úthlutunargerð** er stilltur á **Prósentum lokið** er hægt að færa upphæð inn handvirkt. Í þessu tilfelli er gildið í reitnum **Prósentum lokið** reiknaður samkvæmt upphæðinni sem slegin er inn.</p><p>Vegna sléttunar stemmir reiknuð upphæð ef til vill ekki við það sem er slegið inn handvirkt.</p><p>Þessi reitur er aðeins í boði þegar reiturinn **Úthlutunargerð** er stilltur á **Hlutfall frágengins**.</p> |
| Greina í færslu | <p>Tilgreindu hvort línan sé sjálfkrafa skráð um leið og færslan er bókuð:</p><ul><li>**Valið** – Línan er sjálfkrafa skráð um leið og færslan er bókuð.</li><li>**Hreinsað** – Línan er ekki skráð um leið og færslan er bókuð.</li></ul> |
| Skráningarlykill | <p>Tilgreindu skráningarlykilinn fyrir tilvikið ef lykill er frábrugðin lyklinum sem er notaður fyrir alla frestunaráætlunina.</p><p>Nota má þennan reit með valkostinum **Skrá við bókun**.</p> |

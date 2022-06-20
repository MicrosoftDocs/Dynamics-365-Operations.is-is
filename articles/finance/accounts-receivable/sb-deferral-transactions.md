---
title: Frestunarfærslur í áskriftarreikningi
description: Þessi grein lýsir hinum ýmsu færslum sem hægt er að nota í frestun sem hluta af tekju- og kostnaðarfrestun í áskriftarreikningi.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872587"
---
# <a name="deferral-default-transactions"></a>Sjálfgefnar frestunarfærslur

Þessi grein lýsir þeim færslum sem gera ráð fyrir frestun tekna og gjalda. Frestunaráætlanir eru alltaf byggðar á og eru háðar upprunaskjali eða innheimtuáætlun. Frestunaráætlanir eru búnar til á grundvelli sjálfgefna og ekki er hægt að slá inn eða búa til sérstaklega.

## <a name="sales-order-transaction-deferral"></a>Frestun sölupöntunarfærslu

Nota **Frestun** eða **Búðu til inneignarnótu** síðu til að slá inn eða breyta frestunarfæribreytum fyrir sölupöntunarlínu.

> [!NOTE]
> Þegar sölupöntun er stofnuð úr innheimtuáætlun eru öll gildi á **Frestun** eða **Búðu til inneignarnótu** síða er skrifvarinn og ekki er hægt að breyta frestunarbreytunum. Til að breyta gildunum skaltu nota **Breyta áætlun** síðu.

### <a name="edit-deferral-options"></a>Breyta frestunarvalkostum

Til að breyta frestunarvalkostum fyrir línu skaltu fylgja þessum skrefum.

1. Stofna sölupöntunarfærslu.
2. Veldu línuna og veldu síðan **Frestun**.
3. Á **Frestun viðskipta** síðu, the **Frestað** valkostur verður að vera stilltur á **Já**. Breyttu öðrum sviðum eftir þörfum.
4. Til að forskoða frestunaráætlunina skaltu velja **Forskoðun**.
5. Ef þú gerðir einhverjar breytingar á færslufrestun skaltu velja **Allt í lagi**, og farðu aftur á viðskiptasíðuna.
6. Skuldbinda og bóka færsluna.

Eftir að færslan hefur verið bókuð skaltu opna **Allar frestunaráætlanir** síðu til að skoða frestunaráætlun.

### <a name="create-a-credit-note"></a>Búðu til inneignarnótu

Til að stofna kreditnótu, skal fylgja eftirfarandi skrefum.

1. Stofna sölupöntunarfærslu.
2. Í **Sölupöntunarlínur** kafla, veldu hlutinn sem þú vilt búa til kreditnótu fyrir.
3. Veldu **Sölupöntunarlína** \> **Nýtt**, og veldu síðan **Inneignarnótu**.
4. Veldu **Frestun**.
5. Á **Frestun sölupöntunarfærslu** síðu, stilltu **Stilltu núverandi áætlun** valmöguleika til **Já** fyrir hlutinn.
6. Í **Leiðrétt dagskrá** reit skaltu velja frestunaráætlunina sem þú vilt nota kreditnótuna á.
7. Uppfærðu **Endurreikna dagsetningu** og **Loka dagsetning** reiti eins og þú þarfnast.
8. Veldu **Í lagi**.
9. Ljúktu við að bóka sölupöntunarfærsluna.

### <a name="purchase-orders-and-purchase-invoices"></a>Innkaupapantanir og innkaupareikningar

Ef þú vilt nota frestunaraðgerðina fyrir innkaupapöntun skaltu búa til reikninginn fyrst. Notaðu síðan **Reikningar seljanda í bið** síðu til að breyta eða bæta við frestunaratriðum. Þú getur ekki breytt eða bætt við frestun beint á innkaupapöntun.

1. Nota **Reikningar seljanda í bið** síðu til að slá inn reikning lánardrottins.

    Þegar þú slærð inn línu er frestunin sjálfkrafa stillt fyrir vöruna eða innkaupaflokkinn sem þú velur. Þessi frestun er byggð á uppsetningu frestunarinnar á **Frestun vanskil** síðu. Hægt er að breyta frestuninni eða bæta við á dreifingarstigi.

3. Á innkaupalínunni velurðu **Fjármál \> Úthluta upphæðum**.
4. Veldu fyrir hverja dreifingarupphæð **Frestun**. Þegar reikningurinn er bókaður er búið til frestunaráætlun fyrir hverja dreifingu sem frestun er stillt á.

### <a name="tax"></a>Skattur

Í sumum tilfellum getur skattfjárhæðin verið óafturkræf að fullu eða að hluta. Ef skattupphæð frestunarhæfrar línu inniheldur óafturkræf fjárhæð, er óendurheimtanleg skattfjárhæð innifalin í fresthæfðri áætlunarupphæð þegar reikningurinn er bókaður.

### <a name="variance"></a>Frávik

Ef upphæðin á reikningslínu lánardrottins er frábrugðin upphæðinni á innkaupapöntunarlínunni eru fráviksdreifingar búnar til. Ef línunni er frestað er fjárhagsreikningur fyrir þessar dreifingar stilltur á frestunarreikninginn og upphæðirnar eru innifaldar í frestanlegu áætlunarupphæðinni þegar reikningurinn er bókaður. Þessar dreifingar eru nefndar **Verðfrávik** og **Kostnaðarfrávik**.

### <a name="general-journals-and-invoice-journals"></a>Almenn færslubækur og reikningabækur

Nota **Frestun** síðu til að slá inn frestunarfæribreytur fyrir færslubókar fylgiskjal línu. Þú getur líka forskoðað frestunaráætlunina fyrir frestun beina línu. Þegar þú slærð inn línu er frestunin sjálfkrafa stillt á grundvelli uppsetningar frestunarreikninga á **Frestun vanskil** síðu. Þú getur handvirkt breytt frestunarvalkostum fyrir hverja línu. Þegar færslubókarskírteinið er bókað er frestunaráætlunin búin til.

#### <a name="post-and-transfer"></a>Bóka og flytja

Til að bóka dagbókarskírteini skaltu nota **Birta og flytja** skipun. Frestunarmöguleikarnir munu fylgja línunni sem skírteinið á við. Fyrir fylgiskjöl sem eru ekki með villum er frestunaráætlun búin til ef henni er frestað. Fyrir skírteini sem hefur villu og er flutt, eru allir frestunarmöguleikar einnig fluttir með henni.

#### <a name="tax"></a>Skattur

Í sumum tilfellum getur skattfjárhæðin verið óafturkræf að fullu eða að hluta. Ef skattupphæð frestunarhæfrar línu inniheldur óafturkræf fjárhæð, er óendurheimtanleg skattfjárhæð innifalin í fresthæfðri áætlunarupphæð þegar reikningurinn er bókaður.

## <a name="free-text-invoice-transaction-deferral"></a>Frestun á færslu reiknings með frjálsum texta

Nota **Frestun** síðu til að slá inn frestunarfæribreytur fyrir reikningslínudreifingu með frjálsum texta. Þegar dreifing er slegin inn er frestunin sjálfkrafa stillt á grundvelli frestunarstillinganna á **Frestun vanskil** síðu.

## <a name="fields"></a>Svæði

The **Frestun viðskipta** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|-------|-------------|
| Frestað | <p>Tilgreindu hvort línan sé frestun:</p><ul><li>**Já** - Línan er frestun.</li><li>**Nei** - Línan er ekki frestun.</li></ul><p>Þegar þessi valkostur er stilltur á **Já**, hinn **Stilltu núverandi áætlun** valkostur er ekki í boði. Fyrir vörur og gjöld sem þegar eru sett upp sem frestað er þessi valkostur stilltur á **Já**. Fyrir vörur og gjöld sem eru ekki sett upp sem frestað sjálfgefið skaltu stilla þennan valkost á **Já**.</p> |
| Breyta fyrirliggjandi áætlun | <p>Tilgreindu hvort línan sé leiðrétting á núverandi frestunaráætlun:</p><ul><li>**Já** – Nýja sölulínan er aðlögun að núverandi frestunaráætlun. Í þessu tilviki geturðu valið frestunaráætlun í **Leiðrétt dagskrá** sviði.</li><li>**Nei** – Nýja sölulínan er ekki aðlögun að núverandi frestunaráætlun.</li></ul><p>Þegar þessi valkostur er stilltur á **Já**, hinn **Frestað** valkostur er ekki í boði.</p> |
| Breytt áætlun | <p>Veldu frestunaráætlunina sem línan er að laga. Öll gildi á síðunni eru síðan uppfærð með gildunum frá upphafsfrestunaráætluninni. Ekki er hægt að breyta þessum gildum.</p><p>Þessi reitur er aðeins tiltækur þegar **Stilltu núverandi áætlun** valkostur er stilltur á **Já**.</p> |
| Dagsetning endurútreiknings | <p>Tilgreindu upphafsdag tímabilsins sem þú vilt endurreikna upphæðina sem eftir er af. Sjálfgefin dagsetning er dagsetning næsta óþekkta tímabils.</p><p>Þessi reitur er aðeins tiltækur þegar **Stilltu núverandi áætlun** valkostur er stilltur á **Já**.</p> |
| Lokadagsetning | <p>Það fer eftir tegund frestunarinnar, lokadagsetningin gæti verið uppfærð eða ekki:</p><ul><li>Fyrir beina línu frestun, tilgreinið nýja lokadagsetningu áætlunarinnar. Núverandi lokadagsetning frestunaráætlunarinnar er sjálfgefið gildi.</li><li>Fyrir frestun sem byggir á atburði, tilgreinið lokadagsetningu lánaviðburðarlínunnar. Þessi dagsetning má vera auð.</li></ul><p>Þessi reitur er aðeins tiltækur þegar **Stilltu núverandi áætlun** valkostur er stilltur á **Já**.</p> |
| Númer greiðsluáætlunar | <p>Númer innheimtuáætlunar.</p><p>Þessi reitur er aðeins tiltækur fyrir endurteknar innheimtuáætlanir samninga.</p> |
| Leiðréttingaraðferð frestunar | <p>Frestað aðlögunaraðferðin. Gildið passar við gildið á **Fjöldauppsagnarvinnsla** síðu fyrir endurtekna innheimtuáætlun samnings.</p><p>Þessi reitur er aðeins tiltækur fyrir endurteknar innheimtuáætlanir samninga.</p> |
| **Reikningar - Tekjur** | |
| Lykill frestunar | <p>Frestunarreikningurinn, sem er bókunarreikningurinn sem birtist á **Sölupöntun** síðu.</p><p>Ef línunni er ekki frestað er þessi reitur auður. Í þessu tilviki er bókunarreikningurinn sjálfgefinn tekjureikningur.</p> |
| Skráningarlykill | <p>Tilgreindu reikninginn sem er notaður þegar frestun er viðurkennd. Þessi reikningur verður að vera frábrugðinn frestunarreikningnum.</p><p>Þegar **Frestað** valkostur er upphaflega stilltur á **Já**, eru víddargildin sem eru notuð í frestunarreikningnum afrituð á viðurkenningarreikninginn. Ef víddin í frestunarreikningnum er ekki til fyrir viðurkenningarreikninginn er hún hunsuð.</p> |
| Lykill upphaflegrar skráningar | <p>Veldu reikninginn fyrir upphaflega tekjufærslu. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap** á **Færslur tekna og gjalda frestun** síðu.</p> |
| Mótlykill skráningar | <p>Veldu reikninginn fyrir tekjufærslu á móti. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap** á **Færslur tekna og gjalda frestun** síðu.</p> |
| **Reikningar - Afsláttur** | Þessi hluti birtist aðeins fyrir frestað atriði. Það er falið fyrir frestað gjöld. |
| Lykill frestunar | <p>Tilgreindu númer afsláttarfrestunarreiknings. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Afsláttur frestun valkostur** reiturinn er stilltur á **Sérstök dagskrá fyrir afslátt** á **Færslur tekna og gjalda frestun** síðu og er afsláttur settur á línuna.</p> |
| Skráningarlykill | <p>Tilgreindu númer afsláttarviðurkenningarreiknings. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Afsláttur frestun valkostur** reiturinn er stilltur á **Sérstök dagskrá fyrir afslátt** á **Færslur tekna og gjalda frestun** síðu og er afsláttur settur á línuna.</p> |
| Lykill upphaflegrar skráningar | <p>Veldu reikninginn fyrir upphaflega afsláttarviðurkenningu. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap** á **Færslur tekna og gjalda frestun** síðu og er afsláttur settur á línuna.</p> |
| Mótlykill skráningar | <p>Veldu reikninginn fyrir tekjufærslu á móti. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap** á **Færslur tekna og gjalda frestun** síðu og er afsláttur settur á línuna.</p> |
| **Reikningar - Neysla** | Þessi hluti birtist aðeins fyrir frestað atriði. Það er falið fyrir frestað gjöld. |
| Lykill frestunar | <p>Tilgreindu númer neyslufrestunarreiknings.</p><p>Fyrir staðlaðar vörur eru tvær frestunaráætlanir búnar til:</p><ul><li>**Hefðbundin sala** – Tekjuáætlun sem hefur inneign. Í þessu tilviki skaltu velja neyslufrestunarreikning.</li><li>**Neysla** – Neysla (kostnaður við seldar vörur\[ COGS\]) kostnaðaráætlun sem hefur debetjöfnuð. Í þessu tilviki skaltu velja neysluviðurkenningarreikninginn.</li></ul><p>Þegar reikningur er bókaður er neysluupphæð bókuð á tilgreindan neyslufrestunarreikning. Þessir reitir eru ekki tiltækir fyrir þjónustuvörur.</p> |
| Skráningarlykill | Tilgreindu reikningsnúmer neysluviðurkenningar. |
| Lykill upphaflegrar skráningar | <p>Tilgreindu reikninginn fyrir upphaflega neysluupphæð. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap** á **Færslur tekna og gjalda frestun** síðu.</p> |
| Mótlykill skráningar | <p>Tilgreindu reikninginn fyrir mótvægisupphæð neyslufærslu. Sjálfgefið gildi er frá **Frestun vanskil** síðu.</p><p>Þessi reitur er aðeins tiltækur þegar **Frestun bókunaraðferð** reiturinn er stilltur á **Hagnaður og tap** á **Færslur tekna og gjalda frestun** síðu.</p> |
| **Tímasetja** | |
| Gerð áætlunar | <p>Veldu tegund frestunaráætlunar: **Bein lína** (sjálfgefið) eða **Byggt á viðburðum**.</p><p>Valmöguleikarnir sem birtast á síðunni eru byggðir á frestunaráætlunargerðinni sem þú velur.</p><p>Ef sjálfgefið sniðmát er stillt á **Frestun vanskil** síðu fyrir færslulínuna, er gerð frestunaráætlunar byggð á gerð sniðmáts sem er valið.</p> |
| **Dagskrá - Bein lína** | |
| Sameina fyrri tímabil | <p>Tilgreindu hvort þú vilt sameina frestunaráætlunarlínur fyrir fyrri tímabil:</p><ul><li>**Já** – Sameinaðu frestunaráætlunarlínur fyrir fyrri tímabil.</li><li>**Nei** – Ekki sameina frestunaráætlunarlínur fyrir fyrri tímabil.</li></ul><p>Sjálfgefið gildi er frá **Færslur tekna og gjalda frestun** síðu.</p> |
| Jafnt á tímabili | <p>Tilgreindu hvort fjöldi daga á hverju tímabili sé jafn eða breytilegur eftir tímabili:</p><ul><li>**Já** - Hvert tímabil hefur sama fjölda daga.</li><li>**Nei** – Tímabil hafa ekki sama dagafjölda.</li></ul><p>Þegar þessi valkostur er stilltur á **Nei**, er litið til fjölda daga á tímabili þegar upphæð á hverju tímabili fyrir frestunaráætlun er reiknuð út.</p><p>Sjálfgefið gildi er frá **Færslur tekna og gjalda frestun** síðu.</p> |
| Áætlun úr sniðmáti | <p>Tilgreindu hvort frestunaráætlunin sé búin til á grundvelli sniðmáts eða lokadagsetningar:</p><ul><li>**Já** – Frestunaráætlunin er búin til á grundvelli sniðmáts.</li><li>**Nei** – Frestunaráætlunin er búin til miðað við lokadagsetningu.</li></ul> |
| Sniðmát | Veldu frestunarsniðmátið. |
| Hnekkja upphafsdagsetningu | <p>Tilgreindu hvort þú vilt hnekkja upphafsdagsetningu:</p><ul><li>**Já** – Hneka upphafsdagsetningu með dagsetningunni sem þú slærð inn í **Upphafsdagur** sviði.</li><li>**Nei** - Upphafsdagur er kl **Sjálfgefin upphafsdagur frestunar** regla sem er notuð á reikningsdagsetningu sem tilgreindur er á **Bókun reiknings** síðu. Þessa reglu er hægt að setja á **Færslur tekna og gjalda frestun** síðu.</li></ul> |
| Upphafsdagsetning frestunar | Tilgreindu upphafsdag frestunarinnar. Viðskiptadagsetningin er sjálfgefið gildi. |
| Lokadagsetning frestunar | <p>Lokadagur frestunarinnar.</p><p>Þessi dagsetning er sjálfkrafa reiknuð út frá frestunarsniðmátinu. Ef ekkert sniðmát er valið verður þú að slá inn dagsetninguna handvirkt.</p> |
| **Dagskrá - Byggt á viðburðum** | |
| Sniðmát | <p>Veldu sniðmát sem byggir á viðburðum. Þessi reitur er valfrjáls.</p><p>Ef þú velur sniðmát skrifa gildin úr sniðmátinu yfir öll gögn sem byggjast á atburðum og atburðalínur.</p> |
| Úthlutunargerð | <p>Veldu úthlutunartegund fyrir viðburðarlínurnar:</p><ul><li>**Breytileg upphæð** – Ákveðin úthlutunarupphæð er færð inn fyrir hverja línu.</li><li>**Jafnar upphæðir** – Upphæðinni er úthlutað jafnt fyrir hverja línu.</li><li>**Hlutfall** – Upphæð er úthlutað miðað við prósentugildið sem er slegið inn fyrir hverja línu.</li><li>**Prósenta af verklokum** – Uppsafnað fullnaðargildi er slegið inn fyrir hverja línu.</li><p>**Breytilegt magn** – Ákveðið úthlutunarmagn er fært inn fyrir hverja línu.</li></ul><p>**Athugið:** Ef þú vilt velja **Prósenta af verklokum**, dagsetningar verða að vera í hækkandi röð.</p> |
| **Búa til aðskilin tilvik á hverja einingu** | |
| Lýsing | <p>Tilgreindu hvort þú vilt aðgreina atburði á hverja einingu:</p><ul><li>**Já** – Aðskilið atburðarlínurnar þannig að ein lína sé á hvert magn.<p>Til dæmis eru þrjár viðburðarlínur og reikningurinn hefur fjórar. Í þessu tilviki hefur frestunaráætlunin sem myndast 12 línur.</p></li><li>**Nei** – Ekki aðskilja viðburðalínurnar.</li></ul> |
| Lykill gildistíma | <p>Veldu reikninginn sem er notaður fyrir viðurkenndar útrunnar línur. Þú getur valið reikninginn eftir að frestunaráætlunin er búin til.</p><p>Ef fyrningardagur er stilltur fyrir atburð, á meðan á viðurkenningarferlinu stendur, fer viðurkenningarupphæðin á fyrningarreikninginn í stað viðurkenningarreikningsins.</p> |
| **Dagskrá - Atburðabyggðar línur** | |
| Lýsing | Lýsing á atburðinum. |
| Lokadagsetning frestunar | <p>Veldu lokadagsetningu viðburðarins.</p><p>**Athugið:** Ef þú velur lokadagsetningu, **Gildistími** reitur er hreinsaður. Þú getur ekki notað bæði lokadagsetningu og fyrningardagsetningu.</p> |
| Lokadagur | <p>Veldu gildistíma viðburðarins.</p><p>**Athugið:** Ef þú velur lokadagsetningu, **Gildistími** reitur er hreinsaður. Þú getur ekki notað bæði lokadagsetningu og fyrningardagsetningu.</p> |
| Magn | <p>Tilgreindu úthlutunarmagn. Sjálfgefið gildi fyrir allar línur er **0** (núll). Ef magnið er uppfært verður heildarmagn allra lína að vera jafnt eða minna en magnið sem er tilgreint fyrir línuvöruna í sölupöntuninni.</p><p>Þessi reitur er aðeins tiltækur þegar **Tegund úthlutunar** reiturinn er stilltur á **Breytilegt magn**.</p><p>Ef magni línunnar í sölupöntuninni er breytt þannig að það sé minna en upprunalega magnið og reikningurinn er stofnaður, eru færri atburðabundnar línur búnar til. Heildarúthlutað magn fer ekki yfir magnið sem tilgreint er á upphafssölupöntuninni eða reikningsáætluninni.</p> |
| Úthlutunarhlutfall | <p>Tilgreindu úthlutunarprósentu. Ef **Tegund úthlutunar** reiturinn er stilltur á **Hlutfall** eða **Prósenta af verklokum**, þú getur slegið inn prósentu handvirkt. Annars er það sjálfkrafa reiknað út.</p><p>Ef **Tegund úthlutunar** reiturinn er stilltur á **Hlutfall**, verður heildarhlutfallið að vera 100.</p> |
| Upphæð | <p>Tilgreindu upphæð úthlutunar. Ef **Tegund úthlutunar** reiturinn er stilltur á **Breytileg upphæð** eða **Prósenta af verklokum**, þú getur slegið inn upphæð handvirkt.</p><p>Ef **Tegund úthlutunar** reiturinn er stilltur á **Prósenta af verklokum**, og þú slærð inn upphæð hér, gildið á **Fullnaðarprósenta** reiturinn er sjálfkrafa reiknaður.</p><p>Vegna námundunar gæti reiknað magn gæti ekki passað nákvæmlega við það sem er fært inn handvirkt. Ef þú þarft nákvæma upphæð skaltu stilla **Tegund úthlutunar** sviði til **Breytileg upphæð**.</p> |
| Hlutfall lokinna leikja | <p>Tilgreindu prósentu af fullnustu. Gildið verður að vera á milli 0 (núll) og 100.</p><p>Þessi reitur er aðeins tiltækur þegar **Tegund úthlutunar** reiturinn er stilltur á **Prósenta af verklokum**.</p> |
| Lokaupphæð | <p>Reiknuð heildarfjölda fyrir allar línur í frestunaráætlun.</p><p>Ef **Tegund úthlutunar** reiturinn er stilltur á **Prósenta af verklokum**, þú getur slegið inn upphæð handvirkt. Í þessu tilviki er verðmæti **Fullnaðarprósenta** reiturinn er reiknaður út frá upphæðinni sem þú slærð inn.</p><p>Vegna námundunar gæti reiknað magn gæti ekki passað nákvæmlega við það sem er fært inn handvirkt.</p><p>Þessi reitur er aðeins tiltækur þegar **Tegund úthlutunar** reiturinn er stilltur á **Prósenta af verklokum**.</p> |
| Kannast við færslu | <p>Tilgreindu hvort línan sé sjálfkrafa þekkt um leið og færslan er bókuð:</p><ul><li>**Valið** – Línan er sjálfkrafa þekkt um leið og færslan er bókuð.</li><li>**Hreinsað** – Línan er ekki þekkt um leið og færslan er bókuð.</li></ul> |
| Skráningarlykill | <p>Tilgreindu viðurkenningarreikninginn fyrir viðburðinn, ef reikningurinn er frábrugðinn reikningnum sem er notaður fyrir alla frestunaráætlunina.</p><p>Þú getur notað þennan reit í tengslum við **Kannast við færslu** valmöguleika.</p> |

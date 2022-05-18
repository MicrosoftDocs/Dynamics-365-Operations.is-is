---
title: Frestunaráætlanir í tekju- og kostnaðarfrestun
description: Þetta efnisatriði lýsir frestun áætlunum í tekju- og kostnaðarfrestun.
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
ms.openlocfilehash: 9135ac733496a0c5d79669c35972c273c209f81d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685978"
---
# <a name="deferral-schedules"></a>Frestunaráætlanir

Frestunaráætlanir eru búnar til eftir að færsla hefur verið bókuð.

Þú getur notað **Allar frestunaráætlanir** eða **Virkar frestunaráætlanir** síðu til að fara yfir upplýsingar um frestunaráætlun. Upplýsingarnar sem birtast eru háðar tegund frestunaráætlunar (bein lína eða atburðamiðuð) og færslugerð. Það inniheldur frestunaráætlunarlínur og heildarupphæðir fyrir frestunaráætlunina. Þú getur notað síðuna til að breyta frestunaráætluninni.

## <a name="recognize-revenue"></a>Skrá tekjur

> [!NOTE]
> - Til að greina tekjur fyrir eina frestunaráætlun, byrjaðu á skrefi 1.
> - Til að greina tekjur fyrir margar áætlanir, byrjaðu á skrefi 2.

1. Á **Allar frestunaráætlanir** síðu, í **Dagskrárlínur** hnitanet, veldu línurnar sem þú vilt þekkja og veldu síðan **Kannast við**.
2. Á **Viðurkenningarvinnsla** síðu, stilltu **Viðurkenningaraðgerð** sviði til **Búðu til viðurkenningardagbók**.
3. Í **Lokadagur** reit, veldu lokadagsetningu. Vinnslan mun aðeins innihalda línur þar sem lokadagsetningin er fyrr en eða sú sama og valin lokadagsetning.
4. Veldu **Sía**, og bættu við gagnasíum þannig að listinn sýni aðeins svið skráa sem þú vilt.
5. Veldu **Skoða forskoðun** til að skoða línurnar.
6. Í listanum yfir línur velurðu allar línur sem þú vilt ekki vinna úr og veldu síðan **Fjarlægja**.
7. Veldu hvort þú vilt taka saman viðurkenningarbókarfærsluna.
8. Í **Dagsetning viðskipta** kafla er hægt að hnekkja færsludagsetningu með tiltekinni dagsetningu til að vinna úr færslunni. Hægt er að tilgreina viðskiptadagsetningu fyrir lokuð tímabil.
9. Til að gera vinnsluna sem hluta af lotu skaltu velja **Hópur**. Í **Lotuvinnsla** valmynd, stilltu færibreytur fyrir rununa og veldu síðan **Allt í lagi** að fara aftur til **Viðurkenningarvinnsla** síðu. Tekjufærslan verður afgreidd síðar, þegar lotan er afgreidd.
10. Veldu **Ferli**. Ef þú bættir færslunni ekki við runu eru allar línur unnar strax. Að öðrum kosti verða línurnar unnar þegar lotan er unnin.

## <a name="modify-a-schedule"></a>Breyta áætlun

Fylgdu þessum skrefum til að breyta frestunaráætlun.

1. Á **Allar frestunaráætlanir** síðu, veldu frestunaráætlunina og veldu síðan **Bókhald \> Breyta áætlun**.
2. Á **Breyta áætlun** síðu, breyttu valkostunum sem þú vilt breyta. Það fer eftir frestunaráætluninni, þú munt ekki geta breytt öllum valkostunum.
3. Veldu **Forskoðun** að endurskoða breytingar á frestunaráætlun.
4. Veldu **Í lagi**.

### <a name="straight-line-deferral-schedules"></a>Bein lína frestunaráætlanir

Ef frestunaráætlunin hefur engar viðurkenndar eða ytra bókaðar línur er hægt að breyta allri frestunaráætluninni, þar með talið upphafsdagsetningu.

Ef frestunaráætlunin hefur einhverjar viðurkenndar línur eða bókaðar ytra, og þú breytir frestunaráætluninni, fer framkoma frestunaráætlunarinnar eftir endurútreikningsdegi og lokadagsetningu frestunar viðurkenndra lína. Sjálfgefið er að fyrsta tímabilið sem var ekki viðurkennt ákvarðar lokadagsetningu frestunarinnar.

Til að nota dagsetningu viðurkenningar skaltu velja eitt af eftirfarandi gildum í **Upphaf áætlunar** reit: 
- **Náðu þér** – Upphæðin eftir að allar viðurkenndar línur eru endurreiknaðar.
- **Viðsnúningur** – Allar línur eftir endurútreikningsdagsetningu eru bakfærðar með því að nota tilgreint færslubókarheiti og bókunardagsetningu. Upphæðin eftir endurútreikningsdaginn er síðan endurreiknuð.

Ef sniðmát er notað er sleppt tímabil hunsuð og sniðmátið er aðeins notað til að reikna út lokadagsetningu.

### <a name="event-based-deferral-schedules"></a>Áætlanir um frestun á viðburðum

Fyrir frestunaráætlun sem byggir á viðburðum geturðu breytt öllum óþekktum línum.

Ef frestunaráætlunin hefur einhverjar viðurkenndar eða ytra bókaðar línur er ekki hægt að breyta sniðmátinu og úthlutunargerðinni fyrir frestunaráætlunina. Þegar þú breytir fyrirliggjandi frestunaráætlun geturðu ekki breytt gildinu **Búðu til sérstaka viðburði fyrir hverja einingu** sviði.

Ef lína er viðurkennd eða sett utan á, **Viðurkennd** gátreiturinn er valinn.

## <a name="modify-a-deferral-or-recognition-account"></a>Breyta frestunar- eða viðurkenningarreikningi

Til að breyta frestun eða viðurkenningarreikningi fyrir frestunaráætlun skaltu fylgja þessum skrefum.

1. Á **Allar frestunaráætlanir** síðu, veldu frestunaráætlunina og veldu síðan **Bókhald \> Breyta reikningi**.
2. Á **Breyta reikningi** síðu, veldu reikninginn sem þú vilt breyta (frestun, skammtíma eða viðurkenning).
3. Í **Nýr reikningur** reit, veldu nýja reikninginn.
4. Veldu hvort breytingar á reikningnum stofni leiðréttingarbókarfærslur.
5. Ef þú stillir valkostinn á **Já** í fyrra skrefi skaltu velja dagbókarheitið í **Nafn dagbókar** reitnum og tilgreindu viðskiptadagsetninguna í **Dagsetning viðskipta** sviði.
6. Veldu **Í lagi**.

## <a name="put-a-deferral-schedule-on-hold"></a>Settu frestunaráætlun í bið

Fylgdu þessum skrefum til að setja frestunaráætlun í bið.

1. Á **Allar frestunaráætlanir** síðu, veldu frestunaráætlunina og veldu síðan **Haltu \> Settu haltu**.
2. Á **Settu haltu** síðu, veldu hvort þú vilt flytja stöðuna af frestunarreikningi eða biðreikningi.
3. Ef þú valdir að flytja stöðuna skaltu velja færslubókarheitið í **Nafn dagbókar** reit, veldu biðreikninginn í **Á biðreikningi** reitnum og tilgreindu viðskiptadagsetninguna í **Dagsetning viðskipta** sviði.
4. Veldu **Í lagi**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Fjarlægja bið frá frestun áætlun

Til að fjarlægja frestunaráætlun úr bið skaltu fylgja þessum skrefum.

1. Á **Allar frestunaráætlanir** lista, veldu frestunaráætlun og veldu síðan **Haltu \> Fjarlægðu bið**.
2. Í **Nafn dagbókar** reit, veldu nafn dagbókar.
3. Í **Dagsetning viðskipta** reit, tilgreinið viðskiptadagsetningu.
4. Veldu **Í lagi**.

## <a name="cancel-unrecognized-amounts"></a>Hætta við óskráðar upphæðir

> [!NOTE]
> Allar línur sem þegar hafa verið viðurkenndar eða birtar að utan eru útilokaðar frá þessu ferli.

Til að hætta við óþekktar upphæðir á frestunaráætlun, fylgdu þessum skrefum.

1. Á **Allar frestunaráætlanir** síðu, veldu frestunaráætlunina og veldu síðan **Hætta við \> Óþekktar upphæðir**.
2. Á **Hætta við óviðurkennda upphæð** síðu, veldu hvort þú vilt búa til afpöntunarfærslur.
3. Ef þú valdir að búa til afpöntunarfærslur skaltu velja færslubókarheitið í **Nafn dagbókar** reit skaltu velja afpöntunarreikninginn í **Afpöntunarreikningur** reitnum og tilgreindu viðskiptadagsetninguna í **Dagsetning viðskipta** sviði.
4. Veldu **Í lagi**.

## <a name="cancel-a-completed-schedule"></a>Hætta við lokið dagskrá

Nota **Allar frestunaráætlanir** síðu til að bakfæra allar viðurkenndar eða utanaðkomandi upphæðir og hætta við frestunaráætlunina til að koma í veg fyrir frekari viðurkenningu.

Fylgdu þessum skrefum til að hætta við heila frestunaráætlun.

1. Á **Allar frestunaráætlanir** síðu, veldu frestunaráætlunina og veldu síðan **Hætta við \> Heill dagskrá**.
2. Á **Hætta við heildaráætlun** síðu, veldu hvort þú vilt búa til afpöntunarfærslur.
3. Ef þú valdir að búa til afpöntunarfærslur skaltu velja færslubókarheitið í **Nafn dagbókar** reit, veldu reikninginn í **Afpöntunarreikningur** reitnum og tilgreindu viðskiptadagsetninguna í **Dagsetning viðskipta** sviði.
4. Veldu **Í lagi**.

## <a name="reverse-transactions"></a>Bakfæra færslur

> [!NOTE]
> - Til að snúa við tekjufærslu fyrir eina frestunaráætlun, byrjaðu á skrefi 1.
> - Til að snúa við tekjufærslu fyrir margar áætlanir, byrjaðu á skrefi 2.

1. Á **Allar frestunaráætlanir** síðu, í **Dagskrárlínur** hnitanet, veldu línurnar sem þú vilt ekki þekkja og veldu síðan **Öfugt**.
2. Á **Viðurkenningarvinnsla** síðu, stilltu **Viðurkenningaraðgerð** sviði til **Öfugt viðurkenningardagbók**.
3. Í **Lokadagur** reit, veldu lokadagsetningu. Vinnslan mun aðeins innihalda línur þar sem lokadagsetningin er fyrr en eða sú sama og tilgreindur lokadagsetning.
4. Veldu **Sía**, og bættu við gagnasíum þannig að listinn sýni aðeins svið skráa sem þú vilt.
5. Veldu **Skoða forskoðun** til að skoða línurnar.
6. Í listanum yfir línur velurðu allar línur sem þú vilt ekki vinna úr og veldu síðan **Fjarlægja**.
7. The **Nafn** og **Lýsing** reitirnir eru sjálfkrafa uppfærðir með sjálfgefnu dagbókarheiti og lýsingu. Þú getur breytt gildunum eftir þörfum. Þú getur líka valið hvort þú vilt taka saman viðurkenningarbókarfærsluna.
8. Í **Dagsetning viðskipta** kafla er hægt að hnekkja færsludagsetningu með tiltekinni dagsetningu til að vinna úr færslunni. Hægt er að tilgreina viðskiptadagsetningu fyrir lokuð tímabil.
9. Til að gera vinnsluna sem hluta af lotu skaltu velja **Hópur**. Í **Lotuvinnsla** valmynd, stilltu færibreytur fyrir rununa og veldu síðan **Allt í lagi** að fara aftur til **Viðurkenningarvinnsla** síðu. Öfug tekjufærsla verður afgreidd síðar, þegar lotan er afgreidd.
10. Veldu **Í lagi**. Ef þú bættir færslunni ekki við runu eru allar línur unnar strax. Að öðrum kosti verða línurnar unnar þegar lotan er unnin.

## <a name="apply-or-unapply-a-credit-note"></a>Sækja um eða afskrá inneignarnótu

Til að nota inneignarnótu skaltu fylgja þessum skrefum.

> [!NOTE]
> Þegar þú býrð til inneignarnótu frá **Frestun sölupöntunarfærslu** síðu og stilltu **Stilltu núverandi áætlun** valmöguleika til **Já**, er kreditnótan sjálfkrafa sett á áætlunina þegar kreditnótan er bókuð.

1. Á **Allar frestunaráætlanir** síðu, veldu frestunaráætlun.
2. Í **Lánsfjárleiðréttingar** lista, veldu línu og veldu síðan **Sækja um**.
3. Á **Sækja um inneignarnótu (frestun)** síðu, tilgreinið endurútreikningsdaginn í **Endurútreikningsdagur** reit og lokadagsetning í **Loka dagsetning** sviði.
4. Í **Fyrirsögn** lista, veldu **Sölupöntun** sem er með inneignarnótum.
5. Í **Línur** lista, veldu línuna.
6. Veldu **Í lagi**.
7. Velja skal **Já**.

> [!NOTE]
> Til að setja kreditnótu á nokkra einstaka hluti af mismunandi reikningum verður að endurtaka þessi skref.

Fylgdu þessum skrefum til að ógilda inneignarnótu.

1. Á **Allar frestunaráætlanir** síðu, veldu frestunaráætlun.
2. Í **Lánsfjárleiðréttingar** lista, veldu reikninginn og veldu síðan **Afnota**.
3. Velja skal **Já**.

## <a name="fields"></a>Svæði

The **Allar frestunaráætlanir** síða inniheldur eftirfarandi reiti.

| Svæði | Lýsing |
|--------|-------------|
| **Haus** | |
| **Tímasetja** | |
| Úthlutunargerð | Úthlutunartegund, fyrir frestun sem byggir á viðburðum: **Hlutfall** eða **Magn**. |
| Dagsetning endurflokkunar | <p>Nýjasta dagsetning þegar skammtímaendurflokkun vegna frestunaráætlunar var afgreidd. Þessi dagsetning er uppfærð í hvert skipti sem **Skammtímaendurflokkun viðburða** er notað fyrir frestunaráætlun.</p>Þessi reitur er aðeins tiltækur þegar reglubundin tímabil eða skammtímafrestun á fasta ári er notuð. |
| **Lykill** | |
| Lykill frestunar | Reikningurinn sem er notaður fyrir frestunarupphæðina. |
| Skráningarlykill | Reikningurinn sem er notaður fyrir viðurkenningarupphæðina. |
| Gerð skráningar | Viðurkenningartegundin. |
| Dreifingargerð | Dreifingartegundin. |
| **Færsla** | |
| Uppruni stofnunar | Uppruninn sem viðskiptin voru stofnuð frá. |
| Færslugerð | Færslutegundin. |
| Sölupöntun | Sölupöntunarnúmerið. |
| Reikningur | Reikningsnúmerið. |
| Atriði | Vörunúmerið. |
| **Greiðsluáætlun** | |
| Númer greiðsluáætlunar | Númer samsvarandi innheimtuáætlunar. |
| Staða reikningsfærslulínu | Staða samsvarandi greiðsluáætlunarlínu. |
| Ytri tilvísanir | Upplýsingar um ytri tilvísanir úr innheimtuáætlun: **Ytri** og **Línunúmer**. |
| Samtala | <p>Heildarupphæðir fyrir frestunaráætlun:</p><ul><li>**Langtíma** – Samtala langtíma frestaðra fjárhæða. Þetta gildi er aðeins tiltækt þegar **Skammtíma frestun aðferð** reiturinn er stilltur á **Enginn** á **Færslur tekna og gjalda frestun** síðu, eða skammtímaupphæðin er meira en 0 (núll).</li><li>**Skammtíma** – Samtala skammtíma frestaðra fjárhæða. Þetta gildi er aðeins tiltækt þegar **Skammtíma frestun aðferð** reiturinn er stilltur á **Enginn** á **Færslur tekna og gjalda frestun** síðu, eða skammtímaupphæðin er meira en 0 (núll).</li><li>**Óþekkt** – Summa ófærðra upphæða fyrir allar línur.</li><li>**Stubbaður** – Samtala utanbókaðra upphæða fyrir allar línur.</li><li>**Viðurkennd** – Summa viðurkenndra fjárhæða fyrir allar línur.</li><li>**Að utan og viðurkennd** – Samtala utanaðkomandi bókaða og færðra upphæða fyrir allar línur.</li><li>**Heildarupphæð** – Summa upphæða fyrir allar línur.</li></ul> |
| **Áætlunarlínur** | |
| Lína | Línuraðarnúmerið. |
| Upphafsdagsetning frestunar | Upphafsdagur frestunaráætlunar. |
| Lokadagsetning frestunar | Lokadagur frestunaráætlunar. |
| Upphæð | Frestunarfjárhæðin. |
| Birt að utan | Gildi sem gefur til kynna hvort línan hafi verið bókuð að utan. |
| Skráð | Gildi sem gefur til kynna hvort línan hafi verið þekkt. |
| Rununúmer færslubókar | Lotunúmerið sem magnið var skráð í. |
| Atburðalýsing | Lýsing á atburðinum. Þessi reitur er aðeins tiltækur fyrir frestunaráætlanir sem byggja á viðburðum. |
| **Kreditleiðréttingar** | |
| Reikningur | <p>Reikningsnúmerið.</p><p>Gildið gefur til kynna reikninginn fyrir leiðréttingu kreditnótu sem þegar hefur verið beitt á frestunaráætlun.</p> |
| Upphæð sem notuð er | Fjárhæð lánaleiðréttingar sem þegar hefur verið notuð á frestunaráætlun. |
| Dagsetning skráningar | Dagsetningin þegar lánaleiðréttingunni var beitt. |
| **Leiðrétting** | Leiðréttingargildin birtast aðeins ef unnið var úr kreditreikningi fyrir frestunaráætlunina. Ef engin inneignarnóta var unnin eru þessi gildi falin. |
| Leiðréttingarupphæð | Heildarleiðréttingarfjárhæð, reiknuð sem *Upprunaleg upphæð* –*Áætlunarupphæð*. |
| Upprunaleg lokadagsetning | Upprunaleg lokadagsetning frestunaráætlunar. |
| Upphafleg áætlunarupphæð | Heildarupphæð upphaflegrar frestunaráætlunar. |

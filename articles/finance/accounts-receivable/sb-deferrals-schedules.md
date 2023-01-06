---
title: Frestunaráætlanir í tekju- og kostnaðarfrestunum
description: Þessi grein lýsir frestunaráætlunum í tekju- og kostnaðarfrestunum.
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
ms.openlocfilehash: 093005f9b66d7ce741689b55612f006fa5123910
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903364"
---
# <a name="deferral-schedules"></a>Frestunaráætlanir

Frestunaráætlanir eru búnar til eftir að færsla hefur verið bókuð.

Hægt er að nota síðuna **Allar frestunaráætlanir** eða **Virkar frestunaráætlanir** til að fara yfir upplýsingarnar um frestunaráætlun. Upplýsingarnar sem koma fram fara eftir gerð frestunaráætlunar (línuleg eða tengd tilviki) og færslugerðinni. Þar eru línur fyrir frestunaráætlunarlínur og heildarupphæðir fyrir frestunaráætlunina. Hægt er að nota síðuna til að breyta frestunaráætlun.

## <a name="recognize-revenue"></a>Skrá tekjur

> [!NOTE]
> - Til að skrá tekjur fyrir eina frestunaráætlun skaltu byrja á skrefi 1.
> - Til að skrá tekjur fyrir margar áætlanir skaltu byrja á skrefi 2.

1. Á síðunni **Allar frestunaráætlanir**, í hnitanetinu **Áætlunarlínur**, skal velja línurnar sem á að skrá og síðan velja **Skrá**.
2. Á síðunni **Úrvinnsla skráningar** skal stilla reitinn **Skráningaraðgerð** á **Búa til skráningarbók**.
3. Í svæðinu **Lokadagsetning** skal velja lokadagsetninguna. Vinnslan mun aðeins innihalda línur þar sem lokadagsetning er á undan eða sú sama og valinn lokadagur.
4. Veldu **Sía** og bættu við gagnasíum þannig að listinn sýnir aðeins færslubilið sem þú vilt.
5. Veldu **Skoða forskoðun** til að skoða línurnar.
6. Á línulistanum velur þú allar línur sem þú vilt ekki vinna úr og velur svo **Fjarlægja**.
7. Veljið hvort taka á saman færslu í skráningarbókinni.
8. Í hlutanum **Færsludagsetning** er hægt að hnekkja færsludagsetningunni með tiltekinni dagsetningu til að vinna úr færslunni. Hægt er að tilgreina færsludagsetningu fyrir lokuð tímabil.
9. Ef vinnslan á að vera hluti af runu skal velja **Runa**. Í svarglugganum **Runuvinnsla** skal stilla færibreyturnar fyrir rununa og síðan velja **Í lagi** til að fara aftur á síðuna **Úrvinnsla skráningar**. Tekjuskráningin verður unnin síðar, þegar runan er unnin.
10. Veljið **Ferli**. Ef færslunni var ekki bætt við í runu eru allar línur meðhöndlaðar samstundis. Annars verða línurnar unnar þegar seinni runan er unnin.

## <a name="modify-a-schedule"></a>Breyta áætlun

Til að breyta frestunaráætlun skal fylgja þessum skrefum.

1. Á síðunni **Allar frestunaráætlanir** skal velja frestunaráætlun og síðan velja **Bókhald \> Breyta áætlun**.
2. Á síðunni **Breyta áætlun** skal breyta þeim valkostum sem á að breyta. Ekki er hægt að breyta öllum valkostunum en það fer eftir frestunaráætluninni.
3. Veldu **Forskoðun** til að skoða breytingar á frestunaráætluninni.
4. Veldu **Í lagi**.

### <a name="straight-line-deferral-schedules"></a>Frestunaráætlanir beinnar línu

Ef frestunaráætlunin er ekki með neinar skráðar eða ytri bókaðar línur er hægt að breyta allri frestunaráætluninni, þ.m.t. upphafsdagsetningunni.

Ef frestunaráætlunin er með skráðar eða ytri bókaðar línur og frestunaráætluninni er breytt fer hegðun frestunaráætlunarinnar eftir dagsetningu endurútreiknings og lokadagsetningu skráðra lína fyrir frestunina. Fyrsta tímabilið sem var ekki fært ákvarðar lokadag frestunar.

Til að nota dagsetningu skráningar er hægt að velja eitt af eftirfarandi gildum í reitnum **Upphaf áætlunar**: 
- **Vinna upp** – Upphæðin eftir að allar skráðar línur hafa verið endurreiknaðar.
- **Bakfærsla** – Allar línur eftir dagsetningu endurútreiknings eru bakfærðar með því að nota tilgreint færslubókarheiti og færslubókardag. Upphæðin eftir endurútreikningsdag er síðan endurreiknuð.

Ef sniðmát er notað er slepptu tímabilin hunsuð og sniðmátið er aðeins notað til að reikna út lokadagsetninguna.

### <a name="event-based-deferral-schedules"></a>Frestunaráætlanir sem byggja á viðburðum

Fyrir frestunaráætlun sem byggð er á viðburði er hægt að breyta öllum óskráðum línum.

Ef frestunaráætlunin er með skráðar eða ytri bókaðar línur er ekki hægt að breyta sniðmátinu og úthlutunargerðinni fyrir frestunaráætlunina. Þegar fyrirliggjandi frestunaráætlun er breytt er ekki hægt að breyta gildinu í reitnum **Búa til aðskilin tilvik á hverja einingu**.

Ef lína er skráð eða birt utanaðkomandi er gátreiturinn **Skráð** valinn.

## <a name="modify-a-deferral-or-recognition-account"></a>Breyta frestunarlykli eða skráningarlykli

Til að breyta frestunar- eða skráningarlykli fyrir frestunaráætlun skal fylgja þessum skrefum.

1. Á síðunni **Allar frestunaráætlanir** skal velja frestunaráætlun og síðan velja **Bókhald \> Breyta lykli**.
2. Á síðunni **Breyta lykli** skal velja lykilinn sem á að breyta (frestun, skammtíma eða skráning).
3. Í reitnum **Nýr reikningur** skal velja nýjan reikning.
4. Veldu hvort breytingar á lyklinum stofni færslur í leiðréttingabók.
5. Ef valkosturinn er stilltur á **Já** í fyrra skrefinu skal velja færslubókarheitið í reitnum **Heiti færslubókar** og tilgreina færsludagsetninguna í reitnum **Færsludagsetning**.
6. Veldu **Í lagi**.

## <a name="put-a-deferral-schedule-on-hold"></a>Setja frestunaráætlun í bið

Til að setja frestunaráætlun í bið skal fylgja þessum skrefum.

1. Á síðunni **Allar frestunaráætlanir** skal velja frestunaráætlun og síðan velja **Bið \> Setja í bið**.
2. Á síðunni **Setja í bið** skal velja hvort eigi að flytja stöðuna af frestunarlykli eða biðlykli.
3. Ef þú valdir að flytja stöðuna skal velja heiti færslubókar í reitnum **Heiti færslubókar**, velja biðlykilinn í reitnum **Biðlykill** og tilgreina færsludagsetninguna í reitnum **Færsludagsetning**.
4. Veldu **Í lagi**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Fjarlægja bið af frestunaráætlun

Til að fjarlægja frestunaráætlun úr bið skal fylgja þessum skrefum.

1. Í listanum **Allar frestunaráætlanir** skal velja frestunaráætlun og síðan velja **Bið \> Fjarlægja bið**.
2. Í reitnum **Heiti færslubókar** skal velja færslubókarheitið.
3. Tilgreinið færsludagsetning í reitnum **Dagsetning færslu**.
4. Veldu **Í lagi**.

## <a name="cancel-unrecognized-amounts"></a>Hætta við óskráðar upphæðir

> [!NOTE]
> Allar línur sem þegar hafa verið skráðar eða bókaðar ytra eru útilokaðar frá þessu ferli.

Til að afturkalla óskráðar upphæðir á frestunaráætlun skal fylgja þessum skrefum.

1. Á síðunni **Allar frestunaráætlanir** skal velja frestunaráætlun og síðan velja **Hætta við \> Óskráðar upphæðir**.
2. Á síðunni **Hætta við óskráða upphæð** er valið hvort búa eigi til afbókunarfærslur.
3. Ef þú valdir að búa til afturköllunarfærslur skaltu velja heiti færslubókar í reitnum **Heiti færslubókar**, velja afturköllunarlykilinn í reitnum **Afturköllunarlykill** og tilgreina færsludagsetninguna í reitnum **Færsludagsetning**.
4. Veldu **Í lagi**.

## <a name="cancel-a-completed-schedule"></a>Hætta við fullkláraða áætlun

Notaðu síðuna **Allar frestunaráætlanir** til að bakfæra skráðar eða ytri bókaðar upphæðir og hætta við frestunaráætlun til að koma í veg fyrir frekari skráningu.

Til að hætta við alla frestunaráætlunina skal fylgja þessum skrefum.

1. Á síðunni **Allar frestunaráætlanir** skal velja frestunaráætlun og síðan velja **Hætta við \> Ljúka áætlun**.
2. Á síðunni **Hætta við að ljúka áætlun** er valið hvort búa eigi til afturköllunarfærslur.
3. Ef þú valdir að búa til afturköllunarfærslur skaltu velja heiti færslubókar í reitnum **Heiti færslubókar**, velja lykilinn í reitnum **Afturköllunarlykill** og tilgreina færsludagsetninguna í reitnum **Færsludagsetning**.
4. Veldu **Í lagi**.

## <a name="reverse-transactions"></a>Bakfæra færslur

> [!NOTE]
> - Til að bakfæra tekjuskráningu fyrir eina frestunaráætlun skaltu byrja á skrefi 1.
> - Til að bakfæra tekjuskráningu fyrir margar áætlanir skal byrja á skrefi 2.

1. Á síðunni **Allar frestunaráætlanir**, í hnitanetinu **Áætlunarlínur**, skal velja línurnar sem á að afskrá og síðan velja **Bakfæra**.
2. Á síðunni **Úrvinnsla skráningar** skal stilla reitinn **Skráningaraðgerð** á **Bakfæra skráningarbók**.
3. Í svæðinu **Lokadagsetning** skal velja lokadagsetninguna. Vinnslan mun aðeins innihalda línur þar sem lokadagsetning er á undan eða sú sama og tiltekinn lokadagur.
4. Veldu **Sía** og bættu við gagnasíum þannig að listinn sýnir aðeins færslubilið sem þú vilt.
5. Veldu **Skoða forskoðun** til að skoða línurnar.
6. Á línulistanum velur þú allar línur sem þú vilt ekki vinna úr og velur svo **Fjarlægja**.
7. Reitirnir **Heiti** og **Lýsing** eru sjálfkrafa uppfærðir með sjálfgefnu heiti færslubókar og lýsingu. Hægt að breyta gildinu eins og nauðsynlegt er. Einnig er hægt að velja hvort taka eigi saman skráningarbókarfærslu.
8. Í hlutanum **Færsludagsetning** er hægt að hnekkja færsludagsetningunni með tiltekinni dagsetningu til að vinna úr færslunni. Hægt er að tilgreina færsludagsetningu fyrir lokuð tímabil.
9. Ef vinnslan á að vera hluti af runu skal velja **Runa**. Í svarglugganum **Runuvinnsla** skal stilla færibreyturnar fyrir rununa og síðan velja **Í lagi** til að fara aftur á síðuna **Úrvinnsla skráningar**. Bakfærða tekjuskráningin verður unnin síðar, þegar runan er unnin.
10. Veldu **Í lagi**. Ef færslunni var ekki bætt við í runu eru allar línur meðhöndlaðar samstundis. Annars verða línurnar unnar þegar seinni runan er unnin.

## <a name="apply-or-unapply-a-credit-note"></a>Jafna eða ógilda jöfnun kreditnótu

Til að jafna kreditnótu skal fylgja eftirfarandi skrefum.

> [!NOTE]
> Þegar kreditnóta er stofnuð á síðunni **Frestun sölupöntunarfærslu** og valkosturinn **Breyta fyrirliggjandi áætlun** er stilltur á **Já** er kreditnótan sjálfkrafa notuð í áætluninni þegar kreditnótan er bókuð.

1. Á síðunni **Allar frestunaráætlanir** skal velja frestunaráætlun.
2. Á listanum **Kreditleiðréttingar** skal velja línu og síðan **Nota**.
3. Á síðunni **Nota kreditnóta (frestanir)** skal tilgreina dagsetningu endurútreiknings í reitnum **Dagsetning endurútreiknings** og lokadagsetninguna í reitnum **Lokadagsetning**.
4. Í listanum **Haus** skal velja **Sölupöntun** sem er með kreditnótur.
5. Í listanum **Línur** skal velja línuna.
6. Veldu **Í lagi**.
7. Velja skal **Já**.

> [!NOTE]
> Til að nota kreditnótu á nokkrar einstaka vörur úr mismunandi reikningum þarf að endurtaka þessi skref.

Til að ógilda jöfnun kreditnótu skal fylgja eftirfarandi skrefum.

1. Á síðunni **Allar frestunaráætlanir** skal velja frestunaráætlun.
2. Veljið reikninginn á listanum **Kreditleiðréttingar** og veljið svo **Ógilda jöfnun**.
3. Velja skal **Já**.

## <a name="fields"></a>Svæði

Síðan **Allar frestunaráætlanir** inniheldur eftirfarandi reiti.

| Svæði | Lýsing |
|--------|-------------|
| **Haus** | |
| **Tímasetja** | |
| Úthlutunargerð | Tegund úthlutunar, fyrir frestanir sem byggja á viðburðum: **Prósenta** eða **Upphæð**. |
| Dagsetning endurflokkunar | <p>Nýjasta dagsetningin þegar skammtíma endurflokkun fyrir frestunaráætlun var afgreidd. Þessi dagsetning er uppfærð í hvert sinn sem **Skammtíma endurflokkun tilviks** er notað fyrir frestunaráætlunina.</p>Þessi reitur er aðeins í boði þegar skammtíma frestunaraðferð fyrir hlaupandi tímabil eða fast er er notuð. |
| **Lykill** | |
| Lykill frestunar | Lykillinn sem er notaður fyrir frestunarupphæðina. |
| Skráningarlykill | Lykillinn sem er notaður fyrir skráningarupphæðina. |
| Gerð skráningar | Skráningargerðin. |
| Dreifingargerð | Dreifingargerðin. |
| **Færsla** | |
| Uppruni stofnunar | Uppruninn sem færslan var stofnuð úr. |
| Færslugerð | Færslugerðin. |
| Sölupöntun | Sölupöntunarnúmerið. |
| Reikningur | Reikningsnúmer. |
| Atriði | Vörunúmerið. |
| **Greiðsluáætlun** | |
| Númer greiðsluáætlunar | Númer samsvarandi greiðsluáætlunar. |
| Staða reikningsfærslulínu | Staða samsvarandi vöru á greiðsluáætlunarlínu. |
| Ytri tilvísanir | Upplýsingar um ytri tilvísanir úr greiðsluáætluninni: **Ytri** og **Línunúmer**. |
| Samtala | <p>Samtölur upphæða fyrir frestunaráætlun:</p><ul><li>**Langtíma** – Summa upphæða sem frestað er til langs tíma. Þetta gildi er aðeins í boði þegar reiturinn **Skammtíma frestunaraðferð** er stilltur á **Ekkert** á síðunni **Færibreytur tekju- og kostnaðarfrestana** eða skammtímaupphæðin er hærri en 0 (núll).</li><li>**Skammtíma** – Summa upphæða sem frestað er til skamms tíma. Þetta gildi er aðeins í boði þegar reiturinn **Skammtíma frestunaraðferð** er stilltur á **Ekkert** á síðunni **Færibreytur tekju- og kostnaðarfrestana** eða skammtímaupphæðin er hærri en 0 (núll).</li><li>**Óskráð** – Summa óskráðra upphæða fyrir allar línur.</li><li>**Stytt** – Summa upphæða með ytri bókun fyrir allar línur.</li><li>**Viðurkennt** – Summa skráðra upphæða fyrir allar línur.</li><li>**Ytri bókun og skráning** – Summa skráðra upphæða með ytri bókun og skráningu fyrir allar línur.</li><li>**Heildarupphæð** – summa upphæða fyrir allar línur.</li></ul> |
| **Áætlunarlínur** | |
| Lína | Raðnúmer línunnar. |
| Upphafsdagsetning frestunar | Upphafsdagsetning frestunaráætlunar. |
| Lokadagsetning frestunar | Lokadagsetning frestunaráætlunarinnar. |
| Upphæð | Frestunarupphæðin. |
| Ytri bókun | Gildi sem segir til um hvort línan hefur verið bókuð ytra. |
| Skráð | Gildi sem segir til um hvort línan hefur verið skráð. |
| Rununúmer færslubókar | Rununúmerið sem upphæðin var skráð í. |
| Lýsing tilviks | Lýsing á tilvikinu. Þetta svæði er aðeins tiltækt fyrir frestunaráætlanir sem byggjast á viðburðum. |
| **Kreditleiðréttingar** | |
| Reikningur | <p>Reikningsnúmer.</p><p>Gildið segir til um reikninginn fyrir leiðréttingu kreditnótu sem hefur þegar verið notuð í frestunaráætluninni.</p> |
| Upphæð sem notuð er | Kreditleiðréttingarupphæðin sem þegar hefur verið notuð á frestunaráætlunina. |
| Dagsetning skráningar | Dagsetningin þegar kreditleiðréttingin var notuð. |
| **Leiðrétting** | Leiðréttingargildin birtast aðeins ef kreditreikningur var unninn fyrir frestunaráætlunina. Ef engin kreditnóta var unnin eru þessi gildi falin. |
| Leiðréttingarupphæð | Heildarleiðréttingarupphæðin, reiknuð sem *Upprunaleg upphæð* – *Áætlunarupphæð*. |
| Upphaflegur lokadagur | Upphafleg lokadagsetning frestunaráætlunar. |
| Upphafleg áætlunarupphæð | Heild upphaflegrar frestunaráætlunar. |

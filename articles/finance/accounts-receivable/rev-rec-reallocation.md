---
title: Endurúthlutun tekjuskráningar
description: Í þessu efnisatriði er að finna upplýsingar um endurúthlutun sem gerir fyrirtækjum kleift að endurreikna tekjuupphæðir þegar skilmálum samningsbundinnar sölu er breytt. Þar er að finna tengla á önnur efnisatriði sem útskýra hvernig á að skrá tekjur í ýmsum aðstæðum.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 37c3da576b79d3ae9f6983b5046343a7c8120de6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356126"
---
# <a name="revenue-recognition-reallocation"></a>Endurúthlutun tekjuskráningar

[!include [banner](../includes/banner.md)]

Endurúthlutun gerir fyrirtækjum kleift að endurreikna tekjuupphæðir þegar skilmálum samningsbundinnar sölu er breytt. Þar sem tekjuskráningin er til hliðsjónar verður litið á skjöl sölupöntunar sem samninginn.

Fyrirtækið verður að ákveða hvort endurúthlutun sé nauðsynleg. Viðbót nýrrar línu í sölupöntun, eða viðbót nýrrar sölupöntunar fyrir viðskiptavin, endurspeglar ekki endilega breytingu á samningnum. Eftirfarandi aðstæður gætu þurft endurúthlutun:

- Viðskiptavinur bætti vörum við sölupöntun, eða fjarlægði vörur úr sölupöntuninni, eftir að pöntunin var reikningsfærð að fullu eða að hluta.
- Margar sölupantanir, með annaðhvort staðfesta stöðu eða reikningsfærða stöðu, voru færðar inn fyrir sama umsamda samninginn.
- Viðskiptavinur skilaði eða fékk kredit fyrir vöru eftir að upprunalega sölupöntunin var reikningsfærð að fullu eða að hluta.

Nokkrar mikilvægar takmarkanir eru á endurúthlutunarferlinu:

- Aðeins er hægt að keyra ferlið einu sinni. Því er mikilvægt að keyra það eingöngu eftir að öllum breytingum er lokið.
- Ekki er hægt að keyra ferlið í sölupöntunum verks.
- Ef margar sölupantanir koma við sögu, verða þær að vera fyrir sama viðskiptavinalykilinn.
- Allar endurúthlutaðar sölupantanir verða að vera í sama færslugjaldmiðlinum.
- Ekki er hægt að bakfæra eða afturkalla ferlið þegar búið er að keyra það.

## <a name="set-up-reallocation"></a>Uppsetning endurúthlutunar

Ein færibreyta hefur áhrif á endurúthlutunarferlið.

Vegna þess að hægt er að endurúthluta sölupöntun sem er reikningsfærð að hluta til eða í heild sinni, verður að leiðrétta allar fyrri bókhaldsfærslur fyrir reikninginn með því að nota nýju endurúthlutuðu tekjuupphæðirnar. Leiðréttingin er gerð með því að bakfæra upprunalega bókhaldsfærslu reikningsins og bóka nýja bókhaldsfærslu sem byggir á endurúthlutuðum tekjuupphæðum.

Hvert fyrirtæki fyrir sig verður að ákveða hvort leiðréttingin eigi að uppfæra fjárhag eða hvort hún eigi einnig að uppfæra viðskiptakröfur. Ákvörðunin sem er tekin ákvarðar viðeigandi stillingu á valkostinum **Bóka leiðréttingar reiknings á viðskiptakröfur** í flipanum **Tekjuskráning** á síðunni **Fjárhagsfæribreytur** (**Tekjuskráning \> Uppsetning \> Fjárhagsfæribreytur**). Viðeigandi stilling veltur á tilteknum aðstæðum. Fyrir frekari upplýsingar um mögulegar aðstæður skal nota tenglana í hlutanum [Aðstæður endurúthlutunar](#scenarios-for-reallocation) síðar í þessu efnisatriði.

[![Tekjuskráningarflipi á síðunni Fjárhagsfæribreytur.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Ef valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** er stilltur á **Já** verður niðurstaða endurúthlutunarferlisins eftirfarandi:

- Kreditskjal er stofnað í viðskiptakröfum til að bakfæra reikning sem þarfnast leiðréttingar.

    - Kreditskjalið endurnotar upprunalega reikningsnúmerið, en „-1“ er bætt við.
    - Kreditskjalið er sjálfkrafa jafnað á móti upprunalegum innkaupareikningi. Ef búið var að jafna upprunalegan reikning við annað kreditskjal eða greiðslu verður jöfnunin sjálfkrafa bakfærð.
    - Kreditskjalið er bókað í fjárhag til að bakfæra bókhaldsfærsluna sem var bókuð í upprunalegum reikningi. Hins vegar eru birgða- og kostnaðarfærslur seldra vara ekki bakfærðar.

- Nýr reikningur sem er byggður á nýjum endurúthlutuðum verðupphæðum er stofnaður í Viðskiptakröfur.

    - Nýi reikningurinn endurnotar upprunalega reikningsnúmerið, en „-2“ er bætt við.
    - Nýi reikningurinn er sjálfkrafa jafnaður á móti kreditskjali eða greiðslum sem voru áður jafnaðar við upprunalegan reikning.
    - Nýi reikningurinn er bókaður í fjárhag með því að nota nýju, endurúthlutuðu tekjuupphæðirnar. Hann er ekki bókaður aftur í birgða- og kostnaðarreikningum seldra vara vegna þess að þeim færslum er haldið í bókhaldsfærslu upprunalegs reiknings.

Ef valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** er stilltur á **Nei** verður niðurstaða endurúthlutunarferlisins eftirfarandi:

- Bakfærsla bókhaldsfærslu er aðeins bókuð í fjárhag. Allt bókhaldið frá upprunalegum reikningi er bakfært fyrir utan lykilfærslur birgða- og kostnaðarreiknings seldra vara.
- Ný bókhaldsfærsla er aðeins bókuð í fjárhag samkvæmt nýju, endurúthlutuðum tekjuupphæðum. Hann er ekki bókaður aftur í birgða- og kostnaðarreikningum seldra vara vegna þess að þeim færslum er haldið í bókhaldsfærslu upprunalegs reiknings.
- Reikningurinn á síðunni **Færslur viðskiptavinar** breytist ekki heldur endurspeglar ennþá upprunalegu bókhaldsfærsluna. Engin tilvísun er í bakfærðu eða nýju bókhaldsfærslurnar.

Eins og hefur verið minnst á er hægt að uppfæra fjárhag eingöngu, eða uppfæra bæði fjárhag og viðskiptakröfur. Báðar leiðirnar hafa sína kosti og galla. Mælt er með að þú metir kröfur fyrirtækisins til að finna út hvorn valkostinn eigi að nota. Ef þú uppfærir bæði fjárhag og viðskiptakröfur verða réttar bókhaldsfærslur sýndar í nýja reikningnum og hægt verður að skoða þær í skjalinu á síðunni **Færslur viðskiptavinar**. Auk þess notar jöfnunarferlið uppfærðar bókhaldsfærslur til að bóka allan staðgreiðsluafslátt og hagnað og tap. Á hinn bóginn munu kreditskjalið og nýi reikningurinn birtast á yfirlitum viðskiptavinar og aldursgreiningarskýrslum, rétt eins og önnur kreditskjöl og reikningar viðskiptavina gera. Lýsingin á þeim skjölum mun sýna að þau voru stofnuð í gegnum bókhaldsleiðréttingu.

## <a name="run-the-reallocation-process"></a>Keyra endurúthlutunarferli

Til að hefja endurúthlutunarferlið skal velja **Endurúthluta verði með nýjum pöntunarlínum** í einhverri sölupöntun sem þarf að endurúthluta. Einnig er hægt að fara í **Tekjuskráning \> Reglubundin verk \> Endurúthluta verði með nýjum pöntunarlínum** og síðan færa inn viðeigandi síur eins og viðskiptavinalykilinn.

[![Endurúthluta verði með nýrri síðu pöntunarlína.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Efra hnitanetið á síðunni **Endurúthluta verði með nýjum pöntunarlínum** heitir **Sala**. Þar er að finna sölupantanir fyrir viðskiptavinina. Velja skal sölupantanirnar sem þarf að endurúthluta. Ekki er hægt að velja sölupantanir verks vegna þess að ekki er hægt að endurúthluta þeim. Ekki er heldur hægt að velja sölupantanir sem eru þegar komnar með kenni endurúthlutunar þar sem aðeins má endurúthluta sölupöntunum sem tilheyra ekki verki einu sinni. Ef sölupöntun er með kenni endurúthlutunar hefur annar notandi þegar merkt hana til endurúthlutunar.

Neðra hnitanetið á síðunni kallast **Línur**. Þegar búið er að velja eina eða fleiri sölupantanir í hnitanetinu **Sala** sýnir hnitanetið **Línur** sölupöntunarlínurnar. Velja skal sölupöntunarlínurnar sem á að endurúthluta. Ef aðeins ein sölupöntun er valin verður að endurúthluta línum sömu sölupöntunarinnar. Þessi staða getur komið upp þegar ein af sölupöntunarlínunum var áður reikningsfærð og síðan var nýrri línu bætt við eða fyrirliggjandi lína var fjarlægð eða hætt við hana. Ef lína var fjarlægð birtist hún ekki í hnitanetinu. Þess vegna er ekki hægt að velja hana. Hins vegar verður hún samt tekin til greina þegar endurúthlutunarferlið er keyrt.

Eftir að lokið er við að velja nauðsynlegar sölupöntunarlínur skal nota hnappana á Aðgerðasvæði eins og lýst er hér:

- **Uppfæra endurúthlutun** – Reikna skal nýju tekjuupphæðina fyrir valdar sölupöntunarlínur. Ef lína var fjarlægð eða hætt var við hana verður endurúthlutun aðeins gerð fyrir núverandi línur sem voru valdar. Eftirfarandi mynd sýnir dæmi um sölupöntunarlínur áður en endurúthlutunin er uppfærð.

    [![Sölupöntunarlínur áður en endurúthlutun er uppfærð.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Nýju tekjuupphæðirnar eru sýndar í dálknum **Endurúthlutuð upphæð** í hnitanetinu **Línur**. Á þessu stigi hefur endurúthlutun verið unnin en ekki er búið að reikna hana út. Eftirfarandi mynd sýnir dæmi um sölupöntunarlínur þegar endurúthlutunin hefur verið uppfærð.

    [![Sölupöntunarlínur þegar endurúthlutun hefur verið uppfærð.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Vinna úr** – Vinna úr eða bóka endurúthlutaðar tekjuupphæðir. Þegar þessi hnappur hefur verið valinn er engin leið til að afturkalla endurúthlutun. Ef ekki var valið **Uppfæra endurúthlutun** áður en **Vinna úr** er valið, verður endurúthlutunin keyrð sjálfkrafa.

    - Ef engin sölupöntunarlína hefur verið reikningsfærð eru tekjuupphæðirnar uppfærðar á öllum sölupöntunum sem voru valdar fyrir endurúthlutun.
    - Ef ein eða fleiri sölupöntunarlínur hafa verið reikningsfærðar, verða leiðréttar bókhaldsfærslur bókaðar og upplýsingar um allar tekjuáætlanir sem voru stofnaðar fyrir reikningsfærða sölupöntunarlínu verða leiðréttar.

- **Væntanlegt fylgiskjal** – Sýnir forskoðun bókhaldsfærslna sem hafa verið stofnaðar fyrir allar sölupöntunarlínur sem hafa verið reikningsfærðar. Ef engar línur hafa verið reikningsfærðar verður ekkert sýnt. Ef ekki var valið **Uppfæra endurúthlutun** áður en **Væntanlegt fylgiskjal** er valið, verður endurúthlutunin keyrð sjálfkrafa.
- **Endurúthlutun tekna** – Opna síðu sem sýnir úthlutun tekjuupphæðar fyrir allar valdar línur. Ekki er hægt að breyta neinum upplýsingum á síðunni. Hún sýnir línuupphæðirnar sem voru notaðar til að gera endurúthlutunina.

    [![Línuupphæðir sem voru notaðar fyrir endurúthlutun.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Endurstilla gögn fyrir valinn viðskiptavin** – Ef endurúthlutunarferlið hófst en var ekki klárað skal aðeins hreinsa gögnin í endurúthlutunartöflunni fyrir valinn viðskiptavin. Til dæmis ef þú merkir margar sölupöntunarlínur til endurúthlutunar, skilur síðuna eftir opna án þess að velja **Vinna úr** og svo rennur síðan út á tíma. Þá haldast sölupöntunarlínurnar merktar og þær verða ekki aðgengilegar öðrum notanda til að ljúka endurúthlutunarferlinu. Síðan gæti jafnvel verið auð þegar hún er opnuð. Í þessum aðstæðum er hægt að nota hnappinn **Endurstilla gögn valins viðskiptavinar** til að hreinsa óunnar sölupantanir þannig að annar notandi geti lokið endurúthlutunarferlinu.

## <a name="scenarios-for-reallocation"></a>Aðstæður endurúthlutunar

Eftirfarandi efnisatriði fara í gegnum ýmsar aðstæður tekjuskráningar:

- [Endurúthlutun tekjuskráningar – Aðstæður 1](rev-rec-reallocation-scenario-1.md) – Tvær sölupantanir eru færðar inn, en þær eru eingöngu staðfestar. Sömu aðstæður leiða til svipaðrar niðurstöðu ef fleiri en tvær sölupantanir eru með staðfesta stöðu.
- [Endurúthlutun tekjuskráningar – Aðstæður 2](rev-rec-reallocation-scenario-2.md) – Tvær sölupantanir eru færðar inn og viðskiptavinurinn bætir atriði við samninginn eftir að fyrsta sölupöntunin er reikningsfærð.
- [Endurúthlutun tekjuskráningar – Aðstæður 3](rev-rec-reallocation-scenario-3.md) – Nýrri línu er bætt við núverandi reikningsfærða sölupöntun.
- [Endurúthlutun tekjuskráningar – Aðstæður 4](rev-rec-reallocation-scenario-4.md) – Lína er fjarlægð úr núverandi sölupöntun sem er reikningsfærð að hluta til.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
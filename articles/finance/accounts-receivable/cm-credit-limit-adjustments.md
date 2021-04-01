---
title: Leiðréttingar á lánamörkum
description: Þetta efni útskýrir hvernig á að setja upp og bæta við leiðréttingum á lánamörkum.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 31d83e2083806a518928dc2079c31fab6f95872c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254524"
---
# <a name="credit-limit-adjustments"></a>Leiðréttingar á lánamörkum 

[!include [banner](../includes/banner.md)]

Leiðréttingar á lánamörkum gera lánastjórnendum kleift að uppfæra lánamörk og gildistíma eins viðskiptavinar, hóps viðskiptavina eða allra viðskiptavina með bókunarferli. Þú getur bætt við færslum leiðréttingar á lánamörkum til að uppfæra viðskiptavini og lánshópa viðskiptavina, eða þú getur notað þær til að reikna út sjálfvirk lánamörk. Síðan er hægt að skoða færslurnar, senda þær til samþykktar í gegnum verkflæði og setja þær á reikninga viðskiptavina.

## <a name="set-up-credit-limit-adjustments"></a>Setja upp leiðréttingar á lánamörkum

Þú getur búið til færslur í leiðréttingabók fyrir lánamörk á síðunni **Leiðrétting lánamarka** (**Lánastjórnun \> Leiðréttingar á lánamörkum \> Leiðréttingar á lánamörkum**).

1. Veljið **Nýtt**. Nýr hópur færslna er búinn til með leiðréttingarnúmer lánamarka.
2. Veldu tegund leiðréttingar útlána:

    - Veldu **Lánamörk** til að breyta lánsheimild viðskiptavinarins.
    - Veldu **Tímabundin lánamörk** til að búa til tímabundið lánamörk í stað þess að breyta núverandi lánsfjárhámarki viðskiptavinarins. Tímabundin lánamörk fara yfir lánamörk viðskiptavinar um skilgreindan tíma. Eftir að tímabilinu lýkur er lánshæfi viðskiptavinarins notað aftur.
3. Færðu inn lýsingu. 

Ef gátreiturinn **Bókað** er valinn hefur lánamörkunum verið beitt. Reiturinn **Samþykkisstaða** sýnir stöðu verkflæðis færslubókarinnar. Verkflæði er valkvætt.

### <a name="add-credit-limit-adjustments"></a>Bæta við leiðréttingum á lánamörkum

Til að bæta við leiðréttingum á lánamörkum handvirkt velurðu **Línur** og fylgir síðan þessum skrefum.

1. Til að bæta við leiðréttingu á lánamörkum fyrir viðskiptavin notarðu valmyndina **Leiðréttingar viðskiptavina**. Til að bæta við lánamörkum fyrir lánsfjárhóp viðskiptavina velurðu **Leiðréttingar kredithóps viðskiptavina**.
2. Sláðu inn viðskiptavinareikning fyrir viðskiptavinalykil reiknings sem ætti að uppfæra með nýju lánsfjárhámarkinu. Ef þú valdir **Leiðréttingar kredithóps viðskiptavina** í skrefi 1, sláðu inn kredithóp viðskiptavina. Þú getur ekki slegið inn bæði viðskiptavinalykil og auðkenni viðskiptavinahóps á sömu dagbókarlínu.

    Núverandi lánamörk eru sýnd og nafnið birtist sjálfkrafa.

3. Sláðu inn nýja lánsfjárhæðina sem ætti að koma í stað núverandi lánsfjárhámarks þegar færslan um lánamörk er bókuð.
4. Sláðu inn dagsetningu til að skilgreina nýja lokadagsetningu fyrir lánsheimild viðskiptavina. Þú verður að slá inn gildistíma lánamarks þegar þú býrð til leiðréttingu á lánamörkum.

Reiturinn **Samþykkisstaða** sýnir stöðu verkflæðis færslubókarlínunnar.

Ef þú vilt að leiðréttingar á lánamörkum verði sjálfkrafa myndaðar, geturðu notað valmyndina **Mynda** í aðgerðarglugganum.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Bæta við tímabundnum leiðréttingum á lánamörkum

Til að bæta við tímabundnum leiðréttingum á lánamörkum handvirkt fylgirðu þessum skrefum fyrir færslubókarlínurnar.

1. Til að bæta við leiðréttingu á lánamörkum fyrir viðskiptavin notarðu valmyndina **Leiðréttingar viðskiptavina**. Til að bæta við lánamörkum fyrir lánsfjárhóp viðskiptavina velurðu **Leiðréttingar kredithóps viðskiptavina**.
2. Sláðu inn viðskiptavinareikning fyrir viðskiptavinalykil reiknings sem ætti að uppfæra með nýju lánsfjárhámarkinu. Ef þú valdir **Leiðréttingar kredithóps viðskiptavina** í skrefi 1, sláðu inn kredithóp viðskiptavina. Þú getur ekki slegið inn bæði viðskiptavinalykil og auðkenni viðskiptavinahóps á sömu dagbókarlínu.

    Ef virkt eða framtíðartímabundið lánsfjárhámark er fyrir hendi birtast núverandi tímabundna lánamörk og tímamörk fyrir hvert tímabundið lánamörk. Nafnið birtist sjálfkrafa.

3. Sláðu inn nýju kreditmörkin sem ætti að koma í stað núverandi lánsfjárhámarks.
4. Í reitunum **Nýtt frá dagsetningu** og **Nýtt til þessa** skilgreinirðu tímabilið þegar ítarleg lánamörk eru gild. Þú verður að slá inn gildistíma lánamarks þegar þú býrð til leiðréttingarbók lánamarka.

Reiturinn **Samþykkisstaða** sýnir stöðu verkflæðis færslubókarlínunnar.

## <a name="generate-credit-limit-adjustments"></a>Mynda leiðréttingar á lánamörkum

Þú getur einnig breytt lánamörkum sjálfkrafa. Á Aðgerðasvæði velurðu **Mynda** og síðan velurðu einn af eftirfarandi valkostum:

- Frá fyrirliggjandi viðskiptavin
- Frá núverandi kredithóp viðskiptavina
- Sjálfvirk lánamörk

### <a name="from-existing-customer"></a>Frá fyrirliggjandi viðskiptavin

Þú getur búið til dagbókarlínur frá núverandi viðskiptavinum. Þegar þú velur **Mynda \> Frá fyrirliggjandi viðskiptavin** birtist valmynd þar sem þú getur sett fram forsendur til að velja viðskiptavini og reikna nýju mörkin.

1. Sláðu inn leiðréttingargildi til að bæta við eða draga upphæð frá lánamörkum. Sláðu inn neikvætt gildi til að lækka núverandi lánamörk eða jákvætt gildi til að auka það.
2. Í reitinn **Gerð gildis** velurðu hvernig gildið sem þú slóst inn í skrefi 1 ætti að nota til að reikna út nýja lánsheimildina:

    - Veldu **Fast gildi** til að breyta lánsfjárhæðinni með fjárhæð.
    - Veldu **Hlutfall** til að breyta lánsfjárhæðinni með hlutfalli.

3. Sláðu inn gildi sem er notað til að slétta útreiknuð lánamörk. Til dæmis, sláðu inn **10,00** til að slétta lánamörk að næstu 10,00 gjaldmiðilseiningum.
4. Stilltu reitinn **Sléttunarregla** til að tilgreina hvort afgangurinn skuli sléttaður upp eða niður.
5. Veljið aðferð sem er notuð til að leiðrétta dagsetningar.

    - Ef þú velur **Algildur** geturðu slegið inn dagsetningar sem skilgreina tímabil fyrir lánamörk.
    - Ef þú velur **Hlutfallslegur** geturðu slegið inn jöfnunardagsetningar fyrir sviðið. Núverandi tímabil á lánsfjármörkum verður aðlagað með mótfærslu.

6. Notaðu flýtifærsluna **Færslur til að fela í sér** til að sía lista yfir viðskiptavini sem fylgja með. Ef þú setur ekki með síur verða kreditmörk færslur til fyrir alla viðskiptavini.
7. Veldu **Í lagi** til að búa til færslur um leiðréttingar á lánamörkum.

### <a name="from-existing-customer-credit-group"></a>Frá núverandi kredithóp viðskiptavina

Þú getur búið til dagbókarlínur frá núverandi kredithópa viðskiptavina. Þegar þú velur **Mynda \> Frá fyrirliggjandi kredithóp viðskiptavina** birtist valmynd þar sem þú getur sett fram forsendur til að velja kredithópa viðskiptavina og reikna nýju mörkin. Viðmiðin eru sömu viðmið og eru notuð til að búa til dagbókarlínur frá núverandi viðskiptavinum. Sjá skrefin í fyrri hlutanum.

### <a name="automatic-credit-limits"></a>Sjálfvirk lánamörk

Þú getur búið til sjálfvirk lánamörk til að skilgreina og uppfæra lánamörk viðskiptavina. Sjálfvirk lánamörk eru búin til fyrir áhættuhóp og þau eru byggð á sérstökum gildum sem notuð eru í stigahópunum. Þú getur notað þessi sjálfvirku lánamörk til að búa til færslum um lánamörk. Ef viðskiptavinur hefur verið úthlutaður í tiltekinn áhættuhóp og lánsupplýsingar viðskiptavinarins samsvara skilyrðum um sjálfvirkt lánamörk verður til leiðrétting færslna fyrir lánamörk.

#### <a name="create-automatic-credit-limits"></a>Búðu til sjálfvirk lánamörk

Þú stofnar sjálfvirk lánamörk með því að nota leiðréttingar á lánamörkum. Þegar þú velur **Mynda \> Sjálfvirk lánamörk** birtist valmynd þar sem þú getur stillt lokadag fyrir nýju lánamörkin sem verða búin til út frá áhættuhópunum sem viðskiptavinum er úthlutað. Þegar því er lokið skaltu velja **Í lagi** til að búa til leiðréttingarlínur fyrir lánamörk.

### <a name="post-adjustments"></a>Bóka leiðréttingar

Eftir að þú hefur búið til leiðréttingarlínur fyrir lánamörk geturðu notað hnappinn **Bóka** í aðgerðarglugganum til að bóka færslurnar og uppfæra lánamörk viðskiptavina. Hins vegar, ef þú hefur sett upp verkflæði, verður þú að velja **Verkflæði \> Senda inn** í aðgerðarglugganum til að skila dagbókinni til samþykktar.

### <a name="credit-limit-adjustments-workflows"></a>Leiðréttingaverkflæði lánamarka

Verkflæði **Leiðréttinga á lánamörkum** er hægt að nota til að senda leiðréttingar á lánamörkum í gegnum aðferð til að samþykkja verkflæði. Þú getur búið til tvö verkflæði á síðunni **Verkflæði kreditstjórnunar** (**Lánastjórnun \> uppsetning \> Kreditstjórnun**):

- **Leiðréttingar á lánamörkum** - Hægt er að nota þetta verkflæði til að samþykkja færslur á hausstiginu.
- **Leiðréttingarlínur fyrir lánamörk** - Hægt er að nota þetta verkflæði til að samþykkja aðlögunarfærslurnar svo að færslurnar geti verið samþykktar af mismunandi einstaklingum, byggt á viðmiðunum í verkflæðinu.

> [!NOTE]
> Þegar þú býrð til verkflæðið **Leiðréttingar á lánamörkum** getur þú sett það upp þannig að leiðréttingarnar verða sjálfkrafa settar inn eftir að línurnar eru samþykktar. Hafðu bara verkið **Bóka dagbók sjálfkrafa** með í verkflæðinu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
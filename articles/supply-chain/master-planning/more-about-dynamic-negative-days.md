---
title: Neikvæðir dagar og gagnvirkir neikvæðir dagar
description: Þetta umræðuefni veitir upplýsingar um neikvæða daga og kvika neikvæða daga og hvernig þú getur notað þá til að hjálpa fyrirtækinu.
author: ChristianRytt
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fd573ab1676af292174efce562b010bcbeb6514
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354738"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Neikvæðir dagar og gagnvirkir neikvæðir dagar

[!include [banner](../includes/banner.md)]

Þetta umræðuefni veitir upplýsingar um neikvæða daga og kvika neikvæða daga og hvernig þú getur notað þá til að hjálpa fyrirtækinu. *Tímamörk neikvæðra daga* tákna þann fjölda daga sem þú ert tilbúin/n að bíða áður en þú pantar nýja áfyllingu þegar þú ert með neikvæðan lager.

Í þessu efnisatriði muntu læra eftirfarandi upplýsingar:

- Hvernig pantanatillögur eru stofnaðar
- Samsvörunin á milli tímamarka neikvæðra daga tímabilsins og afhendingartíma vörunnar
- Hvernig kvikir neikvæðir dagar eru reiknaðir út og hvernig afhendingartími vörunnar er tekinn með í útreikninginn
- Hvernig túlka á [tillögur til að bæta keyrslutíma fyrir áætlun efnisþarfa (MRP) (aðaláætlanagerð)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) sem tengjast neikvæðum dögum

Þetta efni notar þrjár fræðilegar aðstæður til að hjálpa þér að skilja þessar upplýsingar. Munurinn á aðstæðunum er sá staður þar sem þú færð eftirspurn: fyrir, á meðan eða eftir afhendingartímabilið.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Aðstæður 1: Þú færð eftirspurn fyrir afhendingartímabil vörunnar

Þú gætir fengið eftirspurn annaðhvort tiltölulega snemma á afhendingartíma vörunnar eða rétt áður en afhendingartímabilið hefst. Hér er dæmi um þessar aðstæður:

- Sýndarafurðarvaran er með sex daga afhendingartíma kaupa.
- Á degi núll (1. janúar) er birgðastigið fyrir sýndarafurðarvöruna 0 (núll).
- Á degi núll (1. janúar) færðu sölupöntun fyrir magn 10 af sýndarafurðarvörunni.
- Á degi sjö (8. janúar) er fyrirliggjandi innkaupapöntun fyrir magn 10 af sýndarafurðarvörunni.

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir þessar aðstæður.

![Myndrænt yfirlit yfir aðstæður 1.](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Mál A: Neikvæðar dagar eru færri en afhendingartími vörunnar

Ef þú stillir neikvæðu dagana á tölu sem er lægri en afhendingartími vörunnar leitar MRP að kvittunum fyrir sýndarafurðarvöruna innan tímamarka neikvæðra daga. MRP stofnar nýja innkaupatillögu af því að það finnur engar nýjar kvittanir. Þessari tillögu er tafarlaust seinkað um sex daga (afhendingar). Þess vegna kemur hún fram 7. janúar. Núverandi innkaupapöntun fær aðgerðaskilaboðin **Hætta við** þar sem stofnun nýrrar innkaupatillögu hefur gert þau óþörf.

Eftirfarandi skýringarmynd sýnir skyndimynd af þessu máli.

![Skjáskot af máli A fyrir aðstæður 1.](./media/negative-days-2.png)

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál A fyrir aðstæður 1.](./media/negative-days-3.png)

Ef þú lítur á MRP frammistöðu og áætlar óróleika , þá er frammistaða þessa máls ekki góð. MRP verður að búa til nýja tillögu og reikna út tafir og aðgerðir. Þessi verki eru tímafrek. Þetta mál bætir einnig tveimur færslum í viðbót við áætlunina. Á hinn bóginn er sölupöntuninni seinkað um aðeins sex daga, ekki sjö daga.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Mál B: Neikvæðar dagar eru fleiri en afhendingartími vörunnar

Til að bæta MRP frammistöðu geturðu stillt neikvæðu dagana á tölu sem er hærri en afhendingartími vörunnar. Vegna þess að þú getur ekki fengið framboðið innan afhendingartímans í þessum aðstæðum getur þú leitað að kvittunum eins lengi og leitin er skynsamleg. Þó að keyrslutíminn fyrir MRP verði styttri ættirðu að gæta þín á frekari töfum á pöntunum.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Mál C: Gerðu sjálfvirka samsvörun á milli tímamarka vörunnar og tímamarka neikvæðra daga

Til að gera sjálfvirka samsvörun á milli tímamarka vörunnar og tímamarka neikvæðra daga notarðu kvika neikvæða daga. Til að nota kvika neikvæða daga skaltu fara í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar** og síðan, á flipanum **Almennt** í hlutanum **Þekja** skaltu stilla valkostinn **Nota kvika neikvæða daga** á **Já**. MRP leitar síðan eftir kvittunum inni í kvikum neikvæðum dögum. Þessi tímamörk eru reiknuð með því að nota eftirfarandi formúlu:

Tímamörk kvikra neikvæðra daga = Afhendingartími innkaupa + Tímamörk neikvæðra daga + (Núverandi dagsetning – Þarfadagsetning)

(Ef sjálfgefin pöntunargerð á sýndarafurðarvörunni er **Framleiðsla** eða **Flutningur** er afhendingartíminn afhendingartími **birgða**.)

Þegar kvikir neikvæðir dagar eru notaðir eru tímamörkin sem MRP leitar að kvittunum núna 6 + 2 + 0 = 8 dagar. MRP finnur núverandi innkaupapöntun og festir sölupöntun við hana. Engar nýjar pantanatillögur eru stofnaðar. Þess vegna er keyrslutími fyrir MRP styttri. Eftirfarandi mynd sýnir netþarfir fyrir sýndarafurðarvöruna.

![Nettóþarfir fyrir mál C fyrir aðstæður 1.](./media/negative-days-4.png)

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál C fyrir aðstæður 1.](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Mál D: Nota aðeins kvika neikvæða daga

Ef þú stillir neikvæða daga á **0** (núll) og notar aðeins tímamörk kvikra neikvæðra daga eru tímamörk kvikra neikvæðra daga 6 + 0 + 0 = 6 dagar. Í þessu máli er niðurstaðan sú sama og niðurstaðan í máli A fyrir þessar aðstæður. MRP verður að búa til nýja tillögu og reikna út tafir og aðgerðir. Þessi verk eru tímafrek og geta einnig verið pirrandi. Þú hefur líka tvær færslur í viðbót til að vinna úr. Þar sem ekki er hægt að uppfylla eftirspurnina á réttum tíma áður en varan berst, bætir þetta mál óþarfa flækjustigi við áætlunina.

Eftirfarandi skýringarmynd sýnir skyndimynd af þessu máli.

![Skjáskot af máli D fyrir aðstæður 1.](./media/negative-days-6.png)

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál D fyrir aðstæður 1.](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Mál E: Notaðu bæði neikvæðu dagana sem eru hærri en tímamörk afhendingartími og tímamörk kvikra neikvæðra daga

Ef þú stillir neikvæðu dagana á tölu sem er hærri en afhendingartími vörunnar og ef þú notar einnig tímamörk kvikra neikvæðra daga eru tímamörk kvikra neikvæðra daga 6 + 6 + 0 = 12 dagar. Þessi nálgun gæti valdið afar löngum tímamörkum sem MRP verður að leita að niðurstöðum í. Til að fá upplýsingar um hvernig mál E er tengt við aðstæður þar sem þú stillir neikvæða daga á löng tímamörk skaltu fara í hlutann [Niðurstaða](#conclusion) í þessu efni.

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Aðstæður 2: Þú færð eftirspurn á afhendingartímabili vörunnar

Þú gætir fengið eftirspurn einhvern tíma á afhendingartíma vörunnar. Hér er dæmi um þessar aðstæður:

- Sýndarafurðarvaran er með sex daga afhendingartíma kaupa. 
- Á degi núll (1. janúar) er birgðastigið fyrir sýndarafurðarvöruna 0 (núll).
- Á fjórða degi (5. janúar), sem er innan afhendingartíma vörunnar, færðu sölupöntun fyrir 10 af sýndarafurðarvvörunni.
- Á degi sjö (8. janúar) er innkaupapöntun fyrir magn 10 af sýndarafurðarvörunni.

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir þessar aðstæður.

![Myndrænt yfirlit yfir aðstæður 2.](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Mál A: Neikvæðar dagar eru færri en afhendingartími vörunnar

Ef þú stillir neikvæðu dagana á tölu sem er lægri en afhendingartími vörunnar leitar MRP að kvittunum fyrir sýndarafurðarvöruna innan tímamarka neikvæðra daga. Vegna þess að það finnur engar kvittanir skapar MRP nýja innkaupatillögu sem notar núverandi dagsetningu sem pöntunardagsetningu. Þessari tillögu er tafarlaust seinkað um sex daga (afhendingar). Þess vegna kemur hún fram 7. janúar. Núverandi innkaupapöntun fær aðgerðaskilaboðin **Hætta við** þar sem stofnun nýrrar innkaupatillögu hefur gert þau óþörf.

Eftirfarandi skýringarmynd sýnir skyndimynd af þessu máli.

![Skjáskot af máli A fyrir aðstæður 2.](./media/negative-days-9.png)

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál A fyrir aðstæður 2.](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Mál B: Neikvæðar dagar eru fleiri en afhendingartími vörunnar

Þetta mál líkist máli B fyrir aðstæður 1. Ef þú stillir neikvæðu dagana á tölu sem er meira en afhendingartími vörunnar færðu ekki nýja tillögu. Sölupöntunin er fest við fyrirliggjandi innkaupapöntun.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Mál C: Gerðu sjálfvirka samsvörun á milli tímamarka vörunnar og tímamarka neikvæðra daga

Þetta mál líkist máli C fyrir aðstæður 1, þar sem kvikir neikvæðir dagar virka alveg jafn vel og þeir gera í því máli. Tímamörk kvikra neikvæðra daga eru núna 6 + 2 - 4 = 4 dagar. Ef þú notar þessa nálgun finnur MRP fyrirliggjandi innkaupapöntun og festir sölupöntun við hana. Þar sem engar nýjar tillögur eru stofnaðar er keyrslutíminn fyrir MRP styttri.

Eftirfarandi skýringarmynd sýnir skyndimynd af þessu máli.

![Skjáskot af máli C fyrir aðstæður 2.](./media/negative-days-11.png)

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál C fyrir aðstæður 2.](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Mál D: Nota aðeins kvika neikvæða daga

Ef þú stillir neikvæða daga á **0** (núll) og notar aðeins tímamörk kvikra neikvæðra daga eru tímamörk kvikra neikvæðra daga núna 6 + 0 – 4 = 2 dagar. Í þessu máli er niðurstaðan sú sama og niðurstaðan í máli A fyrir þessar aðstæður. Til að sjá myndrænt yfirlit af því sem gerist, sjá dæmi A fyrir þessar aðstæður.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Mál E: Notaðu bæði neikvæðu dagana sem eru hærri en tímamörk afhendingartími og tímamörk kvikra neikvæðra daga

Ef þú stillir neikvæðu dagana á tölu sem er hærri en afhendingartími vörunnar og ef þú notar einnig tímamörk kvikra neikvæðra daga eru tímamörk kvikra neikvæðra daga 6 + 6 – 4 = 8 dagar. Þessi nálgun gæti valdið afar löngum tímamörkum sem MRP verður að leita að niðurstöðum í. Til að fá upplýsingar um hvernig mál E er tengt við aðstæður þar sem þú stillir neikvæða daga á löng tímamörk skaltu fara í hlutann [Niðurstaða](#conclusion) í þessu efni.

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Aðstæður 3: Þú færð eftirspurn eftir afhendingartímabil vörunnar

Þú gætir fengið eftirspurn eftir afhendingartímabil vörunnar. Hér er dæmi um þessar aðstæður:

- Sýndarafurðarvaran er með sex daga afhendingartíma kaupa.
- Á degi núll (1. janúar) eru birgðarnar fyrir sýndarafurðarvöruna 0 (núll).
- Á sjöunda degi (8. janúar), sem er utan afhendingartíma vörunnar, færðu sölupöntun fyrir 10 af sýndarafurðarvvörunni.
- Á degi tíu (11. janúar) er boðið upp á innkaupapöntun fyrir magn 10 af DemoProduct.

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir þessar aðstæður.

![Myndrænt yfirlit yfir aðstæður 3.](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Mál A: Neikvæðar dagar eru færri en afhendingartími vörunnar

Ef þú stillir neikvæða daga á tölu sem er lægri en afhendingartími vörunnar lítur MRP tvo daga fram fyrir þarfadagsetningu sölupöntunarinnar. MRP stofnar innkaupatillögu þann 2. janúar af því að það finnur ekki neitt. Þessi innkaupatillaga verður send rétt tímanlega til að uppfylla eftirspurn sölupöntunar. Fyrirliggjandi innkaupapöntun fær aðgerðaboðin **Hætta við** vegna þess að hennar er ekki þörf.

Eftirfarandi skýringarmynd sýnir skyndimynd af þessu máli.

![Skjáskot af máli A fyrir aðstæður 3.](./media/negative-days-14.png)

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál A fyrir aðstæður 3.](./media/negative-days-15.png)

> [!NOTE]
> Í framangreindri skjámynd er þarfadagsetning innkaupapöntunar 12. janúar. Þar sem skjámyndin var tekin árið 2015, þegar 11. janúar var sunnudagur, flutti MRP þarfadagsetningu á næsta vinnudag, sem var mánudaginn 12. janúar. Engu að síður hefur innkaupapöntunin afhendingu þann 11. janúar.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Mál B: Neikvæðar dagar eru fleiri en afhendingartími vörunnar

Ef þú stillir neikvæðu dagana á tölu sem er meira en afhendingartími vörunnar færðu ekki nýja tillögu. Sölupöntunin er fest við fyrirliggjandi innkaupapöntun. Þess vegna seinkar sölupöntuninni. Ef þú býrð til tillögu geturðu sent sölupöntunina á réttum tíma.

Eftirfarandi skýringarmynd sýnir skyndimynd af þessu máli.

![Skjáskot af máli B fyrir aðstæður 3.](./media/negative-days-16.png)

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál B fyrir aðstæður 3.](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Mál C: Gerðu sjálfvirka samsvörun á milli tímamarka vörunnar og tímamarka neikvæðra daga

Þetta mál líkist máli C fyrir aðstæður 1, þar sem kvikir neikvæðir dagar virka alveg jafn vel, ef ekki betur en þeir gera í máli B fyrir þessar aðstæður.

Tímamörk kvikra neikvæðra daga eru núna 6 + 2 - 7 = 1 dagur. Hins vegar telur kerfið í þessu tilfelli samt sem áður neikvæða daga vera afhendingartímann (2), þar sem MRP tekur tillit til hámarksgildis á milli afhendingartíma neikvæðra daga og afhendingartíma kvikra neikvæðra daga. Í þessu máli er því niðurstaðan sú sama og niðurstaðan í máli A fyrir þessar aðstæður.

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist í þessu máli.

![Myndrænt yfirlit yfir mál C fyrir aðstæður 3.](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Mál D: Nota aðeins kvika neikvæða daga

Ef þú stillir neikvæða daga á **0** (núll) og notar aðeins tímamörk kvikra neikvæðra daga eru tímamörk kvikra neikvæðra daga núna 6 + 0 – 7 = -1 dagur. Í þessu máli tekur kerfið enn tillit til afhendingartíma neikvæðra daga (2). Í þessu máli er því niðurstaðan sú sama og niðurstaðan í máli A fyrir þessar aðstæður og er með alla sömu vankantana. Til að sjá myndrænt yfirlit af því sem gerist, sjá dæmi A fyrir aðstæður 2.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Mál E: Notaðu bæði neikvæðu dagana sem eru hærri en tímamörk afhendingartími og tímamörk kvikra neikvæðra daga

Þetta mál er það sama og mál E fyrir aðstæður 1 og 2. Það er í grundvallaratriðum með sömu ávinninga og vankanta.

## <a name="conclusion"></a>Niðurstaða

Eins og aðstæðurnar þrjár í þessu efni sýna er góð hugmynd að stilla neikvæða daga á tölu sem er hærri en afhendingartími varanna í þekjuflokknum. Það er líka góð hugmynd að nota aðeins kvika neikvæða daga og til að stilla neikvæðu dagana á þann fjölda daga sem þú ert tilbúin/n að bíða áður en þú pantar nýja áfyllingu þegar þú ert með neikvæðar birgðir (með öðrum orðum, fjölda daga sem þú ert tilbúin/n að seinka eftirspurn frekar). Að auki skulu vörur í sama þekjuflokki hafa svipaða afhendingartíma.

Ef þú stillir neikvæða daga á **0** (núll) og notar ekki kvika neikvæða daga stofnar MRP alltaf nýja tillögu til að uppfylla eftirspurn. Í þessum aðstæðum er mikilvægt að þú vinnir með aðgerðaboð til að ganga úr skugga um að þú safnir ekki upp birgðum.

Þú gætir viljað setja neikvæða daga í löng tímamörk og vinna síðan með aðgerðaboðunum. Þessi nálgun framleiðir góðar áætlanagerðarniðurstöður, en hún er líka svolítið hægari. Hún gæti líka verið erfiðara að greina því að þú verður að greina og beita aðgerðaboðunum. Eftirfarandi er dæmi:

- Sýndarafurðarvaran er með sex daga afhendingartíma kaupa.
- Á degi núll (1. janúar) eru birgðarnar fyrir sýndarafurðarvöruna 0 (núll).
- Á degi núll (1. janúar) færðu sölupöntun fyrir magn 10 af sýndarafurðarvörunni.
- Á degi níu (10. janúar) þú færð boðið upp á sölupöntun fyrir magn 10 af DemoProduct.
- Á degi ellefu (12. janúar) er boðið upp á innkaupapöntun fyrir magn 10 af DemoProduct.
- Neikvæðir dagar eru stilltir á **20**, sem er miklu hærra en afhendingartími vöru.

Eftirfarandi skýringarmynd sýnir myndrænt yfirlit yfir það sem gerist.

![Myndræn yfirferð á dæminu.](./media/negative-days-19.png)

MRP framleiðir eftirfarandi niðurstöður.

![Dæmi um niðurstöður 1.](./media/negative-days-20.png)

Í framangreindri skjámynd er þarfadagsetning sölupöntunar 9. janúar í stað 10. janúar. Þar sem skjámyndin var tekin árið 2015, þegar 10. janúar var laugardagur, ætti þarfadagsetning pöntunarinnar að vera vinnudagurinn á undan, sem var föstudaginn 9. janúar.

MRP stofnar innkaupatillögu til að uppfylla eftirspurnina sem er krafist af fyrstu sölupöntuninni en mælir einnig með því að þú hættir við tillöguna vegna þess að þú getur gert fært fyrirliggjandi innkaupapöntun fram og aukið magnið í henni.

Niðurstöðurnar eru ekki rangar, en keyrslutíminn fyrir MRP gæti verið lengri, því MRP verður stofna allar tafir og tillögur. Auk þess gæti skipuleggjandi krafist meiri tíma til að skilja niðurstöður MRP. Í þessu máli er mikilvægast að skipuleggjandi skilji og noti aðgerðaskilaboðin.

Ef þú dregur úr neikvæðum dögum í tölu sem er nær afhendingartíma vörunnar og þú notar kvika neikvæða daga, framleiðir MRP eftirfarandi niðurstöður.

![Dæmi um niðurstöður 2.](./media/negative-days-21.png)

MRP býr til tillögu sem er fest við fyrstu sölupöntunina. Síðan, eins og búist er við, er seinni sölupöntunin fest við fyrirliggjandi innkaupapöntun á grundvelli stillinga neikvæðra dagsetninga. Þessi áætlanagerð er einnig rétt og keyrslutíminn fyrir MRP gæti verið styttri. Í þessu máli er ekki nauðsynlegt að skilja og vita hvernig á að vinna með aðgerðaskilaboðunum.

Til að tryggja að rétt gildi séu færð fyrir fyrirtækið, verður þú að hugsa hvað varðar bæði virkni og keyrslutíma MRP. Þess vegna getur það verið svolítíð happa og glappa að ákvarða ákjósanlegustu gildin.

## <a name="see-also"></a>Sjá einnig

Fyrir frekar umfjöllun skaltu sjá upphaflega bloggfærslu [Meira um (kvika) neikvæða daga](/archive/blogs/axmfg/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

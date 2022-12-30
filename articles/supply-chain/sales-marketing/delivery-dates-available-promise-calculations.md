---
title: Pöntun lofað
description: Þessi grein gefur upplýsingar um það þegar pöntun er lofað Pöntun lofað hjálpar þér lofa áreiðanlegum afhendingartíma til viðskiptavina þinna og gefur þér sveigjanleika þannig að þú getur staðið við þessar dagsetningar.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228267"
---
# <a name="order-promising"></a>Pöntun lofað

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um það þegar pöntun er lofað Pöntun lofað hjálpar þér lofa áreiðanlegum afhendingartíma til viðskiptavina þinna og gefur þér sveigjanleika þannig að þú getur staðið við þessar dagsetningar.

Pöntun lofað reiknar fyrstu sendingar- og innhreyfingardagsetningu, og er byggð á stýringaraðgerð afhendingardags og flutningsdaga. Hægt er að velja á milli eftirfarandi stýringaraðferða afhendingardags:

- **Afhendingartími sölu** – afhendingartími sölu er tíminn milli stofnunar sölupöntunarinnar og sendingu vara. Útreikningur afhendingardags er á grundvelli sjálfgefinn fjölda daga, og tekur ekki tillit til birgðastöðu, , þekktrar eftirspurnar eða áætlað framboð.
- **ATP (tiltækt-til-loforðs)** – ATP er magn vöru sem er tiltækur og hægt er að lofa viðskiptavini á tiltekinni dagsetningu. ATP útreikningur felur í sér óstaðfestar birgðir, afhendingartími , áætlaðar innhreyfingar og úthreyfingar.
- **ATP + mörk úthreyfinga**, sendingardagsetning er sú sama og dagsetning sem er tiltækt-til-loforðs (ATP) auk marka úthreyfinga fyrir vöruna. Mörk úthreyfinga er sá tími sem þarf að undirbúa þær vörur sem á að senda.
- **Ctp-Afhendingargetu (óhætt að lofa)**– Framboð er reiknað í gegnum niðurbrot. Ef þú ert að nota fínstilling áætlanagerðar er ekki heimilt að nota *CTP-afhendingargetu* sem stýringaraðferð afhendingardags og ef hún er valin mun það valda villu þegar útreikningur er keyrður. Frekari upplýsingar um hvernig á að setja upp og nota CTP-afhendingargetu er að finna í [Reikna afhendingardaga sölupöntunar með CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).
- **CTP fyrir fínstillingu skipulagningar -** Notaðu CTP útreikninginn sem er gefinn upp með fínstillingu skipulagningar. Þessi valkostur hefur engin áhrif ef þú notar innbyggðu aðaláætlunarvélina. Frekari upplýsingar um hvernig á að setja upp og nota CTP-afhendingargetu er að finna í [Reikna afhendingardaga sölupöntunar með CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

> [!NOTE]
> Þegar sölupöntun er uppfærð eru upplýsingar um pöntunarloforð aðeins uppfærðar ef ekki er hægt að uppfylla fyrirliggjandi dagsetningu pöntunarloforðs, eins og sýnt er í eftirfarandi dæmum:
>
> - **Dæmi 1**: Dagsetning pöntunarloforðs er 20. júlí en vegna aukins magns er ekki hægt að afhenda fyrr en 25. júlí. Vegna þess að ekki er lengur hægt að uppfylla núgildandi dagsetningu er pöntunarloforð ræst.
> - **Dæmi 2**: Dagsetning pöntunarloforðs er 20. júlí en vegna minnkandi magns er nú hægt að afhenda þann 15. júlí. Vegna þess að ekki er enn hægt að uppfylla núgildandi dagsetningu, er pöntunarloforð hins vegar ekki ræst og 20. júlí er enn dagsetning pöntunarloforðs.

## <a name="atp-calculations"></a>ATP útreikninguar

ATP-magn er reiknað út með því að nota aðferðarinnar “uppsafnað ATP með framsýni”. Helsti kostur þessa ATP reikniaðferðin er að hún getur meðhöndlað tilvik þar sem heildartala úthreyfinga á meðal innhreyfinga er meira en síðasta innhreyfing (til dæmis þegar verður að nota magn úr eldri innhreyfingu til að uppfylla kröfu). Útreikningsaðferð "uppsafnað ATP með framsýni" inniheldur allar úthreyfingar þar til uppsafnað magn til innhreyfingar er orðin meiri en uppsafnað magn til úthreyfingar. Þar af leiðandi metur ATP reikniaðferðin hvort hægt er að nota sumt magn úr eldri tímabilum í seinni tímabilum.

Atp-magn er óráðstafað birgðajafnvægi í fyrsta tímabilinu. Yfirleitt er hún er reiknuð fyrir hvert tímabil þar sem innhreyfing er áætluð. Forritið reiknar út ATP-tímabilið í dögum, og reiknar gildandi dagsetningu sem fyrstu dagsetninguna fyrir ATP-magn. Í fyrsta tímabilinu inniheldur ATP birgðir á lager mínus pantanir viðskiptavina sem eru á gjalddaga eða komnir fram yfir hann.

ATP er reiknað út með því að nota eftirfarandi formúlu:

ATP = ATP fyrir undangengið tímabil + innhreyfingarnar fyrir gildandi tímabil - úthreyfingarnar fyrir gildandi tímabil - magn netúthreyfinga fyrir hvert tímabil í framtíðinni þar til að tímabilinu þegar heild innhreyfinga fyrir öll tímabil í framtíðinni, upp að og með framtíðartímabilinu, er umfram heild úthreyfinga, upp að og með framtíðartímabilinu.

Taktu eftir að ATP-útreikningurinn inniheldur ekki upplýsingar um lokadag og fram yfir ATP-tímamörkin sem kerfið gerir ráð fyrir þegar hægt er að lofa einhverju magni.

Þegar það eru engar innhreyfingar eða úthreyfingar að athuga, er ATP-magnið fyrir eftirfarandi dagsetningar það sama og ATP-magnið sem var reiknað út síðast.

Ef að allar víddirnar sem eru notaðar fyrir vöru eru ekki gefnar upp þegar athugun ATP er lokið, gætu þær enn verið tilgreindar á innhreyfingum og úthreyfingum. Í því tilfelli, í ATP-útreikningi, verður að leggja saman innhreyfingarnar og úthreyfingarnar í fyrirliggjandi víddir til að draga úr fjölda innhreyfinga- og úthreyfingalína sem notaður eru í ATP-útreikningi.

Atp-magnið sem er sýnt er alltaf meira en eða jafnt og 0 (núll). Ef útreikningur skilar neikvæðu ATP-magni (til dæmis ef að meira magn en tiltæku magni hafði verið lofað áður), stillir magnið sjálfkrafa stillt á 0.

### <a name="example"></a>Dæmi

Í **atp-tímamörk eftirspurnar afturábak** svæði stýrir hversu langt aftur í tíma á að leita að frestuðum eftirspurnarpöntunum eða birgðaúthreyfingum. Í **atp-tímamörk eftirspurnar afturábak** svæði stýrir hversu langt aftur í tíma á að leita að frestuðum birgðapöntunum eða innhreyfingum birgða. Til dæmis, ef pantanir eru seinkaðar aðeins sjö dögum ætti að fara í atp-útreikningi, bæði svæðin ætti að stilla sem **7**.

Reitirnir **ATP mótfærður tími seinkaðrar eftirspurnar** og **ATP mótfærður tími seinkaðs framboðs** stjórna þegar seinkaðar eftirspurn eða seinkað framboð eru teknar með í atp-útreikningi. Til dæmis, ef seinkuð framboð og eftirspurn ætti að fara í atp-útreikning daginn eftir daginn á morgun ætti báðir reitir að vera stillt á **2**. Gildið **2** þýðir að magn af vöru á seinkuðum innkaupapöntun sem ætti að hafa í huga í útreikningi ATP verður að álíta tiltæk tveimur dögum eftir núgildandi dagsetningu.

Fyrir Eftirfarandi dæmi er **7** færð inn í á **atp-tímamörk eftirspurnar afturábak** og **atp-tímamörk framboðs afturábak** svæði, og **1** er færð inn í á **ATP mótfærður tími seinkaðrar eftirspurnar** og **ATP mótfærður tími seinkaðs framboðs** svæði.

Enn hefur ekki verið móttekin innkaupapöntun fyrir 200 stykki af vöru sem á að hafa verið mótteknar fyrir þremur dögum. Þess vegna sölupöntunarlínu fyrir 75 stykki á sömu afurð sem á að hafa verið sendar gær hefur ekki verið sent.

Viðskiptavinur hringir og vill panta 150 stykki af sömu afurð. Þegar framboð afurðar er athuguð sérðu aðra innkaupapöntun upp á 100 stykki af sömu afurðar sem á að afhenda 10 dögum síðar.

Stofna sölupöntunarlínu fyrir afurðina og færa inn **150** sem magn.

Þar sem stýring fyrir afhendingardagsetningu er aðferðin ATP , eru ATP gögnin reiknuð til að finna fyrstu hugsanlegu sendingardagsetningu. Byggt á stillingum, er tekið tillit til seinkaðar innkaupapöntunar og sölupöntunar, og atp-magnið sem fæst út úr þessu fyrir gildandi dagsetningu er 0. Á Morgun, þegar búist er við að seinkaðar innkaupapöntun sé móttekin, er atp-magnið reiknað sem meira en 0 (í þessu tilfelli er hann reiknaður sem 125). Hins vegar 10 dögum frá núna, þegar viðbótar innkaupapöntun upp á 100 stykki er búist við að vera móttekin, verður atp-magn meira en 150.

Þess vegna sendingardagsetningin er stillt á 10 daga frá núna, samkvæmt atp-útreikningi. Þess vegna er viðskiptavin sem bað um magnið sagt að hægt er að afhenda 10 dögum frá nú.

## <a name="ctp-calculations"></a>CTP-útreikningur

Með CTP-afhendingargeta getur þú gefið viðskiptavinum raunhæfar dagsetningar fyrir hvenær þú getur lofað tilteknum vörum. Fyrir hverja sölulínu getur þú gefið upp dagsetningu sem tekur mið af lagerbirgðum, framleiðslugetu og flutningstíma.

CTP-afhendingargeta stækkar ATP-virknina með því að taka til greina upplýsingar um afkastagetu. Þar sem ATP tekur aðeins til greina efnislegt framboð og gerir ráð fyrir ótakmörkuðum afkastatilföngum tekur CTP tillit til bæði efnis og afkastagetu. Því gefur það raunhæfari mynd af því hvort hægt sé að fullnægja eftirspurn innan ákveðins tímaramma.

CTP-afhendingargeta virka aðeins öðruvísi, eftir því hvaða aðaláætlunarvél þú notar (Fínstilling áætlanagerðar eða innbyggða vélin). CTP-afhendingargeta fyrir fínstilling skipulagningar styður eins og er aðeins hluta af þeim aðstæðum CTP-afhendingargetu sem eru studdar af innbyggðu vélinni.

Nánari upplýsingar um hvernig á að setja upp og nota CTP fyrir hverja vél er að finna í [Reikna afhendingardaga sölupöntunar með CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Valkostir afhendinga
description: "Þeir sem taka við sölupöntun geta notað valkostir afhendingar síðuna til sjá aðra pöntun uppfyllingar valkostir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 79d1e7349df7e5042af016f9b595f9cf9bcfc294
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="delivery-alternatives"></a>Valkostir afhendinga

[!include[banner](../includes/banner.md)]


Þeir sem taka við sölupöntun geta notað valkostir afhendingar síðuna til sjá aðra pöntun uppfyllingar valkostir.

Í Microsoft Dynamics 365 fyrir Operations útgáfu 1611 (Nóvember 2016) sölupöntun viðtakendur getur notað **Valkostir afhendinga** blaðsíðu til að sjá aðra pöntun uppfyllingar valkostir. Endurhönnuð útlitssíða veitir betra yfirlit yfir alla aðra valkosti. Hún gerir kleift viðtakendum pöntunar að leita yfir núverandi fyrirtæki uppfyllingu möguleikar. Þeir geta nú bæði skoðað innan fyrirtækjasamstæðu möguleika og möguleika frá ytri lánardrottnum. Með því að raða valkostir með afhendingardagsetningu, viðtakendur sölupöntun geta skoðað skynsamlegan lista yfir valkosti afhendingar. Að auki hjálpa færibreytur að stjórna betur áætlaðri afhendingu. Þar sem flutningstími geta haft áhrif á afhendingardagsetningar, viðtakendur sölupöntun geta skoðað meira af mismunandi flutningsleiðum aðilum tilboð. Þar sem ítarlegar upplýsingar er sýndur fyrir hverja greiðslutillögulínuna, viðtakendur pöntunar getur tekið ákvarðanir upplýstar beint úr á **Afhendingu valkosti** síðu.

## <a name="open-the-delivery-alternatives-page"></a>Opna síðuna Afhendingu valkosti
Þú getur opnað **Afhending** **valkosti** síðuna úr sölupöntunarlínunni.

1.  Smellt er á **Vara og framboð** &gt; **Afhendingu valkosti**.
2.  Smellt er á **Línu upplýsingar** &gt; **Afhendingu** &gt; **valkosti Afhendingar.**

Einnig er hægt að opna í **valkosti Afhendingu** með því að opna síðuna á **sölupöntun vinnsla og fyrirspurn** vinnusvæði og smella síðan á **Pantanir og eftirlæti** &gt; **Fresta pöntunarlínur** &gt; **valkosti Afhendingu** **Athugasemd:** Þú getur opnað **valkosti Afhendingu** síðunni ef bæði eftirfarandi skilyrði eru uppfyllt:

-   Allar nauðsynlegar upplýsingar sölulínu er færð inn.
-   Í **afhendingardagsetningu stýringu** er stillt á gildi annað en **Ekkert**.

## <a name="delivery-date-control-methods"></a>Stýring afhendingardagsetninga
Aðferð stýringar afhendingardagsetningu ákvarðar hvernig kerfið birtir afhendingardagsetningar, hvernig valkostir afhendingar eru reiknaðar og hvaða upplýsingar birtast. Athugið að gögn stýring afhendingardagsetningar tekur mið af dagatöl. Þar af leiðandi eftirfarandi dagatöl geta haft áhrif á þau móttökudagsetningu: Vöruhús dagatal, flutningsdagatal, dagatal lánardrottins og dagatal viðskiptavinar. Eftirfarandi tafla lýsir sérhverja aðferð stýringu afhendingardagsetninga.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Aðferð</strong></td>
<td><strong>Lýsing</strong></td>
</tr>
<tr class="even">
<td><strong>Ekkert</strong></td>
<td><ul>
<li>Valkostir afhendingar fyrir sölulínum eru ekki studdir. Þessi valkostur slekkur á stýringu gagna afhendingar.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Afhendingartími sölu</strong></td>
<td><ul>
<li>Afhendingardagsetningar valkostir eru reiknaðar út frá afhendingartíma fyrirfram sölu. Flutningsdagar eru reiknaðar út frá afhendingarmáta.</li>
<li>Afhendingarvalkostir innihalda vöruhús sem hafa lagerbirgðir og framboð/eftirspurn pantanir.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Afhendingar valkostir eru reiknaðir út frá tillækt að lofa eðli (ATP). Gildandi framboð og áætlaða síðari framboð er skoðað. Flutningsdagar eru reiknaðar út frá afhendingarmáta.</li>
<li>Afhendingarvalkostir innihalda vöruhús sem hafa lagerbirgðir og framboð/eftirspurn pantanir.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + mörk úthreyfinga</strong></td>
<td><ul>
<li>Valkostir afhendingar eru reiknaðar út frá aðferð ATP en mörk úthreyfinga er innifalin í útreikningunum.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP-afhendingargeta</strong></td>
<td><ul>
<li>Afhending valkostir eru reiknaðir út frá afhendingargetu (CTP) eðli. MRP aukning er notuð til að ákvarða fáanleika. Athugið, CTP jafnar að minnsta kosti afhendingardagsetningar við afhendingartíma sölu. Flutningsdagar eru reiknaðar út frá afhendingarmáta.</li>
<li>Afhending valkostir innihalda tillögur fyrir eftirfarandi vöruhús:
<ul>
<li>Núgildandi vöruhús</li>
<li>Sjálfgefið vöruhús</li>
<li>Öll vöruhús sem hafa tiltækar birgðir</li>
<li>Öll vöruhús sem hafa birgðapöntun</li>
<li>Öll vöruhús sem hafa virka uppskriftina (BOM) útgáfur</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Skoða upplýsingar um afhendingar valkosti
Hér er lýst upplýsingar um afhendingu valkosti sem er tiltæk á hverjum flipa á við **Afhendingu valkosti** síðu.

### <a name="products"></a>Afurðir

Þessi flipi sýnir yfirlit yfir vöruna og upplýsingum um gildandi sölulínu.

### <a name="delivery-alternatives"></a>Valkostir afhendinga

Þessi flipi sýnir lista yfir valkosti afhendingar sem er raðað eftir móttaka gögn. Fyrir ofan listann er hægt að velja þá valkosti sem tillögurnar eiga að byggja á. Einnig er hægt að velja afhendingarmáta, sem ákvarðar flutningsdaga. Eftirtaldir valkostir eru í boði:

-   **Taka til aðrar vöruvíddasamsetningar** - Þessi valkostur er tiltækur fyrir vörur sem hafa vöruvíddasamsetningar. Það tekur til valkosti afhendingar fyrir hinar vöruvíddasamsetningarnar vörunnar. Þessi valkostur er ekki tiltækur fyrir CTP.
-   **Eru hluti af magni** - Sjálfgefnu, aðeins tillögur sem uppfylla fullt magns í sölulínunni eru hafðar með. Veljið þennan valkost til að taka með tillögur sem uppfylla aðeins hluta pöntunarlínunnar. Þessi valkostur er gagnlegur ef viðskiptavinur biður um fyrri afhendingardagsetningu og samþykkir hlutaafhendingu.
-   **Hafa dagsetningu síðar** - Sjálfgefnu, aðeins tillögur sem eru betri (fyrri) en núgildandi dagsetningar á sölulínunni eru sýndar. Veldu þennan valkost til að hafa síðari dagsetingar með. Þessi valkostur getur verið gagnlegt í aðstæðum þar sem færibreytur aðrar en dagsetning hafa forgang. Til dæmis gæti tiltekinn lánardrottin eða vöruhús verið æskilegt.
-   **Afhendingarmáti** - Veljið æskilega afhendingarmáta til að lágmarka flutningstími og kostnað. Strax sjást áhrif á ráðlagða valkosti afhendingar. Þess vegna er auðvelt að bera saman valkosti.
-   **Taka innkaup með** - þegar innkaup er valinn, er innifalið í afhendingarvalkosti möguleikar á innkaupum frá bæði ytri lánardrottnum og annarra fyrirtækja í samstæðunni (innan samstæðu). **Taka innkaup með** valkosturinn er studd fyrir ATP og ATP + mörk úthreyfinga stýringu afhendingardagsetingar. Innkaupa valkostir úr sjálfgefnu keypt lánardrottin fyrir vöru og alla samþykktu lánardrottna fyrir vöru eru teknar með.
-   Fyrir ytri lánardrottna er útreikningurinn byggður á afhendingartíma innkaupa.
-   Fyrir samstæðufyrirtæki, tekur útreikningur til hvað er tiltækt frá upprunafyrirtæki, á grundvelli stýringu afhendingardagsetningar upprunafyrirtækis.
-   **Afhendingargerðinni** (Viðeigandi fyrir innkaup)
    -   **Birgðir** - Vörur eru sendar frá upprunavöruhúsi til svæði/vöruhús á sölulínunni. Þær eru svo sendar úr vöruhúsinu til viðskiptavinar.
    -   **Bein sending** - Vörur eru sendar frá upprunavöruhúsið beint til viðskiptavinar.

### <a name="availability-information"></a>Upplýsingar um framboð

Upplýsingarnar á þessum flipa eru tengduarr afhendingu annarrar línu sem valin er. Eftirfarandi upplýsingar sýnd, allt eftir því hvernig stýringu afhendingardagsetningar fyrir sölulínu er háttað:

-   **Afhendingartími sölu**
    -   **Tiltæk í dag** - Sýna núverandi efnislega á lager, efnislegu fráteknar og tiltæk efnislegum birgðum.
    -   **Færibreytur** - Sýna birgðaeiningu og afhendingartíma sölu.

-   **ATP og ATP + mörk úthreyfinga**
    -   **Tiltæk í dag** - Sýna núverandi efnislega á lager, efnislegu fráteknar og tiltæk efnislegum birgðum.
    -   **Færibreytur** - Sýna birgðaeiningu og afhendingartíma sölu.
    -   **Síðari framboð** - Sýna myndræn framsetning á gildandi og framtíðar framboð fyrir valið svæði og vöruhús í **Afhendingu valkostir**. Hægt er að smella á línuritsdálkana til að sjá ítarlegri upplýsingar um framtíðarframboð afurðarinnar. Sleðinn sýnir lista yfir viðeigandi eftirspurn og pantanir birgðir innan ATP tímamörk.

-   **CTP-afhendingargeta**
    -   **Tiltæk í dag** - Sýna núverandi efnislega á lager, efnislegu fráteknar og tiltæk efnislegum birgðum.
    -   **Færibreytur** - Sýna birgðaeiningu og afhendingartíma sölu.
    -   **Aukning** - Sýna aukningu birgðir fyrir völdu afhendinguna valkostir. Hægt er að nota **Uppsetning** til að breyta svæðunum og birgðavíddum sem sýndar eru í niðurbrot.

### <a name="impact-of-selected-alternative"></a>Áhrif af völdum valkosti

Þessi flipi sýnir áhrif völdu afhendingar valkosturinn. Ef smellt er á **í lagi**, sölulínu uppfærist með auðkennda gilda í dálkunum VALIÐ. Athugið að, ef magnið á völdu afhendingarvalkostur er minna en magnið í sölulínu, afhendingáætlun er stofnuð og pöntunarlínan er skipt í tvær línur: eina línu fyrir valda magnið og eina línu fyrir eftirstandandi magn. Einnig er hægt að uppfæra viðskipta lína þannig að stemmir við áætlaðar línum og hefur áhrif á verðinu.

<a name="see-also"></a>Sjá einnig
--------

[Pöntun lofað](http://ax.help.dynamics.com/en/wiki/delivery-dates-and-available-to-promise-calculations/)






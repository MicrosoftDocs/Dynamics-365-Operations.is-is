---
title: Tímasetja gagnahreinsun söluferils
description: Þessi grein lýsir því hvernig þú getur hjálpað til við að bæta árangur kerfisins með því að skipuleggja reglulegt hreinsunarverkefni vegna söluuppfærsluferlis sem á að keyra með reglulegu millibili.
author: myvakalo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e9a4dd5372afa8a0452449d1cb9121107e6e1610
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335504"
---
# <a name="schedule-sales-history-data-cleanup"></a>Tímasetja gagnahreinsun söluferils

[!include [banner](../includes/banner.md)]

Sem hluti af hefðbundinni starfsemi sinni býr Microsoft Dynamics 365 Supply Chain Management til og geymir sölusögu og uppfærslugögn í sífellu. Með tímanum gæti mikið af úreltum sölugögnum safnast upp í kerfinu þínu. Þessi uppsöfnuðu gögn geta valdið vandamálum varðandi frammistöðu og virkni þegar skjöl sem tengjast sölupöntunum eru birt. (Þessi skjöl eru m.a. staðfestingar á sölupöntunum, fylgiseðlar sölu, tínslulistar fyrir sölu og reikningar). Því ættir þú að setja upp og tímasetja *Hreinsa sögu söluuppfærslna* á sölusögu til að keyra með reglulegu millibili. Þetta verkefni mun fjarlægja öll uppfærslugögn sölusögu sem ekki er lengur þörf fyrir.

Ef þú notar *Hreinsa sögu söluuppfærslna* reglulega mælum við með því að þú virkjir eiginleika fyrir *Endurbætur á afköstum hreinsunar á söluferli* svo að verkefnið gangi betur fyrir sig. (Engu að síður getur þú einnig keyrt verkefnið án þess að virkja þennan eiginleika.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Kveiktu á hreinsunareiginleikum söluferlis

Til að setja upp og nota reglulegt verkefni til að *Hreinsa sögu söluuppfærslna* ásamt öllum eiginleikum sem lýst er í þessari grein verður þú að virkja *Endurbætur á afköstum hreinsunar á söluferli* til að *Hreinsa uppfærsluferil sölu eftir aldri* í Eiginleikastjórnun, eins og lýst er í eftirfarandi undirköflum.

### <a name="sales-history-cleanup-performance-improvements"></a>Afkastaendurbætur á hreinsun söluferils

Reglubundin runuvinnsla **Hreinsun uppfærsluferils sölu** getur tekið langan tíma ef hún er sjaldan keyrð í umhverfum þar sem er mikið um söluuppfærslur. Í þessum tilvikum geta *Endurbætur á afköstum hreinsunar á söluferli* eiginleikinn hjálpað til við að stytta keyrslutíma og bæta áreiðanleika.

Þessi eiginleiki bætir núverandi hreinsunarvinnslu á eftirfarandi hátt:

- Hann skiptir hreinsun í runur (hægt er að breyta runustærð í sérstillingum).
- Hann er keyrður að hámarki í 2 klukkustundir (hægt er að breyta tímalengd í sérstillingum).
- Ef mögulegt nýtir hann getu gagnagrunnsins til að lágmarka læsingu og forðast að sameina færslutöflur við hreinsun.

Eftir að eiginleikinn er virkjaður verður runuvinnslan **Hreinsun uppfærsluferils sölu** (**Sala og markaðssetning \> Tímabilsverk \> Hreinsun \> Hreinsun uppfærsluferils sölu**) keyrð eins og áður en með betri afköstum og að hámarki í 2 klukkustundir. Þetta þýðir að hún þarf kannski að keyra nokkrum sinnum til að hreinsa öll gögn fyrir tiltekinn varðveislutímaramma.

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Sala og markaðssetning*
- **Heiti eiginleika:** *Endurbætur á afköstum hreinsunar á söluferli*

### <a name="clean-up-sales-update-history-based-on-age"></a>Hreinsa uppfærsluferil sölu eftir aldri

Með eiginleikanum *Hreinsa uppfærsluferil sölu eftir aldri* er hægt að tilgreina hámarksaldur færsla þegar *Hreinsa sögu söluuppfærslna* er keyrt. Eldri færslum verður eytt. Þessi eiginleiki er gagnlegur þegar þú setur upp verkefni sem á að keyra reglulega, því aldurinn er alltaf reiknaður út miðað við þann dag sem verkið er keyrt. Ef þessi aðgerð er ekki notuð er aðeins hægt að velja ákveðna dagsetningu fyrir elstu færslurnar.

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Hreinsa uppfærsluferil sölu eftir aldri* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Setja upp og raða reglubundnu hreinsunarverkefni fyrir sölusögu

Til að setja upp og tímasetja *Hreinsun söluferlis* reglubundið verkefni skal fylgja þessum skrefum.

1. Greina þarf rekstur til að ákvarða hversu marga daga af sögulegum sölupöntunum og birtingargögnum verður að geyma. Við mælum yfirleitt með því að þú framkvæmir hreinsunina á þriggja mánaða fresti og að hámarki á sex mánaða fresti.
1. Farið í **Sala og markaðssetning \> Reglubundin verk \> Hreinsun \> Hreinsa sögu söluuppfærslna cleanup**.
1. Í svarglugganum **Hreinsa sögu söluuppfærslna** í flýtiflipanum **Færibreytur** skal stilla eftirfarandi reiti.

    - **Hreinsa** – Veljið eitt af eftirfarandi gildum til að tilgreina hvers konar færslur á að hreinsa:

        - **Keyrt** – Eyða aðeins skrám sem hafa verið fullunnnar. Þar sem ólíklegt er að þú hafir frekari not fyrir þessar skrár er þessi kostur öruggastur.
        - **Keyrt og með villum** – Eyða bæði fullunnum skrám og skrám þar sem villa kom upp. Þessi valkostur er oftast notaður. Þú gætir viljað skoða og jafnvel laga rangar skrár í stað þess að láta hreinsa þær sjálfkrafa. Mörg fyrirtæki velja hins vegar að hreinsa þessar færslur líka eftir um það bil mánuð því þær eiga líklega ekki lengur við eftir þann tíma.
        - **Allt** – Eyða keyrðum skrám, villum og biðskrám. Biðfærslur eru gildar en hafa ekki enn verið unnar að fullu. Í flestum tilfellum viltu ekki að þeim sé eytt sjálfkrafa. Í sumum tilvikum er þó hægt að eyða þeim sjálfkrafa að tilteknum tíma liðnum.

    - **Geyma færslur eftir aldri** – Tilgreindu hvort þú viljir hreinsa færslur miðað við aldur þeirra á þeim degi þegar verkefnið er keyrt eða eyða skrám sem voru búnar til fyrir ákveðinn dag. Ef þú ert að skipuleggja hreinsun sem endurtekið verkefni ættir þú að stilla þennan valkost á *Já*, því aldurinn er alltaf reiknaður miðað við þann dag sem verkið er keyrt.

        - Stillið þennan valkost á *Já* til að virkja reitinn **Hámarksaldur**. Tilgreinið í þessum reit hámarksaldur færsla sem á að geyma í hvert sinn sem verkið er keyrt. Reiturinn **Búið til** er hunsaður.
        - Stillið þennan valkost á *Nei* til að nota reitinn **Stofnað fram að**. Tilgreinið í þessum reit elsta stofndag færslu til að geyma þegar verkið er keyrt. Reiturinn **Hámarksaldur** er hunsaður.

    - **Stofnað fram að** – Þessi stilling á aðeins við þegar valkosturinn **Geyma færslur eftir aldri**“ er stilltur á *Nei*. Tilgreinið elsta stofndag skrár til að geyma þegar verkið er keyrt. Færslum sem voru búnar til fyrir þessa dagsetningu verður eytt.
    - **Hámarksaldur** – Þessi stilling á aðeins við þegar valkosturinn **Geyma færslur eftir aldri**“ er stilltur á *Já*. Tilgreinið hámarksaldur (í dögum) skrárinnar sem á að geyma í hvert sinn sem verkið er keyrt. Eldri færslum verður eytt.

1. Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft þetta er keyrt. Notaðu þessar stillingar til að framkvæma áætlunina sem þú ákvarðaðir í skrefi 1. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [runuvinnslu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum.

---
title: Tímasetja gagnahreinsun söluferils
description: Þessi grein lýsir því hvernig þú getur hjálpað til við að bæta afköst kerfisins með því að skipuleggja reglubundið hreinsunarverkefni Söluuppfærsluferils til að keyra með reglulegu millibili.
author: myvakalo
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1b2c9436fbb5020065f8f6ec30eedeca342d8aa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900826"
---
# <a name="schedule-sales-history-data-cleanup"></a>Tímasetja gagnahreinsun söluferils

[!include [banner](../includes/banner.md)]

Sem hluti af staðlaðri starfsemi sinni, Microsoft Dynamics 365 Supply Chain Management býr til og geymir uppfærsluuppfærsluupplýsingar sölusögu stöðugt. Með tímanum gæti mikið magn af úreltum sölusögugögnum safnast fyrir í kerfinu þínu. Þessi uppsöfnuðu gögn geta valdið afköstum og virknivandamálum þegar skjöl sem tengjast sölupöntunum eru bókuð. (Þessi skjöl innihalda sölupöntunarstaðfestingar, sölu fylgiseðla, sölutínslulista og reikninga). Þess vegna ættir þú að setja upp og tímasetja *Hreinsun söluuppfærslusögu* reglubundið verkefni til að keyra með reglulegu millibili. Þetta verkefni mun fjarlægja öll uppfærslugögn sölusögu sem ekki er lengur þörf á.

Ef þú notar *Hreinsun söluuppfærslusögu* reglubundið verkefni, mælum við með að þú kveikir á *Endurbætur á árangri í hreinsun sölusögu* eiginleiki, sem gerir verkefnið skilvirkara. (Engu að síður geturðu líka keyrt verkefnið án þess að virkja þennan eiginleika.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Kveiktu á hreinsunareiginleikum sölusögu

Til að setja upp og nota *Hreinsun söluuppfærslusögu* reglubundið verkefni ásamt öllum þeim eiginleikum sem lýst er í þessari grein, þú verður að virkja *Endurbætur á árangri í hreinsun sölusögu* og *Hreinsaðu upp söluuppfærsluferil byggt á aldri* eiginleikar í Eiginleikastjórnun, eins og lýst er í eftirfarandi undirköflum.

### <a name="sales-history-cleanup-performance-improvements"></a>Afkastaendurbætur á hreinsun söluferils

Reglubundin runuvinnsla **Hreinsun uppfærsluferils sölu** getur tekið langan tíma ef hún er sjaldan keyrð í umhverfum þar sem er mikið um söluuppfærslur. Í þessum tilvikum geta *Endurbætur á afköstum hreinsunar á söluferli* eiginleikinn hjálpað til við að stytta keyrslutíma og bæta áreiðanleika.

Þessi eiginleiki bætir núverandi hreinsunarvinnslu á eftirfarandi hátt:

- Hann skiptir hreinsun í runur (hægt er að breyta runustærð í sérstillingum).
- Hann er keyrður að hámarki í 2 klukkustundir (hægt er að breyta tímalengd í sérstillingum).
- Ef mögulegt nýtir hann getu gagnagrunnsins til að lágmarka læsingu og forðast að sameina færslutöflur við hreinsun.

Eftir að eiginleikinn er virkjaður verður runuvinnslan **Hreinsun uppfærsluferils sölu** (**Sala og markaðssetning \> Tímabilsverk \> Hreinsun \> Hreinsun uppfærsluferils sölu**) keyrð eins og áður en með betri afköstum og að hámarki í 2 klukkustundir. Þetta þýðir að hún þarf kannski að keyra nokkrum sinnum til að hreinsa öll gögn fyrir tiltekinn varðveislutímaramma.

Kveikja þarf á þessum eiginleika í kerfinu til að hægt sé að nota hann. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Sala og markaðssetning*
- **Heiti eiginleika:** *Endurbætur á afköstum hreinsunar á söluferli*

### <a name="clean-up-sales-update-history-based-on-age"></a>Hreinsa uppfærsluferil sölu eftir aldri

The *Hreinsaðu upp söluuppfærsluferil byggt á aldri* eiginleiki gerir þér kleift að tilgreina hámarksaldur skráa sem á að halda þegar *Hreinsun söluuppfærslusögu* reglubundið verkefni er keyrt. Eldri skrám verður eytt. Þessi eiginleiki er gagnlegur þegar þú setur verkefnið upp til að keyra reglulega, því aldurinn er alltaf reiknaður miðað við dagsetninguna þegar verkefnið er keyrt. Ef þú notar ekki þennan eiginleika geturðu aðeins stillt ákveðna dagsetningu fyrir elstu skrárnar til að halda.

Kveikja þarf á þessum eiginleika í kerfinu til að hægt sé að nota hann. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Sala og markaðssetning*
- **Eiginleikaheiti:** *Hreinsaðu upp söluuppfærsluferil byggt á aldri*

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Settu upp og tímasettu reglubundið hreinsunarverkefni sölusögu

Til að setja upp og tímasetja *Hreinsun sölusögu* reglubundið verkefni, fylgdu þessum skrefum.

1. Greindu þarfir fyrirtækisins til að ákvarða hversu marga daga af sögulegum sölupöntunargögnum þú verður að geyma. Við mælum venjulega með því að þú keyrir hreinsunarverkefnið á þriggja mánaða fresti og að hámarki á sex mánaða fresti.
1. Fara til **Sala og markaðssetning \> Tímabundið verkefni \> Hreinsun \> Hreinsun söluuppfærslusögu**.
1. Í **Hreinsaðu upp söluuppfærslusögu** valmynd, á **Færibreytur** Flýtiflipi, stilltu eftirfarandi reiti:

    - **Hreinsaðu til** – Veldu eitt af eftirfarandi gildum til að tilgreina tegund skráa sem á að hreinsa til:

        - **Framkvæmt** – Eyddu aðeins skrám sem hafa verið fullunnar. Vegna þess að ólíklegt er að þú hafir frekari notkun á þessum gögnum er þessi valkostur öruggastur.
        - **Framkvæmt og rangt** – Eyða bæði fullunnnum skrám og skrám þar sem villa hefur átt sér stað. Þessi valkostur er oftast notaður. Þú gætir viljað skoða og jafnvel laga rangar skrár í stað þess að láta hreinsa þær sjálfkrafa. Hins vegar kjósa mörg fyrirtæki að hreinsa þessar skrár líka eftir um það bil mánuð, vegna þess að þær eru líklega ekki lengur viðeigandi fyrir þann tíma.
        - **Allt** – Eyða framkvæmdum, röngum og biðskrám. Biðfærslur eru gildar en hafa ekki enn verið unnar að fullu. Í flestum tilfellum vilt þú líklega ekki að þeim verði eytt sjálfkrafa. Hins vegar, í sumum tilfellum, gætirðu valið að láta eyða þeim sjálfkrafa eftir að ákveðinn tími er liðinn.

    - **Geymdu skrár byggðar á aldri** – Tilgreindu hvort þú vilt hreinsa upp færslur miðað við aldur þeirra á þeim degi þegar verkefnið er keyrt eða eyða færslum sem voru búnar til fyrir fasta dagsetningu. Ef þú ert að skipuleggja hreinsunina sem endurtekið verkefni, ættir þú að stilla þennan valkost á *Já*, vegna þess að aldurinn er alltaf reiknaður miðað við dagsetninguna þegar verkefnið er keyrt.

        - Stilltu þennan valkost á *Já* til að virkja **Hámarksaldur** sviði. Þú notar þennan reit til að tilgreina hámarksaldur skránna sem á að geyma í hvert skipti sem verkefnið er keyrt. The **Búið til til** reiturinn er hunsaður.
        - Stilltu þennan valkost á *Nei* til að virkja **Búið til til** sviði. Þú notar þennan reit til að tilgreina elstu stofnunardagsetningu gagna sem á að geyma þegar verkefnið er keyrt. The **Hámarksaldur** reiturinn er hunsaður.

    - **Búið til til** – Þessi stilling á aðeins við þegar **Geymdu skrár byggðar á aldri** valkostur er stilltur á *Nei*. Tilgreindu elstu stofnunardagsetningu gagna sem á að geyma þegar verkefnið er keyrt. Færslum sem voru búnar til fyrir þessa dagsetningu verður eytt.
    - **Hámarksaldur** – Þessi stilling á aðeins við þegar **Geymdu skrár byggðar á aldri** valkostur er stilltur á *Já*. Tilgreindu hámarksaldur (í dögum) skránna sem á að halda í hvert skipti sem verkefnið er keyrt. Eldri skrám verður eytt.

1. Á **Hlaupa í bakgrunni** Flýtiflipi, tilgreinið hvernig, hvenær og hversu oft verkefnið er keyrt. Notaðu þessar stillingar til að útfæra áætlunina sem þú ákvaðst í skrefi 1. Reitirnir virka alveg eins og þeir gera fyrir aðrar tegundir af [lotustörf](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í birgðakeðjustjórnun.
1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum.

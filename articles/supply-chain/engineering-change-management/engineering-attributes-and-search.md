---
title: Hönnunareigindir og leit að hönnunareigind
description: Þetta efnisatriði útskýrir hvernig hægt er að nota hönnunareigindir til að skilgreina alla eiginleika sem ekki eru staðlaðir til að tryggja að hægt sé að skrá öll gögn afurðarsniðmáts í kerfinu. Efnisatriðið útskýrir einnig hvernig hægt er að nota leit hönnunareigindar til að leita að afurðum með tilgreinda eiginleika á skjótan hátt.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a4f31af3f76c1af6a0f5546955e810bd1cca375
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430791"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Hönnunareigindir og leit að hönnunareigind

[!include [banner](../includes/banner.md)]

Til að tryggja að hægt sé að skrá öll gögn afurðarsniðmáts í kerfinu ætti að nota hönnunareigindir til að tilgreina alla eiginleika sem eru ekki staðlaðir. Síðan er hægt að nota leit að hönnunareigindum til að leita að afurðum á auðveldan hátt miðað við tilgreinda eiginleika.

## <a name="engineering-attributes"></a>Hönnunareigindir

Yfirleitt hafa hönnunarafurðir fjölda eiginleika sem verður að fanga. Þó að hægt sé að skrá suma eiginleikana með því að nota stöðluð afurðarsvæði er einnig hægt að stofna nýjar hönnunareigindir eftir þörfum. Hægt er að skilgreina eigin *hönnunareigindir* og gera þær hluta af afurðarskilgreiningu.

### <a name="create-engineering-attributes-and-attribute-types"></a>Búa til hönnunareigindir og gerðir eiginda

Hver hönnunareigind verður að tilheyra *gerð eigindar*. Slíkt skilyrði er til staðar því hver hönnunareigind verður að hafa *gagnagerð* sem skilgreinir gerðir gildanna sem slík eigind getur falið í sér. Gerð hönnunareigindar getur verið stöðluð (eins og t.d. frjáls texti, heiltala eða tugabrot) eða sérstillt gerð (eins og texti sem inniheldur sérstakt mengi gilda sem er hægt að velja úr). Hægt er að nota aftur hverja gerð eiginda með hvaða fjölda hönnunareiginda sem er.

#### <a name="set-up-engineering-attribute-types"></a>Setja upp gerð hönnunareiginda

Fylgdu eftirfarandi skrefum til að skoða, búa til eða breyta gerð hönnunareigindar.

1. Opnaðu **Umsjón hönnunarbreytinga \> Uppsetning \> Eigindir \> Gerðir eiginda**.
1. Veljið fyrirliggjandi gerð eigindar til að breyta henni, eða veljið **Nýtt** á aðgerðasvæðinu til að búa til nýja gerð.
1. Stilltu eftirfarandi reiti:

    - **Heiti eigindargerðar** - Færið inn heiti fyrir gerð einingarinnar.
    - **Gerð** – Veldu staðlaða gerð gagna (*Gjaldmiðill*, *Dagsetning og tími*, *Tugabrot*, *Heiltala*, *Texti*, *Boole-gildi* eða *Tilvísun*).
    - **Fastur listi** – Þessi valkostur er aðeins tiltækur ef svæðið **Gerð** er stillt á *Texti*. Stillið svæðið á *Já* til að skilgreina sértæk gildi fyrir eigindir af þessari gerð. Í þessu tilvikum er fellilisti stofnaður. Þú notar flýtiflipann **Gildi** til að búa til gildin sem eru tiltæk fyrir þessa gerð eigindar. Stillið þennan valkost á *Nei* til að gera notendum kleift að færa inn hvaða gildi sem er. Í þessu tilviki er innsláttarsvæði búið til.
    - **Gildissvið** – Þessi valkostur er aðeins í boði ef þú stillir svæðið **Gerð** á *Heiltölu*, *Tugabrot* eða *Gjaldmiðil*. Stillið svæðið á *Já* til að búa til lágmarks- og hámarksgildi sem verða samþykkt sem gildi fyrir þessa gerð. Notaðu flýtiflipann **Svið** til að búa til lágmarks-og hámarksgildin og (fyrir gjaldmiðil) gjaldmiðilinn sem á við um mörkin sem þú færðir inn. Stilltu þennan valkost á *Nei* til að samþykkja hvaða gildi sem er. 
    - **Mælieining** – Þetta svæði er aðeins tiltækt ef þú stillir svæðið **Gerð** á *Heiltölu* eða *Tugabrot*. Velja mælieiningu sem gildir fyrir þessa gerð eigindar. Ef engin eining er nauðsynleg skal hafa þennan reit auðan.

#### <a name="set-up-engineering-attributes"></a>Setja upp hönnunareigindir

Til að skoða, stofna eða breyta hönnunareigind skal fylgja þessum skrefum.

1. Opnaðu **Umsjón hönnunarbreytinga \> Uppsetning \> Eigindir \> Hönnunareigindir**.
1. Veldur núverandi eigind á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýja eigind.
1. Stilltu eftirfarandi reiti:

    - **Heiti** - Færið inn heiti fyrir eigindina. Þetta heiti birtist aðeins á síðunni **Hönnunareigindir**. Alls staðar annars staðar í kerfinu birtist gildi svæðisins **Stutt heiti** yfirleitt til að auðkenna eigindina.
    - **Gerð eigindar** – Veldu gerð eigindar sem þú skilgreindir í fyrri hlutanum.
    - **Stutt heiti** – Sláðu inn heiti til að auðkenna eigindina í kerfinu (nema á síðunni **Hönnunareigindir**). 
    - **Lýsing** - Færið inn lýsingu á eigindinni.
    - **Hjálpartexti** -Sláðu inn hjálpartexta til að aðrir notendur viti hvað eigindin er notuð fyrir.
    - **Sjálfgefið gildi** – Sláðu inn sjálfgefið gildi fyrir eigindina. Valkostirnir sem eru sýndir fara eftir gerð eigindarinnar sem þú valdir.
    - **Gjaldmiðill** – Þegar valin gerð eigindar er gjaldmiðill skal velja gjaldmiðilinn sem eigindin tekur við og birtir gildin.

1. Þegar valin gerð eigindar er heiltala eða tugabrot birtist flýtiflipinn **Svið**. Á þessum flýtiflipa skal stilla eftirfarandi reiti eftir þörfum:

    - **Vikmarkaaðgerð** – Veldu hvernig kerfið skal bregðast við þegar notandi slær inn gildi utan tilgreindra marka. Ef valið er *Viðvörun* er viðvörun sýnd, en notandinn getur vistað gildið. Ef valið er *Ekki leyft* er viðvörun sýnd og ekki er hægt að vista gildið fyrr en notandinn breytir því.
    - **Lágmark** – Færið inn ráðlagt gildi eða samþykkt gildi.
    - **Hámark** – Færið inn ráðlagt hámarksgildi eða samþykkt gildi.

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Tengja hönnunareigindir við flokka hönnunarafurða

Tilteknar hönnunareigindir eiga við um allar afurðir, en aðrar eiga sérstaklega við um tilteknar afurðir eða afurðarflokka. T.d. eru rafmagnseigindir ekki áskildar fyrir vélrænar afurðir. Þar af leiðandi getur þú sett upp *flokka hönnunarafurða*. Flokkur hönnunarafurða myndar tengingu hönnunareiginda sem verða að vera hluti skilgreininga á vörum sem tilheyra áðurnefndum flokki. Þú getur einnig tilgreint hvaða hönnunareigindir eru áskildar og hvort að sjálfgildi sé til staðar.

Frekari upplýsingar um hvernig á að vinna með flokka hönnunarafurða, þ.m.t. upplýsingar um hvernig eigindir eru tengdar við flokka er að finna í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

### <a name="set-values-for-engineering-attributes"></a>Stilla gildi fyrir hönnunareigindir

Hönnunareigindir sem eru tengdar við flokk hönnunarafurða eru sýndar þegar ný hönnunarafurð er búin til miðað við flokkinn sem um ræðir. Á þeim tíma er hægt að setja upp gildi fyrir eigindir. Síðar er hægt að breyta þessum gildum á síðunni **Hönnunarútgáfa** eða sem hluta af umsjón hönnunarbreytinga í pöntun hönnunarbreytinga. Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).

### <a name="create-an-engineering-product"></a>Búa til hönnunarafurð

Opnaðu síðuna **Útgefnar afurðir** til að búa til hönnunarafurð. Svo, á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Ný**, skal velja **Hönnunarafurð**.

Tilgreina verður hönnunartegund sem afurðin tilheyrir. Flokkurinn stillir öll sjálfgefin gildi og eiginleika afurðarinnar. Einnig eru allar eigindir sem eiga við afurðina stilltar. Eftir að flokkurinn er valinn verða gildin stillt fyrir eigindir. Þá er hægt að breyta þessum gildum.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Leita að afurðum með því að nota gildi hönnunareigindar

Þú getur notað leit hönnunareiginda til að leita af afurðum eftir gildum hönnunareiginda slíkra afurða. Þess vegna er auðvelt að finna hönnunarafurðir út frá einkennum þeirra. Hægt er að leita í afurðum sem tilheyra flokki afurðategundar eða leita í öllum hönnunarafurðum.

Leit er tiltæk á gagnasíðum afurðarsniðmáts og færslutengdum atriðum í kerfinu eins og sölupöntunum. Fyrir færslutengdar-vöru er hægt að nota síðuna **Leita að hönnunareigind** til að leita að afurð. Síðan getur þú notað hnappinn **Bæta við sem nýrri línu** til að bæta afurðinni við sölupöntunarlínurnar. Einnig er hægt að bæta afurðum í leitarniðurstöðum beint við pöntunina.

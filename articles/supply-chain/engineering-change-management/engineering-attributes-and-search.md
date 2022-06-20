---
title: Hönnunareigindir og leit að hönnunareigind
description: Þessi grein útskýrir hvernig þú getur notað verkfræðieiginleika til að tilgreina alla óstöðluðu eiginleika, til að tryggja að hægt sé að skrá öll afurðaraðalgögn í kerfið. Efnisatriðið útskýrir einnig hvernig hægt er að nota leit hönnunareigindar til að leita að afurðum með tilgreinda eiginleika á skjótan hátt.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4b25ab0bfda08b7aa091de8c6833007c586b9c87
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852564"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Hönnunareigindir og leit að hönnunareigind

[!include [banner](../includes/banner.md)]

Til að tryggja að hægt sé að skrá öll gögn afurðarsniðmáts í kerfinu ætti að nota hönnunareigindir til að tilgreina alla eiginleika sem eru ekki staðlaðir. Síðan er hægt að nota leit að hönnunareigindum til að leita að afurðum á auðveldan hátt miðað við tilgreinda eiginleika.

## <a name="create-engineering-attributes-and-attribute-types"></a>Búa til hönnunareigindir og gerðir eiginda

Yfirleitt hafa hönnunarafurðir fjölda eiginleika sem verður að fanga. Þó að hægt sé að skrá suma eiginleikana með því að nota stöðluð afurðarsvæði er einnig hægt að stofna nýjar hönnunareigindir eftir þörfum. Hægt er að skilgreina eigin *hönnunareigindir* og gera þær hluta af afurðarskilgreiningu.

Hver hönnunareigind verður að tilheyra *gerð eigindar*. Slíkt skilyrði er til staðar því hver hönnunareigind verður að hafa *gagnagerð* sem skilgreinir gerðir gildanna sem slík eigind getur falið í sér. Gerð hönnunareigindar getur verið stöðluð (eins og t.d. frjáls texti, heiltala eða tugabrot) eða sérstillt gerð (eins og texti sem inniheldur sérstakt mengi gilda sem er hægt að velja úr). Hægt er að nota aftur hverja gerð eiginda með hvaða fjölda hönnunareiginda sem er.

### <a name="set-up-engineering-attribute-types"></a>Setja upp gerð hönnunareiginda

Fylgdu eftirfarandi skrefum til að skoða, búa til eða breyta gerð hönnunareigindar.

1. Opnaðu **Umsjón hönnunarbreytinga \> Uppsetning \> Eigindir \> Gerðir eiginda**.
1. Veljið fyrirliggjandi gerð eigindar til að breyta henni, eða veljið **Nýtt** á aðgerðasvæðinu til að búa til nýja gerð.
1. Stilltu eftirfarandi reiti:

    - **Heiti eigindargerðar** - Færið inn heiti fyrir gerð einingarinnar.
    - **Gerð** – Veldu staðlaða gerð gagna (*Gjaldmiðill*, *Dagsetning og tími*, *Tugabrot*, *Heiltala*, *Texti*, *Boole-gildi* eða *Tilvísun*).
    - **Fastur listi** – Þessi valkostur er aðeins tiltækur ef svæðið **Gerð** er stillt á *Texti*. Stillið svæðið á *Já* til að skilgreina sértæk gildi fyrir eigindir af þessari gerð. Í þessu tilvikum er fellilisti stofnaður. Þú notar flýtiflipann **Gildi** til að búa til gildin sem eru tiltæk fyrir þessa gerð eigindar. Stillið þennan valkost á *Nei* til að gera notendum kleift að færa inn hvaða gildi sem er. Í þessu tilviki er innsláttarsvæði búið til.
    - **Gildissvið** – Þessi valkostur er aðeins í boði ef þú stillir svæðið **Gerð** á *Heiltölu*, *Tugabrot* eða *Gjaldmiðil*. Stillið svæðið á *Já* til að búa til lágmarks- og hámarksgildi sem verða samþykkt sem gildi fyrir þessa gerð. Notaðu flýtiflipann **Svið** til að búa til lágmarks-og hámarksgildin og (fyrir gjaldmiðil) gjaldmiðilinn sem á við um mörkin sem þú færðir inn. Stilltu þennan valkost á *Nei* til að samþykkja hvaða gildi sem er. 
    - **Mælieining** – Þetta svæði er aðeins tiltækt ef þú stillir svæðið **Gerð** á *Heiltölu* eða *Tugabrot*. Velja mælieiningu sem gildir fyrir þessa gerð eigindar. Ef engin eining er nauðsynleg skal hafa þennan reit auðan.

### <a name="set-up-engineering-attributes"></a>Setja upp hönnunareigindir

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

### <a name="engineering-attribute-inheritance"></a>Erfðir hönnunareigindar

Fyrir afurðarskipulag á borð við uppskriftir eða formúlur er hægt að flytja valdar eigindir frá undirvörum upp í yfirvörur. Hægt er að líta á þetta ferli sem „öfugar erfðir“.

#### <a name="turn-engineering-attribute-inheritance-on-or-off"></a>Kveiktu eða slökktu á arfleifð verkfræðieiginda

Þessi eiginleiki krefst þess að bæði *Verkfræðibreytingastjórnun* og *Bætt eigindaarf fyrir verkfræðibreytingastjórnun* kveikt er á eiginleikum fyrir kerfið þitt. Fyrir upplýsingar um hvernig á að kveikja eða slökkva á þessum eiginleikum, sjá [Yfirlit yfir verkfræðibreytingastjórnun](product-engineering-overview.md).

#### <a name="attribute-inheritance-example"></a>Dæmi um erfða eigind

Fyrir matvæli á borð við gulrótarköku verður kerfið að skrá alla ofnæmisvalda sem afurðin inniheldur. Gulrótarkökuna er hægt að sýna í kerfinu sem hönnunarafurð með formúlu. Þessi formúla inniheldur innihaldsefni gulrótarkökunnar, svo sem hveiti, mjólk, gulrætur og hnetur. Í þessu dæmi útvegar fyrirtækið tvær gerðir af gulrótarköku: eina sem inniheldur laktósa og aðra sem inniheldur ekki laktósa.

Kakan sem inniheldur laktósa hefur eftirfarandi eigindir á stigi innihaldsefna:

- Innihaldsefnið „hveiti“: eigind „glúten“ = já
- Innihaldsefnið „mjólk“: eigind „laktósi“ = já
- Innihaldsefnið „hnetur“: eigind „hnetur“ = já

Kakan sem inniheldur ekki laktósa notar laktósafría mjólk og er með eftirfarandi eigindir á stigi innihaldsefna:

- Innihaldsefnið „hveiti“: eigind „glúten“ = já
- Innihaldsefnið „mjólk“: eigind „laktósi“ = nei
- Innihaldsefnið „hnetur“: eigind „hnetur“ = já

Þar sem þessar afurðir eru að mestu leyti eins gæti verið sniðugt að flytja þessar eigindir úr undireiningunni (afbrigðunum tveimur) yfir í yfirafurðina (gulrótarkökuna í grunninn). Til að innleiða þessa „öfugu erfðir“ getur þú nota virknina *Erfðaeigind*. Þessi virkni er skilgreind fyrir hverja [hönnunarútgáfu](engineering-versions-product-category.md).

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Tengja hönnunareigindir við flokka hönnunarafurða

Tilteknar hönnunareigindir eiga við um allar afurðir, en aðrar eiga sérstaklega við um tilteknar afurðir eða afurðarflokka. T.d. eru rafmagnseigindir ekki áskildar fyrir vélrænar afurðir. Þar af leiðandi getur þú sett upp *flokka hönnunarafurða*. Flokkur hönnunarafurða myndar tengingu hönnunareiginda sem verða að vera hluti skilgreininga á vörum sem tilheyra áðurnefndum flokki. Þú getur einnig tilgreint hvaða hönnunareigindir eru áskildar og hvort að sjálfgildi sé til staðar.

Frekari upplýsingar um hvernig á að vinna með flokka hönnunarafurða, þ.m.t. upplýsingar um hvernig eigindir eru tengdar við flokka er að finna í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Stilla eigindagildi fyrir hönnunareigindir

Hönnunareigindir sem eru tengdar við flokk hönnunarafurða eru sýndar þegar ný hönnunarafurð er búin til miðað við flokkinn sem um ræðir. Á þeim tíma er hægt að setja upp gildi fyrir eigindir. Síðar er hægt að breyta þessum gildum á síðunni **Hönnunarútgáfa** eða sem hluta af umsjón hönnunarbreytinga í pöntun hönnunarbreytinga. Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Búa til hönnunarafurð

Opnaðu síðuna **Útgefnar afurðir** til að búa til hönnunarafurð. Svo, á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Ný**, skal velja **Hönnunarafurð**.

Tilgreina verður hönnunartegund sem afurðin tilheyrir. Flokkurinn stillir öll sjálfgefin gildi og eiginleika afurðarinnar. Einnig eru allar eigindir sem eiga við afurðina stilltar. Eftir að flokkurinn er valinn verða gildin stillt fyrir eigindir. Þá er hægt að breyta þessum gildum.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Leita að afurðum með því að nota gildi hönnunareigindar

Þú getur notað leit hönnunareiginda til að leita af afurðum eftir gildum hönnunareiginda slíkra afurða. Þess vegna er auðvelt að finna hönnunarafurðir út frá einkennum þeirra. Hægt er að leita í afurðum sem tilheyra flokki afurðategundar eða leita í öllum hönnunarafurðum.

Leit er tiltæk á gagnasíðum afurðarsniðmáts og færslutengdum atriðum í kerfinu eins og sölupöntunum. Fyrir færslutengdar-vöru er hægt að nota síðuna **Leita að hönnunareigind** til að leita að afurð. Síðan getur þú notað hnappinn **Bæta við sem nýrri línu** til að bæta afurðinni við sölupöntunarlínurnar. Einnig er hægt að bæta afurðum í leitarniðurstöðum beint við pöntunina.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

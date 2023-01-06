---
title: Sniðmát tekjuskiptingar í áskriftargreiðslur
description: Í þessari grein er útskýrt hvernig á að setja upp sniðmát tekjuskiptingar fyrir vörur sem eru seldar sem búnt.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904760"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Sniðmát tekjuskiptingar í áskriftargreiðslur

Notið síðuna **Sniðmát tekjuskiptingar** til að setja upp sniðmát fyrir tekjuskiptingu. Tekjuskipting samanstendur af yfirvöru sem er með undirvöru. Þessi gerð vöru er oft seld til viðskiptavina sem ein vara eða í búnti.

Til dæmis er hægt að búa til tölvuvöru á eftirfarandi hátt:

- **Yfirvara:** Áskriftarsilfur
- **Línuvörur (undireining):**

    - Stuðningur
    - Viðhald
    - Leyfi

Hafðu eftirfarandi takmarkanir í huga þegar yfirhlutur er stofnaður:

- Aðeins er hægt að tilgreina vöru sem yfirvöru í eitt skipti.
- Hægt er að velja yfirvöruna sem undirvöru í sama sniðmáti.
- Gilt sniðmát verður að innihalda minnst eina undirvöru.
- Hægt er að tilgreina vöru sem undirvöru fyrir fleiri en eina búntvöru.
- Tengsl yfireiningar og undireiningar verða að vera einkvæm.

## <a name="create-a-parent-item-that-has-child-items"></a>Stofna yfirvöru sem er með undirvöru

Fylgið eftirfarandi skrefum til að stofna yfirvöru sem er með undirvöru

1. Á síðunni **Sniðmát tekjuskiptingar** skal velja **Nýtt**.
1. Veljið yfirvöru á svæðinu **Yfirvara**. Reiturinn **Afbrigðisnúmer** er uppfærður sjálfkrafa. Hægt er að breyta gildinu eftir þörfum.
1. Í svæðinu **Úthlutunaraðferð** skal velja úthlutunaraðferð.
1. Veldu **Bæta við** á listanum **Hlutir vöru** til að bæta við undirvörum.
1. Ef valið er **Prósenta** í reitnum **Úthlutunaraðferð** skal tilgreina prósentu í reitnum **Prósenta**.

    - Ef valið er **Jöfn upphæð** í reitnum **Úthlutunaraðferð** er reiturinn **Prósenta** sjálfkrafa uppfærður þannig að hver vara sé með eins prósentu
    - Ef valið er **Breytileg upphæð**, **Núll yfirupphæð** eða **Núllupphæð** í reitnum **Úthlutunaraðferð** helst gildið í reitnum **Prósenta** áfram **0** (núll) og er ekki hægt að breyta.

1. Veldu **Vista**.

## <a name="fields"></a>Svæði

Síðan **Sniðmát tekjuskiptingar** inniheldur eftirfarandi reiti.

| Svæði | Lýsing |
|-------|-------------|
| Yfirvara | Veldu vörunúmer. Þessi vara verður yfirvaran fyrir búntvöruna sem þú stofnar. |
| Afurðarheiti | Afurðarheitið. |
| Úthlutunaraðferð | <p>Velja úthlutunaraðferð:</p><ul><li>**Jöfn upphæð** – Úthlutunarprósenturnar eru reiknaðar sjálfkrafa og skipt jafnt á allar vörurnar í sniðmátinu.</li><li>**Prósenta** – Hægt er að tilgreina prósentuupphæð fyrir úthlutun. Samtala allra prósenta verður að vera jöfn 100.</li><li>**Breytileg upphæð** – Undirvörur sem bætt er við eru með nettóupphæðina 0 (núll). Tilgreina verður verð á undirvörum á færslustigi.</li><li>**Núllupphæð** – Yfirvaran heldur einingarverði sínu og nettóupphæð. Allar undirvörur eru með nettóupphæðina 0 (núll).</li><li>**Núll yfirupphæð** – Yfirvaran er með fasta nettóupphæð 0 (núll). Allar undirvörur eru meðhöndlaðar eins og hefðbundnar vörur. Engin villuleit er gerð til að staðfesta að summa upphæða undirvöru séu jafnt og upphæð yfirvöru.</li></ul> |
| **Vöruhlutir** | |
| Hlutur vöru | Veldu vörunúmer. Þetta vara er undirvara. |
| Númer vöruvíddasamsetningar | Veldu afbrigðisnúmerið fyrir vöruna. |
| Afurðarheiti | Afurðarheitið. |
| Prósenta | <p>Úthlutunarprósenta áfangans:</p><ul><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Prósenta** er hægt að tilgreina prósentuna.</li><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Jöfn upphæð** er prósentan sjálfkrafa reiknuð þannig að hver vara í sniðmátinu sé með jafna prósentu.</li><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Breytileg upphæð**, **Núll yfirupphæð** eða **Núllupphæð** er prósentan 0 (núll) og ekki er hægt að breyta henni.</li></ul><p>Gildið í þessum reit getur verið hvaða jákvæða tala sem er á milli 0 (núll) og 100. Samtala allra hlutfalla verður að vera jöfn 100.</p> |
| Prósentusamtala | <p>Summan af gildum í dálknum **Hlutfall**.</p><ul><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Jöfn upphæð** eða **Prósentu** verður summa allra prósentanna að vera jafnt og 100.</li><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Breytileg upphæð**, **Núll yfirupphæð** eða **Núllupphæð** er heildarprósentan 0 (núll).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Tekjuskipting í sölupöntun

Fylgdu eftirfarandi skrefum til að búa til sölupöntun með vöru sem er sett upp fyrir tekjuskiptingu.

1. Stofnið sölupöntun á síðunni **Sölupöntun**.
2. Á línunni fyrir hverja vöru sem sett er upp fyrir tekjuskiptingu skal velja gátreitinn **Tekjuskipting**. Sú vara verður yfirvara. Ef sniðmátið er þegar uppsett birtast undirvörurnar sjálfkrafa á listanum.
3. Til að bæta við fleiri undireiningum skal velja **Bæta við undireiningu tekjuskiptingar** og velja undireininguna sem á að bæta við.
4. Vista röðina.

## <a name="revenue-split-with-billing-schedules"></a>Tekjuskipting með greiðsluáætlunum

Til að búa til greiðsluáætlun sem er með vöru sem er sett upp fyrir tekjuskiptingu skal fylgja þessum skrefum.

1. Á síðunni **Allar/Virkar greiðsluáætlanir** skalt stofna greiðsluáætlun.
2. Á línunni fyrir hverja vöru sem sett er upp fyrir tekjuskiptingu skal velja gátreitinn **Tekjuskipting**. Sú vara verður yfirvara. Ef sniðmátið er þegar uppsett birtast undirvörurnar sjálfkrafa á listanum.
3. Til að bæta við fleiri undireiningum skal velja **Bæta við undireiningu tekjuskiptingar** og velja undireininguna sem á að bæta við.
4. Haltu áfram með skrefin til að vinna með greiðsluáætlunina.

> [!NOTE]
> Ef valkosturinn **Stofna tekjuskiptingu sjálfkrafa** er stilltur á **Já** á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** gerast eftirfarandi aðgerðir:
>
> - Ef vörulínan er sett upp sem yfireining í sniðmáti tekjuskiptingar er gátreiturinn **Tekjuskipting** sjálfkrafa valinn.
> - Undirvörurnar eru sjálfkrafa færðar inn í sölupöntun eða greiðsluáætlunarlínu.
>
> Ef valkosturinn **Stofna tekjuskiptingu sjálfkrafa** er stilltur á **Nei** er hegðunin eins og henni var lýst hér á undan.

## <a name="additional-revenue-split-information"></a>Viðbótarupplýsingar um tekjuskiptingu

Þegar þú bætir við vöru sem tilheyrir tekjuskiptingu skaltu hafa eftirfarandi upplýsingar í huga: 

- Ekki er hægt að fresta yfirupphæðinni.
- Gildi upphafsdagsetningar, lokadagsetningar, magns, einingar, svæðis og vöruhúss fyrir undireiningar byggja á yfireiningum. Ekki er hægt að breyta þessum gildum fyrir undirvörur. Allar breytingar verða að vera gerðar á yfirvörunni. 
- Verðaðferðin er **Fast** og ekki er hægt að breyta henni.
- Hægt er að bæta við eða fjarlægja undirvörur.
- Yfir- og undirvörur verða að nota sama vöruflokkinn. 
- Undirvörur geta haft eina af eftirfarandi uppsetningum:

    - Reitirnir **Greiðslutíðni** og **Greiðslumillibil** eru stilltir á sama gildið og yfireiningin. 
    - Reiturinn **Greiðslutíðni** er stilltur á **Einu sinni**. Í þessu tilfelli er reiturinn **Greiðslumillibil** sjálfkrafa stilltur á **1**. 

- Samtala nettóupphæða undirvaranna jafngildir yfirupphæðinni. Ef úthlutunaraðferðin er **Núllupphæðir** eru bæði summa upphæða undireiningar og yfireiningar 0 (núll). 

    > [!NOTE]
    > Ef úthlutunaraðferðin er **Núll yfirupphæð** er (ekki núll) summa undireininga ekki jafnt og upphæð yfireiningar, sem er 0 (núll). Þessi úthlutunaraðferð er notuð í innri tilgangi þannig að starfsmenn geti séð undireiningarnar. Viðskiptavinir geta þó aðeins séð yfirvöruna.

- Ef gerð margþátta ráðstöfunar fyrir sölupöntun er **Einfalt** er samsvarandi færslulína margþátta tekjuúthlutunar stofnuð þegar yfir- og undireiningum er bætt við. 
- Ef úthlutunaraðferðin fyrir tekjuskiptingu er **Jöfn upphæð** og upphæð yfireiningar er breytt eru upphæðirnar endurreiknaðar fyrir allar undirlínur. 
- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Breytileg upphæð** kemur eftirfarandi hegðun fram:

    - Nettóupphæð yfirvörunnar kemur fram í dálknum **Yfirupphæð**. Hægt er að breyta þessu gildi. Aftur á móti eru einingaverðið, nettóupphæðin og afslátturinn 0 (núll) og ekki hægt að breyta því.
    - Einingarverð undirvara er 0 (núll). Hægt er að breyta einingarverðinu eða nettóupphæðinni. Þegar þú breytir einu gildi uppfærist hitt gildið sjálfkrafa.

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Prósenta** kemur eftirfarandi hegðun fram:

    - Nettóupphæð yfirvörunnar kemur fram í dálknum **Yfirupphæð**. Hægt er að breyta þessu gildi. Aftur á móti eru einingaverðið, nettóupphæðin og afslátturinn 0 (núll) og ekki hægt að breyta því. 
    - Nettóupphæð undirvöru er reiknuð sem *Prósenta* &times; *Yfirupphæð*.

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Jöfn upphæð** kemur eftirfarandi hegðun fram:

    - Nettóupphæð yfirvörunnar kemur fram í dálknum **Yfirupphæð**. Hægt er að breyta þessu gildi. Aftur á móti eru einingaverðið, nettóupphæðin og afslátturinn 0 (núll) og ekki hægt að breyta því. 
    - Nettóupphæð undireininga er reiknuð út með því að deila upphæð yfireiningar jafnt niður á allar undireiningar. 
    - Ef undireiningar eru fjarlægðar eða þeim bætt við er nettóupphæð og einingarverð endurreiknuð þannig að allar línur undireiningar séu með jafnar upphæðir. 
    - Ef ekki er hægt að skipta upphæð yfireiningar jafnt gæti nettóupphæð eða einingarverð síðustu undireiningar verið örlítið hærra eða minna en nettóupphæð og einingarverð hinna undireininganna. 

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Núll** kemur eftirfarandi hegðun fram:

    - Hægt er að breyta einingaverði, nettóupphæð og afslætti. Yfirupphæðin er 0 (núll) og henni er ekki hægt að breyta. 
    - Magn-, einingar-, svæðis- og vöruhússgildi undirvara er byggt á yfirvörunni. Ekki er hægt að breyta þessum gildum fyrir undirvörurnar. Allar breytingar verða að vera gerðar á yfirvörunni. 
    - Einingarverð og nettóverð undirvara er 0 (núll) og því er ekki hægt að breyta. 

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Núllupphæð yfireiningar** kemur eftirfarandi hegðun fram:

    - Einingarverð, yfirupphæð og nettóupphæð yfirvörunnar er 0 (núll).
    - Í greiðsluáætlun birtast línur undireiningar eins og ef þeim væri bætt við handvirkt og öll gildi eru uppfærð út frá völdum greiðsluáætlunarflokki. Hægt er að breyta þessum gildum. Fyrir undireiningar er hægt að nálgast valkostina **Hækkun og afsláttur** og **Ítarleg verðlagning** með því að nota reitina **Magn fært inn**, **Einingarverð**, **Afsláttur** og **Nettóupphæð** í **Skoða greiðsluupplýsingar**. 
    - Í sölupöntun eru undirlínurnar með afslátt og afsláttarprósentu 0 (núll). 
    - Hægt er að breyta greiðslutíðni yfir- og undireininga og hver lína getur verið með mismunandi tíðni. Yfireiningin er hins vegar sjálfkrafa uppfærð þannig að hún notar stystu tíðnina úr línum undireiningar. Tekjuskipting er til dæmis með tvær undireiningar, ein sem notar **Mánaðarlega** greiðslutíðni og önnur sem notar **Árlega** greiðslutíðni. Í þessu tilfelli er greiðslutíðni yfirvörunnar uppfærð í **Mánaðarlega**.

---
title: Sniðmát fyrir tekjuskiptingu í innheimtu áskriftar
description: Þetta efnisatriði útskýrir hvernig á að setja upp tekjuskiptingarsniðmát fyrir vörur sem eru seldar sem búntar.
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
ms.openlocfilehash: 5c2eb6c8e18770eb149c445f662ab7a90aad81a7
ms.sourcegitcommit: 367e323bfcfe41976e5d8aa5f5e24a279909d8ac
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2022
ms.locfileid: "8660515"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Sniðmát fyrir tekjuskiptingu í innheimtu áskriftar

Nota **Sniðmát fyrir skiptingu tekna** síðu til að setja upp sniðmát fyrir skiptingu tekna. Tekjuskipting samanstendur af yfirliði sem hefur undirliði. Þessi tegund af hlutum er oft seld til viðskiptavina sem einn hlutur eða búnt.

Til dæmis er hægt að búa til tölvuhlut á eftirfarandi hátt:

- **Foreldri atriði:** Áskrift Silfur
- **Línu (undir) atriði:**

    - Stuðningur
    - Viðhald
    - Leyfi

Þegar þú býrð til yfirlið skaltu hafa eftirfarandi takmarkanir í huga:

- Aðeins er hægt að tilgreina vöru sem yfirvöru einu sinni.
- Hægt er að velja yfirlið sem undiratriði í sama sniðmáti.
- Gilt sniðmát krefst að minnsta kosti eitt undiratriði.
- Hægt er að tilgreina vöru sem undirvöru fyrir fleiri en eina búntvöru.
- Hvert samband foreldra og barns verður að vera einstakt.

## <a name="create-a-parent-item-that-has-child-items"></a>Búðu til yfiratriði sem hefur undiratriði

Fylgdu þessum skrefum til að búa til yfirvöru sem hefur undiratriði.

1. Á **Sniðmát fyrir skiptingu tekna** síðu, veldu **Nýtt**.
1. Í **Foreldri atriði** reit, veldu yfirlið. The **Afbrigðisnúmer** reiturinn er sjálfkrafa uppfærður. Þú getur breytt gildinu eins og þú vilt.
1. Í **Úthlutunaraðferð** reit, veldu úthlutunaraðferð.
1. Í **Íhlutir** lista, veldu **Bæta við** til að bæta við barnahlutum.
1. Ef þú valdir **Hlutfall** í **Úthlutunaraðferð** reit, tilgreindu prósentu í **Hlutfall** sviði.

    - Ef þú valdir **Jöfn upphæð** í **Úthlutunaraðferð** sviði, the **Hlutfall** reiturinn er sjálfkrafa uppfærður þannig að hver hlutur hefur jafnt hlutfall.
    - Ef þú valdir **Breytileg upphæð**, **foreldri upphæð**, eða **Núll upphæð** í **Úthlutunaraðferð** sviði, gildi á **Hlutfall** reitur eftir **0** (núll) og er ekki hægt að breyta.

1. Veldu **Vista**.

## <a name="fields"></a>Svæði

The **Sniðmát fyrir skiptingu tekna** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|-------|-------------|
| Yfirvara | Veldu vörunúmer. Þessi vara verður yfirhlutur fyrir búnthlutinn sem þú býrð til. |
| Afurðarheiti | Vöruheitið. |
| Úthlutunaraðferð | <p>Veldu úthlutunaraðferð:</p><ul><li>**Jöfn upphæð** – Úthlutunarprósenturnar eru sjálfkrafa reiknaðar og skipt jafnt á milli allra atriða í sniðmátinu.</li><li>**Hlutfall** – Hægt er að tilgreina prósentuupphæð fyrir úthlutunina. Summa allra prósenta verður að vera 100.</li><li>**Breytileg upphæð** – Undirliðir sem bætt er við hafa nettóupphæð 0 (núll). Verð á undirvörum verður að tilgreina á færslustigi.</li><li>**Núll upphæð** – Móðurliður heldur einingaverði sínu og nettóupphæð. Allir undirliðir hafa nettóupphæðina 0 (núll).</li><li>**Núll foreldri upphæð** – Móðurliðurinn hefur fasta nettófjárhæð 0 (núll). Meðhöndlað er með alla undirliði eins og staðlaða hluti. Engin fullgilding er gerð til að sannreyna að summan af fjárhæðum undirliðar sé jöfn upphæð yfirliðar.</li></ul> |
| **Vöruhlutir** | |
| Hlutur vöru | Veldu vörunúmer. Þessi vara er undirhlutur. |
| Númer vöruvíddasamsetningar | Veldu afbrigðisnúmer fyrir hlutinn. |
| Afurðarheiti | Vöruheitið. |
| Prósenta | <p>Úthlutunarprósenta fyrir áfangann:</p><ul><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Hlutfall**, þú getur tilgreint hlutfallið.</li><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Jöfn upphæð**, prósentan er sjálfkrafa reiknuð þannig að hvert atriði í sniðmátinu hefur jafnt hlutfall.</li><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Breytileg upphæð**, **foreldri upphæð**, eða **Núll upphæð**, prósentan er 0 (núll) og ekki er hægt að breyta því.</li></ul><p>Gildi þessa reits getur verið hvaða jákvæð tala sem er á milli 0 (núll) og 100. Summa allra prósentanna verður að vera 100.</p> |
| Prósentusamtala | <p>Summa gilda í **Hlutfall** dálki.</p><ul><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Jöfn upphæð** eða **Hlutfall**, summan af öllum prósentum verður að vera 100.</li><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Breytileg upphæð**, **foreldri upphæð**, eða **Núll upphæð**, heildarhlutfallið er 0 (núll).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Tekjuskipting á sölupöntun

Til að stofna sölupöntun sem hefur vöru sem er sett upp fyrir tekjuskiptingu skal fylgja þessum skrefum.

1. Á **Sölupöntun** síðu, búðu til sölupöntun.
2. Á línunni fyrir hvern lið sem er settur upp fyrir tekjuskiptingu skal velja **Tekjuskipting** gátreit. Sá hlutur verður yfirliður. Ef sniðmátið er þegar sett upp birtast undirhlutirnir sjálfkrafa á listanum.
3. Til að bæta við fleiri undirhlutum skaltu velja **Bættu við tekjuskiptu barni**, og veldu undirliðið sem þú vilt bæta við.
4. Vistaðu pöntunina.

## <a name="revenue-split-with-billing-schedules"></a>Tekjum skipt með innheimtuáætlunum

Til að búa til innheimtuáætlun sem hefur vöru sem er sett upp fyrir tekjuskiptingu skaltu fylgja þessum skrefum.

1. Á **Allar/virkar innheimtuáætlanir** síðu, búðu til innheimtuáætlun.
2. Á línunni fyrir hvern lið sem er settur upp fyrir tekjuskiptingu skal velja **Tekjuskipting** gátreit. Sá hlutur verður yfirliður. Ef sniðmátið er þegar sett upp birtast undirhlutirnir sjálfkrafa á listanum.
3. Til að bæta við fleiri undirhlutum skaltu velja **Bættu við tekjuskiptu barni**, og veldu undirliðið sem þú vilt bæta við.
4. Haltu áfram með skrefunum til að vinna með innheimtuáætlunina.

> [!NOTE]
> Ef **Búðu til tekjuskiptingu sjálfkrafa** valkostur er stilltur á **Já** á **Endurteknar innheimtufæribreytur samnings** síðu, eftirfarandi aðgerðir eiga sér stað:
>
> - Ef línan er sett upp sem yfirliður í tekjuskiptingarsniðmáti, er **Tekjuskipting** gátreiturinn er sjálfkrafa valinn.
> - Undirvörur eru sjálfkrafa færðar inn á sölupöntun eða innheimtuáætlunarlínu.
>
> Ef **Búðu til tekjuskiptingu sjálfkrafa** valkostur er stilltur á **Nei**, hegðunin er eins og útskýrt var áðan.

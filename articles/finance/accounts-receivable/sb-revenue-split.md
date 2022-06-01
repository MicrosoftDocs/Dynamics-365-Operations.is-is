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
ms.openlocfilehash: 73dbc2242639a54d687506e7c325fec4b9a95d12
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770155"
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

## <a name="additional-revenue-split-information"></a>Viðbótarupplýsingar um skiptingu tekna

Þegar þú bætir við hlut sem er hluti af tekjuskiptingu skaltu athuga eftirfarandi upplýsingar: 

- Ekki er hægt að fresta foreldrisupphæðinni.
- Upphafsdagsetning, lokadagsetning, magn, eining, staður og vöruhús gildi undirvöru eru byggð á yfirvörunni. Ekki er hægt að breyta þessum gildum fyrir undiratriðin. Allar breytingar verða að gera á yfirliðnum. 
- Verðlagningaraðferðin er **Flat** og er ekki hægt að breyta.
- Hægt er að bæta við eða fjarlægja barnahluti.
- Foreldri og undirhlutir verða að nota sama vöruflokk. 
- Undirhlutir geta haft eina af eftirfarandi uppsetningum:

    - The **Innheimtutíðni** og **Innheimtutímabil** reitirnir eru stilltir á sama gildi og yfirliðurinn. 
    - The **Innheimtutíðni** reiturinn er stilltur á **Einu sinni**. Í þessu tilviki er **Innheimtutímabil** reiturinn er sjálfkrafa stilltur á **1**. 

- Summa nettófjárhæða undirliðanna jafngildir yfirfjárhæðinni. Ef úthlutunaraðferðin er **Núll upphæðir**, bæði summan af undirliðsupphæðum og yfirupphæð eru 0 (núll). 

    > [!NOTE]
    > Ef úthlutunaraðferðin er **Núll foreldri upphæð**, summan af undirliðunum (ekki núll) jafngildir ekki yfirupphæð, sem er 0 (núll). Þessi úthlutunaraðferð er notuð í innri tilgangi, þannig að starfsmenn geti séð undirliðina. Hins vegar geta viðskiptavinir aðeins séð móðurhlutinn.

- Ef margfeldisfyrirkomulag (MEA) gerð sölupöntunarinnar er **Einhleypur**, samsvarandi færslulína fyrir tekjuúthlutun margfaldra þátta er búin til þegar yfir- og undirliðum er bætt við. 
- Ef úthlutunaraðferð fyrir tekjuskiptingu er **Jafnar upphæðir**, og yfirupphæð er breytt, eru upphæðirnar endurreiknaðar fyrir allar undirlínur. 
- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Breytileg upphæð**, eftirfarandi hegðun á sér stað:

    - Nettófjárhæð yfirliðsins birtist í **Upphæð foreldra** dálki. Þetta gildi er hægt að breyta. Hins vegar er einingarverð, nettóupphæð og afsláttur 0 (núll) og ekki er hægt að breyta þeim.
    - Einingaverð undirvöru er 0 (núll). Þú getur breytt einingaverði eða nettóupphæð. Þegar þú breytir einu gildinu er hitt gildið sjálfkrafa uppfært.

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Hlutfall**, eftirfarandi hegðun á sér stað:

    - Nettófjárhæð yfirliðsins birtist í **Upphæð foreldra** dálki. Þetta gildi er hægt að breyta. Hins vegar er einingarverð, nettóupphæð og afsláttur 0 (núll) og ekki er hægt að breyta þeim. 
    - Nettófjárhæð barnaliða er reiknuð sem *Hlutfall*&times;*Upphæð foreldra*.

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Jöfn upphæð**, eftirfarandi hegðun á sér stað:

    - Nettófjárhæð yfirliðsins birtist í **Upphæð foreldra** dálki. Þetta gildi er hægt að breyta. Hins vegar er einingarverð, nettóupphæð og afsláttur 0 (núll) og ekki er hægt að breyta þeim. 
    - Nettóupphæð undirliða er reiknuð með því að skipta yfirupphæðinni jafnt á milli allra undirliða. 
    - Ef undirliðir eru fjarlægðir eða bætt við er nettóupphæð og einingarverð endurreiknuð þannig að allar undirlínur hafi jafnar upphæðir. 
    - Ef ekki er hægt að skipta yfirupphæðinni jafnt, gæti nettóupphæð og einingaverð síðasta undirliðar verið aðeins meira eða minna en nettóupphæð og einingaverð hinna undirliðanna. 

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Núll upphæð**, eftirfarandi hegðun á sér stað:

    - Hægt er að breyta einingaverði, nettóupphæð og afslætti. Foreldrisupphæðin er 0 (núll) og ekki er hægt að breyta henni. 
    - Magn, eining, staður og vöruhússgildi undirvöru eru byggð á yfirvöru. Þú getur ekki breytt þessum gildum fyrir undiratriðin. Allar breytingar verða að gera á yfirliðnum. 
    - Einingaverð og nettóverð undirvöru er 0 (núll) og ekki er hægt að breyta þeim. 

- Fyrir tekjuskiptingu þar sem úthlutunaraðferðin er **Núll foreldri upphæð**, eftirfarandi hegðun á sér stað:

    - Einingarverð, móðurupphæð og nettóupphæð móðurliðar eru 0 (núll).
    - Í innheimtuáætlun birtast undirlínurnar eins og þeim hafi verið bætt við handvirkt og öll gildi eru uppfærð út frá völdum innheimtuáætlunarhópi. Hægt er að breyta þessum gildum. Fyrir barnavörur geturðu fengið aðgang að **Stækkun og afsláttur** og **Ítarleg verðlagning** valkosti með því að nota **Magn slegið inn**, **·**, **·**, og **Virði** sviðum í **Skoða innheimtuupplýsingar**. 
    - Á sölupöntun hafa undirlínurnar afslátt og afsláttarprósentu 0 (núll). 
    - Hægt er að breyta innheimtutíðni foreldris og undirliða og hver lína getur haft mismunandi tíðni. Hins vegar er yfirliðið sjálfkrafa uppfært þannig að það notar stystu tíðnina úr undirlínum sínum. Til dæmis, tekjuskipting hefur tvo undirliði, þar af einn sem notar **Mánaðarlega** innheimtutíðni og hinn sem notar **Árlega** innheimtutíðni. Í þessu tilviki er innheimtutíðni yfirliðsins uppfærð í **Mánaðarlega**.

---
title: Yfirlit Lean manufacturing
description: Þessi skrá veitir sem yfirlit og lýsingu á lean-framleiðslu aðgerðir í Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow, Kanban, KanbanQuantityOverview, KanbanAssignCard, KanbanCirculatingCards, KanbanRules, WHSKanbanWaveTableManagePickingListPool
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19371"
- intro-internal
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1374a451c65b4bafdc6efeb10949d1f6eceb4758
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343919"
---
# <a name="lean-manufacturing-overview"></a>Yfirlit yfir lean-framleiðslu

[!include [banner](../includes/banner.md)]

Þessi skrá veitir sem yfirlit og lýsingu á lean-framleiðslu aðgerðir í Dynamics 365 Supply Chain Management.

Lean-framleiðsla býður upp á verkfæri sem hægt er að nota til að móta lean-aðgerðir. Þessar verkfæri styðja og ýta undir eftirfarandi hugtök og verkþætti viðskipta:
-   Stofna lean-framleiðslufyrirtæki með því að móta framleiðslu- og vörustjórnunarferli sem framleiðsluflæði.
-   Innleiða lean-dráttarkerfi með því að nota kanbana til að merkja eftirspurn
-   Fylgjast með og viðhalda kanban-vinnslur.

Lean-framleiðsla samanstendur af framleiðsluflæði, verkþáttum og kanban-reglum. Þetta skipulag er að fullu samþætt ferlum Supply Chain Management. Hægt er að nota lean-framleiðsla í blönduðum ham framleiðsluumhverfis sem sameinar mismunandi framboð, framleiðslu og upprunastefnur. Þessar stefnu innihalda framleiðslupantanir , runupantanir fyrir ferlisatvinnugreinar, innkaupapantanir og flutningspantanir.

| **Mikilvægt**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hægt er að nota Supply Chain Management til að styðja innleiðingu lean-framleiðslu með kanban. Hins vegar er árangursrík innleiðing lean-regla byggð á innri viðskiptaferli sem er notuð, og raunverulegum framleiðsluskilyrðum og umhverfi. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a>Móta framleiðslu- og vörustjórnunarferli sem framleiðsluflæði.
Til að Stofna lean-framleiðslufyrirtæki, mótaðu framleiðslu- og vörustjórnunarferli sem framleiðsluflæði. Þessi aðgerð samanstendur af eftirfarandi verkefnum:
1.  Auðkenna ferli sem óskað er að innleiða lean áfyllingaráætlun fyrir og síðan skal móta þessi ferli sem framleiðsluflæði. Síðan er hægt að greina og fínpússa ferlin. Eitt markmið lean innleiðingu er að minnka það sem fer til spillis með því að bæta flæði efnis og upplýsingar.
2.  Skilgreina framleiðsluflæðis sem röð verkþætti sem lýsir flæði efnis. Flutningsverkþáttur skilgreinir hreyfingar á vöru eða vörum úr einum stað á annan. Vinna verkþátts skilgreinir virðisauka aðgerðina sem er beitt á afurð.
3.  Stofna útgáfu af framleiðsluflæðið sem tilgreinir kröfur fyrir framleiðslutími á einingu Þessar þarfir eru notaðar til að reikna út ferlistíma á hvern verkþátt í framleiðsluflæðinu. Hægt er að stofna margar útgáfur framleiðsluflæða og nota þessar útgáfur til að bæta ferli.

## <a name="using-kanbans-to-signal-demand-requirements"></a>Nota Kanban til að merkja eftirspurnarkröfur
Tínslukerfi framleiðir vörur aðeins þegar vörurnar vantar. Þessi venju minnkar afhendingartíma sendinga og umframbirgðir. Hægt er að nota kanbana til að áætla, rekja og vinna þarfir sem eru byggðar á framleiðsluflæði. Til að stofna kanban ramma skal stofna kanban-reglur sem skilgreina þegar kanban eru stofnaðar og hvernig þær kröfur eru uppfylltar. Hægt er að stofna tvær tegundir kanban-regla: Reglur framleiðslu stofna kanban-vinnslur ferlis og kanban-reglur frádráttar stofna kanban-vinnslur flutnings. Hægt er að stofna eftirfarandi áfyllingaraðferðir:
-   **Fast magn** kanban-reglur eru tengdar við fastur fjöldi efnismeðhöndlunareiningar, sem þýðir að fjöldi virkra kanbana eru föst. Þegar allar afurðir úr Kanban eru notaðar og efnismeðhöndlunareiningar eru handvirkt tæmt, er stofnuð ný kanban af sömu gerð. Þegar kanban-reglur fasts magns eru stofnaðar, er hægt að reikna út ákjósanlegar kanban-magn og magn afurðar sem eru notaðar. Útreikningur tekur mið af spá, raunveruleg eftirspurn úr opnum pöntunum, afgreiðslutíma til að fylla á vörum, og söguleg kröfur.
-   **Áætlað** kanban-reglur fylla á kröfur sem eru reiknaðar við aðaláætlanagerð. Áætlanagerð myndar áætluð kanbön sem hægt er að festa við kanbana.
-   **Tilvik** kanban-reglur fylla á kröfur sem koma úr sölupöntunarlínum, uppskriftalínum framleiðslu, kanban-línum og stillingum lágmarksbirgða. Þegar tilvikskanbana eru búin til, eru þær festar við upprunaþarfir.

Þegar kanban er stofnuð, ein eða fleiri kanban-vinnslur eru mynduð á grundvelli aðgerðum kanban-flæðis sem eru skilgreindar í kanban-reglu.

## <a name="monitoring-and-maintaining-kanban-jobs"></a>Fylgjast með og viðhalda kanban-vinnslur.
Lean-framleiðsla veitir sýnileika inn í gildandi stöðu verkþátta framleiðslu og vörustjórnunar sem stjórnast af kanban-reglur. Af þessu leiðir að þú getur áætlað og forgangsraðað eftirfarandi verkum:

-   Fá yfirlit yfir gildandi áætlun kanban-vinnslu.
-   Áætla og endurraða kanban-vinnslur.
-   Fylgjast með og skrá stöðu kanban-vinnslur.

Eftirfarandi listi lýsir sérhæfðum kanban-borð:
-   Áætlun kanban-vinnslu – Veitir yfirlit yfir kanban-vinnslurnar. Taflan birtir kanban-vinnslur og stöðu þeirra fyrir eina eða margar vinnuflokkana. Vinnslur eru talin upp samkvæmt áætlunartímabilum (daga eða vikna) sem eru skilgreindar í framleiðsluflæðislíkan. Borðið sýnir einnig notkun afkastagetu á hverju áætlunartímabili, þannig að hægt er að fylgjast með áætlaða hleðslu. Hægt er að ljúka stöðu kanban-vinnsla og endurröðun á kanban-vinnslum á mismunandi áætlunartímabil, og framkvæma önnur verk.
-   Kanban-borð fyrir flutningsverk - þetta borð veitir yfirlit yfir núverandi flutningsverk. Þú getur uppfært og skráð tiltektarlista, og hefja og ljúka flutningsvinnslum, og framkvæma önnur verk.
-   Kanban-spjald fyrir vinnslukenni verks -Þessa spjald er hannað til að styðja venjulegt framleiðsluflæði og veita yfirlit yfir gildandi stöðu í einni eða mörgum vinnuflokkana. Úr þessari borði er hægt að forgangsraða Kanban tína þau eða framleiða. Borðið er einnig hannað til að styðja skannað strikamerki fyrir skýrslugerð kanbana.

## <a name="kanban-jobs-and-integration-with-supply-chain-management-processes"></a>Kanban störf og samþætting við ferla Supply Chain Management
Kanban-vinnslur eru fyllilega samþættar gildandi ferlum fyrir birgðafærslur í Supply Chain Management.
-   Hægt er að framkvæma tiltektarverkþáttum til að fylla á efni sem er notuð til að uppfylla kröfur kanban-vinnslur.
-   Þú getur Prenta kanban-spjöld, virkt spjald og tiltektarlista til að styðja við notkun kanbana. Þessi skjöl eru notaðar til að tákna, rekja og skrá kanban-vinnslur í vöruhúsinu og í framleiðslu í vinnslusal.
-   Þú getur skrá tiltektar og flutningsaðgerðir í birgðum með því að skanna strikamerki.

Auk þess, Lean-framleiðsla styður innkaupa- og innheimtuferli fyrir þjónustu sem vísað er til úr verkefnum undirverktaka
-   Hægt er að tengja innkaupasamningslínur og þjónustu við úthýsta verkþætti.
-   Hægt er að stofna reglubundnar innkaupapantanir og móttökuráðgjöf til að styðja innkaupa og reikningsfærslu á þjónustu.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
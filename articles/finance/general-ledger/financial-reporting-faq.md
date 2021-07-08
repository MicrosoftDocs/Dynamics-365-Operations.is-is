---
title: Algengar spurningar um fjárhagsskýrslugerð
description: Þetta efnisatriði veitir svör við nokkrum algengum spurningum um fjárhagsskýrslugerð.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266634"
---
# <a name="financial-reporting-faq"></a>Algengar spurningar um fjárhagsskýrslugerð

Þetta efnisatriði veitir svör við algengum spurningum um fjárhagsskýrslugerð.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Hvernig takmarka ég aðgang að skýrslu með öryggistré?

Eftirfarandi dæmi sýnir hvernig hægt er að takmarka aðgang að skýrslu með öryggistré.

USMF-sýnifyrirtækið er með **efnahagsreikningsskýrslu** sem það vill ekki að allir notendur fjárhagsskýrslugerðar hafi aðgang að. Hægt er að nota öryggistré til að takmarka aðgang að einni skýrslu þannig að aðeins tilteknir notendur hafi aðgang að henni.

1. Skráðu þig inn á Financial Reporter Report Designer.
2. Veldu **Skrá \> Ný \> Trjáskilgreining** til að búa til nýja trjáskilgreiningu.
3. Pikkaðu tvisvar (eða tvísmelltu) á línuna **Samantekt** í dálknum **Einingaröryggi**.
4. Veldu **Notendur og hópar**.
5. Veldu notendur eða hópa sem þurfa aðgang að skýrslunni.
6. Veldu **Vista**.
7. Í skýrsluskilgreiningu skal bæta við nýrri trjáskilgreiningu.
8. Í trjáskilgreiningunni skal velja **Stilling**. Síðan undir **Einingaval skipurits** skal velja **taka allar einingar með**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hvernig auðkenni ég hvaða lyklar passa ekki við stöður mínar?

Ef þú ert með skýrslu sem er ekki með samsvarandi stöðu skaltu nota eftirfarandi ferli til að auðkenna hvern lykil og hvert frávik.

### <a name="in-financial-reporter-report-designer"></a>Í Financial Reporter Report Designer

1. Búa til nýja línuskilgreiningu.
2. Veldu **Breyta \> Setja inn línur úr víddum**.
3. Veldu **MainAccount**.
4. Veldu **Í lagi**.
5. Vista línuskilgreininguna.
6. Stofna nýja dálkskilgreiningu.
7. Stofna nýja skýrsluskilgreiningu.
8. Veldu **Stillingar** og afveldu þennan valkost.
9. Mynda skýrslu. 
10. Flytja skýrsluna út í Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>Í Dynamics 365 Finance

1. Opnaðu **Fjárhagur \> Fyrirspurnir og skýrslur \> Prófjöfnuður**.
2. Stilltu eftirfarandi svæði:

    - **Frá dagsetningu** – Færðu inn upphafsdag fjárhagsárs.
    - **Að dagsetningu** – Færðu inn dagsetninguna sem skýrslan er mynduð fyrir.
    - **Fjárhagsvídd** – Stilltu þetta svæði á **Aðallykill stilltur**.

3. Veldu **Reikna út**.
4. Flytja út skýrslu í Excel.

Nú ætti að vera hægt að afrita gögnin úr Excel-skýrslu Financial Reporter yfir í **prófjafnaðarskýrslu** til að bera saman dálkana **Lokastaða**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Þegar ég hanna skýrslu í Report Designer, eða þegar ég mynda fjárhagsskýrslu, fékk ég eftirfarandi skilaboð: „Ekki var hægt að ljúka við aðgerðina vegna bilunar í gagnaveitukerfi.“ Hvernig ætti ég að svara?

Skilaboðin gefa til kynna að vandamál hafi komið upp þegar kerfið reyndi að sækja fjárhagsleg lýsigögn úr gagnaskemmunni á meðan þú notaðir fjárhagsskýrslugerð. Hægt er að leysa úr þessu á tvo vegu:

- Farðu yfir samþættingarstöðu gagnanna með því að fara í **Verkfæri \> Samþættingarstaða** í Report Designer. Ef samþættingunni er ekki lokið skaltu bíða þar til henni líkur. Reyndu svo að gera það aftur sem þú varst að gera þegar skilaboðin birtust.
- Hafðu samband við notendaþjónustu til að finna vandamálið og lagfæra það. Það kann að vera ósamræmi í gögnum í kerfinu. Tæknimenn hjá notendaþjónustu geta aðstoðað þig við að finna vandamálið á þjóninum og þau tilgreindu gögn sem kunna að þarfnast uppfærslu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

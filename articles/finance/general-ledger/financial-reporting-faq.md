---
title: Algengar spurningar um fjárhagsskýrslugerð
description: Þetta efnisatriði sýnir spurningar sem tengjast fjárhagsskýrslugerð sem aðrir notendur hafa lagt fram.
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
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923026"
---
# <a name="financial-reporting-faq"></a>Algengar spurningar um fjárhagsskýrslugerð 

Þetta efnisatriði veitir svör við algengum spurningum um fjárhagsskýrslugerð. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hvernig takmarka ég aðgang að skýrslu með öryggistré?

Eftirfarandi dæmi sýnir hvernig hægt er að takmarka aðgang að skýrslu með öryggistré.

USMF-sýnifyrirtækið er með skýrslu efnahagsreiknings sem það vill ekki að allir notendur fjárhagsskýrslugerðar geti skoðað. Hægt er að nota öryggistré til að takmarka aðgang að einni skýrslu þannig að aðeins tilteknir notendur geti nálgast skýrsluna. Fylgdu eftirfarandi leiðbeiningum til að takmarka aðgang: 

1. Skráðu þig inn í skýrsluhönnun fjárhagsskýrslna.
2. Stofnaðu nýja trésskilgreiningu. Opnaðu **Skrá > Nýtt > Trésskilgreining**.
3. Tvísmellið á línuna **Samantekt** í dálknum **Einingaröryggi**.
4. Veldu **Notendur og hópar**.  
5. Veldu notendur eða hópa sem þurfa aðgang að þessari skýrslu. 
6. Veldu **Vista**.
7. Í skýrsluskilgreiningu skal bæta við nýrri trésskilgreiningu.
8. Í trésskilgreiningunni skal velja **Stilling**. Undir **Einingaval skipurits** skal velja **taka allar einingar með**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Hvernig auðkenni ég lykla sem passa ekki við stöður?

Ef þú ert með skýrslu sem er ekki með samsvarandi stöðu geturðu gert eftirfarandi til að auðkenna hvern lykil og hvert frávik. 

**Skýrsluhönnun fjárhagsskýrslna**
1. Í skýrsluhönnun fjárhagsskýrslna skal stofna nýja línuskilgreiningu. 
2. Veljið **Breyta > Setja inn línur úr víddum**.
3. Veljið **Aðallykill**.  
4. Veljið **Í lagi**.
5. Vistið línuskilgreininguna.
6. Stofna nýja dálkskilgreiningu
7. Stofna nýja skýrsluskilgreiningu.
8. Veljið **Stillingar** og afveljið þennan valkost.  
9. Mynda skýrslu. 
10. Flytja skýrsluna út í Microsoft Excel.

**Dynamics 365 Finance** 
1. Í Dynamics 365 Finance skal opna **Fjárhagur > Fyrirspurnir og skýrslur > Prófjöfnuður**.
2. Stillið eftirfarandi færibreytur:
   - **Frá dagsetningu** – Færið inn upphaf fjárhagsárs.
   - **Að dagsetningu** – Færið inn dagsetninguna sem skýrslan er mynduð fyrir.
   - **Fjárhagsvídd** – Stillið þetta svæði á **Aðallykill stilltur**.
 3. Veljið **Reikna út**.
 4. Flytja skýrsluna út í Microsoft Excel.

Nú ætti að vera hægt að afrita gögnin úr Excel-skýrslu fjárhagsskýrslugerðar yfir í prófjafnaðarskýrslu til að bera saman dálkana **Lokastaða**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
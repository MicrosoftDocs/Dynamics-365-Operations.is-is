---
title: Algengar spurningar um fjárhagsskýrslugerð
description: Þetta efnisatriði sýnir spurningar sem tengjast fjárhagsskýrslugerð sem aðrir notendur hafa lagt fram.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070218"
---
# <a name="financial-reporting-faq"></a>Algengar spurningar um fjárhagsskýrslugerð 

Þetta efnisatriði sýnir spurningar sem tengjast fjárhagsskýrslugerð sem aðrir notendur hafa lagt fram. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hvernig takmarka ég aðgang að skýrslu með tréöryggi?

Aðstæður: USMF-sýnifyrirtækið er með skýrslu efnahagsreiknings sem það vill ekki að allir notendur fjárhagsskýrslugerðar geti skoðað í D365. Lausn: Hægt er að nýta sér tréöryggi til að takmarka aðgang að einni skýrslu þannig að aðeins tilteknir notendur geti nálgast skýrsluna. 

1.  Skrá inn í skýrsluhönnun fjárhagsskýrslna

2.  Stofna nýja Trjáskilgreiningu (Skrá | Nýtt | Trjáskilgreining) a.    Tvísmellið á línu **Samantektar** í dálknum **Einingaröryggi**.
  i.    Smellið á Notendur og hópar.  
          1. Veljið notanda/notendur eða hóp sem vill fá aðgang að þessari skýrslu. 
          
[![skjár notanda](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![öryggisskjár](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Smelltu á **Vista**.
  
[![hnappur til að vista](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Í skýrsluskilgreiningu skal bæta við nýrri trjáskilgreiningu

[![trjáskilgreiningarsnið](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

Svar.  Í trjáskilgreiningunni skal smella á stillingu og undir „Einingaval skipurits“ skal haka í „Taka allar einingar með“

[![skjámynd einingavals skipurits](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Fyrir:** [![fyrir skjáskot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Eftir:** [![eftir skjámynd](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Athugasemd: Ástæða ofangreindra skilaboða er að notandinn minn hefur ekki aðgang að þessari skýrslu eftir notkun Einingaröryggis



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Hvernig ákvarða ég hvaða reikningur/reikningar samsvara ekki stöðu minni í D365?

Þegar þú ert með skýrslu sem passar ekki við það sem þú ættir að gera ráð fyrir í D365, þá eru hér nokkur skref sem þú gætir tekið til að bera kennsl á þessa reikninga og frávik. 

### <a name="in-financial-reporter-report-designer"></a>Í skýrsluhönnun fjárhagsskýrslna

1.  Búa til nýja línuskilgreiningu a.    Smella á Breyta | Setja inn línur úr víddum i.  Veljið MainAccount [![Veljið Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Smellið á „Í lagi“ b.    Vista línuskilgreiningu

2.  Búa til nýja dálkskilgreiningu     [![Búa til nýja dálkskilgreiningu](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Búa til nýja skýrsluskilgreiningu a.    Smellið á Stillingar og takið hak af [![Stillingagluggi](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Mynda skýrslu 

5.  Flytja út skýrslu í Excel.

### <a name="in-d365"></a>Í D365: 
1.  Smellið á Fjárhagur | Fyrirspurnir og skýrslur | Prófjöfnuður a.    Færibreytur i.  Frá dagsetningu: upphaf fjárhagsárs ii. Til dagsetningar: Dagsetning þar sem skýrslan var mynduð fyrir iii.    Fjárhagsvíddasamstæðan „Aðallyklasafn“ [![Skjámynd aðallykils](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Smellið á Reikna

2.  Flytja út skýrslu í Excel

Nú ætti að vera hægt að afrita gögnin úr Excel-skýrslu fjárhagsskýrslugerðar yfir í prófjafnaðarskýrslu D365 og bera saman dálka „Lokunarstöðu“.

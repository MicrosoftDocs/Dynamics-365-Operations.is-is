---
title: Fjárhagsjafnanir
description: Þetta efnisatriði útskýrir hvernig á að nota síðu fjárhagsjafnana til að jafna fjárhagsfærslur og bakfærslur.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e98b012210338e7f18cb874eefbc8a023aa4428b
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075325"
---
# <a name="ledger-settlements"></a>Fjárhagsjafnanir

[!include [banner](../includes/banner.md)]

Fjárhagsuppgjör er ferlið við að passa saman debet- og kreditfærslur í aðalbókinni. Uppgjör debet- og kreditupphæða er notað til að samræma stöðu fjárhagsreiknings við nákvæmar færslur sem mynda þá stöðu.

Uppgjör viðskipti geta verið útilokuð frá fyrirspurnum og skýrslum. Þannig er auðveldara að greina opnu fjárhagsfærslurnar sem mynda stöðu fjárhagsreikningsins.

> [!IMPORTANT] 
> Viðskiptaskuldir (AP) og Viðskiptakröfur (AR) einingarnar hafa einnig uppgjör á reikningum og greiðslum. Þegar uppgjör á sér stað í undirbókum AR og AP eru samsvarandi fjárhagsfærslur ekki sjálfkrafa jafnaðar.

## <a name="ledger-settlement-features"></a>Eiginleikar fjárhagsuppgjörs
Í Microsoft Dynamics 365 Finance útgáfa 10.0.21, the **Virkja háþróaða fjárhagsuppgjör** valkostur var fjarlægður úr **Fjárhagsfæribreytur** síðu. Ítarleg uppgjör fjárhagsbókar er nú alltaf virkjuð.
Í Finance útgáfu 10.0.25 er **Meðvitund milli uppgjörs fjárhags og ársloka** eiginleiki var kynntur. Þessi eiginleiki breytir grundvallarvirkni bæði í uppgjöri fjárhags og ársloka aðalbókar. Áður en þú virkjar þennan eiginleika í **Eiginleikastjórnun** vinnusvæði, sjá, [Meðvitund milli uppgjörs fjárhags og ársloka](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Setja upp fjárhagsuppgjör
Þú verður að velja helstu reikninga sem þú vilt gera fjárhagsuppgjör fyrir. Það eru tvær leiðir til að velja þessa aðalreikninga.

1. Fara til **Aðalbók** > **Uppsetning höfuðbókar** > **Fjárhagsfæribreytur**.
2. Á **Fjárhagsuppgjör** flipanum, veldu reikningaskrána sem þú vilt velja aðalreikningana úr.
3. Veljið helstu reikninga til að gera fjárhagsuppgjör fyrir. Vegna þess að bókhaldsyfirlit eru alþjóðleg, munu öll fyrirtæki sem valdar bókhaldsyfirlitum er úthlutað til hafa sömu aðallykla sem eru valdir til uppgjörs fjárhags.

  -eða-

1. Fara til **Aðalbók** > **Reglubundin verkefni** > **Fjárhagsuppgjör**.
2. Veldu **Fjárhagsuppgjörsreikningar**.
3. Í svarglugganum velurðu bókhaldsyfirlit og aðallykla til að gera fjárhagsuppgjör fyrir. Þessi valmynd er flýtileið. Allir aðalreikningar sem þú bætir við hér munu einnig endurspeglast á **Fjárhagsfæribreytur** síðu.

Þú getur notað sömu grunnaðferðir til að fjarlægja aðalreikninga úr fjárhagsuppgjöri hvenær sem er. Fjarlæging aðalreiknings hefur engin áhrif á fyrri fjárhagsuppgjör. Hins vegar munu aðalreikningur og viðskipti ekki lengur birtast á **Fjárhagsuppgjör** síðu.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Jafna færslur
Til að jafn fjárhagsfærslur skaltu fylgja þessum skrefum.

1. Fara til **Aðalbók** > **Reglubundin verkefni** > **Fjárhagsuppgjör**.
2. Stilltu síurnar efst á síðunni:

    - Veldu tímabil. Að öðrum kosti, veldu dagsetningarbilskóða til að fylla út dagsetningarbilið sjálfkrafa. Við mælum ekki með því að þú gerir fjárhagsuppgjör fyrir færslur sem fara yfir fjárhagsár.
    - Breyttu færslulaginu eftir þörfum. Þú getur ekki jafnað færslur sem eru í mismunandi bókunarlögum.
    - Til að sýna aðallykil og víddir sérstaklega velurðu fjárhagsvíddasamstæðu.

3. Veldu **Birta færslur** til að sýna allar færslur sem samsvara síunum sem þú stillir og lista yfir reikninga sem þú tilgreindir þegar þú settir upp bókhaldslykilinn í fyrri hlutanum.

    - Ef þú breytir einhverjum síum eða víddarsamstæðum þarftu að velja **Birta færslur** aftur.
    - Til að sía færslurnar á einstakan aðalreikning, notaðu síuna á **Fjárhagsreikningur** sviði. Við mælum ekki með því að þú gerir fjárhagsuppgjör fyrir færslur sem eru bókaðar á mismunandi aðallykla.

4. Veldu línur til uppgjörs. Gildið í **Valin upphæð** reiturinn efst á síðunni hækkar eða lækkar til að endurspegla heildarupphæðina á völdum línum.
5. Þegar þú hefur lokið við að velja færslur skaltu velja **Merktu valið**. Fyrir hverja valda færslu birtist gátmerki í **Merkt** dálki. Að auki, gildið í **Merkt magn** reiturinn fyrir ofan hnitanetið hækkar eða minnkar til að endurspegla heildarupphæðina á merktu línunum.
6. Þegar gildið í **Merkt magn** sviði er **0** (núll), veldu **Gerðu upp merktar færslur**. Staða valinna færslna er uppfært í **Jafnað**.

    > [!IMPORTANT]
    > Allar færslur sem þú hefur merkt til uppgjörs fyrir virka lögaðilann verða jafnaðar, jafnvel þótt þær séu ekki sýndar á síðunni Fjárhagsuppgjör vegna þess að þú notaðir síu.

## <a name="make-transactions-easier-to-find"></a>Gera það auðveldara að finna færslur
The **Fjárhagsuppgjör** síðu inniheldur möguleika sem gera það auðveldara að skoða færslurnar sem þú þarfnast fyrir uppgjör.

- Nota **Merkt** sía til að sía viðskipti út frá því hvort **Merkt** gátreiturinn er valinn fyrir þá.
- Nota **Staða** sía til að sía viðskipti út frá stöðu þeirra.
- Veldu **Raða eftir algeru magni** að flokka upphæðirnar eftir algildi. Þannig er hægt að flokka skuldir og inneignir sem hafa sömu upphæð.

## <a name="reverse-a-settlement"></a>Bakfæra jöfnun
Þú getur bakfært jöfnun sem var gerð fyrir mistök.

1. Fylgdu skrefum 1 til 3 í [Gera upp viðskipti](#settle-transactions) kafla til að sýna færslurnar sem þú hefur áhuga á.
2. Í **Staða** síu, veldu **Jöfnuð**.
3. Veldu línur til að snúa við.
4. Veldu **Bakfæra merktar færslur**. Staða allra færslna sem hafa sama uppgjörsauðkenni er uppfærð í **Ekki afgreitt**.

    > [!IMPORTANT]
    > Allar færslur sem hafa sama uppgjörsauðkenni verða bakfærðar, jafnvel þótt þær séu ekki merktar. Til dæmis voru fjórar línur merktar og afgreiddar. Allar fjórar línurnar eru með sama uppgjörsauðkenni. Ef þú merkir við eina af þessum fjórum línum og velur síðan **Bakfæra merktar færslur**, allar fjórar línurnar verða snúnar við.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

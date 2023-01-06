---
title: Fjárhagsjafnanir
description: Þessi grein útskýrir hvernig á að nota síðu fjárhagsjafnana til að jafna fjárhagsfærslur og bakfærslur.
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
ms.openlocfilehash: 39fd6c6677565a4b1e9a9bf6f43a4c630cb5e07b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902488"
---
# <a name="ledger-settlements"></a>Fjárhagsjafnanir

[!include [banner](../includes/banner.md)]

Fjárhagsjöfnun er ferlið við að jafna debet- og kreditfærslur í fjárhagnum. Jöfnun debet- og kreditupphæða er notuð til að afstemma stöðu fjárhagslykilsins með ítarlegum færslum sem staðan samanstendur af.

Hægt er að útiloka jafnaðar færslur frá fyrirspurnum og skýrslum. Þannig er auðveldara að greina opnar fjárhagsfærslur sem staðan samanstendur af í fjárhagslyklinum.

> [!IMPORTANT] 
> Einingar viðskiptaskulda og viðskiptakrafna eru einnig með jöfnun á reikningum og greiðslum. Þegar jöfnun á sér stað í undirbókum viðskiptaskulda og viðskiptakrafna eru samsvarandi fjárhagsfærslur ekki sjálfkrafa jafnaðar.

## <a name="ledger-settlement-features"></a>Eiginleikar fjárhagsjöfnunar
Í Microsoft Dynamics 365 Finance-útgáfu 10.0.21 var valkosturinn **Virkja ítarlega fjárhagsjöfnun** fjarlægður af síðunni **Færibreytur fjárhags**. Nú er ítarleg fjárhagsjöfnun alltaf virk.
Í Finance-útgáfu 10.0.25 var eiginleikinn **Munurinn á fjárhagsjöfnun og árslokalokun** kynntur til sögunnar. Þessi eiginleiki breytir grundvallarvirkni í bæði fjárhagsjöfnun og árslokalokun fjárhags. Áður en þessi eiginleiki er virkjaður á vinnusvæðinu **Eiginleikastjórnun** skal skoða [Munurinn á fjárhagsjöfnun og árslokalokun](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Setja upp fjárhagsjöfnun
Þú verður að velja aðallyklana sem þú vilt gera reikningsuppgjör fyrir. Tvær leiðir eru til að velja þessa aðallykla. 

1. Opnið **Fjárhagur** >  **Fjárhagsuppsetning**  >  **Færibreytur fyrir fjárhag**.
2. Í flipanum **F** skal velja bókhaldslykilinn sem velja á aðallyklana fyrir.
3. Veldu aðallyklana til að gera fjárhagsjafnanir fyrir. Vegna þess að bókhaldslyklar eru alþjóðlegir munu öll fyrirtæki sem valdir bókhaldslyklar eru úthlutaðir á hafa sömu aðallykla valda fyrir fjárhagsjöfnun.

  -eða-

1. Opnið **Fjárhagur**  >  **Reglubundin verkefni**  >  **Fjárhagsuppgjör**.
2. Veljið **Lyklar fjárhagsuppgjörs**.
3. Í svarglugganum skal velja bókhaldslykil og aðallykla til að gera fjárhagsjafnanir fyrir. Þessi svargluggi er flýtileið. Allir aðallyklar sem þú bætir við hér munu einnig koma fram á síðunni **Færibreytur fjárhags**.

Hægt er að nota sömu grunnaðferðir til að fjarlægja aðallykla úr fjárhagsjöfnun hvenær sem er. Að fjarlægja aðallykil hefur engin áhrif á fyrri fjárhagsjafnanir. Aðallyklar og færslur munu hins vegar ekki lengur birtast á síðunni **Fjárhagsjöfnun**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Jafna færslur
Til að jafn fjárhagsfærslur skaltu fylgja þessum skrefum.

1. Opnið **Fjárhagur**  >  **Reglubundin verkefni**  >  **Fjárhagsuppgjör**.
2. Stilltu síurnar efst á síðunni:

    - Velja dagsetningarsvið. Einnig er hægt að velja kóða dagsetningarbils til að fylla dagsetningabil sjálfkrafa inn. Ekki er mælt með því að þú framkvæmir reikningsuppgjör vegna viðskipta á mismunandi reikningsárum.
    - Breyttu bókunarlaginu eins og nauðsynlegt er. Þú getur ekki gert upp færslur sem eru í mismunandi bókunarlögum.
    - Til að sýna aðallykil og víddir aðskilið skal velja fjárhagsvíddarsamstæðu.

3. Veldu **Birta færslur** til að sýna allar færslur sem samsvara síunum sem þú stillir og lista yfir reikninga sem þú tilgreindir þegar þú settir upp bókhaldslykilinn í fyrri hlutanum.

    - Ef þú breytir einhverjum síum eða víddarsamstæðum þarftu að velja **Birta færslur** aftur.
    - Til að sía færslurnar á stakan aðallykil skal nota síuna í reitnum **Fjárhagslykill**. Ekki er mælt með því að fjárhagsjöfnun sé gerð fyrir færslur sem eru bókaðar á aðra aðallykla.

4. Veljið línur sem á að jafna. Gildið á svæðinu **Valin upphæð** efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.
5. Þegar þú hefur lokið við að velja færslur skaltu velja **Merkja sem valið**. Gátmerki birtist í **Merkt** dálknum fyrir hverja færslu sem þú valdir. Auk þess hækkar gildið á svæðinu **Valin upphæð** fyrir ofan hnitanetið eða lækkar með heildarupphæðinni á línunum sem þú merktir.
6. Þegar gildið á svæðinu **Valin upphæð** er **0** (núll) skaltu velja **Jafna valdar færslur**. Staða valinna færslna er uppfært í **Jafnað**.

    > [!IMPORTANT]
    > Allar færslur sem þú hefur merkt fyrir jöfnun fyrir virkan lögaðila verða jafnaðar jafnvel þótt þær séu ekki sýndar á síðu fjárhagsjöfnunar því þú notaðir síu.

## <a name="make-transactions-easier-to-find"></a>Gera það auðveldara að finna færslur
Síðan **Fjárhagsuppgjör** inniheldur aðgerðir sem auðveldar að sjá færslurnar sem þarf að jafna.

- Notaðu síuna **Merkt** til að sía færslur byggt á því hvort gátreiturinn **Merkt** er valinn fyrir þær.
- Notaðu síuna **Staða** til að sía færslur út frá stöðu þeirra.
- Veldu **Raða eftir raunupphæð** til að raða upphæðunum eftir raungildi. Á þennan hátt er hægt að flokka debet- og kreditfærslur sem eru með sömu upphæðina.

## <a name="reverse-a-settlement"></a>Bakfæra jöfnun
Þú getur bakfært jöfnun sem var gerð fyrir mistök.

1. Fylgdu skrefum 1 til 3 í hlutanum [Jafna færslur](#settle-transactions) til að sýna færslurnar sem þú ert að leita að.
2. Í **Staða** síu, veldu **Jöfnuð**.
3. Veljið línur sem á að afturkalla.
4. Veljið **Bakfæra merktar færslur**. Staða allra færslna sem eru með sama jöfnunarkennið er uppfærð í **Ekki jafnað**.

    > [!IMPORTANT]
    > Allar færslur sem eru með sama jöfnunarkennið verða bakfærðar jafnvel þótt þær séu ekki merktar. Til dæmis voru fjórar línur merktar og jafnaðar. Allar fjórar línurnar eru með sama jöfnunarauðkenni. Ef þú merkir eina af þessum fjórum línum og velur síðan **Bakfæra merktar færslur** verða allar fjórar línurnar bakfærðar.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

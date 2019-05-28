---
title: Breyta sniðum með því að endurnýta Microsoft Excel-sniðmát
description: Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, Rafræn skýrslugerð - Hanna grunnstillingu til að mynda skýrslur í OPENXML-sniði.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551162"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Breyta sniðum með því að endurnýta Microsoft Excel-sniðmát

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, Rafræn skýrslugerð - Hanna grunnstillingu til að mynda skýrslur í OPENXML-sniði.

Þetta ferli útskýrir hvernig skal breyta Rafræn skýrslugerð (ER) grunnstillingu sniðs með því að endurnýta Microsoft Excel sniðmát sem hefur verið breytt. Í þessu ferli, muntu flytja breytt Excel sniðmát í Rafræn skýrslugerð grunnstillingar sniðs sem hefur verið stofnað fyrir sýnifyrirtækið, Litware, Inc., og síðan búa til rafræn skjöl. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota GBSI gagnasafn. Áður en þú byrjar, skal hlaða niður og vista skránna, SampleVendPaymWsReport2.xlsx, sem er á lista í Hjálp efnisatriði, breyta sniði Rafræn skýrslugerð með því að endurnýta Excel sniðmát (modify-electronic-reporting-format-reapply-excel-template/).

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk. Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu, Stofna skilgreiningarveitu og merkja hana sem virka.  

## <a name="select-the-er-format"></a>Veljið snið Rafræn skýrslugerð 
1. Smelltu á Grunnstillingar skýrslugerðar
2. Stækkið eða fellið saman „Greiðslulíka“ í trénu.
3. Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.
4. Smellt er á viðhengi
    * Athugið að SampleVendPaymWsReport.xlsx Excel skjalið er nú notað sem sniðmát fyrir greiðslubókarvinnslu.   
5. Smellt er á Opin.
    * Smellið á Opna til að skoða útlit Excel sniðmátsins.  
    * Yfirfara sniðmátið Athugið að það inniheldur eins og er eftirfarandi upplýsingar fyrir hverja greiðslulínu: reikningsnúmer lánardrottins, nafn lánardrottins, banki, leiðarnúmer, reikningsnúmer, debet, kredit og gjaldmiðill. Í þessu dæmi, viljum við útvíkka þennan lista með því að bæta upplýsingum við greiðsludagsetninguna.   
6. Lokið síðunni.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Endurnýta nýtt Excel sniðmát í sniði Rafræn skýrslugerð
1. Smellið á Hönnuður.
    * Opnið drög að sniði valinnar Rafræn skýrslugerð til að breyta.  
2. Í aðgerðasvæðinu er smellt á innflutningur.
3. Smellið á Uppfæra úr Excel
    * Smellið á „Uppfæra sniðmát“ og veljið svo skránna, SampleVendPaymWsReport2.xlsx.  
    * Smellið á Uppfæra sniðmát og flettið til að ná í SampleVendPaymWsReport2.xlsx skránna sem var halað niður áður.  
4. Smellið á „Í lagi“.
    * SampleVendPaymWsReport2.xlsx sniðmátið er virkt. Skipan sniðs Rafræn skýrslugerð er samstillt við innihald sniðmátsins, hvers einingum er bætt við snið Rafræn skýrslugerð. Allar einingar sem enn eru til í sniði Rafræn skýrslugerð, en eru ekki innifaldar í sniðinu, eru teknar út úr skilgreiningu sniðsins.  
5. Í trénu skal velja „Excel“.
    * Athugið að sniðmátsreiturinn inniheldur nú tilvísun í nýja sniðmátið.   
6. Smellt er á viðhengi
7. Smellt er á Opin.
    * Smellið á Opna til til að skoða útlit breytta Excel sniðmátsins.  
    * Yfirfara sniðmátið Athugið að nú inniheldur það línu fyrir greiðsludagsetningu.   
8. Lokið síðunni.
9. Stækkið „Excel“ í trénu.
10. Í tré skal víkka 'Excel\PaymLines'.
11. Í tré skal velja „Excel\PaymLines\PaymDate“.
    * Athugið að sniðið Rafræn skýrslugerð inniheldur nú fleira en eitt atriði. Hólf, PaymDate, hefur verið bætt við Excel sniðmát.  
12. Smelltu á flipann Vörpun.
13. Í trénu skal víkka út 'model'.
14. Í trénu skal víkka út 'model\Payments'.
15. Veljið 'model\Payments\Transaction date(TransactionDate)', í trénu.
16. Smelltu á Binda.
    * Tilgreindu hvaða gögnum er bætt við nýja hólfið við keyrslu.  
17. Smellið á „Vista“.
18. Lokið síðunni.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Virkja breytt drög að sniði Rafræn skýrslugerð til notkunar í greiðslubókarvinnslu
1. Í Aðgerðarrúðunni er smellt á skilgreiningar.
2. Smelltu á Færibreytur notanda
3. Veljið Já í svæðinu Stillingar keyrslu.
4. Smellið á „Í lagi“.
5. Smellið á „Breyta“.
6. Veljið Já í svæðinu drög keyrslu.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Nota breytt drög að sniði Rafræn skýrslugerð fyrir greiðslubókarvinnslu
    * Fara yfir stofnaðar vinnublað, þar á meðal nýjar upplýsingar um greiðslulínur – greiðsludagsetningu.  


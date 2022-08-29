---
title: Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 4 - keyra snið)
description: Þessi grein lýsir því hvernig á að stilla rafrænt skýrslusnið til að telja og leggja saman byggt á gögnum um þegar myndaðan textaúttak. (Hluti 4)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
ms.openlocfilehash: 7610e71346b57a7e624424418b22b40e51f9bb95
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290605"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a>Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 4 - keyra snið)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað. Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 3: Nota útreikninga til að búa til úttak)”.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Prófa þetta afbrigði fyrir myndun intrastat-skýrslur
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Í trénu skal víkka út 'Intrastat model'.
4. Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.
5. Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.
6. Í Aðgerðarrúðunni er smellt á skilgreiningar.
7. Smelltu á Færibreytur notanda
8. Veljið Já í svæðinu Stillingar keyrslu.
9. Smellið á „Í lagi“.
10. Smellið á „Breyta“.
11. Veljið Já í svæðinu drög keyrslu.
12. Smellið á „Vista“.
13. Fara í Skattur > Uppsetning > Erlend viðskipti > Færibreytur erlendra viðskipta.
14. Útvíkka hlutann Rafræn skýrslugerð.
15. Veljið skilgreininguna „Intrastat (DE) með talningu og samlagningu“.
16. Veljið skilgreininguna „Intrastat (DE) með talningu og samlagningu“.
17. Smelltu á Vista.
18. Lokið síðunni.
19. Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.
20. Smellið á úttak
21. Smellið á Skýrsluna.
    * Keyra myndunarferli intrastat-skýrslu.  
22. Í svæði Frá-dagsetningu, stilla á dagsetningu ' 2000-01-01 ".
    * Skilgreinið upphafs og lokadagsetningar fyrir skýrslutímabil sem innihalda fyrirliggjandi færslur í skjámyndinni.  
23. Í svæðinu Til dags, setja dagsetningu ' 2022-12-31'.
    * Skilgreinið upphafs og lokadagsetningar fyrir skýrslutímabil sem innihalda fyrirliggjandi færslur í skjámyndinni.  
24. Í reitnum stefna skal velja "komur".
25. Velja skal Já í svæðinu Mynda skrá.
26. Smellið á „Í lagi“.
    * Fara yfir stofnað úttak með samantektarlínur í lok.  
27. Smellið á „Nýtt“.
28. Í listanum skal merkja valda línu.
29. Í reitnum stefna skal velja "sendingar".
30. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
31. Sláið inn eða veldu gildi í vörur reitnum.
32. Stilla á þyngd á "10".
33. Stilla upphæð reiknings á "10000".
34. Stilla Tölfræðileg upphæð á "10000".
35. Smellið á úttak
36. Smellið á Skýrsluna.
37. Í reitnum stefna skal velja "sendingar".
38. Smellið á „Í lagi“.
    * Fara yfir stofnað úttak með samantektarlínur í lok. Athugið að það hefur verið breytt miðað við fyrstu keyrsluna.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Keyra þetta afbrigði er í kembiham til að endurskoða uppsöfnuð gögn talningar & samlagningar
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal víkka út 'Intrastat model'.
3. Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.
4. Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.
5. Í Aðgerðarrúðunni er smellt á skilgreiningar.
6. Smelltu á Færibreytur notanda
7. Velja skal Já í reitinn keyra í kembingarhami.
8. Smellið á „Í lagi“.
9. Lokið síðunni.
10. Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.
11. Smellið á úttak
12. Smellið á Skýrsluna.
13. Smellið á „Í lagi“.
14. Lokið síðunni.
15. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
16. Í trénu skal víkka út 'Intrastat model'.
17. Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.
18. Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.
19. Smelltu á kembingarkladda.
    * Athugið að kladdfærsla kembingar hefur verið stofnuð fyrir framkvæmd vinnslu á valinni skilgreiningu.  
20. Smellt er á Hengja við.
21. Smellt er á Opin.
    * Fara yfir stofnaða xml-skrána sem inniheldur upplýsingar um talningu og samlagningu sem safnað var við keyrslu á valinni skilgreiningu.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

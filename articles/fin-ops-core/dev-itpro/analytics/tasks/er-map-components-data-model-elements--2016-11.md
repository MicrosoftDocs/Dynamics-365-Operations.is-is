---
title: Rafræn skýrslugerð Varpa efnisþætti ef stofnað snið einingar gagnalíkans (nóvember 2016)
description: Í þessu efnisatriði er útskýrt hvernig á að varpa gagnalíkanseiningum í þætti stofnaðrar skilgreiningar rafrænnar skýrslugerðar.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c3c06abbd0b4cab5e672c83ccf9c28f2d148dae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751535"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>Rafræn skýrslugerð Varpa efnisþætti ef stofnað snið einingar gagnalíkans (nóvember 2016)

[!include [banner](../../includes/banner.md)]

Eftirfarandi ferli sýnir hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili Rafræn skýrslugerð getur varpað gagnalíkanaeiningar í íhluti af stofnaðri grunnstillingu Rafræn skýrslugerð, sem skilgreinir snið rafrænt skjal fyrir viðskiptalén greiðslna. Þetta snið verður notað síðar til að stofna rafræn skjöl fyrir úrvinnsla á greiðslum. Í þessu dæmi muntu stofna grunnstilling sniðs fyrir sýnifyrirtækið, „Litware, Inc.”. Þessi skref er hægt að framkvæma í hvaða fyrirtæki þar sem grunnstillingar rafrænnar skýrslugerðar eru samnýttar í öllum fyrirtækjum. Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkleiðbeiningunum „Stofna grunnstillingu sniðs“.


## <a name="select-a-format-configuration"></a>Velja grunnstillingu sniðs
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.
4. Í trénu, veljið 'Payments (einfaldað líkan)\BACS (UK upphugsað)'.
5. Smellið á Hönnuður.

## <a name="map-format-components-to-data-model-elements"></a>Varpa íhluti sniðs í einingar gagnalíkans
1. Smellt er á Víkka/draga saman.
2. Smelltu á flipann Vörpun.
3. Í trénu skal víkka út 'model'.
4. Í trénu skal velja 'Xml\Message\ProcessingDate\DateTime'.
5. Í trénu skal velja 'model\ProcessingDateTime'.
6. Smelltu á Binda.
7. Í trénu skal velja 'Xml\Message\MessageId\String'.
8. Í trénu skal velja 'model\MessageIdentification'.
9. Smelltu á Binda.
10. Í trénu skal víkka út 'model\Payments'.
11. Í trénu skal velja 'Xml\Message\Payments\Item\Amount\String'.
12. Í trénu skal velja 'model\Payments\InstructedAmount'.
13. Smelltu á Binda.
14. Í trénu skal velja 'Xml\Message\Payments\Item\TransDate\DateTime'.
15. Í trénu skal velja 'model\Payments\TransactionDate'.
16. Smelltu á Binda.
17. Í trénu skal velja 'Xml\Message\Payments\Item\Description\String'.
18. Veljið 'model\Payments\Description', í trénu.
19. Smelltu á Binda.
20. Í trénu skal velja 'Xml\Message\Payments\Item\Currency\String'.
21. Veljið 'líkan\greiðslur', í trénu.
22. Smelltu á Binda.
23. Í trénu skal velja 'Xml\Message\Payments\Item\Id'.
24. Í trénu skal velja 'model\Payments\End2EndID'.
25. Smelltu á Binda.
26. Útvíkka 'model\Payments\Creditor', í trénu.
27. Útvíkka 'model\Payments\Creditor\Account', í trénu.
28. Útvíkka 'model\Payments\Creditor\Agent', í trénu.
29. Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Name\String'.
30. Veljið 'model\Payments\Creditor\Name', í trénu.
31. Smelltu á Binda.
32. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.
33. Í trénu skal velja 'model\Payments\Creditor\Agent\RoutingNumber'.
34. Smelltu á Binda.
35. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.
36. Veljið 'model\Payments\Creditor\Account\Number', í trénu.
37. Smelltu á Binda.
38. Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Name\String'.
39. Útvíkka 'model\Payments\Debtor', í trénu.
40. Útvíkka 'model\Payments\Debtor\Account', í trénu.
41. Útvíkka 'model\Payments\Debtor\Agent', í trénu.
42. Veljið 'model\Payments\Debtor\Name', í trénu.
43. Smelltu á Binda.
44. Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.
45. Í trénu skal velja 'model\Payments\Debtor\Agent\RoutingNumber'.
46. Smelltu á Binda.
47. Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.
48. Veljið 'model\Payments\Debtor\Account\Number', í trénu.
49. Smelltu á Binda.
50. Í trénu skal velja 'Xml\Message\Payments\Item'.
51. Veljið 'model\Payments', í trénu.
52. Smelltu á Binda.
53. Smellið á „Vista“.

## <a name="validate-format-mapping"></a>Sannprófa vörpun sniðs
1. Smella á Villuleita.
    * Sannprófa nýja vörpun til að tryggja að allar bindingar séu í lagi.  
2. Lokið síðunni.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Breyta stöðu á gildandi útgáfu af skilgreiningarsniði
Í næsta skref verður breytt stöðu grunnstillingarsniðs úr Drög í Lokið til að gera það tiltækan fyrir myndun greiðsluskjala.  
1. Smellið á „Breyta stöðu“.
2. Smelltu á Ljúka.
3. Sláið inn gildi í reitnum „Lýsing“.
    * Til dæmis „Útgáfa 1“.  
4. Smellið á „Í lagi“.
5. Velja skal lokna útgáfa af núgildandi grunnstilling.
    * Athugið að sniðið er vistað sem lokin útgáfa 1.1. útgáfa 1 af sniðinu, sem er byggð á útgáfu 1 af gagnalíkaninu.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Tilgreina gildisdagsetning fyrir lokið útgáfa sniðs
Hægt er að skilgreina hverja sniðsútgáfa sem tiltæk fyrir notkun frá tilteknum degi. Þegar fleiri en ein útgáfa sniðs er virk á tilteknum degi, verður síðasta snið (á grundvelli útgáfunúmers) valið fyrir notkun. Dagsetningargildi lotu er notað til að velja rétta útgáfu.  

## <a name="restrict-access-to-created-format-from-companies"></a>Takmarka aðgang að stofnuðu sniði frá fyrirtækjum
1. Víkka út hlutann ISO lands-/svæðiskóða.
    * Hvert aðgangur sniðs má takmarka með því að auðkenna tiltekna lönd/svæði þar sem snið á við. Þegar listi yfir lönd/svæði fyrir tiltekið snið er tómt er hægt að nota þetta snið fyrir öll fyrirtæki. Þegar sumar ISO lands/svæðiskóða eru færðar inn á lista yfir lönd/svæði, er hægt að nota sniðið eingöngu í fyrirtæki sem hafa aðalaðsetur með landskóðinn af þeim lista.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
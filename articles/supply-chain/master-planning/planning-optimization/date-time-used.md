---
title: Færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar
description: Þetta efnisatriði veitir upplýsingar um færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar í sinni aðgerð.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0708404f286253449e0400fc65680e903f6d1e9b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468833"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar í sinni aðgerð.

Innbyggð aðaláætlunarvél notar færsludagsetningar í öllum útreikningum, en fínstilling áætlanagerðar vinnur með gildum dagsetningar og tíma sem eru umbreytt í dagsetningar. Þessi munur í hegðun getur leitt til kringumstæðna þar sem til dæmis spáfærslur sem stofnaðar eru á miðnætti á deginum sem aðaláætlanagerð er keyrð eru ekki hafðar með vegna þess að fínstilling áætlanagerðar lítur svo á að þær hafi verið stofnaðar á undan núverandi degi.

## <a name="parameters-for-issue-and-demand-transactions"></a>Færibreytur fyrir úthreyfingar- og eftirspurnarfærslur

Eftirfarandi tafla sýnir færibreyturnar sem fínstilling áætlanagerðar notar þegar hún vinnur úr úthreyfingar- og eftirspurnarfærslum.

| Færibreyta | Heiti færibreytu í fínstillingu áætlanagerðar | Lýsing | Jafngildur reitur í Microsoft Dynamics 365 Supply Chain Management (í ReqTrans-töflunni) |
|---|---|---|---|
| Áætlaður úthreyfingartími | `PlannedIssueTime` | Dagsetningin sem úthreyfingin er áætluð á. | **Til dagsetningar** (`FuturesDate`) og **Frestað til tíma** (`FuturesTime`) |
| Umbeðinn úthreyfingartími | `RequestedIssueTime` | Dagsetning úthreyfingar sem notandi bað um og stillt í Supply Chain Management. Þessi færibreyta á aðeins við um útgefnar eða samþykktar áætlaðar pantanir. Fyrir áætlaðar pantanir er hún sjálfgefið auð. | **Umbeðin dagsetning** (`ReqDateDlvOrig`) |
| Nauðsynlegur úthreyfingartími | `RequiredIssueTime` | Áskilin dagsetning úthreyfingar sem fínstilling áætlanagerðar breytir. Ef umbeðinn úthreyfingartími er í fortíðinni þegar fínstilling áætlanagerðar er keyrð verður áskildum tíma úthreyfingar breytt í fyrsta opna daginn sem er í fyrsta lagi dagurinn í dag. Ef umbeðinn tími úthreyfingar er merktur sem útilokaður í dagatalinu verður áskildum tíma úthreyfingar breytt í fyrsta opna daginn á undan þeirri dagsetningu. | **Dagsetning þarfa** (`ReqDate`) og **Tími þarfa** (`ReqTime`) |
| Seinkun úthreyfingartíma | `IssueTimeDelay` | Tímamunur milli áætlaðs úthreyfingartíma og annaðhvort umbeðins úthreyfingartíma fyrir samþykktar og útgefnar pantanir eða áskilins úthreyfingartíma. | **Seinkun (í dögum)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Færibreytur fyrir innhreyfingar- og framboðsfærslur

Eftirfarandi tafla sýnir færibreyturnar sem fínstilling áætlanagerðar notar þegar hún vinnur úr innhreyfingar- og framboðsfærslum.

| Færibreyta | Heiti færibreytu í fínstillingu áætlanagerðar | Lýsing | Sambærilegur reitur í Supply Chain Management (í töflunni ReqTrans eða ReqPO) |
|---|---|---|---|
| Áætlaður tími þegar tiltækt | `PlannedAvailabilityTime` | Dagsetningin þegar áætlað er að innhreyfingin sé tiltæk. | **Dagsetning þarfa** (`ReqDate`) og **Tími þarfa** (`ReqTime`) |
| Áætlaður tími innhreyfingar | `PlannedReceiptTime` | Dagsetningin þegar innhreyfingin kemur á staðinn. | **Til dagsetningar** (`FuturesDate`), **Seinkað til klukkan** (`FuturesTime`) og **Afhendingardagsetning** (`ReqDateDlv`) eða **Umbeðin dagsetning** (`ReqDateDlvOrig`) ef pöntunin er ekki enn útgefin. |
| Áskilinn tími þegar tiltækt | `RequiredAvailabilityTime` | Áskilin dagsetning þegar tiltækt sem fínstilling áætlanagerðar breytir. | **Dagsetning þarfa** (`ReqDate`) og **Tími þarfa** (`ReqTime`) |
| Væntanlegur móttökutími | `ExpectedReceiptTime` | Áætluð móttökudagsetning fyrir útgefna innhreyfingu. Notandinn stillir gildið í Supply Chain Management og fínstilling áætlanagerðar breytir því ekki. Þessi færibreyta á aðeins við um útgefnar innhreyfingar. | **Umbeðin dagsetning** (`ReqDateDlvOrig`) |
| Áskilinn tími innhreyfingar | `RequiredReceiptTime` | Áskilin móttökudagsetning sem fínstilling áætlanagerðar breytir. | **Dagsetning þarfa** (`ReqDate`) og **Tími þarfa** (`ReqTime`) |
| Tími áætlaðrar pöntunar | `PlannedOrderingTime` | Pöntunardagsetningin sem fínstilling áætlanagerðar reiknar út. | **Dagsetning pöntunar** (`ReqDateOrder`) og **Tími pöntunar** (`ReqTimeOrder`) |
| Upphafstími áætlaðs verkþáttar | `PlannedActivityStartTime` | Dagsetningin þegar verkþáttur fyrir þessa innhreyfingu á að hefjast. | **Upphafsdagur** (`SchedFromDate`) |
| Seinkun á móttökutíma | `ReceiptTimeDelay` | Tímamunur milli áætlaðs móttökutíma og áskilins móttökutíma. | **Seinkun (dagar)** (`FuturesDays`) og **Seinkað til klukkan** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Dæmi um færibreytu dagsetningar sem fínstilling áætlanagerðar notar

Áætlanirnar á eftirfarandi mynd eru á stigi dags, en fínstilling áætlanagerðar er keyrð á ítarlegra stigi. Þar sem mörkin geta verið í klukkustundum getur pöntunartími áætlanagerðar til að mynda verið 22. janúar 2021 klukkan 11:35 og svo framvegis.

### <a name="example-1-simple-scenario"></a>Dæmi 1: Einfaldar aðstæður

Ein sölupöntun sem hefur umbeðinn innhreyfingartíma 22. janúar er dekkuð af einni innkaupapöntun. Eftirfarandi stillingar eru notaðar:

- Enginn afhendingartími
- Engin dagatöl (Allir dagar eru opnir.)
- Engin framlegð

Eftirfarandi mynd sýnir þessar aðstæður. (Veldu myndina til að opna stærri útgáfu.)

[![Einfaldar aðstæður.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Dæmi 2: Aðstæður afhendingartíma

Ein sölupöntun sem hefur umbeðinn innhreyfingartíma 22. janúar er dekkuð af einni innkaupapöntun. Eftirfarandi stillingar eru notaðar:

- Þriggja daga afhendingartími
- Engin dagatöl (Allir dagar eru opnir.)
- Engin framlegð

Eftirfarandi mynd sýnir þessar aðstæður. (Veldu myndina til að opna stærri útgáfu.)

[![Aðstæður afhendingartíma.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Dæmi 3: Aðstæður svigrúms

Ein sölupöntun sem hefur umbeðinn innhreyfingartíma 22. janúar er dekkuð af einni innkaupapöntun. Eftirfarandi stillingar eru notaðar:

- Þriggja daga afhendingartími
- Fjögurra daga pöntunarbil
- Fimm daga bil til ráðstöfunar
- Engin dagatöl (Allir dagar eru opnir.)

Eftirfarandi mynd sýnir þessar aðstæður. (Veldu myndina til að opna stærri útgáfu.)

[![Aðstæður svigrúms.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Dæmi 4: Aðstæður seinkunar

Ein sölupöntun sem hefur umbeðinn innhreyfingartíma 22. janúar er dekkuð af einni innkaupapöntun. Í þessu dæmi eru notaðar sömu stillingar og í dæmi 3, en dagsetning áætlanagerðar hefur færst til 15. janúar. Röðun afturábak (rauðar merkingar) mistakast vegna þess að áætlaður pöntunartími yrði að vera á undan deginum í dag. Þar af leiðandi þarf aðaláætlanagerð að áætla fram í tíminn og seinkanir verða.

Eftirfarandi mynd sýnir þessar aðstæður. (Veldu myndina til að opna stærri útgáfu.)

[![Aðstæður seinkunar.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Dæmi 5: Flutningsaðstæður

Ein sölupöntun úr vöruhúsi 1 sem hefur umbeðinn útgáfutíma 22. janúar er dekkuð af einni flutningspöntun úr vöruhús 2 sem er dekkuð af áætlaðri innkaupapöntun. Eftirfarandi stillingar eru notaðar:

- Þriggja daga afhendingartími flutnings (vöruhús 1)
- Tveggja daga afhendingartími innkaupa (vöruhús 2)
- Engin dagatöl (Allir dagar eru opnir.)

Eftirfarandi mynd sýnir þessar aðstæður. (Veldu myndina til að opna stærri útgáfu.)

[![Flutningsaðstæður.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Dæmi 6: Aðstæður afhendingartíma með dagatölum

Ein sölupöntun sem hefur umbeðinn innhreyfingartíma 22. janúar er dekkuð af einni innkaupapöntun. Eftirfarandi stillingar eru notaðar:

- Þriggja daga afhendingartími
- Dagatal úthreyfingar (lokað á föstudögum)
- Framboðsdagatal (lokað á fimmtudögum og föstudögum)
- Dagatal móttöku (lokað á þriðjudögum, miðvikudögum og sunnudögum)
- Dagatal afhendingartíma (lokað á fimmtudögum og föstudögum)
- Pöntunardagatal (opið á mánudögum og laugardögum)

Eftirfarandi mynd sýnir þessar aðstæður. (Veldu myndina til að opna stærri útgáfu.)

[![Aðstæður afhendingartíma með dagatölum.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Dæmi 7: Aðstæður seinkunar með dagatölum

Ein sölupöntun sem hefur umbeðinn innhreyfingartíma 22. janúar er dekkuð af einni innkaupapöntun. Í þessu dæmi eru notaðar sömu stillingar og í dæmi 6, en dagsetning áætlanagerðar hefur færst til 13. janúar. Röðun afturábak (rauðar merkingar) mistakast vegna þess að áætlaður pöntunartími yrði að vera á undan deginum í dag. Þar af leiðandi þarf aðaláætlanagerð að áætla fram í tíminn og seinkanir verða.

Eftirfarandi mynd sýnir þessar aðstæður. (Veldu myndina til að opna stærri útgáfu.)

[![Aðstæður seinkunar með dagatölum.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)

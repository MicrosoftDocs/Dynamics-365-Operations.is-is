---
title: Viðhaldsspár
description: Þessi grein útskýrir viðhaldsspár í Eignastýringu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4e3da8ab9a739c8455d2c1d2720f94f91a42927d
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111601"
---
# <a name="maintenance-forecasts"></a>Viðhaldsspár

[!include [banner](../../includes/banner.md)]



Þegar þú býrð til verkbeiðni býrðu til verkbeiðnivinnslur sem hafa tengdar eignir og tegundir viðhaldsverka. Þegar þú velur tegund viðhaldsverks sem inniheldur viðhaldsspár eru spárnar afritaðar sjálfkrafa í verkbeiðnina.

Hugsanlega er hægt að bæta spálínum við verkbeiðni eða eyða þeim úr verkbeiðni. Uppsetning á líftímastöðu verkbeiðni, tengdri verkefnisgerð og stigareglum sem tengjast verkgerðinni ákvarðar hvort þú getur bætt við eða breytt spárlínum. Nánari upplýsingar um líftímastöður verkbeiðna og tengd verkefnastig, sjá [Spár, verkbeiðnir og verk](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Veljið **Eignastýring** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðni á listanum og síðan á aðgerðarrúðunni > flipanmu **Verkbeiðni** > hópnum **Verk**, velurðu **Spá**. Síðan **Viðhaldsspá verkbeiðni** sýnir spálínur úr gerð viðhaldsverks sem er valið í verkbeiðnivinnslunni.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Bættu tímaspá við verkbeiðni

1. Á síðunni **Viðhaldsspá verkbeiðni** velurðu vinnslu verkbeiðni til að bæta spá við.

2. Á flýtiflipanum **Klukkustundir** skaltu velja **Bæta við** til að búa til nýja línu.

3. Í reitnum **Flokkur** velurðu flokk.

4. Settu fjölda spáðra tíma inn í reitinn **Klukkutímar**.

5. Í reitnum **Línueign** skaltu velja tegund gjalds sem á að nota á línunni.


## <a name="add-an-items-forecast-to-a-work-order"></a>Bættu vöruspá við verkbeiðni

Það eru þrjár leiðir til að bæta hlutum við viðhaldsspá fyrir verkbeiðni. Þú getur búið til línur fyrir vörur (varahluti) sem eru ekki með í varahlutalistanum eða uppskrift eignar (BOM), þú getur valið varahluti af samþykktum varahlutalista og þú getur valið vörur úr uppskrift eignar.

- Á síðunni **Viðhaldsspá verkbeiðni** velurðu vinnslu verkbeiðni til að bæta spá við.

- Á flýtiflipanum **Atriði** bætirðu atriðum við viðhaldsspá með því að nota viðeigandi aðferð.

Til að stofna línu fyrir varahlut sem er ekki á varahlutalistanum eða lista yfir uppskriftir eigna fylgirðu þessum skrefum:

1. Veljið **Bæta við**.
2. Veldu vöru í reitnum **Vörunúmer**.
3. Inn í reitinn **Sölumagn** skal slá inn magnið.
4. Í reitnum **Einingu** velurðu mælieiningu fyrir magnið.
5. Í reitunum **Kostnaðarverð** og **Gjaldmiðill** slærðu inn viðeigandi gildi.
6. Í reitnum **Línueign** velurðu línueign.
7. Til að breyta lista yfir víddir sem eur sýndar í vörulínunum velurðu **Birgðir** > **Sýna víddir**, velur víddirnar og stillir síðan valkostinn **Vista uppsetningu** á **Já**.

Fylgdu þessum skrefum til að bæta við varahlutum úr viðurkenndum varahlutalista:

1. Veldu **Bæta við varahlutum**.
2. Veldu varahlutinn og breyttu tengdum upplýsingum eftir þörfum.
3. Veljið **Í lagi**.

Fylgdu þessum skrefum til að bæta við vöru úr uppskrift eignar:

1. Veldu **Bæta uppskriftarhlutum við**.
2. Veldu vöru og breyttu tengdum upplýsingum eftir þörfum.
3. Veljið **Í lagi**.

Til að fá yfirlit sem sýnir hvar hluturinn á völdum línum er notaður í tengslum við eignir, vanskil tegunda viðhaldsverka, varahluti og verkbeiðnir í eignastýringu velurðu **Notkunarstaður vöru**. Fyrir frekari upplýsingar um þetta yfirlit, sjá [Notkunarstaður vöru](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Bættu kostnaðarspá við verkbeiðni

1. Á síðunni **Viðhaldsspá verkbeiðni** velurðu vinnslu verkbeiðni til að bæta spá við.

2. Á flýtiflipanum **Kostnaður** skaltu velja **Bæta við** til að búa til línu.

3. Í reitnum **Flokkur** velurðu flokk.

4. Inn í reitinn **Magn** skal slá inn magnið.

5. Í reitina **Kostnaðarverð**, **Sölugjaldmiðill** og **Söluverð** skaltu rita viðeigandi gildi.

6. Í reitnum **Línueign** skaltu velja tegund gjalds sem á að nota á línunni.

>[!NOTE]
>Flýtiflipinn **Viðhaldsspá samtals** sýnir yfirlit yfir fjölda lína sem hafa verið stofnaðar fyrir valið verk í pöntun og fyrir verkbeiðni á hverjum flýtiflipa. Hann sýnir einnig samtölu af spáðum vinnutíma fyrir verkbeiðnivinnsluna og verkbeiðnina.

Skýringarmyndin hér að neðan sýnir dæmi um síðuna **Viðhaldsspá verkbeiðni**.

![Mynd 1.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Sjálfvirk uppfærsla á spám um verkbeiðnir

Ef tímakostnaður, vörukostnaður og útgjöld eru uppfærð í öðrum einingum er sjálfkrafa hægt að uppfæra verkbeiðni í Eignastýringu í samræmi við þær breytingar. Þessi afkastageta tryggir að nýjustu kostnaðarverðin séu ávallt notuð í spám þínum um verkbeiðnir. Einnig er hægt að gera svipaðar uppfærslur fyrir [spár um viðhaldverk](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Veldu **Eignastjórnun** > **Reglubundið** > **Spá** > **Uppfæra spá um verkbeiðni**.

2. Í glugganum **Uppfæra spá um verkbeiðni** á flýtiflipanum **Færslur til að taka með** er hægt að bæta við vali varðandi sérstakar verkbeiðnir eða verkbeiðnivinnslur, eftir þörfum. Smelltu á **Sía** til að gera viðeigandi val.

3. Á flýtiflipanum **Keyra í bakgrunni** geturðu sett upp sjálfvirka uppfærslu sem runuvinnslu, eftir þörfum.

4. Veldu **Í lagi** til að hefja uppfærslu á spá.


Skýringarmyndin hér að neðan sýnir dæmi um gluggann **Uppfæra verkbeiðnispá**.

![Mynd 2.](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

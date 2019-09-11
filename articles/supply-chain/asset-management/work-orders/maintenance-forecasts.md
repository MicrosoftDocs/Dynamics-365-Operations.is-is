---
title: Viðhaldsspár
description: Þetta efni skýrir viðhaldsspár í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875717"
---
# <a name="maintenance-forecasts"></a>Viðhaldsspár

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Þegar þú býrð til verkbeiðni býrðu til verkbeiðnivinnslur með tengdar eignir og tegundir viðhaldsverka. Þegar þú velur tegund viðhaldsverks sem inniheldur viðhaldsspár eru spárnar afritaðar sjálfkrafa í verkbeiðnina.

Þú gætir verið fær um að bæta við eða eyða spálínum í verkbeiðni. Uppsetning á líftímastöðu verkbeiðni, tengdri verkefnisgerð og stigareglum sem tengjast verkgerðinni ákvarðar hvort þú getur bætt við eða breytt spálínum. 

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina á listanum og smelltu á **Spá**. Í **Viðhaldsspá verkbeiðni** birtast spálínur úr gerð viðhaldsverks sem var valin í verkbeiðnivinnslunni.


## <a name="add-hours-forecast-to-a-work-order"></a>Bættu tímaspá við verkbeiðni

1. Veldu vinnslu verkbeiðni sem þú vilt bæta við spá.

2. Á flýtiflipanum **Klukkustundir** skaltu smella á **Bæta við** til að búa til nýja línu.

3. Veljið flokk í reitnum **Flokkur**.

4. Settu fjölda spáðra tíma inn í reitinn **Klukkutímar**.

5. Í reitnum **Línueign** skaltu velja gjaldtegundina sem á að nota á línunni.


## <a name="add-items-forecast-to-a-work-order"></a>Bættu vöruspá við verkbeiðni

Það eru þrjár leiðir til að bæta vörum við viðhaldsspá fyrir verkbeiðni: Þú getur búið til línur fyrir vörur (varahluti) sem eru ekki með í varahlutalistanum eða uppskrift eignar, þú getur valið varahluti af samþykktum varahlutalista og þú getur valið vörur úr uppskrift eignar.

1. Veldu vinnslu verkbeiðni sem þú vilt bæta við spá.

2. Velja skal flýtiflipann **Vörur**.

3. Smelltu á **Bæta við** til að búa til nýja línu fyrir varahluti sem er ekki á varahlutalistanum eða lista yfir uppskriftir eigna.

4. Veldu vöru í reitnum **Vörunúmer**.

5. Settu magn inn í reitinn **Sölumagn** og veldu magneiningu í reitnum **Eining**.

6. Settu inn kostnaðarverð og gjaldmiðil í viðkomandi reiti og veldu **Línueiginleiki**.

7. Ef þú vilt breyta lista yfir víddir sem birtast í vörulínunum smellirðu á **Birgðir** > **Sýna víddir**, velur víddirnar og velur „Já“ á skiptihnappnum **Vista uppsetningu**.

8. Ef þú vilt bæta viðurkenndum varahlutum við viðhaldsspá smellirðu á **Bæta við varahlutum**, velur varahlutinn, breytir tengdum upplýsingum ef þörf krefur og smellir á **Í lagi**.

9. Ef þú vilt bæta uppskriftahlutum eigna við spána smellirðu á **Bæta uppskriftarhlutum við**, velur hlutinn, breytir upplýsingum ef þörf krefur og smellir á **Í lagi**.

10. Smelltu á **Notkunarstaður vöru** ef þú vilt fá yfirlit yfir hvar vara í valinni línu er notuð í eignastjórnun í tengslum við eignir, tegundasjálfgildi viðhaldsverka, varahluti og verkbeiðnir. 



## <a name="add-expense-forecast-to-a-work-order"></a>Bættu kostnaðarspá við verkbeiðni

1. Þetta efni útskýrir hvernig á að bæta kostnaðarspá við kostnaður. Veldu vinstra megin í skjámyndinni þá verkbeiðni sem þú vilt bæta spá við.

2. Velja skal flýtiflipann **Kostnaður**.

3. Smellt er á **Bæta við** til að búa til nýja línu.

4. Veljið flokk í reitnum **Flokkur**.

5. Settu magn inn í reitinn **Magn**.

6. Settu inn kostnaðarverð, sölugjaldmiðil og söluverð í viðkomandi reiti.

7. Í reitnum **Línueign** skaltu velja gjaldtegundina sem á að nota á línunni.

>[!NOTE]
>Á flýtiflipanum **Viðhaldsspá samtals** geturðu séð yfirlit yfir fjölda lína sem eru búnar til á hverjum flipa, fyrir valið verk í pöntun og fyrir verkbeiðni. Einnig er hægt að sjá summu af spáðum vinnutíma fyrir verkbeiðnivinnsluna og fyrir verkbeiðnina.

![Mynd 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Sjálfvirk uppfærsla á spám um verkbeiðnir

Í eignastjórnun geturðu sjálfkrafa uppfært allar breytingar á spám um verkbeiðnir varðandi kostnað á klukkustund, vörukostnað og útgjöld sem hafa verið uppfærð í öðrum einingum í Dynamics 365 for Finance and Operations. Þetta er gert til að tryggja að nýjustu kostnaðarverðin séu ávallt notuð í spám þínum um verkbeiðnir. Það er líka mögulegt að gera svipaðar uppfærslur fyrir [spár um viðhaldverk](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Smelltu á **Eignastjórnun** > **Reglubundið** > **Spá** > **Uppfæra spá um verkbeiðni**.

2. Í fellivalmyndinni **Uppfæra spá um verkbeiðni** er hægt að bæta við vali varðandi sérstakar verkbeiðnir eða verkbeiðnivinnslur, ef þess er krafist. Smelltu á **Sía** til að gera það val.

3. Ef með þarf er hægt að setja upp sjálfvirka uppfærslu sem runuvinnslu á flýtiflipanum **Keyra í bakgrunni**.

4. Smelltu á **Í lagi** til að hefja uppfærslu á spá.


![Mynd 2](media/07-work-orders.png)


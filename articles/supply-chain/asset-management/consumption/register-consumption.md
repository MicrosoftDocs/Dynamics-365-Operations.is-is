---
title: Skrá notkun
description: Þessi grein útskýrir hvernig á að skrá neyslu í eignastýringu.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 588da2a217a56d2bc25f85c9a10c6589f90b16a1
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015086"
---
# <a name="register-consumption"></a>Skrá notkun

[!include [banner](../../includes/banner.md)]

 

Þegar viðhaldsverkum hefur verið lokið í verkbeiðni er næsta skref að gera notkunarskráningar og bóka færslubækurnar. Þú getur gert skráningar á eftirfarandi notkunargerðum: Tímum, vörum og kostnaði. Mismunandi notkunargerðir eru skráðar og bókaðar á síðunni **Færslubækur verkbeiðna**. Uppsetning færslubókarinnar í **Eignastjórnun** er notuð til að stofna og bóka aðskildar færslubækur fyrir tíma, vörur og kostnað í einingunni **Verkefnisstjórnun og bókhald**.

Í sumum tilfellum kann að vera hægt að bæta við eða eyða spálínum í verkbeiðni. Uppsetning á líftímastöðu verkbeiðni, tengdri verkefnisgerð og stigareglum sem tengjast verkgerðinni ákvarðar hvort þú getur bætt við eða breytt færslubókarlínum. Lestu nánar um líftímastöður verkbeiðna og tengd verkefnastig í [Spár, verkbeiðnir og verk](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Það er mögulegt að setja upp sjálfvirka bókun færslubóka í líftímastöður verkbeiðni. Sjá [Líftímastöður verkbeiðni](../setup-for-work-orders/work-order-lifecycle-states.md) fyrir meiri upplýsingar.

1. Smellur **Eignastýring** > **Verkbeiðnir** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.

2. Veldu verkbeiðnina og smelltu á **Færslubækur**.

3. Smelltu á **Afrita úr spá** til að flytja allar spálínur sem kunna að vera tengdar verkbeiðninni. Þú getur valið hvaða notkunargerðir þú vilt flytja.

4. Ef nauðsyn krefur geturðu bætt við fleiri notkunarlínum á viðkomandi flýtiflipa með því að smella á **Bæta við línu** og fylla út gögn á línunni.

5. Smelltu á **Staðfesta færslubækur** til að staðfesta færslubókarlínurnar áður en þær eru bókaðar.

6. Smelltu á **Bóka færslubækur** til að bóka færslubókarlínur.

7. Eftir að þú hefur sent neysludagbókina geturðu uppfært stöðu líftíma verkbeiðni. Til dæmis, til að gefa til kynna að verkbeiðninni hafi verið lokið, geturðu uppfært líftímastöðunni í „Lokið“.

    - Í reitnum **Sýna** sem er staðsettur efst á síðunni **Verkbeiðnifærslubækur** velurðu hvaða færslubókarlínur þú vilt sjá: **Allar**, **Óbókaðar** eða **Bókaðar**. Bókaðar færslubækur eru með hak í gátreitnum **Bókað**.  
    - Þegar vörulínur eru stofnaðar í verkbeiðnifærslubókinni eru vöruvíddir og rakningarvíddir sem tengjast vörunni sjálfkrafa fluttar á færslubókarlínuna.  

Skjámyndin hér að neðan sýnir dæmi um skráningu klukkutíma og vöru í verkbeiðni í **Verkbeiðnifærslubókum**.

![Mynd 1.](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Skiptu tíma á verkbeiðnum með nokkrum verkbeiðniverkum

Ef verkbeiðni inniheldur nokkur verkbeiðniverk geturðu skráð vinnutíma með því að nota virknina **Skipta tímum**, sem þýðir að klukkustundar skráningarlínu má dreifa jafnt um hvert verkbeiðniverk.

1. Smellur **Eignastýring** > **Verkbeiðnir** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.

2. Veldu verkbeiðnina og smelltu á **Færslubækur**.

3. Veldu klukkutímaskráningarlínuna sem þú vilt skipta og smelltu á **Skipta tímum**.

4. Í glugganum **Skipta tímum á viðhaldsverkum verkbeiðni** birtist nafn starfskrafts sem er innskráður sjálfkrafa í reitnum **Starfskraftur**. Hægt er að velja annan starfskraft, ef þörf krefur.

5. Veldu flokk fyrir klukkutímaskráninguna í reitnum **Flokkur**.

6. Settu fjölda vinnutíma sem á að skipta í reitnum **Klukkutímar**.

    ![Mynd 2.](media/02-consumption.png)

7. Smellt er á **OK**.

*Dæmi:* Í skjámyndinni hér að neðan eru dagbókarlínur fyrir verkbeiðni sem innihalda þrjú verkbeiðniverk. Fyrstu línunni, sem hefur að geyma þrjá vinnutíma, hefur verið skipt og er einn vinnutími skráður í hvert verkbeiðniverk. Eftir að þriggja tíma skráningarlínur eru búnar til ákveður þú hvað þú átt að gera við upphaflegu klukkutímaskráningarlínuna (fyrsta línan í dæminu). Þú getur haldið því eins og það er eða eytt því. 

![Mynd 3.](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Fjárhagsvíddir á notkunarskráningum

Þegar þú skráir notkun er fjárhagsvíddum tengdum mismunandi skráningartegundum bætt við skráningarnar í tiltekinni röð. 

- *Skráning klukkustundar og kostnaðar:* Í fyrsta lagi er fjárhagsvíddum úr færslubókarhaus bætt við, ef einhver er. Næst er fjárhagsvíddum úr tengdri verkbeiðniverki bætt við. Að lokum er fjárhagsvíddum úr tilföngunum (starfsmanni) bætt við.

- *Vöruskráningar:* Í fyrsta lagi er fjárhagsvíddum úr færslubókarhaus bætt við, ef einhver er. Síðan er fjárhagsvíddum úr tengdri verkbeiðniverki bætt við. Næst er fjárhagsvíddum af svæðinu bætt við. Að lokum er fjárhagsvíddum úr vörunni bætt við.

>[!NOTE]
>Fyrir allar þrjár skráningargerðirnar er samsetning fjárhagsvíddar staðfest og ógildar samsetningar eru auðar. Þetta er venjuleg uppsetning í öðrum forritum Finance and Operations.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
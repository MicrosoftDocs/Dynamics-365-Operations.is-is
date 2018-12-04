---
title: "Viðvaranir"
description: "Þetta efnisatriði gefur almennar upplýsingar um viðvaranir í Microsoft Dynamics 365 for Finance and Operations. Þú getur notað viðvaranir til að fylgjast með atburðum sem þú vilt rekja meðan á vinnudegi stendur."
author: tjvass
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 38309e986c1d284ed63be760745b20a5415adb4c
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="alerts"></a>Viðvaranir

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Um viðvaranir
Viðvaranir skapa tilkynningarkerfi fyrir mikilvæga atburði í Microsoft Dynamics 365 for Finance and Operations. Þú getur notað viðvaranir til að fylgjast með atburðum sem þú vilt rekja meðan á vinnudegi stendur. Þú getur auðveldlega búið til þitt eigið sett af viðvörunarreglum þannig að þú fáir viðvaranir um afhendingar sem er komnar fram yfir á tíma, pantanir sem eru eyddar, verð sem breytast eða aðra atburði sem þú verður að bregðast við.

Í áætlunar- og bókhaldskerfi (ERP) eru nokkrar dæmigerðar aðstæður þar sem hægt er að nota viðvörunareiginleikann í Finance and Operations. Hér eru nokkur dæmi.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Dæmi 1: Búðu til viðvörunarreglu fyrir nýjar sölupantanir
1. Opnaðu síðuna **Allar sölupantanir**.
2. Á aðgerðasvæðinu, á flipanum **Valkostir** í flokknum **Deila** skal velja **Búa til sérsniðna viðvörun**.
3. Í svarglugganum **Búa til viðvörunarreglu**, á flýtiflipanum **Láta mig vita þegar**, í reitnum **Atvik** skal velja **Færsla hefur verið búin til**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Dæmi 2: Búðu til viðvörunarreglu um frestun á afhendingardegi
1. Opnaðu síðuna **Allar innkaupapantanir**.
2. Veldu kenni innkaupapöntunar til að fá aðgang að upplýsingum um innkaupapöntunina.
3. Stækkaðu flýtiflipann **Haus innkaupapöntunar**.
4. Á aðgerðasvæðinu, á flipanum **Valkostir** í flokknum **Deila** skal velja **Búa til sérsniðna viðvörun**.
5. Í svarglugganum **Búa til viðvörunarreglu**, á flýtiflipanum **Láta mig vita þegar**, í reitnum **Reitur** skal velja **Afhendingardagur**.
6. Í reitnum **Atvik** skal velja **hefur verið frestað**.
    
Eftir að þú hefur lokað svarglugganum **Búa til viðvörunarreglu** birtist reglan þín á síðunni **Stjórna viðvörunarreglum**. Þú getur notað síðuna **Stjórna viðvörunarreglum** til að uppfæra núverandi viðvörunarreglur. Til dæmis getur þú breytt atburðakveikjum, uppfært tilkynningar um viðburði og uppfært lokadagsetningar. Til að opna síðuna **Stjórna viðvörunarreglum** skal nota hnappinn **Láta mig vita þegar** á flipanum **Valkostir** á aðgerðasvæðinu.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Hvað gerist þegar viðvörunarregla er búin til?
Þegar þú býrð til viðvörunarreglur getur þú tengt fyrirframskilgreint atvik við tiltekinn reit. Til dæmis þegar kemur að dagsetningunni sem tilgreind er í reitnum eða innihald reitsins breytist. Að öðrum kosti er hægt að tengja atvik við færslurnar á tiltekinni síðu. Til dæmis þegar færsla er búin til eða færslu er eytt.

Þegar valið atvik á sér stað fyrir reitinn eða fyrir færslu á síðunni er viðvörun send á þig. Til dæmis, getur þú búið til reglu sem þú tengir reitinn **Afhendingardagur** á tiltekinni innkaupapöntunarlínu við atvikið **var komið á tíma fyrir þetta löngum tíma síðan**. Þú stillir tímarammann í fimm daga. Í þessu tilviki er viðvörun send fimm dögum eftir afhendingardag á þessari innkaupapöntunarlínu.

Að auki geturðu þrengt viðvörunarreglur með því að setja skilyrði. Til dæmis getur þú fengið viðvörun um nýjar innkaupapantanir sem eru búnar til fyrir tiltekna lánardrottnalykla.

## <a name="preparing-for-an-alert"></a>Undirbúningur fyrir viðvörun
Áður en þú setur upp viðvörunarreglu skaltu ákveða hvenær eða í hvaða aðstæðum þú vilt fá viðvaranir. Þegar þú veist hvaða atvik þú vilt fá tilkynningu um skaltu finna, í Finance and Operations, síðuna með gögnunum sem valda því að atvikið birtist. Atvikið getur verið dagsetning sem kemur eða tilteknar breytingar sem eiga sér stað. Þess vegna verður þú að finna síðuna þar sem dagsetningin er tilgreind eða hvar reiturinn er sem breytist eða hvar nýja færslan birtist sem er búin til. Eftir að þú hefur þessar upplýsingar er hægt að búa til viðvörunarregluna.

## <a name="components-of-an-alert-rule"></a>Hlutar viðvörunarreglu
Viðvörunarregla hefur fimm hluta:

- **Atvik** - Atvikið sem kveikir á viðvörunarregla getur verið dagsetning sem kemur eða tiltekin breyting sem á sér stað. Þú skilgreinir atburði á flýtiflipanum **Senda viðvörun í tölvupósti vegna breytinga á stöðu vinnslu** í svarglugganum **Búa til viðvörunarreglu**.
- **Skilyrði** - Á flýtiflipanum **Láta mig vita um** í svarglugganum **Búa til viðvörunarreglu** er hægt að velja umfang skilyrðisins til að stjórna því hvenær þú færð viðvörun um atvik. Þú getur notað regluna annaðhvort aðeins á gildandi færslu eða öllum sýnilegum færslum á síðunni. Ef reglan gildir þvert yfir lögaðila, getur þú stillt valkostinn **Fyrirtækið í heild sinni** á **Já**.
- **Fyrning á reglu** - Á flýtiflipanum **Láta mig vita þangað til** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hversu lengi viðvörunarreglan á að vera virk.
- **Efni** - Á flýtiflipanum **Láta mig vita með** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina efnistexta og textaskilaboð sem viðvörunarskilaboðin eiga að nota.
- **Notandi** - Á flýtiflipanum **Láta hvern vita** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hvaða notandi á að taka á móti viðvörunarskilaboðunum. Að sjálfgefnu er notandakenni þitt valið.

    > [!NOTE]
    > Þessi valkostur er takmarkaður við stjórnendur fyrirtækis.

## <a name="email-notifications-from-alerts"></a>Tilkynningar í tölvupósti frá viðvörunum
Tilkynningar í tölvupósti frá viðvörunum eru enn ekki virkjaðar. Þetta verður gert virkt í síðari útgáfu.


---
title: Kostnaðar- og dagsetningarstýring
description: Þetta efni skýrir kostnaðar- og dagsetningastýringu í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 18373ff16b63ea61a3a4bc38ee7fa0b5e33154b5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430231"
---
# <a name="cost-and-date-control"></a>Kostnaðar- og dagsetningarstýring

[!include [banner](../../includes/banner.md)]

 

Í eignastýringu er hægt að reikna út kostnað til að fá yfirlit yfir raunkostnað miðað við kostnað fjárhagsáætlunar á eignum, virkum staðsetningum og verkbeiðnum. Raunkostnaður byggist á bókfærðum færslum. 

Þú getur líka gert útreikning á dagsetningum ef þú vilt bera saman áætlaðar upphafs- og lokadagsetningar við raunverulegar upphafs- og lokadagsetningar á verkbeiðnum.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kostnaðarstýring á eignum, virkum staðssetningum og verkbeiðnum

Útreikningar á eignum, starfrænum stöðum og vinnupöntunum eru nánast eins. Eini munurinn er sá að fyrir eignir og virkar staðsetningar geturðu einnig haft undireignir og undirstaði með í útreikningum. Dagsetningin er færsludagsetningin þegar skráningin var skráð.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Stýring eignakostnaðar** eða **Kostnaðarstýring virkra staðsetninga**, eða **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Kostnaðarstýring verkbeiðni**.

2. Í glugganum **Stýring eignakostnaðar** / **Kostnaðarstýring virkra staðsetninga** / **Kostnaðarstýring verkbeiðni** velurðu tímabil sem á að reikna út.

3. Ef þörf krefur velurðu fjárhagsvídd sem sett er inn í útreikninginn.

4. Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með kostnað við núll.

5. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að kostnaðarstýringarlínur séu varðandi virkar staðsetningar. 

    Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar kostnaðarstýringarlínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. 
    
    Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar kostnaðarstýringarlínur á öllum virkum staðsetningarstigum sem þær tengjast.

6. Veldu „Já“ á skiptihnappnum **Sýna opinn ráðstafaðan kostnað** ef þú vilt láta dálkinn fylgja með í útreikningnum.

7. Veldu „Já“ á skiptihnappnuum **Hafa undireignir með** til að sýna kostnað sem tengist undireignum sem aðskildar línur.

8. Ef þú vilt takmarka leitina geturðu valið sérstakar eignir / virkar staðsetningar / verkbeiðnum á flýtiflipanum **Færslur til að taka með**.

9. Smellið á **Í lagi** til að byrja að reikna.

    Myndin hér að neðan sýnir dæmi um gluggann **Stýring eignakostnaðar**.

    ![Valmyndin Stýring eignakostnaðar](media/01-controlling-and-reporting.png)

10. Á síðunni **Stýring eignakostnaðar** smellirðu á hnappana **Flokka eftir** til að sýna áskilið upplýsingastig útreikningsins. Valdir hnappar **Flokka eftir** eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

## <a name="example"></a>Dæmi

Skjáskotið hér að neðan sýnir dæmi um niðurstöður útreiknings í **Stýringu eignakostnaðar**.

- Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarkostnað vegna kostnaðar við spá um verkbeiðni. 
- Reiturinn **Ráðstafaður kostnaður** sýnir heildarupphæð kostnaðar sem lögaðili hefur skuldbundið sig til að greiða. 
- Reiturinn **Opinn ráðstafaður kostnaður** sýnir skuldbindingar um greiðslu fyrir vörur, tíma og þjónustu sem þú hefur pantað eða fengið en hefur ekki enn borgað fyrir. 
- Reiturinn **Raunkostnaður** sýnir tengdan kostnað eftir að allar notkunarskráningar hafa verið bókaðar.

![Dæmi um niðurstöður útreikninga í Stýringu eignakostnaðar](media/02-controlling-and-reporting.png)

Önnur leið til að gera kostnaðarútreikning er að velja margar eignir í **Allar eignir** eða **Virkar eignir**. Smelltu síðan á hnappinn **Kostnaðarstýring** á flipnanum **Almennt**. Í glugganum **Stýring eignakostnaðar** eru valdar eignir sjálfkrafa settar inn í reitinn **Eignir** á flýtiflipanum **Færslur til að hafa með**. Smelltu á **Í lagi** og kostnaðarútreikningur fyrir valdar eignir er sýndur. Sama ferli er hægt að gera fyrir virkar staðsetningar í **Allar virkar staðsetningar** eða **Virkar virkar staðsetningar**, og vegna verkbeiðna í **Allar verkbeiðnir** eða **Virkar vinnupantanir**.


## <a name="work-order-date-control"></a>Dagsetningastjórnun verkbeiðni

Notaðu þessa síðu til að fá yfirlit yfir væntanlegar upphafs- og lokadagsetningar samanborið við raunverulega upphafs- og lokadagsetningar á verkbeiðnum.

1. Smelltu á **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Dagsetningarstýring verkbeiðni**.

2. Smelltu á **Reikna út**.

3. Veldu virka staðsetningu í reitnum **Virk staðsetning**.

4. Settu tímabilið sem þú vilt gera útreikninginn fyrir í reitunum **Frá dagsetningu** og **Til dagsetningar**. Allar verkbeiðnir með áætlaða byrjunardags. innan tímabilsins verða með.

5. Smellt er á **OK**.

6. Smelltu á hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn. Valdir hnappar **Flokka eftir** eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

## <a name="example"></a>Dæmi

Skjáskotið hér að neðan sýnir dæmi um niðurstöður útreiknings í **Dagsetningastýringu verkbeiðni**.

- Reiturinn **Meðalseinkun upphafs** sýnir mismuninn í dögum milli áætlaðs upphafsdags fyrir verkbeiðni miðað við raunverulegan upphafsdag. Ef til dæmis raunupphafsdagsetningin var tveimur dögum fyrir áætlaðan upphafsdag birtist „-2“ í þessum reit.  
- Reiturinn **Meðalseinkun loka** sýnir mismuninn í dögum milli áætlaðs lokadags fyrir verkbeiðni miðað við raunverulegan lokadag. Ef til dæmis raunlokadagsetningin var þremur dögum eftir áætlaðan lokadag birtist „-3“ í þessum reit.  
- Reitirnir **Tilvik** sýna fjölda skipta sem frávik eiga sér stað í tengslum við áætlaða og raunverulega upphafsdagsetningu og áætlaða og raunverulega lokadagsetningu í verkbeiðninni.

![Dæmi um niðurstöður útreikninga í Dagsetningastjórnun verkbeiðni](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Stjórnun vinnustunda
description: Þetta efni útskýrir stjórnun vinnustunda í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0d2f4e86b5dec84d4a24db6a4f9f9f16f6a765bd
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889195"
---
# <a name="work-hour-control"></a>Stjórnun vinnustunda

[!include [banner](../../includes/banner.md)]

 

Í eignastýringu er hægt að reikna út stundir til að fá yfirlit yfir raunverulegar stundir miðað við áætlaðar stundir á eignum, virkum staðsetningum eða verkbeiðnum. Raunstundir byggjast á bókfærðum færslum.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Stjórnun vinnustunda á eignum, virkum staðssetningum og verkbeiðnum

Útreikningar á eignum, starfrænum stöðum og vinnupöntunum eru nánast eins. Eini munurinn er sá að fyrir eignir og virkar staðsetningar geturðu einnig haft undireignir og undirstaði með í útreikningum. Dagsetningin er færsludagsetningin þegar skráningin var skráð.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Stjórnun eignastunda** eða **Vinnustundastjórnun virkra staðsetninga**, eða **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Vinnustundastjórnun verkbeiðni**.

2. Í valmyndinni **Vinnustundastjórnun eigna**, .

3. Í glugganum **Stjórnun eignastunda** / **Stjórnun stunda virka staðsetninga** / **Stjórnun stunda verkbeiðni** velurðu tímabil sem á að reikna út í reitunum **Frá dagsetningu** og **Til dags.**.

4. Ef þörf krefur velurðu **Sett fjárhagsvídda** sem sett er inn í útreikninginn.

5. Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með núlltímum.

6. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að stjórnunarlínur stunda séu varðandi virkar staðsetningar. 

    Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar stjórnunarlínur stunda fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. 
    
    Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar stjórnunarlínur stunda á öllum virkum staðsetningarstigum sem þær tengjast.

7. Veldu „Já“ á skiptihnappnuum **Hafa undireignir með** til að sýna kostnað sem tengist undireignum sem aðskildar línur.

8. Ef þú vilt takmarka leitina geturðu valið sérstakar eignir / virkar staðsetningar / verkbeiðnum á flýtiflipanum **Færslur til að taka með**.

9. Smellið á **Í lagi** til að byrja að reikna.

10. Á síðunni **Stjórnun eignastunda** smellirðu á hnappana **Flokka eftir** til að sýna áskilið upplýsingastig útreikningsins. Valdir hnappar **Flokka eftir** eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

## <a name="example"></a>Dæmi

Skjámyndin hér að neðan sýnir dæmi um útreikning á **Stjórnun eignastunda**.

- Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarstundir frá spá um verkbeiðni. 
- Reiturinn **Raunverulegar stundir** sýnir bókaðar stundir vegna verkbeiðna. 
- Reiturinn **Ráðstafaðar stundir** sýnir heildarmagn stunda sem fyrirtækið þitt skuldbindur sig til vegna verkbeiðna.

![Dæmi um útreikning á stjórnun eigna tíma](media/04-controlling-and-reporting.png)

Önnur leið til að gera stundaútreikning er að velja margar eignir í **Allar eignir** eða **Virkar eignir**. Smelltu síðan á hnappinn **Stundastjórnun** á flýtiflipanum **Almennt**. Valdar eignir eru sjálfkrafa settar inn í reitnum **Eignir** á flýtiflipanum **Færslur til að taka með**. Smelltu á **Í lagi** í glugganum **Stjórnun eignastunda** og útreikningur fyrir valdar eignir er sýndur. Sama ferli er hægt að gera fyrir virkar staðsetningar í **Allar virkar staðsetningar** eða **Virkar virkar staðsetningar**, og vegna verkbeiðna í **Allar verkbeiðnir** eða **Virkar vinnupantanir**.



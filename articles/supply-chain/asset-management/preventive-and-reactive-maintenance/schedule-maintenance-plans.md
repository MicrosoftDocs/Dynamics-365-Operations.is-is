---
title: Tímasetja viðhaldsáætlanir
description: Þetta efni skýrir tímasetningu viðhaldsáætlana í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: df5bcd57c611ed5f77a417a28f28fca84057d734
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430446"
---
# <a name="schedule-maintenance-plans"></a>Tímasetja viðhaldsáætlanir

[!include [banner](../../includes/banner.md)]

 

Skipulagning forvirks viðhalds býr til dagatalsfærslur á eignum, byggt á viðhaldsáætlunum sem settar eru upp á eignunum. Þú getur skipulagt dagatalfærslur út frá völdum viðhaldsáætlunum, eignategundum og eignum.

1. Smelltu á **Eignastjórnun** > **Reglubundið** > **Forvirkt viðhald** > **Skipuleggja viðhaldsáætlanir**.

2. Þú getur valið tímabil í reitunum **Tímabil** og **Tímabilstíðni**.

>[!NOTE]
>Reitirnir **Tímabil** og **Tímabilstíðni** gefa til kynna hversu langt fram í tímann þú vilt að viðhaldsáætlunarlínur séu búnar til, byggt á viðhaldsáætlunum sem þú hefur búið til (tímabyggðum eða teljarabyggðum). Á myndinni hér að neðan eru viðhaldsskemalínur (= tillögur um verkbeiðnir) búnar til frá núverandi degi og þrjá mánuði fram í tímann.

3. Veldu „Já“ á skiptihnappnum **Stofna sjálfkrafa ef tilgreint í línunni** ef verkbeiðnir eiga að vera sjálfkrafa stofnaðar í samræmi við viðhaldsáætlunarlínuna.

>[!NOTE]
>Ef þessi rofahnappur er stilltur á „Já“ *og* gátreiturinn **Stofna sjálfvirkt** er einnig valinn í viðhaldsáætlunarlínum í skjámyndinni **Viðhaldsáætlanir** eru verkbeiðnir búnar til út frá viðhaldsáætlunarlínum og viðhaldsskemalínur með stöðuna „Verkbeiðni stofnuð“ eru einnig stofnaðar. Ef aðeins einn valkostur er valinn (**Stofna sjálfkrafa ef tilgreint í línunni** rofahnappinn í þessum glugga eða gátreitnum **Stofna sjálfkrafa** í skjámyndinni **Viðhaldsáætlanir**) eru aðeins viðhaldsskemalínur búnar til með stöðuna „Stofnað“. Þá eru engar verkbeiðnir stofnaðar.

4. Það er hægt að búa til dagatalsfærslur byggðar á viðhaldsáætlunum (tíma eða teljara), eignum, eignategundum, virkum stöðum og virkum staðartegundum. Smelltu á hnappinn **Sía** og gerðu val þitt ef þess er krafist.

- Varðandi röðun á viðhaldsáætlunum á virkum staðsetningum: Ef þú uppfærir uppsetningu á eignategundum, framleiðendum og tegundum í viðhaldsáætlunum í flýtiflipanum **Allar virkar staðsetningar** > **Viðhaldsáætlanir** eftir að þú hefur skipulagt viðhaldsáætlanir, verður núverandi viðhaldsskemafærslum sem tengjast þeirri virku staðsetningu sjálfkrafa eytt. Til að stofna nýjar dagatalsfærslur sem samsvara uppfærðri viðhaldsáætlunaruppsetningu á virkri staðsetningu verður þú að keyra nýja viðhaldsáætlun fyrir þá virku staðsetningu. Lestu meira um uppsetningu á eignategundum, framleiðendum og tegundum um virkar staðsetningar í [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md).

>*Dæmi:* Þú vilt búa til viðhaldsáætlun fyrir tiltekna virka staðsetningu, sem þýðir að allar eignir sem settar eru upp á þeirri virku staðsetningu á hverjum tíma verða með þegar þú áætlar viðhaldsáætlun. Í því tilfelli býrðu til viðhaldsáætlun og velur sérstaka virka staðsetningu en bætir EKKI við neinum eignum í viðhaldsáætluninni. Niðurstaðan er sú að þegar þú áætlar þá viðhaldsáætlun verða línur um viðhaldsskema stofnaðar fyrir allar eignir sem tengjast virkri staðsetningu á þeim tíma.

- Ef þú gerir breytingar á eignategundum, framleiðendum og tegundum í **Gerðir eigna** hafa þessar breytingar aðeins áhrif á nýjar eignir sem nota uppfærðu eignategundina. Lestu meira um uppsetningargerð eigna í [Gerðir eigna](../setup-for-objects/object-types.md).  

5. Smelltu á **Í lagi** til að hefja myndun á viðhaldsskemafærslum á eignum. Myndaðar færslur verða sýndar á listasíðunni **Öll viðhaldsskemu**. Eftirfarandi mynd sýnir dæmi um gluggann **Tímasetja viðhaldsáætlanir**.

![Mynd 1](media/09-preventive-maintenance.png)

- Í glugganum **Skipuleggja viðhaldsáætlanir** er hægt að setja upp runuvinnslur á flýtiflipanum **Keyra í bakgrunni** til að mynda sjálfkrafa dagatalsfærslur með reglulegu millibili.  
- Þegar þú áætlar fyrirbyggjandi viðhald verða viðhaldsskemalínur með áætluðum upphafsdegi og tíma sem er á undan dagsetningu og tíma kerfisins ekki búin til.  

Myndin hér að neðan gefur myndræna mynd af tímabyggðum útreikningi á viðhaldsáætlun.  

![Mynd 2](media/10-preventive-maintenance.jpg)

Varðandi teljarabyggðar viðhaldsáætlanir: Á myndunum hér að neðan eru sýndar tvær mismunandi teljaraskráningarlotur. Þær eru byggðar á viðhaldsáætlun sem sett var upp fyrir eignina „V0001“ og búist við að eignin (bíll) gangi u.þ.b. 2.000 km í hverjum mánuði.

Í fyrra dæminu næst ekki 2.000 km sem búist er við í hverjum mánuði. Samkvæmt teljarabyggðu viðhaldsáætluninni er þröskuldurinn 2.000 km, sem þýðir að þegar þú keyrir tímasetningu viðhaldsáætlunar ætti að búa til viðhaldsskemalínu í hvert skipti sem 2.000 kílómetra þröskuldinum er náð. Í dæmi 1 eru 4 skráningarlínur en 2.000 kílómetra þröskuldinum er aðeins náð einu sinni. Þetta þýðir að þegar þú keyrir áætlun um viðhaldsáætlun fyrir þessa eign, til dæmis í 3 mánaða tímabil, verður aðeins ein viðhaldsskemalína búin til.

Í næstu mynd eru 2.000 km eða meira skráðir í hverjum mánuði. Þess vegna yrðu búnar til þrjár viðhaldslínur ef þú áætlar viðhaldsáætlanir fyrir þessa eign í 3 mánuði. 

Dæmin sem lýst er hér sýna að allar gagnaskráningar sem gerðar hafa verið á eign sýna þróun sem lýsir sliti á eigninni. Sú þróun er notuð sem útreikningsgrundvöllur þegar áætlun um viðhaldsáætlun er gerð.

![Mynd 3](media/11-preventive-maintenance.png)

![Mynd 4](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
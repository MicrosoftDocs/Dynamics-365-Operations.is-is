---
title: Kostnaður viðhaldsáætlunar
description: Þetta efni skýrir kostnað viðhaldsskema í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b30fa3c142057b43202a8f5a323c0b425865e971
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571324"
---
# <a name="maintenance-schedule-cost"></a>Kostnaður viðhaldsáætlunar

[!include [banner](../../includes/banner.md)]

 

Í eignastjórnun geturðu reiknað út kostnaðaráætlun á viðhaldsskemalínum. Þetta er gagnlegt ef þú vilt fá yfirsýn yfir væntanlegan kostnað, til dæmis kostnað vegna fyrirhugaðra forvirkra viðhaldsverka næsta árið. Útreikningarnir eru byggðir á núverandi viðhaldsskemalínum af gerðinni „Viðhaldsáætlanir“ og „Viðhaldslotur“ og „Viðhaldsbeiðnir“.

1. Smelltu á **Eignastýring** > **Fyrirspurnir** > **Eignir** > **Kostnaður við viðhaldsskema**.

2. Í valmyndinni **Kostnaður við viðhaldsskema** er hægt að velja **Fjárhagsvídd stillt** ef þú vilt sjá kostnað flokkaðan í fjárhagsvíddir.

>[!NOTE]
>Fjárhagsvíddarsett eru sett upp í **Fjárhag** > **Bókhaldslykli** > **Víddir** > **Fjárhagsvíddarsett**.

3. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að viðhaldsskemalínur séu varðandi virkar staðsetningar. Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur á öllum virkum staðsetningarstigum sem þær tengjast.

4. Ef þú vilt gera útreikning á tilteknum eignum skaltu smella á **Sía** á flýtiflipanum **Færslur til að hafa með** og velja viðeigandi eignir. Ef þess er krafist geturðu einnig tilgreint dagsetningu **Væntanlegt upphaf** fyrir kostnaðarútreikning eða valið aðra **Stöðu** fyrir kostnaðarútreikninginn

5. Smellið á **Í lagi** til að hefja kostnaðarútreikning.

6. Á flipanum **Kostnaður viðhaldsskema** > í aðgerðarúðuhópunum **Flokka eftir...** skaltu smella á viðeigandi hnappa til að sýna umbeðið upplýsingastil kostnaðarútreiknings. Valdir hóphnappar aðgerðarrúðu eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

7. Smelltu á hnappinn **Reikna kostnað** ef þú vilt gera nýjan kostnaðarútreikning.

Myndin hér að neðan sýnir niðurstöður útreiknings á kostnaði viðhaldsskema.

![Mynd 1](media/17-preventive-maintenance.png)


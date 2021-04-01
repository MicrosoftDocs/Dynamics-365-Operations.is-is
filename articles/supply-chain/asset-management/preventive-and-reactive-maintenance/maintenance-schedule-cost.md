---
title: Kostnaður viðhaldsáætlunar
description: Þetta efni skýrir kostnað viðhaldsskema í eignastýringu.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9686efb228e123671ba93a37480d2daac8d038a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252967"
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

6. Á flipanum **Kostnaður viðhaldsáætlunar** > í **Flokka eftir...** aðgerðarsvæðishópum skal smella á viðeigandi hnappa til að sýna nauðsynlegt upplýsingastig kostnaðarútreikningsins. Hnappar valinna aðgerðasvæðahóps eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

7. Smelltu á hnappinn **Reikna kostnað** ef þú vilt gera nýjan kostnaðarútreikning.

Myndin hér að neðan sýnir niðurstöður útreiknings á kostnaði viðhaldsskema.

![Mynd 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
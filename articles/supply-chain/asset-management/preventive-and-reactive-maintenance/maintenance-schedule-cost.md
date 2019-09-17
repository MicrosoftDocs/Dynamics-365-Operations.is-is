---
title: Kostnaður viðhaldsáætlunar
description: Þetta efni skýrir kostnað viðhaldsskema í eignastýringu.
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
ms.openlocfilehash: 71b958839a914d90a86a0dcd16a09285ca6dcfa4
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875704"
---
# <a name="maintenance-schedule-cost"></a>Kostnaður viðhaldsáætlunar


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Í eignastjórnun geturðu reiknað út kostnaðaráætlun á viðhaldsskemalínum. Þetta er gagnlegt ef þú vilt fá yfirsýn yfir væntanlegan kostnað, til dæmis kostnað vegna fyrirhugaðra forvirkra viðhaldsverka næsta árið. Útreikningarnir eru byggðir á núverandi viðhaldsskemalínum af gerðinni „Viðhaldsáætlanir“ og „Viðhaldslotur“ og „Viðhaldsbeiðnir“.

1. Smelltu á **Eignastýring** > **Fyrirspurnir** > **Eignir** > **Kostnaður við viðhaldsskema**.

2. Í valmyndinni **Kostnaður við viðhaldsskema** er hægt að velja **Fjárhagsvídd stillt** ef þú vilt sjá kostnað flokkaðan í fjárhagsvíddir.

>[!NOTE]
>Fjárhagsvíddarsett eru sett upp í **Fjárhag** > **Bókhaldslykli** > **Víddir** > **Fjárhagsvíddarsett**.

3. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að viðhaldsskemalínur séu varðandi virkar staðsetningar. Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur á öllum virkum staðsetningarstigum sem þær tengjast.

4. Ef þú vilt gera útreikning á tilteknum eignum skaltu smella á **Sía** á flýtiflipanum **Færslur til að hafa með** og velja viðeigandi eignir. Ef þess er krafist geturðu einnig tilgreint dagsetningu **Væntanlegt upphaf** fyrir kostnaðarútreikning eða valið aðra **Stöðu** fyrir kostnaðarútreikninginn

5. Smellið á **Í lagi** til að hefja kostnaðarútreikning.

6. Á flipanum **Kostnaður viðhaldsskema** > í aðgerðarúðuhópunum **Flokka eftir...** skaltu smella á viðeigandi hnappa til að sýna umbeðið upplýsingastil kostnaðarútreiknings. Valdir aðgerðarrúðuhópshnappar eru auðkenndir í bláum lit. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

7. Smelltu á hnappinn **Reikna kostnað** ef þú vilt gera nýjan kostnaðarútreikning.


![Mynd 1](media/17-preventive-maintenance.png)

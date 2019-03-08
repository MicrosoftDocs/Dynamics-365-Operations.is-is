---
title: Úthluta vinnuliðir í verkflæði
description: Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "346250"
---
# <a name="delegate-work-items-in-a-workflow"></a>Úthluta vinnuliðir í verkflæði

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda. Þetta ferli hjálpar að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi.



Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="set-up-automatic-delegation"></a>Setja upp sjálfvirka úthlutun
1. Fara í Algengt > Uppsetning > Notandavalkostir.
2. Smellt er á flipann Verkflæði.
    * Gangið úr skugga um að hlutinn Úthlutun sé stækkaður.    Til að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi, verður að stofna úthlutunarreglur sem tilgreina hvenær ákveðnar gerðir vinnuliða er úthluta. Fylgið þessum skrefum til að stofna úthlutunarreglu.  
3. Smelltu á Bæta við.
4. Í svæði Umfang, velja valkostur.
    * Allt - Úthluta öllum vinnuliðum sem úthlutað á þig.    Eining - Úthluta aðeins vinnuliðum sem tengjast tilgreindri gerð verkflæði. Ef þessi valkostur valinn, verður að velja gerð verkflæðis í svæði Heiti.    Verkflæði - Úthluta aðeins vinnuliðum sem tengjast tilgreindu verkflæði. Ef þessi valkostur valinn, verður að velja verkflæði í svæði Heiti.  
5. Í svæði Úthluta, velja notandi sem á að úthluta vinnuliðir á.
    * Notið svæði Upphafsdagsetning/-tími og Lokadagsetning/-tími til að tilgreina hvenær á sjálfkrafa að úthluta vinnuliður.  
6. Í svæði Upphafsdagsetning/-tími, slá inn dagsetning og tími.
7. Í svæði Lokadagsetning/-tími, slá inn dagsetning og tími.
8. Veljið gátreitinn Virkt til að gera úthlutunarregluna virka.
    * Ef Eining er valið sem umfang, verður að velja einingu í svæði Heiti.    Ef Verkflæði er valið sem umfang, verður að velja sérstakt verkflæði sem á að úthluta í svæði Heiti.  
9. Í svæði Athugasemd skal færa inn athugasemd og útskýra hvers vegna vinnuliðir eru úthlutað.


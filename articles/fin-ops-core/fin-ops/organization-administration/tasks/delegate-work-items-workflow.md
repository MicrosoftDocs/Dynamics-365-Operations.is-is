---
title: Úthluta vinnuliðir í verkflæði
description: Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747370"
---
# <a name="delegate-work-items-in-a-workflow"></a>Úthluta vinnuliðum í verkflæði

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Úthluta vinnulið handvirkt

Til að úthluta einstökum vinnulið skal velja valkostinn **Úthluta** í valmyndinni **Verkflæði** og síðan færa inn notandann sem úthluta á til ásamt athugasemd. Þetta mun endurúthluta vinnuliðnum á þann notanda svo hann geti lokið vinnunni.

## <a name="manually-delegate-multiple-work-items"></a>Úthluta mörgum vinnuliðum handvirkt

Hægt er að úthluta mörgum vinnuliðum saman á síðunni **Vinnuliðum sem mér er úthlutað**. Eftirfarandi verkflæðisgerðir er hægt að fjöldaúthluta: innkaupasamningur, samþykktarverkflæði, verkflæði innkaupapöntunar, yfirferð innkaupabeiðni og verkflæði lánardrottnareiknings. Slökkt er á eiginleikanum **Úthluta mörgum vinnuliðum** að sjálfgefnu og hægt er að virkja hann í **Vinnusvæði > Eiginleikastjórnun**. Hafið samband við kerfisstjóra til að fá aðstoð við að kveikja á eiginleikanum.
1.  Farið á **Algengt > Algengt > Vinnuliðir > Vinnuliðir sem úthlutað er á mig**.
2.  Veljið vinnuliði sem verður úthlutað.
3.  Smellið á valmyndina **Úthluta vinnuliðum**.
4.  Í reitnum **Notandi** skal velja notandann sem á að úthluta vinnuliði á.
5.  Í reitnum **Athugasemd** skal færa inn athugasemd og útskýra hvers vegna vinnuliðum er úthlutað.
6.  Smellið á hnappinn **Úthluta vinnuliðum** til að ljúka úthlutun vinnuliðar.

## <a name="automatically-delegate-work-items"></a>Úthluta vinnuliðum sjálfvirkt

Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnuliðum yfir eitthvert tímabil getur þú úthlutað nýjum vinnuliðum sjálfvirkt á aðra notendur með því að nota síðuna **Valkostir notanda**.

### <a name="set-up-automatic-delegation"></a>Setja upp sjálfvirka úthlutun
1. Farðu í **Algengt > Uppsetning > Notandavalkostir**.
2. Smelltu á flipann **Verkflæði**. Gakktu úr skugga um að hlutinn Úthlutun sé stækkaður. Til að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi, verður að stofna úthlutunarreglur sem tilgreina hvenær ákveðnar gerðir vinnuliða er úthluta. Fylgið þessum skrefum til að stofna úthlutunarreglu.  
3. Smelltu á **Bæta við**.
4. Í svæðinu **Umfang** skal velja valkost.
    - Allt - Úthluta öllum vinnuliðum sem úthlutað á þig.
    - Eining - Úthluta aðeins vinnuliðum sem tengjast tilgreindri gerð verkflæði. Ef þessi valkostur valinn, verður að velja gerð verkflæðis í svæðinu **Heiti**.
    - Verkflæði - Úthluta aðeins vinnuliðum sem tengjast tilgreindu verkflæði. Ef þessi valkostur valinn, verður að velja verkflæði í svæðinu **Heiti**.  
5. Í svæðið **Heiti**:
    - Fyrir **Eining** umfangið skal velja markeininguna.
    - Fyrir **Verkflæði** eininguna skal velja markverkflæðið.
6. Í reitnum **Úthluta** skal velja notanda sem úthluta skal vinnuliðum á. Notið svæðin **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími** til að tilgreina hvenær á sjálfkrafa að úthluta vinnuliður.  
7. Í reitnum **Upphafsdagsetning/-tími** skal slá inn dagsetningu og tíma.
8. Í reitnum **Lokadagsetning/-tími** skal slá inn dagsetningu og tíma.
9. Veljið gátreitinn **Virkjað** til að gera úthlutunarregluna virka. 
10. Í reitnum **Athugasemd** skal færa inn athugasemd og útskýra hvers vegna vinnuliðum er úthlutað.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
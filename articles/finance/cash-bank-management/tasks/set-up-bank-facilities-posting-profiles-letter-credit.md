---
title: Setja upp starfsstöðvar banka og bókunarreglur fyrir bankaábyrgð
description: Þetta ferli fer í gegnum stofnun Bankaaðstöðu og bókunarreglu sem þarf til að vinna kreditbréf.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e72847b9046968c87d9602e141bae6c603c1c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976329"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Setja upp starfsstöðvar banka og bókunarreglur fyrir bankaábyrgð

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum stofnun Bankaaðstöðu og bókunarreglu sem þarf til að vinna kreditbréf. 

Þetta verkefni notar sýnifyrirtækið ‚USMF‘.






## <a name="general-ledger-parameter"></a>Fjárhagsfæribreyta
1. Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.
2. Útvíkka hlutann Bankaskjal.
3. Veldu valkostinn Virkja innflutning kreditbréfs.
4. Veldu valkostinn Virkja útflutning kreditbréfs.
5. Smellið á „Vista“.
6. Lokið síðunni.

## <a name="create-bank-facility"></a>Stofna Bankaaðstöðu
1. Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bankaaðstöður.
2. Smellið á „Nýtt“.
3. Í reitnum Aðstöðuflokkur færirðu inn heiti á bankaaðstöðu.
4. Í svæðinu Lýsing er færð inn lýsing bankaaðstöðuflokks.
5. Smellið á „Vista“.
6. Smellið á flipann Aðstöðugerð.
7. Smellið á „Nýtt“.
8. Færið inn einkvæman kóða í reitnum Aðstaða.
9. Sláið inn gildi í reitnum „Lýsing“.
10. Í reitnum Aðstöðuflokkur skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
12. Í listanum skal smella á tengilinn í valinni línu.
13. Í svæðinu Eðli aðstöðu velurðu eðli bankaaðstöðunnar.
14. Smellið á „Vista“.
15. Lokið síðunni.

## <a name="bank-posting-profile"></a>Bókunarregla banka
1. Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bókunarregla bankaskjala.
2. Smellið á „Nýtt“.
3. Í reitnum Númer reiknings/flokks smellirðu á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Veldu aðallykil til jöfnunar.
    * Þessi reikningur er notaður við útreikning á sjóðsstreymisspá.  
7. Í reitnum Gjaldalykill velurðu lykil fyrir kostnaðarfærslur.
8. Í reitnum Framlegðarlykill velurðu lykil fyrir framlegðarfærslur.
    * Þessi lykill er tekjufærður þegar opnunarframlegð er bókuð og kreditfærð þegar greiðslan er bókuð.  
9. Smellið á „Vista“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
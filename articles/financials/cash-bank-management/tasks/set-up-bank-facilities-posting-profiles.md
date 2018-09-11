--- 
title: "Setja upp starfsstöðvar banka og bókunarreglur fyrir ábyrgðarbréf"
description: "Þetta verk stofnar bankaaðstöðu og bókunarreglu sem þarf til að vinna ábyrgðarbréf."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 022b5d411b8240390c543ba726fe0d6838752944
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Setja upp starfsstöðvar banka og bókunarreglur fyrir ábyrgðarbréf

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta verk stofnar bankaaðstöðu og bókunarreglu sem þarf til að vinna ábyrgðarbréf.



Þetta verkefni notar USMF-sýnifyrirtækið. 




## <a name="general-ledger-parameter"></a>Fjárhagsfæribreyta
1. Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.
2. Útvíkka hlutann Bankaskjal.
3. Veldu valkostinn Virkja ábyrgðarbréf.
4. Í reitnum Færslubók skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smellt er á flipann Númeraraðir.
    * Skilgreina númeraraðarkóða fyrir númer ábyrgðarbréfs og færslutilvísanir ábyrgðarbréfs  
8. Smellið á „Vista“.
9. Lokið síðunni.

## <a name="create-bank-facility"></a>Stofna Bankaaðstöðu
1. Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bankaaðstöður.
2. Smellið á „Nýtt“.
3. Í svæðið Aðstöðuflokkur skal færa inn heiti bankaaðstöðuflokks fyrir ábyrgðarbréf færslu.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smellið á „Vista“.
6. Smellið á flipann Aðstöðugerð.
7. Smellið á „Nýtt“.
8. Í svæðið Aðstöðugerð skal slá inn heiti gerðar bankaaðstöðu sem tengist bankaaðstöðusamningnum.
9. Í reitinn Lýsing skal slá inn gildi.
10. Í reitnum Aðstöðuflokkur skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
12. Í listanum skal smella á tengilinn í valinni línu.
13. Í reitnum Eðli aðstöðu skal velja valkost.
14. Smellið á „Vista“.
15. Lokið síðunni.

## <a name="bank-posting-profile"></a>Bókunarregla banka
1. Fara í Reiðufjár- og bankastjórnun > Uppsetning >Bókunarregla bankaskjala.
2. Smellið á „Nýtt“.
3. Í reitnum Númer reiknings/flokks smellirðu á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Í reitnum Gera upp lykil velurðu lykil fyrir uppgjör.
7. Í reitnum Gjaldalykill velurðu lykil fyrir kostnaðarfærslur.
8. Í reitnum Framlegðarlykill velurðu lykil fyrir framlegðarfærslu.
9. Í reitnum Slitalykill velurðu lykil fyrir slitafærslu. 
10. Smelltu á Vista.
11. Lokið síðunni.



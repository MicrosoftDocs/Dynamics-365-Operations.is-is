---
title: Setja upp starfsstöðvar banka og bókunarreglur fyrir bankaábyrgð
description: Þetta ferli fer í gegnum stofnun Bankaaðstöðu og bókunarreglu sem þarf til að vinna kreditbréf.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779463"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Setja upp starfsstöðvar banka og bókunarreglur fyrir bankaábyrgð

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum stofnun Bankaaðstöðu og bókunarreglu sem þarf til að vinna kreditbréf. 

Þetta verkefni notar sýnifyrirtækið ‚USMF‘.


## <a name="general-ledger-parameter"></a>Fjárhagsfæribreyta
1. Fara til **Reiðufé og bankastjórnun > Uppsetning > Færibreytur reiðufjár og bankastjórnunar**.
2. Stækkaðu **Bankaskjal** kafla.
3. Veldu **Virkja innflutningsbréf** valmöguleika.
4. Veldu **Virkja útflutningsbréf** valmöguleika.
5. Smelltu á **Vista**.
6. Lokið síðunni.

## <a name="create-bank-facility"></a>Stofna Bankaaðstöðu
1. Fara til **Reiðufé og bankastjórnun > Uppsetning > Bankaaðstaða**.
2. Smellt er á **Nýtt**.
3. Í **Aðstaðahópur** reit, sláðu inn heiti bankaaðstöðuhópsins.
4. Í **Lýsing** reit, sláðu inn lýsingu bankafyrirgreiðsluhóps.
5. Smelltu á **Vista**.
6. Smelltu á **Gerðir aðstöðu** flipa.
7. Smellt er á **Nýtt**.
8. Í **Gerð aðstöðu** reit, sláðu inn einstakan kóða.
9. Í reitinn **Lýsing** skal slá inn gildi.
10. Í **Aðstaðahópur** reit, smelltu á fellilistann til að opna leitina.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
12. Í listanum skal smella á tengilinn í valinni línu.
13. Í **Aðstaða náttúra** reit, veldu eðli bankafyrirgreiðslu.
14. Smelltu á **Vista**.
15. Lokið síðunni.

## <a name="bank-posting-profile"></a>Bókunarregla banka
1. Fara til **Reiðufé og bankastjórnun > Uppsetning > Bókunarsnið bankaskjala**.
2. Smellt er á **Nýtt**.
3. Í **Reikningur/hópnúmer** reit, smelltu á fellilistann til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Veldu aðallykil til jöfnunar.
    * Þessi reikningur er notaður við útreikning á sjóðsstreymisspá.  
7. Í **Gjaldreikningur** reit, veldu reikninginn fyrir kostnaðarfærslur.
8. Í **Framlegðarreikningur** reit, veldu reikninginn fyrir framlegðarfærslur.
    * Þessi lykill er tekjufærður þegar opnunarframlegð er bókuð og kreditfærð þegar greiðslan er bókuð.  
9. Smelltu á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

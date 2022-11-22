---
title: Setja upp starfsstöðvar banka og bókunarreglur fyrir ábyrgðarbréf
description: Þetta verk stofnar bankaaðstöðu og bókunarreglu sem þarf til að vinna ábyrgðarbréf.
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
ms.openlocfilehash: 1bfdef0cd535f47bb1df9fb7494043d3dd519c5b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779881"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Setja upp starfsstöðvar banka og bókunarreglur fyrir ábyrgðarbréf

[!include [banner](../../includes/banner.md)]

Þetta verk stofnar bankaaðstöðu og bókunarreglu sem þarf til að vinna ábyrgðarbréf.



Þetta verkefni notar USMF-sýnifyrirtækið. 




## <a name="general-ledger-parameter"></a>Fjárhagsfæribreyta
1. Fara til **Reiðufé og bankastjórnun > Uppsetning > Færibreytur reiðufjár og bankastjórnunar**.
2. Stækkaðu **Bankaskjal** kafla.
3. Veldu **Virkja ábyrgðarbréf** valmöguleika.
4. Í **Færsludagbók** reit, smelltu á fellilistann til að opna leitina.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smelltu á **Númeraraðir** flipa.
    * Skilgreina númeraraðarkóða fyrir númer ábyrgðarbréfs og færslutilvísanir ábyrgðarbréfs  
8. Smelltu á **Vista**.
9. Lokið síðunni.

## <a name="create-bank-facility"></a>Stofna Bankaaðstöðu
1. Fara til **Reiðufé og bankastjórnun > Uppsetning > Bankaaðstaða**.
2. Smellt er á **Nýtt**.
3. Í **Aðstaðahópur** reit skal slá inn heiti bankaaðstöðuhóps fyrir ábyrgðarbréfið.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Smelltu á **Vista**.
6. Smelltu á **Gerðir aðstöðu** flipa.
7. Smellt er á **Nýtt**.
8. Í **Gerð aðstöðu** reit skal slá inn heiti tegundar bankafyrirgreiðslu sem tengist bankafyrirgreiðslusamningnum.
9. Í reitinn **Lýsing** skal slá inn gildi.
10. Í **Aðstaðahópur** reit, smelltu á fellilistann til að opna leitina.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
12. Í listanum skal smella á tengilinn í valinni línu.
13. Í reitnum **Aðstaða eðli, veldu valkost.
14. Smelltu á **Vista**.
15. Lokið síðunni.

## <a name="bank-posting-profile"></a>Bókunarregla banka
1. Fara til **Reiðufé og bankastjórnun > Uppsetning > Bókunarsnið bankaskjala**.
2. Smellt er á **Nýtt**.
3. Í **Reikningur/hópnúmer** reit, smelltu á fellilistann til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Í **Gera upp reikning** reit, veldu aðalreikning fyrir uppgjör.
7. Í **Gjaldreikningur** reit, veldu reikninginn fyrir kostnaðarfærslur.
8. Í **Framlegðarreikningur** reit, veldu reikninginn fyrir framlegðarfærsluna.
9. Í **Skuldareikningur** reit, veldu slitareikning fyrir ábyrgðarbréfsviðskiptin. 
10. Smelltu á **Vista**.
11. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

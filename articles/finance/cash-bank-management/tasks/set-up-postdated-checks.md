---
title: Setja upp fyrirframdagsettar ávísanir
description: Í þessu efnisatriði er útskýrt hvernig á að tilgreina hvort eigi að bóka bókarfærslur fyrir fyrirframdagsettar ávísanir og hvaða bókunarbækur sem nota á fyrir færslur og lánardrottnagreiðslur.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141109"
---
# <a name="set-up-postdated-checks"></a>Setja upp fyrirframdagsettar ávísanir

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að tilgreina hvort eigi að bóka bókarfærslur fyrir fyrirframdagsettar ávísanir og hvaða bókunarbækur sem nota á fyrir færslur og lánardrottnagreiðslur. Einnig er hægt að tilgreina millireikninga fyrir útgefnar ávísanir, mótteknar ávísanir og staðgreiðsluskatt. Fyrirframdagsettar ávísanir sem eru gefnar út til að gera og móttaka greiðslur í framtíðinni. Hægt er að tilgreina hvort ávísunin verði að koma fram í bókhaldsbókum fyrir gjalddaga.



Hlutverk þessa ferlis er fjárreiðustjóri. Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="set-up-postdated-checks"></a>Setja upp fyrirframdagsettar ávísanir
1. Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.
2. Smellið á flipann Fyrirframdagsettar ávísanir.
3. Veldu eða hreinsaðu gátreitinn Virkja fyrirframdagsettar ávísanir.
4. Velja eða hreinsa gátreitinn Bóka bókarfærslur fyrir fyrirframdagsettar ávísanir.
5. Í reitnum Millireikningur fyrir útgefnar ávísanir skal tilgreina þau gildi sem óskað er eftir.
6. Tilgreinið gildin sem óskað er eftir í reitinn Millireikningur fyrir mótteknar ávísanir.
7. Í reitinn Almenn færslubók fyrir jöfnun færslna skal slá inn gildi.
8. Í reitinn Millifæra fyrirframdagsettar ávísanir á þessa færslubók lánardrottins skal slá inn gildi.
9. Í reitnum Millireikningur staðgreiðsluskatts skal tilgreina þau gildi sem óskað er eftir.
10. Smellið á „Vista“.
11. Lokið síðunni.
12. Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.
13. Smellið á „Nýtt“.
14. Færa inn gildi í svæðinu greiðsluaðferð.
15. Velja skal bókunarkostinn Millireikning fyrirframdagsettrar ávísunar til að tilgreina að upphæð ávísunarinnar er bókuð á millireikning.
16. Veljið 'Banki' í svæðinu gerð lykils.
    * Mótlykill greiðslumáta verður banki.  
17. Í reitnum Greiðslulykill skal tilgreina gildi sem óskað er eftir.
    * Veldu reikninginn sem er notaður til að draga reikningsupphæðina frá.  
18. Smelltu á Vista.
19. Lokið síðunni.


---
title: Setja upp fyrirframdagsettar ávísanir
description: Í þessu efnisatriði er útskýrt hvernig á að tilgreina hvort eigi að bóka bókarfærslur fyrir fyrirframdagsettar ávísanir og hvaða bókunarbækur sem nota á fyrir færslur og lánardrottnagreiðslur.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d73a382f1786a73a5af917b28d00384ecc36aa8
ms.sourcegitcommit: f6050b444e636ba662c00d0443c94a99f8ea0b0d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/28/2021
ms.locfileid: "6309767"
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
> [!NOTE]
> Til að geta birt fyrirframgreidda ávísun á bankareikning þegar lotudagurinn er hærri en eða jafn og gjalddaginn verður þú að virkja eiginleikann **Staðfesting gjalddaga fyrir bókun greiðslubókar með fyrirframdagsettum ávísunum á bankareikning**. Þessi valkostur leyfir þér að bóka greiðslubækur fyrir lánardrottna og viðskiptavini með fyrirframdagsettum ávísunum þegar setudagsetning kemur á eftir eða á sömu dagsetningu og gjalddagi.
> 
> Þegar **Greiðslumáti** er stilltur (**Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir**), skal ekki fylla út **Millilykill**. Í þessu tilviki er mótlykillinn fylltur út með bankareikningnum sem er settur upp í **Greiðslumáti**.
>  
> Þegar eiginleikinn er virkur og lotudagsetningin er lægri en gjalddagi birtast eftirfarandi villuskilaboð þegar greiðslubók er bókuð „Gjalddagi verður að vera á undan eða með sömu dagsetningu og setudagsetningin ef gerð mótlykils er banki“. Ef eiginleikinn er ekki virkur er hægt að birta greiðslubók með fyriframdagsettri ávísun þegar lotudagurinn er lægri en gjalddaginn.
> Þessi eiginleiki er tiltækur í útgáfu 10.0.21 og nýrri.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

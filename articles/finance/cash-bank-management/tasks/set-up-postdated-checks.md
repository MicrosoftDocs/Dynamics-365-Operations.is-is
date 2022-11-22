---
title: Setja upp fyrirframdagsettar ávísanir
description: Þessi grein útskýrir hvernig á að tilgreina hvort færslubókarfærslur eigi að bóka fyrir dagsettar ávísanir og hvaða bókunarfærslubækur eigi að nota til að hreinsa færslur og lánardrottnagreiðslur.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7172dd56113de23d841fe59ed9785471e90ed1f
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779610"
---
# <a name="set-up-postdated-checks"></a>Setja upp fyrirframdagsettar ávísanir

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að tilgreina hvort færslubókarfærslur eigi að bóka fyrir dagsettar ávísanir og hvaða bókunarfærslubækur eigi að nota til að hreinsa færslur og lánardrottnagreiðslur. Einnig er hægt að tilgreina millireikninga fyrir útgefnar ávísanir, mótteknar ávísanir og staðgreiðsluskatt. Fyrirframdagsettar ávísanir sem eru gefnar út til að gera og móttaka greiðslur í framtíðinni. Hægt er að tilgreina hvort ávísunin verði að koma fram í bókhaldsbókum fyrir gjalddaga.



Hlutverk þessa ferlis er fjárreiðustjóri. Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="set-up-postdated-checks"></a>Setja upp fyrirframdagsettar ávísanir
1. Fara til **Reiðufé og bankastjórnun > Uppsetning > Færibreytur reiðufjár og bankastjórnunar**.
2. Smelltu á **Uppfærðar ávísanir** flipa.
3. Veldu eða hreinsaðu **Virkjaðu dagsettar athuganir** gátreit.
4. Veldu eða hreinsaðu **Bókaðu dagbókarfærslur fyrir dagsettar ávísanir** gátreit.
5. Í **Jöfnunarreikningur fyrir útgefna ávísanir** reit, tilgreindu þau gildi sem þú vilt.
6. Í **Afgreiðsla reiknings fyrir mótteknar ávísanir** reit, tilgreindu þau gildi sem þú vilt.
7. Í **Almenn dagbók til að hreinsa færslur** reit, sláðu inn gildi.
8. Í **Flytja dagsettar ávísanir í þessa greiðslubók lánardrottins** reit, sláðu inn gildi.
9. Í **Staðgreiðslureikningur** reit, tilgreindu þau gildi sem þú vilt.
10. Smelltu á **Vista**.
11. Lokið síðunni.
12. Fara til **Viðskiptaskuldir > Greiðsluuppsetning > Greiðslumátar**.
13. Smellt er á **Nýtt**.
14. Í reitinn **Greiðsluháttur** skal slá inn gildi.
15. Veldu **Uppfærsla á tékkaafgreiðslu** valkostur til að gefa til kynna að tékkupphæðin sé færð inn á jöfnunarreikning.
16. Í **Tegund reiknings** reit, veldu **Banki**.
    * Mótlykill greiðslumáta verður banki.  
17. Í **Greiðslureikningur** reit, tilgreindu þau gildi sem þú vilt.
    * Veldu reikninginn sem er notaður til að draga reikningsupphæðina frá.  
18. Smelltu á **Vista**.
19. Lokið síðunni.
> [!NOTE]
> Til að geta birt fyrirframgreidda ávísun á bankareikning þegar lotudagurinn er hærri en eða jafn og gjalddaginn verður þú að virkja eiginleikann **Staðfesting gjalddaga fyrir bókun greiðslubókar með fyrirframdagsettum ávísunum á bankareikning**. Þessi valkostur leyfir þér að bóka greiðslubækur fyrir lánardrottna og viðskiptavini með fyrirframdagsettum ávísunum þegar setudagsetning kemur á eftir eða á sömu dagsetningu og gjalddagi.
> 
> Þegar stillt er á **Greiðslumáti** (**Viðskiptaskuldir > Greiðsluuppsetning > Greiðslumátar**), ekki fylla út **Brúarreikningur**. Í þessu tilviki er mótlykillinn fylltur út með bankareikningnum sem er settur upp í **Greiðslumáti**.
>  
> Þegar eiginleikinn er virkur og lotudagsetningin er minni en gjalddagi, birtast eftirfarandi villuboð þegar greiðslubók er bókuð, **Gjalddagi verður að vera minni eða jöfn fundardagsetningu ef tegund mótreiknings er Banki**. Ef eiginleikinn er ekki virkur er hægt að birta greiðslubók með fyriframdagsettri ávísun þegar lotudagurinn er lægri en gjalddaginn.
> Þessi eiginleiki er tiltækur í útgáfu 10.0.21 og nýrri.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

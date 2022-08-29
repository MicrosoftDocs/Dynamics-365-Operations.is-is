---
title: Setja upp greiðslutíðni
description: Microsoft Dynamics 365 Human Resources notar greiðslutíðni til að reikna árleg hlunnindi, ákvarða álagsupphæð sem starfsmaður greiðir hvert launatímabil og hversu oft veitendum er greitt.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0472e2203cc20fcf0904d22778092721b4cbce41
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323929"
---
# <a name="set-up-payment-frequencies"></a>Setja upp greiðslutíðni


Microsoft Dynamics 365 Human Resources notar greiðslutíðni til að reikna árleg hlunnindi, ákvarða álagsupphæð sem starfsmaður greiðir hvert launatímabil og hversu oft veitendum er greitt.

Greiðslutíðni fríðinda notar umbreytingarstuðla til að umbreyta fríðindagreiðslutímabilum milli mánaðarlegra, hálfsmánaðarlegra, tveggja vikna, vikulega og daglegra greiðslutíðna. Þetta gerir fyrirtækjum kleift að skilgreina innbyrðistengsl milli greiðslutíðni innan fríðindaáætlunar.

Reitirnir fyrir umbreytingarstuðla bera kennsl á umbreytingarstuðulinn frá greiðslutíðni yfir í venjuleg greiðslutímabil og leyfa kerfinu að gera útreikninga milli greiðslutíðni. Upphæð umreikningsstuðuls ákvarðar einnig upphæð tryggingariðgjalds sem starfsmaður á að greiða hverja launatíðni.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Greiðslutíðnir**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Greiðslutíðni** | Einkvæmt nafn greiðslutíðni. |
   | **Lýsing** | Lýsing á greiðslutíðninni. |
   | **Tímabil** | Viðeigandi tímabil sem passar best við greiðslutíðni bótaaðila og starfsmanns. Tímabilalistinn er samsettur af venjulegu greiðslutímabilum. |
   | **Fjöldi launatímabila** | Fjöldi launatímabila sem táknar hversu oft bætur veitendur eða starfsmenn eru greiddir. Þessi upphæð verður notuð til að reikna út árlegan kjarabót starfsmanns. |
   | **Árlegur umreiknistuðull** | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 1 ár) = 12 |
   | **Umreiknistuðull annað hvert ár** | Hálfsárs umbreytingarstuðull greiðslutíðni. Til dæmis er hálfsárs viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 2 á ári) = 6 |
   | **Umreiknistuðull á hverjum ársfjórðungi** | Fjórðungslegur umbreytingarstuðull greiðslutíðni. Til dæmis er fjórðungslegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 4 fjórðungar) = 3 |
   | **Mánaðarlegur umreiknistuðull** | Mánaðarlegur umbreytingarstuðull greiðslutíðni. Til dæmis er mánaðarlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 12 mánuðir) = 1 |
   | **Umreiknistuðull annan hvern mánuð** | Annars hvers mánaðar umbreytingarstuðull greiðslutíðni. Til dæmis er annars hvers mánaðar viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 24 (2x á mánuði)) = 0,5 | 
   | **Umreiknistuðull aðra hverja viku** | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 26 vikur) = 0.461538 |
   | **Vikulegur umreiknistuðull** | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 52 vikur) = 0.230769 |
   | **Daglegur umreiknistuðull** | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 365 dagar) = 0.032877 |
   | **Umreiknistuðull fyrir hverja klukkustund** | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 2080 stundir) = 0,005769

4. Veljið **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Setja upp greiðslutíðni
description: Microsoft Dynamics 365 Human Resources notar greiðslutíðni til að reikna árleg hlunnindi, ákvarða álagsupphæð sem starfsmaður greiðir hvert launatímabil og skilgreina tíðni greiðslna eru gerðar til veitenda.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b786485ab53dcdb3b7e5ff02562f674a7f8e6eae
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092592"
---
# <a name="set-up-payment-frequencies"></a>Setja upp greiðslutíðni

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources notar greiðslutíðni til að reikna árleg hlunnindi, ákvarða álagsupphæð sem starfsmaður greiðir hvert launatímabil og skilgreina tíðni greiðslna eru gerðar til veitenda.

Greiðslutíðni fríðinda notar umbreytingarstuðla til að umbreyta fríðindagreiðslutímabilum milli mánaðarlegra, hálfsmánaðarlegra, tveggja vikna, vikulega og daglegra greiðslutíðna. Þetta gerir fyrirtækjum kleift að skilgreina innbyrðistengsl milli greiðslutíðni innan fríðindaáætlunar.

Reitirnir fyrir umbreytingarstuðla bera kennsl á umbreytingarstuðulinn frá greiðslutíðni yfir í venjuleg greiðslutímabil og leyfa kerfinu að gera útreikninga milli greiðslutíðni. Umreikningsstuðul upphæðin er einnig notuð til að ákvarða álagsupphæð sem starfsmaður á að greiða hverja launatíðni.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Greiðslutíðnir**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | Greiðslutíðni | Einkvæmt nafn greiðslutíðni. |
   | Lýsing | Lýsing á greiðslutíðninni. |
   | Tímabil | Viðeigandi tímabil sem passar best við greiðslutíðni bótaaðila og starfsmanns. Tímabilalistinn er samsettur af venjulegu greiðslutímabilum. |
   | Fjöldi launatímabila | Fjöldi launatímabila sem táknar hversu oft bætur veitendur eða starfsmenn eru greiddir. Þessi upphæð verður notuð til að reikna út árlegan kjarabót starfsmanns. |
   | Árlegur umreiknistuðull | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 1 ár) = 12 |
   | Umreiknistuðull annað hvert ár | Hálfsárs umbreytingarstuðull greiðslutíðni. Til dæmis er hálfsárs viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 2 á ári) = 6 |
   | Umreiknistuðull á hverjum ársfjórðungi | Fjórðungslegur umbreytingarstuðull greiðslutíðni. Til dæmis er fjórðungslegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 4 fjórðungar) = 3 |
   | Mánaðarlegur umreiknistuðull | Mánaðarlegur umbreytingarstuðull greiðslutíðni. Til dæmis er mánaðarlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 12 mánuðir) = 1 |
   | Umreiknistuðull annan hvern mánuð | Annars hvers mánaðar umbreytingarstuðull greiðslutíðni. Til dæmis er annars hvers mánaðar viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 24 (2x á mánuði)) = .5 | 
   | Umreiknistuðull aðra hverja viku | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 26 vikur) = 0.461538 |
   | Vikulegur umreiknistuðull | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 52 vikur) = 0.230769 |
   | Daglegur umreiknistuðull | Árlegur umbreytingarstuðull greiðslutíðni. Til dæmis er árlegur viðskiptaþáttur fyrir mánaðarlega launatíðni: </br></br>(12 mánaðarlegar greiðslur / 365 dagar) = 0.032877 |

4. Veljið **Vista**. 

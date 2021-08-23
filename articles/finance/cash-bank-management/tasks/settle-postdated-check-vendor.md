---
title: Gera upp fyrirframdagsetta ávísun fyrir lánardrottin
description: Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b7755c3c3d092692dde6582a8d4ba74f00b10a95ba82a2782e3dad34d28e7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728056"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Gera upp fyrirframdagsetta ávísun fyrir lánardrottin

[!include [banner](../../includes/banner.md)]

Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum. 

Ljúka skal eftirfarandi aðgerðum áður en hann þessi er hafin.

1) Setja upp fyrirframdagsettar ávísanir

2) Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn



Hlutverk þessa ferlis er fjárreiðustjóri. Þessi aðferð notar sýnigögn USMF fyrirtækisins.

1. Fara í Viðskiptaskuldir > Greiðslur > Fyrirframdagsettar ávísanir lánardrottins.
2. Smellt er á Gera upp.
3. Smellt er á Gera upp jöfnunarfærslur.
    * Jafna lykil lánardrottins fyrir ávísunarfærsla.  
4. Lokið síðunni.
5. Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.
6. Í svæði Sýna, velja 'Allt'.
7. Veldu eða hreinsaðu gátreitinn Sýna aðeins notanda-stofnað.
8. Í listanum skal merkja valda línu.
9. Smellið á Línur.
10. Smellt er á Fylgiskjalið.
11. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
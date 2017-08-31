--- 
title: Endurflokka eignir
description: "Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: dcad2c2e225a07bf9e9eb7fe7bbec605f668f8f5
ms.contentlocale: is-is
ms.lasthandoff: 07/28/2017

---
# <a name="reclassify-fixed-assets"></a>Endurflokka eignir

[!include[task guide banner](../../includes/task-guide-banner.md)]

Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks. 

Þegar eign er endurflokkuð:

• Öll virðislíkön fyrirliggjandi eigna eru stofnuð fyrir nýju eignina. Allar upplýsingar sem voru settar upp fyrir upprunalegu eignina eru afritaðar í nýju eignina. Staða virðislíkana fyrir upprunalegu eignina er Lokað. 

• Nýju virðislíkön nýju eignarinnar innihalda dagsetningu endurflokkunarinnar í svæðinu Kaupdagsetning. Dagsetningin í svæði Dagsetning afskriftarkeyrslu er afrituð úr upprunalegu eignaupplýsingunum. Ef afskriftir eru þegar hafnar sýnir svæðið Dagsetningin þegar afskriftir voru síðast keyrðar dagsetningu endurflokkunarinnar. 

• Hætt er við fyrirliggjandi eignafærslur upprunalegu eignarinnar og þær myndaðar aftur fyrir nýju eignina.

1. Fara í Eignir > Reglubundin verkefni > Endurflokkun.
2. Í svæði Eignaflokkur, velja flokk til að endurflokka.
3. Í svæði Eignanúmer, velja eign sem endurflokka.
4. Í svæði  Nýr eignaflokkur, velja flokk til að flytja eign í.
    * Ef nýr eignaflokkur er festur við númeraröð er svæði Nýtt eignanúmer uppfærður með númer úr númeraröð nýtt eignaflokkur. Annars er svæði Nýtt eignanúmer uppfærður með númer úr númeraröð sem er sett upp á síðu Færibreytur eigna. Ef númeraröð er ekki sett upp á síðu Færibreytur eigna skal slá inn númer í svæði Nýtt eignanúmer.  
5. Í svæði Dagsetning endurflokkunar slá inn dagsetning.
6. Í reitinn fylgiskjalaruna skal slá inn eða velja gildi.
7. Smellið á „Í lagi“.



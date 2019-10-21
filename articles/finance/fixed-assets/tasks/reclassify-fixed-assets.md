---
title: Endurflokka eignir
description: Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47d8cf2ff1e275df0466a7fe327a3180c0399e49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186924"
---
# <a name="reclassify-fixed-assets"></a>Endurflokka eignir

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks. 

Þegar eign er endurflokkuð:

• Allar bækur fyrirliggjandi eigna eru stofnaðar fyrir nýju eignina. Allar upplýsingar sem voru settar upp fyrir upprunalegu eignina eru afritaðar í nýju eignina. Staða bókanna fyrir upprunalegu eignina er Lokað. 

• Nýju bækur nýju eignarinnar innihalda dagsetningu endurflokkunarinnar í svæðinu **Kaupdagsetning**. Dagsetningin í svæði **Dagsetning afskriftarkeyrslu** er afrituð úr upprunalegu eignaupplýsingunum. Ef afskriftir eru þegar hafnar sýnir svæðið **Dagsetningin þegar afskriftir voru síðast keyrðar** dagsetningu endurflokkunarinnar. 

• Hætt er við fyrirliggjandi eignafærslur upprunalegu eignarinnar og þær myndaðar aftur fyrir nýju eignina.

Fylgið þessum skrefum til að endurflokka eign:

1. Fara í **Eignir > Reglubundin verkefni > Endurflokkun.**
2. Í svæðinu **Eignaflokkur** skal velja flokk til að endurflokka.
3. Í svæði **Eignanúmer** skal velja eign sem endurflokka.
4. Í reitnum **Nýr eignaflokkur** skal velja flokk til að flytja eign í.
    * Ef nýr eignaflokkur er festur við númeraröð er svæði **Nýtt eignanúmer** uppfærður með númer úr númeraröð nýtt eignaflokkur. Annars er svæðið **Nýtt eignanúmer** uppfært með númeri úr númeraröð sem er sett upp á síðunni **Færibreytur eigna**. Ef númeraröð er ekki sett upp á síðunni **Færibreytur eigna** skal slá inn númerið í svæðinu **Nýtt eignanúmer**.  
5. Í svæði **Dagsetning endurflokkunar** skal slá inn dagsetning.
6. Í reitinn **fylgiskjalaruna** skal slá inn eða velja gildi.
7. Smellt er á **OK**.

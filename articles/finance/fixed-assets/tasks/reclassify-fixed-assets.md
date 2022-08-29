---
title: Endurflokka eignir
description: Þessi grein útskýrir ferlið við endurflokkun eigna. Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bd901b1709f0b006cecfbbf6d8c170b56f89d19
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284364"
---
# <a name="reclassify-fixed-assets"></a>Endurflokka eignir

[!include [banner](../../includes/banner.md)]

Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks. 

Þegar eign er endurflokkuð:

- Allar bækur fyrirliggjandi eigna eru stofnaðar fyrir nýju eignina. Allar upplýsingar sem voru settar upp fyrir upprunalegu eignina eru afritaðar í nýju eignina. Staða bókanna fyrir upprunalegu eignina er Lokað. 

- Nýju bækur nýju eignarinnar innihalda dagsetningu endurflokkunarinnar í reitnum **Kaupdagsetning**. Dagsetningin í svæði **Dagsetning afskriftarkeyrslu** er afrituð úr upprunalegu eignaupplýsingunum. Ef afskriftir eru þegar hafnar sýnir svæðið **Dagsetningin þegar afskriftir voru síðast keyrðar** dagsetningu endurflokkunarinnar. 

- Hætt er við fyrirliggjandi eignafærslur upprunalegu eignarinnar og þær myndaðar aftur fyrir nýju eignina.

- Þegar eign með færslu hefur verið endurflokkuð birtir kerfið skilaboð í **aðgerðamiðstöðinni** um að millifærslu hafi ekki verið lokið meðan á endurflokkunarferlinu stóð. Nauðsynlegt er að ljúka flutningsfærslu til að færa fyrirliggjandi endurflokkunarfærslu í viðeigandi fjárhagsvídd. 

   Meðan á endurflokkunarferlinu stendur keyrir kerfið eftirfarandi aðgerðir til að endurflokka eignastöðuna frá upprunalegu eigninni yfir á nýju eignina. 
   
   - Endurflokkunarferlið afritar gögnin úr upprunalegu eignabókinni í nýju eignabókina.

   - Í endurflokkunarfærslunni eru notaðar upplýsingar úr upprunalegu bókuðu kaupunum sem innihalda upplýsingar um fjárhagsvídd sem eru innifaldar í eignaflutningsfærslunni.  
   
   - Á sama tíma snýr endurflokkunarferlið við upphaflegu eignakaupunum og eignaflutningsfærslunni. 

Eftirfarandi mynd og aðferð gefur dæmi um endurflokkunarferlið. 

[![Mynd sem sýnir endurflokkunarferlið.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Fylgið þessum skrefum til að endurflokka eign:

1. Fara í **Eignir > Reglubundin verkefni > Endurflokkun.**
2. Í svæðinu **Eignaflokkur** skal velja flokk til að endurflokka.
3. Í svæði **Eignanúmer** skal velja eign sem endurflokka.
4. Í reitnum **Nýr eignaflokkur** skal velja flokk til að flytja eign í.
    * Ef nýr eignaflokkur er festur við númeraröð er svæði **Nýtt eignanúmer** uppfærður með númer úr númeraröð nýtt eignaflokkur. Annars er svæðið **Nýtt eignanúmer** uppfært með númeri úr númeraröð sem er sett upp á síðunni **Færibreytur eigna**. Ef númeraröð er ekki sett upp á síðunni **Færibreytur eigna** skal slá inn númerið í svæðinu **Nýtt eignanúmer**.  
5. Í svæði **Dagsetning endurflokkunar** skal slá inn dagsetning.
6. Í reitinn **fylgiskjalaruna** skal slá inn eða velja gildi.
7. Veljið **Í lagi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

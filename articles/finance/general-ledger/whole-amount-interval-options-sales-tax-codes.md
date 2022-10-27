---
title: Útreikningsaðferð heildarupphæðar og tímabils fyrir vsk-kóða
description: Þessi grein útskýrir hvernig valkostir fyrir svæðið Útreikningsaðferðir hafa áhrif á virðisaukaskattskóða og hvernig virðisaukaskattur er reiknaður fyrir tímabil og fullar upphæðir.
author: kailiang
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b81780e60825021ad7a700d85257ba0f5a2447a
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715242"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Útreikningsaðferð heildarupphæðar og tímabils fyrir vsk-kóða

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir valkostina fyrir **Reikniaðferð** reitinn um söluskattskóða og hvernig söluskattur er reiknaður fyrir millibili og heilar upphæðir.

Hægt er að setja upp vsk-kóða til að reikna út byggt á heildarupphæð eða tímabilsupphæð. Á síðunni **VSK-kóðar** skal nota reitinn **Útreikningsaðferð** á flýtiflipanum **Útreikningur** til að velja reikningsaðferðina fyrir VSK-kóða.
- Heildarupphæð – Skatthlutfall er notað fyrir alla skattskyldu upphæðina.
- Tímabil – Skattskyldu upphæðinni er skipt í hluta, en hver þeirra fellur undir upphæðarbil með sérstöku skatthlutfalli. Hlutur upphæðarinnar sem fellur undir tiltekið bil er skattlagt í samræmi við skatthlutfallið fyrir það bil. Virðisaukaskatturinn er samtala skattupphæðanna sem eru reiknaðar fyrir hvert upphæðarbil.
  > [!NOTE]                                                                                                                              
  > valkostur tímabils er aðeins tiltækt þegar Lína er valin í svæðinu Útreikningsaðferð í svæðinu virðisaukaskattur af síðunni færibreytur fjárhags. 

Tímabil eru sett upp í síðunni gildi virðisaukaskatts með því að færa inn Lágmarks og Hámarks upphæðir fyrir hvern skatthlutfall. Til þess að geta reiknað skatt af öllum skattskyldum upphæðum, óháð því hvaða útreikningsaðferð er valin, verða bil að vera samkvæmt eftirfarandi reglum:
-   Fyrsta bilið verður að vera með lágmark núll.
-   Síðasta bilið verður að hafa hámark núll, sem gefur til kynna óendanleika.
-   Hámark bils verður að vera Lágmark næsta bils.

Ef upphæð er hámark fyrra bils og lágmark næsta bils, mun söluskattshlutfallið fyrir fyrsta bilið vera beitt á upphæðina. Ef upphæð fellur utan við bil sem eru skilgreind með efri og neðri mörkum, er söluskatthlutfallið núll notað.

## <a name="example-whole-amount-method-of-calculation"></a>Útreikningsaðferð heildarupphæðar: Dæmi
Í síðunni gildi VSK-kóði, eru Skatthlutfall virðisaukaskatts sett upp í eftirfarandi tímabilum:

| Neðri mörk     | Hámarksgildi     | Skatthlutfall     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

virðisaukaskattur er reiknaður af allri skattskyldri upphæð.

| Skattskyld upphæð (verð) | Útreikningur    | Virðisaukaskattur |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15:00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a>Útreikningsaðferð tímabila: Dæmi
Í síðunni gildi, eru Skatthlutfall virðisaukaskatts sett upp í eftirfarandi tímabilum:

| Neðri mörk     | Hámarksgildi     | Skatthlutfall     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

Virðisaukaskatturinn er samtala skattupphæðanna sem eru reiknaðar fyrir hvert upphæðarbil.

| Skattskyld upphæð (verð) | Útreikningur                                                               | Virðisaukaskattur |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15:00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Nánari upplýsingar er að finna í [Skatthlutfall virðisaukaskatts á grundvelli Jaðargrunns og Útreikningsaðferðar](marginal-base-field.md)







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

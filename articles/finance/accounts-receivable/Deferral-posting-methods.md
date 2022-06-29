---
title: Aðferðir við frestun færslu
description: Þessi grein lýsir muninum á frestunarbókunaraðferðum fyrir frestun tekna og gjalda í áskriftarreikningi.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017475"
---
# <a name="deferral-posting-methods"></a>Aðferðir við frestun færslu

Þessi grein lýsir muninum á frestunarbókunaraðferðum fyrir frestun tekna og gjalda í áskriftarreikningi.

Á **Frestun tekna og gjalda** síðu eru valkostirnir fyrir frestunaraðferðir **Efnahagsreikningur** og **Hagnaður og tap**. Dæmið í þessari grein mun hjálpa til við að útskýra muninn á þessum tveimur aðferðum og ástæðurnar fyrir því að þú gætir notað eina aðferðina eða hina.

The **Efnahagsreikningur** aðferðin notar aðeins tvo reikninga. Því fylgir minni uppsetning. The **Hagnaður og tap** aðferðin hefur tvo reikninga til viðbótar, **Upphafleg viðurkenning** og **Viðurkenningarjöfnun**, fyrir tekjur, afslætti og kostnað, allt eftir tegund viðskipta. Þessir reikningar eru settir upp á **Frestun vanskil** síða (**Innheimta áskriftar \> Frestun tekna og gjalda \> Uppsetning**). Þrátt fyrir að dæmið snúist um frestaðar tekjur er hægt að nota sama hugtak um fresta afslætti og frestan kostnað.

## <a name="example"></a>Dæmi

Sölureikningur 1 hefur samtals $3,000 og hefur frestað tekjur. Eftirfarandi töflur sýna dreifingarnar þegar þessi sölureikningur er bókaður.

**Efnahagsreikningsaðferð**

| Gerð | Lykill | Debet | Kredit|
|---|---|---|---|
| Debet | Viðskiptakröfur | 3,000.00 | |
| Kredit | Frestaðar tekjur | | 3,000.00 |

**Hagnaðar- og tapaðferð**

| Gerð | Lykill | Debet | Kredit |
|---|---|---|---|
| Debet | Viðskiptakröfur | 3,000.00 | |
| Debet | Tekjufærsla á móti | 3,000.00 | |
| Kredit | Frestaðar tekjur | | 3,000.00 |
| Kredit | Upphafleg tekjufærsla | | 3,000.00 |

Sölureikningur 2 hefur samtals $2,000 og hefur ekki frestað tekjur.

| Gerð | Lykill | Upphæð |
|---|---|---|
| Debet | Viðskiptakröfur | 3,000.00 |
| Kredit | Tekjur | 3,000.00 |

**Samtölur efnahagsreikningsaðferðar fyrir sölureikning 1 og 2 samanlagt**

| Lykill | Debet | Kredit |
|---|---|---|
| Viðskiptakröfur | 5,000.00 | |
| Tekjur | | 2,000.00 |
| Frestaðar tekjur | | 3,000.00 |

Þegar **Efnahagsreikningur** aðferð er notuð er ekki eins auðvelt að sjá brúttótekjur á tímabili. Hluti af tekjunum er færður til **Frestað tekjur** reikning. Hafðu í huga að þar sem tekjur eru færðar á hverju tímabili eru margar skuldfærslur og inneignir í **Frestað tekjur** reikning. Brúttótekjum á tilteknu tímabili verður blandað saman við inn- og útfærslur á tekjufærslu.

**Hagnaðar- og tapaðferðarsamtölur fyrir sölureikning 1 og 2 samanlagt**

| Lykill | Debet | Kredit |
|---|---|---|
| Viðskiptakröfur | 5,000.00 | |
| Tekjur | | 5,000.00 |
| Tekjujöfnun | 3,000.00 | |
| Frestaðar tekjur | | 3,000.00 |

Allar tekjur fara í hagnað og tap **Tekjur** reikning. Síðan eru frestað tekjur færðar úr rekstrarreikningi í efnahagsreikning. Þú getur auðveldlega séð brúttótekjurnar, því allt er sett á **Tekjur** reikning. Hins vegar er hluta af þessum brúttótekjum frestað. Þess vegna er það flutt til **Frestað tekjur** reikning og viðurkennd síðar.

Í **Hagnaður og tap** aðferð, þú getur skoðað **Tekjur** reikning og **Tekjujöfnun** reikning til að sjá brúttótekjur af $5,000 og nettótekjur (að frádregnum frestun) af $2,000. Þó að **Hagnaður og tap** aðferð getur auðveldað skýrslugerð, það eru fleiri reikningar sem þarf að setja upp.

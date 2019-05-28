---
title: Uppsöfnun frís sem byggist á vinnustundum
description: Þetta efnisatriði lýsir því hvernig hægt er að stilla leyfisáætlanir til að safna upp fríi sem byggist á vinnustundum.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8589527f75f48c16244c93c3fdbe3ce7fcd4e366
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518259"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Uppsöfnun frís sem byggist á vinnustundum

[!include [banner](includes/banner.md)]


## <a name="overview"></a>Yfirlit

Fyrirtæki með starfsmenn í tímavinnu geta veitt frí sem byggist á vinnustundum í stað ráðningartíma hjá fyrirtækinu. Upplýsingar um vinnustundir eru venjulega geymdar tíma- og viðverukerfi. Í Talent: Core HR, hægt er að flytja inn þessa reglulegu vinnutíma og yfirvinnutíma og nota þá sem grundvöll fyrir umbun starfsmanns.

## <a name="leave-plans"></a>Leyfisáætlanir

Innan leyfisáætlunarinnar getur gerð uppsöfnunar annaðhvort verðir mánuðir í þjónustu eða vinnustundir. Þegar vinnustundir er valið eru tvær gerðir til sem hægt er að nota fyrir uppsöfnunina: reglulegar og yfirvinna.

Til að setja upp leyfisáætlun til að nota vinnustundir skal fylgja þessum skrefum:

1. Á síðunni **Áætlanir leyfis og fjarvista** skal smellt á **Stofna nýja áætlun**.
2. Færðu inn heiti fyrir leyfisáætlunina.
3. Veldu tíðni uppsöfnunar fyrir áætlunina.
5. Veldu upphafsdagsetningu fyrir áætlunina.
6. Veldu tímabilsgrunn uppsöfnunarinnar og veldu starfsmannamiðaða dagsetningu ef það á.
7. Fyrir áætlun uppsöfnunar skal velja **Vinnustundir** fyrir uppsöfnunargerðina.
8. Veldu gerð vinnustunda sem á að nota við uppsöfnunina.
9. Sláðu inn fjölda vinnustunda og tengda upphæð uppsöfnunar, lágmarksstöðu og upphæð á hámarksyfirfærslu eða styrk.

Uppsöfnunarferli fyrir vinnustundaáætlanir notar tíðni uppsöfnunar, ásamt tímabilsgrunn uppsöfnunar, til að ákvarða vinnustundirnar sem safna á upp.

## <a name="annual-accrual-frequency"></a>Árleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Mánaðarleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 1/8/2018-31/8/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 1/8/2018-31/8/2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Hálfsmánaðarleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Vikuleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Úthlutaðar leyfisáætlanir starfsmanns

Í úthlutuðum leyfisáætlunum starfsmanns er grunnlag og gerð vinnustunda birt fyrir áætlanir þar sem vinnustundir eru skilgreindar sem gerð uppsöfnunar. Fyrir virkar áætlanir eru raunverulegir vinnustundir fyrir uppsöfnunartímabilin frá og með núverandi dagsetningu einnig sýndar til viðmiðunar. 

## <a name="loading-data"></a>Hleður gögnum

Hægt er að flytja inn raunverulegar vinnustundir með einingunni unnar leyfis- og fjarvistarstundir í gagnastjórnun. Ef þú ert að nota vinnutímadagatal mun innflutningur sannprófa að reglulegar vinnustundir fari ekki yfir áætlaðar vinnustundir á dag sem er skilgreint af dagatalinu. Innflutningurinn sannprófar einnig að vinnustundir fyrir tiltekinn dag fari ekki yfir 24 klukkustundir. 

Eftirfarandi upplýsingar eru nauðsynlegar til að flytja inn raunverulegar vinnustundir til að nota í uppsöfnunarferli á leyfi:

+ Númer starfsmanns 
+ Dagsetning sem var unnið
+ Gerð
+ Tímar

Ein dagsetning getur aðeins haft eina af hverri gerð sem tengist henni.

| PERSONNELNUMBER       | DATEWORKED           | GERÐ                  | KLST.                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Reglulegur vinnutími               | 8                    |       
| 000337                | 8/7/2018             | Reglulegur vinnutími               | 8                    |
| 000337                | 8/7/2018             | Yfirvinna              | 3                    |
| 000337                | 8/8/2018             | Reglulegur vinnutími               | 8                    |
| 000337                | 8/7/2018             | Reglulegur vinnutími               | 8                    |
| 000337                | 8/9/2018             | Reglulegur vinnutími               | 8                    |

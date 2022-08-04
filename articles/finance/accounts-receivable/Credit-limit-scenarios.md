---
title: Lánshæfissviðsmyndir
description: Þessi grein lýsir því hvernig lánahámark viðskiptavinar er athugað þegar viðskiptavinur tilheyrir lánahámarkshópi viðskiptavina.
author: JodiChristiansen
ms.date: 06/28/2022
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
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130273"
---
# <a name="credit-limit-scenarios"></a>Lánshæfissviðsmyndir

Í lánastýringu er hægt að úthluta lánamörkum til viðskiptavina á viðskiptamannastigi. Hægt er að úthluta hverjum viðskiptavin í a *lánamarkshópur viðskiptavina*, og hver hópur hefur lánsfjárhámark. Þess vegna er einnig hægt að úthluta lánamörkum til viðskiptavina á hópstigi. Allir viðskiptavinir sem eru úthlutaðir í sama lánahóp viðskiptavina hafa sama lánsfjárhámark.

Almennt eru hóplánamörk athugað á undan einstökum lánamörkum. Einstaklingslánahámarkið hnekkir ekki alltaf hóplánahámarkinu.

Þessi grein lýsir fimm sviðsmyndum sem tengjast lánahópum viðskiptavina og einstökum lánamörkum.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Lánamark viðskiptavinahópsins er meira en einstaklingslánamarkið

Til dæmis hefur viðskiptavinurinn einstaklingsbundið lánahámark $10,000. Viðskiptavininum er úthlutað í lánahóp viðskiptavina og er lánahámark hópsins $15,000. Í þessu tilviki er „virk lánsfjármörk“ viðskiptavinarins $10,000, vegna þess að sú upphæð er lægri en hópahámarkið. Útilokunarreglur athugaðu fyrst hóptakmörkin. Þeir athuga síðan einstaklingsmörkin. Öllum sölupöntunum yfir $10,000 verður lokað.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Einstaklingslánahámarkið er meira en lánamark viðskiptavinahópsins

Til dæmis hefur viðskiptavinurinn einstaklingsbundið lánsfjármörk $20,000. Viðskiptavininum er úthlutað í lánahóp viðskiptavina og er lánahámark hópsins $15,000. Í þessu tilviki er virkt lánamark viðskiptavinarins $15,000, vegna þess að bannreglurnar athuga alltaf hóptakmörkin fyrst. Allar sölupantanir yfir $15,000 verða lokaðar.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Einstaklingslánamörk er stillt á 0,00 og skyldubundið lánamark er stillt á Já

Ef viðskiptavinur hefur einstaklingsbundið lánsfjárhámark sem er stillt á **0,00**, og **Lögboðið lánahámark** valkostur er stilltur á **Já**, virkt lánahámark viðskiptavinarins er $0.00, jafnvel þótt viðskiptavinurinn sé úthlutaður í lánahóp viðskiptavina. Þannig getur viðskiptavinurinn verið hluti af hópi en allar pantanir fara í lánastýringu.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Einstaklingslánamörk er stillt á 0,00 og Ótakmarkað lánamörk er stillt á Já

Ef viðskiptavinur hefur einstaklingsbundið lánsfjárhámark sem er stillt á **0,00**, en **Ótakmarkað lánaheimild** valkostur er stilltur á **Já**, mun viðskiptavinurinn hafa ótakmarkaða inneign, jafnvel þótt þeim sé úthlutað í lánahóp viðskiptavina.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Einstaklingslánamörk er stillt á 0,00 og viðskiptavinurinn er hluti af lánahópi viðskiptavina

Til dæmis hefur viðskiptavinurinn einstaklingsbundið lánahámark sem er stillt á **0,00**, hinn **Ótakmarkað inneign** valkostur er stilltur á **Nei**, og **Lögboðið lánahámark** valkostur er stilltur á **Nei**. Viðskiptavininum er úthlutað í lánahóp viðskiptavina og er lánahámark hópsins $15,000. Í þessu tilviki eru virkt lánamörk viðskiptavinarins hámark hópsins, $15,000. Þess vegna verða allar sölupantanir yfir þeirri upphæð lokað. Þessi hegðun gerir kleift að stýra lánahámarkinu á stigi lánahóps viðskiptavina í stað einstakra viðskiptavina. Allir viðskiptavinir sem eru úthlutað í sama hóp hafa sama lánshæfismat.

---
title: Aðstæður við lánamark
description: Í þessari grein er lýst því hvernig lánamörk viðskiptavinar eru athuguð þegar viðskiptavinur tilheyrir lánamörkuðum viðskiptavinar.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130273"
---
# <a name="credit-limit-scenarios"></a>Aðstæður við lánamark

Í lánastýringu er hægt að úthluta lánamarki á viðskiptavini á stigi viðskiptavinar. Hægt er að úthluta hverjum viðskiptavini á *lánamarkahóp viðskiptavinar* og hver hópur er með lánamark. Þess vegna er einnig hægt að úthluta inneign til viðskiptavina á hópastigi. Allir viðskiptavinir sem úthlutað er á sama lánahóp viðskipavinar eru með sama lánamarkið.

Lánamörk hóps eru almennt athuguð á undan einstaka lánamörkum. Einstaklingsbundna lánamarkið hnekkir ekki alltaf lánamarki hóps.

Þessi grein útskýrir fimm aðstæður sem tengjast lánahópum viðskiptavinar og einstaklingsbundnum lánamörkum.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Lánamörk viðskiptavinahóps eru hærri en lánamörk einstaklingsins

Viðskiptavinur er til dæmis með einstaklingsbundið lánamark upp á $10.000. Viðskiptavininum er úthlutað í hóp viðskiptavina og inneign hópsins er USD 15.000. Í þessu tilviki er „gilt lánamark“ viðskiptavinar $10.000 því að upphæðin er minni en lánamark hópsins. Lokunarreglur athuga fyrst lánamark hópsins. Svo eru einstaka mörk athugðu. Lokað verður á allar sölupantanir yfir $10.000.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Lánamark einstaklingsins er hærra en lánamark viðskiptavinahópsins

Viðskiptavinurinn er til dæmis með einstaklingsbundið lánamark upp á $20.000. Viðskiptavininum er úthlutað í hóp viðskiptavina og inneign hópsins er USD 15.000. Í þessu tilviki er gilt lánamark viðskiptavinarins $15.000 því að lokunarreglurnar athuga alltaf lánamark hópsins fyrst. Lokað verður á allar sölupantanir sem kosta meira en USD 15.000.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Lánamark einstaklingsin er stillt á 0,00 og skyldulánamark er stillt á „Já“

Ef viðskiptavinurinn er með einstaklingsbundið lánamark sem stillt er á **0,00** og valkosturinn **Skyldulánamark** er stilltur á **Já** er gilt lánamark viðskiptavinarins $0,00 jafnvel þótt viðskiptavininum er úthlutað á lánahóp viðskiptavinar. Á þennan hátt getur viðskiptavinurinn verið hluti af hópi en allar pantanir fara í lánastýringu.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Lánamark einstaklingsins er stillt á 0,00 og ótakmarkað lánamark er stillt á „Já“

Ef viðskiptavinurinn er með einstaklingsbundið lánamark sem stillt er á **0,00** en valkosturinn **Ótakmarkað lánamark** er stilltur á **Já** mun viðskiptavinurinn fá ótakmarkað lán ef honum er úthlutað á lánahóp viðskiptavinar.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Einstaklingsbundið lánamark er stillt á 0,00 og viðskiptavinurinn er hluti af lánahópi viðskiptavina

Viðskiptavinurinn er til dæmis með einstaklingsbundið lánamark sem stillt er á **0,00**, valkostinn **Ótakmarkað lán** stilltan á **Nei** og valkostinn **Skyldulánamark** stilltan á **Nei**. Viðskiptavininum er úthlutað í hóp viðskiptavina og inneign hópsins er USD 15.000. Í þessu tilviki er gilt lánamark viðskiptavinarins lánamark hópsins, $15.000. Því verður lokað fyrir allar sölupantanir yfir þeirri upphæð. Þessi hegðun gerir kleift að stjórna lánamarki á lánahópsstigi viðskiptavinar í staðinn fyrir einstaklingsbundnu viðskiptavinastigi. Allir viðskiptavinir sem er úthlutað á sama hóp eru með sama lánamarkið.

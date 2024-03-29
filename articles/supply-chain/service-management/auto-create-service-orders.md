---
title: Stofna þjónustupantanir sjálfkrafa
description: Þú getur búið til þjónustupantanir sem eru byggðar á þjónustusamningi fyrir gildistíma þjónustusamningsins.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f48e2156ea5f57e600cc5dec09a78a91992d60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675796"
---
# <a name="automatically-create-service-orders"></a>Stofna þjónustupantanir sjálfkrafa 

[!include [banner](../includes/banner.md)]


Þú getur búið til þjónustupantanir sem eru byggðar á þjónustusamningi fyrir gildistíma þjónustusamningsins.

Þjónustupantanirnar sem þú býrð til úr þjónustusamningi eru allar tengdar við þjónustusamninginn.

Þjónustupantanir eru myndaðar sjálfkrafa samkvæmt eftirfarandi stillingum:

  - Þjónustusamningsbilið sem er sett upp í þjónustusamningslínunum. Þjónustusamningsbilið gefur til kynna hversu oft þjónustupöntunarlínur eru búnar til. Nánari upplýsingar er að finna í [Þjónustutímabil](service-intervals.md).

  - Tímabilið sem þú tilgreinir til að skilgreina þjónustutímabilið í **Frá dagsetningu** og **Til dagsetningar** reitunum í **Búa til þjónustupantanir** skjámyndinni. Nánari upplýsingar er að finna í [Búa til þjónustupantanir sjálfkrafa](create-service-orders-automatically.md).

  - The **Sameina þjónustupantanir** valkostur á þjónustusamningnum haus. Þessi valkostur skilgreinir hvort þjónustupöntunarlínur sem búnar eru til úr þjónustusamningi, sameinar þjónustupantanir samkvæmt starfsmanni, þjónustuverklið, þjónustuhlut eða þjónustusamningi. Nánari upplýsingar er að finna í [Sameina þjónustupantanir](combine-service-orders.md).

  - **Tímagluggi** valkosturinn á þjónustusamningslínunni. Tímaglugginn skilgreinir hversu langt þjónustupöntunarlínan getur færst með tilliti til reiknaðrar dagsetningar hennar. Nánari upplýsingar er að finna í [Tímagluggi](time-windows.md).


> [!NOTE]
> <P>Ef dagurinn sem tilgreindur er fyrir þjónustupöntun er ekki opinn í dagatalinu sem þú hefur valið í <STRONG>Færibreytur þjónustukerfis</STRONG> skjámynd, birtist skilaboð um ósamræmi í dagatali. Þú getur hæglega hunsað skilaboðin; þjónustupöntunin mun verða búin til, jafnvel þótt dagurinn sé lokaður á dagatalinu.</P>

## <a name="example-1"></a>Dæmi 1

Þjónustusamningurinn stendur frá 1. janúar 2012 til 31. desember 2012. Ef þjónustutímabilið sem þú tilgreinir í **Búa til þjónustupantanir** skjámynd er frá 1. nóvember 2012 til 1. febrúar 2013, eru þjónustupantanir búnar til frá 1. nóvember 2012 til 31. desember 2012.

## <a name="example-2"></a>Dæmi 2

Þjónustusamningurinn stendur frá 1. janúar 2012 til 31. desember 2012. Tvær þjónustusamningslínur eru hengdar við þjónustusamninginn. Fyrsti þjónustusamningslínan er með upphafsdagur 2. janúar 2012 og lokadagur 1. mars 2012. Önnur þjónustusamningslína er með upphafsdag 1. apríl 2012 og lokadagsetning 31. desember 2012. Þú tilgreinir tímabil í **Búa til þjónustupantanir** skjámynd sem er frá 1. október 2012 til 31. desember 2012. Þess vegna eru þjónustupantanir aðeins myndaðar fyrir aðra samningslínuna, vegna þess að upphafsdagur og lokadagur fyrstu samningslínunnar eru fyrir tímabilið sem þú tilgreindir fyrir þjónustupöntunina.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
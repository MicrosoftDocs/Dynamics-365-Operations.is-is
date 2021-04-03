---
title: Þjónustuhlutarflokkar
description: Hlutaflokkar gagnast til þess að flokka og sía gögnin um hluti fyrir skýrslur og talnagögn.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9d19e29dbddb0bccf3221cc82e6dbb2c05f7e85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266080"
---
# <a name="service-object-groups"></a>Þjónustuhlutarflokkar 

[!include [banner](../includes/banner.md)]

Hlutaflokkar gagnast til þess að flokka og sía gögnin um hluti fyrir skýrslur og talnagögn. Til dæmis er hægt að flokka hluti eftir landfræðilegri staðsetningu eða gerð.

## <a name="group-by-geographical-location"></a>Flokkur eftir landfræðilegri staðsetningu

Hægt er að nota þessa flokkunaraðferð til þess að sýna hvar hinir ýmsu ólíku hlutir sem fyrirtæki notanda þjónustar eru staðsettir. Flokkun hluta eftir landfræðilegri staðsetningu getur líka verið gagnleg ef nauðsynlegt er að auðkenna hlutina sem fyrirtæki notanda veitir nú þegar þjónustu fyrir í tilteknu landi/svæði, svo dæmi sé tekið.

## <a name="example"></a>Dæmi

Viðskiptavinur frá Belgíu hringir í þjónustumiðstöð notanda og vill stofna þjónustusamning fyrir hlut, ABC. Notandinn hefur tengt hlutaflokk eftir landfræðilegri staðsetningu, Belgíu, við alla hluti sem eru þjónustaðir í Belgíu. Með því að nota þennan flokk sem síu er hægt að leita með hraði til þess að kanna hvort ABC sé þegar til sem færsla í forriti notanda eða hvort nauðsynlegt er að setja upp nýjan hlut. 

## <a name="group-by-type"></a>Flokkur eftir gerð

Hægt er að nota þessa flokkunaraðferð til þess að sýna gerðir þeirra hluta sem fyrirtæki notanda þjónustar. Flokkun hluta eftir gerð getur líka verið gagnleg ef ætlunin er að stofna nýjan hlut byggðan á svipuðum hlutum sem þegar eru til í forritinu.

## <a name="example"></a>Dæmi

Viðskiptavinur hringir og vill setja upp þjónustusamning fyrir loftræstibúnað, HIJ. Engin færsla er til fyrir þetta tæki. Hins vegar er búið að setja upp hlutaflokk með nafninu Loftræstibúnaður og tengja hann við alla loftræstibúnaðarhluti. Þar af leiðandi er hægt að leita fljótt að og auðkenna allan annan loftræstibúnað og nota sniðmátsupplýsingar um þessa hluti til þess að stofna þjónustusamningslínur fyrir HIJ. Með þvi að nota flokka á þennan hátt er hægt að setja upp nýja hluti með hraði og ákvarða þjónustuverkliðina sem þarf að framkvæma á þeim. 

## <a name="create-service-object-groups"></a>Búa til þjónustuhlutaflokka

Stofna flokka sem hægt er að tengja þjónustuhluti við. Þjónustuhlutir eru birgðavara og aðrar vörur sem þjónustur eru framkvæmdar fyrir. Eftir þjónustuhlutum flokkun, hægt er að stofna skýrslur fyrir svipað og tengdar þjónustuhluti. Til dæmis gæti þjónustuhlutaflokk samanstanda af tveimur þjónustuhluti: Einn þjónustuhlut er setti og önnur þjónustuhlut er þjónustan sett upp í setti.

Til að búa til þjónustuhlutaflokka, skal fylgja þessum skrefum:

1. Smelltu á **Þjónustustjórnun > Uppsetning > Þjónustuhlutir > Flokkar þjónustuhluta**.

2. Smelltu á **Nýtt** til að stofna nýjan flokk þjónustuhluta.

3. Færðu inn einkvæmt heiti fyrir hóp þjónustuhluta og hugsanlega lýsingu.

Hægt er að tengja þjónustuhluti við flokk með því að nota skjámyndina **Þjónustuhlutir**. 

## <a name="see-also"></a>Sjá einnig

[Stofna þjónustuhluta](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
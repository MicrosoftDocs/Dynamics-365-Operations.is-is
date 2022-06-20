---
title: Valkostir innleiðingar á efnisbirtingarneti
description: Þessi grein fer yfir mismunandi valkosti fyrir innleiðingu efnisafhendingarnets (CDN) sem hægt er að nota með Microsoft Dynamics 365 Commerce umhverfi. Þessir valmöguleikar fela í sér innbyggð tilvik af Azure Front Door sem Commerce býður upp á og tilvik Azure Front Door í eigu viðskiptavinar.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a63751d42ab98610904191f1c09794b2311b0189
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884418"
---
# <a name="content-delivery-network-implementation-options"></a>Valkostir innleiðingar á efnisbirtingarneti

[!include [banner](includes/banner.md)]

Þessi grein fer yfir mismunandi valkosti fyrir innleiðingu efnisafhendingarnets (CDN) sem hægt er að nota með Microsoft Dynamics 365 Commerce umhverfi. Þessir valmöguleikar fela í sér innbyggð tilvik af Azure Front Door sem Commerce býður upp á og tilvik Azure Front Door í eigu viðskiptavinar.

Viðskiptavinir Commerce hafa úr nokkrum kostum að velja þegar þeir taka ákvörðun um hvaða CDN-þjónustu þeir ætli sér að nota með Commerce-umhverfinu. Commerce er gefið út með grunnstuðningi Azure Front Door sem nær yfir grunnhýsingu og sérsniðnum kröfum um lén. Fyrir fyrirtæki sem vilja hafa meiri stjórn og sértækari öryggisráðstafanir, t.d. eldvegg vefforrits (WAF), gæti besti valkosturinn verið sá að nota annaðhvort tilvik af Azure Front Door í eigu viðskiptavinar eða ytri CDN-þjónustu.

Hægt er að nota eftirtalda þrjá valmöguleika CDN-innleiðingar með Commerce-umhverfum:

- Tilvik Commerce af Azure Front Door
- Tilvik viðskiptavinar af Azure Front Door (fyrir aukna stjórn og fleiri öryggiseiginleika)
- Ytri CDN-þjónusta

Allir valkostir CDN-innleiðingar bjóða aðeins upp á gagnvirkt HTML-efni á sérsniðnum lénum. Commerce sér sjálfkrafa um allt JavaScript, stölluð stílblöð (CSS), myndir, myndbönd og annað fast efni í gegnum CDN sem Microsoft stýrir. Kosturinn sem er valinn ákvarðar aðgerðarmöguleika, stjórnunarmöguleika og frekari öryggismöguleika sem verða í boði.

Eftirfarandi mynd sýnir yfirlit yfir hönnun Commerce.

![Yfirlit Commerce-hönnunar.](media/Commerce_CDN-Option_ComparisonModels.png)

Frekari upplýsingar um hvernig setja á upp tilvik Azure Front Door fyrir svæði Commerce er að finna í [Bæta við CDN-stuðningi](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Nota tilvik Azure Front Door sem Commerce útvegar

Í eftirfarandi töflu er listi yfir kosti og galla þess að nota tilvik af Azure Front Door sem Commerce útvegar til að stjórna endastöðvum efnis.

| VIÐF | Gallar |
|------|------|
| <ul><li>Tilvikið er innifalið í kostnaði Commerce.</li><li>Vegna þess að Commerce-teymið stjórnar tilvikinu þarf minna viðhald og boðið er upp á uppsetningarleiðbeiningar.</li><li>Tölvukerfi hýst af Azure er stillanlegt, öruggt og áreiðanlegt.</li><li>SSL-vottorð krefst uppsetningar í eitt skipti og er sjálfkrafa endurnýjað.</li><li>Commerce-teymið fylgist með villum og frávikum í tilvikinu.</li></ul> | <ul><li>WAF er ekki stutt.</li><li>Engar sérstakar sérstillingar eða breytingar á stillingum eru til staðar.</li><li>Tilvikið er háð Commerce-teyminu hvað varðar uppfærslur og breytingar.</li><li>Sérstakt tilvik af Azure Front Door er nauðsynlegt fyrir apex-lén og leggja þarf aukavinnu í að samþætta apex-lén við Azure DNS.</li><li>Viðskiptavinurinn fær engar fjarmælingar á svörum á sekúndu (RPS) eða villutíðni.</li></ul> |

Eftirfarandi mynd sýnir hönnun Azure Front Door-tilviks sem Commerce útvegar.

![Tilvik Azure Front Door sem Commerce útvegar.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Nota tilvik af Azure Front Door í eigu viðskiptavinar

Í eftirfarandi töflu er listi yfir kosti og galla þess að nota tilvik af Azure Front Door í eigu viðskiptavinar til að stjórna endastöðvum efnis.

| VIÐF | Gallar |
|------|------|
| <ul><li>Uppsetning er örugg og auðvelt að stjórna.</li><li>Tölvukerfi hýst af Azure er stillanlegt, öruggt og áreiðanlegt.</li><li>Tilvikið leyfir samþættingu WAF og grófa stjórnun á reglum fyrir fínstilltara öryggi sem er sérstaklega stillt fyrir svæðið þitt.</li><li>Tilvikið leyfir fínstjórnun á SSL-vottorðum (bæði í eigu viðskiptavinar og stjórnað af Azure Front Door) og lénatengingum.</li><li>Tilvikið býður upp á lausn apex-léns ef það er parað beint við Azure DNS.</li><li>Boðið er upp á fjarmælingar og viðvaranir.</li><li>SSL-vottorðið krefst uppsetningar í eitt skipti og er sjálfkrafa endurnýjað.</li></ul> | <ul><li>Tilvikið er sjálfstýrt.</li><li>Nauðsynlegt er að keyra í gegn forþekkingu.</li></ul> |

Eftirfarandi mynd sýnir tölvukerfi Commerce sem inniheldur tilvik Azure Front Door í eigu viðskiptavinar.

![Tölvukerfi Commerce sem inniheldur tilvik Azure Front Door í eigu viðskiptavinar.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Nota ytri CDN-þjónustu

Í eftirfarandi töflu er að finna kosti og galla þess að nota ytri CDN-þjónustu til að stjórna endastöðvum efnis.

| VIÐF | Gallar |
|------|------|
| <ul><li>Þessi valkostur er gagnlegur þegar núverandi lén eru þegar hýst í ytra CDN.</li><li>WAF: Fer eftir ytri þjónustuaðila.</li></ul> | <ul><li>Annar samningur og viðbótarkostnaður er nauðsynlegur.</li><li>SSL gæti sett á viðbótarkostnað.</li><li>Þar sem þjónustan er aðskilin frá skýjaskipulagi Azure, verður að hafa umsjón með öðru kerfi.</li><li>Þjónustan gæti krafist lengri fjárfestingu á tíma í uppsetningu endastöðvar og öryggis.</li><li>Þjónustan er sjálfstýrð.</li><li>Þjónustunni fylgir eigið eftirlit.</li></ul> |

Eftirfarandi mynd sýnir tölvukerfi Commerce sem inniheldur ytri CDN-þjónustu.

![Tölvukerfi Commerce sem inniheldur ytri CDN-þjónustu.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

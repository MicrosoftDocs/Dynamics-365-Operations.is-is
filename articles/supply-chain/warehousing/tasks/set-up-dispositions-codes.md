---
title: Setja upp ráðstöfunarkóða
description: Þetta ferli leggur áherslu á uppsetningu ráðstöfunarkóða sem hægt er að nota í farsíma fyrir móttökuferli skilapöntunar.
author: Mirzaab
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb83108c934e864da0df39ec4ee36a0bc7ba7588
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574066"
---
# <a name="set-up-dispositions-codes"></a>Setja upp ráðstöfunarkóða

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á uppsetningu ráðstöfunarkóða sem hægt er að nota í farsíma fyrir móttökuferli skilapöntunar. Ráðstöfunarkóðar eru safn reglna sem hægt er að nota þegar vörur eru mótteknar. Til dæmis þegar notandi vinnu notar fartæki til að taka á móti vörum sem var skemmt, verður notandi að skanna ráðstöfunarkóða fyrir skemmdar vörur. birgðastaða mótteknu varanna, vinnusniðmátið, og staðsetningarleiðbeininga er hægt að ákvarða úr skannaðs ráðstöfunarkóða. notkun ráðstöfunarkóða er valfrjáls fyrir móttökuferli innkaupapöntunar og ferlið við að skrá framleiðslupöntun sem lokinni. notkun ráðstöfunarkóða er skylda fyrir ferlið við móttöku sölupöntunar, ef vörur eru skráðar með fartæki.  Þetta Leiðbeiningar var stofnuð með því að nota sýnigögn fyrirtækisins USMF. Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi. 

1. Fara í Vöruhúsakerfi > Uppsetning > Fartæki > Ráðstöfunarkóðar.
2. Smellið á „Nýtt“.
    * Stofna nýjan ráðstöfunarkóða sem nota á fyrir skil viðskiptavinarins.  
3. Í reitnum Ráðstöfunarkóði skal slá inn gildi.
4. Í reitnum birgðastaða, velja birgðastöðu þar sem er birgðalæsing.
    * Ef verið er að nota USMF, veldu ‚Læsing'. Hægt er að bæta birgðastöðu við ráðstöfunarkóða til að hnekkja sjálfgefna stöðu sem er í pöntunarlínum.  
5. Færa inn gildi í reitnum Vinnusniðmát.
    * Valfrjálst: Velja sniðmátskóða vinnu sem er tengd skilapöntun. Ef ekkert gildi er gefið verður vinnusniðmátið leyst með því að nota staðlaða reglur sem skilgreind er í kerfinu þínu. Val á vinnusniðmáti takmarkar þau ferli sem hægt er að nota með þessum ráðstöfunarkóða. Til dæmis hafi ráðstöfunarkóða vinnusniðmát með vinnupöntun af gerðinni innkaupapöntun, er ekki hægt að nota það til að skrá vörur sem er skilað af viðskiptavinum.  
6. Í reitnum Ráðstöfunarkóði skila skal slá inn gildi.
    * Ráðstöfunarkóði skila ákvarðar afgangur skilapöntunarferlis fyrir vörur sem eru skráðar. Í þessu dæmi ætti viðskiptavinar að fá kreditnótu. Bæta við ráðstöfunarkóða skila sem inniheldur lánsfé aðgerðar.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
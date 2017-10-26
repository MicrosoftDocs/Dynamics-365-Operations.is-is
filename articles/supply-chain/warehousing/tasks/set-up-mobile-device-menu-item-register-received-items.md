--- 
title: "Setja upp valmyndaratriði fartækis til að skrá mótteknar vörur"
description: "Þetta verk leggur áherslu á uppsetningu valmyndaratriði fartækis."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7b5d757361c1163bbd0300abd3da4e0a2dd6b0e0
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Setja upp valmyndaratriði fartækis til að skrá mótteknar vörur

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta verk leggur áherslu á uppsetningu valmyndaratriði fartækis. Þetta valmyndaratriði er notuð fyrir skráningu á móttöku á vörum sem eru pantaðar með innkaupapöntun. 

Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF. Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.


## <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis
1. Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis
2. Smellið á „Nýtt“.
3. Í svæðið heiti valmyndaratriðis, færa inn gildi.
    * Þetta er einkvæmt kenni fyrir þetta valmyndaratriði fartækis. Til dæmis væri hægt að slá inn ‚Mín pöntun‘.  
4. Í reitinn Titill skal slá inn gildi.
    * Þetta er titillinn sem birtist notendum í fartækinu. Til dæmis væri hægt að slá inn ‚Skráning pöntunar‘.  
5. Í reitnum Stilling velurðu „Vinna“.
    * Skráning á lagermagni sem er móttekið fyrir innkaupapöntunarlínu stofnar vinnu sem flytur vörur úr móttökusvæði og inn í birgðir. Vinna er ekki stofnuð fyrr en vörur eru skráðar.  Þess vegna skal hafa valkostinn Nota fyrirliggjandi vinnu stilltan á Nei.  
6. Útvíkka eða draga saman hlutann Almennt.
7. Í reitnum Ferli verkstofnunar skal velja ‚Móttaka innkaupapöntunarvöru‘.
    * Innkaupapöntunarlínu verður að vera auðkenna áður en hægt er að skrá á lager í vöruhúsi. Í þessu dæmi verður fartækið skráð á númer innkaupapöntunar og vörunúmer og þetta leyfir kerfinu að auðkenna línu Innkaupapöntunar. Frágangsvinna verður stofnuð og annar starfsmaður getur sótt hana.    Skráningaraðferð vinnu sem er valin ákvarðar hvaða svæði verða tiltæk á flipanum Almennt.  
    * Ef valkosturinn Nota sjálfgefin gögn er valinn er hnappurinn Sjálfgefin gögn virkjaður. Hér er hægt að velja svæðin til að birta þau gögn sem starfsmaður þarf yfirleitt daglegri vinnu í svo að þessi gildi eru sýnd í fartækinu.  
    * Flokkunarfæribreytur númeraplötu virkar í samsetningu með röðunarflokki einingarinnar sem er tengdur við vöruna sem verið er að móttaka. Hægt er að tilgreina hvort flokka skuli innhreyfingar sem eru minni en að meiri en eitt bretti á eina númeraplötu eða skipta þeim á númeraplötu fyrir hverja einingu.  
    * Ef valkosturinn Mynda númeraplötu er valinn myndar þetta einkvæmt númeraplötunúmer samræmi við val á númeraröð.   
    * Hægt er að velja sniðmátið sem notað er þegar vinna er stofnuð. Til dæmis ef þú skráir vöru í innkaupapöntun verður frágangsvinna mynduð samkvæmt vinnusniðmátinu. Ef þú velur ekki vinnusniðmát hér mun kerfið úthluta sniðmáti samkvæmt fyrirspurnarskilyrðum sem tengjast sniðmátunum.  
    * Ef ráðstöfunarkóðar birtast í fartækinu geta starfsmenn metið stöðu eða gæði varanna og valið viðeigandi kóða. Reglur um ráðstöfunarkóða sem ákvarða hvort vörurnar verða tiltækar fyrir önnur vöruhúsaferli. Reglurnar ákvarða einnig hvaða staðsetningarleiðbeiningar eru notaðar fyrir vinnu sem er stofnuð.   
    * Ef valkosturinn Ráðstöfunarkóðar runu er valinn geta starfsmenn metið stöðu eða gæði runu og valið viðeigandi ráðstöfunarkóða.  Reglurnar sem eru settar um ráðstöfunarkóða runu ákvarða hvort runuvinnslan verður tiltæk í öðru vöruhúsaferli.  
    * Ef valkosturinn Prenta merki er valinn verður númeraplata sjálfkrafa prentuð þegar vörur eru mótteknar.  
8. Smellið á „Vista“.
9. Lokið síðunni.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Bæta valmyndaratriði við valmynd fartækis
1. Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmynd fartækis
2. Notaðu flýtiafmörkun til að sía í reitnum Heiti með gildinu ‚Á innleið‘.
3. Smella á Breyta.
4. Í trénu velurðu 'í er Tiltæk fyrir valmyndinni og trjáskipulag vörur, velja valmyndaratriðið sem var stofnuð áður en.'.
    * Valmyndaratriði sem var stofnað áður en valið.  
5. Smella á ör sem vísar til hægri.
6. Smellið á „Vista“.
7. Lokið síðunni.


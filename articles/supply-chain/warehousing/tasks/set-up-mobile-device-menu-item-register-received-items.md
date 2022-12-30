---
title: Setja upp valmyndaratriði fartækis til að skrá mótteknar vörur
description: Í þessari grein er lögð áhersla á uppsetningu valmyndaratriði fartækis.
author: Mirzaab
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b59a78ef98215bec7610fe17ed56e6fc287004c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882316"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Setja upp valmyndaratriði fartækis til að skrá mótteknar vörur

[!include [banner](../../includes/banner.md)]

Í þessari grein er lögð áhersla á uppsetningu valmyndaratriði fartækis. Þetta valmyndaratriði er notuð fyrir skráningu á móttöku á vörum sem eru pantaðar með innkaupapöntun. 

Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF. Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.


## <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis
1. Í skoðunarrúðunni ferðu í **Einingar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmyndaratriði fartækis**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti valmyndaratriðis** skal færa inn gildi. Þetta er einkvæmt kenni fyrir þetta valmyndaratriði fartækis. Til dæmis væri hægt að slá inn `My PO registration`.  
4. Í reitinn **Titill** skal slá inn gildi. Þetta er titillinn sem birtist notendum í fartækinu. Til dæmis væri hægt að slá inn `PO registration`.  
5. Í reitnum **Stilling** velurðu **Vinna**. Skráning á lagermagni sem er móttekið fyrir innkaupapöntunarlínu stofnar vinnu sem flytur vörur úr móttökusvæði og inn í birgðir. Vinna er ekki stofnuð fyrr en vörur eru skráðar. Þess vegna skal hafa valkostinn **Nota fyrirliggjandi vinnu** stilltan á **Nei**.
6. Í reitnum **Ferli verkstofnunar** í hlutanum **Almennt** skal velja **Móttaka innkaupapöntunarvöru**.
    - Innkaupapöntunarlínu verður að vera auðkenna áður en hægt er að skrá á lager í vöruhúsi. Í þessu dæmi verður fartækið skráð á númer innkaupapöntunar og vörunúmer og þetta leyfir kerfinu að auðkenna línu Innkaupapöntunar. Frágangsvinna verður stofnuð og annar starfsmaður getur sótt hana. Skráningaraðferð vinnu sem er valin ákvarðar hvaða svæði verða tiltæk á flýtiflipanum **Almennt**.  
    - Ef valkosturinn **Nota sjálfgefin gögn** er valinn er hnappurinn **Sjálfgefin gögn** virkjaður. Hér er hægt að velja svæðin til að birta þau gögn sem starfsmaður þarf yfirleitt daglegri vinnu í svo að þessi gildi eru sýnd í fartækinu.  
    - **Flokkunarfæribreytur númeraplötu** virkar í samsetningu með röðunarflokki einingarinnar sem er tengdur við vöruna sem verið er að móttaka. Hægt er að tilgreina hvort flokka skuli innhreyfingar sem eru minni en að meiri en eitt bretti á eina númeraplötu eða skipta þeim á númeraplötu fyrir hverja einingu.  
    - Ef valkosturinn **Mynda númeraplötu** er valinn myndar þetta einkvæmt númeraplötunúmer samræmi við val á númeraröð.  
    - Hægt er að velja sniðmátið sem notað er þegar vinna er stofnuð. Til dæmis ef þú skráir vöru í innkaupapöntun verður frágangsvinna mynduð samkvæmt vinnusniðmátinu. Ef þú velur ekki vinnusniðmát hér mun kerfið úthluta sniðmáti samkvæmt fyrirspurnarskilyrðum sem tengjast sniðmátunum.  
    - Ef ráðstöfunarkóðar birtast í fartækinu geta starfsmenn metið stöðu eða gæði varanna og valið viðeigandi kóða. Reglur um ráðstöfunarkóða sem ákvarða hvort vörurnar verða tiltækar fyrir önnur vöruhúsaferli. Reglurnar ákvarða einnig hvaða staðsetningarleiðbeiningar eru notaðar fyrir vinnu sem er stofnuð.   
    - Ef valkosturinn **Ráðstöfunarkóðar runu** er valinn geta starfsmenn metið stöðu eða gæði runu og valið viðeigandi ráðstöfunarkóða. Reglurnar sem eru settar um ráðstöfunarkóða runu ákvarða hvort runuvinnslan verður tiltæk í öðru vöruhúsaferli.  
    - Ef valkosturinn **Prenta merki** er valinn verður númeraplata sjálfkrafa prentuð þegar vörur eru mótteknar.  
7. Veljið **Vista**.
8. Lokið síðunni.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Bæta valmyndaratriði við valmynd fartækis
1. Í Skoðunarrúðunni ferðu í **Einingar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmyndaratriði fartækis**.
2. Nota **flýtiafmörkun** til að sía í reitnum **Heiti** með gildið `inbound`.
3. Veljið **Breyta**.
4. Í trénu Tiltækar valmyndr og atriði, velja valmyndaratriðið sem var stofnuð áður.
5. Veldu örina sem vísar til hægri.
6. Veljið **Vista**.
7. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
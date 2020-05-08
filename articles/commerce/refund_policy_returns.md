---
title: Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás
description: Þetta efni útskýrir hvernig á að setja upp skil og endurgreiðslu stefnu fyrir rás.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265585"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Yfirlit

Return stefnu rásarinnar í Dynamics 365 Commerce gerir smásöluaðilum kleift að stilla framfylgni þar sem hægt er að leyfa greiðslutilboð til að vinna úr skilum á sölustað (POS) tæki.  

Þetta efni lýsir þrepunum til að setja upp skil og endurgreiðslu stefnu fyrir rás.

Umfang stefnunnar er sem stendur takmarkað við að setja greiðslutilboð sem hægt er að leyfa fyrir rás. Listinn „leyfður“ er byggður á greiðslumáta sem notaðir voru við kaupin. Dæmi:

- Ef kaup voru gerð með gjafakorti er verslunin stefna að afgreiða endurgreiðslur aðeins á nýju gjafakorti eða veita lánsfé. 
- Ef sala fer fram með reiðufé eru möguleikarnir sem eru leyfðir til endurgreiðslu reiðufé, gjafakort og viðskiptareikningur en ekki kreditkort. 


## <a name="enable-return-policy"></a>Virkja skilareglu

Gerðu eftirfarandi til að virkja skilareglu rásarvirkninnar:

1. Farðu í vinnusvæðið **Eiginleikastjórnun** í Dynamics 365 Commerce.
2. Leitaðu að eiginleikanum **Virkja skilareglur rása** á listanum yfir heiti eiginleika.
3. Veldu **Virkja núna**. 

## <a name="configure-return-policy"></a>Stilla skilareglu

Fylgdu þessum skrefum til að stilla aftur stefnu fyrir smásöluverslun eða netverslun.

1. Farðu í **Verslun og verslun** \> **Uppsetning rásar** \> **Skilar** \> **Skilastefna rásarinnar**.

2. Veldu **Nýtt** til að búa til nýtt sniðmát skilareglu. Veldu sniðmátið í vinstri glugganum til að nota sniðmát sem fyrir er. Fyrir ný sniðmát skaltu bæta við nafni og lýsingu sem mun hjálpa þér að bera kennsl á stefnuna þegar henni er beitt á rásina.

   ![Bættu við nýrri skilareglu](media/Return-policy-page1.png "Bæta við nýrri skilareglu")
     
   
3. Í kaflanum **Leyfðar endurgreiðsluaðferðir**, skilgreina **Leyft** greiðslutilboðum skila sem eru sértæk fyrir hverja greiðslumáta.
   ![Bæta við greiðslumátum](media/Return-policy-page2.PNG "Stilltu leyfðar greiðslumáta fyrir hverja greiðslugerð")
   
    > [!IMPORTANT]
    > - Greiðslumátarnir eru fengnir af þeim greiðslumáta sem settur er fyrir stofnunina.
    > - Með því að bæta við leyfðri útboðsgerð fyrir hverja skráða greiðslumáta verður tryggt að hægt sé að skila í leyfilega gerð útboðs.
    
4. Tengdu sniðmát skilareglu við verslanirnar þar sem það verður notað. Veldu **Bæta við** á flipann **Smásölurásir** og tengdu tiltækar rásir. 

    - Í glugganum **Velja fyrirtækjahnúta** velurðu verslanir, svæði og fyrirtæki sem sniðmátið ætti að vera tengt við.
    - Aðeins er hægt að tengja eitt sniðmát skilareglu við hverja verslun.
    - Notaðu örvahnappana til að velja verslanir, svæði eða fyrirtæki.
    - Gildistaka stefnunnar verður sá dagur sem stefnunum er beitt á rásirnar og rásastörfin eru keyrð. 

    ![Svarglugginn Veljið fyrirtækjahnúta](media/Return-policy-page3.PNG "Svarglugginn Veljið fyrirtækjahnúta")

5. Á síðunni **Dreifingaráætlun**, keyrðu **1070** vinnslu til að gera skilaregluna á rásinni tiltæka fyrir POS.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Forskoðaðu aftur skilareglu rásarinnar í POS

Fylgdu skrefunum í báðum eftirfarandi dæmum til að skoða leyfðar gerðir tilboða í POS.

1. Skráðu þig inn í POS sem gjaldkera eða stjórnandi.
2. Undir **Vakt og skúffa**, veldu **Sýna færslubók**.
3. Veldu færslu sem er hluti af skilunum. 
4. Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.  
- Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.
- Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.
- Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.

-eða-

1. Skráðu þig inn í POS sem gjaldkera eða stjórnandi.
2. Veldu **Skilafærsla** og sláðu inn kvittunarauðkenni með strikamerkjaskönnun eða með handvirkri færslu. 
3. Veldu færslu sem er hluti af skilunum. 
4. Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.  
- Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.
- Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.
- Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.

![Endurgreiðsla ekki leyfð](media/Return-policy-page6.png "Gerð endurgreiðslu ekki leyfð")



![Listi yfir greiðsluhætti](media/Return-policy-page5.PNG "Gerðir endurgreiðslu ekki leyfð")

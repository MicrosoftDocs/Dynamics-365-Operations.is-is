---
title: Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás
description: Þessi grein útskýrir hvernig á að setja upp skila- og endurgreiðslustefnu fyrir rás.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: b93852bfb7c6f5a9f2f83f30a1f76da3f9559c7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286838"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás

[!include [banner](includes/banner.md)]

Return stefnu rásarinnar í Dynamics 365 Commerce gerir smásöluaðilum kleift að stilla framfylgni þar sem hægt er að leyfa greiðslutilboð til að vinna úr skilum á sölustað (POS) tæki.  

Þessi grein lýsir skrefunum til að setja upp skila- og endurgreiðslustefnu fyrir rás.

Umfang stefnunnar er sem stendur takmarkað við að setja greiðslutilboð sem hægt er að leyfa fyrir rás. Listinn „leyfður“ er byggður á greiðslumáta sem notaðir voru við kaupin. Dæmi:

- Ef kaup voru gerð með gjafakorti er verslunin stefna að afgreiða endurgreiðslur aðeins á nýju gjafakorti eða veita lánsfé. 
- Ef sala fer fram með reiðufé eru möguleikarnir sem eru leyfðir til endurgreiðslu reiðufé, gjafakort og viðskiptareikningur en ekki kreditkort. 

## <a name="enable-return-policy"></a>Virkja skilareglu

Til að virkja skilareglu rásar í Commerce Headquarters skal fylgja þessum skrefum.

1. Farðu í vinnusvæðið **Eiginleikastjórnun** í Dynamics 365 Commerce.
1. Leitaðu að eiginleikanum **Virkja skilareglur rása** á listanum yfir heiti eiginleika.
1. Veldu **Virkja núna**.
1. Á síðunni **Dreifingaráætlun** skal keyra vinnsluna **1110** (altæka skilgreiningu) til að dreifa eiginleikabreytingunni.

## <a name="configure-return-policy"></a>Stilla skilareglu

Fylgdu þessum skrefum til að stilla aftur stefnu fyrir smásöluverslun eða netverslun.

1. Farðu í **Verslun og verslun** \> **Uppsetning rásar** \> **Skilar** \> **Skilastefna rásarinnar**.

1. Veldu **Nýtt** til að búa til nýtt sniðmát skilareglu. Veldu sniðmátið í vinstri glugganum til að nota sniðmát sem fyrir er. Fyrir ný sniðmát skaltu bæta við nafni og lýsingu sem mun hjálpa þér að bera kennsl á stefnuna þegar henni er beitt á rásina.

   ![Bættu við nýrri skilareglu.](media/Return-policy-page1.png)
     
   
1. Í kaflanum **Leyfðar endurgreiðsluaðferðir**, skilgreina **Leyft** greiðslutilboðum skila sem eru sértæk fyrir hverja greiðslumáta.
   ![Stilla leyfða greiðslumáta fyrir hverja greiðslugerð.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Greiðslumátarnir eru fengnir af þeim greiðslumáta sem settur er fyrir stofnunina.
    > - Með því að bæta við leyfðri útboðsgerð fyrir hverja skráða greiðslumáta verður tryggt að hægt sé að skila í leyfilega gerð útboðs.
    
1. Tengdu sniðmát skilareglu við verslanirnar þar sem það verður notað. Veldu **Bæta við** á flipann **Smásölurásir** og tengdu tiltækar rásir. 

    - Í glugganum **Velja fyrirtækjahnúta** velurðu verslanir, svæði og fyrirtæki sem sniðmátið ætti að vera tengt við.
    - Aðeins er hægt að tengja eitt sniðmát skilareglu við hverja verslun.
    - Notaðu örvahnappana til að velja verslanir, svæði eða fyrirtæki.
    - Gildistaka stefnunnar verður sá dagur sem stefnunum er beitt á rásirnar og rásastörfin eru keyrð. 

    ![Svarglugginn Veljið fyrirtækjahnúta.](media/Return-policy-page3.png)

1. Á síðunni **Dreifingaráætlun**, keyrðu **1070** vinnslu til að gera skilaregluna á rásinni tiltæka fyrir POS.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Forskoðaðu aftur skilareglu rásarinnar í POS

Fylgdu skrefunum í báðum eftirfarandi dæmum til að skoða leyfðar gerðir tilboða í POS.

1. Skráðu þig inn í POS sem gjaldkera eða stjórnandi.
1. Undir **Vakt og skúffa**, veldu **Sýna færslubók**.
1. Veldu færslu sem er hluti af skilunum. 
1. Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.  
    - Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.
    - Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.
    - Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.

-eða-

1. Skráðu þig inn í POS sem gjaldkera eða stjórnandi.
1. Veldu **Skilafærsla** og sláðu inn kvittunarauðkenni með strikamerkjaskönnun eða með handvirkri færslu. 
1. Veldu færslu sem er hluti af skilunum. 
1. Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.  
    - Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.
    - Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.
    - Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.

![Gerð endurgreiðslu ekki leyfð.](media/Return-policy-page6.png)



![Gerðir endurgreiðslu leyfðar.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Stuðningur skattaeiginleika fyrir flutningspantanir
description: Þetta efnisatriði útskýrir nýjan stuðning skattaeiginleika fyrir flutningspantanir með því að nota skattaútreikningsþjónustuna.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d1b99046b0e439c9dadbb240050e270a7b2a6914
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920956"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Stuðningur skattaeiginleika fyrir flutningspantanir

[!include [banner](../../includes/banner.md)]

Þetta efni inniheldur upplýsingar um samþættingu skattaútreiknings og bókunar í flutningspöntunum. Þessi virkni gerir kleift að setja upp skattaútreikning og bókun í flutningspöntunum fyrir birgðaflutninga. Samkvæmt VSK-reglugerðum Evrópusambandsins er litið á birgðaflutninga sem framboð og kaup innan sambandsins.

Til að grunnstilla og nota þessa virkni þarf að ljúka þremur meginskrefum:

1. **RCS-uppsetning:** í Regulatory Configuration Service skal setja upp skattaeiginleika, skattkóða og gildissvið skattkóða fyrir ákvörðun skattkóða í flutningspöntunum.
2. **Fjárhagsuppsetning:** Í Microsoft Dynamics 365 Finance skal kveikja á eiginleikanum **Skattar í flutningspöntun**, setja upp færibreytur skattþjónustu fyrir birgðir og setja upp grunnfæribreytur skatts.
3. **Uppsetning birgða:** Setjið upp skilgreiningu birgða fyrir færslur flutningspöntunar.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Setja upp RCS fyrir skattfærslur og færslur flutningspöntunar

Fylgið þessum skrefum til að setja upp skattinn sem tengist flutningspöntun. Í dæminu sem er sýnt hér er flutningspöntunin frá Hollandi og Belgíu.

1. Á síðunni **Skattaeiginleikar**, í flipanum **Útgáfur**, skal velja drög að eiginleikaútgáfu og síðan velja **Breyta**.

    ![Breyta valið](../media/image1.png)

2. Á síðunni **Uppsetning skattaeiginleika**, í flipanum **Skattkóðar**, skal velja **Bæta við** til að stofna nýja skattkóða. Fyrir þetta dæmi eru þrír skattkóðar stofnaður: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.

    - Þegar flutningspöntun er send úr vöruhúsi í Hollandi er notaður skattkóði fyrir undanskilinn virðisaukaskatt Hollands (**NL-Exempt**).
      
        Búið til skattkóðann **NL-Exempt**.
        1. Veljið **Bæta við**, sláið inn **NL-Exempt** í reitinn **Skattkóði**.
        2. Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.
        3. Veljið **Vista**.
        4. Veljið **Bæta við** í töflunni **Taxti**.
        5. Skiptið **Er undanskilið** í **Já** í hlutanum **Almennt**.

        ![Skattkóði NL-Exempt](../media/image2.png)

    - Þegar flutningspöntun er móttekin í belgísku vöruhúsi er leið bakfærðs gjalds notað með því að nota skattkóðana **BE-RC-21** og **BE-RC+21**.
        
        Búið til skattkóðann **BE-RC-21**.      
        1. Veljið **Bæta við**, sláið inn **BE-RC-21** í reitinn **Skattkóði**.
        2. Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.
        3. Veljið **Vista**.
        4. Veljið **Bæta við** í töflunni **Taxti**.
        5. Sláið inn **-21** í reitinn **Skatthlutfall**.
        6. Skiptið **Er bakfært gjald** í **Já** í hlutanum **Almennt**.
        7. Veljið **Vista**.

        ![BE-RC-21 skattkóði fyrir bakfærð gjöld](../media/image3.png)
        
        Búið til skattkóðann **BE-RC+21**.
        1. Veljið **Bæta við**, sláið inn **BE-RC-21** í reitinn **Skattkóði**.
        2. Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.
        3. Veljið **Vista**.
        4. Veljið **Bæta við** í töflunni **Taxti**.
        5. Sláið inn **21** í reitinn **Skatthlutfall**.
        6. Veljið **Vista**.

        ![BE-RC+21 skattkóði fyrir bakfærð gjöld](../media/image4.png)

3. Skilgreinið gildissvið skattkóðanna.

    1. Veljið **Stjórna dálkum** og veljið síðan dálka sem á að nota til að búa til töflu gildissviðs.

        > [!NOTE]
        > Gangið úr skugga um að bæta dálkunum **Viðskiptaferli** og **Skattstefnur** við töfluna. Báðir dálkarnir eru nauðsynlegir fyrir virknina fyrir skatt í flutningspöntunum.

    2. Bætið við gildissviðsreglum. Ekki skilja reitina **Skattkóðar**, **Skattflokkur** og **Vöruskattflokkur** eftir auða.
        
        Bæta við nýrri reglu fyrir sendingu flutningspöntunar.
        1. Veljið **Bæta við** í töflunni **Gildissviðsreglur**.
        2. Í reitnum **Viðskiptaferli** skal velja **Birgðir** til að reglan gildi um flutningspöntun.
        3. Í reitinn **Senda frá landi/svæði** skal færa inn **NLD**.
        4. Í reitinn **Senda til lands/svæðis** skal færa inn **BEL**.
        5. Í reitnum **Skattstefnan** skal velja **Úttak** til að reglan gildi um sendingu flutningspöntunar.
        6. Í reitnum **Skattkóðar** skal velja **NL-Exempt**.
        7. Í reitinn **Skattflokkur** og **VSK-flokkur vöru** skal færa inn viðeigandi VSK-flokk og VSK-flokk vöru sem eru skilgreindir í kerfi Finance.
        
        Bætið við annarri reglu fyrir móttöku flutningspöntunar.
        1. Veljið **Bæta við** í töflunni **Gildissviðsreglur**.
        2. Í reitnum **Viðskiptaferli** skal velja **Birgðir** til að reglan gildi um flutningspöntun.
        3. Í reitinn **Senda frá landi/svæði** skal færa inn **NLD**.
        4. Í reitinn **Senda til lands/svæðis** skal færa inn **BEL**.
        5. Í reitnum **Skattstefnan** skal velja **Inntak** til að reglan gildi um móttöku flutningspöntunar.
        6. Í reitnum **Skattkóðar** skal velja **BE-RC+21** og **BE-RC-21**.
        7. Í reitinn **Skattflokkur** og **VSK-flokkur vöru** skal færa inn viðeigandi VSK-flokk og VSK-flokk vöru sem eru skilgreindir í kerfi Finance.

        ![Gildissviðsreglur](../media/image5.png)

4. Ljúka og birta nýja útgáfu nýs skattaeiginleika.

    [![Stöðu nýju útgáfunnar breytt](../media/image6.png)](../media/image6.png)

## <a name="set-up-finance-for-transfer-order-transactions"></a>Setja upp Finance fyrir færslur flutningspöntunar

Fylgið þessum skrefum til að virkja og setja upp skatta fyrir flutningspantanir.

1. Í Finance skal opna **Vinnusvæði** \> **Eiginleikastjórnun**.
2. Í listanum skal finna og velja eiginleikann **Skattar í flutningspöntun** og síðan velja **Virkja núna** til að kveikja á honum.

    > [!IMPORTANT]
    > Eiginleikinn **Skattur í flutningspöntun** er algjörlega háður skattþjónustunni. Þess vegna er aðeins hægt að kveikja á honum þegar búið er að setja upp skattþjónustuna.

    ![Skattur í flutningspöntunareiginleika](../media/image7.png)

3. Virkið skattþjónustuna og veljið viðskiptaferlið **Birgðir**.

    > [!IMPORTANT]
    > Ljúka þarf þessu skrefi fyrir hvern lögaðila í Finance þar sem skattþjónustan og virknin fyrir skatt í flutningspöntunum eiga að vera tiltækar.

    1. Farið í **Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Uppsetning skattþjónustu**.
    2. Í reitnum **Viðskiptaferli** skal velja **Birgðir**.

    ![Reitur viðskiptaferlis stilltur](../media/image8.png)

4. Gangið úr skugga um að leið bakfærðs gjalds sé uppsett. Farið í **Fjárhagur** \> **Uppsetning** \> **Færibreytur** og síðan, í flipanum **Bakfært gjald**, skal staðfesta að valkosturinn **Virkja bakfært gjald** sé stilltur á **Já**.

    ![Virkja valkost bakfærðra gjalda](../media/image9.png)

5. Gangið úr skugga um að tengdir skattkóðar, skattflokkar, skattflokkar vöru og skráningarnúmer virðisaukaskatts hafi verið sett upp í Finance samkvæmt leiðsögn skattþjónustunnar.
6. Setja upp bráðabirgðareikning flutnings. Þetta þrep er aðeins áskilið þegar skatturinn sem er notaður í flutningspöntun á ekki við um leið skattundanþágu eða bakfærðs gjalds.

    1. Opnið **Skattur** \> **Uppsetning** \> **Söluskattur** \> **Fjárhagsbókunarflokkar**.
    2. Í reitnum **Bráðabirgðaflutningur** skal velja fjárhagslykil.

    ![Bráðabirgðareikningur flutnings valinn](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Setja upp grunnbirgðir fyrir færslur flutningspöntunar

Fylgið þessum skrefum til að setja upp grunnbirgðir til að virkja færslur flutningspöntunar.

1. Búið til senda-til og senda-frá svæði fyrir vöruhúsin í mismunandi löndum eða svæðum og bætið við aðalaðsetrinu fyrir hvert svæði.

    1. Farðu í **Vöruhúsakerfi** \> **Setja upp** \> **Vöruhús** \> **Svæði**.
    2. Veljið **Nýtt** til að búa til nýtt svæði sem verður úthlutað á vöruhúsið síðar.
    3. Endurtakið skref 2 fyrir öll önnur svæði sem þarf að búa til.

    > [!NOTE]
    > Eitt svæðanna sem var búið til ætti að kalla **Flutningur**. Í síðari skrefum þessa ferlis verður þessu svæði úthlutað á flutningsvöruhúsið þannig að hægt sé að bóka skatttengd fylgiskjöl birgða í „senda“ og „móttaka“ færslum fyrir flutningspantanir. Aðsetur flutningasvæðis tengist ekki skattaútreikningum. Þess vegna er hægt að skilja hann eftir auðan.

    ![Uppsetning svæða](../media/image11.png)

2. Búið til vöruhús fyrir senda-til, flutning og senda-til. Allar upplýsingar um aðsetur sem er viðhaldið í vöruhúsi munu hnekkja aðsetri svæðis í skattaútreikningum.

    1. Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Vöruhús** \> **Vöruhús**.
    2. Veljið **Nýtt** til að stofna vöruhús og úthluta því á samsvarandi svæði.
    3. Endurtakið skref 2 til að búa til vöruhús fyrir hvert svæði eftir þörfum.

    ![Setja upp vöruhús](../media/image12.png)

    > [!NOTE]
    > Fyrir senda-til vöruhús þarf að velja flutningsvöruhús í reitnum **Flutningsvöruhús** fyrir færslur flutningspöntunar.
    >
    > ![Val á flutningsvöruhúsi](../media/image13.png)

3. Gangið úr skugga um að skilgreining birgðabókunar sé sett upp fyrir færslur flutningspöntunar.

    1. Opnið **Birgðastjórnun** \> **Uppsetning** \> **Bókun** \> **Bókun**.
    2. Í flipanum **Birgðir** skal ganga úr skugga um að fjárhagslykill sé settur upp fyrri bæði bókanir á **Úthreyfingu birgða** og **Innhreyfingu birgða**.

        ![Uppsetning á bókun innhreyfinga og úthreyfinga birgða](../media/image14.png)

    3. Gangið úr skugga um að fjárhagslykillinn sé settur upp fyrir bókun á **Millieining, lánardrottnar**.

        ![Bókun millieiningar lánardrottins sett upp](../media/image15.png)

    4. Gangið úr skugga um að fjárhagslykillinn sé settur upp fyrir bókun á **Millieining, viðskiptavinir**.

        ![Bókun millieiningar viðskiptavinar sett upp](../media/image16.png)

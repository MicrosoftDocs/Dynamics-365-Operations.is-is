---
title: Skattaeiginleikaþjónusta fyrir flutningspantanir
description: Þessi grein útskýrir nýjan stuðning skattaeiginleika fyrir flutningspantanir með því að nota skattaútreikningsþjónustuna.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c55d0891ed37d63f89ee09759965ac443db20dc6
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542245"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Skattaeiginleikaþjónusta fyrir flutningspantanir

[!include [banner](../../includes/banner.md)]

Þessi grein inniheldur upplýsingar um samþættingu skattaútreiknings og bókunar í flutningspöntunum. Þessi virkni gerir kleift að setja upp skattaútreikning og bókun í flutningspöntunum fyrir birgðaflutninga. Samkvæmt VSK-reglugerðum Evrópusambandsins er litið á birgðaflutninga sem framboð og kaup innan sambandsins.

Til að grunnstilla og nota þessa virkni þarf að ljúka þremur meginskrefum:

1. **RCS-uppsetning:** í Regulatory Configuration Service skal setja upp skattaeiginleika, skattkóða og gildissvið skattkóða fyrir ákvörðun skattkóða í flutningspöntunum.
2. **Uppsetning Dynamics 365 Finance:** Í Finance skal kveikja á eiginleikanum **Skattur í flutningspöntun**, setja upp færibreytur skattaútreikningsþjónustu fyrir birgðir og setja upp grunnfæribreytur skatts.
3. **Uppsetning birgða:** Setjið upp skilgreiningu birgða fyrir færslur flutningspöntunar.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Setja upp RCS fyrir skattfærslur og færslur flutningspöntunar

Fylgið þessum skrefum til að setja upp skattinn sem tengist flutningspöntun. Í dæminu sem er sýnt hér er flutningspöntunin frá Hollandi og Belgíu.

1. Á síðunni **Skattaeiginleikar**, í flipanum **Útgáfur**, skal velja drög að eiginleikaútgáfu og síðan velja **Breyta**.

2. Á síðunni **Uppsetning skattaeiginleika**, í flipanum **Skattkóðar**, skal velja **Bæta við** til að stofna nýja skattkóða. Fyrir þetta dæmi eru þrír skattkóðar stofnaður: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.

    - Þegar flutningspöntun er send úr vöruhúsi í Hollandi er notaður skattkóði fyrir undanskilinn virðisaukaskatt Hollands (**NL-Exempt**).
      
        Búið til skattkóðann **NL-Exempt**.
        1. Veljið **Bæta við**, sláið inn **NL-Exempt** í reitinn **Skattkóði**.
        2. Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.
        3. Veldu **Vista**.
        4. Veljið **Bæta við** í töflunni **Taxti**.
        5. Stillið **Er undanskilið** á **Já** í hlutanum **Almennt**.
        6. Í reitinn **Undanþágukóði** skal slá inn **EB**.

    - Þegar flutningspöntun er móttekin í belgísku vöruhúsi er leið bakfærðs gjalds notað með því að nota skattkóðana **BE-RC-21** og **BE-RC+21**.
        
        Búið til skattkóðann **BE-RC-21**.      
        1. Veljið **Bæta við**, sláið inn **BE-RC-21** í reitinn **Skattkóði**.
        2. Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.
        3. Veljið **Vista**.
        4. Veljið **Bæta við** í töflunni **Taxti**.
        5. Sláið inn **-21** í reitinn **Skatthlutfall**.
        6. Stillið **Er bakfært gjald** á **Já** í hlutanum **Almennt**.
        7. Veldu **Vista**.
        
        Búið til skattkóðann **BE-RC+21**.
        1. Veljið **Bæta við**, sláið inn **BE-RC+21** í reitinn **Skattkóði**.
        2. Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.
        3. Veljið **Vista**.
        4. Veljið **Bæta við** í töflunni **Taxti**.
        5. Sláið inn **21** í reitinn **Skatthlutfall**.
        6. Veldu **Vista**.

3. Skilgreindu skattflokkinn.
    1. Veldu **Stjórna dálkum** og veldu síðan línureitinn **Skattflokkur**.
    2. Veldu **->** og veldu síðan **Í lagi**.
    3. Smelltu á **Bæta við** til að bæta við skattflokki.
    4. Í dálkinn **Skattflokkur** skal færa inn **AR-EU** og síðan velja skattkóðann **NL-Exempt**.
    5. Smelltu á **Bæta við** til að bæta við skattflokki.
    6. Í dálkinn **Skattflokkur** skal færa inn **RC-VAT** og síðan velja skattkóðana **BE-RC-21** og **BE-RC+21**.
4. Skilgreindu skattflokk vöru.
    1. Veldu **Stjórna dálkum** og veldu síðan línureitinn **Skattflokkur vöru**.
    2. Veldu **->** og veldu síðan **Í lagi**.
    3. Veldu **Bæta við** til að bæta við skattflokki vöru.
    4. Sláðu inn **FULL** í dálkinn **Skattflokkur vöru**. Veldu skattkóðana **BE-RC-21**, **BE-RC+21** og **NL-Exempt**.
5. Skilgreindu gildissvið skattflokksins.

    1. Veljið **Stjórna dálkum** og veljið síðan dálka sem á að nota til að búa til töflu gildissviðs.

        > [!NOTE]
        > Gangið úr skugga um að bæta dálkunum **Viðskiptaferli** og **Skattstefnur** við töfluna. Báðir dálkarnir eru nauðsynlegir fyrir virknina fyrir skatt í flutningspöntunum.

    2. Bætið við gildissviðsreglum. Ekki skilja reitinn **Skattflokkur** eftir auðan.
        
        Bæta við nýrri reglu fyrir sendingu flutningspöntunar.
        1. Veljið **Bæta við** í töflunni **Gildissviðsreglur**.
        2. Í reitnum **Viðskiptaferli** skal velja **Birgðir** til að reglan gildi um flutningspöntun.
        3. Í reitinn **Senda frá landi/svæði** skal færa inn **NLD**.
        4. Í reitinn **Senda til lands/svæðis** skal færa inn **BEL**.
        5. Í reitnum **Skattstefnan** skal velja **Úttak** til að reglan gildi um sendingu flutningspöntunar.
        6. Í reitnum **Skattflokkur** skal velja **AR-EU**.
        
        Bætið við annarri reglu fyrir móttöku flutningspöntunar.
        
        1. Veljið **Bæta við** í töflunni **Gildissviðsreglur**.
        2. Í reitnum **Viðskiptaferli** skal velja **Birgðir** til að reglan gildi um flutningspöntun.
        3. Í reitinn **Senda frá landi/svæði** skal færa inn **NLD**.
        4. Í reitinn **Senda til lands/svæðis** skal færa inn **BEL**.
        5. Í reitnum **Skattstefnan** skal velja **Inntak** til að reglan gildi um móttöku flutningspöntunar.
        6. Í reitnum **Skattflokkur** skal velja **RC-VAT**.

6. Skilgreindu gildissvið fyrir skattflokk vöru.

    1. Veljið **Stjórna dálkum** og veljið síðan dálka sem á að nota til að búa til töflu gildissviðs.
    2. Bætið við gildissviðsreglum.
        
       > [!NOTE]
       > Ef VSK-flokkur vöru sem er sjálfgefinn á línum skattskylts skjals er þegar réttur skal hafa þetta autt. 
        
        Bættu nýrri reglu við fyrir sendingu og móttöku flutningspöntunar.
        1. Á síðunni **Gildissviðsreglur** skal velja **Bæta við**.
        2. Í reitnum **Viðskiptaferli** skal velja **Birgðir** til að reglan gildi um flutningspöntun.
        3. Í reitnum **VSK-flokkur vöru** skal velja **FULL**.
7. Ljúka og birta nýja útgáfu nýs skattaeiginleika.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Setja upp Finance fyrir færslur flutningspöntunar

Fylgið þessum skrefum til að virkja og setja upp skatta fyrir flutningspantanir.

1. Í Finance skal opna **Vinnusvæði** > **Eiginleikastjórnun**.
2. Í listanum skal finna og velja eiginleikann **Skattar í flutningspöntun** og síðan velja **Virkja núna** til að kveikja á honum.

    > [!IMPORTANT]
    > Eiginleikinn **Skattur í flutningspöntun** er algjörlega háður skattreikningsþjónustunni. Þess vegna er aðeins hægt að kveikja á honum þegar búið er að setja upp skattreikningsþjónustuna.

    ![Eiginleiki skatts í flutningspöntun.](../media/image7.png)

3. Virkjaðu skattaútreikningsþjónustuna og veldu viðskiptaferlið **Birgðir**.

    > [!IMPORTANT]
    > Ljúka þarf þessu skrefi fyrir hvern lögaðila í Finance þar sem skattreikningsþjónustan og virknin fyrir skatt í flutningspöntunum eiga að vera tiltækar.

    1. Opnið **Skattur** > **Uppsetning** > **Skattaskilgreining** > **Færibreytur skattaútreiknings**.
    2. Í reitnum **Viðskiptaferli** skal velja **Birgðir**.

4. Gangið úr skugga um að leið bakfærðs gjalds sé uppsett. Farið í **Fjárhagur** \> **Uppsetning** \> **Færibreytur** og síðan, í flipanum **Bakfært gjald**, skal staðfesta að valkosturinn **Virkja bakfært gjald** sé stilltur á **Já**.

    ![Virkja valkost bakfærðra gjalda.](../media/image9.png)

5. Gangið úr skugga um að tengdir skattkóðar, skattflokkar, skattflokkar vöru og skráningarnúmer virðisaukaskatts hafi verið sett upp í Finance samkvæmt leiðsögn skattreikningsþjónustunnar.
6. Setja upp bráðabirgðareikning flutnings. Þetta þrep er aðeins áskilið þegar skatturinn sem er notaður í flutningspöntun á ekki við um leið skattundanþágu eða bakfærðs gjalds.

    1. Opnið **Skattur** > **Uppsetning** > **Söluskattur** > **Fjárhagsbókunarflokkar**.
    2. Í reitnum **Bráðabirgðaflutningur** skal velja fjárhagslykil.

       ![Bráðabirgðareikningur flutnings valinn.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Setja upp grunnbirgðir fyrir færslur flutningspöntunar

Fylgið þessum skrefum til að setja upp grunnbirgðir til að virkja færslur flutningspöntunar.

1. Búið til senda-til og senda-frá svæði fyrir vöruhúsin í mismunandi löndum eða svæðum og bætið við aðalaðsetrinu fyrir hvert svæði.

    1. Farðu í **Warehouse management** > **Setja upp** > **Vöruhús** > **Svæði**.
    2. Veljið **Nýtt** til að búa til nýtt svæði sem verður úthlutað á vöruhúsið síðar.
    3. Endurtakið skref 2 fyrir öll önnur svæði sem þarf að búa til.

    > [!NOTE]
    > Eitt svæðanna sem var búið til ætti að kalla **Flutningur**. Í síðari skrefum þessa ferlis verður þessu svæði úthlutað á flutningsvöruhúsið þannig að hægt sé að bóka skatttengd fylgiskjöl birgða í „senda“ og „móttaka“ færslum fyrir flutningspantanir. Aðsetur flutningasvæðis tengist ekki skattaútreikningum. Þess vegna er hægt að skilja hann eftir auðan.

    ![Uppsetning svæða.](../media/image11.png)

2. Búið til vöruhús fyrir senda-til, flutning og senda-til. Allar upplýsingar um aðsetur sem er viðhaldið í vöruhúsi munu hnekkja aðsetri svæðis í skattaútreikningum.

    1. Farðu í **Vöruhúsakerfi** > **Uppsetning** > **Vöruhús** > **Vöruhús**.
    2. Veljið **Nýtt** til að stofna vöruhús og úthluta því á samsvarandi svæði.
    3. Endurtakið skref 2 til að búa til vöruhús fyrir hvert svæði eftir þörfum.

       ![Setja upp vöruhús.](../media/image12.png)

    > [!NOTE]
    > Fyrir senda-til vöruhús þarf að velja flutningsvöruhús í reitnum **Flutningsvöruhús** fyrir færslur flutningspöntunar.
    >
    > ![Val á flutningsvöruhúsi.](../media/image13.png)

3. Gangið úr skugga um að skilgreining birgðabókunar sé sett upp fyrir færslur flutningspöntunar.

    1. Opnið **Birgðastjórnun** > **Uppsetning** > **Bókun** > **Bókun**.
    2. Í flipanum **Birgðir** skal ganga úr skugga um að fjárhagslykill sé settur upp fyrri bæði bókanir á **Úthreyfingu birgða** og **Innhreyfingu birgða**.

        ![Uppsetning á bókun innhreyfinga og úthreyfinga birgða.](../media/image14.png)

    3. Gangið úr skugga um að fjárhagslykillinn sé settur upp fyrir bókun á **Millieining, lánardrottnar**.

        ![Bókun millieiningar lánardrottins sett upp.](../media/image15.png)

    4. Gangið úr skugga um að fjárhagslykillinn sé settur upp fyrir bókun á **Millieining, viðskiptavinir**.

        ![Bókun millieiningar viðskiptavinar sett upp.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]

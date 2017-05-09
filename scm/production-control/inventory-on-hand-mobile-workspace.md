---
title: "Vinnusvæði samstarfs lánardrottna fyrir fartæki fyrir forritið Microsoft Dynamics 365 for Operations"
description: "Fartækjavinnusvæði birgða á lager hjálpar þér að fá yfirsýn gegnum fartæki yfir pantaðar og tiltækar birgðir, hvar og hvenær sem er."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Vinnusvæði samstarfs lánardrottna fyrir fartæki fyrir forritið Microsoft Dynamics 365 for Operations

Fartækjavinnusvæði birgða á lager hjálpar þér að fá yfirsýn gegnum fartæki yfir pantaðar og tiltækar birgðir, hvar og hvenær sem er. 

<a name="prerequisites"></a>Forkröfur
-------------

| Skilyrði                                                         | lýsing                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesa um Microsoft Dynamics 365 for Operations verkvang | [Microsoft Dynamics 365 for Operations verkvangur](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Vertu viss um að þú sért að nota umhverfi sem er með Microsoft Dynamics 365 for Operations útgáfu 1611 og uppfærslu verkvangs Microsoft Dynamics for Operations 3 (nóvember 2016). |
| Bráðabót KB 3215650                                                    | Setja upp bráðabót til að virkja vinnusvæðin sem veitt eru í Microsoft Dynamics 365 for Operations.                                       |
| Lýsingarlína fartækis með forritið Dynamics 365 for Operations uppsett | Sækja forritið Dynamics 365 for Operations úr forritaverslun fartækis.                                                                           |

## <a name="introduction"></a>Inngangur
Yfirleitt eru fyrirtæki með margar sendingar og margar vörumóttökur á degi hverjum. Slíkar hreyfingar breyta birgðastöðu á lager sífellt. Fartækjavinnusvæðið Birgðastaða á lager gerir þér kleift að sjá birgðastöðu á lager þvert á fyrirtæki og fá nýjasta yfirlit yfir birgðastöðugögn á fartækinu sem þú vilt helst nota. Hvort sem þú vinnur í vöruhúsi, í innkaupum, sölu, framleiðslu eða stjórnun eða hefur önnur hlutverk getur þú fengið yfirlit yfir birgðastöðu á lager hvar og hvenær sem er. Farsímavinnusvæðið veitir skjótt yfirlit birgðastöðu á  lager þvert á fyrirtæki og yfirlit yfir birgðastöðu á lager þvert á fyrritæki, núverandi efnislegar frátektir og óbókaðar birgðir á lager. Þú getur einnig fært inn vörunúmer til að spyrjast fyrir um birgðastöðu á lager og framkvæmt síaða leit að afurðum eða tilbrigðum eftir birgðastöðu á lager. Fartækjavinnusvæði tryggir einkum eftirfarandi eiginleika:

-   Leit eftir vörunúmeri eða vöruheiti til að finna afurðir til að skoða birgðastöðu á lager fyrir þær vörur.
-   Hægt er að skoða eftirfarandi upplýsingar fyrir valdar vörur:
    -   Birgðastaða á lager eftir svæðum
    -   Birgðastaða á lager eftir vöruhúsum
    -   Birgðastaða á lager eftir staðsetningu
    -   Birgðastaða á lager eftir runum (fyrir runustýrðar vörur)
    -   Birgðastaða á lager eftir birgðastöðu

<!-- -->

-   Birgðastaða á lager fyrir vörur er sýnd með eftirfarandi hætti:
    -   Eftir efnislegum birgðum (Þetta yfirlit táknar heildarmagn).
    -   Eftir efnislegum frátektum (Þetta yfirlit táknar frátekið magn).
    -   Eftir efnislegu vörum sem eru tiltækar (þetta yfirlit táknar tiltækt magn sem ekki er bókað).

## <a name="get-started"></a>Hefjast handa
Til að hefjast handa í fartækinu þínu:

1.  Sæktu forritið Microsoft Dynamics 365 for Operations úr forritaverslun farsímans og settu það upp.
2.  Ræstu forritið í snjallsímanum.
3.  Færðu inn vefslóð þína fyrir Dynamics 365.
4.  Skráðu fyrirtækið sem á að skrá sig inn á . Til dæmis: Færið inn **USMF**.
5.  Fyrsta skipti sem þú skráir þig inn verðurðu beðin um notandanafn og aðgangsorð fyrir þinn Microsoft Dynamics 365 for Operations reikning. Færðu inn skilríki Eftir að þú skrá inn, sérðu tiltækt vinnusvæði fyrir Þitt fyrirtæki.

Til að skoða vinnusvæði í farsímaforritinu verður fyrst að gefa út æskileg vinnusvæði í forritið Dynamics 365 for Operations.

1.  Ræstu Dynamics 365 for Operations.
2.  Opnaðu **Kerfisstjórnun** &gt; **Uppsetning** &gt; **kerfisfæribreytur**.
3.  Veldu **Stjórna fartækjaforriti**.
4.  Velja vinnusvæðið til að birta í verkvangi farsíma.
5.  Veldu **Birta vinnusvæði**.
6.  Endurhlaða Þitt tæki til að sjá útgefin vinnusvæði.

## <a name="view-the-onhand-inventory-for-a-product"></a>Veldu tiltækar birgðir á lager fyrir vöru
1.  Í farsímanum velurðu vinnusvæðið ** birgðir á lager**.
2.  Veldu **Kanna birgðir á lager fyrir vöru**. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Frekari upplýsingar eru í handbókinni.
3.  Ef þitt atriði er ekki á listanum skal velja **Leita áfram** til að framkvæma leit á netinu í  Dynamics 365 for Operations. Leitaðu eftir vörunúmeri eða skiptu í leit eftir vöruheiti.
4.  Veljið afurð. Ef mynd fylgir vörunni er myndin sýnd.
5.  Veldu einn af eftirfarandi valkostum til að skoða birgðastöðu á lager:
    -   Skoða birgðastöðu á lager eftir svæði
    -   Skoða birgðastöðu á lager eftir vöruhúsi
    -   Skoða birgðastöðu á lager eftir staðsetningu
    -   Birgðastaða á lager eftir runum (fyrir runustýrðar vörur)
    -   Skoða birgðastöðu á lager eftir stöðu birgða

    Birgðastaða á lager fyrir vörur er sýnd með eftirfarandi hætti:
    -   Eftir efnislegum birgðum (Þetta yfirlit táknar heildarmagn).
    -   Eftir efnislegum frátektum (Þetta yfirlit táknar frátekið magn).
    -   Eftir efnislegu vörum sem eru tiltækar (þetta yfirlit táknar tiltækt magn sem ekki er bókað).





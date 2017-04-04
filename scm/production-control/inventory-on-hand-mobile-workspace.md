---
title: "Birgðir á lager fartæki vinnusvæði fyrir Microsoft Dynamics 365 Aðgerðir forrits"
description: "Birgðir á lager vinnusvæði fartæki hjálpar innsýn fartæki í birgðir, frátekna og tiltæka hvar og gerir."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Birgðir á lager fartæki vinnusvæði fyrir Microsoft Dynamics 365 Aðgerðir forrits

Birgðir á lager vinnusvæði fartæki hjálpar innsýn fartæki í birgðir, frátekna og tiltæka hvar og gerir. 

<a name="prerequisites"></a>Forkröfur
-------------

| Skilyrði                                                         | lýsing                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesa um Microsoft Dynamics 365 fyrir fartæki svæðis Aðgerðir | [Dynamics 365 fyrir fartæki svæðis Aðgerðir](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 fyrir Aðgerðir                                          | Í umhverfi með Microsoft Dynamics 365 Aðgerðir útgáfu 1611 og Microsoft Dynamics fyrir Aðgerðir svæðis uppfæra 3 (Nóvember 2016) |
| Bráðabót KB 3215650                                                    | Setja upp bráðabót til að virkja vinnusvæðin sem eru gefnir í skal Microsoft Dynamics 365 fyrir Aðgerðir.                                       |
| Lýsingarlína fartækis með Dynamics 365 fyrir Aðgerðir forrits uppsett | Sækja Dynamics 365 fyrir Aðgerðir forrits úr verslunin fartæki forrits.                                                                           |

## <a name="introduction"></a>Inngangur
Yfirleitt, fyrirtæki hafa margar sendingar og margar innhreyfingar á birgðum hverjum degi. Þessar hreyfingar constantly breyta birgðastöðu á lager. Birgðir á lager vinnusvæði fartæki gerir það mögulegt að sjá stöðu fyrirtækja lagerbirgðir, þannig að hægt innsýn í síðustu í birgðum gögn í fartækinu vali. Óháð því hvort að vinna í vöruhús, innkaup, sölu, framleiðslu eða stjórnun, eða með annað hlutverk, er hægt að nálgast gögn lagerbirgðir gerir og hvar. Fartæki vinnusvæði veitir snatri yfirlit yfir stöðu á lager milli aðstöðu, og gerir þér kleift að skoða lagerbirgðir fyrir aðstöðu, efni gildandi frátekningar og ófrátekið birgðir á lager. Einnig er hægt inn vörunúmer á fyrirspurn birgðir á lager, og framkvæma leit síaðar afurðir á lager eða vöruvíddasamsetningar. Sérstaklega fartæki vinnusvæði veitir þessar aðgerðir:

-   Hægt er að leita eftir afurðarnúmer eða afurðarheiti til að finna afurðir sem á að skoða birgðastöðu á lager fyrir.
-   Fyrir valdar afurðir, hægt er að skoða eftirfarandi upplýsingar:
    -   Birgðir á lager fyrir hvert vefsvæði
    -   Lagerbirgðir á hvert vöruhús
    -   Birgðir á lager eftir staðsetningu
    -   Birgðir á lager fyrir hverja runu (fyrir runustýrðu afurðir)
    -   Birgðir á lager eftir birgðastöðu

<!-- -->

-   Afurð á lager birtist á eftirfarandi hátt:
    -   Með efnislegum birgðum (Þetta yfirlit sýnir heildarupphæð.)
    -   Eftir efnislegt magn frátekið (Þetta yfirlit sýnir frátekið upphæð.)
    -   Eftir tiltækt efnislegt magn (skoða stendur fyrir tiltækar upphæðin sem hefur ekkert frátekningar.)

## <a name="get-started"></a>Hefjast handa
Til að byrja á því fartækis:

1.  Sækja og setja upp Microsoft Dynamics 365 fyrir aðgerðir forrits úr verslunin fartæki forrits.
2.  Byrja forritið þitt tækis.
3.  Færið inn Vefslóð skal Dynamics 365.
4.  Færið inn fyrirtæki að skrá sig inn á. Til dæmis inn **USMF**.
5.  Í fyrsta sinn sem þú skráir þig inn, verið beðið um notandanafn og aðgangsorð fyrir notanda Microsoft Dynamics 365 fyrir Aðgerðir. Færið inn skilríkjum þínum. Eftir að skrá er að sjá tiltækar vinnusvæða fyrirtækisins.

Til að skoða vinnusvæða fartæki forritið, er verður fyrst að birta skal vinnusvæðin sem óskað er eftir að Dynamics 365 fyrir Aðgerðir forrits.

1.  Ræsa Dynamics 365 aðgerða.
2.  Fara í **kerfisstjórnun**&gt;**Uppsetningu**&gt;**kerfisfæribreytum**.
3.  Veljið **Stjórna fartæki forrits**.
4.  Veljið vinnusvæði til að birta í fartæki svæðis.
5.  Velja **Birta vinnusvæði**.
6.  Endurnýja skal tæki til að sjá birt vinnusvæði.

## <a name="view-the-onhand-inventory-for-a-product"></a>Skoða birgðir onhand afurðar
1.  Fartækis, veljið þá **Birgðir á lager** vinnusvæði.
2.  Velja **Athuga á lager fyrir vöru**. Er að sjá lista yfir afurðir sem hlaðið inn í forritið fyrir notkun ótengdur. Sjálfgefið 50 vörur eru hlaðnar, en hægt er að breyta þessari tölu. Nánari upplýsingar, sjá fyrirfram lesa handbook.
3.  Ef vöru notanda er ekki á listanum, veljið **Leita fleiri** til að gera á netinu leita í Dynamics 365 Aðgerðir. Leita eftir afurðarnúmer eða skipta yfir í leit að nafni afurðar.
4.  Veljið afurð. Ef varan hefur mynd, myndin sýnd.
5.  Veljið eina af eftirfarandi valkostum til að skoða stöðu á lager:
    -   Skoða lagerbirgðir eftir svæði
    -   Skoða lagerbirgðir eftir vöruhúsi
    -   Skoða lagerbirgðir eftir staðsetningu
    -   Skoða lagerbirgðir eftir runu (fyrir runustýrðu afurðir)
    -   Skoða lagerbirgðir eftir birgðastöðu

    Afurð á lager birtist á eftirfarandi hátt:
    -   Með efnislegum birgðum (Þetta yfirlit sýnir heildarupphæð.)
    -   Eftir efnislegt magn frátekið (Þetta yfirlit sýnir frátekið upphæð.)
    -   Eftir tiltækt efnislegt magn (Þetta yfirlit sýnir tiltæk upphæð sem hefur ekkert frátekningar.)





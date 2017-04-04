---
title: "Kostnaður stýra fartæki vinnusvæði fyrir Microsoft Dynamics 365 Aðgerðir forrits"
description: "Með Kostnaði stýra fartæki vinnusvæði kostnaður vinnustöðvar stjórnendur sjá afköst vinnustöðvarinnar kostnaðar gerir og hvar."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kostnaður stýra fartæki vinnusvæði fyrir Microsoft Dynamics 365 Aðgerðir forrits

Með Kostnaði stýra fartæki vinnusvæði kostnaður vinnustöðvar stjórnendur sjá afköst vinnustöðvarinnar kostnaðar gerir og hvar. 

<a name="prerequisites"></a>Forkröfur
-------------

| Skilyrði                                                         | lýsing                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesa um Microsoft Dynamics 365 fyrir fartæki svæðis Aðgerðir | [Dynamics 365 fyrir fartæki svæðis Aðgerðir](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 fyrir Aðgerðir                                          | Verið viss um að afskriftareglur eru umhverfi sem er með Microsoft Dynamics 365 Aðgerðir útgáfu 1611 og uppfærslu Microsoft Dynamics fyrir Aðgerðir svæðis (Nóvember 2016) 3. |
| Bráðabót KB 3215650                                                    | Setja upp bráðabót til að virkja skal vinnusvæðin sem eru gefnir í Microsoft Dynamics 365 fyrir Aðgerðir.                                                                       |
| Lýsingarlína fartækis með Dynamics 365 fyrir Aðgerðir forrits uppsett | Sækja Dynamics 365 fyrir Aðgerðir forrits úr verslunin fartæki forrits.                                                                                                      |

## <a name="introduction"></a>Inngangur
Kostnaður stýra fartæki vinnusvæði veitir snatri yfirlit á gildandi afköstum á kostnaðarstaði með því að bera saman raunkostnað við áætlaðan kostnað. Hægt er að kafa niður stöður stakar einingar.

### <a name="example"></a>Dæmi

Starfsmaður fær boð um að koma á alþjóðlegum conference. Fyrirtæki verður að ná yfir öll ferðakostnaður. Starfsmaður biður hans manger ef hann hægt að sækja í conference. Stjórnanda opnar fljótt Kostnaður stýra fartæki vinnusvæði á farsímanúmer hans til að sjá hvort hann hefur fjárhagsáætlunar fyrir starfsmanninn til að sækja í conference.

### <a name="data-security"></a>Öryggi gagna

Gögn í Kostnaði stýra vinnusvæði er tryggð með notendaheimildir. Stjórnandi vinnustöðvar er aðeins heimilt að sjá gögn varðandi hans eigin kostnaðarstað. Gagnastýrður aðgangur aðgang er stjórnað innan kostnaðarbókhaldslíkani. Kostnaður bókhaldarar skilgreina grunnstillingar vinnusvæðis fartæki í kostnaðarbókhaldslíkani stýra Kostnaði. Eftir að vinnusvæðið er birt í Microsoft Dynamics 365 til Aðgerðir forrits, er tiltækt í 365 Dynamics fyrir fartæki Aðgerðir forrits. Þetta tryggir að allar kostnaður vinnustöðvar stjórnendur í fyrirtækinu þvínæst gögn í sama snið.

### <a name="actions-views-and-links"></a>Aðgerðir yfirlit og tengla

Kostnaður stýra fartæki vinnusvæði fyrir Dynamics 365 Aðgerðir forrits veitir eftirfarandi aðgerðir, yfirlit og tengla:

-   Aðgerðir 
    -   Velja **Skilgreiningar** til að taka með útlit.
    -   Velja **Kostnaður hlutir** til að taka kostnaðarstað sem er á sem síu gögn. **Athugasemd:** birtur listi eftir aðgangur veittur í kostnaðarbókhaldslíkani.

<!-- -->

-   Samkvæmt hvað er valið undir **Aðgerðir** og hvað er skilgreind í kostnaðarbókhaldslíkani, er hægt að skoða eftirfarandi upplýsingar í Kort. Athuga upphæð birtist í sama snið: Raunveruleg, Áætlun, Fráviks og Frávik %. 
    -   Raunverulegt samaborið við Áætlun (gildandi tímabil)
    -   Raunverulegt miðað við fjárhagsáætlun Yfirfarnar (gildandi tímabil)
    -   Raunverulegt samaborið við Áætlun (fyrra tímabil)
    -   Yfirfarnar raunverulegt miðað við fjárhagsáætlun (fyrra tímabil)
    -   Raunverulegt samaborið við Áætlun (ári)
    -   Yfirfarnar raunverulegt miðað við fjárhagsáætlun (ári)

<!-- -->

-   Tenglar
    -   Upplýsingar fyrir núverandi tímabil.
    -   Upplýsingar fyrir fyrri tímabil.
    -   Upplýsingar um ári.

Þegar ein tengla, birtist Kort á kostnaðareiningunni. Upphæð í Kort birtast með eftirfarandi sniði: Raun, Áætlaðan, fjárhagsfrávik fráviks % Fjárhagsáætlunar, Yfirfarnar fjárhagsáætlunar, fjárhagsfrávik Yfirfarnar og Yfirfarnar fjárhagsáætlunar fráviks %.  [![stjórnun kostnaðar](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Hefjast handa
Fylgið eftirfarandi skrefum til að byrja nota kostnað stýringu forritið fartæki í þínu fartækis.

1.  Verslunin fartæki forritið á að sækja og setja upp Microsoft Dynamics 365 til aðgerðir forrits.
2.  Byrja forritið þitt tækis.
3.  Færið inn Vefslóð skal Dynamics 365.
4.  Færið inn fyrirtæki að skrá sig inn á. Til dæmis inn **USMF**.
5.  Í fyrsta sinn sem þú skráir þig inn, verið beðið um notandanafn og aðgangsorð fyrir notanda Microsoft Dynamics 365 fyrir Aðgerðir. Færið inn skilríkjum þínum. Eftir að skrá er að sjá tiltækar vinnusvæða fyrirtækisins.

Til að skoða vinnusvæða fartæki forritið, er verður fyrst að birta skal vinnusvæðin sem óskað er eftir að Dynamics 365 fyrir Aðgerðir forrits.

1.  Ræsa Dynamics 365 aðgerða.
2.  Fara í **kerfisstjórnun**&gt;**Uppsetningu**&gt;**kerfisfæribreytum**.
3.  Veljið **Stjórna fartæki forrits**.
4.  Velja vinnusvæðið ** Kostnaður stýra ** til að birta í fartæki svæðis.
5.  Velja **Birta vinnusvæði**.
6.  Endurnýja skal tæki til að sjá birt vinnusvæði.

## <a name="view-the-performance-of-your-cost-center"></a>Skoða afköst fyrirtækisins kostnaðarstaður
1.  Fartækis, veljið þá **Kostnaður stýra** vinnusvæði.
2.  Velja **Kostnaður hlut stýra**.
3.  Smellið á **Aðgerðir**.
4.  Smellið á **Velja afbrigði** til að velja útlit stýra kostnaði.
5.  Click **Done**.
6.  Smellið á **Aðgerðir**.
7.  Smellið á **Hluturinn kostnaður** til að velja á kostnaðarstaði sem þú hefur verið veittur aðgangur.
8.  Click **Done**.
9.  Skoða heildarframmistöðu fyrirtækisins kostnaðarstaður.
10. Smellið á **Upplýsingar fyrir núverandi tímabil**.
11. Skoða afköst stakar einingar.
12. Einnig er hægt að leita fyrir tiltekinn kostnað einingar.




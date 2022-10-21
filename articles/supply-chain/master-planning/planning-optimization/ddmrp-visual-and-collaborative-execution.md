---
title: Sjónræn framkvæmd og samvinnuframkvæmd
description: Þessi grein lýsir því hvernig á að fylgjast með eftirspurnardrifnu efnisþörfskipulagi (DDMRP) aftengingarpunktum, biðminni, fyrirhuguðum pöntunum og sögu.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 92e38c6ea19b60ae0a61e55f240ff52698e06933
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689777"
---
# <a name="visual-and-collaborative-execution"></a>Sjónræn framkvæmd og samvinnuframkvæmd

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Þessi grein lýsir því hvernig á að fylgjast með eftirspurnardrifnu efnisþörfskipulagi (DDMRP) aftengingarpunktum, biðminni, fyrirhuguðum pöntunum og sögu.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Fylgstu sjónrænt með biðmunum og magni fyrir valinn hlut

Í Microsoft Dynamics 365 Supply Chain Management, þú getur sjónrænt fylgst með því hvernig stuðpúðar, magn á lager og nettóflæðisstig breytast með tímanum fyrir hvaða útgefna vöru sem er valin. Fylgdu þessum skrefum til að opna og skoða töflurnar.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu útgefinn hlut sem er settur upp sem aftengingarpunktur. (Nánari upplýsingar er að finna í [Staðsetning birgða](ddmrp-inventory-positioning.md) .)
1. Á aðgerðarrúðunni, á **Áætlun** flipa, veldu **Vöruumfjöllun**.
1. Á **Vöruumfjöllun** síðu, veldu vöruþekjuskrá sem býr til aftengingarpunkt. (Þessi skrá mun sýna nafn umfjöllunarhóps sem er settur upp til að búa til aftengingarpunkta.)
1. Veldu **Á hendi** flipa. Þessi flipi inniheldur myndrit sem sýnir hvernig magn á lager breyst með tímanum, ásamt gildi vörustigsins sem var skráð fyrir tiltekið tímabil í hvert skipti sem hagræðing áætlanagerðar er keyrð. Flipinn inniheldur einnig töflu sem sýnir hvaða af eftirtöldum flokkum hvert skráð stig fellur inn í:

    - **Krítískt lágt** – Innan við helmingur lágmarks á tímabilinu.
    - **Lágt** – Á milli helmings lágmarks og lágmarks.
    - **Meðaltal við höndina** – Á milli lágmarks og lágmarks plús græna svæðið.
    - **Hærri en meðaltal** - Hærra en meðaltal.

    ![Söguleg stig á hendi á flipanum Til staðar.](media/ddmrp-on-hand-graph.png "Söguleg stig á hendi á flipanum Til staðar")

    > [!NOTE]
    > Litirnir sem eru notaðir á **Á hendi** flipinn tákna önnur svið en svipaðir litir sem notaðir eru á **Buffer gildi** flipa.

1. Til að skoða hvernig biðminnisgildin þín breyttust með tímanum og hvernig þau eru í samanburði við álags- og netflæðisstig skaltu velja **Buffer gildi** flipa.

    ![Söguleg álags- og netflæðisstig á flipanum Buffer values.](media/ddmrp-buffer-values-graph.png "Söguleg álags- og netflæðisstig á flipanum Buffer values")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Fylgstu með stöðu og fyrirhuguðum pöntunum fyrir alla aftengingarpunkta

The **Eftirspurnardrifið MRP** vinnusvæði býður upp á nokkur verkfæri, ásamt lykilframmistöðuvísum (KPIs) og yfirlitum yfir stöðu aftengingarpunkta þinna og tengdra fyrirhugaðra pantana. Til að opna það skaltu fara á **Aðalskipulag \> Vinnurými \> Eftirspurnardrifið MRP**.

![Eftirspurnardrifið MRP vinnusvæði.](media/ddmrp-workspace.png "Eftirspurnardrifið MRP vinnusvæði")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Fáðu yfirlit yfir aftengingarpunkta og fyrirhugaðar pantanir

Í viðbót við **Eftirspurnardrifið MRP** vinnusvæði býður Supply Chain Management upp á nokkrar síður þar sem þú getur skoðað upplýsingar um DDMRP uppsetningu þína, aftengingarpunkta og fyrirhugaðar pantanir. Sumar þessara síðna bjóða einnig upp á þægilega hnappa á aðgerðarrúðunni sem gerir þér kleift að stjórna biðmunum, keyra aðalskipulagningu og opna aðrar tengdar skoðanir.

- Til að skoða stöðu aftengingarpunkta eftir nettóflæðisstigi, farðu á **Aðalskipulag \> Aðalskipulag \> DDMRP \> Staða aftengingarpunkta eftir nettóflæði**.
- Til að skoða stöðu aftengingarpunkta eftir birgðastigi á lager, farðu á **Aðalskipulag \> Aðalskipulag \> DDMRP \> Staða aftengingar punkta á hendi**.
- Til að skoða fyrirhugaðar pantanir fyrir aftengingarpunkta, farðu á **Aðalskipulag \> Aðalskipulag \> DDMRP \> Skipulagðar pantanir fyrir aftengingarpunkta**.
- Til að skoða aftengdan afgreiðslutíma, farðu á **Aðalskipulag \> Aðalskipulag \> DDMRP \> Aftengdur leiðtími**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Hreinsaðu upp aftengingarpunkta biðminni

Með tímanum mun kerfið þitt byggja upp mikið magn af sögulegum gögnum sem tengjast áframhaldandi biðminniútreikningum. Þessi söguleg gögn munu valda því að gagnamagn þitt eykst og geta að lokum haft áhrif á afköst kerfisins þíns. Þess vegna mælum við með að þú hreinsir af og til upp gömlu aftengingarpunkta biðminni gildi.

> [!WARNING]
> Hreinsunarstarfið mun fjarlægja sögulegar biðminnigildistillingar og sögulegar upplýsingar um áhald/netflæði. Það er ekki afturkræft.

Fylgdu þessum skrefum til að hreinsa upp aftengingarpunkta biðminni.

1. Fara til **Aðalskipulag \> Aðalskipulag \> DDMRP \> Hreinsaðu upp aftengingarpunkta biðminni**.
1. Í **Hreinsaðu upp aftengingarpunkta biðminni** valmynd, stilltu eftirfarandi reiti:

    - **Eyða skrám eldri en (dögum)** – Tilgreindu aldur yngstu skránna sem á að halda, í dögum. Öllum aftengingarpunkta biðminni gildisfærslum sem eru eldri en þetta gildi verður eytt.
    - **Snilldaráætlun** – Veldu aðalskipulag sem inniheldur hluti sem ætti að verða fyrir áhrifum af þessari hreinsun. Hreinsunin mun gilda um alla hluti áætlunarinnar eftir kl **Sía** stillingar sem þú tilgreinir í þessum glugga eru notaðar.

1. Til að takmarka safnið af færslum sem runuvinnan ætti að keyra á, á **Skrár til að hafa með** Flýtiflipi, veldu **Sía** að opna **Fyrirspurn** valmynd. Þessi gluggi virkar alveg eins og hann gerir fyrir aðrar gerðir af [bakgrunnsstörf](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í birgðakeðjustjórnun.
1. Á **Hlaupa í bakgrunni** Flýtiflipi, tilgreinið hvernig, hvenær og hversu oft skal hreinsa. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Allt í lagi** til að bæta nýja verkinu við hópröð fyrir framkvæmd.

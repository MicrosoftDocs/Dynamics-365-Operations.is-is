---
title: "tími og mæting smásölu"
description: "Þetta efnisatriði lýsir aðstæðum sem eru studdar hvað varðar tíma- og mætingastjórnun í Microsoft Dynamics 365 for Retail."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: b458d1938f49a2f33f7dd3ce3062880f0d4d7bfc
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017

---

# <a name="retail-time-and-attendance"></a>Retail-tími og -viðvera

[!include[banner](includes/banner.md)]


Þetta efnisatriði lýsir aðstæðum sem eru studdar hvað varðar tíma- og mætingastjórnun í Microsoft Dynamics 365 for Retail. 

<a name="manage-worker-setup-and-scheduling"></a>Stjórna uppsetningu starfsmanns og áætlun
----------------------------------

### <a name="initial-configuration"></a> Upphafleg skilgreining

-   Keyrið leiðsagnarforrit grunnstillingar
-   Skrá starfsmenn sem starfsmenn tímaskráningar.

### <a name="plan-worker-schedules"></a>Áætla áætlanir starfsmanns

-   Nota forstillingar með vinnuáætlun Nánari upplýsingar, sjá <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Sjá upplýsingar um skilgreiningarskref <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Skilgreining fyrir smásölu

-   Virkja virknireglu Stimpilklukku, fyrir starfsmenn sem á að virkja tímaskráningar fyrir. Smellið á **Virkniforstilling sölustaðar** &gt; **Aðgerðir** &gt; **POS tímaskráning** &gt; **Virkja tímaskráningar**.
-   Skilgreina heimildaflokka sölustaðs (POS) til að virkja heimild fyrir Skoða færslur stimpilklukku. Þessi heimild gerir notanda kleift að skoða skráningar stimpilklukku annarra starfsmanna í versluninni (og úr öllum öðrum verslunum sem notandinn er tengdur, með aðsetursbókinni). Þú gætir viljað virkja þessar heimildir fyrir hlutverk stjórnanda en ekki fyrir hlutverk gjaldkera . Smellið á **Heimildaflokka sölustaðar** &gt; **Skoða færslur stimpilklukku**.

## <a name="register-time"></a>Tími á afgreiðslukassa
### <a name="cashier-and-non-cashier-time-registrations"></a>tímaskráningar Gjaldkera og þess sem er ekki gjaldkeri

-   Á sölustað
    -   Innstimplunaraðgerðir:
        -   Skráið inn með aðgerð utan skúffu eða nýrri vakt.
        -   Velja aðgerð stimpilklukku
        -   Velja aðgerð sem óskað er:
            -   Innstimplun
            -   Hlé fyrir vinnu
            -   Hádegishlé
            -   Útstimplun

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Núgildandi staða</th>
    <th>Tiltækir valkostir</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Innstimplun</td>
    <td><ul>
    <li>Hlé fyrir vinnu</li>
    <li>Hádegishlé</li>
    <li>Útstimplun</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Hlé fyrir vinnu</td>
    <td>Innstimplun</td>
    </tr>
    <tr class="odd">
    <td>Hádegishlé</td>
    <td>Innstimplun</td>
    </tr>
    <tr class="even">
    <td>Útstimplun</td>
    <td>Innstimplun</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Skoða staðfestingarskilaboðin og votta að núverandi tími verkþáttar sé réttur.
-   Færslubók:
    -   Smellið á **Kladdabók** til að skoða verkþátt stimpilklukku .
    -   nota tímasíur til að velja mismunandi tímaglugga.
    -   Ef þú vinnur á mörgum stöðum, sérð þú tímaskráningar þínum frá öllum verslunum þar sem þú skráðir tíma. Hægt er að nota síu verslunar til að skoða tímaskráningar úr valinni verslun.

<!-- -->

-   Mismunandi tímabelti:
    -   Ef þú skoðar tíma frá öðrum staðsetningum (fyrir færslubók gjaldkera , eða með því að nota **skoða færslur stimpilklukku** fyrir aðstæður stjórnanda ), og að staðsetning er í öðru tímabelti, eru tímafærslur sem þú sérð umbreytt í þinn staðartíma. Til dæmis er stjórnandi fyrir tvær verslanir, ein í Arizona og önnur Nevada. Gjaldkeri skráir innstimplun við 9:00 F.HÁD í Arizona. Á þeirri stundu er tími í Nevada 8:00 F.HÁD Þess vegna ef þú ert í versluninni í Nevada og skoðar færslur tímaskráningar, eru  tímaskráningarnar merktar sem F.HÁD 8

## <a name="view-worker-time-registrations"></a>Stjórna tímaskráningu starfskrafts
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Skoða tímaskráningar starfsmanna og sía eftir verslun eða gerð verkþáttar

Á sölustað

-   Velja **skoða færslur stimpilklukku**
-   Þú sérð skráningar tímaklukku fyrir aðgerðir fyrir  alla starfsmenn sem úthlutaðir eru á verslunum sem þú ert úthlutað til.
-   Hægt er að nota verkþáttargerð og síur verslunar til að sía tímaskráningar.

## <a name="process-and-manage-time-registrations"></a>Vinna með og stjórna tímaskráningum
Notandi Dynamics 365 for Retail fylgist með verkflæðinu til að reikna, samþykkja og flytja tímaskráningar í launaskrá.

### <a name="primary-operations"></a>Aðalaðgerðir

-   Reikna
-   Samþykkja
-   Senda í laun

### <a name="other-common-operations"></a>Aðrar algengar aðgerðir

-   Fjöldaútstimplun
-   Skrá Fjarvist

Nánari upplýsingar um hvernig skal vinna skráningu tíma og viðveru ferli í <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




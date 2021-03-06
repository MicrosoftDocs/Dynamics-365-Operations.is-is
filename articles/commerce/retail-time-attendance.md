---
title: Stjórnun tíma og viðveru í Retail
description: Þessi efnisþáttur lýsir aðstæðum sem styður stjórnun á tíma og mætingu í Dynamics 365 Commerce.
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7ac7eec69bda7ad2fa41a7311a71a969eddeafb6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021489"
---
# <a name="time-and-attendance-management-in-retail"></a>Stjórnun tíma og viðveru í Retail

[!include [banner](includes/banner.md)]

Þessi efnisþáttur lýsir aðstæðum sem styður stjórnun á tíma og mætingu í Dynamics 365 Commerce.

## <a name="manage-worker-setup-and-scheduling"></a>Stjórna uppsetningu starfsmanns og áætlun

### <a name="initial-configuration"></a>Upphafleg skilgreining

- Keyrið leiðsagnarforrit grunnstillingar
- Skrá starfsmenn sem starfsmenn tímaskráningar.

### <a name="plan-worker-schedules"></a>Áætla áætlanir starfsmanns

- Nota forstillingar með vinnuáætlun Nánari upplýsingar er að finna í [Nota forstillingar með vinnuáætlun](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).

Nánari upplýsingar um skilgreiningarskref er að finna í [Uppsetning á tíma og viðveru](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).

### <a name="commerce-specific-configuration"></a>Commerce-sértæk skilgreining

- Virkja virknireglu Stimpilklukku, fyrir starfsmenn sem á að virkja tímaskráningar fyrir. Smellið á **Virkniforstilling sölustaðar** &gt; **Aðgerðir** &gt; **POS tímaskráning** &gt; **Virkja tímaskráningar**.
- Skilgreina heimildaflokka sölustaðs (POS) til að virkja heimild fyrir Skoða færslur stimpilklukku. Þessi heimild gerir notanda kleift að skoða skráningar stimpilklukku annarra starfsmanna í versluninni (og úr öllum öðrum verslunum sem notandinn er tengdur, með aðsetursbókinni). Þú gætir viljað virkja þessar heimildir fyrir hlutverk stjórnanda en ekki fyrir hlutverk gjaldkera . Smellið á **Heimildaflokka sölustaðar** &gt; **Skoða færslur stimpilklukku**.

## <a name="register-time"></a>Tími á afgreiðslukassa

### <a name="cashier-and-non-cashier-time-registrations"></a>tímaskráningar Gjaldkera og þess sem er ekki gjaldkeri

- Á sölustað

    - Innstimplunaraðgerðir:

        - Skráið inn með aðgerð utan skúffu eða nýrri vakt.
        - Velja aðgerð stimpilklukku
        - Velja aðgerð sem óskað er:

            - Innstimplun
            - Hlé fyrir vinnu
            - Hádegishlé
            - Útstimplun

        <table>
        <thead>
        <tr>
        <th>Núgildandi staða</th>
        <th>Tiltækir valkostir</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Innstimplun</td>
        <td>
        <ul>
        <li>Hlé fyrir vinnu</li>
        <li>Hádegishlé</li>
        <li>Útstimplun</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Hlé fyrir vinnu</td>
        <td>Innstimplun</td>
        </tr>
        <tr>
        <td>Hádegishlé</td>
        <td>Innstimplun</td>
        </tr>
        <tr>
        <td>Útstimplun</td>
        <td>Innstimplun</td>
        </tr>
        </tbody>
        </table>

        [![Stöður stimpilklukku](./media/timeclockstates.png)](./media/timeclockstates.png)

- Skoða staðfestingarskilaboðin og votta að núverandi tími verkþáttar sé réttur.
- Færslubók:

    - Smellið á **Kladdabók** til að skoða verkþátt stimpilklukku .
    - nota tímasíur til að velja mismunandi tímaglugga.
    - Ef þú vinnur á mörgum stöðum, sérð þú tímaskráningar þínum frá öllum verslunum þar sem þú skráðir tíma. Hægt er að nota síu verslunar til að skoða tímaskráningar úr valinni verslun.

- Mismunandi tímabelti:

    - Ef þú skoðar tíma frá öðrum staðsetningum (fyrir færslubók gjaldkera , eða með því að nota **skoða færslur stimpilklukku** fyrir aðstæður stjórnanda ), og að staðsetning er í öðru tímabelti, eru tímafærslur sem þú sérð umbreytt í þinn staðartíma. Til dæmis er stjórnandi fyrir tvær verslanir, ein í Arizona og önnur Nevada. Gjaldkeri skráir innstimplun við 9:00 F.HÁD í Arizona. Á þeirri stundu er tími í Nevada 8:00 F.HÁD Þess vegna ef þú ert í versluninni í Nevada og skoðar færslur tímaskráningar, eru tímaskráningarnar merktar sem F.HÁD 8

## <a name="view-worker-time-registrations"></a>Stjórna tímaskráningu starfskrafts

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Skoða tímaskráningar starfsmanna og sía eftir verslun eða gerð verkþáttar

Á sölustað

- Velja **skoða færslur stimpilklukku**
- Þú sérð skráningar tímaklukku fyrir aðgerðir fyrir alla starfsmenn sem úthlutaðir eru á verslunum sem þú ert úthlutað til.
- Hægt er að nota verkþáttargerð og síur verslunar til að sía tímaskráningar.

## <a name="process-and-manage-time-registrations"></a>Vinna með og stjórna tímaskráningum

Notandi Commerce fylgist með verkflæðið til að reikna, samþykkja og flytja tímaskráningar í laun.

### <a name="primary-operations"></a>Aðalaðgerðir

- Reikna
- Samþykkja
- Senda í laun

### <a name="other-common-operations"></a>Aðrar algengar aðgerðir

- Fjöldaútstimplun
- Skrá Fjarvist

Nánari upplýsingar um hvernig skal vinna með skráningu tíma og viðveru er að finna í [Vinna með skráningu tíma og viðveru](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
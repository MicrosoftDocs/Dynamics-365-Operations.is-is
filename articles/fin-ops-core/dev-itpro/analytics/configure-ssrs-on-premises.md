---
title: Skilgreina SQL Server Reporting Services fyrir staðbundna uppsetningu
description: Þessi grein veitir upplýsingar um grunnstillingu á SQL Server Reporting Services (SSRS) fyrir virkjun á staðnum.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.custom: 55651
ms.assetid: ''
ms.service: ''
ms.openlocfilehash: 9acb681ce07c3a7da82a630c7a87a4271a411b51
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275417"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>Skilgreina SQL Server Reporting Services fyrir staðbundna uppsetningu

[!include [banner](../includes/banner.md)]

Notið skrefin í þessari grein til að grunnstilla SQL Server Reporting Services (SSRS) fyrir virkjun Microsoft Dynamics 365 Finance + Operations (on-premises).

1. Opnaðu grunnstillingarstjóra skýrslugerðarþjónustu.
2. Skildu eftir sjálfgefið **Þjónsnafn**, sem ætti að vera nafn vélarinnar sem er í notkun, og **Heiti skýrsluþjónstilviks**, **MSSQLSERVER**.
3. Smelltu á **Tengja**.

    [![Grunnstillingartenging skýrslugerðarþjónustu.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Smellið á flipann **Þjónustureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    [![Þjónustureikningsflipi.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Smellið á flipann **Vefþjónustuslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    [![Flipi vefþjónustuslóðar.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Smellið á flipann **Gagnagrunnur** og sannreynið að **Gagnagrunnsnafn** og **Skilríkjastillingar** passi við eftirfarandi mynd.

    > [!NOTE]
    > Þú þarft að búa til nýjan gagnagrunn. Til að gera það skal smella á **Breyta gagnagrunni** og staðfest að nýja gagnagrunnsnafnið sé: **DynamicsAxReportServer**.

    [![gagnagrunnsflipi.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Smellið á flipann **Vefgáttarslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    > [!NOTE]
    > Nauðsynlegt er að smella á **Nota** til að búa til og skilgreina gáttina almennilega.

    [![flipi vefgáttarslóðar.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Eftir að gáttin er grunnstillt passar flipinn **Vefgátt** við eftirfarandi mynd.

    [![vefgáttarflipi.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Smelltu á skýrsluvefslóðina til að skoða vefgátt SQL Server Reporting Services.
9. Í gáttinni skal stofna nýja möppu með nafninu **Dynamics**.

    [![dynamics mappa.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Í **grunnstillingarstjóra skýrslugerðarþjónustu** skal smella á flipann **tölvupóststillingar** og sannreyna að stillingarnar passi við eftirfarandi mynd.

    [![tölvupóststillingaflipi.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Smellið á flipann **Keyrslureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    [![keyrslureikningsflipi.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Ekki breyta sjálfgefnum stillingum á flipanum **Dulritunarlyklar**.

    [![dulritunarlyklaflipi.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Smellið á flipann **Áskriftarstillingar** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    [![áskriftarstillingaflipi.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Ekki breyta sjálfgefnum stillingum á flipanum **Uppsetning útvíkkunar** flipanum.

    [![flipi útskölunarvirkjunar.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Ekki breyta sjálfgefnum stillingum á flipanum **Power BI-samþætting**.

    [![power bi-samþættingaflipi.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Smelltu á **Hætta** til að loka **grunnstillingarstjóra skýrslugerðarþjónustu.**.

    [![loka grunnstillingarstjóra skýrslugerðarþjónustu.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

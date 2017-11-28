---
title: "Stilla SQL Server Reporting Services fyrir staðbundna uppsetningu"
description: "Þetta efnisatriði veitir upplýsingar um grunnstillingu á SQL Server Reporting Services (SSRS) fyrir virkjun á staðnum."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a1f11641a2ec055cfaa0157ac9a40525daa4006
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>Stilla SQL Server Reporting Services fyrir staðbundna uppsetningu

Fylgið skrefunumm í þessu efnisatriði til að grunnstilla virkjun SQL Server Reporting Services (SSRS) fyrir Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (á staðnum).

1. Opnaðu grunnstillingarstjóra skýrslugerðarþjónustu.
2. Skildu eftir sjálfgefið **Þjónsnafn**, sem ætti að vera nafn vélarinnar sem er í notkun, og **Heiti skýrsluþjónstilviks**, **MSSQLSERVER**. 
3. Smelltu á **Tengja**.
   
   [![Grunnstillingartenging skýrslugerðarþjónustu](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. Smellið á flipann **Þjónustureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    [![Þjónustureikningsflipi](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. Smellið á flipann **Vefþjónustuslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd. 

    [![Flipi vefþjónustuslóðar](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. Smellið á flipann **Gagnagrunnur** og sannreynið að **Gagnagrunnsnafn** og **Skilríkjastillingar** passi við eftirfarandi mynd. **Athugið:** Það þarf að stofna nýjan gagnagrunn. Til að gera það skal smella á **Breyta gagnagrunni** og staðfest að nýja gagnagrunnsnafnið sé: **DynamicsAxReportServer**.

    [![gagnagrunnsflipi](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. Smellið á flipann **Vefgáttarslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd. **Athugið:** Það þarf að smella á **Nota** til að stofna og grunnstilla gáttina rétt.

    [![flipi vefgáttarslóðar](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  Eftir að gáttin er grunnstillt passar flipinn **Vefgátt** við eftirfarandi mynd.
    [![vefgáttarflipi](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. Smelltu á skýrsluvefslóðina til að skoða vefgátt SQL Server Reporting Services. 
9.  Í gáttinni skal stofna nýja möppu með nafninu **Dynamics**.

    [![dynamics mappa](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. Í **grunnstillingarstjóra skýrslugerðarþjónustu** skal smella á flipann **tölvupóststillingar** og sannreyna að stillingarnar passi við eftirfarandi mynd.

    [![tölvupóststillingaflipi](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. Smellið á flipann **Keyrslureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    [![keyrslureikningsflipi](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  Ekki breyta sjálfgefnum stillingum á flipanum **Dulritunarlyklar**. [![flipinn dulritunarlyklar](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. Smellið á flipann **Áskriftarstillingar** og sannreynið að stillingarnar passi við eftirfarandi mynd.

    [![áskriftarstillingaflipi](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  Ekki breyta sjálfgefnum stillingum á flipanum **Uppsetning útvíkkunar**. [![flipinn uppsetning útvíkkunar](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  Ekki breyta sjálfgefnum stillingum á flipanum **Power BI samþætting**. [![flipinn Power BI samþætting](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. Smelltu á **Hætta** til að loka **grunnstillingarstjóra skýrslugerðarþjónustu.**.

    [![loka grunnstillingarstjóra skýrslugerðarþjónustu](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    



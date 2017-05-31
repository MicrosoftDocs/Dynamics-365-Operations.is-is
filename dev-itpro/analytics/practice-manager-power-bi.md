---
title: "Power BI-efni aðferðastjórnunar"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni aðferðastjórnunar. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnispakka."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Power BI-efni aðferðastjórnunar

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvað er innifalið í Microsoft Power BI-efni **Aðferðarstjóri**. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

Power BI-efni **aðferðastjórnunar** var búið til fyrir aðferðastjóra og verkefnastjóra. Það veitir lykileiningarnar sem tengjast verkefnunum sem fyrirtækið er að vinna að. Á yfirlitinu má sjá yfirlit verkefna og tengdra viðskiptamanna. Afmörkun á skýrslustigi má nota til að gefa skýrslu um tilgreinda lögaðila. Þetta Power BI-efni sækir gögn úr uppsöfnuðum mælingum verkbókhalds fyrir Microsoft Dynamics 365 for Operations.

Power BI-efni **aðferðastjórnunar** inniheldur fimm skýrslusíður: eina yfirlitssíðu og fjórar síður með upplýsingum um kostnaður verks, tekjur, stjórnun unnins virðis og stundaeiningarnar sem eru skornar og hlutaðar í ýmsum víddum.

Upphæðir í efni eru sýndar í gjaldmiðli kerfisins. Hægt er að stilla gjaldmiðil kerfis á síðunni **Kerfisfæribreytur**.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni

Hægt er að finna Power BI-efni **aðferðastjórnunar** í safninu Samnýttar eignar í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnið og tengja það við gögn Dynamics 365 for Operations er að finna í [Power BI-efni í LCS frá Microsoft og samstarfsaðilum þínum](power-bi-content-microsoft-partners.md).

Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office mix.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni

Eftirfarandi tafla veitir upplýsingar um einingarnar sem finna má á hverri síðu skýrslunnar í Power BI-efni **aðferðastjórnunar**.

| Skýrslusíða                                          | Einingar               |
|------------------------------------------------------|-----------------------------------------------|
| Yfirlit  | Stofnuð verk<br>Metin verk<br>Verk í vinnslu<br>Fjöldi verka eftir stigum<br>Fjöldi verka eftir borgum<br>Rauntekjur eftir viðskiptamanni<br>Fjárhagsáætlun brúttóframlegðar eftir verkum<br>Yfirlit yfir stjórnun áunnins virðis |
| Kostnaður                                                 | Raunverulegur sb. v. fjárhagsáætlun eftir mánuðum<br>Raunverulegur sb. v. fjárhagsáætlun eftir árum<br>Raunverulegur sb. v. fjárhagsáætlun eftir flokkum<br>Raunverulegur eftir færslugerð       |
| Tekjur                                              | Tekjur eftir mánuði<br>Rauntekjur eftir póstnúmeri<br>Rauntekjur sb. v. tekjur í fjárhagsáætlun eftir flokkum<br>Rauntekjur eftir atvinnugrein viðskiptamanns        |
| EVM                                                  | Kostnaðarvísir og vísir fyrir áætluð afköst eftir verki                 |
| Tímar                                                | Raunverulega rukkanlegar nýttar stundir sb. v. raunverulega rukkanlegar álagsstundir sb. v. fjárhagsáætlunarstundir<br>Raunverulega rukkanlegar nýttar stundir sb. v. raunverulega rukkanlegar álagsstundir eftir verki<br>Raunverulega rukkanlegar nýttar stundir sb. v. raunverulega rukkanlegar álagsstundir eftir tilföngum<br>Hlutfall raunverulega rukkanlegra nýttra stunda eftir verki<br>Hlutfall raunverulega rukkanlegra nýttra stunda eftir tilföngum |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að afmarka og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Einnig má nota virknina Flytja út undirliggjandi gögn til að flytja út undirliggjandi gögn sem eru sýnd í myndrænni samantekt.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Gögn Dynamics 365 for Operations eru notuð til að fylla út skýrslusíður í Power BI-efni **aðferðastjórnunar**. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni sem Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)

Í eftirfarandi hluta er fjallað um uppsafnaðar mælingar sem notaðar eru á hverja einingu.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Eining: ProjectAccountingCube_ActualHourUtilization
**Gagnaveita**: ProjEmplTrans

| Lykiluppsafnaðar mælingar                | Svæði                                | lýsing                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Samtala (ActualUtilizationBillableRate)   | Samtala fyrir raunverulega rukkanlegar nýttar stundir |
| ActualBillableBurdenHours                | Samtala (ActualBurdenBillableRate)        | Samtala fyrir verð fyrir raunverulegar álagsstundir             |

### <a name="entity-projectaccountingcubeactuals"></a>Eining: ProjectAccountingCube_Actuals
**Gagnaveita**: ProjTransPosting

| Lykiluppsafnaðar mælingar                | Svæði                                | lýsing                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Samtala (ActualRevenue)               |  Samtala fyrir bókaðar tekjur fyrir allar færslur |   
| ActualCost   |                             Samtala (ActualCost)           |    Samtala bókaðs kostnaðar fyrir allar færslugerðir    |

### <a name="entity-projectaccountingcubecustomer"></a>Eining: ProjectAccountingCube_Customer
**Gagnaveita**: CustTable

| Lykiluppsafnaðar mælingar                | Svæði                                | lýsing                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Fjöldi verka        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Fjöldi tiltækra verka    |


### <a name="entity-projectaccountingcubeforecasts"></a>Eining: ProjectAccountingCube_Forecasts
**Gagnaveita**: ProjTransBudget

| Lykiluppsafnaðar mælingar                | Svæði                                | lýsing                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Samtala (BudgetCost)  |       Heildarkostnaðaráætlun fyrir allar færslugerðir     |
|     BudgetRevenue    |         Samtala (BudgetRevenue)    |    Samtala fyrir áætlaðar uppsafnaðar/reikningsfærðar tekjur         |
|BudgetGrossMargin | Samtala (BudgetGrossMargin) |Munur milli samtölu fyrir áætlaðar uppsafnaðar tekjur og samtölu fyrir áætlaðan kostnað

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Eining: ProjectAccountingCube_ProjectPlanCostsView
**Gagnaveita**: Verk

| Lykiluppsafnaðar mælingar                | Svæði                                | lýsing                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Samtala (SumOfTotalCostPrice)   | Áætlað heildarkostnaðarverð fyrir allar færslugerðir með áætluðum verkum |

### <a name="entity-projectaccountingcubeprojects"></a>Eining: ProjectAccountingCube_Projects
**Gagnaveita**: Verk

| Lykiluppsafnaðar mælingar                | Svæði                                | lýsing                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Vísi kostnaðarafkomu  |ProjectAccountingCube_Projects[Áunnið virði] / ProjectAccountingCube_Projects[heildarraunkostnaður við lokin verk] |     Útreikningur heildar áunnu virði deilt með heildarraunkostnaði|
|  Vísir fyrir áætluð afköst |ProjectAccountingCube_Projects[Áunnið virði] / ProjectAccountingCube_Projects[Áætlaður heildarkostnaður við lokin verk]|Útreikningur heildar áunnu virði deilt með áætluðum heildakostnaði |
|Prósenta vinnu sem er lokið |Prósenta vinnu sem lokið = ProjectAccountingCube_Projects [Heildarraunkostnaður lokinna verka] / (ProjectAccountingCube_Projects [Heildarraunkostnaður lokinna verka] + ProjectAccountingCube_Projects [Heildar áætlaður kostnaður við verk] - ProjectAccountingCube_Projects [Áætlaður heildarkostnaður við lokin verk])|Heildarhlutfall lokinnar vinnu miðaður við raunkostnað lokinna verk og áætlaðan kostnað verksins|
|Hlutfall raunverulega rukkanlegra nýttra stunda|ProjectAccountingCube_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir] / (ProjectAccountingCube_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir] + ProjectAccountingCube_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar álagsstundir])|Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir m.v. nýttar stundir + álagsstundir|
|Áunnið virði|ProjectAccountingCube_Projects[Áætlaður heildarkostnaður verks] * ProjectAccountingCube_Projects[Hlutfall lokinna verka]|Áætlaður heildarkostnaður margfaldaður með hlutfalli lokinna verka|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Eining: ProjectAccountingCube_TotalEstimatedCosts 
**Gagnaveita**: ProjTable

| Lykiluppsafnaðar mælingar                | Svæði                                | lýsing                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Samtala (TotalCostPrice)  |   Heildarkostnaðarverð á mat fyrir allar færslugerðir með loknum verkum|

## <a name="additional-resources"></a>Frekari upplýsingar

Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

- [Gagnaeiningar](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Grunnstilla Power BI samþættingu fyrir vinnusvæði](configure-power-bi-integration.md)


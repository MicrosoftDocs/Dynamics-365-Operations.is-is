---
title: "Power BI-efni aðferðastjórnunar"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni aðferðastjórnunar. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem eru notaðar til að búa til efnið."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017

---

# <a name="practice-manager-power-bi-content"></a>Power BI-efni aðferðastjórnunar

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í Microsoft Power BI-efni **Aðferðarstjóri**. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

Power BI-efni **aðferðastjórnunar** var búið til fyrir aðferðastjóra og verkefnastjóra. Það veitir lykileiningarnar sem tengjast verkefnunum sem fyrirtækið er að vinna að. Á yfirlitinu má sjá yfirlit verkefna og tengdra viðskiptamanna. Afmörkun á skýrslustigi má nota til að gefa skýrslu um tilgreinda lögaðila. Þetta Power BI efni sækir gögn úr uppsöfnuðum mælingum verkbókhalds.

Power BI efnið **Aðferðastjóri** inniheldur fimm skýrslusíður: eina yfirlitssíðu og fjórar síður með upplýsingum um kostnað verks, tekjur, stjórnun áunnins virðis og stundaeiningarnar sem er skipt niður eftir ýmsum víddum.

Upphæðir í efni eru sýndar í gjaldmiðli kerfisins. Hægt er að stilla gjaldmiðil kerfis á síðunni **Kerfisfæribreytur**.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Ef verið er að nota Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition með uppfærslu frá júlí 2017 birtist Power BI efnið **Aðferðastjóri** á vinnusvæðinu **Verkefnastjórnun**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni

Eftirfarandi tafla veitir upplýsingar um einingarnar sem finna má á hverri síðu skýrslunnar í Power BI-efni **aðferðastjórnunar**.

| Skýrslusíða       | Einingar |
|-------------------|---------|
| Yfirlit verka | <ul><li>Stofnuð verk</li><li>Metin verk</li><li>Verk í vinnslu</li><li>Fjöldi verka eftir stigum</li><li>Fjöldi verka eftir borgum</li><li>Rauntekjur eftir viðskiptamanni</li><li>Fjárhagsáætlun brúttóframlegðar eftir verkum</li><li>Yfirlit yfir stjórnun áunnins virðis</li></ul> |
| Kostnaður              | <ul><li>Raunkostnaður gegn áætluðum kostnaði eftir mánuðum</li><li>Raunkostnaður gegn áætluðum kostnaði eftir árum</li><li>Raunkostnaður gegn áætluðum kostnaði eftir flokkum</li><li>Raunverulegur eftir færslugerð</li></ul> |
| Tekjur           | <ul><li>Tekjur eftir mánuði</li><li>Rauntekjur eftir póstnúmeri</li><li>Rauntekjur gegn áætluðum tekjum eftir flokkum</li><li>Rauntekjur eftir atvinnugrein viðskiptamanns</li></ul> |
| EVM               | Kostnaðarvísir og vísir fyrir áætluð afköst eftir verki |
| Tímar             | <ul><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum gegn áætluðum vinnustundum</li><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum eftir verki</li><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum eftir tilföngum</li><li>Hlutfall raunverulega rukkanlegra nýttra stunda eftir verki</li><li>Hlutfall raunverulega rukkanlegra nýttra stunda eftir tilföngum</li></ul> |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að afmarka og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Einnig má nota virknina Flytja út undirliggjandi gögn til að flytja út undirliggjandi gögn sem eru sýnd í myndrænni samantekt.

## <a name="extending-the-power-bi-content"></a>Stækkun efnis Power BI
Með því að nota þjónustupakka sem eru í boði í Microsoft Dynamics Lifecycle Services (LCS) er hægt að veita fólki sem skráir sig ekki inn í Microsoft Dynamics 365 öflugri greiningu. Hægt er að breyta þessum efnispökkum þannig að þeir innihaldi aðrar skýrslur eða myndræna framsetningu og afhenda svo Power BI.com leigjandanum til greiningar. 

Hægt er að finna efni Power BI efnið **Aðferðastjóri** í safninu Samnýttar eignir í LCS. Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

Gakktu úr skugga um að hlaða niður efninu **Aðferðastjóri** sem á við um þá útgáfu Microsoft Dynamics 365 sem verið er að nota.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í Power BI efninu **Aðferðastjóri**. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Entity-verslunin er Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)

Í eftirfarandi hluta er fjallað um uppsafnaðar mælingar sem notaðar eru á hverja einingu.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Eining: ProjectAccountingCube_ActualHourUtilization
**Gagnagjafi:** ProjEmplTrans

| Lykiluppsafnaðar mælingar      | Svæði                              | lýsing | 
|--------------------------------|------------------------------------|-------------|
| Raunverulega rukkanlegar nýttar stundir | Samtala (ActualUtilizationBillableRate) | Samtala fyrir unnar reikningshæfar vinnustundir. |
| Raunverulega rukkanlegar álagsstundir   | Samtala (ActualBurdenBillableRate)      | Samtala fyrir verð fyrir unnar álagsstundir. |

### <a name="entity-projectaccountingcubeactuals"></a>Eining: ProjectAccountingCube_Actuals
**Gagnagjafi:** ProjTransPosting

| Lykiluppsafnaðar mælingar | Svæði              | lýsing | 
|---------------------------|--------------------|-------------|
| Rauntekjur            | Samtala (ActualRevenue) | Samtala fyrir bókaðar tekjur fyrir allar færslur. |   
| Raunkostnaður               | Samtala (ActualCost)    | Samtala bókaðs kostnaðar fyrir allar færslugerðir. |

### <a name="entity-projectaccountingcubecustomer"></a>Eining: ProjectAccountingCube_Customer
**Gagnagjafi:** CustTable

| Lykiluppsafnaðar mælingar | Svæði                                            | lýsing | 
|---------------------------|--------------------------------------------------|-------------|
| Fjöldi verka        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Fjöldi tiltækra verka. |


### <a name="entity-projectaccountingcubeforecasts"></a>Eining: ProjectAccountingCube_Forecasts
**Gagnagjafi:** ProjTransBudget

| Lykiluppsafnaðar mælingar | Svæði                  | lýsing | 
|---------------------------|------------------------|-------------|
| Áætlaður kostnaður               | Samtala (BudgetCost)        | Heildarkostnaðaráætlun fyrir allar færslugerðir. |
| Tekjuáætlun            | Samtala (BudgetRevenue)     | Samtala fyrir áætlaðar uppsafnaðar/reikningsfærðar tekjur.  |
| Áætluð brúttóframlegð       | Samtala (BudgetGrossMargin) | Munur milli samtölu fyrir áætlaðar uppsafnaðar tekjur og samtölu fyrir áætlaðan kostnað. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Eining: ProjectAccountingCube_ProjectPlanCostsView
**Gagnagjafi:** Verk

| Lykiluppsafnaðar mælingar | Svæði                    | lýsing | 
|---------------------------|--------------------------|-------------|
| Áætlaður kostnaður              | Samtala (SumOfTotalCostPrice) | Áætlað heildarkostnaðarverð fyrir allar færslugerðir sem hafa áætluð verk. |

### <a name="entity-projectaccountingcubeprojects"></a>Eining: ProjectAccountingCube_Projects
**Gagnagjafi:** Verk

| Lykiluppsafnaðar mælingar    | Svæði | lýsing | 
|------------------------------|-------|-------------|
| Vísi kostnaðarafkomu       | ProjectAccountingCube_Projects[Áunnið virði] / ProjectAccountingCube_Projects[heildarraunkostnaður við lokin verk] | Útreikningur á samtölu áunnins virðis deilt með heildarraunkostnaði. |
| Vísir fyrir áætluð afköst   | ProjectAccountingCube_Projects[Áunnið virði] / ProjectAccountingCube_Projects[Áætlaður heildarkostnaður við lokin verk] | Útreikningur á samtölu áunnins virðis deilt með áætluðum heildarkostnaði. |
| Prósenta vinnu sem er lokið | Prósenta vinnu sem lokið = ProjectAccountingCube_Projects [Heildarraunkostnaður lokinna verka] / (ProjectAccountingCube_Projects [Heildarraunkostnaður lokinna verka] + ProjectAccountingCube_Projects [Heildar áætlaður kostnaður við verk] - ProjectAccountingCube_Projects [Áætlaður heildarkostnaður við lokin verk]) | Heildarhlutfall lokinnar vinnu miðað við raunkostnað lokinna verka og áætlaðan kostnað verksins. |
| Hlutfall unninna reikningshæfra vinnustunda  | ProjectAccountingCube_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir] / (ProjectAccountingCube_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir] + ProjectAccountingCube_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar álagsstundir]) | Samtala unninna reikningshæfra vinnustunda, miðað við nýttar stundir og álagsstundir. |
| Áunnið virði                 | ProjectAccountingCube_Projects[Áætlaður heildarkostnaður verks] * ProjectAccountingCube_Projects[Hlutfall lokinna verka] | Áætlaður heildarkostnaður margfaldaður með hlutfalli lokinna verka. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Eining: ProjectAccountingCube_TotalEstimatedCosts 
**Gagnagjafi:** ProjTable

| Lykiluppsafnaðar mælingar       | Svæði               | lýsing | 
|---------------------------------|---------------------|-------------|
| Áætlaður kostnaður lokinna aðgerða | Samtala (TotalCostPrice) | Áætlað heildarkostnaðarverð fyrir allar færslugerðir þar sem verkum er lokið. |


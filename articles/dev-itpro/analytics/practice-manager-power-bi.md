---
title: "Power BI-efni aðferðastjórnunar"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni aðferðastjórnunar. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem eru notaðar til að búa til efnið."
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 44f017fc3460b83b730f2f7c909c6b88480dd918
ms.contentlocale: is-is
ms.lasthandoff: 12/18/2017

---

# <a name="practice-manager-power-bi-content"></a>Power BI-efni aðferðastjórnunar

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í Microsoft Power BI-efni **Aðferðarstjóri**. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

Power BI-efni **aðferðastjórnunar** var búið til fyrir aðferðastjóra og verkefnastjóra. Það veitir lykileiningarnar sem tengjast verkefnunum sem fyrirtækið er að vinna að. Á yfirlitinu má sjá yfirlit verkefna og tengdra viðskiptamanna. Afmörkun á skýrslustigi má nota til að gefa skýrslu um tilgreinda lögaðila. Þetta Power BI efni sækir gögn úr uppsöfnuðum mælingum verkbókhalds.

Power BI efnið **Aðferðastjóri** inniheldur fimm skýrslusíður: eina yfirlitssíðu og fjórar síður með upplýsingum um kostnað verks, tekjur, stjórnun áunnins virðis og stundaeiningarnar sem er skipt niður eftir ýmsum víddum.

Upphæðir í efni eru sýndar í gjaldmiðli kerfisins. Hægt er að stilla gjaldmiðil kerfis á síðunni **Kerfisfæribreytur**.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni

**Aðferðastjóri** Power BI efni er sýnt í vinnusvæðinu **Verkefnastjórnun**.


## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni

Eftirfarandi tafla veitir upplýsingar um einingarnar sem finna má á hverri síðu skýrslunnar í Power BI-efni **aðferðastjórnunar**.

| Skýrslusíða       | Einingar |
|-------------------|---------|
| Yfirlit verka | <ul><li>Stofnuð verk</li><li>Metin verk</li><li>Verk í vinnslu</li><li>Rauntekjur eftir viðskiptamanni</li><li>Fjárhagsáætlun brúttóframlegðar eftir verkum</li><li>Yfirlit yfir stjórnun áunnins virðis</li></ul> |
| Kostnaður              | <ul><li>Raunkostnaður gegn áætluðum kostnaði eftir mánuðum</li><li>Raunkostnaður gegn áætluðum kostnaði eftir árum</li><li>Raunkostnaður gegn áætluðum kostnaði eftir flokkum</li><li>Raunverulegur eftir færslugerð</li></ul> |
| Tekjur           | <ul><li>Tekjur eftir mánuði</li><li>Rauntekjur eftir póstnúmeri</li><li>Rauntekjur gegn áætluðum tekjum eftir flokkum</li><li>Rauntekjur eftir atvinnugrein viðskiptamanns</li></ul> |
| EVM               | Kostnaðarvísir og vísir fyrir áætluð afköst eftir verki |
| Tímar             | <ul><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum gegn áætluðum vinnustundum</li><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum eftir verki</li><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum eftir tilföngum</li><li>Hlutfall raunverulega rukkanlegra nýttra stunda eftir verki</li><li>Hlutfall raunverulega rukkanlegra nýttra stunda eftir tilföngum</li></ul> |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að afmarka og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Einnig má nota virknina Flytja út undirliggjandi gögn til að flytja út undirliggjandi gögn sem eru sýnd í myndrænni samantekt.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í Power BI efninu **Aðferðastjóri**. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Entity-verslunin er Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)

Í eftirfarandi hluta er fjallað um uppsafnaðar mælingar sem notaðar eru á hverja einingu.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Eining: ProjectAccountingCube\_ActualHourUtilization
**Gagnagjafi:** ProjEmplTrans

| Lykiluppsafnaðar mælingar      | Svæði                              | lýsing |
|--------------------------------|------------------------------------|-------------|
| Raunverulega rukkanlegar nýttar stundir | Samtala (ActualUtilizationBillableRate) | Samtala fyrir unnar reikningshæfar vinnustundir. |
| Raunverulega rukkanlegar álagsstundir   | Samtala (ActualBurdenBillableRate)      | Samtala fyrir verð fyrir unnar álagsstundir. |

### <a name="entity-projectaccountingcubeactuals"></a>Eining: ProjectAccountingCube\_Actuals
**Gagnagjafi:** ProjTransPosting

| Lykiluppsafnaðar mælingar | Svæði              | lýsing |
|---------------------------|--------------------|-------------|
| Rauntekjur            | Samtala (ActualRevenue) | Samtala fyrir bókaðar tekjur fyrir allar færslur. |
| Raunkostnaður               | Samtala (ActualCost)    | Samtala bókaðs kostnaðar fyrir allar færslugerðir. |

### <a name="entity-projectaccountingcubecustomer"></a>Eining: ProjectAccountingCube\_Customer
**Gagnagjafi:** CustTable

| Lykiluppsafnaðar mælingar | Svæði                                             | lýsing |
|---------------------------|---------------------------------------------------|-------------|
| Fjöldi verka        | COUNTA(ProjectAccountingCube\_Projects[PROJECTS]) | Fjöldi tiltækra verka. |


### <a name="entity-projectaccountingcubeforecasts"></a>Eining: ProjectAccountingCube\_Forecasts
**Gagnagjafi:** ProjTransBudget

| Lykiluppsafnaðar mælingar | Svæði                  | lýsing |
|---------------------------|------------------------|-------------|
| Áætlaður kostnaður               | Samtala (BudgetCost)        | Heildarkostnaðaráætlun fyrir allar færslugerðir. |
| Tekjuáætlun            | Samtala (BudgetRevenue)     | Samtala fyrir áætlaðar uppsafnaðar/reikningsfærðar tekjur. |
| Áætluð brúttóframlegð       | Samtala (BudgetGrossMargin) | Munur milli samtölu fyrir áætlaðar uppsafnaðar tekjur og samtölu fyrir áætlaðan kostnað. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Eining: ProjectAccountingCube\_ProjectPlanCostsView
**Gagnagjafi:** Verk

| Lykiluppsafnaðar mælingar | Svæði                    | lýsing |
|---------------------------|--------------------------|-------------|
| Áætlaður kostnaður              | Samtala (SumOfTotalCostPrice) | Áætlað heildarkostnaðarverð fyrir allar færslugerðir sem hafa áætluð verk. |

### <a name="entity-projectaccountingcubeprojects"></a>Eining: ProjectAccountingCube\_Projects
**Gagnagjafi:** Verk

| Lykiluppsafnaðar mælingar    | Svæði | lýsing |
|------------------------------|-------|-------------|
| Vísi kostnaðarafkomu       | ProjectAccountingCube\_Projects[Áunnið virði] ÷ ProjectAccountingCube\_Projects[heildarraunkostnaður við lokin verk] | Útreikningur á samtölu áunnins virðis deilt með heildarraunkostnaði. |
| Vísir fyrir áætluð afköst   | ProjectAccountingCube\_Projects[Áunnið virði] ÷ ProjectAccountingCube\_Projects[Áætlaður heildarkostnaður við lokin verk] | Útreikningur á samtölu áunnins virðis deilt með áætluðum heildarkostnaði. |
| Prósenta vinnu sem er lokið | Prósenta vinnu sem lokið = ProjectAccountingCube\_Projects [Heildarraunkostnaður lokinna verka] ÷ (ProjectAccountingCube\_Projects [Heildarraunkostnaður lokinna verka] + ProjectAccountingCube\_Projects [Heildar áætlaður kostnaður við verk] - ProjectAccountingCube\_Projects [Áætlaður heildarkostnaður við lokin verk]) | Heildarhlutfall lokinnar vinnu miðað við raunkostnað lokinna verka og áætlaðan kostnað verksins. |
| Hlutfall unninna reikningshæfra vinnustunda  | ProjectAccountingCube\_Projects[Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir] ÷ (ProjectAccountingCube\_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir] + ProjectAccountingCube\_Projects [Heildarfjöldi fyrir raunverulega rukkanlegar álagsstundir]) | Samtala unninna reikningshæfra vinnustunda, miðað við nýttar stundir og álagsstundir. |
| Áunnið virði                 | ProjectAccountingCube\_Projects[Áætlaður heildarkostnaður verks] × ProjectAccountingCube\_Projects[Hlutfall lokinna verka] | Áætlaður heildarkostnaður margfaldaður með hlutfalli lokinna verka. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Eining: ProjectAccountingCube\_TotalEstimatedCosts 
**Gagnagjafi:** ProjTable

| Lykiluppsafnaðar mælingar       | Svæði               | lýsing |
|---------------------------------|---------------------|-------------|
| Áætlaður kostnaður lokinna aðgerða | Samtala (TotalCostPrice) | Áætlað heildarkostnaðarverð fyrir allar færslugerðir þar sem verkum er lokið. |


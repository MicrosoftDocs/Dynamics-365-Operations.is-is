---
title: Power BI-efni aðferðastjórnunar
description: Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni aðferðastjórnunar. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem eru notaðar til að búa til efnið.
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 17a68e5aedb8b085c85d1ed7b6ad87f3eaecfc25
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685706"
---
# <a name="practice-manager-power-bi-content"></a>Power BI-efni aðferðastjórnunar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í **Aðferðastjórnun** Microsoft Power BI-efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Aðferðastjóri** Power BI-efnis var búið til fyrir aðferðastjóra og verkefnastjóra. Það veitir lykileiningarnar sem tengjast verkefnunum sem fyrirtækið er að vinna að. Á yfirlitinu má sjá yfirlit verkefna og tengdra viðskiptamanna. Afmörkun á skýrslustigi má nota til að gefa skýrslu um tilgreinda lögaðila. Þetta Power BI-efni dregur gögn úr uppsöfnuðum mælingum verkbókhalds.

**Aðferðastjóri** Power BI efnis inniheldur fimm skýrslusíður: eina yfirlitssíðu og fjórar síður með upplýsingum um kostnaður verks, tekjur, stjórnun unnins virðis og stundaeiningarnar sem eru skornar og hlutaðar í ýmsum víddum.

Upphæðir í efni eru sýndar í gjaldmiðli kerfisins. Hægt er að stilla gjaldmiðil kerfis á síðunni **Kerfisfæribreytur**.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni

**Aðferðastjóri** Power BI-efnis er sýnt í vinnusvæðinu **Verkefnastjórnun**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðar með í Power BI efni

Eftirfarandi tafla veitir upplýsingar um einingarnar sem finna má á hverri síðu skýrslunnar í **aðferðastjórnunar** Power BI-efni .

| Skýrslusíða       | Einingar |
|-------------------|---------|
| Yfirlit verka | <ul><li>Stofnuð verk</li><li>Metin verk</li><li>Verk í vinnslu</li><li>Rauntekjur eftir viðskiptamanni</li><li>Fjárhagsáætlun brúttóframlegðar eftir verkum</li><li>Yfirlit yfir stjórnun áunnins virðis</li></ul> |
| Kostnaður              | <ul><li>Raunkostnaður gegn áætluðum kostnaði eftir mánuðum</li><li>Raunkostnaður gegn áætluðum kostnaði eftir árum</li><li>Raunkostnaður gegn áætluðum kostnaði eftir flokkum</li><li>Raunverulegur eftir færslugerð</li></ul> |
| Tekjur           | <ul><li>Tekjur eftir mánuði</li><li>Rauntekjur eftir póstnúmeri</li><li>Rauntekjur gegn áætluðum tekjum eftir flokkum</li><li>Rauntekjur eftir atvinnugrein viðskiptamanns</li></ul> |
| EVM               | Kostnaðarvísir og vísir fyrir áætluð afköst eftir verki |
| Tímar             | <ul><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum gegn áætluðum vinnustundum</li><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum eftir verki</li><li>Unnar reikningshæfar vinnustundir gegn unnum reikningshæfum álagsstundum eftir tilföngum</li><li>Hlutfall raunverulega rukkanlegra nýttra stunda eftir verki</li><li>Hlutfall raunverulega rukkanlegra nýttra stunda eftir tilföngum</li></ul> |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Einnig má nota virknina Flytja út undirliggjandi gögn til að flytja út undirliggjandi gögn sem eru sýnd í myndrænni samantekt.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í **aðferðastjórnunar** Power BI efni. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar. Nánari upplýsingar er að finna í [Power BI samþætting við einingaverslun](power-bi-integration-entity-store.md).

Í eftirfarandi hluta er fjallað um uppsafnaðar mælingar sem notaðar eru á hverja einingu.

### <a name="entity-projectaccountingcube_actualhourutilization"></a>Eining: ProjectAccountingCube\_ActualHourUtilization
**Gagnagjafi:** ProjEmplTrans

| Lykiluppsafnaðar mælingar      | Svæði                              | lýsing |
|--------------------------------|------------------------------------|-------------|
| Raunverulega rukkanlegar nýttar stundir | Samtala (ActualUtilizationBillableRate) | Samtala fyrir unnar reikningshæfar vinnustundir. |
| Raunverulega rukkanlegar álagsstundir   | Samtala (ActualBurdenBillableRate)      | Samtala fyrir verð fyrir unnar álagsstundir. |

### <a name="entity-projectaccountingcube_actuals"></a>Eining: ProjectAccountingCube\_Actuals
**Gagnagjafi:** ProjTransPosting

| Lykiluppsafnaðar mælingar | Svæði              | lýsing |
|---------------------------|--------------------|-------------|
| Rauntekjur            | Samtala (ActualRevenue) | Samtala fyrir bókaðar tekjur fyrir allar færslur. |
| Raunkostnaður               | Samtala (ActualCost)    | Samtala bókaðs kostnaðar fyrir allar færslugerðir. |

### <a name="entity-projectaccountingcube_customer"></a>Eining: ProjectAccountingCube\_Customer
**Gagnagjafi:** CustTable

| Lykiluppsafnaðar mælingar | Svæði                                             | lýsing |
|---------------------------|---------------------------------------------------|-------------|
| Fjöldi verka        | COUNTA(ProjectAccountingCube\_Verkefni\[VERKEFNI\]) | Fjöldi tiltækra verka. |

### <a name="entity-projectaccountingcube_forecasts"></a>Eining: ProjectAccountingCube\_Forecasts
**Gagnagjafi:** ProjTransBudget

| Lykiluppsafnaðar mælingar | Svæði                  | lýsing |
|---------------------------|------------------------|-------------|
| Áætlaður kostnaður               | Samtala (BudgetCost)        | Heildarkostnaðaráætlun fyrir allar færslugerðir. |
| Tekjuáætlun            | Samtala (BudgetRevenue)     | Samtala fyrir áætlaðar uppsafnaðar/reikningsfærðar tekjur. |
| Áætluð brúttóframlegð       | Samtala (BudgetGrossMargin) | Munur milli samtölu fyrir áætlaðar uppsafnaðar tekjur og samtölu fyrir áætlaðan kostnað. |

### <a name="entity-projectaccountingcube_projectplancostsview"></a>Eining: ProjectAccountingCube\_ProjectPlanCostsView
**Gagnagjafi:** Verk

| Lykiluppsafnaðar mælingar | Svæði                    | lýsing |
|---------------------------|--------------------------|-------------|
| Áætlaður kostnaður              | Samtala (SumOfTotalCostPrice) | Áætlað heildarkostnaðarverð fyrir allar færslugerðir sem hafa áætluð verk. |

### <a name="entity-projectaccountingcube_projects"></a>Eining: ProjectAccountingCube\_Projects
**Gagnagjafi:** Verk

| Lykiluppsafnaðar mælingar    | Svæði | lýsing |
|------------------------------|-------|-------------|
| Vísi kostnaðarafkomu       | ProjectAccountingCube\_Verkefni\[Aflað gildi\] ÷ ProjectAccountingCube\_Verkefni\[Samtals raunverulegur kostnaður á loknum verkefni\] | Útreikningur á samtölu áunnins virðis deilt með heildarraunkostnaði. |
| Vísir fyrir áætluð afköst   | ProjectAccountingCube\_Verkefni\[Aflað gildi\] ÷ ProjectAccountingCube\_Verkefni\[Samtals áætlaður kostnaður á loknum verkefnum\] | Útreikningur á samtölu áunnins virðis deilt með áætluðum heildarkostnaði. |
| Prósenta vinnu sem er lokið | Hlutfall vinnu lokið = ProjectAccountingCube\_Verkefni\[Samtals raunverulegur kostnaður á loknum verkefnum\] ÷ (ProjectAccountingCube\_Verkefni\[Samtals raunverulegur kostnaður á loknum verkefnum\] + ProjectAccountingCube\_Verkefni\[Samtals áætlaður kostnaður verkefnis\] - ProjectAccountingCube\_Verkefni\[Samtals áætlaður kostnaður á loknum verkefnum\]) | Heildarhlutfall lokinnar vinnu miðað við raunkostnað lokinna verka og áætlaðan kostnað verksins. |
| Hlutfall unninna reikningshæfra vinnustunda  | ProjectAccountingCube\_Verkefni\[Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir\] ÷ (ProjectAccountingCube\_Verkefni\[Heildarfjöldi fyrir raunverulega rukkanlegar nýttar stundir\] + ProjectAccountingCube\_Verkefni\[Heildarfjöldi fyrir raunverulega rukkanlegar álagsstundir\]) | Samtala unninna reikningshæfra vinnustunda, miðað við nýttar stundir og álagsstundir. |
| Áunnið virði                 | ProjectAccountingCube\_Verkefni\[Samtals áætlaður kostnaður verkefnis\] × ProjectAccountingCube\_Verkefni\[Hlutfall lokinnar vinnu\] | Áætlaður heildarkostnaður margfaldaður með hlutfalli lokinna verka. |

### <a name="entity-projectaccountingcube_totalestimatedcosts"></a>Eining: ProjectAccountingCube\_TotalEstimatedCosts 
**Gagnagjafi:** ProjTable

| Lykiluppsafnaðar mælingar       | Svæði               | lýsing |
|---------------------------------|---------------------|-------------|
| Áætlaður kostnaður lokinna aðgerða | Samtala (TotalCostPrice) | Áætlað heildarkostnaðarverð fyrir allar færslugerðir þar sem verkum er lokið. |

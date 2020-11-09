---
title: Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar
description: Þetta efnisatriði veitir upplýsingar um hvernig á að ákvarða rétt stig aukakostnaðareininga og stofna reglur fyrir samantekt kostnaðar sem hæfa skýrslugerð fyrirtækis og rekjanleika kostnaðar.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy, CAMOverheadRatePolicy
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b02bfd83cfc4f1585c9044ebca8b20413042124a
ms.sourcegitcommit: d61c43b6bc04bb8786aa3c47932be0ccd84ebaeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2020
ms.locfileid: "4006167"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar 

[!include [banner](../includes/banner.md)]

Kostnaðarbókhald gerir kleift að fá innsýn í hvernig kostnaðarflæði tengist afurðum og þjónustu sem innt er af hendi innan fyrirtækis. Mikilvægt er að kostnaðarúthlutun milli kostnaðarhluta sé byggð á viðeigandi úthlutunargrunni til að kostnaður sé gagnsær. Sjálfgefið er að kostnaðarúthlutun sé á aðalkostnaðareiningu, sem er æskilegt í sumum tilvikum, en það hefur ákveðin áhrif sem hafa þarf í huga.

-   Hjálparkostnaðarhlutir hafa núllstöðu fyrir aðalkostnaðareiningar eftir útreikning á sameiginlegum kostnaði.

-   Fjöldi kostnaðarfærslna sem til verða vegna útreiknings á sameiginlegum kostnaði getur verið mjög mikill.

-   Ekki er hægt að fylgjast með kostnaðarflæði milli kostnaðarhluta.

Til að forðast það gerir kostnaðarbókhald kleift að skilgreina kostnaðarúthlutun þannig að hún passi inn í stjórnunarlegar skýrslukröfur fyrirtækisins. Þetta efnisatriði fjallar um hvernig þú getur ákvarðað rétt stig aukakostnaðareininga og stofnað reglur fyrir samantekt kostnaðar sem hæfa skýrslugerð fyrirtækis og rekjanleika kostnaðar.

> [!NOTE]
> Hægt er að breyta skilgreiningum ef skýrslukröfur breytast.

## <a name="example-of-cost-rollup-policy-setup"></a>Dæmi um uppsetningu á stefnu fyrir samantekt kostnaðar

Hugsum okkur að fyrirtæki hafi eftirfarandi uppsetningu með 4 kostnaðarstöðum.

![Dæmi um skipulag fyrirtækis](./media/dimension-hierarchy-org.png)

**Vídd kostnaðarhlutar**

| Kostnaðarstaðir | lýsing          |
|--------------|-----------|
| CC001        | Mannauður        |
| CC002        | Fjármál   |
| CC003        | Smölun  |
| CC004        | Pakkning |

**Vídd kostnaðareiningar**

| Kostnaðareiningar | lýsing | Gerð    |
|---------------|-------------|---------|
| 1001          | Rafmagn | Aðal |
| 1002          | Laun    | Aðal |
| 1003          | Auglýsingar | Aðal |

Hægt er að setja upp víddarstigveldi sem uppfyllir skýrslukröfur fyrirtækis eins og sýnt er hér.

**Upplýsingar um víddarstigveldi**

| Heiti víddarstigveldis | Vídd    | Heiti gerðar víddarstigveldis      | Stigveldi aðgangslista |
|--------------------------|--------------|------------------------------------|-----------------------|
| Fyrirtæki             | Kostnaðarstaðir | Stigveldi víddaflokkunar | Númer                    |

**Víddarstigveldi**

|    &nbsp;    | Svið víddarstaks | &nbsp;              |
|--------------|-------------------------|---------------------|
| **Hnútar**        | **Úr víddarstaki**   | **Til víddarstaks** |
| Fyrirtæki |                         |                     |
| &nbsp;&nbsp;Stjórnandi             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Fjármál              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;Mannauður               | CC002                   | CC002               |
| &nbsp;&nbsp;Framleiðsla               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkning              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Smölun             | CC004                   | CC004               |

Víddarstigveldi sem uppfyllir reglur er hægt að setja upp eins og sýnt er hér.

**Upplýsingar um víddarstigveldi**

| Heiti víddarstigveldis | Vídd     | Heiti gerðar víddarstigveldis      |
|--------------------------|---------------|------------------------------------|
| Rekstrarreikningur  | Kostnaðareiningar | Stigveldi víddaflokkunar |

**Víddarstigveldi**

|      &nbsp;             | Svið víddarstaks |      &nbsp;         |
|-------------------------|-------------------------|---------------------|
| Hnútar                   | Úr víddarstaki   | Til víddarstaks |
| Rekstrarreikningur |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Aðalkostnaður                    | 10001                   | 10003               |

Eftir að lokið hefur verið við fjárhagsfærslur lítur færslustaða kostnaðar eftir kostnaðarhlutum svona út.

|      &nbsp;          | **Kostnaðarhlutur** | &nbsp;    |  &nbsp;   |  &nbsp;   | **Samtala**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Kostnaðareining**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Rafmagn** | 100,00          | 200,00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Laun**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Auglýsingar** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Tölfræðileg vídd**

| Tölfræðilegar einingar |    lýsing   |
|----------------------|------------------|
| SE-1                 | Mannauðsþjónusta      |
| SE-2                 | Fjármálaþjónusta |

Kostnaðarhlutur CC001 HR leggur til mannauðsþjónustu til nokkurra kostnaðarhluta.

Mannauðsþjónusta er notuð samkvæmt eftirfarandi magndreifingu.

| Kostnaðarhlutur | lýsing |   Mannauðsþjónusta |
|-------------|-------------|----|
| CC002       | Fjármál     | 35 |
| CC003       | Smölun    | 55 |
| CC004       | Pakkning   | 10 |

Kostnaðarhlutur CC002 Fjármál leggur til nokkurra kostnaðarhluta.

Fjármálaþjónusta er notuð samkvæmt eftirfarandi magndreifingu.

| Kostnaðarhlutur |   lýsing    |  Fjármálaþjónusta   |
|-------------|------------------|----|
| CC003       | Smölun         | 65 |
| CC004       | Pakkning        | 35 |

Hægt er að setja upp stefnur kostnaðarúthlutunar sem hér segir.

| Stefnuheiti | lýsing     | Víddarstigveldi kostnaðarhlutar | Tölfræðileg vídd | Vídd kostnaðareiningar |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Kostnaðarúthlutun | Fyrirtæki                    | Tölfræðilegar einingar  | Kostnaðareiningar          |

Hægt er að setja upp reglur kostnaðarúthlutunar sem hér segir.

| Hnútur á víddarstigveldi kostnaðarhlutar | Kostnaðarhegðun | Úthlutunargrunnur        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Samtala         | **Mannauðsþjónusta**        |
| CC002                                | Samtala         | **Fjármálaþjónusta** |

<a name="brhow-cost-flows-between-cost-centers"></a><br>Svona flæðir kostnaður milli kostnaðarstaða 
---------------------------------------------------

Ef þú vilt vita hvernig kostnaður flæðir milli kostnaðarstaða í fyrirtækinu getur þú stofnað kostnaðareiningar af gerðinni **Auka** fyrir hvern kostnaðarstað. Þessar kostnaðareiningar verða þá notaðar til að flytja stöður milli kostnaðarstaða meðan á útreikningi á sameiginlegum kostnaði stendur.

Hægt er að setja upp víddarstök kostnaðareiningar eins og hér segir.

| Kostnaðareiningar | Gerð          |     &nbsp;    |
|---------------|---------------|---------------|
| 1001          | Rafmagn   | Aðal       |
| 1002          | Laun      | Aðal       |
| 1003          | Auglýsingar   | Aðal       |
| **SC-CC001**  | **Mannauður**        | **Auka** |
| **SC-CC002**  | **Fjármál**   | **Auka** |
| **SC-CC003**  | **Samsetning**  | **Auka** |
| **SC-CC004**  | **Pakkning** | **Auka** |

Uppfæra þarf víddarstigveldið **Rekstrarreikningur** með nýjum víddarstökum þannig að víddarstigveldið innihaldi rétt gögn sem nota má til að skilgreina skýrslugerð og stefnur.

**Upplýsingar um víddarstigveldi**

| Heiti víddarstigveldis | Vídd     | Heiti gerðar víddarstigveldis      |
|--------------------------|---------------|------------------------------------|
| Rekstrarreikningur  | Kostnaðareiningar | Stigveldi víddaflokkunar |

**Víddarstigveldi**

|      &nbsp;             | Svið víddarstaks |  &nbsp;             |
|-------------------------|-------------------------|---------------------|
| Hnútar                   | Úr víddarstaki   | Til víddarstaks |
| Rekstrarreikningur |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Aðalkostnaður                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Aukakostnaður                         | **SC-CC001**            | **SC-CC004**        |

Stofnaðu **Stefnu fyrir samantekt kostnaðar** þar sem hver kostnaðarstaður er tengdur við samsvarandi kostnaðareiningu af gerðinni **Auka**.

**Stefnur fyrir samantekt kostnaðar**

| Stefnuheiti | lýsing | Víddarstigveldi kostnaðarhlutar | Víddarstigveldi kostnaðareiningar |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Kostnaðarflæði   | Fyrirtæki                    | Rekstrarreikningur          |

**Reglur fyrir samantekt kostnaðar**

| Hnútur á víddarstigveldi kostnaðarhlutar | Hnútur á víddarstigveldi kostnaðareiningar | Aukakostnaðareining |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Rekstrarreikningur               | **SC-CC001**           |
| CC002                                | Rekstrarreikningur               | **SC-CC002**           |
| CC003                                | Rekstrarreikningur               | **SC-CC003**           |
| CC004                                | Rekstrarreikningur               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Útreikningur rekstrarkostnaðar

**Færslubók**

| Færslubók | Færslubókargerð            | Fjárhagsdagatalstímabil | Ár | Tímabil | Útgáfa       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Færslubók kostnaðarúthlutunar | Fjárhagur                 | 2017    | 1. tímabil | Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1 |

Kerfið beitir nú **Stefnu fyrir samantekt kostnaðar** þegar það stofnar **Færslubókarfærslur stöðu kostnaðarhlutar**.

**Færslubókarfærslur stöðu kostnaðarhlutar**

| Dagsetning reikningsskila | Kostnaðarhlutur | lýsing  | Kostnaðareining | lýsing |  Upphæð |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31-01-2017      | CC001       | Mannauður           | SC-CC001 | Mannauður        | 10.100,00 |
| 31-01-2017      | CC002       | Fjármál      | SC-CC002 | Fjármál   | 17.735,00 |
| 31-01-2017      | CC003       | Smölun     | SC-CC003 | Smölun  | 31.082,75 |
| 31-01-2017      | CC004       | Pakkning    | SC-CC004 | Pakkning | 15.717,25 |

> [!NOTE]
> Færslur í færslubók eru stofnaðar eftir reglunum í **Stefnu fyrir samantekt kostnaðar** ef stefna er til staðar. Staðan sem birtist er staða á útreikningi á sameiginlegum kostnaði.

Síðan **Upplýsingar um bókarfærslu fyrir kostnaðarstöðu kostnaðarhlutar** er opnuð úr færslum í færslubók og þannig er staðan fengin.

**Dæmi: Færslan fyrir kostnaðarhlutinn CC002 Fjármál**

**Upplýsingar um bókarfærslu fyrir kostnaðarstöðu kostnaðarhlutar**

| Víddarstak kostnaðareiningar | lýsing |  Upphæð   |
|-------------------------------|-------------|-----------|
| 1001                          | Rafmagn | 200,00    |
| 1002                          | Laun    | 10.000,00 |
| 1003                          | Auglýsingar | 4.000,00  |
| SC-CC001                      | Mannauður          | 3.535,00  |

**Kostnaðarfærslur myndaðar af útreikningi sameiginlegs kostnaðar**

| Kostnaðarhlutur | lýsing  | Kostnaðareining   | lýsing  |        Upphæð     |       Dagsetning reikningsskila     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | Mannauður           | SC-CC001 | Mannauður              | \-10.100,00 | 31-01-2017 |
| CC002       | Fjármál      | SC-CC001 | Mannauður              | 3.535,00    | 31-01-2017 |
| CC003       | Smölun     | SC-CC001 | Mannauður              | 5.555,00    | 31-01-2017 |
| CC004       | Pakkning    | SC-CC001 | Mannauður              | 1.010,00    | 31-01-2017 |
| CC002       | Fjármál      | SC-CC002 | Fjármál         | \-17.735,00 | 31-01-2017 |
| CC003       | Smölun     | SC-CC002 | Fjármál         | 11.527,75   | 31-01-2017 |
| CC004       | Pakkning    | SC-CC002 | Fjármál         | 6.207,25    | 31-01-2017 |

Eftir að **Útreikningur fastakostnaðar** er lokið er hægt tilkynna um niðurstöðuna með því að nota verkfæri á borð við Microsoft SharePoint vinnusvæði, Excel eða Power BI.

## <a name="view-reporting-in-excel"></a>Skoða skýrslugerð í Excel 

Víddarstigveldi gera þér kleift að sjá gögn á mismunandi flokkunarstigum.

Hér er dæmi um Power Pivot skýrslugjöf í Excel.

| **Rekstrarreikningur** | **Kostnaðarhlutur** |      &nbsp;    |   &nbsp;      |     &nbsp;    |  **Samtala**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Aðalkostnaður**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| &nbsp;&nbsp;&nbsp;&nbsp;1001                            | 100,00          | 200,00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**Aukakostnaður**                            | **-10.100,00**  | **-14.200,00** | **17.082.75** | **7.217,25**  | **0.00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | \-10.100,00     | 3.535,00       | 5.555,00      | 1.010,00      | **0.00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | \-17.735,00    | 11.527,75     | 6.207,25      | **0.00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **Samtala**                   | **0.00**        | **0.00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Með því að nota **Stefnu fyrir samantekt kostnaðar** og **Kostnaðareiningu af aukagerð** getur þú gert aðalkostnað á kostnaðarhlut fyrir innri skýrslugerð að aðalkostnaði sem er eftirstandandi eftir **Útreikning á sameiginlegum kostnaði**.

Ef það sama hefði verið framkvæmt án þess að stofna **Stefnu fyrir samantekt kostnaðar** myndu niðurstöður líta svona út. Kostnaður flæðir réttilega en rekjanleiki og innsæi í það hvernig kostnaður flæðir milli kostnaðarstaða glatast.

| **Rekstrarreikningur** | **Kostnaðarhlutur** |   &nbsp;  |    &nbsp;     |  &nbsp;       |          **Samtala**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Aðalkostnaður**            | **0.00**        | **0.00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1001                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Aukakostnaður**                            | **0.00**        | **0.00**  | **0.00**      | **0.00**      | **0.00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0.00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0.00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **Samtala**                   | **0.00**        | **0.00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Kröfur um skýrslugerð og rekjanleika segja til um hvernig þú getur ákvarðað rétt stig aukakostnaðareininga og stofnað reglur fyrir samantekt kostnaðar sem uppfylla þarfir þínar.

Skýr aðgreining milli **Kostnaðarúthlutunar** og **Stefnu fyrir samantekt kostnaðar** veitir sveigjanleikann til að framkvæma samfelldar uppfærslur án þess að þær hafi áhrif sín á milli.



## <a name="additional-resources"></a>Frekari upplýsingar
-  [Víddir kostnaðarhlutar](cost-objects.md)
-  [Víddir kostnaðareiningar](cost-elements.md)
-  [Víddarstigveldi](dimension-hierarchy.md)
-  [Útreikningur fastakostnaður](overhead-calculation.md)

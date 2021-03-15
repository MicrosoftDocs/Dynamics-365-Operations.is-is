---
title: Úrræðaleit vandamála vegna uppfærslna Finance and Operations forrita
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem tengjast uppfærslu á forritum Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131222"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Úrræðaleit vandamála vegna uppfærslna Finance and Operations forrita

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast uppfærslu á forritum Finance and Operations.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="database-synchronization-errors"></a>Villur í gagnagrunnssamstillingu

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið villuboð sem líkjast eftirfarandi dæmi þegar þú reynir að nota töfluna **DualWriteProjectConfiguration** til að uppfæra forrit Finance and Operations í verkvangs uppfærslu 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.
2. Opnaðu Visual Studio sem stjórnandi og opnaðu hugbúnaðarhlutatré (AOT).
3. Leita að **DualWriteProjectConfiguration**.
4. I AOT hægrismellirðu á **DualWriteProjectConfiguration** og velur **Bæta við nýtt verkefni**. Veldu **Í lagi** til að búa til nýja verkið sem notar sjálfgefna valkosti.
5. Í Solution Explorer hægrismellirðu á **Eiginleikar verks** og stillir **Samstilla gagnagrunn á uppbyggingu** á **True**.
6. Smíðaðu verkefnið og staðfestu að smíðin heppnaðist.
7. Í valmyndinni **Dynamics 365** velurðu **Samstilla gagnagrunn**.
8. Veldu **Samstilla** til að gera fulla samstillingu gagnagrunnsins.
9. Eftir að samstilling gagnagrunnsins hefur náðst að fullu skaltu endurtaka samstillingu gagnagrunnsins Microsoft Dynamics Lifecycle Services (LCS) og notaðu handvirka uppfærsluhandritin eftir því sem við á, svo þú getir haldið áfram með uppfærsluna.

## <a name="missing-table-columns-issue-on-maps"></a>Vandamál með töfludálka sem vantar á kort

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Á síðunni **Tvöfalt skrif** gætirðu fengið villuboð sem líkjast eftirfarandi dæmi:

*Upprunareitur sem vantar \<field name\> í skemanu.*

![Dæmi um villuboð vantar upprunadálk](media/error_missing_field.png)

Til að laga málið skaltu fyrst fylgja þessum skrefum til að ganga úr skugga um að dálkarnir séu í töflunni.

1. Skráðu þig inn á VM fyrir forrit Finance and Operations.
2. Opnaðu **Vinnusvæði \> Gagnastjórnun**, veldu reitinn **Færibreytur ramma** og síðan á flipanum **Töflustillingar** skaltu velja **Uppfæra töflulista** til að uppfæra töflurnar.
3. Opnaðu **Vinnusvæði \> Gagnastjórnun**, veldu flipann **Gagnatöflur** og gakktu úr skugga um að taflan sé skráð. Ef taflan er ekki skráð skaltu skrá þig inn á VM fyrir forrit Finance and Operations og ganga úr skugga um að taflan sé tiltæk.
4. Opnaðu síðuna **Vörpun töflu** á síðunni **Tvöföld skráning** í Finance and Operations -forritinu.
5. Veldu **Uppfæra töflulista** til að fylla sjálfkrafa út reitina í töfluvörpunum.

Ef málið er enn ekki lagað skaltu fylgja þessum skrefum.

> [!IMPORTANT]
> Þessi skref leiðbeina þér í gegnum ferlið við að eyða töflu og bæta henni síðan við aftur. Vertu viss um að fylgja leiðbeiningunum nákvæmlega til að forðast vandamál.

1. Í Finance and Operations -forritinu skal opna **Vinnusvæði \> Gagnastjórnun** og velja reitinn **Gagnatöflur**.
2. Finnið töfluna sem vantar eigindina. Smelltu á **Breyta markvörpun** á tækjastikunni.
3. Á **Varpa sviðsetningu á mark** svæðinu skaltu smella á **Búa til vörpun**.
4. Opnaðu síðuna **Vörpun töflu** á síðunni **Tvöföld skráning** í Finance and Operations -forritinu.
5. Ef vörpunin býr ekki sjálfkrafa til eigindina skaltu bæta henni við með því að smella á **Bæta við eigind** hnappinn og svo **Vista**. 
6. Veldu vörpunina og smelltu á **Keyra**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
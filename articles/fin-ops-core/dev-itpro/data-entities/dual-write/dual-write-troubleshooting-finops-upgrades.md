---
title: Leysaðu vandamál vegna uppfærslu á fjármála- og rekstrarforritum
description: Þessi grein veitir upplýsingar um úrræðaleit sem geta hjálpað þér að laga vandamál sem tengjast uppfærslu á fjármála- og rekstrarforritum.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b75034cbc8ca7a24472cfec1ad93d3dfef4a8fdc
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111141"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Leysaðu vandamál vegna uppfærslu á fjármála- og rekstrarforritum

[!include [banner](../../includes/banner.md)]





Þessi grein veitir upplýsingar um bilanaleit fyrir samþættingu tvískrifa milli fjármála- og rekstrarforrita og Dataverse. Nánar tiltekið veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast uppfærslu á fjármála- og rekstrarforritum.

> [!IMPORTANT]
> Sum vandamálin sem þessi grein fjallar um gætu þurft annað hvort kerfisstjórahlutverkið eða Microsoft Azure Active Directory (Azure AD) leigjanda stjórnanda skilríki. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="database-synchronization-errors"></a>Villur í gagnagrunnssamstillingu

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið villuboð sem líkjast eftirfarandi dæmi þegar þú reynir að nota **DualWriteProjectConfiguration** töflu til að uppfæra fjármála- og rekstrarapp í pallauppfærslu 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Skráðu þig inn á sýndarvélina (VM) fyrir fjármála- og rekstrarappið.
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

![Dæmi um villuboð vegna upprunadálks sem vantar.](media/error_missing_field.png)

Til að laga málið skaltu fyrst fylgja þessum skrefum til að ganga úr skugga um að dálkarnir séu í töflunni.

1. Skráðu þig inn á VM fyrir fjármála- og rekstrarappið.
2. Opnaðu **Vinnusvæði \> Gagnastjórnun**, veldu reitinn **Færibreytur ramma** og síðan á flipanum **Töflustillingar** skaltu velja **Uppfæra töflulista** til að uppfæra töflurnar.
3. Opnaðu **Vinnusvæði \> Gagnastjórnun**, veldu flipann **Gagnatöflur** og gakktu úr skugga um að taflan sé skráð. Ef taflan er ekki skráð skaltu skrá þig inn á VM fyrir fjármála- og rekstrarappið og ganga úr skugga um að taflan sé tiltæk.
4. Opnaðu **Taflakortlagning** síðu frá **Tvöfalt skrifa** síðu í fjármála- og rekstrarappinu.
5. Veldu **Uppfæra töflulista** til að fylla sjálfkrafa út reitina í töfluvörpunum.

Ef málið er enn ekki lagað skaltu fylgja þessum skrefum.

> [!IMPORTANT]
> Þessi skref leiðbeina þér í gegnum ferlið við að eyða töflu og bæta henni síðan við aftur. Vertu viss um að fylgja leiðbeiningunum nákvæmlega til að forðast vandamál.

1. Í fjármála- og rekstrarappinu skaltu fara á **Vinnurými \> Gagnastjórnun**, og veldu **Gagnatöflur** flísar.
2. Finnið töfluna sem vantar eigindina. Smelltu á **Breyta markvörpun** á tækjastikunni.
3. Á **Varpa sviðsetningu á mark** svæðinu skaltu smella á **Búa til vörpun**.
4. Opnaðu **Taflakortlagning** síðu frá **Tvöfalt skrifa** síðu í fjármála- og rekstrarappinu.
5. Ef vörpunin býr ekki sjálfkrafa til eigindina skaltu bæta henni við með því að smella á **Bæta við eigind** hnappinn og svo **Vista**. 
6. Veldu vörpunina og smelltu á **Keyra**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

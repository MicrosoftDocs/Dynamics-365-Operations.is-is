---
title: Úrræðaleit vandamál sem tengjast uppfærslu á forritum Finance and Operations
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172878"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Úrræðaleit vandamál sem tengjast uppfærslu á forritum Finance and Operations

[!include [banner](../../includes/banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast uppfærslu á forritum Finance and Operations.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="database-synchronization-errors"></a>Villur í gagnagrunnssamstillingu

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið villuboð sem líkjast eftirfarandi dæmi þegar þú reynir að nota eininguna **DualWriteProjectConfiguration** til að uppfæra forrit Finance and Operations í verkvangs uppfærslu 30.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
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

## <a name="missing-entity-fields-issue-on-maps"></a>Reitir sem vantar einingar á kortum

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Á síðunni **Tvöfalt skrif** gætirðu fengið villuboð sem líkjast eftirfarandi dæmi:

*Upprunasvið vantar \<reitnafn\> í skemanu.*

![Dæmi um villuboð vantar upprunasvið](media/error_missing_field.png)

Til að laga málið, fylgdu fyrst þessum skrefum til að ganga úr skugga um að reitirnir séu í einingunni.

1. Skráðu þig inn á VM fyrir forrit Finance and Operations.
2. Farðu í **Vinnusvæði \> Gagnastjórnun**, veldu reitinn **Rammafæribreytur** og síðan, á flipanum **Einingarstillingar**, velurðu **Uppfæra einingalista** til að endurræsa einingarnar.
3. Farðu í **Vinnusvæði \> Gagnastjórnun**, veldu flipann **Gagnaeiningar** og gakktu úr skugga um að einingin sé skráð. Ef einingin er ekki skráð skaltu skrá þig inn á VM fyrir forrit Finance and Operations og gakktu úr skugga um að einingin sé tiltæk.
4. Opnaðu síðuna **Vörpun eininga** af síðunni **Tvöfalt skrif** í forriti Finance and Operations.
5. Veldu **Uppfæra einingalista** til að fylla sjálfkrafa reitina í vörpunum eininga.

Ef málið er enn ekki lagað skaltu fylgja þessum skrefum.

> [!IMPORTANT]
> Þessi skref leiðbeina þér í gegnum ferlið við að eyða einingu og bæta henni síðan við aftur. Vertu viss um að fylgja leiðbeiningunum nákvæmlega til að forðast vandamál.

1. Í forriti Finance and Operations ferðu í **Vinnusvæði \> Gagnastjórnun** og velur reitinn **Gagnaeiningar**.
2. Finndu eininguna sem vantar reitinn. Skrifaðu mið af einingunni, stigatöflu, heiti einingarinnar og öðrum dálkagildum.
3. Ef einhver af vinnsluhópunum þínum er háður þessari einingu, gerðu viðeigandi ráðstafanir fyrir vinnsluhópana áður en þú eyðir einingunni.
4. Eyddu einingunni sem vantar reitinn.
5. Veldu **Nýtt** og bættu einingunni aftur við. Tilgreindu gildin sem þú tókst eftir í skrefi 2.
6. Opnaðu síðuna **Vörpun eininga** af síðunni **Tvöfalt skrif** í forriti Finance and Operations.
7. Veldu **Uppfæra einingalista** til að fylla sjálfkrafa reitina í vörpunum eininga.

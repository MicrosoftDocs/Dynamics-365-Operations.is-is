---
title: Fjöldalokun fjárhagstímabils
description: Þetta efni fer í gegnum hvernig setja skal tímabil á bið eða loka varanlega tímabili eða meira en einn lögaðila í einu.
author: aprilolson
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54a5b16f731e850b468ea2e05e47b47774e45838
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826499"
---
# <a name="mass-financial-period-close"></a>Fjöldalokun fjárhagstímabils

[!include [banner](../../includes/banner.md)]

Þetta efni fer í gegnum hvernig setja skal tímabil á bið eða loka varanlega tímabili eða meira en einn lögaðila í einu. Þar að auki sýnir verkið hvernig á að takmarka bókun notandaflokks í ákveðnar kerfiseiningar.

1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Lok tímabils > Dagbækur fjárhags**. Athugið að lista yfir lögaðila sem birt er háð fjárhagsdagatalinu sem var valin á síðunni. Aðeins lögaðila sem nota valið fjárhagsdagatal birtast.
2. Veljið **Breyta**.
3. Velja tímabil sem ætlunin er að breyta stöðu fyrir.
4. Velja lögaðilar sem ætlunin er að Uppfæra stöðu fyrir. Hægt er að velja alla lögaðila fljótt með því að velja gátmerki efst vinstra megin á hnitanetinu.  
5. Veldu **Uppfæra aðgang kerfiseiningar** til að skilgreina bókunaraðgang að valinni einingu. Stöðu kerfiseiningar má einnig uppfæra eina í einu með því að breyta færslum í hnitanetinu. Hnappurinn er gagnleg þegar á að uppfæra margar færslur lögaðila á skjótan hátt.  
6. Í einingunni **Forrit** skaltu velja eininguna sem þú vilt að uppfæri stöðuna. Smellið á **Velja**.
7. Í stiginu **Aðgangur** skal velja **Allt**, **Ekkert** eða tiltekinn notendaflokk. Smellið á **Velja**. Allar tilgreinir að allir notendur með breytingaaðgang að kerfið geti bókað ef tímabilið er opið. Ekkert tilgreinir að notendur geta ekki bókað í kerfinu ef tímabilið er opið. Ákveðinn notendaflokkur gefur til kynna að aðeins notendur í flokknum geti bókað í kerfiseininguna ef tímabilið er opið.  
8. Veldu **Uppfæra**.
9. Veljið annað tímabil til að uppfæra stöðu.
10. Velja lögaðilar sem ætlunin er að Uppfæra stöðu tímabils fyrir.
11. Veldu **Uppfæra stöðu tímabils** og stilltu stöðuna **Á bið**, **Opið** eða **Endanlega lokað**. **Opið** tilgreinir að hægt er að bóka á tímabilið, að því tilskildu að notandi hafi aðgang. **Á bið** þýðir að ekki er hægt að bóka á tímabilið en hægt er að enduropna tímabilið. **Endanlega lokað** þýðir að tímabilið er lokað og að aldrei er hægt að opna það aftur. Ekki er hægt að bóka í leiðrétting. Ekki er ráðlagt að stilla tímabil sem **Endanlega lokað** fyrr en öllum leiðréttingum og endurskoðunum er lokið.  
12. Veldu **Uppfæra**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
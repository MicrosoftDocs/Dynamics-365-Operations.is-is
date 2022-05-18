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
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0acaad0d6e89fe7c81537e554b36ffb210e5abad
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722067"
---
# <a name="mass-financial-period-close"></a>Fjöldalokun fjárhagstímabils

[!include [banner](../../includes/banner.md)]

Þetta efni fer í gegnum hvernig setja skal tímabil á bið eða loka varanlega tímabili eða meira en einn lögaðila í einu. Þar að auki sýnir verkið hvernig á að takmarka bókun notandaflokks í ákveðnar kerfiseiningar.

1. Í yfirlitsrúðunni, farðu í **Fjárhagsbók > Lokun tímabils > Fjárhagsdagatöl**. Athugið að lista yfir lögaðila sem birt er háð fjárhagsdagatalinu sem var valin á síðunni. Aðeins lögaðila sem nota valið fjárhagsdagatal birtast.
2. Veljið **Breyta**.
3. Velja tímabil sem ætlunin er að breyta stöðu fyrir.
4. Velja lögaðilar sem ætlunin er að Uppfæra stöðu fyrir. Hægt er að velja alla lögaðila fljótt með því að velja gátmerki efst vinstra megin á hnitanetinu.  
5. Veldu **Uppfæra aðgang kerfiseiningar** til að skilgreina bókunaraðgang að valinni einingu. Stöðu kerfiseiningar má einnig uppfæra eina í einu með því að breyta færslum í hnitanetinu. Hnappurinn er gagnleg þegar á að uppfæra margar færslur lögaðila á skjótan hátt.  
6. Í einingunni **Forrit** skaltu velja eininguna sem þú vilt að uppfæri stöðuna. Smellið á **Velja**.
7. Í stiginu **Aðgangur** skal velja **Allt**, **Ekkert** eða tiltekinn notendaflokk. Smellið á **Velja**.  
- **Allt** - allir notendur með breytingaaðgang að einingunni geta sent inn ef tímabilið er opið. 
- **Enginn** - notendur geta ekki sent inn á eininguna ef tímabilið er opið. Ákveðinn notendaflokkur gefur til kynna að aðeins notendur í flokknum geti bókað í kerfiseininguna ef tímabilið er opið.  
8. Veldu **Uppfærsla**, 
9. Veljið annað tímabil til að uppfæra stöðu.
10. Velja lögaðilar sem ætlunin er að Uppfæra stöðu tímabils fyrir.
11. Veldu **Uppfæra stöðu tímabils** og stilltu stöðuna **Á bið**, **Opið** eða **Endanlega lokað**. **Opið** tilgreinir að hægt er að bóka á tímabilið, að því tilskildu að notandi hafi aðgang. **Á bið** þýðir að ekki er hægt að bóka á tímabilið en hægt er að enduropna tímabilið. **Endanlega lokað** þýðir að tímabilið er lokað og að aldrei er hægt að opna það aftur. Ekki er hægt að bóka í leiðrétting. Ekki er ráðlagt að stilla tímabil sem **Endanlega lokað** fyrr en öllum leiðréttingum og endurskoðunum er lokið.  
12. Veldu **Uppfæra**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

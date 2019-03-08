---
title: Fjöldalokun fjárhagstímabils
description: Þessi verklýsing fer í gegnum hvernig setja skal tímabil á bið eða loka varanlega tímabili eða meira en einn lögaðila í einu.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "311382"
---
# <a name="mass-financial-period-close"></a>Fjöldalokun fjárhagstímabils

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing fer í gegnum hvernig setja skal tímabil á bið eða loka varanlega tímabili eða meira en einn lögaðila í einu. Þar að auki sýnir verkið hvernig á að takmarka bókun notandaflokks í ákveðnar kerfiseiningar.

1. Fara í Fjárhag > Loka tímabili > Dagatal fjárhags.
    * Athugið að lista yfir lögaðila sem birt er háð fjárhagsdagatalinu sem var valin á síðunni. Aðeins lögaðila sem nota valið fjárhagsdagatal birtast.  
2. Smellið á „Breyta“.
3. Velja tímabil sem ætlunin er að breyta stöðu fyrir.
4. Velja lögaðilar sem ætlunin er að Uppfæra stöðu fyrir.
    * Hægt er að velja alla lögaðila fljótt með því að velja gátmerki efri vinstra megin á hnitanetinu.  
5. Velja uppfæra kerfiseiningu til að skilgreina bókunaraðgang að valinni einingu.
    * Stöðu kerfiseiningar má einnig uppfæra eina í einu með því að breyta færslum í hnitanetinu. Hnappurinn er gagnleg þegar á að uppfæra margar færslur lögaðila á skjótan hátt.  
6. Veldu einingu sem þú vilt að uppfæri stöðuna í einungu forrits. Smellið á Velja.
7. Í Aðgangsstig skal velja Allt, Ekkert eða tiltekinn notendaflokkinn. Smellið á Velja.
    * Allar tilgreinir að allir notendur með breytingaaðgang að kerfið geti bókað ef tímabilið er opið. Ekkert tilgreinir að notendur geta ekki bókað í kerfinu ef tímabilið er opið. Ákveðinn notendaflokkur gefur til kynna að aðeins notendur í flokknum geti bókað í kerfiseininguna ef tímabilið er opið.  
8. Smelltu á Uppfæra.
9. Veljið annað tímabil til að uppfæra stöðu.
10. Velja lögaðilar sem ætlunin er að Uppfæra stöðu tímabils fyrir.
11. Veldu að uppfæra stöðu tímabils og stilltu stöðuna Á bið, eða Endanlega lokað.
    * Opna tilgreinir að hægt er að bóka á tímabilið, að því tilskildu að notandi hafi aðgang. Á bið þýðir að ekki er hægt að bóka á tímabilið en hægt er að enduropna tímabilið. Endanlega lokað þýðir að tímabilið er lokað og að aldrei er hægt að opna það aftur. Ekki er hægt að bóka í leiðrétting. Ekki er ráðlagt að stilla tímabil sem varanlega lokað fyrr en öllum leiðréttingum og endurskoðunum er lokið.  
12. Smelltu á Uppfæra.


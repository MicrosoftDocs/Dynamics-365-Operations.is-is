---
title: "kerfisskilgreindar og notandaskilgreindar taflaskorður."
description: "Þessi grein útskýrir hinar tvær tegundir töfluskorða fyrir íhluti í skilgreiningarlíkani afurðar: Skilgreint af notanda og skilgreint af kerfi. Töfluskorður standa fyrir fylki leyfðra eigindasamsetninga þar sem hver röð skilgreinir eitt safn mögulegra eigindagilda."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 0393c52c9128eb975c26b67323046a289872c4b0
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="system-defined-and-user-defined-table-constraints"></a>kerfisskilgreindar og notandaskilgreindar taflaskorður.

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir hinar tvær tegundir töfluskorða fyrir íhluti í skilgreiningarlíkani afurðar: Skilgreint af notanda og skilgreint af kerfi. Töfluskorður standa fyrir fylki leyfðra eigindasamsetninga þar sem hver röð skilgreinir eitt safn mögulegra eigindagilda.

Töfluskorður tákna fylki samsetninga eiginds sem  eru leyfðar fyrir íhluti í afbrigðalíkani afurðar. Hver lína í töflunni skilgreinir eitt safn mögulegra eigindagilda. Hægt er að telja fram tvær gerðir skorða í afbrigðalíkani afurðar:

-   **Segðarskorða** – Stofna segð sem skilgreinir vensl milli eiginda til að tryggja að hægt er að velja aðeins samhæf gildi við skilgreiningu afurðar.
-   **Töfluskorða** – Búa til töflu sem skilgreinir allar samsetningar sem eru leyfðar fyrir tilgreint safn eiginleika. Tvær gerðir af töfluskorðum eru tiltækar: notandaskilgreindur töfluskorðum og kerfisskilgreindar töfluskorðum.

Þessi skrá lýsir notandaskilgreindur og kerfisskilgreindar töfluskorðum fyrir íhluti í afbrigðalíkani afurðar.

## <a name="user-defined-table-constraints"></a>Notandaskilgreind töfluskorða
Notandaskilgreind töfluskorða er gerð fylkis sem má nota til að lýsa samsetningu fyrir eigindagildin sem eru skilgreind í eigindagerðum. Til dæmis, ef þú framleiðir hátalara geturðu haft með dálk fyrir áferð hússins og framgrillið í notandaskilgreindu töfluskorðunni. Gerð eigindar fyrir áferð hússins hefur fjögur gildi og eigindargerð fyrir framgrill hefur þrjú gildi. Þess vegna ef ekki eru notuð skorður eru 4 × 3 = 12 mögulegar samsetningar. Hins vegar í þessu dæmi eru aðeins sex samsetningar leyfðar, eins og sýnt er í eftirfarandi töflu. Þessar upplýsingar birtast í á **Leyfðar samsetningar** flipanum á í **Breyta töfluskorðu** síðu.

| Ljúka cabinet | Framgrill |
|----------------|-------------|
| Svart          | Svart       |
| Svart          | Málmur       |
| Eik            | Svart       |
| Rósaviður       | Hvítt       |
| Hvítt          | Svart       |
| Hvítt          | Hvítt       |

Notandaskilgreind töfluskorðum eru skilgreindar eftir ílag fastrar töflu sem vinnur á sama hátt og segðarskorða. Þegar notendaskilgreinda töfluskorðu er notuð, er kosturinn að töflur eru oft auðveldara að stofna, skilja og viðhalda en langar segðarskorður.

## <a name="system-defined-table-constraints"></a>kerfisskilgreindar töfluskorður
Kerfisskilgreind töfluskorða stpfmar gagnvirkri vörpun á milli gerð eigindar og svæðis í töflu. Þegar kerfisskilgreindar töfluskorða er höfð með í afbrigðalíkani afurðar tryggir vörpun að gögn í töflunni er sýnd í stað gilda fyrir gerð eigindar. Niðurstaðan er breytileg töfluskorða þar sem hægt er að breyta innihaldi töflu (til dæmis, með öðrum kerfum).  

Þegar-kerfisskilgreindrar töfluskorðu er stofnuð er velja töflu, einnig er hægt að skilgreina fyrirspurn til að nota og tengja svo gerðir eiginda í svæði í valinni töflu. Gerðir svæða verður að samsvara gerðum gerða eiginda.  

Áður en töfluskorðu getur tekið gildi í afbrigðalíkani afurðar, verður töfluskorðunni að vera innifalin í skorðu í einum af íhlutum líkans. Ferlið er að stofna nýja skorðu, velja gerð töfluskorðu og veljið síðan skilgreiningu töfluskorðu sem nota á. Loks, öll svæði í töfluskorðunni verða að varpa eigindum í afbrigðalíkani afurðar.

<a name="see-also"></a>Sjá einnig
--------

[Lykilhugtök í afbrigðalíkan afurðar](product-configuration-models.md)





---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (7. febrúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 002dcd8253a0ab753ac9002e7027441db6d0b858
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461539"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (7. febrúar 2019)

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="interview-scheduling-enhancements"></a>Endurbætur á viðtalsáætlun
Endurbætur hafa verið gerðar á allri upplifun viðtalsáætlunar. Þú getur nú séð lausa tíma á dagatali fyrir umsækjanda innan fyrirtækisins og notað dagatalið hans til að stinga upp á tímasetningu. Nánari upplýsingar er að finna í [Viðtalsáætlun og endurgjöf](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Starfsauglýsing á LinkedIn - skekkja fyrirtækis lagfærð
Vandamál hefur verið lagað þar sem störf auglýst á LinkedIn úr Attract birtust undir röngu fyrirtækisheiti. Nánari upplýsingar er að finna í [Búðu til, samþykkja og auglýsa störf í Attract](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Vefslóð starfatorgsins sýnd í stjórnandastillingum
Vefslóð á heimasíðu starfatorgsins er nú sýnd í **Stjórnandastillingar** undir **Stjórnun starfatorgs**.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

**Smíði 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Mörg launastig studd í störfum
Þessi breyting gerir kleift að skilgreina fleiri en eitt launastig í starfi, sem virkjar bil á föstum launum starfsmanns sem kunna að vera mismunandi milli áætlana þegar sama starfið er notað. 

Dæmi:    
*Starf* - Kerfisstjóri *Tengd launastig:* B1 og B2 - Hvert stig er með skilgreint bil fyrir gildin. B1 = Min 50.000, Mid 60.000, Max 75.000 og B2 = Min 65.000, Mid 74.000, Max 85.000. Þegar föst laun eru búin til fyrir starfsmenn, byggt á skilgreindum hæfnisreglum, getur sérhver föst laun nú bent á sama starfið og mismunandi stig starfsins. Þetta leyfir skilgreiningar á áætlunum á mismunandi svæðum/fyrirtækjum og að benda á sama starfið, en mismunandi bil, án þess að afrita störfin til að gera grein fyrir þessum mismun.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Svæði fyrir launastig hefur verið bætt við eininguna fyrir föst laun starfsmanns 
Með þessari uppfærslu hefur einingin fyrir föst laun starfsmanns verið uppfærð til að innihalda svæðið **Launastig**. Þessi viðbót gerir það auðveldara að uppfæra fyrirkomulag fastra launa starfsmanns. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Uppfærðu starfasafn þegar nýjar stöður eru uppfærðar eða búnar til
Þegar starfi er breytt fyrir stöðu, verður **Starfasafn** nú fá sjálfgildi byggt á völdu starfi.

### <a name="performance-improvements-when-rendering-workspaces"></a>Bætt afköst þegar vinnusvæði birtast
Greiningarflipar á vinnusvæðum munu nú eingöngu hlaðast þegar þessar síður eru opnaðar. Vísir birtist meðan á fyrstu birtingu á síðunni efst í vinstra horni síðunnar.
